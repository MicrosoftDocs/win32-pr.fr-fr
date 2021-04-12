---
description: La table CreateFolder contient des références à des dossiers qui doivent être créés explicitement pour un composant particulier.
ms.assetid: b17b470b-6971-4124-8ec3-73914fdea95f
title: Table CreateFolder
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc286b32b48e0db9e5b991ab10af663c51538bf2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104204015"
---
# <a name="createfolder-table"></a><span data-ttu-id="92b1d-103">Table CreateFolder</span><span class="sxs-lookup"><span data-stu-id="92b1d-103">CreateFolder Table</span></span>

<span data-ttu-id="92b1d-104">La table CreateFolder contient des références à des dossiers qui doivent être créés explicitement pour un composant particulier.</span><span class="sxs-lookup"><span data-stu-id="92b1d-104">The CreateFolder table contains references to folders that need to be created explicitly for a particular component.</span></span>

<span data-ttu-id="92b1d-105">La table CreateFolder contient les colonnes suivantes.</span><span class="sxs-lookup"><span data-stu-id="92b1d-105">The CreateFolder table has the following columns.</span></span>



| <span data-ttu-id="92b1d-106">Colonne</span><span class="sxs-lookup"><span data-stu-id="92b1d-106">Column</span></span>      | <span data-ttu-id="92b1d-107">Type</span><span class="sxs-lookup"><span data-stu-id="92b1d-107">Type</span></span>                         | <span data-ttu-id="92b1d-108">Clé</span><span class="sxs-lookup"><span data-stu-id="92b1d-108">Key</span></span> | <span data-ttu-id="92b1d-109">Nullable</span><span class="sxs-lookup"><span data-stu-id="92b1d-109">Nullable</span></span> |
|-------------|------------------------------|-----|----------|
| <span data-ttu-id="92b1d-110">Répertoire\_</span><span class="sxs-lookup"><span data-stu-id="92b1d-110">Directory\_</span></span> | [<span data-ttu-id="92b1d-111">Identificateur</span><span class="sxs-lookup"><span data-stu-id="92b1d-111">Identifier</span></span>](identifier.md) | <span data-ttu-id="92b1d-112">O</span><span class="sxs-lookup"><span data-stu-id="92b1d-112">Y</span></span>   | <span data-ttu-id="92b1d-113">N</span><span class="sxs-lookup"><span data-stu-id="92b1d-113">N</span></span>        |
| <span data-ttu-id="92b1d-114">-\_</span><span class="sxs-lookup"><span data-stu-id="92b1d-114">Component\_</span></span> | [<span data-ttu-id="92b1d-115">Identificateur</span><span class="sxs-lookup"><span data-stu-id="92b1d-115">Identifier</span></span>](identifier.md) | <span data-ttu-id="92b1d-116">O</span><span class="sxs-lookup"><span data-stu-id="92b1d-116">Y</span></span>   | <span data-ttu-id="92b1d-117">N</span><span class="sxs-lookup"><span data-stu-id="92b1d-117">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="92b1d-118">Colonnes</span><span class="sxs-lookup"><span data-stu-id="92b1d-118">Columns</span></span>

<dl> <dt>

<span data-ttu-id="92b1d-119"><span id="Directory_"></span><span id="directory_"></span><span id="DIRECTORY_"></span>Directory\_</span><span class="sxs-lookup"><span data-stu-id="92b1d-119"><span id="Directory_"></span><span id="directory_"></span><span id="DIRECTORY_"></span>Directory\_</span></span>
</dt> <dd>

<span data-ttu-id="92b1d-120">Clé externe dans la première colonne de la [table de répertoires](directory-table.md).</span><span class="sxs-lookup"><span data-stu-id="92b1d-120">External key into the first column of the [Directory table](directory-table.md).</span></span>

</dd> <dt>

<span data-ttu-id="92b1d-121"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>-\_</span><span class="sxs-lookup"><span data-stu-id="92b1d-121"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Component\_</span></span>
</dt> <dd>

<span data-ttu-id="92b1d-122">Clé externe dans la première colonne de la [table des composants](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="92b1d-122">External key into the first column of the [Component table](component-table.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="92b1d-123">Notes</span><span class="sxs-lookup"><span data-stu-id="92b1d-123">Remarks</span></span>

<span data-ttu-id="92b1d-124">Les dossiers de ce tableau sont créés lors de l’installation du composant.</span><span class="sxs-lookup"><span data-stu-id="92b1d-124">The folders in this table are created when the component is installed.</span></span> <span data-ttu-id="92b1d-125">Une tentative est effectuée pour supprimer ces dossiers uniquement lorsque le composant est désinstallé ou déplacé vers l’exécution à partir de la source.</span><span class="sxs-lookup"><span data-stu-id="92b1d-125">An attempt is made to remove these folders only when the component is uninstalled or moved to run-from-source.</span></span> <span data-ttu-id="92b1d-126">Aucune suppression automatique n’est déclenchée si les dossiers sont vides.</span><span class="sxs-lookup"><span data-stu-id="92b1d-126">No automatic removal is triggered if the folders become empty.</span></span> <span data-ttu-id="92b1d-127">En revanche, les dossiers créés par le programme d’installation mais non répertoriés dans ce tableau sont supprimés lorsqu’ils sont vides.</span><span class="sxs-lookup"><span data-stu-id="92b1d-127">In contrast, folders created by the installer but not listed in this table are removed when they become empty.</span></span>

<span data-ttu-id="92b1d-128">Étant donné que les dossiers créés par le programme d’installation sont supprimés lorsqu’ils sont vides, vous devez créer une entrée dans la table CreateFolder pour installer un composant qui se compose d’un dossier vide.</span><span class="sxs-lookup"><span data-stu-id="92b1d-128">Because folders created by the installer are deleted when they become empty, you must author an entry into the CreateFolder table to install a component that consists of an empty folder.</span></span>

<span data-ttu-id="92b1d-129">Cette table est référencée lorsque l’action [CreateFolders](createfolders-action.md) ou l’action [RemoveFolders](removefolders-action.md) est appelée.</span><span class="sxs-lookup"><span data-stu-id="92b1d-129">This table is referred to when the [CreateFolders](createfolders-action.md) action or the [RemoveFolders](removefolders-action.md) action is called.</span></span>

<span data-ttu-id="92b1d-130">Pour plus d’informations sur la sécurisation d’un dossier, consultez la [table MsiLockPermissionsEx](msilockpermissionsex-table.md) et la [table LockPermissions](lockpermissions-table.md).</span><span class="sxs-lookup"><span data-stu-id="92b1d-130">For information on how to secure a folder see the [MsiLockPermissionsEx Table](msilockpermissionsex-table.md) and [LockPermissions Table](lockpermissions-table.md).</span></span>

## <a name="validation"></a><span data-ttu-id="92b1d-131">Validation</span><span class="sxs-lookup"><span data-stu-id="92b1d-131">Validation</span></span>

<dl>

[<span data-ttu-id="92b1d-132">ICE03</span><span class="sxs-lookup"><span data-stu-id="92b1d-132">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="92b1d-133">ICE06</span><span class="sxs-lookup"><span data-stu-id="92b1d-133">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="92b1d-134">ICE18</span><span class="sxs-lookup"><span data-stu-id="92b1d-134">ICE18</span></span>](ice18.md)  
[<span data-ttu-id="92b1d-135">ICE32</span><span class="sxs-lookup"><span data-stu-id="92b1d-135">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="92b1d-136">ICE55</span><span class="sxs-lookup"><span data-stu-id="92b1d-136">ICE55</span></span>](ice55.md)  
</dl>

 

 



