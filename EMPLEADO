/*HERENCIA*/  

class Empleado {
    Id: number=0;
    Identificacion: number = 0;
    Nombre: string = '';
    Edad: number=0;
    Estatura: number=0;
    Pais: string = '';
    Cargo: string = '';
    EmpleadoArray:Array<any>=[];
}

/*INTERFAZ*/
interface IEmpleado extends Empleado{
obtener():void;
obteneridentificacion(Identificacion: number):void;
crear():void;
actualizar():void;
eliminar():void;
}

class Empresa implements IEmpleado{
    Id: number=0;
    Identificacion:number = 0;
    Nombre: string = '';
    Edad: number=0;
    Estatura: number=0;
    Pais: string = '';
    Cargo: string = '';

   EmpleadoArray = [{Id: 1, Identificacion:1037667985, Nombre:'Deiner',Edad:24, Estatura:1.60,Pais:'Colombia',Cargo:'Sistemas'},
   {Id: 2, Identificacion:10376679, Nombre:'Carlos',Edad:24, Estatura:1.80,Pais:'Colombia',Cargo:'Caja'},
   {Id: 3, Identificacion:10377985, Nombre:'Karen',Edad:20, Estatura:1.60,Pais:'Colombia',Cargo:'Administradora'},
   {Id: 4, Identificacion:37667985, Nombre:'Francia',Edad:28, Estatura:1.80,Pais:'Colombia',Cargo:'Gerente'},
   {Id: 5, Identificacion:667985, Nombre:'Julian',Edad:24, Estatura:1.60,Pais:'Colombia',Cargo:'Contadora'}]

   
   obtener(): void{
    for(let empresa of this.EmpleadoArray){
         console.log(empresa.Id,empresa.Identificacion,empresa.Nombre,empresa.Edad,empresa.Estatura,empresa.Pais,empresa.Cargo)
        }    
    }




   obteneridentificacion(idd: number): void{
    for(let empresa of this.EmpleadoArray){
        if(empresa.Identificacion == idd){
            console.log(empresa.Identificacion,empresa.Nombre,empresa.Edad,empresa.Estatura,empresa.Pais,empresa.Cargo)
        }
        
      }
    
     }

      
      crear():void{
      var objEmpresa = new Empresa();
      var id:number = Number(window.prompt("Digite Id"));
      var identificacion:number = Number(window.prompt("Digite Identificacion"));
      var nombre:string = String(window.prompt("Digite Nombre"));
      var edad:number = Number(window.prompt("Digite Edad"));
      var estatura:number = Number(window.prompt("Digite Estatura"));
      var pais:string = String(window.prompt("Digite Pais"));
      var cargo:string = String(window.prompt("Digite Cargo"));
      this.EmpleadoArray.push({Id: id,Identificacion:identificacion, Nombre: nombre, Edad:edad, Estatura: estatura, Pais: pais, Cargo: cargo})
      console.log(this.EmpleadoArray);
     
      console.log(objEmpresa.crear());
      
        
    }

    




     actualizar(Id:number):void{  
var objEmpresa = new Empresa();
var Id:number = Number(window.prompt("Digite Id"));
var identificacion:number = Number(window.prompt("Digite Identificacion"));
var nombre:string = String(window.prompt("Digite Nombre"));
var edad:number = Number(window.prompt("Digite Edad"));
var estatura:number = Number(window.prompt("Digite Estatura"));
var pais:string = String(window.prompt("Digite Pais"));
var cargo:string = String(window.prompt("Digite Cargo"));
console.log(objEmpresa.actualizar(Id));


    const actualizarIndex = this.EmpleadoArray.findIndex(element => element.Id == Id);
    this.EmpleadoArray[actualizarIndex].Identificacion = identificacion
    this.EmpleadoArray[actualizarIndex].Nombre = nombre
    this.EmpleadoArray[actualizarIndex].Edad = edad
    this.EmpleadoArray[actualizarIndex].Estatura = estatura
    this.EmpleadoArray[actualizarIndex].Pais = pais
    this.EmpleadoArray[actualizarIndex].Cargo = cargo
    console.log(this.EmpleadoArray[actualizarIndex])
  }
  

  
      eliminar(Id: number): void{
      for(let empresa of this.EmpleadoArray.filter((i) => i.Id !=Id){
         console.log(empresa)
        }   
        
        }
}


/*MENU*/




class Iniciar {
    opc: any = 0;
    respuesta: string = '';
    Operar() {
        let objEmpresa = new Empresa();
        do {
            this.opc = prompt
                (`
             Elige una opcion:
             
             1: Obtener Todos los Empleados
             2: Buscar Empleados por Identificacion
             3: Crear Empleado
             4: Actualizar Empleado
             5: Eliminar Empleado
             6: Salir
             `)

            switch (parseInt(this.opc)) {

                case 1:{
                    console.log(objEmpresa.obtener());  
                    break;
                }
                  
                  

                case 2:{
                    var idd:number = Number(window.prompt("Digite Identificacion"));
                    console.log(objEmpresa.obteneridentificacion(idd));
                    break;

                }
                   
                    

                case 3:{
                    console.log(objEmpresa.crear());   
                    break;
                }
                  

                case 4:{
                    var Id:number = Number(window.prompt("Digite Id"));
                    console.log(objEmpresa.actualizar(Id));
                    break;
                }
                    

                case 5:{
                    var Id:number = Number(window.prompt("Digite id para eliminar"));
                  console.log(objEmpresa.eliminar(Id));
                    break;

                }
                    

                case 6:{
                    this.respuesta = prompt("Seguro que quieres salir ? s : si,  n : no")
                    if (this.respuesta === "s") {
                        this.opc = 6;
                        alert("Hasta Luego")
                    }else{
                        this.opc = 0;
                    }
                    break;

                }
                    
            }
        }
        while (this.opc < 6)
    }

}



let iniciar = new Iniciar();
iniciar.Operar();
