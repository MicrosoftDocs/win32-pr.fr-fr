---
description: Représente un enregistrement d’attribut.
ms.assetid: f9d9458c-b179-441c-9f62-ff0ac2f75329
title: Structure ATTRIBUTE_RECORD_HEADER
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ATTRIBUTE_RECORD_HEADER
api_type:
- NA
api_location: ''
ms.openlocfilehash: ae710ca04f11cb70c1bad9b5e6fec25f8fb5e94f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847014"
---
# <a name="attribute_record_header-structure"></a><span data-ttu-id="440de-103">\_Structure d' \_ en-tête d’enregistrement d’attribut</span><span class="sxs-lookup"><span data-stu-id="440de-103">ATTRIBUTE\_RECORD\_HEADER structure</span></span>

<span data-ttu-id="440de-104">\[Cette structure est valide uniquement pour la version 3 des volumes NTFS ; elles peuvent être modifiées dans les versions ultérieures.\]</span><span class="sxs-lookup"><span data-stu-id="440de-104">\[This structure is valid only for version 3 of NTFS volumes; it may be altered in future versions.\]</span></span>

<span data-ttu-id="440de-105">Représente un enregistrement d’attribut.</span><span class="sxs-lookup"><span data-stu-id="440de-105">Represents an attribute record.</span></span>

## <a name="syntax"></a><span data-ttu-id="440de-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="440de-106">Syntax</span></span>


```C++
typedef struct _ATTRIBUTE_RECORD_HEADER {
  ATTRIBUTE_TYPE_CODE TypeCode;
  ULONG               RecordLength;
  UCHAR               FormCode;
  UCHAR               NameLength;
  USHORT              NameOffset;
  USHORT              Flags;
  USHORT              Instance;
  union {
    struct {
      ULONG  ValueLength;
      USHORT ValueOffset;
      UCHAR  Reserved[2];
    } Resident;
    struct {
      VCN      LowestVcn;
      VCN      HighestVcn;
      USHORT   MappingPairsOffset;
      UCHAR    Reserved[6];
      LONGLONG AllocatedLength;
      LONGLONG FileSize;
      LONGLONG ValidDataLength;
      LONGLONG TotalAllocated;
    } Nonresident;
  } Form;
} ATTRIBUTE_RECORD_HEADER, *PATTRIBUTE_RECORD_HEADER;
```



## <a name="members"></a><span data-ttu-id="440de-107">Membres</span><span class="sxs-lookup"><span data-stu-id="440de-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="440de-108">**TypeCode**</span><span class="sxs-lookup"><span data-stu-id="440de-108">**TypeCode**</span></span>
</dt> <dd>

<span data-ttu-id="440de-109">Code du type d’attribut.</span><span class="sxs-lookup"><span data-stu-id="440de-109">The attribute type code.</span></span>



