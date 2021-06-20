---
title: InprocHandler
description: InprocHandler spécifie si une application utilise un gestionnaire personnalisé dans la clé de Registre HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID.
ms.assetid: b371b331-148b-46f2-a21e-b88b285bcfc9
keywords:
- Clé de Registre InprocHandler COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aea1ca0d5eb5dec58a36578d268d7020a963a95e
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112404732"
---
# <a name="inprochandler"></a><span data-ttu-id="a594b-104">InprocHandler</span><span class="sxs-lookup"><span data-stu-id="a594b-104">InprocHandler</span></span>

<span data-ttu-id="a594b-105">Spécifie si une application utilise un gestionnaire personnalisé.</span><span class="sxs-lookup"><span data-stu-id="a594b-105">Specifies whether an application uses a custom handler.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="a594b-106">Entrée de Registre</span><span class="sxs-lookup"><span data-stu-id="a594b-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      InprocHandler = handler.dll
```

## <a name="remarks"></a><span data-ttu-id="a594b-107">Remarques</span><span class="sxs-lookup"><span data-stu-id="a594b-107">Remarks</span></span>

<span data-ttu-id="a594b-108">Il s’agit d’une valeur de **reg \_ SZ** qui spécifie le gestionnaire personnalisé utilisé par l’application.</span><span class="sxs-lookup"><span data-stu-id="a594b-108">This is a **REG\_SZ** value that specifies the custom handler used by the application.</span></span> <span data-ttu-id="a594b-109">Si un gestionnaire personnalisé n’est pas utilisé, l’entrée doit être définie sur Ole32.dll.</span><span class="sxs-lookup"><span data-stu-id="a594b-109">If a custom handler is not used, the entry should be set to Ole32.dll.</span></span>

<span data-ttu-id="a594b-110">Si un conteneur recherche un gestionnaire personnalisé dans le registre, la version 16 bits a la priorité sur un conteneur de 16 bits et la version 32 bits a la priorité sur un conteneur de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="a594b-110">If a container is searching the registry for a custom handler, the 16-bit version has priority with a 16-bit container and the 32-bit version has priority with a 32-bit container.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a594b-111">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a594b-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a594b-112">**InprocHandler32**</span><span class="sxs-lookup"><span data-stu-id="a594b-112">**InprocHandler32**</span></span>](inprochandler32.md)
</dt> </dl>

 

 




