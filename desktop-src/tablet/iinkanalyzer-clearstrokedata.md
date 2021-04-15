---
description: Efface les données de paquets de trait du IInkAnalyzer.
ms.assetid: c87a1e73-5e3f-4d27-93e9-e30d9ec5d9e3
title: 'IInkAnalyzer :: ClearStrokeData, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.ClearStrokeData
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 823ceaa825b454af851fab43e233526285445c80
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104485081"
---
# <a name="iinkanalyzerclearstrokedata-method"></a>IInkAnalyzer :: ClearStrokeData, méthode

Efface les données de paquets de trait du [**IInkAnalyzer**](iinkanalyzer.md).

## <a name="syntax"></a>Syntaxe


```C++
HRESULT ClearStrokeData(
  [in] LONG lStrokeId
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lStrokeId* \[ dans\]
</dt> <dd>

Identificateur du trait pour lequel les données du paquet sont effacées.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.

## <a name="remarks"></a>Notes

Utilisez cette méthode lorsque les données de paquet d’un trait sont modifiées, par exemple lorsqu’un trait est déplacé ou transformé autrement. [**IInkAnalyzer**](iinkanalyzer.md) déclenche l’événement [**\_ IAnalysisEvents :: UpdateStrokesCache**](-ianalysisevents-updatestrokescache.md) lorsqu’il a besoin de tracer des données de paquets à partir d’un trait pour lequel les données du paquet ont été effacées.

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

[**IInkAnalyzer :: UpdateStrokesData, méthode**](iinkanalyzer-updatestrokesdata.md)
</dt> <dt>

[Référence de l’analyse de l’encre](ink-analysis-reference.md)
</dt> </dl>

 

 




