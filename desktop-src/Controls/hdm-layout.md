---
title: Message HDM_LAYOUT (commctrl. h)
description: Récupère les informations utilisées pour définir la taille et la position du contrôle d’en-tête dans le rectangle cible de la fenêtre parente. Vous pouvez envoyer ce message de manière explicite ou utiliser la macro disposition d’en-tête \_ .
ms.assetid: 0763e483-f01d-4739-8c61-1c52d1aad0b4
keywords:
- HDM_LAYOUT les contrôles de Windows de message
topic_type:
- apiref
api_name:
- HDM_LAYOUT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff4194ad5aa1847aa977bac1269a7ab88d36a571824387e07264713726135f25
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119435929"
---
# <a name="hdm_layout-message"></a>\_Message de disposition HDM

Récupère les informations utilisées pour définir la taille et la position du contrôle d’en-tête dans le rectangle cible de la fenêtre parente. Vous pouvez envoyer ce message de manière explicite ou utiliser la macro [**\_ disposition d’en-tête**](/windows/desktop/api/Commctrl/nf-commctrl-header_layout) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**HDLAYOUT**](/windows/win32/api/commctrl/ns-commctrl-hdlayout) . Le membre **PRC** spécifie les coordonnées d’un rectangle, tandis que le membre **pwpos** reçoit la taille et la position du contrôle header dans le rectangle.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la **valeur true** en cas de réussite, ou **false** dans le cas contraire.

## <a name="remarks"></a>Remarques

Le membre **pwpos** de la structure *lParam* reçoit les valeurs de taille et de position appropriées pour positionner le contrôle le long du bord supérieur du rectangle spécifié. La valeur de hauteur est la somme des hauteurs des bordures horizontales du contrôle et de la hauteur moyenne des caractères de la police actuellement sélectionnée dans le contexte de périphérique du contrôle.

Pour utiliser **la \_ disposition HDM** pour définir la taille et la position initiales d’un contrôle header, définissez l’état de visibilité initial du contrôle afin qu’il soit masqué. Après l’envoi de la **\_ disposition HDM** pour récupérer les valeurs de taille et de position, utilisez la fonction [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos) pour définir la nouvelle taille, la position et l’état de visibilité.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

