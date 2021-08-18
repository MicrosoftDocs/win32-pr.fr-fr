---
title: Tableaux variables
description: Dans MIDL, les tableaux variables ont une taille fixe. Ils permettent aux clients de transmettre différentes parties de tableaux des clients aux serveurs. La taille de la partie de tableau peut varier d’un appel à l’appel. Toutefois, la taille du tableau global est fixe.
ms.assetid: 31c4bc63-de55-4937-832e-8dde9bcc47b9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3919eed28ef7a9c888d7c23e4ebe12a1db39c97b18fa325c6daf8a4cd62d6554
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119010547"
---
# <a name="varying-arrays"></a>Tableaux variables

Dans MIDL, les tableaux variables ont une taille fixe. Ils permettent aux clients de transmettre différentes parties de tableaux des clients aux serveurs. La taille de la partie de tableau peut varier d’un appel à l’appel. Toutefois, la taille du tableau global est fixe.

Par exemple, l’exemple suivant illustre la définition d’une procédure distante dans une interface dans un fichier MIDL. La taille du tableau que le client transmet au serveur est fixe par la taille de tableau constante \_ . L’interface spécifie la partie du tableau que le client transmet au serveur dans les paramètres firstElement et chunkSize.

``` syntax
[
    /*Attributes are defined here. */
]
interface MyInterface
{
    const long ARRAY_SIZE = 1000;

    MyRemoteProc(
        [in] long lFirstElement,
        [in] long lChunkSize,
        [in, first_is(lFirstElement), 
          length_is(lChunkSize)] char achArray[ARRAY_SIZE]
    );

    /* Other interface procedures are defined here. */
}
```

La définition d’interface utilise \[ [**tout d’abord \_**](/windows/desktop/Midl/first-is) l’attribut MIDL pour \] spécifier le numéro d’index du premier élément de la partie du tableau que le client transmet au serveur. La \[ [**longueur \_ est**](/windows/desktop/Midl/length-is) \] attribute spécifie le nombre total d’éléments de tableau que le client passe. Pour plus d’informations sur ces attributs MIDL, consultez [attributs de tableau](array-attributes.md).

Le fragment de code suivant montre comment un client peut appeler la procédure distante définie dans le fichier MIDL précédent.


```C++
long lFirstArrayElementNumber = 20;
long lTotalElementsPassed = 100;
char achCharArray[ARRAY_SIZE];

// Code to store chars in the array goes here.

MyRemoteProc(
    lFirstArrayElementNumber ,
    lTotalElementsPassed , 
    achCharArray);

firstArrayElementNumber = 120;
totalElementsPassed = 200;

MyRemoteProc(
    lFirstArrayElementNumber ,
    lTotalElementsPassed , 
    achCharArray);
```



Ce fragment appelle à deux reprises la procédure distante MyRemoteProc. Lors du premier appel, il transmet les éléments de tableau numérotés de 20 à 119, comme indiqué par les valeurs des variables firstArrayElementNumber et totalElementsPassed. Lors du deuxième appel, le client passe les éléments de tableau numérotés de 120 à 319.

 

 