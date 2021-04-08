---
description: Récupère des données spécifiques à l’application ou d’autres données de propriété pour l’identificateur spécifié.
ms.assetid: eaf95ff8-7b31-4c05-aa49-0c3bb9e996c0
title: 'IContextNode :: GetPropertyData, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.GetPropertyData
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 381d137dd73056a2a6f4c2e9cd3746f9f16c5b2e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751845"
---
# <a name="icontextnodegetpropertydata-method"></a><span data-ttu-id="e2c3a-103">IContextNode :: GetPropertyData, méthode</span><span class="sxs-lookup"><span data-stu-id="e2c3a-103">IContextNode::GetPropertyData method</span></span>

<span data-ttu-id="e2c3a-104">Récupère des données spécifiques à l’application ou d’autres données de propriété pour l’identificateur spécifié.</span><span class="sxs-lookup"><span data-stu-id="e2c3a-104">Retrieves application-specific data or other property data for the specified identifier.</span></span>

## <a name="syntax"></a><span data-ttu-id="e2c3a-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e2c3a-105">Syntax</span></span>


```C++
HRESULT GetPropertyData(
  [in]      const GUID  *pPropertyDataId,
  [in, out]       ULONG *pulPropertyDataSize,
  [out]           BYTE  **ppbPropertyData
);
```



## <a name="parameters"></a><span data-ttu-id="e2c3a-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e2c3a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e2c3a-107">*pPropertyDataId* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e2c3a-107">*pPropertyDataId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e2c3a-108">Identificateur des données.</span><span class="sxs-lookup"><span data-stu-id="e2c3a-108">The identifier for the data.</span></span>

</dd> <dt>

<span data-ttu-id="e2c3a-109">*pulPropertyDataSize* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="e2c3a-109">*pulPropertyDataSize* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="e2c3a-110">Taille des données en octets.</span><span class="sxs-lookup"><span data-stu-id="e2c3a-110">The size of the data in bytes.</span></span> <span data-ttu-id="e2c3a-111">La valeur transmise n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="e2c3a-111">The value that is passed in is not used.</span></span>

</dd> <dt>

<span data-ttu-id="e2c3a-112">*ppbPropertyData* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="e2c3a-112">*ppbPropertyData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e2c3a-113">Pointeur vers un tableau d’entiers non signés 8 bits qui contient les données de propriété.</span><span class="sxs-lookup"><span data-stu-id="e2c3a-113">A pointer to an 8-bit unsigned integer array that contains the property data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e2c3a-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e2c3a-114">Return value</span></span>

<span data-ttu-id="e2c3a-115">Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.</span><span class="sxs-lookup"><span data-stu-id="e2c3a-115">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="e2c3a-116">Notes</span><span class="sxs-lookup"><span data-stu-id="e2c3a-116">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="e2c3a-117">Pour éviter une fuite de mémoire, utilisez [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) pour libérer la mémoire à partir de \* *ppbPropertyData* lorsque vous n’avez plus besoin des informations.</span><span class="sxs-lookup"><span data-stu-id="e2c3a-117">To avoid a memory leak, use [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) to release the memory from \**ppbPropertyData* when you no longer need the information.</span></span>

 

<span data-ttu-id="e2c3a-118">En plus de récupérer des données spécifiques à l’application qui ont été ajoutées avec [**IContextNode :: AddPropertyData**](icontextnode-addpropertydata.md), cette méthode est utilisée pour récupérer les propriétés communes qui sont décrites par les constantes des [Propriétés du nœud de contexte](context-node-properties.md) .</span><span class="sxs-lookup"><span data-stu-id="e2c3a-118">In addition to retrieving application-specific data that was added with [**IContextNode::AddPropertyData**](icontextnode-addpropertydata.md), this method is used to retrieve common properties that are described by the [Context Node Properties](context-node-properties.md) constants.</span></span>

<span data-ttu-id="e2c3a-119">Les propriétés de type chaîne sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="e2c3a-119">The string-type properties include:</span></span>

