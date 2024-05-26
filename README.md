Христијан Давидовски 223252

Control Flow Graph

![ULM SLIKA](https://github.com/davidoviski/SI_2024_lab2_223252/assets/138602939/8488aa7a-db86-41b6-9ff6-af6d9b6c4a8e)

Тест случаи според критериумот Every statement

ТЕСТ 1: Проверка дали (allItems== null), за влез имаме allItems= null и payment = 50, имаме очекуван излез за искулучок со порака "allItems list can't be null!".

ТЕСТ 2: Проверка за празна листа на allItems, за влез имаме allItems=[] и payment=50, имаме очекуван излез "TRUE".

ТЕСТ 3: Проверка на item.getName() да е null, за влез имаме allItems = [new Item("", "654", 50, 0.2f)], имаме очекуван излез "TRUE" , односно поставуванје на name на "unknown".

ТЕСТ 4: Проверка на allowed.indexOf(c) == -1, за влез имаме allItems = [new Item("", "6a5v4", 50, 0.2f)], имаме очекуван излез за исклучок со порака "Invalid character in item barcode!".

ТЕСТ 5: Проверка за попуст на item.getDiscount() > 0, за влез имаме allItems = [new Item("gelato", "223252", 50, 0.2f)], и имаме очекуван излез со резултат по формула  sum += item.getPrice()*item.getDiscount(); односно 50*0.2.

ТЕСТ 6: Проверка без попуст на item.getDiscount() <= 0, за влез имаме allItems = [new Item("gelato", "223252", 50, 0)], и имаме очекуван излез од внесената цена односно 50.

ТЕСТ 7: Проверка на item.getBarcode() != null , за внес имаме allItems = [new Item("gelato", "null", 50, 0)], и имаме очекуван излез за исклучок со фрлање на порака "No barcode!".

ТЕСТ 8: Проверка на item.getPrice() > 300 && item.getDiscount() > 0 && item.getBarcode().charAt(0) == '0', за влез имаме allItems = [new Item("gelato", "0223252", 400, 0.1f)], имаме очекуван излез од sum -= 30; односно 370.

ТЕСТ 9: Проверка на sum <= payment , доколку sum=100 а payment =200, имаме очекуван излез од "TRUE".

ТЕСТ 10: Проверка на sum <= payment , доколку sum=200 а payment =100, имаме очекуван излез од "FALSE".


Тест случаи според критериумот Every path

ТЕСТ 1:За Влез имаме PRICE=400 , DISCOUNT=0.1 , BARCODE=0223252 , според податоците добиваме "TRUE" && "TRUE" && "TRUE", и заклучуваме дека условот е исполнет и ќе се изврши sum -= 30;.

ТЕСТ 2:За Влез имаме PRICE=200 , DISCOUNT=0.1 , BARCODE=0223252 , според податоците добиваме "FALSE" && "TRUE" && "TRUE", и заклучуваме дека условот  item.getPrice() > 300 не е исполнет и не  се извршуваат дополнителни акции.

ТЕСТ 3:За Влез имаме PRICE=400 , DISCOUNT=0 , BARCODE=0223252 , според податоците добиваме "TRUE" && "FALSE" && "TRUE", и заклучуваме дека условот  item.getDiscount() > 0 не е исполнет и не  се извршуваат дополнителни акции.

ТЕСТ 4:За Влез имаме PRICE=400 , DISCOUNT=0.1 , BARCODE=223252 , според податоците добиваме "TRUE" && "TRUE" && "FALSE", и заклучуваме дека условот   item.getBarcode().charAt(0) == '0' не е исполнет и не  се извршуваат дополнителни акции.

ТЕСТ 5:За Влез имаме PRICE=200 , DISCOUNT=0 , BARCODE=0223252 , според податоците добиваме "FALSE" && "FALSE" && "TRUE", и заклучуваме дека условите  item.getPrice() > 300 и  item.getDiscount() > 0 не се исполнети и не  се извршуваат дополнителни акции.

ТЕСТ 6:За Влез имаме PRICE=200 , DISCOUNT=0.1 , BARCODE=223252 , според податоците добиваме "FALSE" && "TRUE" && "FALSE", и заклучуваме дека условите  item.getPrice() > 300 и  item.getBarcode().charAt(0) == '0' не се исполнети и не  се извршуваат дополнителни акции.

ТЕСТ 7:За Влез имаме PRICE=400 , DISCOUNT=0 , BARCODE=223252 , според податоците добиваме "TRUE" && "FALSE" && "FALSE", и заклучуваме дека условите  item.getDiscount() > 0 и  item.getBarcode().charAt(0) == '0' не се исполнети и не  се извршуваат дополнителни акции.

ТЕСТ 8:За Влез имаме PRICE=200 , DISCOUNT=0 , BARCODE=223252 , според податоците добиваме "FALSE" && "FALSE" && "FALSE", и заклучуваме дека условите item.getPrice() > 300  и item.getDiscount() > 0 и  item.getBarcode().charAt(0) == '0' не се исполнети и не  се извршуваат дополнителни акции.










