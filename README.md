#define L1 13
#define L2 12
#define L3 11
#define L4 10
#define Bot1 2
#define B2 3
#define B3 4
#define ATIVO LOW
#define DESTATIVADO HIGH

const byte entradaSaida[7] [7] = {{13,1},{12,1}, {11,1},{10,1},{2,0}, {3,0},{4,0}};

void setup() {
for (int i=0;i<7;i++)
  pinMode(entradaSaida[i][0],
entradaSaida[i][1]);

    Serial.begin (9600);

}

void testaEntrada(int entrada, int saida){
  if(digitalRead(entrada)==ATIVO);
  else
  digitalWrite(saida, LOW);
}

void estadoEntrada (int botao){
  Serial.print("BOT");
  Serial.print(botao);
  Serial.print(":");

  if(digitalRead(botao)==ATIVO)
  Serial.println("ATIVO");
  else
  Serial.println("DESATIVADO");
}
