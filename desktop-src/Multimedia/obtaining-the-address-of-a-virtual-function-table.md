---
title: Obtention de l’adresse d’une table de fonctions virtuelles
description: Obtention de l’adresse d’une table de fonctions virtuelles
ms.assetid: c9e9e2df-75e6-4684-a465-6905e76b10a2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c0d618e75d2c3a4fcc2550fca7cb90bd2a51d2f
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124368268"
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



 

 




