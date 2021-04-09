---
title: IVMHostInfo NetworkAdapters, propriété (VPCCOMInterfaces. h)
description: Récupère une collection énumérable de cartes réseau sur l’ordinateur hôte.
ms.assetid: 17393d7a-c883-4d67-826b-83b886c0d7a6
keywords:
- NetworkAdapters propriété Virtual PC
- NetworkAdapters, propriété Virtual PC, IVMHostInfo, interface
- IVMHostInfo interface Virtual PC, propriété NetworkAdapters
topic_type:
- apiref
api_name:
- IVMHostInfo.NetworkAdapters
- IVMHostInfo.get_NetworkAdapters
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eeff5c6d459fb8f6999f896c3c13fcd980bf70ac
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941633"
---
# <a name="ivmhostinfonetworkadapters-property"></a><span data-ttu-id="4e1a3-106">IVMHostInfo :: NetworkAdapters, propriété</span><span class="sxs-lookup"><span data-stu-id="4e1a3-106">IVMHostInfo::NetworkAdapters property</span></span>

<span data-ttu-id="4e1a3-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="4e1a3-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="4e1a3-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="4e1a3-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="4e1a3-109">Récupère une collection énumérable de cartes réseau sur l’ordinateur hôte.</span><span class="sxs-lookup"><span data-stu-id="4e1a3-109">Retrieves an enumerable collection of NICs in the host machine.</span></span>

<span data-ttu-id="4e1a3-110">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="4e1a3-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="4e1a3-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4e1a3-111">Syntax</span></span>


```C++
HRESULT get_NetworkAdapters(
  [out, retval] VARIANT *hostNICs
);
```



## <a name="property-value"></a><span data-ttu-id="4e1a3-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="4e1a3-112">Property value</span></span>

<span data-ttu-id="4e1a3-113">Collection de cartes d’interface réseau.</span><span class="sxs-lookup"><span data-stu-id="4e1a3-113">A collection of network interface cards.</span></span> <span data-ttu-id="4e1a3-114">Il s’agit d’un tableau de valeurs **BSTR** .</span><span class="sxs-lookup"><span data-stu-id="4e1a3-114">This is an array of **BSTR** values.</span></span>

## <a name="error-codes"></a><span data-ttu-id="4e1a3-115">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="4e1a3-115">Error codes</span></span>



| <span data-ttu-id="4e1a3-116">Nom/valeur</span><span class="sxs-lookup"><span data-stu-id="4e1a3-116">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="4e1a3-117">Signification</span><span class="sxs-lookup"><span data-stu-id="4e1a3-117">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="4e1a3-118"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="4e1a3-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="4e1a3-119">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="4e1a3-119">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="4e1a3-120"><dt>E \_ POINTEUR</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="4e1a3-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="4e1a3-121">Le paramètre a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="4e1a3-121">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="4e1a3-122"><dt>DISP \_ E \_ exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="4e1a3-122"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="4e1a3-123">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="4e1a3-123">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="4e1a3-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4e1a3-124">Requirements</span></span>



| <span data-ttu-id="4e1a3-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4e1a3-125">Requirement</span></span> | <span data-ttu-id="4e1a3-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="4e1a3-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="4e1a3-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4e1a3-127">Minimum supported client</span></span><br/> | <span data-ttu-id="4e1a3-128">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4e1a3-128">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="4e1a3-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4e1a3-129">Minimum supported server</span></span><br/> | <span data-ttu-id="4e1a3-130">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="4e1a3-130">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="4e1a3-131">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="4e1a3-131">End of client support</span></span><br/>    | <span data-ttu-id="4e1a3-132">Windows 7</span><span class="sxs-lookup"><span data-stu-id="4e1a3-132">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="4e1a3-133">Produit</span><span class="sxs-lookup"><span data-stu-id="4e1a3-133">Product</span></span><br/>                  | <span data-ttu-id="4e1a3-134">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="4e1a3-134">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="4e1a3-135">En-tête</span><span class="sxs-lookup"><span data-stu-id="4e1a3-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="4e1a3-136"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="4e1a3-136"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="4e1a3-137">IID</span><span class="sxs-lookup"><span data-stu-id="4e1a3-137">IID</span></span><br/>                      | <span data-ttu-id="4e1a3-138">IID \_ IVMHostInfo est défini en tant que 5b5cf343-05ad-453B-BE99-adf4e27b2ebc</span><span class="sxs-lookup"><span data-stu-id="4e1a3-138">IID\_IVMHostInfo is defined as 5b5cf343-05ad-453b-be99-adf4e27b2ebc</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="4e1a3-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4e1a3-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e1a3-140">**IVMHostInfo**</span><span class="sxs-lookup"><span data-stu-id="4e1a3-140">**IVMHostInfo**</span></span>](ivmhostinfo.md)
</dt> </dl>

 

