---
description: L’action RemoveExistingProducts passe par les codes de produit figurant dans la colonne ActionProperty de la table de mise à niveau et supprime les produits en séquence en appelant des installations simultanées.
ms.assetid: 3e96283b-1085-4ace-b004-2fd94310eeb2
title: Action RemoveExistingProducts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dea3b792b02352277e8f29fa422b093fe876b560
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106543115"
---
# <a name="removeexistingproducts-action"></a><span data-ttu-id="68964-103">Action RemoveExistingProducts</span><span class="sxs-lookup"><span data-stu-id="68964-103">RemoveExistingProducts Action</span></span>

<span data-ttu-id="68964-104">L’action RemoveExistingProducts passe par les codes de produit figurant dans la colonne ActionProperty de la [table de mise à niveau](upgrade-table.md) et supprime les produits en séquence en appelant des installations simultanées.</span><span class="sxs-lookup"><span data-stu-id="68964-104">The RemoveExistingProducts action goes through the product codes listed in the ActionProperty column of the [Upgrade table](upgrade-table.md) and removes the products in sequence by invoking concurrent installations.</span></span> <span data-ttu-id="68964-105">Pour chaque installation simultanée, le programme d’installation définit la propriété [**ProductCode**](productcode.md) sur le code du produit et définit la propriété [**Remove**](remove.md) sur la valeur du champ Remove de la table Upgrade.</span><span class="sxs-lookup"><span data-stu-id="68964-105">For each concurrent installation the installer sets the [**ProductCode**](productcode.md) property to the product code and sets the [**REMOVE**](remove.md) property to the value in the Remove field of the Upgrade table.</span></span> <span data-ttu-id="68964-106">Si le champ supprimer est vide, sa valeur par défaut est tous et le programme d’installation supprime l’intégralité du produit.</span><span class="sxs-lookup"><span data-stu-id="68964-106">If the Remove field is blank, its value defaults to ALL and the installer removes the entire product.</span></span>

<span data-ttu-id="68964-107">Le programme d’installation exécute uniquement l’action RemoveExistingProducts la première fois qu’il installe un produit.</span><span class="sxs-lookup"><span data-stu-id="68964-107">The installer only runs the RemoveExistingProducts action the first time it installs a product.</span></span> <span data-ttu-id="68964-108">Elle n’exécute pas l’action pendant une [installation](maintenance-installation.md) ou une désinstallation de maintenance.</span><span class="sxs-lookup"><span data-stu-id="68964-108">It does not run the action during a [maintenance installation](maintenance-installation.md) or uninstallation.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="68964-109">Restrictions de séquence</span><span class="sxs-lookup"><span data-stu-id="68964-109">Sequence Restrictions</span></span>

<span data-ttu-id="68964-110">L’action RemoveExistingProducts doit être planifiée dans la séquence d’action à l’un des emplacements suivants.</span><span class="sxs-lookup"><span data-stu-id="68964-110">The RemoveExistingProducts action must be scheduled in the action sequence in one of the following locations.</span></span>

