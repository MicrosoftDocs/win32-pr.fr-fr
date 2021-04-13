---
title: Méthode IVMVirtualMachine RemoveNetworkAdapter (VPCCOMInterfaces. h)
description: Supprime une interface réseau de la machine virtuelle.
ms.assetid: 25a5b172-55b8-4cbe-98aa-630148cf6b6d
keywords:
- Méthode RemoveNetworkAdapter Virtual PC
- Méthode RemoveNetworkAdapter Virtual PC, interface IVMVirtualMachine
- IVMVirtualMachine interface Virtual PC, méthode RemoveNetworkAdapter
topic_type:
- apiref
api_name:
- IVMVirtualMachine.RemoveNetworkAdapter
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27424f7a3dc5445f56d960393aa12345fcf5f1cc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466395"
---
# <a name="ivmvirtualmachineremovenetworkadapter-method"></a><span data-ttu-id="e93a8-106">IVMVirtualMachine :: RemoveNetworkAdapter, méthode</span><span class="sxs-lookup"><span data-stu-id="e93a8-106">IVMVirtualMachine::RemoveNetworkAdapter method</span></span>

<span data-ttu-id="e93a8-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="e93a8-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="e93a8-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="e93a8-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="e93a8-109">Supprime une interface réseau de la machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="e93a8-109">Removes a network interface from the virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="e93a8-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e93a8-110">Syntax</span></span>


```C++
HRESULT RemoveNetworkAdapter(
  [in] IVMNetworkAdapter *networkAdapter
);
```



## <a name="parameters"></a><span data-ttu-id="e93a8-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e93a8-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e93a8-112">Carte réseau  \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e93a8-112">*networkAdapter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e93a8-113">Objet [**IVMNetworkAdapter**](ivmnetworkadapter.md) qui représente la carte réseau à supprimer.</span><span class="sxs-lookup"><span data-stu-id="e93a8-113">An [**IVMNetworkAdapter**](ivmnetworkadapter.md) object that represents the network adapter to be removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e93a8-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e93a8-114">Return value</span></span>

<span data-ttu-id="e93a8-115">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="e93a8-115">This method can return one of these values.</span></span>



| <span data-ttu-id="e93a8-116">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="e93a8-116">Return code/value</span></span>                                                                                                                                                            | <span data-ttu-id="e93a8-117">Description</span><span class="sxs-lookup"><span data-stu-id="e93a8-117">Description</span></span>                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <dl> <span data-ttu-id="e93a8-118"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="e93a8-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                  | <span data-ttu-id="e93a8-119">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="e93a8-119">The operation was successful.</span></span><br/>                       |
| <dl> <span data-ttu-id="e93a8-120"><dt>**E \_ POINTEUR**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="e93a8-120"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                    | <span data-ttu-id="e93a8-121">Le paramètre a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="e93a8-121">The parameter is **NULL**.</span></span><br/>                          |
| <dl> <span data-ttu-id="e93a8-122"><dt>**Ordinateur virtuel \_ \_Machine virtuelle \_**</dt> <dt>0xA0040207</dt> inconnue</span><span class="sxs-lookup"><span data-stu-id="e93a8-122"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>            | <span data-ttu-id="e93a8-123">La configuration est inconnue.</span><span class="sxs-lookup"><span data-stu-id="e93a8-123">The configuration is unknown.</span></span><br/>                       |
| <dl> <span data-ttu-id="e93a8-124"><dt>**Ordinateur virtuel \_ \_Machine virtuelle \_ en cours d’exécution \_ ou \_**</dt> <dt>0xA004020B</dt></span><span class="sxs-lookup"><span data-stu-id="e93a8-124"><dt>**VM\_E\_VM\_RUNNING\_OR\_SAVED**</dt> <dt>0xA004020B</dt></span></span> </dl> | <span data-ttu-id="e93a8-125">L’ordinateur virtuel est dans un État en cours d’exécution ou enregistré.</span><span class="sxs-lookup"><span data-stu-id="e93a8-125">The virtual machine is in a running or saved state.</span></span><br/> |
| <dl> <span data-ttu-id="e93a8-126"><dt>**DISP \_ E \_ exception**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="e93a8-126"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>            | <span data-ttu-id="e93a8-127">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="e93a8-127">An unexpected error has occurred.</span></span><br/>                   |



 

## <a name="remarks"></a><span data-ttu-id="e93a8-128">Notes</span><span class="sxs-lookup"><span data-stu-id="e93a8-128">Remarks</span></span>

<span data-ttu-id="e93a8-129">Vous pouvez uniquement supprimer une interface réseau existante d’un ordinateur virtuel qui est arrêté.</span><span class="sxs-lookup"><span data-stu-id="e93a8-129">You can only remove an existing network interface from a virtual machine that is stopped.</span></span>

## <a name="requirements"></a><span data-ttu-id="e93a8-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e93a8-130">Requirements</span></span>



| <span data-ttu-id="e93a8-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e93a8-131">Requirement</span></span> | <span data-ttu-id="e93a8-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="e93a8-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="e93a8-133">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e93a8-133">Minimum supported client</span></span><br/> | <span data-ttu-id="e93a8-134">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e93a8-134">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e93a8-135">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e93a8-135">Minimum supported server</span></span><br/> | <span data-ttu-id="e93a8-136">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="e93a8-136">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="e93a8-137">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="e93a8-137">End of client support</span></span><br/>    | <span data-ttu-id="e93a8-138">Windows 7</span><span class="sxs-lookup"><span data-stu-id="e93a8-138">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="e93a8-139">Produit</span><span class="sxs-lookup"><span data-stu-id="e93a8-139">Product</span></span><br/>                  | <span data-ttu-id="e93a8-140">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="e93a8-140">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="e93a8-141">En-tête</span><span class="sxs-lookup"><span data-stu-id="e93a8-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="e93a8-142"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="e93a8-142"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="e93a8-143">IID</span><span class="sxs-lookup"><span data-stu-id="e93a8-143">IID</span></span><br/>                      | <span data-ttu-id="e93a8-144">IID \_ IVMVirtualMachine est défini en tant que f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="e93a8-144">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="e93a8-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e93a8-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e93a8-146">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="e93a8-146">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