| <span data-ttu-id="440de-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="440de-110">Value</span></span>                                                                                                                                                                                                                                           | <span data-ttu-id="440de-111">Signification</span><span class="sxs-lookup"><span data-stu-id="440de-111">Meaning</span></span>                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="_STANDARD_INFORMATION"></span><span id="_standard_information"></span><dl> <span data-ttu-id="440de-112"><dt>**$Standard \_ INFORMATION**</dt> <dt>0x10</dt></span><span class="sxs-lookup"><span data-stu-id="440de-112"><dt>**$STANDARD\_INFORMATION**</dt> <dt>0x10</dt></span></span> </dl> | <span data-ttu-id="440de-113">Les attributs de fichier (par exemple, lecture seule et Archive), les horodatages (tels que la création et la dernière modification de fichier) et le nombre de liens physiques.</span><span class="sxs-lookup"><span data-stu-id="440de-113">File attributes (such as read-only and archive), time stamps (such as file creation and last modified), and the hard link count.</span></span><br/> |
| <span id="_ATTRIBUTE_LIST"></span><span id="_attribute_list"></span><dl> <span data-ttu-id="440de-114"><dt>**$Attribute \_ LISTE**</dt> <dt>0x20</dt></span><span class="sxs-lookup"><span data-stu-id="440de-114"><dt>**$ATTRIBUTE\_LIST**</dt> <dt>0x20</dt></span></span> </dl>                   | <span data-ttu-id="440de-115">Liste des attributs qui composent le fichier et la référence de fichier de l’enregistrement du fichier MFT dans lequel se trouve chaque attribut.</span><span class="sxs-lookup"><span data-stu-id="440de-115">A list of attributes that make up the file and the file reference of the MFT file record in which each attribute is located.</span></span><br/>     |
| <span id="_FILE_NAME"></span><span id="_file_name"></span><dl> <span data-ttu-id="440de-116"><dt>**$File \_ NOM**</dt> <dt>0x30</dt></span><span class="sxs-lookup"><span data-stu-id="440de-116"><dt>**$FILE\_NAME**</dt> <dt>0x30</dt></span></span> </dl>                                  | <span data-ttu-id="440de-117">Nom du fichier, en caractères Unicode.</span><span class="sxs-lookup"><span data-stu-id="440de-117">The name of the file, in Unicode characters.</span></span><br/>                                                                                     |
| <span id="_OBJECT_ID"></span><span id="_object_id"></span><dl> <span data-ttu-id="440de-118"><dt>**$Object \_ ID**</dt> <dt>0x40</dt></span><span class="sxs-lookup"><span data-stu-id="440de-118"><dt>**$OBJECT\_ID**</dt> <dt>0x40</dt></span></span> </dl>                                  | <span data-ttu-id="440de-119">Identificateur d’objet de 64 octets assigné par le service de suivi des liens.</span><span class="sxs-lookup"><span data-stu-id="440de-119">An 64-byte object identifier assigned by the link-tracking service.</span></span><br/>                                                              |
| <span id="_VOLUME_NAME"></span><span id="_volume_name"></span><dl> <span data-ttu-id="440de-120"><dt>**$Volume \_ NOM**</dt> <dt>0x60</dt></span><span class="sxs-lookup"><span data-stu-id="440de-120"><dt>**$VOLUME\_NAME**</dt> <dt>0x60</dt></span></span> </dl>                            | <span data-ttu-id="440de-121">Étiquette de volume.</span><span class="sxs-lookup"><span data-stu-id="440de-121">The volume label.</span></span> <span data-ttu-id="440de-122">Présent dans le fichier $Volume.</span><span class="sxs-lookup"><span data-stu-id="440de-122">Present in the $Volume file.</span></span><br/>                                                                                   |
| <span id="_VOLUME_INFORMATION"></span><span id="_volume_information"></span><dl> <span data-ttu-id="440de-123"><dt>**$Volume \_ INFORMATIONS**</dt> <dt>0x70</dt></span><span class="sxs-lookup"><span data-stu-id="440de-123"><dt>**$VOLUME\_INFORMATION**</dt> <dt>0x70</dt></span></span> </dl>       | <span data-ttu-id="440de-124">Informations sur le volume.</span><span class="sxs-lookup"><span data-stu-id="440de-124">The volume information.</span></span> <span data-ttu-id="440de-125">Présent dans le fichier $Volume.</span><span class="sxs-lookup"><span data-stu-id="440de-125">Present in the $Volume file.</span></span><br/>                                                                             |
| <span id="_DATA"></span><span id="_data"></span><dl> <span data-ttu-id="440de-126"><dt>**$Data**</dt> <dt>0x80</dt></span><span class="sxs-lookup"><span data-stu-id="440de-126"><dt>**$DATA**</dt> <dt>0x80</dt></span></span> </dl>                                                  | <span data-ttu-id="440de-127">Contenu du fichier.</span><span class="sxs-lookup"><span data-stu-id="440de-127">The contents of the file.</span></span><br/>                                                                                                        |
| <span id="_INDEX_ROOT"></span><span id="_index_root"></span><dl> <span data-ttu-id="440de-128"><dt>**$Index \_**</dt> <dt>0X90</dt> racine</span><span class="sxs-lookup"><span data-stu-id="440de-128"><dt>**$INDEX\_ROOT**</dt> <dt>0x90</dt></span></span> </dl>                               | <span data-ttu-id="440de-129">Utilisé pour implémenter l’allocation de noms de fichiers pour des répertoires volumineux.</span><span class="sxs-lookup"><span data-stu-id="440de-129">Used to implement filename allocation for large directories.</span></span><br/>                                                                     |
| <span id="_INDEX_ALLOCATION"></span><span id="_index_allocation"></span><dl> <span data-ttu-id="440de-130"><dt>**$Index \_ ALLOCATION**</dt> <dt>0xa0</dt></span><span class="sxs-lookup"><span data-stu-id="440de-130"><dt>**$INDEX\_ALLOCATION**</dt> <dt>0xA0</dt></span></span> </dl>             | <span data-ttu-id="440de-131">Utilisé pour implémenter l’allocation de noms de fichiers pour des répertoires volumineux.</span><span class="sxs-lookup"><span data-stu-id="440de-131">Used to implement filename allocation for large directories.</span></span><br/>                                                                     |
| <span id="_BITMAP"></span><span id="_bitmap"></span><dl> <span data-ttu-id="440de-132"><dt>**$Bitmap**</dt> <dt>0xB0</dt></span><span class="sxs-lookup"><span data-stu-id="440de-132"><dt>**$BITMAP**</dt> <dt>0xB0</dt></span></span> </dl>                                            | <span data-ttu-id="440de-133">Index bitmap pour un répertoire volumineux.</span><span class="sxs-lookup"><span data-stu-id="440de-133">A bitmap index for a large directory.</span></span><br/>                                                                                            |
| <span id="_REPARSE_POINT"></span><span id="_reparse_point"></span><dl> <span data-ttu-id="440de-134"><dt>**$REPARSE \_ POINT**</dt> <dt>0xC0</dt></span><span class="sxs-lookup"><span data-stu-id="440de-134"><dt>**$REPARSE\_POINT**</dt> <dt>0xC0</dt></span></span> </dl>                      | <span data-ttu-id="440de-135">Données du point d’analyse.</span><span class="sxs-lookup"><span data-stu-id="440de-135">The reparse point data.</span></span><br/>                                                                                                          |



 

