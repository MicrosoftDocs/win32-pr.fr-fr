---
title: Message WM_ADSPROP_NOTIFY_PAGEHWND (Adsprop. h)
description: Une extension de feuille de propriétés de service d’annuaire Active Directory appelle ADsPropSetHwnd pour informer l’objet de notification du handle de fenêtre de la page de propriétés.
ms.assetid: eb8bf525-cd7f-44d0-a0f9-43178a29c443
ms.tgt_platform: multiple
keywords:
- Message de WM_ADSPROP_NOTIFY_PAGEHWND Active Directory
topic_type:
- apiref
api_name:
- WM_ADSPROP_NOTIFY_PAGEHWND
api_location:
- Adsprop.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2835b4e0ff878b4c747f8c34b983beb3d66c550008a82ecadb2e5a23667abc8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118181730"
---
# <a name="wm_adsprop_notify_pagehwnd-message"></a>\_Message WM ADSPROP \_ Notify \_ PAGEHWND

Une extension de feuille de propriétés de service d’annuaire Active Directory appelle [**ADsPropSetHwnd**](/windows/desktop/api/Adsprop/nf-adsprop-adspropsethwnd) pour informer l’objet de notification du handle de fenêtre de la page de propriétés. La fonction **ADsPropSetHwnd** envoie le message **WM \_ ADSPROP \_ Notify \_ PAGEHWND** à l’objet de notification, qui informe l’objet de notification du handle de fenêtre de la page de propriétés.


```C++
WM_ADSPROP_NOTIFY_PAGEHWND

    WPARAM hPage
    LPARAM ptzTitle
    
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hNotifyObj* 
</dt> <dd>

Handle de l’objet de notification. Pour obtenir ce handle, appelez [**ADsPropCreateNotifyObj**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj).

</dd> <dt>

*hPage* 
</dt> <dd>

Handle de fenêtre de la page de propriétés.

</dd> <dt>

*ptzTitle* 
</dt> <dd>

Pointeur vers une mémoire tampon **WCHAR** se terminant par un caractère null qui contient le titre de la page de propriétés.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Ce message n’a pas de valeur de retour.

## <a name="remarks"></a>Notes

Une Active Directory extension de la feuille de propriétés appelle normalement la fonction [**ADsPropSetHwnd**](/windows/desktop/api/Adsprop/nf-adsprop-adspropsethwnd) lors du traitement du message [**WM \_ INITDIALOG**](../dlgbox/wm-initdialog.md) .

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

[**ADsPropSetHwnd**](/windows/desktop/api/Adsprop/nf-adsprop-adspropsethwnd)
</dt> <dt>

[**ADsPropCreateNotifyObj**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj)
</dt> <dt>

[**\_INITDIALOG WM**](../dlgbox/wm-initdialog.md)
</dt> </dl>

 

