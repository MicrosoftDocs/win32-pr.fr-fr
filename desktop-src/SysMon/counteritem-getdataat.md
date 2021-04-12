---
title: Méthode CounterItem. GetDataAt
description: Récupère la valeur de compteur spécifiée à partir d’un point spécifique du graphique.
ms.assetid: e8484301-4575-41ee-9c6d-a454eca0e82d
keywords:
- Méthode GetDataAt SysMon
- Méthode GetDataAt SysMon, objet CounterItem
- Objet CounterItem SysMon, méthode GetDataAt
topic_type:
- apiref
api_name:
- CounterItem.GetDataAt
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 354d8242e6cb765980878a7783805416bb1a1009
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508670"
---
# <a name="counteritemgetdataat-method"></a>Méthode CounterItem. GetDataAt

Récupère la valeur de compteur spécifiée à partir d’un point spécifique du graphique.

## <a name="syntax"></a>Syntaxe


```VB
CounterItem.GetDataAt( _
  ByVal index As Long, _
  ByVal which As SysmonDataType, _
  ByRef variant As Object _
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*index* \[ dans\]
</dt> <dd>

Index de base zéro du point de graphique dont vous souhaitez récupérer la valeur. Les valeurs valides sont comprises entre 0 et ([**systemmonitor. DataPointCount**](systemmonitor-datapointcount.md) -1).

</dd> <dt>

*qui* \[ dans\]
</dt> <dd>

Type de valeur de compteur à récupérer, par exemple, la valeur moyenne du compteur tel qu’il s’affiche dans la fenêtre du graphique. Pour connaître les valeurs possibles, consultez [**SysmonDataType**](/windows/win32/api/isysmon/ne-isysmon-sysmondatatype).

</dd> <dt>

*variante* \[ à\]
</dt> <dd>

Valeur de compteur qui a été récupérée.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Utilisez cette méthode uniquement si

-   [**Systemmonitor. DisplayType**](systemmonitor-displaytype.md) a la valeur sysmonLineGraph
-   [**Systemmonitor. DataSourceType**](systemmonitor-datasourcetype.md) est défini sur SysmonLogFiles ou sysmonSqlLog

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon. ocx</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CounterItem**](counteritem.md)
</dt> <dt>

[**CounterItem.GetStatistics**](counteritem-getstatistics.md)
</dt> <dt>

[**CounterItem. GetValue**](counteritem-getvalue.md)
</dt> </dl>

 

 





