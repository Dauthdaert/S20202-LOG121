# Pattron Médiateurt

```plantuml
@startuml
skinparam style strictuml

interface Mediator {
	 saleOffer(String stock, int shares, int collCode): void
	 buyOffer(String stock, int shares, int collCode): void
	 addColleague(Colleague colleague): void
}


abstract class  Colleague {
  	  saleOffer(String stock, int shares): void
	  buyOffer(String stock, int shares): void
	  setCollCode(int CollegueCode): void
}
class StockOffer
class GormanSlacks extends Colleague
class JTPoorman extends Colleague
class StockMediator implements Mediator

StockMediator "1" --> "*" Colleague: mediate for
StockMediator "1" -right-> "*" StockOffer: stockBuyOffers
StockMediator "1" --> "*" StockOffer: stockSaleOffers
	
@enduml
```