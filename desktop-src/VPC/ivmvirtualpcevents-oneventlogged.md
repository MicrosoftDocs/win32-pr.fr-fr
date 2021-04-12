---
title: Méthode IVMVirtualPCEvents OnEventLogged (VPCCOMInterfaces. h)
description: Reçoit une notification indiquant que Windows Virtual PC enregistre un événement.
ms.assetid: 89439e8e-e9bf-409e-a129-525b9feb8fdd
keywords:
- Méthode OnEventLogged Virtual PC
- Méthode OnEventLogged Virtual PC, interface IVMVirtualPCEvents
- IVMVirtualPCEvents interface Virtual PC, méthode OnEventLogged
topic_type:
- apiref
api_name:
- IVMVirtualPCEvents.OnEventLogged
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 196d480383f488c9c0885e95857c8d1a053d5887
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508726"
---
# <a name="ivmvirtualpceventsoneventlogged-method"></a><span data-ttu-id="2311c-106">IVMVirtualPCEvents :: OnEventLogged, méthode</span><span class="sxs-lookup"><span data-stu-id="2311c-106">IVMVirtualPCEvents::OnEventLogged method</span></span>

<span data-ttu-id="2311c-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="2311c-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="2311c-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="2311c-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="2311c-109">Reçoit une notification indiquant que Windows Virtual PC enregistre un événement.</span><span class="sxs-lookup"><span data-stu-id="2311c-109">Receives notification that Windows Virtual PC logs an event.</span></span>

## <a name="syntax"></a><span data-ttu-id="2311c-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2311c-110">Syntax</span></span>


```C++
HRESULT OnEventLogged(
  [in] long logMessageID
);
```



## <a name="parameters"></a><span data-ttu-id="2311c-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2311c-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2311c-112">*logMessageID* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2311c-112">*logMessageID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2311c-113">Identificateur du message du journal des événements qui a été enregistré.</span><span class="sxs-lookup"><span data-stu-id="2311c-113">The message identifier of the event log message that was logged.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2311c-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2311c-114">Return value</span></span>

<span data-ttu-id="2311c-115">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="2311c-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="2311c-116">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="2311c-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="2311c-117">Notes</span><span class="sxs-lookup"><span data-stu-id="2311c-117">Remarks</span></span>

<span data-ttu-id="2311c-118">Cette méthode est appelée lorsque Windows Virtual PC consigne un message dans le journal des événements Windows.</span><span class="sxs-lookup"><span data-stu-id="2311c-118">This method is called when Windows Virtual PC logs a message to the Windows event log.</span></span> <span data-ttu-id="2311c-119">Le programme client doit implémenter cette méthode d’interface pour recevoir la notification de l’événement **vmVirtualPCEvent \_ EventLogged** provenant de [**IVMVirtualPC**](ivmvirtualpc.md).</span><span class="sxs-lookup"><span data-stu-id="2311c-119">The client program must implement this interface method to receive notification of the **vmVirtualPCEvent\_EventLogged** event originating from [**IVMVirtualPC**](ivmvirtualpc.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2311c-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2311c-120">Requirements</span></span>



| <span data-ttu-id="2311c-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2311c-121">Requirement</span></span> | <span data-ttu-id="2311c-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="2311c-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="2311c-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2311c-123">Minimum supported client</span></span><br/> | <span data-ttu-id="2311c-124">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2311c-124">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="2311c-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2311c-125">Minimum supported server</span></span><br/> | <span data-ttu-id="2311c-126">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="2311c-126">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="2311c-127">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="2311c-127">End of client support</span></span><br/>    | <span data-ttu-id="2311c-128">Windows 7</span><span class="sxs-lookup"><span data-stu-id="2311c-128">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="2311c-129">Produit</span><span class="sxs-lookup"><span data-stu-id="2311c-129">Product</span></span><br/>                  | <span data-ttu-id="2311c-130">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="2311c-130">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="2311c-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="2311c-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="2311c-132"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="2311c-132"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="2311c-133">IID</span><span class="sxs-lookup"><span data-stu-id="2311c-133">IID</span></span><br/>                      | <span data-ttu-id="2311c-134">DIID \_ IVMVirtualPCEvents est défini comme efed1ef1-3c09-41f7-a9c2-7e29fa286c9d</span><span class="sxs-lookup"><span data-stu-id="2311c-134">DIID\_IVMVirtualPCEvents is defined as efed1ef1-3c09-41f7-a9c2-7e29fa286c9d</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="2311c-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2311c-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2311c-136">**IVMVirtualPCEvents**</span><span class="sxs-lookup"><span data-stu-id="2311c-136">**IVMVirtualPCEvents**</span></span>](ivmvirtualpcevents.md)
</dt> </dl>

 