</dd> <dt>

<span data-ttu-id="440de-136">**RecordLength**</span><span class="sxs-lookup"><span data-stu-id="440de-136">**RecordLength**</span></span>
</dt> <dd>

<span data-ttu-id="440de-137">Taille de l’enregistrement d’attribut, en octets.</span><span class="sxs-lookup"><span data-stu-id="440de-137">The size of the attribute record, in bytes.</span></span> <span data-ttu-id="440de-138">Cette valeur reflète la taille requise pour la variante d’enregistrement et est toujours arrondie à la limite du mot quadruple le plus proche.</span><span class="sxs-lookup"><span data-stu-id="440de-138">This value reflects the required size for the record variant and is always rounded to the nearest quadword boundary.</span></span>

</dd> <dt>

<span data-ttu-id="440de-139">**FormCode**</span><span class="sxs-lookup"><span data-stu-id="440de-139">**FormCode**</span></span>
</dt> <dd>

<span data-ttu-id="440de-140">Code du formulaire d’attribut.</span><span class="sxs-lookup"><span data-stu-id="440de-140">The attribute form code.</span></span>



| <span data-ttu-id="440de-141">Valeur</span><span class="sxs-lookup"><span data-stu-id="440de-141">Value</span></span>                                                                                                                                                                                                                            | <span data-ttu-id="440de-142">Signification</span><span class="sxs-lookup"><span data-stu-id="440de-142">Meaning</span></span>                                                                                                   |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span id="RESIDENT_FORM"></span><span id="resident_form"></span><dl> <span data-ttu-id="440de-143"><dt>**Résident \_ FORME**</dt> <dt>0x00</dt></span><span class="sxs-lookup"><span data-stu-id="440de-143"><dt>**RESIDENT\_FORM**</dt> <dt>0x00</dt></span></span> </dl>          | <span data-ttu-id="440de-144">La valeur est contenue dans l’enregistrement de fichier et suit immédiatement l’en-tête d’enregistrement d’attribut.</span><span class="sxs-lookup"><span data-stu-id="440de-144">The value is contained in the file record and immediately follows the attribute record header.</span></span><br/> |
| <span id="NONRESIDENT_FORM"></span><span id="nonresident_form"></span><dl> <span data-ttu-id="440de-145">Pas de <dt>**résident \_ FORMAT**</dt> <dt>0x01</dt></span><span class="sxs-lookup"><span data-stu-id="440de-145"><dt>**NONRESIDENT\_FORM**</dt> <dt>0x01</dt></span></span> </dl> | <span data-ttu-id="440de-146">La valeur est contenue dans d’autres secteurs sur le disque.</span><span class="sxs-lookup"><span data-stu-id="440de-146">The value is contained in other sectors on the disk.</span></span><br/>                                           |



 

