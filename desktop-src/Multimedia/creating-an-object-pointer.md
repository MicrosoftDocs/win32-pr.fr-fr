---
title: Création d’un pointeur d’objet
description: Création d’un pointeur d’objet
ms.assetid: b66a2725-6ba1-4aea-b165-fe3f4da00375
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 586ba0b8c9ee261e29f21ed58c84193f4cc89d1399c62d75d82a2c0a49075dcc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119144682"
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



 

 




