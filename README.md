# UniProjekt
//UniProjekt aus dem Modul Webbasierte Anwendungen

class Kegelstumpf {

  /*
        R steht für Radius der Grundfläche
        r steht für Radius der Deckfläche
        h steht für Höhe
    */

  constructor(R, r, h) {
    this.R = R;
    this.r = r;
    this.h = h;
  }

  // Rechnet das Volumen
  volumen() {
    return (
      ((Math.PI * this.h) / 3) *
      (this.R * this.R + this.R * this.r + this.r * this.r)
    );
  }

  // Rechnet die Mentalfläche
  mantelflaeche() {
    const m = Math.sqrt(
      (this.R - this.r) * (this.R - this.r) + this.h * this.h
    );
    return Math.PI * m * (this.R + this.r);
  }

  // Rechnet die Oberfläche
  oberflaeche() {
    return (
      Math.PI * (this.R * this.R) +
      Math.PI * (this.r * this.r) +
      this.mantelflaeche()
    );
  }
}


const k = new Kegelstumpf(18, 15, 28);
