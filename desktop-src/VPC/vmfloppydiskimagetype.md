---
title: Énumération VMFloppyDiskImageType (VPCCOMInterfaces. h)
description: Spécifie les formats de disquette.
ms.assetid: 7eb504c0-dfb7-45eb-a943-b453b5f8ca63
keywords:
- Virtual PC de l’énumération VMFloppyDiskImageType
topic_type:
- apiref
api_name:
- VMFloppyDiskImageType
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f20732e46617288602e841a1047db5db30eba5ae
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384628"
---
# <a name="vmfloppydiskimagetype-enumeration"></a><span data-ttu-id="3a153-104">Énumération VMFloppyDiskImageType</span><span class="sxs-lookup"><span data-stu-id="3a153-104">VMFloppyDiskImageType enumeration</span></span>

<span data-ttu-id="3a153-105">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="3a153-105">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="3a153-106">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="3a153-106">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="3a153-107">Spécifie les formats de disquette.</span><span class="sxs-lookup"><span data-stu-id="3a153-107">Specifies the floppy disk formats.</span></span>

## <a name="syntax"></a><span data-ttu-id="3a153-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3a153-108">Syntax</span></span>


```C++
typedef enum  { 
  vmFloppyDiskImage_Unknown                = 0,
  vmFloppyDiskImage_LowDensity             = 1,
  vmFloppyDiskImage_HighDensity            = 2,
  vmFloppyDiskImage_DMF                    = 3,
  vmFloppyDiskImage_LowDensitySingleSided  = 4,
  vmFloppyDiskImage_MediumDensity          = 5,
  vmFloppyDiskImage_HighDensityMSS         = 6
} VMFloppyDiskImageType;
```



## <a name="constants"></a><span data-ttu-id="3a153-109">Constantes</span><span class="sxs-lookup"><span data-stu-id="3a153-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="3a153-110"><span id="vmFloppyDiskImage_Unknown"></span><span id="vmfloppydiskimage_unknown"></span><span id="VMFLOPPYDISKIMAGE_UNKNOWN"></span>**vmFloppyDiskImage \_ inconnu**</span><span class="sxs-lookup"><span data-stu-id="3a153-110"><span id="vmFloppyDiskImage_Unknown"></span><span id="vmfloppydiskimage_unknown"></span><span id="VMFLOPPYDISKIMAGE_UNKNOWN"></span>**vmFloppyDiskImage\_Unknown**</span></span>
</dt> <dd>

<span data-ttu-id="3a153-111">Format inconnu.</span><span class="sxs-lookup"><span data-stu-id="3a153-111">Unknown format.</span></span>

</dd> <dt>

<span data-ttu-id="3a153-112"><span id="vmFloppyDiskImage_LowDensity"></span><span id="vmfloppydiskimage_lowdensity"></span><span id="VMFLOPPYDISKIMAGE_LOWDENSITY"></span>**vmFloppyDiskImage \_ LowDensity**</span><span class="sxs-lookup"><span data-stu-id="3a153-112"><span id="vmFloppyDiskImage_LowDensity"></span><span id="vmfloppydiskimage_lowdensity"></span><span id="VMFLOPPYDISKIMAGE_LOWDENSITY"></span>**vmFloppyDiskImage\_LowDensity**</span></span>
</dt> <dd>

<span data-ttu-id="3a153-113">Format à faible densité (720K).</span><span class="sxs-lookup"><span data-stu-id="3a153-113">A low density format (720K).</span></span>

</dd> <dt>

<span data-ttu-id="3a153-114"><span id="vmFloppyDiskImage_HighDensity"></span><span id="vmfloppydiskimage_highdensity"></span><span id="VMFLOPPYDISKIMAGE_HIGHDENSITY"></span>**vmFloppyDiskImage \_ HighDensity**</span><span class="sxs-lookup"><span data-stu-id="3a153-114"><span id="vmFloppyDiskImage_HighDensity"></span><span id="vmfloppydiskimage_highdensity"></span><span id="VMFLOPPYDISKIMAGE_HIGHDENSITY"></span>**vmFloppyDiskImage\_HighDensity**</span></span>
</dt> <dd>

<span data-ttu-id="3a153-115">Un format à haute densité (1,44 Mo).</span><span class="sxs-lookup"><span data-stu-id="3a153-115">A high density format (1.44MB).</span></span>

</dd> <dt>

<span data-ttu-id="3a153-116"><span id="vmFloppyDiskImage_DMF"></span><span id="vmfloppydiskimage_dmf"></span><span id="VMFLOPPYDISKIMAGE_DMF"></span>**\_DMF vmFloppyDiskImage**</span><span class="sxs-lookup"><span data-stu-id="3a153-116"><span id="vmFloppyDiskImage_DMF"></span><span id="vmfloppydiskimage_dmf"></span><span id="VMFLOPPYDISKIMAGE_DMF"></span>**vmFloppyDiskImage\_DMF**</span></span>
</dt> <dd>

