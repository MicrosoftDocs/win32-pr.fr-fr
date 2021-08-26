---
title: Code de notification NM_CUSTOMDRAW (TrackBar) (commctrl. h)
description: Envoyé par un contrôle TrackBar pour notifier à ses fenêtres parentes les opérations de dessin. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: b31d774d-e418-4162-aa2a-40fa49452d58
keywords:
- NM_CUSTOMDRAW (trackbar) code de notification Windows contrôles
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
ms.openlocfilehash: 6d863b180948676342a49615a526c8f6860905744aaf5269468807ad6dc04fa7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120109549"
---
# <a name="nm_customdraw-trackbar-notification-code"></a>\_Code de notification CUSTOMDRAW nm (TrackBar)

Envoyé par un contrôle TrackBar pour notifier à ses fenêtres parentes les opérations de dessin. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .


```C++
NM_CUSTOMDRAW

    lpNMCustomDraw = (LPNMCUSTOMDRAW) lParam;
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) qui contient des informations sur l’opération de dessin. Le membre **dwItemSpec** de cette structure contient une des valeurs de [dessin personnalisées](custom-draw-values.md) qui indique quelle partie du contrôle est dessinée. Les contrôles TrackBar insèrent les valeurs suivantes dans le membre **dwItemSpec** de cette structure pour identifier la partie du contrôle qui est dessinée :



| Valeur                                                                                                                                                      | Signification                                                                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span id="TBCD_CHANNEL"></span><span id="tbcd_channel"></span><dl> <dt>**\_canal TBCD**</dt> </dl> | Identifie le canal que le marqueur de curseur de défilement du contrôle TrackBar délimite. <br/>                           |
| <span id="TBCD_THUMB"></span><span id="tbcd_thumb"></span><dl> <dt>**\_Thumb TBCD**</dt> </dl>       | Identifie le marqueur de curseur de défilement du contrôle TrackBar. Il s’agit de la partie du contrôle qui est déplacée par l’utilisateur. <br/> |
| <span id="TBCD_TICS"></span><span id="tbcd_tics"></span><dl> <dt>**TBCD \_ tics**</dt> </dl>          | Identifie les graduations d’incrément qui apparaissent le long du bord du contrôle TrackBar. <br/>                 |



 

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La valeur que votre application peut retourner dépend de l’étape de dessin actuelle. Le membre **dwDrawStage** de la structure [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) associée contient une valeur qui spécifie la phase de dessin. Vous devez retourner l’une des valeurs suivantes.



| Code de retour                                                                                            | Description                                                                                                                                                                                                                                                                               |
|--------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**CDRF \_ par défaut**</dt> </dl>         | Le contrôle se dessine lui-même. Il n’enverra pas de codes de notification [ \_ CUSTOMDRAW nm](nm-customdraw.md) supplémentaires pour ce cycle de peinture. Cela se produit lorsque **dwDrawStage** est égal à CDDS \_ prépaint.<br/>                                                                             |
| <dl> <dt>**CDRF \_ NOTIFYITEMDRAW**</dt> </dl>    | Le contrôle notifie le parent de toutes les opérations de dessin liées aux éléments. Il envoie les codes de notification [ \_ CUSTOMDRAW nm](nm-customdraw.md) avant et après les éléments de dessin. Cela se produit lorsque **dwDrawStage** est égal à CDDS \_ prépaint.<br/>                                         |
| <dl> <dt>**CDRF \_ NOTIFYPOSTERASE**</dt> </dl>   | Le contrôle notifie le parent après l’effacement d’un élément. Cela se produit lorsque **dwDrawStage** est égal à CDDS \_ prépaint.<br/>                                                                                                                                                              |
| <dl> <dt>**CDRF \_ NOTIFYPOSTPAINT**</dt> </dl>   | Le contrôle notifie le parent après avoir peint un élément. Cela se produit lorsque **dwDrawStage** est égal à CDDS \_ prépaint.<br/>                                                                                                                                                             |
| <dl> <dt>**CDRF \_ NOTIFYSUBITEMDRAW**</dt> </dl> | [Version 4,71](common-control-versions.md). Le contrôle notifie le parent lorsqu’un sous-élément de vue liste est en cours de dessin. Cela se produit lorsque **dwDrawStage** est égal à CDDS \_ prépaint.<br/>                                                                                               |
| <dl> <dt>**CDRF \_ NEWFONT**</dt> </dl>           | Votre application a spécifié une nouvelle police pour l’élément. le contrôle utilise la nouvelle police. Pour plus d’informations sur la modification des polices, consultez [modification des polices et des couleurs](custom-draw.md). Cela se produit lorsque **dwDrawStage** est égal à CDDS \_ ITEMPREPAINT.<br/> |
| <dl> <dt>**CDRF \_ SKIPDEFAULT**</dt> </dl>       | Votre application a dessiné l’élément manuellement. Le contrôle ne dessine pas l’élément. Cela se produit lorsque **dwDrawStage** est égal à CDDS \_ ITEMPREPAINT.<br/>                                                                                                                                       |



 

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

 

 