-   <span data-ttu-id="e2c3a-120">GUID \_ CNP \_ RECOGNIZEDSTRING</span><span class="sxs-lookup"><span data-stu-id="e2c3a-120">GUID\_CNP\_RECOGNIZEDSTRING</span></span>
-   <span data-ttu-id="e2c3a-121">GUID \_ CNP \_ SHAPENAME</span><span class="sxs-lookup"><span data-stu-id="e2c3a-121">GUID\_CNP\_SHAPENAME</span></span>
-   <span data-ttu-id="e2c3a-122">GUID \_ AHP \_ ANALYSISHINTNAME</span><span class="sxs-lookup"><span data-stu-id="e2c3a-122">GUID\_AHP\_ANALYSISHINTNAME</span></span>
-   <span data-ttu-id="e2c3a-123">GUID \_ AHP \_ PREFIXTEXT</span><span class="sxs-lookup"><span data-stu-id="e2c3a-123">GUID\_AHP\_PREFIXTEXT</span></span>
-   <span data-ttu-id="e2c3a-124">GUID \_ AHP \_ SUFFIXTEXT</span><span class="sxs-lookup"><span data-stu-id="e2c3a-124">GUID\_AHP\_SUFFIXTEXT</span></span>
-   <span data-ttu-id="e2c3a-125">GUID \_ AHP \_ FACTOID</span><span class="sxs-lookup"><span data-stu-id="e2c3a-125">GUID\_AHP\_FACTOID</span></span>

<span data-ttu-id="e2c3a-126">La valeur de retour est \*\* \* WCHAR\*_. Si vous effectuez un cast du \_ paramètre *ppbPropertyData* en \**\* WCHAR*_ , sa longueur retournée est `(length of the string + 1) _ sizeof(WCHAR)` .</span><span class="sxs-lookup"><span data-stu-id="e2c3a-126">The return value is \**WCHAR\**_. If you cast the \_*ppbPropertyData* parameter to \**WCHAR\**_ its returned length is `(length of the string + 1) _ sizeof(WCHAR)`.</span></span>

<span data-ttu-id="e2c3a-127">Les propriétés de type booléen sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="e2c3a-127">The Boolean-type properties include:</span></span>

-   <span data-ttu-id="e2c3a-128">GUID \_ AHP \_ OVERRIDELANGUAGEID</span><span class="sxs-lookup"><span data-stu-id="e2c3a-128">GUID\_AHP\_OVERRIDELANGUAGEID</span></span>
-   <span data-ttu-id="e2c3a-129">GUID \_ AHP \_ COERCETOFACTOID</span><span class="sxs-lookup"><span data-stu-id="e2c3a-129">GUID\_AHP\_COERCETOFACTOID</span></span>
-   <span data-ttu-id="e2c3a-130">GUID \_ AHP \_ WORDMODE</span><span class="sxs-lookup"><span data-stu-id="e2c3a-130">GUID\_AHP\_WORDMODE</span></span>

<span data-ttu-id="e2c3a-131">La valeur de retour est de **type Variant \_ booléen**.</span><span class="sxs-lookup"><span data-stu-id="e2c3a-131">The return value is **VARIANT\_BOOL**.</span></span> <span data-ttu-id="e2c3a-132">Si vous effectuez un cast du \* paramètre *ppbPropertyData* en \**Variant \_ \* bool* _, sa longueur retournée est `sizeof(VARIANT_BOOL)` .</span><span class="sxs-lookup"><span data-stu-id="e2c3a-132">If you cast the \**ppbPropertyData* parameter to \**VARIANT\_BOOL\** _ its returned length is `sizeof(VARIANT_BOOL)`.</span></span>

<span data-ttu-id="e2c3a-133">GUID \_ AHP \_ Guide est une propriété de type guide.</span><span class="sxs-lookup"><span data-stu-id="e2c3a-133">GUID\_AHP\_GUIDE is a guide-type property.</span></span> <span data-ttu-id="e2c3a-134">La valeur de retour _*est \* InkAnalysisRecognitionGuide*_.</span><span class="sxs-lookup"><span data-stu-id="e2c3a-134">The return value is _*InkAnalysisRecognitionGuide\**_.</span></span> <span data-ttu-id="e2c3a-135">Si vous effectuez un cast du \_ paramètre *ppbPropertyData* en \**\* InkAnalysisRecognitionGuide* _ sa longueur retournée est `sizeof(InkAnalysisRecognitionGuide)` .</span><span class="sxs-lookup"><span data-stu-id="e2c3a-135">If you cast the \_*ppbPropertyData* parameter to \**InkAnalysisRecognitionGuide\** _ its returned length is `sizeof(InkAnalysisRecognitionGuide)`.</span></span>