</dd> <dt>

<span data-ttu-id="440de-147">**NameLength**</span><span class="sxs-lookup"><span data-stu-id="440de-147">**NameLength**</span></span>
</dt> <dd>

<span data-ttu-id="440de-148">Taille du nom d’attribut facultatif, en caractères, ou 0 s’il n’y a aucun nom d’attribut.</span><span class="sxs-lookup"><span data-stu-id="440de-148">The size of the optional attribute name, in characters, or 0 if there is no attribute name.</span></span> <span data-ttu-id="440de-149">La longueur maximale du nom d’attribut est de 255 caractères.</span><span class="sxs-lookup"><span data-stu-id="440de-149">The maximum attribute name length is 255 characters.</span></span>

</dd> <dt>

<span data-ttu-id="440de-150">**NameOffset**</span><span class="sxs-lookup"><span data-stu-id="440de-150">**NameOffset**</span></span>
</dt> <dd>

<span data-ttu-id="440de-151">Offset du nom d’attribut à partir du début de l’enregistrement d’attribut, en octets.</span><span class="sxs-lookup"><span data-stu-id="440de-151">The offset of the attribute name from the start of the attribute record, in bytes.</span></span> <span data-ttu-id="440de-152">Si le membre **NameLength** a la valeur 0, ce membre n’est pas défini.</span><span class="sxs-lookup"><span data-stu-id="440de-152">If the **NameLength** member is 0, this member is undefined.</span></span>

</dd> <dt>

<span data-ttu-id="440de-153">**Indicateurs**</span><span class="sxs-lookup"><span data-stu-id="440de-153">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="440de-154">Indicateurs d’attribut.</span><span class="sxs-lookup"><span data-stu-id="440de-154">The attribute flags.</span></span>

<dl> <dt>

<span data-ttu-id="440de-155"><span id="ATTRIBUTE_FLAG_COMPRESSION_MASK"></span><span id="attribute_flag_compression_mask"></span>**Attribut \_ \_ \_ Masque de compression des indicateurs** (0x00FF)</span><span class="sxs-lookup"><span data-stu-id="440de-155"><span id="ATTRIBUTE_FLAG_COMPRESSION_MASK"></span><span id="attribute_flag_compression_mask"></span>**ATTRIBUTE\_FLAG\_COMPRESSION\_MASK** (0x00FF)</span></span>
</dt> <dt>

<span data-ttu-id="440de-156"><span id="ATTRIBUTE_FLAG_SPARSE"></span><span id="attribute_flag_sparse"></span>**Attribut \_ INDICATEUR \_ Sparse** (0x8000)</span><span class="sxs-lookup"><span data-stu-id="440de-156"><span id="ATTRIBUTE_FLAG_SPARSE"></span><span id="attribute_flag_sparse"></span>**ATTRIBUTE\_FLAG\_SPARSE** (0x8000)</span></span>
</dt> <dt>

