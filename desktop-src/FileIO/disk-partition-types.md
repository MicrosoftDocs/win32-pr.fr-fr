---
description: Types de partition valides utilisés par les pilotes de disque.
ms.assetid: b2e15b93-a02b-4d6f-b242-b5ec9a30c97b
title: Types de partition de disque (WinIoCtl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4109d4386d4892ca695fe8876b61501110cef455
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106536583"
---
# <a name="disk-partition-types"></a><span data-ttu-id="1aa0e-103">Types de partition de disque</span><span class="sxs-lookup"><span data-stu-id="1aa0e-103">Disk Partition Types</span></span>

<span data-ttu-id="1aa0e-104">Le tableau suivant identifie les types de partition valides qui sont utilisés par les pilotes de disque.</span><span class="sxs-lookup"><span data-stu-id="1aa0e-104">The following table identifies the valid partition types that are used by disk drivers.</span></span>



| <span data-ttu-id="1aa0e-105">Constante/valeur</span><span class="sxs-lookup"><span data-stu-id="1aa0e-105">Constant/value</span></span>                                                                                                                                                                                                                                      | <span data-ttu-id="1aa0e-106">Description</span><span class="sxs-lookup"><span data-stu-id="1aa0e-106">Description</span></span>                                                                                                                                                |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PARTITION_ENTRY_UNUSED"></span><span id="partition_entry_unused"></span><dl> <span data-ttu-id="1aa0e-107"><dt>**Partition \_ ENTRÉE \_ non utilisée**</dt> <dt>0x00</dt></span><span class="sxs-lookup"><span data-stu-id="1aa0e-107"><dt>**PARTITION\_ENTRY\_UNUSED**</dt> <dt>0x00</dt></span></span> </dl> | <span data-ttu-id="1aa0e-108">Partition d’entrée inutilisée.</span><span class="sxs-lookup"><span data-stu-id="1aa0e-108">An unused entry partition.</span></span><br/>                                                                                                                      |
| <span id="PARTITION_EXTENDED"></span><span id="partition_extended"></span><dl> <span data-ttu-id="1aa0e-109"><dt>**Partition \_**</dt> <dt>0x05</dt> étendu</span><span class="sxs-lookup"><span data-stu-id="1aa0e-109"><dt>**PARTITION\_EXTENDED**</dt> <dt>0x05</dt></span></span> </dl>              | <span data-ttu-id="1aa0e-110">Partition étendue.</span><span class="sxs-lookup"><span data-stu-id="1aa0e-110">An extended partition.</span></span><br/>                                                                                                                          |
| <span id="PARTITION_FAT_12"></span><span id="partition_fat_12"></span><dl> <span data-ttu-id="1aa0e-111"><dt>**Partition \_ FAT \_ 12**</dt> <dt>0x01</dt></span><span class="sxs-lookup"><span data-stu-id="1aa0e-111"><dt>**PARTITION\_FAT\_12**</dt> <dt>0x01</dt></span></span> </dl>                   | <span data-ttu-id="1aa0e-112">Partition de système de fichiers FAT12.</span><span class="sxs-lookup"><span data-stu-id="1aa0e-112">A FAT12 file system partition.</span></span><br/>                                                                                                                  |
| <span id="PARTITION_FAT_16"></span><span id="partition_fat_16"></span><dl> <span data-ttu-id="1aa0e-113"><dt>**Partition \_ FAT \_ 16**</dt> <dt>0x04</dt></span><span class="sxs-lookup"><span data-stu-id="1aa0e-113"><dt>**PARTITION\_FAT\_16**</dt> <dt>0x04</dt></span></span> </dl>                   | <span data-ttu-id="1aa0e-114">Partition de système de fichiers FAT16.</span><span class="sxs-lookup"><span data-stu-id="1aa0e-114">A FAT16 file system partition.</span></span><br/>                                                                                                                  |
| <span id="PARTITION_FAT32"></span><span id="partition_fat32"></span><dl> <span data-ttu-id="1aa0e-115"><dt>**Partition \_**</dt> <dt>0x0B</dt> FAT32</span><span class="sxs-lookup"><span data-stu-id="1aa0e-115"><dt>**PARTITION\_FAT32**</dt> <dt>0x0B</dt></span></span> </dl>                       | <span data-ttu-id="1aa0e-116">Partition de système de fichiers FAT32.</span><span class="sxs-lookup"><span data-stu-id="1aa0e-116">A FAT32 file system partition.</span></span><br/>                                                                                                                  |
| <span id="PARTITION_IFS"></span><span id="partition_ifs"></span><dl> <span data-ttu-id="1aa0e-117"><dt>**Partition \_**</dt>Le <dt>0x07</dt> IFS</span><span class="sxs-lookup"><span data-stu-id="1aa0e-117"><dt>**PARTITION\_IFS**</dt> <dt>0x07</dt></span></span> </dl>                             | <span data-ttu-id="1aa0e-118">Partition IFS.</span><span class="sxs-lookup"><span data-stu-id="1aa0e-118">An IFS partition.</span></span><br/>                                                                                                                               |
| <span id="PARTITION_LDM"></span><span id="partition_ldm"></span><dl> <span data-ttu-id="1aa0e-119"><dt>**Partition \_ LDM**</dt> <dt>0x42</dt></span><span class="sxs-lookup"><span data-stu-id="1aa0e-119"><dt>**PARTITION\_LDM**</dt> <dt>0x42</dt></span></span> </dl>                             | <span data-ttu-id="1aa0e-120">Partition LDM (Logical Disk Manager).</span><span class="sxs-lookup"><span data-stu-id="1aa0e-120">A logical disk manager (LDM) partition.</span></span><br/>                                                                                                         |
| <span id="PARTITION_NTFT"></span><span id="partition_ntft"></span><dl> <span data-ttu-id="1aa0e-121"><dt>**Partition \_ NTFT**</dt> <dt>0x80</dt></span><span class="sxs-lookup"><span data-stu-id="1aa0e-121"><dt>**PARTITION\_NTFT**</dt> <dt>0x80</dt></span></span> </dl>                          | <span data-ttu-id="1aa0e-122">Une partition NTFT.</span><span class="sxs-lookup"><span data-stu-id="1aa0e-122">An NTFT partition.</span></span><br/>                                                                                                                              |
| <span id="VALID_NTFT"></span><span id="valid_ntft"></span><dl> <span data-ttu-id="1aa0e-123"><dt>**Valide \_ NTFT**</dt> <dt>0xC0</dt></span><span class="sxs-lookup"><span data-stu-id="1aa0e-123"><dt>**VALID\_NTFT**</dt> <dt>0xC0</dt></span></span> </dl>                                      | <span data-ttu-id="1aa0e-124">Une partition NTFT valide.</span><span class="sxs-lookup"><span data-stu-id="1aa0e-124">A valid NTFT partition.</span></span><br/> <span data-ttu-id="1aa0e-125">Le bit le plus élevé d’un code de type de partition indique qu’une partition fait partie d’un miroir NTFT ou d’un tableau agrégé par bandes.</span><span class="sxs-lookup"><span data-stu-id="1aa0e-125">The high bit of a partition type code indicates that a partition is part of an NTFT mirror or striped array.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="1aa0e-126">Notes</span><span class="sxs-lookup"><span data-stu-id="1aa0e-126">Remarks</span></span>

<span data-ttu-id="1aa0e-127">Plusieurs macros peuvent vous aider à détecter le type de partition : **IsContainerPartition**, **IsFTPartition** et **IsRecognizedPartition**.</span><span class="sxs-lookup"><span data-stu-id="1aa0e-127">There are several macros that can help you detect the partition type: **IsContainerPartition**, **IsFTPartition**, and **IsRecognizedPartition**.</span></span> <span data-ttu-id="1aa0e-128">Pour plus d’informations, consultez WinIoCtl. h.</span><span class="sxs-lookup"><span data-stu-id="1aa0e-128">For more information, see WinIoCtl.h.</span></span>

## <a name="requirements"></a><span data-ttu-id="1aa0e-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1aa0e-129">Requirements</span></span>



| <span data-ttu-id="1aa0e-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1aa0e-130">Requirement</span></span> | <span data-ttu-id="1aa0e-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="1aa0e-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1aa0e-132">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1aa0e-132">Minimum supported client</span></span><br/> | <span data-ttu-id="1aa0e-133">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1aa0e-133">Windows XP \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="1aa0e-134">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1aa0e-134">Minimum supported server</span></span><br/> | <span data-ttu-id="1aa0e-135">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1aa0e-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="1aa0e-136">En-tête</span><span class="sxs-lookup"><span data-stu-id="1aa0e-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="1aa0e-137"><dt>WinIoCtl. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1aa0e-137"><dt>WinIoCtl.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1aa0e-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1aa0e-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1aa0e-139">**informations de PARTITION \_ \_ ex**</span><span class="sxs-lookup"><span data-stu-id="1aa0e-139">**PARTITION\_INFORMATION\_EX**</span></span>](/windows/desktop/api/WinIoCtl/ns-winioctl-partition_information_ex)
</dt> <dt>

[<span data-ttu-id="1aa0e-140">**\_MBR des informations de partition \_**</span><span class="sxs-lookup"><span data-stu-id="1aa0e-140">**PARTITION\_INFORMATION\_MBR**</span></span>](/windows/desktop/api/WinIoCtl/ns-winioctl-partition_information_mbr)
</dt> <dt>

[<span data-ttu-id="1aa0e-141">**DÉFINIR \_ les \_ informations de partition**</span><span class="sxs-lookup"><span data-stu-id="1aa0e-141">**SET\_PARTITION\_INFORMATION**</span></span>](/windows/desktop/api/WinIoCtl/ns-winioctl-set_partition_information)
</dt> </dl>

 

 




