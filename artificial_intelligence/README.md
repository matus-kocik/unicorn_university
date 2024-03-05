# Artificial Intelligence

Domácí úkol 10
Posilované učení v nebezpečném světě
Naimplementujte způsob, jak procházet světem a vhodně kombinovat exploraci a exploataci, abyste se dozvěděli strategii, kterou pro každé políčko hry máte ideálně využít.
Prostředí máte předimplementované v příslušném souboru k příslušné kapitole
Při přechodu akcí ze stavu obdržíte pomocí funkce move(x, y, action) nový stav, odměnu a info, zda je stav terminální, agent ale nesmí znalosti této funkce využívat a dozvídá se informaci o odměně a novém stavu vždy po jednom kroku
Jak jsou implementované akce a prostředí zjistíte v příslušném souboru (pokud to budete potřebovat, dejte pozor na reprezentaci scény v poli prostředí), ve světě jsou souřadnice x, y brány tak jak jsme zvyklí v kartézské soustavě souřadnic

Domácí úkol 9
Minimax pro Tic-tac-toe
Naimplementujte funkci ttt_move(game, myplayer, otherplayer), která vezme na vstupu seznam seznamů (matici 3x3) herního plánu tic-tac-toe obsahující 0, 1 nebo 2 = (prázdné políčko, křížek nebo kolečko). Parametr myplayer určuje číslo hráče, který je na tahu - 1 (hraje křížky) nebo 2 (hraje kolečky). Parametr otherplayer je číslo druhého hráče. Funkce vrací nový herní plán rozšířený o tah hráče myplayer.
Můžete využít předimplementované funkce v příslušném jupyter notebooku

Domácí úkol 8
Hledání cesty ve 2D mapě
Naimplementujte metodu path_planner(self, start, goal), která vezme dvojici souřadnic start a dvojici souřadnic cíl a v mapě block.py vrátí dvě proměnné - frontu obsahující souvislou posloupnost dvojic souřadnic ze startu do cíle a pole expandovaných uzlů k vybarvení
V metodě implementujte algoritmy Greedy best first search, Dijkstra a A*
Díky vizualizaci porovnejte množství expandovaných uzlů u jednotlivých algoritmů

Domácí úkol 7
Učení neuronové sítě s učitelem
stáhněte si vhodná trénovací + testovací data z https://www.tensorflow.org/datasets/catalog/overview#all_datasets
předzpracujte vhodně data
zvolte vhodnou topologii sítě (struktura a typ vrstev, přechodové funkce), učící algoritmus a měření chyby
naučte síť, aby dosahovala přesnosti alespoň 90% na testovacích datech

Domácí úkol 6
Evoluční učení neuronové sítě
naimplementujte vlastní sentorické funkce, kterými budou agenti vnímat prosředí
navrhněte funkci nn_function(inp, wei), která na základě vstupů inp a vektoru vah wei neuronové sítě (genomu neuronové sítě / zlinearizované sítě) provede výpočet výstupů této sítě
navrhněte funkci nn_navigate_me(me, inp), která pro agenta me a jeho senzorické vstupy inp provede výpočet jeho pohybu na základě jeho vnitřního genomu reprezentujícího jeho neuronovou síť (zda pojede up, down, left, right)
doimplementujte mechanismus výpočtu fitness jedinců ve funkci handle_mes_fitnesses(mes), která dostane seznam jedinců mes a vypočítá jim fitness na základě jednoho herního kola
nastavte vhodně parametry evolučního algoritmu (mutace, crossover, selekce)

Domácí úkol 5
Evoluční generování strategie pro iterované vězňovo dilema
navrhnout kódování tabulky reaktivního agenta, vracejícího další tah 0 (nezradit) či 1 (zradit) na základě historie vlastních tahů a tahů protihráče
evolučně najít 0/1 genom, který nejlépe hraje iterované vězňovo dilema
implementovat na základě vyevolvovaného genomu funkci zrada(moje_hostorie, protihracova_historie) vracejici nasledujici tah 0/1

Domácí úkol 4
Evoluční generování terénu
nainstalovat a rozchodit knihovnu DEAP
pomocí DEAP evolučně vygenerovat funkci terénu v závislosti na sofistikované fitness funkci

Domácí úkol 3
Barvení grafu pomocí lokálního prohledávání
implementovat funkci iscoloring(G, col), která pro zadaný seznam/pole barev a graf G ověří, že se jedná o validní obarvení
implementovat funkci color(G, k, steps), která se pomocí lokálního prohledávání pokusí nalézt obarvení grafu G pomocí k barev, steps je maximální počet kroků lokálního prohledávání. Funkce vrací dvojici - seznam/pole obarvení a boolovskou hodnotu true/false, která indikuje, zda se obarvení podařilo nalézt. Funkce by měla vhodně kombinovat náhodnou procházku a hill climbing, případně další představené techniky.
Abychom poměřili síly, zkuste prosím váš algoritmus pustit na zadání dsjc125.9. Může to nějakou dobu (pár hodin) trvat, dejte si kafe nebo čaj a zkuste dát algoritmu čas, zda najde obarvení s co nejnižším počtem barev. Známé optimum je 44 barev. K němu bude těžké se přiblížit, nicméně se pokuste počet barev co nejvíce snížit postupným pouštěním s čím dál nižším počtem barev jako parametrem funkce.

Domácí úkol 2
Schellingův model (2D)
rozmyslet vhodnou reprezentaci Schellingova modelu
implementovat funkci step(rep), která vezme jako vstup reprezentaci situace a aplikuje jeden krok dle Schellingova modelu, vrací pozměněnou reprezentaci
implementovat funkci plot(rep), která vykreslí na výstup aktuální situaci v reprezentaci
simulujte na reprezentaci s náhodným rozmístěním agentů poslopnost kroků modelu, dokud existuje nespokojený agent, zobrazte grafem vývoj počtu spokojených jedinců v čase

Domácí úkol 1
Game of life (1D)
nainstalovat a rozchodit Python + Anaconda
implementovat funkci step(row), která vezme za parametr seznam reprezentující generaci/řádek jedinců a vrací seznam generaci novou
implementovat funkci printrow(row), která vypíše na výstup řádek - seznam na vstupu
experminentování s vlastními pravidly a počáteční populací
vygenerování vlastního originálního vzoru pomocí sekvenčního generování určitého počtu generací