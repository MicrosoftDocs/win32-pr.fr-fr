---
description: L’action RegisterExtensionInfo gère l’inscription des informations relatives à l’extension avec le système.
ms.assetid: 3c243ca3-9fa7-41ec-968e-7954d7d45432
title: Action RegisterExtensionInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0310344b6579ef65faac41238bb607ce98411b52
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517065"
---
# <a name="registerextensioninfo-action"></a><span data-ttu-id="0f46b-103">Action RegisterExtensionInfo</span><span class="sxs-lookup"><span data-stu-id="0f46b-103">RegisterExtensionInfo Action</span></span>

<span data-ttu-id="0f46b-104">L’action RegisterExtensionInfo gère l’inscription des informations relatives à l’extension avec le système.</span><span class="sxs-lookup"><span data-stu-id="0f46b-104">The RegisterExtensionInfo action manages the registration of extension related information with the system.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="0f46b-105">Restrictions de séquence</span><span class="sxs-lookup"><span data-stu-id="0f46b-105">Sequence Restrictions</span></span>

<span data-ttu-id="0f46b-106">L’action RegisterExtensionInfo doit être postérieure à l’action [InstallFiles](installfiles-action.md) et à l’action [UnregisterExtensionInfo](unregisterextensioninfo-action.md) .</span><span class="sxs-lookup"><span data-stu-id="0f46b-106">The RegisterExtensionInfo action must come after the [InstallFiles](installfiles-action.md) action and the [UnregisterExtensionInfo](unregisterextensioninfo-action.md) action.</span></span>

<span data-ttu-id="0f46b-107">Le séquencement des actions dans le groupe suivant est limité.</span><span class="sxs-lookup"><span data-stu-id="0f46b-107">The sequencing of the actions in the following group is restricted.</span></span> <span data-ttu-id="0f46b-108">Si un sous-ensemble de ces actions se produit ensemble dans une table de séquences, elles doivent avoir le même ordre de séquence relatif comme indiqué :</span><span class="sxs-lookup"><span data-stu-id="0f46b-108">If any subset of these actions occur together in a sequence table, they must have the same relative sequence order as shown:</span></span>

-   [<span data-ttu-id="0f46b-109">UnregisterClassInfo</span><span class="sxs-lookup"><span data-stu-id="0f46b-109">UnregisterClassInfo</span></span>](unregisterclassinfo-action.md)
-   [<span data-ttu-id="0f46b-110">UnregisterExtensionInfo</span><span class="sxs-lookup"><span data-stu-id="0f46b-110">UnregisterExtensionInfo</span></span>](unregisterextensioninfo-action.md)
-   [<span data-ttu-id="0f46b-111">UnregisterProgIdInfo</span><span class="sxs-lookup"><span data-stu-id="0f46b-111">UnregisterProgIdInfo</span></span>](unregisterprogidinfo-action.md)
-   [<span data-ttu-id="0f46b-112">UnregisterMIMEInfo</span><span class="sxs-lookup"><span data-stu-id="0f46b-112">UnregisterMIMEInfo</span></span>](unregistermimeinfo-action.md)
-   [<span data-ttu-id="0f46b-113">RegisterClassInfo</span><span class="sxs-lookup"><span data-stu-id="0f46b-113">RegisterClassInfo</span></span>](registerclassinfo-action.md)
-   <span data-ttu-id="0f46b-114">RegisterExtensionInfo</span><span class="sxs-lookup"><span data-stu-id="0f46b-114">RegisterExtensionInfo</span></span>
-   [<span data-ttu-id="0f46b-115">RegisterProgIdInfo</span><span class="sxs-lookup"><span data-stu-id="0f46b-115">RegisterProgIdInfo</span></span>](registerprogidinfo-action.md)
-   [<span data-ttu-id="0f46b-116">RegisterMIMEInfo</span><span class="sxs-lookup"><span data-stu-id="0f46b-116">RegisterMIMEInfo</span></span>](registermimeinfo-action.md)

<span data-ttu-id="0f46b-117">Par exemple, RegisterExtensionInfo doit venir après [UnregisterMIMEInfo](unregistermimeinfo-action.md) dans la table Sequence.</span><span class="sxs-lookup"><span data-stu-id="0f46b-117">For example, RegisterExtensionInfo must come after [UnregisterMIMEInfo](unregistermimeinfo-action.md) in the sequence table.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="0f46b-118">Messages ActionData</span><span class="sxs-lookup"><span data-stu-id="0f46b-118">ActionData Messages</span></span>



| <span data-ttu-id="0f46b-119">Champ</span><span class="sxs-lookup"><span data-stu-id="0f46b-119">Field</span></span> | <span data-ttu-id="0f46b-120">Description des données d’action</span><span class="sxs-lookup"><span data-stu-id="0f46b-120">Description of action data</span></span> |
|-------|----------------------------|
| <span data-ttu-id="0f46b-121">\[1\]</span><span class="sxs-lookup"><span data-stu-id="0f46b-121">\[1\]</span></span> | <span data-ttu-id="0f46b-122">Extension inscrite.</span><span class="sxs-lookup"><span data-stu-id="0f46b-122">Registered extension.</span></span>      |



 

## <a name="remarks"></a><span data-ttu-id="0f46b-123">Notes</span><span class="sxs-lookup"><span data-stu-id="0f46b-123">Remarks</span></span>

<span data-ttu-id="0f46b-124">Si le système prend en charge l’installation à la demande pour les serveurs d’extension, RegisterExtensionInfo inscrit tous les serveurs d’extension dans la [table d’extension](extension-table.md) associée aux fonctionnalités définies pour l’installation ou la publication.</span><span class="sxs-lookup"><span data-stu-id="0f46b-124">If the system supports installation-on-demand for extension servers, RegisterExtensionInfo registers all extension servers in the [Extension table](extension-table.md) associated with features set for installation or advertisement.</span></span> <span data-ttu-id="0f46b-125">Dans le cas contraire, cette action inscrit uniquement les serveurs d’extension associés aux fonctionnalités définies sur installation.</span><span class="sxs-lookup"><span data-stu-id="0f46b-125">Otherwise this action only registers extension servers associated with features set to installation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0f46b-126">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="0f46b-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0f46b-127">**Propriété ShellAdvtSupport**</span><span class="sxs-lookup"><span data-stu-id="0f46b-127">**ShellAdvtSupport property**</span></span>](shelladvtsupport.md)
</dt> </dl>

 

 



