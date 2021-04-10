---
description: Représente le segment d’enregistrement de fichier. Il s’agit de l’en-tête pour chaque segment d’enregistrement de fichier dans la table de fichiers maîtres (MFT).
ms.assetid: 4548ad49-1924-4888-8966-c45f8e453c6f
title: Structure FILE_RECORD_SEGMENT_HEADER
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FILE_RECORD_SEGMENT_HEADER
api_type:
- NA
api_location: ''
ms.openlocfilehash: 293bb14dbaee0853aa1ef293502724458e02e26f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104200879"
---
# <a name="file_record_segment_header-structure"></a><span data-ttu-id="f81df-104">\_Structure d' \_ \_ en-tête de segment d’enregistrement de fichier</span><span class="sxs-lookup"><span data-stu-id="f81df-104">FILE\_RECORD\_SEGMENT\_HEADER structure</span></span>

<span data-ttu-id="f81df-105">\[Cette structure est valide uniquement pour la version 3 des volumes NTFS ; elles peuvent être modifiées dans les versions ultérieures.\]</span><span class="sxs-lookup"><span data-stu-id="f81df-105">\[This structure is valid only for version 3 of NTFS volumes; it may be altered in future versions.\]</span></span>

<span data-ttu-id="f81df-106">Représente le segment d’enregistrement de fichier.</span><span class="sxs-lookup"><span data-stu-id="f81df-106">Represents the file record segment.</span></span> <span data-ttu-id="f81df-107">Il s’agit de l’en-tête pour chaque segment d’enregistrement de fichier dans la table de fichiers maîtres (MFT).</span><span class="sxs-lookup"><span data-stu-id="f81df-107">This is the header for each file record segment in the master file table (MFT).</span></span>

## <a name="syntax"></a><span data-ttu-id="f81df-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f81df-108">Syntax</span></span>


```C++
typedef struct _FILE_RECORD_SEGMENT_HEADER {
  MULTI_SECTOR_HEADER   MultiSectorHeader;
  ULONGLONG             Reserved1;
  USHORT                SequenceNumber;
  USHORT                Reserved2;
  USHORT                FirstAttributeOffset;
  USHORT                Flags;
  ULONG                 Reserved3[2];
  FILE_REFERENCE        BaseFileRecordSegment;
  USHORT                Reserved4;
  UPDATE_SEQUENCE_ARRAY UpdateSequenceArray;
} FILE_RECORD_SEGMENT_HEADER, *PFILE_RECORD_SEGMENT_HEADER;
```



## <a name="members"></a><span data-ttu-id="f81df-109">Membres</span><span class="sxs-lookup"><span data-stu-id="f81df-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="f81df-110">**MultiSectorHeader**</span><span class="sxs-lookup"><span data-stu-id="f81df-110">**MultiSectorHeader**</span></span>
</dt> <dd>

<span data-ttu-id="f81df-111">En-tête multisecteur défini par le gestionnaire de cache.</span><span class="sxs-lookup"><span data-stu-id="f81df-111">The multisector header defined by the cache manager.</span></span> <span data-ttu-id="f81df-112">La structure d' [**\_ \_ en-tête multisecteur**](multi-sector-header.md) contient toujours la signature « fichier » et une description de l’emplacement et de la taille du tableau de séquences de mise à jour.</span><span class="sxs-lookup"><span data-stu-id="f81df-112">The [**MULTI\_SECTOR\_HEADER**](multi-sector-header.md) structure always contains the signature "FILE" and a description of the location and size of the update sequence array.</span></span>

</dd> <dt>

<span data-ttu-id="f81df-113">**Reserved1**</span><span class="sxs-lookup"><span data-stu-id="f81df-113">**Reserved1**</span></span>
</dt> <dd>

<span data-ttu-id="f81df-114">Réservé.</span><span class="sxs-lookup"><span data-stu-id="f81df-114">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="f81df-115">**SequenceNumber**</span><span class="sxs-lookup"><span data-stu-id="f81df-115">**SequenceNumber**</span></span>
</dt> <dd>

<span data-ttu-id="f81df-116">Numéro séquentiel.</span><span class="sxs-lookup"><span data-stu-id="f81df-116">The sequence number.</span></span> <span data-ttu-id="f81df-117">Cette valeur est incrémentée chaque fois qu’un segment d’enregistrement de fichier est libéré ; elle est égale à 0 si le segment n’est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="f81df-117">This value is incremented each time that a file record segment is freed; it is 0 if the segment is not used.</span></span> <span data-ttu-id="f81df-118">Le **champ de** champ d’une référence de fichier doit correspondre au contenu de ce champ ; Si elles ne correspondent pas, la référence de fichier est incorrecte et probablement obsolète.</span><span class="sxs-lookup"><span data-stu-id="f81df-118">The **SequenceNumber** field of a file reference must match the contents of this field; if they do not match, the file reference is incorrect and probably obsolete.</span></span>

</dd> <dt>

<span data-ttu-id="f81df-119">**Reserved2**</span><span class="sxs-lookup"><span data-stu-id="f81df-119">**Reserved2**</span></span>
</dt> <dd>

