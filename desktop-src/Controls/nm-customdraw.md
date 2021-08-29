---
title: NM_CUSTOMDRAW le code de notification (commctrl. h)
description: Avertit la fenêtre parente d’un contrôle des opérations de dessin personnalisées. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 2ca51ee0-4431-45c0-880c-a8b74318d8a9
keywords:
- NM_CUSTOMDRAW les contrôles de Windows de code de notification
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
ms.openlocfilehash: ff8f1a7fe570d88ce583bc0d0aaa34576f8c440836060904d182559e46c3950a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119078913"
---
# <a name="nm_customdraw-notification-code"></a>\_Code de notification CUSTOMDRAW nm

Avertit la fenêtre parente d’un contrôle des opérations de dessin personnalisées. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .


```C++
NM_CUSTOMDRAW

#ifdef LIST_VIEW_CUSTOM_DRAW

    lpNMCustomDraw = (LPNMLVCUSTOMDRAW) lParam;

#elif TOOL_TIPS_CUSTOM_DRAW

    lpNMCustomDraw = (LPNMTTCUSTOMDRAW) lParam;

#elif TREE_VIEW_CUSTOM_DRAW

    lpNMCustomDraw = (LPNMTVCUSTOMDRAW) lParam;

#elif TOOL_BAR_CUSTOM_DRAW

    lpNMCustomDraw = (LPNMTBCUSTOMDRAW) lParam;

#else

    lpNMCustomDraw = (LPNMCUSTOMDRAW) lParam;

#endif
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure de dessin personnalisée qui contient des informations sur l’opération de dessin. La liste suivante spécifie les contrôles et leurs structures associées.



| Contrôler                     | Structure de dessin personnalisée                    |
|-----------------------------|------------------------------------------|
| Rebar, TrackBar et en-tête | [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw)     |
| Affichage Liste                   | [**NMLVCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmlvcustomdraw) |
| Info-bulle                     | [**NMTTCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmttcustomdraw) |
| Arborescence                   | [**NMTVCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmtvcustomdraw) |
| Barre d’outils                     | [**NMTBCUSTOMDRAW**](/windows/desktop/api/Commctrl/ns-commctrl-nmtbcustomdraw) |



 

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La valeur que votre application peut retourner dépend de l’étape de dessin actuelle. Le membre **dwDrawStage** de la structure [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) associée contient une valeur qui spécifie la phase de dessin. Vous devez retourner l’une des valeurs suivantes.



| Code de retour                                                                                            | Description                                                                                                                                                                                                                                                                                                                                                                                                                      |
|--------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**CDRF \_ par défaut**</dt> </dl>         | Le contrôle se dessine lui-même. Il n’enverra pas de codes de notification [ \_ CUSTOMDRAW nm](nm-customdraw.md) supplémentaires pour ce cycle de peinture. Cet indicateur ne peut pas être utilisé avec un autre indicateur. <br/>                                                                                                                                                                                                                                 |
| <dl> <dt>**CDRF, \_ INerase**</dt> </dl>           | Le contrôle dessinera uniquement l’arrière-plan.<br/>                                                                                                                                                                                                                                                                                                                                                                            |
| <dl> <dt>**CDRF \_ NEWFONT**</dt> </dl>           | Votre application a spécifié une nouvelle police pour l’élément. le contrôle utilise la nouvelle police. Pour plus d’informations sur la modification des polices, consultez [modification des polices et des couleurs](custom-draw.md). Cela se produit lorsque **dwDrawStage** est égal à CDDS \_ ITEMPREPAINT.<br/>                                                                                                                                        |
| <dl> <dt>**CDRF \_ NOTIFYITEMDRAW**</dt> </dl>    | Le contrôle notifie le parent de toutes les opérations de dessin liées aux éléments. Il envoie les codes de notification [ \_ CUSTOMDRAW nm](nm-customdraw.md) avant et après les éléments de dessin. Cela se produit lorsque **dwDrawStage** est égal à CDDS \_ prépaint.<br/>                                                                                                                                                                                |
| <dl> <dt>**CDRF \_ NOTIFYPOSTERASE**</dt> </dl>   | Le contrôle notifie le parent après l’effacement d’un élément. Cela se produit lorsque **dwDrawStage** est égal à CDDS \_ prépaint.<br/>                                                                                                                                                                                                                                                                                                     |
| <dl> <dt>**CDRF \_ NOTIFYPOSTPAINT**</dt> </dl>   | Le contrôle enverra un code de notification [ \_ CUSTOMDRAW nm](nm-customdraw.md) lorsque le cycle de peinture de l’ensemble du contrôle est terminé. Cela se produit lorsque **dwDrawStage** est égal à CDDS \_ prépaint.<br/>                                                                                                                                                                                                                    |
| <dl> <dt>**CDRF \_ NOTIFYSUBITEMDRAW**</dt> </dl> | Votre application recevra un code de notification [ \_ CUSTOMDRAW nm](nm-customdraw.md) avec **dwDrawStage** défini sur CDDS \_ ITEMPREPAINT CDDS sous- \| \_ élément avant que chaque sous-élément de vue liste soit dessiné. Vous pouvez ensuite spécifier la police et la couleur de chaque sous-élément séparément ou retourner [**CDRF \_ par défaut**](cdrf-constants.md) pour le traitement par défaut. Cela se produit lorsque **dwDrawStage** est égal à CDDS \_ ITEMPREPAINT.<br/> |
| <dl> <dt>**CDRF \_ SKIPDEFAULT**</dt> </dl>       | Votre application a dessiné l’élément manuellement. Le contrôle ne dessine pas l’élément. Cela se produit lorsque **dwDrawStage** est égal à CDDS \_ ITEMPREPAINT.<br/>                                                                                                                                                                                                                                                                              |
| <dl> <dt>**CDRF \_ SKIPPOSTPAINT**</dt> </dl>     | Le contrôle ne dessine pas le rectangle de focus autour d’un élément.<br/>                                                                                                                                                                                                                                                                                                                                                         |



 

## <a name="remarks"></a>Remarques

Actuellement, les contrôles suivants prennent en charge la fonctionnalité de dessin personnalisée : en-tête, mode liste, rebar, barre d’outils, info-bulle, TrackBar et arborescence. Le dessin personnalisé est également pris en charge pour les contrôles Button si vous disposez d’un manifeste d’application pour vous assurer que Comctl32.dll version 6 est disponible.

Si ce message est géré dans une procédure de dialogue, vous devez définir la valeur de retour dans le cadre des données de la fenêtre avant de retourner la valeur **true**. Pour plus d’informations, consultez [**DialogProc**](/windows/desktop/api/winuser/nc-winuser-dlgproc).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Méthodologique**
</dt> <dt>

[Dessin personnalisé](custom-draw.md)
</dt> </dl>

 

