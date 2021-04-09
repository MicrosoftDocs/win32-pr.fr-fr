---
description: L’action UnregisterProgIdInfo gère l’annulation de l’inscription des informations ProgId OLE avec le système.
ms.assetid: c9837845-4ffc-4496-8330-11b46d27ec7a
title: Action UnregisterProgIdInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff880c1d339fc3db3db50bd34d3afb828f65ec07
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103869037"
---
# <a name="unregisterprogidinfo-action"></a><span data-ttu-id="05f02-103">Action UnregisterProgIdInfo</span><span class="sxs-lookup"><span data-stu-id="05f02-103">UnregisterProgIdInfo Action</span></span>

<span data-ttu-id="05f02-104">L’action UnregisterProgIdInfo gère l’annulation de l’inscription des informations ProgId OLE avec le système.</span><span class="sxs-lookup"><span data-stu-id="05f02-104">The UnregisterProgIdInfo action manages the unregistration of OLE ProgId information with the system.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="05f02-105">Restrictions de séquence</span><span class="sxs-lookup"><span data-stu-id="05f02-105">Sequence Restrictions</span></span>

<span data-ttu-id="05f02-106">L’action UnregisterProgIdInfo doit venir après l’action [InstallInitialize](installinitialize-action.md) , [UnregisterClassInfo](unregisterclassinfo-action.md) action, [UnregisterExtensioninfo](unregisterextensioninfo-action.md) action et avant l’action [RegisterProgIdInfo](registerprogidinfo-action.md) .</span><span class="sxs-lookup"><span data-stu-id="05f02-106">The UnregisterProgIdInfo action must come after the [InstallInitialize](installinitialize-action.md) action, [UnregisterClassInfo](unregisterclassinfo-action.md) action, [UnregisterExtensioninfo](unregisterextensioninfo-action.md) action, and before the [RegisterProgIdInfo](registerprogidinfo-action.md) action.</span></span>

<span data-ttu-id="05f02-107">[RemoveRegistryValues](removeregistryvalues-action.md) doit précéder UnregisterProgIdInfo dans la séquence.</span><span class="sxs-lookup"><span data-stu-id="05f02-107">[RemoveRegistryValues](removeregistryvalues-action.md) must come before UnregisterProgIdInfo in the sequence.</span></span>

<span data-ttu-id="05f02-108">Le séquencement des actions dans le groupe suivant est limité.</span><span class="sxs-lookup"><span data-stu-id="05f02-108">The sequencing of the actions in the following group is restricted.</span></span> <span data-ttu-id="05f02-109">Si un sous-ensemble de ces actions se produit ensemble dans une table de séquences, elles doivent avoir le même ordre de séquence relatif comme indiqué :</span><span class="sxs-lookup"><span data-stu-id="05f02-109">If any subset of these actions occur together in a sequence table, they must have the same relative sequence order as shown:</span></span>

-   [<span data-ttu-id="05f02-110">UnregisterClassInfo</span><span class="sxs-lookup"><span data-stu-id="05f02-110">UnregisterClassInfo</span></span>](unregisterclassinfo-action.md)
-   [<span data-ttu-id="05f02-111">UnregisterExtensioninfo</span><span class="sxs-lookup"><span data-stu-id="05f02-111">UnregisterExtensioninfo</span></span>](unregisterextensioninfo-action.md)
-   <span data-ttu-id="05f02-112">UnregisterProgIdInfo</span><span class="sxs-lookup"><span data-stu-id="05f02-112">UnregisterProgIdInfo</span></span>
-   [<span data-ttu-id="05f02-113">UnregisterMIMEInfo</span><span class="sxs-lookup"><span data-stu-id="05f02-113">UnregisterMIMEInfo</span></span>](unregistermimeinfo-action.md)
-   [<span data-ttu-id="05f02-114">RegisterClassInfo</span><span class="sxs-lookup"><span data-stu-id="05f02-114">RegisterClassInfo</span></span>](registerclassinfo-action.md)
-   [<span data-ttu-id="05f02-115">RegisterExtensionInfo</span><span class="sxs-lookup"><span data-stu-id="05f02-115">RegisterExtensionInfo</span></span>](registerextensioninfo-action.md)
-   [<span data-ttu-id="05f02-116">RegisterProgIdInfo</span><span class="sxs-lookup"><span data-stu-id="05f02-116">RegisterProgIdInfo</span></span>](registerprogidinfo-action.md)
-   [<span data-ttu-id="05f02-117">RegisterMIMEInfo</span><span class="sxs-lookup"><span data-stu-id="05f02-117">RegisterMIMEInfo</span></span>](registermimeinfo-action.md)

<span data-ttu-id="05f02-118">Par exemple, UnregisterProgIdInfo doit précéder [UnregisterMIMEInfo](unregistermimeinfo-action.md) dans la table Sequence.</span><span class="sxs-lookup"><span data-stu-id="05f02-118">For example, UnregisterProgIdInfo must come before [UnregisterMIMEInfo](unregistermimeinfo-action.md) in the sequence table.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="05f02-119">Messages ActionData</span><span class="sxs-lookup"><span data-stu-id="05f02-119">ActionData Messages</span></span>



| <span data-ttu-id="05f02-120">Champ</span><span class="sxs-lookup"><span data-stu-id="05f02-120">Field</span></span> | <span data-ttu-id="05f02-121">Description des données d’action</span><span class="sxs-lookup"><span data-stu-id="05f02-121">Description of action data</span></span>                |
|-------|-------------------------------------------|
| <span data-ttu-id="05f02-122">\[1\]</span><span class="sxs-lookup"><span data-stu-id="05f02-122">\[1\]</span></span> | <span data-ttu-id="05f02-123">Identificateur du programme enregistré.</span><span class="sxs-lookup"><span data-stu-id="05f02-123">Program identifier of registered program.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="05f02-124">Notes</span><span class="sxs-lookup"><span data-stu-id="05f02-124">Remarks</span></span>

<span data-ttu-id="05f02-125">L’action UnregisterProgIdInfo supprime les informations ProgId du Registre ([table ProgID](progid-table.md)) pour les fonctionnalités qui sont connectées aux informations d’extension ([table d’extension](extension-table.md)) ou les informations de classe (table de[classes](class-table.md)) et qui sont actuellement sélectionnées pour être désinstallées.</span><span class="sxs-lookup"><span data-stu-id="05f02-125">The UnregisterProgIdInfo action removes ProgId information from the registry ([ProgId Table](progid-table.md)) for features that are connected to the extension information ([Extension table](extension-table.md)) or the Class information ([Class table](class-table.md)) and are currently selected to be uninstalled.</span></span>

 

 



