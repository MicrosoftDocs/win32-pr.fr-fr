---
title: Message WM_DDE_REQUEST (DDE. h)
description: une application cliente de échange dynamique de données (dde) envoie un \_ message de requête de l’échange de données (dde) WM \_ à une application de serveur dde pour demander la valeur d’un élément de données. Pour poster ce message, appelez la fonction PostMessage avec les paramètres suivants.
ms.assetid: 922452d2-455c-43e1-a8a8-e3c52b0fab51
keywords:
- WM_DDE_REQUEST des données de message Exchange
topic_type:
- apiref
api_name:
- WM_DDE_REQUEST
api_location:
- Dde.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 05c58877b15f39d2de907688972905e98007658981bcc57df62655634bafe8be
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118811349"
---
# <a name="wm_dde_request-message"></a>\_Message de \_ requête DDE WM

une application cliente de échange dynamique de données (dde) envoie un message de **\_ \_ requête** de l’échange de données (dde) WM à une application de serveur dde pour demander la valeur d’un élément de données.

Pour poster ce message, appelez la fonction [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) avec les paramètres suivants.


```C++
#define WM_DDE_REQUEST     0x03E6
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Handle de la fenêtre cliente qui envoie le message.

</dd> <dt>

*lParam* 
</dt> <dd>

Le mot de poids faible spécifie un format de presse-papiers standard ou inscrit.

Le mot de poids fort contient un atome qui identifie l’élément de données demandé par le serveur.

</dd> </dl>

## <a name="remarks"></a>Remarques

### <a name="posting"></a>Publication

L’application cliente alloue Atom en appelant la fonction [**GlobalAddAtom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma) .

### <a name="receiving"></a>Réception

Si l’application de réception (serveur) peut répondre à la demande, elle répond avec un message de [**\_ \_ données de l’échange WM**](wm-dde-data.md) contenant les données demandées. Dans le cas contraire, il répond avec un message d' [**\_ \_ accusé**](wm-dde-ack.md) de réception DDE négatif négatif.

Lorsque vous répondez avec un message de type de [**\_ \_ données DDE**](wm-dde-data.md) ou un message d' [**\_ \_ accusé**](wm-dde-ack.md) de réception DDE de WM, l’application serveur peut réutiliser l’Atom ou supprimer l’atome et en créer un nouveau.

## <a name="requirements"></a>Conditions requises



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                           |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                 |
| En-tête<br/>                   | <dl> <dt>Dde. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Référence**
</dt> <dt>

[**GlobalAddAtom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma)
</dt> <dt>

[**PackDDElParam**](/windows/desktop/api/Dde/nf-dde-packddelparam)
</dt> <dt>

[**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea)
</dt> <dt>

[**ReuseDDElParam**](/windows/desktop/api/Dde/nf-dde-reuseddelparam)
</dt> <dt>

[**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage)
</dt> <dt>

[**UnpackDDElParam**](/windows/desktop/api/Dde/nf-dde-unpackddelparam)
</dt> <dt>

[**\_ACK DDE \_ ACK**](wm-dde-ack.md)
</dt> <dt>

[**\_données DDE \_ WM**](wm-dde-data.md)
</dt> <dt>

**Méthodologique**
</dt> <dt>

[À propos de échange dynamique de données](about-dynamic-data-exchange.md)
</dt> </dl>

 

