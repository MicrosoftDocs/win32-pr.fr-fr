---
title: Méthode SystemMonitor CollectSample
description: Échantillonne une valeur pour chaque compteur dans l’objet compteurs.
ms.assetid: 4c91c759-597f-4aa8-aa77-eb181616e8b0
keywords:
- Méthode CollectSample SysMon
- Méthode CollectSample SysMon, interface SystemMonitor
- Interface SystemMonitor SysMon, méthode CollectSample
topic_type:
- apiref
api_name:
- SystemMonitor.CollectSample
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e1c269d044c17a2ec1322fa969e0c86f468a901
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465562"
---
# <a name="systemmonitorcollectsample-method"></a>SystemMonitor :: CollectSample, méthode

Échantillonne une valeur pour chaque compteur dans l’objet [**compteurs**](counters.md) .

## <a name="syntax"></a>Syntaxe


```VB
Sub CollectSample()
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Appelez **CollectSample** uniquement si [**ManualUpdate**](systemmonitor-manualupdate.md) a la valeur true et si vous échantillonnez des valeurs de compteur à partir de l’activité actuelle de l’ordinateur, n’utilisez pas cette méthode lors de l’échantillonnage à partir d’un fichier journal. Le graphique ou le rapport est mis à jour avec la nouvelle valeur. Notez que certains types de graphiques ont besoin de deux échantillons pour représenter graphiquement les données, par exemple, le graphique en courbes.

Pour recevoir une notification lorsque l’exemple a été collecté, implémentez l’événement [**OnSampleCollected**](-systemmonitor-onsamplecollected.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                            |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon. ocx</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Counters**](counters.md)
</dt> <dt>

[**SystemMonitor**](systemmonitor.md)
</dt> </dl>

 

 