<span data-ttu-id="e2c3a-136">Les propriétés de type entier sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="e2c3a-136">Integer-type properties include:</span></span>

-   <span data-ttu-id="e2c3a-137">GUID \_ CNP \_ LINENUMBER</span><span class="sxs-lookup"><span data-stu-id="e2c3a-137">GUID\_CNP\_LINENUMBER</span></span>
-   <span data-ttu-id="e2c3a-138">GUID \_ CNP \_ POINTSPERINCH</span><span class="sxs-lookup"><span data-stu-id="e2c3a-138">GUID\_CNP\_POINTSPERINCH</span></span>
-   <span data-ttu-id="e2c3a-139">GUID \_ CNP \_ CONFIDENCELEVEL</span><span class="sxs-lookup"><span data-stu-id="e2c3a-139">GUID\_CNP\_CONFIDENCELEVEL</span></span>
-   <span data-ttu-id="e2c3a-140">\_confirmation CNP \_ GUID</span><span class="sxs-lookup"><span data-stu-id="e2c3a-140">GUID\_CNP\_CONFIRMATION</span></span>
-   <span data-ttu-id="e2c3a-141">GUID \_ CNP \_ MAXIMUMSTROKECOUNT</span><span class="sxs-lookup"><span data-stu-id="e2c3a-141">GUID\_CNP\_MAXIMUMSTROKECOUNT</span></span>
-   <span data-ttu-id="e2c3a-142">\_ \_ segmentation GUID CNP</span><span class="sxs-lookup"><span data-stu-id="e2c3a-142">GUID\_CNP\_SEGMENTATION</span></span>
-   <span data-ttu-id="e2c3a-143">GUID \_ CNP \_ ALIGNMENTLEVEL</span><span class="sxs-lookup"><span data-stu-id="e2c3a-143">GUID\_CNP\_ALIGNMENTLEVEL</span></span>

<span data-ttu-id="e2c3a-144">La valeur de retour _*est \* longue*_.</span><span class="sxs-lookup"><span data-stu-id="e2c3a-144">The return value is _*LONG\**_.</span></span> <span data-ttu-id="e2c3a-145">Si vous effectuez un cast du \_ paramètre *ppbPropertyData* en \**\* long* _, sa longueur retournée est `sizeof(LONG)` .</span><span class="sxs-lookup"><span data-stu-id="e2c3a-145">If you cast the \_*ppbPropertyData* parameter to \**LONG\** _ its returned length is `sizeof(LONG)`.</span></span>

<span data-ttu-id="e2c3a-146">Métriques de ligne : les propriétés de type sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="e2c3a-146">Line metrics-type properties include:</span></span>

-   <span data-ttu-id="e2c3a-147">GUID \_ CNP \_ ascendants</span><span class="sxs-lookup"><span data-stu-id="e2c3a-147">GUID\_CNP\_ASCENDERS</span></span>
-   <span data-ttu-id="e2c3a-148">GUID \_ CNP les \_ descendants</span><span class="sxs-lookup"><span data-stu-id="e2c3a-148">GUID\_CNP\_DESCENDERS</span></span>
-   <span data-ttu-id="e2c3a-149">\_ligne de \_ base GUID CNP</span><span class="sxs-lookup"><span data-stu-id="e2c3a-149">GUID\_CNP\_BASELINE</span></span>
-   <span data-ttu-id="e2c3a-150">GUID \_ CNP- \_ média</span><span class="sxs-lookup"><span data-stu-id="e2c3a-150">GUID\_CNP\_MIDLINE</span></span>

<span data-ttu-id="e2c3a-151">La valeur de retour _*est \* longue*_.</span><span class="sxs-lookup"><span data-stu-id="e2c3a-151">The return value is _*LONG\**_.</span></span> <span data-ttu-id="e2c3a-152">Si vous effectuez un cast du \_ paramètre *ppbPropertyData* en \**\* long* _ sa longueur retournée est `sizeof(LONG)_4` , ce qui signifie que les valeurs (x, y) des points de départ sont suivies des valeurs (x, y) des points de fin.</span><span class="sxs-lookup"><span data-stu-id="e2c3a-152">If you cast the \_*ppbPropertyData* parameter to \**LONG\** _ its returned length is `sizeof(LONG)_4`, signifying the (x, y) values for the starting points followed by the (x, y) values for the ending points.</span></span>

