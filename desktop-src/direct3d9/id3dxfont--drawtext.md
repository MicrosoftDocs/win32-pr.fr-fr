---
description: Dessine du texte mis en forme. Cette méthode prend en charge les chaînes ANSI et Unicode.
ms.assetid: c1c3657e-632e-46a5-91da-e102ac8ef9bb
title: ID3DXFont ::D méthode rawText (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFont.DrawText
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 96636c372ee48d516286935f03d80b8e9815ffc8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104211754"
---
# <a name="id3dxfontdrawtext-method"></a><span data-ttu-id="bc367-104">ID3DXFont ::D méthode rawText</span><span class="sxs-lookup"><span data-stu-id="bc367-104">ID3DXFont::DrawText method</span></span>

<span data-ttu-id="bc367-105">Dessine du texte mis en forme.</span><span class="sxs-lookup"><span data-stu-id="bc367-105">Draws formatted text.</span></span> <span data-ttu-id="bc367-106">Cette méthode prend en charge les chaînes ANSI et Unicode.</span><span class="sxs-lookup"><span data-stu-id="bc367-106">This method supports ANSI and Unicode strings.</span></span>

## <a name="syntax"></a><span data-ttu-id="bc367-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bc367-107">Syntax</span></span>


```C++
INT DrawText(
  [in] LPD3DXSPRITE pSprite,
  [in] LPCTSTR      pString,
  [in] INT          Count,
  [in] LPRECT       pRect,
  [in] DWORD        Format,
  [in] D3DCOLOR     Color
);
```



## <a name="parameters"></a><span data-ttu-id="bc367-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bc367-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bc367-109">*pSprite* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="bc367-109">*pSprite* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bc367-110">Type : **[ **LPD3DXSPRITE**](id3dxsprite.md)**</span><span class="sxs-lookup"><span data-stu-id="bc367-110">Type: **[**LPD3DXSPRITE**](id3dxsprite.md)**</span></span>

<span data-ttu-id="bc367-111">Pointeur vers un objet [**ID3DXSprite**](id3dxsprite.md) qui contient la chaîne.</span><span class="sxs-lookup"><span data-stu-id="bc367-111">Pointer to an [**ID3DXSprite**](id3dxsprite.md) object that contains the string.</span></span> <span data-ttu-id="bc367-112">Peut avoir la **valeur null**, auquel cas Direct3D affiche la chaîne avec son propre objet Sprite.</span><span class="sxs-lookup"><span data-stu-id="bc367-112">Can be **NULL**, in which case Direct3D will render the string with its own sprite object.</span></span> <span data-ttu-id="bc367-113">Pour améliorer l’efficacité, un objet Sprite doit être spécifié si **DrawText** doit être appelé plusieurs fois dans une ligne.</span><span class="sxs-lookup"><span data-stu-id="bc367-113">To improve efficiency, a sprite object should be specified if **DrawText** is to be called more than once in a row.</span></span>

</dd> <dt>

<span data-ttu-id="bc367-114">*pString* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="bc367-114">*pString* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bc367-115">Type : **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="bc367-115">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="bc367-116">Pointeur vers une chaîne à dessiner.</span><span class="sxs-lookup"><span data-stu-id="bc367-116">Pointer to a string to draw.</span></span> <span data-ttu-id="bc367-117">Si le paramètre count a la valeur-1, la chaîne doit se terminer par un caractère null.</span><span class="sxs-lookup"><span data-stu-id="bc367-117">If the Count parameter is -1, the string must be null-terminated.</span></span>

</dd> <dt>

<span data-ttu-id="bc367-118">*Nombre* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="bc367-118">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bc367-119">Type : **[ **int**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="bc367-119">Type: **[**INT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="bc367-120">Spécifie le nombre de caractères de la chaîne.</span><span class="sxs-lookup"><span data-stu-id="bc367-120">Specifies the number of characters in the string.</span></span> <span data-ttu-id="bc367-121">Si Count a la valeur-1, le paramètre pString est supposé être un pointeur vers une chaîne terminée par le caractère null et **DrawText** calcule automatiquement le nombre de caractères.</span><span class="sxs-lookup"><span data-stu-id="bc367-121">If Count is -1, then the pString parameter is assumed to be a pointer to a null-terminated string and **DrawText** computes the character count automatically.</span></span>

</dd> <dt>

<span data-ttu-id="bc367-122">*pRect* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="bc367-122">*pRect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bc367-123">Type : **[ **LPRECT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="bc367-123">Type: **[**LPRECT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="bc367-124">Pointeur vers une structure [**Rect**](/previous-versions//dd162897(v=vs.85)) qui contient le rectangle, en coordonnées logiques, dans lequel le texte doit être mis en forme.</span><span class="sxs-lookup"><span data-stu-id="bc367-124">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that contains the rectangle, in logical coordinates, in which the text is to be formatted.</span></span> <span data-ttu-id="bc367-125">La valeur de coordonnée du côté droit du rectangle doit être supérieure à celle du côté gauche.</span><span class="sxs-lookup"><span data-stu-id="bc367-125">The coordinate value of the rectangle's right side must be greater than that of its left side.</span></span> <span data-ttu-id="bc367-126">De même, la valeur de coordonnée du bas doit être supérieure à celle du haut.</span><span class="sxs-lookup"><span data-stu-id="bc367-126">Likewise, the coordinate value of the bottom must be greater than that of the top.</span></span>

</dd> <dt>

<span data-ttu-id="bc367-127">*Format* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="bc367-127">*Format* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bc367-128">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="bc367-128">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="bc367-129">Spécifie la méthode de mise en forme du texte.</span><span class="sxs-lookup"><span data-stu-id="bc367-129">Specifies the method of formatting the text.</span></span> <span data-ttu-id="bc367-130">Il peut s’agir de n’importe quelle combinaison des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="bc367-130">It can be any combination of the following values:</span></span>



| <span data-ttu-id="bc367-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="bc367-131">Value</span></span>                                                                                                                                                         | <span data-ttu-id="bc367-132">Signification</span><span class="sxs-lookup"><span data-stu-id="bc367-132">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DT_BOTTOM"></span><span id="dt_bottom"></span><dl> <span data-ttu-id="bc367-133"><dt>**DT en \_ bas**</dt></span><span class="sxs-lookup"><span data-stu-id="bc367-133"><dt>**DT\_BOTTOM**</dt></span></span> </dl>             | <span data-ttu-id="bc367-134">Justifie le texte en bas du rectangle.</span><span class="sxs-lookup"><span data-stu-id="bc367-134">Justifies the text to the bottom of the rectangle.</span></span> <span data-ttu-id="bc367-135">Cette valeur doit être combinée avec DT \_ Singleline.</span><span class="sxs-lookup"><span data-stu-id="bc367-135">This value must be combined with DT\_SINGLELINE.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="DT_CALCRECT"></span><span id="dt_calcrect"></span><dl> <span data-ttu-id="bc367-136"><dt>**\_CALCRECT DT**</dt></span><span class="sxs-lookup"><span data-stu-id="bc367-136"><dt>**DT\_CALCRECT**</dt></span></span> </dl>       | <span data-ttu-id="bc367-137">Détermine la largeur et la hauteur du rectangle.</span><span class="sxs-lookup"><span data-stu-id="bc367-137">Determines the width and height of the rectangle.</span></span> <span data-ttu-id="bc367-138">S’il y a plusieurs lignes de texte, **DrawText** utilise la largeur du rectangle vers lequel pointe le paramètre pRect et étend la base du rectangle pour délimiter la dernière ligne de texte.</span><span class="sxs-lookup"><span data-stu-id="bc367-138">If there are multiple lines of text, **DrawText** uses the width of the rectangle pointed to by the pRect parameter and extends the base of the rectangle to bound the last line of text.</span></span> <span data-ttu-id="bc367-139">S’il n’existe qu’une seule ligne de texte, **DrawText** modifie le côté droit du rectangle afin qu’il limite le dernier caractère de la ligne.</span><span class="sxs-lookup"><span data-stu-id="bc367-139">If there is only one line of text, **DrawText** modifies the right side of the rectangle so that it bounds the last character in the line.</span></span> <span data-ttu-id="bc367-140">Dans les deux cas, **DrawText** retourne la hauteur du texte mis en forme, mais ne dessine pas le texte.</span><span class="sxs-lookup"><span data-stu-id="bc367-140">In either case, **DrawText** returns the height of the formatted text but does not draw the text.</span></span><br/> |
| <span id="DT_CENTER"></span><span id="dt_center"></span><dl> <span data-ttu-id="bc367-141"><dt>**\_Centre DT**</dt></span><span class="sxs-lookup"><span data-stu-id="bc367-141"><dt>**DT\_CENTER**</dt></span></span> </dl>             | <span data-ttu-id="bc367-142">Centre le texte horizontalement dans le rectangle.</span><span class="sxs-lookup"><span data-stu-id="bc367-142">Centers text horizontally in the rectangle.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="DT_EXPANDTABS"></span><span id="dt_expandtabs"></span><dl> <span data-ttu-id="bc367-143"><dt>**\_ExpandTabs DT**</dt></span><span class="sxs-lookup"><span data-stu-id="bc367-143"><dt>**DT\_EXPANDTABS**</dt></span></span> </dl> | <span data-ttu-id="bc367-144">Développe des caractères de tabulation.</span><span class="sxs-lookup"><span data-stu-id="bc367-144">Expands tab characters.</span></span> <span data-ttu-id="bc367-145">Le nombre par défaut de caractères par tabulation est huit.</span><span class="sxs-lookup"><span data-stu-id="bc367-145">The default number of characters per tab is eight.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span id="DT_LEFT"></span><span id="dt_left"></span><dl> <span data-ttu-id="bc367-146"><dt>**DT à \_ gauche**</dt></span><span class="sxs-lookup"><span data-stu-id="bc367-146"><dt>**DT\_LEFT**</dt></span></span> </dl>                   | <span data-ttu-id="bc367-147">Aligne le texte à gauche.</span><span class="sxs-lookup"><span data-stu-id="bc367-147">Aligns text to the left.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="DT_NOCLIP"></span><span id="dt_noclip"></span><dl> <span data-ttu-id="bc367-148"><dt>**DT \_ NOclip**</dt></span><span class="sxs-lookup"><span data-stu-id="bc367-148"><dt>**DT\_NOCLIP**</dt></span></span> </dl>             | <span data-ttu-id="bc367-149">Dessine sans découpage.</span><span class="sxs-lookup"><span data-stu-id="bc367-149">Draws without clipping.</span></span> <span data-ttu-id="bc367-150">**DrawText** est un peu plus rapide lorsque DT \_ noclip est utilisé.</span><span class="sxs-lookup"><span data-stu-id="bc367-150">**DrawText** is somewhat faster when DT\_NOCLIP is used.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="DT_RIGHT"></span><span id="dt_right"></span><dl> <span data-ttu-id="bc367-151"><dt>**DT- \_ droit**</dt></span><span class="sxs-lookup"><span data-stu-id="bc367-151"><dt>**DT\_RIGHT**</dt></span></span> </dl>                | <span data-ttu-id="bc367-152">Aligne le texte à droite.</span><span class="sxs-lookup"><span data-stu-id="bc367-152">Aligns text to the right.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| <span id="DT_RTLREADING"></span><span id="dt_rtlreading"></span><dl> <span data-ttu-id="bc367-153"><dt>**\_RTLREADING DT**</dt></span><span class="sxs-lookup"><span data-stu-id="bc367-153"><dt>**DT\_RTLREADING**</dt></span></span> </dl> | <span data-ttu-id="bc367-154">Affiche le texte dans l’ordre de lecture de droite à gauche pour le texte bidirectionnel lorsqu’une police hébraïque ou arabe est sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="bc367-154">Displays text in right-to-left reading order for bidirectional text when a Hebrew or Arabic font is selected.</span></span> <span data-ttu-id="bc367-155">L’ordre de lecture par défaut pour tout le texte est de gauche à droite.</span><span class="sxs-lookup"><span data-stu-id="bc367-155">The default reading order for all text is left-to-right.</span></span><br/>                                                                                                                                                                                                                                                                                                                   |
| <span id="DT_SINGLELINE"></span><span id="dt_singleline"></span><dl> <span data-ttu-id="bc367-156"><dt>**DT \_ Singleline**</dt></span><span class="sxs-lookup"><span data-stu-id="bc367-156"><dt>**DT\_SINGLELINE**</dt></span></span> </dl> | <span data-ttu-id="bc367-157">Affiche du texte sur une seule ligne.</span><span class="sxs-lookup"><span data-stu-id="bc367-157">Displays text on a single line only.</span></span> <span data-ttu-id="bc367-158">Les retours chariot et les sauts de ligne n’interrompent pas la ligne.</span><span class="sxs-lookup"><span data-stu-id="bc367-158">Carriage returns and line feeds do not break the line.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="DT_TOP"></span><span id="dt_top"></span><dl> <span data-ttu-id="bc367-159"><dt>**DT en \_ haut**</dt></span><span class="sxs-lookup"><span data-stu-id="bc367-159"><dt>**DT\_TOP**</dt></span></span> </dl>                      | <span data-ttu-id="bc367-160">Top-justifie le texte.</span><span class="sxs-lookup"><span data-stu-id="bc367-160">Top-justifies text.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="DT_VCENTER"></span><span id="dt_vcenter"></span><dl> <span data-ttu-id="bc367-161"><dt>**\_VCENTER DT**</dt></span><span class="sxs-lookup"><span data-stu-id="bc367-161"><dt>**DT\_VCENTER**</dt></span></span> </dl>          | <span data-ttu-id="bc367-162">Centre le texte verticalement (une seule ligne).</span><span class="sxs-lookup"><span data-stu-id="bc367-162">Centers text vertically (single line only).</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="DT_WORDBREAK"></span><span id="dt_wordbreak"></span><dl> <span data-ttu-id="bc367-163"><dt>**\_WordBreak DT**</dt></span><span class="sxs-lookup"><span data-stu-id="bc367-163"><dt>**DT\_WORDBREAK**</dt></span></span> </dl>    | <span data-ttu-id="bc367-164">Arrête les mots.</span><span class="sxs-lookup"><span data-stu-id="bc367-164">Breaks words.</span></span> <span data-ttu-id="bc367-165">Les lignes sont automatiquement réparties entre les mots si un mot s’étend au-delà du bord du rectangle spécifié par le paramètre pRect.</span><span class="sxs-lookup"><span data-stu-id="bc367-165">Lines are automatically broken between words if a word would extend past the edge of the rectangle specified by the pRect parameter.</span></span> <span data-ttu-id="bc367-166">Une séquence de retour chariot/saut de ligne interrompt également la ligne.</span><span class="sxs-lookup"><span data-stu-id="bc367-166">A carriage return/line feed sequence also breaks the line.</span></span><br/>                                                                                                                                                                                                                                                                            |



 

</dd> <dt>

<span data-ttu-id="bc367-167">*Couleur* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="bc367-167">*Color* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bc367-168">Type : **[ **D3DCOLOR**](d3dcolor.md)**</span><span class="sxs-lookup"><span data-stu-id="bc367-168">Type: **[**D3DCOLOR**](d3dcolor.md)**</span></span>

<span data-ttu-id="bc367-169">Couleur du texte.</span><span class="sxs-lookup"><span data-stu-id="bc367-169">Color of the text.</span></span> <span data-ttu-id="bc367-170">Pour plus d’informations, consultez [**D3DCOLOR**](d3dcolor.md).</span><span class="sxs-lookup"><span data-stu-id="bc367-170">For more information, see [**D3DCOLOR**](d3dcolor.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bc367-171">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="bc367-171">Return value</span></span>

<span data-ttu-id="bc367-172">Type : **[ **int**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="bc367-172">Type: **[**INT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="bc367-173">Si la fonction est réussie, la valeur de retour est la hauteur du texte en unités logiques.</span><span class="sxs-lookup"><span data-stu-id="bc367-173">If the function succeeds, the return value is the height of the text in logical units.</span></span> <span data-ttu-id="bc367-174">Si DT \_ VCENTER ou DT \_ Bottom est spécifié, la valeur de retour est le décalage de pRect (de haut en bas) du texte dessiné.</span><span class="sxs-lookup"><span data-stu-id="bc367-174">If DT\_VCENTER or DT\_BOTTOM is specified, the return value is the offset from pRect (top to the bottom) of the drawn text.</span></span> <span data-ttu-id="bc367-175">Si la fonction échoue, la valeur de retour est égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="bc367-175">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="bc367-176">Notes</span><span class="sxs-lookup"><span data-stu-id="bc367-176">Remarks</span></span>

<span data-ttu-id="bc367-177">Les paramètres de cette méthode sont très similaires à ceux de la fonction GDI [**DrawText**](/windows/win32/api/winuser/nf-winuser-drawtext) .</span><span class="sxs-lookup"><span data-stu-id="bc367-177">The parameters of this method are very similar to those of the GDI [**DrawText**](/windows/win32/api/winuser/nf-winuser-drawtext) function.</span></span>

<span data-ttu-id="bc367-178">Cette méthode prend en charge les chaînes ANSI et Unicode.</span><span class="sxs-lookup"><span data-stu-id="bc367-178">This method supports both ANSI and Unicode strings.</span></span>

<span data-ttu-id="bc367-179">Cette méthode doit être appelée à l’intérieur d’un [**BeginScene**](/windows/desktop/api) ... Bloc [**EndScene**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-endscene) .</span><span class="sxs-lookup"><span data-stu-id="bc367-179">This method must be called inside a [**BeginScene**](/windows/desktop/api) ... [**EndScene**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-endscene) block.</span></span> <span data-ttu-id="bc367-180">La seule exception est lorsqu’une application appelle **DrawText** avec DT \_ CALCRECT pour calculer la taille d’un bloc de texte donné.</span><span class="sxs-lookup"><span data-stu-id="bc367-180">The only exception is when an application calls **DrawText** with DT\_CALCRECT to calculate the size of a given block of text.</span></span>

<span data-ttu-id="bc367-181">À moins que le \_ format DT NOclip ne soit utilisé, cette méthode découpe le texte afin qu’il n’apparaisse pas en dehors du rectangle spécifié.</span><span class="sxs-lookup"><span data-stu-id="bc367-181">Unless the DT\_NOCLIP format is used, this method clips the text so that it does not appear outside the specified rectangle.</span></span> <span data-ttu-id="bc367-182">Toute la mise en forme est supposée avoir plusieurs lignes, sauf si le \_ format DT Singleline est spécifié.</span><span class="sxs-lookup"><span data-stu-id="bc367-182">All formatting is assumed to have multiple lines unless the DT\_SINGLELINE format is specified.</span></span>

<span data-ttu-id="bc367-183">Si la police sélectionnée est trop grande pour le rectangle, cette méthode n’essaie pas de remplacer une police plus petite.</span><span class="sxs-lookup"><span data-stu-id="bc367-183">If the selected font is too large for the rectangle, this method does not attempt to substitute a smaller font.</span></span>

<span data-ttu-id="bc367-184">Cette méthode prend en charge uniquement les polices dont l’échappement et l’orientation sont toutes deux égales à zéro.</span><span class="sxs-lookup"><span data-stu-id="bc367-184">This method supports only fonts whose escapement and orientation are both zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="bc367-185">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bc367-185">Requirements</span></span>



| <span data-ttu-id="bc367-186">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bc367-186">Requirement</span></span> | <span data-ttu-id="bc367-187">Valeur</span><span class="sxs-lookup"><span data-stu-id="bc367-187">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="bc367-188">En-tête</span><span class="sxs-lookup"><span data-stu-id="bc367-188">Header</span></span><br/>  | <dl> <span data-ttu-id="bc367-189"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="bc367-189"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="bc367-190">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="bc367-190">Library</span></span><br/> | <dl> <span data-ttu-id="bc367-191"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bc367-191"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="bc367-192">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bc367-192">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc367-193">ID3DXFont</span><span class="sxs-lookup"><span data-stu-id="bc367-193">ID3DXFont</span></span>](id3dxfont.md)
</dt> </dl>

 

 
