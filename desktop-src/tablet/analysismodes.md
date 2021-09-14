---
description: Spécifie la manière dont le IInkAnalyzer effectue l’analyse de l’encre.
ms.assetid: bc526445-0c9c-4c53-8b02-32cf758266e6
title: Énumération AnalysisModes (IACom. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AnalysisModes
api_type:
- HeaderDef
api_location:
- IACom.h
ms.openlocfilehash: b9fdebd3ef3cd505b49ff6c82f7609bc339af0a4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127226660"
---
# <a name="analysismodes-enumeration"></a>Énumération AnalysisModes

Spécifie la manière dont le [**IInkAnalyzer**](iinkanalyzer.md) effectue l’analyse de l’encre.

## <a name="syntax"></a>Syntaxe


```C++
typedef enum AnalysisModes { 
  AnalysisModes_None                     = 0x0000,
  AnalysisModes_AutomaticReconciliation  = 0x0002,
  AnalysisModes_StrokeCacheAutoCleanup   = 0x0004,
  AnalysisModes_PersonalizationEnabled   = 0x0008,
  AnalysisModes_Default                  = 0x000d
} AnalysisModes;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="AnalysisModes_None"></span><span id="analysismodes_none"></span><span id="ANALYSISMODES_NONE"></span>**AnalysisModes \_ aucun**
</dt> <dd>

Aucun mode n’est spécifié.

</dd> <dt>

<span id="AnalysisModes_AutomaticReconciliation"></span><span id="analysismodes_automaticreconciliation"></span><span id="ANALYSISMODES_AUTOMATICRECONCILIATION"></span>**AnalysisModes \_ AutomaticReconciliation**
</dt> <dd>

Indique si le [**IInkAnalyzer**](iinkanalyzer.md) démarre automatiquement l’opération de rapprochement dès que les résultats intermédiaires ou finaux sont prêts.

Si ce mode est activé, l’événement [**\_ IAnalysisEvents :: ReadyToReconcile**](-ianalysisevents-readytoreconcile.md) n’est pas déclenché. Si ce mode est désactivé, l’événement **\_ IAnalysisEvents :: ReadyToReconcile** est déclenché.

</dd> <dt>

<span id="AnalysisModes_StrokeCacheAutoCleanup"></span><span id="analysismodes_strokecacheautocleanup"></span><span id="ANALYSISMODES_STROKECACHEAUTOCLEANUP"></span>**AnalysisModes \_ StrokeCacheAutoCleanup**
</dt> <dd>

Indique si le [**IInkAnalyzer**](iinkanalyzer.md) efface automatiquement les traits inutiles du cache de trait avant d’effectuer l’analyse.

Si ce mode est activé, le [**IInkAnalyzer**](iinkanalyzer.md) efface les données de trait avant d’effectuer l’analyse. Votre code doit également gérer l’événement [**\_ IAnalysisEvents :: UpdateStrokesCache**](-ianalysisevents-updatestrokescache.md) . Si l’événement **\_ IAnalysisEvents :: UpdateStrokesCache** n’est pas géré, une exception est levée. Cette vérification s’effectue à la fois au niveau des phases Analyze (ou BackgroundAnalyze) et de la réconciliation.

Si ce mode est désactivé, [**IInkAnalyzer**](iinkanalyzer.md) n’efface pas les données du trait. Pour effacer les données de trait, appelez la [**méthode IInkAnalyzer :: ClearStrokeData**](iinkanalyzer-clearstrokedata.md). Si ce mode est désactivé, l’événement [**\_ IAnalysisEvents :: UpdateStrokesCache**](-ianalysisevents-updatestrokescache.md) est déclenché afin que le **IInkAnalyzer** puisse récupérer les données de trait les plus récentes pour tous les traits dont le cache a été effacé. Si le cache de trait est effacé, mais que l’événement **\_ IAnalysisEvents :: UpdateStrokesCache** n’est pas géré, une exception est levée.

</dd> <dt>

<span id="AnalysisModes_PersonalizationEnabled"></span><span id="analysismodes_personalizationenabled"></span><span id="ANALYSISMODES_PERSONALIZATIONENABLED"></span>**AnalysisModes \_ PersonalizationEnabled**
</dt> <dd>

La personnalisation de la reconnaissance de l’écriture manuscrite est activée.

</dd> <dt>

<span id="AnalysisModes_Default"></span><span id="analysismodes_default"></span><span id="ANALYSISMODES_DEFAULT"></span>**AnalysisModes \_ par défaut**
</dt> <dd>

Tous les modes sont activés.

</dd> </dl>

## <a name="remarks"></a>Notes

Cette énumération permet une combinaison au niveau du bit de ses valeurs membres.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Applications de bureau XP Édition Tablet PC \[ uniquement\]<br/>                                                 |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                                     |
| En-tête<br/>                   | <dl> <dt>IACom. h (nécessite également IACom \_ i. c)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IInkAnalyzer :: GetAnalysisModes, méthode**](iinkanalyzer-getanalysismodes.md)
</dt> <dt>

[**IInkAnalyzer :: SetAnalysisModes, méthode**](iinkanalyzer-setanalysismodes.md)
</dt> <dt>

[**\_IAnalysisEvents::IntermediateResults**](-ianalysisevents-intermediateresults.md)
</dt> <dt>

[**\_IAnalysisEvents::ReadyToReconcile**](-ianalysisevents-readytoreconcile.md)
</dt> <dt>

[**\_IAnalysisEvents::UpdateStrokesCache**](-ianalysisevents-updatestrokescache.md)
</dt> <dt>

[Référence de l’analyse de l’encre](ink-analysis-reference.md)
</dt> </dl>

 

 




