---
description: 'Structure de STORAGE_HW_FIRMWARE_INFO : cette structure contient des informations sur le microprogramme de l’appareil.'
ms.assetid: 7BDACD50-0FD1-4F00-BAE5-884D8C1485BC
title: Structure STORAGE_HW_FIRMWARE_INFO (winioctl. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- STORAGE_HW_FIRMWARE_INFO
api_type:
- HeaderDef
api_location:
- winioctl.h.h
ms.openlocfilehash: e7aa3d33f744b00fc742a2862add83149cb265b4
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090957"
---
# <a name="storage_hw_firmware_info-structure"></a><span data-ttu-id="2cf53-103">\_Structure d' \_ \_ informations sur le microprogramme matériel de stockage</span><span class="sxs-lookup"><span data-stu-id="2cf53-103">STORAGE\_HW\_FIRMWARE\_INFO structure</span></span>

<span data-ttu-id="2cf53-104">Cette structure contient des informations sur le microprogramme de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="2cf53-104">This structure contains information about the device firmware.</span></span>

## <a name="syntax"></a><span data-ttu-id="2cf53-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2cf53-105">Syntax</span></span>


```C++
typedef struct _STORAGE_HW_FIRMWARE_INFO {
  DWORD                         Version;
  DWORD                         Size;
  BYTE                          SupportUpgrade  :1;
  BYTE                          Reserved0  :7;
  BYTE                          SlotCount;
  BYTE                          ActiveSlot;
  BYTE                          PendingActivateSlot;
  BOOLEAN                       FirmwareShared;
  BYTE                          Reserved[3];
  DWORD                         ImagePayloadAlignment;
  DWORD                         ImagePayloadMaxSize;
  STORAGE_HW_FIRMWARE_SLOT_INFO Slot[ANYSIZE_ARRAY];
} STORAGE_HW_FIRMWARE_INFO, *PSTORAGE_HW_FIRMWARE_INFO;
```



## <a name="members"></a><span data-ttu-id="2cf53-106">Membres</span><span class="sxs-lookup"><span data-stu-id="2cf53-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="2cf53-107">**Version**</span><span class="sxs-lookup"><span data-stu-id="2cf53-107">**Version**</span></span>
</dt> <dd>

<span data-ttu-id="2cf53-108">Version de cette structure.</span><span class="sxs-lookup"><span data-stu-id="2cf53-108">The version of this structure.</span></span> <span data-ttu-id="2cf53-109">Elle doit être définie sur sizeof ( \_ \_ informations sur le microprogramme matériel de stockage \_ )</span><span class="sxs-lookup"><span data-stu-id="2cf53-109">This should be set to sizeof(STORAGE\_HW\_FIRMWARE\_INFO)</span></span>

</dd> <dt>

<span data-ttu-id="2cf53-110">**Taille**</span><span class="sxs-lookup"><span data-stu-id="2cf53-110">**Size**</span></span>
</dt> <dd>

<span data-ttu-id="2cf53-111">Taille de cette structure sous la forme d’une mémoire tampon incluant l’emplacement.</span><span class="sxs-lookup"><span data-stu-id="2cf53-111">The size of this structure as a buffer including slot.</span></span>

</dd> <dt>

<span data-ttu-id="2cf53-112">**SupportUpgrade**</span><span class="sxs-lookup"><span data-stu-id="2cf53-112">**SupportUpgrade**</span></span>
</dt> <dd>

<span data-ttu-id="2cf53-113">Indique que ce microprogramme prend en charge une mise à niveau.</span><span class="sxs-lookup"><span data-stu-id="2cf53-113">Indicates that this firmware supports an upgrade.</span></span>

</dd> <dt>

<span data-ttu-id="2cf53-114">**Reserved0**</span><span class="sxs-lookup"><span data-stu-id="2cf53-114">**Reserved0**</span></span>
</dt> <dd>

<span data-ttu-id="2cf53-115">Réservé pour un usage futur.</span><span class="sxs-lookup"><span data-stu-id="2cf53-115">Reserved for future use.</span></span>

</dd> <dt>

<span data-ttu-id="2cf53-116">**SlotCount**</span><span class="sxs-lookup"><span data-stu-id="2cf53-116">**SlotCount**</span></span>
</dt> <dd>

<span data-ttu-id="2cf53-117">Nombre d’emplacements de microprogramme sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="2cf53-117">The number of firmware slots on the device.</span></span> <span data-ttu-id="2cf53-118">Il s’agit de la dimension du tableau d’emplacements.</span><span class="sxs-lookup"><span data-stu-id="2cf53-118">This is the dimension of the Slot array.</span></span>

> [!Note]  
> <span data-ttu-id="2cf53-119">Certains appareils peuvent stocker plus d’une image de microprogramme, s’ils possèdent plus d’un emplacement de microprogramme.</span><span class="sxs-lookup"><span data-stu-id="2cf53-119">Some devices can store more than 1 firmware image, if they have more than 1 firmware slot.</span></span>

 

</dd> <dt>

<span data-ttu-id="2cf53-120">**ActiveSlot**</span><span class="sxs-lookup"><span data-stu-id="2cf53-120">**ActiveSlot**</span></span>
</dt> <dd>

<span data-ttu-id="2cf53-121">Emplacement du microprogramme contenant l’image de microprogramme actuellement active/en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="2cf53-121">The firmware slot containing the currently active/running firmware image.</span></span>

</dd> <dt>

<span data-ttu-id="2cf53-122">**PendingActivateSlot**</span><span class="sxs-lookup"><span data-stu-id="2cf53-122">**PendingActivateSlot**</span></span>
</dt> <dd>

<span data-ttu-id="2cf53-123">Emplacement du microprogramme en attente d’activation.</span><span class="sxs-lookup"><span data-stu-id="2cf53-123">The firmware slot that is pending activation.</span></span>

</dd> <dt>

<span data-ttu-id="2cf53-124">**FirmwareShared**</span><span class="sxs-lookup"><span data-stu-id="2cf53-124">**FirmwareShared**</span></span>
</dt> <dd>

<span data-ttu-id="2cf53-125">Indique que le microprogramme s’applique à la fois à l’appareil et au contrôleur/adaptateur, par exemple, SSD NVMe.</span><span class="sxs-lookup"><span data-stu-id="2cf53-125">Indicates that the firmware applies to both the device and controller/adapter, e.g. NVMe SSD.</span></span>

</dd> <dt>

<span data-ttu-id="2cf53-126">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="2cf53-126">**Reserved**</span></span>
</dt> <dd>

<span data-ttu-id="2cf53-127">Réservé pour un usage futur.</span><span class="sxs-lookup"><span data-stu-id="2cf53-127">Reserved for future use.</span></span>

</dd> <dt>

<span data-ttu-id="2cf53-128">**ImagePayloadAlignment**</span><span class="sxs-lookup"><span data-stu-id="2cf53-128">**ImagePayloadAlignment**</span></span>
</dt> <dd>

<span data-ttu-id="2cf53-129">Alignement de la charge utile de l’image, en nombre d’octets.</span><span class="sxs-lookup"><span data-stu-id="2cf53-129">The alignment of the image payload, in number of bytes.</span></span> <span data-ttu-id="2cf53-130">La taille de PAGE maximale est \_ .</span><span class="sxs-lookup"><span data-stu-id="2cf53-130">The maximum is PAGE\_SIZE.</span></span> <span data-ttu-id="2cf53-131">La taille de transfert est un multiple de cette taille.</span><span class="sxs-lookup"><span data-stu-id="2cf53-131">The transfer size is a mutliple of this size.</span></span> <span data-ttu-id="2cf53-132">Certains protocoles nécessitent au moins la taille du secteur.</span><span class="sxs-lookup"><span data-stu-id="2cf53-132">Some protocols require at least sector size.</span></span> <span data-ttu-id="2cf53-133">Lorsque cette valeur est définie sur 0, cela signifie que cette valeur n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="2cf53-133">When this value is set to 0, this means that this value is invalid.</span></span>

</dd> <dt>

<span data-ttu-id="2cf53-134">**ImagePayloadMaxSize**</span><span class="sxs-lookup"><span data-stu-id="2cf53-134">**ImagePayloadMaxSize**</span></span>
</dt> <dd>

<span data-ttu-id="2cf53-135">La taille maximale de la charge utile d’image est utilisée pour une seule commande.</span><span class="sxs-lookup"><span data-stu-id="2cf53-135">The image payload maximum size, this is used for a single command.</span></span>

</dd> <dt>

<span data-ttu-id="2cf53-136">**Emplacement**</span><span class="sxs-lookup"><span data-stu-id="2cf53-136">**Slot**</span></span>
</dt> <dd>

<span data-ttu-id="2cf53-137">Contient les informations relatives à l’emplacement de chaque emplacement sur l’appareil, de type informations sur l' [**\_ \_ \_ emplacement \_ du microprogramme de stockage matériel**](storage-hw-firmware-slot-info.md).</span><span class="sxs-lookup"><span data-stu-id="2cf53-137">Contains the slot information for each slot on the device, of type [**STORAGE\_HW\_FIRMWARE\_SLOT\_INFO**](storage-hw-firmware-slot-info.md).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2cf53-138">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2cf53-138">Requirements</span></span>



| <span data-ttu-id="2cf53-139">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2cf53-139">Requirement</span></span> | <span data-ttu-id="2cf53-140">Valeur</span><span class="sxs-lookup"><span data-stu-id="2cf53-140">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2cf53-141">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2cf53-141">Minimum supported client</span></span><br/> | <span data-ttu-id="2cf53-142">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2cf53-142">Windows 10 \[desktop apps only\]</span></span><br/>                                                                 |
| <span data-ttu-id="2cf53-143">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2cf53-143">Minimum supported server</span></span><br/> | <span data-ttu-id="2cf53-144">Applications de bureau Windows Server 2016 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2cf53-144">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                                        |
| <span data-ttu-id="2cf53-145">En-tête</span><span class="sxs-lookup"><span data-stu-id="2cf53-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="2cf53-146"><dt>Winioctl. h. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2cf53-146"><dt>Winioctl.h.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2cf53-147">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2cf53-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2cf53-148">**\_ \_ activation du microprogramme de stockage IOCTL \_**</span><span class="sxs-lookup"><span data-stu-id="2cf53-148">**IOCTL\_STORAGE\_FIRMWARE\_ACTIVATE**</span></span>](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_firmware_activate)
</dt> <dt>

