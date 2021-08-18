---
description: Envoyé lorsqu’un utilisateur exécute un raccourci stylet. Une fenêtre reçoit ce message par le biais de sa fonction WindowProc.
ms.assetid: 9433aadf-3440-4249-8f2c-3e22ebc949fb
title: Message WM_TABLET_FLICK (Tpcshrd. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5bb01fce646d2e7c6cb4e1b25c2f49f0c4dde5258ba2167e117a23eff22a5d1c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119842773"
---
# <a name="wm_tablet_flick-message"></a>Message du raccourci de \_ tablette WM \_

Envoyé lorsqu’un utilisateur exécute un raccourci stylet. Une fenêtre reçoit ce message par le biais de sa fonction [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
#define WM_TABLET_DEFBASE  0x02C0
#define WM_TABLET_FLICK    (WM_TABLET_DEFBASE + 11)     
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

[**Structure de \_ données de raccourci**](/windows/desktop/api/tabflicks/ns-tabflicks-flick_data) qui contient des informations sur le raccourci du stylet qui s’est produit.

</dd> <dt>

*lParam* 
</dt> <dd>

[**Structure de \_ point de mouvement**](/windows/desktop/api/tabflicks/ns-tabflicks-flick_point) qui spécifie où le raccourci du stylet s’est produit.

</dd> </dl>

## <a name="remarks"></a>Remarques

Un raccourci stylet est un mouvement de stylet unidirectionnel qui requiert que l’utilisateur contacte le digitaliseur dans un mouvement de raccourci rapide et direct. Un raccourci est caractérisé par une vitesse élevée et un degré élevé d’angles. Un raccourci est identifié par sa direction. Les raccourcis peuvent être effectués dans huit directions correspondant aux directions cardinales et secondaires de la boussole.

en cas de mouvement du stylet, Windows signale d’abord une application en envoyant un message de **\_ \_ scintillement de tablette WM** , qu’une fenêtre reçoit par le biais de sa fonction [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) . Retournez la constante du **\_ \_ \_ masque géré WM WM** , décrite dans [constantes de raccourcis](flicks-constants.md), pour indiquer que l’application a répondu au message de **\_ \_ scintille de la tablette WM** . si l’application ne retourne pas le masque avec le **\_ WM WM \_ \_ géré**, Windows effectue l’action par défaut spécifiée dans le panneau de configuration raccourcis en envoyant une notification de suivi, telle que [**wm \_ APPCOMMAND**](../inputdev/wm-appcommand.md), [**wm \_ VSCROLL**](../controls/wm-vscroll.md)ou [**wm \_ keyverse**](../inputdev/wm-keydown.md), selon l’action associée au raccourci pen.

Soyez prudent lors du traitement du message de **\_ \_ raccourci WM** de la tablette. **WM \_ Le \_ raccourci de tablette** est passé via la fonction [**SendMessageTimeout**](/windows/win32/api/winuser/nf-winuser-sendmessagetimeouta) . Si vous appelez des méthodes sur une interface COM, cet objet doit être dans le même processus. Si ce n’est pas le cas, COM lève une exception.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                 |
| En-tête<br/>                   | <dl> <dt>Tpcshrd. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**structure des données de raccourci \_**](/windows/desktop/api/tabflicks/ns-tabflicks-flick_data)
</dt> <dt>

[**message du raccourci de \_ tablette WM \_**](wm-tablet-flick-message.md)
</dt> <dt>

[mouvements de raccourcis](flicks-gestures.md)
</dt> <dt>

[réponse aux raccourcis stylet](/previous-versions/windows/desktop/ms703447(v=vs.85))
</dt> </dl>

 

 
