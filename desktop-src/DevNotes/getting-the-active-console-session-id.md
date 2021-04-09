---
description: La définition winternl. h suivante est l’adresse mémoire statique de l’ID de session active des services Terminal Server. Cet ID de session de la console active n’est pas défini dans les versions du système d’exploitation Microsoft Windows antérieures à Windows XP.
ms.assetid: f3022ab8-60ea-490b-a87d-cc1afc99d26f
title: Obtention de l’ID de session de la console active
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 936db3f8038348864fc90fc55eeb4287a67c45d6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103860997"
---
# <a name="getting-the-active-console-session-id"></a><span data-ttu-id="18116-104">Obtention de l’ID de session de la console active</span><span class="sxs-lookup"><span data-stu-id="18116-104">Getting the Active Console Session ID</span></span>

<span data-ttu-id="18116-105">La définition winternl. h suivante est l’adresse mémoire statique de l’ID de session active des services Terminal Server.</span><span class="sxs-lookup"><span data-stu-id="18116-105">The following Winternl.h definition is the static memory address of the active Terminal Services console session ID.</span></span> <span data-ttu-id="18116-106">Cet ID de session de la console active n’est pas défini dans les versions du système d’exploitation Microsoft Windows antérieures à Windows XP.</span><span class="sxs-lookup"><span data-stu-id="18116-106">This active console session ID is not defined in versions of the Microsoft Windows operating system earlier than Windows XP.</span></span>

> [!Note]  
> <span data-ttu-id="18116-107">Cette définition peut changer dans les versions ultérieures de Windows.</span><span class="sxs-lookup"><span data-stu-id="18116-107">This definition may change in future releases of Windows.</span></span> <span data-ttu-id="18116-108">Pour vous assurer que votre application continuera à s’exécuter correctement à l’avenir, votre application doit appeler [**WTSGetActiveConsoleSessionId**](/windows/win32/api/winbase/nf-winbase-wtsgetactiveconsolesessionid).</span><span class="sxs-lookup"><span data-stu-id="18116-108">To ensure that your application will continue to run correctly in the future, your application must call [**WTSGetActiveConsoleSessionId**](/windows/win32/api/winbase/nf-winbase-wtsgetactiveconsolesessionid).</span></span>

 

``` syntax
#define INTERNAL_TS_ACTIVE_CONSOLE_ID    
        (*((volatile ULONG*)(0x7ffe02d8)))
```

 

 
