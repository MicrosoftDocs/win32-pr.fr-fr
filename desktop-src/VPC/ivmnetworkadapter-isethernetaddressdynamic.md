---
title: IVMNetworkAdapter IsEthernetAddressDynamic, propriété (VPCCOMInterfaces. h)
description: Détermine si l’adresse Ethernet est générée dynamiquement.
ms.assetid: 7bd87868-f1d1-48e5-9e1b-04d2126f9dad
keywords:
- IsEthernetAddressDynamic propriété Virtual PC
- IsEthernetAddressDynamic, propriété Virtual PC, IVMNetworkAdapter, interface
- IVMNetworkAdapter interface Virtual PC, propriété IsEthernetAddressDynamic
topic_type:
- apiref
api_name:
- IVMNetworkAdapter.IsEthernetAddressDynamic
- IVMNetworkAdapter.get_IsEthernetAddressDynamic
- IVMNetworkAdapter.put_IsEthernetAddressDynamic
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b16074243094d410e8d39538b024120daa1871e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032300"
---
# <a name="ivmnetworkadapterisethernetaddressdynamic-property"></a><span data-ttu-id="6df55-106">IVMNetworkAdapter :: IsEthernetAddressDynamic, propriété</span><span class="sxs-lookup"><span data-stu-id="6df55-106">IVMNetworkAdapter::IsEthernetAddressDynamic property</span></span>

<span data-ttu-id="6df55-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="6df55-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="6df55-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="6df55-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="6df55-109">Détermine si l’adresse Ethernet est générée dynamiquement.</span><span class="sxs-lookup"><span data-stu-id="6df55-109">Determines whether the Ethernet address is dynamically generated.</span></span>

<span data-ttu-id="6df55-110">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="6df55-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="6df55-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6df55-111">Syntax</span></span>


```C++
HRESULT put_IsEthernetAddressDynamic(
  [in]          VARIANT_BOOL isDynamic
);

HRESULT get_IsEthernetAddressDynamic(
  [out, retval] VARIANT_BOOL *isDynamic
);
```



## <a name="property-value"></a><span data-ttu-id="6df55-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="6df55-112">Property value</span></span>

<span data-ttu-id="6df55-113">Affectez la valeur VARIANT \_ true si l’adresse Ethernet doit être générée dynamiquement et la valeur \_ false pour la valeur false si l’adresse Ethernet est statique.</span><span class="sxs-lookup"><span data-stu-id="6df55-113">Set to VARIANT\_TRUE if the Ethernet address should be dynamically generated and VARIANT\_FALSE if the Ethernet address is static.</span></span>

## <a name="error-codes"></a><span data-ttu-id="6df55-114">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="6df55-114">Error codes</span></span>



| <span data-ttu-id="6df55-115">Nom/valeur</span><span class="sxs-lookup"><span data-stu-id="6df55-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="6df55-116">Signification</span><span class="sxs-lookup"><span data-stu-id="6df55-116">Meaning</span></span>                                                                                                                                                              |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="6df55-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="6df55-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="6df55-118">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="6df55-118">The operation was successful.</span></span><br/>                                                                                                                             |
| <dl> <span data-ttu-id="6df55-119"><dt>E \_ POINTEUR</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="6df55-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="6df55-120">Le paramètre a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="6df55-120">The parameter is **NULL**.</span></span><br/>                                                                                                                                |
| <dl> <span data-ttu-id="6df55-121"><dt>Ordinateur virtuel \_ \_Machine virtuelle \_ </dt> <dt>0xA0040207</dt> inconnue</span><span class="sxs-lookup"><span data-stu-id="6df55-121"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="6df55-122">L’ordinateur virtuel est introuvable.</span><span class="sxs-lookup"><span data-stu-id="6df55-122">The virtual machine was not found.</span></span> <span data-ttu-id="6df55-123">Cela peut se produire si l’ordinateur a été supprimé après la création de l’objet [**IVMNetworkAdapter**](ivmnetworkadapter.md) .</span><span class="sxs-lookup"><span data-stu-id="6df55-123">This may occur if the machine was removed after the [**IVMNetworkAdapter**](ivmnetworkadapter.md) object was created.</span></span><br/> |
| <dl> <span data-ttu-id="6df55-124"><dt>DISP \_ E \_ exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="6df55-124"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="6df55-125">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="6df55-125">An unexpected error has occurred.</span></span><br/>                                                                                                                         |



## <a name="remarks"></a><span data-ttu-id="6df55-126">Notes</span><span class="sxs-lookup"><span data-stu-id="6df55-126">Remarks</span></span>

<span data-ttu-id="6df55-127">Cette propriété doit avoir la valeur **true** (valeur par défaut) pour la plupart des interfaces réseau virtuelles.</span><span class="sxs-lookup"><span data-stu-id="6df55-127">This property should be set to **TRUE** (default) for most virtual network interfaces.</span></span> <span data-ttu-id="6df55-128">Si les logiciels de l’invité requièrent une adresse Ethernet statique, cette propriété doit avoir la valeur **false**.</span><span class="sxs-lookup"><span data-stu-id="6df55-128">If software in the guest requires a static Ethernet address, this property should be set to **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="6df55-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6df55-129">Requirements</span></span>



| <span data-ttu-id="6df55-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6df55-130">Requirement</span></span> | <span data-ttu-id="6df55-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="6df55-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="6df55-132">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6df55-132">Minimum supported client</span></span><br/> | <span data-ttu-id="6df55-133">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6df55-133">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="6df55-134">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6df55-134">Minimum supported server</span></span><br/> | <span data-ttu-id="6df55-135">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="6df55-135">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="6df55-136">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="6df55-136">End of client support</span></span><br/>    | <span data-ttu-id="6df55-137">Windows 7</span><span class="sxs-lookup"><span data-stu-id="6df55-137">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="6df55-138">Produit</span><span class="sxs-lookup"><span data-stu-id="6df55-138">Product</span></span><br/>                  | <span data-ttu-id="6df55-139">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="6df55-139">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="6df55-140">En-tête</span><span class="sxs-lookup"><span data-stu-id="6df55-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="6df55-141"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="6df55-141"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="6df55-142">IID</span><span class="sxs-lookup"><span data-stu-id="6df55-142">IID</span></span><br/>                      | <span data-ttu-id="6df55-143">IID \_ IVMNetworkAdapter est défini en tant que e32e4165-22b8-4DC0-8d57-850171ae207a</span><span class="sxs-lookup"><span data-stu-id="6df55-143">IID\_IVMNetworkAdapter is defined as e32e4165-22b8-4dc0-8d57-850171ae207a</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="6df55-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6df55-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6df55-145">**IVMNetworkAdapter**</span><span class="sxs-lookup"><span data-stu-id="6df55-145">**IVMNetworkAdapter**</span></span>](ivmnetworkadapter.md)
</dt> </dl>

 

