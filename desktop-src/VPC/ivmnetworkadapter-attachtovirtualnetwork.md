---
title: Méthode IVMNetworkAdapter AttachToVirtualNetwork (VPCCOMInterfaces. h)
description: Attache l’interface réseau au réseau virtuel spécifié.
ms.assetid: c743e930-c22e-4f32-b691-f7adc2485fed
keywords:
- Méthode AttachToVirtualNetwork Virtual PC
- Méthode AttachToVirtualNetwork Virtual PC, interface IVMNetworkAdapter
- IVMNetworkAdapter interface Virtual PC, méthode AttachToVirtualNetwork
topic_type:
- apiref
api_name:
- IVMNetworkAdapter.AttachToVirtualNetwork
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01e7d0d9822e73ef6081a35f19ef628fd10051b1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465622"
---
# <a name="ivmnetworkadapterattachtovirtualnetwork-method"></a><span data-ttu-id="2bbf0-106">IVMNetworkAdapter :: AttachToVirtualNetwork, méthode</span><span class="sxs-lookup"><span data-stu-id="2bbf0-106">IVMNetworkAdapter::AttachToVirtualNetwork method</span></span>

<span data-ttu-id="2bbf0-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="2bbf0-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="2bbf0-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="2bbf0-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="2bbf0-109">Attache l’interface réseau au réseau virtuel spécifié.</span><span class="sxs-lookup"><span data-stu-id="2bbf0-109">Attaches the network interface to the specified virtual network.</span></span>

## <a name="syntax"></a><span data-ttu-id="2bbf0-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2bbf0-110">Syntax</span></span>


```C++
HRESULT AttachToVirtualNetwork(
  [in] IVMVirtualNetwork *virtualNetwork
);
```



## <a name="parameters"></a><span data-ttu-id="2bbf0-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2bbf0-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2bbf0-112">*virtualNetwork* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2bbf0-112">*virtualNetwork* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2bbf0-113">Le réseau virtuel auquel cette carte d’interface réseau virtuelle sera connectée.</span><span class="sxs-lookup"><span data-stu-id="2bbf0-113">The virtual network to which this virtual NIC will be connected.</span></span> <span data-ttu-id="2bbf0-114">Consultez [**IVMVirtualNetwork**](ivmvirtualnetwork.md).</span><span class="sxs-lookup"><span data-stu-id="2bbf0-114">See [**IVMVirtualNetwork**](ivmvirtualnetwork.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2bbf0-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2bbf0-115">Return value</span></span>

<span data-ttu-id="2bbf0-116">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="2bbf0-116">This method can return one of these values.</span></span>



