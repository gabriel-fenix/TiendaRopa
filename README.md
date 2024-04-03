struct Articulo {
let nombre: String?
let precio: Double?
var stock: Int?
}


var articulos = [
Articulo(nombre: "Zapatos", precio: 250, stock: 150),
Articulo(nombre: "Playeras", precio: 100, stock: 700),
Articulo(nombre: "Pantalones", precio: 200, stock: 20),
Articulo(nombre: "Sombreros", precio: 300, stock: 100),
]
var aux: String = ""
var opcionIngresada: String = aux
var cuenta: Double = 0.0
while opcionIngresada != "2" {
print("******Bien venidos a tienda online******")
print("******ARTICULOS******")
print("******--------******")
print("--------------------------------------------")
print(" articulos 1 \(articulos[0].nombre!)")
print(" Precio \(articulos[0].precio!)")
print(" Stock: \(articulos[0].stock!)")
print("--------------------------------------------")
print(" articulos 2 \(articulos[1].nombre!)")
print(" Precio \(articulos[1].precio!)")
print(" Stock: \(articulos[1].stock!)")
print("--------------------------------------------")
print(" articulos 3 \(articulos[2].nombre!)")
print(" Precio \(articulos[2].precio!)")
print(" Stock: \(articulos[2].stock!)")
print("--------------------------------------------")
print(" articulos 4 \(articulos[3].nombre!)")
print(" Precio \(articulos[3].precio!)")
print(" Stock: \(articulos[3].stock!)")
print("--------------------------------------------")
print ("1.- Comprar articulo")
print ("2.- Salir")


print("--------------------------------------------")
aux = readLine()!
opcionIngresada = aux
switch opcionIngresada {
case "1":
print("--------------------------------------------")
print("Ingresar el numero de articulo a comprar: ")
aux = readLine()!
opcionIngresada = aux
switch opcionIngresada {
case "1":
print("--------------------------------------------")
print("Ingresa la cantidad de zapatos que desea comprar: ")
aux = readLine()!
opcionIngresada = aux
let cantidadIngresada = Int(opcionIngresada)!
if cantidadIngresada <= articulos[0].stock! {
// Se puede comprar
articulos[0].stock! = articulos[0].stock! - cantidadIngresada
cuenta = Double(cantidadIngresada) * articulos[0].precio!
print("Total a pagar: \(cuenta)")
print("******GRACIA POR SU COMPRA VUELVA PRONTO A TIENDA COPPEL******")
} else {
print("No hay suficiente stock lo sentimos!")
}
case "2":
print("--------------------------------------------")
print("Ingresa la cantidad de Playeras que desea comprar: ")
aux = readLine()!
opcionIngresada = aux


let cantidadIngresada = Int(opcionIngresada)!
if cantidadIngresada <= articulos[1].stock! {
// Se puede comprar
articulos[1].stock! = articulos[1].stock! - cantidadIngresada
cuenta = Double(cantidadIngresada) * articulos[1].precio!
print("Total a pagar: \(cuenta)")
print("******GRACIA POR SU COMPRA VUELVA PRONTO A COPPEL******")
} else {
print("No hay suficiente stock lo sentimos!")
}
case "3":
print("--------------------------------------------")
print("Ingresa la cantidad de Pantalones que desea comprar: ")
aux = readLine()!
opcionIngresada = aux
let cantidadIngresada = Int(opcionIngresada)!
if cantidadIngresada <= articulos[2].stock! {
// Se puede comprar
articulos[2].stock! = articulos[2].stock! - cantidadIngresada
cuenta = Double(cantidadIngresada) * articulos[2].precio!
print("Total a pagar: \(cuenta)")
print("****GRACIA POR SU COMPRA VUELVA PRONTO A COPPEL*****")
} else {
print("Noy suficiente stock lo sentimos!")
}
case "4":
print("--------------------------------------------")
print("Ingresa la cantidad de Sombreros que desea comprar: ")
aux = readLine()!
opcionIngresada = aux
let cantidadIngresada = Int(opcionIngresada)!


if cantidadIngresada <= articulos[3].stock! {
// Se puede comprar
articulos[3].stock! = articulos[3].stock! - cantidadIngresada
cuenta = Double(cantidadIngresada) * articulos[3].precio!
print("Total a pagar: \(cuenta)")
print("******GRACIA POR SU COMPRA VUELVA PRONTO A COPPEL******")
} else {
print("No hay suficiente stock lo sentimos!")
}

default:
print("Opcion no valida")

}

case "2":
// Salir
print("Hasta pronto!")
aux = readLine()!
default:
print("opcion no valida")
aux = readLine()!
}
}
