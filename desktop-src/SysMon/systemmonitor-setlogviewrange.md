---
title: Méthode SystemMonitor. SetLogViewRange
description: Définit la date de début utilisée pour récupérer les valeurs de compteur à partir des fichiers journaux.
ms.assetid: ced641d0-cf71-4826-8ff0-c05f20a71aaa
keywords:
- Méthode SetLogViewRange SysMon
- Méthode SetLogViewRange SysMon, objet SystemMonitor
- Objet SystemMonitor SysMon, méthode SetLogViewRange
topic_type:
- apiref
api_name:
- SystemMonitor.SetLogViewRange
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 534a7dc3bf711832ec99e4202f4f56cc347f336b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384240"
---
# <a name="systemmonitorsetlogviewrange-method"></a>Méthode SystemMonitor. SetLogViewRange

Définit la date de début utilisée pour récupérer les valeurs de compteur à partir des fichiers journaux.

## <a name="syntax"></a>Syntaxe


```VB
SystemMonitor.SetLogViewRange( _
  ByVal StartTime As Date, _
  ByVal StopTime As Date _
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*StartTime* \[ dans\]
</dt> <dd>

Date de début utilisée pour récupérer les valeurs de compteur à partir des fichiers journaux.

</dd> <dt>

*StopTime* \[ dans\]
</dt> <dd>

Date de fin utilisée pour récupérer les valeurs de compteur à partir des fichiers journaux.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Notes

SYSMON récupère les valeurs de compteur à partir des fichiers journaux qui se trouvent dans les dates de début et de fin, inclus.

Si vous ne spécifiez pas de date de début ou si vous définissez la date de début sur une valeur de date qui se trouve en dehors de la plage de valeurs de date trouvée dans les fichiers journaux, SYSMON remplace la valeur par la valeur de date la plus ancienne trouvée dans les fichiers journaux. Si la valeur de début est supérieure à la valeur d’arrêt, SYSMON remplace la valeur de début par la même valeur que la valeur d’arrêt.

Si vous ne spécifiez pas de valeur d’arrêt ou si vous définissez la valeur d’arrêt sur une valeur de date postérieure à la dernière date contenue dans le fichier journal, SYSMON remplace la valeur par la valeur de date la plus récente trouvée dans les fichiers journaux. Si la valeur d’arrêt est inférieure à la valeur d’arrêt, SYSMON change la valeur d’arrêt pour qu’elle soit de la même valeur que la valeur de début.

Si vous spécifiez une date de début et de fin, vous devez spécifier les dates avant de définir [**systemmonitor. DataSourceType**](systemmonitor-datasourcetype.md). Si vous définissez les dates après avoir défini **systemmonitor. DataSourceType**, seule la première valeur de compteur est récupérée à partir du fichier journal.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon. ocx</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**SystemMonitor**](systemmonitor.md)
</dt> <dt>

[**SystemMonitor.GetLogViewRange**](systemmonitor-getlogviewrange.md)
</dt> </dl>

 

 





