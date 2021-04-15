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
# <a name="obtaining-the-address-of-a-virtual-function-table"></a><span data-ttu-id="d0d98-103">Obtention de l’adresse d’une table de fonctions virtuelles</span><span class="sxs-lookup"><span data-stu-id="d0d98-103">Obtaining the Address of a Virtual Function Table</span></span>

<span data-ttu-id="d0d98-104">Dans une application écrite en langage de programmation C, vous pouvez récupérer l’adresse de la structure **IAVIStreamVtbl** à l’aide de la fonction NewBall.</span><span class="sxs-lookup"><span data-stu-id="d0d98-104">In an application written in the C programming language, you can retrieve the address of the **IAVIStreamVtbl** structure by using the NewBall function.</span></span> <span data-ttu-id="d0d98-105">Cette fonction retourne l’adresse d’une structure contenant un pointeur vers **IAVIStreamVtbl**.</span><span class="sxs-lookup"><span data-stu-id="d0d98-105">This function returns the address of a structure containing a pointer to **IAVIStreamVtbl**.</span></span> <span data-ttu-id="d0d98-106">Les informations qui suivent le pointeur **IAVIStreamVtbl** spécifient les données utilisées en interne par AVIBall.</span><span class="sxs-lookup"><span data-stu-id="d0d98-106">Information following the **IAVIStreamVtbl** pointer specifies data used internally by AVIBall.</span></span> <span data-ttu-id="d0d98-107">Votre gestionnaire de flux peut ajouter ses propres informations après le pointeur **IAVIStreamVtbl** .</span><span class="sxs-lookup"><span data-stu-id="d0d98-107">Your stream handler can append its own information after the **IAVIStreamVtbl** pointer.</span></span> <span data-ttu-id="d0d98-108">Ces informations sont retournées dans les appels suivants à votre gestionnaire de flux.</span><span class="sxs-lookup"><span data-stu-id="d0d98-108">This information is returned in subsequent calls to your stream handler.</span></span>


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



 

 




