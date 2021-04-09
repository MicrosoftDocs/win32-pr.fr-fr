---
title: SystemMonitor propriété SqlLogSetName
description: Récupère ou définit le nom convivial du jeu de journaux.
ms.assetid: a4593743-6b70-4f70-8e91-3324a808d97b
keywords:
- Propriété SqlLogSetName SysMon
- Propriété SqlLogSetName SysMon, interface SystemMonitor
- Interface SystemMonitor SysMon, propriété SqlLogSetName
topic_type:
- apiref
api_name:
- SystemMonitor.SqlLogSetName
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be20ccc561eb3e9292b4a95dcc654ed7bac00ba7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032315"
---
# <a name="systemmonitorsqllogsetname-property"></a>SystemMonitor :: SqlLogSetName, propriété

Récupère ou définit le nom convivial du jeu de journaux.

## <a name="syntax"></a>Syntaxe


```VB
Property SqlLogSetName As String
```



## <a name="property-value"></a>Valeur de la propriété

Nom convivial du jeu de journaux, qui correspond à un fichier journal unique contenant des données binaires ou de texte dans la base de données SQL.

## <a name="remarks"></a>Notes

**Avant Windows Vista :** Vous ne pouvez pas modifier cette propriété si la valeur de [**systemmonitor. DataSourceType**](systemmonitor-datasourcetype.md) est définie sur sysmonSqlLog.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                            |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon. ocx</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**SystemMonitor**](systemmonitor.md)
</dt> <dt>

[**SystemMonitor.SqlDsnName**](systemmonitor-sqllogsetname.md)
</dt> </dl>

 

 





