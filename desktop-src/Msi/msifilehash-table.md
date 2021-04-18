---
description: La table MsiFileHash est utilisée pour stocker un hachage 128 bits d’un fichier source fourni par le package Windows Installer. Le hachage est divisé en valeurs 4 32 bits et stocké dans des colonnes distinctes de la table.
ms.assetid: 972a2784-418d-4cb3-b13c-df89b079e94c
title: Table MsiFileHash
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86acb299e5d7f099a8d49affc64810d128e88369
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515992"
---
# <a name="msifilehash-table"></a><span data-ttu-id="ea4a3-104">Table MsiFileHash</span><span class="sxs-lookup"><span data-stu-id="ea4a3-104">MsiFileHash Table</span></span>

<span data-ttu-id="ea4a3-105">La table **MsiFileHash** est utilisée pour stocker un hachage 128 bits d’un fichier source fourni par le package Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="ea4a3-105">The **MsiFileHash** table is used to store a 128-bit hash of a source file provided by the Windows Installer package.</span></span> <span data-ttu-id="ea4a3-106">Le hachage est divisé en valeurs 4 32 bits et stocké dans des colonnes distinctes de la table.</span><span class="sxs-lookup"><span data-stu-id="ea4a3-106">The hash is split into four 32-bit values and stored in separate columns of the table.</span></span>

<span data-ttu-id="ea4a3-107">Windows Installer pouvez utiliser le hachage de fichiers comme moyen de détecter et d’éliminer la copie inutile de fichiers.</span><span class="sxs-lookup"><span data-stu-id="ea4a3-107">Windows Installer can use file hashing as a means to detect and eliminate unnecessary file copying.</span></span> <span data-ttu-id="ea4a3-108">Un hachage de fichier stocké dans la table **MsiFileHash** peut être comparé à un hachage d’un fichier existant sur l’ordinateur de l’utilisateur obtenu en appelant [**MsiGetFileHash**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha).</span><span class="sxs-lookup"><span data-stu-id="ea4a3-108">A file hash stored in the **MsiFileHash** table may be compared to a hash of an existing file on the user's computer obtained by calling [**MsiGetFileHash**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha).</span></span> <span data-ttu-id="ea4a3-109">La table **MsiFileHash** peut uniquement être utilisée avec des fichiers sans version.</span><span class="sxs-lookup"><span data-stu-id="ea4a3-109">The **MsiFileHash** table can only be used with unversioned files.</span></span>

<span data-ttu-id="ea4a3-110">La table **MsiFileHash** contient les colonnes suivantes.</span><span class="sxs-lookup"><span data-stu-id="ea4a3-110">The **MsiFileHash** table has the following columns.</span></span>



| <span data-ttu-id="ea4a3-111">Colonne</span><span class="sxs-lookup"><span data-stu-id="ea4a3-111">Column</span></span>    | <span data-ttu-id="ea4a3-112">Type</span><span class="sxs-lookup"><span data-stu-id="ea4a3-112">Type</span></span>                               | <span data-ttu-id="ea4a3-113">Clé</span><span class="sxs-lookup"><span data-stu-id="ea4a3-113">Key</span></span> | <span data-ttu-id="ea4a3-114">Nullable</span><span class="sxs-lookup"><span data-stu-id="ea4a3-114">Nullable</span></span> |
|-----------|------------------------------------|-----|----------|
| <span data-ttu-id="ea4a3-115">fichier\_</span><span class="sxs-lookup"><span data-stu-id="ea4a3-115">File\_</span></span>    | [<span data-ttu-id="ea4a3-116">Identificateur</span><span class="sxs-lookup"><span data-stu-id="ea4a3-116">Identifier</span></span>](identifier.md)       | <span data-ttu-id="ea4a3-117">O</span><span class="sxs-lookup"><span data-stu-id="ea4a3-117">Y</span></span>   | <span data-ttu-id="ea4a3-118">N</span><span class="sxs-lookup"><span data-stu-id="ea4a3-118">N</span></span>        |
| <span data-ttu-id="ea4a3-119">Options</span><span class="sxs-lookup"><span data-stu-id="ea4a3-119">Options</span></span>   | [<span data-ttu-id="ea4a3-120">Integer</span><span class="sxs-lookup"><span data-stu-id="ea4a3-120">Integer</span></span>](integer.md)             | <span data-ttu-id="ea4a3-121">N</span><span class="sxs-lookup"><span data-stu-id="ea4a3-121">N</span></span>   | <span data-ttu-id="ea4a3-122">N</span><span class="sxs-lookup"><span data-stu-id="ea4a3-122">N</span></span>        |
| <span data-ttu-id="ea4a3-123">HashPart1</span><span class="sxs-lookup"><span data-stu-id="ea4a3-123">HashPart1</span></span> | [<span data-ttu-id="ea4a3-124">DoubleInteger</span><span class="sxs-lookup"><span data-stu-id="ea4a3-124">DoubleInteger</span></span>](doubleinteger.md) | <span data-ttu-id="ea4a3-125">N</span><span class="sxs-lookup"><span data-stu-id="ea4a3-125">N</span></span>   | <span data-ttu-id="ea4a3-126">N</span><span class="sxs-lookup"><span data-stu-id="ea4a3-126">N</span></span>        |
| <span data-ttu-id="ea4a3-127">HashPart2</span><span class="sxs-lookup"><span data-stu-id="ea4a3-127">HashPart2</span></span> | [<span data-ttu-id="ea4a3-128">DoubleInteger</span><span class="sxs-lookup"><span data-stu-id="ea4a3-128">DoubleInteger</span></span>](doubleinteger.md) | <span data-ttu-id="ea4a3-129">N</span><span class="sxs-lookup"><span data-stu-id="ea4a3-129">N</span></span>   | <span data-ttu-id="ea4a3-130">N</span><span class="sxs-lookup"><span data-stu-id="ea4a3-130">N</span></span>        |
| <span data-ttu-id="ea4a3-131">HashPart3</span><span class="sxs-lookup"><span data-stu-id="ea4a3-131">HashPart3</span></span> | [<span data-ttu-id="ea4a3-132">DoubleInteger</span><span class="sxs-lookup"><span data-stu-id="ea4a3-132">DoubleInteger</span></span>](doubleinteger.md) | <span data-ttu-id="ea4a3-133">N</span><span class="sxs-lookup"><span data-stu-id="ea4a3-133">N</span></span>   | <span data-ttu-id="ea4a3-134">N</span><span class="sxs-lookup"><span data-stu-id="ea4a3-134">N</span></span>        |
| <span data-ttu-id="ea4a3-135">Hashpart4</span><span class="sxs-lookup"><span data-stu-id="ea4a3-135">Hashpart4</span></span> | [<span data-ttu-id="ea4a3-136">DoubleInteger</span><span class="sxs-lookup"><span data-stu-id="ea4a3-136">DoubleInteger</span></span>](doubleinteger.md) | <span data-ttu-id="ea4a3-137">N</span><span class="sxs-lookup"><span data-stu-id="ea4a3-137">N</span></span>   | <span data-ttu-id="ea4a3-138">N</span><span class="sxs-lookup"><span data-stu-id="ea4a3-138">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="ea4a3-139">Colonnes</span><span class="sxs-lookup"><span data-stu-id="ea4a3-139">Columns</span></span>