<span data-ttu-id="440de-157"><span id="ATTRIBUTE_FLAG_ENCRYPTED"></span><span id="attribute_flag_encrypted"></span>**Attribut \_ INDICATEUR \_ chiffré** (0x4000)</span><span class="sxs-lookup"><span data-stu-id="440de-157"><span id="ATTRIBUTE_FLAG_ENCRYPTED"></span><span id="attribute_flag_encrypted"></span>**ATTRIBUTE\_FLAG\_ENCRYPTED** (0x4000)</span></span>
</dt> </dl> </dd> <dt>

<span data-ttu-id="440de-158">**Instance**</span><span class="sxs-lookup"><span data-stu-id="440de-158">**Instance**</span></span>
</dt> <dd>

<span data-ttu-id="440de-159">Instance unique de cet attribut dans l’enregistrement de fichier.</span><span class="sxs-lookup"><span data-stu-id="440de-159">The unique instance for this attribute in the file record.</span></span>

</dd> <dt>

<span data-ttu-id="440de-160">**Forme**</span><span class="sxs-lookup"><span data-stu-id="440de-160">**Form**</span></span>
</dt> <dd>

<span data-ttu-id="440de-161">Si le membre **FormCode** est \_ un formulaire résident, l’Union est une structure **résidente** .</span><span class="sxs-lookup"><span data-stu-id="440de-161">If the **FormCode** member is RESIDENT\_FORM, the union is a **Resident** structure.</span></span> <span data-ttu-id="440de-162">Si **FormCode** n’est pas \_ une forme résidente, l’Union est une structure non **résidente** .</span><span class="sxs-lookup"><span data-stu-id="440de-162">If **FormCode** is NONRESIDENT\_FORM, the union is a **Nonresident** structure.</span></span>

<dl> <dt>

<span data-ttu-id="440de-163">**Ceux**</span><span class="sxs-lookup"><span data-stu-id="440de-163">**Resident**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="440de-164">**ValueLength**</span><span class="sxs-lookup"><span data-stu-id="440de-164">**ValueLength**</span></span>
</dt> <dd>

<span data-ttu-id="440de-165">Taille de la valeur de l’attribut, en octets.</span><span class="sxs-lookup"><span data-stu-id="440de-165">The size of the attribute value, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="440de-166">**ValueOffset**</span><span class="sxs-lookup"><span data-stu-id="440de-166">**ValueOffset**</span></span>
</dt> <dd>

<span data-ttu-id="440de-167">Offset de la valeur à partir du début de l’enregistrement d’attribut, en octets.</span><span class="sxs-lookup"><span data-stu-id="440de-167">The offset to the value from the start of the attribute record, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="440de-168">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="440de-168">**Reserved**</span></span>
</dt> <dd>

<span data-ttu-id="440de-169">Réservé.</span><span class="sxs-lookup"><span data-stu-id="440de-169">Reserved.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="440de-170">**Pas de résident**</span><span class="sxs-lookup"><span data-stu-id="440de-170">**Nonresident**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="440de-171">**LowestVcn**</span><span class="sxs-lookup"><span data-stu-id="440de-171">**LowestVcn**</span></span>
</dt> <dd>

<span data-ttu-id="440de-172">Numéro de cluster virtuel le plus bas (VCN) couvert par cet enregistrement d’attribut.</span><span class="sxs-lookup"><span data-stu-id="440de-172">The lowest virtual cluster number (VCN) covered by this attribute record.</span></span>

</dd> <dt>

<span data-ttu-id="440de-173">**HighestVcn**</span><span class="sxs-lookup"><span data-stu-id="440de-173">**HighestVcn**</span></span>
</dt> <dd>

<span data-ttu-id="440de-174">Le VCN le plus élevé couvert par cet enregistrement d’attribut.</span><span class="sxs-lookup"><span data-stu-id="440de-174">The highest VCN covered by this attribute record.</span></span>

</dd> <dt>

<span data-ttu-id="440de-175">**MappingPairsOffset**</span><span class="sxs-lookup"><span data-stu-id="440de-175">**MappingPairsOffset**</span></span>
</dt> <dd>

