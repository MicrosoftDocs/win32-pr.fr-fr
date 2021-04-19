---
description: Définit les attributs de police.
ms.assetid: 66e8a320-2b83-4766-a9a7-5571ee6c9f2a
title: Structure D3DX10_FONT_DESC (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_FONT_DESC
api_type:
- HeaderDef
api_location:
- D3DX10.h
ms.openlocfilehash: 0b358c57e6410827177e76e3da30b2f5f9896ee2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106539162"
---
# <a name="d3dx10_font_desc-structure"></a><span data-ttu-id="1889f-103">Structure de la \_ police d3dx10 \_</span><span class="sxs-lookup"><span data-stu-id="1889f-103">D3DX10\_FONT\_DESC structure</span></span>

<span data-ttu-id="1889f-104">Définit les attributs de police.</span><span class="sxs-lookup"><span data-stu-id="1889f-104">Defines font attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="1889f-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1889f-105">Syntax</span></span>


```C++
typedef struct D3DX10_FONT_DESC {
  INT   Height;
  UINT  Width;
  UINT  Weight;
  UINT  MipLevels;
  BOOL  Italic;
  BYTE  CharSet;
  BYTE  OutputPrecision;
  BYTE  Quality;
  BYTE  PitchAndFamily;
  TCHAR FaceName[LF_FACESIZE];
} D3DX10_FONT_DESC, *LPD3DX10_FONT_DESC;
```



## <a name="members"></a><span data-ttu-id="1889f-106">Membres</span><span class="sxs-lookup"><span data-stu-id="1889f-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="1889f-107">**Height**</span><span class="sxs-lookup"><span data-stu-id="1889f-107">**Height**</span></span>
</dt> <dd>

<span data-ttu-id="1889f-108">Type : **[ **int**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1889f-108">Type: **[**INT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="1889f-109">Hauteur, en unités logiques, de la cellule de caractère ou du caractère de la police.</span><span class="sxs-lookup"><span data-stu-id="1889f-109">Height, in logical units, of the font's character cell or character.</span></span>

</dd> <dt>

<span data-ttu-id="1889f-110">**Width**</span><span class="sxs-lookup"><span data-stu-id="1889f-110">**Width**</span></span>
</dt> <dd>

<span data-ttu-id="1889f-111">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1889f-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="1889f-112">Largeur, en unités logiques, des caractères de la police.</span><span class="sxs-lookup"><span data-stu-id="1889f-112">Width, in logical units, of characters in the font.</span></span>

</dd> <dt>

<span data-ttu-id="1889f-113">**Poids**</span><span class="sxs-lookup"><span data-stu-id="1889f-113">**Weight**</span></span>
</dt> <dd>

<span data-ttu-id="1889f-114">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1889f-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="1889f-115">Poids de la police dans la plage comprise entre 0 et 1000.</span><span class="sxs-lookup"><span data-stu-id="1889f-115">Weight of the font in the range from 0 through 1000.</span></span>

</dd> <dt>

<span data-ttu-id="1889f-116">**Miplevels a**</span><span class="sxs-lookup"><span data-stu-id="1889f-116">**MipLevels**</span></span>
</dt> <dd>

<span data-ttu-id="1889f-117">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1889f-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="1889f-118">Nombre de niveaux de mipmap demandés.</span><span class="sxs-lookup"><span data-stu-id="1889f-118">Number of mipmap levels requested.</span></span> <span data-ttu-id="1889f-119">Si cette valeur est égale à zéro ou à D3DX \_ default, une chaîne mipmap complète est créée.</span><span class="sxs-lookup"><span data-stu-id="1889f-119">If this value is zero or D3DX\_DEFAULT, a complete mipmap chain is created.</span></span> <span data-ttu-id="1889f-120">Si la valeur est 1, l’espace de texture est mappé de manière identique à l’espace à l’écran.</span><span class="sxs-lookup"><span data-stu-id="1889f-120">If the value is 1, the texture space is mapped identically to the screen space.</span></span>

</dd> <dt>

<span data-ttu-id="1889f-121">**Italique**</span><span class="sxs-lookup"><span data-stu-id="1889f-121">**Italic**</span></span>
</dt> <dd>

<span data-ttu-id="1889f-122">Type : **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1889f-122">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="1889f-123">Affectez la valeur **true** à une police en italique.</span><span class="sxs-lookup"><span data-stu-id="1889f-123">Set to **TRUE** for an Italic font.</span></span>

</dd> <dt>

<span data-ttu-id="1889f-124">**CharSet**</span><span class="sxs-lookup"><span data-stu-id="1889f-124">**CharSet**</span></span>
</dt> <dd>

<span data-ttu-id="1889f-125">Type : **[ **Byte**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1889f-125">Type: **[**BYTE**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="1889f-126">Jeu de caractères.</span><span class="sxs-lookup"><span data-stu-id="1889f-126">Character set.</span></span>

</dd> <dt>

<span data-ttu-id="1889f-127">**OutputPrecision**</span><span class="sxs-lookup"><span data-stu-id="1889f-127">**OutputPrecision**</span></span>
</dt> <dd>

<span data-ttu-id="1889f-128">Type : **[ **Byte**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1889f-128">Type: **[**BYTE**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="1889f-129">Précision de sortie.</span><span class="sxs-lookup"><span data-stu-id="1889f-129">Output precision.</span></span> <span data-ttu-id="1889f-130">La précision de sortie définit la précision selon laquelle la sortie doit correspondre à la hauteur de police, à la largeur, à l’orientation des caractères, à l’échappement, au tangage et au type de police demandés.</span><span class="sxs-lookup"><span data-stu-id="1889f-130">The output precision defines how closely the output must match the requested font height, width, character orientation, escapement, pitch, and font type.</span></span>

</dd> <dt>

<span data-ttu-id="1889f-131">**Qualité**</span><span class="sxs-lookup"><span data-stu-id="1889f-131">**Quality**</span></span>
</dt> <dd>

<span data-ttu-id="1889f-132">Type : **[ **Byte**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1889f-132">Type: **[**BYTE**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="1889f-133">Qualité de sortie.</span><span class="sxs-lookup"><span data-stu-id="1889f-133">Output quality.</span></span>

</dd> <dt>

<span data-ttu-id="1889f-134">**PitchAndFamily**</span><span class="sxs-lookup"><span data-stu-id="1889f-134">**PitchAndFamily**</span></span>
</dt> <dd>

<span data-ttu-id="1889f-135">Type : **[ **Byte**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1889f-135">Type: **[**BYTE**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="1889f-136">Hauteur et largeur de la police.</span><span class="sxs-lookup"><span data-stu-id="1889f-136">Pitch and family of the font.</span></span>

</dd> <dt>

<span data-ttu-id="1889f-137">**FaceName \[ LF- \_ face\]**</span><span class="sxs-lookup"><span data-stu-id="1889f-137">**FaceName\[LF\_FACESIZE\]**</span></span>
</dt> <dd>

<span data-ttu-id="1889f-138">Type : **TCHAR**</span><span class="sxs-lookup"><span data-stu-id="1889f-138">Type: **TCHAR**</span></span>

</dd> <dd>

<span data-ttu-id="1889f-139">Chaîne terminée par le caractère NULL qui spécifie le nom de la police de la police.</span><span class="sxs-lookup"><span data-stu-id="1889f-139">A NULL-terminated string that specifies the typeface name of the font.</span></span> <span data-ttu-id="1889f-140">La longueur de la chaîne ne doit pas dépasser 32 caractères, y compris le caractère **null** de fin.</span><span class="sxs-lookup"><span data-stu-id="1889f-140">The length of the string must not exceed 32 characters, including the terminating **NULL** character.</span></span> <span data-ttu-id="1889f-141">Si FaceName est une chaîne vide, la première police qui correspond aux autres attributs spécifiés sera utilisée.</span><span class="sxs-lookup"><span data-stu-id="1889f-141">If FaceName is an empty string, the first font that matches the other specified attributes will be used.</span></span> <span data-ttu-id="1889f-142">Si les paramètres du compilateur requièrent Unicode, le type de données TCHAR correspond à WCHAR ; dans le cas contraire, le type de données correspond à CHAR.</span><span class="sxs-lookup"><span data-stu-id="1889f-142">If the compiler settings require Unicode, the data type TCHAR resolves to WCHAR; otherwise, the data type resolves to CHAR.</span></span> <span data-ttu-id="1889f-143">Consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="1889f-143">See Remarks.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1889f-144">Notes</span><span class="sxs-lookup"><span data-stu-id="1889f-144">Remarks</span></span>

<span data-ttu-id="1889f-145">Le paramètre du compilateur détermine également le type de structure.</span><span class="sxs-lookup"><span data-stu-id="1889f-145">The compiler setting also determines the structure type.</span></span> <span data-ttu-id="1889f-146">Si Unicode est défini, le \_ type de \_ structure Description de la police d3dx10 correspond à un \_ DESCW de police d3dx10 ; dans \_ le cas contraire, le type de structure est résolu en une \_ police d3dx10 \_ DESCA.</span><span class="sxs-lookup"><span data-stu-id="1889f-146">If Unicode is defined, the D3DX10\_FONT\_DESC structure type resolves to a D3DX10\_FONT\_DESCW; otherwise the structure type resolves to a D3DX10\_FONT\_DESCA.</span></span>

<span data-ttu-id="1889f-147">Les valeurs possibles des membres ci-dessus sont fournies dans la structure GDI [LOGFONT](/previous-versions//ms533931(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="1889f-147">Possible values of the above members are given in the GDI [LOGFONT](/previous-versions//ms533931(v=vs.85)) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="1889f-148">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1889f-148">Requirements</span></span>



| <span data-ttu-id="1889f-149">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1889f-149">Requirement</span></span> | <span data-ttu-id="1889f-150">Valeur</span><span class="sxs-lookup"><span data-stu-id="1889f-150">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="1889f-151">En-tête</span><span class="sxs-lookup"><span data-stu-id="1889f-151">Header</span></span><br/> | <dl> <span data-ttu-id="1889f-152"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="1889f-152"><dt>D3DX10.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1889f-153">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1889f-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1889f-154">Structures D3DX</span><span class="sxs-lookup"><span data-stu-id="1889f-154">D3DX Structures</span></span>](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
