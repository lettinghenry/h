
int B = 9;
//int R = 10;
//int G = 11;

void setup() {

  Serial.begin(9600);// FROM SERIAL IN, ARDUINO PIN NUMBER 0,1
//  pinMode(R, OUTPUT);
//  pinMode(G, OUTPUT);
  pinMode(B, OUTPUT);

//  digitalWrite(R, HIGH);
//  delay(100);
//
//
//  digitalWrite(G, HIGH);
//  delay(100);
//  
//
//  digitalWrite(B, HIGH);
//  delay(100);
// 
}

void loop() {
  // put your main code here, to run repeatedly:
  if (Serial.available() > 0) {
    char data = Serial.read();
    switch (data) {

//      //red
//      case 'r': {
//          digitalWrite(R, HIGH);
//          digitalWrite(G, LOW);
//          digitalWrite(B, LOW);
//          break;
//        }
//      //green
//      case 'g': {
//          digitalWrite(R, LOW);
//          digitalWrite(G, HIGH);
//          digitalWrite(B, LOW);
//          break;
//        }
      //blue
      case 'b': {
          digitalWrite(B, HIGH);
          break;
        }

//      //white
      case 'w': {
//          digitalWrite(R, HIGH);
//          digitalWrite(G, HIGH);
          digitalWrite(B, LOW);
          break;
        }
//
//      //chameleon
//      case 'c': {
//
//          
//            for (int i = 0; i <255; i++) {
//
//              for (int j = 0; j < 50; j++) {
//
//                for(int k=0;k<20;k++){
//                  
//                analogWrite(R, j);
//                analogWrite(G, i );
//                analogWrite(B, k);
//                
//                
//                }
//
//              }
//           
//
//            }
//
//          
//          break;
//        }
//
//      //purple
//      case 'p': {
//          analogWrite(R, 255);
//          analogWrite(B, 120);
//          digitalWrite(G, LOW);
//          break;
//        }
//
//      //orange
//      case 'o': {
//          analogWrite(R, 255);
//          analogWrite(G, 12);
//          digitalWrite(B, LOW);
//          break;
//        }
//
//
//
//      //cyan
//      case 'y': {
//          analogWrite(B, 255);
//          analogWrite(G, 255);
//          digitalWrite(R, LOW);
//          break;
//        }
//      default:{if(data != 'b') digitalWrite(B, LOW);break;}
    }
    
    Serial.println(data);
  }
  delay(50);
}
