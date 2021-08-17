---
description: Spécifie les attributs d’un IInkAnalysisRecognizer.
ms.assetid: e9577d83-0212-4f2f-88d7-e9153ec9fae5
title: Énumération RecognizerCapabilities (IACom. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InkAnalysisRecognizerCapabilities
api_type:
- HeaderDef
api_location:
- IACom.h
ms.openlocfilehash: 96e932b8e47f323198e1b0cc87da0df7839a593a76850c00c2c2e4d095854851
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119091449"
---
# <a name="recognizercapabilities-enumeration"></a>Énumération RecognizerCapabilities

Spécifie les attributs d’un [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md).

## <a name="syntax"></a>Syntaxe


```C++
typedef enum RecognizerCapabilities { 
  RC_None                            = 0,
  RC_DoNotCare                       = 0x1,
  RC_Object                          = 0x2,
  RC_FreeInput                       = 0x4,
  RC_LinedInput                      = 0x8,
  RC_BoxedInput                      = 0x10,
  RC_CharacterAutoCompletionInput    = 0x20,
  RC_RightAndDown                    = 0x40,
  RC_LeftAndDown                     = 0x80,
  RC_DownAndLeft                     = 0x100,
  RC_DownAndRight                    = 0x200,
  RC_ArbitraryAngle                  = 0x400,
  RC_Lattice                         = 0x800,
  RC_AdviseInkChange                 = 0x1000,
  RC_StrokeReorder                   = 0x2000,
  RC_Personalizable                  = 0x4000,
  RC_PrefersArbitraryAngle           = 0x8000,
  RC_PrefersParagraphBreaking        = 0x10000,
  RC_PrefersSegmentationRecognition  = 0x20000
} InkAnalysisRecognizerCapabilities;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="RC_None"></span><span id="rc_none"></span><span id="RC_NONE"></span>**RC \_ aucun**
</dt> <dd>

Aucune fonctionnalité n’est spécifiée.

</dd> <dt>

<span id="RC_DoNotCare"></span><span id="rc_donotcare"></span><span id="RC_DONOTCARE"></span>**RC \_ DoNotCare**
</dt> <dd>

Ignore tous les autres indicateurs définis.

</dd> <dt>

<span id="RC_Object"></span><span id="rc_object"></span><span id="RC_OBJECT"></span>**\_Objet RC**
</dt> <dd>

Prend en charge la reconnaissance d’objets ; Sinon, reconnaît uniquement le texte.

</dd> <dt>

<span id="RC_FreeInput"></span><span id="rc_freeinput"></span><span id="RC_FREEINPUT"></span>**RC \_ FreeInput**
</dt> <dd>

Prend en charge l’entrée gratuite, où l’encre est entrée sans utiliser de guide de reconnaissance, tel qu’une ligne ou une zone.

</dd> <dt>

<span id="RC_LinedInput"></span><span id="rc_linedinput"></span><span id="RC_LINEDINPUT"></span>**RC \_ LinedInput**
</dt> <dd>

Prend en charge l’entrée en ligne, qui est semblable à l’écriture sur le papier en courbes.

</dd> <dt>

<span id="RC_BoxedInput"></span><span id="rc_boxedinput"></span><span id="RC_BOXEDINPUT"></span>**RC \_ BoxedInput**
</dt> <dd>

Prend en charge les entrées boxed, où chaque caractère ou mot est entré dans une zone.

</dd> <dt>

<span id="RC_CharacterAutoCompletionInput"></span><span id="rc_characterautocompletioninput"></span><span id="RC_CHARACTERAUTOCOMPLETIONINPUT"></span>**RC \_ CharacterAutoCompletionInput**
</dt> <dd>

Prend en charge la saisie semi-automatique de caractères. Les détecteurs qui prennent en charge la saisie semi-automatique des caractères nécessitent une entrée boxed.

</dd> <dt>

<span id="RC_RightAndDown"></span><span id="rc_rightanddown"></span><span id="RC_RIGHTANDDOWN"></span>**RC \_ RightAndDown**
</dt> <dd>

Prend en charge les entrées d’écriture manuscrite dans l’ordre de droite et de baisse, par exemple dans les langues occidentales et les langues d’Extrême-Orient.

</dd> <dt>

<span id="RC_LeftAndDown"></span><span id="rc_leftanddown"></span><span id="RC_LEFTANDDOWN"></span>**RC \_ LeftAndDown**
</dt> <dd>

Prend en charge l’entrée manuscrite dans l’ordre de gauche et de droite, comme dans les langues hébreu et arabe.

</dd> <dt>

<span id="RC_DownAndLeft"></span><span id="rc_downandleft"></span><span id="RC_DOWNANDLEFT"></span>**RC \_ DownAndLeft**
</dt> <dd>

Prend en charge l’entrée de l’écriture manuscrite dans le sens le plus à gauche, par exemple dans certaines langues d’Extrême-Orient.

</dd> <dt>

<span id="RC_DownAndRight"></span><span id="rc_downandright"></span><span id="RC_DOWNANDRIGHT"></span>**RC \_ DownAndRight**
</dt> <dd>

Prend en charge l’entrée d’écriture manuscrite dans le sens le plus approprié, par exemple dans certaines langues d’Extrême-Orient.

</dd> <dt>

<span id="RC_ArbitraryAngle"></span><span id="rc_arbitraryangle"></span><span id="RC_ARBITRARYANGLE"></span>**RC \_ ArbitraryAngle**
</dt> <dd>

Prend en charge le texte écrit à des angles arbitraires.

</dd> <dt>

<span id="RC_Lattice"></span><span id="rc_lattice"></span><span id="RC_LATTICE"></span>**\_Treillis RC**
</dt> <dd>

Prend en charge le retour d’un treillis comme alternative à une chaîne pour les résultats de reconnaissance de l’écriture manuscrite.

</dd> <dt>

<span id="RC_AdviseInkChange"></span><span id="rc_adviseinkchange"></span><span id="RC_ADVISEINKCHANGE"></span>**RC \_ AdviseInkChange**
</dt> <dd>

Prend en charge l’interruption de la reconnaissance en arrière-plan, par exemple lorsque l’encre a changé.

</dd> <dt>

<span id="RC_StrokeReorder"></span><span id="rc_strokereorder"></span><span id="RC_STROKEREORDER"></span>**RC \_ StrokeReorder**
</dt> <dd>

Prend en charge l’ordre des traits, l’spatial et le temporal, est géré dans le cadre de l’opération de reconnaissance. [**IInkAnalyzer**](iinkanalyzer.md) ne réorganise pas les traits avant l’envoi de l’encre au [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md).

</dd> <dt>

<span id="RC_Personalizable"></span><span id="rc_personalizable"></span><span id="RC_PERSONALIZABLE"></span>**RC \_ personnalisable**
</dt> <dd>

Prend en charge l’écriture manuscrite personnalisée, où le module de reconnaissance améliore la reconnaissance lorsqu’il est exposé à la même écriture manuscrite dans le temps.

</dd> <dt>

<span id="RC_PrefersArbitraryAngle"></span><span id="rc_prefersarbitraryangle"></span><span id="RC_PREFERSARBITRARYANGLE"></span>**RC \_ PrefersArbitraryAngle**
</dt> <dd>

Les [**IInkAnalyzer**](iinkanalyzer.md) n’ont pas besoin de faire pivoter l’écriture manuscrite vers l’orientation horizontale avant d’envoyer l’encre au [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md).

</dd> <dt>

<span id="RC_PrefersParagraphBreaking"></span><span id="rc_prefersparagraphbreaking"></span><span id="RC_PREFERSPARAGRAPHBREAKING"></span>**RC \_ PrefersParagraphBreaking**
</dt> <dd>

Le [**IInkAnalyzer**](iinkanalyzer.md) doit envoyer des paragraphes entiers d’encre au [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md), ce qui permet au **IInkAnalysisRecognizer** d’effectuer les sauts de ligne et de mot (ou caractère).

</dd> <dt>

<span id="RC_PrefersSegmentationRecognition"></span><span id="rc_preferssegmentationrecognition"></span><span id="RC_PREFERSSEGMENTATIONRECOGNITION"></span>**RC \_ PrefersSegmentationRecognition**
</dt> <dd>

Reconnaît un seul mot ou caractère par opération de reconnaissance. Le [**IInkAnalyzer**](iinkanalyzer.md) effectue la segmentation de l’écriture manuscrite et envoie un seul segment à la fois au [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md).

</dd> </dl>

## <a name="remarks"></a>Remarques

Cette énumération permet une combinaison au niveau du bit de ses valeurs membres. Utilisez cette énumération pour rechercher un module de reconnaissance d’encre installée qui prend en charge les attributs dont vous avez besoin.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Applications de bureau XP Édition Tablet PC \[ uniquement\]<br/>                                                 |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                                     |
| En-tête<br/>                   | <dl> <dt>IACom. h (nécessite également IACom \_ i. c)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IInkAnalysisRecognizer :: GetCapabilities**](iinkanalysisrecognizer-getcapabilities.md)
</dt> <dt>

[Référence de l’analyse de l’encre](ink-analysis-reference.md)
</dt> </dl>

 

 




