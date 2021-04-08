---
title: IVMGuestOS IntegrationComponentsVersion, propriété (VPCCOMInterfaces. h)
description: Récupère la version des composants d’intégration installés dans le système d’exploitation invité.
ms.assetid: 4baccb7d-5a3e-460f-9669-ee8dbaec91a9
keywords:
- IntegrationComponentsVersion propriété Virtual PC
- IntegrationComponentsVersion, propriété Virtual PC, IVMGuestOS, interface
- IVMGuestOS interface Virtual PC, propriété IntegrationComponentsVersion
topic_type:
- apiref
api_name:
- IVMGuestOS.IntegrationComponentsVersion
- IVMGuestOS.get_IntegrationComponentsVersion
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f85352614b89ab208377fe44fe3b970c693d60dd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740165"
---
# <a name="ivmguestosintegrationcomponentsversion-property"></a><span data-ttu-id="63d8b-106">IVMGuestOS :: IntegrationComponentsVersion, propriété</span><span class="sxs-lookup"><span data-stu-id="63d8b-106">IVMGuestOS::IntegrationComponentsVersion property</span></span>

<span data-ttu-id="63d8b-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="63d8b-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="63d8b-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="63d8b-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="63d8b-109">Récupère la version des composants d’intégration installés dans le système d’exploitation invité.</span><span class="sxs-lookup"><span data-stu-id="63d8b-109">Retrieves the version of the Integration Components installed in the guest operating system.</span></span>

<span data-ttu-id="63d8b-110">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="63d8b-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="63d8b-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="63d8b-111">Syntax</span></span>


```C++
HRESULT get_IntegrationComponentsVersion(
  [out, retval] BSTR *ICVersion
);
```



## <a name="property-value"></a><span data-ttu-id="63d8b-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="63d8b-112">Property value</span></span>

<span data-ttu-id="63d8b-113">Version.</span><span class="sxs-lookup"><span data-stu-id="63d8b-113">The version.</span></span>

## <a name="error-codes"></a><span data-ttu-id="63d8b-114">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="63d8b-114">Error codes</span></span>



| <span data-ttu-id="63d8b-115">Nom/valeur</span><span class="sxs-lookup"><span data-stu-id="63d8b-115">Name/value</span></span>                                                                                                                                                              | <span data-ttu-id="63d8b-116">Signification</span><span class="sxs-lookup"><span data-stu-id="63d8b-116">Meaning</span></span>                                                                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="63d8b-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="63d8b-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                 | <span data-ttu-id="63d8b-118">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="63d8b-118">The operation was successful.</span></span><br/>                                                     |
| <dl> <span data-ttu-id="63d8b-119"><dt>E \_ POINTEUR</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="63d8b-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                   | <span data-ttu-id="63d8b-120">Le paramètre a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="63d8b-120">The parameter is **NULL**.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="63d8b-121"><dt>Ordinateur virtuel \_ \_Machine virtuelle \_ </dt> <dt>0xA0040207</dt> inconnue</span><span class="sxs-lookup"><span data-stu-id="63d8b-121"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl>           | <span data-ttu-id="63d8b-122">Impossible de trouver la machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="63d8b-122">The virtual machine (VM) could not be found.</span></span><br/>                                      |
| <dl> <span data-ttu-id="63d8b-123"><dt>Ordinateur virtuel \_ \_Ajouts \_ non \_ </dt> réalisés <dt>0xA0040504</dt></span><span class="sxs-lookup"><span data-stu-id="63d8b-123"><dt>VM\_E\_ADDITIONS\_NOT\_AVAIL</dt> <dt>0xA0040504</dt></span></span> </dl> | <span data-ttu-id="63d8b-124">Les composants d’intégration ne sont pas installés sur cette machine virtuelle ou la machine virtuelle n’a jamais été démarrée.</span><span class="sxs-lookup"><span data-stu-id="63d8b-124">Integration Components are not installed in this VM, or the VM was never started.</span></span><br/> |
| <dl> <span data-ttu-id="63d8b-125"><dt>DISP \_ E \_ exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="63d8b-125"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>           | <span data-ttu-id="63d8b-126">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="63d8b-126">An unexpected error has occurred.</span></span><br/>                                                 |



## <a name="requirements"></a><span data-ttu-id="63d8b-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="63d8b-127">Requirements</span></span>



| <span data-ttu-id="63d8b-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="63d8b-128">Requirement</span></span> | <span data-ttu-id="63d8b-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="63d8b-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="63d8b-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="63d8b-130">Minimum supported client</span></span><br/> | <span data-ttu-id="63d8b-131">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="63d8b-131">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="63d8b-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="63d8b-132">Minimum supported server</span></span><br/> | <span data-ttu-id="63d8b-133">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="63d8b-133">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="63d8b-134">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="63d8b-134">End of client support</span></span><br/>    | <span data-ttu-id="63d8b-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="63d8b-135">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="63d8b-136">Produit</span><span class="sxs-lookup"><span data-stu-id="63d8b-136">Product</span></span><br/>                  | <span data-ttu-id="63d8b-137">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="63d8b-137">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="63d8b-138">En-tête</span><span class="sxs-lookup"><span data-stu-id="63d8b-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="63d8b-139"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="63d8b-139"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="63d8b-140">IID</span><span class="sxs-lookup"><span data-stu-id="63d8b-140">IID</span></span><br/>                      | <span data-ttu-id="63d8b-141">IID \_ IVMGuestOS est défini en tant que 99fea0db-4880-499a-B6D8-73dff9bc91be</span><span class="sxs-lookup"><span data-stu-id="63d8b-141">IID\_IVMGuestOS is defined as 99fea0db-4880-499a-b6d8-73dff9bc91be</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="63d8b-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="63d8b-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63d8b-143">**IVMGuestOS**</span><span class="sxs-lookup"><span data-stu-id="63d8b-143">**IVMGuestOS**</span></span>](ivmguestos.md)
</dt> </dl>

 

