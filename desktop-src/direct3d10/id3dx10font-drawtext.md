---
description: Dessinez du texte mis en forme. Cette méthode prend en charge les chaînes ANSI et Unicode.
ms.assetid: 205e9e23-4293-4195-9e41-d8c06dabd285
title: ID3DX10Font ::D méthode rawText (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Font.DrawText
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 5fa23684be1b63cfbd8e3d07d3578d87fdfbf46a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106532447"
---
# <a name="id3dx10fontdrawtext-method"></a><span data-ttu-id="144c5-104">ID3DX10Font ::D méthode rawText</span><span class="sxs-lookup"><span data-stu-id="144c5-104">ID3DX10Font::DrawText method</span></span>

<span data-ttu-id="144c5-105">Dessinez du texte mis en forme.</span><span class="sxs-lookup"><span data-stu-id="144c5-105">Draw formatted text.</span></span> <span data-ttu-id="144c5-106">Cette méthode prend en charge les chaînes ANSI et Unicode.</span><span class="sxs-lookup"><span data-stu-id="144c5-106">This method supports ANSI and Unicode strings.</span></span>

## <a name="syntax"></a><span data-ttu-id="144c5-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="144c5-107">Syntax</span></span>


```C++
INT DrawText(
  [in] LPD3DX10SPRITE pSprite,
  [in] LPCTSTR        pString,
  [in] INT            Count,
  [in] LPRECT         pRect,
  [in] UINT           Format,
  [in] D3DXCOLOR      Color
);
```



## <a name="parameters"></a><span data-ttu-id="144c5-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="144c5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="144c5-109">*pSprite* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="144c5-109">*pSprite* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="144c5-110">Type : **[ **LPD3DX10SPRITE**](id3dx10sprite.md)**</span><span class="sxs-lookup"><span data-stu-id="144c5-110">Type: **[**LPD3DX10SPRITE**](id3dx10sprite.md)**</span></span>

<span data-ttu-id="144c5-111">Pointeur vers un objet ID3DX10Sprite qui contient la chaîne que vous souhaitez dessiner.</span><span class="sxs-lookup"><span data-stu-id="144c5-111">Pointer to an ID3DX10Sprite object that contains the string you wish to draw.</span></span> <span data-ttu-id="144c5-112">Peut avoir la **valeur null**, auquel cas Direct3D affiche la chaîne avec son propre objet Sprite.</span><span class="sxs-lookup"><span data-stu-id="144c5-112">Can be **NULL**, in which case Direct3D will render the string with its own sprite object.</span></span> <span data-ttu-id="144c5-113">Pour améliorer l’efficacité, un objet Sprite doit être spécifié si ID3DX10Font ::D rawText doit être appelé plusieurs fois dans une ligne.</span><span class="sxs-lookup"><span data-stu-id="144c5-113">To improve efficiency, a sprite object should be specified if ID3DX10Font::DrawText is to be called more than once in a row.</span></span>

</dd> <dt>

<span data-ttu-id="144c5-114">*pString* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="144c5-114">*pString* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="144c5-115">Type : **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="144c5-115">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="144c5-116">Pointeur vers une chaîne à dessiner.</span><span class="sxs-lookup"><span data-stu-id="144c5-116">Pointer to a string to draw.</span></span> <span data-ttu-id="144c5-117">Si UNICODE est défini, ce type de paramètre correspond à un LPCWSTR, dans le cas contraire, le type correspond à un LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="144c5-117">If UNICODE is defined, this parameter type resolves to an LPCWSTR, otherwise, the type resolves to an LPCSTR.</span></span> <span data-ttu-id="144c5-118">Si le paramètre count a la valeur-1, la chaîne doit se terminer par **null** .</span><span class="sxs-lookup"><span data-stu-id="144c5-118">If the Count parameter is -1, the string must be **NULL** terminated.</span></span>

</dd> <dt>

<span data-ttu-id="144c5-119">*Nombre* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="144c5-119">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="144c5-120">Type : **[ **int**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="144c5-120">Type: **[**INT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="144c5-121">Nombre de caractères dans la chaîne.</span><span class="sxs-lookup"><span data-stu-id="144c5-121">The number of characters in the string.</span></span> <span data-ttu-id="144c5-122">Si Count a la valeur-1, le paramètre pString est supposé être un pointeur vers un sprite contenant une chaîne se terminant par un caractère NULL et ID3DX10Font ::D rawText calcule le nombre de caractères automatiquement.</span><span class="sxs-lookup"><span data-stu-id="144c5-122">If Count is -1, then the pString parameter is assumed to be a pointer to a sprite containing a NULL-terminated string and ID3DX10Font::DrawText computes the character count automatically.</span></span>

</dd> <dt>

<span data-ttu-id="144c5-123">*pRect* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="144c5-123">*pRect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="144c5-124">Type : **LPRECT**</span><span class="sxs-lookup"><span data-stu-id="144c5-124">Type: **LPRECT**</span></span>

<span data-ttu-id="144c5-125">Pointeur vers une structure [Rect](/previous-versions//ms536136(v=vs.85)) qui contient le rectangle, en coordonnées logiques, dans lequel le texte doit être mis en forme.</span><span class="sxs-lookup"><span data-stu-id="144c5-125">Pointer to a [RECT](/previous-versions//ms536136(v=vs.85)) structure that contains the rectangle, in logical coordinates, in which the text is to be formatted.</span></span> <span data-ttu-id="144c5-126">Comme avec n’importe quel objet RECT, la valeur de coordonnée du côté droit du rectangle doit être supérieure à celle de son côté gauche.</span><span class="sxs-lookup"><span data-stu-id="144c5-126">As with any RECT object, the coordinate value of the rectangle's right side must be greater than that of its left side.</span></span> <span data-ttu-id="144c5-127">De même, la valeur de coordonnée du bas doit être supérieure à celle du haut.</span><span class="sxs-lookup"><span data-stu-id="144c5-127">Likewise, the coordinate value of the bottom must be greater than that of the top.</span></span>

</dd> <dt>

<span data-ttu-id="144c5-128">*Format* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="144c5-128">*Format* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="144c5-129">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="144c5-129">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="144c5-130">Spécifiez la méthode de mise en forme du texte.</span><span class="sxs-lookup"><span data-stu-id="144c5-130">Specify the method of formatting the text.</span></span> <span data-ttu-id="144c5-131">Il peut s’agir de n’importe quelle combinaison des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="144c5-131">It can be any combination of the following values:</span></span>



| <span data-ttu-id="144c5-132">Élément</span><span class="sxs-lookup"><span data-stu-id="144c5-132">Item</span></span>                                                                                      | <span data-ttu-id="144c5-133">Description</span><span class="sxs-lookup"><span data-stu-id="144c5-133">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|-------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="144c5-134"><span id="DT_BOTTOM"></span><span id="dt_bottom"></span>DT en \_ bas</span><span class="sxs-lookup"><span data-stu-id="144c5-134"><span id="DT_BOTTOM"></span><span id="dt_bottom"></span>DT\_BOTTOM</span></span><br/>             | <span data-ttu-id="144c5-135">Justifie le texte en bas du rectangle.</span><span class="sxs-lookup"><span data-stu-id="144c5-135">Justify the text to the bottom of the rectangle.</span></span> <span data-ttu-id="144c5-136">Cette valeur doit être combinée avec DT \_ Singleline.</span><span class="sxs-lookup"><span data-stu-id="144c5-136">This value must be combined with DT\_SINGLELINE.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="144c5-137"><span id="DT_CALCRECT"></span><span id="dt_calcrect"></span>\_CALCRECT DT</span><span class="sxs-lookup"><span data-stu-id="144c5-137"><span id="DT_CALCRECT"></span><span id="dt_calcrect"></span>DT\_CALCRECT</span></span><br/>       | <span data-ttu-id="144c5-138">Indiquez à DrawText de calculer automatiquement la largeur et la hauteur du rectangle en fonction de la longueur de la chaîne que vous lui indiquez de dessiner.</span><span class="sxs-lookup"><span data-stu-id="144c5-138">Tell DrawText to automatically calculate the width and height of the rectangle based on the length of the string you tell it to draw.</span></span> <span data-ttu-id="144c5-139">S’il y a plusieurs lignes de texte, ID3DX10Font ::D rawText utilise la largeur du rectangle vers lequel pointe le paramètre pRect et étend la base du rectangle pour délimiter la dernière ligne de texte.</span><span class="sxs-lookup"><span data-stu-id="144c5-139">If there are multiple lines of text, ID3DX10Font::DrawText uses the width of the rectangle pointed to by the pRect parameter and extends the base of the rectangle to bound the last line of text.</span></span> <span data-ttu-id="144c5-140">S’il n’existe qu’une seule ligne de texte, ID3DX10Font ::D rawText modifie le côté droit du rectangle afin qu’il limite le dernier caractère de la ligne.</span><span class="sxs-lookup"><span data-stu-id="144c5-140">If there is only one line of text, ID3DX10Font::DrawText modifies the right side of the rectangle so that it bounds the last character in the line.</span></span> <span data-ttu-id="144c5-141">Dans les deux cas, ID3DX10Font ::D rawText retourne la hauteur du texte mis en forme, mais ne dessine pas le texte.</span><span class="sxs-lookup"><span data-stu-id="144c5-141">In either case, ID3DX10Font::DrawText returns the height of the formatted text but does not draw the text.</span></span><br/> |
| <span data-ttu-id="144c5-142"><span id="DT_CENTER"></span><span id="dt_center"></span>\_Centre DT</span><span class="sxs-lookup"><span data-stu-id="144c5-142"><span id="DT_CENTER"></span><span id="dt_center"></span>DT\_CENTER</span></span><br/>             | <span data-ttu-id="144c5-143">Centrer le texte horizontalement dans le rectangle.</span><span class="sxs-lookup"><span data-stu-id="144c5-143">Center text horizontally in the rectangle.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="144c5-144"><span id="DT_EXPANDTABS"></span><span id="dt_expandtabs"></span>\_ExpandTabs DT</span><span class="sxs-lookup"><span data-stu-id="144c5-144"><span id="DT_EXPANDTABS"></span><span id="dt_expandtabs"></span>DT\_EXPANDTABS</span></span><br/> | <span data-ttu-id="144c5-145">Développez caractères de tabulation.</span><span class="sxs-lookup"><span data-stu-id="144c5-145">Expand tab characters.</span></span> <span data-ttu-id="144c5-146">Le nombre par défaut de caractères par tabulation est huit.</span><span class="sxs-lookup"><span data-stu-id="144c5-146">The default number of characters per tab is eight.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="144c5-147"><span id="DT_LEFT"></span><span id="dt_left"></span>DT à \_ gauche</span><span class="sxs-lookup"><span data-stu-id="144c5-147"><span id="DT_LEFT"></span><span id="dt_left"></span>DT\_LEFT</span></span><br/>                   | <span data-ttu-id="144c5-148">Aligner le texte à gauche.</span><span class="sxs-lookup"><span data-stu-id="144c5-148">Align text to the left.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="144c5-149"><span id="DT_NOCLIP"></span><span id="dt_noclip"></span>DT \_ NOclip</span><span class="sxs-lookup"><span data-stu-id="144c5-149"><span id="DT_NOCLIP"></span><span id="dt_noclip"></span>DT\_NOCLIP</span></span><br/>             | <span data-ttu-id="144c5-150">Dessin sans découpage.</span><span class="sxs-lookup"><span data-stu-id="144c5-150">Draw without clipping.</span></span> <span data-ttu-id="144c5-151">ID3DX10Font ::D rawText est un peu plus rapide lorsque DT \_ noclip est utilisé.</span><span class="sxs-lookup"><span data-stu-id="144c5-151">ID3DX10Font::DrawText is somewhat faster when DT\_NOCLIP is used.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="144c5-152"><span id="DT_RIGHT"></span><span id="dt_right"></span>DT- \_ droit</span><span class="sxs-lookup"><span data-stu-id="144c5-152"><span id="DT_RIGHT"></span><span id="dt_right"></span>DT\_RIGHT</span></span><br/>                | <span data-ttu-id="144c5-153">Aligner le texte à droite.</span><span class="sxs-lookup"><span data-stu-id="144c5-153">Align text to the right.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="144c5-154"><span id="DT_RTLREADING"></span><span id="dt_rtlreading"></span>\_RTLREADING DT</span><span class="sxs-lookup"><span data-stu-id="144c5-154"><span id="DT_RTLREADING"></span><span id="dt_rtlreading"></span>DT\_RTLREADING</span></span><br/> | <span data-ttu-id="144c5-155">Affichez le texte dans l’ordre de lecture de droite à gauche pour le texte bidirectionnel lorsqu’une police hébraïque ou arabe est sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="144c5-155">Display text in right-to-left reading order for bidirectional text when a Hebrew or Arabic font is selected.</span></span> <span data-ttu-id="144c5-156">L’ordre de lecture par défaut pour tout le texte est de gauche à droite.</span><span class="sxs-lookup"><span data-stu-id="144c5-156">The default reading order for all text is left-to-right.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="144c5-157"><span id="DT_SINGLELINE"></span><span id="dt_singleline"></span>DT \_ Singleline</span><span class="sxs-lookup"><span data-stu-id="144c5-157"><span id="DT_SINGLELINE"></span><span id="dt_singleline"></span>DT\_SINGLELINE</span></span><br/> | <span data-ttu-id="144c5-158">Affichez le texte sur une seule ligne.</span><span class="sxs-lookup"><span data-stu-id="144c5-158">Display text on a single line only.</span></span> <span data-ttu-id="144c5-159">Les retours chariot et les sauts de ligne n’interrompent pas la ligne.</span><span class="sxs-lookup"><span data-stu-id="144c5-159">Carriage returns and line feeds do not break the line.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="144c5-160"><span id="DT_TOP"></span><span id="dt_top"></span>DT en \_ haut</span><span class="sxs-lookup"><span data-stu-id="144c5-160"><span id="DT_TOP"></span><span id="dt_top"></span>DT\_TOP</span></span><br/>                      | <span data-ttu-id="144c5-161">Texte de justification en haut.</span><span class="sxs-lookup"><span data-stu-id="144c5-161">Top-justify text.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="144c5-162"><span id="DT_VCENTER"></span><span id="dt_vcenter"></span>\_VCENTER DT</span><span class="sxs-lookup"><span data-stu-id="144c5-162"><span id="DT_VCENTER"></span><span id="dt_vcenter"></span>DT\_VCENTER</span></span><br/>          | <span data-ttu-id="144c5-163">Centrer le texte verticalement (une seule ligne).</span><span class="sxs-lookup"><span data-stu-id="144c5-163">Center text vertically (single line only).</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="144c5-164"><span id="DT_WORDBREAK"></span><span id="dt_wordbreak"></span>\_WordBreak DT</span><span class="sxs-lookup"><span data-stu-id="144c5-164"><span id="DT_WORDBREAK"></span><span id="dt_wordbreak"></span>DT\_WORDBREAK</span></span><br/>    | <span data-ttu-id="144c5-165">Mots insécables.</span><span class="sxs-lookup"><span data-stu-id="144c5-165">Break words.</span></span> <span data-ttu-id="144c5-166">Les lignes sont automatiquement réparties entre les mots si un mot s’étend au-delà du bord du rectangle spécifié par le paramètre pRect.</span><span class="sxs-lookup"><span data-stu-id="144c5-166">Lines are automatically broken between words if a word would extend past the edge of the rectangle specified by the pRect parameter.</span></span> <span data-ttu-id="144c5-167">Une séquence de retour chariot/saut de ligne interrompt également la ligne.</span><span class="sxs-lookup"><span data-stu-id="144c5-167">A carriage return/line feed sequence also breaks the line.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                            |



 

</dd> <dt>

<span data-ttu-id="144c5-168">*Couleur* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="144c5-168">*Color* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="144c5-169">Type : **[ **D3DXCOLOR**](../direct3d9/d3dxcolor.md)**</span><span class="sxs-lookup"><span data-stu-id="144c5-169">Type: **[**D3DXCOLOR**](../direct3d9/d3dxcolor.md)**</span></span>

<span data-ttu-id="144c5-170">Couleur du texte.</span><span class="sxs-lookup"><span data-stu-id="144c5-170">Color of the text.</span></span> <span data-ttu-id="144c5-171">Consultez [**D3DXCOLOR**](d3d10-d3dxcolor.md).</span><span class="sxs-lookup"><span data-stu-id="144c5-171">See [**D3DXCOLOR**](d3d10-d3dxcolor.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="144c5-172">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="144c5-172">Return value</span></span>

<span data-ttu-id="144c5-173">Type : **[ **int**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="144c5-173">Type: **[**INT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="144c5-174">Si la fonction est réussie, la valeur de retour est la hauteur du texte en unités logiques.</span><span class="sxs-lookup"><span data-stu-id="144c5-174">If the function succeeds, the return value is the height of the text in logical units.</span></span> <span data-ttu-id="144c5-175">Si DT \_ VCENTER ou DT \_ Bottom est spécifié, la valeur de retour est le décalage de pRect (de haut en bas) du texte dessiné.</span><span class="sxs-lookup"><span data-stu-id="144c5-175">If DT\_VCENTER or DT\_BOTTOM is specified, the return value is the offset from pRect (top to the bottom) of the drawn text.</span></span> <span data-ttu-id="144c5-176">Si la fonction échoue, la valeur de retour est égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="144c5-176">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="144c5-177">Notes</span><span class="sxs-lookup"><span data-stu-id="144c5-177">Remarks</span></span>

<span data-ttu-id="144c5-178">Les paramètres de cette méthode sont très similaires à ceux de la fonction [GDI DrawText](/previous-versions//ms533909(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="144c5-178">The parameters of this method are very similar to those of the [GDI DrawText](/previous-versions//ms533909(v=vs.85)) function.</span></span>

<span data-ttu-id="144c5-179">Cette méthode prend en charge les chaînes ANSI et Unicode.</span><span class="sxs-lookup"><span data-stu-id="144c5-179">This method supports both ANSI and Unicode strings.</span></span>

<span data-ttu-id="144c5-180">À moins que le \_ format DT NOclip ne soit utilisé, cette méthode découpe le texte afin qu’il n’apparaisse pas en dehors du rectangle spécifié.</span><span class="sxs-lookup"><span data-stu-id="144c5-180">Unless the DT\_NOCLIP format is used, this method clips the text so that it does not appear outside the specified rectangle.</span></span> <span data-ttu-id="144c5-181">Toute la mise en forme est supposée avoir plusieurs lignes, sauf si le \_ format DT Singleline est spécifié.</span><span class="sxs-lookup"><span data-stu-id="144c5-181">All formatting is assumed to have multiple lines unless the DT\_SINGLELINE format is specified.</span></span>

<span data-ttu-id="144c5-182">Si la police sélectionnée est trop grande pour le rectangle, cette méthode n’essaie pas de remplacer une police plus petite.</span><span class="sxs-lookup"><span data-stu-id="144c5-182">If the selected font is too large for the rectangle, this method does not attempt to substitute a smaller font.</span></span>

<span data-ttu-id="144c5-183">Cette méthode prend en charge uniquement les polices dont l’échappement et l’orientation sont toutes deux égales à zéro.</span><span class="sxs-lookup"><span data-stu-id="144c5-183">This method supports only fonts whose escapement and orientation are both zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="144c5-184">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="144c5-184">Requirements</span></span>



| <span data-ttu-id="144c5-185">Condition requise</span><span class="sxs-lookup"><span data-stu-id="144c5-185">Requirement</span></span> | <span data-ttu-id="144c5-186">Valeur</span><span class="sxs-lookup"><span data-stu-id="144c5-186">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="144c5-187">En-tête</span><span class="sxs-lookup"><span data-stu-id="144c5-187">Header</span></span><br/>  | <dl> <span data-ttu-id="144c5-188"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="144c5-188"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="144c5-189">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="144c5-189">Library</span></span><br/> | <dl> <span data-ttu-id="144c5-190"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="144c5-190"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="144c5-191">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="144c5-191">See also</span></span>

<dl> <dt>

[<span data-ttu-id="144c5-192">ID3DX10Font</span><span class="sxs-lookup"><span data-stu-id="144c5-192">ID3DX10Font</span></span>](id3dx10font.md)
</dt> <dt>

[<span data-ttu-id="144c5-193">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="144c5-193">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
