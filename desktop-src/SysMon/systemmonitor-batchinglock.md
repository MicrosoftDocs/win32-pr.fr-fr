---
title: SystemMonitor.Batméthode chingLock
description: Verrouille le moniteur système pour l’empêcher d’échantillonner les données de compteur à partir du nouveau compteur ou fichier journal.
ms.assetid: 6b9d683a-7a97-44a4-9eb6-6caaafe2abdd
keywords:
- Méthode BatchingLock SysMon
- Méthode BatchingLock SysMon, objet SystemMonitor
- Objet SystemMonitor SysMon, méthode BatchingLock
topic_type:
- apiref
api_name:
- SystemMonitor.BatchingLock
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b858a6920b039d911ae571d81744eb99dea4ef4f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106511569"
---
# <a name="systemmonitorbatchinglock-method"></a>SystemMonitor.Batméthode chingLock

Verrouille le moniteur système pour l’empêcher d’échantillonner les données de compteur à partir du nouveau compteur ou fichier journal.

## <a name="syntax"></a>Syntaxe


```VB
SystemMonitor.BatchingLock( _
  ByVal lock As Boolean, _
  ByVal batchReason As SysmonBatchReason _
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*verrou* \[ dans\]
</dt> <dd>

Affectez la valeur true pour verrouiller le moniteur système et l’empêcher d’échantillonner les données de compteur à partir du nouveau compteur ou fichier journal. Affectez la valeur false pour supprimer le verrou.

</dd> <dt>

*batchReason* \[ dans\]
</dt> <dd>

Identifie la source des données que vous verrouillez. Utilisez la même valeur de raison lorsque vous verrouillez et déverrouillez la ressource. Pour connaître les valeurs possibles, consultez l’énumération [**SysmonBatchReason**](/windows/win32/api/isysmon/ne-isysmon-sysmonbatchreason) .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Vous devez appeler cette méthode deux fois, une fois pour verrouiller la source (true) et une fois pour déverrouiller la source (false).

Vous ne pouvez placer qu’un seul verrou. Par exemple, si vous définissez le verrou pour SysmonBatchAddFiles et que vous effectuez ensuite un deuxième appel à l’aide de SysmonBatchAddCounters comme raison, le deuxième appel supprime le verrou placé par le premier appel.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon. ocx</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**SystemMonitor**](systemmonitor.md)
</dt> </dl>

 

 





