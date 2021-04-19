---
title: Message WM_ADSPROP_NOTIFY_APPLY (Adsprop. h)
description: Une extension de feuille de propriétés de service de Active Directory Directory envoie le \_ \_ \_ message de notification d’application ADSPROP WM à l’objet de notification si la page de propriétés PSN \_ apply Handler a été établie.
ms.assetid: 3536054b-83ee-4cfa-ab54-c0af3a46289e
ms.tgt_platform: multiple
keywords:
- Message de WM_ADSPROP_NOTIFY_APPLY Active Directory
topic_type:
- apiref
api_name:
- WM_ADSPROP_NOTIFY_APPLY
api_location:
- Adsprop.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0ccd5bb95e3f092634d54ba0534e81ded6701bf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106543632"
---
# <a name="wm_adsprop_notify_apply-message"></a>\_Message d' \_ application de notification WM ADSPROP \_

Une extension de feuille de propriétés de service de Active Directory Directory envoie le message de notification d' **\_ \_ \_ application ADSPROP WM** à l’objet de notification si la page de propriétés PSN \_ apply Handler a été établie.


```C++
WM_ADSPROP_NOTIFY_APPLY

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

## <a name="return-value"></a>Valeur retournée

Ce message n’a pas de valeur de retour.

## <a name="remarks"></a>Notes

Lorsque vous ajoutez des pages au composant logiciel enfichable MMC Active Directory Manager, Active Directory feuilles de propriétés MMC créent les objets de notification par un appel à la fonction [**ADsPropCreateNotifyObj**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj) , puis passe le handle d’objet de notification à chaque page de propriétés.

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

 

 





