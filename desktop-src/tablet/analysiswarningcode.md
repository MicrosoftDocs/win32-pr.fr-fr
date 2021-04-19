---
description: Spécifie l’ensemble des avertissements disponibles qui peuvent se produire lors de l’analyse de l’encre.
ms.assetid: 52676f1d-8d67-4bdb-9d4f-3e409ffa8332
title: Énumération AnalysisWarningCode (IACom. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AnalysisWarningCode
api_type:
- HeaderDef
api_location:
- IACom.h
ms.openlocfilehash: 651408678daa64788952b2706980968ca315abf6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106518736"
---
# <a name="analysiswarningcode-enumeration"></a><span data-ttu-id="880b1-103">Énumération AnalysisWarningCode</span><span class="sxs-lookup"><span data-stu-id="880b1-103">AnalysisWarningCode enumeration</span></span>

<span data-ttu-id="880b1-104">Spécifie l’ensemble des avertissements disponibles qui peuvent se produire lors de l’analyse de l’encre.</span><span class="sxs-lookup"><span data-stu-id="880b1-104">Specifies the set of available warnings that can occur during ink analysis.</span></span>

## <a name="syntax"></a><span data-ttu-id="880b1-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="880b1-105">Syntax</span></span>


```C++
typedef enum AnalysisWarningCode { 
  AnalysisWarningCode_Aborted                                    = 0,
  AnalysisWarningCode_NoMatchingInkAnalysisRecognizerFound       = 1,
  AnalysisWarningCode_FactoidNotSupported                        = 2,
  AnalysisWarningCode_FactoidCoercionNotSupported                = 3,
  AnalysisWarningCode_GuideNotSupported                          = 4,
  AnalysisWarningCode_WordlistNotSupported                       = 5,
  AnalysisWarningCode_WordModeNotSupported                       = 6,
  AnalysisWarningCode_PartialDictionaryTermsNotSupported         = 7,
  AnalysisWarningCode_TextRecognitionProcessFailed               = 8,
  AnalysisWarningCode_AddInkToRecognizerFailed                   = 9,
  AnalysisWarningCode_SetPrefixSuffixFailed                      = 10,
  AnalysisWarningCode_InkAnalysisRecognizerInitializationFailed  = 11,
  AnalysisWarningCode_ConfirmedWithoutInkRecognition             = 12,
  AnalysisWarningCode_BackgroundException                        = 13,
  AnalysisWarningCode_ContextNodeLocationNotSet                  = 14,
  AnalysisWarningCode_LanguageIdNotRespected                     = 15,
  AnalysisWarningCode_EnableUnicodeCharacterRangesNotSupported   = 16,
  AnalysisWarningCode_TopInkBreaksOnlyNotSupported               = 17,
  AnalysisWarningCode_AnalysisAlreadyRunning                     = 18
} AnalysisWarningCode;
```



## <a name="constants"></a><span data-ttu-id="880b1-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="880b1-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="880b1-107"><span id="AnalysisWarningCode_Aborted"></span><span id="analysiswarningcode_aborted"></span><span id="ANALYSISWARNINGCODE_ABORTED"></span>**AnalysisWarningCode \_ abandonné**</span><span class="sxs-lookup"><span data-stu-id="880b1-107"><span id="AnalysisWarningCode_Aborted"></span><span id="analysiswarningcode_aborted"></span><span id="ANALYSISWARNINGCODE_ABORTED"></span>**AnalysisWarningCode\_Aborted**</span></span>
</dt> <dd>

<span data-ttu-id="880b1-108">L’opération d’analyse a été abandonnée.</span><span class="sxs-lookup"><span data-stu-id="880b1-108">The analysis operation was aborted.</span></span>

<span data-ttu-id="880b1-109">Retourné uniquement lorsque l’opération d’analyse synchrone est appelée.</span><span class="sxs-lookup"><span data-stu-id="880b1-109">Returned only when the synchronous analysis operation is called.</span></span> <span data-ttu-id="880b1-110">L’abandon d’une opération asynchrone ne déclenche pas d’événement [**\_ IAnalysisEvents :: Results**](-ianalysisevents-results.md) .</span><span class="sxs-lookup"><span data-stu-id="880b1-110">Aborting an asynchronous operation will not raise an [**\_IAnalysisEvents::Results**](-ianalysisevents-results.md) event.</span></span>

</dd> <dt>

<span data-ttu-id="880b1-111"><span id="AnalysisWarningCode_NoMatchingInkAnalysisRecognizerFound"></span><span id="analysiswarningcode_nomatchinginkanalysisrecognizerfound"></span><span id="ANALYSISWARNINGCODE_NOMATCHINGINKANALYSISRECOGNIZERFOUND"></span>**AnalysisWarningCode \_ NoMatchingInkAnalysisRecognizerFound**</span><span class="sxs-lookup"><span data-stu-id="880b1-111"><span id="AnalysisWarningCode_NoMatchingInkAnalysisRecognizerFound"></span><span id="analysiswarningcode_nomatchinginkanalysisrecognizerfound"></span><span id="ANALYSISWARNINGCODE_NOMATCHINGINKANALYSISRECOGNIZERFOUND"></span>**AnalysisWarningCode\_NoMatchingInkAnalysisRecognizerFound**</span></span>
</dt> <dd>

<span data-ttu-id="880b1-112">Le [**IInkAnalyzer**](iinkanalyzer.md) ne peut pas trouver un module de reconnaissance d’encre qui répond aux exigences de langue ou de capacité nécessaires à l’exécution de l’opération d’analyse.</span><span class="sxs-lookup"><span data-stu-id="880b1-112">The [**IInkAnalyzer**](iinkanalyzer.md) cannot find an ink recognizer that meets language or capability requirements needed to perform the analysis operation.</span></span>

</dd> <dt>

<span data-ttu-id="880b1-113"><span id="AnalysisWarningCode_FactoidNotSupported"></span><span id="analysiswarningcode_factoidnotsupported"></span><span id="ANALYSISWARNINGCODE_FACTOIDNOTSUPPORTED"></span>**AnalysisWarningCode \_ FactoidNotSupported**</span><span class="sxs-lookup"><span data-stu-id="880b1-113"><span id="AnalysisWarningCode_FactoidNotSupported"></span><span id="analysiswarningcode_factoidnotsupported"></span><span id="ANALYSISWARNINGCODE_FACTOIDNOTSUPPORTED"></span>**AnalysisWarningCode\_FactoidNotSupported**</span></span>
</dt> <dd>

<span data-ttu-id="880b1-114">Le module de reconnaissance de l’encre n’a pas pu respecter le jeu de Factoid spécifié sur le nœud de l’indicateur d’analyse (consultez [**IContextNode :: GetType**](icontextnode-gettype.md) et propriétés de l' [indicateur d’analyse](analysis-hint-properties.md)).</span><span class="sxs-lookup"><span data-stu-id="880b1-114">The ink recognizer was unable to respect the specified factoid set on the analysis hint node (see [**IContextNode::GetType**](icontextnode-gettype.md) and [Analysis Hint Properties](analysis-hint-properties.md)).</span></span>

</dd> <dt>

<span data-ttu-id="880b1-115"><span id="AnalysisWarningCode_FactoidCoercionNotSupported"></span><span id="analysiswarningcode_factoidcoercionnotsupported"></span><span id="ANALYSISWARNINGCODE_FACTOIDCOERCIONNOTSUPPORTED"></span>**AnalysisWarningCode \_ FactoidCoercionNotSupported**</span><span class="sxs-lookup"><span data-stu-id="880b1-115"><span id="AnalysisWarningCode_FactoidCoercionNotSupported"></span><span id="analysiswarningcode_factoidcoercionnotsupported"></span><span id="ANALYSISWARNINGCODE_FACTOIDCOERCIONNOTSUPPORTED"></span>**AnalysisWarningCode\_FactoidCoercionNotSupported**</span></span>
</dt> <dd>

<span data-ttu-id="880b1-116">Le module de reconnaissance de l’encre n’a pas pu contraindre ses résultats au jeu de Factoid spécifié sur le nœud de l’indicateur d’analyse (consultez [**IContextNode :: GetType**](icontextnode-gettype.md) et propriétés de l' [indicateur d’analyse](analysis-hint-properties.md)).</span><span class="sxs-lookup"><span data-stu-id="880b1-116">The ink recognizer was unable to coerce its results to the specified factoid set on the analysis hint node (see [**IContextNode::GetType**](icontextnode-gettype.md) and [Analysis Hint Properties](analysis-hint-properties.md)).</span></span>

</dd> <dt>

<span data-ttu-id="880b1-117"><span id="AnalysisWarningCode_GuideNotSupported"></span><span id="analysiswarningcode_guidenotsupported"></span><span id="ANALYSISWARNINGCODE_GUIDENOTSUPPORTED"></span>**AnalysisWarningCode \_ GuideNotSupported**</span><span class="sxs-lookup"><span data-stu-id="880b1-117"><span id="AnalysisWarningCode_GuideNotSupported"></span><span id="analysiswarningcode_guidenotsupported"></span><span id="ANALYSISWARNINGCODE_GUIDENOTSUPPORTED"></span>**AnalysisWarningCode\_GuideNotSupported**</span></span>
</dt> <dd>

<span data-ttu-id="880b1-118">Le module de reconnaissance de l’encre n’a pas pu respecter le jeu de guides spécifié sur le nœud de l’indicateur d’analyse (consultez [**IContextNode :: GetType**](icontextnode-gettype.md) et propriétés de l' [indicateur d’analyse](analysis-hint-properties.md)).</span><span class="sxs-lookup"><span data-stu-id="880b1-118">The ink recognizer was unable to respect the specified guide set on the analysis hint node (see [**IContextNode::GetType**](icontextnode-gettype.md) and [Analysis Hint Properties](analysis-hint-properties.md)).</span></span>

</dd> <dt>

<span data-ttu-id="880b1-119"><span id="AnalysisWarningCode_WordlistNotSupported"></span><span id="analysiswarningcode_wordlistnotsupported"></span><span id="ANALYSISWARNINGCODE_WORDLISTNOTSUPPORTED"></span>**AnalysisWarningCode \_ WordlistNotSupported**</span><span class="sxs-lookup"><span data-stu-id="880b1-119"><span id="AnalysisWarningCode_WordlistNotSupported"></span><span id="analysiswarningcode_wordlistnotsupported"></span><span id="ANALYSISWARNINGCODE_WORDLISTNOTSUPPORTED"></span>**AnalysisWarningCode\_WordlistNotSupported**</span></span>
</dt> <dd>

<span data-ttu-id="880b1-120">Le module de reconnaissance de l’encre n’a pas pu respecter la liste de mots spécifiée définie sur le nœud de l’indicateur d’analyse (consultez [**IContextNode :: GetType**](icontextnode-gettype.md) et propriétés de l' [indicateur d’analyse](analysis-hint-properties.md)).</span><span class="sxs-lookup"><span data-stu-id="880b1-120">The ink recognizer was unable to respect the specified word list set on the analysis hint node (see [**IContextNode::GetType**](icontextnode-gettype.md) and [Analysis Hint Properties](analysis-hint-properties.md)).</span></span>

</dd> <dt>

<span data-ttu-id="880b1-121"><span id="AnalysisWarningCode_WordModeNotSupported"></span><span id="analysiswarningcode_wordmodenotsupported"></span><span id="ANALYSISWARNINGCODE_WORDMODENOTSUPPORTED"></span>**AnalysisWarningCode \_ WordModeNotSupported**</span><span class="sxs-lookup"><span data-stu-id="880b1-121"><span id="AnalysisWarningCode_WordModeNotSupported"></span><span id="analysiswarningcode_wordmodenotsupported"></span><span id="ANALYSISWARNINGCODE_WORDMODENOTSUPPORTED"></span>**AnalysisWarningCode\_WordModeNotSupported**</span></span>
</dt> <dd>

<span data-ttu-id="880b1-122">Le module de reconnaissance de l’encre n’a pas pu respecter le mode Word spécifié défini sur le nœud de l’indicateur d’analyse (consultez [**IContextNode :: GetType**](icontextnode-gettype.md) et propriétés de l' [indicateur d’analyse](analysis-hint-properties.md)).</span><span class="sxs-lookup"><span data-stu-id="880b1-122">The ink recognizer was unable to respect the specified word mode set on the analysis hint node (see [**IContextNode::GetType**](icontextnode-gettype.md) and [Analysis Hint Properties](analysis-hint-properties.md)).</span></span>

</dd> <dt>

<span data-ttu-id="880b1-123"><span id="AnalysisWarningCode_PartialDictionaryTermsNotSupported"></span><span id="analysiswarningcode_partialdictionarytermsnotsupported"></span><span id="ANALYSISWARNINGCODE_PARTIALDICTIONARYTERMSNOTSUPPORTED"></span>**AnalysisWarningCode \_ PartialDictionaryTermsNotSupported**</span><span class="sxs-lookup"><span data-stu-id="880b1-123"><span id="AnalysisWarningCode_PartialDictionaryTermsNotSupported"></span><span id="analysiswarningcode_partialdictionarytermsnotsupported"></span><span id="ANALYSISWARNINGCODE_PARTIALDICTIONARYTERMSNOTSUPPORTED"></span>**AnalysisWarningCode\_PartialDictionaryTermsNotSupported**</span></span>
</dt> <dd>

<span data-ttu-id="880b1-124">Indique que les termes du dictionnaire partiels n’ont pas pu être retournés à partir du [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md).</span><span class="sxs-lookup"><span data-stu-id="880b1-124">Indicates that partial dictionary terms could not be returned from the [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md).</span></span>

</dd> <dt>

<span data-ttu-id="880b1-125"><span id="AnalysisWarningCode_TextRecognitionProcessFailed"></span><span id="analysiswarningcode_textrecognitionprocessfailed"></span><span id="ANALYSISWARNINGCODE_TEXTRECOGNITIONPROCESSFAILED"></span>**AnalysisWarningCode \_ TextRecognitionProcessFailed**</span><span class="sxs-lookup"><span data-stu-id="880b1-125"><span id="AnalysisWarningCode_TextRecognitionProcessFailed"></span><span id="analysiswarningcode_textrecognitionprocessfailed"></span><span id="ANALYSISWARNINGCODE_TEXTRECOGNITIONPROCESSFAILED"></span>**AnalysisWarningCode\_TextRecognitionProcessFailed**</span></span>
</dt> <dd>

<span data-ttu-id="880b1-126">Indique que le processus de reconnaissance du texte a échoué.</span><span class="sxs-lookup"><span data-stu-id="880b1-126">Indicates the text recognition process failed.</span></span>

</dd> <dt>

<span data-ttu-id="880b1-127"><span id="AnalysisWarningCode_AddInkToRecognizerFailed"></span><span id="analysiswarningcode_addinktorecognizerfailed"></span><span id="ANALYSISWARNINGCODE_ADDINKTORECOGNIZERFAILED"></span>**AnalysisWarningCode \_ AddInkToRecognizerFailed**</span><span class="sxs-lookup"><span data-stu-id="880b1-127"><span id="AnalysisWarningCode_AddInkToRecognizerFailed"></span><span id="analysiswarningcode_addinktorecognizerfailed"></span><span id="ANALYSISWARNINGCODE_ADDINKTORECOGNIZERFAILED"></span>**AnalysisWarningCode\_AddInkToRecognizerFailed**</span></span>
</dt> <dd>

<span data-ttu-id="880b1-128">Impossible d’ajouter l’encre au [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md).</span><span class="sxs-lookup"><span data-stu-id="880b1-128">The ink could not be added to the [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md).</span></span> <span data-ttu-id="880b1-129">Par exemple, l’ajout de traits collectés à partir d’une souris sur un module de reconnaissance de mouvement échouera, car le module de reconnaissance de mouvement exige des traits collectés à partir d’un digitaliseur.</span><span class="sxs-lookup"><span data-stu-id="880b1-129">For example, adding strokes collected from a mouse on a gesture recognizer will fail, as the gesture recognizer requires strokes collected from a digitizer.</span></span>

</dd> <dt>

<span data-ttu-id="880b1-130"><span id="AnalysisWarningCode_SetPrefixSuffixFailed"></span><span id="analysiswarningcode_setprefixsuffixfailed"></span><span id="ANALYSISWARNINGCODE_SETPREFIXSUFFIXFAILED"></span>**AnalysisWarningCode \_ SetPrefixSuffixFailed**</span><span class="sxs-lookup"><span data-stu-id="880b1-130"><span id="AnalysisWarningCode_SetPrefixSuffixFailed"></span><span id="analysiswarningcode_setprefixsuffixfailed"></span><span id="ANALYSISWARNINGCODE_SETPREFIXSUFFIXFAILED"></span>**AnalysisWarningCode\_SetPrefixSuffixFailed**</span></span>
</dt> <dd>

<span data-ttu-id="880b1-131">[**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) n’a pas pu respecter le préfixe ou le texte de suffixe spécifié d’un nœud d’indicateur d’analyse (consultez [**IContextNode :: GetType**](icontextnode-gettype.md) et propriétés de l' [indicateur d’analyse](analysis-hint-properties.md)).</span><span class="sxs-lookup"><span data-stu-id="880b1-131">The [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) was unable to respect the specified prefix or suffix text of an analysis hint node (see [**IContextNode::GetType**](icontextnode-gettype.md) and [Analysis Hint Properties](analysis-hint-properties.md)).</span></span>

</dd> <dt>

<span data-ttu-id="880b1-132"><span id="AnalysisWarningCode_InkAnalysisRecognizerInitializationFailed"></span><span id="analysiswarningcode_inkanalysisrecognizerinitializationfailed"></span><span id="ANALYSISWARNINGCODE_INKANALYSISRECOGNIZERINITIALIZATIONFAILED"></span>**AnalysisWarningCode \_ InkAnalysisRecognizerInitializationFailed**</span><span class="sxs-lookup"><span data-stu-id="880b1-132"><span id="AnalysisWarningCode_InkAnalysisRecognizerInitializationFailed"></span><span id="analysiswarningcode_inkanalysisrecognizerinitializationfailed"></span><span id="ANALYSISWARNINGCODE_INKANALYSISRECOGNIZERINITIALIZATIONFAILED"></span>**AnalysisWarningCode\_InkAnalysisRecognizerInitializationFailed**</span></span>
</dt> <dd>

<span data-ttu-id="880b1-133">[**IInkAnalyzer**](iinkanalyzer.md) n’a pas été en mesure d’instancier, de cloner ou de définir des traits sur [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md).</span><span class="sxs-lookup"><span data-stu-id="880b1-133">The [**IInkAnalyzer**](iinkanalyzer.md) was not able to instantiate, clone, or set strokes on the [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md).</span></span>

</dd> <dt>

<span data-ttu-id="880b1-134"><span id="AnalysisWarningCode_ConfirmedWithoutInkRecognition"></span><span id="analysiswarningcode_confirmedwithoutinkrecognition"></span><span id="ANALYSISWARNINGCODE_CONFIRMEDWITHOUTINKRECOGNITION"></span>**AnalysisWarningCode \_ ConfirmedWithoutInkRecognition**</span><span class="sxs-lookup"><span data-stu-id="880b1-134"><span id="AnalysisWarningCode_ConfirmedWithoutInkRecognition"></span><span id="analysiswarningcode_confirmedwithoutinkrecognition"></span><span id="ANALYSISWARNINGCODE_CONFIRMEDWITHOUTINKRECOGNITION"></span>**AnalysisWarningCode\_ConfirmedWithoutInkRecognition**</span></span>
</dt> <dd>

<span data-ttu-id="880b1-135">Indique qu’un objet [**IContextNode**](icontextnode.md) a été confirmé par l’utilisateur sans que des valeurs de reconnaissance soient calculées pour le nœud.</span><span class="sxs-lookup"><span data-stu-id="880b1-135">Indicates that an [**IContextNode**](icontextnode.md) object has been confirmed by the user without having any recognition values computed for the node.</span></span>

</dd> <dt>

<span data-ttu-id="880b1-136"><span id="AnalysisWarningCode_BackgroundException"></span><span id="analysiswarningcode_backgroundexception"></span><span id="ANALYSISWARNINGCODE_BACKGROUNDEXCEPTION"></span>**AnalysisWarningCode \_ BackgroundException**</span><span class="sxs-lookup"><span data-stu-id="880b1-136"><span id="AnalysisWarningCode_BackgroundException"></span><span id="analysiswarningcode_backgroundexception"></span><span id="ANALYSISWARNINGCODE_BACKGROUNDEXCEPTION"></span>**AnalysisWarningCode\_BackgroundException**</span></span>
</dt> <dd>

<span data-ttu-id="880b1-137">L’opération d’arrière-plan ne s’est pas terminée en raison d’une exception.</span><span class="sxs-lookup"><span data-stu-id="880b1-137">The background operation did not complete due to an exception.</span></span> <span data-ttu-id="880b1-138">Il s’agit d’une erreur irrécupérable qui requiert la réinstanciation du [**IInkAnalyzer**](iinkanalyzer.md) avant d’utiliser.</span><span class="sxs-lookup"><span data-stu-id="880b1-138">This is a fatal error and requires that the [**IInkAnalyzer**](iinkanalyzer.md) is re-instantiated before further use.</span></span>

</dd> <dt>

<span data-ttu-id="880b1-139"><span id="AnalysisWarningCode_ContextNodeLocationNotSet"></span><span id="analysiswarningcode_contextnodelocationnotset"></span><span id="ANALYSISWARNINGCODE_CONTEXTNODELOCATIONNOTSET"></span>**AnalysisWarningCode \_ ContextNodeLocationNotSet**</span><span class="sxs-lookup"><span data-stu-id="880b1-139"><span id="AnalysisWarningCode_ContextNodeLocationNotSet"></span><span id="analysiswarningcode_contextnodelocationnotset"></span><span id="ANALYSISWARNINGCODE_CONTEXTNODELOCATIONNOTSET"></span>**AnalysisWarningCode\_ContextNodeLocationNotSet**</span></span>
</dt> <dd>

<span data-ttu-id="880b1-140">Indique qu’un objet [**IContextNode**](icontextnode.md) n’a pas de jeu d’emplacements approprié (consultez [**IContextNode :: SetLocation**](icontextnode-setlocation.md)).</span><span class="sxs-lookup"><span data-stu-id="880b1-140">Indicates that an [**IContextNode**](icontextnode.md) object does not have a proper location set (see [**IContextNode::SetLocation**](icontextnode-setlocation.md)).</span></span> <span data-ttu-id="880b1-141">La méthode [**IContextNode :: GetLocation**](icontextnode-getlocation.md) doit retourner une valeur non vide, sauf si l’objet **IContextNode** est marqué comme partiellement rempli.</span><span class="sxs-lookup"><span data-stu-id="880b1-141">The [**IContextNode::GetLocation**](icontextnode-getlocation.md) method must return a non-empty value unless the **IContextNode** object is marked as partially populated.</span></span>

</dd> <dt>

<span data-ttu-id="880b1-142"><span id="AnalysisWarningCode_LanguageIdNotRespected"></span><span id="analysiswarningcode_languageidnotrespected"></span><span id="ANALYSISWARNINGCODE_LANGUAGEIDNOTRESPECTED"></span>**AnalysisWarningCode \_ LanguageIdNotRespected**</span><span class="sxs-lookup"><span data-stu-id="880b1-142"><span id="AnalysisWarningCode_LanguageIdNotRespected"></span><span id="analysiswarningcode_languageidnotrespected"></span><span id="ANALYSISWARNINGCODE_LANGUAGEIDNOTRESPECTED"></span>**AnalysisWarningCode\_LanguageIdNotRespected**</span></span>
</dt> <dd>

<span data-ttu-id="880b1-143">L’identificateur de langue défini sur un trait associé à un nœud de reconnaissance personnalisé (voir [**IContextNode :: GetType**](icontextnode-gettype.md)) ne correspond pas à l’identificateur de langue du [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) utilisé.</span><span class="sxs-lookup"><span data-stu-id="880b1-143">The language identifier set on a stroke associated with a custom recognizer node (see [**IContextNode::GetType**](icontextnode-gettype.md)) did not match the language identifier of the [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) used.</span></span> <span data-ttu-id="880b1-144">L’encre était toujours reconnue avec le **IInkAnalysisRecognizer** spécifié.</span><span class="sxs-lookup"><span data-stu-id="880b1-144">The ink was still recognized with the specified **IInkAnalysisRecognizer**.</span></span>

</dd> <dt>

<span data-ttu-id="880b1-145"><span id="AnalysisWarningCode_EnableUnicodeCharacterRangesNotSupported"></span><span id="analysiswarningcode_enableunicodecharacterrangesnotsupported"></span><span id="ANALYSISWARNINGCODE_ENABLEUNICODECHARACTERRANGESNOTSUPPORTED"></span>**AnalysisWarningCode \_ EnableUnicodeCharacterRangesNotSupported**</span><span class="sxs-lookup"><span data-stu-id="880b1-145"><span id="AnalysisWarningCode_EnableUnicodeCharacterRangesNotSupported"></span><span id="analysiswarningcode_enableunicodecharacterrangesnotsupported"></span><span id="ANALYSISWARNINGCODE_ENABLEUNICODECHARACTERRANGESNOTSUPPORTED"></span>**AnalysisWarningCode\_EnableUnicodeCharacterRangesNotSupported**</span></span>
</dt> <dd>

<span data-ttu-id="880b1-146">[**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) ne prend pas en charge l’activation des plages de caractères Unicode comme spécifié.</span><span class="sxs-lookup"><span data-stu-id="880b1-146">The [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) does not support enabling Unicode character ranges as specified.</span></span>

</dd> <dt>

<span data-ttu-id="880b1-147"><span id="AnalysisWarningCode_TopInkBreaksOnlyNotSupported"></span><span id="analysiswarningcode_topinkbreaksonlynotsupported"></span><span id="ANALYSISWARNINGCODE_TOPINKBREAKSONLYNOTSUPPORTED"></span>**AnalysisWarningCode \_ TopInkBreaksOnlyNotSupported**</span><span class="sxs-lookup"><span data-stu-id="880b1-147"><span id="AnalysisWarningCode_TopInkBreaksOnlyNotSupported"></span><span id="analysiswarningcode_topinkbreaksonlynotsupported"></span><span id="ANALYSISWARNINGCODE_TOPINKBREAKSONLYNOTSUPPORTED"></span>**AnalysisWarningCode\_TopInkBreaksOnlyNotSupported**</span></span>
</dt> <dd>

<span data-ttu-id="880b1-148">[**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) ne prend pas en charge TopInkBreaks uniquement, même si les indicateurs contiennent uniquement la demande de TopInkBreaks.</span><span class="sxs-lookup"><span data-stu-id="880b1-148">The [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) does not support TopInkBreaks only even though the hints contained the request for TopInkBreaks only.</span></span>

</dd> <dt>

<span data-ttu-id="880b1-149"><span id="AnalysisWarningCode_AnalysisAlreadyRunning"></span><span id="analysiswarningcode_analysisalreadyrunning"></span><span id="ANALYSISWARNINGCODE_ANALYSISALREADYRUNNING"></span>**AnalysisWarningCode \_ AnalysisAlreadyRunning**</span><span class="sxs-lookup"><span data-stu-id="880b1-149"><span id="AnalysisWarningCode_AnalysisAlreadyRunning"></span><span id="analysiswarningcode_analysisalreadyrunning"></span><span id="ANALYSISWARNINGCODE_ANALYSISALREADYRUNNING"></span>**AnalysisWarningCode\_AnalysisAlreadyRunning**</span></span>
</dt> <dd>

<span data-ttu-id="880b1-150">[**IInkAnalyzer**](iinkanalyzer.md) effectue déjà une analyse en arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="880b1-150">The [**IInkAnalyzer**](iinkanalyzer.md) is already performing background analysis.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="880b1-151">Notes</span><span class="sxs-lookup"><span data-stu-id="880b1-151">Remarks</span></span>

<span data-ttu-id="880b1-152">**AnalysisWarningCode \_ BackgroundException** est la seule valeur de code d’avertissement qui exige que l’objet [**IInkAnalyzer**](iinkanalyzer.md) soit réinstancié avant d’être utilisé.</span><span class="sxs-lookup"><span data-stu-id="880b1-152">**AnalysisWarningCode\_BackgroundException** is the only warning code value that requires that the [**IInkAnalyzer**](iinkanalyzer.md) object is re-instantiated before further use.</span></span>

<span data-ttu-id="880b1-153">D’autres valeurs de code d’avertissements, telles que **AnalysisWarningCode \_ InkAnalysisRecognizerInitializationFailed** et **AnalysisWarningCode \_ NoMatchingInkAnalysisRecognizerFound**, peuvent exiger que l’objet [**IInkAnalyzer**](iinkanalyzer.md) utilise un autre module de reconnaissance.</span><span class="sxs-lookup"><span data-stu-id="880b1-153">Other warnings code values, such as **AnalysisWarningCode\_InkAnalysisRecognizerInitializationFailed** and **AnalysisWarningCode\_NoMatchingInkAnalysisRecognizerFound**, might require that the [**IInkAnalyzer**](iinkanalyzer.md) object use a different recognizer.</span></span>

## <a name="requirements"></a><span data-ttu-id="880b1-154">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="880b1-154">Requirements</span></span>



| <span data-ttu-id="880b1-155">Condition requise</span><span class="sxs-lookup"><span data-stu-id="880b1-155">Requirement</span></span> | <span data-ttu-id="880b1-156">Valeur</span><span class="sxs-lookup"><span data-stu-id="880b1-156">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="880b1-157">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="880b1-157">Minimum supported client</span></span><br/> | <span data-ttu-id="880b1-158">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="880b1-158">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="880b1-159">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="880b1-159">Minimum supported server</span></span><br/> | <span data-ttu-id="880b1-160">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="880b1-160">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="880b1-161">En-tête</span><span class="sxs-lookup"><span data-stu-id="880b1-161">Header</span></span><br/>                   | <dl> <span data-ttu-id="880b1-162"><dt>IACom. h (nécessite également IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="880b1-162"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="880b1-163">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="880b1-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="880b1-164">**IAnalysisWarning::GetWarningCode**</span><span class="sxs-lookup"><span data-stu-id="880b1-164">**IAnalysisWarning::GetWarningCode**</span></span>](ianalysiswarning-getwarningcode.md)
</dt> <dt>

[<span data-ttu-id="880b1-165">Référence de l’analyse de l’encre</span><span class="sxs-lookup"><span data-stu-id="880b1-165">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




