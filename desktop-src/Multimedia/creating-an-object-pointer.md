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
# <a name="creating-an-object-pointer"></a>Création d’un pointeur d’objet

AVIBall utilise la structure suivante comme pointeur d’objet. Le premier membre de cette structure pointe vers la table de fonctions virtuelles que AVIBall utilise pour accéder à ses fonctions. Les applications peuvent effectuer un cast de cette structure vers le type de données PAVISTREAM. Les méthodes qui utilisent le type de données PAVISTREAM utilisent uniquement le pointeur vers la table de fonctions virtuelles. Les membres qui suivent le pointeur vers la table de fonctions virtuelles sont utilisés en interne par AVIBall.


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



 

 




