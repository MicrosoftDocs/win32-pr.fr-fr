---
description: La table de correctifs spécifie le fichier qui doit recevoir un correctif particulier et l’emplacement physique des fichiers de correctifs sur les images de support.
ms.assetid: 1b624702-de25-4b1a-9dac-21f359ee97f7
title: Table des correctifs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 061b2082f88a8c7c3967652900bb6bf6e1c29802
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103760150"
---
# <a name="patch-table"></a><span data-ttu-id="7c82b-103">Table des correctifs</span><span class="sxs-lookup"><span data-stu-id="7c82b-103">Patch Table</span></span>

<span data-ttu-id="7c82b-104">La table de correctifs spécifie le fichier qui doit recevoir un correctif particulier et l’emplacement physique des fichiers de correctifs sur les images de support.</span><span class="sxs-lookup"><span data-stu-id="7c82b-104">The Patch table specifies the file that is to receive a particular patch and the physical location of the patch files on the media images.</span></span>

<span data-ttu-id="7c82b-105">La table des correctifs contient les colonnes suivantes.</span><span class="sxs-lookup"><span data-stu-id="7c82b-105">The Patch table has the following columns.</span></span>



| <span data-ttu-id="7c82b-106">Colonne</span><span class="sxs-lookup"><span data-stu-id="7c82b-106">Column</span></span>      | <span data-ttu-id="7c82b-107">Type</span><span class="sxs-lookup"><span data-stu-id="7c82b-107">Type</span></span>                               | <span data-ttu-id="7c82b-108">Clé</span><span class="sxs-lookup"><span data-stu-id="7c82b-108">Key</span></span> | <span data-ttu-id="7c82b-109">Nullable</span><span class="sxs-lookup"><span data-stu-id="7c82b-109">Nullable</span></span> |
|-------------|------------------------------------|-----|----------|
| <span data-ttu-id="7c82b-110">fichier\_</span><span class="sxs-lookup"><span data-stu-id="7c82b-110">File\_</span></span>      | [<span data-ttu-id="7c82b-111">Identificateur</span><span class="sxs-lookup"><span data-stu-id="7c82b-111">Identifier</span></span>](identifier.md)       | <span data-ttu-id="7c82b-112">O</span><span class="sxs-lookup"><span data-stu-id="7c82b-112">Y</span></span>   | <span data-ttu-id="7c82b-113">N</span><span class="sxs-lookup"><span data-stu-id="7c82b-113">N</span></span>        |
| <span data-ttu-id="7c82b-114">Séquence</span><span class="sxs-lookup"><span data-stu-id="7c82b-114">Sequence</span></span>    | [<span data-ttu-id="7c82b-115">Integer</span><span class="sxs-lookup"><span data-stu-id="7c82b-115">Integer</span></span>](integer.md)             | <span data-ttu-id="7c82b-116">O</span><span class="sxs-lookup"><span data-stu-id="7c82b-116">Y</span></span>   | <span data-ttu-id="7c82b-117">N</span><span class="sxs-lookup"><span data-stu-id="7c82b-117">N</span></span>        |
| <span data-ttu-id="7c82b-118">PatchSize</span><span class="sxs-lookup"><span data-stu-id="7c82b-118">PatchSize</span></span>   | [<span data-ttu-id="7c82b-119">DoubleInteger</span><span class="sxs-lookup"><span data-stu-id="7c82b-119">DoubleInteger</span></span>](doubleinteger.md) | <span data-ttu-id="7c82b-120">N</span><span class="sxs-lookup"><span data-stu-id="7c82b-120">N</span></span>   | <span data-ttu-id="7c82b-121">N</span><span class="sxs-lookup"><span data-stu-id="7c82b-121">N</span></span>        |
| <span data-ttu-id="7c82b-122">Attributs</span><span class="sxs-lookup"><span data-stu-id="7c82b-122">Attributes</span></span>  | [<span data-ttu-id="7c82b-123">Integer</span><span class="sxs-lookup"><span data-stu-id="7c82b-123">Integer</span></span>](integer.md)             | <span data-ttu-id="7c82b-124">N</span><span class="sxs-lookup"><span data-stu-id="7c82b-124">N</span></span>   | <span data-ttu-id="7c82b-125">N</span><span class="sxs-lookup"><span data-stu-id="7c82b-125">N</span></span>        |
| <span data-ttu-id="7c82b-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="7c82b-126">Header</span></span>      | [<span data-ttu-id="7c82b-127">Binaire</span><span class="sxs-lookup"><span data-stu-id="7c82b-127">Binary</span></span>](binary.md)               | <span data-ttu-id="7c82b-128">N</span><span class="sxs-lookup"><span data-stu-id="7c82b-128">N</span></span>   | <span data-ttu-id="7c82b-129">O</span><span class="sxs-lookup"><span data-stu-id="7c82b-129">Y</span></span>        |
| <span data-ttu-id="7c82b-130">StreamRef\_</span><span class="sxs-lookup"><span data-stu-id="7c82b-130">StreamRef\_</span></span> | [<span data-ttu-id="7c82b-131">Identificateur</span><span class="sxs-lookup"><span data-stu-id="7c82b-131">Identifier</span></span>](identifier.md)       | <span data-ttu-id="7c82b-132">N</span><span class="sxs-lookup"><span data-stu-id="7c82b-132">N</span></span>   | <span data-ttu-id="7c82b-133">O</span><span class="sxs-lookup"><span data-stu-id="7c82b-133">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="7c82b-134">Colonnes</span><span class="sxs-lookup"><span data-stu-id="7c82b-134">Columns</span></span>

