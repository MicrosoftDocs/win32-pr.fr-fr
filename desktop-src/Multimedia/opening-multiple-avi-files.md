---
title: Ouverture de plusieurs fichiers AVI
description: Ouverture de plusieurs fichiers AVI
ms.assetid: 982bcea1-77b0-4a38-893d-1f506ffb18f5
keywords:
- initAVI fonction)
- termAVI fonction)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ac540d670b15eaf1befb1d2f253223e3571ecee
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127123569"
---
# <a name="opening-multiple-avi-files"></a>Ouverture de plusieurs fichiers AVI

Si votre application ouvre plusieurs fichiers, elle doit inclure des routines telles que les fonctions simples suivantes. L’application utilise la fonction « initAVI » lors de son initialisation et la fonction « termAVI » pendant son arrêt. Ces fonctions encapsulent simplement la fonction [**mciSendString**](/previous-versions//dd757161(v=vs.85)) .


```C++
// Initialize the MCIAVI driver. This returns TRUE if OK, 
// FALSE on error. 
 
BOOL initAVI(VOID) 
{ 
    // Perform additional initialization before loading first file. 
    return mciSendString("open digitalvideo", NULL, 0, NULL) == 0; 
} 
 
// Close the MCIAVI driver. 
void termAVI(VOID) 
{ 
    mciSendString("close digitalvideo", NULL, 0, NULL); 
} 
```



 

 