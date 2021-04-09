---
description: La table DuplicateFile contient une liste des fichiers qui doivent être dupliqués, soit vers un répertoire différent de celui du fichier d’origine, soit vers le même répertoire, mais avec un nom différent. Le fichier d’origine doit être un fichier installé par l’action InstallFiles.
ms.assetid: 7fe1b52d-4b06-48cd-afe5-2bd5495bb55e
title: Table DuplicateFile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 766f28b7984aedfc682a2bf23378d46ee0519c65
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104034645"
---
# <a name="duplicatefile-table"></a><span data-ttu-id="3ee50-104">Table DuplicateFile</span><span class="sxs-lookup"><span data-stu-id="3ee50-104">DuplicateFile Table</span></span>

<span data-ttu-id="3ee50-105">La table DuplicateFile contient une liste des fichiers qui doivent être dupliqués, soit vers un répertoire différent de celui du fichier d’origine, soit vers le même répertoire, mais avec un nom différent.</span><span class="sxs-lookup"><span data-stu-id="3ee50-105">The DuplicateFile table contains a list of files that are to be duplicated, either to a different directory than the original file or to the same directory but with a different name.</span></span> <span data-ttu-id="3ee50-106">Le fichier d’origine doit être un fichier installé par l' [action InstallFiles](installfiles-action.md).</span><span class="sxs-lookup"><span data-stu-id="3ee50-106">The original file must be a file installed by the [InstallFiles action](installfiles-action.md).</span></span>

<span data-ttu-id="3ee50-107">La table DuplicateFile contient les colonnes suivantes.</span><span class="sxs-lookup"><span data-stu-id="3ee50-107">The DuplicateFile table has the following columns.</span></span>



| <span data-ttu-id="3ee50-108">Colonne</span><span class="sxs-lookup"><span data-stu-id="3ee50-108">Column</span></span>      | <span data-ttu-id="3ee50-109">Type</span><span class="sxs-lookup"><span data-stu-id="3ee50-109">Type</span></span>                         | <span data-ttu-id="3ee50-110">Clé</span><span class="sxs-lookup"><span data-stu-id="3ee50-110">Key</span></span> | <span data-ttu-id="3ee50-111">Nullable</span><span class="sxs-lookup"><span data-stu-id="3ee50-111">Nullable</span></span> |
|-------------|------------------------------|-----|----------|
| <span data-ttu-id="3ee50-112">FileKey</span><span class="sxs-lookup"><span data-stu-id="3ee50-112">FileKey</span></span>     | [<span data-ttu-id="3ee50-113">Identificateur</span><span class="sxs-lookup"><span data-stu-id="3ee50-113">Identifier</span></span>](identifier.md) | <span data-ttu-id="3ee50-114">O</span><span class="sxs-lookup"><span data-stu-id="3ee50-114">Y</span></span>   | <span data-ttu-id="3ee50-115">N</span><span class="sxs-lookup"><span data-stu-id="3ee50-115">N</span></span>        |
| <span data-ttu-id="3ee50-116">-\_</span><span class="sxs-lookup"><span data-stu-id="3ee50-116">Component\_</span></span> | [<span data-ttu-id="3ee50-117">Identificateur</span><span class="sxs-lookup"><span data-stu-id="3ee50-117">Identifier</span></span>](identifier.md) | <span data-ttu-id="3ee50-118">N</span><span class="sxs-lookup"><span data-stu-id="3ee50-118">N</span></span>   | <span data-ttu-id="3ee50-119">N</span><span class="sxs-lookup"><span data-stu-id="3ee50-119">N</span></span>        |
| <span data-ttu-id="3ee50-120">fichier\_</span><span class="sxs-lookup"><span data-stu-id="3ee50-120">File\_</span></span>      | [<span data-ttu-id="3ee50-121">Identificateur</span><span class="sxs-lookup"><span data-stu-id="3ee50-121">Identifier</span></span>](identifier.md) | <span data-ttu-id="3ee50-122">N</span><span class="sxs-lookup"><span data-stu-id="3ee50-122">N</span></span>   | <span data-ttu-id="3ee50-123">N</span><span class="sxs-lookup"><span data-stu-id="3ee50-123">N</span></span>        |
| <span data-ttu-id="3ee50-124">DestName</span><span class="sxs-lookup"><span data-stu-id="3ee50-124">DestName</span></span>    | [<span data-ttu-id="3ee50-125">Nom du fichier</span><span class="sxs-lookup"><span data-stu-id="3ee50-125">Filename</span></span>](filename.md)     | <span data-ttu-id="3ee50-126">N</span><span class="sxs-lookup"><span data-stu-id="3ee50-126">N</span></span>   | <span data-ttu-id="3ee50-127">O</span><span class="sxs-lookup"><span data-stu-id="3ee50-127">Y</span></span>        |
| <span data-ttu-id="3ee50-128">DestFolder</span><span class="sxs-lookup"><span data-stu-id="3ee50-128">DestFolder</span></span>  | [<span data-ttu-id="3ee50-129">Identificateur</span><span class="sxs-lookup"><span data-stu-id="3ee50-129">Identifier</span></span>](identifier.md) | <span data-ttu-id="3ee50-130">N</span><span class="sxs-lookup"><span data-stu-id="3ee50-130">N</span></span>   | <span data-ttu-id="3ee50-131">O</span><span class="sxs-lookup"><span data-stu-id="3ee50-131">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="3ee50-132">Colonnes</span><span class="sxs-lookup"><span data-stu-id="3ee50-132">Columns</span></span>

