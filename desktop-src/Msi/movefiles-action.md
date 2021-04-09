---
description: L’action MoveFiles localise les fichiers existants sur l’ordinateur de l’utilisateur et déplace ou copie ces fichiers vers un nouvel emplacement.
ms.assetid: f08f751d-877b-4b17-8015-7108d5fd8195
title: Action MoveFiles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f06db0cef12753652bf94bf05875b2c2f9d4067c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868865"
---
# <a name="movefiles-action"></a><span data-ttu-id="a8c76-103">Action MoveFiles</span><span class="sxs-lookup"><span data-stu-id="a8c76-103">MoveFiles Action</span></span>

<span data-ttu-id="a8c76-104">L’action MoveFiles localise les fichiers existants sur l’ordinateur de l’utilisateur et déplace ou copie ces fichiers vers un nouvel emplacement.</span><span class="sxs-lookup"><span data-stu-id="a8c76-104">The MoveFiles action locates existing files on the user's computer and moves or copies those files to a new location.</span></span> <span data-ttu-id="a8c76-105">L’action MoveFiles interroge la [table MoveFile](movefile-table.md) et déplace les fichiers spécifiés ici si le composant lié aux entrées est spécifié pour être installé localement ou s’il est en cours d’exécution à partir de la source.</span><span class="sxs-lookup"><span data-stu-id="a8c76-105">The MoveFiles action queries the [MoveFile table](movefile-table.md) and moves files specified there if the component linked to the entries is specified to be install locally or is being run from source.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="a8c76-106">Restrictions de séquence</span><span class="sxs-lookup"><span data-stu-id="a8c76-106">Sequence Restrictions</span></span>

<span data-ttu-id="a8c76-107">L’action MoveFiles doit venir après l’action [InstallValidate](installvalidate-action.md) et avant l’action [InstallFiles](installfiles-action.md) .</span><span class="sxs-lookup"><span data-stu-id="a8c76-107">The MoveFiles action must come after the [InstallValidate](installvalidate-action.md) action and before the [InstallFiles](installfiles-action.md) action.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="a8c76-108">Messages ActionData</span><span class="sxs-lookup"><span data-stu-id="a8c76-108">ActionData Messages</span></span>



| <span data-ttu-id="a8c76-109">Champ</span><span class="sxs-lookup"><span data-stu-id="a8c76-109">Field</span></span> | <span data-ttu-id="a8c76-110">Description des données d’action</span><span class="sxs-lookup"><span data-stu-id="a8c76-110">Description of action data</span></span>                  |
|-------|---------------------------------------------|
| <span data-ttu-id="a8c76-111">\[1\]</span><span class="sxs-lookup"><span data-stu-id="a8c76-111">\[1\]</span></span> | <span data-ttu-id="a8c76-112">Identificateur du fichier déplacé.</span><span class="sxs-lookup"><span data-stu-id="a8c76-112">Identifier of moved file.</span></span>                   |
| <span data-ttu-id="a8c76-113">\[6\]</span><span class="sxs-lookup"><span data-stu-id="a8c76-113">\[6\]</span></span> | <span data-ttu-id="a8c76-114">Taille du fichier installé en octets.</span><span class="sxs-lookup"><span data-stu-id="a8c76-114">Size of installed file in bytes.</span></span>            |
| <span data-ttu-id="a8c76-115">\[9\]</span><span class="sxs-lookup"><span data-stu-id="a8c76-115">\[9\]</span></span> | <span data-ttu-id="a8c76-116">Identificateur du répertoire contenant le fichier déplacé.</span><span class="sxs-lookup"><span data-stu-id="a8c76-116">Identifier of directory holding moved file.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="a8c76-117">Notes</span><span class="sxs-lookup"><span data-stu-id="a8c76-117">Remarks</span></span>

<span data-ttu-id="a8c76-118">La table MoveFiles contient une colonne nommée « options » qui spécifie les fichiers sources à déplacer ou à copier.</span><span class="sxs-lookup"><span data-stu-id="a8c76-118">The MoveFiles table contain a column named "options" which specifies the source files to be moved or copied.</span></span> <span data-ttu-id="a8c76-119">Un fichier source déplacé est supprimé une fois qu’il a été copié vers un nouvel emplacement.</span><span class="sxs-lookup"><span data-stu-id="a8c76-119">A moved source file is deleted after it has been copied to a new location.</span></span> <span data-ttu-id="a8c76-120">Pour connaître la syntaxe exacte, consultez la [table MoveFile](movefile-table.md).</span><span class="sxs-lookup"><span data-stu-id="a8c76-120">For the exact syntax, see the [MoveFile table](movefile-table.md).</span></span>

