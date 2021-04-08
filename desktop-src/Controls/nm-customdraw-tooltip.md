---
title: Code de notification NM_CUSTOMDRAW (info-bulle) (commctrl. h)
description: Envoyé par un contrôle ToolTip pour signaler à sa fenêtre parente les opérations de dessin. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 82939901-baed-452b-85bf-3c0c01e1f5df
keywords:
- Contrôles Windows de code de notification NM_CUSTOMDRAW (info-bulle)
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
ms.openlocfilehash: 9ce1047f63c8580051f7d57abf3308bde37238a6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743980"
---
# <a name="nm_customdraw-tooltip-notification-code"></a>\_Code de notification CUSTOMDRAW nm (info-bulle)

Envoyé par un contrôle ToolTip pour signaler à sa fenêtre parente les opérations de dessin. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .


```C++
NM_CUSTOMDRAW

    lpNMCustomDraw = (LPNMTTCUSTOMDRAW) lParam;
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**NMTTCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmttcustomdraw) qui contient des informations sur l’opération de dessin.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La valeur que votre application peut retourner dépend de l’étape de dessin actuelle. Le membre **dwDrawStage** de la structure [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) associée contient une valeur qui spécifie la phase de dessin. Vous devez retourner l’une des valeurs suivantes.



| Code de retour                                                                                            | Description                                                                                                                                                                                                                                                                                  |
|--------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**CDRF \_ par défaut**</dt> </dl>         | Le contrôle se dessine lui-même. Il n’enverra pas de codes de notification [ \_ CUSTOMDRAW nm](nm-customdraw.md) supplémentaires pour ce cycle de peinture. Cela se produit lorsque **dwDrawStage** est égal à CDDS \_ prépaint.<br/>                                                                                |
| <dl> <dt>**CDRF \_ NOTIFYITEMDRAW**</dt> </dl>    | Le contrôle notifie le parent de toutes les opérations de dessin liées aux éléments. Il envoie les codes de notification [ \_ CUSTOMDRAW nm](nm-customdraw.md) avant et après les éléments de dessin. Cela se produit lorsque **dwDrawStage** est égal à CDDS \_ prépaint.<br/>                                            |
| <dl> <dt>**CDRF \_ NOTIFYPOSTERASE**</dt> </dl>   | Le contrôle notifie le parent après l’effacement d’un élément. Cela se produit lorsque **dwDrawStage** est égal à CDDS \_ prépaint.<br/>                                                                                                                                                                 |
| <dl> <dt>**CDRF \_ NOTIFYPOSTPAINT**</dt> </dl>   | Le contrôle notifie le parent après avoir peint un élément. Cela se produit lorsque **dwDrawStage** est égal à CDDS \_ prépaint.<br/>                                                                                                                                                                |
| <dl> <dt>**CDRF \_ NOTIFYSUBITEMDRAW**</dt> </dl> | [Version 4,71](common-control-versions.md). Le contrôle notifie le parent lorsqu’un sous-élément de vue liste est en cours de dessin. Cela se produit lorsque **dwDrawStage** est égal à CDDS \_ prépaint.<br/>                                                                                                  |
| <dl> <dt>**CDRF \_ NEWFONT**</dt> </dl>           | Votre application a spécifié une nouvelle police pour l’élément. Le contrôle utilise la nouvelle police. Pour plus d’informations sur la modification des polices, consultez [modification des polices et des couleurs](custom-draw.md). Cela se produit lorsque **dwDrawStage** est égal à CDDS \_ ITEMPREPAINT.<br/> |
| <dl> <dt>**CDRF \_ SKIPDEFAULT**</dt> </dl>       | Votre application a dessiné l’élément manuellement. Le contrôle ne dessine pas l’élément. Cela se produit lorsque **dwDrawStage** est égal à CDDS \_ ITEMPREPAINT.<br/>                                                                                                                                          |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Utilisation d’un dessin personnalisé](custom-draw.md)
</dt> </dl>

 

 





