---
title: Méthode SystemMonitor. GetLogViewRange
description: Récupère la date de début utilisée pour récupérer les valeurs de compteur à partir des fichiers journaux.
ms.assetid: c74c3a5b-d2ec-43d8-b715-e399f42e8ae5
keywords:
- Méthode GetLogViewRange SysMon
- Méthode GetLogViewRange SysMon, objet SystemMonitor
- Objet SystemMonitor SysMon, méthode GetLogViewRange
topic_type:
- apiref
api_name:
- SystemMonitor.GetLogViewRange
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d494a5861ff9c0d2c076abe2bdad749d21653500
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508589"
---
# <a name="systemmonitorgetlogviewrange-method"></a>Méthode SystemMonitor. GetLogViewRange

Récupère la date de début utilisée pour récupérer les valeurs de compteur à partir des fichiers journaux.

## <a name="syntax"></a>Syntaxe


```VB
SystemMonitor.GetLogViewRange( _
  ByRef StartTime As Date, _
  ByRef StopTime As Date _
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*StartTime* \[ à\]
</dt> <dd>

Date de début utilisée pour récupérer les valeurs de compteur à partir des fichiers journaux.

</dd> <dt>

*StopTime* \[ à\]
</dt> <dd>

Date de fin utilisée pour récupérer les valeurs de compteur à partir des fichiers journaux.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Notes

SYSMON récupère les valeurs de compteur à partir des fichiers journaux qui se trouvent dans les dates de début et de fin, inclus.

L’utilisation de cette méthode revient à accéder aux propriétés [**systemmonitor. LogViewStart**](systemmonitor-logviewstart.md) et [**systemmonitor. LogViewStop**](systemmonitor-logviewstop.md) .

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

[**SystemMonitor.SetLogViewRange**](systemmonitor-setlogviewrange.md)
</dt> </dl>

 

 





