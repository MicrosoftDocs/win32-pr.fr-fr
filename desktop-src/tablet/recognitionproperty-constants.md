---
description: Définit des valeurs qui spécifient les propriétés d’un substitut de reconnaissance. L’interface de programmation d’applications (API) Tablet PC utilise des identificateurs globaux uniques (GUID) pour identifier les propriétés des paquets, qui sont des chaînes constantes dans Automation.
ms.assetid: 2bfb0cbf-73a3-4e83-a4e9-f0803bd3dee8
title: Constantes RecognitionProperty (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62971276b6348af3d8ac971851d70b03f7b003c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320430"
---
# <a name="recognitionproperty-constants"></a><span data-ttu-id="eef27-104">Constantes RecognitionProperty</span><span class="sxs-lookup"><span data-stu-id="eef27-104">RecognitionProperty Constants</span></span>

<span data-ttu-id="eef27-105">Définit des valeurs qui spécifient les propriétés d’un substitut de reconnaissance.</span><span class="sxs-lookup"><span data-stu-id="eef27-105">Defines values that specify the properties of a recognition alternate.</span></span> <span data-ttu-id="eef27-106">L’interface de programmation d’applications (API) Tablet PC utilise des identificateurs globaux uniques (GUID) pour identifier les propriétés des paquets, qui sont des chaînes constantes dans Automation.</span><span class="sxs-lookup"><span data-stu-id="eef27-106">The Tablet PC application programming interface (API) uses globally unique identifiers (GUIDs) to identify packet properties, which in Automation are constant strings.</span></span>

<span data-ttu-id="eef27-107">Le tableau suivant répertorie les champs de l’identificateur global unique (GUID) de la propriété de remplacement disponibles.</span><span class="sxs-lookup"><span data-stu-id="eef27-107">The following table lists the available recognition alternate property globally unique identifier (GUID) fields.</span></span> <span data-ttu-id="eef27-108">Utilisez ces GUID pour accéder aux propriétés d’un objet [**IInkRecognitionAlternate**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate) en appelant la méthode [**GetPropertyValue**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionalternate-getpropertyvalue) .</span><span class="sxs-lookup"><span data-stu-id="eef27-108">Use these GUIDs to access properties of an [**IInkRecognitionAlternate**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate) object by calling the [**GetPropertyValue**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionalternate-getpropertyvalue) method.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="eef27-109">Nom de la constante</span><span class="sxs-lookup"><span data-stu-id="eef27-109">Constant Name</span></span></th>
<th style="text-align: left;"><span data-ttu-id="eef27-110">Description</span><span class="sxs-lookup"><span data-stu-id="eef27-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="___________INKRECOGNITIONPROPERTY_LINENUMBER_________"></span><span id="___________inkrecognitionproperty_linenumber_________"></span><dl> <span data-ttu-id="eef27-111"><dt><strong>INKRECOGNITIONPROPERTY_LINENUMBER</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="eef27-111"><dt> <strong>INKRECOGNITIONPROPERTY_LINENUMBER</strong> </dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="eef27-112">GUID qui identifie la propriété pour le numéro de ligne de l’objet <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate"><strong>IInkRecognitionAlternate</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="eef27-112">The GUID that identifies the property for the line number of the <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate"><strong>IInkRecognitionAlternate</strong></a> object.</span></span> <br/> <span data-ttu-id="eef27-113">LineNumber spécifie les alternatives avec un numéro de ligne particulier.</span><span class="sxs-lookup"><span data-stu-id="eef27-113">LineNumber specifies the alternates with a particular line number.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="eef27-114">Ce champ n’est pas pris en charge pour les identificateurs de caractères d’Extrême-Orient.</span><span class="sxs-lookup"><span data-stu-id="eef27-114">This field is not supported for recognizers of East Asian characters.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="___________INKRECOGNITIONPROPERTY_SEGMENTATION_________"></span><span id="___________inkrecognitionproperty_segmentation_________"></span><dl> <span data-ttu-id="eef27-115"><dt><strong>INKRECOGNITIONPROPERTY_SEGMENTATION</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="eef27-115"><dt> <strong>INKRECOGNITIONPROPERTY_SEGMENTATION</strong> </dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="eef27-116">GUID qui identifie la propriété pour la segmentation de l’objet <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate"><strong>IInkRecognitionAlternate</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="eef27-116">The GUID that identifies the property for the segmentation of the <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate"><strong>IInkRecognitionAlternate</strong></a> object.</span></span> <br/> <span data-ttu-id="eef27-117">La segmentation spécifie le fragment ou l’unité d’encre de base que le module de reconnaissance utilise pour produire un résultat de reconnaissance.</span><span class="sxs-lookup"><span data-stu-id="eef27-117">Segmentation specifies the basic ink fragment or unit that the recognizer uses to produce a recognition result.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="eef27-118">Non implémenté.</span><span class="sxs-lookup"><span data-stu-id="eef27-118">Not implemented.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="___________INKRECOGNITIONPROPERTY_HOTPOINT_________"></span><span id="___________inkrecognitionproperty_hotpoint_________"></span><dl> <span data-ttu-id="eef27-119"><dt><strong>INKRECOGNITIONPROPERTY_HOTPOINT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="eef27-119"><dt> <strong>INKRECOGNITIONPROPERTY_HOTPOINT</strong> </dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="eef27-120">GUID qui identifie la propriété pour le point réactif de reconnaissance de l’objet <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate"><strong>IInkRecognitionAlternate</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="eef27-120">The GUID that identifies the property for the recognition hot point of the <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate"><strong>IInkRecognitionAlternate</strong></a> object.</span></span> <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="___________INKRECOGNITIONPROPERTY_MAXIMUMSTROKECOUNT_________"></span><span id="___________inkrecognitionproperty_maximumstrokecount_________"></span><dl> <span data-ttu-id="eef27-121"><dt><strong>INKRECOGNITIONPROPERTY_MAXIMUMSTROKECOUNT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="eef27-121"><dt> <strong>INKRECOGNITIONPROPERTY_MAXIMUMSTROKECOUNT</strong> </dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="eef27-122">GUID qui identifie la propriété pour le nombre de traits maximal du résultat de la reconnaissance pour l’objet <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate"><strong>IInkRecognitionAlternate</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="eef27-122">The GUID that identifies the property for the maximum stroke count of the recognition result for the <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate"><strong>IInkRecognitionAlternate</strong></a> object.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="eef27-123">Non implémenté.</span><span class="sxs-lookup"><span data-stu-id="eef27-123">Not implemented.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="___________INKRECOGNITIONPROPERTY_POINTSPERINCH_________"></span><span id="___________inkrecognitionproperty_pointsperinch_________"></span><dl> <span data-ttu-id="eef27-124"><dt><strong>INKRECOGNITIONPROPERTY_POINTSPERINCH</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="eef27-124"><dt> <strong>INKRECOGNITIONPROPERTY_POINTSPERINCH</strong> </dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="eef27-125">GUID qui identifie la propriété de la métrique point par pouce de l’objet <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate"><strong>IInkRecognitionAlternate</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="eef27-125">The GUID that identifies the property for the points-per-inch metric of the <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate"><strong>IInkRecognitionAlternate</strong></a> object.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="eef27-126">Non implémenté.</span><span class="sxs-lookup"><span data-stu-id="eef27-126">Not implemented.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="___________INKRECOGNITIONPROPERTY_CONFIDENCELEVEL_________"></span><span id="___________inkrecognitionproperty_confidencelevel_________"></span><dl> <span data-ttu-id="eef27-127"><dt><strong>INKRECOGNITIONPROPERTY_CONFIDENCELEVEL</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="eef27-127"><dt> <strong>INKRECOGNITIONPROPERTY_CONFIDENCELEVEL</strong> </dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="eef27-128">GUID qui identifie la propriété pour le niveau de confiance que le module de reconnaissance a dans le résultat de la reconnaissance.</span><span class="sxs-lookup"><span data-stu-id="eef27-128">The GUID that identifies the property for the level of confidence that the recognizer has in the recognition result.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="eef27-129">L’évaluation de la confiance est disponible uniquement pour États-Unis anglais et tous les module de reconnaissance de mouvement dans Microsoft Windows XP Édition Tablet PC et Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="eef27-129">Confidence evaluation is available only for United States English and all gesture recognizers in Microsoft Windows XP Tablet PC Edition and Windows Vista.</span></span> <span data-ttu-id="eef27-130">Les méthodes qui fournissent la propriété confidence pour tout autre module de reconnaissance retournent E_NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="eef27-130">Methods that provide the confidence property for any other recognizer return E_NOTIMPL.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="___________INKRECOGNITIONPROPERTY_LINEMETRICS_________"></span><span id="___________inkrecognitionproperty_linemetrics_________"></span><dl> <span data-ttu-id="eef27-131"><dt><strong>INKRECOGNITIONPROPERTY_LINEMETRICS</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="eef27-131"><dt> <strong>INKRECOGNITIONPROPERTY_LINEMETRICS</strong> </dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="eef27-132">GUID qui identifie la propriété pour les métriques de ligne de l’objet <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate"><strong>IInkRecognitionAlternate</strong></a> , qui est la ligne pour laquelle les métriques doivent être récupérées.</span><span class="sxs-lookup"><span data-stu-id="eef27-132">The GUID that identifies the property for the line metrics of the <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate"><strong>IInkRecognitionAlternate</strong></a> object, which is the line for which to retrieve metrics.</span></span> <br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a><span data-ttu-id="eef27-133">Notes</span><span class="sxs-lookup"><span data-stu-id="eef27-133">Remarks</span></span>

<span data-ttu-id="eef27-134">En C++, vous pouvez accéder à ces constantes dans le fichier d’en-tête Msinkaut. h, qui se trouve dans le dossier <systemdrive> : \\ Program Files \\ Microsoft SDK \\ Windows \\ v 6.0 \\ include si vous avez installé le kit de développement logiciel (SDK) à l’emplacement par défaut.</span><span class="sxs-lookup"><span data-stu-id="eef27-134">In C++, you can access these constants in the Msinkaut.h header file, which is located in the <systemdrive>:\\Program Files\\Microsoft SDKs\\Windows\\v6.0\\Include directory if you installed the SDK in the default location.</span></span>

> [!Note]  
> <span data-ttu-id="eef27-135">En C++, ces constantes sont WCHARs, et non BSTR.</span><span class="sxs-lookup"><span data-stu-id="eef27-135">In C++, these constants are WCHARs, not BSTRs.</span></span> <span data-ttu-id="eef27-136">Convertissez-les en BSTR avant d’utiliser.</span><span class="sxs-lookup"><span data-stu-id="eef27-136">Convert them into BSTRs before use.</span></span> <span data-ttu-id="eef27-137">Pour plus d’informations sur le type de données BSTR, consultez [utilisation de la bibliothèque com](using-the-com-library.md).</span><span class="sxs-lookup"><span data-stu-id="eef27-137">For more information about the BSTR data type, see [Using the COM Library](using-the-com-library.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="eef27-138">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="eef27-138">Requirements</span></span>



| <span data-ttu-id="eef27-139">Condition requise</span><span class="sxs-lookup"><span data-stu-id="eef27-139">Requirement</span></span> | <span data-ttu-id="eef27-140">Valeur</span><span class="sxs-lookup"><span data-stu-id="eef27-140">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eef27-141">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="eef27-141">Minimum supported client</span></span><br/> | <span data-ttu-id="eef27-142">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="eef27-142">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="eef27-143">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="eef27-143">Minimum supported server</span></span><br/> | <span data-ttu-id="eef27-144">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="eef27-144">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="eef27-145">En-tête</span><span class="sxs-lookup"><span data-stu-id="eef27-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="eef27-146"><dt>Msinkaut. h (nécessite également Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="eef27-146"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eef27-147">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="eef27-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eef27-148">**Méthode AlternatesWithConstantPropertyValues**</span><span class="sxs-lookup"><span data-stu-id="eef27-148">**AlternatesWithConstantPropertyValues Method**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionalternate-alternateswithconstantpropertyvalues)
</dt> <dt>

[<span data-ttu-id="eef27-149">**Propriété ConfidenceAlternates**</span><span class="sxs-lookup"><span data-stu-id="eef27-149">**ConfidenceAlternates Property**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionalternate-get_confidencealternates)
</dt> <dt>

[<span data-ttu-id="eef27-150">**Propriété LineAlternates**</span><span class="sxs-lookup"><span data-stu-id="eef27-150">**LineAlternates Property**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionalternate-get_linealternates)
</dt> <dt>

[<span data-ttu-id="eef27-151">**Interface IInkRecognitionAlternates**</span><span class="sxs-lookup"><span data-stu-id="eef27-151">**IInkRecognitionAlternates Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternates)
</dt> </dl>

 

 




