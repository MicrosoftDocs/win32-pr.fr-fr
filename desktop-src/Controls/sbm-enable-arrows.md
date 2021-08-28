---
title: Message SBM_ENABLE_ARROWS (winuser. h)
description: Une application envoie un \_ message de flèches d’activation SBM \_ pour activer ou désactiver une ou deux flèches d’un contrôle de barre de défilement.
ms.assetid: 9646826a-3a7c-490b-822d-7511e4ef2262
keywords:
- SBM_ENABLE_ARROWS les contrôles de Windows de message
topic_type:
- apiref
api_name:
- SBM_ENABLE_ARROWS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85e7f3ef8728befe72ec4f2c4afe39caeb10bc0b58984612a5db2445963dc549
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119770019"
---
# <a name="sbm_enable_arrows-message"></a>\_Message d’activation des \_ flèches SBM

Une application envoie un message de **\_ \_ flèches d’activation SBM** pour activer ou désactiver une ou deux flèches d’un contrôle de barre de défilement.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Spécifie si les flèches de barre de défilement sont activées ou désactivées, et indique quelles flèches sont activées ou désactivées. Ce paramètre peut prendre les valeurs suivantes.



| Valeur                                                                                                                                                                   | Signification                                                                                                    |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| <span id="ESB_DISABLE_BOTH"></span><span id="esb_disable_both"></span><dl> <dt>**ESB \_ désactiver \_ les deux**</dt> </dl> | Désactive les deux flèches sur une barre de défilement.<br/>                                                           |
| <span id="ESB_DISABLE_DOWN"></span><span id="esb_disable_down"></span><dl> <dt>**désactivation de ESB \_ \_**</dt> </dl> | Désactive la flèche vers le bas sur une barre de défilement verticale.<br/>                                               |
| <span id="ESB_DISABLE_LTUP"></span><span id="esb_disable_ltup"></span><dl> <dt>**ESB \_ désactiver \_ LTUP**</dt> </dl> | Désactive la flèche gauche sur une barre de défilement horizontale ou la flèche vers le haut sur une barre de défilement verticale.<br/>    |
| <span id="ESB_DISABLE_LEFT"></span><span id="esb_disable_left"></span><dl> <dt>**ESB- \_ désactiver la \_ gauche**</dt> </dl> | Désactive la flèche gauche sur une barre de défilement horizontale.<br/>                                             |
| <span id="ESB_DISABLE_RTDN"></span><span id="esb_disable_rtdn"></span><dl> <dt>**ESB \_ désactiver \_ RTDN**</dt> </dl> | Désactive la flèche droite sur une barre de défilement horizontale ou la flèche vers le bas sur une barre de défilement verticale.<br/> |
| <span id="ESB_DISABLE_UP"></span><span id="esb_disable_up"></span><dl> <dt>**désactivation d’ESB \_ \_**</dt> </dl>       | Désactive la flèche vers le haut sur une barre de défilement verticale.<br/>                                                 |
| <span id="ESB_ENABLE_BOTH"></span><span id="esb_enable_both"></span><dl> <dt>**ESB \_ activer \_ les deux**</dt> </dl>    | Active les deux flèches sur une barre de défilement.<br/>                                                            |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Ce paramètre n'est pas utilisé.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si le message est correctement exécuté, la valeur de retour est **true**; Sinon, la **valeur est false**.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                                           |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



 

 





