# Examen

## Nombre Pattern Design: Observer

Usar observer para el modo de esperar a que se realize un pago para poder enviarlo a cada uno de los 
servicios en el cual se podrá reproducir el streaming de la canción, en este caso el observer tendrá 
como suscriptores a los servicios de Youtube, Spotify, Amazon Music y Apple Music, cuando el observador 
principal les envie la notificacion de que el estado de pago cambio, el suscriptor que tenga un true 
en su estado de pago podra hacer match y continuaria el servicio de streaming.

En este caso, cuando uno de los servicios devuelva true los demás ya estarán notificados y no tendrán
que continuar en modo "observer", unicamente el principal, si el estado vuelve a cambiar, puede volver
a mandar una notificación para a visar a los demás que el estado cambio y volverá a empezar la espera
del pago.

![alt text](https://github.com/samsaavel/liquids_examen/blob/master/pattern/IMG_20190228_180420097.jpg)