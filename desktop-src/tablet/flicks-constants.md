---
description: Voici les constantes de raccourcis.
ms.assetid: 21aaf8f0-13b7-4f97-ad4a-3557a7020337
title: Constantes de raccourcis (Tabflicks. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b9a83f9a35a2c1a9cbd7c4b048a8c985f5eea34
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113419"
---
# <a name="flicks-constants"></a>Constantes de raccourcis

Voici les constantes de raccourcis.



| Constante/valeur                                                                                                                                                                                                                                   | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FLICK_WM_HANDLED_MASK"></span><span id="flick_wm_handled_mask"></span><dl> <dt>**Raccourci \_ \_ \_ Masque WM traité**</dt> <dt>0x1</dt> </dl> | Valeur à retourner après la gestion du message du [**\_ message de \_ raccourci WM**](wm-tablet-flick-message.md) de la tablette. Si **le \_ \_ \_ masque WM WM géré** est retourné, aucune action supplémentaire ne se produit. Dans le cas contraire, Windows envoie des notifications de suivi, telles que [**WM \_ APPCOMMAND**](/windows/desktop/inputdev/wm-appcommand), [**WM \_ VSCROLL**](/windows/desktop/Controls/wm-vscroll)ou [**WM \_ keyverse**](/windows/desktop/inputdev/wm-keydown), selon l’action associée au raccourci Pen. <br/> |
| <span id="NUM_FLICK_DIRECTIONS"></span><span id="num_flick_directions"></span><dl> <dt>**Nombre \_ \_Directions de mouvement**</dt> <dt>8</dt> </dl>       | Nombre de directions définies dans l’énumération [**FLICKDIRECTION**](/windows/desktop/api/tabflicks/ne-tabflicks-flickdirection) .<br/>                                                                                                                                                                                                                                                                                                                                                              |



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                         |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                   |
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

 

