---
description: Représente une entrée dans la liste d’attributs.
ms.assetid: daa0c97d-2ebe-4e14-b1f8-e4be3075b13e
title: Structure ATTRIBUTE_LIST_ENTRY
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ATTRIBUTE_LIST_ENTRY
api_type:
- NA
api_location: ''
ms.openlocfilehash: 67ee65a22c9e880c76d3b250c4859077f471b018
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847017"
---
# <a name="attribute_list_entry-structure"></a><span data-ttu-id="c1b65-103">Structure d’entrée d’une liste d’attributs \_ \_</span><span class="sxs-lookup"><span data-stu-id="c1b65-103">ATTRIBUTE\_LIST\_ENTRY structure</span></span>

<span data-ttu-id="c1b65-104">\[Cette structure est valide uniquement pour la version 3 des volumes NTFS ; elles peuvent être modifiées dans les versions ultérieures.\]</span><span class="sxs-lookup"><span data-stu-id="c1b65-104">\[This structure is valid only for version 3 of NTFS volumes; it may be altered in future versions.\]</span></span>

<span data-ttu-id="c1b65-105">Représente une entrée dans la liste d’attributs.</span><span class="sxs-lookup"><span data-stu-id="c1b65-105">Represents an entry in the attribute list.</span></span>

## <a name="syntax"></a><span data-ttu-id="c1b65-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c1b65-106">Syntax</span></span>


```C++
typedef struct _ATTRIBUTE_LIST_ENTRY {
  ATTRIBUTE_TYPE_CODE   AttributeTypeCode;
  USHORT                RecordLength;
  UCHAR                 AttributeNameLength;
  UCHAR                 AttributeNameOffset;
  VCN                   LowestVcn;
  MFT_SEGMENT_REFERENCE SegmentReference;
  USHORT                Reserved;
  WCHAR                 AttributeName[1];
} ATTRIBUTE_LIST_ENTRY, *PATTRIBUTE_LIST_ENTRY;
```



## <a name="members"></a><span data-ttu-id="c1b65-107">Membres</span><span class="sxs-lookup"><span data-stu-id="c1b65-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="c1b65-108">**AttributeTypeCode**</span><span class="sxs-lookup"><span data-stu-id="c1b65-108">**AttributeTypeCode**</span></span>
</dt> <dd>

<span data-ttu-id="c1b65-109">Code du type d’attribut.</span><span class="sxs-lookup"><span data-stu-id="c1b65-109">The attribute type code.</span></span>



