---
title: Méthode IVMVirtualMachineEvents OnRequestShutdown (VPCCOMInterfaces. h)
description: Reçoit une notification indiquant qu’une demande d’arrêt a été effectuée.
ms.assetid: e04131fd-5ca7-4392-9725-ba62b905324a
keywords:
- Méthode OnRequestShutdown Virtual PC
- Méthode OnRequestShutdown Virtual PC, interface IVMVirtualMachineEvents
- IVMVirtualMachineEvents interface Virtual PC, méthode OnRequestShutdown
topic_type:
- apiref
api_name:
- IVMVirtualMachineEvents.OnRequestShutdown
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94dce60a7dfdb5ed5dce714e8b8eafcbd9558b95
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465766"
---
# <a name="ivmvirtualmachineeventsonrequestshutdown-method"></a><span data-ttu-id="fda14-106">IVMVirtualMachineEvents :: OnRequestShutdown, méthode</span><span class="sxs-lookup"><span data-stu-id="fda14-106">IVMVirtualMachineEvents::OnRequestShutdown method</span></span>

<span data-ttu-id="fda14-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="fda14-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="fda14-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="fda14-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="fda14-109">Reçoit une notification indiquant qu’une demande d’arrêt a été effectuée.</span><span class="sxs-lookup"><span data-stu-id="fda14-109">Receives notification that a shutdown request has been made.</span></span>

## <a name="syntax"></a><span data-ttu-id="fda14-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fda14-110">Syntax</span></span>


```C++
HRESULT OnRequestShutdown();
```



## <a name="parameters"></a><span data-ttu-id="fda14-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fda14-111">Parameters</span></span>

<span data-ttu-id="fda14-112">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="fda14-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="fda14-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="fda14-113">Return value</span></span>

<span data-ttu-id="fda14-114">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="fda14-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="fda14-115">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="fda14-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="fda14-116">Notes</span><span class="sxs-lookup"><span data-stu-id="fda14-116">Remarks</span></span>

<span data-ttu-id="fda14-117">Cette méthode est appelée chaque fois que la session de l’ordinateur virtuel va être arrêtée.</span><span class="sxs-lookup"><span data-stu-id="fda14-117">This method is called whenever the virtual machine session is about to shut down.</span></span> <span data-ttu-id="fda14-118">Le programme client doit implémenter cette méthode d’interface pour recevoir la notification de l’événement **vmVirtualMachineEvent \_ RequestShutdown** provenant de [**IVMVirtualMachine**](ivmvirtualmachine.md).</span><span class="sxs-lookup"><span data-stu-id="fda14-118">The client program must implement this interface method to receive notification of the **vmVirtualMachineEvent\_RequestShutdown** event originating from [**IVMVirtualMachine**](ivmvirtualmachine.md).</span></span>

<span data-ttu-id="fda14-119">Cette notification d’événement est envoyée uniquement lorsque la session machines virtuelles est sur le paragraphe d’être arrêtée.</span><span class="sxs-lookup"><span data-stu-id="fda14-119">This event notification is sent only when the virtual machines session is about to shut down.</span></span> <span data-ttu-id="fda14-120">Les routines d’arrêt du système d’exploitation, telles que [**IVMGuestOS :: Shutdown**](ivmguestos-shutdown.md), ne déclenchent pas cet événement directement, sauf si elles tentent également d’effectuer une mise hors tension logicielle du matériel virtuel.</span><span class="sxs-lookup"><span data-stu-id="fda14-120">Operating system shutdown routines, such as [**IVMGuestOS::Shutdown**](ivmguestos-shutdown.md), do not fire this event directly unless they also attempt to perform a software power off of the virtual hardware.</span></span>

## <a name="requirements"></a><span data-ttu-id="fda14-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fda14-121">Requirements</span></span>



| <span data-ttu-id="fda14-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fda14-122">Requirement</span></span> | <span data-ttu-id="fda14-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="fda14-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="fda14-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fda14-124">Minimum supported client</span></span><br/> | <span data-ttu-id="fda14-125">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fda14-125">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="fda14-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fda14-126">Minimum supported server</span></span><br/> | <span data-ttu-id="fda14-127">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="fda14-127">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="fda14-128">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="fda14-128">End of client support</span></span><br/>    | <span data-ttu-id="fda14-129">Windows 7</span><span class="sxs-lookup"><span data-stu-id="fda14-129">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="fda14-130">Produit</span><span class="sxs-lookup"><span data-stu-id="fda14-130">Product</span></span><br/>                  | <span data-ttu-id="fda14-131">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="fda14-131">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="fda14-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="fda14-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="fda14-133"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="fda14-133"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="fda14-134">IID</span><span class="sxs-lookup"><span data-stu-id="fda14-134">IID</span></span><br/>                      | <span data-ttu-id="fda14-135">DIID \_ IVMVirtualMachineEvents est défini comme 9d84f560-bb67-4961-BD12-a4da780c67e4</span><span class="sxs-lookup"><span data-stu-id="fda14-135">DIID\_IVMVirtualMachineEvents is defined as 9d84f560-bb67-4961-bd12-a4da780c67e4</span></span><br/>   |



## <a name="see-also"></a><span data-ttu-id="fda14-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fda14-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fda14-137">**IVMVirtualMachineEvents**</span><span class="sxs-lookup"><span data-stu-id="fda14-137">**IVMVirtualMachineEvents**</span></span>](ivmvirtualmachineevents.md)
</dt> </dl>

 

