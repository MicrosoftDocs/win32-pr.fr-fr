---
title: " in, out, size_is prototype"
description: '\ in, out, size \_ is \ prototype utilise un tableau de caractères à un seul comptage qui est passé du client au serveur et du serveur au client.'
ms.assetid: bce9a36f-9f7c-4438-9b5a-15b8877f74c0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37829ce0d5a4bb44fefa038e9ce71773f9c4c9bd
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127311561"
---
# <a name="in-out-size_is-prototype"></a>\[in, out, la taille \_ est un \] prototype

Le prototype de fonction suivant utilise un tableau de caractères à un seul comptage qui reçoit les deux manières : du client au serveur et du serveur au client :

``` syntax
#define STRSIZE 500 //maximum string length

void Analyze(
    [in, out, length_is(*pcbSize), size_is(STRSIZE)] char  achInOut[],
    [in, out]  long *pcbSize);
```

En tant que \[ [](/windows/desktop/Midl/in) \] paramètre in, *achInOut* doit pointer vers un stockage valide côté client. Le développeur alloue de la mémoire associée au tableau côté client avant d’effectuer l’appel de procédure distante.

Les stubs utilisent la \[ [**\_ taille**](/windows/desktop/Midl/size-is) du \] paramètre *strsize* pour allouer de la mémoire sur le serveur, puis la longueur est le paramètre de la valeur de la fonction \[ [**\_**](/windows/desktop/Midl/length-is) \] de paramètre pour transmettre les éléments du tableau dans cette mémoire.  Le développeur doit s’assurer que le code client définit que la **\[ longueur \_ est \]** variable avant d’appeler la procédure distante.

Dans certains cas, l’utilisation de paramètres distincts au lieu d’une chaîne unique pour l’entrée et la sortie est plus efficace et offre une certaine flexibilité. Cela est illustré dans l’exemple suivant :

``` syntax
/* client */ 
char achInOut[STRSIZE];
long cbSize;
...
gets_s(achInOut, STRSIZE);       // get patient input
cbSize = strlen(achInOut) + 1;   // transmit '\0' too
Analyze(achInOut, &cbSize);
```

Dans l’exemple précédent, le tableau de caractères achInOut est également utilisé comme \[ paramètre de [**sortie**](/windows/desktop/Midl/out-idl) \] . En C, le nom du tableau est équivalent à l’utilisation d’un pointeur. Par défaut, tous les pointeurs de niveau supérieur sont des pointeurs de référence, ils ne changent pas dans la valeur et pointent vers la même zone de mémoire sur le client avant et après l’appel. Toute la mémoire à laquelle la procédure distante accède doit correspondre à la taille que le client spécifie avant l’appel, ou les stubs génèrent une exception.

Avant de retourner, la fonction analyze sur le serveur doit réinitialiser le paramètre *PCB* pour indiquer le nombre d’éléments que le serveur transmet au client comme indiqué ci-dessous :

``` syntax
/* server */ 
Analyze(char * str, long * pcbSize)
{
   ...
   *pcbSize = strlen(str) + 1; // transmit '\0' too
   return;
}
```

 

 