---
description: L’action DuplicateFiles duplique les fichiers installés par l’action InstallFiles. Les fichiers dupliqués peuvent être copiés dans le même répertoire avec un nom différent ou dans un répertoire différent avec le nom d’origine.
ms.assetid: 51cc0b3f-aa01-4f4d-9a4d-add832698061
title: Action DuplicateFiles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 711f6bbd4716beb227dea348826bc302e2f4ba2a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106522041"
---
# <a name="duplicatefiles-action"></a><span data-ttu-id="b4cfd-104">Action DuplicateFiles</span><span class="sxs-lookup"><span data-stu-id="b4cfd-104">DuplicateFiles Action</span></span>

<span data-ttu-id="b4cfd-105">L’action DuplicateFiles duplique les fichiers installés par l’action [InstallFiles](installfiles-action.md) .</span><span class="sxs-lookup"><span data-stu-id="b4cfd-105">The DuplicateFiles action duplicates files installed by the [InstallFiles](installfiles-action.md) action.</span></span> <span data-ttu-id="b4cfd-106">Les fichiers dupliqués peuvent être copiés dans le même répertoire avec un nom différent ou dans un répertoire différent avec le nom d’origine.</span><span class="sxs-lookup"><span data-stu-id="b4cfd-106">The duplicate files can be copied to the same directory with a different name or to a different directory with the original name.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="b4cfd-107">Restrictions de séquence</span><span class="sxs-lookup"><span data-stu-id="b4cfd-107">Sequence Restrictions</span></span>

<span data-ttu-id="b4cfd-108">L’action DuplicateFiles doit venir après l' [action InstallFiles](installfiles-action.md).</span><span class="sxs-lookup"><span data-stu-id="b4cfd-108">The DuplicateFiles action must come after the [InstallFiles action](installfiles-action.md).</span></span> <span data-ttu-id="b4cfd-109">L’action DuplicateFiles doit également être postérieure à l' [action PatchFiles](patchfiles-action.md) pour empêcher la duplication de la version non corrigée du fichier.</span><span class="sxs-lookup"><span data-stu-id="b4cfd-109">The DuplicateFiles Action must also come after the [PatchFiles action](patchfiles-action.md) to prevent duplicating the unpatched version of the file.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="b4cfd-110">Messages ActionData</span><span class="sxs-lookup"><span data-stu-id="b4cfd-110">ActionData Messages</span></span>



| <span data-ttu-id="b4cfd-111">Champ</span><span class="sxs-lookup"><span data-stu-id="b4cfd-111">Field</span></span> | <span data-ttu-id="b4cfd-112">Description des données d’action</span><span class="sxs-lookup"><span data-stu-id="b4cfd-112">Description of action data</span></span>                       |
|-------|--------------------------------------------------|
| <span data-ttu-id="b4cfd-113">\[1\]</span><span class="sxs-lookup"><span data-stu-id="b4cfd-113">\[1\]</span></span> | <span data-ttu-id="b4cfd-114">Identificateur du fichier dupliqué.</span><span class="sxs-lookup"><span data-stu-id="b4cfd-114">Identifier of duplicated file.</span></span>                   |
| <span data-ttu-id="b4cfd-115">\[6\]</span><span class="sxs-lookup"><span data-stu-id="b4cfd-115">\[6\]</span></span> | <span data-ttu-id="b4cfd-116">Taille du fichier dupliqué.</span><span class="sxs-lookup"><span data-stu-id="b4cfd-116">Size of duplicated file.</span></span>                         |
| <span data-ttu-id="b4cfd-117">\[9\]</span><span class="sxs-lookup"><span data-stu-id="b4cfd-117">\[9\]</span></span> | <span data-ttu-id="b4cfd-118">Identificateur du répertoire contenant le fichier dupliqué.</span><span class="sxs-lookup"><span data-stu-id="b4cfd-118">Identifier of directory holding duplicated file.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="b4cfd-119">Notes</span><span class="sxs-lookup"><span data-stu-id="b4cfd-119">Remarks</span></span>

<span data-ttu-id="b4cfd-120">L’action DuplicateFiles traite une entrée de [table DuplicateFile](duplicatefile-table.md) uniquement si le composant lié à cette entrée est installé localement.</span><span class="sxs-lookup"><span data-stu-id="b4cfd-120">The DuplicateFiles action processes a [DuplicateFile table](duplicatefile-table.md) entry only if the component linked to that entry is being installed locally.</span></span> <span data-ttu-id="b4cfd-121">Pour plus d’informations, consultez [table des composants](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="b4cfd-121">For more information, see [Component table](component-table.md).</span></span>

<span data-ttu-id="b4cfd-122">La chaîne dans le champ DestFolder est un nom de propriété dont la valeur est supposée être résolue en chemin d’accès qualifié complet.</span><span class="sxs-lookup"><span data-stu-id="b4cfd-122">The string in the DestFolder field is a property name whose value is expected to resolve to a fully qualified path.</span></span> <span data-ttu-id="b4cfd-123">Cette propriété peut être l’une des entrées d’annuaire de la table de [répertoire](directory-table.md) , toute propriété de dossier prédéfinie ([**CommonFilesFolder**](commonfilesfolder.md), par exemple) ou une propriété définie par une entrée de la table [AppSearch](appsearch-table.md) .</span><span class="sxs-lookup"><span data-stu-id="b4cfd-123">This property can either be any of the directory entries in the [Directory](directory-table.md) table, any pre-defined folder property ([**CommonFilesFolder**](commonfilesfolder.md), for example), or a property set by any entry in the [AppSearch](appsearch-table.md) table.</span></span> <span data-ttu-id="b4cfd-124">Si la propriété **DestFolder** ne correspond pas à un chemin d’accès valide, l’action DuplicateFiles ne fait rien pour cette entrée.</span><span class="sxs-lookup"><span data-stu-id="b4cfd-124">If the **DestFolder** property does not evaluate to a valid path the DuplicateFiles action does nothing for that entry.</span></span>

<span data-ttu-id="b4cfd-125">Si le nom du fichier de destination dans la colonne DestName de la table DuplicateFile est vide, le nom du fichier de destination sera le même que le nom du fichier d’origine.</span><span class="sxs-lookup"><span data-stu-id="b4cfd-125">If the name of the destination file in the DestName column of the DuplicateFile table is left blank, the destination file name will be the same as the original file name.</span></span>

<span data-ttu-id="b4cfd-126">Les fichiers installés par l’action DuplicateFiles sont supprimés par l’action [RemoveDuplicateFiles](removeduplicatefiles-action.md) le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="b4cfd-126">Files installed by the DuplicateFiles action are removed by the [RemoveDuplicateFiles](removeduplicatefiles-action.md) action when appropriate.</span></span>

 

 



