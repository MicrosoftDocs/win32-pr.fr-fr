---
description: Représente une adresse dans la table de fichiers maîtres (MFT). L’adresse est marquée avec un numéro de séquence réutilisé circulairement qui est défini au moment où la référence de segment MFT était valide.
ms.assetid: 59d83b95-83fb-4630-8ce4-f58441c748ab
title: Structure MFT_SEGMENT_REFERENCE
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MFT_SEGMENT_REFERENCE
api_type:
- NA
api_location: ''
ms.openlocfilehash: beabe7620dadd01b25b3556715b33e2f10c2c230
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104109930"
---
# <a name="mft_segment_reference-structure"></a><span data-ttu-id="ebff3-104">Structure de référence du \_ segment MFT \_</span><span class="sxs-lookup"><span data-stu-id="ebff3-104">MFT\_SEGMENT\_REFERENCE structure</span></span>

<span data-ttu-id="ebff3-105">\[Cette structure est valide uniquement pour la version 3 des volumes NTFS ; elles peuvent être modifiées dans les versions ultérieures.\]</span><span class="sxs-lookup"><span data-stu-id="ebff3-105">\[This structure is valid only for version 3 of NTFS volumes; it may be altered in future versions.\]</span></span>

<span data-ttu-id="ebff3-106">Représente une adresse dans la table de fichiers maîtres (MFT).</span><span class="sxs-lookup"><span data-stu-id="ebff3-106">Represents an address in the master file table (MFT).</span></span> <span data-ttu-id="ebff3-107">L’adresse est marquée avec un numéro de séquence réutilisé circulairement qui est défini au moment où la référence de segment MFT était valide.</span><span class="sxs-lookup"><span data-stu-id="ebff3-107">The address is tagged with a circularly reused sequence number that is set at the time the MFT segment reference was valid.</span></span>

## <a name="syntax"></a><span data-ttu-id="ebff3-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ebff3-108">Syntax</span></span>


```C++
typedef struct _MFT_SEGMENT_REFERENCE {
  ULONG  SegmentNumberLowPart;
  USHORT SegmentNumberHighPart;
  USHORT SequenceNumber;
} MFT_SEGMENT_REFERENCE, *PMFT_SEGMENT_REFERENCE;
```



## <a name="members"></a><span data-ttu-id="ebff3-109">Membres</span><span class="sxs-lookup"><span data-stu-id="ebff3-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="ebff3-110">**SegmentNumberLowPart**</span><span class="sxs-lookup"><span data-stu-id="ebff3-110">**SegmentNumberLowPart**</span></span>
</dt> <dd>

<span data-ttu-id="ebff3-111">Partie inférieure du numéro de segment.</span><span class="sxs-lookup"><span data-stu-id="ebff3-111">The low part of the segment number.</span></span>

</dd> <dt>

<span data-ttu-id="ebff3-112">**SegmentNumberHighPart**</span><span class="sxs-lookup"><span data-stu-id="ebff3-112">**SegmentNumberHighPart**</span></span>
</dt> <dd>

<span data-ttu-id="ebff3-113">Partie haute du numéro de segment.</span><span class="sxs-lookup"><span data-stu-id="ebff3-113">The high part of the segment number.</span></span>

</dd> <dt>

<span data-ttu-id="ebff3-114">**SequenceNumber**</span><span class="sxs-lookup"><span data-stu-id="ebff3-114">**SequenceNumber**</span></span>
</dt> <dd>

<span data-ttu-id="ebff3-115">Numéro de séquence différent de zéro.</span><span class="sxs-lookup"><span data-stu-id="ebff3-115">The nonzero sequence number.</span></span> <span data-ttu-id="ebff3-116">La valeur 0 est réservée.</span><span class="sxs-lookup"><span data-stu-id="ebff3-116">The value 0 is reserved.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ebff3-117">Notes</span><span class="sxs-lookup"><span data-stu-id="ebff3-117">Remarks</span></span>

<span data-ttu-id="ebff3-118">Notez qu’il n’y a aucun fichier d’en-tête associé pour cette structure.</span><span class="sxs-lookup"><span data-stu-id="ebff3-118">Note that there is no associated header file for this structure.</span></span>

<span data-ttu-id="ebff3-119">Cette définition de structure est valide uniquement pour la version majeure de la version 3 et la version mineure 0 ou 1, comme indiqué par [**FSCTL \_ obtenir les \_ \_ \_ données du volume NTFS**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_ntfs_volume_data).</span><span class="sxs-lookup"><span data-stu-id="ebff3-119">This structure definition is valid only for major version 3 and minor version 0 or 1, as reported by [**FSCTL\_GET\_NTFS\_VOLUME\_DATA**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_ntfs_volume_data).</span></span>

<span data-ttu-id="ebff3-120">Le type de données de **\_ référence de fichier** est défini comme suit.</span><span class="sxs-lookup"><span data-stu-id="ebff3-120">The **FILE\_REFERENCE** data type is defined as follows.</span></span>

``` syntax
typedef MFT_SEGMENT_REFERENCE FILE_REFERENCE, *PFILE_REFERENCE;
```

## <a name="see-also"></a><span data-ttu-id="ebff3-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ebff3-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ebff3-122">Table de fichiers maîtres</span><span class="sxs-lookup"><span data-stu-id="ebff3-122">Master File Table</span></span>](master-file-table.md)
</dt> </dl>

 

 
