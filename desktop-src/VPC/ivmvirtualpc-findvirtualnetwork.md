---
title: Méthode IVMVirtualPC FindVirtualNetwork (VPCCOMInterfaces. h)
description: Récupère un objet réseau virtuel qui correspond au nom demandé.
ms.assetid: 84526fa4-fe88-4466-866d-c432ed3125aa
keywords:
- Méthode FindVirtualNetwork Virtual PC
- Méthode FindVirtualNetwork Virtual PC, interface IVMVirtualPC
- IVMVirtualPC interface Virtual PC, méthode FindVirtualNetwork
topic_type:
- apiref
api_name:
- IVMVirtualPC.FindVirtualNetwork
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c59306d2e2022c1323ab52f1a47bd386347f504e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509037"
---
# <a name="ivmvirtualpcfindvirtualnetwork-method"></a><span data-ttu-id="f9a5d-106">IVMVirtualPC :: FindVirtualNetwork, méthode</span><span class="sxs-lookup"><span data-stu-id="f9a5d-106">IVMVirtualPC::FindVirtualNetwork method</span></span>

<span data-ttu-id="f9a5d-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="f9a5d-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="f9a5d-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="f9a5d-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="f9a5d-109">Récupère un objet réseau virtuel qui correspond au nom demandé.</span><span class="sxs-lookup"><span data-stu-id="f9a5d-109">Retrieves a virtual network object that matches the requested name.</span></span>

## <a name="syntax"></a><span data-ttu-id="f9a5d-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f9a5d-110">Syntax</span></span>


```C++
HRESULT FindVirtualNetwork(
  [in]          BSTR              virtualNetworkName,
  [out, retval] IVMVirtualNetwork **virtualNetwork
);
```



## <a name="parameters"></a><span data-ttu-id="f9a5d-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f9a5d-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f9a5d-112">*virtualNetworkName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f9a5d-112">*virtualNetworkName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f9a5d-113">Nom du réseau virtuel à rechercher.</span><span class="sxs-lookup"><span data-stu-id="f9a5d-113">The name of the virtual network to find.</span></span>

</dd> <dt>

<span data-ttu-id="f9a5d-114">*virtualNetwork* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="f9a5d-114">*virtualNetwork* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="f9a5d-115">Pointeur vers un nouvel objet [**IVMVirtualNetwork**](ivmvirtualnetwork.md) qui représente ce réseau virtuel.</span><span class="sxs-lookup"><span data-stu-id="f9a5d-115">A pointer to a new [**IVMVirtualNetwork**](ivmvirtualnetwork.md) object that represents this virtual network.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f9a5d-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f9a5d-116">Return value</span></span>

<span data-ttu-id="f9a5d-117">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="f9a5d-117">This method can return one of these values.</span></span>



