# Patron Adaptateur Customer

```plantuml
@startuml
interface AddressIF {
   
     getAddress1(): String
     setAddress1(String address1):  void
     getAddress2():  String
     setAddress2(String address2):  void
     getCity():  String
     setCity(String city):  void
     getState():  String
     setState(String state):  void
     getPostalCode() :  String
     setPostalCode(String postalCode):  void
}
class Customer
Class CuttomerBillToAdapter implements AddressIF {
  getAddress1(): String
     setAddress1(String address1):  void
     getAddress2():  String
     setAddress2(String address2):  void
     getCity():  String
     setCity(String city):  void
     getState():  String
     setState(String state):  void
     getPostalCode() :  String
     setPostalCode(String postalCode):  void
}
CuttomerBillToAdapter -> Customer: adapt

@enduml
```