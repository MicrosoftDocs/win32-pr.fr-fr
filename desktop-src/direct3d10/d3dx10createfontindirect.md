---
description: Crée un objet de police. Remarque au lieu d’utiliser cette fonction, nous vous recommandons d’utiliser DirectWrite et la bibliothèque DirectXTK, SpriteFont Class.
ms.assetid: 057ee033-37d8-4fc1-9f35-776393fff008
title: D3DX10CreateFontIndirect, fonction (D3DX10Core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateFontIndirect
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: ae69b02483a94a80a06ef52ee4857eb081cfcfb2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322770"
---
# <a name="d3dx10createfontindirect-function"></a><span data-ttu-id="6e2ac-103">D3DX10CreateFontIndirect fonction)</span><span class="sxs-lookup"><span data-stu-id="6e2ac-103">D3DX10CreateFontIndirect function</span></span>

<span data-ttu-id="6e2ac-104">Crée un objet de police.</span><span class="sxs-lookup"><span data-stu-id="6e2ac-104">Creates a font object.</span></span>

> [!Note]  
> <span data-ttu-id="6e2ac-105">Au lieu d’utiliser cette fonction, nous vous recommandons d’utiliser [DirectWrite](../directwrite/direct-write-portal.md) et la bibliothèque [DirectXTK](https://github.com/Microsoft/DirectXTK) , la classe **SpriteFont** .</span><span class="sxs-lookup"><span data-stu-id="6e2ac-105">Instead of using this function, we recommend that you use [DirectWrite](../directwrite/direct-write-portal.md) and the [DirectXTK](https://github.com/Microsoft/DirectXTK) library, **SpriteFont** class.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="6e2ac-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6e2ac-106">Syntax</span></span>


```C++
HRESULT D3DX10CreateFontIndirect(
  _In_        ID3D10Device     *pDevice,
  _In_  const D3DX10_FONT_DESC *pDesc,
  _Out_       LPD3DX10FONT     *ppFont
);
```



## <a name="parameters"></a><span data-ttu-id="6e2ac-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6e2ac-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6e2ac-108">*pDevice* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6e2ac-108">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6e2ac-109">Type : **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***</span><span class="sxs-lookup"><span data-stu-id="6e2ac-109">Type: **[**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***</span></span>

<span data-ttu-id="6e2ac-110">Pointeur vers une interface d' [**interface ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device) .</span><span class="sxs-lookup"><span data-stu-id="6e2ac-110">Pointer to an [**ID3D10Device Interface**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device) interface.</span></span>

</dd> <dt>

<span data-ttu-id="6e2ac-111">*pDesc* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6e2ac-111">*pDesc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6e2ac-112">Type : **const [**d3dx10 \_ \_ Description**](d3dx10-font-desc.md) \*** de la police</span><span class="sxs-lookup"><span data-stu-id="6e2ac-112">Type: **const [**D3DX10\_FONT\_DESC**](d3dx10-font-desc.md)\***</span></span>

<span data-ttu-id="6e2ac-113">Pointeur vers une structure de [**\_ police d3dx10 \_**](d3dx10-font-desc.md) décrivant les attributs de l’objet font à créer.</span><span class="sxs-lookup"><span data-stu-id="6e2ac-113">Pointer to a [**D3DX10\_FONT\_DESC**](d3dx10-font-desc.md) structure, describing the attributes of the font object to create.</span></span> <span data-ttu-id="6e2ac-114">Si Unicode est défini, l’appel de fonction est résolu en D3DXCreateFontIndirectW.</span><span class="sxs-lookup"><span data-stu-id="6e2ac-114">If Unicode is defined, the function call resolves to D3DXCreateFontIndirectW.</span></span> <span data-ttu-id="6e2ac-115">Dans le cas contraire, l’appel de fonction est résolu en D3DXCreateFontIndirectA, car les chaînes ANSI sont utilisées.</span><span class="sxs-lookup"><span data-stu-id="6e2ac-115">Otherwise, the function call resolves to D3DXCreateFontIndirectA because ANSI strings are being used.</span></span>

</dd> <dt>

<span data-ttu-id="6e2ac-116">*ppFont* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="6e2ac-116">*ppFont* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6e2ac-117">Type : **[ **LPD3DX10FONT**](id3dx10font.md)\***</span><span class="sxs-lookup"><span data-stu-id="6e2ac-117">Type: **[**LPD3DX10FONT**](id3dx10font.md)\***</span></span>

<span data-ttu-id="6e2ac-118">Retourne un pointeur vers une [**interface ID3DX10Font**](id3dx10font.md).</span><span class="sxs-lookup"><span data-stu-id="6e2ac-118">Returns a pointer to an [**ID3DX10Font Interface**](id3dx10font.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6e2ac-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6e2ac-119">Return value</span></span>

<span data-ttu-id="6e2ac-120">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="6e2ac-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="6e2ac-121">La valeur de retour est l’une des valeurs indiquées dans les [codes de retour Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="6e2ac-121">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6e2ac-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6e2ac-122">Requirements</span></span>



| <span data-ttu-id="6e2ac-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6e2ac-123">Requirement</span></span> | <span data-ttu-id="6e2ac-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="6e2ac-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6e2ac-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="6e2ac-125">Header</span></span><br/>  | <dl> <span data-ttu-id="6e2ac-126"><dt>D3DX10Core. h</dt></span><span class="sxs-lookup"><span data-stu-id="6e2ac-126"><dt>D3DX10Core.h</dt></span></span> </dl> |
| <span data-ttu-id="6e2ac-127">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="6e2ac-127">Library</span></span><br/> | <dl> <span data-ttu-id="6e2ac-128"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6e2ac-128"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="6e2ac-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6e2ac-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6e2ac-130">Fonctions usage général</span><span class="sxs-lookup"><span data-stu-id="6e2ac-130">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
