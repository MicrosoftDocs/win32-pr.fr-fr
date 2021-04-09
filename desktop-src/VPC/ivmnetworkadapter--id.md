---
title: IVMNetworkAdapter _ID, méthode (VPCCOMInterfaces. h)
description: Récupère l’identificateur interne de cette interface réseau.
ms.assetid: 3e71c2cd-1a75-44d9-9a6d-04e6344dfec3
keywords:
- Méthode _ID Virtual PC
- _ID méthode Virtual PC, interface IVMNetworkAdapter
- IVMNetworkAdapter interface Virtual PC, méthode _ID
topic_type:
- apiref
api_name:
- IVMNetworkAdapter._ID
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b9df514d24f9826b58964b4c51c9a76a9ba982e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942253"
---
# <a name="ivmnetworkadapter_id-method"></a><span data-ttu-id="73b10-106">IVMNetworkAdapter :: \_ ID, méthode</span><span class="sxs-lookup"><span data-stu-id="73b10-106">IVMNetworkAdapter::\_ID method</span></span>

<span data-ttu-id="73b10-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="73b10-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="73b10-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="73b10-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="73b10-109">Récupère l’identificateur interne de cette interface réseau.</span><span class="sxs-lookup"><span data-stu-id="73b10-109">Retrieves the internal identifier of this network interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="73b10-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="73b10-110">Syntax</span></span>


```C++
HRESULT _ID(
  [out] long *identifier
);
```



## <a name="parameters"></a><span data-ttu-id="73b10-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="73b10-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="73b10-112">*identificateur* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="73b10-112">*identifier* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="73b10-113">Identificateur interne.</span><span class="sxs-lookup"><span data-stu-id="73b10-113">The internal identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="73b10-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="73b10-114">Return value</span></span>

<span data-ttu-id="73b10-115">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="73b10-115">This method can return one of these values.</span></span>



| <span data-ttu-id="73b10-116">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="73b10-116">Return code/value</span></span>                                                                                                                                                 | <span data-ttu-id="73b10-117">Description</span><span class="sxs-lookup"><span data-stu-id="73b10-117">Description</span></span>                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <span data-ttu-id="73b10-118"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="73b10-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="73b10-119">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="73b10-119">The operation was successful.</span></span><br/>        |
| <dl> <span data-ttu-id="73b10-120"><dt>**E \_ POINTEUR**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="73b10-120"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="73b10-121">Le paramètre a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="73b10-121">The parameter is **NULL**.</span></span><br/>           |
| <dl> <span data-ttu-id="73b10-122"><dt>**Ordinateur virtuel \_ \_Machine virtuelle \_**</dt> <dt>0xA0040207</dt> inconnue</span><span class="sxs-lookup"><span data-stu-id="73b10-122"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="73b10-123">L’ordinateur virtuel est introuvable.</span><span class="sxs-lookup"><span data-stu-id="73b10-123">The virtual machine cannot be found.</span></span><br/> |
| <dl> <span data-ttu-id="73b10-124"><dt>**DISP \_ E \_ exception**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="73b10-124"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="73b10-125">L’opération a rencontré une erreur inconnue.</span><span class="sxs-lookup"><span data-stu-id="73b10-125">The operation had an unknown error.</span></span><br/>  |



 

## <a name="remarks"></a><span data-ttu-id="73b10-126">Notes</span><span class="sxs-lookup"><span data-stu-id="73b10-126">Remarks</span></span>

<span data-ttu-id="73b10-127">Cette méthode n’est pas utilisable par les langages de script.</span><span class="sxs-lookup"><span data-stu-id="73b10-127">This method is not usable by scripting languages.</span></span>

## <a name="requirements"></a><span data-ttu-id="73b10-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="73b10-128">Requirements</span></span>



| <span data-ttu-id="73b10-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="73b10-129">Requirement</span></span> | <span data-ttu-id="73b10-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="73b10-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="73b10-131">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="73b10-131">Minimum supported client</span></span><br/> | <span data-ttu-id="73b10-132">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="73b10-132">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="73b10-133">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="73b10-133">Minimum supported server</span></span><br/> | <span data-ttu-id="73b10-134">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="73b10-134">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="73b10-135">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="73b10-135">End of client support</span></span><br/>    | <span data-ttu-id="73b10-136">Windows 7</span><span class="sxs-lookup"><span data-stu-id="73b10-136">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="73b10-137">Produit</span><span class="sxs-lookup"><span data-stu-id="73b10-137">Product</span></span><br/>                  | <span data-ttu-id="73b10-138">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="73b10-138">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="73b10-139">En-tête</span><span class="sxs-lookup"><span data-stu-id="73b10-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="73b10-140"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="73b10-140"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="73b10-141">IID</span><span class="sxs-lookup"><span data-stu-id="73b10-141">IID</span></span><br/>                      | <span data-ttu-id="73b10-142">IID \_ IVMNetworkAdapter est défini en tant que e32e4165-22b8-4DC0-8d57-850171ae207a</span><span class="sxs-lookup"><span data-stu-id="73b10-142">IID\_IVMNetworkAdapter is defined as e32e4165-22b8-4dc0-8d57-850171ae207a</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="73b10-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="73b10-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73b10-144">**IVMNetworkAdapter**</span><span class="sxs-lookup"><span data-stu-id="73b10-144">**IVMNetworkAdapter**</span></span>](ivmnetworkadapter.md)
</dt> </dl>

 

