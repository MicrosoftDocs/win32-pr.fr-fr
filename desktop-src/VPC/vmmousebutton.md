---
title: Énumération VMMouseButton (VPCCOMInterfaces. h)
description: Spécifie le bouton de la souris.
ms.assetid: d09e63cb-9dc5-424f-b130-c0b0dd07fe11
keywords:
- Virtual PC de l’énumération VMMouseButton
topic_type:
- apiref
api_name:
- VMMouseButton
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18744af5a4f8068b9bb371cb15e06c365561f2cf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466370"
---
# <a name="vmmousebutton-enumeration"></a><span data-ttu-id="fd08c-104">Énumération VMMouseButton</span><span class="sxs-lookup"><span data-stu-id="fd08c-104">VMMouseButton enumeration</span></span>

<span data-ttu-id="fd08c-105">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="fd08c-105">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="fd08c-106">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="fd08c-106">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="fd08c-107">Spécifie le bouton de la souris.</span><span class="sxs-lookup"><span data-stu-id="fd08c-107">Specifies the mouse button.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd08c-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fd08c-108">Syntax</span></span>


```C++
typedef enum  { 
  vmMouseButton_Left    = 1,
  vmMouseButton_Right   = 2,
  vmMouseButton_Center  = 3
} VMMouseButton;
```



## <a name="constants"></a><span data-ttu-id="fd08c-109">Constantes</span><span class="sxs-lookup"><span data-stu-id="fd08c-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="fd08c-110"><span id="vmMouseButton_Left"></span><span id="vmmousebutton_left"></span><span id="VMMOUSEBUTTON_LEFT"></span>**vmMouseButton \_ gauche**</span><span class="sxs-lookup"><span data-stu-id="fd08c-110"><span id="vmMouseButton_Left"></span><span id="vmmousebutton_left"></span><span id="VMMOUSEBUTTON_LEFT"></span>**vmMouseButton\_Left**</span></span>
</dt> <dd>

<span data-ttu-id="fd08c-111">Bouton gauche de la souris.</span><span class="sxs-lookup"><span data-stu-id="fd08c-111">The left mouse button.</span></span>

</dd> <dt>

<span data-ttu-id="fd08c-112"><span id="vmMouseButton_Right"></span><span id="vmmousebutton_right"></span><span id="VMMOUSEBUTTON_RIGHT"></span>**vmMouseButton \_ droit**</span><span class="sxs-lookup"><span data-stu-id="fd08c-112"><span id="vmMouseButton_Right"></span><span id="vmmousebutton_right"></span><span id="VMMOUSEBUTTON_RIGHT"></span>**vmMouseButton\_Right**</span></span>
</dt> <dd>

<span data-ttu-id="fd08c-113">Bouton droit de la souris.</span><span class="sxs-lookup"><span data-stu-id="fd08c-113">The right mouse button.</span></span>

</dd> <dt>

<span data-ttu-id="fd08c-114"><span id="vmMouseButton_Center"></span><span id="vmmousebutton_center"></span><span id="VMMOUSEBUTTON_CENTER"></span>**\_Centre vmMouseButton**</span><span class="sxs-lookup"><span data-stu-id="fd08c-114"><span id="vmMouseButton_Center"></span><span id="vmmousebutton_center"></span><span id="VMMOUSEBUTTON_CENTER"></span>**vmMouseButton\_Center**</span></span>
</dt> <dd>

<span data-ttu-id="fd08c-115">Bouton central de la souris.</span><span class="sxs-lookup"><span data-stu-id="fd08c-115">The center mouse button.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fd08c-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fd08c-116">Requirements</span></span>



| <span data-ttu-id="fd08c-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fd08c-117">Requirement</span></span> | <span data-ttu-id="fd08c-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="fd08c-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="fd08c-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fd08c-119">Minimum supported client</span></span><br/> | <span data-ttu-id="fd08c-120">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fd08c-120">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="fd08c-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fd08c-121">Minimum supported server</span></span><br/> | <span data-ttu-id="fd08c-122">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="fd08c-122">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="fd08c-123">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="fd08c-123">End of client support</span></span><br/>    | <span data-ttu-id="fd08c-124">Windows 7</span><span class="sxs-lookup"><span data-stu-id="fd08c-124">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="fd08c-125">Produit</span><span class="sxs-lookup"><span data-stu-id="fd08c-125">Product</span></span><br/>                  | <span data-ttu-id="fd08c-126">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="fd08c-126">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="fd08c-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="fd08c-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="fd08c-128"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="fd08c-128"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fd08c-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fd08c-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd08c-130">**IVMMouse**</span><span class="sxs-lookup"><span data-stu-id="fd08c-130">**IVMMouse**</span></span>](ivmmouse.md)
</dt> </dl>

 

