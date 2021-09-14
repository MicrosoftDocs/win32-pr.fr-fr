---
title: Message EM_SHOWBALLOONTIP (commctrl. h)
description: Le \_ message em SHOWBALLOONTIP affiche une info-bulle associée à un contrôle d’édition.
ms.assetid: 1e6915b7-4b61-43b2-be13-b89c72378a1a
keywords:
- EM_SHOWBALLOONTIP les contrôles de Windows de message
topic_type:
- apiref
api_name:
- EM_SHOWBALLOONTIP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8fc0174752ab8214873da9478a0af435be76427
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127006342"
---
# <a name="em_showballoontip-message"></a>\_Message SHOWBALLOONTIP em

Le message **em \_ SHOWBALLOONTIP** affiche une info-bulle associée à un contrôle d’édition.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Non utilisé ; doit être égal à zéro.

</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**EDITBALLOONTIP**](/windows/desktop/api/Commctrl/ns-commctrl-editballoontip) qui contient des informations sur l’info-bulle à afficher.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Si le message est correctement exécuté, la méthode retourne la **valeur true**. Sinon, elle retourne **false**.

## <a name="remarks"></a>Notes

> [!Note]  
> Pour utiliser ce message, vous devez fournir un manifeste spécifiant Comclt32.dll version 6,0. Pour plus d’informations sur les manifestes, consultez [activation des styles visuels](cookbook-overview.md).

 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Référence**
</dt> <dt>

[**EDITBALLOONTIP**](/windows/desktop/api/Commctrl/ns-commctrl-editballoontip)
</dt> <dt>

[**Modifier \_ ShowBalloonTip**](/windows/desktop/api/Commctrl/nf-commctrl-edit_showballoontip)
</dt> </dl>

 

 





