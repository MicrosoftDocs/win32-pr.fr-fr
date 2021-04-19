---
description: Crée un maillage contenant le texte spécifié, à l’aide de la police associée au contexte de périphérique.
ms.assetid: 1c8b0dc6-51b8-45bf-b4c0-b67e3d128097
title: D3DXCreateText, fonction (D3dx9shape. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateText
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 4f6202a534dde727e21b6513ad30077f2e3b3e52
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106538336"
---
# <a name="d3dxcreatetext-function"></a><span data-ttu-id="42e90-103">D3DXCreateText fonction)</span><span class="sxs-lookup"><span data-stu-id="42e90-103">D3DXCreateText function</span></span>

<span data-ttu-id="42e90-104">Crée un maillage contenant le texte spécifié, à l’aide de la police associée au contexte de périphérique.</span><span class="sxs-lookup"><span data-stu-id="42e90-104">Creates a mesh containing the specified text, using the font associated with the device context.</span></span>

## <a name="syntax"></a><span data-ttu-id="42e90-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="42e90-105">Syntax</span></span>


```C++
HRESULT D3DXCreateText(
  _In_  LPDIRECT3DDEVICE9   pDevice,
  _In_  HDC                 hDC,
  _In_  LPCTSTR             pText,
  _In_  FLOAT               Deviation,
  _In_  FLOAT               Extrusion,
  _Out_ LPD3DXMESH          *ppMesh,
  _Out_ LPD3DXBUFFER        *ppAdjacency,
  _Out_ LPGLYPHMETRICSFLOAT pGlyphMetrics
);
```



## <a name="parameters"></a><span data-ttu-id="42e90-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="42e90-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="42e90-107">*pDevice* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="42e90-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="42e90-108">Type : **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="42e90-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="42e90-109">Pointeur vers l’appareil qui a créé le maillage.</span><span class="sxs-lookup"><span data-stu-id="42e90-109">Pointer to the device that created the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="42e90-110">*HDC* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="42e90-110">*hDC* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="42e90-111">Type : **HDC**</span><span class="sxs-lookup"><span data-stu-id="42e90-111">Type: **HDC**</span></span>

<span data-ttu-id="42e90-112">Contexte de périphérique, contenant la police de sortie.</span><span class="sxs-lookup"><span data-stu-id="42e90-112">Device context, containing the font for output.</span></span> <span data-ttu-id="42e90-113">La police sélectionnée par le contexte de périphérique doit être une police TrueType.</span><span class="sxs-lookup"><span data-stu-id="42e90-113">The font selected by the device context must be a TrueType font.</span></span>

</dd> <dt>

<span data-ttu-id="42e90-114">*pText* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="42e90-114">*pText* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="42e90-115">Type : **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="42e90-115">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="42e90-116">Pointeur vers une chaîne qui spécifie le texte à générer.</span><span class="sxs-lookup"><span data-stu-id="42e90-116">Pointer to a string that specifies the text to generate.</span></span> <span data-ttu-id="42e90-117">Si les paramètres du compilateur requièrent Unicode, le type de données LPCTSTR est résolu en LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="42e90-117">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="42e90-118">Dans le cas contraire, le type de données String est résolu en LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="42e90-118">Otherwise, the string data type resolves to LPCSTR.</span></span> <span data-ttu-id="42e90-119">Consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="42e90-119">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="42e90-120">*Écart* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="42e90-120">*Deviation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="42e90-121">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="42e90-121">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="42e90-122">Écart de corde maximal à partir des contours de police TrueType.</span><span class="sxs-lookup"><span data-stu-id="42e90-122">Maximum chordal deviation from TrueType font outlines.</span></span>

</dd> <dt>

<span data-ttu-id="42e90-123">*Extrusion* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="42e90-123">*Extrusion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="42e90-124">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="42e90-124">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="42e90-125">Quantité d’extrusion du texte dans l’axe z négatif.</span><span class="sxs-lookup"><span data-stu-id="42e90-125">Amount to extrude text in the negative z-direction.</span></span>

</dd> <dt>

<span data-ttu-id="42e90-126">*ppMesh* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="42e90-126">*ppMesh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="42e90-127">Type : **[ **LPD3DXMESH**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="42e90-127">Type: **[**LPD3DXMESH**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="42e90-128">Pointeur vers le maillage retourné.</span><span class="sxs-lookup"><span data-stu-id="42e90-128">Pointer to the returned mesh.</span></span>

</dd> <dt>

<span data-ttu-id="42e90-129">*ppAdjacency* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="42e90-129">*ppAdjacency* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="42e90-130">Type : **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="42e90-130">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="42e90-131">Pointeur vers une mémoire tampon qui contient des informations d’adjacence.</span><span class="sxs-lookup"><span data-stu-id="42e90-131">Pointer to a buffer containing adjacency information.</span></span> <span data-ttu-id="42e90-132">Peut avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="42e90-132">May be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="42e90-133">*pGlyphMetrics* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="42e90-133">*pGlyphMetrics* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="42e90-134">Type : **[ **LPGLYPHMETRICSFLOAT**](/windows/win32/api/wingdi/ns-wingdi-glyphmetricsfloat)**</span><span class="sxs-lookup"><span data-stu-id="42e90-134">Type: **[**LPGLYPHMETRICSFLOAT**](/windows/win32/api/wingdi/ns-wingdi-glyphmetricsfloat)**</span></span>

<span data-ttu-id="42e90-135">Pointeur vers un tableau de structures [**GLYPHMETRICSFLOAT**](/windows/win32/api/wingdi/ns-wingdi-glyphmetricsfloat) qui contiennent les données de métrique de glyphe.</span><span class="sxs-lookup"><span data-stu-id="42e90-135">Pointer to an array of [**GLYPHMETRICSFLOAT**](/windows/win32/api/wingdi/ns-wingdi-glyphmetricsfloat) structures that contain the glyph metric data.</span></span> <span data-ttu-id="42e90-136">Chaque élément contient des informations sur la position et l’orientation du glyphe correspondant dans la chaîne.</span><span class="sxs-lookup"><span data-stu-id="42e90-136">Each element contains information about the position and orientation of the corresponding glyph in the string.</span></span> <span data-ttu-id="42e90-137">Le nombre d’éléments dans le tableau doit être égal au nombre de caractères de la chaîne.</span><span class="sxs-lookup"><span data-stu-id="42e90-137">The number of elements in the array should be equal to the number of characters in the string.</span></span> <span data-ttu-id="42e90-138">Notez que l’origine dans chaque structure n’est pas relative à la chaîne entière, mais qu’elle est relative à cette cellule de caractère.</span><span class="sxs-lookup"><span data-stu-id="42e90-138">Note that the origin in each structure is not relative to the entire string, but rather is relative to that character cell.</span></span> <span data-ttu-id="42e90-139">Pour calculer l’intégralité du cadre englobant, ajoutez l’incrément pour chaque glyphe tout en parcourant la chaîne.</span><span class="sxs-lookup"><span data-stu-id="42e90-139">To compute the entire bounding box, add the increment for each glyph while traversing the string.</span></span> <span data-ttu-id="42e90-140">Si vous n’êtes pas concerné par les tailles de glyphe, définissez ce paramètre sur la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="42e90-140">If you are not concerned with the glyph sizes, set this parameter to **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="42e90-141">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="42e90-141">Return value</span></span>

<span data-ttu-id="42e90-142">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="42e90-142">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="42e90-143">Si la fonction est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="42e90-143">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="42e90-144">Si la fonction échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, D3DXERR \_ sera déplacé, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="42e90-144">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="42e90-145">Notes</span><span class="sxs-lookup"><span data-stu-id="42e90-145">Remarks</span></span>

<span data-ttu-id="42e90-146">Le paramètre du compilateur détermine également la version de la fonction.</span><span class="sxs-lookup"><span data-stu-id="42e90-146">The compiler setting also determines the function version.</span></span> <span data-ttu-id="42e90-147">Si Unicode est défini, l’appel de fonction est résolu en D3DXCreateTextW.</span><span class="sxs-lookup"><span data-stu-id="42e90-147">If Unicode is defined, the function call resolves to D3DXCreateTextW.</span></span> <span data-ttu-id="42e90-148">Dans le cas contraire, l’appel de fonction est résolu en D3DXCreateTextA, car les chaînes ANSI sont utilisées.</span><span class="sxs-lookup"><span data-stu-id="42e90-148">Otherwise, the function call resolves to D3DXCreateTextA because ANSI strings are being used.</span></span>

<span data-ttu-id="42e90-149">Cette fonction crée une maille avec l' \_ option de création managée D3DXMESH et [D3DFVF \_ xyz \| D3DFVF \_ ](d3dfvf.md) le format de vertex flexible normal.</span><span class="sxs-lookup"><span data-stu-id="42e90-149">This function creates a mesh with the D3DXMESH\_MANAGED creation option and [D3DFVF\_XYZ \| D3DFVF\_NORMAL](d3dfvf.md) flexible vertex format (FVF).</span></span>

## <a name="requirements"></a><span data-ttu-id="42e90-150">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="42e90-150">Requirements</span></span>



| <span data-ttu-id="42e90-151">Condition requise</span><span class="sxs-lookup"><span data-stu-id="42e90-151">Requirement</span></span> | <span data-ttu-id="42e90-152">Valeur</span><span class="sxs-lookup"><span data-stu-id="42e90-152">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="42e90-153">En-tête</span><span class="sxs-lookup"><span data-stu-id="42e90-153">Header</span></span><br/>  | <dl> <span data-ttu-id="42e90-154"><dt>D3dx9shape. h</dt></span><span class="sxs-lookup"><span data-stu-id="42e90-154"><dt>D3dx9shape.h</dt></span></span> </dl> |
| <span data-ttu-id="42e90-155">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="42e90-155">Library</span></span><br/> | <dl> <span data-ttu-id="42e90-156"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="42e90-156"><dt>D3dx9.lib</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="42e90-157">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="42e90-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42e90-158">Fonctions de dessin de forme</span><span class="sxs-lookup"><span data-stu-id="42e90-158">Shape Drawing Functions</span></span>](dx9-graphics-reference-d3dx-functions-shape.md)
</dt> </dl>

 

 
