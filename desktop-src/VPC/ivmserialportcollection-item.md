---
title: IVMSerialPortCollection, propriété d’élément (VPCCOMInterfaces. h)
description: Récupère l’objet de port série qui correspond à l’index spécifié.
ms.assetid: 24ce1404-d7aa-4125-b1f9-9c54418ea205
keywords:
- Propriété de l’élément Virtual PC
- Propriété d’élément Virtual PC, interface IVMSerialPortCollection
- IVMSerialPortCollection interface Virtual PC, propriété Item
topic_type:
- apiref
api_name:
- IVMSerialPortCollection.Item
- IVMSerialPortCollection.get_Item
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be44cc92507954848c369273ae27de49df8d0ad8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106509531"
---
# <a name="ivmserialportcollectionitem-property"></a><span data-ttu-id="a9fcd-106">IVMSerialPortCollection :: Item, propriété</span><span class="sxs-lookup"><span data-stu-id="a9fcd-106">IVMSerialPortCollection::Item property</span></span>

<span data-ttu-id="a9fcd-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="a9fcd-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="a9fcd-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="a9fcd-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="a9fcd-109">Récupère l’objet de port série qui correspond à l’index spécifié.</span><span class="sxs-lookup"><span data-stu-id="a9fcd-109">Retrieves the serial port object that corresponds to the specified index.</span></span>

<span data-ttu-id="a9fcd-110">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="a9fcd-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="a9fcd-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a9fcd-111">Syntax</span></span>


```C++
HRESULT get_Item(
  [in]          long          index,
  [out, retval] IVMSerialPort **serialPort
);
```



## <a name="property-value"></a><span data-ttu-id="a9fcd-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="a9fcd-112">Property value</span></span>

<span data-ttu-id="a9fcd-113">Objet [**IVMSerialPort**](ivmserialport.md) .</span><span class="sxs-lookup"><span data-stu-id="a9fcd-113">The [**IVMSerialPort**](ivmserialport.md) object.</span></span>

## <a name="error-codes"></a><span data-ttu-id="a9fcd-114">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="a9fcd-114">Error codes</span></span>



| <span data-ttu-id="a9fcd-115">Nom/valeur</span><span class="sxs-lookup"><span data-stu-id="a9fcd-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="a9fcd-116">Signification</span><span class="sxs-lookup"><span data-stu-id="a9fcd-116">Meaning</span></span>                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="a9fcd-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="a9fcd-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="a9fcd-118">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="a9fcd-118">The operation was successful.</span></span> <br/>                                                      |
| <dl> <span data-ttu-id="a9fcd-119"><dt>E \_ POINTEUR</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="a9fcd-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="a9fcd-120">Le paramètre *serialPort* a la valeur null.</span><span class="sxs-lookup"><span data-stu-id="a9fcd-120">The *serialPort* parameter is NULL.</span></span> <br/>                                                |
| <dl> <span data-ttu-id="a9fcd-121"><dt>DISP \_ \_BADINDEX</dt> <dt>0x8002000B</dt></span><span class="sxs-lookup"><span data-stu-id="a9fcd-121"><dt>DISP\_E\_BADINDEX</dt> <dt>0x8002000B</dt></span></span> </dl>  | <span data-ttu-id="a9fcd-122">L’index de l’élément demandé ne correspond pas à un élément de cette collection.</span><span class="sxs-lookup"><span data-stu-id="a9fcd-122">The index of the requested item does not correspond to an item in this collection.</span></span> <br/> |
| <dl> <span data-ttu-id="a9fcd-123"><dt>Ordinateur virtuel \_ \_Machine virtuelle \_ </dt> <dt>0xA0040207</dt> inconnue</span><span class="sxs-lookup"><span data-stu-id="a9fcd-123"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="a9fcd-124">La configuration est inconnue.</span><span class="sxs-lookup"><span data-stu-id="a9fcd-124">The configuration is unknown.</span></span><br/>                                                       |
| <dl> <span data-ttu-id="a9fcd-125"><dt>DISP \_ E \_ exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="a9fcd-125"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="a9fcd-126">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="a9fcd-126">An unexpected error has occurred.</span></span><br/>                                                   |



## <a name="requirements"></a><span data-ttu-id="a9fcd-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a9fcd-127">Requirements</span></span>



| <span data-ttu-id="a9fcd-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a9fcd-128">Requirement</span></span> | <span data-ttu-id="a9fcd-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="a9fcd-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="a9fcd-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a9fcd-130">Minimum supported client</span></span><br/> | <span data-ttu-id="a9fcd-131">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a9fcd-131">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a9fcd-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a9fcd-132">Minimum supported server</span></span><br/> | <span data-ttu-id="a9fcd-133">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="a9fcd-133">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="a9fcd-134">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="a9fcd-134">End of client support</span></span><br/>    | <span data-ttu-id="a9fcd-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="a9fcd-135">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="a9fcd-136">Produit</span><span class="sxs-lookup"><span data-stu-id="a9fcd-136">Product</span></span><br/>                  | <span data-ttu-id="a9fcd-137">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="a9fcd-137">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="a9fcd-138">En-tête</span><span class="sxs-lookup"><span data-stu-id="a9fcd-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="a9fcd-139"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="a9fcd-139"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="a9fcd-140">IID</span><span class="sxs-lookup"><span data-stu-id="a9fcd-140">IID</span></span><br/>                      | <span data-ttu-id="a9fcd-141">IID \_ IVMSerialPortCollection est défini en tant que dd3c6175-1f04-4341-9f85-104074880289</span><span class="sxs-lookup"><span data-stu-id="a9fcd-141">IID\_IVMSerialPortCollection is defined as dd3c6175-1f04-4341-9f85-104074880289</span></span><br/>    |



## <a name="see-also"></a><span data-ttu-id="a9fcd-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a9fcd-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9fcd-143">**IVMSerialPort**</span><span class="sxs-lookup"><span data-stu-id="a9fcd-143">**IVMSerialPort**</span></span>](ivmserialport.md)
</dt> <dt>

[<span data-ttu-id="a9fcd-144">**IVMSerialPortCollection**</span><span class="sxs-lookup"><span data-stu-id="a9fcd-144">**IVMSerialPortCollection**</span></span>](ivmserialportcollection.md)
</dt> </dl>

 

