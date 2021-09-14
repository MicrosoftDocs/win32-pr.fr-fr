---
title: Combinaison d’attributs de tableau
description: Les attributs de champ peuvent être fournis dans différentes combinaisons tant que le stub peut utiliser les informations pour déterminer la taille du tableau et le nombre d’octets à transmettre au serveur.
ms.assetid: ff4f971f-9e46-4454-9d57-d8ebdf70b261
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffc60777caeb3950e37fe167fe09ecc181d88b8f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127011429"
---
# <a name="combining-array-attributes"></a>Combinaison d’attributs de tableau

Les attributs de champ peuvent être fournis dans différentes combinaisons tant que le stub peut utiliser les informations pour déterminer la taille du tableau et le nombre d’octets à transmettre au serveur. Les relations entre les attributs sont définies à l’aide des formules suivantes :

``` syntax
size_is = max_is + 1;
length_is = last_is - first_is + 1;
```

Les valeurs associées aux attributs doivent respecter plusieurs règles de sens commun basées sur ces formules. Il s’agit des règles suivantes :

-   Ne spécifiez pas un premier si la \[ valeur d’index [**\_ est**](/windows/desktop/Midl/first-is) \] inférieure à zéro ou si la \[ [**dernière \_**](/windows/desktop/Midl/last-is) \] valeur supérieure à \[ [**Max \_ est**](/windows/desktop/Midl/max-is) \] .
-   Ne spécifiez pas de taille négative pour un tableau. Définissez le premier et le dernier élément afin qu’ils génèrent une valeur de longueur égale ou supérieure à zéro. Définissez la \[ valeur [**Max \_ is**](/windows/desktop/Midl/max-is) \] pour que la taille soit égale à zéro ou supérieure. Si MIDL a été appelé avec l’option de vérification des limites [**/Error**](/windows/desktop/Midl/-error) \_ , le stub lève une exception lorsque la taille est inférieure à zéro, ou la longueur transmise est inférieure à zéro.
-   N’utilisez pas la \[ [**longueur \_ :**](/windows/desktop/Midl/length-is) \] et le \[ [**dernier \_ est**](/windows/desktop/Midl/last-is) un \] attribut en même temps, ou la \[ **taille \_** est \] et le \[ **dernier attribut \_ est** \] en même temps.

En raison de la relation étroite en C entre les tableaux et les pointeurs, MIDL vous permet également de déclarer des tableaux dans des listes de paramètres à l’aide de la notation par pointeur. MIDL traite un paramètre qui est un pointeur vers un type en tant que tableau de ce type si le paramètre possède l’un des attributs couramment associés aux tableaux.

``` syntax
/* IDL file */
[ 
  uuid(ba209999-0c6c-11d2-97cf-00c04f8eea45)
  version(6.0) 
]
interface arraytest
{
  void fArray6([in] short sSize, 
               [in, out, size_is(sSize)] char * p1);
  void fArray7([in] short sSize, 
               [in, out, size_is(sSize)] char achArray[]);
}
```

Dans l’exemple précédent, les paramètres de tableau et de pointeur dans les fonctions fArray6 et fArray7 sont équivalents.

 

 