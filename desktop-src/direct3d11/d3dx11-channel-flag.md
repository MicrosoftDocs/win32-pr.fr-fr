---
title: Énumération D3DX11_CHANNEL_FLAG (D3DX11tex. h)
description: 'Remarque : la bibliothèque de l’utilitaire D3DX (D3DX 9, D3DX 10 et D3DX 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications du Windows Store. Ces indicateurs sont utilisés par les fonctions qui opèrent sur un ou plusieurs canaux dans une texture.'
ms.assetid: 058a0a1e-3c1b-4397-a41a-2e47d878cd92
keywords:
- Énumération D3DX11_CHANNEL_FLAG Direct3D 11
- Pointeur d’énumération LPD3DX11_CHANNEL_FLAG Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_CHANNEL_FLAG
api_location:
- D3DX11tex.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2e3097552637ce96663671dda443684ebda2b65
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104394255"
---
# <a name="d3dx11_channel_flag-enumeration"></a><span data-ttu-id="68231-106">\_Énumération de l’indicateur de canal D3DX11 \_</span><span class="sxs-lookup"><span data-stu-id="68231-106">D3DX11\_CHANNEL\_FLAG enumeration</span></span>

> [!Note]  
> <span data-ttu-id="68231-107">La bibliothèque d’utilitaires D3DX (D3DX 9, D3DX 10 et D3DX 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications du Windows Store.</span><span class="sxs-lookup"><span data-stu-id="68231-107">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

<span data-ttu-id="68231-108">Ces indicateurs sont utilisés par les fonctions qui opèrent sur un ou plusieurs canaux dans une texture.</span><span class="sxs-lookup"><span data-stu-id="68231-108">These flags are used by functions which operate on one or more channels in a texture.</span></span>

## <a name="syntax"></a><span data-ttu-id="68231-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="68231-109">Syntax</span></span>


```C++
typedef enum D3DX11_CHANNEL_FLAG { 
  D3DX11_CHANNEL_RED        = (1 << 0),
  D3DX11_CHANNEL_BLUE       = (1 << 1),
  D3DX11_CHANNEL_GREEN      = (1 << 2),
  D3DX11_CHANNEL_ALPHA      = (1 << 3),
  D3DX11_CHANNEL_LUMINANCE  = (1 << 4)
} D3DX11_CHANNEL_FLAG, *LPD3DX11_CHANNEL_FLAG;
```



## <a name="constants"></a><span data-ttu-id="68231-110">Constantes</span><span class="sxs-lookup"><span data-stu-id="68231-110">Constants</span></span>

<dl> <dt>

<span data-ttu-id="68231-111"><span id="D3DX11_CHANNEL_RED"></span><span id="d3dx11_channel_red"></span>**D3DX11 \_ canal \_ rouge**</span><span class="sxs-lookup"><span data-stu-id="68231-111"><span id="D3DX11_CHANNEL_RED"></span><span id="d3dx11_channel_red"></span>**D3DX11\_CHANNEL\_RED**</span></span>
</dt> <dd>

<span data-ttu-id="68231-112">Indique que le canal rouge doit être utilisé.</span><span class="sxs-lookup"><span data-stu-id="68231-112">Indicates the red channel should be used.</span></span>

</dd> <dt>

<span data-ttu-id="68231-113"><span id="D3DX11_CHANNEL_BLUE"></span><span id="d3dx11_channel_blue"></span>**D3DX11 le \_ canal \_ bleu**</span><span class="sxs-lookup"><span data-stu-id="68231-113"><span id="D3DX11_CHANNEL_BLUE"></span><span id="d3dx11_channel_blue"></span>**D3DX11\_CHANNEL\_BLUE**</span></span>
</dt> <dd>

<span data-ttu-id="68231-114">Indique que le canal bleu doit être utilisé.</span><span class="sxs-lookup"><span data-stu-id="68231-114">Indicates the blue channel should be used.</span></span>

</dd> <dt>

<span data-ttu-id="68231-115"><span id="D3DX11_CHANNEL_GREEN"></span><span id="d3dx11_channel_green"></span>**\_Canal D3DX11 \_ vert**</span><span class="sxs-lookup"><span data-stu-id="68231-115"><span id="D3DX11_CHANNEL_GREEN"></span><span id="d3dx11_channel_green"></span>**D3DX11\_CHANNEL\_GREEN**</span></span>
</dt> <dd>

<span data-ttu-id="68231-116">Indique que le canal vert doit être utilisé.</span><span class="sxs-lookup"><span data-stu-id="68231-116">Indicates the green channel should be used.</span></span>

</dd> <dt>

<span data-ttu-id="68231-117"><span id="D3DX11_CHANNEL_ALPHA"></span><span id="d3dx11_channel_alpha"></span>**D3DX11 \_ canal \_ alpha**</span><span class="sxs-lookup"><span data-stu-id="68231-117"><span id="D3DX11_CHANNEL_ALPHA"></span><span id="d3dx11_channel_alpha"></span>**D3DX11\_CHANNEL\_ALPHA**</span></span>
</dt> <dd>

<span data-ttu-id="68231-118">Indique que le canal alpha doit être utilisé.</span><span class="sxs-lookup"><span data-stu-id="68231-118">Indicates the alpha channel should be used.</span></span>

</dd> <dt>

<span data-ttu-id="68231-119"><span id="D3DX11_CHANNEL_LUMINANCE"></span><span id="d3dx11_channel_luminance"></span>**\_Luminance du canal D3DX11 \_**</span><span class="sxs-lookup"><span data-stu-id="68231-119"><span id="D3DX11_CHANNEL_LUMINANCE"></span><span id="d3dx11_channel_luminance"></span>**D3DX11\_CHANNEL\_LUMINANCE**</span></span>
</dt> <dd>

<span data-ttu-id="68231-120">Indique que les luminaces des canaux rouge, vert et bleu doivent être utilisés.</span><span class="sxs-lookup"><span data-stu-id="68231-120">Indicates the luminaces of the red, green, and blue channels should be used.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="68231-121">Spécifications</span><span class="sxs-lookup"><span data-stu-id="68231-121">Requirements</span></span>



| <span data-ttu-id="68231-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="68231-122">Requirement</span></span> | <span data-ttu-id="68231-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="68231-123">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="68231-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="68231-124">Header</span></span><br/> | <dl> <span data-ttu-id="68231-125"><dt>D3DX11tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="68231-125"><dt>D3DX11tex.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="68231-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="68231-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68231-127">Énumérations D3DX</span><span class="sxs-lookup"><span data-stu-id="68231-127">D3DX Enumerations</span></span>](d3d11-graphics-reference-d3dx11-enums.md)
</dt> </dl>

 

 