<span data-ttu-id="3a153-117">Un format de média de distribution (1.68 Mo).</span><span class="sxs-lookup"><span data-stu-id="3a153-117">A distribution media format (1.68Mb).</span></span>

</dd> <dt>

<span data-ttu-id="3a153-118"><span id="vmFloppyDiskImage_LowDensitySingleSided"></span><span id="vmfloppydiskimage_lowdensitysinglesided"></span><span id="VMFLOPPYDISKIMAGE_LOWDENSITYSINGLESIDED"></span>**vmFloppyDiskImage \_ LowDensitySingleSided**</span><span class="sxs-lookup"><span data-stu-id="3a153-118"><span id="vmFloppyDiskImage_LowDensitySingleSided"></span><span id="vmfloppydiskimage_lowdensitysinglesided"></span><span id="VMFLOPPYDISKIMAGE_LOWDENSITYSINGLESIDED"></span>**vmFloppyDiskImage\_LowDensitySingleSided**</span></span>
</dt> <dd>

<span data-ttu-id="3a153-119">Format à faible densité à un seul côté.</span><span class="sxs-lookup"><span data-stu-id="3a153-119">A single-sided low density format.</span></span>

</dd> <dt>

<span data-ttu-id="3a153-120"><span id="vmFloppyDiskImage_MediumDensity"></span><span id="vmfloppydiskimage_mediumdensity"></span><span id="VMFLOPPYDISKIMAGE_MEDIUMDENSITY"></span>**vmFloppyDiskImage \_ MediumDensity**</span><span class="sxs-lookup"><span data-stu-id="3a153-120"><span id="vmFloppyDiskImage_MediumDensity"></span><span id="vmfloppydiskimage_mediumdensity"></span><span id="VMFLOPPYDISKIMAGE_MEDIUMDENSITY"></span>**vmFloppyDiskImage\_MediumDensity**</span></span>
</dt> <dd>

<span data-ttu-id="3a153-121">Un format de densité moyenne (1,2 Mo).</span><span class="sxs-lookup"><span data-stu-id="3a153-121">A medium density format (1.2MB).</span></span>

</dd> <dt>

<span data-ttu-id="3a153-122"><span id="vmFloppyDiskImage_HighDensityMSS"></span><span id="vmfloppydiskimage_highdensitymss"></span><span id="VMFLOPPYDISKIMAGE_HIGHDENSITYMSS"></span>**vmFloppyDiskImage \_ HighDensityMSS**</span><span class="sxs-lookup"><span data-stu-id="3a153-122"><span id="vmFloppyDiskImage_HighDensityMSS"></span><span id="vmfloppydiskimage_highdensitymss"></span><span id="VMFLOPPYDISKIMAGE_HIGHDENSITYMSS"></span>**vmFloppyDiskImage\_HighDensityMSS**</span></span>
</dt> <dd>

<span data-ttu-id="3a153-123">Une taille de secteur multiple à haute densité (MSS), utilisée par le format de distribution étendue (XDF).</span><span class="sxs-lookup"><span data-stu-id="3a153-123">A high-density Multiple Sector Size (MSS), used by eXtended Distribution Format (XDF).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3a153-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3a153-124">Requirements</span></span>



| <span data-ttu-id="3a153-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3a153-125">Requirement</span></span> | <span data-ttu-id="3a153-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="3a153-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="3a153-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3a153-127">Minimum supported client</span></span><br/> | <span data-ttu-id="3a153-128">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3a153-128">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3a153-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3a153-129">Minimum supported server</span></span><br/> | <span data-ttu-id="3a153-130">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="3a153-130">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="3a153-131">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="3a153-131">End of client support</span></span><br/>    | <span data-ttu-id="3a153-132">Windows 7</span><span class="sxs-lookup"><span data-stu-id="3a153-132">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="3a153-133">Produit</span><span class="sxs-lookup"><span data-stu-id="3a153-133">Product</span></span><br/>                  | <span data-ttu-id="3a153-134">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="3a153-134">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="3a153-135">En-tête</span><span class="sxs-lookup"><span data-stu-id="3a153-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="3a153-136"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="3a153-136"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3a153-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3a153-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a153-138">**IVMVirtualPC::CreateFloppyDiskImage**</span><span class="sxs-lookup"><span data-stu-id="3a153-138">**IVMVirtualPC::CreateFloppyDiskImage**</span></span>](ivmvirtualpc-createfloppydiskimage.md)
</dt> <dt>

[<span data-ttu-id="3a153-139">**IVMVirtualPC::GetFloppyDiskImageType**</span><span class="sxs-lookup"><span data-stu-id="3a153-139">**IVMVirtualPC::GetFloppyDiskImageType**</span></span>](ivmvirtualpc-getfloppydiskimagetype.md)
</dt> </dl>

 

