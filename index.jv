class Postac {
  constructor(imie, plec, klasaPostaci, hp = 100, predkosc = 10) {
    this.imie = imie;
    this.plec = plec;
    this.klasaPostaci = klasaPostaci;
    this.hp = hp;
    this.predkosc = predkosc;
    this.poziom = 1;
    this.doswiadczenie = 0;
    this.ekwipunek = [];
    this.umiejetnosci = [];
  }

  otrzymajObrazenia(ilosc) {
    this.hp -= ilosc;
    if (this.hp < 0) this.hp = 0;
    console.log(`${this.imie} otrzymał ${ilosc} obrażeń. HP: ${this.hp}`);
  }

  ustawPredkosc(nowaPredkosc) {
    this.predkosc = nowaPredkosc;
    console.log(`${this.imie} ma teraz prędkość: ${this.predkosc}`);
  }

  getHP() {
    return this.hp;
  }

  dodajUmiejetnosc(nazwa) {
    if (!this.umiejetnosci.includes(nazwa)) {
      this.umiejetnosci.push(nazwa);
      console.log(`${this.imie} nauczył się umiejętności: ${nazwa}`);
    }
  }

  zdobyjDoswiadczenie(ilosc) {
    this.doswiadczenie += ilosc;
    console.log(`${this.imie} zdobył ${ilosc} XP`);

    while (this.doswiadczenie >= this.potrzebneXPDoAwansu()) {
      this.doswiadczenie -= this.potrzebneXPDoAwansu();
      this.poziom++;
      this.hp += 20;
      console.log(`${this.imie} awansował na poziom ${this.poziom}! HP zwiększone do ${this.hp}`);
    }
  }

  potrzebneXPDoAwansu() {
    return this.poziom * 100;
  }

  dodajDoEkwipunku(przedmiot) {
    this.ekwipunek.push(przedmiot);
    console.log(`${this.imie} zdobył przedmiot: ${przedmiot}`);
  }

  pokazStatus() {
    console.log(`--- STATUS POSTACI ---
Imię: ${this.imie}
Płeć: ${this.plec}
Klasa: ${this.klasaPostaci}
HP: ${this.hp}
Prędkość: ${this.predkosc}
Poziom: ${this.poziom}
XP: ${this.doswiadczenie}/${this.potrzebneXPDoAwansu()}
Umiejętności: ${this.umiejetnosci.join(', ') || 'brak'}
Ekwipunek: ${this.ekwipunek.join(', ') || 'brak'}
------------------------`);
  }
}
