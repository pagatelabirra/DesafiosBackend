class User {
    constructor(name, lastName, books = [], pets = []){
        this.name = name;
        this.lastName = lastName;
        this.books = books;
        this.pets = pets
    }
    getFullName(){
        return(`${this.name} ${this.lastName}`)
    }
    addMascota(name){
        this.pets.push(name);
        void this.pets
    }
    countPets(){
        return this.pets.length
    }
    addBook(name, author){
        this.books.push({name : name, author : author});
        void this.books
    }
    getBookNames(){
        let bookNames = [];
        this.books.forEach(book => bookNames.push(book.name));
        return bookNames
    }
}

const usuario1 = new User('Matias', 'Cabral') // Creating new instance of User class
console.warn('Nuevo usuario creado')
console.log(usuario1)
usuario1.addMascota('Perro')
usuario1.addMascota('Loro')
usuario1.addMascota('Puma')
console.warn('Nuevas mascotas agregadas')
console.log(usuario1)
console.log(`Cantidad de mascotas : ${usuario1.countPets()}`)
usuario1.addBook('Introduction to Algorithms', 'Cormen, Leiserson, Rivest, Stein')
usuario1.addBook('Parallel Programming', 'Rauber, Rünger')
usuario1.addBook('Functional Programming Patterns', 'Bevilacqua, Linn')
console.warn('Nuevos Libros Agregados')
console.log(usuario1)
console.log(`Nombres de Libros agregados : ${usuario1.getBookNames()}`)