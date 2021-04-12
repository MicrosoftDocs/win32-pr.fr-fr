---
title: Message WM_DDE_INITIATE (DDE. h)
description: Une application cliente échange dynamique de données (DDE) envoie un \_ message de lancement de l’échange de messages (DDE) WM \_ pour initier une conversation avec une application serveur qui répond aux noms d’application et de rubrique spécifiés.
ms.assetid: d486f584-75a3-4ffd-ba5d-f95f2692cd6c
keywords:
- WM_DDE_INITIATE l’échange de données de message
topic_type:
- apiref
api_name:
- WM_DDE_INITIATE
api_location:
- Dde.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 36485db262c46d5364ee0ee26e7e6f39ccf0e677
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384519"
---
# <a name="wm_dde_initiate-message"></a>\_Message de lancement DDE de WM \_

Une application cliente échange dynamique de données (DDE) envoie un message de **\_ \_ lancement** de l’échange de messages (DDE) WM pour initier une conversation avec une application serveur qui répond aux noms d’application et de rubrique spécifiés. Lors de la réception de ce message, toutes les applications serveur avec des noms qui correspondent à l’application spécifiée et qui prennent en charge la rubrique spécifiée sont censées la reconnaître. (Pour plus d’informations, consultez le message d' [**\_ \_ accusé**](wm-dde-ack.md) de réception DDE de WM.)


```C++
#define WM_DDE_INITIATE        0x03E0
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Handle de la fenêtre cliente qui envoie le message.

</dd> <dt>

*lParam* 
</dt> <dd>

Le mot de poids faible contient un atome qui identifie l’application avec laquelle une conversation est demandée. Le nom de l’application ne peut pas contenir de barres obliques (/) ou de barres obliques inverses ( \) . Ces caractères sont réservés aux implémentations réseau. Si ce paramètre a la **valeur null**, une conversation avec toutes les applications est demandée.

Le mot de poids fort contient un atome qui identifie la rubrique pour laquelle une conversation est demandée. Si la rubrique est **null**, les conversations pour toutes les rubriques disponibles sont demandées.

</dd> </dl>

## <a name="remarks"></a>Notes

Si le mot de poids faible de *lParam* est **null**, toute application serveur peut répondre. Si le mot de poids fort de *lParam* est **null**, toute rubrique est valide. Lors de la réception d’une requête de **\_ \_ lancement DDE WM** avec le mot de poids fort du paramètre *lParam* défini sur **null**, un serveur doit envoyer un message d' [**\_ \_ accusé**](wm-dde-ack.md) de réception DDE pour chacune des rubriques qu’il prend en charge.

### <a name="sending"></a>Envoi

Le client diffuse le message à toutes les fenêtres de niveau supérieur en définissant le premier paramètre de [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) sur la **\_ diffusion HWND**.

Si l’application cliente a déjà obtenu le descripteur de fenêtre du serveur souhaité, elle peut envoyer un lancement de l' **\_ échange de \_ liaison** de script WM directement à la fenêtre du serveur en passant le handle de fenêtre du serveur comme premier paramètre de [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage).

L’application cliente alloue des atomes en appelant la fonction [**GlobalAddAtom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma) .

Lorsque [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) retourne, l’application cliente doit supprimer les atomes.

### <a name="receiving"></a>Réception

Pour terminer l’initiation d’une conversation, l’application serveur doit répondre avec un ou plusieurs messages de l' [**\_ \_ accusé**](wm-dde-ack.md) de réception DDE de WM, où chaque message est destiné à une rubrique distincte. Lors de l’envoi d’un message d' **\_ \_ accusé** de réception DDE, le serveur doit créer des atomes ; il ne doit pas réutiliser les atomes envoyés avec l' **\_ \_ initialisation DDE WM**.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                           |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                 |
| En-tête<br/>                   | <dl> <dt>DDE. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Référence**
</dt> <dt>

[**GlobalAddAtom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma)
</dt> <dt>

[**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea)
</dt> <dt>

[**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage)
</dt> <dt>

[**\_ACK DDE \_ ACK**](wm-dde-ack.md)
</dt> <dt>

**Méthodologique**
</dt> <dt>

[À propos de échange dynamique de données](about-dynamic-data-exchange.md)
</dt> </dl>

 

