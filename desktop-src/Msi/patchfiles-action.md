---
description: L’action PatchFiles interroge la table des correctifs pour déterminer les correctifs à appliquer. L’action PatchFiles effectue également la mise à jour corrective basée sur les octets des fichiers.
ms.assetid: 4026755e-a006-40c0-8816-de5358f4582e
title: Action PatchFiles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53583a93089444f014d9cc837fb18acf21cec82d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103865213"
---
# <a name="patchfiles-action"></a><span data-ttu-id="a2679-104">Action PatchFiles</span><span class="sxs-lookup"><span data-stu-id="a2679-104">PatchFiles Action</span></span>

<span data-ttu-id="a2679-105">L’action PatchFiles interroge la [table des correctifs](patch-table.md) pour déterminer les correctifs à appliquer.</span><span class="sxs-lookup"><span data-stu-id="a2679-105">The PatchFiles action queries the [Patch table](patch-table.md) to determine which patches are to be applied.</span></span> <span data-ttu-id="a2679-106">L’action PatchFiles effectue également la mise à jour corrective basée sur les octets des fichiers.</span><span class="sxs-lookup"><span data-stu-id="a2679-106">The PatchFiles action also performs the byte-wise patching of the files.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="a2679-107">Restrictions de séquence</span><span class="sxs-lookup"><span data-stu-id="a2679-107">Sequence Restrictions</span></span>

<span data-ttu-id="a2679-108">Si le fichier à corriger n’est pas installé, l’action PatchFiles doit venir après l' [action InstallFiles](installfiles-action.md) qui installe le fichier.</span><span class="sxs-lookup"><span data-stu-id="a2679-108">If the file that is to be patched is not installed, the PatchFiles action must come after the [InstallFiles action](installfiles-action.md) that installs the file.</span></span> <span data-ttu-id="a2679-109">Les fichiers précédemment installés peuvent être corrigés à tout moment dans la séquence d’action.</span><span class="sxs-lookup"><span data-stu-id="a2679-109">Previously installed files may be patched at any point in the action sequence.</span></span> <span data-ttu-id="a2679-110">L' [action DuplicateFiles](duplicatefiles-action.md) doit venir après l’action PatchFiles pour empêcher la duplication de la version non corrigée du fichier.</span><span class="sxs-lookup"><span data-stu-id="a2679-110">The [DuplicateFiles Action](duplicatefiles-action.md) must come after the PatchFiles action to prevent duplicating the unpatched version of the file.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="a2679-111">Messages ActionData</span><span class="sxs-lookup"><span data-stu-id="a2679-111">ActionData Messages</span></span>



| <span data-ttu-id="a2679-112">Champ</span><span class="sxs-lookup"><span data-stu-id="a2679-112">Field</span></span> | <span data-ttu-id="a2679-113">Description des données d’action</span><span class="sxs-lookup"><span data-stu-id="a2679-113">Description of action data</span></span>                    |
|-------|-----------------------------------------------|
| <span data-ttu-id="a2679-114">\[1\]</span><span class="sxs-lookup"><span data-stu-id="a2679-114">\[1\]</span></span> | <span data-ttu-id="a2679-115">Identificateur du fichier corrigé.</span><span class="sxs-lookup"><span data-stu-id="a2679-115">Identifier of patched file.</span></span>                   |
| <span data-ttu-id="a2679-116">\[2\]</span><span class="sxs-lookup"><span data-stu-id="a2679-116">\[2\]</span></span> | <span data-ttu-id="a2679-117">Identificateur du répertoire contenant le fichier corrigé.</span><span class="sxs-lookup"><span data-stu-id="a2679-117">Identifier of directory holding patched file.</span></span> |
| <span data-ttu-id="a2679-118">\[3\]</span><span class="sxs-lookup"><span data-stu-id="a2679-118">\[3\]</span></span> | <span data-ttu-id="a2679-119">Taille du correctif en octets.</span><span class="sxs-lookup"><span data-stu-id="a2679-119">Size of patch in bytes.</span></span>                       |



 

 

 



