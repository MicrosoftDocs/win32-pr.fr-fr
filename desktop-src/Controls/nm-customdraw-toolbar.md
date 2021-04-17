---
title: Code de notification NM_CUSTOMDRAW (barre d’outils) (commctrl. h)
description: Envoyé par une barre d’outils pour signaler à sa fenêtre parente les opérations de dessin. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: e83a85f4-7955-411d-9a08-29f5b30158c5
keywords:
- Contrôles Windows de code de notification NM_CUSTOMDRAW (barre d’outils)
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
ms.openlocfilehash: c8d1a33e6b7e9a26237813ec3a90e560f05dd9ce
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104519321"
---
# <a name="nm_customdraw-toolbar-notification-code"></a>\_Code de notification CUSTOMDRAW nm (barre d’outils)

Envoyé par une barre d’outils pour signaler à sa fenêtre parente les opérations de dessin. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .


```C++
NM_CUSTOMDRAW
        
    lpNMCustomDraw = (LPNMCUSTOMDRAW) lParam;
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lParam* 
</dt> <dd>

[Version 4,70](common-control-versions.md). Pointeur vers une structure [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) qui contient des informations sur l’opération de dessin. Le membre **dwItemSpec** de cette structure contient l’identificateur de commande de l’élément qui est en train d’être dessiné. Le membre **lItemlParam** de cette structure contient la valeur **dwData** pour l’élément qui est en train d’être dessiné.

[Version 4,71](common-control-versions.md). Pointeur vers une structure [**NMTBCUSTOMDRAW**](/windows/desktop/api/Commctrl/ns-commctrl-nmtbcustomdraw) qui contient des informations sur l’opération de dessin. Le membre **dwItemSpec** du membre **NMCD** de cette structure contient l’identificateur de commande de l’élément qui est en train d’être dessiné. Le membre **lItemlParam** du membre **NMCD** de cette structure contient la valeur **dwData** pour l’élément qui est en train d’être dessiné.

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
| <dl> <dt>**TBCDRF \_ BLENDICON**</dt> </dl>       | [Version 5,00](common-control-versions.md). Mélangez le bouton 50 pour cent avec l’arrière-plan. Cela se produit lorsque **dwDrawStage** est égal à CDDS \_ ITEMPREPAINT.<br/>                                                                                                                      |
| <dl> <dt>**TBCDRF \_ NObackground**</dt> </dl>    | [Version 5,00](common-control-versions.md). Ne dessinez pas l’arrière-plan du bouton. Cela se produit lorsque **dwDrawStage** est égal à CDDS \_ ITEMPREPAINT.<br/>                                                                                                                                        |
| <dl> <dt>**TBCDRF \_ NOpériphéries**</dt> </dl>         | [Version 4,71](common-control-versions.md). Ne dessinez pas les bords du bouton. Cela se produit lorsque **dwDrawStage** est égal à CDDS \_ ITEMPREPAINT.<br/>                                                                                                                                             |
| <dl> <dt>**TBCDRF \_ HILITEHOTTRACK**</dt> </dl>  | [Version 4,71](common-control-versions.md). Utilisez le membre **clrHighlightHotTrack** de la structure [**NMTBCUSTOMDRAW**](/windows/desktop/api/Commctrl/ns-commctrl-nmtbcustomdraw) pour dessiner l’arrière-plan des éléments suivis à chaud. Cela se produit lorsque **dwDrawStage** est égal à CDDS \_ ITEMPREPAINT.<br/>                        |
| <dl> <dt>**nooffset TBCDRF \_**</dt> </dl>        | [Version 4,71](common-control-versions.md). Ne pas décaler le bouton lorsqu’il est enfoncé. Cela se produit lorsque **dwDrawStage** est égal à CDDS \_ ITEMPREPAINT.<br/>                                                                                                                                |
| <dl> <dt>**nomark TBCDRF \_**</dt> </dl>          | Ne dessinez pas la surbrillance par défaut des éléments pour lesquels le [**TBSTATE est \_ marqué**](toolbar-button-states.md). Cela se produit lorsque **dwDrawStage** est égal à CDDS \_ ITEMPREPAINT.<br/>                                                                                              |
| <dl> <dt>**TBCDRF \_ NOETCHEDEFFECT**</dt> </dl>  | [Version 4,71](common-control-versions.md). Ne dessinez pas d’effet gravé pour les éléments désactivés. Cela se produit lorsque **dwDrawStage** est égal à CDDS \_ ITEMPREPAINT.<br/>                                                                                                                         |
| <dl> <dt>**TBCDRF \_ USECDCOLORS**</dt> </dl>     | [Version 6,00](common-control-versions.md), **Windows Vista** uniquement. Utilisez des couleurs de dessin personnalisées pour restituer le texte quel que soit le style visuel.<br/>                                                                                                                                         |



 

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

 

 