<dl> <dt>

<span data-ttu-id="7c82b-135"><span id="File_"></span><span id="file_"></span><span id="FILE_"></span>Txt\_</span><span class="sxs-lookup"><span data-stu-id="7c82b-135"><span id="File_"></span><span id="file_"></span><span id="FILE_"></span>File\_</span></span>
</dt> <dd>

<span data-ttu-id="7c82b-136">Le correctif est appliqué au fichier spécifié par l’identificateur dans cette colonne.</span><span class="sxs-lookup"><span data-stu-id="7c82b-136">The patch is applied to the file specified by the identifier in this column.</span></span> <span data-ttu-id="7c82b-137">Il s’agit d’une clé primaire pour la table et il s’agit d’une clé étrangère de la [table de fichiers](file-table.md).</span><span class="sxs-lookup"><span data-stu-id="7c82b-137">This is a primary key for the table and it is a foreign key to the [File table](file-table.md).</span></span>

</dd> <dt>

<span data-ttu-id="7c82b-138"><span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>Séquence</span><span class="sxs-lookup"><span data-stu-id="7c82b-138"><span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>Sequence</span></span>
</dt> <dd>

<span data-ttu-id="7c82b-139">Il s’agit de la position du fichier correctif dans l’ordre séquentiel des fichiers sur les images de média.</span><span class="sxs-lookup"><span data-stu-id="7c82b-139">This is the position of the patch file in the sequence order of files on the media images.</span></span> <span data-ttu-id="7c82b-140">L’ordre des séquences doit correspondre à l’ordre des fichiers dans le fichier CAB du package correctif.</span><span class="sxs-lookup"><span data-stu-id="7c82b-140">The sequence order must correspond to the order of the files in the patch package cabinet file.</span></span> <span data-ttu-id="7c82b-141">Il s’agit d’une clé primaire pour cette table.</span><span class="sxs-lookup"><span data-stu-id="7c82b-141">This is a primary key for this table.</span></span> <span data-ttu-id="7c82b-142">La limite maximale est de 32767 fichiers. pour créer un package de Windows Installer avec d’autres fichiers, consultez [création d’un package volumineux](authoring-a-large-package.md).</span><span class="sxs-lookup"><span data-stu-id="7c82b-142">The maximum limit is 32767 files, to create a Windows Installer package with more files, see [Authoring a Large Package](authoring-a-large-package.md).</span></span>

