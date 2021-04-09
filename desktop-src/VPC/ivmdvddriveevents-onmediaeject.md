---
title: Méthode IVMDVDDriveEvents OnMediaEject (VPCCOMInterfaces. h)
description: Reçoit une notification indiquant que le média a été éjecté du lecteur. | Méthode IVMDVDDriveEvents OnMediaEject (VPCCOMInterfaces. h)
ms.assetid: ec90fbce-7123-4bfa-abab-300e916fa089
keywords:
- Méthode OnMediaEject Virtual PC
- Méthode OnMediaEject Virtual PC, interface IVMDVDDriveEvents
- IVMDVDDriveEvents interface Virtual PC, méthode OnMediaEject
topic_type:
- apiref
api_name:
- IVMDVDDriveEvents.OnMediaEject
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3b66091dcc6cc5ee28ab6e0cb3d58e3e647e41cb
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "103869734"
---
# <a name="ivmdvddriveeventsonmediaeject-method"></a><span data-ttu-id="f3636-107">IVMDVDDriveEvents :: OnMediaEject, méthode</span><span class="sxs-lookup"><span data-stu-id="f3636-107">IVMDVDDriveEvents::OnMediaEject method</span></span>

<span data-ttu-id="f3636-108">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="f3636-108">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="f3636-109">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="f3636-109">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="f3636-110">Reçoit une notification indiquant que le média a été éjecté du lecteur.</span><span class="sxs-lookup"><span data-stu-id="f3636-110">Receives notification that media has been ejected from the drive.</span></span>

## <a name="syntax"></a><span data-ttu-id="f3636-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f3636-111">Syntax</span></span>


```C++
HRESULT OnMediaEject(
  [in] BSTR mediaPath
);
```



## <a name="parameters"></a><span data-ttu-id="f3636-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f3636-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f3636-113">*mediaPath* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f3636-113">*mediaPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f3636-114">Lettre de lecteur hôte, ou chemin d’accès, à l’image ISO.</span><span class="sxs-lookup"><span data-stu-id="f3636-114">The host drive letter, or path, to the ISO image.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f3636-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f3636-115">Return value</span></span>

<span data-ttu-id="f3636-116">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="f3636-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="f3636-117">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="f3636-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="f3636-118">Notes</span><span class="sxs-lookup"><span data-stu-id="f3636-118">Remarks</span></span>

<span data-ttu-id="f3636-119">Cette méthode est appelée lorsque le média (une image ISO ou un disque d’un lecteur hôte) est éjecté.</span><span class="sxs-lookup"><span data-stu-id="f3636-119">This method is called when media (an ISO image or a disc in a host drive) is ejected.</span></span> <span data-ttu-id="f3636-120">Le programme client doit implémenter cette méthode d’interface pour recevoir la notification de l' \_ événement vmDVDDriveEvent OnEject provenant de [**IVMDVDDrive**](ivmdvddrive.md).</span><span class="sxs-lookup"><span data-stu-id="f3636-120">The client program must implement this interface method to receive notification of the vmDVDDriveEvent\_OnEject event originating from [**IVMDVDDrive**](ivmdvddrive.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f3636-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f3636-121">Requirements</span></span>



| <span data-ttu-id="f3636-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f3636-122">Requirement</span></span> | <span data-ttu-id="f3636-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="f3636-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="f3636-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f3636-124">Minimum supported client</span></span><br/> | <span data-ttu-id="f3636-125">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f3636-125">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f3636-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f3636-126">Minimum supported server</span></span><br/> | <span data-ttu-id="f3636-127">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="f3636-127">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="f3636-128">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="f3636-128">End of client support</span></span><br/>    | <span data-ttu-id="f3636-129">Windows 7</span><span class="sxs-lookup"><span data-stu-id="f3636-129">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="f3636-130">Produit</span><span class="sxs-lookup"><span data-stu-id="f3636-130">Product</span></span><br/>                  | <span data-ttu-id="f3636-131">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="f3636-131">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="f3636-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="f3636-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="f3636-133"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="f3636-133"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="f3636-134">IID</span><span class="sxs-lookup"><span data-stu-id="f3636-134">IID</span></span><br/>                      | <span data-ttu-id="f3636-135">DIID \_ IVMDVDDriveEvents est défini comme c2a7d8e9-E76C-4EB8-94f7-71a5122d249b</span><span class="sxs-lookup"><span data-stu-id="f3636-135">DIID\_IVMDVDDriveEvents is defined as c2a7d8e9-e76c-4eb8-94f7-71a5122d249b</span></span><br/>         |



## <a name="see-also"></a><span data-ttu-id="f3636-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f3636-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3636-137">**IVMDVDDriveEvents**</span><span class="sxs-lookup"><span data-stu-id="f3636-137">**IVMDVDDriveEvents**</span></span>](ivmdvddriveevents.md)
</dt> </dl>

 

