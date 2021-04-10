---
description: L’action RegisterComPlus inscrit des applications COM+.
ms.assetid: e42bb993-7079-4d5b-bb2e-c958e99e705e
title: Action RegisterComPlus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb824d67e776a99f8cd05c56f73f171f436c71d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104115502"
---
# <a name="registercomplus-action"></a><span data-ttu-id="17e17-103">Action RegisterComPlus</span><span class="sxs-lookup"><span data-stu-id="17e17-103">RegisterComPlus Action</span></span>

<span data-ttu-id="17e17-104">L’action RegisterComPlus inscrit des applications COM+.</span><span class="sxs-lookup"><span data-stu-id="17e17-104">The RegisterComPlus action registers COM+ applications.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="17e17-105">Restrictions de séquence</span><span class="sxs-lookup"><span data-stu-id="17e17-105">Sequence Restrictions</span></span>

<span data-ttu-id="17e17-106">L’action RegisterComPlus doit suivre l' [action InstallFiles](installfiles-action.md) et l' [action UnregisterComPlus](unregistercomplus-action.md).</span><span class="sxs-lookup"><span data-stu-id="17e17-106">The RegisterComPlus action must follow the [InstallFiles action](installfiles-action.md) and the [UnregisterComPlus action](unregistercomplus-action.md).</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="17e17-107">Messages ActionData</span><span class="sxs-lookup"><span data-stu-id="17e17-107">ActionData Messages</span></span>



| <span data-ttu-id="17e17-108">Champ</span><span class="sxs-lookup"><span data-stu-id="17e17-108">Field</span></span> | <span data-ttu-id="17e17-109">Description des données d’action</span><span class="sxs-lookup"><span data-stu-id="17e17-109">Description of action data</span></span>              |
|-------|-----------------------------------------|
| <span data-ttu-id="17e17-110">\[1\]</span><span class="sxs-lookup"><span data-stu-id="17e17-110">\[1\]</span></span> | <span data-ttu-id="17e17-111">ID d’application de l’application COM+.</span><span class="sxs-lookup"><span data-stu-id="17e17-111">Application ID of the COM+ application.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="17e17-112">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="17e17-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="17e17-113">Table ComPlus</span><span class="sxs-lookup"><span data-stu-id="17e17-113">Complus table</span></span>](complus-table.md)
</dt> <dt>

[<span data-ttu-id="17e17-114">Action UnregisterComPlus</span><span class="sxs-lookup"><span data-stu-id="17e17-114">UnregisterComPlus action</span></span>](unregistercomplus-action.md)
</dt> <dt>

[<span data-ttu-id="17e17-115">Installation d’une application COM+ avec la Windows Installer</span><span class="sxs-lookup"><span data-stu-id="17e17-115">Installing a COM+ Application with the Windows Installer</span></span>](installing-a-com--application-with-the-windows-installer.md)
</dt> </dl>

 

 



