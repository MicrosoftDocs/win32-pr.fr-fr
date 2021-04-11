---
description: Chargez le texte mis en forme dans la mémoire vidéo pour améliorer l’efficacité du rendu sur l’appareil. Cette méthode prend en charge les chaînes ANSI et Unicode.
ms.assetid: 0e5380fc-7a01-4e09-9c18-22087be56780
title: ID3DX10Font ::P méthode reloadText (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Font.PreloadText
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: c7294fb7e86b3532960a34a15e1118dc33f748f2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104211781"
---
# <a name="id3dx10fontpreloadtext-method"></a><span data-ttu-id="c9b3b-104">ID3DX10Font ::P méthode reloadText</span><span class="sxs-lookup"><span data-stu-id="c9b3b-104">ID3DX10Font::PreloadText method</span></span>

<span data-ttu-id="c9b3b-105">Chargez le texte mis en forme dans la mémoire vidéo pour améliorer l’efficacité du rendu sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="c9b3b-105">Load formatted text into video memory to improve the efficiency of rendering to the device.</span></span> <span data-ttu-id="c9b3b-106">Cette méthode prend en charge les chaînes ANSI et Unicode.</span><span class="sxs-lookup"><span data-stu-id="c9b3b-106">This method supports ANSI and Unicode strings.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9b3b-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c9b3b-107">Syntax</span></span>


```C++
HRESULT PreloadText(
  [in] LPCSTR pString,
  [in] INT    Count
);
```



## <a name="parameters"></a><span data-ttu-id="c9b3b-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c9b3b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c9b3b-109">*pString* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c9b3b-109">*pString* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c9b3b-110">Type : **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c9b3b-110">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c9b3b-111">Pointeur vers une chaîne de caractères à charger dans la mémoire vidéo.</span><span class="sxs-lookup"><span data-stu-id="c9b3b-111">Pointer to a string of characters to be loaded into video memory.</span></span> <span data-ttu-id="c9b3b-112">Si les paramètres du compilateur requièrent Unicode, le type de données LPCTSTR est résolu en LPCWSTR ; dans le cas contraire, le type de données est résolu en LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="c9b3b-112">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR; otherwise, the data type resolves to LPCSTR.</span></span> <span data-ttu-id="c9b3b-113">Consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="c9b3b-113">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="c9b3b-114">*Nombre* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c9b3b-114">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c9b3b-115">Type : **[ **int**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c9b3b-115">Type: **[**INT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c9b3b-116">Nombre de caractères dans la chaîne de texte.</span><span class="sxs-lookup"><span data-stu-id="c9b3b-116">Number of characters in the text string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c9b3b-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c9b3b-117">Return value</span></span>

<span data-ttu-id="c9b3b-118">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c9b3b-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c9b3b-119">Si la méthode est réussie, la valeur de retour est S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="c9b3b-119">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="c9b3b-120">Si la méthode échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, D3DXERR \_ sera déplacé.</span><span class="sxs-lookup"><span data-stu-id="c9b3b-120">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="c9b3b-121">Notes</span><span class="sxs-lookup"><span data-stu-id="c9b3b-121">Remarks</span></span>

<span data-ttu-id="c9b3b-122">Le paramètre du compilateur détermine également la version de la fonction.</span><span class="sxs-lookup"><span data-stu-id="c9b3b-122">The compiler setting also determines the function version.</span></span> <span data-ttu-id="c9b3b-123">Si Unicode est défini, l’appel de fonction est résolu en PreloadTextW.</span><span class="sxs-lookup"><span data-stu-id="c9b3b-123">If Unicode is defined, the function call resolves to PreloadTextW.</span></span> <span data-ttu-id="c9b3b-124">Dans le cas contraire, l’appel de fonction est résolu en PreloadTextA, car les chaînes ANSI sont utilisées.</span><span class="sxs-lookup"><span data-stu-id="c9b3b-124">Otherwise, the function call resolves to PreloadTextA because ANSI strings are being used.</span></span>

<span data-ttu-id="c9b3b-125">Cette méthode génère des textures qui contiennent des glyphes qui représentent le texte d’entrée.</span><span class="sxs-lookup"><span data-stu-id="c9b3b-125">This method generates textures that contain glyphs that represent the input text.</span></span> <span data-ttu-id="c9b3b-126">Les glyphes sont dessinés sous la forme d’une série de triangles.</span><span class="sxs-lookup"><span data-stu-id="c9b3b-126">The glyphs are drawn as a series of triangles.</span></span>

<span data-ttu-id="c9b3b-127">Le texte ne sera pas rendu sur l’appareil ; ID3DX10Font ::D rawText doit encore être appelé pour restituer le texte.</span><span class="sxs-lookup"><span data-stu-id="c9b3b-127">Text will not be rendered to the device; ID3DX10Font::DrawText must still be called to render the text.</span></span> <span data-ttu-id="c9b3b-128">Toutefois, en préchargeant du texte dans la mémoire vidéo, ID3DX10Font ::D rawText utilisera beaucoup moins de ressources processeur.</span><span class="sxs-lookup"><span data-stu-id="c9b3b-128">However, by preloading text into video memory, ID3DX10Font::DrawText will use substantially fewer CPU resources.</span></span>

<span data-ttu-id="c9b3b-129">Cette méthode convertit en interne les caractères en glyphes à l’aide de la fonction GDI [GetCharacterPlacement](/previous-versions//ms534004(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="c9b3b-129">This method internally converts characters to glyphs using the GDI function [GetCharacterPlacement](/previous-versions//ms534004(v=vs.85)).</span></span>

## <a name="requirements"></a><span data-ttu-id="c9b3b-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c9b3b-130">Requirements</span></span>



| <span data-ttu-id="c9b3b-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c9b3b-131">Requirement</span></span> | <span data-ttu-id="c9b3b-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="c9b3b-132">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c9b3b-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="c9b3b-133">Header</span></span><br/>  | <dl> <span data-ttu-id="c9b3b-134"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="c9b3b-134"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="c9b3b-135">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="c9b3b-135">Library</span></span><br/> | <dl> <span data-ttu-id="c9b3b-136"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c9b3b-136"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c9b3b-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c9b3b-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9b3b-138">ID3DX10Font</span><span class="sxs-lookup"><span data-stu-id="c9b3b-138">ID3DX10Font</span></span>](id3dx10font.md)
</dt> <dt>

[<span data-ttu-id="c9b3b-139">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="c9b3b-139">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
