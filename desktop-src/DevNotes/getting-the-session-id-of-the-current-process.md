---
description: L’exemple de code d’assembly x86 suivant obtient l’ID de session des services Terminal Server associé au processus en cours.
ms.assetid: 9fcb35cb-6813-46a5-aa38-e102f1b6b7dc
title: Obtention de l’ID de session du processus en cours
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac76865bcfe9144e8b95d4642385804aaf1af8fa
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110579"
---
# <a name="getting-the-session-id-of-the-current-process"></a><span data-ttu-id="80701-103">Obtention de l’ID de session du processus en cours</span><span class="sxs-lookup"><span data-stu-id="80701-103">Getting the Session ID of the Current Process</span></span>

<span data-ttu-id="80701-104">\[Les adresses mémoire spécifiées par cet exemple de code peuvent changer dans les versions ultérieures de Windows.</span><span class="sxs-lookup"><span data-stu-id="80701-104">\[The memory addresses specified by this example code may change in future releases of Windows.</span></span> <span data-ttu-id="80701-105">Pour vous assurer que votre application continuera à s’exécuter correctement à l’avenir, votre application doit appeler [**GetCurrentProcessId**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocessid) , puis [**ProcessIdToSessionId**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-processidtosessionid) au lieu de l’exemple de code suivant.\]</span><span class="sxs-lookup"><span data-stu-id="80701-105">To ensure that your application will continue to run correctly in the future, your application must call [**GetCurrentProcessId**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocessid) and then [**ProcessIdToSessionId**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-processidtosessionid) instead of the following sample code.\]</span></span>

<span data-ttu-id="80701-106">L’exemple de code d’assembly x86 suivant obtient l’ID de session des services Terminal Server associé au processus en cours.</span><span class="sxs-lookup"><span data-stu-id="80701-106">The following example x86 assembly code gets the Terminal Services session ID associated with the current process.</span></span>

``` syntax
mov     eax,fs:[00000018]
mov     eax,[eax+0x30]
mov     eax,[eax+0x1d4]
```

 

 
