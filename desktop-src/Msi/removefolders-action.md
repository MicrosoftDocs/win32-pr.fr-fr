---
description: L’action RemoveFolders supprime tous les dossiers liés à des composants définis pour être supprimés ou exécutés à partir de la source. Ces dossiers sont supprimés uniquement s’ils sont vides. Si un dossier est supprimé, il est désinscrit avec l’identificateur de composant approprié.
ms.assetid: 0f68458e-ae9a-4ca5-bc60-06d4de91e2e9
title: Action RemoveFolders
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69648fbae333f0e7b989f2e989f0982d49736317
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203773"
---
# <a name="removefolders-action"></a><span data-ttu-id="e1912-105">Action RemoveFolders</span><span class="sxs-lookup"><span data-stu-id="e1912-105">RemoveFolders Action</span></span>

<span data-ttu-id="e1912-106">L’action RemoveFolders supprime tous les dossiers liés à des composants définis pour être supprimés ou exécutés à partir de la source.</span><span class="sxs-lookup"><span data-stu-id="e1912-106">The RemoveFolders action removes any folders linked to components set to be removed or run from source.</span></span> <span data-ttu-id="e1912-107">Ces dossiers sont supprimés uniquement s’ils sont vides.</span><span class="sxs-lookup"><span data-stu-id="e1912-107">These folders are removed only if they are empty.</span></span> <span data-ttu-id="e1912-108">Si un dossier est supprimé, il est désinscrit avec l’identificateur de composant approprié.</span><span class="sxs-lookup"><span data-stu-id="e1912-108">If a folder is removed, it is unregistered with the appropriate component identifier.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="e1912-109">Restrictions de séquence</span><span class="sxs-lookup"><span data-stu-id="e1912-109">Sequence Restrictions</span></span>

<span data-ttu-id="e1912-110">L’action RemoveFolders doit venir après l’action [RemoveFiles](removefiles-action.md) ou toute action qui peut supprimer des fichiers de dossiers.</span><span class="sxs-lookup"><span data-stu-id="e1912-110">The RemoveFolders action must come after the [RemoveFiles](removefiles-action.md) action or any action that may remove files from folders.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="e1912-111">Messages ActionData</span><span class="sxs-lookup"><span data-stu-id="e1912-111">ActionData Messages</span></span>



| <span data-ttu-id="e1912-112">Champ</span><span class="sxs-lookup"><span data-stu-id="e1912-112">Field</span></span> | <span data-ttu-id="e1912-113">Description des données d’action</span><span class="sxs-lookup"><span data-stu-id="e1912-113">Description of action data</span></span>    |
|-------|-------------------------------|
| <span data-ttu-id="e1912-114">\[1\]</span><span class="sxs-lookup"><span data-stu-id="e1912-114">\[1\]</span></span> | <span data-ttu-id="e1912-115">Identificateur du dossier supprimé.</span><span class="sxs-lookup"><span data-stu-id="e1912-115">Identifier of removed folder.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="e1912-116">Notes</span><span class="sxs-lookup"><span data-stu-id="e1912-116">Remarks</span></span>

<span data-ttu-id="e1912-117">Le programme d’installation ne supprime pas automatiquement les dossiers créés par l' [action CreateFolders](createfolders-action.md) pendant la désinstallation de l’application.</span><span class="sxs-lookup"><span data-stu-id="e1912-117">The installer does not automatically remove the folders created by the [CreateFolders action](createfolders-action.md) during an uninstallation of the application.</span></span> <span data-ttu-id="e1912-118">Le programme d’installation doit être invité à supprimer ces dossiers en créant l’action RemoveFolders dans la séquence d’action.</span><span class="sxs-lookup"><span data-stu-id="e1912-118">The installer must be instructed to remove these folders by authoring the RemoveFolders action into the action sequence.</span></span>

<span data-ttu-id="e1912-119">Pour spécifier le nom et l’emplacement du dossier, utilisez la \_ colonne Directory de la [table CreateFolder](createfolder-table.md).</span><span class="sxs-lookup"><span data-stu-id="e1912-119">To specify the name and location of the folder, use the Directory\_ column of the [CreateFolder table](createfolder-table.md).</span></span> <span data-ttu-id="e1912-120">Chaque nom de dossier dans la table CreateFolder est supposé être une propriété qui définit l’emplacement du dossier.</span><span class="sxs-lookup"><span data-stu-id="e1912-120">Each folder name in the CreateFolder table is assumed to be a property defining the folder location.</span></span>

<span data-ttu-id="e1912-121">Pour spécifier le composant propriétaire du dossier, utilisez la colonne ComponentId de la [table des composants](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="e1912-121">To specify the component owning the folder, use the ComponentId column of the [Component table](component-table.md).</span></span>

 

 



