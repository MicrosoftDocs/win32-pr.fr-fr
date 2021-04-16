---
description: L’exemple de code suivant illustre l’utilisation d’un objet mutex pour déterminer si MSN Explorer est connecté.
ms.assetid: ec52a61c-9d2c-4327-977b-fb13d042bc37
title: Détermination de l’état de connexion de MSN
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba2d7af3511035c997493f0439a8635c1a928a75
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523959"
---
# <a name="determining-if-msn-is-in-the-sign-in-state"></a><span data-ttu-id="27d30-103">Détermination de l’état de connexion de MSN</span><span class="sxs-lookup"><span data-stu-id="27d30-103">Determining if MSN Is in the Sign-in State</span></span>

<span data-ttu-id="27d30-104">L’exemple de code suivant illustre l’utilisation d’un objet mutex pour déterminer si MSN Explorer est connecté.</span><span class="sxs-lookup"><span data-stu-id="27d30-104">The following code example shows the usage of a mutex object to determine if MSN Explorer is signed in.</span></span> <span data-ttu-id="27d30-105">Lorsque vous avez fini d’utiliser le descripteur, veillez à appeler la fonction [**CloseHandle**](/windows/win32/api/handleapi/nf-handleapi-closehandle) .</span><span class="sxs-lookup"><span data-stu-id="27d30-105">When you have finished using the handle, be sure to call the [**CloseHandle**](/windows/win32/api/handleapi/nf-handleapi-closehandle) function.</span></span>

> [!Note]  
> <span data-ttu-id="27d30-106">Cet objet mutex peut être utilisé pour la vérification de MSN Explorer 7. État de la connexion *x* .</span><span class="sxs-lookup"><span data-stu-id="27d30-106">This mutex object is available for use in checking MSN Explorer 7.*x* sign-in status.</span></span> <span data-ttu-id="27d30-107">Elle n’est peut-être pas disponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="27d30-107">It may be unavailable in subsequent versions.</span></span>

 


```C++
    HANDLE hMSNSignedInMutex;

    hMSNSignedInMutex = OpenMutex(SYNCHRONIZE, FALSE, 
        "{ECCC50B5-064B-4693-B104-925714A4C74B}");

    if (hMSNSignedInMutex != NULL)
    {
        // MSN Explorer is signed in
    }
```



 

 
