---
title: InprocHandler32
description: InprocHandler32 spécifie si une application utilise un gestionnaire personnalisé dans la clé de Registre HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID.
ms.assetid: da611bb6-1f69-449a-9821-e2fbbe413a97
keywords:
- Clé de Registre InprocHandler32 COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be73a8b2577a554b0bb8b5ba5a851e630edbf90a
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406002"
---
# <a name="inprochandler32"></a><span data-ttu-id="5a530-104">InprocHandler32</span><span class="sxs-lookup"><span data-stu-id="5a530-104">InprocHandler32</span></span>

<span data-ttu-id="5a530-105">Spécifie si une application utilise un gestionnaire personnalisé.</span><span class="sxs-lookup"><span data-stu-id="5a530-105">Specifies whether an application uses a custom handler.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="5a530-106">Entrée de Registre</span><span class="sxs-lookup"><span data-stu-id="5a530-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      InprocHandler32 = handler.dll
```

## <a name="remarks"></a><span data-ttu-id="5a530-107">Remarques</span><span class="sxs-lookup"><span data-stu-id="5a530-107">Remarks</span></span>

<span data-ttu-id="5a530-108">Il s’agit d’une valeur de **reg \_ SZ** qui spécifie le gestionnaire personnalisé utilisé par l’application.</span><span class="sxs-lookup"><span data-stu-id="5a530-108">This is a **REG\_SZ** value that specifies the custom handler used by the application.</span></span> <span data-ttu-id="5a530-109">Si un gestionnaire personnalisé n’est pas utilisé, l’entrée doit être définie sur Ole32.dll.</span><span class="sxs-lookup"><span data-stu-id="5a530-109">If a custom handler is not used, the entry should be set to Ole32.dll.</span></span>

<span data-ttu-id="5a530-110">Si un conteneur recherche un gestionnaire personnalisé dans le registre, la version 16 bits a la priorité sur un conteneur de 16 bits et la version 32 bits a la priorité sur un conteneur de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="5a530-110">If a container is searching the registry for a custom handler, the 16-bit version has priority with a 16-bit container and the 32-bit version has priority with a 32-bit container.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5a530-111">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="5a530-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5a530-112">**InprocHandler**</span><span class="sxs-lookup"><span data-stu-id="5a530-112">**InprocHandler**</span></span>](inprochandler.md)
</dt> </dl>

 

 




