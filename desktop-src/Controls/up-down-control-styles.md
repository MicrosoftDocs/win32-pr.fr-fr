---
title: Styles de contrôle Up-Down (CommCtrl. h)
description: Cette section répertorie les styles utilisés lors de la création de contrôles Up-Up.
ms.assetid: d35198cb-6a5b-485e-a914-1b2ede53462f
topic_type:
- apiref
api_name:
- UDS_ALIGNLEFT
- UDS_ALIGNRIGHT
- UDS_ARROWKEYS
- UDS_AUTOBUDDY
- UDS_HORZ
- UDS_HOTTRACK
- UDS_NOTHOUSANDS
- UDS_SETBUDDYINT
- UDS_WRAP
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b27cd27123f4c1a071314fd20d1874e61b590d4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127115401"
---
# <a name="up-down-control-styles"></a>Styles de contrôle Up-Down

Cette section répertorie les styles utilisés lors de la création de contrôles Up-Up.



| Constante                                                                                                                                                            | Description                                                                                                                                                                                                                                                                                                                                                                                               |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="UDS_ALIGNLEFT"></span><span id="uds_alignleft"></span><dl> <dt>**UDS \_ ALIGNLEFT**</dt> </dl>       | Positionne le contrôle up-up en regard du bord gauche de la fenêtre associée. La fenêtre associée est déplacée vers la droite et sa largeur diminue pour s’adapter à la largeur du contrôle up-up.<br/>                                                                                                                                                                                                   |
| <span id="UDS_ALIGNRIGHT"></span><span id="uds_alignright"></span><dl> <dt>**ALIGNRIGHT-UDS \_**</dt> </dl>    | Positionne le contrôle up-up en regard du bord droit de la fenêtre associée. La largeur de la fenêtre associée est réduite pour s’adapter à la largeur du contrôle up-up.<br/>                                                                                                                                                                                                                          |
| <span id="UDS_ARROWKEYS"></span><span id="uds_arrowkeys"></span><dl> <dt>**UDS \_ ARROWKEYS**</dt> </dl>       | Fait en sorte que le contrôle up-descend incrémente et décrémente la position lorsque vous appuyez sur les touches haut et bas.<br/>                                                                                                                                                                                                                                                                          |
| <span id="UDS_AUTOBUDDY"></span><span id="uds_autobuddy"></span><dl> <dt>**l' \_ AUTOcopain de l’UDS**</dt> </dl>       | Sélectionne automatiquement la fenêtre précédente dans l’ordre de plan comme fenêtre associée du contrôle up-up.<br/>                                                                                                                                                                                                                                                                                                |
| <span id="UDS_HORZ"></span><span id="uds_horz"></span><dl> <dt>**UDS \_ Horiz**</dt> </dl>                      | Fait en sorte que les flèches du contrôle up-up pointent vers la gauche et vers la droite, et non vers le haut et vers le bas.<br/>                                                                                                                                                                                                                                                                                                            |
| <span id="UDS_HOTTRACK"></span><span id="uds_hottrack"></span><dl> <dt>**UDS \_ HOTTRACK**</dt> </dl>          | Provoque l’exposition du comportement « suivi réactif » par le contrôle. Autrement dit, il met en surbrillance les flèches haut et bas du contrôle lorsque le pointeur passe dessus. ce style requiert Windows 98 ou Windows 2000. si le système exécute Windows 95 ou Windows NT 4,0, l’indicateur est ignoré. Pour vérifier si la surveillance à chaud est activée, appelez [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa). <br/> |
| <span id="UDS_NOTHOUSANDS"></span><span id="uds_nothousands"></span><dl> <dt>**UDS \_ uds**</dt> </dl> | N’insère pas de séparateur de milliers entre tous les trois chiffres décimaux. <br/>                                                                                                                                                                                                                                                                                                                     |
| <span id="UDS_SETBUDDYINT"></span><span id="uds_setbuddyint"></span><dl> <dt>**UDS \_ SETBUDDYINT**</dt> </dl> | Fait en sorte que le contrôle up-out définisse le texte de la fenêtre associée (à l’aide du message [**WM \_ SETTEXT**](/windows/desktop/winmsg/wm-settext) ) lorsque la position change. Le texte se compose de la position mise en forme en tant que chaîne décimale ou hexadécimale.<br/>                                                                                                                                                             |
| <span id="UDS_WRAP"></span><span id="uds_wrap"></span><dl> <dt>**UDS de \_ Retour à la ligne**</dt> </dl>                      | Fait en sorte que la position « encapsule » si elle est incrémentée ou décrémentée au-delà du début ou de la fin de la plage.<br/>                                                                                                                                                                                                                                                                                 |



## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------|---------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>CommCtrl. h</dt> </dl> |



 

