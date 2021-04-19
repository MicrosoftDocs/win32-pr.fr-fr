---
title: Méthode IVMFloppyDriveEvents OnMediaInsert (VPCCOMInterfaces. h)
description: Reçoit une notification indiquant que le média a été inséré dans le lecteur. | Méthode IVMFloppyDriveEvents OnMediaInsert (VPCCOMInterfaces. h)
ms.assetid: 922fca14-8ef6-4d3d-b1b6-72d2ea83e8ef
keywords:
- Méthode OnMediaInsert Virtual PC
- Méthode OnMediaInsert Virtual PC, interface IVMFloppyDriveEvents
- IVMFloppyDriveEvents interface Virtual PC, méthode OnMediaInsert
topic_type:
- apiref
api_name:
- IVMFloppyDriveEvents.OnMediaInsert
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d607a2f63836ca1cb151e602b2d3b2021f4e3913
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "106524834"
---
# <a name="ivmfloppydriveeventsonmediainsert-method"></a><span data-ttu-id="65ff0-107">IVMFloppyDriveEvents :: OnMediaInsert, méthode</span><span class="sxs-lookup"><span data-stu-id="65ff0-107">IVMFloppyDriveEvents::OnMediaInsert method</span></span>

<span data-ttu-id="65ff0-108">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="65ff0-108">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="65ff0-109">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="65ff0-109">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="65ff0-110">Reçoit une notification indiquant que le média a été inséré dans le lecteur.</span><span class="sxs-lookup"><span data-stu-id="65ff0-110">Receives notification that media has been inserted into the drive.</span></span>

## <a name="syntax"></a><span data-ttu-id="65ff0-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="65ff0-111">Syntax</span></span>


```C++
HRESULT OnMediaInsert(
  [in] BSTR mediaPath
);
```



## <a name="parameters"></a><span data-ttu-id="65ff0-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="65ff0-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="65ff0-113">*mediaPath* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="65ff0-113">*mediaPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="65ff0-114">Lettre de lecteur hôte ou chemin d’accès à l’image de disquette.</span><span class="sxs-lookup"><span data-stu-id="65ff0-114">The host drive letter, or path, to floppy image.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="65ff0-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="65ff0-115">Return value</span></span>

<span data-ttu-id="65ff0-116">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="65ff0-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="65ff0-117">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="65ff0-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="65ff0-118">Notes</span><span class="sxs-lookup"><span data-stu-id="65ff0-118">Remarks</span></span>

<span data-ttu-id="65ff0-119">Cette méthode est appelée lors de l’insertion d’un média (une image de disquette ou une disquette dans un lecteur hôte).</span><span class="sxs-lookup"><span data-stu-id="65ff0-119">This method is called when media (a floppy disk image or a floppy disk in a host drive) is inserted.</span></span> <span data-ttu-id="65ff0-120">Le programme client doit implémenter cette méthode d’interface pour recevoir la notification de l' \_ événement vmFloppyDriveEvent OnMediaInsert provenant de [**IVMFloppyDrive**](ivmfloppydrive.md).</span><span class="sxs-lookup"><span data-stu-id="65ff0-120">The client program must implement this interface method to receive notification of the vmFloppyDriveEvent\_OnMediaInsert event originating from [**IVMFloppyDrive**](ivmfloppydrive.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="65ff0-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="65ff0-121">Requirements</span></span>



| <span data-ttu-id="65ff0-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="65ff0-122">Requirement</span></span> | <span data-ttu-id="65ff0-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="65ff0-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="65ff0-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="65ff0-124">Minimum supported client</span></span><br/> | <span data-ttu-id="65ff0-125">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="65ff0-125">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="65ff0-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="65ff0-126">Minimum supported server</span></span><br/> | <span data-ttu-id="65ff0-127">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="65ff0-127">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="65ff0-128">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="65ff0-128">End of client support</span></span><br/>    | <span data-ttu-id="65ff0-129">Windows 7</span><span class="sxs-lookup"><span data-stu-id="65ff0-129">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="65ff0-130">Produit</span><span class="sxs-lookup"><span data-stu-id="65ff0-130">Product</span></span><br/>                  | <span data-ttu-id="65ff0-131">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="65ff0-131">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="65ff0-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="65ff0-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="65ff0-133"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="65ff0-133"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="65ff0-134">IID</span><span class="sxs-lookup"><span data-stu-id="65ff0-134">IID</span></span><br/>                      | <span data-ttu-id="65ff0-135">DIID \_ IVMFloppyDriveEvents est défini comme a9ed3401-4e09-4177-86ec-a13bf9fa7d4e</span><span class="sxs-lookup"><span data-stu-id="65ff0-135">DIID\_IVMFloppyDriveEvents is defined as a9ed3401-4e09-4177-86ec-a13bf9fa7d4e</span></span><br/>      |



## <a name="see-also"></a><span data-ttu-id="65ff0-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="65ff0-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65ff0-137">**IVMFloppyDriveEvents**</span><span class="sxs-lookup"><span data-stu-id="65ff0-137">**IVMFloppyDriveEvents**</span></span>](ivmfloppydriveevents.md)
</dt> </dl>

 

