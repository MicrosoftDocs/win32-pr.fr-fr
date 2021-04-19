---
description: L’action RegisterProgIdInfo gère l’inscription des informations ProgId OLE avec le système.
ms.assetid: f6fd4d0d-d2dc-4953-9402-314c7932746b
title: Action RegisterProgIdInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4c7d53ca4c4125c6ebfc4d089c1c5a0934f9a58
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106534248"
---
# <a name="registerprogidinfo-action"></a><span data-ttu-id="b04a5-103">Action RegisterProgIdInfo</span><span class="sxs-lookup"><span data-stu-id="b04a5-103">RegisterProgIdInfo Action</span></span>

<span data-ttu-id="b04a5-104">L’action RegisterProgIdInfo gère l’inscription des informations ProgId OLE avec le système.</span><span class="sxs-lookup"><span data-stu-id="b04a5-104">The RegisterProgIdInfo action manages the registration of OLE ProgId information with the system.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="b04a5-105">Restrictions de séquence</span><span class="sxs-lookup"><span data-stu-id="b04a5-105">Sequence Restrictions</span></span>

<span data-ttu-id="b04a5-106">L’action RegisterProgIdInfo doit être postérieure à l’action [InstallFiles](installfiles-action.md) , à l’action [UnregisterProgIdInfo](unregisterprogidinfo-action.md) , à l’action [RegisterClassInfo](registerclassinfo-action.md) et à l’action [RegisterExtensionInfo](registerextensioninfo-action.md) .</span><span class="sxs-lookup"><span data-stu-id="b04a5-106">The RegisterProgIdInfo action must come after the [InstallFiles](installfiles-action.md) action, [UnregisterProgIdInfo](unregisterprogidinfo-action.md) action, [RegisterClassInfo](registerclassinfo-action.md) action, and the [RegisterExtensionInfo](registerextensioninfo-action.md) action.</span></span>

<span data-ttu-id="b04a5-107">Le séquencement des actions dans le groupe suivant est limité.</span><span class="sxs-lookup"><span data-stu-id="b04a5-107">The sequencing of the actions in the following group is restricted.</span></span> <span data-ttu-id="b04a5-108">Si un sous-ensemble de ces actions se produit ensemble dans une table de séquences, elles doivent avoir le même ordre de séquence relatif comme indiqué :</span><span class="sxs-lookup"><span data-stu-id="b04a5-108">If any subset of these actions occur together in a sequence table, they must have the same relative sequence order as shown:</span></span>

-   [<span data-ttu-id="b04a5-109">UnregisterClassInfo</span><span class="sxs-lookup"><span data-stu-id="b04a5-109">UnregisterClassInfo</span></span>](unregisterclassinfo-action.md)
-   [<span data-ttu-id="b04a5-110">UnregisterExtensionInfo</span><span class="sxs-lookup"><span data-stu-id="b04a5-110">UnregisterExtensionInfo</span></span>](unregisterextensioninfo-action.md)
-   [<span data-ttu-id="b04a5-111">UnregisterProgIdInfo</span><span class="sxs-lookup"><span data-stu-id="b04a5-111">UnregisterProgIdInfo</span></span>](unregisterprogidinfo-action.md)
-   [<span data-ttu-id="b04a5-112">UnregisterMIMEInfo</span><span class="sxs-lookup"><span data-stu-id="b04a5-112">UnregisterMIMEInfo</span></span>](unregistermimeinfo-action.md)
-   [<span data-ttu-id="b04a5-113">RegisterClassInfo</span><span class="sxs-lookup"><span data-stu-id="b04a5-113">RegisterClassInfo</span></span>](registerclassinfo-action.md)
-   [<span data-ttu-id="b04a5-114">RegisterExtensionInfo</span><span class="sxs-lookup"><span data-stu-id="b04a5-114">RegisterExtensionInfo</span></span>](registerextensioninfo-action.md)
-   <span data-ttu-id="b04a5-115">RegisterProgIdInfo</span><span class="sxs-lookup"><span data-stu-id="b04a5-115">RegisterProgIdInfo</span></span>
-   [<span data-ttu-id="b04a5-116">RegisterMIMEInfo</span><span class="sxs-lookup"><span data-stu-id="b04a5-116">RegisterMIMEInfo</span></span>](registermimeinfo-action.md)

<span data-ttu-id="b04a5-117">Par exemple, RegisterProgIdInfo doit venir après [RegisterExtensionInfo](registerextensioninfo-action.md) dans la table Sequence.</span><span class="sxs-lookup"><span data-stu-id="b04a5-117">For example, RegisterProgIdInfo must come after [RegisterExtensionInfo](registerextensioninfo-action.md) in the sequence table.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="b04a5-118">Messages ActionData</span><span class="sxs-lookup"><span data-stu-id="b04a5-118">ActionData Messages</span></span>



| <span data-ttu-id="b04a5-119">Champ</span><span class="sxs-lookup"><span data-stu-id="b04a5-119">Field</span></span> | <span data-ttu-id="b04a5-120">Description des données d’action</span><span class="sxs-lookup"><span data-stu-id="b04a5-120">Description of action data</span></span>                |
|-------|-------------------------------------------|
| <span data-ttu-id="b04a5-121">\[1\]</span><span class="sxs-lookup"><span data-stu-id="b04a5-121">\[1\]</span></span> | <span data-ttu-id="b04a5-122">Identificateur du programme enregistré.</span><span class="sxs-lookup"><span data-stu-id="b04a5-122">Program identifier of registered program.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="b04a5-123">Notes</span><span class="sxs-lookup"><span data-stu-id="b04a5-123">Remarks</span></span>

<span data-ttu-id="b04a5-124">L’action RegisterProgIdInfo enregistre toutes les informations ProgId pour les serveurs qui sont spécifiés dans la [table ProgID](progid-table.md) et pour lesquels le serveur de classe ou d’extension correspondant a été sélectionné pour être installé.</span><span class="sxs-lookup"><span data-stu-id="b04a5-124">The RegisterProgIdInfo action registers all ProgId information for servers that are specified in the [ProgId table](progid-table.md) and for which the corresponding class server or extension server has been selected to be installed.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b04a5-125">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b04a5-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b04a5-126">Table de classe</span><span class="sxs-lookup"><span data-stu-id="b04a5-126">Class table</span></span>](class-table.md)
</dt> <dt>

[<span data-ttu-id="b04a5-127">Table d’extension</span><span class="sxs-lookup"><span data-stu-id="b04a5-127">Extension table</span></span>](extension-table.md)
</dt> </dl>

 

 



