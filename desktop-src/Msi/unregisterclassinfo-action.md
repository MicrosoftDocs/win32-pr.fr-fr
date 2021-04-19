---
description: L’action UnregisterClassInfo gère la suppression des informations de classe COM du Registre système. Elle utilise la table AppId.
ms.assetid: 579a69ee-92cd-4d4c-a007-998ec042f9fc
title: Action UnregisterClassInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57ee701925e07e4f74439efb45da00d430d90304
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106545161"
---
# <a name="unregisterclassinfo-action"></a><span data-ttu-id="61bd8-104">Action UnregisterClassInfo</span><span class="sxs-lookup"><span data-stu-id="61bd8-104">UnregisterClassInfo Action</span></span>

<span data-ttu-id="61bd8-105">L’action UnregisterClassInfo gère la suppression des informations de classe COM du Registre système.</span><span class="sxs-lookup"><span data-stu-id="61bd8-105">The UnregisterClassInfo action manages the removal of COM class information from the system registry.</span></span> <span data-ttu-id="61bd8-106">Elle utilise la [table AppID](appid-table.md).</span><span class="sxs-lookup"><span data-stu-id="61bd8-106">It uses the [AppId table](appid-table.md).</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="61bd8-107">Restrictions de séquence</span><span class="sxs-lookup"><span data-stu-id="61bd8-107">Sequence Restrictions</span></span>

<span data-ttu-id="61bd8-108">L’action UnregisterClassInfo doit venir après l’action [InstallInitialize](installinitialize-action.md) et avant l’action [RegisterClassInfo](registerclassinfo-action.md) .</span><span class="sxs-lookup"><span data-stu-id="61bd8-108">The UnregisterClassInfo action must come after the [InstallInitialize](installinitialize-action.md) action and before the [RegisterClassInfo](registerclassinfo-action.md) action.</span></span>

<span data-ttu-id="61bd8-109">[RemoveRegistryValues](removeregistryvalues-action.md) doit précéder UnregisterClassInfo dans la séquence.</span><span class="sxs-lookup"><span data-stu-id="61bd8-109">[RemoveRegistryValues](removeregistryvalues-action.md) must come before UnregisterClassInfo in the sequence.</span></span>

<span data-ttu-id="61bd8-110">Le séquencement des actions dans le groupe suivant est limité.</span><span class="sxs-lookup"><span data-stu-id="61bd8-110">The sequencing of the actions in the following group is restricted.</span></span> <span data-ttu-id="61bd8-111">Si un sous-ensemble de ces actions se produit ensemble dans une table de séquences, elles doivent se produire dans la même séquence relative, comme indiqué dans le tableau suivant :</span><span class="sxs-lookup"><span data-stu-id="61bd8-111">If any subset of these actions occur together in a sequence table, they must occur in the same relative sequence as shown in the following table:</span></span>

-   <span data-ttu-id="61bd8-112">UnregisterClassInfo</span><span class="sxs-lookup"><span data-stu-id="61bd8-112">UnregisterClassInfo</span></span>
-   [<span data-ttu-id="61bd8-113">UnregisterExtensionInfo</span><span class="sxs-lookup"><span data-stu-id="61bd8-113">UnregisterExtensionInfo</span></span>](unregisterextensioninfo-action.md)
-   [<span data-ttu-id="61bd8-114">UnregisterProgIdInfo</span><span class="sxs-lookup"><span data-stu-id="61bd8-114">UnregisterProgIdInfo</span></span>](unregisterprogidinfo-action.md)
-   [<span data-ttu-id="61bd8-115">UnregisterMIMEInfo</span><span class="sxs-lookup"><span data-stu-id="61bd8-115">UnregisterMIMEInfo</span></span>](unregistermimeinfo-action.md)
-   [<span data-ttu-id="61bd8-116">RegisterClassInfo</span><span class="sxs-lookup"><span data-stu-id="61bd8-116">RegisterClassInfo</span></span>](registerclassinfo-action.md)
-   [<span data-ttu-id="61bd8-117">RegisterExtensionInfo</span><span class="sxs-lookup"><span data-stu-id="61bd8-117">RegisterExtensionInfo</span></span>](registerextensioninfo-action.md)
-   [<span data-ttu-id="61bd8-118">RegisterProgIdInfo</span><span class="sxs-lookup"><span data-stu-id="61bd8-118">RegisterProgIdInfo</span></span>](registerprogidinfo-action.md)
-   [<span data-ttu-id="61bd8-119">RegisterMIMEInfo</span><span class="sxs-lookup"><span data-stu-id="61bd8-119">RegisterMIMEInfo</span></span>](registermimeinfo-action.md)

<span data-ttu-id="61bd8-120">Par exemple, [RegisterExtensionInfo](registerextensioninfo-action.md) doit précéder UnregisterClassInfo dans la table Sequence.</span><span class="sxs-lookup"><span data-stu-id="61bd8-120">For example, [RegisterExtensionInfo](registerextensioninfo-action.md) must come before UnregisterClassInfo in the sequence table.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="61bd8-121">Messages ActionData</span><span class="sxs-lookup"><span data-stu-id="61bd8-121">ActionData Messages</span></span>



| <span data-ttu-id="61bd8-122">Champ</span><span class="sxs-lookup"><span data-stu-id="61bd8-122">Field</span></span> | <span data-ttu-id="61bd8-123">Description des données d’action</span><span class="sxs-lookup"><span data-stu-id="61bd8-123">Description of action data</span></span>      |
|-------|---------------------------------|
| <span data-ttu-id="61bd8-124">\[1\]</span><span class="sxs-lookup"><span data-stu-id="61bd8-124">\[1\]</span></span> | <span data-ttu-id="61bd8-125">GUID de la classe COM non inscrite.</span><span class="sxs-lookup"><span data-stu-id="61bd8-125">GUID of unregistered COM class.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="61bd8-126">Notes</span><span class="sxs-lookup"><span data-stu-id="61bd8-126">Remarks</span></span>

<span data-ttu-id="61bd8-127">Le programme d’installation définit la propriété [**OLEAdvtSupport**](oleadvtsupport.md) sur true lorsque le système de l’utilisateur actuel a été mis à niveau pour fonctionner avec Install-on-demand via com.</span><span class="sxs-lookup"><span data-stu-id="61bd8-127">The installer sets the [**OLEAdvtSupport**](oleadvtsupport.md) property to true when the current user's system has been upgraded to work with install-on-demand through COM.</span></span> <span data-ttu-id="61bd8-128">Si le système ne prend pas en charge l’installation à la demande via COM, UnregisterClassInfo supprime toutes les classes COM listées dans la [table de classe](class-table.md) associée aux fonctionnalités ou fonctionnalités installées comme publiées à partir du Registre système.</span><span class="sxs-lookup"><span data-stu-id="61bd8-128">If the system does not support install-on-demand through COM, UnregisterClassInfo removes all COM classes listed in the [Class table](class-table.md) associated with either uninstalled features or features installed as advertised from the system registry.</span></span> <span data-ttu-id="61bd8-129">Dans le cas contraire, cette action supprime uniquement les classes COM associées aux fonctionnalités sélectionnées pour être désinstallées dans le registre système.</span><span class="sxs-lookup"><span data-stu-id="61bd8-129">Otherwise, this action removes only the COM classes associated with features selected to be uninstalled from the system registry.</span></span>

 

 



