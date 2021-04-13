---
title: IVMParallelPortCollection, propriété d’élément (VPCCOMInterfaces. h)
description: Récupère l’objet Port parallèle qui correspond à l’index spécifié.
ms.assetid: f67a4224-ca96-4d68-9f0f-4977ffff859e
keywords:
- Propriété de l’élément Virtual PC
- Propriété d’élément Virtual PC, interface IVMParallelPortCollection
- IVMParallelPortCollection interface Virtual PC, propriété Item
topic_type:
- apiref
api_name:
- IVMParallelPortCollection.Item
- IVMParallelPortCollection.get_Item
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: daa450f1859db8af6ed884b37fc693fc4fb1990f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466626"
---
# <a name="ivmparallelportcollectionitem-property"></a><span data-ttu-id="2aa45-106">IVMParallelPortCollection :: Item, propriété</span><span class="sxs-lookup"><span data-stu-id="2aa45-106">IVMParallelPortCollection::Item property</span></span>

<span data-ttu-id="2aa45-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="2aa45-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="2aa45-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="2aa45-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="2aa45-109">Récupère l’objet Port parallèle qui correspond à l’index spécifié.</span><span class="sxs-lookup"><span data-stu-id="2aa45-109">Retrieves the parallel port object that corresponds to the specified index.</span></span>

<span data-ttu-id="2aa45-110">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="2aa45-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="2aa45-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2aa45-111">Syntax</span></span>


```C++
HRESULT get_Item(
  [in]          long            index,
  [out, retval] IVMParallelPort **vmParallelPort
);
```



## <a name="property-value"></a><span data-ttu-id="2aa45-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="2aa45-112">Property value</span></span>

<span data-ttu-id="2aa45-113">Objet [**IVMParallelPort**](ivmparallelport.md) .</span><span class="sxs-lookup"><span data-stu-id="2aa45-113">The [**IVMParallelPort**](ivmparallelport.md) object.</span></span>

## <a name="error-codes"></a><span data-ttu-id="2aa45-114">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="2aa45-114">Error codes</span></span>



| <span data-ttu-id="2aa45-115">Nom/valeur</span><span class="sxs-lookup"><span data-stu-id="2aa45-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="2aa45-116">Signification</span><span class="sxs-lookup"><span data-stu-id="2aa45-116">Meaning</span></span>                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="2aa45-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="2aa45-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="2aa45-118">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="2aa45-118">The operation was successful.</span></span> <br/>                                                      |
| <dl> <span data-ttu-id="2aa45-119"><dt>E \_ POINTEUR</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="2aa45-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="2aa45-120">Le paramètre *vmParallelPort* a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="2aa45-120">The *vmParallelPort* parameter is **NULL**.</span></span> <br/>                                        |
| <dl> <span data-ttu-id="2aa45-121"><dt>DISP \_ \_BADINDEX</dt> <dt>0x8002000B</dt></span><span class="sxs-lookup"><span data-stu-id="2aa45-121"><dt>DISP\_E\_BADINDEX</dt> <dt>0x8002000B</dt></span></span> </dl>  | <span data-ttu-id="2aa45-122">L’index de l’élément demandé ne correspond pas à un élément de cette collection.</span><span class="sxs-lookup"><span data-stu-id="2aa45-122">The index of the requested item does not correspond to an item in this collection.</span></span> <br/> |
| <dl> <span data-ttu-id="2aa45-123"><dt>Ordinateur virtuel \_ \_Machine virtuelle \_ </dt> <dt>0xA0040207</dt> inconnue</span><span class="sxs-lookup"><span data-stu-id="2aa45-123"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="2aa45-124">La configuration est inconnue.</span><span class="sxs-lookup"><span data-stu-id="2aa45-124">The configuration is unknown.</span></span><br/>                                                       |
| <dl> <span data-ttu-id="2aa45-125"><dt>DISP \_ E \_ exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="2aa45-125"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="2aa45-126">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="2aa45-126">An unexpected error has occurred.</span></span><br/>                                                   |



## <a name="requirements"></a><span data-ttu-id="2aa45-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2aa45-127">Requirements</span></span>



| <span data-ttu-id="2aa45-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2aa45-128">Requirement</span></span> | <span data-ttu-id="2aa45-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="2aa45-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="2aa45-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2aa45-130">Minimum supported client</span></span><br/> | <span data-ttu-id="2aa45-131">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2aa45-131">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="2aa45-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2aa45-132">Minimum supported server</span></span><br/> | <span data-ttu-id="2aa45-133">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="2aa45-133">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="2aa45-134">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="2aa45-134">End of client support</span></span><br/>    | <span data-ttu-id="2aa45-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="2aa45-135">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="2aa45-136">Produit</span><span class="sxs-lookup"><span data-stu-id="2aa45-136">Product</span></span><br/>                  | <span data-ttu-id="2aa45-137">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="2aa45-137">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="2aa45-138">En-tête</span><span class="sxs-lookup"><span data-stu-id="2aa45-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="2aa45-139"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="2aa45-139"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="2aa45-140">IID</span><span class="sxs-lookup"><span data-stu-id="2aa45-140">IID</span></span><br/>                      | <span data-ttu-id="2aa45-141">IID \_ IVMParallelPortCollection est défini en tant que 27c3e036-198f-430c-8735-6e652f7203fd</span><span class="sxs-lookup"><span data-stu-id="2aa45-141">IID\_IVMParallelPortCollection is defined as 27c3e036-198f-430c-8735-6e652f7203fd</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="2aa45-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2aa45-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2aa45-143">**IVMParallelPort**</span><span class="sxs-lookup"><span data-stu-id="2aa45-143">**IVMParallelPort**</span></span>](ivmparallelport.md)
</dt> <dt>

[<span data-ttu-id="2aa45-144">**IVMParallelPortCollection**</span><span class="sxs-lookup"><span data-stu-id="2aa45-144">**IVMParallelPortCollection**</span></span>](ivmparallelportcollection.md)
</dt> </dl>

 

