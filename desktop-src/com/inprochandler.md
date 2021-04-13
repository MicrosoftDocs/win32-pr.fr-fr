---
title: InprocHandler
description: Spécifie si une application utilise un gestionnaire personnalisé.
ms.assetid: b371b331-148b-46f2-a21e-b88b285bcfc9
keywords:
- Clé de Registre InprocHandler COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a8c19089ece43496465351b44e9faa8793ba893
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104380198"
---
# <a name="inprochandler"></a><span data-ttu-id="f09eb-104">InprocHandler</span><span class="sxs-lookup"><span data-stu-id="f09eb-104">InprocHandler</span></span>

<span data-ttu-id="f09eb-105">Spécifie si une application utilise un gestionnaire personnalisé.</span><span class="sxs-lookup"><span data-stu-id="f09eb-105">Specifies whether an application uses a custom handler.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="f09eb-106">Entrée de Registre</span><span class="sxs-lookup"><span data-stu-id="f09eb-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      InprocHandler = handler.dll
```

## <a name="remarks"></a><span data-ttu-id="f09eb-107">Notes</span><span class="sxs-lookup"><span data-stu-id="f09eb-107">Remarks</span></span>

<span data-ttu-id="f09eb-108">Il s’agit d’une valeur de **reg \_ SZ** qui spécifie le gestionnaire personnalisé utilisé par l’application.</span><span class="sxs-lookup"><span data-stu-id="f09eb-108">This is a **REG\_SZ** value that specifies the custom handler used by the application.</span></span> <span data-ttu-id="f09eb-109">Si un gestionnaire personnalisé n’est pas utilisé, l’entrée doit être définie sur Ole32.dll.</span><span class="sxs-lookup"><span data-stu-id="f09eb-109">If a custom handler is not used, the entry should be set to Ole32.dll.</span></span>

<span data-ttu-id="f09eb-110">Si un conteneur recherche un gestionnaire personnalisé dans le registre, la version 16 bits a la priorité sur un conteneur de 16 bits et la version 32 bits a la priorité sur un conteneur de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="f09eb-110">If a container is searching the registry for a custom handler, the 16-bit version has priority with a 16-bit container and the 32-bit version has priority with a 32-bit container.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f09eb-111">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f09eb-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f09eb-112">**InprocHandler32**</span><span class="sxs-lookup"><span data-stu-id="f09eb-112">**InprocHandler32**</span></span>](inprochandler32.md)
</dt> </dl>

 

 




