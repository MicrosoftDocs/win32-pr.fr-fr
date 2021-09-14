---
title: Méthode CounterItem. GetStatistics
description: Récupère les valeurs moyennes, maximales et minimales du compteur.
ms.assetid: fb55d68b-1dbe-48b1-88c8-51f33048ec24
keywords:
- Méthode GetStatistics SysMon
- Méthode GetStatistics SysMon, classe CounterItem
- CounterItem classe SysMon, méthode GetStatistics
topic_type:
- apiref
api_name:
- CounterItem.GetStatistics
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c993ed8b9bb39a4d8bb3ff18663f2d884ece156
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127008885"
---
# <a name="counteritemgetstatistics-method"></a>Méthode CounterItem. GetStatistics

Récupère les valeurs moyennes, maximales et minimales du compteur.

## <a name="syntax"></a>Syntaxe


```VB
CounterItem.GetStatistics( _
  ByRef max As Double, _
  ByRef min As Double, _
  ByRef average As Double, _
  ByRef status As Long _
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*maximum* \[ à\]
</dt> <dd>

Valeur maximale du compteur.

</dd> <dt>

*min* \[ . à\]
</dt> <dd>

Valeur minimale du compteur.

</dd> <dt>

*moyenne* \[ à\]
</dt> <dd>

Valeur moyenne du compteur.

</dd> <dt>

*État* \[ à\]
</dt> <dd>

Indique si les valeurs sont valides.



| Valeur                                                                                              | Signification                              |
|----------------------------------------------------------------------------------------------------|--------------------------------------|
| <dl> <dt>0</dt> </dl>                       | Les valeurs sont valides.<br/>     |
| <dl> <dt>0xC0000BBA (3221228474)</dt> </dl> | Les valeurs ne sont pas valides.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

Seules les valeurs de compteur qui sont visibles dans la fenêtre graphique sont utilisées pour calculer les valeurs statistiques.

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

[**CounterItem.GetDataAt**](counteritem-getdataat.md)
</dt> <dt>

[**CounterItem. GetValue**](counteritem-getvalue.md)
</dt> </dl>

 

 