<span data-ttu-id="a8c76-121">Les colonnes SourceFolder et DestFolder de la table MoveFile sont des noms de propriétés dont les valeurs sont censées être résolues en chemins d’accès complets.</span><span class="sxs-lookup"><span data-stu-id="a8c76-121">The SourceFolder and DestFolder columns of the MoveFile table are property names whose values are expected to resolve to fully qualified paths.</span></span> <span data-ttu-id="a8c76-122">Ces propriétés peuvent correspondre à l’une des entrées d’annuaire de la table de [répertoire](directory-table.md) , à toute propriété de dossier prédéfinie ([**FavoritesFolder**](favoritesfolder.md), par exemple) ou à une propriété définie par une entrée de la table [AppSearch](appsearch-table.md) .</span><span class="sxs-lookup"><span data-stu-id="a8c76-122">These properties can be any of the directory entries in the [Directory](directory-table.md) table, any predefined folder property ([**FavoritesFolder**](favoritesfolder.md), for example), or a property set by any entry in the [AppSearch](appsearch-table.md) table.</span></span> <span data-ttu-id="a8c76-123">Ces propriétés peuvent contenir un chemin d’accès complet contenant le nom de fichier d’un fichier spécifique.</span><span class="sxs-lookup"><span data-stu-id="a8c76-123">These properties may contain a full path containing the file name to a specific file.</span></span> <span data-ttu-id="a8c76-124">Par exemple, la table AppSearch peut être créée pour rechercher un fichier particulier et définir une propriété sur le chemin d’accès complet à ce fichier.</span><span class="sxs-lookup"><span data-stu-id="a8c76-124">For example, the AppSearch table can be authored to search for a particular file and set a property to the full path to that file.</span></span> <span data-ttu-id="a8c76-125">Dans cet exemple, la colonne SourceName de la table MoveFile peut être laissée vide pour indiquer que la valeur de la propriété SourceFolder contient un chemin d’accès complet au fichier.</span><span class="sxs-lookup"><span data-stu-id="a8c76-125">In this example, the SourceName column in the MoveFile table can be left blank to indicate that the value in the SourceFolder property contains a full file path.</span></span> <span data-ttu-id="a8c76-126">Le point-virgule est le délimiteur de liste pour les transformations, les sources et les correctifs, et ne doit pas être utilisé dans les chemins d’accès ou les noms de fichiers.</span><span class="sxs-lookup"><span data-stu-id="a8c76-126">The semicolon is the list delimiter for transforms, sources, and patches and should not be used in file names or paths.</span></span>

<span data-ttu-id="a8c76-127">L’action MoveFiles n’agit pas sur les entrées de la table MoveFile dans lesquelles la propriété SourceFolder ou DestFolder ne correspond pas à un chemin d’accès complet.</span><span class="sxs-lookup"><span data-stu-id="a8c76-127">The MoveFiles action does not act on entries in the MoveFile table in which either the SourceFolder or DestFolder property does not evaluate to a full path.</span></span>

<span data-ttu-id="a8c76-128">L’action MoveFiles tente de déplacer ou de copier tous les fichiers du répertoire source qui correspondent au nom donné dans la colonne SourceName de la table MoveFiles.</span><span class="sxs-lookup"><span data-stu-id="a8c76-128">The MoveFiles action attempts to move or copy all files in the source directory that match the name given in the SourceName column of the MoveFiles table.</span></span> <span data-ttu-id="a8c76-129">Le nom dans la colonne SourceName peut inclure \* ou ?</span><span class="sxs-lookup"><span data-stu-id="a8c76-129">The name in the SourceName column can include either the \* or ?</span></span> <span data-ttu-id="a8c76-130">caractères génériques qui permettent de déplacer ou de copier un groupe de fichiers.</span><span class="sxs-lookup"><span data-stu-id="a8c76-130">wildcards which allow a group of files to be moved or copied.</span></span> <span data-ttu-id="a8c76-131">Par exemple, la colonne SourceName peut contenir une entrée de « \* . xls » et l’action MoveFiles déplace ou copie chaque classeur Microsoft Excel du répertoire source vers la destination.</span><span class="sxs-lookup"><span data-stu-id="a8c76-131">For example, the SourceName column may contain an entry of "\*.xls" and the MoveFiles action moves or copies every Microsoft Excel workbook from the source directory to the destination.</span></span>

<span data-ttu-id="a8c76-132">Le nom à attribuer au fichier de destination peut être spécifié dans la colonne DestName de la table MoveFile.</span><span class="sxs-lookup"><span data-stu-id="a8c76-132">The name to be given to the destination file can be specified in the DestName column of the MoveFile table.</span></span> <span data-ttu-id="a8c76-133">Le nom du fichier de destination conserve le nom du fichier source si cette colonne est laissée vide.</span><span class="sxs-lookup"><span data-stu-id="a8c76-133">The destination file name retains the source file name if this column is left blank.</span></span>

<span data-ttu-id="a8c76-134">Si un \* caractère générique «» est entré dans la colonne SourceName de la [table MoveFile](movefile-table.md) et qu’un nom de fichier de destination est spécifié dans la colonne DestName, tous les fichiers déplacés ou copiés conservent les noms dans les sources.</span><span class="sxs-lookup"><span data-stu-id="a8c76-134">If a "\*" wildcard is entered in the SourceName column of the [MoveFile table](movefile-table.md) and a destination file name is specified in the DestName column, all moved or copied files retain the names in the sources.</span></span>

<span data-ttu-id="a8c76-135">Les fichiers qui sont déplacés ou copiés par l’action MoveFiles ne sont pas supprimés lorsque le produit est désinstallé.</span><span class="sxs-lookup"><span data-stu-id="a8c76-135">Files that are moved or copied by the MoveFiles action are not deleted when the product is uninstalled.</span></span>

 

 