<dl> <dt>

<span data-ttu-id="ea4a3-140"><span id="File_"></span><span id="file_"></span><span id="FILE_"></span>Txt\_</span><span class="sxs-lookup"><span data-stu-id="ea4a3-140"><span id="File_"></span><span id="file_"></span><span id="FILE_"></span>File\_</span></span>
</dt> <dd>

<span data-ttu-id="ea4a3-141">Clé étrangère vers [table de fichiers](file-table.md).</span><span class="sxs-lookup"><span data-stu-id="ea4a3-141">Foreign key to [File table](file-table.md).</span></span> <span data-ttu-id="ea4a3-142">chaîne de caractères 72.</span><span class="sxs-lookup"><span data-stu-id="ea4a3-142">72 char string.</span></span>

</dd> <dt>

<span data-ttu-id="ea4a3-143"><span id="Options"></span><span id="options"></span><span id="OPTIONS"></span>Options</span><span class="sxs-lookup"><span data-stu-id="ea4a3-143"><span id="Options"></span><span id="options"></span><span id="OPTIONS"></span>Options</span></span>
</dt> <dd>

<span data-ttu-id="ea4a3-144">Cette colonne doit avoir la valeur 0 et être réservée à une utilisation ultérieure.</span><span class="sxs-lookup"><span data-stu-id="ea4a3-144">This column must be 0 and is reserved for future use.</span></span>

</dd> <dt>

<span data-ttu-id="ea4a3-145"><span id="HashPart1"></span><span id="hashpart1"></span><span id="HASHPART1"></span>HashPart1</span><span class="sxs-lookup"><span data-stu-id="ea4a3-145"><span id="HashPart1"></span><span id="hashpart1"></span><span id="HASHPART1"></span>HashPart1</span></span>
</dt> <dd>

<span data-ttu-id="ea4a3-146">Premier 32 bits de hachage.</span><span class="sxs-lookup"><span data-stu-id="ea4a3-146">First 32 bits of hash.</span></span> <span data-ttu-id="ea4a3-147">Le hachage de fichier entré dans ce champ doit être obtenu en appelant [**MsiGetFileHash**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha) ou la [**méthode FileHash**](installer-filehash.md).</span><span class="sxs-lookup"><span data-stu-id="ea4a3-147">The file hash entered in this field must be obtained by calling [**MsiGetFileHash**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha) or the [**FileHash method**](installer-filehash.md).</span></span> <span data-ttu-id="ea4a3-148">N’utilisez pas d’autres méthodes.</span><span class="sxs-lookup"><span data-stu-id="ea4a3-148">Do not use other methods.</span></span>

</dd> <dt>

