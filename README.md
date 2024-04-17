# MarkdownS2
ResistorColorDuo
El código ResistorColorDuo se utiliza para decodificar un par de colores de una resistencia y devolver el valor numérico correspondiente.

typescript
Copy code
export enum ResistorValues {
  black = 0,
  brown = 1,
  red = 2,
  orange = 3,
  yellow = 4,
  green = 5,
  blue = 6,
  violet = 7,
  grey = 8,
  white = 9,
}

type Color = keyof typeof ResistorValues;

export function decodedValue([first, second]: Color[]): number {
  return Number(`${ResistorValues[first]}${ResistorValues[second]}`);
}
La problemática original era decodificar un par de colores de una resistencia para calcular su valor numérico. Se utilizó un enum ResistorValues para asignar valores numéricos a cada color, y luego se implementó la función decodedValue que toma un array de dos colores y devuelve el valor numérico correspondiente.

ResistorColorTrio
El código ResistorColorTrio es similar al ResistorColorDuo, pero decodifica un conjunto de tres colores de una resistencia.

typescript
Copy code
export enum ResistorValues {
  black = 0,
  brown = 1,
  red = 2,
  orange = 3,
  yellow = 4,
  green = 5,
  blue = 6,
  violet = 7,
  grey = 8,
  white = 9,
}

type Color = keyof typeof ResistorValues;

export function decodedValue([first, second, third]: Color[]): number {
  return Number(`${ResistorValues[first]}${ResistorValues[second]}${ResistorValues[third]}`);
}
Se modificó la función decodedValue para aceptar un array de tres colores en lugar de dos. De esta manera, se puede decodificar un conjunto de tres colores de una resistencia para calcular su valor numérico.
