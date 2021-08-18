---
description: Dans MOF, les nombres sont des chiffres qui décrivent des valeurs numériques. MOF fournit un large éventail de types de données qui se traduisent par l’automatisation, et permet également à ces nombres d’être dans différents formats. Le tableau suivant répertorie les valeurs numériques prises en charge par MOF.
ms.assetid: 7a18ed36-9c12-42be-a4ee-0f6c0097b130
ms.tgt_platform: multiple
title: Nombres (WMI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f3441988bb91d4bb2f3742016f01cb69996e3dcb55081a6723d851ed74cc1cb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118555135"
---
# <a name="numbers-wmi"></a>Nombres (WMI)

Dans MOF, les nombres sont des chiffres qui décrivent des valeurs numériques. MOF fournit un large éventail de types de données qui se traduisent par l’automatisation, et permet également à ces nombres d’être dans différents formats. Le tableau suivant répertorie les valeurs numériques prises en charge par MOF.



| Type de données  | Type Automation | Description                                                                                                                                                             |
|------------|-----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **sint8**  | **VT \_ I2**      | Entier 8 bits signé.<br/>                                                                                                                                        |
| **sint16** | **VT \_ I2**      | Entier 16 bits signé.<br/>                                                                                                                                       |
| **sint32** | VT \_          | Entier 32 bits signé.<br/>                                                                                                                                       |
| **sint64** | **VT \_ BSTR**    | Entier 64 bits signé sous forme de chaîne. Ce type suit le format hexadécimal ou décimal en fonction des règles C du American National Standards Institute (ANSI).<br/> |
| **real32** | **VT \_ R4**      | valeur à virgule flottante de 4 octets qui suit la norme IEEE (Institute of Electrical and Electronics Engineers, Inc.).<br/>                                        |
| **real64** | **VT \_ R8**      | valeur à virgule flottante de 8 octets qui suit la norme IEEE.<br/>                                                                                                  |
| **destinées**  | **\_UI1 VT**     | Entier 8 bits non signé.<br/>                                                                                                                                      |
| **UInt16** | **VT \_**      | Entier 16 bits non signé.<br/>                                                                                                                                     |
| **uint32** | **VT \_**      | Entier non signé 32 bits.<br/>                                                                                                                                     |
| **uint64** | **VT \_ BSTR**    | Entier 64 bits non signé sous forme de chaîne. Ce type suit le format hexadécimal ou décimal conformément aux règles C ANSI.<br/>                                           |



 

Bien que flexible, le code MOF rencontre des modifications lors du traitement de l’automatisation :

-   Vous devez encoder des entiers 64 bits sous forme de chaînes.

    Automation ne prend pas en charge un type intégral 64 bits.

-   Les types Automation ne correspondent pas toujours aux types de données MOF en taille binaire.

    Par exemple, Automation utilise VT \_ I4 pour retourner une valeur non signée de 16 bits. Cette différence existe en raison de problèmes d’extension de signature. Si Automation a utilisé VT \_ I2 au lieu de VT \_ I4, 65 536 serait la valeur 1, provoquant des problèmes de type et de plage. De même, Automation représente le type **UInt32** en tant que VT \_ i4, car il n’existe pas de type entier plus grand pour contenir **UInt32**.

-   Vous n’avez pas besoin de modifier une représentation pour les types de chiffres 8 bits.

    Automation prend en charge VT \_ UI1, un type non signé de 8 bits.

MOF prend en charge les constantes longues. Vous déclarez une constante longue à l’aide d’une simple série de chiffres avec un signe négatif facultatif. Une constante longue ne peut pas dépasser la taille de la variable déclarée pour la conserver. 1000 et 12310 sont des exemples de constantes longues.

MOF prend également en charge d’autres formats numériques. Le tableau suivant répertorie les caractères spéciaux que vous devez utiliser pour décrire les constantes hexadécimales, binaires et octales.



| Constante               | Caractère spécial     |  Exemple                   |
|------------------------|-----------------------|---------------------------|
| Decimal<br/>     | Aucun<br/>       | Val = 65<br/>       |
| Valeur hexadécimale<br/> | préfixe 0x<br/>  | Val = 0x41 vers<br/>     |
| Octal<br/>       | 0 de début<br/>  | Val = 0101<br/>     |
| Binary<br/>      | Fin B<br/> | Val = 1000001B<br/> |



 

Vous pouvez utiliser une constante à virgule flottante pour représenter une notation scientifique et des fractions, comme indiqué ci-dessous :

``` syntax
3.14
-3.14
-1.2778E+02
```

WMI considère les constantes à virgule flottante comme des types **VT \_ R8** pour l’automatisation.

L’exemple suivant décrit les déclarations de classes et d’instances qui illustrent l’utilisation de chacun des types de données numériques pour définir des propriétés :

``` syntax
Class NumericDataClass
 {
   [key] uint8 Duint8;
   SInt8       Dchar;
   UInt16      Dtword;
   Sint16      Dinst16;
   UInt32      Ddword;
   Sint32      Dinst1;
   Sint32      Dinst2;
   Sint32      Dinst3;
   Sint32      Dinst4;
   Sint32      Dinst5;
   Real32      Dfloat;
   Real64      Ddouble1;
   Real64      Ddouble2;
 };

instance of NumericDataClass
 {
   Duint8   =  122;
   Dchar    = -128;
   Dtword   =  30;
   Dinst16  = -1445;
   Ddword   =  6987777;
   Dinst1   = -455589;
   Dinst2   =  23;
   Dinst3   =  03;         // Base 8
   Dinst4   =  0xFe;       // Base 16
   Dinst5   =  11b;        // Base 2
   Dfloat   =  3.1478;
   Ddouble1 =  99987.3654;
   Ddouble2 =  2.3e-2;
 };
```

 

 




