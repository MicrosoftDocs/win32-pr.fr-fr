---
description: L' \_ \_ énumération de la page S0 MXDC \_ est utilisée pour spécifier les types de ressources qui peuvent être associées à des pages dans les documents XPS et qui peuvent être traitées, ou transmises sans traitement, par Microsoft XPS Document Converter (MXDC) dans sa sortie.
ms.assetid: e111d92e-5102-4b39-b311-f9ff1d1a96f1
title: Énumération MXDC_S0_PAGE_ENUMS (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MXDC_S0_PAGE_ENUMS
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 1b4331210027f7fc23f36fb6b9d13a2c232ccbf6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864958"
---
# <a name="mxdc_s0_page_enums-enumeration"></a><span data-ttu-id="b1628-103">Énumération des énumérations de la \_ page S0 MXDC \_ \_</span><span class="sxs-lookup"><span data-stu-id="b1628-103">MXDC\_S0\_PAGE\_ENUMS enumeration</span></span>

<span data-ttu-id="b1628-104">L’énumération de la **\_ \_ page \_ S0 MXDC** est utilisée pour spécifier les types de ressources qui peuvent être associées à des pages dans les documents XPS et qui peuvent être traitées, ou transmises sans traitement, par Microsoft XPS Document Converter (MXDC) dans sa sortie.</span><span class="sxs-lookup"><span data-stu-id="b1628-104">The **MXDC\_S0\_PAGE\_ENUMS** enumeration is used to specify types of resources that can be associated with pages in XPS documents and that can be processed, or passed unprocessed, by Microsoft XPS Document Converter (MXDC) to its output.</span></span>

## <a name="syntax"></a><span data-ttu-id="b1628-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b1628-105">Syntax</span></span>


```C++
typedef enum tagMxdcS0PageEnums { 
  MXDC_RESOURCE_TTF,
  MXDC_RESOURCE_JPEG,
  MXDC_RESOURCE_PNG,
  MXDC_RESOURCE_TIFF,
  MXDC_RESOURCE_WDP,
  MXDC_RESOURCE_DICTIONARY,
  MXDC_RESOURCE_ICC_PROFILE,
  MXDC_RESOURCE_JPEG_THUMBNAIL,
  MXDC_RESOURCE_PNG_THUMBNAIL,
  MXDC_RESOURCE_MAX
} MXDC_S0_PAGE_ENUMS;
```



## <a name="constants"></a><span data-ttu-id="b1628-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="b1628-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="b1628-107"><span id="MXDC_RESOURCE_TTF"></span><span id="mxdc_resource_ttf"></span>**MXDC, \_ ressource \_ ttf**</span><span class="sxs-lookup"><span data-stu-id="b1628-107"><span id="MXDC_RESOURCE_TTF"></span><span id="mxdc_resource_ttf"></span>**MXDC\_RESOURCE\_TTF**</span></span>
</dt> <dd>

<span data-ttu-id="b1628-108">Police TrueType ou OpenType.</span><span class="sxs-lookup"><span data-stu-id="b1628-108">TrueType or OpenType font.</span></span>

</dd> <dt>

<span data-ttu-id="b1628-109"><span id="MXDC_RESOURCE_JPEG"></span><span id="mxdc_resource_jpeg"></span>**MXDC \_ ressource \_ JPEG**</span><span class="sxs-lookup"><span data-stu-id="b1628-109"><span id="MXDC_RESOURCE_JPEG"></span><span id="mxdc_resource_jpeg"></span>**MXDC\_RESOURCE\_JPEG**</span></span>
</dt> <dd>

<span data-ttu-id="b1628-110">Image JPEG</span><span class="sxs-lookup"><span data-stu-id="b1628-110">JPEG image</span></span>

</dd> <dt>

<span data-ttu-id="b1628-111"><span id="MXDC_RESOURCE_PNG"></span><span id="mxdc_resource_png"></span>**MXDC \_ ressource \_ PNG**</span><span class="sxs-lookup"><span data-stu-id="b1628-111"><span id="MXDC_RESOURCE_PNG"></span><span id="mxdc_resource_png"></span>**MXDC\_RESOURCE\_PNG**</span></span>
</dt> <dd>

<span data-ttu-id="b1628-112">Image PNG.</span><span class="sxs-lookup"><span data-stu-id="b1628-112">PNG image.</span></span>

</dd> <dt>

<span data-ttu-id="b1628-113"><span id="MXDC_RESOURCE_TIFF"></span><span id="mxdc_resource_tiff"></span>**MXDC \_ ressource \_ TIFF**</span><span class="sxs-lookup"><span data-stu-id="b1628-113"><span id="MXDC_RESOURCE_TIFF"></span><span id="mxdc_resource_tiff"></span>**MXDC\_RESOURCE\_TIFF**</span></span>
</dt> <dd>

<span data-ttu-id="b1628-114">Image TIFF.</span><span class="sxs-lookup"><span data-stu-id="b1628-114">TIFF image.</span></span>

</dd> <dt>

<span data-ttu-id="b1628-115"><span id="MXDC_RESOURCE_WDP"></span><span id="mxdc_resource_wdp"></span>**\_ressource MXDC \_ WDP**</span><span class="sxs-lookup"><span data-stu-id="b1628-115"><span id="MXDC_RESOURCE_WDP"></span><span id="mxdc_resource_wdp"></span>**MXDC\_RESOURCE\_WDP**</span></span>
</dt> <dd>

<span data-ttu-id="b1628-116">Image Windows Media photo.</span><span class="sxs-lookup"><span data-stu-id="b1628-116">Windows Media Photo image.</span></span>

</dd> <dt>

<span data-ttu-id="b1628-117"><span id="MXDC_RESOURCE_DICTIONARY"></span><span id="mxdc_resource_dictionary"></span>**\_dictionnaire de ressources MXDC \_**</span><span class="sxs-lookup"><span data-stu-id="b1628-117"><span id="MXDC_RESOURCE_DICTIONARY"></span><span id="mxdc_resource_dictionary"></span>**MXDC\_RESOURCE\_DICTIONARY**</span></span>
</dt> <dd>

<span data-ttu-id="b1628-118">Dictionnaire de ressources distant qui doit être passé à la sortie de MXDC non traité.</span><span class="sxs-lookup"><span data-stu-id="b1628-118">Remote resource dictionary that should be passed to MXDC's output unprocessed.</span></span>

</dd> <dt>

<span data-ttu-id="b1628-119"><span id="MXDC_RESOURCE_ICC_PROFILE"></span><span id="mxdc_resource_icc_profile"></span>**\_ \_ profil ICC de la ressource MXDC \_**</span><span class="sxs-lookup"><span data-stu-id="b1628-119"><span id="MXDC_RESOURCE_ICC_PROFILE"></span><span id="mxdc_resource_icc_profile"></span>**MXDC\_RESOURCE\_ICC\_PROFILE**</span></span>
</dt> <dd>

<span data-ttu-id="b1628-120">Profil ICC qui doit être passé à la sortie de MXDC non traité.</span><span class="sxs-lookup"><span data-stu-id="b1628-120">ICC profile that should be passed to MXDC's output unprocessed.</span></span>

</dd> <dt>

<span data-ttu-id="b1628-121"><span id="MXDC_RESOURCE_JPEG_THUMBNAIL"></span><span id="mxdc_resource_jpeg_thumbnail"></span>**\_ \_ miniature JPEG de la ressource MXDC \_**</span><span class="sxs-lookup"><span data-stu-id="b1628-121"><span id="MXDC_RESOURCE_JPEG_THUMBNAIL"></span><span id="mxdc_resource_jpeg_thumbnail"></span>**MXDC\_RESOURCE\_JPEG\_THUMBNAIL**</span></span>
</dt> <dd>

<span data-ttu-id="b1628-122">Miniature JPEG qui doit être transmise à la sortie de MXDC non traité.</span><span class="sxs-lookup"><span data-stu-id="b1628-122">JPEG thumbnail that should be passed to MXDC's output unprocessed.</span></span>

</dd> <dt>

<span data-ttu-id="b1628-123"><span id="MXDC_RESOURCE_PNG_THUMBNAIL"></span><span id="mxdc_resource_png_thumbnail"></span>**\_ \_ miniature png de ressource MXDC \_**</span><span class="sxs-lookup"><span data-stu-id="b1628-123"><span id="MXDC_RESOURCE_PNG_THUMBNAIL"></span><span id="mxdc_resource_png_thumbnail"></span>**MXDC\_RESOURCE\_PNG\_THUMBNAIL**</span></span>
</dt> <dd>

<span data-ttu-id="b1628-124">Miniature PNG qui doit être transmise à la sortie de MXDC non traité.</span><span class="sxs-lookup"><span data-stu-id="b1628-124">PNG thumbnail that should be passed to MXDC's output unprocessed.</span></span>

</dd> <dt>

<span data-ttu-id="b1628-125"><span id="MXDC_RESOURCE_MAX"></span><span id="mxdc_resource_max"></span>**MXDC \_ ressource \_ Max.**</span><span class="sxs-lookup"><span data-stu-id="b1628-125"><span id="MXDC_RESOURCE_MAX"></span><span id="mxdc_resource_max"></span>**MXDC\_RESOURCE\_MAX**</span></span>
</dt> <dd>

<span data-ttu-id="b1628-126">Nombre maximal de ressources pour la validation.</span><span class="sxs-lookup"><span data-stu-id="b1628-126">The maximum resource count for validation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b1628-127">Notes</span><span class="sxs-lookup"><span data-stu-id="b1628-127">Remarks</span></span>

<span data-ttu-id="b1628-128">Cette énumération est principalement utilisée en tant que membre **dwResourceType** de la structure de la [**\_ ressource MXDC XPS \_ S0PAGE \_ \_**](mxdcxpss0pageresource.md) .</span><span class="sxs-lookup"><span data-stu-id="b1628-128">This enumeration is primarily used as the **dwResourceType** member of the [**MXDC\_XPS\_S0PAGE\_RESOURCE\_T**](mxdcxpss0pageresource.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="b1628-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b1628-129">Requirements</span></span>



| <span data-ttu-id="b1628-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b1628-130">Requirement</span></span> | <span data-ttu-id="b1628-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="b1628-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b1628-132">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b1628-132">Minimum supported client</span></span><br/> | <span data-ttu-id="b1628-133">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b1628-133">Windows Vista \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="b1628-134">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b1628-134">Minimum supported server</span></span><br/> | <span data-ttu-id="b1628-135">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b1628-135">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="b1628-136">En-tête</span><span class="sxs-lookup"><span data-stu-id="b1628-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="b1628-137"><dt>Winspool. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b1628-137"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |



 

 




