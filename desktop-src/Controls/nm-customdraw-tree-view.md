---
title: Code de notification NM_CUSTOMDRAW (arborescence) (commctrl. h)
description: Envoyé par un contrôle Tree-View pour signaler à sa fenêtre parente les opérations de dessin. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: eafe2427-20eb-4f3b-9407-bece897ffe16
keywords:
- NM_CUSTOMDRAW (arborescence) code de notification Windows les contrôles
topic_type:
- apiref
api_name:
- NM_CUSTOMDRAW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9571d8461b43cebe047d80933af53a0c1aa1b865ede6280b8de2a33b74a60f4c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120088839"
---
# <a name="nm_customdraw-tree-view-notification-code"></a>\_Code de notification CUSTOMDRAW nm (arborescence)

Envoyé par un contrôle Tree-View pour signaler à sa fenêtre parente les opérations de dessin. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .


```C++
NM_CUSTOMDRAW

    lpNMCustomDraw = (LPNMTVCUSTOMDRAW) lParam;
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**NMTVCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmtvcustomdraw) qui contient et reçoit des informations sur l’opération de dessin. Le membre **dwItemSpec** du membre **NMCD** de cette structure contient le handle de l’élément qui est en train d’être dessiné. Le membre **lItemlParam** du membre **NMCD** de cette structure contient le *lParam* de l’élément qui est en train d’être dessiné.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La valeur que votre application peut retourner dépend de l’étape de dessin actuelle. Le membre **dwDrawStage** de la structure [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) associée contient une valeur qui spécifie la phase de dessin. Vous devez retourner l’une des valeurs suivantes.



| Code de retour                                                                                            | Description                                                                                                                                                                                                                                                                               |
|--------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**CDRF \_ par défaut**</dt> </dl>         | Le contrôle se dessine lui-même. Elle n’envoie pas de codes [ \_ CUSTOMDRAW nm](nm-customdraw.md) supplémentaires pour ce cycle de peinture. Cela se produit lorsque **dwDrawStage** est égal à CDDS \_ prépaint.<br/>                                                                                              |
| <dl> <dt>**CDRF \_ NOTIFYITEMDRAW**</dt> </dl>    | Le contrôle notifie le parent de toutes les opérations de dessin liées aux éléments. Elle envoie les codes de notification [ \_ CUSTOMDRAW nm](nm-customdraw.md) avant et après les éléments de dessin. Cela se produit lorsque **dwDrawStage** est égal à CDDS \_ prépaint.<br/>                                                |
| <dl> <dt>**CDRF \_ NOTIFYPOSTERASE**</dt> </dl>   | Le contrôle avertit le parent après l’effacement d’un élément. Cela se produit lorsque **dwDrawStage** est égal à CDDS \_ prépaint.<br/>                                                                                                                                                                  |
| <dl> <dt>**CDRF \_ NOTIFYPOSTPAINT**</dt> </dl>   | Le contrôle notifie le parent après avoir peint un élément. Cela se produit lorsque **dwDrawStage** est égal à CDDS \_ prépaint.<br/>                                                                                                                                                                |
| <dl> <dt>**CDRF \_ NOTIFYSUBITEMDRAW**</dt> </dl> | [Version 4,71.](common-control-versions.md) Le contrôle notifie le parent lorsqu’un sous-élément de vue liste est en train d’être dessiné. Cela se produit lorsque **dwDrawStage** est égal à CDDS \_ prépaint.<br/>                                                                                                  |
| <dl> <dt>**CDRF \_ NEWFONT**</dt> </dl>           | Votre application a spécifié une nouvelle police pour l’élément. le contrôle utilise la nouvelle police. Pour plus d’informations sur la modification des polices, consultez [modification des polices et des couleurs](custom-draw.md). Cela se produit lorsque **dwDrawStage** est égal à CDDS \_ ITEMPREPAINT.<br/> |
| <dl> <dt>**CDRF \_ SKIPDEFAULT**</dt> </dl>       | Votre application a dessiné l’élément manuellement. Le contrôle ne dessine pas l’élément. Cela se produit lorsque **dwDrawStage** est égal à CDDS \_ ITEMPREPAINT.<br/>                                                                                                                                       |



 

## <a name="remarks"></a>Remarques

[Version 5,80.](common-control-versions.md) Si vous modifiez la police en retournant [**CDRF \_ NEWFONT**](cdrf-constants.md), le contrôle Tree-View peut afficher du texte tronqué. Ce comportement est nécessaire pour la compatibilité descendante avec les versions antérieures des contrôles communs. Si vous souhaitez modifier la police d’un contrôle Tree-View, vous obtiendrez de meilleurs résultats si vous envoyez un message [**CCM \_ SETVERSION**](ccm-setversion.md) avec la valeur *wParam* définie sur 5 avant d’ajouter des éléments au contrôle.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Utilisation d’un dessin personnalisé](custom-draw.md)
</dt> </dl>

 

 





