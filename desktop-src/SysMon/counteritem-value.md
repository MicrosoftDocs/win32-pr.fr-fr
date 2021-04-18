---
title: CounterItem. Value (propriété)
description: Récupère la dernière valeur échantillonnée du compteur.
ms.assetid: c5aeaa00-e185-484d-8a7a-d45a21690e20
keywords:
- Propriété valeur SysMon
- Propriété Value SysMon, classe CounterItem
- Classe CounterItem SysMon, propriété Value
topic_type:
- apiref
api_name:
- CounterItem.Value
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62c0d6bd9e1751e34c980bc95f790314017eeb49
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106527160"
---
# <a name="counteritemvalue-property"></a>CounterItem. Value (propriété)

Récupère la dernière valeur échantillonnée du compteur.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```VB
Property Value As Double
```



## <a name="property-value"></a>Valeur de la propriété

Dernière valeur échantillonnée du compteur. La valeur est-1 si une erreur se produit.

## <a name="remarks"></a>Notes

Il s’agit de la propriété par défaut de l’objet [**CounterItem**](counteritem.md) .

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

[**CounterItem. GetValue**](counteritem-getvalue.md)
</dt> </dl>

 

 





