---
title: énumération vmFloppyDriveEvent (VPCCOMInterfaces. h)
description: Spécifie les événements du lecteur de disquette.
ms.assetid: 31d0c748-609a-4e03-8b5c-0a17a2587242
keywords:
- Virtual PC de l’énumération vmFloppyDriveEvent
topic_type:
- apiref
api_name:
- vmFloppyDriveEvent
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a11b1485f91264713cf96a4f95cab8286261eea4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743077"
---
# <a name="vmfloppydriveevent-enumeration"></a><span data-ttu-id="1bdf2-104">énumération vmFloppyDriveEvent</span><span class="sxs-lookup"><span data-stu-id="1bdf2-104">vmFloppyDriveEvent enumeration</span></span>

<span data-ttu-id="1bdf2-105">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="1bdf2-105">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="1bdf2-106">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="1bdf2-106">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="1bdf2-107">Spécifie les événements du lecteur de disquette.</span><span class="sxs-lookup"><span data-stu-id="1bdf2-107">Specifies the floppy drive events.</span></span>

## <a name="syntax"></a><span data-ttu-id="1bdf2-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1bdf2-108">Syntax</span></span>


```C++
typedef enum  { 
  vmFloppyDriveEvent_OnInsert  = 1,
  vmFloppyDriveEvent_OnEject   = 2
} vmFloppyDriveEvent;
```



## <a name="constants"></a><span data-ttu-id="1bdf2-109">Constantes</span><span class="sxs-lookup"><span data-stu-id="1bdf2-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="1bdf2-110"><span id="vmFloppyDriveEvent_OnInsert"></span><span id="vmfloppydriveevent_oninsert"></span><span id="VMFLOPPYDRIVEEVENT_ONINSERT"></span>**vmFloppyDriveEvent \_ OnInsert**</span><span class="sxs-lookup"><span data-stu-id="1bdf2-110"><span id="vmFloppyDriveEvent_OnInsert"></span><span id="vmfloppydriveevent_oninsert"></span><span id="VMFLOPPYDRIVEEVENT_ONINSERT"></span>**vmFloppyDriveEvent\_OnInsert**</span></span>
</dt> <dd>

<span data-ttu-id="1bdf2-111">Une image de disquette est attachée ou un média réel est inséré dans un lecteur hôte.</span><span class="sxs-lookup"><span data-stu-id="1bdf2-111">A floppy disk image is attached or real media is inserted into a host drive.</span></span>

</dd> <dt>

<span data-ttu-id="1bdf2-112"><span id="vmFloppyDriveEvent_OnEject"></span><span id="vmfloppydriveevent_oneject"></span><span id="VMFLOPPYDRIVEEVENT_ONEJECT"></span>**vmFloppyDriveEvent \_ OnEject**</span><span class="sxs-lookup"><span data-stu-id="1bdf2-112"><span id="vmFloppyDriveEvent_OnEject"></span><span id="vmfloppydriveevent_oneject"></span><span id="VMFLOPPYDRIVEEVENT_ONEJECT"></span>**vmFloppyDriveEvent\_OnEject**</span></span>
</dt> <dd>

<span data-ttu-id="1bdf2-113">Le média a été éjecté.</span><span class="sxs-lookup"><span data-stu-id="1bdf2-113">Media has been ejected.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1bdf2-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1bdf2-114">Requirements</span></span>



| <span data-ttu-id="1bdf2-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1bdf2-115">Requirement</span></span> | <span data-ttu-id="1bdf2-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="1bdf2-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="1bdf2-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1bdf2-117">Minimum supported client</span></span><br/> | <span data-ttu-id="1bdf2-118">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1bdf2-118">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="1bdf2-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1bdf2-119">Minimum supported server</span></span><br/> | <span data-ttu-id="1bdf2-120">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="1bdf2-120">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="1bdf2-121">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="1bdf2-121">End of client support</span></span><br/>    | <span data-ttu-id="1bdf2-122">Windows 7</span><span class="sxs-lookup"><span data-stu-id="1bdf2-122">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="1bdf2-123">Produit</span><span class="sxs-lookup"><span data-stu-id="1bdf2-123">Product</span></span><br/>                  | <span data-ttu-id="1bdf2-124">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="1bdf2-124">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="1bdf2-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="1bdf2-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="1bdf2-126"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="1bdf2-126"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1bdf2-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1bdf2-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1bdf2-128">**IVMFloppyDriveEvents**</span><span class="sxs-lookup"><span data-stu-id="1bdf2-128">**IVMFloppyDriveEvents**</span></span>](ivmfloppydriveevents.md)
</dt> </dl>

 

