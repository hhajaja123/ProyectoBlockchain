# ProyectoBlockchain
Proyecto educativo para conocer mas a profundidad el concepto de Blockchain
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.2;


contract Aprende_Blockchain {
    
    address private jugador;
    uint256 premio;
    string posibleRespuesta;
    string public Respuesta;
    string posible = "si";
    string posible_b = "Si";
    string posible_c = "SI";
    
    
    event Pregunta(string, string respuesta, string, uint256 premio);
    
    function Blockchain_Es_Descentralizado(string memory _Aprende_Blockchain) public{
        posibleRespuesta = _Aprende_Blockchain;
        Respuesta = 'Si, Blockchain es una programacion descentralizada.';
        
        premio = 0;
        if(keccak256(abi.encodePacked((posibleRespuesta))) == keccak256(abi.encodePacked((posible)))||keccak256(abi.encodePacked((posibleRespuesta))) == keccak256(abi.encodePacked((posible_b)))||keccak256(abi.encodePacked((posibleRespuesta))) == keccak256(abi.encodePacked((posible_c)))){
            //jugador = msg.sender;
            premio = 10000000000000000000;
        }
        
    emit Pregunta("Su respuesta es ", posibleRespuesta, "Ganaste ", premio);
    }

}

2.	Explicación:

A través de la implementación del código smart contrac se busca llevar una idea por medio de diferentes procesos como la definición y análisis de conceptos, aplicaciones y funcionalidades básicas que brinda la herramienta BlockChain, en este primer avance se realiza un código de una pequeña demostración del funcionamiento de las divisas sobre las cuales se ha realizado un análisis de la forma de trabajo de un Smart Contarct que cumple con labor de analizar y tomar decisiones bajo una serie de parámetros que son definidas por un diseñador o desarrollador; Como por ejemplo un juego que incluye un usuario y un premio mediante la ejecución de preguntas que se responden de manera secuencial y según sea la respuesta se otorgara un premio al dicho jugador podemos afirmar que este programa es capaz de analizar patrones de juego y establecer un puntaje según su resultado.

