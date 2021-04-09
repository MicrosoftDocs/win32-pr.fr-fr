---
title: IVMVirtualNetwork _ID, méthode (VPCCOMInterfaces. h)
description: Récupère l’identificateur interne du réseau virtuel.
ms.assetid: 6f1f75be-4218-40b8-8c73-938f0801f5e5
keywords:
- Méthode _ID Virtual PC
- _ID méthode Virtual PC, interface IVMVirtualNetwork
- IVMVirtualNetwork interface Virtual PC, méthode _ID
topic_type:
- apiref
api_name:
- IVMVirtualNetwork._ID
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 68b79c4d6f4dfa778fee156b1bfa09ab39b8bedf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104033159"
---
# <a name="ivmvirtualnetwork_id-method"></a><span data-ttu-id="705dd-106">IVMVirtualNetwork :: \_ ID, méthode</span><span class="sxs-lookup"><span data-stu-id="705dd-106">IVMVirtualNetwork::\_ID method</span></span>

<span data-ttu-id="705dd-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="705dd-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="705dd-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="705dd-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="705dd-109">Récupère l’identificateur interne du réseau virtuel.</span><span class="sxs-lookup"><span data-stu-id="705dd-109">Retrieves the internal identifier of the virtual network.</span></span>

## <a name="syntax"></a><span data-ttu-id="705dd-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="705dd-110">Syntax</span></span>


```C++
HRESULT _ID(
  [out] VARIANT *virtualNetworkID
);
```



## <a name="parameters"></a><span data-ttu-id="705dd-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="705dd-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="705dd-112">*virtualNetworkID* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="705dd-112">*virtualNetworkID* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="705dd-113">Identificateur du réseau virtuel.</span><span class="sxs-lookup"><span data-stu-id="705dd-113">The virtual network identifier.</span></span> <span data-ttu-id="705dd-114">L’identificateur du réseau virtuel de réseau partagé (NAT) est 01010101010101010101010101010101.</span><span class="sxs-lookup"><span data-stu-id="705dd-114">The identifier for the Shared Networking (NAT) virtual network is 01010101010101010101010101010101.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="705dd-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="705dd-115">Return value</span></span>

<span data-ttu-id="705dd-116">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="705dd-116">This method can return one of these values.</span></span>



| <span data-ttu-id="705dd-117">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="705dd-117">Return code/value</span></span>                                                                                                                                                 | <span data-ttu-id="705dd-118">Description</span><span class="sxs-lookup"><span data-stu-id="705dd-118">Description</span></span>                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="705dd-119"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="705dd-119"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="705dd-120">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="705dd-120">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="705dd-121"><dt>**E \_ POINTEUR**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="705dd-121"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="705dd-122">Le paramètre a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="705dd-122">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="705dd-123"><dt>**DISP \_ E \_ exception**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="705dd-123"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="705dd-124">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="705dd-124">An unexpected error has occurred.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="705dd-125">Notes</span><span class="sxs-lookup"><span data-stu-id="705dd-125">Remarks</span></span>

<span data-ttu-id="705dd-126">Cette propriété n’est pas utilisable par les langages de script.</span><span class="sxs-lookup"><span data-stu-id="705dd-126">This property is not usable by scripting languages.</span></span>

## <a name="requirements"></a><span data-ttu-id="705dd-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="705dd-127">Requirements</span></span>



| <span data-ttu-id="705dd-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="705dd-128">Requirement</span></span> | <span data-ttu-id="705dd-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="705dd-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="705dd-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="705dd-130">Minimum supported client</span></span><br/> | <span data-ttu-id="705dd-131">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="705dd-131">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="705dd-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="705dd-132">Minimum supported server</span></span><br/> | <span data-ttu-id="705dd-133">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="705dd-133">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="705dd-134">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="705dd-134">End of client support</span></span><br/>    | <span data-ttu-id="705dd-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="705dd-135">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="705dd-136">Produit</span><span class="sxs-lookup"><span data-stu-id="705dd-136">Product</span></span><br/>                  | <span data-ttu-id="705dd-137">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="705dd-137">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="705dd-138">En-tête</span><span class="sxs-lookup"><span data-stu-id="705dd-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="705dd-139"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="705dd-139"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="705dd-140">IID</span><span class="sxs-lookup"><span data-stu-id="705dd-140">IID</span></span><br/>                      | <span data-ttu-id="705dd-141">IID \_ IVMVirtualNetwork est défini en tant que 431cb7a1-2469-4563-b94e-38b987adca63</span><span class="sxs-lookup"><span data-stu-id="705dd-141">IID\_IVMVirtualNetwork is defined as 431cb7a1-2469-4563-b94e-38b987adca63</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="705dd-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="705dd-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="705dd-143">**IVMVirtualNetwork**</span><span class="sxs-lookup"><span data-stu-id="705dd-143">**IVMVirtualNetwork**</span></span>](ivmvirtualnetwork.md)
</dt> </dl>

 

