---
title: Tableaux fixes
description: Si votre interface spécifie un tableau avec un nombre spécifique d’éléments en tant que paramètre, elle utilise un tableau fixe. Lors de l’utilisation de MIDL, vous définissez des tableaux fixes de la même façon que vous les définissez en C. Vous spécifiez le type, le nom et la taille du tableau.
ms.assetid: b9a2fa0b-1386-43e1-ab55-0a57cd8d1f18
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1040e417cc896b9f4bd2271dc69e23033332354357b2aad32053724d94b79035
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118929978"
---
# <a name="fixed-arrays"></a>Tableaux fixes

Si votre interface spécifie un tableau avec un nombre spécifique d’éléments en tant que paramètre, elle utilise un tableau fixe. Lors de l’utilisation de MIDL, vous définissez des tableaux fixes de la même façon que vous les définissez en C. Vous spécifiez le type, le nom et la taille du tableau.

L’exemple suivant montre comment définir un tableau fixe.

``` syntax
[
    /*Attributes are defined here. */
]
interface MyInterface
{
    const long ARRAY_SIZE = 1000;

    MyRemoteProc(char achArray[ARRAY_SIZE]);

    /* Other interface procedures are defined here. */
}
```

Lorsqu’un programme client transmet un tableau fixe à un programme serveur, le stub client envoie l’intégralité du tableau au stub serveur. Le stub serveur alloue de la mémoire pour le tableau et stocke les données de tableau qu’il reçoit sur le réseau dans la mémoire allouée. Il passe ensuite le tableau à la procédure distante sur le serveur. Le serveur peut modifier les données dans le tableau.

Lorsque la procédure distante se termine, le stub serveur renvoie le contenu du tableau au client. Le stub client copie les données qu’il a reçues du stub serveur dans le tableau d’origine. Le programme client peut ensuite utiliser les données comme si elles avaient reçu les données d’un appel de procédure local.

 

 




