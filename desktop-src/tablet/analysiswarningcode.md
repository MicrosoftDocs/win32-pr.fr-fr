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
ms.openlocfilehash: 48d03c0f4c479ddf6a3f1f9f371bc13b889641994f86df75b107b17ca081a97a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119660869"
---
# <a name="analysiswarningcode-enumeration"></a>Énumération AnalysisWarningCode

Spécifie l’ensemble des avertissements disponibles qui peuvent se produire lors de l’analyse de l’encre.

## <a name="syntax"></a>Syntaxe


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



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="AnalysisWarningCode_Aborted"></span><span id="analysiswarningcode_aborted"></span><span id="ANALYSISWARNINGCODE_ABORTED"></span>**AnalysisWarningCode \_ abandonné**
</dt> <dd>

L’opération d’analyse a été abandonnée.

Retourné uniquement lorsque l’opération d’analyse synchrone est appelée. L’abandon d’une opération asynchrone ne déclenche pas d’événement [**\_ IAnalysisEvents :: Results**](-ianalysisevents-results.md) .

</dd> <dt>

<span id="AnalysisWarningCode_NoMatchingInkAnalysisRecognizerFound"></span><span id="analysiswarningcode_nomatchinginkanalysisrecognizerfound"></span><span id="ANALYSISWARNINGCODE_NOMATCHINGINKANALYSISRECOGNIZERFOUND"></span>**AnalysisWarningCode \_ NoMatchingInkAnalysisRecognizerFound**
</dt> <dd>

Le [**IInkAnalyzer**](iinkanalyzer.md) ne peut pas trouver un module de reconnaissance d’encre qui répond aux exigences de langue ou de capacité nécessaires à l’exécution de l’opération d’analyse.

</dd> <dt>

<span id="AnalysisWarningCode_FactoidNotSupported"></span><span id="analysiswarningcode_factoidnotsupported"></span><span id="ANALYSISWARNINGCODE_FACTOIDNOTSUPPORTED"></span>**AnalysisWarningCode \_ FactoidNotSupported**
</dt> <dd>

