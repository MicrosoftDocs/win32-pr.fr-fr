---
title: Énumération VMDVDDriveAttachmentType (VPCCOMInterfaces. h)
description: Spécifie ce qui est attaché à un lecteur de DVD.
ms.assetid: 66f33974-8622-4fa3-b5ac-3fae5a637434
keywords:
- Virtual PC de l’énumération VMDVDDriveAttachmentType
topic_type:
- apiref
api_name:
- VMDVDDriveAttachmentType
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f63c5918fd414a5a83a114ebddf5752647e8db83
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465759"
---
# <a name="vmdvddriveattachmenttype-enumeration"></a><span data-ttu-id="1ae4a-104">Énumération VMDVDDriveAttachmentType</span><span class="sxs-lookup"><span data-stu-id="1ae4a-104">VMDVDDriveAttachmentType enumeration</span></span>

<span data-ttu-id="1ae4a-105">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="1ae4a-105">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="1ae4a-106">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="1ae4a-106">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="1ae4a-107">Spécifie ce qui est attaché à un lecteur de DVD.</span><span class="sxs-lookup"><span data-stu-id="1ae4a-107">Specifies what is attached to a DVD drive.</span></span>

## <a name="syntax"></a><span data-ttu-id="1ae4a-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1ae4a-108">Syntax</span></span>


```C++
typedef enum  { 
  vmDVDDrive_None       = 0,
  vmDVDDrive_Image      = 1,
  vmDVDDrive_HostDrive  = 2
} VMDVDDriveAttachmentType;
```



## <a name="constants"></a><span data-ttu-id="1ae4a-109">Constantes</span><span class="sxs-lookup"><span data-stu-id="1ae4a-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="1ae4a-110"><span id="vmDVDDrive_None"></span><span id="vmdvddrive_none"></span><span id="VMDVDDRIVE_NONE"></span>**vmDVDDrive \_ aucun**</span><span class="sxs-lookup"><span data-stu-id="1ae4a-110"><span id="vmDVDDrive_None"></span><span id="vmdvddrive_none"></span><span id="VMDVDDRIVE_NONE"></span>**vmDVDDrive\_None**</span></span>
</dt> <dd>

<span data-ttu-id="1ae4a-111">Aucun élément n’est attaché.</span><span class="sxs-lookup"><span data-stu-id="1ae4a-111">There is nothing attached.</span></span>

</dd> <dt>

<span data-ttu-id="1ae4a-112"><span id="vmDVDDrive_Image"></span><span id="vmdvddrive_image"></span><span id="VMDVDDRIVE_IMAGE"></span>**\_image vmDVDDrive**</span><span class="sxs-lookup"><span data-stu-id="1ae4a-112"><span id="vmDVDDrive_Image"></span><span id="vmdvddrive_image"></span><span id="VMDVDDRIVE_IMAGE"></span>**vmDVDDrive\_Image**</span></span>
</dt> <dd>

<span data-ttu-id="1ae4a-113">Un fichier image ISO est attaché.</span><span class="sxs-lookup"><span data-stu-id="1ae4a-113">There is an ISO image file attached.</span></span>

</dd> <dt>

<span data-ttu-id="1ae4a-114"><span id="vmDVDDrive_HostDrive"></span><span id="vmdvddrive_hostdrive"></span><span id="VMDVDDRIVE_HOSTDRIVE"></span>**vmDVDDrive \_ HostDrive**</span><span class="sxs-lookup"><span data-stu-id="1ae4a-114"><span id="vmDVDDrive_HostDrive"></span><span id="vmdvddrive_hostdrive"></span><span id="VMDVDDRIVE_HOSTDRIVE"></span>**vmDVDDrive\_HostDrive**</span></span>
</dt> <dd>

<span data-ttu-id="1ae4a-115">Un lecteur de CD ou de DVD hôte est attaché.</span><span class="sxs-lookup"><span data-stu-id="1ae4a-115">There is a host CD or DVD drive attached.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1ae4a-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1ae4a-116">Requirements</span></span>



| <span data-ttu-id="1ae4a-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1ae4a-117">Requirement</span></span> | <span data-ttu-id="1ae4a-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="1ae4a-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="1ae4a-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1ae4a-119">Minimum supported client</span></span><br/> | <span data-ttu-id="1ae4a-120">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1ae4a-120">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="1ae4a-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1ae4a-121">Minimum supported server</span></span><br/> | <span data-ttu-id="1ae4a-122">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="1ae4a-122">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="1ae4a-123">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="1ae4a-123">End of client support</span></span><br/>    | <span data-ttu-id="1ae4a-124">Windows 7</span><span class="sxs-lookup"><span data-stu-id="1ae4a-124">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="1ae4a-125">Produit</span><span class="sxs-lookup"><span data-stu-id="1ae4a-125">Product</span></span><br/>                  | <span data-ttu-id="1ae4a-126">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="1ae4a-126">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="1ae4a-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="1ae4a-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="1ae4a-128"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="1ae4a-128"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1ae4a-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1ae4a-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ae4a-130">**IVMDVDDrive :: Attachment**</span><span class="sxs-lookup"><span data-stu-id="1ae4a-130">**IVMDVDDrive::Attachment**</span></span>](ivmdvddrive-attachment.md)
</dt> </dl>

 

