---
description: Met à jour les données du paquet pour les traits spécifiés.
ms.assetid: 7fca4c39-eef2-4019-86a0-27cd0e4e7510
title: 'IInkAnalyzer :: UpdateStrokesData, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.UpdateStrokesData
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 151403a7114bca2644d0425fdba0155135ac9ed8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514629"
---
# <a name="iinkanalyzerupdatestrokesdata-method"></a>IInkAnalyzer :: UpdateStrokesData, méthode

Met à jour les données du paquet pour les traits spécifiés.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT UpdateStrokesData(
  [in] ULONG ulStrokeIdsCount,
  [in] LONG  *plStrokeIds,
  [in] ULONG ulStrokePacketDescriptionCount,
  [in] GUID  *pStrokePacketDescriptionGuids,
  [in] ULONG *pulPacketDataCountPerStroke,
  [in] LONG  *plStrokePacketData
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ulStrokeIdsCount* \[ dans\]
</dt> <dd>

Nombre de traits à mettre à jour.

</dd> <dt>

*plStrokeIds* \[ dans\]
</dt> <dd>

Tableau contenant les identificateurs de trait.

</dd> <dt>

*ulStrokePacketDescriptionCount* \[ dans\]
</dt> <dd>

Nombre de propriétés dans chaque paquet.

</dd> <dt>

*pStrokePacketDescriptionGuids* \[ dans\]
</dt> <dd>

Tableau contenant les identificateurs de propriété de paquet.

</dd> <dt>

*pulPacketDataCountPerStroke* \[ dans\]
</dt> <dd>

Tableau contenant le nombre de paquets dans chaque trait.

</dd> <dt>

*plStrokePacketData* \[ dans\]
</dt> <dd>

Tableau contenant les données du paquet pour les traits.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.

## <a name="remarks"></a>Notes

le paramètre *plStrokePacketData* contient des données de paquet pour tous les traits. Le paramètre *pStrokePacketDescriptionGuids* contient les identificateurs globaux uniques (Guid) qui décrivent les types de données de paquets inclus pour chaque point de chaque trait. Pour obtenir la liste complète des propriétés de paquet disponibles, consultez [constantes PacketPropertyGuids](packetpropertyguids-constants.md).

Seuls les traits avec les mêmes descriptions de paquets peuvent être mis à jour dans un seul appel à la **méthode IInkAnalyzer :: UpdateStrokesData**.

Cette méthode ne met pas à jour la région de modification de l’analyseur d’encre (consultez la [**méthode IInkAnalyzer :: GetDirtyRegion**](iinkanalyzer-getdirtyregion.md)).

Si un trait spécifié n’est pas associé à [**IInkAnalyzer**](iinkanalyzer.md), cette méthode ignore l’identificateur.

Si aucun des traits spécifiés n’identifie un trait associé à [**IInkAnalyzer**](iinkanalyzer.md), cette méthode retourne sans mettre à jour le **IInkAnalyzer**.

Cette méthode retourne un code d’erreur lorsque *plStrokeIds* a la **valeur null**.

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

[**IInkAnalyzer :: AddStroke, méthode**](iinkanalyzer-addstroke.md)
</dt> <dt>

[**IInkAnalyzer :: AddStrokeForLanguage, méthode**](iinkanalyzer-addstrokeforlanguage.md)
</dt> <dt>

[**IInkAnalyzer :: AddStrokeToCustomRecognizer, méthode**](iinkanalyzer-addstroketocustomrecognizer.md)
</dt> <dt>

[**IInkAnalyzer :: AddStrokes, méthode**](iinkanalyzer-addstrokes.md)
</dt> <dt>

[**IInkAnalyzer :: AddStrokesForLanguage, méthode**](iinkanalyzer-addstrokesforlanguage.md)
</dt> <dt>

[**IInkAnalyzer :: AddStrokesToCustomRecognizer, méthode**](iinkanalyzer-addstrokestocustomrecognizer.md)
</dt> <dt>

[**IInkAnalyzer :: ClearStrokeData, méthode**](iinkanalyzer-clearstrokedata.md)
</dt> <dt>

[**\_IAnalysisEvents::UpdateStrokesCache**](-ianalysisevents-updatestrokescache.md)
</dt> <dt>

[Référence de l’analyse de l’encre](ink-analysis-reference.md)
</dt> </dl>

 

 




