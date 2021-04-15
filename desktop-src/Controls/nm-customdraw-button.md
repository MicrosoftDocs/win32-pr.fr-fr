---
title: Code de notification NM_CUSTOMDRAW (bouton) (commctrl. h)
description: Notifie la fenêtre parente d’un contrôle bouton sur les opérations de dessin personnalisées sur le bouton. Le contrôle Button envoie ce code de notification sous la forme d’un \_ message WM Notify.
ms.assetid: cabe5515-ba64-4c53-8746-7a0559df8989
keywords:
- Contrôles Windows de code de notification NM_CUSTOMDRAW (bouton)
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
ms.openlocfilehash: ab3cc4eb73c3a0185131bb6ef2198458888ec89d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104467114"
---
# <a name="nm_customdraw-button-notification-code"></a>\_Code de notification CUSTOMDRAW nm (bouton)

Notifie la fenêtre parente d’un contrôle bouton sur les opérations de dessin personnalisées sur le bouton.

Le contrôle Button envoie ce code de notification sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .


```C++
NM_CUSTOMDRAW

    lpNMCustomDraw = (LPNMCUSTOMDRAW) lParam;
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) qui contient des informations sur l’opération de dessin. Le membre **dwItemSpec** de cette structure contient l’index de l’élément qui est en train d’être dessiné et le membre **lItemlParam** de cette structure contient le *lParam* de l’élément.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La valeur que votre application peut retourner dépend de l’étape de dessin actuelle. Le membre **dwDrawStage** de la structure [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) associée contient une valeur qui spécifie la phase de dessin. Vous devez retourner l’une des valeurs suivantes.



| Code de retour                                                                                          | Description                                                                                                                                                           |
|------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**CDRF \_ NOTIFYPOSTERASE**</dt> </dl> | Le contrôle notifie le parent après l’effacement d’un élément. Cette valeur ne peut être utilisée que si **dwDrawStage** est égal à CDDS \_ preerase.<br/>                                  |
| <dl> <dt>**CDRF \_ NOTIFYPOSTPAINT**</dt> </dl> | Le contrôle notifie le parent après avoir peint un élément. Cela peut être utilisé uniquement si **dwDrawStage** est égal à CDDS \_ prépaint.<br/>                                 |
| <dl> <dt>**CDRF \_ SKIPDEFAULT**</dt> </dl>     | L’application a dessiné l’élément manuellement. Le contrôle ne dessine pas l’élément. Cela peut être utilisé lorsque **dwDrawStage** est égal à CDDS \_ PREerase ou CDDS \_ PrePaint.<br/> |



 

## <a name="remarks"></a>Notes

Si le contrôle Button est marqué comme OwnerDraw (BS \_ OwnerDraw), le \_ Code de notification CUSTOMDRAW nm n’est pas envoyé.

Pour plus d’informations, consultez Utilisation d’un [dessin personnalisé](custom-draw.md) .

> [!Note]  
> Pour utiliser ce code de notification, vous devez fournir un manifeste spécifiant Comclt32.dll version 6,0. Pour plus d’informations sur les manifestes, consultez [activation des styles visuels](cookbook-overview.md).

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                                            |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                                      |
| En-tête<br/>                   | <dl> <dt>Commctrl. h (inclure Windows. h)</dt> </dl> |



 

 





