#define LED 12 //DEFINE O QUE EU QUERO USAR, SEJA UM BOTÃO OU UM LED, AI COLOCA O NOME E ENTRADA/SAIDA DO COMPONENTE

void blink(const int led); //CRIAÇÃO DA VARIAVEL BLINK, O QUE TEM DENTRO É O VALOR DO LED

void setup()
{
  pinMode(LED, OUTPUT); // O LED QUE QUERO E SE A PORTA QUE COLOQUEI É ENTRADA OU SAIDA
}

void loop()
{
  blink(LED); //LOOP DA VARIAVEL QUE CRIEI, E ESSA VARIAVEL VAI RECEBER O LED DO DEFINE, E VAI FICAR NO LOOP
}

void blink(const int led) // MINHA FUNÇÃO, ELA VAI ACENDER A APAGAR O LED, E PARA ISSO USA O DIGITALWRITE(E SE É NIVEL ALTO OU BAIXO);
{
  digitalWrite(led, HIGH);
  delay(1000);
  digitalWrite(led, LOW);
  delay(1000); 
}

segundo codigo com delay e status

#define LED 12
int StatusLED = 1; // AQUI EU DIGO SE O STATUS DO LED VAI SER ALTO OU BAIXO

void blink(const int led, const int status, const int delayy); // EU ACRESCENTEI MAIS DUAS VARIAVEIS, STATUS QUE VAI RECBER O STATUSLED E O DELAYY QUE VAI SER COLOCADO NO LOOP

void setup()
{
  pinMode(LED, OUTPUT);
}

void loop()
{
  blink(LED, StatusLED,100); //O STATUSLED VAI RECEBER O 1 E O 100 E EM RELAÇÃO A O DELAYY
}

void blink(const int led, const int status, const int delayy)
{
  digitalWrite(led, status);
  delay(delayy);
}