<span data-ttu-id="f81df-120">Réservé.</span><span class="sxs-lookup"><span data-stu-id="f81df-120">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="f81df-121">**FirstAttributeOffset**</span><span class="sxs-lookup"><span data-stu-id="f81df-121">**FirstAttributeOffset**</span></span>
</dt> <dd>

<span data-ttu-id="f81df-122">Décalage du premier enregistrement d’attribut, en octets.</span><span class="sxs-lookup"><span data-stu-id="f81df-122">The offset of the first attribute record, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="f81df-123">**Indicateurs**</span><span class="sxs-lookup"><span data-stu-id="f81df-123">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="f81df-124">Indicateurs de fichier.</span><span class="sxs-lookup"><span data-stu-id="f81df-124">The file flags.</span></span>

<dl> <dt>

<span data-ttu-id="f81df-125"><span id="FILE_RECORD_SEGMENT_IN_USE"></span><span id="file_record_segment_in_use"></span>**Fichier \_ \_Segment \_ d’enregistrement en cours d' \_ utilisation** (0x0001)</span><span class="sxs-lookup"><span data-stu-id="f81df-125"><span id="FILE_RECORD_SEGMENT_IN_USE"></span><span id="file_record_segment_in_use"></span>**FILE\_RECORD\_SEGMENT\_IN\_USE** (0x0001)</span></span>
</dt> <dt>

<span data-ttu-id="f81df-126"><span id="FILE_FILE_NAME_INDEX_PRESENT"></span><span id="file_file_name_index_present"></span>**Fichier \_ INDEX de nom de fichier \_ \_ \_ présent** (0x0002)</span><span class="sxs-lookup"><span data-stu-id="f81df-126"><span id="FILE_FILE_NAME_INDEX_PRESENT"></span><span id="file_file_name_index_present"></span>**FILE\_FILE\_NAME\_INDEX\_PRESENT** (0x0002)</span></span>
</dt> </dl> </dd> <dt>

<span data-ttu-id="f81df-127">**Reserved3**</span><span class="sxs-lookup"><span data-stu-id="f81df-127">**Reserved3**</span></span>
</dt> <dd>

<span data-ttu-id="f81df-128">Réservé.</span><span class="sxs-lookup"><span data-stu-id="f81df-128">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="f81df-129">**BaseFileRecordSegment**</span><span class="sxs-lookup"><span data-stu-id="f81df-129">**BaseFileRecordSegment**</span></span>
</dt> <dd>

<span data-ttu-id="f81df-130">Référence de fichier au segment d’enregistrement de fichier de base pour ce fichier.</span><span class="sxs-lookup"><span data-stu-id="f81df-130">A file reference to the base file record segment for this file.</span></span> <span data-ttu-id="f81df-131">S’il s’agit de l’enregistrement de fichier de base, la valeur est 0.</span><span class="sxs-lookup"><span data-stu-id="f81df-131">If this is the base file record, the value is 0.</span></span> <span data-ttu-id="f81df-132">Consultez [**\_ \_ référence de segment MFT**](mft-segment-reference.md).</span><span class="sxs-lookup"><span data-stu-id="f81df-132">See [**MFT\_SEGMENT\_REFERENCE**](mft-segment-reference.md).</span></span>

</dd> <dt>

<span data-ttu-id="f81df-133">**Reserved4**</span><span class="sxs-lookup"><span data-stu-id="f81df-133">**Reserved4**</span></span>
</dt> <dd>

<span data-ttu-id="f81df-134">Réservé.</span><span class="sxs-lookup"><span data-stu-id="f81df-134">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="f81df-135">**UpdateSequenceArray**</span><span class="sxs-lookup"><span data-stu-id="f81df-135">**UpdateSequenceArray**</span></span>
</dt> <dd>

<span data-ttu-id="f81df-136">Tableau de séquence de mise à jour pour protéger les transferts multisecteur du segment d’enregistrement de fichier.</span><span class="sxs-lookup"><span data-stu-id="f81df-136">The update sequence array to protect multisector transfers of the file record segment.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f81df-137">Notes</span><span class="sxs-lookup"><span data-stu-id="f81df-137">Remarks</span></span>

<span data-ttu-id="f81df-138">Notez qu’il n’y a aucun fichier d’en-tête associé pour cette structure.</span><span class="sxs-lookup"><span data-stu-id="f81df-138">Note that there is no associated header file for this structure.</span></span>

<span data-ttu-id="f81df-139">Cette définition de structure est valide uniquement pour la version majeure de la version 3 et la version mineure 0 ou 1, comme indiqué par [**FSCTL \_ obtenir les \_ \_ \_ données du volume NTFS**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_ntfs_volume_data).</span><span class="sxs-lookup"><span data-stu-id="f81df-139">This structure definition is valid only for major version 3 and minor version 0 or 1, as reported by [**FSCTL\_GET\_NTFS\_VOLUME\_DATA**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_ntfs_volume_data).</span></span>

## <a name="see-also"></a><span data-ttu-id="f81df-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f81df-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f81df-141">Table de fichiers maîtres</span><span class="sxs-lookup"><span data-stu-id="f81df-141">Master File Table</span></span>](master-file-table.md)
</dt> </dl>

 

 
