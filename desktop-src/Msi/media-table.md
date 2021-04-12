---
description: La table des médias décrit l’ensemble des disques qui composent le média source pour l’installation.
ms.assetid: f9789f1d-35bf-40d6-9724-d5a160a0d06d
title: Table des médias
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a59cd8bf864aa890891873ed92a39225c6eebdf
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "104321478"
---
# <a name="media-table"></a><span data-ttu-id="8efad-103">Table des médias</span><span class="sxs-lookup"><span data-stu-id="8efad-103">Media Table</span></span>

<span data-ttu-id="8efad-104">La table des médias décrit l’ensemble des disques qui composent le média source pour l’installation.</span><span class="sxs-lookup"><span data-stu-id="8efad-104">The Media table describes the set of disks that make up the source media for the installation.</span></span>

<span data-ttu-id="8efad-105">La table des médias contient les colonnes indiquées dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="8efad-105">The Media table contains the columns shown in the following table.</span></span>



| <span data-ttu-id="8efad-106">Colonne</span><span class="sxs-lookup"><span data-stu-id="8efad-106">Column</span></span>       | <span data-ttu-id="8efad-107">Type</span><span class="sxs-lookup"><span data-stu-id="8efad-107">Type</span></span>                     | <span data-ttu-id="8efad-108">Clé</span><span class="sxs-lookup"><span data-stu-id="8efad-108">Key</span></span> | <span data-ttu-id="8efad-109">Nullable</span><span class="sxs-lookup"><span data-stu-id="8efad-109">Nullable</span></span> |
|--------------|--------------------------|-----|----------|
| <span data-ttu-id="8efad-110">DiskId</span><span class="sxs-lookup"><span data-stu-id="8efad-110">DiskId</span></span>       | [<span data-ttu-id="8efad-111">Integer</span><span class="sxs-lookup"><span data-stu-id="8efad-111">Integer</span></span>](integer.md)   | <span data-ttu-id="8efad-112">O</span><span class="sxs-lookup"><span data-stu-id="8efad-112">Y</span></span>   | <span data-ttu-id="8efad-113">N</span><span class="sxs-lookup"><span data-stu-id="8efad-113">N</span></span>        |
| <span data-ttu-id="8efad-114">LastSequence</span><span class="sxs-lookup"><span data-stu-id="8efad-114">LastSequence</span></span> | [<span data-ttu-id="8efad-115">Integer</span><span class="sxs-lookup"><span data-stu-id="8efad-115">Integer</span></span>](integer.md)   | <span data-ttu-id="8efad-116">N</span><span class="sxs-lookup"><span data-stu-id="8efad-116">N</span></span>   | <span data-ttu-id="8efad-117">N</span><span class="sxs-lookup"><span data-stu-id="8efad-117">N</span></span>        |
| <span data-ttu-id="8efad-118">DiskPrompt</span><span class="sxs-lookup"><span data-stu-id="8efad-118">DiskPrompt</span></span>   | [<span data-ttu-id="8efad-119">Text</span><span class="sxs-lookup"><span data-stu-id="8efad-119">Text</span></span>](text.md)         | <span data-ttu-id="8efad-120">N</span><span class="sxs-lookup"><span data-stu-id="8efad-120">N</span></span>   | <span data-ttu-id="8efad-121">O</span><span class="sxs-lookup"><span data-stu-id="8efad-121">Y</span></span>        |
| <span data-ttu-id="8efad-122">CAB</span><span class="sxs-lookup"><span data-stu-id="8efad-122">Cabinet</span></span>      | [<span data-ttu-id="8efad-123">CAB</span><span class="sxs-lookup"><span data-stu-id="8efad-123">Cabinet</span></span>](cabinet.md)   | <span data-ttu-id="8efad-124">N</span><span class="sxs-lookup"><span data-stu-id="8efad-124">N</span></span>   | <span data-ttu-id="8efad-125">O</span><span class="sxs-lookup"><span data-stu-id="8efad-125">Y</span></span>        |
| <span data-ttu-id="8efad-126">VolumeLabel</span><span class="sxs-lookup"><span data-stu-id="8efad-126">VolumeLabel</span></span>  | [<span data-ttu-id="8efad-127">Text</span><span class="sxs-lookup"><span data-stu-id="8efad-127">Text</span></span>](text.md)         | <span data-ttu-id="8efad-128">N</span><span class="sxs-lookup"><span data-stu-id="8efad-128">N</span></span>   | <span data-ttu-id="8efad-129">O</span><span class="sxs-lookup"><span data-stu-id="8efad-129">Y</span></span>        |
| <span data-ttu-id="8efad-130">Source</span><span class="sxs-lookup"><span data-stu-id="8efad-130">Source</span></span>       | [<span data-ttu-id="8efad-131">Propriété</span><span class="sxs-lookup"><span data-stu-id="8efad-131">Property</span></span>](property.md) | <span data-ttu-id="8efad-132">N</span><span class="sxs-lookup"><span data-stu-id="8efad-132">N</span></span>   | <span data-ttu-id="8efad-133">O</span><span class="sxs-lookup"><span data-stu-id="8efad-133">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="8efad-134">Colonnes</span><span class="sxs-lookup"><span data-stu-id="8efad-134">Columns</span></span>

