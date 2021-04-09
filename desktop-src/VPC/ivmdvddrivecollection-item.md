---
title: IVMDVDDriveCollection, propriété d’élément (VPCCOMInterfaces. h)
description: Récupère l’objet lecteur CD ou DVD qui correspond à l’index spécifié.
ms.assetid: ecc94eea-9ddc-46c8-87e2-e67aca83eecc
keywords:
- Propriété de l’élément Virtual PC
- Propriété d’élément Virtual PC, interface IVMDVDDriveCollection
- IVMDVDDriveCollection interface Virtual PC, propriété Item
topic_type:
- apiref
api_name:
- IVMDVDDriveCollection.Item
- IVMDVDDriveCollection.get_Item
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8cc631ab6d4de3ab65071bf2b8692236f3ae03ee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032820"
---
# <a name="ivmdvddrivecollectionitem-property"></a><span data-ttu-id="6d1aa-106">IVMDVDDriveCollection :: Item, propriété</span><span class="sxs-lookup"><span data-stu-id="6d1aa-106">IVMDVDDriveCollection::Item property</span></span>

<span data-ttu-id="6d1aa-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="6d1aa-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="6d1aa-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="6d1aa-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="6d1aa-109">Récupère l’objet lecteur CD ou DVD qui correspond à l’index spécifié.</span><span class="sxs-lookup"><span data-stu-id="6d1aa-109">Retrieves the CD or DVD drive object that corresponds to the specified index.</span></span>

<span data-ttu-id="6d1aa-110">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="6d1aa-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="6d1aa-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6d1aa-111">Syntax</span></span>


```C++
HRESULT get_Item(
  [in]          long        index,
  [out, retval] IVMDVDDrive **dvdDrive
);
```



## <a name="property-value"></a><span data-ttu-id="6d1aa-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="6d1aa-112">Property value</span></span>

<span data-ttu-id="6d1aa-113">Objet [**IVMDVDDrive**](ivmdvddrive.md) .</span><span class="sxs-lookup"><span data-stu-id="6d1aa-113">The [**IVMDVDDrive**](ivmdvddrive.md) object.</span></span>

## <a name="error-codes"></a><span data-ttu-id="6d1aa-114">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="6d1aa-114">Error codes</span></span>



| <span data-ttu-id="6d1aa-115">Nom/valeur</span><span class="sxs-lookup"><span data-stu-id="6d1aa-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="6d1aa-116">Signification</span><span class="sxs-lookup"><span data-stu-id="6d1aa-116">Meaning</span></span>                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="6d1aa-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="6d1aa-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="6d1aa-118">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="6d1aa-118">The operation was successful.</span></span> <br/>                                                      |
| <dl> <span data-ttu-id="6d1aa-119"><dt>E \_ POINTEUR</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="6d1aa-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="6d1aa-120">Le paramètre a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="6d1aa-120">The parameter is **NULL**.</span></span><br/>                                                          |
| <dl> <span data-ttu-id="6d1aa-121"><dt>E \_ ÉCHEC</dt> <dt>0x80004005</dt></span><span class="sxs-lookup"><span data-stu-id="6d1aa-121"><dt>E\_FAIL</dt> <dt>0x80004005</dt></span></span> </dl>            | <span data-ttu-id="6d1aa-122">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="6d1aa-122">An unexpected error has occurred.</span></span><br/>                                                   |
| <dl> <span data-ttu-id="6d1aa-123"><dt>DISP \_ \_BADINDEX</dt> <dt>0x8002000B</dt></span><span class="sxs-lookup"><span data-stu-id="6d1aa-123"><dt>DISP\_E\_BADINDEX</dt> <dt>0x8002000B</dt></span></span> </dl>  | <span data-ttu-id="6d1aa-124">L’index de l’élément demandé ne correspond pas à un élément de cette collection.</span><span class="sxs-lookup"><span data-stu-id="6d1aa-124">The index of the requested item does not correspond to an item in this collection.</span></span> <br/> |
| <dl> <span data-ttu-id="6d1aa-125"><dt>Ordinateur virtuel \_ \_Machine virtuelle \_ </dt> <dt>0xA0040207</dt> inconnue</span><span class="sxs-lookup"><span data-stu-id="6d1aa-125"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="6d1aa-126">La configuration est inconnue.</span><span class="sxs-lookup"><span data-stu-id="6d1aa-126">The configuration is unknown.</span></span><br/>                                                       |
| <dl> <span data-ttu-id="6d1aa-127"><dt>DISP \_ E \_ exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="6d1aa-127"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="6d1aa-128">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="6d1aa-128">An unexpected error has occurred.</span></span><br/>                                                   |



## <a name="requirements"></a><span data-ttu-id="6d1aa-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6d1aa-129">Requirements</span></span>



| <span data-ttu-id="6d1aa-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6d1aa-130">Requirement</span></span> | <span data-ttu-id="6d1aa-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="6d1aa-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="6d1aa-132">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6d1aa-132">Minimum supported client</span></span><br/> | <span data-ttu-id="6d1aa-133">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6d1aa-133">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="6d1aa-134">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6d1aa-134">Minimum supported server</span></span><br/> | <span data-ttu-id="6d1aa-135">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="6d1aa-135">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="6d1aa-136">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="6d1aa-136">End of client support</span></span><br/>    | <span data-ttu-id="6d1aa-137">Windows 7</span><span class="sxs-lookup"><span data-stu-id="6d1aa-137">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="6d1aa-138">Produit</span><span class="sxs-lookup"><span data-stu-id="6d1aa-138">Product</span></span><br/>                  | <span data-ttu-id="6d1aa-139">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="6d1aa-139">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="6d1aa-140">En-tête</span><span class="sxs-lookup"><span data-stu-id="6d1aa-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="6d1aa-141"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="6d1aa-141"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="6d1aa-142">IID</span><span class="sxs-lookup"><span data-stu-id="6d1aa-142">IID</span></span><br/>                      | <span data-ttu-id="6d1aa-143">IID \_ IVMDVDDriveCollection est défini en tant que bc86e297-e55f-4742-9614-ad11d3131f68</span><span class="sxs-lookup"><span data-stu-id="6d1aa-143">IID\_IVMDVDDriveCollection is defined as bc86e297-e55f-4742-9614-ad11d3131f68</span></span><br/>      |



## <a name="see-also"></a><span data-ttu-id="6d1aa-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6d1aa-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d1aa-145">**IVMDVDDrive**</span><span class="sxs-lookup"><span data-stu-id="6d1aa-145">**IVMDVDDrive**</span></span>](ivmdvddrive.md)
</dt> <dt>

[<span data-ttu-id="6d1aa-146">**IVMDVDDriveCollection**</span><span class="sxs-lookup"><span data-stu-id="6d1aa-146">**IVMDVDDriveCollection**</span></span>](ivmdvddrivecollection.md)
</dt> </dl>

 

