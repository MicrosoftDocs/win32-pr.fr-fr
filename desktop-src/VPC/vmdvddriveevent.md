---
title: Énumération VMDVDDriveEvent (VPCCOMInterfaces. h)
description: Spécifie les événements du lecteur de DVD.
ms.assetid: 17126138-614f-42d9-937e-1aca9393557c
keywords:
- Virtual PC de l’énumération VMDVDDriveEvent
topic_type:
- apiref
api_name:
- VMDVDDriveEvent
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 967fcd545c0ddd24d01c5dc779929ef4639c6736
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741396"
---
# <a name="vmdvddriveevent-enumeration"></a><span data-ttu-id="5834d-104">Énumération VMDVDDriveEvent</span><span class="sxs-lookup"><span data-stu-id="5834d-104">VMDVDDriveEvent enumeration</span></span>

<span data-ttu-id="5834d-105">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="5834d-105">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="5834d-106">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="5834d-106">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="5834d-107">Spécifie les événements du lecteur de DVD.</span><span class="sxs-lookup"><span data-stu-id="5834d-107">Specifies the DVD drive events.</span></span>

## <a name="syntax"></a><span data-ttu-id="5834d-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5834d-108">Syntax</span></span>


```C++
typedef enum  { 
  vmDVDDriveEvent_OnInsert  = 1,
  vmDVDDriveEvent_OnEject   = 2
} VMDVDDriveEvent;
```



## <a name="constants"></a><span data-ttu-id="5834d-109">Constantes</span><span class="sxs-lookup"><span data-stu-id="5834d-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="5834d-110"><span id="vmDVDDriveEvent_OnInsert"></span><span id="vmdvddriveevent_oninsert"></span><span id="VMDVDDRIVEEVENT_ONINSERT"></span>**vmDVDDriveEvent \_ OnInsert**</span><span class="sxs-lookup"><span data-stu-id="5834d-110"><span id="vmDVDDriveEvent_OnInsert"></span><span id="vmdvddriveevent_oninsert"></span><span id="VMDVDDRIVEEVENT_ONINSERT"></span>**vmDVDDriveEvent\_OnInsert**</span></span>
</dt> <dd>

<span data-ttu-id="5834d-111">Une image ISO est attachée ou un média réel est inséré dans un lecteur hôte.</span><span class="sxs-lookup"><span data-stu-id="5834d-111">An ISO image is attached or real media is inserted into a host drive.</span></span>

</dd> <dt>

<span data-ttu-id="5834d-112"><span id="vmDVDDriveEvent_OnEject"></span><span id="vmdvddriveevent_oneject"></span><span id="VMDVDDRIVEEVENT_ONEJECT"></span>**vmDVDDriveEvent \_ OnEject**</span><span class="sxs-lookup"><span data-stu-id="5834d-112"><span id="vmDVDDriveEvent_OnEject"></span><span id="vmdvddriveevent_oneject"></span><span id="VMDVDDRIVEEVENT_ONEJECT"></span>**vmDVDDriveEvent\_OnEject**</span></span>
</dt> <dd>

<span data-ttu-id="5834d-113">Le support a été éjecté.</span><span class="sxs-lookup"><span data-stu-id="5834d-113">The media has been ejected.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5834d-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5834d-114">Requirements</span></span>



| <span data-ttu-id="5834d-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5834d-115">Requirement</span></span> | <span data-ttu-id="5834d-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="5834d-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="5834d-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5834d-117">Minimum supported client</span></span><br/> | <span data-ttu-id="5834d-118">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5834d-118">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="5834d-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5834d-119">Minimum supported server</span></span><br/> | <span data-ttu-id="5834d-120">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="5834d-120">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="5834d-121">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="5834d-121">End of client support</span></span><br/>    | <span data-ttu-id="5834d-122">Windows 7</span><span class="sxs-lookup"><span data-stu-id="5834d-122">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="5834d-123">Produit</span><span class="sxs-lookup"><span data-stu-id="5834d-123">Product</span></span><br/>                  | <span data-ttu-id="5834d-124">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="5834d-124">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="5834d-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="5834d-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="5834d-126"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="5834d-126"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5834d-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5834d-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5834d-128">**IVMDVDDriveEvents**</span><span class="sxs-lookup"><span data-stu-id="5834d-128">**IVMDVDDriveEvents**</span></span>](ivmdvddriveevents.md)
</dt> </dl>

 

