---
title: IVMNetworkAdapter EthernetAddress, propriété (VPCCOMInterfaces. h)
description: Adresse Ethernet (MAC) de l’interface réseau.
ms.assetid: 2d94c5b3-6b69-4fb1-bee4-081dc026dde3
keywords:
- EthernetAddress propriété Virtual PC
- EthernetAddress, propriété Virtual PC, IVMNetworkAdapter, interface
- IVMNetworkAdapter interface Virtual PC, propriété EthernetAddress
topic_type:
- apiref
api_name:
- IVMNetworkAdapter.EthernetAddress
- IVMNetworkAdapter.get_EthernetAddress
- IVMNetworkAdapter.put_EthernetAddress
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7afb8f9035b0a663e01eeead95dc3f4f6bdec2e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103739757"
---
# <a name="ivmnetworkadapterethernetaddress-property"></a><span data-ttu-id="3c8a5-106">IVMNetworkAdapter :: EthernetAddress, propriété</span><span class="sxs-lookup"><span data-stu-id="3c8a5-106">IVMNetworkAdapter::EthernetAddress property</span></span>

<span data-ttu-id="3c8a5-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="3c8a5-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="3c8a5-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="3c8a5-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="3c8a5-109">Récupère et définit l’adresse Ethernet (MAC) de l’interface réseau.</span><span class="sxs-lookup"><span data-stu-id="3c8a5-109">Retrieves and sets the Ethernet (MAC) address of the network interface.</span></span>

<span data-ttu-id="3c8a5-110">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="3c8a5-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c8a5-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3c8a5-111">Syntax</span></span>


```C++
HRESULT put_EthernetAddress(
  [in]          BSTR ethernetAddress
);

HRESULT get_EthernetAddress(
  [out, retval] BSTR *ethernetAddress
);
```



## <a name="property-value"></a><span data-ttu-id="3c8a5-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="3c8a5-112">Property value</span></span>

<span data-ttu-id="3c8a5-113">Adresse MAC de la carte réseau virtuelle.</span><span class="sxs-lookup"><span data-stu-id="3c8a5-113">The MAC address of the virtual NIC.</span></span> <span data-ttu-id="3c8a5-114">Elle doit être au format "*XX* XX XX XX XX XX -  -  -  -  - *XX*", où chaque *X* est un chiffre hexadécimal.</span><span class="sxs-lookup"><span data-stu-id="3c8a5-114">It should have the form "*XX*-*XX*-*XX*-*XX*-*XX*-*XX*" where each *X* is a hexadecimal digit.</span></span>

## <a name="error-codes"></a><span data-ttu-id="3c8a5-115">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="3c8a5-115">Error codes</span></span>



