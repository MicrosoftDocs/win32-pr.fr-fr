---
title: Création d’un pointeur d’objet
description: Création d’un pointeur d’objet
ms.assetid: b66a2725-6ba1-4aea-b165-fe3f4da00375
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f57451e2781a94642e61365d3a6c694758f4056
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104196607"
---
# <a name="creating-an-object-pointer"></a><span data-ttu-id="c9f67-103">Création d’un pointeur d’objet</span><span class="sxs-lookup"><span data-stu-id="c9f67-103">Creating an Object Pointer</span></span>

<span data-ttu-id="c9f67-104">AVIBall utilise la structure suivante comme pointeur d’objet.</span><span class="sxs-lookup"><span data-stu-id="c9f67-104">AVIBall uses the following structure as its object pointer.</span></span> <span data-ttu-id="c9f67-105">Le premier membre de cette structure pointe vers la table de fonctions virtuelles que AVIBall utilise pour accéder à ses fonctions.</span><span class="sxs-lookup"><span data-stu-id="c9f67-105">The first member of this structure points to the virtual function table that AVIBall uses to access its functions.</span></span> <span data-ttu-id="c9f67-106">Les applications peuvent effectuer un cast de cette structure vers le type de données PAVISTREAM.</span><span class="sxs-lookup"><span data-stu-id="c9f67-106">Applications can cast this structure to the PAVISTREAM data type.</span></span> <span data-ttu-id="c9f67-107">Les méthodes qui utilisent le type de données PAVISTREAM utilisent uniquement le pointeur vers la table de fonctions virtuelles.</span><span class="sxs-lookup"><span data-stu-id="c9f67-107">Methods that use the PAVISTREAM data type use only the pointer to the virtual function table.</span></span> <span data-ttu-id="c9f67-108">Les membres qui suivent le pointeur vers la table de fonctions virtuelles sont utilisés en interne par AVIBall.</span><span class="sxs-lookup"><span data-stu-id="c9f67-108">The members following the pointer to the virtual function table are used internally by AVIBall.</span></span>


```C++
typedef struct 
{ 
    IAVIStreamVtbl FAR * lpvtbl; 
 
    // Ball instance data. 
    ULONG     ulRefCount; 
    DWORD     fccType;  // is this audio/video? 
    int        width;    // size, in pixels, of each frame 
    int        height; 
    int        length;   // length, in frames 
    int        size; 
    COLORREF    color;    // ball color 
} AVIBALL, FAR * PAVIBALL; 

```



 

 




