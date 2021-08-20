---
title: Compteurs. Remove, méthode
description: Supprime une instance CounterItem de la collection.
ms.assetid: 88e5907a-8c8f-4a24-9c5d-0c592f61dac0
keywords:
- Supprimer la méthode SysMon
- Remove, méthode SysMon, classe Counters
- Compteurs Class SysMon, Remove, méthode
topic_type:
- apiref
api_name:
- Counters.Remove
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 77226d87c49fdfd2e9d8d26c2699bcb4606de29a21bf2bd20a12ad0b70d6daa4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117956651"
---
# <a name="countersremove-method"></a>Compteurs. Remove, méthode

Supprime une instance [**CounterItem**](counteritem.md) de la collection.

## <a name="syntax"></a>Syntaxe


```VB
Counters.Remove( _
  ByVal index As Object _
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*index* \[ dans\]
</dt> <dd>

Index de l’objet [**CounterItem**](counteritem.md) à supprimer de la collection. L’index est de base un.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="exceptions"></a>Exceptions



| Type d'exception                                  | Condition                                                      |
|-------------------------------------------------|----------------------------------------------------------------|
| **System. Runtime. InteropServices. COMException** | L’index spécifié n’est pas valide. La valeur de Err. Number est ???. |



 

## <a name="remarks"></a>Remarques

Pour supprimer tous les compteurs de la collection, vous pouvez appeler [**systemmonitor. Reset**](systemmonitor-reset.md).

## <a name="requirements"></a>Conditions requises



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                            |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon. ocx</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Counters**](counters.md)
</dt> <dt>

[**SystemMonitor. Reset**](systemmonitor-reset.md)
</dt> </dl>

 

 





