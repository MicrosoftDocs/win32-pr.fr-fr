---
description: L’action RegisterClassInfo gère l’inscription des informations de classe COM auprès du système. Elle utilise la table AppId.
ms.assetid: f8b60a75-9c0e-41c5-b6af-6a05a26b2d71
title: Action RegisterClassInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd916772bc236dfc86df336347514c10d5dfbce7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106527458"
---
# <a name="registerclassinfo-action"></a><span data-ttu-id="82769-104">Action RegisterClassInfo</span><span class="sxs-lookup"><span data-stu-id="82769-104">RegisterClassInfo Action</span></span>

<span data-ttu-id="82769-105">L’action RegisterClassInfo gère l’inscription des informations de classe COM auprès du système.</span><span class="sxs-lookup"><span data-stu-id="82769-105">The RegisterClassInfo action manages the registration of COM class information with the system.</span></span> <span data-ttu-id="82769-106">Elle utilise la [table AppID](appid-table.md).</span><span class="sxs-lookup"><span data-stu-id="82769-106">It uses the [AppId table](appid-table.md).</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="82769-107">Restrictions de séquence</span><span class="sxs-lookup"><span data-stu-id="82769-107">Sequence Restrictions</span></span>

<span data-ttu-id="82769-108">L’action RegisterClassInfo doit être postérieure à l’action [InstallFiles](installfiles-action.md) et à l’action [UnregisterClassInfo](unregisterclassinfo-action.md) .</span><span class="sxs-lookup"><span data-stu-id="82769-108">The RegisterClassInfo action must come after the [InstallFiles](installfiles-action.md) action and the [UnregisterClassInfo](unregisterclassinfo-action.md) action.</span></span>

<span data-ttu-id="82769-109">Le séquencement des actions dans le groupe suivant est limité.</span><span class="sxs-lookup"><span data-stu-id="82769-109">The sequencing of the actions in the following group is restricted.</span></span> <span data-ttu-id="82769-110">Si un sous-ensemble de ces actions se produit ensemble dans une table de séquences, elles doivent avoir le même ordre de séquence relatif comme indiqué :</span><span class="sxs-lookup"><span data-stu-id="82769-110">If any subset of these actions occur together in a sequence table, they must have the same relative sequence order as shown:</span></span>

-   [<span data-ttu-id="82769-111">UnregisterClassInfo</span><span class="sxs-lookup"><span data-stu-id="82769-111">UnregisterClassInfo</span></span>](unregisterclassinfo-action.md)
-   [<span data-ttu-id="82769-112">UnregisterExtensionInfo</span><span class="sxs-lookup"><span data-stu-id="82769-112">UnregisterExtensionInfo</span></span>](unregisterextensioninfo-action.md)
-   [<span data-ttu-id="82769-113">UnregisterProgIdInfo</span><span class="sxs-lookup"><span data-stu-id="82769-113">UnregisterProgIdInfo</span></span>](unregisterprogidinfo-action.md)
-   [<span data-ttu-id="82769-114">UnregisterMIMEInfo</span><span class="sxs-lookup"><span data-stu-id="82769-114">UnregisterMIMEInfo</span></span>](unregistermimeinfo-action.md)
-   <span data-ttu-id="82769-115">RegisterClassInfo</span><span class="sxs-lookup"><span data-stu-id="82769-115">RegisterClassInfo</span></span>
-   [<span data-ttu-id="82769-116">RegisterExtensionInfo</span><span class="sxs-lookup"><span data-stu-id="82769-116">RegisterExtensionInfo</span></span>](registerextensioninfo-action.md)
-   [<span data-ttu-id="82769-117">RegisterProgIdInfo</span><span class="sxs-lookup"><span data-stu-id="82769-117">RegisterProgIdInfo</span></span>](registerprogidinfo-action.md)
-   [<span data-ttu-id="82769-118">RegisterMIMEInfo</span><span class="sxs-lookup"><span data-stu-id="82769-118">RegisterMIMEInfo</span></span>](registermimeinfo-action.md)

<span data-ttu-id="82769-119">Par exemple, RegisterClassInfo doit venir après [UnregisterMIMEInfo](unregistermimeinfo-action.md) dans la table Sequence.</span><span class="sxs-lookup"><span data-stu-id="82769-119">For example, RegisterClassInfo must come after [UnregisterMIMEInfo](unregistermimeinfo-action.md) in the sequence table.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="82769-120">Messages ActionData</span><span class="sxs-lookup"><span data-stu-id="82769-120">ActionData Messages</span></span>



| <span data-ttu-id="82769-121">Champ</span><span class="sxs-lookup"><span data-stu-id="82769-121">Field</span></span> | <span data-ttu-id="82769-122">Description des données d’action</span><span class="sxs-lookup"><span data-stu-id="82769-122">Description of action data</span></span>                          |
|-------|-----------------------------------------------------|
| <span data-ttu-id="82769-123">\[1\]</span><span class="sxs-lookup"><span data-stu-id="82769-123">\[1\]</span></span> | <span data-ttu-id="82769-124">Identificateur de classe GUID du serveur COM inscrit.</span><span class="sxs-lookup"><span data-stu-id="82769-124">GUID class identifier of the registered COM server.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="82769-125">Notes</span><span class="sxs-lookup"><span data-stu-id="82769-125">Remarks</span></span>

<span data-ttu-id="82769-126">Si le système prend en charge l’installation à la demande pour les serveurs OLE, RegisterClassInfo inscrit toutes les classes COM dans la [table de classes](class-table.md) associée à une fonctionnalité sélectionnée pour être installée ou publiée.</span><span class="sxs-lookup"><span data-stu-id="82769-126">If the system supports install-on-demand for OLE servers, RegisterClassInfo registers all COM classes in the [Class table](class-table.md) associated with a feature selected to be installed or advertised.</span></span> <span data-ttu-id="82769-127">Dans le cas contraire, cette action inscrit uniquement les classes COM associées à une fonctionnalité sélectionnée pour l’installation.</span><span class="sxs-lookup"><span data-stu-id="82769-127">Otherwise this action only registers the COM classes associated with a feature selected for installation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="82769-128">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="82769-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="82769-129">**Propriété OLEAdvtSupport**</span><span class="sxs-lookup"><span data-stu-id="82769-129">**OLEAdvtSupport property**</span></span>](oleadvtsupport.md)
</dt> </dl>

 

 



