---
description: Ces indicateurs sont utilisés par les fonctions qui opèrent sur un ou plusieurs canaux dans une texture.
ms.assetid: 54ecb39a-a36e-43bb-bb51-78b7375716d8
title: Énumération D3DX10_CHANNEL_FLAG (D3DX10Tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_CHANNEL_FLAG
api_type:
- HeaderDef
api_location:
- D3DX10Tex.h
ms.openlocfilehash: f21958ab964a70116a551c0cb8dadbce6db88f7d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104323230"
---
# <a name="d3dx10_channel_flag-enumeration"></a><span data-ttu-id="bcaa4-103">\_Énumération de l’indicateur de canal d3dx10 \_</span><span class="sxs-lookup"><span data-stu-id="bcaa4-103">D3DX10\_CHANNEL\_FLAG enumeration</span></span>

<span data-ttu-id="bcaa4-104">Ces indicateurs sont utilisés par les fonctions qui opèrent sur un ou plusieurs canaux dans une texture.</span><span class="sxs-lookup"><span data-stu-id="bcaa4-104">These flags are used by functions which operate on one or more channels in a texture.</span></span>

## <a name="syntax"></a><span data-ttu-id="bcaa4-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bcaa4-105">Syntax</span></span>


```C++
typedef enum D3DX10_CHANNEL_FLAG { 
  D3DX10_CHANNEL_RED        = (1 << 0),
  D3DX10_CHANNEL_BLUE       = (1 << 1),
  D3DX10_CHANNEL_GREEN      = (1 << 2),
  D3DX10_CHANNEL_ALPHA      = (1 << 3),
  D3DX10_CHANNEL_LUMINANCE  = (1 << 4)
} D3DX10_CHANNEL_FLAG, *LPD3DX10_CHANNEL_FLAG;
```



## <a name="constants"></a><span data-ttu-id="bcaa4-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="bcaa4-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="bcaa4-107"><span id="D3DX10_CHANNEL_RED"></span><span id="d3dx10_channel_red"></span>**D3DX10 \_ canal \_ rouge**</span><span class="sxs-lookup"><span data-stu-id="bcaa4-107"><span id="D3DX10_CHANNEL_RED"></span><span id="d3dx10_channel_red"></span>**D3DX10\_CHANNEL\_RED**</span></span>
</dt> <dd>

<span data-ttu-id="bcaa4-108">Indique que le canal rouge doit être utilisé.</span><span class="sxs-lookup"><span data-stu-id="bcaa4-108">Indicates the red channel should be used.</span></span>

</dd> <dt>

<span data-ttu-id="bcaa4-109"><span id="D3DX10_CHANNEL_BLUE"></span><span id="d3dx10_channel_blue"></span>**D3DX10 le \_ canal \_ bleu**</span><span class="sxs-lookup"><span data-stu-id="bcaa4-109"><span id="D3DX10_CHANNEL_BLUE"></span><span id="d3dx10_channel_blue"></span>**D3DX10\_CHANNEL\_BLUE**</span></span>
</dt> <dd>

<span data-ttu-id="bcaa4-110">Indique que le canal bleu doit être utilisé.</span><span class="sxs-lookup"><span data-stu-id="bcaa4-110">Indicates the blue channel should be used.</span></span>

</dd> <dt>

<span data-ttu-id="bcaa4-111"><span id="D3DX10_CHANNEL_GREEN"></span><span id="d3dx10_channel_green"></span>**\_Canal d3dx10 \_ vert**</span><span class="sxs-lookup"><span data-stu-id="bcaa4-111"><span id="D3DX10_CHANNEL_GREEN"></span><span id="d3dx10_channel_green"></span>**D3DX10\_CHANNEL\_GREEN**</span></span>
</dt> <dd>

<span data-ttu-id="bcaa4-112">Indique que le canal vert doit être utilisé.</span><span class="sxs-lookup"><span data-stu-id="bcaa4-112">Indicates the green channel should be used.</span></span>

</dd> <dt>

<span data-ttu-id="bcaa4-113"><span id="D3DX10_CHANNEL_ALPHA"></span><span id="d3dx10_channel_alpha"></span>**D3DX10 \_ canal \_ alpha**</span><span class="sxs-lookup"><span data-stu-id="bcaa4-113"><span id="D3DX10_CHANNEL_ALPHA"></span><span id="d3dx10_channel_alpha"></span>**D3DX10\_CHANNEL\_ALPHA**</span></span>
</dt> <dd>

<span data-ttu-id="bcaa4-114">Indique que le canal alpha doit être utilisé.</span><span class="sxs-lookup"><span data-stu-id="bcaa4-114">Indicates the alpha channel should be used.</span></span>

</dd> <dt>

<span data-ttu-id="bcaa4-115"><span id="D3DX10_CHANNEL_LUMINANCE"></span><span id="d3dx10_channel_luminance"></span>**\_Luminance du canal d3dx10 \_**</span><span class="sxs-lookup"><span data-stu-id="bcaa4-115"><span id="D3DX10_CHANNEL_LUMINANCE"></span><span id="d3dx10_channel_luminance"></span>**D3DX10\_CHANNEL\_LUMINANCE**</span></span>
</dt> <dd>

<span data-ttu-id="bcaa4-116">Indique que les luminaces des canaux rouge, vert et bleu doivent être utilisés.</span><span class="sxs-lookup"><span data-stu-id="bcaa4-116">Indicates the luminaces of the red, green, and blue channels should be used.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="bcaa4-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bcaa4-117">Requirements</span></span>



| <span data-ttu-id="bcaa4-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bcaa4-118">Requirement</span></span> | <span data-ttu-id="bcaa4-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="bcaa4-119">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="bcaa4-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="bcaa4-120">Header</span></span><br/> | <dl> <span data-ttu-id="bcaa4-121"><dt>D3DX10Tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="bcaa4-121"><dt>D3DX10Tex.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bcaa4-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bcaa4-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bcaa4-123">Énumérations D3DX</span><span class="sxs-lookup"><span data-stu-id="bcaa4-123">D3DX Enumerations</span></span>](d3d10-graphics-reference-d3dx10-enums.md)
</dt> </dl>

 

 




