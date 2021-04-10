---
description: L’action UnregisterComPlus supprime les applications COM+ du Registre.
ms.assetid: bcedc436-a048-487e-9a84-e766da57a0b3
title: Action UnregisterComPlus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e32d39255229151757f7d6be0ada871f555f77e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103953166"
---
# <a name="unregistercomplus-action"></a><span data-ttu-id="92722-103">Action UnregisterComPlus</span><span class="sxs-lookup"><span data-stu-id="92722-103">UnregisterComPlus Action</span></span>

<span data-ttu-id="92722-104">L’action UnregisterComPlus supprime les applications COM+ du Registre.</span><span class="sxs-lookup"><span data-stu-id="92722-104">The UnregisterComPlus action removes COM+ applications from the registry.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="92722-105">Restrictions de séquence</span><span class="sxs-lookup"><span data-stu-id="92722-105">Sequence Restrictions</span></span>

<span data-ttu-id="92722-106">L’action [RegisterComPlus](registercomplus-action.md) doit suivre l' [action InstallFiles](installfiles-action.md) et l’action UnregisterComPlus.</span><span class="sxs-lookup"><span data-stu-id="92722-106">The [RegisterComPlus action](registercomplus-action.md) must follow the [InstallFiles action](installfiles-action.md) and the UnregisterComPlus action.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="92722-107">Messages ActionData</span><span class="sxs-lookup"><span data-stu-id="92722-107">ActionData Messages</span></span>



| <span data-ttu-id="92722-108">Champ</span><span class="sxs-lookup"><span data-stu-id="92722-108">Field</span></span> | <span data-ttu-id="92722-109">Description des données d’action</span><span class="sxs-lookup"><span data-stu-id="92722-109">Description of action data</span></span>                                    |
|-------|---------------------------------------------------------------|
| <span data-ttu-id="92722-110">\[1\]</span><span class="sxs-lookup"><span data-stu-id="92722-110">\[1\]</span></span> | <span data-ttu-id="92722-111">Identificateur d’application de l’application COM+ en cours de suppression.</span><span class="sxs-lookup"><span data-stu-id="92722-111">Application identifier of the COM+ application being removed.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="92722-112">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="92722-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="92722-113">Action RegisterComPlus</span><span class="sxs-lookup"><span data-stu-id="92722-113">RegisterComPlus action</span></span>](registercomplus-action.md)
</dt> <dt>

[<span data-ttu-id="92722-114">Table ComPlus</span><span class="sxs-lookup"><span data-stu-id="92722-114">Complus table</span></span>](complus-table.md)
</dt> <dt>

[<span data-ttu-id="92722-115">Installation d’une application COM+ avec la Windows Installer</span><span class="sxs-lookup"><span data-stu-id="92722-115">Installing a COM+ Application with the Windows Installer</span></span>](installing-a-com--application-with-the-windows-installer.md)
</dt> </dl>

 

 



