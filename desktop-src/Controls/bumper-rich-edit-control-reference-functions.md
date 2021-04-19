---
title: Fonctions RichEdit
description: Fonctions RichEdit
ms.assetid: 5e913cb6-d561-447f-b33e-9160a8f46cda
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99f776b9a08095fa66645713e107a3d66920e80f
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "106537219"
---
# <a name="rich-edit-functions"></a><span data-ttu-id="d90be-103">Fonctions RichEdit</span><span class="sxs-lookup"><span data-stu-id="d90be-103">Rich Edit Functions</span></span>

## <a name="in-this-section"></a><span data-ttu-id="d90be-104">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="d90be-104">In this section</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d90be-105">Rubrique</span><span class="sxs-lookup"><span data-stu-id="d90be-105">Topic</span></span></th>
<th><span data-ttu-id="d90be-106">Description</span><span class="sxs-lookup"><span data-stu-id="d90be-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d90be-107"><a href="/windows/desktop/api/Richedit/nc-richedit-autocorrectproc"><em>AutoCorrectProc</em></a></span><span class="sxs-lookup"><span data-stu-id="d90be-107"><a href="/windows/desktop/api/Richedit/nc-richedit-autocorrectproc"><em>AutoCorrectProc</em></a></span></span><br/></td>
<td><span data-ttu-id="d90be-108">La fonction <a href="/windows/desktop/api/Richedit/nc-richedit-autocorrectproc"><em>AutoCorrectProc</em></a> est une fonction de rappel définie par l’application qui est utilisée avec le message <a href="em-setautocorrectproc.md"><strong>EM_SETAUTOCORRECTPROC</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="d90be-108">The <a href="/windows/desktop/api/Richedit/nc-richedit-autocorrectproc"><em>AutoCorrectProc</em></a> function is an application-defined callback function that is used with the <a href="em-setautocorrectproc.md"><strong>EM_SETAUTOCORRECTPROC</strong></a> message.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d90be-109"><a href="/windows/desktop/api/Richedit/nc-richedit-editstreamcallback"><em>EditStreamCallback</em></a></span><span class="sxs-lookup"><span data-stu-id="d90be-109"><a href="/windows/desktop/api/Richedit/nc-richedit-editstreamcallback"><em>EditStreamCallback</em></a></span></span><br/></td>
<td><span data-ttu-id="d90be-110">La fonction <a href="/windows/desktop/api/Richedit/nc-richedit-editstreamcallback"><em>EditStreamCallback</em></a> est une fonction de rappel définie par l’application utilisée avec les messages <a href="em-streamin.md"><strong>EM_STREAMIN</strong></a> et <a href="em-streamout.md"><strong>EM_STREAMOUT</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="d90be-110">The <a href="/windows/desktop/api/Richedit/nc-richedit-editstreamcallback"><em>EditStreamCallback</em></a> function is an application defined callback function used with the <a href="em-streamin.md"><strong>EM_STREAMIN</strong></a> and <a href="em-streamout.md"><strong>EM_STREAMOUT</strong></a> messages.</span></span> <span data-ttu-id="d90be-111">Il est utilisé pour transférer un flux de données vers ou à partir d’un contrôle RichEdit.</span><span class="sxs-lookup"><span data-stu-id="d90be-111">It is used to transfer a stream of data into or out of a rich edit control.</span></span> <span data-ttu-id="d90be-112">Le type <strong>EDITSTREAMCALLBACK</strong> définit un pointeur vers cette fonction de rappel.</span><span class="sxs-lookup"><span data-stu-id="d90be-112">The <strong>EDITSTREAMCALLBACK</strong> type defines a pointer to this callback function.</span></span> <span data-ttu-id="d90be-113"><em>EditStreamCallback</em> est un espace réservé pour le nom de la fonction définie par l’application.</span><span class="sxs-lookup"><span data-stu-id="d90be-113"><em>EditStreamCallback</em> is a placeholder for the application-defined function name.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d90be-114"><a href="/windows/desktop/api/Richedit/nc-richedit-editwordbreakprocex"><em>EditWordBreakProcEx</em></a></span><span class="sxs-lookup"><span data-stu-id="d90be-114"><a href="/windows/desktop/api/Richedit/nc-richedit-editwordbreakprocex"><em>EditWordBreakProcEx</em></a></span></span><br/></td>
<td><span data-ttu-id="d90be-115">La fonction <a href="/windows/desktop/api/Richedit/nc-richedit-editwordbreakprocex"><em>EditWordBreakProcEx</em></a> est une fonction de rappel définie par l’application utilisée avec le message <a href="em-setwordbreakprocex.md"><strong>EM_SETWORDBREAKPROCEX</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="d90be-115">The <a href="/windows/desktop/api/Richedit/nc-richedit-editwordbreakprocex"><em>EditWordBreakProcEx</em></a> function is an application defined callback function used with the <a href="em-setwordbreakprocex.md"><strong>EM_SETWORDBREAKPROCEX</strong></a> message.</span></span> <span data-ttu-id="d90be-116">Il détermine l’index de caractère de l’arrêt de mot ou la classe de caractères et les indicateurs de césure lexicale des caractères du texte spécifié.</span><span class="sxs-lookup"><span data-stu-id="d90be-116">It determines the character index of the word break or the character class and word-break flags of the characters in the specified text.</span></span> <span data-ttu-id="d90be-117">Le type <strong>EDITWORDBREAKPROCEX</strong> définit un pointeur vers cette fonction de rappel.</span><span class="sxs-lookup"><span data-stu-id="d90be-117">The <strong>EDITWORDBREAKPROCEX</strong> type defines a pointer to this callback function.</span></span> <span data-ttu-id="d90be-118"><em>EditWordBreakProcEx</em> est un espace réservé pour le nom de la fonction définie par l’application.</span><span class="sxs-lookup"><span data-stu-id="d90be-118"><em>EditWordBreakProcEx</em> is a placeholder for the application-defined function name.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d90be-119"><a href="/previous-versions/windows/desktop/legacy/hh780353(v=vs.85)"><strong>GetMathAlphanumeric</strong></a></span><span class="sxs-lookup"><span data-stu-id="d90be-119"><a href="/previous-versions/windows/desktop/legacy/hh780353(v=vs.85)"><strong>GetMathAlphanumeric</strong></a></span></span><br/></td>
<td><span data-ttu-id="d90be-120">Récupère le caractère alphanumérique de transformation UTF (Unicode Transformation Format)-32 qui correspond au caractère BMP (Basic Multilingual Plane) et au style mathématique spécifiés.</span><span class="sxs-lookup"><span data-stu-id="d90be-120">Retrieves the Unicode Transformation Format (UTF)-32 math alphanumeric character that corresponds to the specified Basic Multilingual Plane (BMP) character and math style.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d90be-121"><a href="/previous-versions/windows/desktop/legacy/hh780354(v=vs.85)"><strong>GetMathAlphanumericCode</strong></a></span><span class="sxs-lookup"><span data-stu-id="d90be-121"><a href="/previous-versions/windows/desktop/legacy/hh780354(v=vs.85)"><strong>GetMathAlphanumericCode</strong></a></span></span><br/></td>
<td><span data-ttu-id="d90be-122">Récupère le style mathématique et le code de caractère BMP (Basic Multilingual Plane) qui correspond à l’octet de fin spécifié d’une paire de substitution mathématique.</span><span class="sxs-lookup"><span data-stu-id="d90be-122">Retrieves the math style and the upright Basic Multilingual Plane (BMP) character code that corresponds to the specified trailing byte of a math surrogate pair.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d90be-123"><a href="/windows/desktop/api/Richedit/nf-richedit-hyphenateproc"><em>HyphenateProc</em></a></span><span class="sxs-lookup"><span data-stu-id="d90be-123"><a href="/windows/desktop/api/Richedit/nf-richedit-hyphenateproc"><em>HyphenateProc</em></a></span></span><br/></td>
<td><span data-ttu-id="d90be-124">La fonction <a href="/windows/desktop/api/Richedit/nf-richedit-hyphenateproc"><em>HyphenateProc</em></a> est une fonction de rappel définie par l’application utilisée avec le message <a href="em-sethyphenateinfo.md"><strong>EM_SETHYPHENATEINFO</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="d90be-124">The <a href="/windows/desktop/api/Richedit/nf-richedit-hyphenateproc"><em>HyphenateProc</em></a> function is an application defined callback function used with the <a href="em-sethyphenateinfo.md"><strong>EM_SETHYPHENATEINFO</strong></a> message.</span></span> <span data-ttu-id="d90be-125">Elle détermine la façon dont la césure est effectuée dans un contrôle Rich Edit Microsoft.</span><span class="sxs-lookup"><span data-stu-id="d90be-125">It determines how hyphenation is done in a Microsoft Rich Edit control.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d90be-126"><a href="/previous-versions/windows/desktop/legacy/hh780443(v=vs.85)"><strong>MathBuildDown</strong></a></span><span class="sxs-lookup"><span data-stu-id="d90be-126"><a href="/previous-versions/windows/desktop/legacy/hh780443(v=vs.85)"><strong>MathBuildDown</strong></a></span></span><br/></td>
<td><span data-ttu-id="d90be-127">Traduit les objets incorporés Math, Ruby et other inclus dans la plage spécifiée au format linéaire.</span><span class="sxs-lookup"><span data-stu-id="d90be-127">Translates the built-up math, ruby, and other inline objects in the specified range to linear form.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d90be-128"><a href="/previous-versions/windows/desktop/legacy/hh780445(v=vs.85)"><strong>MathBuildUp</strong></a></span><span class="sxs-lookup"><span data-stu-id="d90be-128"><a href="/previous-versions/windows/desktop/legacy/hh780445(v=vs.85)"><strong>MathBuildUp</strong></a></span></span><br/></td>
<td><span data-ttu-id="d90be-129">Convertit les maths de format linéaire d’une plage en un formulaire intégré, ou modifie le formulaire de création actuel.</span><span class="sxs-lookup"><span data-stu-id="d90be-129">Converts the linear-format math in a range to a built-up form, or modifies the current built-up form.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d90be-130"><a href="/previous-versions/windows/desktop/legacy/hh780446(v=vs.85)"><strong>MathTranslate</strong></a></span><span class="sxs-lookup"><span data-stu-id="d90be-130"><a href="/previous-versions/windows/desktop/legacy/hh780446(v=vs.85)"><strong>MathTranslate</strong></a></span></span><br/></td>
<td><span data-ttu-id="d90be-131">Traduit les caractères mathématiques dans la plage spécifiée.</span><span class="sxs-lookup"><span data-stu-id="d90be-131">Translates the math characters in the specified range.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d90be-132"><a href="reextendedregisterclass.md"><strong>REExtendedRegisterClass</strong></a></span><span class="sxs-lookup"><span data-stu-id="d90be-132"><a href="reextendedregisterclass.md"><strong>REExtendedRegisterClass</strong></a></span></span><br/></td>
<td><span data-ttu-id="d90be-133">Inscrit deux noms de classe, REListBox20W et RECombobox20W, qui peuvent être utilisés pour créer des fenêtres modifiables RichEdit ou de zone de liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="d90be-133">Registers two class names, REListBox20W and RECombobox20W, that could be used to create Rich Edit listbox or combobox windows.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="d90be-134">Destiné à un usage interne ; non recommandé pour une utilisation dans les applications.</span><span class="sxs-lookup"><span data-stu-id="d90be-134">Intended for internal use; not recommended for use in applications.</span></span> <span data-ttu-id="d90be-135">Cette fonction peut ne pas être prise en charge dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="d90be-135">This function may not be supported in future versions.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

 

