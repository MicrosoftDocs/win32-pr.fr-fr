---
description: L’utilisation de virgules et de points-virgules peut être le problème de syntaxe le plus complexe dans le format de fichier, et cette utilisation est très stricte. Les virgules sont utilisées pour séparer les membres de tableau ; les points-virgules mettent fin à chaque élément de données.
ms.assetid: 82582213-907c-4760-a849-e6cf5f6d60bc
title: Utilisation de virgules et de points-virgules
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b44d20d4a8e99a75522fa3703d58d82f3bf4dfe130e530d18141b7f45e572717
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119044057"
---
# <a name="use-of-commas-and-semicolons"></a>Utilisation de virgules et de points-virgules

L’utilisation de virgules et de points-virgules peut être le problème de syntaxe le plus complexe dans le format de fichier, et cette utilisation est très stricte. Les virgules sont utilisées pour séparer les membres de tableau ; les points-virgules mettent fin à chaque élément de données.

Par exemple, si un modèle est défini de la manière suivante :


```
template mytemp {
DWORD myvar;
}
```



Une instance de ce modèle ressemble alors à ce qui suit :


```
mytemp dataTemp {
1;
}
```



Si un modèle contenant un autre modèle est défini de la manière suivante :


```
template mytemp {
DWORD myvar;
DWORD myvar2;
}
template container {
FLOAT aFloat;
mytemp aTemp;
}
```



Une instance de ce modèle ressemble alors à ce qui suit :


```
container dataContainer {
1.1;
2; 
3;;
}
```



Notez que la deuxième ligne qui représente le mytemp à l’intérieur d’un conteneur a deux points-virgules à la fin de la ligne. Le premier point-virgule indique la fin de l’élément de données, aTemp (dans le conteneur) et le deuxième point-virgule indique la fin du conteneur.

Si un tableau est défini de la manière suivante :


```
Template mytemp {

array DWORD myvar[3];

}
```



Une instance de cet exemple se présente comme suit :


```
mytemp aTemp {
1, 2, 3;
}
```



Dans l’exemple de tableau, il n’est pas nécessaire que les éléments de données soient séparés par des points-virgules, car ils sont délimités par des virgules. Le point-virgule à la fin marque la fin du tableau.

Prenons l’exemple d’un modèle qui contient un tableau d’éléments de données définis par un modèle.


```
template mytemp {
DWORD myvar;
DWORD myvar2;
}
template container {
DWORD count;
array mytemp tempArray[count];
}
```



Une instance de cela ressemble à l’exemple suivant.


```
container aContainer {
3;
1;2;,3;4;,5;6;;
}
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Encodage de texte](text-encoding.md)
</dt> </dl>

 

 



