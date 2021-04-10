---
title: Méthode IVMVirtualMachineEvents OnConfigurationChanged (VPCCOMInterfaces. h)
description: Reçoit une notification indiquant qu’une valeur de la configuration de cet ordinateur virtuel a changé.
ms.assetid: 1955f23e-b318-41aa-b82e-81283be81608
keywords:
- Méthode OnConfigurationChanged Virtual PC
- Méthode OnConfigurationChanged Virtual PC, interface IVMVirtualMachineEvents
- IVMVirtualMachineEvents interface Virtual PC, méthode OnConfigurationChanged
topic_type:
- apiref
api_name:
- IVMVirtualMachineEvents.OnConfigurationChanged
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10459562da2d87b8c883217e003cd822ef923fad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941629"
---
# <a name="ivmvirtualmachineeventsonconfigurationchanged-method"></a><span data-ttu-id="d3416-106">IVMVirtualMachineEvents :: OnConfigurationChanged, méthode</span><span class="sxs-lookup"><span data-stu-id="d3416-106">IVMVirtualMachineEvents::OnConfigurationChanged method</span></span>

<span data-ttu-id="d3416-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="d3416-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="d3416-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="d3416-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="d3416-109">Reçoit une notification indiquant qu’une valeur de la configuration de cet ordinateur virtuel a changé.</span><span class="sxs-lookup"><span data-stu-id="d3416-109">Receives notification that a value in the configuration for this virtual machine has changed.</span></span>

## <a name="syntax"></a><span data-ttu-id="d3416-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d3416-110">Syntax</span></span>


```C++
HRESULT OnConfigurationChanged(
  [in] BSTR    configKey,
  [in] VARIANT configData
);
```



## <a name="parameters"></a><span data-ttu-id="d3416-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d3416-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d3416-112">*configKey* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d3416-112">*configKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d3416-113">Valeur à l’intérieur de la configuration qui a changé.</span><span class="sxs-lookup"><span data-stu-id="d3416-113">The value inside the configuration that has changed.</span></span>

</dd> <dt>

<span data-ttu-id="d3416-114">*configData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d3416-114">*configData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d3416-115">Nouvelle valeur de la configuration.</span><span class="sxs-lookup"><span data-stu-id="d3416-115">The new value for the configuration.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d3416-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d3416-116">Return value</span></span>

<span data-ttu-id="d3416-117">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="d3416-117">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="d3416-118">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d3416-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="d3416-119">Notes</span><span class="sxs-lookup"><span data-stu-id="d3416-119">Remarks</span></span>

<span data-ttu-id="d3416-120">Cette méthode est appelée lorsque la configuration est modifiée pour cet ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="d3416-120">This method is called when the configuration changes for this virtual machine.</span></span> <span data-ttu-id="d3416-121">Le programme client doit implémenter cette méthode d’interface pour recevoir la notification de l' \_ événement vmVirtualMachineEvent ConfigurationChanged provenant de [**IVMVirtualMachine**](ivmvirtualmachine.md).</span><span class="sxs-lookup"><span data-stu-id="d3416-121">The client program must implement this interface method to receive notification of the vmVirtualMachineEvent\_ConfigurationChanged event originating from [**IVMVirtualMachine**](ivmvirtualmachine.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d3416-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d3416-122">Requirements</span></span>



| <span data-ttu-id="d3416-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d3416-123">Requirement</span></span> | <span data-ttu-id="d3416-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="d3416-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="d3416-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d3416-125">Minimum supported client</span></span><br/> | <span data-ttu-id="d3416-126">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d3416-126">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d3416-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d3416-127">Minimum supported server</span></span><br/> | <span data-ttu-id="d3416-128">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="d3416-128">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="d3416-129">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="d3416-129">End of client support</span></span><br/>    | <span data-ttu-id="d3416-130">Windows 7</span><span class="sxs-lookup"><span data-stu-id="d3416-130">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="d3416-131">Produit</span><span class="sxs-lookup"><span data-stu-id="d3416-131">Product</span></span><br/>                  | <span data-ttu-id="d3416-132">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="d3416-132">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="d3416-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="d3416-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="d3416-134"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="d3416-134"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="d3416-135">IID</span><span class="sxs-lookup"><span data-stu-id="d3416-135">IID</span></span><br/>                      | <span data-ttu-id="d3416-136">DIID \_ IVMVirtualMachineEvents est défini comme 9d84f560-bb67-4961-BD12-a4da780c67e4</span><span class="sxs-lookup"><span data-stu-id="d3416-136">DIID\_IVMVirtualMachineEvents is defined as 9d84f560-bb67-4961-bd12-a4da780c67e4</span></span><br/>   |



## <a name="see-also"></a><span data-ttu-id="d3416-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d3416-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3416-138">**IVMVirtualMachineEvents**</span><span class="sxs-lookup"><span data-stu-id="d3416-138">**IVMVirtualMachineEvents**</span></span>](ivmvirtualmachineevents.md)
</dt> </dl>

 

