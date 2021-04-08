---
description: L’action RemoveDuplicateFiles supprime les fichiers installés par l’action DuplicateFiles.
ms.assetid: 3d8ba4c5-775f-471e-a479-32fa6f7a1bf0
title: Action RemoveDuplicateFiles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 555379f3810770abc9f91fd449e71434e9fa6244
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751124"
---
# <a name="removeduplicatefiles-action"></a><span data-ttu-id="fcfce-103">Action RemoveDuplicateFiles</span><span class="sxs-lookup"><span data-stu-id="fcfce-103">RemoveDuplicateFiles Action</span></span>

<span data-ttu-id="fcfce-104">L’action RemoveDuplicateFiles supprime les fichiers installés par l’action [DuplicateFiles](duplicatefiles-action.md) .</span><span class="sxs-lookup"><span data-stu-id="fcfce-104">The RemoveDuplicateFiles action deletes files installed by the [DuplicateFiles](duplicatefiles-action.md) action.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="fcfce-105">Restrictions de séquence</span><span class="sxs-lookup"><span data-stu-id="fcfce-105">Sequence Restrictions</span></span>

<span data-ttu-id="fcfce-106">L’action RemoveDuplicateFiles doit se produire après l’action [InstallValidate](installvalidate-action.md) et avant l’action [InstallFiles](installfiles-action.md) .</span><span class="sxs-lookup"><span data-stu-id="fcfce-106">The RemoveDuplicateFiles action must occur after the [InstallValidate](installvalidate-action.md) action and before the [InstallFiles](installfiles-action.md) action.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="fcfce-107">Messages ActionData</span><span class="sxs-lookup"><span data-stu-id="fcfce-107">ActionData Messages</span></span>



| <span data-ttu-id="fcfce-108">Champ</span><span class="sxs-lookup"><span data-stu-id="fcfce-108">Field</span></span> | <span data-ttu-id="fcfce-109">Description des données d’action</span><span class="sxs-lookup"><span data-stu-id="fcfce-109">Description of action data</span></span>                    |
|-------|-----------------------------------------------|
| <span data-ttu-id="fcfce-110">\[1\]</span><span class="sxs-lookup"><span data-stu-id="fcfce-110">\[1\]</span></span> | <span data-ttu-id="fcfce-111">Identificateur du fichier supprimé.</span><span class="sxs-lookup"><span data-stu-id="fcfce-111">Identifier of removed file.</span></span>                   |
| <span data-ttu-id="fcfce-112">\[9\]</span><span class="sxs-lookup"><span data-stu-id="fcfce-112">\[9\]</span></span> | <span data-ttu-id="fcfce-113">Identificateur du répertoire contenant le fichier supprimé.</span><span class="sxs-lookup"><span data-stu-id="fcfce-113">Identifier of directory holding removed file.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="fcfce-114">Notes</span><span class="sxs-lookup"><span data-stu-id="fcfce-114">Remarks</span></span>

<span data-ttu-id="fcfce-115">Pour supprimer un fichier dupliqué avec l' [action DuplicateFiles](duplicatefiles-action.md) à l’aide de l’action RemoveDuplicateFiles, vous devez sélectionner le composant associé à l’entrée du fichier dans la table DuplicateFile pour la suppression.</span><span class="sxs-lookup"><span data-stu-id="fcfce-115">To delete a file duplicated with the [DuplicateFiles action](duplicatefiles-action.md) using the RemoveDuplicateFiles action, the component associated with the file's entry in the DuplicateFile table must be selected for removal.</span></span>

<span data-ttu-id="fcfce-116">Utilisez la colonne DestFolder de la [table DuplicateFile](duplicatefile-table.md) pour spécifier le nom de la propriété dont la valeur identifie le dossier de destination.</span><span class="sxs-lookup"><span data-stu-id="fcfce-116">Use the DestFolder column of the [DuplicateFile table](duplicatefile-table.md) to specify the property name whose value identifies the destination folder.</span></span>

 

 



