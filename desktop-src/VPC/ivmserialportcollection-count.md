---
title: Propriété Count IVMSerialPortCollection (VPCCOMInterfaces. h)
description: Récupère le nombre de ports série de cette collection.
ms.assetid: 94ff6c9d-17bc-4aa5-a486-d4428c829d02
keywords:
- Propriété Count Virtual PC
- Propriété Count Virtual PC, IVMSerialPortCollection, interface
- IVMSerialPortCollection interface Virtual PC, propriété Count
topic_type:
- apiref
api_name:
- IVMSerialPortCollection.Count
- IVMSerialPortCollection.get_Count
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bbf0503f00fd1df7d27a8eeafedd3efe42619b98
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843834"
---
# <a name="ivmserialportcollectioncount-property"></a><span data-ttu-id="a588d-106">IVMSerialPortCollection :: Count, propriété</span><span class="sxs-lookup"><span data-stu-id="a588d-106">IVMSerialPortCollection::Count property</span></span>

<span data-ttu-id="a588d-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="a588d-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="a588d-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="a588d-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="a588d-109">Récupère le nombre de ports série de cette collection.</span><span class="sxs-lookup"><span data-stu-id="a588d-109">Retrieves the number of serial ports in this collection.</span></span>

<span data-ttu-id="a588d-110">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="a588d-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="a588d-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a588d-111">Syntax</span></span>


```C++
HRESULT get_Count(
  [out, retval] long *count
);
```



## <a name="property-value"></a><span data-ttu-id="a588d-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="a588d-112">Property value</span></span>

<span data-ttu-id="a588d-113">Nombre de ports série.</span><span class="sxs-lookup"><span data-stu-id="a588d-113">The number of serial ports.</span></span>

## <a name="error-codes"></a><span data-ttu-id="a588d-114">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="a588d-114">Error codes</span></span>



| <span data-ttu-id="a588d-115">Nom/valeur</span><span class="sxs-lookup"><span data-stu-id="a588d-115">Name/value</span></span>                                                                                                                                            | <span data-ttu-id="a588d-116">Signification</span><span class="sxs-lookup"><span data-stu-id="a588d-116">Meaning</span></span>                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------|
| <dl> <span data-ttu-id="a588d-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="a588d-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>               | <span data-ttu-id="a588d-118">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="a588d-118">The operation was successful.</span></span><br/> |
| <dl> <span data-ttu-id="a588d-119"><dt>E \_ POINTEUR</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="a588d-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl> | <span data-ttu-id="a588d-120">Le paramètre a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="a588d-120">The parameter is **NULL**.</span></span><br/>    |



## <a name="requirements"></a><span data-ttu-id="a588d-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a588d-121">Requirements</span></span>



| <span data-ttu-id="a588d-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a588d-122">Requirement</span></span> | <span data-ttu-id="a588d-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="a588d-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="a588d-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a588d-124">Minimum supported client</span></span><br/> | <span data-ttu-id="a588d-125">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a588d-125">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a588d-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a588d-126">Minimum supported server</span></span><br/> | <span data-ttu-id="a588d-127">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="a588d-127">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="a588d-128">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="a588d-128">End of client support</span></span><br/>    | <span data-ttu-id="a588d-129">Windows 7</span><span class="sxs-lookup"><span data-stu-id="a588d-129">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="a588d-130">Produit</span><span class="sxs-lookup"><span data-stu-id="a588d-130">Product</span></span><br/>                  | <span data-ttu-id="a588d-131">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="a588d-131">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="a588d-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="a588d-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="a588d-133"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="a588d-133"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="a588d-134">IID</span><span class="sxs-lookup"><span data-stu-id="a588d-134">IID</span></span><br/>                      | <span data-ttu-id="a588d-135">IID \_ IVMSerialPortCollection est défini en tant que dd3c6175-1f04-4341-9f85-104074880289</span><span class="sxs-lookup"><span data-stu-id="a588d-135">IID\_IVMSerialPortCollection is defined as dd3c6175-1f04-4341-9f85-104074880289</span></span><br/>    |



## <a name="see-also"></a><span data-ttu-id="a588d-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a588d-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a588d-137">**IVMSerialPortCollection**</span><span class="sxs-lookup"><span data-stu-id="a588d-137">**IVMSerialPortCollection**</span></span>](ivmserialportcollection.md)
</dt> </dl>

 

