---
description: Pour une application traitant du texte non mis en forme, Uniscribe fournit les \* fonctions ScriptString.
ms.assetid: bfbba5df-ce06-4012-a7b1-55d8ea580942
title: Utilisation des fonctions ScriptString
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93a2df5e7515bd605ad48cc7a246941e9b6f08f2
ms.sourcegitcommit: 3d718d8f69d3f86eaecf94c5705d761c5a9ef4a1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/20/2020
ms.locfileid: "104032050"
---
# <a name="using-the-scriptstring-functions"></a><span data-ttu-id="c2787-103">Utilisation des fonctions ScriptString</span><span class="sxs-lookup"><span data-stu-id="c2787-103">Using the ScriptString Functions</span></span>

<span data-ttu-id="c2787-104">Pour une application traitant du texte non mis en forme, Uniscribe fournit les fonctions **ScriptString \*** .</span><span class="sxs-lookup"><span data-stu-id="c2787-104">For an application dealing with unformatted text, Uniscribe provides the **ScriptString\*** functions.</span></span> <span data-ttu-id="c2787-105">Ces fonctions sont similaires à [**ExtTextOut**](/windows/win32/api/wingdi/nf-wingdi-exttextouta), [**DrawText**](/windows/win32/api/winuser/nf-winuser-drawtext)et [**GetTextExtent**](/cpp/mfc/reference/cdc-class#gettextextent), mais elles fournissent une prise en charge complète des scripts, y compris l’emplacement du signe insertion.</span><span class="sxs-lookup"><span data-stu-id="c2787-105">These functions are similar to [**ExtTextOut**](/windows/win32/api/wingdi/nf-wingdi-exttextouta), [**DrawText**](/windows/win32/api/winuser/nf-winuser-drawtext), and [**GetTextExtent**](/cpp/mfc/reference/cdc-class#gettextextent), but they provide full complex script support, including caret placement.</span></span> <span data-ttu-id="c2787-106">Ces fonctions sont similaires aux autres fonctions Uniscribe, mais elles sont adaptées aux exigences de traitement de texte brut les plus simples.</span><span class="sxs-lookup"><span data-stu-id="c2787-106">These functions are similar to the other Uniscribe functions, but are tailored to the simpler requirements of plain text processing.</span></span>

<span data-ttu-id="c2787-107">Le tableau suivant détaille les fonctions **ScriptString \*** et tous les équivalents dans les autres fonctions Uniscribe.</span><span class="sxs-lookup"><span data-stu-id="c2787-107">The following table details the **ScriptString\*** functions and any counterparts in the other Uniscribe functions.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="c2787-108">Fonction</span><span class="sxs-lookup"><span data-stu-id="c2787-108">Function</span></span></th>
<th><span data-ttu-id="c2787-109">Description</span><span class="sxs-lookup"><span data-stu-id="c2787-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c2787-110"><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstringanalyse"><strong>ScriptStringAnalyse</strong></a></span><span class="sxs-lookup"><span data-stu-id="c2787-110"><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstringanalyse"><strong>ScriptStringAnalyse</strong></a></span></span></td>
<td><span data-ttu-id="c2787-111">Analyse le texte brut.</span><span class="sxs-lookup"><span data-stu-id="c2787-111">Analyzes plain text.</span></span> <span data-ttu-id="c2787-112">Cette fonction correspond aux fonctions suivantes :</span><span class="sxs-lookup"><span data-stu-id="c2787-112">This function corresponds to the following functions:</span></span><br/> <dl><span data-ttu-id="c2787-113"><a href="/windows/desktop/api/Usp10/nf-usp10-scriptitemize"><strong>ScriptItemize</strong></a></span><span class="sxs-lookup"><span data-stu-id="c2787-113"><a href="/windows/desktop/api/Usp10/nf-usp10-scriptitemize"><strong>ScriptItemize</strong></a></span></span><br /><span data-ttu-id="c2787-114">
<a href="/windows/desktop/api/Usp10/nf-usp10-scriptshape"><strong>ScriptShape</strong></a></span><span class="sxs-lookup"><span data-stu-id="c2787-114">
<a href="/windows/desktop/api/Usp10/nf-usp10-scriptshape"><strong>ScriptShape</strong></a></span></span><br /><span data-ttu-id="c2787-115">
<a href="/windows/desktop/api/Usp10/nf-usp10-scriptplace"><strong>ScriptPlace</strong></a></span><span class="sxs-lookup"><span data-stu-id="c2787-115">
<a href="/windows/desktop/api/Usp10/nf-usp10-scriptplace"><strong>ScriptPlace</strong></a></span></span><br /><span data-ttu-id="c2787-116">
<a href="/windows/desktop/api/Usp10/nf-usp10-scriptbreak"><strong>ScriptBreak</strong></a></span><span class="sxs-lookup"><span data-stu-id="c2787-116">
<a href="/windows/desktop/api/Usp10/nf-usp10-scriptbreak"><strong>ScriptBreak</strong></a></span></span><br /><span data-ttu-id="c2787-117">
<a href="/windows/desktop/api/Usp10/nf-usp10-scriptgetcmap"><strong>ScriptGetCMap</strong></a></span><span class="sxs-lookup"><span data-stu-id="c2787-117">
<a href="/windows/desktop/api/Usp10/nf-usp10-scriptgetcmap"><strong>ScriptGetCMap</strong></a></span></span><br /><span data-ttu-id="c2787-118">
<a href="/windows/desktop/api/Usp10/nf-usp10-scriptjustify"><strong>ScriptJustify</strong></a></span><span class="sxs-lookup"><span data-stu-id="c2787-118">
<a href="/windows/desktop/api/Usp10/nf-usp10-scriptjustify"><strong>ScriptJustify</strong></a></span></span><br /><span data-ttu-id="c2787-119">
<a href="/windows/desktop/api/Usp10/nf-usp10-scriptlayout"><strong>ScriptLayout</strong></a></span><span class="sxs-lookup"><span data-stu-id="c2787-119">
<a href="/windows/desktop/api/Usp10/nf-usp10-scriptlayout"><strong>ScriptLayout</strong></a></span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c2787-120"><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstringcptox"><strong>ScriptStringCPtoX</strong></a></span><span class="sxs-lookup"><span data-stu-id="c2787-120"><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstringcptox"><strong>ScriptStringCPtoX</strong></a></span></span></td>
<td><span data-ttu-id="c2787-121">Récupère la coordonnée x d’une position de caractère.</span><span class="sxs-lookup"><span data-stu-id="c2787-121">Retrieves the x coordinate for a character position.</span></span> <span data-ttu-id="c2787-122">Cette fonction correspond à <a href="/windows/desktop/api/Usp10/nf-usp10-scriptcptox"><strong>ScriptCPtoX</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="c2787-122">This function corresponds to <a href="/windows/desktop/api/Usp10/nf-usp10-scriptcptox"><strong>ScriptCPtoX</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c2787-123"><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstringfree"><strong>ScriptStringFree</strong></a></span><span class="sxs-lookup"><span data-stu-id="c2787-123"><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstringfree"><strong>ScriptStringFree</strong></a></span></span></td>
<td><span data-ttu-id="c2787-124">Libère une structure <a href="script-string-analysis.md"><strong>SCRIPT_STRING_ANALYSIS</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="c2787-124">Frees a <a href="script-string-analysis.md"><strong>SCRIPT_STRING_ANALYSIS</strong></a> structure.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c2787-125"><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstringgetlogicalwidths"><strong>ScriptStringGetLogicalWidths</strong></a></span><span class="sxs-lookup"><span data-stu-id="c2787-125"><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstringgetlogicalwidths"><strong>ScriptStringGetLogicalWidths</strong></a></span></span></td>
<td><span data-ttu-id="c2787-126">Convertit les largeurs visuelles en largeurs logiques.</span><span class="sxs-lookup"><span data-stu-id="c2787-126">Converts visual widths to logical widths.</span></span> <span data-ttu-id="c2787-127">Cette fonction correspond à <a href="/windows/desktop/api/Usp10/nf-usp10-scriptgetlogicalwidths"><strong>ScriptGetLogicalWidths</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="c2787-127">This function corresponds to <a href="/windows/desktop/api/Usp10/nf-usp10-scriptgetlogicalwidths"><strong>ScriptGetLogicalWidths</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c2787-128"><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstringgetorder"><strong>ScriptStringGetOrder</strong></a></span><span class="sxs-lookup"><span data-stu-id="c2787-128"><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstringgetorder"><strong>ScriptStringGetOrder</strong></a></span></span></td>
<td><span data-ttu-id="c2787-129">Mappe les positions des glyphes de caractères d’une façon similaire à <a href="/windows/desktop/api/wingdi/nf-wingdi-getcharacterplacementa">GetCharacterPlacement</a>, pour une utilisation héritée uniquement.</span><span class="sxs-lookup"><span data-stu-id="c2787-129">Maps character glyph positions in a similar way to <a href="/windows/desktop/api/wingdi/nf-wingdi-getcharacterplacementa">GetCharacterPlacement</a>, for legacy use only.</span></span> <span data-ttu-id="c2787-130">Cette fonction ne fonctionne pas correctement avec les scripts qui génèrent plus d’un glyphe par point de code.</span><span class="sxs-lookup"><span data-stu-id="c2787-130">This function does not work well with scripts that generate more than one glyph per code point.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c2787-131"><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstringout"><strong>ScriptStringOut</strong></a></span><span class="sxs-lookup"><span data-stu-id="c2787-131"><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstringout"><strong>ScriptStringOut</strong></a></span></span></td>
<td><span data-ttu-id="c2787-132">Affiche du texte brut.</span><span class="sxs-lookup"><span data-stu-id="c2787-132">Displays plain text.</span></span> <span data-ttu-id="c2787-133">Cette fonction correspond à <a href="/windows/desktop/api/Usp10/nf-usp10-scripttextout"><strong>ScriptTextOut</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="c2787-133">This function corresponds to <a href="/windows/desktop/api/Usp10/nf-usp10-scripttextout"><strong>ScriptTextOut</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c2787-134"><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstring_pcoutchars"><strong>ScriptString_pcOutChars</strong></a></span><span class="sxs-lookup"><span data-stu-id="c2787-134"><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstring_pcoutchars"><strong>ScriptString_pcOutChars</strong></a></span></span></td>
<td><span data-ttu-id="c2787-135">Retourne un pointeur vers la longueur d’une chaîne de texte brut découpé.</span><span class="sxs-lookup"><span data-stu-id="c2787-135">Returns a pointer to the length of a clipped plain text string.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c2787-136"><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstring_plogattr"><strong>ScriptString_pLogAttr</strong></a></span><span class="sxs-lookup"><span data-stu-id="c2787-136"><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstring_plogattr"><strong>ScriptString_pLogAttr</strong></a></span></span></td>
<td><span data-ttu-id="c2787-137">Retourne un pointeur vers la mémoire tampon d’attributs logiques pour une chaîne de texte brut analysée.</span><span class="sxs-lookup"><span data-stu-id="c2787-137">Returns a pointer to the logical attributes buffer for an analyzed plain text string.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c2787-138"><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstring_psize"><strong>ScriptString_pSize</strong></a></span><span class="sxs-lookup"><span data-stu-id="c2787-138"><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstring_psize"><strong>ScriptString_pSize</strong></a></span></span></td>
<td><span data-ttu-id="c2787-139">Retourne un pointeur vers la taille (largeur et hauteur) d’une chaîne de texte brut analysée.</span><span class="sxs-lookup"><span data-stu-id="c2787-139">Returns a pointer to the size (width and height) for an analyzed plain text string.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c2787-140"><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstringvalidate"><strong>ScriptStringValidate</strong></a></span><span class="sxs-lookup"><span data-stu-id="c2787-140"><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstringvalidate"><strong>ScriptStringValidate</strong></a></span></span></td>
<td><span data-ttu-id="c2787-141">Identifie les séquences de points de code non valides dans le script donné.</span><span class="sxs-lookup"><span data-stu-id="c2787-141">Identifies code point sequences not valid in the given script.</span></span> <span data-ttu-id="c2787-142">Cette fonction est différente de <a href="/windows/desktop/api/Usp10/nf-usp10-scriptgetcmap"><strong>ScriptGetCMap</strong></a>, qui identifie les points de code qui ne sont pas présents dans une police.</span><span class="sxs-lookup"><span data-stu-id="c2787-142">This function is different from <a href="/windows/desktop/api/Usp10/nf-usp10-scriptgetcmap"><strong>ScriptGetCMap</strong></a>, which identifies code points not present in a font.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c2787-143"><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstringxtocp"><strong>ScriptStringXtoCP</strong></a></span><span class="sxs-lookup"><span data-stu-id="c2787-143"><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstringxtocp"><strong>ScriptStringXtoCP</strong></a></span></span></td>
<td><span data-ttu-id="c2787-144">Convertit une coordonnée x en une position de caractère.</span><span class="sxs-lookup"><span data-stu-id="c2787-144">Converts an x coordinate to a character position.</span></span> <span data-ttu-id="c2787-145">Cette fonction correspond à <a href="/windows/desktop/api/Usp10/nf-usp10-scriptxtocp"><strong>ScriptXtoCP</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="c2787-145">This function corresponds to <a href="/windows/desktop/api/Usp10/nf-usp10-scriptxtocp"><strong>ScriptXtoCP</strong></a>.</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="c2787-146">Pour afficher uniquement du texte brut sans aucune modification, une application doit appeler [**ScriptStringAnalyse**](/windows/desktop/api/Usp10/nf-usp10-scriptstringanalyse), [**ScriptStringOut**](/windows/desktop/api/Usp10/nf-usp10-scriptstringout), puis [**ScriptStringFree**](/windows/desktop/api/Usp10/nf-usp10-scriptstringfree).</span><span class="sxs-lookup"><span data-stu-id="c2787-146">To only display plain text without any modifications, an application should call [**ScriptStringAnalyse**](/windows/desktop/api/Usp10/nf-usp10-scriptstringanalyse), [**ScriptStringOut**](/windows/desktop/api/Usp10/nf-usp10-scriptstringout), and then [**ScriptStringFree**](/windows/desktop/api/Usp10/nf-usp10-scriptstringfree).</span></span> <span data-ttu-id="c2787-147">Les autres fonctions sont utilisées pour modifier le texte brut avant l’affichage.</span><span class="sxs-lookup"><span data-stu-id="c2787-147">The other functions are used to modify the plain text before display.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c2787-148">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c2787-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c2787-149">Utilisation de Uniscribe</span><span class="sxs-lookup"><span data-stu-id="c2787-149">Using Uniscribe</span></span>](using-uniscribe.md)
</dt> </dl>

 

 
