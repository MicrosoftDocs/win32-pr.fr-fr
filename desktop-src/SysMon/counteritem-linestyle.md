---
title: CounterItem. LineStyle, propriété
description: Récupère ou définit le style de ligne utilisé pour représenter sous forme de graphique la valeur de compteur.
ms.assetid: 5801f0f8-37e5-4b15-a13f-24c71fea550d
keywords:
- Propriété LineStyle SysMon
- Propriété LineStyle SysMon, classe CounterItem
- Classe CounterItem SysMon, propriété LineStyle
topic_type:
- apiref
api_name:
- CounterItem.LineStyle
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bbff1dd78c6fd65d72c28fe8f13f7bbf5603c75f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942089"
---
# <a name="counteritemlinestyle-property"></a>CounterItem. LineStyle, propriété

Récupère ou définit le style de ligne utilisé pour représenter sous forme de graphique la valeur de compteur.

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntaxe


```VB
Property LineStyle As Long
```



## <a name="property-value"></a>Valeur de la propriété

Style de ligne utilisé pour représenter sous forme de graphique la valeur de compteur. Les valeurs correspondent aux constantes système répertoriées dans le tableau suivant.



| Valeur                                                                                                                                                                                                                                                                                                                                                                               | Signification                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <span id="System.Drawing.Drawing2D.DashStyle.Solid"></span><span id="system.drawing.drawing2d.dashstyle.solid"></span><span id="SYSTEM.DRAWING.DRAWING2D.DASHSTYLE.SOLID"></span><dl> <dt>**System. Drawing. Drawing2D. DashStyle. Solid**</dt> <dt>0</dt> </dl>                     | Ligne pleine. Il s’agit de la valeur par défaut.<br/>                |
| <span id="System.Drawing.Drawing2D.DashStyle.Dash"></span><span id="system.drawing.drawing2d.dashstyle.dash"></span><span id="SYSTEM.DRAWING.DRAWING2D.DASHSTYLE.DASH"></span><dl> <dt>**System. Drawing. Drawing2D. DashStyle. Dash**</dt> <dt>1</dt> </dl>                         | Ligne en pointillés avec des segments longs et des espaces étroits.<br/>     |
| <span id="System.Drawing.Drawing2D.DashStyle.Dot"></span><span id="system.drawing.drawing2d.dashstyle.dot"></span><span id="SYSTEM.DRAWING.DRAWING2D.DASHSTYLE.DOT"></span><dl> <dt>**System. Drawing. Drawing2D. DashStyle. dot**</dt> <dt>2</dt> </dl>                             | Ligne en pointillés avec des segments et des espaces uniformes.<br/>         |
| <span id="System.Drawing.Drawing2D.DashStyle.DashDot"></span><span id="system.drawing.drawing2d.dashstyle.dashdot"></span><span id="SYSTEM.DRAWING.DRAWING2D.DASHSTYLE.DASHDOT"></span><dl> <dt>**System. Drawing. Drawing2D. DashStyle. tiret point**</dt> <dt>3</dt> </dl>             | Ligne en pointillés avec des segments courts et longs.<br/> |
| <span id="System.Drawing.Drawing2D.DashStyle.DashDotDot"></span><span id="system.drawing.drawing2d.dashstyle.dashdotdot"></span><span id="SYSTEM.DRAWING.DRAWING2D.DASHSTYLE.DASHDOTDOT"></span><dl> <dt>**System. Drawing. Drawing2D. DashStyle. tiret point point**</dt> <dt>4</dt> </dl> | Ligne en pointillés avec des tirets et des points doubles en alternance.<br/>  |



 

## <a name="exceptions"></a>Exceptions



| Type d'exception               | Condition                              |
|------------------------------|----------------------------------------|
| **System.ArgumentException** | Le style de ligne spécifié n’est pas valide. |



 

## <a name="remarks"></a>Notes

Pour spécifier une valeur autre que DashStyle. Solid, [**CounterItem. Width**](counteritem-width.md) doit avoir la valeur 1. Si la largeur est supérieure à 1, SYSMON ignore le style de ligne spécifié et utilise DashStyle. Solid.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                            |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon. ocx</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CounterItem**](counteritem.md)
</dt> </dl>

 

 