| <span data-ttu-id="c1b65-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="c1b65-110">Value</span></span>                                                                                                                                                                                                                                           | <span data-ttu-id="c1b65-111">Signification</span><span class="sxs-lookup"><span data-stu-id="c1b65-111">Meaning</span></span>                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="_STANDARD_INFORMATION"></span><span id="_standard_information"></span><dl> <span data-ttu-id="c1b65-112"><dt>**$Standard \_ INFORMATION**</dt> <dt>0x10</dt></span><span class="sxs-lookup"><span data-stu-id="c1b65-112"><dt>**$STANDARD\_INFORMATION**</dt> <dt>0x10</dt></span></span> </dl> | <span data-ttu-id="c1b65-113">Les attributs de fichier (par exemple, lecture seule et Archive), les horodatages (tels que la création et la dernière modification de fichier) et le nombre de liens physiques.</span><span class="sxs-lookup"><span data-stu-id="c1b65-113">File attributes (such as read-only and archive), time stamps (such as file creation and last modified), and the hard link count.</span></span><br/> |
| <span id="_ATTRIBUTE_LIST"></span><span id="_attribute_list"></span><dl> <span data-ttu-id="c1b65-114"><dt>**$Attribute \_ LISTE**</dt> <dt>0x20</dt></span><span class="sxs-lookup"><span data-stu-id="c1b65-114"><dt>**$ATTRIBUTE\_LIST**</dt> <dt>0x20</dt></span></span> </dl>                   | <span data-ttu-id="c1b65-115">Liste des attributs qui composent le fichier et la référence de fichier de l’enregistrement du fichier MFT dans lequel se trouve chaque attribut.</span><span class="sxs-lookup"><span data-stu-id="c1b65-115">A list of attributes that make up the file and the file reference of the MFT file record in which each attribute is located.</span></span><br/>     |
| <span id="_FILE_NAME"></span><span id="_file_name"></span><dl> <span data-ttu-id="c1b65-116"><dt>**$File \_ NOM**</dt> <dt>0x30</dt></span><span class="sxs-lookup"><span data-stu-id="c1b65-116"><dt>**$FILE\_NAME**</dt> <dt>0x30</dt></span></span> </dl>                                  | <span data-ttu-id="c1b65-117">Nom du fichier, en caractères Unicode.</span><span class="sxs-lookup"><span data-stu-id="c1b65-117">The name of the file, in Unicode characters.</span></span><br/>                                                                                     |
| <span id="_OBJECT_ID"></span><span id="_object_id"></span><dl> <span data-ttu-id="c1b65-118"><dt>**$Object \_ ID**</dt> <dt>0x40</dt></span><span class="sxs-lookup"><span data-stu-id="c1b65-118"><dt>**$OBJECT\_ID**</dt> <dt>0x40</dt></span></span> </dl>                                  | <span data-ttu-id="c1b65-119">Identificateur d’objet de 16 octets assigné par le service de suivi des liens.</span><span class="sxs-lookup"><span data-stu-id="c1b65-119">An 16-byte object identifier assigned by the link-tracking service.</span></span><br/>                                                              |
| <span id="_VOLUME_NAME"></span><span id="_volume_name"></span><dl> <span data-ttu-id="c1b65-120"><dt>**$Volume \_ NOM**</dt> <dt>0x60</dt></span><span class="sxs-lookup"><span data-stu-id="c1b65-120"><dt>**$VOLUME\_NAME**</dt> <dt>0x60</dt></span></span> </dl>                            | <span data-ttu-id="c1b65-121">Étiquette de volume.</span><span class="sxs-lookup"><span data-stu-id="c1b65-121">The volume label.</span></span> <span data-ttu-id="c1b65-122">Présent dans le fichier $Volume.</span><span class="sxs-lookup"><span data-stu-id="c1b65-122">Present in the $Volume file.</span></span><br/>                                                                                   |
| <span id="_VOLUME_INFORMATION"></span><span id="_volume_information"></span><dl> <span data-ttu-id="c1b65-123"><dt>**$Volume \_ INFORMATIONS**</dt> <dt>0x70</dt></span><span class="sxs-lookup"><span data-stu-id="c1b65-123"><dt>**$VOLUME\_INFORMATION**</dt> <dt>0x70</dt></span></span> </dl>       | <span data-ttu-id="c1b65-124">Informations sur le volume.</span><span class="sxs-lookup"><span data-stu-id="c1b65-124">The volume information.</span></span> <span data-ttu-id="c1b65-125">Présent dans le fichier $Volume.</span><span class="sxs-lookup"><span data-stu-id="c1b65-125">Present in the $Volume file.</span></span><br/>                                                                             |
| <span id="_DATA"></span><span id="_data"></span><dl> <span data-ttu-id="c1b65-126"><dt>**$Data**</dt> <dt>0x80</dt></span><span class="sxs-lookup"><span data-stu-id="c1b65-126"><dt>**$DATA**</dt> <dt>0x80</dt></span></span> </dl>                                                  | <span data-ttu-id="c1b65-127">Contenu du fichier.</span><span class="sxs-lookup"><span data-stu-id="c1b65-127">The contents of the file.</span></span><br/>                                                                                                        |
| <span id="_INDEX_ROOT"></span><span id="_index_root"></span><dl> <span data-ttu-id="c1b65-128"><dt>**$Index \_**</dt> <dt>0X90</dt> racine</span><span class="sxs-lookup"><span data-stu-id="c1b65-128"><dt>**$INDEX\_ROOT**</dt> <dt>0x90</dt></span></span> </dl>                               | <span data-ttu-id="c1b65-129">Utilisé pour implémenter l’allocation de noms de fichiers pour des répertoires volumineux.</span><span class="sxs-lookup"><span data-stu-id="c1b65-129">Used to implement filename allocation for large directories.</span></span><br/>                                                                     |
| <span id="_INDEX_ALLOCATION"></span><span id="_index_allocation"></span><dl> <span data-ttu-id="c1b65-130"><dt>**$Index \_ ALLOCATION**</dt> <dt>0xa0</dt></span><span class="sxs-lookup"><span data-stu-id="c1b65-130"><dt>**$INDEX\_ALLOCATION**</dt> <dt>0xA0</dt></span></span> </dl>             | <span data-ttu-id="c1b65-131">Utilisé pour implémenter l’allocation de noms de fichiers pour des répertoires volumineux.</span><span class="sxs-lookup"><span data-stu-id="c1b65-131">Used to implement filename allocation for large directories.</span></span><br/>                                                                     |
| <span id="_BITMAP"></span><span id="_bitmap"></span><dl> <span data-ttu-id="c1b65-132"><dt>**$Bitmap**</dt> <dt>0xB0</dt></span><span class="sxs-lookup"><span data-stu-id="c1b65-132"><dt>**$BITMAP**</dt> <dt>0xB0</dt></span></span> </dl>                                            | <span data-ttu-id="c1b65-133">Index bitmap pour un répertoire volumineux.</span><span class="sxs-lookup"><span data-stu-id="c1b65-133">A bitmap index for a large directory.</span></span><br/>                                                                                            |
| <span id="_REPARSE_POINT"></span><span id="_reparse_point"></span><dl> <span data-ttu-id="c1b65-134"><dt>**$REPARSE \_ POINT**</dt> <dt>0xC0</dt></span><span class="sxs-lookup"><span data-stu-id="c1b65-134"><dt>**$REPARSE\_POINT**</dt> <dt>0xC0</dt></span></span> </dl>                      | <span data-ttu-id="c1b65-135">Données du point d’analyse.</span><span class="sxs-lookup"><span data-stu-id="c1b65-135">The reparse point data.</span></span><br/>                                                                                                          |



 

