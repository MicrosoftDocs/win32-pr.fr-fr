---
title: IVMMouse UsingAbsoluteCoordinates, propriété (VPCCOMInterfaces. h)
description: Récupère si les coordonnées de la souris représentent des coordonnées absolues ou relatives.
ms.assetid: 668278f8-28ae-4128-9653-4985bddbe184
keywords:
- UsingAbsoluteCoordinates propriété Virtual PC
- UsingAbsoluteCoordinates, propriété Virtual PC, IVMMouse, interface
- IVMMouse interface Virtual PC, propriété UsingAbsoluteCoordinates
topic_type:
- apiref
api_name:
- IVMMouse.UsingAbsoluteCoordinates
- IVMMouse.get_UsingAbsoluteCoordinates
- IVMMouse.put_UsingAbsoluteCoordinates
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc216466ab8ef0483d3c1a229f6a493d4ba913dd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509198"
---
# <a name="ivmmouseusingabsolutecoordinates-property"></a><span data-ttu-id="0209b-106">IVMMouse :: UsingAbsoluteCoordinates, propriété</span><span class="sxs-lookup"><span data-stu-id="0209b-106">IVMMouse::UsingAbsoluteCoordinates property</span></span>

<span data-ttu-id="0209b-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="0209b-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="0209b-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="0209b-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="0209b-109">Récupère si les coordonnées de la souris représentent des coordonnées absolues ou relatives.</span><span class="sxs-lookup"><span data-stu-id="0209b-109">Retrieves whether mouse coordinates represent absolute or relative coordinates.</span></span>

<span data-ttu-id="0209b-110">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="0209b-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="0209b-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0209b-111">Syntax</span></span>


```C++
HRESULT put_UsingAbsoluteCoordinates(
  [in]          VARIANT_BOOL usingAbsoluteCoordinates
);

HRESULT get_UsingAbsoluteCoordinates(
  [out, retval] VARIANT_BOOL *usingAbsoluteCoordinates
);
```



## <a name="property-value"></a><span data-ttu-id="0209b-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="0209b-112">Property value</span></span>

<span data-ttu-id="0209b-113">**Variante \_ TRUE** pour configurer le périphérique de la souris pour qu’il utilise des coordonnées absolues, la **\_ valeur variant false** pour utiliser des coordonnées relatives.</span><span class="sxs-lookup"><span data-stu-id="0209b-113">**VARIANT\_TRUE** to set the mouse device to use absolute coordinates, **VARIANT\_FALSE** to use relative coordinates.</span></span>

## <a name="error-codes"></a><span data-ttu-id="0209b-114">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="0209b-114">Error codes</span></span>



| <span data-ttu-id="0209b-115">Nom/valeur</span><span class="sxs-lookup"><span data-stu-id="0209b-115">Name/value</span></span>                                                                                                                                                                       | <span data-ttu-id="0209b-116">Signification</span><span class="sxs-lookup"><span data-stu-id="0209b-116">Meaning</span></span>                                                                                                               |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="0209b-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="0209b-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                          | <span data-ttu-id="0209b-118">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="0209b-118">The operation was successful.</span></span><br/>                                                                              |
| <dl> <span data-ttu-id="0209b-119"><dt>E \_ POINTEUR</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="0209b-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                            | <span data-ttu-id="0209b-120">Le paramètre a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="0209b-120">The parameter is **NULL**.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="0209b-121"><dt>Ordinateur virtuel \_ \_Machine virtuelle \_ non \_ exécutée</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="0209b-121"><dt>VM\_E\_VM\_NOT\_RUNNING</dt> <dt>0xA0040206</dt></span></span> </dl>               | <span data-ttu-id="0209b-122">L’ordinateur virtuel auquel ce périphérique de souris est attaché n’est pas en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="0209b-122">The virtual machine to which this mouse device is attached is not currently running.</span></span><br/>                       |
| <dl> <span data-ttu-id="0209b-123"><dt>Ordinateur virtuel \_ La \_ fonctionnalité d’ajouts E \_ \_ n’est pas disponible \_ </dt> <dt>0xA0040505</dt></span><span class="sxs-lookup"><span data-stu-id="0209b-123"><dt>VM\_E\_ADDITIONS\_FEATURE\_NOT\_AVAIL</dt> <dt>0xA0040505</dt></span></span> </dl> | <span data-ttu-id="0209b-124">Les composants d’intégration ne sont pas installés.</span><span class="sxs-lookup"><span data-stu-id="0209b-124">Integration components are not installed.</span></span> <span data-ttu-id="0209b-125">Les composants d’intégration sont requis pour utiliser des coordonnées absolues.</span><span class="sxs-lookup"><span data-stu-id="0209b-125">Integration components are required to use absolute coordinates.</span></span><br/> |
| <dl> <span data-ttu-id="0209b-126"><dt>DISP \_ E \_ exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="0209b-126"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                    | <span data-ttu-id="0209b-127">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="0209b-127">An unexpected error has occurred.</span></span><br/>                                                                          |



## <a name="remarks"></a><span data-ttu-id="0209b-128">Notes</span><span class="sxs-lookup"><span data-stu-id="0209b-128">Remarks</span></span>

<span data-ttu-id="0209b-129">Cette propriété est locale uniquement à cet objet et prend par défaut **la \_ valeur false** pour un nouvel objet [**IVMMouse**](ivmmouse.md) .</span><span class="sxs-lookup"><span data-stu-id="0209b-129">This property is local only to this object and will default to **VARIANT\_FALSE** for a new [**IVMMouse**](ivmmouse.md) object.</span></span> <span data-ttu-id="0209b-130">Notez que les composants d’intégration doivent être installés pour pouvoir utiliser des coordonnées absolues.</span><span class="sxs-lookup"><span data-stu-id="0209b-130">Note that integration components must be installed in order to use absolute coordinates.</span></span>

## <a name="requirements"></a><span data-ttu-id="0209b-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0209b-131">Requirements</span></span>



| <span data-ttu-id="0209b-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0209b-132">Requirement</span></span> | <span data-ttu-id="0209b-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="0209b-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="0209b-134">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0209b-134">Minimum supported client</span></span><br/> | <span data-ttu-id="0209b-135">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0209b-135">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="0209b-136">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0209b-136">Minimum supported server</span></span><br/> | <span data-ttu-id="0209b-137">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="0209b-137">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="0209b-138">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="0209b-138">End of client support</span></span><br/>    | <span data-ttu-id="0209b-139">Windows 7</span><span class="sxs-lookup"><span data-stu-id="0209b-139">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="0209b-140">Produit</span><span class="sxs-lookup"><span data-stu-id="0209b-140">Product</span></span><br/>                  | <span data-ttu-id="0209b-141">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="0209b-141">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="0209b-142">En-tête</span><span class="sxs-lookup"><span data-stu-id="0209b-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="0209b-143"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="0209b-143"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="0209b-144">IID</span><span class="sxs-lookup"><span data-stu-id="0209b-144">IID</span></span><br/>                      | <span data-ttu-id="0209b-145">IID \_ IVMmouse est défini en tant que ac903f6d-6346-4f29-8875-5d511a13895e</span><span class="sxs-lookup"><span data-stu-id="0209b-145">IID\_IVMmouse is defined as ac903f6d-6346-4f29-8875-5d511a13895e</span></span><br/>                   |



## <a name="see-also"></a><span data-ttu-id="0209b-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0209b-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0209b-147">**IVMMouse**</span><span class="sxs-lookup"><span data-stu-id="0209b-147">**IVMMouse**</span></span>](ivmmouse.md)
</dt> </dl>

 

