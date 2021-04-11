---
description: Charge le texte mis en forme dans la mémoire vidéo pour améliorer l’efficacité du rendu sur l’appareil. Cette méthode prend en charge les chaînes ANSI et Unicode.
ms.assetid: f2a4e9f5-87c5-46c0-965d-ce1535a6921d
title: ID3DXFont ::P méthode reloadText (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFont.PreloadText
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 958979e3008cf9ae0b79e2de3591635187df0f12
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104116286"
---
# <a name="id3dxfontpreloadtext-method"></a><span data-ttu-id="f653e-104">ID3DXFont ::P méthode reloadText</span><span class="sxs-lookup"><span data-stu-id="f653e-104">ID3DXFont::PreloadText method</span></span>

<span data-ttu-id="f653e-105">Charge le texte mis en forme dans la mémoire vidéo pour améliorer l’efficacité du rendu sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="f653e-105">Loads formatted text into video memory to improve the efficiency of rendering to the device.</span></span> <span data-ttu-id="f653e-106">Cette méthode prend en charge les chaînes ANSI et Unicode.</span><span class="sxs-lookup"><span data-stu-id="f653e-106">This method supports ANSI and Unicode strings.</span></span>

## <a name="syntax"></a><span data-ttu-id="f653e-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f653e-107">Syntax</span></span>


```C++
HRESULT PreloadText(
  [in] LPCTSTR *pString,
  [in] INT     Count
);
```



## <a name="parameters"></a><span data-ttu-id="f653e-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f653e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f653e-109">*pString* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f653e-109">*pString* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f653e-110">Type : **[ **LPCTSTR**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="f653e-110">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="f653e-111">Pointeur vers une chaîne de caractères à charger dans la mémoire vidéo.</span><span class="sxs-lookup"><span data-stu-id="f653e-111">Pointer to a string of characters to be loaded into video memory.</span></span> <span data-ttu-id="f653e-112">Si les paramètres du compilateur requièrent Unicode, le type de données LPCTSTR est résolu en LPCWSTR ; dans le cas contraire, le type de données est résolu en LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="f653e-112">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR; otherwise, the data type resolves to LPCSTR.</span></span> <span data-ttu-id="f653e-113">Consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="f653e-113">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="f653e-114">*Nombre* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f653e-114">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f653e-115">Type : **[ **int**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f653e-115">Type: **[**INT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f653e-116">Nombre de caractères dans la chaîne de texte.</span><span class="sxs-lookup"><span data-stu-id="f653e-116">Number of characters in the text string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f653e-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f653e-117">Return value</span></span>

<span data-ttu-id="f653e-118">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f653e-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f653e-119">Si la méthode est réussie, la valeur de retour est S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="f653e-119">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="f653e-120">Si la méthode échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, D3DXERR \_ sera déplacé.</span><span class="sxs-lookup"><span data-stu-id="f653e-120">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="f653e-121">Notes</span><span class="sxs-lookup"><span data-stu-id="f653e-121">Remarks</span></span>

<span data-ttu-id="f653e-122">Le paramètre du compilateur détermine également la version de la fonction.</span><span class="sxs-lookup"><span data-stu-id="f653e-122">The compiler setting also determines the function version.</span></span> <span data-ttu-id="f653e-123">Si Unicode est défini, l’appel de fonction est résolu en PreloadTextW.</span><span class="sxs-lookup"><span data-stu-id="f653e-123">If Unicode is defined, the function call resolves to PreloadTextW.</span></span> <span data-ttu-id="f653e-124">Dans le cas contraire, l’appel de fonction est résolu en PreloadTextA, car les chaînes ANSI sont utilisées.</span><span class="sxs-lookup"><span data-stu-id="f653e-124">Otherwise, the function call resolves to PreloadTextA because ANSI strings are being used.</span></span>

<span data-ttu-id="f653e-125">Cette méthode génère des textures qui contiennent des glyphes qui représentent le texte d’entrée.</span><span class="sxs-lookup"><span data-stu-id="f653e-125">This method generates textures that contain glyphs that represent the input text.</span></span> <span data-ttu-id="f653e-126">Les glyphes sont dessinés sous la forme d’une série de triangles.</span><span class="sxs-lookup"><span data-stu-id="f653e-126">The glyphs are drawn as a series of triangles.</span></span>

<span data-ttu-id="f653e-127">Le texte ne sera pas rendu sur l’appareil ; [**DrawText**](id3dxfont--drawtext.md) doit encore être appelé pour restituer le texte.</span><span class="sxs-lookup"><span data-stu-id="f653e-127">Text will not be rendered to the device; [**DrawText**](id3dxfont--drawtext.md) must still be called to render the text.</span></span> <span data-ttu-id="f653e-128">Toutefois, en préchargeant le texte dans la mémoire vidéo, **DrawText** utilise beaucoup moins de ressources processeur.</span><span class="sxs-lookup"><span data-stu-id="f653e-128">However, by preloading text into video memory, **DrawText** will use substantially fewer CPU resources.</span></span>

<span data-ttu-id="f653e-129">Cette méthode convertit en interne les caractères en glyphes à l’aide de la fonction GDI [**GetCharacterPlacement**](/windows/win32/api/wingdi/nf-wingdi-getcharacterplacementa).</span><span class="sxs-lookup"><span data-stu-id="f653e-129">This method internally converts characters to glyphs using the GDI function [**GetCharacterPlacement**](/windows/win32/api/wingdi/nf-wingdi-getcharacterplacementa).</span></span>

## <a name="requirements"></a><span data-ttu-id="f653e-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f653e-130">Requirements</span></span>



| <span data-ttu-id="f653e-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f653e-131">Requirement</span></span> | <span data-ttu-id="f653e-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="f653e-132">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f653e-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="f653e-133">Header</span></span><br/>  | <dl> <span data-ttu-id="f653e-134"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="f653e-134"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="f653e-135">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="f653e-135">Library</span></span><br/> | <dl> <span data-ttu-id="f653e-136"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f653e-136"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="f653e-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f653e-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f653e-138">ID3DXFont</span><span class="sxs-lookup"><span data-stu-id="f653e-138">ID3DXFont</span></span>](id3dxfont.md)
</dt> </dl>

 

 