</dd> <dt>

<span data-ttu-id="c1b65-136">**RecordLength**</span><span class="sxs-lookup"><span data-stu-id="c1b65-136">**RecordLength**</span></span>
</dt> <dd>

<span data-ttu-id="c1b65-137">Taille de cette structure, plus la mémoire tampon de nom facultative, en octets.</span><span class="sxs-lookup"><span data-stu-id="c1b65-137">The size of this structure, plus the optional name buffer, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="c1b65-138">**AttributeNameLength**</span><span class="sxs-lookup"><span data-stu-id="c1b65-138">**AttributeNameLength**</span></span>
</dt> <dd>

<span data-ttu-id="c1b65-139">Taille du nom d’attribut facultatif, en caractères.</span><span class="sxs-lookup"><span data-stu-id="c1b65-139">The size of the optional attribute name, in characters.</span></span> <span data-ttu-id="c1b65-140">Si un nom existe, cette valeur est différente de zéro et la structure est immédiatement suivie d’une chaîne Unicode du nombre spécifié de caractères.</span><span class="sxs-lookup"><span data-stu-id="c1b65-140">If a name exists, this value is nonzero and the structure is followed immediately by a Unicode string of the specified number of characters.</span></span>

</dd> <dt>

<span data-ttu-id="c1b65-141">**AttributeNameOffset**</span><span class="sxs-lookup"><span data-stu-id="c1b65-141">**AttributeNameOffset**</span></span>
</dt> <dd>

<span data-ttu-id="c1b65-142">Réservé.</span><span class="sxs-lookup"><span data-stu-id="c1b65-142">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="c1b65-143">**LowestVcn**</span><span class="sxs-lookup"><span data-stu-id="c1b65-143">**LowestVcn**</span></span>
</dt> <dd>

<span data-ttu-id="c1b65-144">Numéro de cluster virtuel (VCN) le plus bas pour cet attribut.</span><span class="sxs-lookup"><span data-stu-id="c1b65-144">The lowest virtual cluster number (VCN) for this attribute.</span></span> <span data-ttu-id="c1b65-145">Ce membre est égal à zéro, sauf si l’attribut requiert plusieurs segments d’enregistrement de fichier et si cette entrée est une référence à un segment autre que le premier.</span><span class="sxs-lookup"><span data-stu-id="c1b65-145">This member is zero unless the attribute requires multiple file record segments and unless this entry is a reference to a segment other than the first one.</span></span> <span data-ttu-id="c1b65-146">Dans ce cas, cette valeur est le VCN le plus bas qui est décrit par le segment référencé.</span><span class="sxs-lookup"><span data-stu-id="c1b65-146">In this case, this value is the lowest VCN that is described by the referenced segment.</span></span>

