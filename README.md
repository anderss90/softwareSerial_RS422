# softwareSerial_RS422
An rs422 version of the Arduino softwareSerial library. It has two TX pins, TX+ and TX-. It only uses one pin for RX, as the positive pin of rs422 can be read as normal rs232. 

NB! It has an EVEN parity bit hard coded in. You can remove this by removing the code under "//write parity bit" on line 489 in src/SoftwareSerial_rs422.cpp
/*
//write parity bit
  if (p & 0x01){
    *reg_plus |= reg_mask_plus; // send 1
    *reg_minus &= inv_mask_minus; // send 0
  }
  else {
    *reg_plus &= inv_mask_plus; // send 0
    *reg_minus |= reg_mask_minus; // send 1
  }
*/
