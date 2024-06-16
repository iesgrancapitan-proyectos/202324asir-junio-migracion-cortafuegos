Marcos Cáceres García

Implementación de alta disponibilidad WAN en calisto

Índice

1. [**Añadimos la NIC.................................................................................................................3**](#_page2_x72.00_y72.00)
1. [**Configuración de interfaz..................................................................................................4**](#_page3_x72.00_y72.00)
1. [**Creación de los Gateway...................................................................................................5**](#_page4_x72.00_y72.00)
1. [**Creación de reglas firewall................................................................................................7**](#_page6_x72.00_y72.00)

<a name="_page2_x72.00_y72.00"></a>1.Añadimos la NIC

Para añadir nuestra tarjeta de red debemos situarnos en la pestaña de hardware y seleccionamos añadir:

![](Aspose.Words.5cbb4429-ef4b-41f3-b27e-c67f9d2a32ab.001.png)

Seleccionamos Network Device y una vez allí seleccionamos en el desplegable la NIC que queremo añadir, en mi caso la de Andared:

![](Aspose.Words.5cbb4429-ef4b-41f3-b27e-c67f9d2a32ab.002.jpeg)

Una vez añadida la NIC ya podemos disponernos a entrar en nuestro firewall y configurar dicha interfaz.

<a name="_page3_x72.00_y72.00"></a>2.Configuración de interfaz.

Al igual que ocurre con el laboratorio que monté, debemos de asignar las interfaces a las NIC, así que nos disponemos en interfaces > assigment y quedarán de la siguiente manera:

![](Aspose.Words.5cbb4429-ef4b-41f3-b27e-c67f9d2a32ab.003.jpeg)

La interfaz queda configurada con la IP, DNS y gateway necesarios según se me pide en mi paquete de trabajo:

![](Aspose.Words.5cbb4429-ef4b-41f3-b27e-c67f9d2a32ab.004.jpeg)

<a name="_page4_x72.00_y72.00"></a>3.Creación de los Gateway.

Ahora debemos de crear una Gateway nueva para nuestra interfaz ANDARED, para ello nos situamos en System > Routing > Gateway, y ahí creamos las Gateway según se pide en el paquete de trabajo:

![](Aspose.Words.5cbb4429-ef4b-41f3-b27e-c67f9d2a32ab.005.jpeg)

Una vez creadas las interfaces debemos de configurar el grupo de gateway, dicho grupo nos servirá más tarde para configurar el balanceo de carga entre ambas interfaces la de informática y la de andared, para ello vamos a gateway groups y establecemos la siguiente configuración:

![](Aspose.Words.5cbb4429-ef4b-41f3-b27e-c67f9d2a32ab.006.jpeg)

![](Aspose.Words.5cbb4429-ef4b-41f3-b27e-c67f9d2a32ab.007.jpeg)

<a name="_page6_x72.00_y72.00"></a>4.Creación de reglas firewall.

Ahora debemos de crear las reglas que obligarán a al tráfico de la LAN a circular por el grupo de gateway, para ello nos disponemos a firewall > rules y creamos la siguiente regla:

![](Aspose.Words.5cbb4429-ef4b-41f3-b27e-c67f9d2a32ab.008.jpeg)

![](Aspose.Words.5cbb4429-ef4b-41f3-b27e-c67f9d2a32ab.009.jpeg)Como se puede ver hace que todo el tráfico saliente de la LAN sea obligado a circular por el grupo de gateway.

Quedando de la siguiente manera, es importante ponerla la primera de todas ya que las reglas están ordenadas por orden de prioridad:

![](Aspose.Words.5cbb4429-ef4b-41f3-b27e-c67f9d2a32ab.010.jpeg)
8
