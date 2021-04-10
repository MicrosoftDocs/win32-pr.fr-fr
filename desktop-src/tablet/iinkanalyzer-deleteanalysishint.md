---
description: Supprime un indicateur d’analyse de IInkAnalyzer.
ms.assetid: ba5498d4-d31c-4b3f-9004-0448e18d4835
title: IInkAnalyzer ::D méthode eleteAnalysisHint (IACom. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.DeleteAnalysisHint
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: f84f718701abd5bc76b55427aab9df072f758c3a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113351"
---
# <a name="iinkanalyzerdeleteanalysishint-method"></a>IInkAnalyzer ::D méthode eleteAnalysisHint

Supprime un indicateur d’analyse de [**IInkAnalyzer**](iinkanalyzer.md).

## <a name="syntax"></a>Syntaxe


```C++
HRESULT DeleteAnalysisHint(
  [in] IContextNode *pHintToDelete
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pHintToDelete* \[ dans\]
</dt> <dd>

Indicateur d’analyse de [**IInkAnalyzer**](iinkanalyzer.md).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.

## <a name="remarks"></a>Notes

La suppression d’un indicateur d’analyse ne marque pas la zone de l’indicateur pour la réanalyse. Pour marquer la zone dans l’indicateur pour la réanalyse, utilisez la [**méthode IInkAnalyzer :: SetDirtyRegion**](iinkanalyzer-setdirtyregion.md) pour définir la région de modification sur l’Union de la région et de la zone de modification actuelles de l’indicateur d’analyse.

L’indicateur est supprimé de l’analyseur. Toutefois, le [**IContextNode**](icontextnode.md) lui-même n’est pas supprimé.

Cette méthode retourne un code d’erreur quand *pHintToDelete* est un [**IContextNode**](icontextnode.md) qui n’est pas de type AnalysisHint (consultez [**IContextNode :: GetType**](icontextnode-gettype.md)).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]<br/>                                                 |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                                     |
| En-tête<br/>                   | <dl> <dt>IACom. h (nécessite également IACom \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IInkAnalyzer**](iinkanalyzer.md)
</dt> <dt>

[**IInkAnalyzer :: CreateAnalysisHint, méthode**](iinkanalyzer-createanalysishint.md)
</dt> <dt>

[**IInkAnalyzer :: GetAnalysisHints, méthode**](iinkanalyzer-getanalysishints.md)
</dt> <dt>

[**IInkAnalyzer :: GetAnalysisHintsByName, méthode**](iinkanalyzer-getanalysishintsbyname.md)
</dt> <dt>

[Référence de l’analyse de l’encre](ink-analysis-reference.md)
</dt> </dl>

 

 




