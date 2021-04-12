---
title: Énumération VMDisplayVideoMode (VPCCOMInterfaces. h)
description: Spécifie le mode vidéo de l’affichage.
ms.assetid: 9ffd1bb5-115d-4554-92c6-5dcf86f904a5
keywords:
- Virtual PC de l’énumération VMDisplayVideoMode
topic_type:
- apiref
api_name:
- VMDisplayVideoMode
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b159a8c251c83643ae9897842b313ea9be567e4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465194"
---
# <a name="vmdisplayvideomode-enumeration"></a><span data-ttu-id="677fd-104">Énumération VMDisplayVideoMode</span><span class="sxs-lookup"><span data-stu-id="677fd-104">VMDisplayVideoMode enumeration</span></span>

<span data-ttu-id="677fd-105">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="677fd-105">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="677fd-106">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="677fd-106">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="677fd-107">Spécifie le mode vidéo de l’affichage.</span><span class="sxs-lookup"><span data-stu-id="677fd-107">Specifies the display video mode.</span></span>

## <a name="syntax"></a><span data-ttu-id="677fd-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="677fd-108">Syntax</span></span>


```C++
typedef enum  { 
  vmVideoMode_TextMode  = 0,
  vmVideoMode_CGAMode   = 1,
  vmVideoMode_VGAMode   = 2,
  vmVideoMode_SVGAMode  = 3
} VMDisplayVideoMode;
```



## <a name="constants"></a><span data-ttu-id="677fd-109">Constantes</span><span class="sxs-lookup"><span data-stu-id="677fd-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="677fd-110"><span id="vmVideoMode_TextMode"></span><span id="vmvideomode_textmode"></span><span id="VMVIDEOMODE_TEXTMODE"></span>**vmVideoMode, \_ TextMode**</span><span class="sxs-lookup"><span data-stu-id="677fd-110"><span id="vmVideoMode_TextMode"></span><span id="vmvideomode_textmode"></span><span id="VMVIDEOMODE_TEXTMODE"></span>**vmVideoMode\_TextMode**</span></span>
</dt> <dd>

<span data-ttu-id="677fd-111">Mode texte.</span><span class="sxs-lookup"><span data-stu-id="677fd-111">Text mode.</span></span>

</dd> <dt>

<span data-ttu-id="677fd-112"><span id="vmVideoMode_CGAMode"></span><span id="vmvideomode_cgamode"></span><span id="VMVIDEOMODE_CGAMODE"></span>**vmVideoMode \_ CGAMode**</span><span class="sxs-lookup"><span data-stu-id="677fd-112"><span id="vmVideoMode_CGAMode"></span><span id="vmvideomode_cgamode"></span><span id="VMVIDEOMODE_CGAMODE"></span>**vmVideoMode\_CGAMode**</span></span>
</dt> <dd>

<span data-ttu-id="677fd-113">Mode CGA.</span><span class="sxs-lookup"><span data-stu-id="677fd-113">CGA mode.</span></span>

</dd> <dt>

<span data-ttu-id="677fd-114"><span id="vmVideoMode_VGAMode"></span><span id="vmvideomode_vgamode"></span><span id="VMVIDEOMODE_VGAMODE"></span>**vmVideoMode \_ VGAMode**</span><span class="sxs-lookup"><span data-stu-id="677fd-114"><span id="vmVideoMode_VGAMode"></span><span id="vmvideomode_vgamode"></span><span id="VMVIDEOMODE_VGAMODE"></span>**vmVideoMode\_VGAMode**</span></span>
</dt> <dd>

<span data-ttu-id="677fd-115">Mode VGA.</span><span class="sxs-lookup"><span data-stu-id="677fd-115">VGA mode.</span></span>

</dd> <dt>

<span data-ttu-id="677fd-116"><span id="vmVideoMode_SVGAMode"></span><span id="vmvideomode_svgamode"></span><span id="VMVIDEOMODE_SVGAMODE"></span>**vmVideoMode \_ SVGAMode**</span><span class="sxs-lookup"><span data-stu-id="677fd-116"><span id="vmVideoMode_SVGAMode"></span><span id="vmvideomode_svgamode"></span><span id="VMVIDEOMODE_SVGAMODE"></span>**vmVideoMode\_SVGAMode**</span></span>
</dt> <dd>

<span data-ttu-id="677fd-117">Mode SVGA.</span><span class="sxs-lookup"><span data-stu-id="677fd-117">SVGA mode.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="677fd-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="677fd-118">Requirements</span></span>



| <span data-ttu-id="677fd-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="677fd-119">Requirement</span></span> | <span data-ttu-id="677fd-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="677fd-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="677fd-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="677fd-121">Minimum supported client</span></span><br/> | <span data-ttu-id="677fd-122">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="677fd-122">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="677fd-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="677fd-123">Minimum supported server</span></span><br/> | <span data-ttu-id="677fd-124">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="677fd-124">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="677fd-125">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="677fd-125">End of client support</span></span><br/>    | <span data-ttu-id="677fd-126">Windows 7</span><span class="sxs-lookup"><span data-stu-id="677fd-126">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="677fd-127">Produit</span><span class="sxs-lookup"><span data-stu-id="677fd-127">Product</span></span><br/>                  | <span data-ttu-id="677fd-128">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="677fd-128">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="677fd-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="677fd-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="677fd-130"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="677fd-130"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="677fd-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="677fd-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="677fd-132">**IVMDisplay::VideoMode**</span><span class="sxs-lookup"><span data-stu-id="677fd-132">**IVMDisplay::VideoMode**</span></span>](ivmdisplay-videomode.md)
</dt> </dl>

 