</dd> <dt>

<span data-ttu-id="c1b65-147">**SegmentReference**</span><span class="sxs-lookup"><span data-stu-id="c1b65-147">**SegmentReference**</span></span>
</dt> <dd>

<span data-ttu-id="c1b65-148">Segment de table de fichiers maîtres (MFT) dans lequel réside l’attribut.</span><span class="sxs-lookup"><span data-stu-id="c1b65-148">The master file table (MFT) segment in which the attribute resides.</span></span> <span data-ttu-id="c1b65-149">Consultez [**\_ \_ référence de segment MFT**](mft-segment-reference.md).</span><span class="sxs-lookup"><span data-stu-id="c1b65-149">See [**MFT\_SEGMENT\_REFERENCE**](mft-segment-reference.md).</span></span>

</dd> <dt>

<span data-ttu-id="c1b65-150">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="c1b65-150">**Reserved**</span></span>
</dt> <dd>

<span data-ttu-id="c1b65-151">Réservé.</span><span class="sxs-lookup"><span data-stu-id="c1b65-151">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="c1b65-152">**AttributeName**</span><span class="sxs-lookup"><span data-stu-id="c1b65-152">**AttributeName**</span></span>
</dt> <dd>

<span data-ttu-id="c1b65-153">Début du nom d’attribut facultatif.</span><span class="sxs-lookup"><span data-stu-id="c1b65-153">The start of the optional attribute name.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c1b65-154">Notes</span><span class="sxs-lookup"><span data-stu-id="c1b65-154">Remarks</span></span>

<span data-ttu-id="c1b65-155">La liste des attributs est une liste ordonnée de structures d' **\_ \_ entrée de liste d’attributs** alignés sur le mot quadruple.</span><span class="sxs-lookup"><span data-stu-id="c1b65-155">The attributes list is an ordered list of quadword-aligned **ATTRIBUTE\_LIST\_ENTRY** structures.</span></span> <span data-ttu-id="c1b65-156">Cette liste est d’abord triée par le code de type d’attribut, puis par le nom d’attribut (le cas échéant).</span><span class="sxs-lookup"><span data-stu-id="c1b65-156">This list is ordered first by the attribute type code and then by the attribute name (if present).</span></span> <span data-ttu-id="c1b65-157">Deux attributs ne peuvent pas avoir le même code de type, le même nom et le VCN le plus bas.</span><span class="sxs-lookup"><span data-stu-id="c1b65-157">No two attributes can have the same type code, name, and lowest VCN.</span></span> <span data-ttu-id="c1b65-158">Par conséquent, il ne peut y avoir qu’un seul attribut pour chaque code de type sans nom.</span><span class="sxs-lookup"><span data-stu-id="c1b65-158">Therefore, there can be at most one attribute for each type code without a name.</span></span>

<span data-ttu-id="c1b65-159">Cette définition de structure est valide uniquement pour la version majeure de la version 3 et la version mineure 0 ou 1, comme indiqué par [**FSCTL \_ obtenir les \_ \_ \_ données du volume NTFS**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_ntfs_volume_data).</span><span class="sxs-lookup"><span data-stu-id="c1b65-159">This structure definition is valid only for major version 3 and minor version 0 or 1, as reported by [**FSCTL\_GET\_NTFS\_VOLUME\_DATA**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_ntfs_volume_data).</span></span>

<span data-ttu-id="c1b65-160">Notez qu’il n’y a aucun fichier d’en-tête associé pour cette structure.</span><span class="sxs-lookup"><span data-stu-id="c1b65-160">Note that there is no associated header file for this structure.</span></span>

## <a name="see-also"></a><span data-ttu-id="c1b65-161">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c1b65-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1b65-162">Table de fichiers maîtres</span><span class="sxs-lookup"><span data-stu-id="c1b65-162">Master File Table</span></span>](master-file-table.md)
</dt> </dl>

 

 
