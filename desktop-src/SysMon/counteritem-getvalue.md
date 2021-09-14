---
title: CounterItem. GetValue, méthode
description: Récupère la dernière valeur du compteur.
ms.assetid: cf50d878-a119-42b0-bc59-b0e37ed15321
keywords:
- GetValue, méthode SysMon
- GetValue, méthode SysMon, CounterItem, classe
- CounterItem classe SysMon, GetValue, méthode
topic_type:
- apiref
api_name:
- CounterItem.GetValue
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94e40950ce4a8bf24a6a4301db133779b34ce4ec
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127008883"
---
# <a name="counteritemgetvalue-method"></a>CounterItem. GetValue, méthode

Récupère la dernière valeur du compteur.

## <a name="syntax"></a>Syntaxe


```VB
CounterItem.GetValue( _
  ByRef value As Double, _
  ByRef status As Long _
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*valeur* \[ à\]
</dt> <dd>

Dernière valeur échantillonnée du compteur.

</dd> <dt>

*État* \[ à\]
</dt> <dd>

Indique si la valeur est valide.



| Valeur                                                                                              | Signification                            |
|----------------------------------------------------------------------------------------------------|------------------------------------|
| <dl> <dt>0</dt> </dl>                       | La valeur est valide.<br/>     |
| <dl> <dt>0xC0000BBA (3221228474)</dt> </dl> | La valeur n’est pas valide.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Si la source des données de compteur provient d’un fichier journal, la valeur est la dernière valeur de compteur dans le fichier journal.

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

[**CounterItem.GetStatistics**](counteritem-getstatistics.md)
</dt> <dt>

[**CounterItem. Value**](counteritem-value.md)
</dt> </dl>

 

 