Le module de reconnaissance de l’encre n’a pas pu respecter le jeu de Factoid spécifié sur le nœud de l’indicateur d’analyse (consultez [**IContextNode :: GetType**](icontextnode-gettype.md) et propriétés de l' [indicateur d’analyse](analysis-hint-properties.md)).

</dd> <dt>

<span id="AnalysisWarningCode_FactoidCoercionNotSupported"></span><span id="analysiswarningcode_factoidcoercionnotsupported"></span><span id="ANALYSISWARNINGCODE_FACTOIDCOERCIONNOTSUPPORTED"></span>**AnalysisWarningCode \_ FactoidCoercionNotSupported**
</dt> <dd>

Le module de reconnaissance de l’encre n’a pas pu contraindre ses résultats au jeu de Factoid spécifié sur le nœud de l’indicateur d’analyse (consultez [**IContextNode :: GetType**](icontextnode-gettype.md) et propriétés de l' [indicateur d’analyse](analysis-hint-properties.md)).

</dd> <dt>

<span id="AnalysisWarningCode_GuideNotSupported"></span><span id="analysiswarningcode_guidenotsupported"></span><span id="ANALYSISWARNINGCODE_GUIDENOTSUPPORTED"></span>**AnalysisWarningCode \_ GuideNotSupported**
</dt> <dd>

Le module de reconnaissance de l’encre n’a pas pu respecter le jeu de guides spécifié sur le nœud de l’indicateur d’analyse (consultez [**IContextNode :: GetType**](icontextnode-gettype.md) et propriétés de l' [indicateur d’analyse](analysis-hint-properties.md)).

</dd> <dt>

<span id="AnalysisWarningCode_WordlistNotSupported"></span><span id="analysiswarningcode_wordlistnotsupported"></span><span id="ANALYSISWARNINGCODE_WORDLISTNOTSUPPORTED"></span>**AnalysisWarningCode \_ WordlistNotSupported**
</dt> <dd>

Le module de reconnaissance de l’encre n’a pas pu respecter la liste de mots spécifiée définie sur le nœud de l’indicateur d’analyse (consultez [**IContextNode :: GetType**](icontextnode-gettype.md) et propriétés de l' [indicateur d’analyse](analysis-hint-properties.md)).

</dd> <dt>

<span id="AnalysisWarningCode_WordModeNotSupported"></span><span id="analysiswarningcode_wordmodenotsupported"></span><span id="ANALYSISWARNINGCODE_WORDMODENOTSUPPORTED"></span>**AnalysisWarningCode \_ WordModeNotSupported**
</dt> <dd>

Le module de reconnaissance de l’encre n’a pas pu respecter le mode Word spécifié défini sur le nœud de l’indicateur d’analyse (consultez [**IContextNode :: GetType**](icontextnode-gettype.md) et propriétés de l' [indicateur d’analyse](analysis-hint-properties.md)).

</dd> <dt>

<span id="AnalysisWarningCode_PartialDictionaryTermsNotSupported"></span><span id="analysiswarningcode_partialdictionarytermsnotsupported"></span><span id="ANALYSISWARNINGCODE_PARTIALDICTIONARYTERMSNOTSUPPORTED"></span>**AnalysisWarningCode \_ PartialDictionaryTermsNotSupported**
</dt> <dd>

Indique que les termes du dictionnaire partiels n’ont pas pu être retournés à partir du [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md).

</dd> <dt>

<span id="AnalysisWarningCode_TextRecognitionProcessFailed"></span><span id="analysiswarningcode_textrecognitionprocessfailed"></span><span id="ANALYSISWARNINGCODE_TEXTRECOGNITIONPROCESSFAILED"></span>**AnalysisWarningCode \_ TextRecognitionProcessFailed**
</dt> <dd>

Indique que le processus de reconnaissance du texte a échoué.

</dd> <dt>

<span id="AnalysisWarningCode_AddInkToRecognizerFailed"></span><span id="analysiswarningcode_addinktorecognizerfailed"></span><span id="ANALYSISWARNINGCODE_ADDINKTORECOGNIZERFAILED"></span>**AnalysisWarningCode \_ AddInkToRecognizerFailed**
</dt> <dd>

Impossible d’ajouter l’encre au [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md). Par exemple, l’ajout de traits collectés à partir d’une souris sur un module de reconnaissance de mouvement échouera, car le module de reconnaissance de mouvement exige des traits collectés à partir d’un digitaliseur.

</dd> <dt>

<span id="AnalysisWarningCode_SetPrefixSuffixFailed"></span><span id="analysiswarningcode_setprefixsuffixfailed"></span><span id="ANALYSISWARNINGCODE_SETPREFIXSUFFIXFAILED"></span>**AnalysisWarningCode \_ SetPrefixSuffixFailed**
</dt> <dd>

[**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) n’a pas pu respecter le préfixe ou le texte de suffixe spécifié d’un nœud d’indicateur d’analyse (consultez [**IContextNode :: GetType**](icontextnode-gettype.md) et propriétés de l' [indicateur d’analyse](analysis-hint-properties.md)).

</dd> <dt>

<span id="AnalysisWarningCode_InkAnalysisRecognizerInitializationFailed"></span><span id="analysiswarningcode_inkanalysisrecognizerinitializationfailed"></span><span id="ANALYSISWARNINGCODE_INKANALYSISRECOGNIZERINITIALIZATIONFAILED"></span>**AnalysisWarningCode \_ InkAnalysisRecognizerInitializationFailed**
</dt> <dd>

[**IInkAnalyzer**](iinkanalyzer.md) n’a pas été en mesure d’instancier, de cloner ou de définir des traits sur [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md).

</dd> <dt>

<span id="AnalysisWarningCode_ConfirmedWithoutInkRecognition"></span><span id="analysiswarningcode_confirmedwithoutinkrecognition"></span><span id="ANALYSISWARNINGCODE_CONFIRMEDWITHOUTINKRECOGNITION"></span>**AnalysisWarningCode \_ ConfirmedWithoutInkRecognition**
</dt> <dd>

Indique qu’un objet [**IContextNode**](icontextnode.md) a été confirmé par l’utilisateur sans que des valeurs de reconnaissance soient calculées pour le nœud.

</dd> <dt>

<span id="AnalysisWarningCode_BackgroundException"></span><span id="analysiswarningcode_backgroundexception"></span><span id="ANALYSISWARNINGCODE_BACKGROUNDEXCEPTION"></span>**AnalysisWarningCode \_ BackgroundException**
</dt> <dd>

L’opération d’arrière-plan ne s’est pas terminée en raison d’une exception. Il s’agit d’une erreur irrécupérable qui requiert la réinstanciation du [**IInkAnalyzer**](iinkanalyzer.md) avant d’utiliser.

</dd> <dt>

<span id="AnalysisWarningCode_ContextNodeLocationNotSet"></span><span id="analysiswarningcode_contextnodelocationnotset"></span><span id="ANALYSISWARNINGCODE_CONTEXTNODELOCATIONNOTSET"></span>**AnalysisWarningCode \_ ContextNodeLocationNotSet**
</dt> <dd>

Indique qu’un objet [**IContextNode**](icontextnode.md) n’a pas de jeu d’emplacements approprié (consultez [**IContextNode :: SetLocation**](icontextnode-setlocation.md)). La méthode [**IContextNode :: GetLocation**](icontextnode-getlocation.md) doit retourner une valeur non vide, sauf si l’objet **IContextNode** est marqué comme partiellement rempli.

</dd> <dt>

<span id="AnalysisWarningCode_LanguageIdNotRespected"></span><span id="analysiswarningcode_languageidnotrespected"></span><span id="ANALYSISWARNINGCODE_LANGUAGEIDNOTRESPECTED"></span>**AnalysisWarningCode \_ LanguageIdNotRespected**
</dt> <dd>

L’identificateur de langue défini sur un trait associé à un nœud de reconnaissance personnalisé (voir [**IContextNode :: GetType**](icontextnode-gettype.md)) ne correspond pas à l’identificateur de langue du [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) utilisé. L’encre était toujours reconnue avec le **IInkAnalysisRecognizer** spécifié.

</dd> <dt>

<span id="AnalysisWarningCode_EnableUnicodeCharacterRangesNotSupported"></span><span id="analysiswarningcode_enableunicodecharacterrangesnotsupported"></span><span id="ANALYSISWARNINGCODE_ENABLEUNICODECHARACTERRANGESNOTSUPPORTED"></span>**AnalysisWarningCode \_ EnableUnicodeCharacterRangesNotSupported**
</dt> <dd>

[**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) ne prend pas en charge l’activation des plages de caractères Unicode comme spécifié.

</dd> <dt>

<span id="AnalysisWarningCode_TopInkBreaksOnlyNotSupported"></span><span id="analysiswarningcode_topinkbreaksonlynotsupported"></span><span id="ANALYSISWARNINGCODE_TOPINKBREAKSONLYNOTSUPPORTED"></span>**AnalysisWarningCode \_ TopInkBreaksOnlyNotSupported**
</dt> <dd>

[**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) ne prend pas en charge TopInkBreaks uniquement, même si les indicateurs contiennent uniquement la demande de TopInkBreaks.

</dd> <dt>

<span id="AnalysisWarningCode_AnalysisAlreadyRunning"></span><span id="analysiswarningcode_analysisalreadyrunning"></span><span id="ANALYSISWARNINGCODE_ANALYSISALREADYRUNNING"></span>**AnalysisWarningCode \_ AnalysisAlreadyRunning**
</dt> <dd>

[**IInkAnalyzer**](iinkanalyzer.md) effectue déjà une analyse en arrière-plan.

</dd> </dl>

## <a name="remarks"></a>Remarques

**AnalysisWarningCode \_ BackgroundException** est la seule valeur de code d’avertissement qui exige que l’objet [**IInkAnalyzer**](iinkanalyzer.md) soit réinstancié avant d’être utilisé.

D’autres valeurs de code d’avertissements, telles que **AnalysisWarningCode \_ InkAnalysisRecognizerInitializationFailed** et **AnalysisWarningCode \_ NoMatchingInkAnalysisRecognizerFound**, peuvent exiger que l’objet [**IInkAnalyzer**](iinkanalyzer.md) utilise un autre module de reconnaissance.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Applications de bureau XP Édition Tablet PC \[ uniquement\]<br/>                                                 |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                                     |
| En-tête<br/>                   | <dl> <dt>IACom. h (nécessite également IACom \_ i. c)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IAnalysisWarning::GetWarningCode**](ianalysiswarning-getwarningcode.md)
</dt> <dt>

[Référence de l’analyse de l’encre](ink-analysis-reference.md)
</dt> </dl>

 

 




