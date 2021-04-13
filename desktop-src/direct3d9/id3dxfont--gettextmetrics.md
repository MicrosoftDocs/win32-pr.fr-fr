---
description: Récupère les caractéristiques de police qui sont identifiées dans une structure TEXTMETRIC. Cette méthode prend en charge les paramètres du compilateur ANSI et Unicode.
ms.assetid: 37788281-5bb0-45bb-b6d4-bdc4d811e3af
title: 'ID3DXFont :: GetTextMetrics, méthode (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFont.GetTextMetrics
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6ce6064804d2aac2846cbea6971f145fc07759f3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322882"
---
# <a name="id3dxfontgettextmetrics-method"></a><span data-ttu-id="e24f0-104">ID3DXFont :: GetTextMetrics, méthode</span><span class="sxs-lookup"><span data-stu-id="e24f0-104">ID3DXFont::GetTextMetrics method</span></span>

<span data-ttu-id="e24f0-105">Récupère les caractéristiques de police qui sont identifiées dans une structure [**TEXTMETRIC**](/windows/win32/api/wingdi/ns-wingdi-textmetrica) .</span><span class="sxs-lookup"><span data-stu-id="e24f0-105">Retrieves font characteristics that are identified in a [**TEXTMETRIC**](/windows/win32/api/wingdi/ns-wingdi-textmetrica) structure.</span></span> <span data-ttu-id="e24f0-106">Cette méthode prend en charge les paramètres du compilateur ANSI et Unicode.</span><span class="sxs-lookup"><span data-stu-id="e24f0-106">This method supports ANSI and Unicode compiler settings.</span></span>

## <a name="syntax"></a><span data-ttu-id="e24f0-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e24f0-107">Syntax</span></span>


```C++
BOOL GetTextMetrics(
  [out] TEXTMETRIC *pTextMetrics
);
```



## <a name="parameters"></a><span data-ttu-id="e24f0-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e24f0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e24f0-109">*pTextMetrics* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="e24f0-109">*pTextMetrics* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e24f0-110">Type : **[ **TEXTMETRIC**](/windows/win32/api/wingdi/ns-wingdi-textmetrica)\***</span><span class="sxs-lookup"><span data-stu-id="e24f0-110">Type: **[**TEXTMETRIC**](/windows/win32/api/wingdi/ns-wingdi-textmetrica)\***</span></span>

<span data-ttu-id="e24f0-111">Pointeur vers une structure [**TEXTMETRIC**](/windows/win32/api/wingdi/ns-wingdi-textmetrica) , qui contient les propriétés de police.</span><span class="sxs-lookup"><span data-stu-id="e24f0-111">Pointer to a [**TEXTMETRIC**](/windows/win32/api/wingdi/ns-wingdi-textmetrica) structure, which contains font properties.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e24f0-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e24f0-112">Return value</span></span>

<span data-ttu-id="e24f0-113">Type : **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e24f0-113">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e24f0-114">Une valeur différente de zéro si la fonction réussit ; sinon, 0.</span><span class="sxs-lookup"><span data-stu-id="e24f0-114">Nonzero if the function is successful; otherwise 0.</span></span>

## <a name="remarks"></a><span data-ttu-id="e24f0-115">Notes</span><span class="sxs-lookup"><span data-stu-id="e24f0-115">Remarks</span></span>

<span data-ttu-id="e24f0-116">Le paramètre du compilateur détermine également le type de structure.</span><span class="sxs-lookup"><span data-stu-id="e24f0-116">The compiler setting also determines the structure type.</span></span> <span data-ttu-id="e24f0-117">Si Unicode est défini, la fonction retourne une structure TEXTMETRICW.</span><span class="sxs-lookup"><span data-stu-id="e24f0-117">If Unicode is defined, the function returns a TEXTMETRICW structure.</span></span> <span data-ttu-id="e24f0-118">Dans le cas contraire, l’appel de fonction retourne une structure TEXTMETRICA.</span><span class="sxs-lookup"><span data-stu-id="e24f0-118">Otherwise, the function call returns a TEXTMETRICA structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="e24f0-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e24f0-119">Requirements</span></span>



| <span data-ttu-id="e24f0-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e24f0-120">Requirement</span></span> | <span data-ttu-id="e24f0-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="e24f0-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e24f0-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="e24f0-122">Header</span></span><br/>  | <dl> <span data-ttu-id="e24f0-123"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="e24f0-123"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="e24f0-124">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="e24f0-124">Library</span></span><br/> | <dl> <span data-ttu-id="e24f0-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e24f0-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="e24f0-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e24f0-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e24f0-127">ID3DXFont</span><span class="sxs-lookup"><span data-stu-id="e24f0-127">ID3DXFont</span></span>](id3dxfont.md)
</dt> </dl>

 

 
