---
title: TBN_DROPDOWN le code de notification (commctrl. h)
description: Envoyé par un contrôle de barre d’outils lorsque l’utilisateur clique sur un bouton déroulant. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 85360f74-4b43-4d0a-8c89-22b0741fe96a
keywords:
- TBN_DROPDOWN les contrôles de Windows de code de notification
topic_type:
- apiref
api_name:
- TBN_DROPDOWN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad7adbb9e0e2ed3d77f8ca8bfb6b09dedd2265be
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127116321"
---
# <a name="tbn_dropdown-notification-code"></a>\_Code de notification de liste déroulante TBN

Envoyé par un contrôle de barre d’outils lorsque l’utilisateur clique sur un bouton déroulant. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .


```C++
TBN_DROPDOWN

    lpnmtb = (LPNMTOOLBAR) lParam;
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**NMTOOLBAR**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara) qui contient des informations sur ce code de notification. Pour ce code de notification, seuls les membres **HDR** et **iItem** de cette structure sont valides.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Renvoie l'une des valeurs suivantes :



| Code de retour                                                                                          | Description                                                                       |
|------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| <dl> <dt>**TBDDRET \_ par défaut**</dt> </dl>      | La liste déroulante a été gérée.<br/>                                             |
| <dl> <dt>**TBDDRET \_ NOdéfaut**</dt> </dl>    | La liste déroulante n’a pas été gérée.<br/>                                         |
| <dl> <dt>**TBDDRET \_ TREATPRESSED**</dt> </dl> | La liste déroulante a été gérée, mais traite le bouton comme un bouton normal.<br/> |



 

## <a name="remarks"></a>Notes

> [!Note]  
> Les boutons déroulants peuvent être bruts (style de [**\_ liste déroulante BTNS**](toolbar-control-and-button-styles.md) ), afficher une flèche en regard de l’image du bouton (style de [**\_ WHOLEDROPDOWN BTNS**](toolbar-control-and-button-styles.md) ) ou afficher une flèche séparée de l’image ([**TBSTYLE \_ ex \_ DRAWDDARROWS**](toolbar-extended-styles.md) style). Si une flèche séparée est utilisée, \_ la liste déroulante TBN est envoyée uniquement si l’utilisateur clique sur la partie de flèche du bouton. Si l’utilisateur clique sur la partie principale du bouton, un message de [**\_ commande WM**](/windows/desktop/menurc/wm-command) avec l’ID du bouton est envoyé, comme avec un bouton standard. Pour les deux autres styles du bouton déroulant, \_ la liste déroulante TBN est envoyée lorsque l’utilisateur clique sur une partie du bouton.

 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

