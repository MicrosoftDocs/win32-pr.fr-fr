---
description: L’action UnregisterExtensionInfo gère la suppression des informations relatives à l’extension à partir du Registre système.
ms.assetid: 62bb9d17-c221-4bd2-bd7f-9930e28bb946
title: Action UnregisterExtensionInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85d069a686c5f0e517a0cc9556634895216dd8cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106539333"
---
# <a name="unregisterextensioninfo-action"></a><span data-ttu-id="8664e-103">Action UnregisterExtensionInfo</span><span class="sxs-lookup"><span data-stu-id="8664e-103">UnregisterExtensionInfo Action</span></span>

<span data-ttu-id="8664e-104">L’action UnregisterExtensionInfo gère la suppression des informations relatives à l’extension à partir du Registre système.</span><span class="sxs-lookup"><span data-stu-id="8664e-104">The UnregisterExtensionInfo action manages the removal of extension-related information from the system registry.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="8664e-105">Restrictions de séquence</span><span class="sxs-lookup"><span data-stu-id="8664e-105">Sequence Restrictions</span></span>

<span data-ttu-id="8664e-106">L’action UnregisterExtensionInfo doit venir après l’action [InstallInitialize](installinitialize-action.md) et avant l’action [RegisterExtensionInfo](registerextensioninfo-action.md) .</span><span class="sxs-lookup"><span data-stu-id="8664e-106">The UnregisterExtensionInfo action must come after the [InstallInitialize](installinitialize-action.md) action and before the [RegisterExtensionInfo](registerextensioninfo-action.md) action.</span></span>

<span data-ttu-id="8664e-107">[RemoveRegistryValues](removeregistryvalues-action.md) doit précéder UnregisterExtensionInfo dans la séquence.</span><span class="sxs-lookup"><span data-stu-id="8664e-107">[RemoveRegistryValues](removeregistryvalues-action.md) must come before UnregisterExtensionInfo in the sequence.</span></span>

<span data-ttu-id="8664e-108">Le séquencement des actions dans le groupe suivant est limité.</span><span class="sxs-lookup"><span data-stu-id="8664e-108">The sequencing of the actions in the following group is restricted.</span></span> <span data-ttu-id="8664e-109">Si un sous-ensemble de ces actions se produit ensemble dans une table de séquences, elles doivent avoir le même ordre de séquence relatif comme indiqué :</span><span class="sxs-lookup"><span data-stu-id="8664e-109">If any subset of these actions occur together in a sequence table, they must have the same relative sequence order as shown:</span></span>

-   [<span data-ttu-id="8664e-110">UnregisterClassInfo</span><span class="sxs-lookup"><span data-stu-id="8664e-110">UnregisterClassInfo</span></span>](unregisterclassinfo-action.md)
-   <span data-ttu-id="8664e-111">UnregisterExtensionInfo</span><span class="sxs-lookup"><span data-stu-id="8664e-111">UnregisterExtensionInfo</span></span>
-   [<span data-ttu-id="8664e-112">UnregisterProgIdInfo</span><span class="sxs-lookup"><span data-stu-id="8664e-112">UnregisterProgIdInfo</span></span>](unregisterprogidinfo-action.md)
-   [<span data-ttu-id="8664e-113">UnregisterMIMEInfo</span><span class="sxs-lookup"><span data-stu-id="8664e-113">UnregisterMIMEInfo</span></span>](unregistermimeinfo-action.md)
-   [<span data-ttu-id="8664e-114">RegisterClassInfo</span><span class="sxs-lookup"><span data-stu-id="8664e-114">RegisterClassInfo</span></span>](registerclassinfo-action.md)
-   [<span data-ttu-id="8664e-115">RegisterExtensionInfo</span><span class="sxs-lookup"><span data-stu-id="8664e-115">RegisterExtensionInfo</span></span>](registerextensioninfo-action.md)
-   [<span data-ttu-id="8664e-116">RegisterProgIdInfo</span><span class="sxs-lookup"><span data-stu-id="8664e-116">RegisterProgIdInfo</span></span>](registerprogidinfo-action.md)
-   [<span data-ttu-id="8664e-117">RegisterMIMEInfo</span><span class="sxs-lookup"><span data-stu-id="8664e-117">RegisterMIMEInfo</span></span>](registermimeinfo-action.md)

<span data-ttu-id="8664e-118">Par exemple, UnregisterExtensionInfo doit précéder [UnregisterProgIdInfo](unregisterprogidinfo-action.md) dans la table Sequence.</span><span class="sxs-lookup"><span data-stu-id="8664e-118">For example, UnregisterExtensionInfo must come before [UnregisterProgIdInfo](unregisterprogidinfo-action.md) in the sequence table.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="8664e-119">Messages ActionData</span><span class="sxs-lookup"><span data-stu-id="8664e-119">ActionData Messages</span></span>



| <span data-ttu-id="8664e-120">Champ</span><span class="sxs-lookup"><span data-stu-id="8664e-120">Field</span></span> | <span data-ttu-id="8664e-121">Description des données d’action</span><span class="sxs-lookup"><span data-stu-id="8664e-121">Description of action data</span></span> |
|-------|----------------------------|
| <span data-ttu-id="8664e-122">\[1\]</span><span class="sxs-lookup"><span data-stu-id="8664e-122">\[1\]</span></span> | <span data-ttu-id="8664e-123">Extension supprimée.</span><span class="sxs-lookup"><span data-stu-id="8664e-123">Removed extension.</span></span>         |



 

## <a name="remarks"></a><span data-ttu-id="8664e-124">Notes</span><span class="sxs-lookup"><span data-stu-id="8664e-124">Remarks</span></span>

<span data-ttu-id="8664e-125">Si le système ne prend pas en charge l’installation à la demande des serveurs d’extension, UnregisterExtensionInfo supprime tous les serveurs d’extension de la [table d’extension](extension-table.md) associée à une fonctionnalité désinstallée ou à une fonctionnalité installée comme publiée à partir du Registre.</span><span class="sxs-lookup"><span data-stu-id="8664e-125">If the system does not support the install-on-demand of extension servers, UnregisterExtensionInfo removes all extension servers in the [Extension table](extension-table.md) associated with either an uninstalled feature or a feature installed as advertised from the registry.</span></span> <span data-ttu-id="8664e-126">Dans le cas contraire, cette action supprime les serveurs d’extension associés à une fonctionnalité qui est sélectionnée pour être supprimée du Registre.</span><span class="sxs-lookup"><span data-stu-id="8664e-126">Otherwise, this action removes the extension servers associated with a feature that is selected to be removed from the registry.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8664e-127">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="8664e-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8664e-128">**Propriété ShellAdvtSupport**</span><span class="sxs-lookup"><span data-stu-id="8664e-128">**ShellAdvtSupport Property**</span></span>](shelladvtsupport.md)
</dt> </dl>

 

 



