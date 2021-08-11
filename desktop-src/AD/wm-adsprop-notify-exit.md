---
title: Message WM_ADSPROP_NOTIFY_EXIT (Adsprop. h)
description: Une extension de feuille de propriétés Active Directory envoie \_ le \_ \_ message de sortie de notification WM ADSPROP à l’objet de notification lorsque l’objet de notification n’est plus nécessaire.
ms.assetid: b0f58c73-8953-412d-b801-bf34967fe0b4
ms.tgt_platform: multiple
keywords:
- Message de WM_ADSPROP_NOTIFY_EXIT Active Directory
topic_type:
- apiref
api_name:
- WM_ADSPROP_NOTIFY_EXIT
api_location:
- Adsprop.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e144bb0b24112cabe1a806d4c746aac07708443665c0f457df8756be36d80b0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118181963"
---
# <a name="wm_adsprop_notify_exit-message"></a>\_Message de \_ sortie de notification WM ADSPROP \_

Une extension de feuille de propriétés Active Directory envoie le message de **\_ \_ \_ sortie de notification WM ADSPROP** à l’objet de notification lorsque l’objet de notification n’est plus nécessaire.


```C++
WM_ADSPROP_NOTIFY_EXIT

    WPARAM wParam
    LPARAM lParam
    
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*HWND* 
</dt> <dd>

Handle de l’objet de notification. Pour obtenir ce handle, appelez [**ADsPropCreateNotifyObj**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj).

</dd> <dt>

*wParam* 
</dt> <dd>

Non utilisé.

</dd> <dt>

*lParam* 
</dt> <dd>

Non utilisé.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Ce message n’a pas de valeur de retour.

## <a name="remarks"></a>Notes

L’objet de notification se supprime lui-même en réponse à ce message. Lorsque ce message a été envoyé, le descripteur d’objet de notification doit être considéré comme non valide.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                             |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                       |
| En-tête<br/>                   | <dl> <dt>Adsprop. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ADsPropCreateNotifyObj**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj)
</dt> <dt>

[Messages dans Active Directory Domain Services](messages-in-active-directory-domain-services.md)
</dt> </dl>

 

 





