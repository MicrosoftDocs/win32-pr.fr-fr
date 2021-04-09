---
title: Méthode IVMFloppyDriveEvents OnMediaEject (VPCCOMInterfaces. h)
description: Reçoit une notification indiquant que le média a été éjecté du lecteur. | Méthode IVMFloppyDriveEvents OnMediaEject (VPCCOMInterfaces. h)
ms.assetid: 3e9c0b5d-8fec-4f34-93d2-c5975403798b
keywords:
- Méthode OnMediaEject Virtual PC
- Méthode OnMediaEject Virtual PC, interface IVMFloppyDriveEvents
- IVMFloppyDriveEvents interface Virtual PC, méthode OnMediaEject
topic_type:
- apiref
api_name:
- IVMFloppyDriveEvents.OnMediaEject
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd640f7b8eb143eba4f3b19e984792f2b6779ad6
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "103870054"
---
# <a name="ivmfloppydriveeventsonmediaeject-method"></a><span data-ttu-id="bd91c-107">IVMFloppyDriveEvents :: OnMediaEject, méthode</span><span class="sxs-lookup"><span data-stu-id="bd91c-107">IVMFloppyDriveEvents::OnMediaEject method</span></span>

<span data-ttu-id="bd91c-108">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="bd91c-108">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="bd91c-109">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="bd91c-109">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="bd91c-110">Reçoit une notification indiquant que le média a été éjecté du lecteur.</span><span class="sxs-lookup"><span data-stu-id="bd91c-110">Receives notification that media has been ejected from the drive.</span></span>

## <a name="syntax"></a><span data-ttu-id="bd91c-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bd91c-111">Syntax</span></span>


```C++
HRESULT OnMediaEject(
  [in] BSTR mediaPath
);
```



## <a name="parameters"></a><span data-ttu-id="bd91c-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bd91c-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bd91c-113">*mediaPath* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="bd91c-113">*mediaPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bd91c-114">Lettre de lecteur hôte ou chemin d’accès à l’image de disquette.</span><span class="sxs-lookup"><span data-stu-id="bd91c-114">The host drive letter, or path, to floppy image.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bd91c-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="bd91c-115">Return value</span></span>

<span data-ttu-id="bd91c-116">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="bd91c-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="bd91c-117">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="bd91c-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="bd91c-118">Notes</span><span class="sxs-lookup"><span data-stu-id="bd91c-118">Remarks</span></span>

<span data-ttu-id="bd91c-119">Cette méthode est appelée lorsque le média (une image de disquette ou une disquette dans un lecteur hôte) est éjecté.</span><span class="sxs-lookup"><span data-stu-id="bd91c-119">This method is called when media (a floppy disk image or a floppy disk in a host drive) is ejected.</span></span> <span data-ttu-id="bd91c-120">Le programme client doit implémenter cette méthode d’interface pour recevoir la notification de l' \_ événement vmFloppyDriveEvent OnMediaEject provenant de [**IVMFloppyDrive**](ivmfloppydrive.md).</span><span class="sxs-lookup"><span data-stu-id="bd91c-120">The client program must implement this interface method to receive notification of the vmFloppyDriveEvent\_OnMediaEject event originating from [**IVMFloppyDrive**](ivmfloppydrive.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="bd91c-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bd91c-121">Requirements</span></span>



| <span data-ttu-id="bd91c-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bd91c-122">Requirement</span></span> | <span data-ttu-id="bd91c-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="bd91c-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="bd91c-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bd91c-124">Minimum supported client</span></span><br/> | <span data-ttu-id="bd91c-125">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bd91c-125">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="bd91c-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bd91c-126">Minimum supported server</span></span><br/> | <span data-ttu-id="bd91c-127">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="bd91c-127">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="bd91c-128">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="bd91c-128">End of client support</span></span><br/>    | <span data-ttu-id="bd91c-129">Windows 7</span><span class="sxs-lookup"><span data-stu-id="bd91c-129">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="bd91c-130">Produit</span><span class="sxs-lookup"><span data-stu-id="bd91c-130">Product</span></span><br/>                  | <span data-ttu-id="bd91c-131">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="bd91c-131">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="bd91c-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="bd91c-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="bd91c-133"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="bd91c-133"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="bd91c-134">IID</span><span class="sxs-lookup"><span data-stu-id="bd91c-134">IID</span></span><br/>                      | <span data-ttu-id="bd91c-135">DIID \_ IVMFloppyDriveEvents est défini comme a9ed3401-4e09-4177-86ec-a13bf9fa7d4e</span><span class="sxs-lookup"><span data-stu-id="bd91c-135">DIID\_IVMFloppyDriveEvents is defined as a9ed3401-4e09-4177-86ec-a13bf9fa7d4e</span></span><br/>      |



## <a name="see-also"></a><span data-ttu-id="bd91c-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bd91c-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bd91c-137">**IVMFloppyDriveEvents**</span><span class="sxs-lookup"><span data-stu-id="bd91c-137">**IVMFloppyDriveEvents**</span></span>](ivmfloppydriveevents.md)
</dt> </dl>

 

