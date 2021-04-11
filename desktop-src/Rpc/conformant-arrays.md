---
title: Tableaux conformes
description: La taille d’un tableau conforme peut varier ou se conformer chaque fois que le client le transmet à une procédure distante sur le serveur.
ms.assetid: b4aaec77-b7ae-495d-8666-4702017e675f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed6f1491354f9cd26ef6100ab8d21f2ace3133f4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031691"
---
# <a name="conformant-arrays"></a>Tableaux conformes

La taille d’un tableau conforme peut varier ou se conformer chaque fois que le client le transmet à une procédure distante sur le serveur. La définition d’interface dans le fichier MIDL de l’application permet au client de spécifier la taille du tableau chaque fois qu’il appelle la procédure distante. Utilisez des crochets vides ( \[ \] ) ou un astérisque entre crochets ( \[ \* \] ) dans la définition du tableau pour indiquer un tableau conforme.

L’exemple suivant contient la définition d’une procédure distante dans une interface d’un fichier MIDL. Le client spécifie la taille du tableau qu’il transmet au serveur à l’aide du paramètre *arraySize*.

``` syntax
[
    /*Attributes are defined here. */
]
interface MyInterface
{
    MyRemoteProc(
         long lArraySize,
         [size_is(lArraySize)] char achArray[*]
    );

    /* Other interface procedures are defined here. */
}
```

La définition d’interface utilise la \[ [**taille \_**](/windows/desktop/Midl/size-is) d’attribut MIDL \] pour spécifier la taille du tableau que le client transmet au serveur. Si vous préférez indiquer la valeur maximale des numéros d’index du tableau, utilisez plutôt l' \[ attribut [**Max \_ is**](/windows/desktop/Midl/max-is) \] . Pour plus d’informations sur ces attributs MIDL, consultez [attributs de tableau](array-attributes.md).

Le fragment de code suivant montre comment un client peut appeler la procédure distante définie dans le fichier MIDL précédent.


```C++
long lArrayLength = 20;
char achCharArray[20], achAnotherCharArray[200];

// Code to store 20 chars in achCharArray goes here.

MyRemoteProc(
    lArrayLength ,
    achCharArray);

lArrayLength = 200;

// Code to store 200 chars in achAnotherCharArray goes here.

MyRemoteProc(
    lArrayLength ,
    achAnotherCharArray);
```



Ce fragment appelle à deux reprises la procédure distante MyRemoteProc. Lors du premier appel, il passe un tableau de 20 éléments. Lors du deuxième appel, le client passe un tableau de 200 éléments.

 

 