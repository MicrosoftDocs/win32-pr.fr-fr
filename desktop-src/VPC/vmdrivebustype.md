---
title: Énumération VMDriveBusType (VPCCOMInterfaces. h)
description: Spécifie le type de bus.
ms.assetid: 7e0926f3-8218-49c9-8d3a-27214c111a77
keywords:
- Virtual PC de l’énumération VMDriveBusType
topic_type:
- apiref
api_name:
- VMDriveBusType
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c53b8da4b9c7a6943f083eec62a144dcfb5bd68
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104266"
---
# <a name="vmdrivebustype-enumeration"></a><span data-ttu-id="f5ff4-104">Énumération VMDriveBusType</span><span class="sxs-lookup"><span data-stu-id="f5ff4-104">VMDriveBusType enumeration</span></span>

<span data-ttu-id="f5ff4-105">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="f5ff4-105">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="f5ff4-106">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="f5ff4-106">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="f5ff4-107">Spécifie le type de bus.</span><span class="sxs-lookup"><span data-stu-id="f5ff4-107">Specifies the type of bus.</span></span>

## <a name="syntax"></a><span data-ttu-id="f5ff4-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f5ff4-108">Syntax</span></span>


```C++
typedef enum  { 
  vmDriveBusType_Invalid  = -1,
  vmDriveBusType_IDE      = 0,
  vmDriveBusType_SCSI     = 1
} VMDriveBusType;
```



## <a name="constants"></a><span data-ttu-id="f5ff4-109">Constantes</span><span class="sxs-lookup"><span data-stu-id="f5ff4-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="f5ff4-110"><span id="vmDriveBusType_Invalid"></span><span id="vmdrivebustype_invalid"></span><span id="VMDRIVEBUSTYPE_INVALID"></span>**vmDriveBusType \_ non valide**</span><span class="sxs-lookup"><span data-stu-id="f5ff4-110"><span id="vmDriveBusType_Invalid"></span><span id="vmdrivebustype_invalid"></span><span id="VMDRIVEBUSTYPE_INVALID"></span>**vmDriveBusType\_Invalid**</span></span>
</dt> <dd>

<span data-ttu-id="f5ff4-111">Aucun type de bus.</span><span class="sxs-lookup"><span data-stu-id="f5ff4-111">No bus type.</span></span>

</dd> <dt>

<span data-ttu-id="f5ff4-112"><span id="vmDriveBusType_IDE"></span><span id="vmdrivebustype_ide"></span><span id="VMDRIVEBUSTYPE_IDE"></span>**\_IDE vmDriveBusType**</span><span class="sxs-lookup"><span data-stu-id="f5ff4-112"><span id="vmDriveBusType_IDE"></span><span id="vmdrivebustype_ide"></span><span id="VMDRIVEBUSTYPE_IDE"></span>**vmDriveBusType\_IDE**</span></span>
</dt> <dd>

<span data-ttu-id="f5ff4-113">Type de bus IDE.</span><span class="sxs-lookup"><span data-stu-id="f5ff4-113">IDE bus type.</span></span>

</dd> <dt>

<span data-ttu-id="f5ff4-114"><span id="vmDriveBusType_SCSI"></span><span id="vmdrivebustype_scsi"></span><span id="VMDRIVEBUSTYPE_SCSI"></span>**\_SCSI vmDriveBusType**</span><span class="sxs-lookup"><span data-stu-id="f5ff4-114"><span id="vmDriveBusType_SCSI"></span><span id="vmdrivebustype_scsi"></span><span id="VMDRIVEBUSTYPE_SCSI"></span>**vmDriveBusType\_SCSI**</span></span>
</dt> <dd>

<span data-ttu-id="f5ff4-115">Type de bus SCSI.</span><span class="sxs-lookup"><span data-stu-id="f5ff4-115">SCSI bus type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f5ff4-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f5ff4-116">Requirements</span></span>



| <span data-ttu-id="f5ff4-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f5ff4-117">Requirement</span></span> | <span data-ttu-id="f5ff4-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="f5ff4-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="f5ff4-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f5ff4-119">Minimum supported client</span></span><br/> | <span data-ttu-id="f5ff4-120">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f5ff4-120">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f5ff4-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f5ff4-121">Minimum supported server</span></span><br/> | <span data-ttu-id="f5ff4-122">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="f5ff4-122">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="f5ff4-123">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="f5ff4-123">End of client support</span></span><br/>    | <span data-ttu-id="f5ff4-124">Windows 7</span><span class="sxs-lookup"><span data-stu-id="f5ff4-124">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="f5ff4-125">Produit</span><span class="sxs-lookup"><span data-stu-id="f5ff4-125">Product</span></span><br/>                  | <span data-ttu-id="f5ff4-126">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="f5ff4-126">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="f5ff4-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="f5ff4-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="f5ff4-128"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="f5ff4-128"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |



 