| <span data-ttu-id="2bbf0-117">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="2bbf0-117">Return code/value</span></span>                                                                                                                                                                          | <span data-ttu-id="2bbf0-118">Description</span><span class="sxs-lookup"><span data-stu-id="2bbf0-118">Description</span></span>                                                        |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="2bbf0-119"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="2bbf0-119"><dt>**S\_OK**</dt></span></span> </dl>                                                                                                       | <span data-ttu-id="2bbf0-120">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="2bbf0-120">The operation was successful.</span></span><br/>                           |
| <dl> <span data-ttu-id="2bbf0-121"><dt>**E \_ POINTEUR**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="2bbf0-121"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                  | <span data-ttu-id="2bbf0-122">Le paramètre a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="2bbf0-122">The parameter is **NULL**.</span></span><br/>                              |
| <dl> <span data-ttu-id="2bbf0-123"><dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="2bbf0-123"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>                               | <span data-ttu-id="2bbf0-124">Le paramètre ne contient pas de réseau virtuel valide.</span><span class="sxs-lookup"><span data-stu-id="2bbf0-124">The parameter does not contain a valid virtual network.</span></span><br/> |
| <dl> <span data-ttu-id="2bbf0-125">Valeur <dt>**HRESULT \_ À partir de \_ Win32 ( \_ accès à l’erreur \_ refusé)**</dt> <dt>0x80070005</dt></span><span class="sxs-lookup"><span data-stu-id="2bbf0-125"><dt>**HRESULT\_FROM\_WIN32(ERROR\_ACCESS\_DENIED)**</dt> <dt>0x80070005</dt></span></span> </dl> | <span data-ttu-id="2bbf0-126">L’accès a été refusé au réseau virtuel demandé.</span><span class="sxs-lookup"><span data-stu-id="2bbf0-126">Access was denied to the requested virtual network.</span></span><br/>     |
| <dl> <span data-ttu-id="2bbf0-127"><dt>**Ordinateur virtuel \_ \_Machine virtuelle \_**</dt> <dt>0xA0040207</dt> inconnue</span><span class="sxs-lookup"><span data-stu-id="2bbf0-127"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>                          | <span data-ttu-id="2bbf0-128">L’ordinateur virtuel n’est pas valide ou n’existe plus.</span><span class="sxs-lookup"><span data-stu-id="2bbf0-128">The virtual machine is invalid or no longer exists.</span></span><br/>     |
| <dl> <span data-ttu-id="2bbf0-129"><dt>**\_ID de \_ réseau virtuel non valide de \_ la machine \_ virtuelle \_**</dt></span><span class="sxs-lookup"><span data-stu-id="2bbf0-129"><dt>**VM\_E\_INVALID\_VIRTUAL\_NETWORK\_ID**</dt></span></span> </dl>                                                                        | <span data-ttu-id="2bbf0-130">Le paramètre n’est pas un réseau virtuel existant.</span><span class="sxs-lookup"><span data-stu-id="2bbf0-130">The parameter is not an existing virtual network.</span></span><br/>       |
| <dl> <span data-ttu-id="2bbf0-131"><dt>**\_exception DISP E \_**</dt></span><span class="sxs-lookup"><span data-stu-id="2bbf0-131"><dt>**DISP\_E\_EXCEPTION**</dt></span></span> </dl>                                                                                          | <span data-ttu-id="2bbf0-132">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="2bbf0-132">An unexpected error has occurred.</span></span><br/>                       |



 

## <a name="requirements"></a><span data-ttu-id="2bbf0-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2bbf0-133">Requirements</span></span>



| <span data-ttu-id="2bbf0-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2bbf0-134">Requirement</span></span> | <span data-ttu-id="2bbf0-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="2bbf0-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="2bbf0-136">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2bbf0-136">Minimum supported client</span></span><br/> | <span data-ttu-id="2bbf0-137">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2bbf0-137">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="2bbf0-138">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2bbf0-138">Minimum supported server</span></span><br/> | <span data-ttu-id="2bbf0-139">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="2bbf0-139">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="2bbf0-140">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="2bbf0-140">End of client support</span></span><br/>    | <span data-ttu-id="2bbf0-141">Windows 7</span><span class="sxs-lookup"><span data-stu-id="2bbf0-141">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="2bbf0-142">Produit</span><span class="sxs-lookup"><span data-stu-id="2bbf0-142">Product</span></span><br/>                  | <span data-ttu-id="2bbf0-143">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="2bbf0-143">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="2bbf0-144">En-tête</span><span class="sxs-lookup"><span data-stu-id="2bbf0-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="2bbf0-145"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="2bbf0-145"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="2bbf0-146">IID</span><span class="sxs-lookup"><span data-stu-id="2bbf0-146">IID</span></span><br/>                      | <span data-ttu-id="2bbf0-147">IID \_ IVMNetworkAdapter est défini en tant que e32e4165-22b8-4DC0-8d57-850171ae207a</span><span class="sxs-lookup"><span data-stu-id="2bbf0-147">IID\_IVMNetworkAdapter is defined as e32e4165-22b8-4dc0-8d57-850171ae207a</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="2bbf0-148">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2bbf0-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2bbf0-149">**IVMNetworkAdapter**</span><span class="sxs-lookup"><span data-stu-id="2bbf0-149">**IVMNetworkAdapter**</span></span>](ivmnetworkadapter.md)
</dt> </dl>

 

