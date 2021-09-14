---
title: Message WM_DDE_UNADVISE (DDE. h)
description: une application cliente de échange dynamique de données (dde) publie \_ un \_ message de notification d’inversion dde WM pour informer une application serveur dde que l’élément spécifié ou un format de presse-papiers particulier pour l’élément ne doit plus être mis à jour.
ms.assetid: 9a5f9a86-e6fa-450e-b8bf-f20042c7e6d1
keywords:
- WM_DDE_UNADVISE des données de message Exchange
topic_type:
- apiref
api_name:
- WM_DDE_UNADVISE
api_location:
- Dde.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dba83badcb689789d2654d99780bcb8cc503511d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127193016"
---
# <a name="wm_dde_unadvise-message"></a>\_Message d' \_ innotification DDE

une application cliente de échange dynamique de données (dde) publie un message de **\_ \_ notification** d’inversion dde WM pour informer une application serveur dde que l’élément spécifié ou un format de presse-papiers particulier pour l’élément ne doit plus être mis à jour. Cela met fin au lien de données chaud ou chaud pour l’élément spécifié.

Pour poster ce message, appelez la fonction [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) avec les paramètres suivants.


```C++
#define WM_DDE_UNADVISE        0x03E3
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Handle de la fenêtre cliente qui envoie le message.

</dd> <dt>

*lParam* 
</dt> <dd>

Le mot de poids faible spécifie le format du presse-papiers de l’élément pour lequel la demande de mise à jour est retirée. Si la **valeur est null**, toutes les conversations de [**\_ \_ notifications WM DDE**](wm-dde-advise.md) actives pour l’élément doivent être arrêtées.

Le mot de poids fort contient un atome global qui identifie l’élément pour lequel la demande de mise à jour est retirée. Si la **valeur est null**, tous les liens de [**\_ \_ notification WM DDE**](wm-dde-advise.md) actifs associés à la conversation doivent être terminés.

</dd> </dl>

## <a name="remarks"></a>Notes

L’application cliente alloue le mot de poids fort de *lParam* en appelant la fonction [**GlobalAddAtom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma) .

L’application serveur publie le message d’accusé de réception [**\_ DDE DDE \_**](wm-dde-ack.md) pour répondre positivement ou négativement. Lors de la publication d’un accusé de réception **\_ DDE DDE \_**, le serveur peut réutiliser l’Atom, ou il peut supprimer l’atome et en créer un nouveau.

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

[**\_avis DDE \_ WM**](wm-dde-advise.md)
</dt> <dt>

**Conceptuel**
</dt> <dt>

[À propos de échange dynamique de données](about-dynamic-data-exchange.md)
</dt> </dl>

 

