---
title: IVMFloppyDriveCollection, propriété d’élément (VPCCOMInterfaces. h)
description: Objet Floppy qui correspond à l’index spécifié.
ms.assetid: 068a1f1c-ae84-4689-b68a-ce25b68fc06b
keywords:
- Propriété de l’élément Virtual PC
- Propriété d’élément Virtual PC, interface IVMFloppyDriveCollection
- IVMFloppyDriveCollection interface Virtual PC, propriété Item
topic_type:
- apiref
api_name:
- IVMFloppyDriveCollection.Item
- IVMFloppyDriveCollection.get_Item
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 315eaea13699d78a75457f39c6c915b30fa2fa9c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106063"
---
# <a name="ivmfloppydrivecollectionitem-property"></a><span data-ttu-id="3a47b-106">IVMFloppyDriveCollection :: Item, propriété</span><span class="sxs-lookup"><span data-stu-id="3a47b-106">IVMFloppyDriveCollection::Item property</span></span>

<span data-ttu-id="3a47b-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="3a47b-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="3a47b-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="3a47b-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="3a47b-109">Récupère l’objet Floppy qui correspond à l’index spécifié.</span><span class="sxs-lookup"><span data-stu-id="3a47b-109">Retrieves the floppy object that corresponds to the specified index.</span></span>

<span data-ttu-id="3a47b-110">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="3a47b-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="3a47b-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3a47b-111">Syntax</span></span>


```C++
HRESULT get_Item(
  [in]          long           index,
  [out, retval] IVMFloppyDrive **floppyDrive
);
```



## <a name="property-value"></a><span data-ttu-id="3a47b-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="3a47b-112">Property value</span></span>

<span data-ttu-id="3a47b-113">Objet [**IVMFloppyDrive**](ivmfloppydrive.md) .</span><span class="sxs-lookup"><span data-stu-id="3a47b-113">The [**IVMFloppyDrive**](ivmfloppydrive.md) object.</span></span>

## <a name="error-codes"></a><span data-ttu-id="3a47b-114">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="3a47b-114">Error codes</span></span>



| <span data-ttu-id="3a47b-115">Nom/valeur</span><span class="sxs-lookup"><span data-stu-id="3a47b-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="3a47b-116">Signification</span><span class="sxs-lookup"><span data-stu-id="3a47b-116">Meaning</span></span>                                                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="3a47b-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="3a47b-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="3a47b-118">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="3a47b-118">The operation was successful.</span></span><br/>                                                      |
| <dl> <span data-ttu-id="3a47b-119"><dt>E \_ POINTEUR</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="3a47b-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="3a47b-120">Le paramètre *floppyDrive* a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="3a47b-120">The *floppyDrive* parameter is **NULL**.</span></span><br/>                                           |
| <dl> <span data-ttu-id="3a47b-121"><dt>DISP \_ \_BADINDEX</dt> <dt>0x8002000B</dt></span><span class="sxs-lookup"><span data-stu-id="3a47b-121"><dt>DISP\_E\_BADINDEX</dt> <dt>0x8002000B</dt></span></span> </dl>  | <span data-ttu-id="3a47b-122">L’index de l’élément demandé ne correspond pas à un élément de cette collection.</span><span class="sxs-lookup"><span data-stu-id="3a47b-122">The index of the requested item does not correspond to an item in this collection.</span></span><br/> |
| <dl> <span data-ttu-id="3a47b-123"><dt>Ordinateur virtuel \_ \_Machine virtuelle \_ </dt> <dt>0xA0040207</dt> inconnue</span><span class="sxs-lookup"><span data-stu-id="3a47b-123"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="3a47b-124">La configuration est inconnue.</span><span class="sxs-lookup"><span data-stu-id="3a47b-124">The configuration is unknown.</span></span><br/>                                                      |
| <dl> <span data-ttu-id="3a47b-125"><dt>DISP \_ E \_ exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="3a47b-125"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="3a47b-126">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="3a47b-126">An unexpected error has occurred.</span></span><br/>                                                  |



## <a name="requirements"></a><span data-ttu-id="3a47b-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3a47b-127">Requirements</span></span>



| <span data-ttu-id="3a47b-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3a47b-128">Requirement</span></span> | <span data-ttu-id="3a47b-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="3a47b-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="3a47b-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3a47b-130">Minimum supported client</span></span><br/> | <span data-ttu-id="3a47b-131">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3a47b-131">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3a47b-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3a47b-132">Minimum supported server</span></span><br/> | <span data-ttu-id="3a47b-133">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="3a47b-133">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="3a47b-134">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="3a47b-134">End of client support</span></span><br/>    | <span data-ttu-id="3a47b-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="3a47b-135">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="3a47b-136">Produit</span><span class="sxs-lookup"><span data-stu-id="3a47b-136">Product</span></span><br/>                  | <span data-ttu-id="3a47b-137">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="3a47b-137">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="3a47b-138">En-tête</span><span class="sxs-lookup"><span data-stu-id="3a47b-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="3a47b-139"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="3a47b-139"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="3a47b-140">IID</span><span class="sxs-lookup"><span data-stu-id="3a47b-140">IID</span></span><br/>                      | <span data-ttu-id="3a47b-141">IID \_ IVMFloppyDriveCollection est défini en tant que 8ba70a25-F698-4EE5-85ce-3cc93a925516</span><span class="sxs-lookup"><span data-stu-id="3a47b-141">IID\_IVMFloppyDriveCollection is defined as 8ba70a25-f698-4ee5-85ce-3cc93a925516</span></span><br/>   |



## <a name="see-also"></a><span data-ttu-id="3a47b-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3a47b-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a47b-143">**IVMFloppyDrive**</span><span class="sxs-lookup"><span data-stu-id="3a47b-143">**IVMFloppyDrive**</span></span>](ivmfloppydrive.md)
</dt> <dt>

[<span data-ttu-id="3a47b-144">**IVMFloppyDriveCollection**</span><span class="sxs-lookup"><span data-stu-id="3a47b-144">**IVMFloppyDriveCollection**</span></span>](ivmfloppydrivecollection.md)
</dt> </dl>

 

