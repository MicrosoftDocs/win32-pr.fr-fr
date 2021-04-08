---
description: Fournit une recherche basée sur une expression approximative et non sensible à la casse pour les traits d’écriture analysés et les traits de dessin analysés qui ont des types reconnus.
ms.assetid: dfd481f9-38fd-433f-b1fc-697c735c13da
title: 'IInkAnalyzer :: SearchWithLanguageId, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.SearchWithLanguageId
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 829878a6fd326abb8a685b644cfc222ba6921385
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751796"
---
# <a name="iinkanalyzersearchwithlanguageid-method"></a><span data-ttu-id="a7f8b-103">IInkAnalyzer :: SearchWithLanguageId, méthode</span><span class="sxs-lookup"><span data-stu-id="a7f8b-103">IInkAnalyzer::SearchWithLanguageId method</span></span>

<span data-ttu-id="a7f8b-104">Fournit une recherche basée sur une expression approximative et non sensible à la casse pour les traits d’écriture analysés et les traits de dessin analysés qui ont des types reconnus.</span><span class="sxs-lookup"><span data-stu-id="a7f8b-104">Provides a fuzzy, case-insensitive phrase based search for analyzed writing strokes and analyzed drawing strokes that have recognized types.</span></span>

## <a name="syntax"></a><span data-ttu-id="a7f8b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a7f8b-105">Syntax</span></span>


```C++
HRESULT SearchWithLanguageId(
  [in]      BSTR  bstrPhraseToMatch,
  [in]      LONG  lSearchStringLanguageId,
  [in, out] ULONG *pulSearchResultCount,
  [out]     ULONG **ppulStrokeCountPerResult,
  [in, out] ULONG *pulStrokeIdsCount,
  [out]     ULONG **ppulStrokeIds
);
```



## <a name="parameters"></a><span data-ttu-id="a7f8b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a7f8b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a7f8b-107">*bstrPhraseToMatch* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a7f8b-107">*bstrPhraseToMatch* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a7f8b-108">Expression qui sera trouvée dans les alternatives pour les traits actuellement analysés.</span><span class="sxs-lookup"><span data-stu-id="a7f8b-108">The phrase that will be found in the alternates for the currently analyzed strokes.</span></span>

</dd> <dt>

<span data-ttu-id="a7f8b-109">*lSearchStringLanguageId* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a7f8b-109">*lSearchStringLanguageId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a7f8b-110">LCID associé à la chaîne qui est passée.</span><span class="sxs-lookup"><span data-stu-id="a7f8b-110">The LCID associated with the string that is passed.</span></span> <span data-ttu-id="a7f8b-111">Utilisé pour convertir le cas en interne pour prendre en charge les comparaisons qui ne respectent pas la casse.</span><span class="sxs-lookup"><span data-stu-id="a7f8b-111">Used to convert the case internally to support case insensitive comparisons.</span></span>

</dd> <dt>

<span data-ttu-id="a7f8b-112">*pulSearchResultCount* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="a7f8b-112">*pulSearchResultCount* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="a7f8b-113">Nombre maximal de résultats retournés par la recherche.</span><span class="sxs-lookup"><span data-stu-id="a7f8b-113">The maximum number of results returned from the search.</span></span>

</dd> <dt>

<span data-ttu-id="a7f8b-114">*ppulStrokeCountPerResult* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="a7f8b-114">*ppulStrokeCountPerResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a7f8b-115">Pointeur vers un tableau du nombre de traits dans chaque résultat de recherche.</span><span class="sxs-lookup"><span data-stu-id="a7f8b-115">Pointer to an array of the number of strokes in each search result.</span></span>

</dd> <dt>

<span data-ttu-id="a7f8b-116">*pulStrokeIdsCount* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="a7f8b-116">*pulStrokeIdsCount* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="a7f8b-117">Nombre d’ID de trait dans *ppulStrokeIds*.</span><span class="sxs-lookup"><span data-stu-id="a7f8b-117">The number of stroke IDs in *ppulStrokeIds*.</span></span>

</dd> <dt>

<span data-ttu-id="a7f8b-118">*ppulStrokeIds* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="a7f8b-118">*ppulStrokeIds* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a7f8b-119">Pointeur vers un tableau d’ID de trait représentant un jeu de traits.</span><span class="sxs-lookup"><span data-stu-id="a7f8b-119">Pointer to an array of stroke IDs representing a set of sets of strokes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a7f8b-120">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a7f8b-120">Return value</span></span>

<span data-ttu-id="a7f8b-121">Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.</span><span class="sxs-lookup"><span data-stu-id="a7f8b-121">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="a7f8b-122">Notes</span><span class="sxs-lookup"><span data-stu-id="a7f8b-122">Remarks</span></span>

<span data-ttu-id="a7f8b-123">Cette recherche recherche les sous-chaînes de mots multiples et à mots uniques.</span><span class="sxs-lookup"><span data-stu-id="a7f8b-123">This search finds multi-word and single word substrings.</span></span> <span data-ttu-id="a7f8b-124">Les résultats de la reconnaissance alternative et les autres segments sont recherchés.</span><span class="sxs-lookup"><span data-stu-id="a7f8b-124">Both alternate recognition results and alternate segmentations are searched.</span></span>