</dd> <dt>

<span data-ttu-id="7c82b-143"><span id="PatchSize"></span><span id="patchsize"></span><span id="PATCHSIZE"></span>PatchSize</span><span class="sxs-lookup"><span data-stu-id="7c82b-143"><span id="PatchSize"></span><span id="patchsize"></span><span id="PATCHSIZE"></span>PatchSize</span></span>
</dt> <dd>

<span data-ttu-id="7c82b-144">Cette colonne indique la taille du correctif en octets écrits sous la forme d’un entier long.</span><span class="sxs-lookup"><span data-stu-id="7c82b-144">This column gives the size of the patch in bytes written as a long integer.</span></span>

</dd> <dt>

<span data-ttu-id="7c82b-145"><span id="Attributes"></span><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributs</span><span class="sxs-lookup"><span data-stu-id="7c82b-145"><span id="Attributes"></span><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>
</dt> <dd>

<span data-ttu-id="7c82b-146">Entier contenant des indicateurs binaires représentant des attributs de correctif.</span><span class="sxs-lookup"><span data-stu-id="7c82b-146">Integer containing bit flags representing patch attributes.</span></span> <span data-ttu-id="7c82b-147">Insérez la valeur 1 dans cette colonne pour indiquer que l’échec de l’application de ce correctif logiciel n’est pas une erreur irrécupérable.</span><span class="sxs-lookup"><span data-stu-id="7c82b-147">Insert a value of 1 in this column to indicate that the failure to apply this patch is not a fatal error.</span></span>



| <span data-ttu-id="7c82b-148">Constante</span><span class="sxs-lookup"><span data-stu-id="7c82b-148">Constant</span></span>                         | <span data-ttu-id="7c82b-149">Valeur hexadécimale</span><span class="sxs-lookup"><span data-stu-id="7c82b-149">Hexadecimal</span></span> | <span data-ttu-id="7c82b-150">Decimal</span><span class="sxs-lookup"><span data-stu-id="7c82b-150">Decimal</span></span> | <span data-ttu-id="7c82b-151">Description</span><span class="sxs-lookup"><span data-stu-id="7c82b-151">Description</span></span>                                                          |
|----------------------------------|-------------|---------|----------------------------------------------------------------------|
| <span data-ttu-id="7c82b-152">(aucun)</span><span class="sxs-lookup"><span data-stu-id="7c82b-152">(none)</span></span>                           | <span data-ttu-id="7c82b-153">0x000</span><span class="sxs-lookup"><span data-stu-id="7c82b-153">0x000</span></span>       | <span data-ttu-id="7c82b-154">0</span><span class="sxs-lookup"><span data-stu-id="7c82b-154">0</span></span>       | <span data-ttu-id="7c82b-155">L’échec de l’application de ce correctif est une erreur irrécupérable.</span><span class="sxs-lookup"><span data-stu-id="7c82b-155">Failure to apply this patch is a fatal error.</span></span>                        |
| <span data-ttu-id="7c82b-156">**msidbPatchAttributesNonVital**</span><span class="sxs-lookup"><span data-stu-id="7c82b-156">**msidbPatchAttributesNonVital**</span></span> | <span data-ttu-id="7c82b-157">0x001</span><span class="sxs-lookup"><span data-stu-id="7c82b-157">0x001</span></span>       | <span data-ttu-id="7c82b-158">1</span><span class="sxs-lookup"><span data-stu-id="7c82b-158">1</span></span>       | <span data-ttu-id="7c82b-159">Indique que l’échec de l’application de ce correctif n’est pas une erreur irrécupérable.</span><span class="sxs-lookup"><span data-stu-id="7c82b-159">Indicates that the failure to apply this patch is not a fatal error.</span></span> |



 

