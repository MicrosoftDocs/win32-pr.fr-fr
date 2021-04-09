---
title: Énumération VMDriveType (VPCCOMInterfaces. h)
description: Spécifie le type de lecteur attaché à un emplacement de bus.
ms.assetid: 7d3acff2-e1e3-4622-a448-0996ee7436ae
keywords:
- Virtual PC de l’énumération VMDriveType
topic_type:
- apiref
api_name:
- VMDriveType
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e6001a4a68db51b64eea9bb44d1d4c75863d315
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741397"
---
# <a name="vmdrivetype-enumeration"></a><span data-ttu-id="79004-104">Énumération VMDriveType</span><span class="sxs-lookup"><span data-stu-id="79004-104">VMDriveType enumeration</span></span>

<span data-ttu-id="79004-105">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="79004-105">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="79004-106">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="79004-106">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="79004-107">Spécifie le type de lecteur attaché à un emplacement de bus.</span><span class="sxs-lookup"><span data-stu-id="79004-107">Specifies the type of drive attached to a bus location.</span></span>

## <a name="syntax"></a><span data-ttu-id="79004-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="79004-108">Syntax</span></span>


```C++
typedef enum  { 
  vmDriveType_Null      = 0,
  vmDriveType_HardDisk  = 1,
  vmDriveType_DVD       = 2
} VMDriveType;
```



## <a name="constants"></a><span data-ttu-id="79004-109">Constantes</span><span class="sxs-lookup"><span data-stu-id="79004-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="79004-110"><span id="vmDriveType_Null"></span><span id="vmdrivetype_null"></span><span id="VMDRIVETYPE_NULL"></span>**vmDriveType \_ null**</span><span class="sxs-lookup"><span data-stu-id="79004-110"><span id="vmDriveType_Null"></span><span id="vmdrivetype_null"></span><span id="VMDRIVETYPE_NULL"></span>**vmDriveType\_Null**</span></span>
</dt> <dd>

<span data-ttu-id="79004-111">Aucun lecteur n’est attaché.</span><span class="sxs-lookup"><span data-stu-id="79004-111">There is no drive attached.</span></span>

</dd> <dt>

<span data-ttu-id="79004-112"><span id="vmDriveType_HardDisk"></span><span id="vmdrivetype_harddisk"></span><span id="VMDRIVETYPE_HARDDISK"></span>**vmDriveType \_**</span><span class="sxs-lookup"><span data-stu-id="79004-112"><span id="vmDriveType_HardDisk"></span><span id="vmdrivetype_harddisk"></span><span id="VMDRIVETYPE_HARDDISK"></span>**vmDriveType\_HardDisk**</span></span>
</dt> <dd>

<span data-ttu-id="79004-113">Un disque dur est attaché.</span><span class="sxs-lookup"><span data-stu-id="79004-113">There is a hard disk attached.</span></span>

</dd> <dt>

<span data-ttu-id="79004-114"><span id="vmDriveType_DVD"></span><span id="vmdrivetype_dvd"></span><span id="VMDRIVETYPE_DVD"></span>**\_DVD vmDriveType**</span><span class="sxs-lookup"><span data-stu-id="79004-114"><span id="vmDriveType_DVD"></span><span id="vmdrivetype_dvd"></span><span id="VMDRIVETYPE_DVD"></span>**vmDriveType\_DVD**</span></span>
</dt> <dd>

<span data-ttu-id="79004-115">Un lecteur de CD ou DVD est attaché.</span><span class="sxs-lookup"><span data-stu-id="79004-115">There is a CD or DVD drive attached.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="79004-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="79004-116">Requirements</span></span>



| <span data-ttu-id="79004-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="79004-117">Requirement</span></span> | <span data-ttu-id="79004-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="79004-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="79004-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="79004-119">Minimum supported client</span></span><br/> | <span data-ttu-id="79004-120">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="79004-120">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="79004-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="79004-121">Minimum supported server</span></span><br/> | <span data-ttu-id="79004-122">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="79004-122">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="79004-123">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="79004-123">End of client support</span></span><br/>    | <span data-ttu-id="79004-124">Windows 7</span><span class="sxs-lookup"><span data-stu-id="79004-124">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="79004-125">Produit</span><span class="sxs-lookup"><span data-stu-id="79004-125">Product</span></span><br/>                  | <span data-ttu-id="79004-126">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="79004-126">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="79004-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="79004-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="79004-128"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="79004-128"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="79004-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="79004-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79004-130">**IVMVirtualMachine::AttachedDriveTypes**</span><span class="sxs-lookup"><span data-stu-id="79004-130">**IVMVirtualMachine::AttachedDriveTypes**</span></span>](ivmvirtualmachine-attacheddrivetypes.md)
</dt> </dl>

 

