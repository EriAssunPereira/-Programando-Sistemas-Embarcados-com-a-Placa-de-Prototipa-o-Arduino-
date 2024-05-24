# -Programando-Sistemas-Embarcados-com-a-Placa-de-Prototipa-o-Arduino-

A programação de sistemas embarcados com Arduino abre um mundo de possibilidades para criadores, engenheiros e entusiastas da tecnologia. O Arduino é uma plataforma de prototipagem eletrônica de código aberto que é fácil de usar e altamente versátil, tornando-a ideal para o desenvolvimento rápido de projetos de hardware.

**Módulo 1: Introdução ao Arduino**
O Arduino é uma placa que pode ser conectada a um computador, permitindo o envio de comandos que interagem com sensores, motores e outras peças eletrônicas. A linguagem de programação utilizada é baseada em C, o que facilita a aprendizagem para quem já tem conhecimento nessa linguagem.

**Exemplo de Código: Piscar LED**
```c
void setup() {
  pinMode(13, OUTPUT); // Define o pino 13 como saída
}

void loop() {
  digitalWrite(13, HIGH); // Acende o LED
  delay(1000);            // Espera por um segundo
  digitalWrite(13, LOW);  // Apaga o LED
  delay(1000);            // Espera por um segundo
}
```

**Módulo 2: Entradas e Saídas Digitais**
As entradas e saídas digitais são a base para a interação com o mundo externo. Podemos ler o estado de botões ou sensores (entradas) e controlar LEDs ou relés (saídas).

**Exemplo de Código: Leitura de Botão**
```c
const int buttonPin = 2; // O pino onde o botão está conectado
const int ledPin =  13;  // O pino do LED

void setup() {
  pinMode(ledPin, OUTPUT);      
  pinMode(buttonPin, INPUT);
}

void loop(){
  int buttonState = digitalRead(buttonPin);
  if (buttonState == HIGH) {   
    digitalWrite(ledPin, HIGH);  
  } else {
    digitalWrite(ledPin, LOW); 
  }
}
```

**Módulo 3: Comunicação Serial**
A comunicação serial é essencial para enviar dados para o computador ou receber comandos dele. Isso permite uma interação mais complexa entre o hardware e o software.

**Exemplo de Código: Comunicação Serial**
```c
void setup() {
  Serial.begin(9600); // Inicia a comunicação serial a 9600 bps
}

void loop() {
  if (Serial.available() > 0) {
    int receivedValue = Serial.read(); // Lê o valor recebido
    Serial.println(receivedValue);     // Imprime o valor recebido
  }
}
```

**Conclusão**
Com estes módulos básicos, você pode começar a explorar o vasto universo da programação de sistemas embarcados. O Arduino é uma ferramenta poderosa que, quando combinada com a linguagem C, oferece uma plataforma robusta para a criação de projetos interativos e inovadores. Experimente, explore e divirta-se criando seus próprios sistemas embarcados!