-   <span data-ttu-id="68964-111">Entre l' [action InstallValidate](installvalidate-action.md) et l' [action InstallInitialize](installinitialize-action.md).</span><span class="sxs-lookup"><span data-stu-id="68964-111">Between the [InstallValidate action](installvalidate-action.md) and the [InstallInitialize action](installinitialize-action.md).</span></span> <span data-ttu-id="68964-112">Dans ce cas, le programme d’installation supprime les anciennes applications entièrement avant d’installer les nouvelles applications.</span><span class="sxs-lookup"><span data-stu-id="68964-112">In this case, the installer removes the old applications entirely before installing the new applications.</span></span> <span data-ttu-id="68964-113">Il s’agit d’un emplacement inefficace pour l’action, car tous les fichiers réutilisés doivent être recopiés.</span><span class="sxs-lookup"><span data-stu-id="68964-113">This is an inefficient placement for the action because all reused files have to be recopied.</span></span>
-   <span data-ttu-id="68964-114">Après l' [action InstallInitialize](installinitialize-action.md) et avant toute action qui génère le script d’exécution.</span><span class="sxs-lookup"><span data-stu-id="68964-114">After the [InstallInitialize action](installinitialize-action.md) and before any actions that generate execution script.</span></span>
-   <span data-ttu-id="68964-115">Entre l’action [InstallExecute](installexecute-action.md), l’action [InstallExecuteAgain](installexecuteagain-action.md)et l' [action InstallFinalize](installfinalize-action.md).</span><span class="sxs-lookup"><span data-stu-id="68964-115">Between the [InstallExecute action](installexecute-action.md), or the [InstallExecuteAgain action](installexecuteagain-action.md), and the [InstallFinalize action](installfinalize-action.md).</span></span> <span data-ttu-id="68964-116">En général, les trois dernières actions sont planifiées juste après l’autre : InstallExecute, RemoveExistingProducts et InstallFinalize.</span><span class="sxs-lookup"><span data-stu-id="68964-116">Generally the last three actions are scheduled right after one another: InstallExecute, RemoveExistingProducts, and InstallFinalize.</span></span> <span data-ttu-id="68964-117">Dans ce cas, les fichiers mis à jour sont installés en premier, puis les anciens fichiers sont supprimés.</span><span class="sxs-lookup"><span data-stu-id="68964-117">In this case the updated files are installed first and then the old files are removed.</span></span> <span data-ttu-id="68964-118">Toutefois, si la suppression de l’ancienne application échoue, le programme d’installation annule la suppression de l’ancienne application et l’installation de la nouvelle application.</span><span class="sxs-lookup"><span data-stu-id="68964-118">However, if the removal of the old application fails, then the installer rolls back both the removal of the old application and the install of the new application.</span></span>
-   <span data-ttu-id="68964-119">Après l' [action InstallFinalize](installfinalize-action.md).</span><span class="sxs-lookup"><span data-stu-id="68964-119">After the [InstallFinalize action](installfinalize-action.md).</span></span> <span data-ttu-id="68964-120">Il s’agit du positionnement le plus efficace pour l’action.</span><span class="sxs-lookup"><span data-stu-id="68964-120">This is the most efficient placement for the action.</span></span> <span data-ttu-id="68964-121">Dans ce cas, le programme d’installation met à jour les fichiers avant de supprimer les anciennes applications.</span><span class="sxs-lookup"><span data-stu-id="68964-121">In this case, the installer updates files before removing the old applications.</span></span> <span data-ttu-id="68964-122">Seuls les fichiers en cours de mise à jour sont installés pendant l’installation.</span><span class="sxs-lookup"><span data-stu-id="68964-122">Only the files being updated get installed during the installation.</span></span> <span data-ttu-id="68964-123">Si la suppression de l’ancienne application échoue, le programme d’installation annule uniquement la désinstallation de l’ancienne application.</span><span class="sxs-lookup"><span data-stu-id="68964-123">If the removal of the old application fails, then the installer only rolls back the uninstallation of the old application.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="68964-124">Messages ActionData</span><span class="sxs-lookup"><span data-stu-id="68964-124">ActionData Messages</span></span>



| <span data-ttu-id="68964-125">Champ</span><span class="sxs-lookup"><span data-stu-id="68964-125">Field</span></span> | <span data-ttu-id="68964-126">Description des données d’action</span><span class="sxs-lookup"><span data-stu-id="68964-126">Description of action data</span></span> |
|-------|----------------------------|
| <span data-ttu-id="68964-127">\[1\]</span><span class="sxs-lookup"><span data-stu-id="68964-127">\[1\]</span></span> | <span data-ttu-id="68964-128">Produit supprimé.</span><span class="sxs-lookup"><span data-stu-id="68964-128">Removed product.</span></span>           |



 

## <a name="remarks"></a><span data-ttu-id="68964-129">Notes</span><span class="sxs-lookup"><span data-stu-id="68964-129">Remarks</span></span>

<span data-ttu-id="68964-130">Windows Installer définit la propriété [**UPGRADINGPRODUCTCODE**](upgradingproductcode.md) lors de l’exécution de cette action.</span><span class="sxs-lookup"><span data-stu-id="68964-130">Windows Installer sets the [**UPGRADINGPRODUCTCODE**](upgradingproductcode.md) Property when it runs this action.</span></span>

 

 



