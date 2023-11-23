# VEHICULO

/*fun main(args: Array<String>) {
    println("Hello World!")

    val myphone = Phone()
    myphone.getTurn()
    myphone.turnOn()
    myphone.getTurn()

    /*val vehiculo = Vehiculo()
    vehiculo.color = "Verde"
    vehiculo.marca = "Ford"
    vehiculo.modelo = "Focus"
    vehiculo.placas = "RSDFSDA"

    println("el carro esta: ${vehiculo.encendido} " )
    vehiculo.encender()
    println("El carro esta encendido: ${vehiculo.encendido}")
    println("el carro tiene gasolina: ${vehiculo.gasolina} " )
    vehiculo.recargar(20.07f)
    println("El carro tiene gasolina: ${vehiculo.gasolina}")
*/
    val miVehiculo = Vehiculo ("Volkwagen", "67", "Blanco", "AF7845")
    println("el carro es de la marca: ${miVehiculo.marca} " )

    val Per = Persona ("Simon", "Bolivar", "Masculino", 1.78f)
}*/


        fun main(){
            var mario= Mario()
       //     mario.collision("pipe")
         for(i in 1..6 ){
             mario.collision("Gomba")
             println("Te quedan ${mario.vidas}")
         }
        }

  class Persona constructor(val nombre: String, val apellidos: String, val sexo: String, val altura: Float) {
    init {
        println("""Los datos de la persona son:
            nombre: $nombre
            apellidos: $apellidos
            sexo: $sexo
            altura: $altura
        """.trimMargin())
    }
}

class Phone {
    var isON = false

    fun turnOn(){
        isON = true
    }

    fun getTurn(){
        val turnmode = if (isON) "encendido" else "apagado"
        println("el telefono esta $turnmode")
    }


}

lass Vehiculo constructor(val marca:String, val modelo: String, var color: String = "Lila") {

    init {
        println("""
            Los datos del coche son:
            marca: $marca
            modelo: $modelo
            color: $color
        """.trimIndent())
    }
    constructor(marca: String, modelo: String, color: String, placas:  String): this (marca, modelo, color){
        this.placas = placas
        println("Las placas son: ${this.placas}")
    }
    var placas = ""
    var gasolina = 0f
    var encendido = false

    fun encender (){
        encendido = true
    }

    fun apagar(){
        encendido = false
    }

    fun recargar(litros:Float) {
        gasolina = litros
    }
}
