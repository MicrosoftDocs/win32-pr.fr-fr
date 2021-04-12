---
description: Utilisé pour définir des messages privés, généralement sous la forme WM \_ app + x, où x est une valeur entière.
ms.assetid: fdb549df-426f-4af5-9c17-6e8730e4abc0
title: WM_APP (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4998f8240b08d248a75b375bb813ba02cd02344e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203801"
---
# <a name="wm_app"></a>\_application WM

Utilisé pour définir des messages privés, généralement au format **WM \_ app** + *x*, où *x* est une valeur entière.

``` syntax
#define WM_APP                          0x8000
```

## <a name="remarks"></a>Notes

La constante d' **\_ application WM** est utilisée pour faire la distinction entre les valeurs de message qui sont réservées à une utilisation par le système et les valeurs qui peuvent être utilisées par une application pour envoyer des messages dans une classe de fenêtre privée. Voici les plages de numéros de message disponibles.



| Plage                                                 | Signification                                                        |
|-------------------------------------------------------|----------------------------------------------------------------|
| 0 à [**\_ utilisateur WM**](wm-user.md) – 1<br/>   | Messages réservés pour une utilisation par le système.<br/>            |
| [**WM \_ UTILISATEUR**](wm-user.md) via 0x7FFF<br/> | Messages entiers à utiliser par les classes de fenêtre privées.<br/> |
| **WM \_ APPLICATION** via 0xBFFF<br/>                 | Messages disponibles pour une utilisation par des applications.<br/>         |
| 0xC000 à 0xFFFF<br/>                      | Messages de chaîne à utiliser par les applications.<br/>            |
| Supérieur à 0xFFFF<br/>                        | Réservé par le système.<br/>                             |



 

Les numéros de message dans la première plage (0 à [**\_ utilisateur WM**](wm-user.md) – 1) sont définis par le système. Les valeurs de cette plage qui ne sont pas définies explicitement sont réservées par le système.

Les numéros de message dans la deuxième plage ([**\_ utilisateur WM**](wm-user.md) via 0x7FFF) peuvent être définis et utilisés par une application pour envoyer des messages dans une classe de fenêtre privée. Ces valeurs ne peuvent pas être utilisées pour définir des messages significatifs dans une application, car certaines classes de fenêtres prédéfinies définissent déjà des valeurs dans cette plage. Par exemple, les classes de contrôle prédéfinies telles que **Button**, **Edit**, **ListBox** et **ComboBox** peuvent utiliser ces valeurs. Les messages de cette plage ne doivent pas être envoyés à d’autres applications, sauf si les applications ont été conçues pour échanger des messages et pour attacher la même signification aux numéros de message.

Les numéros de message dans la troisième plage (0x8000 à 0xBFFF) sont disponibles pour les applications à utiliser comme messages privés. Les messages de cette plage ne sont pas en conflit avec les messages système.

Les numéros de message dans la quatrième plage (0xC000 à 0xFFFF) sont définis au moment de l’exécution lorsqu’une application appelle la fonction [**RegisterWindowMessage**](/windows/win32/api/winuser/nf-winuser-registerwindowmessagea) pour récupérer un numéro de message pour une chaîne. Toutes les applications qui inscrivent la même chaîne peuvent utiliser le numéro de message associé à l’échange de messages. Toutefois, le numéro de message réel n’est pas une constante et ne peut pas être utilisé de la même façon entre différentes sessions.

Les numéros de message dans la cinquième plage (supérieure à 0xFFFF) sont réservés par le système.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                               |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Référence**
</dt> <dt>

[**RegisterWindowMessage**](/windows/win32/api/winuser/nf-winuser-registerwindowmessagea)
</dt> <dt>

[**\_utilisateur WM**](wm-user.md)
</dt> <dt>

**Méthodologique**
</dt> <dt>

[Messages et files d’attente de messages](messages-and-message-queues.md)
</dt> </dl>

 

 
