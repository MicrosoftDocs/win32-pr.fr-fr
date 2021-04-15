---
title: Obtention de l’adresse d’une table de fonctions virtuelles
description: Obtention de l’adresse d’une table de fonctions virtuelles
ms.assetid: c9e9e2df-75e6-4684-a465-6905e76b10a2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c0d618e75d2c3a4fcc2550fca7cb90bd2a51d2f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104507207"
---
# <a name="obtaining-the-address-of-a-virtual-function-table"></a>Obtention de l’adresse d’une table de fonctions virtuelles

Dans une application écrite en langage de programmation C, vous pouvez récupérer l’adresse de la structure **IAVIStreamVtbl** à l’aide de la fonction NewBall. Cette fonction retourne l’adresse d’une structure contenant un pointeur vers **IAVIStreamVtbl**. Les informations qui suivent le pointeur **IAVIStreamVtbl** spécifient les données utilisées en interne par AVIBall. Votre gestionnaire de flux peut ajouter ses propres informations après le pointeur **IAVIStreamVtbl** . Ces informations sont retournées dans les appels suivants à votre gestionnaire de flux.


```C++
PAVISTREAM WINAPI NewBall(VOID) 
{ 
    PAVIBALL pball; 
    pball = (PAVIBALL) GlobalAllocPtr(GHND, sizeof(AVIBALL)); 
    if (!pball) 
        return 0; 
    pball->lpvtbl = &AVIBallHandler; 
    pball->lpvtbl->Create((PAVISTREAM) pball, 0, 0); 
    return (PAVISTREAM) pball; 
} 
```



 

 




