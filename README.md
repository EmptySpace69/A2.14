//A2.14
//Sensores
#include <LinkedList.h>

class Sensores {
      public: 
            string name;
            bool STATUS;
            float  Value;
            char units;
};
LinkedList<Sensores*> sensorlist = LinkedList<Sensores*>();

void setup()
{
      Serial.begin(9600);
      Serial.println("Hello");
      
     //Sensor de luz
     Sensores.luz = otrosensor();
     luz->name = "Sensor de Luz "
     luz->STATUS = true
     luz-> Value = 2585;
     luz-> units = 'Lm'
     
     //Sensor de temperatura
     Sensores.temperatura=otrosensor();
     tem->name = "Sensor de temperatura \n"
     tem->STATUS = true
     tem-> Value = 25;
     tem-> units = '°C'
     
     //Sensor de posicion
     Sensores.posicion=otrosensor();
     tem->name = "Sensor de posicion \n"
     tem->STATUS = true
     tem-> Value = 150;
     tem-> units = 'm'
     
     //Sensor de presion
     Sensores.presion=otrosensor();
     tem->name = "Sensor de presion \n"
     tem->STATUS = true
     tem-> Value = 1;
     tem-> units = 'atm'
     
     //Sensor de humedad
     Sensores.humedad=otrosensor();
     tem->name = "Sensor de humedad \n"
     tem->STATUS = true
     tem-> Value = 80
     tem-> units = '% g/m3'
     
     //Sensor de velocidad
     Sensores.velocidad=otrosensor();
     tem->name = "Sensor de velocidad \n"
     tem->STATUS = true
     tem-> Value = 30
     tem-> units = 'k/h'
    
    sensorlist.add(luz)
    sensorlist.add(temperatura)
    sensorlist.add(posicion)
    sensorlist.add(presion)
    sensorlist.add(humedad)
    sensorlist.add(velocidad)
    }
void(loop){
Serial.print("Hoy ");
Serial.print(sensorlist.size());
Serial.print(" sensores en la lista. Los sensores activos son: ");

int current=0;
Sensores *sensor;
for(int i = 0; i<sensorlist.size(); i++){
      sensor = sensorlist.get(i);
      if(animal->STATUS){
            if(current++)
                  Serial.print(", ")
            Serial.print(sensor->name);
            Serial.print(sensor->value);
            Serial.print(sensor->units);
            }
}

while (true);
}
    
