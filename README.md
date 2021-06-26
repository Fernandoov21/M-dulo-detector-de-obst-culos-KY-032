# Modulo-KY-032

#**¿Que es el modeulo KY-032?**

Este sensor infrarrojo posee la habilidad de evitar obstáculos al devolver una señal cuando detecta un obstáculo dentro de su rango de medición (entre 2-40 cm). Este módulo dispone de 4 pines, lo que le permite habilitar/deshabilitar la detección. Este dispositivo tiene un emisor y un receptor infrarrojo que permite la detección. El emisor genera una señal que rebota sobre el obstáculo y que superado un cierto nivel ajustable mediante dos potenciómetros (uno para determinar el nivel umbral a partir del cual se detecta y el otro para modificar la frecuencia de emisión del transmisor).
Por sus dimensiones este módulo es perfecto para proyectos mini sumo. Es compatible con tarjetas que manejen un voltaje de entre 3.3 y 5V como Arduino.

[![ky-032.jpg](https://i.postimg.cc/9MdqNnCx/ky-032.jpg)](https://postimg.cc/xJdCXgkH)


**Conexion arduino**

[![ardiiob.png](https://i.postimg.cc/4xG4WxmT/ardiiob.png)](https://postimg.cc/9rxjMVdx)

**Caracteristicas**

- Tensión de alimentación: 3.3V-5V
- Consumo: ≥ 20mA
- Rango de operación: -10 ℃ – +50 ℃
- Distancia de detección :2-40cm
- Señales: (GND / VCC/ OUT / EN)
- Señal OUT: Nivel bajo hay un obstáculo.
- Ángulo de medición: 35°
- Tamaño: 38mm × 16mm
- Peso: 9g

**Codigo basico**
Aqui se muestra un codigo de pruebas

´´´´
int valor,sensor=3; // Variables con su pin y nombre 

void setup() {
  Serial.begin(9600); // Velocidad de comunicación serial a 9600 baudios
  pinMode(sensor,INPUT); // Se configura sensor como entrada
}

void loop() {
  valor=digitalRead(sensor); // Se lee el valor digital del sensor y se asigna a valor
  if(valor==1){              // Sí el valor es igual a uno se accede a las instrucciones
    Serial.println("NEGRO"); // Se imprime un texto en el monitor serial
  }else if(valor==0){        // Sí el valor es igual a cero se ejecuta la instrucción  
   Serial.println("BLANCO"); // Se imprime blanco en el monitor serial
   }
}
´´´´
