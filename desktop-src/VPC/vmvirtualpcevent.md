---
title: Énumération VMVirtualPCEvent (VPCCOMInterfaces. h)
description: Spécifie les événements de PC virtuels Windows.
ms.assetid: 3b239cd0-d922-42de-8bcc-51f625c0d8b0
keywords:
- Virtual PC de l’énumération VMVirtualPCEvent
topic_type:
- apiref
api_name:
- VMVirtualPCEvent
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4de7ecb639d0b62165dec691d522bed8116670c8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104033248"
---
# <a name="vmvirtualpcevent-enumeration"></a><span data-ttu-id="1692c-104">Énumération VMVirtualPCEvent</span><span class="sxs-lookup"><span data-stu-id="1692c-104">VMVirtualPCEvent enumeration</span></span>

<span data-ttu-id="1692c-105">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="1692c-105">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="1692c-106">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="1692c-106">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="1692c-107">Spécifie les événements de PC virtuels Windows.</span><span class="sxs-lookup"><span data-stu-id="1692c-107">Specifies the Windows Virtual PC events.</span></span>

## <a name="syntax"></a><span data-ttu-id="1692c-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1692c-108">Syntax</span></span>


```C++
typedef enum  { 
  vmVirtualPCEvent_VMStateChange  = 2,
  vmVirtualPCEvent_EventLogged    = 3
} VMVirtualPCEvent;
```



## <a name="constants"></a><span data-ttu-id="1692c-109">Constantes</span><span class="sxs-lookup"><span data-stu-id="1692c-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="1692c-110"><span id="vmVirtualPCEvent_VMStateChange"></span><span id="vmvirtualpcevent_vmstatechange"></span><span id="VMVIRTUALPCEVENT_VMSTATECHANGE"></span>**vmVirtualPCEvent \_ VMStateChange**</span><span class="sxs-lookup"><span data-stu-id="1692c-110"><span id="vmVirtualPCEvent_VMStateChange"></span><span id="vmvirtualpcevent_vmstatechange"></span><span id="VMVIRTUALPCEVENT_VMSTATECHANGE"></span>**vmVirtualPCEvent\_VMStateChange**</span></span>
</dt> <dd>

<span data-ttu-id="1692c-111">L’état d’une machine virtuelle a été modifié.</span><span class="sxs-lookup"><span data-stu-id="1692c-111">A virtual machine's state has changed.</span></span>

</dd> <dt>

<span data-ttu-id="1692c-112"><span id="vmVirtualPCEvent_EventLogged"></span><span id="vmvirtualpcevent_eventlogged"></span><span id="VMVIRTUALPCEVENT_EVENTLOGGED"></span>**vmVirtualPCEvent \_ EventLogged**</span><span class="sxs-lookup"><span data-stu-id="1692c-112"><span id="vmVirtualPCEvent_EventLogged"></span><span id="vmvirtualpcevent_eventlogged"></span><span id="VMVIRTUALPCEVENT_EVENTLOGGED"></span>**vmVirtualPCEvent\_EventLogged**</span></span>
</dt> <dd>

<span data-ttu-id="1692c-113">Virtual PC a consigné un événement.</span><span class="sxs-lookup"><span data-stu-id="1692c-113">Virtual PC has logged an event.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1692c-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1692c-114">Requirements</span></span>



| <span data-ttu-id="1692c-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1692c-115">Requirement</span></span> | <span data-ttu-id="1692c-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="1692c-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="1692c-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1692c-117">Minimum supported client</span></span><br/> | <span data-ttu-id="1692c-118">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1692c-118">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="1692c-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1692c-119">Minimum supported server</span></span><br/> | <span data-ttu-id="1692c-120">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="1692c-120">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="1692c-121">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="1692c-121">End of client support</span></span><br/>    | <span data-ttu-id="1692c-122">Windows 7</span><span class="sxs-lookup"><span data-stu-id="1692c-122">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="1692c-123">Produit</span><span class="sxs-lookup"><span data-stu-id="1692c-123">Product</span></span><br/>                  | <span data-ttu-id="1692c-124">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="1692c-124">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="1692c-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="1692c-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="1692c-126"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="1692c-126"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1692c-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1692c-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1692c-128">**IVMVirtualPCEvents**</span><span class="sxs-lookup"><span data-stu-id="1692c-128">**IVMVirtualPCEvents**</span></span>](ivmvirtualpcevents.md)
</dt> </dl>

 

