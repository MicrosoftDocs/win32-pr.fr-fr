---
title: SystemMonitor. Highlight, propriété
description: Récupère ou définit une valeur indiquant si les valeurs des compteurs sélectionnés sont mises en surbrillance dans le graphique.
ms.assetid: 5342b81f-71bb-4564-b520-1e91d3002c5b
keywords:
- Mettre en surbrillance la propriété SysMon
- Mettre en surbrillance la propriété SysMon, classe SystemMonitor
- SystemMonitor classe SysMon, Highlight, propriété
topic_type:
- apiref
api_name:
- SystemMonitor.Highlight
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3009501123673175c64d88acd838f94aa7e332aa
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127324717"
---
# <a name="systemmonitorhighlight-property"></a>SystemMonitor. Highlight, propriété

Récupère ou définit une valeur indiquant si les valeurs des compteurs sélectionnés sont mises en surbrillance dans le graphique.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```VB
Property Highlight As Boolean
```



## <a name="property-value"></a>Valeur de la propriété

True indique que les valeurs des compteurs sélectionnés sont mises en surbrillance dans le graphique ; Sinon, false. La valeur par défaut est False.

## <a name="remarks"></a>Notes

Pour sélectionner un ou plusieurs compteurs, vous pouvez définir [**CounterItem. Selected**](counteritem-selected.md) sur true ou l’utilisateur peut sélectionner les compteurs dans la liste des compteurs affichée dans la légende.

**avant Windows Vista :** Vous ne pouvez pas sélectionner des compteurs par programmation et l’utilisateur ne peut sélectionner qu’un seul compteur dans la liste des compteurs affichée dans la légende.

La mise en surbrillance peut être en noir ou en blanc, en fonction de la valeur de la propriété [**BackColor**](systemmonitor-backcolor.md) . La mise en surbrillance est automatiquement définie sur la couleur qui fournira un contraste suffisant entre la couleur de surbrillance et la couleur d’arrière-plan.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                            |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon. ocx</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**SystemMonitor**](systemmonitor.md)
</dt> <dt>

[**CounterItem. Selected**](counteritem-selected.md)
</dt> </dl>

 

 





