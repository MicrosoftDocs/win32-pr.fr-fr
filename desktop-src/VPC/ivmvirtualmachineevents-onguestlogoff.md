---
title: Méthode IVMVirtualMachineEvents OnGuestLogoff (VPCCOMInterfaces. h)
description: Reçoit une notification indiquant qu’un utilisateur s’est déconnecté du système d’exploitation invité.
ms.assetid: 3771ba28-eea9-4c8b-9224-231b00d2f2f5
keywords:
- Méthode OnGuestLogoff Virtual PC
- Méthode OnGuestLogoff Virtual PC, interface IVMVirtualMachineEvents
- IVMVirtualMachineEvents interface Virtual PC, méthode OnGuestLogoff
topic_type:
- apiref
api_name:
- IVMVirtualMachineEvents.OnGuestLogoff
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ce5100c3901b3de32a769b6bae0e16fcffe26a8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941628"
---
# <a name="ivmvirtualmachineeventsonguestlogoff-method"></a><span data-ttu-id="5274b-106">IVMVirtualMachineEvents :: OnGuestLogoff, méthode</span><span class="sxs-lookup"><span data-stu-id="5274b-106">IVMVirtualMachineEvents::OnGuestLogoff method</span></span>

<span data-ttu-id="5274b-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="5274b-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="5274b-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="5274b-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="5274b-109">Reçoit une notification indiquant qu’un utilisateur s’est déconnecté du système d’exploitation invité.</span><span class="sxs-lookup"><span data-stu-id="5274b-109">Receives notification that a user has logged off from the guest operating system.</span></span>

## <a name="syntax"></a><span data-ttu-id="5274b-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5274b-110">Syntax</span></span>


```C++
HRESULT OnGuestLogoff(
  [in] VMLogoffType logoffType
);
```



## <a name="parameters"></a><span data-ttu-id="5274b-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5274b-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5274b-112">*logoffType* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5274b-112">*logoffType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5274b-113">Valeur de l’énumération [**VMLogoffType**](vmlogofftype.md) qui décrit le type de fermeture de session.</span><span class="sxs-lookup"><span data-stu-id="5274b-113">Value from the [**VMLogoffType**](vmlogofftype.md) enumeration that describes the type of logoff.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5274b-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5274b-114">Return value</span></span>

<span data-ttu-id="5274b-115">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="5274b-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="5274b-116">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="5274b-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="5274b-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5274b-117">Requirements</span></span>



| <span data-ttu-id="5274b-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5274b-118">Requirement</span></span> | <span data-ttu-id="5274b-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="5274b-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="5274b-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5274b-120">Minimum supported client</span></span><br/> | <span data-ttu-id="5274b-121">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5274b-121">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="5274b-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5274b-122">Minimum supported server</span></span><br/> | <span data-ttu-id="5274b-123">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="5274b-123">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="5274b-124">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="5274b-124">End of client support</span></span><br/>    | <span data-ttu-id="5274b-125">Windows 7</span><span class="sxs-lookup"><span data-stu-id="5274b-125">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="5274b-126">Produit</span><span class="sxs-lookup"><span data-stu-id="5274b-126">Product</span></span><br/>                  | <span data-ttu-id="5274b-127">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="5274b-127">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="5274b-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="5274b-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="5274b-129"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="5274b-129"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="5274b-130">IID</span><span class="sxs-lookup"><span data-stu-id="5274b-130">IID</span></span><br/>                      | <span data-ttu-id="5274b-131">DIID \_ IVMVirtualMachineEvents est défini comme 9d84f560-bb67-4961-BD12-a4da780c67e4</span><span class="sxs-lookup"><span data-stu-id="5274b-131">DIID\_IVMVirtualMachineEvents is defined as 9d84f560-bb67-4961-bd12-a4da780c67e4</span></span><br/>   |



## <a name="see-also"></a><span data-ttu-id="5274b-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5274b-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5274b-133">**IVMVirtualMachineEvents**</span><span class="sxs-lookup"><span data-stu-id="5274b-133">**IVMVirtualMachineEvents**</span></span>](ivmvirtualmachineevents.md)
</dt> <dt>

[<span data-ttu-id="5274b-134">**VMLogoffType**</span><span class="sxs-lookup"><span data-stu-id="5274b-134">**VMLogoffType**</span></span>](vmlogofftype.md)
</dt> </dl>

 

