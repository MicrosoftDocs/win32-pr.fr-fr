---
description: Définit les attributs d’une police.
ms.assetid: 6f456f26-3410-4205-a013-e3c12bf0feb1
title: Structure D3DXFONT_DESC (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFONT_DESC
api_type:
- HeaderDef
api_location:
- d3dx9core.h
ms.openlocfilehash: d7c142787e4e4fac5be53763a3c19fd86a27efd9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106527105"
---
# <a name="d3dxfont_desc-structure"></a><span data-ttu-id="a678d-103">D3DXFONT \_ desc, structure</span><span class="sxs-lookup"><span data-stu-id="a678d-103">D3DXFONT\_DESC structure</span></span>

<span data-ttu-id="a678d-104">Définit les attributs d’une police.</span><span class="sxs-lookup"><span data-stu-id="a678d-104">Defines the attributes of a font.</span></span>

## <a name="syntax"></a><span data-ttu-id="a678d-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a678d-105">Syntax</span></span>


```C++
typedef struct D3DXFONT_DESC {
  INT   Height;
  UINT  Width;
  UINT  Weight;
  UINT  MipLevels;
  BOOL  Italic;
  BYTE  CharSet;
  BYTE  OutputPrecision;
  BYTE  Quality;
  BYTE  PitchAndFamily;
  TCHAR FaceName;
} D3DXFONT_DESC, *LPD3DXFONT_DESC;
```



## <a name="members"></a><span data-ttu-id="a678d-106">Membres</span><span class="sxs-lookup"><span data-stu-id="a678d-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="a678d-107">**Height**</span><span class="sxs-lookup"><span data-stu-id="a678d-107">**Height**</span></span>
</dt> <dd>

<span data-ttu-id="a678d-108">Type : **[ **int**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a678d-108">Type: **[**INT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="a678d-109">Hauteur, en unités logiques, de la cellule de caractère ou du caractère de la police.</span><span class="sxs-lookup"><span data-stu-id="a678d-109">Height, in logical units, of the font's character cell or character.</span></span>

</dd> <dt>

<span data-ttu-id="a678d-110">**Width**</span><span class="sxs-lookup"><span data-stu-id="a678d-110">**Width**</span></span>
</dt> <dd>

<span data-ttu-id="a678d-111">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a678d-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="a678d-112">Largeur, en unités logiques, des caractères de la police.</span><span class="sxs-lookup"><span data-stu-id="a678d-112">Width, in logical units, of characters in the font.</span></span>

</dd> <dt>

<span data-ttu-id="a678d-113">**Poids**</span><span class="sxs-lookup"><span data-stu-id="a678d-113">**Weight**</span></span>
</dt> <dd>

<span data-ttu-id="a678d-114">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a678d-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="a678d-115">Poids de la police dans la plage comprise entre 0 et 1000.</span><span class="sxs-lookup"><span data-stu-id="a678d-115">Weight of the font in the range from 0 through 1000.</span></span>

</dd> <dt>

<span data-ttu-id="a678d-116">**Miplevels a**</span><span class="sxs-lookup"><span data-stu-id="a678d-116">**MipLevels**</span></span>
</dt> <dd>

<span data-ttu-id="a678d-117">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a678d-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="a678d-118">Nombre de niveaux MIP demandés.</span><span class="sxs-lookup"><span data-stu-id="a678d-118">Number of mip levels requested.</span></span> <span data-ttu-id="a678d-119">Si cette valeur est égale à zéro ou à D3DX \_ default, une chaîne mipmap complète est créée.</span><span class="sxs-lookup"><span data-stu-id="a678d-119">If this value is zero or D3DX\_DEFAULT, a complete mipmap chain is created.</span></span> <span data-ttu-id="a678d-120">Si la valeur est 1, l’espace de texture est mappé de manière identique à l’espace à l’écran.</span><span class="sxs-lookup"><span data-stu-id="a678d-120">If the value is 1, the texture space is mapped identically to the screen space.</span></span>

</dd> <dt>

<span data-ttu-id="a678d-121">**Italique**</span><span class="sxs-lookup"><span data-stu-id="a678d-121">**Italic**</span></span>
</dt> <dd>

<span data-ttu-id="a678d-122">Type : **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a678d-122">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="a678d-123">Affectez la valeur **true** à une police en italique.</span><span class="sxs-lookup"><span data-stu-id="a678d-123">Set to **TRUE** for an Italic font.</span></span>

</dd> <dt>

<span data-ttu-id="a678d-124">**CharSet**</span><span class="sxs-lookup"><span data-stu-id="a678d-124">**CharSet**</span></span>
</dt> <dd>

<span data-ttu-id="a678d-125">Type : **[ **Byte**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a678d-125">Type: **[**BYTE**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="a678d-126">Jeu de caractères.</span><span class="sxs-lookup"><span data-stu-id="a678d-126">Character set.</span></span>

</dd> <dt>

<span data-ttu-id="a678d-127">**OutputPrecision**</span><span class="sxs-lookup"><span data-stu-id="a678d-127">**OutputPrecision**</span></span>
</dt> <dd>

<span data-ttu-id="a678d-128">Type : **[ **Byte**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a678d-128">Type: **[**BYTE**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="a678d-129">Précision de sortie.</span><span class="sxs-lookup"><span data-stu-id="a678d-129">Output precision.</span></span> <span data-ttu-id="a678d-130">La précision de sortie définit la précision selon laquelle la sortie doit correspondre à la hauteur de police, à la largeur, à l’orientation des caractères, à l’échappement, au tangage et au type de police demandés.</span><span class="sxs-lookup"><span data-stu-id="a678d-130">The output precision defines how closely the output must match the requested font height, width, character orientation, escapement, pitch, and font type.</span></span>

</dd> <dt>

<span data-ttu-id="a678d-131">**Qualité**</span><span class="sxs-lookup"><span data-stu-id="a678d-131">**Quality**</span></span>
</dt> <dd>

<span data-ttu-id="a678d-132">Type : **[ **Byte**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a678d-132">Type: **[**BYTE**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="a678d-133">Qualité de sortie.</span><span class="sxs-lookup"><span data-stu-id="a678d-133">Output quality.</span></span>

</dd> <dt>

<span data-ttu-id="a678d-134">**PitchAndFamily**</span><span class="sxs-lookup"><span data-stu-id="a678d-134">**PitchAndFamily**</span></span>
</dt> <dd>

<span data-ttu-id="a678d-135">Type : **[ **Byte**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a678d-135">Type: **[**BYTE**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="a678d-136">Hauteur et largeur de la police.</span><span class="sxs-lookup"><span data-stu-id="a678d-136">Pitch and family of the font.</span></span>

</dd> <dt>

<span data-ttu-id="a678d-137">**FaceName**</span><span class="sxs-lookup"><span data-stu-id="a678d-137">**FaceName**</span></span>
</dt> <dd>

<span data-ttu-id="a678d-138">Type : **TCHAR**</span><span class="sxs-lookup"><span data-stu-id="a678d-138">Type: **TCHAR**</span></span>

</dd> <dd>

<span data-ttu-id="a678d-139">Chaîne ou caractères se terminant par un caractère null qui spécifie le nom de la police de la police.</span><span class="sxs-lookup"><span data-stu-id="a678d-139">A null-terminated string or characters that specifies the typeface name of the font.</span></span> <span data-ttu-id="a678d-140">La longueur de la chaîne ne doit pas dépasser 32 caractères, y compris le caractère null de fin.</span><span class="sxs-lookup"><span data-stu-id="a678d-140">The length of the string must not exceed 32 characters, including the terminating null character.</span></span> <span data-ttu-id="a678d-141">Si FaceName est une chaîne vide, la première police qui correspond aux autres attributs spécifiés sera utilisée.</span><span class="sxs-lookup"><span data-stu-id="a678d-141">If FaceName is an empty string, the first font that matches the other specified attributes will be used.</span></span> <span data-ttu-id="a678d-142">Si les paramètres du compilateur requièrent Unicode, le type de données TCHAR correspond à WCHAR ; dans le cas contraire, le type de données correspond à CHAR.</span><span class="sxs-lookup"><span data-stu-id="a678d-142">If the compiler settings require Unicode, the data type TCHAR resolves to WCHAR; otherwise, the data type resolves to CHAR.</span></span> <span data-ttu-id="a678d-143">Consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="a678d-143">See Remarks.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a678d-144">Notes</span><span class="sxs-lookup"><span data-stu-id="a678d-144">Remarks</span></span>

<span data-ttu-id="a678d-145">Le paramètre du compilateur détermine également le type de structure.</span><span class="sxs-lookup"><span data-stu-id="a678d-145">The compiler setting also determines the structure type.</span></span> <span data-ttu-id="a678d-146">Si Unicode est défini, le \_ type de structure D3DXFONT DESC correspond à un DESCW D3DXFONT \_ ; sinon, le type de structure est résolu en D3DXFONT \_ DESCA.</span><span class="sxs-lookup"><span data-stu-id="a678d-146">If Unicode is defined, the D3DXFONT\_DESC structure type resolves to a D3DXFONT\_DESCW; otherwise the structure type resolves to a D3DXFONT\_DESCA.</span></span>

<span data-ttu-id="a678d-147">Les valeurs possibles des membres ci-dessus sont fournies dans la structure GDI [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) .</span><span class="sxs-lookup"><span data-stu-id="a678d-147">Possible values of the above members are given in the GDI [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="a678d-148">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a678d-148">Requirements</span></span>



| <span data-ttu-id="a678d-149">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a678d-149">Requirement</span></span> | <span data-ttu-id="a678d-150">Valeur</span><span class="sxs-lookup"><span data-stu-id="a678d-150">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a678d-151">En-tête</span><span class="sxs-lookup"><span data-stu-id="a678d-151">Header</span></span><br/> | <dl> <span data-ttu-id="a678d-152"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="a678d-152"><dt>D3dx9core.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a678d-153">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a678d-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a678d-154">Structures D3DX</span><span class="sxs-lookup"><span data-stu-id="a678d-154">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[<span data-ttu-id="a678d-155">**GetDesc**</span><span class="sxs-lookup"><span data-stu-id="a678d-155">**GetDesc**</span></span>](id3dxfont--getdesc.md)
</dt> </dl>

 

 
