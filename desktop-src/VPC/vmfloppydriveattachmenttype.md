---
title: Énumération VMFloppyDriveAttachmentType (VPCCOMInterfaces. h)
description: Spécifie ce qui est attaché à un lecteur de disquette.
ms.assetid: aba1be92-bd07-4edb-ad62-f8d76dbd19b9
keywords:
- Virtual PC de l’énumération VMFloppyDriveAttachmentType
topic_type:
- apiref
api_name:
- VMFloppyDriveAttachmentType
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a4a291778b2fea8039bf41fc04799a03421342f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942318"
---
# <a name="vmfloppydriveattachmenttype-enumeration"></a><span data-ttu-id="a912f-104">Énumération VMFloppyDriveAttachmentType</span><span class="sxs-lookup"><span data-stu-id="a912f-104">VMFloppyDriveAttachmentType enumeration</span></span>

<span data-ttu-id="a912f-105">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="a912f-105">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="a912f-106">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="a912f-106">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="a912f-107">Spécifie ce qui est attaché à un lecteur de disquette.</span><span class="sxs-lookup"><span data-stu-id="a912f-107">Specifies what is attached to a floppy drive.</span></span>

## <a name="syntax"></a><span data-ttu-id="a912f-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a912f-108">Syntax</span></span>


```C++
typedef enum  { 
  vmFloppyDrive_None       = 0,
  vmFloppyDrive_Image      = 1,
  vmFloppyDrive_HostDrive  = 2
} VMFloppyDriveAttachmentType;
```



## <a name="constants"></a><span data-ttu-id="a912f-109">Constantes</span><span class="sxs-lookup"><span data-stu-id="a912f-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="a912f-110"><span id="vmFloppyDrive_None"></span><span id="vmfloppydrive_none"></span><span id="VMFLOPPYDRIVE_NONE"></span>**vmFloppyDrive \_ aucun**</span><span class="sxs-lookup"><span data-stu-id="a912f-110"><span id="vmFloppyDrive_None"></span><span id="vmfloppydrive_none"></span><span id="VMFLOPPYDRIVE_NONE"></span>**vmFloppyDrive\_None**</span></span>
</dt> <dd>

<span data-ttu-id="a912f-111">Aucun élément n’est attaché.</span><span class="sxs-lookup"><span data-stu-id="a912f-111">There is nothing attached.</span></span>

</dd> <dt>

<span data-ttu-id="a912f-112"><span id="vmFloppyDrive_Image"></span><span id="vmfloppydrive_image"></span><span id="VMFLOPPYDRIVE_IMAGE"></span>**\_image vmFloppyDrive**</span><span class="sxs-lookup"><span data-stu-id="a912f-112"><span id="vmFloppyDrive_Image"></span><span id="vmfloppydrive_image"></span><span id="VMFLOPPYDRIVE_IMAGE"></span>**vmFloppyDrive\_Image**</span></span>
</dt> <dd>

<span data-ttu-id="a912f-113">Un fichier image de disquette est attaché.</span><span class="sxs-lookup"><span data-stu-id="a912f-113">There is a floppy disk image file attached.</span></span>

</dd> <dt>

<span data-ttu-id="a912f-114"><span id="vmFloppyDrive_HostDrive"></span><span id="vmfloppydrive_hostdrive"></span><span id="VMFLOPPYDRIVE_HOSTDRIVE"></span>**vmFloppyDrive \_ HostDrive**</span><span class="sxs-lookup"><span data-stu-id="a912f-114"><span id="vmFloppyDrive_HostDrive"></span><span id="vmfloppydrive_hostdrive"></span><span id="VMFLOPPYDRIVE_HOSTDRIVE"></span>**vmFloppyDrive\_HostDrive**</span></span>
</dt> <dd>

<span data-ttu-id="a912f-115">Un lecteur de disquette hôte est attaché.</span><span class="sxs-lookup"><span data-stu-id="a912f-115">There is a host floppy drive attached.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a912f-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a912f-116">Requirements</span></span>



| <span data-ttu-id="a912f-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a912f-117">Requirement</span></span> | <span data-ttu-id="a912f-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="a912f-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="a912f-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a912f-119">Minimum supported client</span></span><br/> | <span data-ttu-id="a912f-120">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a912f-120">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a912f-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a912f-121">Minimum supported server</span></span><br/> | <span data-ttu-id="a912f-122">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="a912f-122">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="a912f-123">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="a912f-123">End of client support</span></span><br/>    | <span data-ttu-id="a912f-124">Windows 7</span><span class="sxs-lookup"><span data-stu-id="a912f-124">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="a912f-125">Produit</span><span class="sxs-lookup"><span data-stu-id="a912f-125">Product</span></span><br/>                  | <span data-ttu-id="a912f-126">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="a912f-126">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="a912f-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="a912f-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="a912f-128"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="a912f-128"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a912f-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a912f-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a912f-130">**IVMFloppyDrive :: Attachment**</span><span class="sxs-lookup"><span data-stu-id="a912f-130">**IVMFloppyDrive::Attachment**</span></span>](ivmfloppydrive-attachment.md)
</dt> </dl>

 