<dl> <dt>

<span data-ttu-id="8efad-135"><span id="DiskId"></span><span id="diskid"></span><span id="DISKID"></span>DiskId</span><span class="sxs-lookup"><span data-stu-id="8efad-135"><span id="DiskId"></span><span id="diskid"></span><span id="DISKID"></span>DiskId</span></span>
</dt> <dd>

<span data-ttu-id="8efad-136">Détermine l’ordre de tri de la table.</span><span class="sxs-lookup"><span data-stu-id="8efad-136">Determines the sort order for the table.</span></span> <span data-ttu-id="8efad-137">Ce nombre doit être supérieur ou égal à 1.</span><span class="sxs-lookup"><span data-stu-id="8efad-137">This number must be equal to or greater than 1.</span></span>

</dd> <dt>

<span data-ttu-id="8efad-138"><span id="LastSequence"></span><span id="lastsequence"></span><span id="LASTSEQUENCE"></span>LastSequence</span><span class="sxs-lookup"><span data-stu-id="8efad-138"><span id="LastSequence"></span><span id="lastsequence"></span><span id="LASTSEQUENCE"></span>LastSequence</span></span>
</dt> <dd>

<span data-ttu-id="8efad-139">Numéro de séquence du fichier pour le dernier fichier de ce média.</span><span class="sxs-lookup"><span data-stu-id="8efad-139">File sequence number for the last file for this media.</span></span> <span data-ttu-id="8efad-140">Les nombres dans la colonne LastSequence spécifient les fichiers de la table de [fichiers](file-table.md) qui se trouvent sur un disque source particulier.</span><span class="sxs-lookup"><span data-stu-id="8efad-140">The numbers in the LastSequence column specify which of the files in the [File](file-table.md) table are found on a particular source disk.</span></span> <span data-ttu-id="8efad-141">Chaque disque source contient tous les fichiers avec des numéros de séquence (comme indiqué dans la colonne séquence de la table file) inférieurs ou égaux à la valeur de la colonne LastSequence et supérieur à la valeur LastSequence du disque précédent (ou supérieur à 0, pour la première entrée de la table Media).</span><span class="sxs-lookup"><span data-stu-id="8efad-141">Each source disk contains all files with sequence numbers (as shown in the Sequence column of the File table) less than or equal to the value in the LastSequence column, and greater than the LastSequence value of the previous disk (or greater than 0, for the first entry in the Media table).</span></span> <span data-ttu-id="8efad-142">Ce nombre ne doit pas être négatif. la limite maximale est de 32767 fichiers.</span><span class="sxs-lookup"><span data-stu-id="8efad-142">This number must be non-negative; the maximum limit is 32767 files.</span></span> <span data-ttu-id="8efad-143">Pour plus d’informations sur la création d’un package Windows Installer avec d’autres fichiers, consultez [création d’un package volumineux](authoring-a-large-package.md).</span><span class="sxs-lookup"><span data-stu-id="8efad-143">For more information about creating a Windows Installer package with more files, see [Authoring a Large Package](authoring-a-large-package.md).</span></span>

