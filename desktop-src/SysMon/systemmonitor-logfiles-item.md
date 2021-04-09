---
title: LogFiles. Item, propriété
description: Récupère l’instance LogFileItem spécifiée de la collection.
ms.assetid: 518c1343-f659-4434-910c-958c09ffab6a
keywords:
- Propriétés de l’élément SysMon
- Propriété Item SysMon, classe LogFiles
- LogFiles, classe SysMon, Item, propriété
topic_type:
- apiref
api_name:
- LogFiles.Item
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85af003cd6c0291ec90d17906f249726dfd526f9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032592"
---
# <a name="logfilesitem-property"></a>LogFiles. Item, propriété

Récupère l’instance [**LogFileItem**](logfileitem.md) spécifiée de la collection.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```VB
Property Item( _
  ByVal index As Object _
) As LogFileItem
```



## <a name="property-value"></a>Valeur de la propriété

Instance [**LogFileItem**](logfileitem.md) qui correspond à la valeur d’index spécifiée.

## <a name="remarks"></a>Notes

Il s’agit de la propriété par défaut de l’objet [**LogFiles**](systemmonitor-logfiles.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                            |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon. ocx</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[LogFiles](logfiles.md)
</dt> <dt>

[**LogFileItem**](logfileitem.md)
</dt> <dt>

[**LogFiles**](systemmonitor-logfiles.md)
</dt> </dl>

 

 





