---
title: Message WM_ADSPROP_NOTIFY_ERROR (Adsprop. h)
description: Le \_ \_ \_ message d’erreur WM ADSPROP Notify ajoute un message d’erreur à la liste des messages d’erreur affichés en appelant la fonction ADsPropShowErrorDialog.
ms.assetid: 7abf1b3d-5abe-42cd-baeb-1bf863c7f04d
ms.tgt_platform: multiple
keywords:
- Message de WM_ADSPROP_NOTIFY_ERROR Active Directory
topic_type:
- apiref
api_name:
- WM_ADSPROP_NOTIFY_ERROR
api_location:
- Adsprop.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 52f88cd4c60dcfcceed60ca644f7c59f65bee16e344cc17664e8b4be1ee18fab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119024287"
---
# <a name="wm_adsprop_notify_error-message"></a>\_Message d' \_ erreur de notification WM ADSPROP \_

Le message d' **\_ \_ \_ erreur WM ADSPROP Notify** ajoute un message d’erreur à la liste des messages d’erreur affichés en appelant la fonction [**ADsPropShowErrorDialog**](/windows/desktop/api/Adsprop/nf-adsprop-adspropshowerrordialog) .


```C++
WM_ADSPROP_NOTIFY_ERROR

    WPARAM wParam
    LPARAM lParam
    
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*HWND* 
</dt> <dd>

Handle de l’objet de notification. Il s’agit du paramètre *hNotifyObject* obtenu par [**ADsPropCreateNotifyObj**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj).

</dd> <dt>

*wParam* 
</dt> <dd>

Non utilisé.

</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**ADSPROPERROR**](/windows/desktop/api/Adsprop/ns-adsprop-adsproperror) qui contient les données de message d’erreur.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Ce message n’a pas de valeur de retour.

## <a name="remarks"></a>Remarques

La fonction [**ADsPropSendErrorMessage**](/windows/desktop/api/Adsprop/nf-adsprop-adspropsenderrormessage) est la méthode recommandée pour envoyer ce message.

Les messages d’erreur ajoutés par le message d' **\_ \_ \_ erreur de notification WM ADSPROP** sont accumulés jusqu’à ce que [**ADsPropShowErrorDialog**](/windows/desktop/api/Adsprop/nf-adsprop-adspropshowerrordialog) soit appelé. **ADsPropShowErrorDialog** combine et affiche les messages d’erreur accumulés. Quand la boîte de dialogue d’erreur est fermée, les messages d’erreur accumulés sont supprimés.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                             |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                       |
| En-tête<br/>                   | <dl> <dt>Adsprop. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Messages dans Active Directory Domain Services](messages-in-active-directory-domain-services.md)
</dt> <dt>

[**ADSPROPERROR**](/windows/desktop/api/Adsprop/ns-adsprop-adsproperror)
</dt> <dt>

[**ADsPropSendErrorMessage**](/windows/desktop/api/Adsprop/nf-adsprop-adspropsenderrormessage)
</dt> <dt>

[**ADsPropShowErrorDialog**](/windows/desktop/api/Adsprop/nf-adsprop-adspropshowerrordialog)
</dt> </dl>

 

 





