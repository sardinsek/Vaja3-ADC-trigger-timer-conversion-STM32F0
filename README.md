# Vaja3-ADC-trigger-timer-conversion-STM32F0
Glede na najino razvojno ploščico in razširitveno vezje z tipkami ter potenciometri, sva izbrala ustrezni analogni vhod PC0.
Glede na potenciometer na najini ploščici izberemo-obkljukajmo ustrezni kanal/pin. Na zaslonu se nam mora usterzno pobarvati izbrani pin v zeleno barvo. Poleg pina se izpiše ADC_IN10.
Aktiviramo samo zeleno LED diodo na ustreznem izhodu PC9.
V Clock Configuration spremenimo APB1 Timer clock (MHz) na 16 MHz (pritisnemo ENTER). Opazimo, da se frekvenca nastavi na 16 MHz.
V razdelku TIM1, pod Counter Settings, bi radi časovniku spremenili frekvenco na 1 kHz, zato sva frekvenco ABP1 Timer Clock preskalirala v polju Prescaler (PSC – 16 bit value). Ta vrednost znaša 16.000. 
Komentar delovanja: Branje spremenljivke oz. potenciometra, deluje dobro vendar, kot sva že omenila pri prejšnji vaji ne moramo prebrati maksimalne vrednosti. Sicer je natančnost branja manj natančna kot pri prejšnji vaji, saj smo pri tej vaji nastavili resolucijo na 8 bitno, pri prejšnji vaji pa je bila nastavljena na 32 bitno. Sicer pri takšnem branju ta resolucija ni toliko pomembna, saj ne rabimo tako natančnega mirjenja. Izbira 32 bitne resolucije, bi bila bolj smisena, če bi potrebovali bolj natančno merjenje oz. bolj natančne podatke meritev.
