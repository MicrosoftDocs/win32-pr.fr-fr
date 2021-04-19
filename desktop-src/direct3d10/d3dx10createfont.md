---
description: Crée un objet de police pour un appareil et une police. Remarque au lieu d’utiliser cette fonction, nous vous recommandons d’utiliser DirectWrite et la bibliothèque DirectXTK, SpriteFont Class.
ms.assetid: a0dd02f1-c512-46d3-9e83-a785ac3ad7ee
title: D3DX10CreateFont, fonction (D3DX10Core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateFont
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: d6e5966e50c9c997085d35854868a2a7dd0455c7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106538343"
---
# <a name="d3dx10createfont-function"></a><span data-ttu-id="bf2fc-103">D3DX10CreateFont fonction)</span><span class="sxs-lookup"><span data-stu-id="bf2fc-103">D3DX10CreateFont function</span></span>

<span data-ttu-id="bf2fc-104">Crée un objet de police pour un appareil et une police.</span><span class="sxs-lookup"><span data-stu-id="bf2fc-104">Creates a font object for a device and font.</span></span>

> [!Note]  
> <span data-ttu-id="bf2fc-105">Au lieu d’utiliser cette fonction, nous vous recommandons d’utiliser [DirectWrite](../directwrite/direct-write-portal.md) et la bibliothèque [DirectXTK](https://github.com/Microsoft/DirectXTK) , la classe **SpriteFont** .</span><span class="sxs-lookup"><span data-stu-id="bf2fc-105">Instead of using this function, we recommend that you use [DirectWrite](../directwrite/direct-write-portal.md) and the [DirectXTK](https://github.com/Microsoft/DirectXTK) library, **SpriteFont** class.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="bf2fc-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bf2fc-106">Syntax</span></span>


```C++
HRESULT D3DX10CreateFont(
  _In_  ID3D10Device *pDevice,
  _In_  INT          Height,
  _In_  UINT         Width,
  _In_  UINT         Weight,
  _In_  UINT         MipLevels,
  _In_  BOOL         Italic,
  _In_  UINT         CharSet,
  _In_  UINT         OutputPrecision,
  _In_  UINT         Quality,
  _In_  UINT         PitchAndFamily,
  _In_  LPCTSTR      pFaceName,
  _Out_ LPD3DX10FONT *ppFont
);
```



## <a name="parameters"></a><span data-ttu-id="bf2fc-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bf2fc-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bf2fc-108">*pDevice* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="bf2fc-108">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bf2fc-109">Type : **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***</span><span class="sxs-lookup"><span data-stu-id="bf2fc-109">Type: **[**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***</span></span>

<span data-ttu-id="bf2fc-110">Pointeur vers une interface ID3D10Device, l’appareil à associer à l’objet font.</span><span class="sxs-lookup"><span data-stu-id="bf2fc-110">Pointer to an ID3D10Device interface, the device to be associated with the font object.</span></span>

</dd> <dt>

<span data-ttu-id="bf2fc-111">*Hauteur* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="bf2fc-111">*Height* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bf2fc-112">Type : **[ **int**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="bf2fc-112">Type: **[**INT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="bf2fc-113">Hauteur des caractères dans les unités logiques.</span><span class="sxs-lookup"><span data-stu-id="bf2fc-113">The height of the characters in logical units.</span></span>

</dd> <dt>

<span data-ttu-id="bf2fc-114">*Largeur* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="bf2fc-114">*Width* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bf2fc-115">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="bf2fc-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="bf2fc-116">Largeur des caractères en unités logiques.</span><span class="sxs-lookup"><span data-stu-id="bf2fc-116">The width of the characters in logical units.</span></span>

</dd> <dt>

<span data-ttu-id="bf2fc-117">*Poids* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="bf2fc-117">*Weight* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bf2fc-118">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="bf2fc-118">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="bf2fc-119">Épaisseur du caractère.</span><span class="sxs-lookup"><span data-stu-id="bf2fc-119">Typeface weight.</span></span> <span data-ttu-id="bf2fc-120">Un exemple est le gras.</span><span class="sxs-lookup"><span data-stu-id="bf2fc-120">One example is bold.</span></span>

</dd> <dt>

<span data-ttu-id="bf2fc-121">*Miplevels a* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="bf2fc-121">*MipLevels* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bf2fc-122">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="bf2fc-122">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="bf2fc-123">Nombre de niveaux de mipmap.</span><span class="sxs-lookup"><span data-stu-id="bf2fc-123">The number of mipmap levels.</span></span>

</dd> <dt>

<span data-ttu-id="bf2fc-124">*Italique* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="bf2fc-124">*Italic* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bf2fc-125">Type : **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="bf2fc-125">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="bf2fc-126">True pour la police en italique ; sinon, false.</span><span class="sxs-lookup"><span data-stu-id="bf2fc-126">True for italic font, false otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="bf2fc-127">*Jeu* \[ de caractères dans\]</span><span class="sxs-lookup"><span data-stu-id="bf2fc-127">*CharSet* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bf2fc-128">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="bf2fc-128">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="bf2fc-129">Jeu de caractères de la police.</span><span class="sxs-lookup"><span data-stu-id="bf2fc-129">The character set of the font.</span></span>

</dd> <dt>

<span data-ttu-id="bf2fc-130">*OutputPrecision* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="bf2fc-130">*OutputPrecision* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bf2fc-131">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="bf2fc-131">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="bf2fc-132">Spécifie comment Windows doit tenter de faire correspondre les tailles de police et les caractéristiques souhaitées avec les polices réelles.</span><span class="sxs-lookup"><span data-stu-id="bf2fc-132">Specifies how Windows should attempt to match the desired font sizes and characteristics with actual fonts.</span></span> <span data-ttu-id="bf2fc-133">Utilisez \_ TT \_ uniquement \_ precis par exemple, pour vous assurer que vous recevez toujours une police TrueType.</span><span class="sxs-lookup"><span data-stu-id="bf2fc-133">Use OUT\_TT\_ONLY\_PRECIS for instance, to ensure that you always get a TrueType font.</span></span>

</dd> <dt>

<span data-ttu-id="bf2fc-134">*Qualité* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="bf2fc-134">*Quality* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bf2fc-135">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="bf2fc-135">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="bf2fc-136">Spécifie comment Windows doit correspondre à la police souhaitée avec une police réelle.</span><span class="sxs-lookup"><span data-stu-id="bf2fc-136">Specifies how Windows should match the desired font with a real font.</span></span> <span data-ttu-id="bf2fc-137">Elle s’applique uniquement aux polices Raster et ne doit pas affecter les polices TrueType.</span><span class="sxs-lookup"><span data-stu-id="bf2fc-137">It applies to raster fonts only and should not affect TrueType fonts.</span></span>

</dd> <dt>

<span data-ttu-id="bf2fc-138">*PitchAndFamily* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="bf2fc-138">*PitchAndFamily* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bf2fc-139">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="bf2fc-139">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="bf2fc-140">Index de la famille et de la hauteur.</span><span class="sxs-lookup"><span data-stu-id="bf2fc-140">Pitch and family index.</span></span>

</dd> <dt>

<span data-ttu-id="bf2fc-141">*pFaceName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="bf2fc-141">*pFaceName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bf2fc-142">Type : **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="bf2fc-142">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="bf2fc-143">Chaîne contenant le nom de la police.</span><span class="sxs-lookup"><span data-stu-id="bf2fc-143">String containing the typeface name.</span></span> <span data-ttu-id="bf2fc-144">Si les paramètres du compilateur requièrent Unicode, le type de données LPCTSTR est résolu en LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="bf2fc-144">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="bf2fc-145">Dans le cas contraire, le type de données est résolu en LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="bf2fc-145">Otherwise, the data type resolves to LPCSTR.</span></span> <span data-ttu-id="bf2fc-146">Consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="bf2fc-146">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="bf2fc-147">*ppFont* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="bf2fc-147">*ppFont* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bf2fc-148">Type : **[ **LPD3DX10FONT**](id3dx10font.md)\***</span><span class="sxs-lookup"><span data-stu-id="bf2fc-148">Type: **[**LPD3DX10FONT**](id3dx10font.md)\***</span></span>

<span data-ttu-id="bf2fc-149">Retourne un pointeur vers une interface ID3DX10Font représentant l’objet de police créé.</span><span class="sxs-lookup"><span data-stu-id="bf2fc-149">Returns a pointer to an ID3DX10Font interface, representing the created font object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bf2fc-150">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="bf2fc-150">Return value</span></span>

<span data-ttu-id="bf2fc-151">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="bf2fc-151">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="bf2fc-152">Si la fonction est réussie, la valeur de retour est S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="bf2fc-152">If the function succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="bf2fc-153">Si la fonction échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, D3DXERR \_ sera déplacé, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="bf2fc-153">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="bf2fc-154">Notes</span><span class="sxs-lookup"><span data-stu-id="bf2fc-154">Remarks</span></span>

<span data-ttu-id="bf2fc-155">Le paramètre du compilateur détermine également la version de la fonction.</span><span class="sxs-lookup"><span data-stu-id="bf2fc-155">The compiler setting also determines the function version.</span></span> <span data-ttu-id="bf2fc-156">Si Unicode est défini, l’appel de fonction est résolu en D3DXCreateFontW.</span><span class="sxs-lookup"><span data-stu-id="bf2fc-156">If Unicode is defined, the function call resolves to D3DXCreateFontW.</span></span> <span data-ttu-id="bf2fc-157">Dans le cas contraire, l’appel de fonction est résolu en D3DXCreateFontA, car les chaînes ANSI sont utilisées.</span><span class="sxs-lookup"><span data-stu-id="bf2fc-157">Otherwise, the function call resolves to D3DXCreateFontA because ANSI strings are being used.</span></span>

<span data-ttu-id="bf2fc-158">Si vous souhaitez plus d’informations sur les paramètres de police, consultez [la police logique](/previous-versions//ms533985(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="bf2fc-158">If you want more information about font parameters, see [The Logical Font](/previous-versions//ms533985(v=vs.85)).</span></span>

## <a name="requirements"></a><span data-ttu-id="bf2fc-159">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bf2fc-159">Requirements</span></span>



| <span data-ttu-id="bf2fc-160">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bf2fc-160">Requirement</span></span> | <span data-ttu-id="bf2fc-161">Valeur</span><span class="sxs-lookup"><span data-stu-id="bf2fc-161">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bf2fc-162">En-tête</span><span class="sxs-lookup"><span data-stu-id="bf2fc-162">Header</span></span><br/>  | <dl> <span data-ttu-id="bf2fc-163"><dt>D3DX10Core. h</dt></span><span class="sxs-lookup"><span data-stu-id="bf2fc-163"><dt>D3DX10Core.h</dt></span></span> </dl> |
| <span data-ttu-id="bf2fc-164">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="bf2fc-164">Library</span></span><br/> | <dl> <span data-ttu-id="bf2fc-165"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bf2fc-165"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="bf2fc-166">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bf2fc-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf2fc-167">Fonctions usage général</span><span class="sxs-lookup"><span data-stu-id="bf2fc-167">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
