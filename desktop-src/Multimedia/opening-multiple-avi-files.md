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
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "106518008"
---
# <a name="opening-multiple-avi-files"></a><span data-ttu-id="ce238-105">Ouverture de plusieurs fichiers AVI</span><span class="sxs-lookup"><span data-stu-id="ce238-105">Opening Multiple AVI Files</span></span>

<span data-ttu-id="ce238-106">Si votre application ouvre plusieurs fichiers, elle doit inclure des routines telles que les fonctions simples suivantes.</span><span class="sxs-lookup"><span data-stu-id="ce238-106">If your application opens multiple files, it should include routines such as the following simple functions.</span></span> <span data-ttu-id="ce238-107">L’application utilise la fonction « initAVI » lors de son initialisation et la fonction « termAVI » pendant son arrêt.</span><span class="sxs-lookup"><span data-stu-id="ce238-107">The application would use the "initAVI" function during its initialization and the "termAVI" function during its termination.</span></span> <span data-ttu-id="ce238-108">Ces fonctions encapsulent simplement la fonction [**mciSendString**](/previous-versions//dd757161(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="ce238-108">These functions simply wrap the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function.</span></span>


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



 

 