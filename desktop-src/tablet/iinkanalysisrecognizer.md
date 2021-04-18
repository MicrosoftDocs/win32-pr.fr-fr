---
description: Donne accès aux reconnaissance de l’écriture manuscrite pour une utilisation avec l’analyse de l’encre.
ms.assetid: de536cca-889e-413e-a6f7-c2229a77c801
title: Interface IInkAnalysisRecognizer (IACom. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalysisRecognizer
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: b091b47d14929e155548dc057ef0fdb1731133a2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516018"
---
# <a name="iinkanalysisrecognizer-interface"></a><span data-ttu-id="ec98f-103">Interface IInkAnalysisRecognizer</span><span class="sxs-lookup"><span data-stu-id="ec98f-103">IInkAnalysisRecognizer interface</span></span>

<span data-ttu-id="ec98f-104">Donne accès aux reconnaissance de l’écriture manuscrite pour une utilisation avec l’analyse de l’encre.</span><span class="sxs-lookup"><span data-stu-id="ec98f-104">Provides access to handwriting recognizers for use with ink analysis.</span></span>

## <a name="members"></a><span data-ttu-id="ec98f-105">Membres</span><span class="sxs-lookup"><span data-stu-id="ec98f-105">Members</span></span>

<span data-ttu-id="ec98f-106">L’interface **IInkAnalysisRecognizer** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="ec98f-106">The **IInkAnalysisRecognizer** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="ec98f-107">**IInkAnalysisRecognizer** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="ec98f-107">**IInkAnalysisRecognizer** also has these types of members:</span></span>

-   [<span data-ttu-id="ec98f-108">Méthodes</span><span class="sxs-lookup"><span data-stu-id="ec98f-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="ec98f-109">Méthodes</span><span class="sxs-lookup"><span data-stu-id="ec98f-109">Methods</span></span>

<span data-ttu-id="ec98f-110">L’interface **IInkAnalysisRecognizer** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="ec98f-110">The **IInkAnalysisRecognizer** interface has these methods.</span></span>



| <span data-ttu-id="ec98f-111">Méthode</span><span class="sxs-lookup"><span data-stu-id="ec98f-111">Method</span></span>                                                                          | <span data-ttu-id="ec98f-112">Description</span><span class="sxs-lookup"><span data-stu-id="ec98f-112">Description</span></span>                                                                                                                    |
|:--------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ec98f-113">**GetCapabilities**</span><span class="sxs-lookup"><span data-stu-id="ec98f-113">**GetCapabilities**</span></span>](iinkanalysisrecognizer-getcapabilities.md)               | <span data-ttu-id="ec98f-114">Récupère les fonctionnalités du module de reconnaissance.</span><span class="sxs-lookup"><span data-stu-id="ec98f-114">Retrieves the capabilities of the recognizer.</span></span><br/>                                                                       |
| [<span data-ttu-id="ec98f-115">**GetGuid**</span><span class="sxs-lookup"><span data-stu-id="ec98f-115">**GetGuid**</span></span>](iinkanalysisrecognizer-getguid.md)                               | <span data-ttu-id="ec98f-116">Récupère l’identificateur global unique (GUID) du module de reconnaissance.</span><span class="sxs-lookup"><span data-stu-id="ec98f-116">Retrieves the globally unique identifier (GUID) of the recognizer.</span></span><br/>                                                  |
| [<span data-ttu-id="ec98f-117">**GetLanguages**</span><span class="sxs-lookup"><span data-stu-id="ec98f-117">**GetLanguages**</span></span>](iinkanalysisrecognizer-getlanguages.md)                     | <span data-ttu-id="ec98f-118">Récupère les identificateurs pour les paramètres régionaux pris en charge par ce **IInkAnalysisRecognizer** .</span><span class="sxs-lookup"><span data-stu-id="ec98f-118">Retrieves the identifiers for the locales that this **IInkAnalysisRecognizer** supports.</span></span><br/>                            |
| [<span data-ttu-id="ec98f-119">**GetName**</span><span class="sxs-lookup"><span data-stu-id="ec98f-119">**GetName**</span></span>](iinkanalysisrecognizer-getname.md)                               | <span data-ttu-id="ec98f-120">Récupère le nom du module de reconnaissance.</span><span class="sxs-lookup"><span data-stu-id="ec98f-120">Retrieves the name of the recognizer.</span></span><br/>                                                                               |
| [<span data-ttu-id="ec98f-121">**GetSupportedProperties**</span><span class="sxs-lookup"><span data-stu-id="ec98f-121">**GetSupportedProperties**</span></span>](iinkanalysisrecognizer-getsupportedproperties.md) | <span data-ttu-id="ec98f-122">Récupère les identificateurs globaux uniques (GUID) pour les propriétés prises en charge par ce **IInkAnalysisRecognizer** .</span><span class="sxs-lookup"><span data-stu-id="ec98f-122">Retrieves the globally unique identifiers (GUIDs) for the properties that this **IInkAnalysisRecognizer** supports.</span></span><br/> |
| [<span data-ttu-id="ec98f-123">**GetVendor**</span><span class="sxs-lookup"><span data-stu-id="ec98f-123">**GetVendor**</span></span>](iinkanalysisrecognizer-getvendor.md)                           | <span data-ttu-id="ec98f-124">Récupère le nom du fournisseur du **IInkAnalysisRecognizer**.</span><span class="sxs-lookup"><span data-stu-id="ec98f-124">Retrieves the vendor name of the **IInkAnalysisRecognizer**.</span></span><br/>                                                        |



 

## <a name="remarks"></a><span data-ttu-id="ec98f-125">Notes</span><span class="sxs-lookup"><span data-stu-id="ec98f-125">Remarks</span></span>

<span data-ttu-id="ec98f-126">Un module de reconnaissance possède des attributs et des propriétés spécifiques qui lui permettent d’effectuer la reconnaissance.</span><span class="sxs-lookup"><span data-stu-id="ec98f-126">A recognizer has specific attributes and properties that allow it to perform recognition.</span></span> <span data-ttu-id="ec98f-127">Les propriétés d’un module de reconnaissance doivent être déterminées avant que la reconnaissance ne se produise.</span><span class="sxs-lookup"><span data-stu-id="ec98f-127">The properties of a recognizer must be determined before recognition can occur.</span></span> <span data-ttu-id="ec98f-128">Les types de propriétés qu’un module de reconnaissance prend en charge déterminent les types de reconnaissance qu’il peut effectuer.</span><span class="sxs-lookup"><span data-stu-id="ec98f-128">The types of properties that a recognizer supports determine the types of recognition that it can perform.</span></span> <span data-ttu-id="ec98f-129">Par exemple, si un module de reconnaissance ne prend pas en charge l’écriture cursive, il renvoie des résultats inexacts lorsqu’un utilisateur écrit en cursive.</span><span class="sxs-lookup"><span data-stu-id="ec98f-129">For instance, if a recognizer does not support cursive handwriting, it returns inaccurate results when a user writes in cursive.</span></span>

<span data-ttu-id="ec98f-130">Un module de reconnaissance possède également une fonctionnalité intégrée qui gère automatiquement de nombreux aspects de l’écriture manuscrite.</span><span class="sxs-lookup"><span data-stu-id="ec98f-130">A recognizer also has built-in functionality that automatically manages many aspects of handwriting.</span></span> <span data-ttu-id="ec98f-131">Par exemple, il détermine les métriques pour les lignes sur lesquelles les traits sont dessinés.</span><span class="sxs-lookup"><span data-stu-id="ec98f-131">For instance, it determines the metrics for the lines on which strokes are drawn.</span></span> <span data-ttu-id="ec98f-132">Vous pouvez retourner le numéro de ligne d’un trait, mais vous n’avez jamais besoin de spécifier la façon dont ces métriques de ligne sont déterminées en raison de la fonctionnalité intégrée du module de reconnaissance.</span><span class="sxs-lookup"><span data-stu-id="ec98f-132">You can return the line number of a stroke, but you never need to specify how those line metrics are determined because of the built-in functionality of the recognizer.</span></span>

<span data-ttu-id="ec98f-133">Le [**IInkAnalyzer**](iinkanalyzer.md) gère une liste des module de reconnaissance disponibles.</span><span class="sxs-lookup"><span data-stu-id="ec98f-133">The [**IInkAnalyzer**](iinkanalyzer.md) maintains a list of available recognizers.</span></span> <span data-ttu-id="ec98f-134">Pour accéder à cette liste, utilisez la méthode de [**méthode IInkAnalyzer :: GetInkAnalysisRecognizersByPriority**](iinkanalyzer-getinkanalysisrecognizersbypriority.md) .</span><span class="sxs-lookup"><span data-stu-id="ec98f-134">To access this list, use the [**IInkAnalyzer::GetInkAnalysisRecognizersByPriority Method**](iinkanalyzer-getinkanalysisrecognizersbypriority.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="ec98f-135">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ec98f-135">Requirements</span></span>



| <span data-ttu-id="ec98f-136">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ec98f-136">Requirement</span></span> | <span data-ttu-id="ec98f-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="ec98f-137">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ec98f-138">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ec98f-138">Minimum supported client</span></span><br/> | <span data-ttu-id="ec98f-139">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ec98f-139">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="ec98f-140">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ec98f-140">Minimum supported server</span></span><br/> | <span data-ttu-id="ec98f-141">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="ec98f-141">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="ec98f-142">En-tête</span><span class="sxs-lookup"><span data-stu-id="ec98f-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="ec98f-143"><dt>IACom. h (nécessite également IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="ec98f-143"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="ec98f-144">DLL</span><span class="sxs-lookup"><span data-stu-id="ec98f-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ec98f-145"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ec98f-145"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="ec98f-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ec98f-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec98f-147">**IInkAnalysisRecognizers**</span><span class="sxs-lookup"><span data-stu-id="ec98f-147">**IInkAnalysisRecognizers**</span></span>](iinkanalysisrecognizers.md)
</dt> <dt>

[<span data-ttu-id="ec98f-148">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="ec98f-148">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="ec98f-149">**IInkAnalyzer :: CreateCustomRecognizer, méthode**</span><span class="sxs-lookup"><span data-stu-id="ec98f-149">**IInkAnalyzer::CreateCustomRecognizer Method**</span></span>](iinkanalyzer-createcustomrecognizer.md)
</dt> <dt>

[<span data-ttu-id="ec98f-150">Types de nœuds de contexte</span><span class="sxs-lookup"><span data-stu-id="ec98f-150">Context Node Types</span></span>](context-node-types.md)
</dt> <dt>

[<span data-ttu-id="ec98f-151">Référence de l’analyse de l’encre</span><span class="sxs-lookup"><span data-stu-id="ec98f-151">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