<span data-ttu-id="a7f8b-125">Toutes les chaînes entrantes seront converties en une seule casse pour la comparaison utilisant le LCID du thread actuel pour effectuer cette conversion en respectant les conventions de cas culturels.</span><span class="sxs-lookup"><span data-stu-id="a7f8b-125">All incoming strings will be converted to a single casing for comparison utilizing the LCID of the current thread to do this conversion to respect cultural case conventions.</span></span>

<span data-ttu-id="a7f8b-126">La chaîne transmise est traitée comme une expression.</span><span class="sxs-lookup"><span data-stu-id="a7f8b-126">The string passed is treated as a phrase.</span></span> <span data-ttu-id="a7f8b-127">Les mots et les caractères doivent apparaître dans le alterantes pour les traits dans l’ordre spécifié.</span><span class="sxs-lookup"><span data-stu-id="a7f8b-127">Words and characters must appear in the alterantes for the strokes in the order specified.</span></span> <span data-ttu-id="a7f8b-128">Les premier et dernier mots de l’expression peuvent être mis en correspondance en tant que sous-chaînes (le premier mot apparaissant à la fin d’un autre et le dernier mot apparaissant à l’begginging d’un), mais tous les autres mots (ceux qui se trouvent à l’intérieur de l’expression) doivent apparaître en tant que mots entiers.</span><span class="sxs-lookup"><span data-stu-id="a7f8b-128">The first and last words of the phrase may be matched as substrings (the first word appearing at the end of an alternate and the last word appearing at the begginging of one), but any other words (those inside of the phrase) must appear as whole words.</span></span>

<span data-ttu-id="a7f8b-129">Si la chaîne passée n’a pas d’espace blanc entre les caractères, la sous-chaîne peut être trouvée n’importe où dans un mot unique dans une autre.</span><span class="sxs-lookup"><span data-stu-id="a7f8b-129">If the string passed in has no whitespace in between characters, the substring may be found anywhere inside of a single word in an alternate.</span></span>

<span data-ttu-id="a7f8b-130">Seule la présence ou l’absence d’espace blanc entre les caractères modifie les résultats de la recherche.</span><span class="sxs-lookup"><span data-stu-id="a7f8b-130">Only the presence or absence of whitespace between characters changes the results of search.</span></span> <span data-ttu-id="a7f8b-131">Les espaces blancs qui ne sont pas entourés de caractères sont ignorés.</span><span class="sxs-lookup"><span data-stu-id="a7f8b-131">Whitespace that is not surrounded by characters is ignored.</span></span> <span data-ttu-id="a7f8b-132">Le type de l’espace blanc est ignoré (un onglet ou un espace entre les caractères donnera le même résultat).</span><span class="sxs-lookup"><span data-stu-id="a7f8b-132">The type of the whitespace is ignored (a tab or a space between characters will give the same result).</span></span> <span data-ttu-id="a7f8b-133">La quantité d’espace blanc n’a pas d’importance : un espace ou deux espaces entre les caractères donnent le même résultat.</span><span class="sxs-lookup"><span data-stu-id="a7f8b-133">The amount of whitespace does not matter - one space or two spaces in between characters will give the same result.</span></span>

<span data-ttu-id="a7f8b-134">La recherche ne génère pas d’événements PopulateContextNode.</span><span class="sxs-lookup"><span data-stu-id="a7f8b-134">Search does not generate PopulateContextNode events.</span></span> <span data-ttu-id="a7f8b-135">Seuls les traits qui ont déjà été remplis sont recherchés.</span><span class="sxs-lookup"><span data-stu-id="a7f8b-135">Only the strokes that have already been populated will be searched.</span></span>

## <a name="requirements"></a><span data-ttu-id="a7f8b-136">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a7f8b-136">Requirements</span></span>



| <span data-ttu-id="a7f8b-137">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a7f8b-137">Requirement</span></span> | <span data-ttu-id="a7f8b-138">Valeur</span><span class="sxs-lookup"><span data-stu-id="a7f8b-138">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a7f8b-139">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a7f8b-139">Minimum supported client</span></span><br/> | <span data-ttu-id="a7f8b-140">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a7f8b-140">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="a7f8b-141">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a7f8b-141">Minimum supported server</span></span><br/> | <span data-ttu-id="a7f8b-142">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="a7f8b-142">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="a7f8b-143">En-tête</span><span class="sxs-lookup"><span data-stu-id="a7f8b-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="a7f8b-144"><dt>IACom. h (nécessite également IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="a7f8b-144"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="a7f8b-145">DLL</span><span class="sxs-lookup"><span data-stu-id="a7f8b-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a7f8b-146"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a7f8b-146"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="a7f8b-147">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a7f8b-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a7f8b-148">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="a7f8b-148">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> </dl>

 

 




