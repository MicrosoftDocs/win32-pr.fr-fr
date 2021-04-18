---
title: Énumération VMHardDiskType (VPCCOMInterfaces. h)
description: Spécifie le type d’image de disque dur.
ms.assetid: 14480bad-523a-40d8-a6ba-9ec31fe4b217
keywords:
- Virtual PC de l’énumération VMHardDiskType
topic_type:
- apiref
api_name:
- VMHardDiskType
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b59fed6577aa957bae960f7af65be766a03c727e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106540778"
---
# <a name="vmharddisktype-enumeration"></a><span data-ttu-id="852b3-104">Énumération VMHardDiskType</span><span class="sxs-lookup"><span data-stu-id="852b3-104">VMHardDiskType enumeration</span></span>

<span data-ttu-id="852b3-105">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="852b3-105">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="852b3-106">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="852b3-106">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="852b3-107">Spécifie le type d’image de disque dur.</span><span class="sxs-lookup"><span data-stu-id="852b3-107">Specifies the hard disk image type.</span></span>

## <a name="syntax"></a><span data-ttu-id="852b3-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="852b3-108">Syntax</span></span>


```C++
typedef enum  { 
  vmDiskType_Dynamic       = 0,
  vmDiskType_FixedSize     = 1,
  vmDiskType_Differencing  = 2
} VMHardDiskType;
```



## <a name="constants"></a><span data-ttu-id="852b3-109">Constantes</span><span class="sxs-lookup"><span data-stu-id="852b3-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="852b3-110"><span id="vmDiskType_Dynamic"></span><span id="vmdisktype_dynamic"></span><span id="VMDISKTYPE_DYNAMIC"></span>**vmDiskType \_ dynamique**</span><span class="sxs-lookup"><span data-stu-id="852b3-110"><span id="vmDiskType_Dynamic"></span><span id="vmdisktype_dynamic"></span><span id="VMDISKTYPE_DYNAMIC"></span>**vmDiskType\_Dynamic**</span></span>
</dt> <dd>

<span data-ttu-id="852b3-111">Image de disque dur de taille dynamique.</span><span class="sxs-lookup"><span data-stu-id="852b3-111">A dynamically expanding hard disk image.</span></span>

</dd> <dt>

<span data-ttu-id="852b3-112"><span id="vmDiskType_FixedSize"></span><span id="vmdisktype_fixedsize"></span><span id="VMDISKTYPE_FIXEDSIZE"></span>**vmDiskType \_ FixedSize**</span><span class="sxs-lookup"><span data-stu-id="852b3-112"><span id="vmDiskType_FixedSize"></span><span id="vmdisktype_fixedsize"></span><span id="VMDISKTYPE_FIXEDSIZE"></span>**vmDiskType\_FixedSize**</span></span>
</dt> <dd>

<span data-ttu-id="852b3-113">Image de disque dur de taille fixe.</span><span class="sxs-lookup"><span data-stu-id="852b3-113">A fixed-size hard disk image.</span></span>

</dd> <dt>

<span data-ttu-id="852b3-114"><span id="vmDiskType_Differencing"></span><span id="vmdisktype_differencing"></span><span id="VMDISKTYPE_DIFFERENCING"></span>**\_différenciation vmDiskType**</span><span class="sxs-lookup"><span data-stu-id="852b3-114"><span id="vmDiskType_Differencing"></span><span id="vmdisktype_differencing"></span><span id="VMDISKTYPE_DIFFERENCING"></span>**vmDiskType\_Differencing**</span></span>
</dt> <dd>

<span data-ttu-id="852b3-115">Image de disque dur de différenciation.</span><span class="sxs-lookup"><span data-stu-id="852b3-115">A differencing hard disk image.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="852b3-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="852b3-116">Requirements</span></span>



| <span data-ttu-id="852b3-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="852b3-117">Requirement</span></span> | <span data-ttu-id="852b3-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="852b3-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="852b3-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="852b3-119">Minimum supported client</span></span><br/> | <span data-ttu-id="852b3-120">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="852b3-120">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="852b3-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="852b3-121">Minimum supported server</span></span><br/> | <span data-ttu-id="852b3-122">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="852b3-122">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="852b3-123">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="852b3-123">End of client support</span></span><br/>    | <span data-ttu-id="852b3-124">Windows 7</span><span class="sxs-lookup"><span data-stu-id="852b3-124">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="852b3-125">Produit</span><span class="sxs-lookup"><span data-stu-id="852b3-125">Product</span></span><br/>                  | <span data-ttu-id="852b3-126">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="852b3-126">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="852b3-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="852b3-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="852b3-128"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="852b3-128"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="852b3-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="852b3-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="852b3-130">**IVMHardDisk**</span><span class="sxs-lookup"><span data-stu-id="852b3-130">**IVMHardDisk**</span></span>](ivmharddisk.md)
</dt> </dl>

 