<span data-ttu-id="440de-176">Offset du tableau de paires de mappage à partir du début de l’enregistrement d’attribut, en octets.</span><span class="sxs-lookup"><span data-stu-id="440de-176">The offset to the mapping pairs array from the start of the attribute record, in bytes.</span></span> <span data-ttu-id="440de-177">Pour plus d'informations, consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="440de-177">For more information, see Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="440de-178">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="440de-178">**Reserved**</span></span>
</dt> <dd>

<span data-ttu-id="440de-179">Réservé.</span><span class="sxs-lookup"><span data-stu-id="440de-179">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="440de-180">**AllocatedLength**</span><span class="sxs-lookup"><span data-stu-id="440de-180">**AllocatedLength**</span></span>
</dt> <dd>

<span data-ttu-id="440de-181">Taille allouée du fichier, en octets.</span><span class="sxs-lookup"><span data-stu-id="440de-181">The allocated size of the file, in bytes.</span></span> <span data-ttu-id="440de-182">Cette valeur est un multiple pair de la taille du cluster.</span><span class="sxs-lookup"><span data-stu-id="440de-182">This value is an even multiple of the cluster size.</span></span> <span data-ttu-id="440de-183">Ce membre n’est pas valide si le membre **LowestVcn** est différent de zéro.</span><span class="sxs-lookup"><span data-stu-id="440de-183">This member is not valid if the **LowestVcn** member is nonzero.</span></span>

</dd> <dt>

<span data-ttu-id="440de-184">**FileSize**</span><span class="sxs-lookup"><span data-stu-id="440de-184">**FileSize**</span></span>
</dt> <dd>

<span data-ttu-id="440de-185">Taille de fichier (octet le plus élevé pouvant être lu plus 1), en octets.</span><span class="sxs-lookup"><span data-stu-id="440de-185">The file size (highest byte that can be read plus 1), in bytes.</span></span> <span data-ttu-id="440de-186">Ce membre n’est pas valide si **LowestVcn** est différent de zéro.</span><span class="sxs-lookup"><span data-stu-id="440de-186">This member is not valid if **LowestVcn** is nonzero.</span></span>

</dd> <dt>

<span data-ttu-id="440de-187">**ValidDataLength**</span><span class="sxs-lookup"><span data-stu-id="440de-187">**ValidDataLength**</span></span>
</dt> <dd>

<span data-ttu-id="440de-188">Longueur de données valide (plus grand octet initialisé plus 1), en octets.</span><span class="sxs-lookup"><span data-stu-id="440de-188">The valid data length (highest initialized byte plus 1), in bytes.</span></span> <span data-ttu-id="440de-189">Cette valeur est arrondie à la limite de cluster la plus proche.</span><span class="sxs-lookup"><span data-stu-id="440de-189">This value is rounded to the nearest cluster boundary.</span></span> <span data-ttu-id="440de-190">Ce membre n’est pas valide si **LowestVcn** est différent de zéro.</span><span class="sxs-lookup"><span data-stu-id="440de-190">This member is not valid if **LowestVcn** is nonzero.</span></span>

</dd> <dt>

<span data-ttu-id="440de-191">**TotalAllocated**</span><span class="sxs-lookup"><span data-stu-id="440de-191">**TotalAllocated**</span></span>
</dt> <dd>

<span data-ttu-id="440de-192">Total alloué pour le fichier (la somme des clusters alloués).</span><span class="sxs-lookup"><span data-stu-id="440de-192">The total allocated for the file (the sum of the allocated clusters).</span></span>

</dd> </dl> </dd> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="440de-193">Notes</span><span class="sxs-lookup"><span data-stu-id="440de-193">Remarks</span></span>

<span data-ttu-id="440de-194">Notez qu’il n’y a aucun fichier d’en-tête associé pour cette structure.</span><span class="sxs-lookup"><span data-stu-id="440de-194">Note that there is no associated header file for this structure.</span></span>