</dd> <dt>

<span data-ttu-id="8efad-144"><span id="DiskPrompt"></span><span id="diskprompt"></span><span id="DISKPROMPT"></span>DiskPrompt</span><span class="sxs-lookup"><span data-stu-id="8efad-144"><span id="DiskPrompt"></span><span id="diskprompt"></span><span id="DISKPROMPT"></span>DiskPrompt</span></span>
</dt> <dd>

<span data-ttu-id="8efad-145">Le nom du disque, qui est généralement le texte visible imprimé sur le disque.</span><span class="sxs-lookup"><span data-stu-id="8efad-145">The disk name, which is usually the visible text printed on the disk.</span></span> <span data-ttu-id="8efad-146">Ce texte localisable est utilisé pour inviter l’utilisateur lorsque ce disque doit être inséré.</span><span class="sxs-lookup"><span data-stu-id="8efad-146">This localizable text is used to prompt the user when this disk needs to be inserted.</span></span>

</dd> <dt>

<span data-ttu-id="8efad-147"><span id="Cabinet"></span><span id="cabinet"></span><span id="CABINET"></span>CAB</span><span class="sxs-lookup"><span data-stu-id="8efad-147"><span id="Cabinet"></span><span id="cabinet"></span><span id="CABINET"></span>Cabinet</span></span>
</dt> <dd>

<span data-ttu-id="8efad-148">Nom de l’armoire si certains ou l’ensemble des fichiers stockés sur le support sont compressés dans un fichier CAB.</span><span class="sxs-lookup"><span data-stu-id="8efad-148">The name of the cabinet if some or all of the files stored on the media are compressed into a cabinet file.</span></span> <span data-ttu-id="8efad-149">Si aucune armoire n’est utilisée, cette colonne doit être vide.</span><span class="sxs-lookup"><span data-stu-id="8efad-149">If no cabinets are used, this column must be blank.</span></span> <span data-ttu-id="8efad-150">Le nom du fichier cab doit utiliser la syntaxe du type de données [Cabinet](cabinet.md) .</span><span class="sxs-lookup"><span data-stu-id="8efad-150">The name of the cabinet must use the syntax of the [Cabinet](cabinet.md) data type.</span></span> <span data-ttu-id="8efad-151">Windows Installer requiert toujours une source valide pour réparer les fichiers inclus dans les fichiers CAB incorporés.</span><span class="sxs-lookup"><span data-stu-id="8efad-151">Windows Installer always requires a valid source to repair files included in embedded cabinet files.</span></span> <span data-ttu-id="8efad-152">Lorsque Windows Installer installe un package contenant un fichier CAB incorporé, une copie du fichier CAB peut être enregistrée par le système.</span><span class="sxs-lookup"><span data-stu-id="8efad-152">When Windows Installer installs a package containing an embedded cabinet file, a copy of the cabinet file can be saved by the system.</span></span> <span data-ttu-id="8efad-153">Cette copie ne peut pas être utilisée pour réparer le fichier CAB.</span><span class="sxs-lookup"><span data-stu-id="8efad-153">This copy cannot be used to repair the cabinet file.</span></span> <span data-ttu-id="8efad-154">Pour économiser de l’espace disque, utilisez des fichiers CAB externes plutôt que des fichiers CAB incorporés.</span><span class="sxs-lookup"><span data-stu-id="8efad-154">To conserve disk space, use external cabinet files instead of embedded cabinet files.</span></span>

</dd> <dt>

<span data-ttu-id="8efad-155"><span id="VolumeLabel"></span><span id="volumelabel"></span><span id="VOLUMELABEL"></span>VolumeLabel</span><span class="sxs-lookup"><span data-stu-id="8efad-155"><span id="VolumeLabel"></span><span id="volumelabel"></span><span id="VOLUMELABEL"></span>VolumeLabel</span></span>
</dt> <dd>

