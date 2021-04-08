---
description: Crée un objet de police pour un appareil et une police.
ms.assetid: 3e65dfdc-9608-420c-9672-c38289d13ab1
title: D3DXCreateFont, fonction (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateFont
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 488a400928ecc270612a307fbede971e02b43b25
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762193"
---
# <a name="d3dxcreatefont-function"></a><span data-ttu-id="fefbf-103">D3DXCreateFont fonction)</span><span class="sxs-lookup"><span data-stu-id="fefbf-103">D3DXCreateFont function</span></span>

<span data-ttu-id="fefbf-104">Crée un objet de police pour un appareil et une police.</span><span class="sxs-lookup"><span data-stu-id="fefbf-104">Creates a font object for a device and font.</span></span>

## <a name="syntax"></a><span data-ttu-id="fefbf-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fefbf-105">Syntax</span></span>


```C++
HRESULT D3DXCreateFont(
  _In_  LPDIRECT3DDEVICE9 pDevice,
  _In_  INT               Height,
  _In_  UINT              Width,
  _In_  UINT              Weight,
  _In_  UINT              MipLevels,
  _In_  BOOL              Italic,
  _In_  DWORD             CharSet,
  _In_  DWORD             OutputPrecision,
  _In_  DWORD             Quality,
  _In_  DWORD             PitchAndFamily,
  _In_  LPCTSTR           pFacename,
  _Out_ LPD3DXFONT        *ppFont
);
```



## <a name="parameters"></a><span data-ttu-id="fefbf-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fefbf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fefbf-107">*pDevice* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fefbf-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fefbf-108">Type : **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="fefbf-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="fefbf-109">Pointeur vers une interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , l’appareil à associer à l’objet font.</span><span class="sxs-lookup"><span data-stu-id="fefbf-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, the device to be associated with the font object.</span></span>

</dd> <dt>

<span data-ttu-id="fefbf-110">*Hauteur* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fefbf-110">*Height* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fefbf-111">Type : **[ **int**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fefbf-111">Type: **[**INT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fefbf-112">Hauteur des caractères dans les unités logiques.</span><span class="sxs-lookup"><span data-stu-id="fefbf-112">The height of the characters in logical units.</span></span>

</dd> <dt>

<span data-ttu-id="fefbf-113">*Largeur* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fefbf-113">*Width* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fefbf-114">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fefbf-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fefbf-115">Largeur des caractères en unités logiques.</span><span class="sxs-lookup"><span data-stu-id="fefbf-115">The width of the characters in logical units.</span></span>

</dd> <dt>

<span data-ttu-id="fefbf-116">*Poids* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fefbf-116">*Weight* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fefbf-117">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fefbf-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fefbf-118">Épaisseur du caractère.</span><span class="sxs-lookup"><span data-stu-id="fefbf-118">Typeface weight.</span></span> <span data-ttu-id="fefbf-119">Un exemple est le gras.</span><span class="sxs-lookup"><span data-stu-id="fefbf-119">One example is bold.</span></span>

</dd> <dt>

<span data-ttu-id="fefbf-120">*Miplevels a* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fefbf-120">*MipLevels* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fefbf-121">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fefbf-121">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fefbf-122">Nombre de niveaux de mipmap.</span><span class="sxs-lookup"><span data-stu-id="fefbf-122">The number of mipmap levels.</span></span>

</dd> <dt>

<span data-ttu-id="fefbf-123">*Italique* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fefbf-123">*Italic* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fefbf-124">Type : **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fefbf-124">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fefbf-125">True pour la police en italique ; sinon, false.</span><span class="sxs-lookup"><span data-stu-id="fefbf-125">True for italic font, false otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="fefbf-126">*Jeu* \[ de caractères dans\]</span><span class="sxs-lookup"><span data-stu-id="fefbf-126">*CharSet* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fefbf-127">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fefbf-127">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fefbf-128">Jeu de caractères de la police.</span><span class="sxs-lookup"><span data-stu-id="fefbf-128">The character set of the font.</span></span>

</dd> <dt>

<span data-ttu-id="fefbf-129">*OutputPrecision* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fefbf-129">*OutputPrecision* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fefbf-130">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fefbf-130">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fefbf-131">Spécifie comment Windows doit tenter de faire correspondre les tailles de police et les caractéristiques souhaitées avec les polices réelles.</span><span class="sxs-lookup"><span data-stu-id="fefbf-131">Specifies how Windows should attempt to match the desired font sizes and characteristics with actual fonts.</span></span> <span data-ttu-id="fefbf-132">Utilisez \_ TT \_ uniquement \_ precis par exemple, pour vous assurer que vous recevez toujours une police TrueType.</span><span class="sxs-lookup"><span data-stu-id="fefbf-132">Use OUT\_TT\_ONLY\_PRECIS for instance, to ensure that you always get a TrueType font.</span></span>

</dd> <dt>

<span data-ttu-id="fefbf-133">*Qualité* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fefbf-133">*Quality* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fefbf-134">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fefbf-134">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fefbf-135">Spécifie comment Windows doit correspondre à la police souhaitée avec une police réelle.</span><span class="sxs-lookup"><span data-stu-id="fefbf-135">Specifies how Windows should match the desired font with a real font.</span></span> <span data-ttu-id="fefbf-136">Elle s’applique uniquement aux polices Raster et ne doit pas affecter les polices TrueType.</span><span class="sxs-lookup"><span data-stu-id="fefbf-136">It applies to raster fonts only and should not affect TrueType fonts.</span></span>

</dd> <dt>

<span data-ttu-id="fefbf-137">*PitchAndFamily* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fefbf-137">*PitchAndFamily* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fefbf-138">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fefbf-138">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fefbf-139">Index de la famille et de la hauteur.</span><span class="sxs-lookup"><span data-stu-id="fefbf-139">Pitch and family index.</span></span>

</dd> <dt>

<span data-ttu-id="fefbf-140">*pFacename* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fefbf-140">*pFacename* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fefbf-141">Type : **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fefbf-141">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fefbf-142">Chaîne contenant le nom de la police.</span><span class="sxs-lookup"><span data-stu-id="fefbf-142">String containing the typeface name.</span></span> <span data-ttu-id="fefbf-143">Si les paramètres du compilateur requièrent Unicode, le type de données LPCTSTR est résolu en LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="fefbf-143">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="fefbf-144">Dans le cas contraire, le type de données String est résolu en LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="fefbf-144">Otherwise, the string data type resolves to LPCSTR.</span></span> <span data-ttu-id="fefbf-145">Consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="fefbf-145">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="fefbf-146">*ppFont* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="fefbf-146">*ppFont* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fefbf-147">Type : **[ **LPD3DXFONT**](id3dxfont.md)\***</span><span class="sxs-lookup"><span data-stu-id="fefbf-147">Type: **[**LPD3DXFONT**](id3dxfont.md)\***</span></span>

<span data-ttu-id="fefbf-148">Retourne un pointeur vers une interface [**ID3DXFont**](id3dxfont.md) représentant l’objet de police créé.</span><span class="sxs-lookup"><span data-stu-id="fefbf-148">Returns a pointer to an [**ID3DXFont**](id3dxfont.md) interface, representing the created font object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fefbf-149">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="fefbf-149">Return value</span></span>

<span data-ttu-id="fefbf-150">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="fefbf-150">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="fefbf-151">Si la fonction est réussie, la valeur de retour est S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="fefbf-151">If the function succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="fefbf-152">Si la fonction échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, D3DXERR \_ sera déplacé, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="fefbf-152">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="fefbf-153">Notes</span><span class="sxs-lookup"><span data-stu-id="fefbf-153">Remarks</span></span>

<span data-ttu-id="fefbf-154">La création d’un objet ID3DXFont nécessite que l’appareil prenne en charge la couleur 32 bits.</span><span class="sxs-lookup"><span data-stu-id="fefbf-154">The creation of an ID3DXFont object requires that the device supports 32-bit color.</span></span>

<span data-ttu-id="fefbf-155">Le paramètre du compilateur détermine également la version de la fonction.</span><span class="sxs-lookup"><span data-stu-id="fefbf-155">The compiler setting also determines the function version.</span></span> <span data-ttu-id="fefbf-156">Si Unicode est défini, l’appel de fonction est résolu en D3DXCreateFontW.</span><span class="sxs-lookup"><span data-stu-id="fefbf-156">If Unicode is defined, the function call resolves to D3DXCreateFontW.</span></span> <span data-ttu-id="fefbf-157">Dans le cas contraire, l’appel de fonction est résolu en D3DXCreateFontA, car les chaînes ANSI sont utilisées.</span><span class="sxs-lookup"><span data-stu-id="fefbf-157">Otherwise, the function call resolves to D3DXCreateFontA because ANSI strings are being used.</span></span>

<span data-ttu-id="fefbf-158">Si vous souhaitez plus d’informations sur les paramètres de police, consultez [la police logique](../gdi/creating-a-logical-font.md).</span><span class="sxs-lookup"><span data-stu-id="fefbf-158">If you want more information about font parameters, see [The Logical Font](../gdi/creating-a-logical-font.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="fefbf-159">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fefbf-159">Requirements</span></span>



| <span data-ttu-id="fefbf-160">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fefbf-160">Requirement</span></span> | <span data-ttu-id="fefbf-161">Valeur</span><span class="sxs-lookup"><span data-stu-id="fefbf-161">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fefbf-162">En-tête</span><span class="sxs-lookup"><span data-stu-id="fefbf-162">Header</span></span><br/>  | <dl> <span data-ttu-id="fefbf-163"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="fefbf-163"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="fefbf-164">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="fefbf-164">Library</span></span><br/> | <dl> <span data-ttu-id="fefbf-165"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fefbf-165"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="fefbf-166">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fefbf-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fefbf-167">Fonctions usage général</span><span class="sxs-lookup"><span data-stu-id="fefbf-167">General Purpose Functions</span></span>](dx9-graphics-reference-d3dx-functions-general-purpose.md)
</dt> </dl>

 

 
