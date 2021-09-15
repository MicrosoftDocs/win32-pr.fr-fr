---
title: Message WM_DDE_TERMINATE (DDE. h)
description: une application échange dynamique de données (dde) (client ou serveur) publie un \_ message WM DDE \_ terminate pour mettre fin à une conversation. Pour poster ce message, appelez la fonction PostMessage avec les paramètres suivants.
ms.assetid: 4fc162c0-ccc2-44e3-9c07-d49d7426af8b
keywords:
- WM_DDE_TERMINATE des données de message Exchange
topic_type:
- apiref
api_name:
- WM_DDE_TERMINATE
api_location:
- Dde.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 105b4a7daab87b1311a58a7b5e5805bbd81e73ce
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127404087"
---
# <a name="wm_dde_terminate-message"></a>Message de fin du \_ DDE WM \_

une application échange dynamique de données (dde) (client ou serveur) publie un message **WM \_ DDE \_ terminate** pour mettre fin à une conversation.

Pour poster ce message, appelez la fonction [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) avec les paramètres suivants.


```C++
#define WM_DDE_TERMINATE       0x03E1
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Handle de la fenêtre du client ou du serveur qui publie le message.

</dd> <dt>

*lParam* 
</dt> <dd>

Ce paramètre n'est pas utilisé.

</dd> </dl>

## <a name="remarks"></a>Notes

### <a name="posting"></a>Publication

Lors de l’attente de la confirmation de la résiliation, l’application de publication ne doit pas publier d’autres messages dans l’application réceptrice. Si l’application émettrice reçoit des messages (autres **que \_ WM DDE \_ Terminate**) à partir de l’application réceptrice, elle doit supprimer tous les atomes ou objets de mémoire partagée qui accompagnent les messages, à l’exception des objets de mémoire globale associés à des messages de données d’interception [**\_ DDE \_**](wm-dde-poke.md) ou de [**\_ \_ données DDE WM**](wm-dde-data.md) qui n’ont pas de membre **fRelease** défini.

### <a name="receiving"></a>Réception

L’application cliente ou serveur doit répondre en publiant un message **WM \_ DDE \_ Terminate** .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                           |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                 |
| En-tête<br/>                   | <dl> <dt>Dde. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Référence**
</dt> <dt>

[**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea)
</dt> <dt>

[**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage)
</dt> <dt>

[**\_données DDE \_ WM**](wm-dde-data.md)
</dt> <dt>

[**en-dessous du protocole WM \_ DDE \_**](wm-dde-poke.md)
</dt> <dt>

**Conceptuel**
</dt> <dt>

[À propos de échange dynamique de données](about-dynamic-data-exchange.md)
</dt> </dl>

 

