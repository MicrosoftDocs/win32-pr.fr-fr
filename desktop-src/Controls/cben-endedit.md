---
title: CBEN_ENDEDIT le code de notification (commctrl. h)
description: Envoyé lorsque l’utilisateur a terminé une opération dans la zone d’édition ou a sélectionné un élément dans la liste déroulante du contrôle. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: b6b50951-7304-4499-b57b-a5b592de2190
keywords:
- CBEN_ENDEDIT les contrôles de Windows de code de notification
topic_type:
- apiref
api_name:
- CBEN_ENDEDIT
- CBEN_ENDEDITA
- CBEN_ENDEDITW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 22ae9205e84e4f1c0b10e516b1f406f2d167f1bc5cc38417a31379d20e16fcac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118413949"
---
# <a name="cben_endedit-notification-code"></a>\_Code de notification CBEN ENDEDIT

Envoyé lorsque l’utilisateur a terminé une opération dans la zone d’édition ou a sélectionné un élément dans la liste déroulante du contrôle. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .


```C++
CBEN_ENDEDIT

    pnmEditInfo = (PNMCBEENDEDIT) lParam;
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**NMCBEENDEDIT**](/windows/desktop/api/Commctrl/ns-commctrl-nmcbeendedita) qui contient des informations sur la façon dont l’utilisateur a conclu l’opération de modification.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

**False** pour accepter le code de notification et autoriser le contrôle à afficher l’élément sélectionné ; Sinon, **true**.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Noms Unicode et ANSI<br/>   | **CBEN \_ ENDEDITW** (Unicode) et **CBEN \_ ENDEDITA** (ANSI)<br/>                 |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[À propos des contrôles ComboBoxEx](comboboxex-controls.md)
</dt> </dl>

 

 





