---
description: Cette structure contient des informations sur un emplacement sur un appareil.
ms.assetid: 37475351-DE0F-4B80-B26B-1482FBCC16CD
title: Structure STORAGE_HW_FIRMWARE_SLOT_INFO (winioctl. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- STORAGE_HW_FIRMWARE_SLOT_INFO
api_type:
- HeaderDef
api_location:
- winioctl.h.h
ms.openlocfilehash: afb38e3dc866f31b6ada6797dcb611bce1ac81a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106531803"
---
# <a name="storage_hw_firmware_slot_info-structure"></a><span data-ttu-id="04959-103">\_Structure d' \_ \_ informations sur l’emplacement du microprogramme du matériel de stockage \_</span><span class="sxs-lookup"><span data-stu-id="04959-103">STORAGE\_HW\_FIRMWARE\_SLOT\_INFO structure</span></span>

<span data-ttu-id="04959-104">Cette structure contient des informations sur un emplacement sur un appareil.</span><span class="sxs-lookup"><span data-stu-id="04959-104">This structure contains information about a slot on a device.</span></span>

## <a name="syntax"></a><span data-ttu-id="04959-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="04959-105">Syntax</span></span>


```C++
typedef struct _STORAGE_HW_FIRMWARE_SLOT_INFO {
  DWORD Version;
  DWORD Size;
  BYTE  SlotNumber;
  BYTE  ReadOnly  :1;
  BYTE  Reserved0  :7;
  BYTE  Reserved1[6];
  BYTE  Revision[STORAGE_HW_FIRMWARE_REVISION_LENGTH];
} STORAGE_HW_FIRMWARE_SLOT_INFO, *PSTORAGE_HW_FIRMWARE_SLOT_INFO;
```



## <a name="members"></a><span data-ttu-id="04959-106">Membres</span><span class="sxs-lookup"><span data-stu-id="04959-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="04959-107">**Version**</span><span class="sxs-lookup"><span data-stu-id="04959-107">**Version**</span></span>
</dt> <dd>

<span data-ttu-id="04959-108">Version de cette structure.</span><span class="sxs-lookup"><span data-stu-id="04959-108">The version of this structure.</span></span> <span data-ttu-id="04959-109">Elle doit être définie sur sizeof (stockage \_ \_ informations sur l’emplacement du microprogramme matériel de stockage \_ \_ )</span><span class="sxs-lookup"><span data-stu-id="04959-109">This should be set to sizeof(STORAGE\_HW\_FIRMWARE\_SLOT\_INFO)</span></span>

</dd> <dt>

<span data-ttu-id="04959-110">**Taille**</span><span class="sxs-lookup"><span data-stu-id="04959-110">**Size**</span></span>
</dt> <dd>

<span data-ttu-id="04959-111">La taille de cette structure.</span><span class="sxs-lookup"><span data-stu-id="04959-111">The size of this structure.</span></span>

</dd> <dt>

<span data-ttu-id="04959-112">**SlotNumber**</span><span class="sxs-lookup"><span data-stu-id="04959-112">**SlotNumber**</span></span>
</dt> <dd>

<span data-ttu-id="04959-113">Numéro de l’emplacement de cet emplacement.</span><span class="sxs-lookup"><span data-stu-id="04959-113">The slot number of this slot.</span></span>

</dd> <dt>

<span data-ttu-id="04959-114">**Lecture seule**</span><span class="sxs-lookup"><span data-stu-id="04959-114">**ReadOnly**</span></span>
</dt> <dd>

<span data-ttu-id="04959-115">Indique si cet emplacement est en lecture seule ou non.</span><span class="sxs-lookup"><span data-stu-id="04959-115">Indicates whether this slot is read-only or not.</span></span>

</dd> <dt>

<span data-ttu-id="04959-116">**Reserved0**</span><span class="sxs-lookup"><span data-stu-id="04959-116">**Reserved0**</span></span>
</dt> <dd>

<span data-ttu-id="04959-117">Réservé pour un usage futur.</span><span class="sxs-lookup"><span data-stu-id="04959-117">Reserved for future use.</span></span>

</dd> <dt>

<span data-ttu-id="04959-118">**Reserved1**</span><span class="sxs-lookup"><span data-stu-id="04959-118">**Reserved1**</span></span>
</dt> <dd>

<span data-ttu-id="04959-119">Réservé pour un usage futur.</span><span class="sxs-lookup"><span data-stu-id="04959-119">Reserved for future use.</span></span>

</dd> <dt>

<span data-ttu-id="04959-120">**Faisant**</span><span class="sxs-lookup"><span data-stu-id="04959-120">**Revision**</span></span>
</dt> <dd>

<span data-ttu-id="04959-121">Révision du microprogramme sur cet emplacement.</span><span class="sxs-lookup"><span data-stu-id="04959-121">The revision of the firmware on this slot.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="04959-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="04959-122">Requirements</span></span>



| <span data-ttu-id="04959-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="04959-123">Requirement</span></span> | <span data-ttu-id="04959-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="04959-124">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="04959-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="04959-125">Minimum supported client</span></span><br/> | <span data-ttu-id="04959-126">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="04959-126">Windows 10 \[desktop apps only\]</span></span><br/>                                                                 |
| <span data-ttu-id="04959-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="04959-127">Minimum supported server</span></span><br/> | <span data-ttu-id="04959-128">Applications de bureau Windows Server 2016 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="04959-128">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                                        |
| <span data-ttu-id="04959-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="04959-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="04959-130"><dt>Winioctl. h. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="04959-130"><dt>Winioctl.h.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="04959-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="04959-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04959-132">**\_ \_ activation du microprogramme de stockage IOCTL \_**</span><span class="sxs-lookup"><span data-stu-id="04959-132">**IOCTL\_STORAGE\_FIRMWARE\_ACTIVATE**</span></span>](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_firmware_activate)
</dt> <dt>

[<span data-ttu-id="04959-133">**\_ \_ activation du microprogramme matériel de stockage \_**</span><span class="sxs-lookup"><span data-stu-id="04959-133">**STORAGE\_HW\_FIRMWARE\_ACTIVATE**</span></span>](/windows/desktop/api/winioctl/ns-winioctl-storage_hw_firmware_activate)
</dt> <dt>

[<span data-ttu-id="04959-134">**\_ \_ Téléchargement du microprogramme de stockage IOCTL \_**</span><span class="sxs-lookup"><span data-stu-id="04959-134">**IOCTL\_STORAGE\_FIRMWARE\_DOWNLOAD**</span></span>](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_firmware_download)
</dt> <dt>

[<span data-ttu-id="04959-135">**\_ \_ Téléchargement du microprogramme matériel de stockage \_**</span><span class="sxs-lookup"><span data-stu-id="04959-135">**STORAGE\_HW\_FIRMWARE\_DOWNLOAD**</span></span>](/windows/desktop/api/winioctl/ns-winioctl-storage_hw_firmware_download)
</dt> <dt>

[<span data-ttu-id="04959-136">**\_informations de \_ récupération du microprogramme de stockage IOCTL \_ \_**</span><span class="sxs-lookup"><span data-stu-id="04959-136">**IOCTL\_STORAGE\_FIRMWARE\_GET\_INFO**</span></span>](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_firmware_get_info)
</dt> <dt>

[<span data-ttu-id="04959-137">**\_ \_ informations sur le microprogramme matériel de stockage \_**</span><span class="sxs-lookup"><span data-stu-id="04959-137">**STORAGE\_HW\_FIRMWARE\_INFO**</span></span>](storage-hw-firmware-info.md)
</dt> <dt>

[<span data-ttu-id="04959-138">**\_requête d' \_ \_ informations sur le microprogramme matériel de stockage \_**</span><span class="sxs-lookup"><span data-stu-id="04959-138">**STORAGE\_HW\_FIRMWARE\_INFO\_QUERY**</span></span>](storage-hw-firmware-info-query.md)
</dt> </dl>

 

 