<span data-ttu-id="8efad-156">Étiquette attribuée au volume.</span><span class="sxs-lookup"><span data-stu-id="8efad-156">The label attributed to the volume.</span></span> <span data-ttu-id="8efad-157">Il s’agit de l’étiquette de volume retournée par la fonction [**GetVolumeInformation**](/windows/win32/api/fileapi/nf-fileapi-getvolumeinformationa) .</span><span class="sxs-lookup"><span data-stu-id="8efad-157">This is the volume label returned by the [**GetVolumeInformation**](/windows/win32/api/fileapi/nf-fileapi-getvolumeinformationa) function.</span></span> <span data-ttu-id="8efad-158">Si la propriété [**SourceDir**](sourcedir.md) fait référence à un volume amovible (disquette ou CD-ROM), ce nom de volume est utilisé pour vérifier que le disque approprié se trouve dans le lecteur avant de tenter d’installer des fichiers.</span><span class="sxs-lookup"><span data-stu-id="8efad-158">If the [**SourceDir**](sourcedir.md) property refers to a removable (floppy or CD-ROM) volume, then this volume label is used to verify that the proper disk is in the drive before attempting to install files.</span></span> <span data-ttu-id="8efad-159">L’entrée dans cette colonne doit correspondre à l’étiquette de volume du support physique.</span><span class="sxs-lookup"><span data-stu-id="8efad-159">The entry in this column must match the volume label of the physical media.</span></span>

</dd> <dt>

<span data-ttu-id="8efad-160"><span id="Source"></span><span id="source"></span><span id="SOURCE"></span>Code</span><span class="sxs-lookup"><span data-stu-id="8efad-160"><span id="Source"></span><span id="source"></span><span id="SOURCE"></span>Source</span></span>
</dt> <dd>

<span data-ttu-id="8efad-161">Ce champ est utilisé uniquement par la mise à jour corrective et n’est pas vide.</span><span class="sxs-lookup"><span data-stu-id="8efad-161">This field is only used by patching and is otherwise left blank.</span></span> <span data-ttu-id="8efad-162">Une transformation de correctif peut entrer ici une propriété qui correspond à l’emplacement du fichier cab contenant les fichiers correctifs ou les nouveaux fichiers ajoutés par le correctif.</span><span class="sxs-lookup"><span data-stu-id="8efad-162">A patch transform can enter a property here that is the location of the cabinet file containing the patch files or any new files added by the patch.</span></span> <span data-ttu-id="8efad-163">Vous devez spécifier une source différente pour ces fichiers, car la source du package de correctifs peut être stockée séparément de la source du produit.</span><span class="sxs-lookup"><span data-stu-id="8efad-163">A different source needs to be specified for these files because the source of the patch package can be stored separately from the product's source.</span></span> <span data-ttu-id="8efad-164">Si le champ Cabinet est vide, le programme d’installation ignore la valeur de cette colonne.</span><span class="sxs-lookup"><span data-stu-id="8efad-164">If the Cabinet field is empty, the installer ignores the value in this column.</span></span> <span data-ttu-id="8efad-165">Si ce champ est vide, le programme d’installation utilise la valeur de la propriété [**SourceDir**](sourcedir.md) comme source du fichier CAB.</span><span class="sxs-lookup"><span data-stu-id="8efad-165">If this field is empty, the installer uses the value of the [**SourceDir**](sourcedir.md) property as the source of the cabinet.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8efad-166">Notes</span><span class="sxs-lookup"><span data-stu-id="8efad-166">Remarks</span></span>

