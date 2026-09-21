# Controle-de-dois-LEDs-Arduino-IoT

<img width="1545" height="698" alt="image" src="https://github.com/user-attachments/assets/bc8762a7-8bbb-4bcb-b323-27bcd37911c4" />

Resumo da aula

Nesta aula, aprendemos a controlar dois LEDs usando um botão e Arduino. Cada aperto altera o estado dos LEDs, seguindo uma sequência programada. A atividade foi montada e simulada no Tinkercad.




````
int buttonPin = 7;

int led1 = 10;
int led2 = 11;

int estado = 0;

void setup() {
  pinMode(buttonPin, INPUT_PULLUP);

  pinMode(led1, OUTPUT);
  pinMode(led2, OUTPUT);

  digitalWrite(led1, LOW);
  digitalWrite(led2, LOW);
}

void loop() {

  if (digitalRead(buttonPin) == LOW) {

    estado++;

    if (estado > 3) {
      estado = 1;
    }

    if (estado == 1) {
      digitalWrite(led1, HIGH);
      digitalWrite(led2, LOW);
    }

    if (estado == 2) {
      digitalWrite(led1, LOW);
      digitalWrite(led2, HIGH);
    }

    if (estado == 3) {
      digitalWrite(led1, LOW);
      digitalWrite(led2, LOW);
    }

    delay(300);
  }
}

````




















https://www.tinkercad.com/things/cWIrtRy2YVC/editel?returnTo=%2Fdashboard&amp;sharecode=sOUW5o7iEBxuKW150VEzhrZjndRSe_cK4MBI_Jc9ZTM
