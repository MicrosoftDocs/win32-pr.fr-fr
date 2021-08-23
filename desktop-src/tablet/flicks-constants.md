---
description: Voici les constantes de raccourcis.
ms.assetid: 21aaf8f0-13b7-4f97-ad4a-3557a7020337
title: Constantes de raccourcis (Tabflicks. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e927d0715c9f34e7e1db979c32545a0d8c8efad18186192a751f2cdbed13172
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119092646"
---
# <a name="flicks-constants"></a>Constantes de raccourcis

Voici les constantes de raccourcis.



| Constante/valeur                                                                                                                                                                                                                                   | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FLICK_WM_HANDLED_MASK"></span><span id="flick_wm_handled_mask"></span><dl> <dt>**Raccourci \_ \_ \_ Masque WM traité**</dt> <dt>0x1</dt> </dl> | Valeur à retourner après la gestion du message du [**\_ message de \_ raccourci WM**](wm-tablet-flick-message.md) de la tablette. Si **le \_ \_ \_ masque WM WM géré** est retourné, aucune action supplémentaire ne se produit. sinon, Windows envoie des notifications de suivi, telles que [**wm \_ APPCOMMAND**](/windows/desktop/inputdev/wm-appcommand), [**wm \_ VSCROLL**](/windows/desktop/Controls/wm-vscroll)ou [**wm \_ keyverse**](/windows/desktop/inputdev/wm-keydown), selon l’action associée au raccourci du stylet. <br/> |
| <span id="NUM_FLICK_DIRECTIONS"></span><span id="num_flick_directions"></span><dl> <dt>**Nombre \_ \_Directions de mouvement**</dt> <dt>8</dt> </dl>       | Nombre de directions définies dans l’énumération [**FLICKDIRECTION**](/windows/desktop/api/tabflicks/ne-tabflicks-flickdirection) .<br/>                                                                                                                                                                                                                                                                                                                                                              |



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                         |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                   |
| En-tête<br/>                   | <dl> <dt>Tabflicks. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Énumération FLICKDIRECTION**](/windows/desktop/api/tabflicks/ne-tabflicks-flickdirection)
</dt> <dt>

[**Message du raccourci de \_ tablette WM \_**](wm-tablet-flick-message.md)
</dt> <dt>

[Mouvements de raccourcis](flicks-gestures.md)
</dt> <dt>

[Réponse aux raccourcis stylet](/previous-versions//dd356077(v=vs.85))
</dt> </dl>

 

