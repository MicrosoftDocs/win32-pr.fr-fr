---
title: Méthode IVMVirtualMachine AddNetworkAdapter (VPCCOMInterfaces. h)
description: Ajoute une interface réseau à la machine virtuelle.
ms.assetid: 1fa39d2c-4a5a-42cb-afa4-520bf19b8cc8
keywords:
- Méthode AddNetworkAdapter Virtual PC
- Méthode AddNetworkAdapter Virtual PC, interface IVMVirtualMachine
- IVMVirtualMachine interface Virtual PC, méthode AddNetworkAdapter
topic_type:
- apiref
api_name:
- IVMVirtualMachine.AddNetworkAdapter
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8d24351e5f5a32aff08e755329ac12baaaaf546
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106509543"
---
# <a name="ivmvirtualmachineaddnetworkadapter-method"></a><span data-ttu-id="3fb33-106">IVMVirtualMachine :: AddNetworkAdapter, méthode</span><span class="sxs-lookup"><span data-stu-id="3fb33-106">IVMVirtualMachine::AddNetworkAdapter method</span></span>

<span data-ttu-id="3fb33-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="3fb33-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="3fb33-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="3fb33-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="3fb33-109">Ajoute une interface réseau à la machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="3fb33-109">Adds a network interface to the virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="3fb33-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3fb33-110">Syntax</span></span>


```C++
HRESULT AddNetworkAdapter(
  [out, retval] IVMNetworkAdapter **networkAdapter
);
```



## <a name="parameters"></a><span data-ttu-id="3fb33-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3fb33-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3fb33-112">Carte réseau  \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="3fb33-112">*networkAdapter* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="3fb33-113">Objet [**IVMNetworkAdapter**](ivmnetworkadapter.md) .</span><span class="sxs-lookup"><span data-stu-id="3fb33-113">An [**IVMNetworkAdapter**](ivmnetworkadapter.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3fb33-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3fb33-114">Return value</span></span>

<span data-ttu-id="3fb33-115">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="3fb33-115">This method can return one of these values.</span></span>



| <span data-ttu-id="3fb33-116">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="3fb33-116">Return code/value</span></span>                                                                                                                                                            | <span data-ttu-id="3fb33-117">Description</span><span class="sxs-lookup"><span data-stu-id="3fb33-117">Description</span></span>                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="3fb33-118"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="3fb33-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                  | <span data-ttu-id="3fb33-119">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="3fb33-119">The operation was successful.</span></span><br/>                        |
| <dl> <span data-ttu-id="3fb33-120"><dt>**E \_ POINTEUR**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="3fb33-120"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                    | <span data-ttu-id="3fb33-121">Le paramètre *networkAdapter* a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="3fb33-121">The *networkAdapter* parameter is **NULL**.</span></span><br/>          |
| <dl> <span data-ttu-id="3fb33-122"><dt>**Ordinateur virtuel \_ \_Machine virtuelle \_**</dt> <dt>0xA0040207</dt> inconnue</span><span class="sxs-lookup"><span data-stu-id="3fb33-122"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>            | <span data-ttu-id="3fb33-123">La configuration est inconnue.</span><span class="sxs-lookup"><span data-stu-id="3fb33-123">The configuration is unknown.</span></span><br/>                        |
| <dl> <span data-ttu-id="3fb33-124"><dt>**Ordinateur virtuel \_ E \_ pref \_ \_ valeur non conforme**</dt> <dt>0xA0040301</dt></span><span class="sxs-lookup"><span data-stu-id="3fb33-124"><dt>**VM\_E\_PREF\_ILLEGAL\_VALUE**</dt> <dt>0xA0040301</dt></span></span> </dl>   | <span data-ttu-id="3fb33-125">Vous ne pouvez pas ajouter plus de quatre (4) cartes réseau.</span><span class="sxs-lookup"><span data-stu-id="3fb33-125">No more than four (4) network adapters can be added.</span></span><br/> |
| <dl> <span data-ttu-id="3fb33-126"><dt>**Ordinateur virtuel \_ \_Machine virtuelle \_ en cours d’exécution \_ ou \_**</dt> <dt>0xA004020B</dt></span><span class="sxs-lookup"><span data-stu-id="3fb33-126"><dt>**VM\_E\_VM\_RUNNING\_OR\_SAVED**</dt> <dt>0xA004020B</dt></span></span> </dl> | <span data-ttu-id="3fb33-127">L’ordinateur virtuel est dans un État en cours d’exécution ou enregistré.</span><span class="sxs-lookup"><span data-stu-id="3fb33-127">The virtual machine is in a running or saved state.</span></span><br/>  |
| <dl> <span data-ttu-id="3fb33-128"><dt>**DISP \_ E \_ exception**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="3fb33-128"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>            | <span data-ttu-id="3fb33-129">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="3fb33-129">An unexpected error has occurred.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="3fb33-130">Notes</span><span class="sxs-lookup"><span data-stu-id="3fb33-130">Remarks</span></span>

<span data-ttu-id="3fb33-131">Vous pouvez uniquement ajouter une nouvelle interface réseau à une machine virtuelle arrêtée.</span><span class="sxs-lookup"><span data-stu-id="3fb33-131">You can only add a new network interface to a stopped virtual machine.</span></span> <span data-ttu-id="3fb33-132">La carte réseau nouvellement créée n’est pas connectée à un réseau virtuel.</span><span class="sxs-lookup"><span data-stu-id="3fb33-132">The newly created network adapter is not connected to a virtual network.</span></span>

## <a name="requirements"></a><span data-ttu-id="3fb33-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3fb33-133">Requirements</span></span>



| <span data-ttu-id="3fb33-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3fb33-134">Requirement</span></span> | <span data-ttu-id="3fb33-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="3fb33-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="3fb33-136">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3fb33-136">Minimum supported client</span></span><br/> | <span data-ttu-id="3fb33-137">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3fb33-137">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3fb33-138">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3fb33-138">Minimum supported server</span></span><br/> | <span data-ttu-id="3fb33-139">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="3fb33-139">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="3fb33-140">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="3fb33-140">End of client support</span></span><br/>    | <span data-ttu-id="3fb33-141">Windows 7</span><span class="sxs-lookup"><span data-stu-id="3fb33-141">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="3fb33-142">Produit</span><span class="sxs-lookup"><span data-stu-id="3fb33-142">Product</span></span><br/>                  | <span data-ttu-id="3fb33-143">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="3fb33-143">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="3fb33-144">En-tête</span><span class="sxs-lookup"><span data-stu-id="3fb33-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="3fb33-145"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="3fb33-145"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="3fb33-146">IID</span><span class="sxs-lookup"><span data-stu-id="3fb33-146">IID</span></span><br/>                      | <span data-ttu-id="3fb33-147">IID \_ IVMVirtualMachine est défini en tant que f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="3fb33-147">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="3fb33-148">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3fb33-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3fb33-149">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="3fb33-149">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

