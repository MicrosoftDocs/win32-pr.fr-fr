---
title: Méthode IVMDVDDriveEvents OnMediaInsert (VPCCOMInterfaces. h)
description: Reçoit une notification indiquant que le média a été inséré dans le lecteur. | Méthode IVMDVDDriveEvents OnMediaInsert (VPCCOMInterfaces. h)
ms.assetid: a246e2dd-638e-4d2f-9089-74771cd8bb2b
keywords:
- Méthode OnMediaInsert Virtual PC
- Méthode OnMediaInsert Virtual PC, interface IVMDVDDriveEvents
- IVMDVDDriveEvents interface Virtual PC, méthode OnMediaInsert
topic_type:
- apiref
api_name:
- IVMDVDDriveEvents.OnMediaInsert
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 883f7990de17a9d1dbb21db9651e0f5ad4ec74aa
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "103953558"
---
# <a name="ivmdvddriveeventsonmediainsert-method"></a><span data-ttu-id="56bfd-107">IVMDVDDriveEvents :: OnMediaInsert, méthode</span><span class="sxs-lookup"><span data-stu-id="56bfd-107">IVMDVDDriveEvents::OnMediaInsert method</span></span>

<span data-ttu-id="56bfd-108">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="56bfd-108">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="56bfd-109">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="56bfd-109">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="56bfd-110">Reçoit une notification indiquant que le média a été inséré dans le lecteur.</span><span class="sxs-lookup"><span data-stu-id="56bfd-110">Receives notification that media has been inserted into the drive.</span></span>

## <a name="syntax"></a><span data-ttu-id="56bfd-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="56bfd-111">Syntax</span></span>


```C++
HRESULT OnMediaInsert(
  [in] BSTR mediaPath
);
```



## <a name="parameters"></a><span data-ttu-id="56bfd-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="56bfd-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="56bfd-113">*mediaPath* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="56bfd-113">*mediaPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="56bfd-114">Lettre de lecteur hôte, ou chemin d’accès, à l’image ISO.</span><span class="sxs-lookup"><span data-stu-id="56bfd-114">The host drive letter, or path, to the ISO image.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="56bfd-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="56bfd-115">Return value</span></span>

<span data-ttu-id="56bfd-116">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="56bfd-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="56bfd-117">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="56bfd-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="56bfd-118">Notes</span><span class="sxs-lookup"><span data-stu-id="56bfd-118">Remarks</span></span>

<span data-ttu-id="56bfd-119">Cette méthode est appelée lorsque le média (une image ISO ou un disque d’un lecteur hôte) est inséré.</span><span class="sxs-lookup"><span data-stu-id="56bfd-119">This method is called when media (an ISO image or a disc in a host drive) is inserted.</span></span> <span data-ttu-id="56bfd-120">Le programme client doit implémenter cette méthode d’interface pour recevoir la notification de l' \_ événement vmDVDDriveEvent OnInsert provenant de [**IVMDVDDrive**](ivmdvddrive.md).</span><span class="sxs-lookup"><span data-stu-id="56bfd-120">The client program must implement this interface method to receive notification of the vmDVDDriveEvent\_OnInsert event originating from [**IVMDVDDrive**](ivmdvddrive.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="56bfd-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="56bfd-121">Requirements</span></span>



| <span data-ttu-id="56bfd-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="56bfd-122">Requirement</span></span> | <span data-ttu-id="56bfd-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="56bfd-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="56bfd-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="56bfd-124">Minimum supported client</span></span><br/> | <span data-ttu-id="56bfd-125">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="56bfd-125">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="56bfd-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="56bfd-126">Minimum supported server</span></span><br/> | <span data-ttu-id="56bfd-127">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="56bfd-127">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="56bfd-128">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="56bfd-128">End of client support</span></span><br/>    | <span data-ttu-id="56bfd-129">Windows 7</span><span class="sxs-lookup"><span data-stu-id="56bfd-129">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="56bfd-130">Produit</span><span class="sxs-lookup"><span data-stu-id="56bfd-130">Product</span></span><br/>                  | <span data-ttu-id="56bfd-131">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="56bfd-131">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="56bfd-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="56bfd-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="56bfd-133"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="56bfd-133"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="56bfd-134">IID</span><span class="sxs-lookup"><span data-stu-id="56bfd-134">IID</span></span><br/>                      | <span data-ttu-id="56bfd-135">DIID \_ IVMDVDDriveEvents est défini comme c2a7d8e9-E76C-4EB8-94f7-71a5122d249b</span><span class="sxs-lookup"><span data-stu-id="56bfd-135">DIID\_IVMDVDDriveEvents is defined as c2a7d8e9-e76c-4eb8-94f7-71a5122d249b</span></span><br/>         |



## <a name="see-also"></a><span data-ttu-id="56bfd-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="56bfd-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56bfd-137">**IVMDVDDriveEvents**</span><span class="sxs-lookup"><span data-stu-id="56bfd-137">**IVMDVDDriveEvents**</span></span>](ivmdvddriveevents.md)
</dt> </dl>

 

