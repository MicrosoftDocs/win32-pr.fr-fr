---
title: Utilisation de macros pour la gestion des erreurs
description: COM définit un certain nombre de macros qui facilitent l’utilisation des valeurs HRESULT.
ms.assetid: ad28eb80-cab9-4bec-9601-34660f6dcad4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6605ecc05f2d24d3671d28becd770b15d56e1413
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103730421"
---
# <a name="using-macros-for-error-handling"></a><span data-ttu-id="601ca-103">Utilisation de macros pour la gestion des erreurs</span><span class="sxs-lookup"><span data-stu-id="601ca-103">Using Macros for Error Handling</span></span>

<span data-ttu-id="601ca-104">COM définit un certain nombre de macros qui facilitent l’utilisation des valeurs **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="601ca-104">COM defines a number of macros that make it easier to work with **HRESULT** values.</span></span>

<span data-ttu-id="601ca-105">Les macros de gestion des erreurs sont décrites dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="601ca-105">The error handling macros are described in the following table.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="601ca-106">Macro</span><span class="sxs-lookup"><span data-stu-id="601ca-106">Macro</span></span></th>
<th><span data-ttu-id="601ca-107">Description</span><span class="sxs-lookup"><span data-stu-id="601ca-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="601ca-108"><a href="/windows/desktop/api/dmerror/nf-dmerror-make_hresult"><strong>MAKE_HRESULT</strong></a></span><span class="sxs-lookup"><span data-stu-id="601ca-108"><a href="/windows/desktop/api/dmerror/nf-dmerror-make_hresult"><strong>MAKE_HRESULT</strong></a></span></span><br/></td>
<td><span data-ttu-id="601ca-109">Retourne un <strong>HRESULT</strong> en fonction du bit de gravité, du code d’installation et du code d’erreur qui composent le <strong>HRESULT</strong>.</span><span class="sxs-lookup"><span data-stu-id="601ca-109">Returns an <strong>HRESULT</strong> given the severity bit, facility code, and error code that comprise the <strong>HRESULT</strong>.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="601ca-110">L’appel de <a href="/windows/desktop/api/dmerror/nf-dmerror-make_hresult"><strong>MAKE_HRESULT</strong></a> pour la vérification de S_OK entraîne une baisse des performances.</span><span class="sxs-lookup"><span data-stu-id="601ca-110">Calling <a href="/windows/desktop/api/dmerror/nf-dmerror-make_hresult"><strong>MAKE_HRESULT</strong></a> for S_OK verification carries a performance penalty.</span></span> <span data-ttu-id="601ca-111">Vous ne devez pas utiliser régulièrement <strong>MAKE_HRESULT</strong> pour obtenir des résultats corrects.</span><span class="sxs-lookup"><span data-stu-id="601ca-111">You should not routinely use <strong>MAKE_HRESULT</strong> for successful results.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="601ca-112"><a href="/windows/desktop/api/Winerror/nf-winerror-make_scode"><strong>MAKE_SCODE</strong></a></span><span class="sxs-lookup"><span data-stu-id="601ca-112"><a href="/windows/desktop/api/Winerror/nf-winerror-make_scode"><strong>MAKE_SCODE</strong></a></span></span><br/></td>
<td><span data-ttu-id="601ca-113">Retourne un <strong>SCODE</strong> en fonction du bit de gravité, du code d’installation et du code d’erreur qui composent le <strong>SCODE</strong>.</span><span class="sxs-lookup"><span data-stu-id="601ca-113">Returns an <strong>SCODE</strong> given the severity bit, facility code, and error code that comprise the <strong>SCODE</strong>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="601ca-114"><a href="/windows/desktop/api/Winerror/nf-winerror-hresult_code"><strong>HRESULT_CODE</strong></a></span><span class="sxs-lookup"><span data-stu-id="601ca-114"><a href="/windows/desktop/api/Winerror/nf-winerror-hresult_code"><strong>HRESULT_CODE</strong></a></span></span><br/></td>
<td><span data-ttu-id="601ca-115">Extrait la partie du code d’erreur de <strong>HRESULT</strong>.</span><span class="sxs-lookup"><span data-stu-id="601ca-115">Extracts the error code portion of the <strong>HRESULT</strong>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="601ca-116"><a href="/windows/desktop/api/Winerror/nf-winerror-hresult_facility"><strong>HRESULT_FACILITY</strong></a></span><span class="sxs-lookup"><span data-stu-id="601ca-116"><a href="/windows/desktop/api/Winerror/nf-winerror-hresult_facility"><strong>HRESULT_FACILITY</strong></a></span></span><br/></td>
<td><span data-ttu-id="601ca-117">Extrait le code d’installation de la valeur <strong>HRESULT</strong>.</span><span class="sxs-lookup"><span data-stu-id="601ca-117">Extracts the facility code of the <strong>HRESULT</strong>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="601ca-118"><a href="/windows/desktop/api/Winerror/nf-winerror-hresult_severity"><strong>HRESULT_SEVERITY</strong></a></span><span class="sxs-lookup"><span data-stu-id="601ca-118"><a href="/windows/desktop/api/Winerror/nf-winerror-hresult_severity"><strong>HRESULT_SEVERITY</strong></a></span></span><br/></td>
<td><span data-ttu-id="601ca-119">Extrait le bit de gravité de <strong>HRESULT</strong>.</span><span class="sxs-lookup"><span data-stu-id="601ca-119">Extracts the severity bit of the <strong>HRESULT</strong>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="601ca-120"><a href="/windows/desktop/api/Winerror/nf-winerror-scode_code"><strong>SCODE_CODE</strong></a></span><span class="sxs-lookup"><span data-stu-id="601ca-120"><a href="/windows/desktop/api/Winerror/nf-winerror-scode_code"><strong>SCODE_CODE</strong></a></span></span><br/></td>
<td><span data-ttu-id="601ca-121">Extrait la partie du code d’erreur du <strong>SCODE</strong>.</span><span class="sxs-lookup"><span data-stu-id="601ca-121">Extracts the error code portion of the <strong>SCODE</strong>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="601ca-122"><a href="/windows/desktop/api/Winerror/nf-winerror-scode_facility"><strong>SCODE_FACILITY</strong></a></span><span class="sxs-lookup"><span data-stu-id="601ca-122"><a href="/windows/desktop/api/Winerror/nf-winerror-scode_facility"><strong>SCODE_FACILITY</strong></a></span></span><br/></td>
<td><span data-ttu-id="601ca-123">Extrait le code d’installation du <strong>SCODE</strong>.</span><span class="sxs-lookup"><span data-stu-id="601ca-123">Extracts the facility code of the <strong>SCODE</strong>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="601ca-124"><a href="/windows/desktop/api/Winerror/nf-winerror-scode_severity"><strong>SCODE_SEVERITY</strong></a></span><span class="sxs-lookup"><span data-stu-id="601ca-124"><a href="/windows/desktop/api/Winerror/nf-winerror-scode_severity"><strong>SCODE_SEVERITY</strong></a></span></span><br/></td>
<td><span data-ttu-id="601ca-125">Extrait le champ de gravité du <strong>SCODE</strong>.</span><span class="sxs-lookup"><span data-stu-id="601ca-125">Extracts the severity field of the <strong>SCODE</strong>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="601ca-126"><a href="/windows/desktop/api/Winerror/nf-winerror-succeeded"><strong>A réussi</strong></a></span><span class="sxs-lookup"><span data-stu-id="601ca-126"><a href="/windows/desktop/api/Winerror/nf-winerror-succeeded"><strong>SUCCEEDED</strong></a></span></span><br/></td>
<td><span data-ttu-id="601ca-127">Teste le bit de gravité de <strong>SCODE</strong> ou <strong>HRESULT</strong>; retourne la <strong>valeur true</strong> si la gravité est égale à zéro et la <strong>valeur false</strong> si c’est un.</span><span class="sxs-lookup"><span data-stu-id="601ca-127">Tests the severity bit of the <strong>SCODE</strong> or <strong>HRESULT</strong>; returns <strong>TRUE</strong> if the severity is zero and <strong>FALSE</strong> if it is one.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="601ca-128"><a href="/windows/desktop/api/Winerror/nf-winerror-failed"><strong>DÉFECTUEUX</strong></a></span><span class="sxs-lookup"><span data-stu-id="601ca-128"><a href="/windows/desktop/api/Winerror/nf-winerror-failed"><strong>FAILED</strong></a></span></span><br/></td>
<td><span data-ttu-id="601ca-129">Teste le bit de gravité de <strong>SCODE</strong> ou <strong>HRESULT</strong>; retourne la <strong>valeur true</strong> si la gravité est égale à 1 et <strong>false</strong> si elle est égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="601ca-129">Tests the severity bit of the <strong>SCODE</strong> or <strong>HRESULT</strong>; returns <strong>TRUE</strong> if the severity is one and <strong>FALSE</strong> if it is zero.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="601ca-130"><a href="/windows/desktop/api/Winerror/nf-winerror-is_error"><strong>IS_ERROR</strong></a></span><span class="sxs-lookup"><span data-stu-id="601ca-130"><a href="/windows/desktop/api/Winerror/nf-winerror-is_error"><strong>IS_ERROR</strong></a></span></span><br/></td>
<td><span data-ttu-id="601ca-131">Fournit un test générique des erreurs sur toute valeur d’État.</span><span class="sxs-lookup"><span data-stu-id="601ca-131">Provides a generic test for errors on any status value.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="601ca-132"><a href="/windows/desktop/api/Winerror/nf-winerror-hresult_from_win32"><strong>HRESULT_FROM_WIN32</strong></a></span><span class="sxs-lookup"><span data-stu-id="601ca-132"><a href="/windows/desktop/api/Winerror/nf-winerror-hresult_from_win32"><strong>HRESULT_FROM_WIN32</strong></a></span></span><br/></td>
<td><span data-ttu-id="601ca-133">Mappe un <a href="/windows/desktop/Debug/system-error-codes">code d’erreur système</a> à une valeur <strong>HRESULT</strong> .</span><span class="sxs-lookup"><span data-stu-id="601ca-133">Maps a <a href="/windows/desktop/Debug/system-error-codes">system error code</a> to an <strong>HRESULT</strong> value.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="601ca-134"><a href="/windows/desktop/api/Winerror/nf-winerror-hresult_from_nt"><strong>HRESULT_FROM_NT</strong></a></span><span class="sxs-lookup"><span data-stu-id="601ca-134"><a href="/windows/desktop/api/Winerror/nf-winerror-hresult_from_nt"><strong>HRESULT_FROM_NT</strong></a></span></span><br/></td>
<td><span data-ttu-id="601ca-135">Mappe une valeur d’état NT à une valeur <strong>HRESULT</strong> .</span><span class="sxs-lookup"><span data-stu-id="601ca-135">Maps an NT status value to an <strong>HRESULT</strong> value.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="601ca-136">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="601ca-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="601ca-137">Gestion des erreurs dans COM</span><span class="sxs-lookup"><span data-stu-id="601ca-137">Error Handling in COM</span></span>](error-handling-in-com.md)
</dt> </dl>

 

