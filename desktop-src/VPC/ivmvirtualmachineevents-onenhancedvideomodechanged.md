---
title: Méthode IVMVirtualMachineEvents OnEnhancedVideoModeChanged (VPCCOMInterfaces. h)
description: Reçoit une notification indiquant que la prise en charge d’un ordinateur virtuel pour le mode vidéo amélioré a changé.
ms.assetid: be22a859-4687-4647-9f53-f79ae8ad52a5
keywords:
- Méthode OnEnhancedVideoModeChanged Virtual PC
- Méthode OnEnhancedVideoModeChanged Virtual PC, interface IVMVirtualMachineEvents
- IVMVirtualMachineEvents interface Virtual PC, méthode OnEnhancedVideoModeChanged
topic_type:
- apiref
api_name:
- IVMVirtualMachineEvents.OnEnhancedVideoModeChanged
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29bbc67fe298c1a47d853072d8c58ab5b3ce1988
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464182"
---
# <a name="ivmvirtualmachineeventsonenhancedvideomodechanged-method"></a><span data-ttu-id="b73c8-106">IVMVirtualMachineEvents :: OnEnhancedVideoModeChanged, méthode</span><span class="sxs-lookup"><span data-stu-id="b73c8-106">IVMVirtualMachineEvents::OnEnhancedVideoModeChanged method</span></span>

<span data-ttu-id="b73c8-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="b73c8-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="b73c8-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="b73c8-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="b73c8-109">Reçoit une notification indiquant que la prise en charge d’un ordinateur virtuel pour le mode vidéo amélioré a changé.</span><span class="sxs-lookup"><span data-stu-id="b73c8-109">Receives notification that a virtual machine's support for enhanced video mode has changed.</span></span>

## <a name="syntax"></a><span data-ttu-id="b73c8-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b73c8-110">Syntax</span></span>


```C++
HRESULT OnEnhancedVideoModeChanged(
  [in] VARIANT_BOOL enhancedVideoMode
);
```



## <a name="parameters"></a><span data-ttu-id="b73c8-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b73c8-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b73c8-112">*enhancedVideoMode* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b73c8-112">*enhancedVideoMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b73c8-113">Indique si le mode vidéo étendu est disponible.</span><span class="sxs-lookup"><span data-stu-id="b73c8-113">Indicates whether enhanced video mode is available.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b73c8-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b73c8-114">Return value</span></span>

<span data-ttu-id="b73c8-115">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="b73c8-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="b73c8-116">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="b73c8-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="b73c8-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b73c8-117">Requirements</span></span>



| <span data-ttu-id="b73c8-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b73c8-118">Requirement</span></span> | <span data-ttu-id="b73c8-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="b73c8-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="b73c8-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b73c8-120">Minimum supported client</span></span><br/> | <span data-ttu-id="b73c8-121">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b73c8-121">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b73c8-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b73c8-122">Minimum supported server</span></span><br/> | <span data-ttu-id="b73c8-123">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="b73c8-123">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="b73c8-124">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="b73c8-124">End of client support</span></span><br/>    | <span data-ttu-id="b73c8-125">Windows 7</span><span class="sxs-lookup"><span data-stu-id="b73c8-125">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="b73c8-126">Produit</span><span class="sxs-lookup"><span data-stu-id="b73c8-126">Product</span></span><br/>                  | <span data-ttu-id="b73c8-127">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="b73c8-127">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="b73c8-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="b73c8-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="b73c8-129"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="b73c8-129"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="b73c8-130">IID</span><span class="sxs-lookup"><span data-stu-id="b73c8-130">IID</span></span><br/>                      | <span data-ttu-id="b73c8-131">DIID \_ IVMVirtualMachineEvents est défini comme 9d84f560-bb67-4961-BD12-a4da780c67e4</span><span class="sxs-lookup"><span data-stu-id="b73c8-131">DIID\_IVMVirtualMachineEvents is defined as 9d84f560-bb67-4961-bd12-a4da780c67e4</span></span><br/>   |



## <a name="see-also"></a><span data-ttu-id="b73c8-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b73c8-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b73c8-133">**IVMVirtualMachineEvents**</span><span class="sxs-lookup"><span data-stu-id="b73c8-133">**IVMVirtualMachineEvents**</span></span>](ivmvirtualmachineevents.md)
</dt> </dl>

 