</dd> <dt>

<span data-ttu-id="7c82b-160"><span id="Header"></span><span id="header"></span><span id="HEADER"></span>Titre</span><span class="sxs-lookup"><span data-stu-id="7c82b-160"><span id="Header"></span><span id="header"></span><span id="HEADER"></span>Header</span></span>
</dt> <dd>

<span data-ttu-id="7c82b-161">Cette colonne est l’en-tête de correctif de flux binaire utilisé pour la validation des correctifs.</span><span class="sxs-lookup"><span data-stu-id="7c82b-161">This column is the binary stream patch header used for patch validation.</span></span> <span data-ttu-id="7c82b-162">Cette colonne doit avoir la valeur null si la \_ colonne StreamRef n’a pas la valeur null.</span><span class="sxs-lookup"><span data-stu-id="7c82b-162">This column should be null if the StreamRef\_ column is not null.</span></span> <span data-ttu-id="7c82b-163">Dans ce cas, le flux d’en-tête de correctif est stocké dans la [table MsiPatchHeaders](msipatchheaders-table.md) pour surmonter la limitation de nom de flux décrite dans [restrictions OLE sur les flux](ole-limitations-on-streams.md).</span><span class="sxs-lookup"><span data-stu-id="7c82b-163">In this case, the patch header stream is stored in the [MsiPatchHeaders table](msipatchheaders-table.md) to overcome the stream name limitation described in [OLE Limitations on Streams](ole-limitations-on-streams.md).</span></span>

</dd> <dt>

<span data-ttu-id="7c82b-164"><span id="StreamRef_"></span><span id="streamref_"></span><span id="STREAMREF_"></span>StreamRef\_</span><span class="sxs-lookup"><span data-stu-id="7c82b-164"><span id="StreamRef_"></span><span id="streamref_"></span><span id="STREAMREF_"></span>StreamRef\_</span></span>
</dt> <dd>

<span data-ttu-id="7c82b-165">Clé externe dans la table MsiPatchHeaders spécifiant la ligne qui contient le flux d’en-tête de correctif.</span><span class="sxs-lookup"><span data-stu-id="7c82b-165">External key into the MsiPatchHeaders table specifying the row that contains the patch header stream.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7c82b-166">Notes</span><span class="sxs-lookup"><span data-stu-id="7c82b-166">Remarks</span></span>

<span data-ttu-id="7c82b-167">Cette table est traitée par l' [action PatchFiles](patchfiles-action.md).</span><span class="sxs-lookup"><span data-stu-id="7c82b-167">This table is processed by the [PatchFiles action](patchfiles-action.md).</span></span> <span data-ttu-id="7c82b-168">Il est généralement ajouté au package d’installation par une transformation à partir d’un package de correctifs.</span><span class="sxs-lookup"><span data-stu-id="7c82b-168">It is usually added to the install package by a transform from a patch package.</span></span> <span data-ttu-id="7c82b-169">En général, il n’est pas directement créé dans un package d’installation.</span><span class="sxs-lookup"><span data-stu-id="7c82b-169">It is usually not authored directly into an install package.</span></span>

## <a name="validation"></a><span data-ttu-id="7c82b-170">Validation</span><span class="sxs-lookup"><span data-stu-id="7c82b-170">Validation</span></span>

<dl>

[<span data-ttu-id="7c82b-171">ICE03</span><span class="sxs-lookup"><span data-stu-id="7c82b-171">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="7c82b-172">ICE06</span><span class="sxs-lookup"><span data-stu-id="7c82b-172">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="7c82b-173">ICE29</span><span class="sxs-lookup"><span data-stu-id="7c82b-173">ICE29</span></span>](ice29.md)  
[<span data-ttu-id="7c82b-174">ICE45</span><span class="sxs-lookup"><span data-stu-id="7c82b-174">ICE45</span></span>](ice45.md)  
</dl>

 

 



