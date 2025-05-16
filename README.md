# Viernes16mayo
Ejemplos 3 y 4 juntos

------
```ts
interface Planet {
	name: string;
	galaxy: string;
	numberOfMoons: number;
	weight: number;
}

// Objeto con propiedades
let planet: Planet = {
	name: "Earth",
	galaxy: "Milky Way",
	numberOfMoons: 1,
	weight: 100000
};

// Mostrar propiedades individualmente
console.log("Planet Name :- " + planet.name);
console.log("Planet Galaxy :- " + planet.galaxy);
console.log("Planet Number of Moons :- " + planet.numberOfMoons);
console.log("Planet Weight :- " + planet.weight);

// Iterar sobre las propiedades del objeto
for (let prop in planet) {
	if (planet.hasOwnProperty(prop)) {
		console.log(`Planet ${prop} :- ${planet[prop as keyof Planet]}`);
	}
}
