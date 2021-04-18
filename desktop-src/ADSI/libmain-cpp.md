---
title: LibMain. COTISATIONS
description: Dans l’exemple de composant fournisseur, un exemple de code de point d’entrée de DLL standard pour Adssmp.dll se trouve dans LibMain. cpp. Les routines prises en charge sont répertoriées dans le tableau suivant.
ms.assetid: aa05fbd1-509d-4ed6-8a49-1ce11ce54c0e
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e309d3c6454901b26f5ab67351033b39d73dd7aa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106526927"
---
# <a name="libmaincpp"></a><span data-ttu-id="1ccf3-104">LibMain. COTISATIONS</span><span class="sxs-lookup"><span data-stu-id="1ccf3-104">LIBMAIN.CPP</span></span>

<span data-ttu-id="1ccf3-105">Dans l’exemple de composant fournisseur, un exemple de code de point d’entrée de DLL standard pour Adssmp.dll se trouve dans LibMain. cpp.</span><span class="sxs-lookup"><span data-stu-id="1ccf3-105">In the example provider component, a code example of the standard DLL entry point for Adssmp.dll is in Libmain.cpp.</span></span> <span data-ttu-id="1ccf3-106">Les routines prises en charge sont répertoriées dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="1ccf3-106">Supported routines are listed in the following table.</span></span>



| <span data-ttu-id="1ccf3-107">Élément</span><span class="sxs-lookup"><span data-stu-id="1ccf3-107">Item</span></span>                                  | <span data-ttu-id="1ccf3-108">Description</span><span class="sxs-lookup"><span data-stu-id="1ccf3-108">Description</span></span>                                                              |
|---------------------------------------|--------------------------------------------------------------------------|
| <span data-ttu-id="1ccf3-109">**DllGetClassObject**</span><span class="sxs-lookup"><span data-stu-id="1ccf3-109">**DllGetClassObject**</span></span><br/>      | <span data-ttu-id="1ccf3-110">Point d’entrée de DLL standard pour la localisation des fabriques de classes.</span><span class="sxs-lookup"><span data-stu-id="1ccf3-110">Standard DLL entry point for locating class factories.</span></span><br/>        |
| <span data-ttu-id="1ccf3-111">**DllCanUnloadNow**</span><span class="sxs-lookup"><span data-stu-id="1ccf3-111">**DllCanUnloadNow**</span></span><br/>        | <span data-ttu-id="1ccf3-112">Point d’entrée de DLL standard pour déterminer si la DLL peut être déchargée.</span><span class="sxs-lookup"><span data-stu-id="1ccf3-112">Standard DLL entry point to determine if DLL can be unloaded.</span></span><br/> |
| <span data-ttu-id="1ccf3-113">**LibMain**</span><span class="sxs-lookup"><span data-stu-id="1ccf3-113">**LibMain**</span></span><br/>                | <span data-ttu-id="1ccf3-114">Point d’entrée de l’initialisation de la DLL standard.</span><span class="sxs-lookup"><span data-stu-id="1ccf3-114">Standard DLL initialization entry point.</span></span><br/>                      |
| <span data-ttu-id="1ccf3-115">**IsCompatibleOleVersion**</span><span class="sxs-lookup"><span data-stu-id="1ccf3-115">**IsCompatibleOleVersion**</span></span><br/> | <span data-ttu-id="1ccf3-116">Vérifiez la compatibilité avec l’exécution OLE.</span><span class="sxs-lookup"><span data-stu-id="1ccf3-116">Verify compatibility with the OLE run time.</span></span><br/>                   |
| <span data-ttu-id="1ccf3-117">**DllMain**</span><span class="sxs-lookup"><span data-stu-id="1ccf3-117">**DllMain**</span></span><br/>                | <span data-ttu-id="1ccf3-118">Point d’entrée pour la plupart des versions de Windows 2000 ou Windows NT.</span><span class="sxs-lookup"><span data-stu-id="1ccf3-118">Entry point for most Windows 2000 or Windows NT versions.</span></span><br/>     |



 

 

 





