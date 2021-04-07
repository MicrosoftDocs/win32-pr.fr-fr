---
title: InprocServer
description: Spécifie le chemin d’accès à la DLL du serveur in-process.
ms.assetid: f14cc8f7-e93e-4db8-8b0d-ea77a6301f33
keywords:
- Clé de Registre InprocServer COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5682693d711f734bbc60def8a711f11e2bad0ef9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103939951"
---
# <a name="inprocserver"></a><span data-ttu-id="426fe-104">InprocServer</span><span class="sxs-lookup"><span data-stu-id="426fe-104">InprocServer</span></span>

<span data-ttu-id="426fe-105">Spécifie le chemin d’accès à la DLL du serveur in-process.</span><span class="sxs-lookup"><span data-stu-id="426fe-105">Specifies the path to the in-process server DLL.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="426fe-106">Entrée de Registre</span><span class="sxs-lookup"><span data-stu-id="426fe-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      InprocServer
         (Default) = path
```

## <a name="remarks"></a><span data-ttu-id="426fe-107">Notes</span><span class="sxs-lookup"><span data-stu-id="426fe-107">Remarks</span></span>

<span data-ttu-id="426fe-108">L’entrée **InprocServer** est relativement rare pour les classes Insertables.</span><span class="sxs-lookup"><span data-stu-id="426fe-108">The **InprocServer** entry is relatively rare for insertable classes.</span></span>

<span data-ttu-id="426fe-109">Les serveurs in-process sont actuellement inscrits à l’aide de l’entrée de Registre **InprocServer** .</span><span class="sxs-lookup"><span data-stu-id="426fe-109">In-process servers are currently registered using the **InprocServer** registry entry.</span></span> <span data-ttu-id="426fe-110">Les serveurs in-process 32 bits et 64 bits doivent utiliser l’entrée [**InprocServer32**](inprocserver32.md) .</span><span class="sxs-lookup"><span data-stu-id="426fe-110">The 32-bit and 64-bit in-process servers should use the [**InprocServer32**](inprocserver32.md) entry.</span></span> <span data-ttu-id="426fe-111">Si un conteneur recherche un serveur in-process dans le registre, la version 16 bits a la priorité avec un conteneur de 16 bits et la version 32 bits a la priorité avec un conteneur de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="426fe-111">If a container is searching the registry for an in-process server, the 16-bit version has priority with a 16-bit container and 32-bit version has priority with a 32-bit container.</span></span>

## <a name="related-topics"></a><span data-ttu-id="426fe-112">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="426fe-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="426fe-113">**InprocServer32**</span><span class="sxs-lookup"><span data-stu-id="426fe-113">**InprocServer32**</span></span>](inprocserver32.md)
</dt> </dl>

 

 