<span data-ttu-id="440de-195">Cette définition de structure est valide uniquement pour la version majeure de la version 3 et la version mineure 0 ou 1, comme indiqué par [**FSCTL \_ obtenir les \_ \_ \_ données du volume NTFS**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_ntfs_volume_data).</span><span class="sxs-lookup"><span data-stu-id="440de-195">This structure definition is valid only for major version 3 and minor version 0 or 1, as reported by [**FSCTL\_GET\_NTFS\_VOLUME\_DATA**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_ntfs_volume_data).</span></span>

<span data-ttu-id="440de-196">Les enregistrements d’attributs sont toujours alignés sur une limite de mot quadruple.</span><span class="sxs-lookup"><span data-stu-id="440de-196">Attribute records are always aligned on a quadword boundary.</span></span>

<span data-ttu-id="440de-197">Si l’attribut est non résident, l’en-tête d’enregistrement d’attribut contient une liste d’informations de récupération qui fournit un mappage entre VCN et le numéro de cluster logique (LCN) de l’attribut.</span><span class="sxs-lookup"><span data-stu-id="440de-197">If the attribute is nonresident, the attribute record header contains a list of retrieval information that provides a mapping between VCN and logical cluster number (LCN) for the attribute.</span></span> <span data-ttu-id="440de-198">Si les informations de récupération ne tiennent pas dans le segment de fichier de base, elles peuvent être stockées dans un segment d’enregistrement de fichier externe.</span><span class="sxs-lookup"><span data-stu-id="440de-198">If the retrieval information does not fit in the base file segment, it can be stored in an external file record segment by itself.</span></span> <span data-ttu-id="440de-199">S’il n’est toujours pas contenu dans un segment d’enregistrement de fichier externe, la liste d’attributs contient plusieurs entrées pour un attribut qui nécessite des informations de récupération supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="440de-199">If it still does not fit into one external file record segment, there is a provision in the attribute list to contain multiple entries for an attribute that requires additional retrieval information.</span></span>

<span data-ttu-id="440de-200">Le tableau de paires de mappage est stocké sous forme compressée et suppose que les informations sont décompressées et mises en cache par le système.</span><span class="sxs-lookup"><span data-stu-id="440de-200">The mapping pairs array is stored in a compressed form and assumes that the information is decompressed and cached by the system.</span></span> <span data-ttu-id="440de-201">Il se compose d’une série de paires NextVcn/CurrentLcn.</span><span class="sxs-lookup"><span data-stu-id="440de-201">It consists of a series of NextVcn/CurrentLcn pairs.</span></span> <span data-ttu-id="440de-202">Par exemple, si un fichier a une seule exécution de 8 clusters à partir de LCN 128 et que le fichier commence à LowestVcn 0, le tableau de paires de mappage n’a qu’une seule entrée, qui est NextVcn = 8 et CurrentLcn = 128.</span><span class="sxs-lookup"><span data-stu-id="440de-202">For example, if a file has a single run of 8 clusters starting at LCN 128 and the file starts at LowestVcn 0, then the mapping pairs array has just one entry, which is NextVcn=8 and CurrentLcn=128.</span></span> <span data-ttu-id="440de-203">Le tableau est un flux d’octets qui stocke les modifications apportées aux variables de travail lors du traitement séquentiel.</span><span class="sxs-lookup"><span data-stu-id="440de-203">The array is a byte stream that stores the changes to the working variables when processed sequentially.</span></span> <span data-ttu-id="440de-204">Le flux d’octets doit être interprété comme un flux de triples terminé par zéro, comme suit :</span><span class="sxs-lookup"><span data-stu-id="440de-204">The byte stream is to be interpreted as a zero-terminated stream of triples, as follows:</span></span>

<span data-ttu-id="440de-205">nombre d’octets = *v* + (*l* \* 16)</span><span class="sxs-lookup"><span data-stu-id="440de-205">count byte = *v* + (*l* \* 16)</span></span>

<span data-ttu-id="440de-206">où *v* est le nombre d’octets VCN de poids faible modifié et *l* est le nombre d’octets LCN de poids faible modifiés.</span><span class="sxs-lookup"><span data-stu-id="440de-206">where *v* is the number of changed low-order VCN bytes and *l* is the number of changed low-order LCN bytes.</span></span>

