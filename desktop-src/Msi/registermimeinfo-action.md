---
description: L’action RegisterMIMEInfo enregistre les informations de Registre liées à MIME auprès du système.
ms.assetid: 2ba88b5f-bd8a-4572-af82-9c0b91b9b6d9
title: Action RegisterMIMEInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41130d9e595cc2d95557470f79c217f3c3235d75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103756466"
---
# <a name="registermimeinfo-action"></a><span data-ttu-id="4c31e-103">Action RegisterMIMEInfo</span><span class="sxs-lookup"><span data-stu-id="4c31e-103">RegisterMIMEInfo Action</span></span>

<span data-ttu-id="4c31e-104">L’action RegisterMIMEInfo enregistre les informations de Registre liées à MIME auprès du système.</span><span class="sxs-lookup"><span data-stu-id="4c31e-104">The RegisterMIMEInfo action registers MIME-related registry information with the system.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="4c31e-105">Restrictions de séquence</span><span class="sxs-lookup"><span data-stu-id="4c31e-105">Sequence Restrictions</span></span>

<span data-ttu-id="4c31e-106">L’action RegisterMIMEInfo doit être postérieure à l’action [InstallFiles](installfiles-action.md) , à l’action [UnregisterMIMEInfo](unregistermimeinfo-action.md) , à l’action [RegisterClassInfo](registerclassinfo-action.md) et à l’action [RegisterExtensionInfo](registerextensioninfo-action.md) .</span><span class="sxs-lookup"><span data-stu-id="4c31e-106">The RegisterMIMEInfo action must come after the [InstallFiles](installfiles-action.md) action, [UnregisterMIMEInfo](unregistermimeinfo-action.md) action, [RegisterClassInfo](registerclassinfo-action.md) action, and the [RegisterExtensionInfo](registerextensioninfo-action.md) action.</span></span>

<span data-ttu-id="4c31e-107">Le séquencement des actions dans le groupe suivant est limité.</span><span class="sxs-lookup"><span data-stu-id="4c31e-107">The sequencing of the actions in the following group is restricted.</span></span> <span data-ttu-id="4c31e-108">Si un sous-ensemble de ces actions se produit ensemble dans une table de séquences, elles doivent avoir le même ordre de séquence relatif comme indiqué :</span><span class="sxs-lookup"><span data-stu-id="4c31e-108">If any subset of these actions occur together in a sequence table, they must have the same relative sequence order as shown:</span></span>

-   [<span data-ttu-id="4c31e-109">UnregisterClassInfo</span><span class="sxs-lookup"><span data-stu-id="4c31e-109">UnregisterClassInfo</span></span>](unregisterclassinfo-action.md)
-   [<span data-ttu-id="4c31e-110">UnregisterExtensionInfo</span><span class="sxs-lookup"><span data-stu-id="4c31e-110">UnregisterExtensionInfo</span></span>](unregisterextensioninfo-action.md)
-   [<span data-ttu-id="4c31e-111">UnregisterProgIdInfo</span><span class="sxs-lookup"><span data-stu-id="4c31e-111">UnregisterProgIdInfo</span></span>](unregisterprogidinfo-action.md)
-   [<span data-ttu-id="4c31e-112">UnregisterMIMEInfo</span><span class="sxs-lookup"><span data-stu-id="4c31e-112">UnregisterMIMEInfo</span></span>](unregistermimeinfo-action.md)
-   [<span data-ttu-id="4c31e-113">RegisterClassInfo</span><span class="sxs-lookup"><span data-stu-id="4c31e-113">RegisterClassInfo</span></span>](registerclassinfo-action.md)
-   [<span data-ttu-id="4c31e-114">RegisterExtensionInfo</span><span class="sxs-lookup"><span data-stu-id="4c31e-114">RegisterExtensionInfo</span></span>](registerextensioninfo-action.md)
-   [<span data-ttu-id="4c31e-115">RegisterProgIdInfo</span><span class="sxs-lookup"><span data-stu-id="4c31e-115">RegisterProgIdInfo</span></span>](registerprogidinfo-action.md)
-   <span data-ttu-id="4c31e-116">RegisterMIMEInfo</span><span class="sxs-lookup"><span data-stu-id="4c31e-116">RegisterMIMEInfo</span></span>

<span data-ttu-id="4c31e-117">Par exemple, RegisterMIMEInfo doit venir après [UnregisterMIMEInfo](unregistermimeinfo-action.md) dans la table Sequence.</span><span class="sxs-lookup"><span data-stu-id="4c31e-117">For example, RegisterMIMEInfo must come after [UnregisterMIMEInfo](unregistermimeinfo-action.md) in the sequence table.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="4c31e-118">Messages ActionData</span><span class="sxs-lookup"><span data-stu-id="4c31e-118">ActionData Messages</span></span>



| <span data-ttu-id="4c31e-119">Champ</span><span class="sxs-lookup"><span data-stu-id="4c31e-119">Field</span></span> | <span data-ttu-id="4c31e-120">Description des données d’action</span><span class="sxs-lookup"><span data-stu-id="4c31e-120">Description of action data</span></span>                   |
|-------|----------------------------------------------|
| <span data-ttu-id="4c31e-121">\[1\]</span><span class="sxs-lookup"><span data-stu-id="4c31e-121">\[1\]</span></span> | <span data-ttu-id="4c31e-122">Identificateur du type de contenu MIME inscrit.</span><span class="sxs-lookup"><span data-stu-id="4c31e-122">Identifier of registered MIME content type.</span></span>  |
| <span data-ttu-id="4c31e-123">\[2\]</span><span class="sxs-lookup"><span data-stu-id="4c31e-123">\[2\]</span></span> | <span data-ttu-id="4c31e-124">Extension associée au type de contenu MIME.</span><span class="sxs-lookup"><span data-stu-id="4c31e-124">Extension associated with MIME content type.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="4c31e-125">Notes</span><span class="sxs-lookup"><span data-stu-id="4c31e-125">Remarks</span></span>

<span data-ttu-id="4c31e-126">L’action RegisterMIMEInfo enregistre toutes les informations MIME pour les serveurs à partir de la [table MIME](mime-table.md) pour laquelle le serveur de classe ou d’extension correspondant a été sélectionné pour être installé.</span><span class="sxs-lookup"><span data-stu-id="4c31e-126">The RegisterMIMEInfo action registers all MIME information for servers from the [MIME table](mime-table.md) for which the corresponding class server or extension server has been selected to be installed.</span></span>

 

 