| <span data-ttu-id="3c8a5-116">Nom/valeur</span><span class="sxs-lookup"><span data-stu-id="3c8a5-116">Name/value</span></span>                                                                                                                                                                         | <span data-ttu-id="3c8a5-117">Signification</span><span class="sxs-lookup"><span data-stu-id="3c8a5-117">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="3c8a5-118"><dt>\_OK</dt></span><span class="sxs-lookup"><span data-stu-id="3c8a5-118"><dt>S\_OK</dt></span></span> </dl>                                                                                                   | <span data-ttu-id="3c8a5-119">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="3c8a5-119">The operation was successful.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                    |
| <dl> <span data-ttu-id="3c8a5-120"><dt>E \_ POINTEUR</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="3c8a5-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                              | <span data-ttu-id="3c8a5-121">Le paramètre a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="3c8a5-121">The parameter is **NULL**.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                       |
| <dl> <span data-ttu-id="3c8a5-122"><dt>E \_ INVALIDARG</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="3c8a5-122"><dt>E\_INVALIDARG</dt> <dt>0x80000003</dt></span></span> </dl>                           | <span data-ttu-id="3c8a5-123">Le format du paramètre n’est pas correct.</span><span class="sxs-lookup"><span data-stu-id="3c8a5-123">The parameter is not in the correct format.</span></span><br/>                                                                                                                                                                                                                                                                                                                                      |
| <dl> <span data-ttu-id="3c8a5-124"><dt>Ordinateur virtuel \_ E \_ Impossible de \_ définir l' \_ \_ \_ adresse MAC dynamique</dt> <dt>0xA004070A</dt></span><span class="sxs-lookup"><span data-stu-id="3c8a5-124"><dt>VM\_E\_CANT\_SET\_DYNAMIC\_MAC\_ADDRESS</dt> <dt>0xA004070A</dt></span></span> </dl> | <span data-ttu-id="3c8a5-125">L’adresse Ethernet pour une interface réseau peut être générée de façon dynamique ou peut être définie sur une adresse statique par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="3c8a5-125">The Ethernet address for a network interface can either be generated dynamically or can be set to a static address by the user.</span></span> <span data-ttu-id="3c8a5-126">Cette méthode ne peut pas être appelée lorsque l’adresse est définie pour être générée dynamiquement.</span><span class="sxs-lookup"><span data-stu-id="3c8a5-126">This method cannot be called when the address is set to be generated dynamically.</span></span> <span data-ttu-id="3c8a5-127">La propriété [**IsEthernetAddressDynamic**](ivmnetworkadapter-isethernetaddressdynamic.md) est utilisée pour modifier le comportement de génération de l’adresse Ethernet.</span><span class="sxs-lookup"><span data-stu-id="3c8a5-127">The [**IsEthernetAddressDynamic**](ivmnetworkadapter-isethernetaddressdynamic.md) property is used to change the generation behavior of the Ethernet address.</span></span><br/> |
| <dl> <span data-ttu-id="3c8a5-128"><dt>Ordinateur virtuel \_ \_Machine virtuelle \_ </dt> <dt>0xA0040207</dt> inconnue</span><span class="sxs-lookup"><span data-stu-id="3c8a5-128"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl>                      | <span data-ttu-id="3c8a5-129">L’ordinateur virtuel est introuvable.</span><span class="sxs-lookup"><span data-stu-id="3c8a5-129">The virtual machine was not found.</span></span> <span data-ttu-id="3c8a5-130">Cela peut se produire si l’ordinateur a été supprimé après la création de l’objet [**IVMNetworkAdapter**](ivmnetworkadapter.md) .</span><span class="sxs-lookup"><span data-stu-id="3c8a5-130">This may occur if the machine was removed after the [**IVMNetworkAdapter**](ivmnetworkadapter.md) object was created.</span></span><br/>                                                                                                                                                                                                                        |
| <dl> <span data-ttu-id="3c8a5-131"><dt>DISP \_ E \_ exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="3c8a5-131"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                      | <span data-ttu-id="3c8a5-132">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="3c8a5-132">An unexpected error has occurred.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                |



## <a name="requirements"></a><span data-ttu-id="3c8a5-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3c8a5-133">Requirements</span></span>



| <span data-ttu-id="3c8a5-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3c8a5-134">Requirement</span></span> | <span data-ttu-id="3c8a5-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="3c8a5-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="3c8a5-136">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3c8a5-136">Minimum supported client</span></span><br/> | <span data-ttu-id="3c8a5-137">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3c8a5-137">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3c8a5-138">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3c8a5-138">Minimum supported server</span></span><br/> | <span data-ttu-id="3c8a5-139">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="3c8a5-139">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="3c8a5-140">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="3c8a5-140">End of client support</span></span><br/>    | <span data-ttu-id="3c8a5-141">Windows 7</span><span class="sxs-lookup"><span data-stu-id="3c8a5-141">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="3c8a5-142">Produit</span><span class="sxs-lookup"><span data-stu-id="3c8a5-142">Product</span></span><br/>                  | <span data-ttu-id="3c8a5-143">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="3c8a5-143">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="3c8a5-144">En-tête</span><span class="sxs-lookup"><span data-stu-id="3c8a5-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="3c8a5-145"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="3c8a5-145"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="3c8a5-146">IID</span><span class="sxs-lookup"><span data-stu-id="3c8a5-146">IID</span></span><br/>                      | <span data-ttu-id="3c8a5-147">IID \_ IVMNetworkAdapter est défini en tant que e32e4165-22b8-4DC0-8d57-850171ae207a</span><span class="sxs-lookup"><span data-stu-id="3c8a5-147">IID\_IVMNetworkAdapter is defined as e32e4165-22b8-4dc0-8d57-850171ae207a</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="3c8a5-148">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3c8a5-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c8a5-149">**IVMNetworkAdapter**</span><span class="sxs-lookup"><span data-stu-id="3c8a5-149">**IVMNetworkAdapter**</span></span>](ivmnetworkadapter.md)
</dt> </dl>

 

