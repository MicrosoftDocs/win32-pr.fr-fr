---
description: Cette structure contient des informations sur le microprogramme de l’appareil.
ms.assetid: 1A2D30F3-F2DE-40CB-BFFC-8BAD19793AE1
title: Structure STORAGE_HW_FIRMWARE_INFO_QUERY (winioctl. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- STORAGE_HW_FIRMWARE_INFO_QUERY
api_type:
- HeaderDef
api_location:
- winioctl.h.h
ms.openlocfilehash: c5c4294a733a57a6735691a134f997189736def0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517088"
---
# <a name="storage_hw_firmware_info_query-structure"></a><span data-ttu-id="8897e-103">\_Structure de \_ \_ requête informations sur le microprogramme matériel de stockage \_</span><span class="sxs-lookup"><span data-stu-id="8897e-103">STORAGE\_HW\_FIRMWARE\_INFO\_QUERY structure</span></span>

<span data-ttu-id="8897e-104">Cette structure contient des informations sur le microprogramme de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="8897e-104">This structure contains information about the device firmware.</span></span>

## <a name="syntax"></a><span data-ttu-id="8897e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8897e-105">Syntax</span></span>


```C++
typedef struct _STORAGE_HW_FIRMWARE_INFO_QUERY {
  DWORD Version;
  DWORD Size;
  DWORD Flags;
  DWORD Reserved;
} STORAGE_HW_FIRMWARE_INFO_QUERY, *PSTORAGE_HW_FIRMWARE_INFO_QUERY;
```



## <a name="members"></a><span data-ttu-id="8897e-106">Membres</span><span class="sxs-lookup"><span data-stu-id="8897e-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="8897e-107">**Version**</span><span class="sxs-lookup"><span data-stu-id="8897e-107">**Version**</span></span>
</dt> <dd>

<span data-ttu-id="8897e-108">Version de cette structure.</span><span class="sxs-lookup"><span data-stu-id="8897e-108">The version of this structure.</span></span> <span data-ttu-id="8897e-109">Elle doit être définie sur sizeof ( \_ \_ requête informations sur le microprogramme matériel de stockage \_ \_ )</span><span class="sxs-lookup"><span data-stu-id="8897e-109">This should be set to sizeof(STORAGE\_HW\_FIRMWARE\_INFO\_QUERY)</span></span>

</dd> <dt>

<span data-ttu-id="8897e-110">**Taille**</span><span class="sxs-lookup"><span data-stu-id="8897e-110">**Size**</span></span>
</dt> <dd>

<span data-ttu-id="8897e-111">Taille de cette structure sous la forme d’une mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="8897e-111">The size of this structure as a buffer.</span></span>

</dd> <dt>

<span data-ttu-id="8897e-112">**Indicateurs**</span><span class="sxs-lookup"><span data-stu-id="8897e-112">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="8897e-113">Indicateurs associés à la requête.</span><span class="sxs-lookup"><span data-stu-id="8897e-113">The flags associated with the query.</span></span> <span data-ttu-id="8897e-114">Les indicateurs suivants peuvent être définis dans ce membre.</span><span class="sxs-lookup"><span data-stu-id="8897e-114">The following are flags that can be set in this member.</span></span>



| <span data-ttu-id="8897e-115">Indicateur</span><span class="sxs-lookup"><span data-stu-id="8897e-115">Flag</span></span>                                             | <span data-ttu-id="8897e-116">Description</span><span class="sxs-lookup"><span data-stu-id="8897e-116">Description</span></span>                                                                        |
|--------------------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="8897e-117">contrôleur de l' \_ \_ indicateur de demande de microprogramme matériel \_ \_ de stockage \_</span><span class="sxs-lookup"><span data-stu-id="8897e-117">STORAGE\_HW\_FIRMWARE\_REQUEST\_FLAG\_CONTROLLER</span></span> | <span data-ttu-id="8897e-118">Indique que la cible de la requête autre que la main/l’objet de l’appareil lui-même.</span><span class="sxs-lookup"><span data-stu-id="8897e-118">Indicates that the target of the request other than the device hand/object itself.</span></span> |



 

</dd> <dt>

<span data-ttu-id="8897e-119">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="8897e-119">**Reserved**</span></span>
</dt> <dd>

<span data-ttu-id="8897e-120">Réservé pour un usage futur.</span><span class="sxs-lookup"><span data-stu-id="8897e-120">Reserved for future use.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8897e-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8897e-121">Requirements</span></span>



| <span data-ttu-id="8897e-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8897e-122">Requirement</span></span> | <span data-ttu-id="8897e-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="8897e-123">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8897e-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8897e-124">Minimum supported client</span></span><br/> | <span data-ttu-id="8897e-125">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8897e-125">Windows 10 \[desktop apps only\]</span></span><br/>                                                                 |
| <span data-ttu-id="8897e-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8897e-126">Minimum supported server</span></span><br/> | <span data-ttu-id="8897e-127">Applications de bureau Windows Server 2016 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8897e-127">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                                        |
| <span data-ttu-id="8897e-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="8897e-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="8897e-129"><dt>Winioctl. h. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8897e-129"><dt>Winioctl.h.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8897e-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8897e-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8897e-131">**\_ \_ activation du microprogramme de stockage IOCTL \_**</span><span class="sxs-lookup"><span data-stu-id="8897e-131">**IOCTL\_STORAGE\_FIRMWARE\_ACTIVATE**</span></span>](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_firmware_activate)
</dt> <dt>

[<span data-ttu-id="8897e-132">**\_ \_ activation du microprogramme matériel de stockage \_**</span><span class="sxs-lookup"><span data-stu-id="8897e-132">**STORAGE\_HW\_FIRMWARE\_ACTIVATE**</span></span>](/windows/desktop/api/winioctl/ns-winioctl-storage_hw_firmware_activate)
</dt> <dt>

[<span data-ttu-id="8897e-133">**\_ \_ Téléchargement du microprogramme de stockage IOCTL \_**</span><span class="sxs-lookup"><span data-stu-id="8897e-133">**IOCTL\_STORAGE\_FIRMWARE\_DOWNLOAD**</span></span>](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_firmware_download)
</dt> <dt>

[<span data-ttu-id="8897e-134">**\_ \_ Téléchargement du microprogramme matériel de stockage \_**</span><span class="sxs-lookup"><span data-stu-id="8897e-134">**STORAGE\_HW\_FIRMWARE\_DOWNLOAD**</span></span>](/windows/desktop/api/winioctl/ns-winioctl-storage_hw_firmware_download)
</dt> <dt>

[<span data-ttu-id="8897e-135">**\_informations de \_ récupération du microprogramme de stockage IOCTL \_ \_**</span><span class="sxs-lookup"><span data-stu-id="8897e-135">**IOCTL\_STORAGE\_FIRMWARE\_GET\_INFO**</span></span>](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_firmware_get_info)
</dt> <dt>

[<span data-ttu-id="8897e-136">**\_ \_ informations sur le microprogramme matériel de stockage \_**</span><span class="sxs-lookup"><span data-stu-id="8897e-136">**STORAGE\_HW\_FIRMWARE\_INFO**</span></span>](storage-hw-firmware-info.md)
</dt> <dt>

[<span data-ttu-id="8897e-137">**\_ \_ \_ informations sur l’emplacement du microprogramme matériel de stockage \_**</span><span class="sxs-lookup"><span data-stu-id="8897e-137">**STORAGE\_HW\_FIRMWARE\_SLOT\_INFO**</span></span>](storage-hw-firmware-slot-info.md)
</dt> </dl>

 

 




