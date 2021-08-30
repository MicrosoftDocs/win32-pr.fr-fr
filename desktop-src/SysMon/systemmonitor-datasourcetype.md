---
title: SystemMonitor propriété DataSourceType
description: Récupère ou définit la source des données du compteur de performance.
ms.assetid: 53c1e9bc-dafd-445c-8d82-13a74f6c488a
keywords:
- Propriété DataSourceType SysMon
- Propriété DataSourceType SysMon, interface SystemMonitor
- Interface SystemMonitor SysMon, propriété DataSourceType
topic_type:
- apiref
api_name:
- SystemMonitor.DataSourceType
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79adffc396a581daee16218fc5d39a6480805f0f
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122481855"
---
# <a name="systemmonitordatasourcetype-property"></a>SystemMonitor ::D propriété ataSourceType

Récupère ou définit la source des données du compteur de performance.

## <a name="syntax"></a>Syntax


```VB
Property DataSourceType As DataSourceTypeConstants
```



## <a name="property-value"></a>Valeur de la propriété

Source des données du compteur de performance. Pour connaître les valeurs possibles, consultez [**DataSourceTypeConstants**](/windows/win32/api/isysmon/ne-isysmon-datasourcetypeconstants).

## <a name="exceptions"></a>Exceptions




| Type d'exception | Condition | 
|----------------|-----------|
| <strong>System.ArgumentException</strong> | Vous pouvez recevoir cette exception pour l’une des raisons suivantes :<ul><li>La valeur de la source de données spécifiée n’est pas valide.</li><li>Si la source de données est un fichier journal, SYSMON ne peut pas trouver l’un des fichiers spécifiés. La valeur de Err. Number est 0xC0000BD1.</li></ul> | 




 

## <a name="remarks"></a>Remarques

**avant Windows Vista :** Vous ne pouvez pas ajouter ou supprimer des fichiers journaux de la [**collection de fichiers journaux**](systemmonitor-logfiles.md) si la valeur de cette propriété est définie sur sysmonLogFiles. Définissez uniquement la valeur de cette propriété sur sysmonLogFiles après avoir créé ou modifié la collection de fichiers journaux.

En outre, vous ne pouvez pas modifier les propriétés [**SqlDsnName**](systemmonitor-sqldsnname.md) et [**SqlLogSetName**](systemmonitor-sqllogsetname.md) si la valeur de cette propriété ne doit pas être définie sur sysmonSqlLog. Définissez uniquement la valeur de cette propriété sur sysmonSqlLog après avoir modifié les noms du serveur et de la base de données.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                            |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon. ocx</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**SystemMonitor**](systemmonitor.md)
</dt> </dl>

 

 