| <span data-ttu-id="f9a5d-118">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="f9a5d-118">Return code/value</span></span>                                                                                                                                                                            | <span data-ttu-id="f9a5d-119">Description</span><span class="sxs-lookup"><span data-stu-id="f9a5d-119">Description</span></span>                                                                                     |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="f9a5d-120"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="f9a5d-120"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                                  | <span data-ttu-id="f9a5d-121">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="f9a5d-121">The operation was successful.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="f9a5d-122"><dt>**S \_ FALSe**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="f9a5d-122"><dt>**S\_FALSE**</dt> <dt>1</dt></span></span> </dl>                                               | <span data-ttu-id="f9a5d-123">Le réseau virtuel spécifié est introuvable.</span><span class="sxs-lookup"><span data-stu-id="f9a5d-123">The specified virtual network could not be found.</span></span><br/>                                    |
| <dl> <span data-ttu-id="f9a5d-124"><dt>**E \_ POINTEUR**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="f9a5d-124"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                    | <span data-ttu-id="f9a5d-125">Le paramètre *virtualNetwork* est **null** ou le réseau virtuel est introuvable.</span><span class="sxs-lookup"><span data-stu-id="f9a5d-125">The *virtualNetwork* parameter is **NULL** or the virtual network cannot be found.</span></span><br/>   |
| <dl> <span data-ttu-id="f9a5d-126"><dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="f9a5d-126"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>                                 | <span data-ttu-id="f9a5d-127">Le paramètre *virtualNetworkName* n’est pas valide ou est une chaîne vide.</span><span class="sxs-lookup"><span data-stu-id="f9a5d-127">The *virtualNetworkName* parameter is not valid or is an empty string.</span></span><br/>               |
| <dl> <span data-ttu-id="f9a5d-128">Valeur <dt>**HRESULT \_ FROM \_ Win32 ( \_ fichier d' \_ erreur \_ introuvable)**</dt> <dt>0x80070002</dt></span><span class="sxs-lookup"><span data-stu-id="f9a5d-128"><dt>**HRESULT\_FROM\_WIN32(ERROR\_FILE\_NOT\_FOUND)**</dt> <dt>0x80070002</dt></span></span> </dl> | <span data-ttu-id="f9a5d-129">Le fichier de réseau virtuel est introuvable.</span><span class="sxs-lookup"><span data-stu-id="f9a5d-129">The virtual network file could not be found.</span></span><br/>                                         |
| <dl> <span data-ttu-id="f9a5d-130"><dt>**DISP \_ E \_ exception**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="f9a5d-130"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                            | <span data-ttu-id="f9a5d-131">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="f9a5d-131">An unexpected error has occurred.</span></span><br/>                                                    |
| <dl> <span data-ttu-id="f9a5d-132"><dt>**Ordinateur virtuel \_ \_Virtualisation matérielle E \_ \_ désactivée**</dt> <dt>0xA0040951</dt></span><span class="sxs-lookup"><span data-stu-id="f9a5d-132"><dt>**VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED**</dt> <dt>0xA0040951</dt></span></span> </dl>     | <span data-ttu-id="f9a5d-133">Le processeur ne prend pas en charge les extensions avez (Hardware Accelerated Virtualization).</span><span class="sxs-lookup"><span data-stu-id="f9a5d-133">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="f9a5d-134">Notes</span><span class="sxs-lookup"><span data-stu-id="f9a5d-134">Remarks</span></span>

<span data-ttu-id="f9a5d-135">Les noms de réseaux virtuels ne respectent pas la casse, par exemple, « MyNetwork » et « mynetwork » font référence au même réseau virtuel.</span><span class="sxs-lookup"><span data-stu-id="f9a5d-135">Virtual network names are case-insensitive, for example, "MyNetwork" and "mynetwork" refer to the same virtual network.</span></span>

## <a name="requirements"></a><span data-ttu-id="f9a5d-136">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f9a5d-136">Requirements</span></span>



| <span data-ttu-id="f9a5d-137">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f9a5d-137">Requirement</span></span> | <span data-ttu-id="f9a5d-138">Valeur</span><span class="sxs-lookup"><span data-stu-id="f9a5d-138">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="f9a5d-139">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f9a5d-139">Minimum supported client</span></span><br/> | <span data-ttu-id="f9a5d-140">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f9a5d-140">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f9a5d-141">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f9a5d-141">Minimum supported server</span></span><br/> | <span data-ttu-id="f9a5d-142">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="f9a5d-142">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="f9a5d-143">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="f9a5d-143">End of client support</span></span><br/>    | <span data-ttu-id="f9a5d-144">Windows 7</span><span class="sxs-lookup"><span data-stu-id="f9a5d-144">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="f9a5d-145">Produit</span><span class="sxs-lookup"><span data-stu-id="f9a5d-145">Product</span></span><br/>                  | <span data-ttu-id="f9a5d-146">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="f9a5d-146">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="f9a5d-147">En-tête</span><span class="sxs-lookup"><span data-stu-id="f9a5d-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="f9a5d-148"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="f9a5d-148"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="f9a5d-149">IID</span><span class="sxs-lookup"><span data-stu-id="f9a5d-149">IID</span></span><br/>                      | <span data-ttu-id="f9a5d-150">IID \_ IVMVirtualPC est défini en tant que 236ba0d9-a24a-4292-A132-27c1421dfd01</span><span class="sxs-lookup"><span data-stu-id="f9a5d-150">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="f9a5d-151">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f9a5d-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9a5d-152">**IVMVirtualPC**</span><span class="sxs-lookup"><span data-stu-id="f9a5d-152">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> </dl>

 