<span data-ttu-id="8efad-167">Si le nom du fichier cab est précédé d’un signe dièse ( \# ), les fichiers qui font référence à cet enregistrement de table de média sont empaquetés dans un fichier CAB stocké dans la base de données sous la forme d’un flux distinct.</span><span class="sxs-lookup"><span data-stu-id="8efad-167">If the cabinet name is preceded by a number sign (\#), then the files referencing this Media table record are packed in a cabinet file that is stored within the database as a separate stream.</span></span>

<span data-ttu-id="8efad-168">Pour plus d’informations sur l’ajout d’armoires aux tables de fichiers et aux tables multimédias, consultez [utilisation des armoires et des sources compressées](using-cabinets-and-compressed-sources.md).</span><span class="sxs-lookup"><span data-stu-id="8efad-168">For more information about how to add cabinets to the File tables and Media tables, see [Using Cabinets and Compressed Sources](using-cabinets-and-compressed-sources.md).</span></span>

<span data-ttu-id="8efad-169">Windows Installer nécessite que le fichier. msi se trouve sur le premier disque d’un support amovible (CD, DVD ou disquette) utilisé pour l’installation du produit.</span><span class="sxs-lookup"><span data-stu-id="8efad-169">Windows Installer requires that the .msi file be on the first disk of removable media (CD, DVD or floppy) used for the product's installation.</span></span>

<span data-ttu-id="8efad-170">**Détermination de la SourceMode**</span><span class="sxs-lookup"><span data-stu-id="8efad-170">**Determining the SourceMode**</span></span>

<span data-ttu-id="8efad-171">La propriété [**Résumé du nombre de mots**](word-count-summary.md) détermine le mode source pour l’installation actuelle.</span><span class="sxs-lookup"><span data-stu-id="8efad-171">The [**Word Count Summary**](word-count-summary.md) property determines the source mode for the current install.</span></span> <span data-ttu-id="8efad-172">Si cette propriété a la valeur 2 ou 3, l’installation d’un fichier cab est supposée.</span><span class="sxs-lookup"><span data-stu-id="8efad-172">If this property is set to 2 or 3, a cabinet install is assumed.</span></span> <span data-ttu-id="8efad-173">Dans ce mode, les fichiers CAB sont supposés exister dans le répertoire indiqué par la propriété [**SourceDir**](sourcedir.md) .</span><span class="sxs-lookup"><span data-stu-id="8efad-173">In this mode, the cabinet files are assumed to exist in the directory indicated by the [**SourceDir**](sourcedir.md) property.</span></span> <span data-ttu-id="8efad-174">Si la valeur du type de source est 0 ou 1, tous les fichiers sources sont supposés exister dans l’arborescence dont la racine est indiquée par la propriété **SourceDir** .</span><span class="sxs-lookup"><span data-stu-id="8efad-174">If the Source Type value is 0 or 1, all source files are assumed to exist in the tree whose root is indicated by the **SourceDir** property.</span></span>

<span data-ttu-id="8efad-175">Notez que cela s’applique uniquement aux fichiers de la table de fichiers qui n’ont pas les bits compressés ou non compressés définis dans la colonne attributs.</span><span class="sxs-lookup"><span data-stu-id="8efad-175">Note that this only applies to files in the File table that do not have either the Compressed or Uncompressed bits set in the attributes column.</span></span> <span data-ttu-id="8efad-176">Ces bits remplacent la valeur de la propriété [**Résumé du nombre de mots**](word-count-summary.md) lorsque vous déterminez si un fichier particulier est compressé ou non.</span><span class="sxs-lookup"><span data-stu-id="8efad-176">These bits override the value of the [**Word Count Summary**](word-count-summary.md) property when determining if a particular file is compressed or uncompressed.</span></span>

## <a name="validation"></a><span data-ttu-id="8efad-177">Validation</span><span class="sxs-lookup"><span data-stu-id="8efad-177">Validation</span></span>

<dl>

[<span data-ttu-id="8efad-178">ICE03</span><span class="sxs-lookup"><span data-stu-id="8efad-178">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="8efad-179">ICE04</span><span class="sxs-lookup"><span data-stu-id="8efad-179">ICE04</span></span>](ice04.md)  
[<span data-ttu-id="8efad-180">ICE06</span><span class="sxs-lookup"><span data-stu-id="8efad-180">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="8efad-181">ICE35</span><span class="sxs-lookup"><span data-stu-id="8efad-181">ICE35</span></span>](ice35.md)  
[<span data-ttu-id="8efad-182">ICE58</span><span class="sxs-lookup"><span data-stu-id="8efad-182">ICE58</span></span>](ice58.md)  
[<span data-ttu-id="8efad-183">ICE71</span><span class="sxs-lookup"><span data-stu-id="8efad-183">ICE71</span></span>](ice71.md)  
[<span data-ttu-id="8efad-184">ICE81</span><span class="sxs-lookup"><span data-stu-id="8efad-184">ICE81</span></span>](ice81.md)  
</dl>

 

 