<dl> <dt>

<span data-ttu-id="3ee50-133"><span id="FileKey"></span><span id="filekey"></span><span id="FILEKEY"></span>FileKey</span><span class="sxs-lookup"><span data-stu-id="3ee50-133"><span id="FileKey"></span><span id="filekey"></span><span id="FILEKEY"></span>FileKey</span></span>
</dt> <dd>

<span data-ttu-id="3ee50-134">Une clé primaire, un jeton non localisé, identifiant un enregistrement DuplicateFile unique.</span><span class="sxs-lookup"><span data-stu-id="3ee50-134">A primary key, a non-localized token, identifying a unique DuplicateFile record.</span></span>

</dd> <dt>

<span data-ttu-id="3ee50-135"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>-\_</span><span class="sxs-lookup"><span data-stu-id="3ee50-135"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Component\_</span></span>
</dt> <dd>

<span data-ttu-id="3ee50-136">Clé externe de la première colonne de la [table de composants](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="3ee50-136">An external key to the first column of the [Component table](component-table.md).</span></span> <span data-ttu-id="3ee50-137">Si le composant identifié par la clé n’est pas sélectionné pour l’installation ou la suppression, aucune action n’est effectuée sur cet enregistrement DuplicateFile.</span><span class="sxs-lookup"><span data-stu-id="3ee50-137">If the component identified by the key is not selected for installation or removal, then no action is taken on this DuplicateFile record.</span></span>

</dd> <dt>

<span data-ttu-id="3ee50-138"><span id="File_"></span><span id="file_"></span><span id="FILE_"></span>Txt\_</span><span class="sxs-lookup"><span data-stu-id="3ee50-138"><span id="File_"></span><span id="file_"></span><span id="FILE_"></span>File\_</span></span>
</dt> <dd>

<span data-ttu-id="3ee50-139">Clé étrangère dans la [table de fichiers](file-table.md) qui représente le fichier d’origine à dupliquer.</span><span class="sxs-lookup"><span data-stu-id="3ee50-139">Foreign key into the [File table](file-table.md) representing the original file that is to be duplicated.</span></span>

</dd> <dt>

<span data-ttu-id="3ee50-140"><span id="DestName"></span><span id="destname"></span><span id="DESTNAME"></span>DestName</span><span class="sxs-lookup"><span data-stu-id="3ee50-140"><span id="DestName"></span><span id="destname"></span><span id="DESTNAME"></span>DestName</span></span>
</dt> <dd>

<span data-ttu-id="3ee50-141">Nom localisable à attribuer au fichier dupliqué.</span><span class="sxs-lookup"><span data-stu-id="3ee50-141">Localizable name to be given to the duplicate file.</span></span> <span data-ttu-id="3ee50-142">Si ce champ est vide, le fichier de destination se voit attribuer le même nom que le fichier d’origine.</span><span class="sxs-lookup"><span data-stu-id="3ee50-142">If this field is blank, then the destination file is given the same name as the original file.</span></span>

</dd> <dt>

<span data-ttu-id="3ee50-143"><span id="DestFolder"></span><span id="destfolder"></span><span id="DESTFOLDER"></span>DestFolder</span><span class="sxs-lookup"><span data-stu-id="3ee50-143"><span id="DestFolder"></span><span id="destfolder"></span><span id="DESTFOLDER"></span>DestFolder</span></span>
</dt> <dd>

<span data-ttu-id="3ee50-144">Nom d’une propriété qui est le chemin d’accès complet à l’emplacement où le fichier dupliqué doit être copié.</span><span class="sxs-lookup"><span data-stu-id="3ee50-144">Name of a property that is the full path to where the duplicate file is to be copied.</span></span> <span data-ttu-id="3ee50-145">Si ce répertoire est le même que le répertoire contenant le fichier d’origine et que le nom du fichier dupliqué proposé est identique à l’original, aucune action n’a lieu.</span><span class="sxs-lookup"><span data-stu-id="3ee50-145">If this directory is the same as the directory containing the original file and the name for the proposed duplicate file is the same as the original, then no action takes place.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3ee50-146">Notes</span><span class="sxs-lookup"><span data-stu-id="3ee50-146">Remarks</span></span>

<span data-ttu-id="3ee50-147">La table est traitée par l' [action DuplicateFiles](duplicatefiles-action.md) et l' [action RemoveDuplicateFiles](removeduplicatefiles-action.md).</span><span class="sxs-lookup"><span data-stu-id="3ee50-147">The table is processed by the [DuplicateFiles action](duplicatefiles-action.md) and the [RemoveDuplicateFiles action](removeduplicatefiles-action.md).</span></span>

## <a name="validation"></a><span data-ttu-id="3ee50-148">Validation</span><span class="sxs-lookup"><span data-stu-id="3ee50-148">Validation</span></span>

<dl>

[<span data-ttu-id="3ee50-149">ICE03</span><span class="sxs-lookup"><span data-stu-id="3ee50-149">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="3ee50-150">ICE06</span><span class="sxs-lookup"><span data-stu-id="3ee50-150">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="3ee50-151">ICE18</span><span class="sxs-lookup"><span data-stu-id="3ee50-151">ICE18</span></span>](ice18.md)  
[<span data-ttu-id="3ee50-152">ICE32</span><span class="sxs-lookup"><span data-stu-id="3ee50-152">ICE32</span></span>](ice32.md)  
</dl>

 

 



