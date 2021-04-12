---
title: Compteurs. Item, propriété
description: Récupère l’instance CounterItem spécifiée de la collection.
ms.assetid: bf503371-c8bd-4e0d-ab8d-58de3f8fac5f
keywords:
- Propriétés de l’élément SysMon
- Propriété d’élément SysMon, classe Counters
- Compteurs classe SysMon, propriété Item
topic_type:
- apiref
api_name:
- Counters.Item
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 251a645f0a4ceacdbfb4e2ab7e650f41e44dd508
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464714"
---
# <a name="countersitem-property"></a>Compteurs. Item, propriété

Récupère l’instance [**CounterItem**](counteritem.md) spécifiée de la collection.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```VB
Property Item( _
  ByVal index As Object _
) As CounterItem
```



## <a name="property-value"></a>Valeur de la propriété

Instance [**CounterItem**](counteritem.md) qui correspond à la valeur d’index spécifiée.

## <a name="exceptions"></a>Exceptions



| Type d'exception                                  | Condition                         |
|-------------------------------------------------|-----------------------------------|
| **System. Runtime. InteropServices. COMException** | L’index spécifié n’est pas valide. |



 

## <a name="remarks"></a>Notes

Il s’agit de la propriété par défaut de l’objet [**Counters**](counters.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                            |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon. ocx</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CounterItem**](counteritem.md)
</dt> <dt>

[**Counters**](counters.md)
</dt> </dl>

 

 