[<span data-ttu-id="2cf53-149">**\_ \_ activation du microprogramme matériel de stockage \_**</span><span class="sxs-lookup"><span data-stu-id="2cf53-149">**STORAGE\_HW\_FIRMWARE\_ACTIVATE**</span></span>](/windows/desktop/api/winioctl/ns-winioctl-storage_hw_firmware_activate)
</dt> <dt>

[<span data-ttu-id="2cf53-150">**\_ \_ Téléchargement du microprogramme de stockage IOCTL \_**</span><span class="sxs-lookup"><span data-stu-id="2cf53-150">**IOCTL\_STORAGE\_FIRMWARE\_DOWNLOAD**</span></span>](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_firmware_download)
</dt> <dt>

[<span data-ttu-id="2cf53-151">**\_ \_ Téléchargement du microprogramme matériel de stockage \_**</span><span class="sxs-lookup"><span data-stu-id="2cf53-151">**STORAGE\_HW\_FIRMWARE\_DOWNLOAD**</span></span>](/windows/desktop/api/winioctl/ns-winioctl-storage_hw_firmware_download)
</dt> <dt>

[<span data-ttu-id="2cf53-152">**\_informations de \_ récupération du microprogramme de stockage IOCTL \_ \_**</span><span class="sxs-lookup"><span data-stu-id="2cf53-152">**IOCTL\_STORAGE\_FIRMWARE\_GET\_INFO**</span></span>](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_firmware_get_info)
</dt> <dt>

[<span data-ttu-id="2cf53-153">**\_requête d' \_ \_ informations sur le microprogramme matériel de stockage \_**</span><span class="sxs-lookup"><span data-stu-id="2cf53-153">**STORAGE\_HW\_FIRMWARE\_INFO\_QUERY**</span></span>](storage-hw-firmware-info-query.md)
</dt> <dt>

[<span data-ttu-id="2cf53-154">**\_ \_ \_ informations sur l’emplacement du microprogramme matériel de stockage \_**</span><span class="sxs-lookup"><span data-stu-id="2cf53-154">**STORAGE\_HW\_FIRMWARE\_SLOT\_INFO**</span></span>](storage-hw-firmware-slot-info.md)
</dt> </dl>

 

 