<span data-ttu-id="ea4a3-149"><span id="HashPart2"></span><span id="hashpart2"></span><span id="HASHPART2"></span>HashPart2</span><span class="sxs-lookup"><span data-stu-id="ea4a3-149"><span id="HashPart2"></span><span id="hashpart2"></span><span id="HASHPART2"></span>HashPart2</span></span>
</dt> <dd>

<span data-ttu-id="ea4a3-150">Deuxième 32 bits de hachage.</span><span class="sxs-lookup"><span data-stu-id="ea4a3-150">Second 32 bits of hash.</span></span> <span data-ttu-id="ea4a3-151">Le hachage de fichier entré dans ce champ doit être obtenu en appelant [**MsiGetFileHash**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha) ou la [**méthode FileHash**](installer-filehash.md).</span><span class="sxs-lookup"><span data-stu-id="ea4a3-151">The file hash entered in this field must be obtained by calling [**MsiGetFileHash**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha) or the [**FileHash method**](installer-filehash.md).</span></span> <span data-ttu-id="ea4a3-152">N’utilisez pas d’autres méthodes de hachage.</span><span class="sxs-lookup"><span data-stu-id="ea4a3-152">Do not use other hashing methods.</span></span>

</dd> <dt>

<span data-ttu-id="ea4a3-153"><span id="HashPart3"></span><span id="hashpart3"></span><span id="HASHPART3"></span>HashPart3</span><span class="sxs-lookup"><span data-stu-id="ea4a3-153"><span id="HashPart3"></span><span id="hashpart3"></span><span id="HASHPART3"></span>HashPart3</span></span>
</dt> <dd>

<span data-ttu-id="ea4a3-154">Troisième 32 bits de hachage.</span><span class="sxs-lookup"><span data-stu-id="ea4a3-154">Third 32 bits of hash.</span></span> <span data-ttu-id="ea4a3-155">Le hachage de fichier entré dans ce champ doit être obtenu en appelant [**MsiGetFileHash**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha) ou la [**méthode FileHash**](installer-filehash.md).</span><span class="sxs-lookup"><span data-stu-id="ea4a3-155">The file hash entered in this field must be obtained by calling [**MsiGetFileHash**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha) or the [**FileHash method**](installer-filehash.md).</span></span> <span data-ttu-id="ea4a3-156">N’utilisez pas d’autres méthodes.</span><span class="sxs-lookup"><span data-stu-id="ea4a3-156">Do not use other methods.</span></span>

</dd> <dt>

<span data-ttu-id="ea4a3-157"><span id="HashPart4"></span><span id="hashpart4"></span><span id="HASHPART4"></span>HashPart4</span><span class="sxs-lookup"><span data-stu-id="ea4a3-157"><span id="HashPart4"></span><span id="hashpart4"></span><span id="HASHPART4"></span>HashPart4</span></span>
</dt> <dd>

<span data-ttu-id="ea4a3-158">Quatrième 32 bits de hachage.</span><span class="sxs-lookup"><span data-stu-id="ea4a3-158">Fourth 32 bits of hash.</span></span> <span data-ttu-id="ea4a3-159">Le hachage de fichier entré dans ce champ doit être obtenu en appelant [**MsiGetFileHash**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha) ou la [**méthode FileHash**](installer-filehash.md).</span><span class="sxs-lookup"><span data-stu-id="ea4a3-159">The file hash entered in this field must be obtained by calling [**MsiGetFileHash**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha) or the [**FileHash method**](installer-filehash.md).</span></span> <span data-ttu-id="ea4a3-160">N’utilisez pas d’autres méthodes.</span><span class="sxs-lookup"><span data-stu-id="ea4a3-160">Do not use other methods.</span></span>

</dd> </dl>

## <a name="validation"></a><span data-ttu-id="ea4a3-161">Validation</span><span class="sxs-lookup"><span data-stu-id="ea4a3-161">Validation</span></span>

<dl>

[<span data-ttu-id="ea4a3-162">ICE03</span><span class="sxs-lookup"><span data-stu-id="ea4a3-162">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="ea4a3-163">ICE06</span><span class="sxs-lookup"><span data-stu-id="ea4a3-163">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="ea4a3-164">ICE32</span><span class="sxs-lookup"><span data-stu-id="ea4a3-164">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="ea4a3-165">ICE60</span><span class="sxs-lookup"><span data-stu-id="ea4a3-165">ICE60</span></span>](ice60.md)  
[<span data-ttu-id="ea4a3-166">ICE66</span><span class="sxs-lookup"><span data-stu-id="ea4a3-166">ICE66</span></span>](ice66.md)  
</dl>

## <a name="related-topics"></a><span data-ttu-id="ea4a3-167">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ea4a3-167">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ea4a3-168">**MsiGetFileHash**</span><span class="sxs-lookup"><span data-stu-id="ea4a3-168">**MsiGetFileHash**</span></span>](/windows/desktop/api/Msi/nf-msi-msigetfilehasha)
</dt> <dt>

[<span data-ttu-id="ea4a3-169">Contrôle de version de fichier par défaut</span><span class="sxs-lookup"><span data-stu-id="ea4a3-169">Default File Versioning</span></span>](default-file-versioning.md)
</dt> </dl>

 

 