<span data-ttu-id="e2c3a-153">GUID \_ CNP \_ TEXTRECOGNIZERID est une propriété **GUID** .</span><span class="sxs-lookup"><span data-stu-id="e2c3a-153">GUID\_CNP\_TEXTRECOGNIZERID is a **GUID** property.</span></span> <span data-ttu-id="e2c3a-154">La valeur de retour est \*\* \* GUID\*_. Si vous effectuez un cast du \_ paramètre *ppbPropertyData* en \**\* GUID*_ , sa longueur retournée est `sizeof(GUID)` .</span><span class="sxs-lookup"><span data-stu-id="e2c3a-154">The return value is \**GUID\**_. If you cast the \_*ppbPropertyData* parameter to \**GUID\**_ its returned length is `sizeof(GUID)`.</span></span>

<span data-ttu-id="e2c3a-155">GUID \_ CNP \_ ROTATEDBOUNDINGBOX est une propriété de cadre englobant pivotée.</span><span class="sxs-lookup"><span data-stu-id="e2c3a-155">GUID\_CNP\_ROTATEDBOUNDINGBOX is a rotated bounding box property.</span></span> <span data-ttu-id="e2c3a-156">La valeur de retour _*est \* longue*_.</span><span class="sxs-lookup"><span data-stu-id="e2c3a-156">The return value is _*LONG\**_.</span></span> <span data-ttu-id="e2c3a-157">Si vous effectuez un cast du \_ paramètre *ppbPropertyData* en \**\* long* _ sa longueur retournée est `sizeof(LONG)_8` , ce qui signifie les valeurs (x, y) des quatre coins de la zone.</span><span class="sxs-lookup"><span data-stu-id="e2c3a-157">If you cast the \_*ppbPropertyData* parameter to \**LONG\** _ its returned length is `sizeof(LONG)_8`, signifying the (x, y) values for the four corners of the box.</span></span>

<span data-ttu-id="e2c3a-158">GUID \_ CNP \_ HOTPOINT est une propriété de point réactif.</span><span class="sxs-lookup"><span data-stu-id="e2c3a-158">GUID\_CNP\_HOTPOINT is a hot point property.</span></span> <span data-ttu-id="e2c3a-159">La valeur de retour est \*\* \* long\*_. Si vous effectuez un cast du \_ paramètre *ppbPropertyData* en \**long \**_ sa longueur retournée est `sizeof(LONG)_2` , ce qui signifie les valeurs (x, y) pour le point.</span><span class="sxs-lookup"><span data-stu-id="e2c3a-159">The return value is \**LONG\**_. If you cast the \_*ppbPropertyData* parameter to \**LONG\**_ its returned length is `sizeof(LONG)_2`, signifying the (x, y) values for the point.</span></span>

<span data-ttu-id="e2c3a-160">GUID \_ AHP \_ liste de mots est une propriété de liste de mots.</span><span class="sxs-lookup"><span data-stu-id="e2c3a-160">GUID\_AHP\_WORDLIST is a word list property.</span></span> <span data-ttu-id="e2c3a-161">La valeur de retour est \*\* \* WCHAR\*_. Si vous effectuez un cast du \_ paramètre *ppbPropertyData* en \**WCHAR \**_ , sa longueur retournée est `n _ sizeof(WCHAR)` , où `n` est la somme des longueurs de chaîne du nombre de chaînes de la liste plus 1 pour chaque caractère de fin **null** pour chaque chaîne.</span><span class="sxs-lookup"><span data-stu-id="e2c3a-161">The return value is \**WCHAR\**_. If you cast the \_*ppbPropertyData* parameter to \**WCHAR\**_ its returned length is `n _ sizeof(WCHAR)`, where `n` is the sum of the string lengths of the number of strings in the list plus 1 for each **NULL** termination character for each string.</span></span>

## <a name="examples"></a><span data-ttu-id="e2c3a-162">Exemples</span><span class="sxs-lookup"><span data-stu-id="e2c3a-162">Examples</span></span>

