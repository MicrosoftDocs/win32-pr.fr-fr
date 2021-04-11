---
description: L’action UnregisterMIMEInfo annule l’enregistrement des informations de Registre liées à MIME à partir du système. L’action annule l’enregistrement des informations MIME pour les serveurs de la table MIME pour lesquels la fonctionnalité correspondante est actuellement sélectionnée pour être désinstallée.
ms.assetid: 9a5c12da-e78f-4c99-9b82-d41624593c61
title: Action UnregisterMIMEInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02c1ca7c0cd12d9ec6236a0c0298ba793713f5ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210921"
---
# <a name="unregistermimeinfo-action"></a><span data-ttu-id="245f1-104">Action UnregisterMIMEInfo</span><span class="sxs-lookup"><span data-stu-id="245f1-104">UnregisterMIMEInfo Action</span></span>

<span data-ttu-id="245f1-105">L’action UnregisterMIMEInfo annule l’enregistrement des informations de Registre liées à MIME à partir du système.</span><span class="sxs-lookup"><span data-stu-id="245f1-105">The UnregisterMIMEInfo action unregisters MIME-related registry information from the system.</span></span> <span data-ttu-id="245f1-106">L’action annule l’enregistrement des informations MIME pour les serveurs de la [table MIME](mime-table.md) pour lesquels la fonctionnalité correspondante est actuellement sélectionnée pour être désinstallée.</span><span class="sxs-lookup"><span data-stu-id="245f1-106">The action unregisters MIME information for servers from the [MIME table](mime-table.md) for which the corresponding feature is currently selected to be uninstalled.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="245f1-107">Restrictions de séquence</span><span class="sxs-lookup"><span data-stu-id="245f1-107">Sequence Restrictions</span></span>

<span data-ttu-id="245f1-108">L’action UnregisterMIMEInfo doit venir après l’action [InstallInitialize](installinitialize-action.md) , [UnregisterClassInfo](unregisterclassinfo-action.md) action, [UnregisterExtensionInfo](unregisterextensioninfo-action.md) action et avant l’action [RegisterMIMEInfo](registermimeinfo-action.md) .</span><span class="sxs-lookup"><span data-stu-id="245f1-108">The UnregisterMIMEInfo action must come after the [InstallInitialize](installinitialize-action.md) action, [UnregisterClassInfo](unregisterclassinfo-action.md) action, [UnregisterExtensionInfo](unregisterextensioninfo-action.md) action, and before the [RegisterMIMEInfo](registermimeinfo-action.md) action.</span></span>

<span data-ttu-id="245f1-109">[RemoveRegistryValues](removeregistryvalues-action.md) doit précéder UnregisterMIMEInfo dans la séquence.</span><span class="sxs-lookup"><span data-stu-id="245f1-109">[RemoveRegistryValues](removeregistryvalues-action.md) must come before UnregisterMIMEInfo in the sequence.</span></span>

<span data-ttu-id="245f1-110">Le séquencement des actions dans le groupe suivant est limité.</span><span class="sxs-lookup"><span data-stu-id="245f1-110">The sequencing of the actions in the following group is restricted.</span></span> <span data-ttu-id="245f1-111">Si un sous-ensemble de ces actions se produit ensemble dans une table de séquences, elles doivent avoir le même ordre de séquence relatif comme indiqué :</span><span class="sxs-lookup"><span data-stu-id="245f1-111">If any subset of these actions occur together in a sequence table, they must have the same relative sequence order as shown:</span></span>

-   [<span data-ttu-id="245f1-112">UnregisterClassInfo</span><span class="sxs-lookup"><span data-stu-id="245f1-112">UnregisterClassInfo</span></span>](unregisterclassinfo-action.md)
-   [<span data-ttu-id="245f1-113">UnregisterExtensionInfo</span><span class="sxs-lookup"><span data-stu-id="245f1-113">UnregisterExtensionInfo</span></span>](unregisterextensioninfo-action.md)
-   [<span data-ttu-id="245f1-114">UnregisterProgIdInfo</span><span class="sxs-lookup"><span data-stu-id="245f1-114">UnregisterProgIdInfo</span></span>](unregisterprogidinfo-action.md)
-   <span data-ttu-id="245f1-115">UnregisterMIMEInfo</span><span class="sxs-lookup"><span data-stu-id="245f1-115">UnregisterMIMEInfo</span></span>
-   [<span data-ttu-id="245f1-116">RegisterClassInfo</span><span class="sxs-lookup"><span data-stu-id="245f1-116">RegisterClassInfo</span></span>](registerclassinfo-action.md)
-   [<span data-ttu-id="245f1-117">RegisterExtensionInfo</span><span class="sxs-lookup"><span data-stu-id="245f1-117">RegisterExtensionInfo</span></span>](registerextensioninfo-action.md)
-   [<span data-ttu-id="245f1-118">RegisterProgIdInfo</span><span class="sxs-lookup"><span data-stu-id="245f1-118">RegisterProgIdInfo</span></span>](registerprogidinfo-action.md)
-   [<span data-ttu-id="245f1-119">RegisterMIMEInfo</span><span class="sxs-lookup"><span data-stu-id="245f1-119">RegisterMIMEInfo</span></span>](registermimeinfo-action.md)

<span data-ttu-id="245f1-120">Par exemple, UnregisterMIMEInfo doit précéder [RegisterExtensionInfo](registerextensioninfo-action.md) dans la table Sequence.</span><span class="sxs-lookup"><span data-stu-id="245f1-120">For example, UnregisterMIMEInfo must come before [RegisterExtensionInfo](registerextensioninfo-action.md) in the sequence table.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="245f1-121">Messages ActionData</span><span class="sxs-lookup"><span data-stu-id="245f1-121">ActionData Messages</span></span>



| <span data-ttu-id="245f1-122">Champ</span><span class="sxs-lookup"><span data-stu-id="245f1-122">Field</span></span> | <span data-ttu-id="245f1-123">Description des données d’action</span><span class="sxs-lookup"><span data-stu-id="245f1-123">Description of action data</span></span>                    |
|-------|-----------------------------------------------|
| <span data-ttu-id="245f1-124">\[1\]</span><span class="sxs-lookup"><span data-stu-id="245f1-124">\[1\]</span></span> | <span data-ttu-id="245f1-125">Identificateur du type de contenu MIME non inscrit.</span><span class="sxs-lookup"><span data-stu-id="245f1-125">Identifier of unregistered MIME content type.</span></span> |
| <span data-ttu-id="245f1-126">\[2\]</span><span class="sxs-lookup"><span data-stu-id="245f1-126">\[2\]</span></span> | <span data-ttu-id="245f1-127">Extension associée au type de contenu MIME.</span><span class="sxs-lookup"><span data-stu-id="245f1-127">Extension associated with MIME content type.</span></span>  |



 

 

 