<span data-ttu-id="440de-207">L’algorithme de décompression est le suivant :</span><span class="sxs-lookup"><span data-stu-id="440de-207">The decompression algorithm is as follows:</span></span>

1.  <span data-ttu-id="440de-208">Initialisez NextVcn sur `Attribute->LowestVcn` et CurrentLcn sur 0.</span><span class="sxs-lookup"><span data-stu-id="440de-208">Initialize NextVcn to `Attribute->LowestVcn` and CurrentLcn to 0.</span></span>
2.  <span data-ttu-id="440de-209">Initialisez le pointeur de flux d’octets vers `(PCHAR)Attribute + Attribute->AttributeForm->Nonresident->MappingPairsOffset` .</span><span class="sxs-lookup"><span data-stu-id="440de-209">Initialize the byte stream pointer to `(PCHAR)Attribute + Attribute->AttributeForm->Nonresident->MappingPairsOffset`.</span></span>
3.  <span data-ttu-id="440de-210">Définissez CurrentVcn sur NextVcn.</span><span class="sxs-lookup"><span data-stu-id="440de-210">Set CurrentVcn to NextVcn.</span></span>
4.  <span data-ttu-id="440de-211">Lit l’octet suivant à partir du flux.</span><span class="sxs-lookup"><span data-stu-id="440de-211">Read the next byte from the stream.</span></span> <span data-ttu-id="440de-212">Si la valeur est 0, arrêter ; Sinon, extrayez *v* et *l* comme décrit précédemment.</span><span class="sxs-lookup"><span data-stu-id="440de-212">If it is 0, then break; else extract *v* and *l* as previously described.</span></span>
5.  <span data-ttu-id="440de-213">Interpréter les octets *v* suivants comme une quantité signée, en commençant par l’octet de poids faible.</span><span class="sxs-lookup"><span data-stu-id="440de-213">Interpret the next *v* bytes as a signed quantity, with the low-order byte first.</span></span> <span data-ttu-id="440de-214">Décompressez-le de façon à ce qu’il soit étendu à 64 bits et ajoutez-le à NextVcn.</span><span class="sxs-lookup"><span data-stu-id="440de-214">Unpack it sign-extended into 64 bits and add it to NextVcn.</span></span>
6.  <span data-ttu-id="440de-215">Interpréter les octets *suivants comme* une quantité signée, en commençant par l’octet de poids faible.</span><span class="sxs-lookup"><span data-stu-id="440de-215">Interpret the next *l* bytes as a signed quantity, with the low-order byte first.</span></span> <span data-ttu-id="440de-216">Décompressez-le de façon à ce qu’il soit étendu à 64 bits et ajoutez-le à CurrentLcn.</span><span class="sxs-lookup"><span data-stu-id="440de-216">Unpack it sign-extended into 64 bits and add it to CurrentLcn.</span></span> <span data-ttu-id="440de-217">Si cette valeur produit un CurrentLcn de 0, les VCNs de CurrentVcn à NextVcn – 1 ne sont pas alloués.</span><span class="sxs-lookup"><span data-stu-id="440de-217">If this produces a CurrentLcn of 0, then the VCNs from CurrentVcn to NextVcn–1 are unallocated.</span></span>
7.  <span data-ttu-id="440de-218">Mettez à jour les informations de mappage mises en cache à partir de CurrentVcn, NextVcn et CurrentLcn.</span><span class="sxs-lookup"><span data-stu-id="440de-218">Update the cached mapping information from CurrentVcn, NextVcn, and CurrentLcn.</span></span>
8.  <span data-ttu-id="440de-219">Passez à l’étape 3.</span><span class="sxs-lookup"><span data-stu-id="440de-219">Go to step 3.</span></span>

## <a name="see-also"></a><span data-ttu-id="440de-220">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="440de-220">See also</span></span>

<dl> <dt>

[<span data-ttu-id="440de-221">Table de fichiers maîtres</span><span class="sxs-lookup"><span data-stu-id="440de-221">Master File Table</span></span>](master-file-table.md)
</dt> </dl>

 

 
