// 定義腳位
const int sensorPin = A0;    // 感測器接在類比腳位 A0
const int ledPin = 6;        // LED 接在數位腳位 6

// 設定閾值
const int THRESHOLD = 500;    // 感測器觸發閾值

void setup() {
  pinMode(ledPin, OUTPUT);    // 設定LED為輸出
  Serial.begin(9600);        // 啟動序列通訊，用於監看數值
}

void loop() {
  // 讀取感測器數值 (0-1023)
  int sensorValue = analogRead(sensorPin);
  
  // 將數值顯示在序列監視器
  Serial.print("感測器數值: ");
  Serial.println(sensorValue);
  
  // 當數值超過閾值時點亮LED
  if (sensorValue > THRESHOLD) {
    digitalWrite(ledPin, HIGH);
  } else {
    digitalWrite(ledPin, LOW);
  }
  
  delay(100);  // 短暫延遲
}
