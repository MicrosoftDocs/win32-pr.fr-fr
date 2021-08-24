---
title: Constantes RF (CommCtrl. h)
description: Ces constantes sont utilisées comme valeurs de retour par un contrôle en réponse à un \_ Code de notification CUSTOMDRAW nm.
ms.assetid: 6b05e27e-5d18-46f2-b326-2a5148597852
topic_type:
- apiref
api_name:
- CDRF_DODEFAULT
- CDRF_NEWFONT
- CDRF_SKIPDEFAULT
- CDRF_DOERASE
- CDRF_NOTIFYPOSTPAINT
- CDRF_NOTIFYITEMDRAW
- CDRF_NOTIFYSUBITEMDRAW
- CDRF_NOTIFYPOSTERASE
- CDRF_SKIPPOSTPAINT
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 817bab7c2ec41134d71c92ada94c62475b01cc2db96a9f8c74ecb2c7b9274451
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119770379"
---
# <a name="rf-constants"></a>Constantes RF

Ces constantes sont utilisées comme valeurs de retour par un contrôle en réponse à un code de notification [ \_ CUSTOMDRAW nm](nm-customdraw.md) .



| Constante/valeur                                                                                                                                                                                                                                           | Description                                                                                                                                                                                                                                                                                                                                                                                                                           |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CDRF_DODEFAULT"></span><span id="cdrf_dodefault"></span><dl> <dt>**CDRF \_ Valeur par défaut**</dt> <dt>0x00000000</dt> </dl>                         | Le contrôle se dessine lui-même. Il n’enverra pas de codes de notification [ \_ CUSTOMDRAW nm](nm-customdraw.md) supplémentaires pour ce cycle de peinture. Cela se produit lorsque le **dwDrawStage** de la structure [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) est égal à CDDS \_ prépaint.<br/>                                                                                                                                                               |
| <span id="CDRF_NEWFONT"></span><span id="cdrf_newfont"></span><dl> <dt>**CDRF \_ NEWFONT**</dt> <dt>0x00000002</dt> </dl>                               | L’application a spécifié une nouvelle police pour l’élément ; le contrôle utilise la nouvelle police. Pour plus d’informations sur la modification des polices, consultez Modification des polices et des couleurs. Cela se produit lorsque le **dwDrawStage** de la structure [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) est égal à CDDS \_ ITEMPREPAINT.<br/>                                                                                                                                      |
| <span id="CDRF_SKIPDEFAULT"></span><span id="cdrf_skipdefault"></span><dl> <dt>**CDRF \_ SKIPDEFAULT**</dt> <dt>0x00000004</dt> </dl>                   | L’application a dessiné l’élément manuellement. Le contrôle ne dessine pas l’élément. Cela se produit lorsque le **dwDrawStage** de la structure [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) est égal à CDDS \_ ITEMPREPAINT.<br/>                                                                                                                                                                                                                          |
| <span id="CDRF_DOERASE"></span><span id="cdrf_doerase"></span><dl> <dt>**CDRF \_ Inerase**</dt> <dt>0x00000008</dt> </dl>                               | **Windows Vista et versions ultérieures.** Le contrôle dessinera l’arrière-plan.<br/>                                                                                                                                                                                                                                                                                                                                                         |
| <span id="CDRF_NOTIFYPOSTPAINT"></span><span id="cdrf_notifypostpaint"></span><dl> <dt>**CDRF \_ NOTIFYPOSTPAINT**</dt> <dt>0x00000010</dt> </dl>       | Le contrôle notifie le parent après avoir peint un élément. Cela se produit lorsque le **dwDrawStage** de la structure [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) est égal à CDDS \_ prépaint.<br/>                                                                                                                                                                                                                                               |
| <span id="CDRF_NOTIFYITEMDRAW"></span><span id="cdrf_notifyitemdraw"></span><dl> <dt>**CDRF \_ NOTIFYITEMDRAW**</dt> <dt>0x00000020</dt> </dl>          | Le contrôle notifie le parent de toutes les opérations de dessin liées aux éléments. Il envoie les codes de notification [ \_ CUSTOMDRAW nm](nm-customdraw.md) avant et après les éléments de dessin. Cela se produit lorsque le **dwDrawStage** de la structure [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) est égal à CDDS \_ prépaint.<br/>                                                                                                                           |
| <span id="CDRF_NOTIFYSUBITEMDRAW"></span><span id="cdrf_notifysubitemdraw"></span><dl> <dt>**CDRF \_ NOTIFYSUBITEMDRAW**</dt> <dt>0x00000020</dt> </dl> | **Internet Explorer 4,0 et versions ultérieures.** Le contrôle notifie le parent de toutes les opérations de dessin liées aux éléments. Il envoie les codes de notification [ \_ CUSTOMDRAW nm](nm-customdraw.md) avant et après les éléments de dessin. Cela se produit lorsque le **dwDrawStage** de la structure [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) est égal à CDDS \_ prépaint. Cet indicateur est identique à **CDRF \_ NOTIFYITEMDRAW** et son utilisation dépend du contexte.<br/> |
| <span id="CDRF_NOTIFYPOSTERASE"></span><span id="cdrf_notifyposterase"></span><dl> <dt>**CDRF \_ NOTIFYPOSTERASE**</dt> <dt>0x00000040</dt> </dl>       | Le contrôle notifie le parent après l’effacement d’un élément. Cela se produit lorsque le **dwDrawStage** de la structure [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) est égal à CDDS \_ prépaint.<br/>                                                                                                                                                                                                                                                |
| <span id="CDRF_SKIPPOSTPAINT"></span><span id="cdrf_skippostpaint"></span><dl> <dt>**CDRF \_ SKIPPOSTPAINT**</dt> <dt>0x00000100</dt> </dl>             | **Windows Vista et versions ultérieures.** Le contrôle ne dessine pas le rectangle de focus.<br/>                                                                                                                                                                                                                                                                                                                                                |



## <a name="remarks"></a>Remarques

Ces constantes sont définies dans commctrl. h.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|---------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>CommCtrl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Personnalisation de l’apparence d’un contrôle à l’aide d’un dessin personnalisé](custom-draw.md)
</dt> </dl>

 

 