<span data-ttu-id="e2c3a-163">Cet exemple montre une méthode qui accède à la propriété de nœud de contexte AlignmentLevel d’un type de nœud de contexte de paragraphe.</span><span class="sxs-lookup"><span data-stu-id="e2c3a-163">This example shows a method that accesses the AlignmentLevel context node property of a Paragraph context node type.</span></span>


```C++
// Checks a paragraph context node's alignment level property.
// Only paragraph type context nodes contain the alignment level property.
HRESULT CMyClass::ExploreParagraphNode(
    IContextNode *pParagraphNode)
{
    // Get the AlignmentLevel property data for the paragraph.
    LONG * alignmentLevel = NULL;
    ULONG ulDataLen = 0;

    HRESULT hr = pParagraphNode->GetPropertyData(
        (const GUID*)&GUID_CNP_ALIGNMENTLEVEL,
        &ulDataLen,
        (BYTE**)&alignmentLevel);

    if( FAILED(hr) ||
        ulDataLen != sizeof(LONG) ||
        alignmentLevel == NULL )
    {
        // Insert code that handles an error here.
    }
    else
    {
        // Insert code that uses the alignment level here.
    }

    // Free the memory allocated for the property data.
    ::CoTaskMemFree(alignmentLevel);

    return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="e2c3a-164">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e2c3a-164">Requirements</span></span>



| <span data-ttu-id="e2c3a-165">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e2c3a-165">Requirement</span></span> | <span data-ttu-id="e2c3a-166">Valeur</span><span class="sxs-lookup"><span data-stu-id="e2c3a-166">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e2c3a-167">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e2c3a-167">Minimum supported client</span></span><br/> | <span data-ttu-id="e2c3a-168">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e2c3a-168">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="e2c3a-169">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e2c3a-169">Minimum supported server</span></span><br/> | <span data-ttu-id="e2c3a-170">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="e2c3a-170">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="e2c3a-171">En-tête</span><span class="sxs-lookup"><span data-stu-id="e2c3a-171">Header</span></span><br/>                   | <dl> <span data-ttu-id="e2c3a-172"><dt>IACom. h (nécessite également IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="e2c3a-172"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="e2c3a-173">DLL</span><span class="sxs-lookup"><span data-stu-id="e2c3a-173">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e2c3a-174"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e2c3a-174"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="e2c3a-175">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e2c3a-175">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2c3a-176">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="e2c3a-176">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="e2c3a-177">**IContextNode::AddPropertyData**</span><span class="sxs-lookup"><span data-stu-id="e2c3a-177">**IContextNode::AddPropertyData**</span></span>](icontextnode-addpropertydata.md)
</dt> <dt>

[<span data-ttu-id="e2c3a-178">**IContextNode::RemovePropertyData**</span><span class="sxs-lookup"><span data-stu-id="e2c3a-178">**IContextNode::RemovePropertyData**</span></span>](icontextnode-removepropertydata.md)
</dt> <dt>

[<span data-ttu-id="e2c3a-179">**IContextNode::GetPropertyDataIds**</span><span class="sxs-lookup"><span data-stu-id="e2c3a-179">**IContextNode::GetPropertyDataIds**</span></span>](icontextnode-getpropertydataids.md)
</dt> <dt>

[<span data-ttu-id="e2c3a-180">**IContextNode::ContainsPropertyData**</span><span class="sxs-lookup"><span data-stu-id="e2c3a-180">**IContextNode::ContainsPropertyData**</span></span>](icontextnode-containspropertydata.md)
</dt> <dt>

[<span data-ttu-id="e2c3a-181">**IContextNode::LoadPropertiesData**</span><span class="sxs-lookup"><span data-stu-id="e2c3a-181">**IContextNode::LoadPropertiesData**</span></span>](icontextnode-loadpropertiesdata.md)
</dt> <dt>

[<span data-ttu-id="e2c3a-182">**IContextNode::SavePropertiesData**</span><span class="sxs-lookup"><span data-stu-id="e2c3a-182">**IContextNode::SavePropertiesData**</span></span>](icontextnode-savepropertiesdata.md)
</dt> <dt>

[<span data-ttu-id="e2c3a-183">Référence de l’analyse de l’encre</span><span class="sxs-lookup"><span data-stu-id="e2c3a-183">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

