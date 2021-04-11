---
title: SystemMonitor propriété SqlDsnName
description: Récupère ou définit le nom de source de données (DSN) ODBC.
ms.assetid: 7906204a-a208-42c7-855b-c29689b4d36a
keywords:
- Propriété SqlDsnName SysMon
- Propriété SqlDsnName SysMon, interface SystemMonitor
- Interface SystemMonitor SysMon, propriété SqlDsnName
topic_type:
- apiref
api_name:
- SystemMonitor.SqlDsnName
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 666b10ad91956adf7148e54b68f2b6db98e9a5b2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104383827"
---
# <a name="systemmonitorsqldsnname-property"></a>SystemMonitor :: SqlDsnName, propriété

Récupère ou définit le nom de source de données (DSN) ODBC.

## <a name="syntax"></a>Syntaxe


```VB
Property SqlDsnName As String
```



## <a name="property-value"></a>Valeur de la propriété

Nom de la source de données ODBC qui pointe vers une base de données qui contient les tables Perfmon appropriées. Le format est SQL : DSN.

## <a name="remarks"></a>Notes

Vous devez utiliser le composant logiciel enfichable MMC Perfmon. msc pour générer le fichier journal SQL. Les journaux de compteur se trouvent sous **journaux et alertes de performance**. Pour spécifier un journal SQL, cliquez avec le bouton droit sur le fichier journal que vous avez créé, puis sélectionnez **Propriétés** dans le menu. Sur la page de propriétés **fichiers journaux** , sélectionnez **SQL Database** dans la zone de liste déroulante **type de fichier journal** .

**Avant Windows Vista :** Vous ne pouvez pas modifier cette propriété si la valeur de [**systemmonitor. DataSourceType**](systemmonitor-datasourcetype.md) est définie sur [**DataSourceTypeConstants.sysmonSqlLog**](/windows/desktop/api/ISysmon/ne-isysmon-datasourcetypeconstants). Vous devez d’abord spécifier le nom, puis définir **systemmonitor. DataSourceType** sur **DataSourceTypeConstants.sysmonSqlLog**.

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

[**SystemMonitor.SqlLogSetName**](systemmonitor-sqllogsetname.md)
</dt> </dl>

 

 





