---
title: Message WM_ADSPROP_NOTIFY_PAGEINIT (Adsprop. h)
description: Une Active Directory extension de la feuille de propriétés appelle le ADsPropGetInitInfo pour obtenir des informations sur l’objet d’annuaire auquel s’applique l’extension de la feuille de propriétés.
ms.assetid: 473c5a75-d0d9-4d12-b855-63683e8cdf3f
ms.tgt_platform: multiple
keywords:
- Message de WM_ADSPROP_NOTIFY_PAGEINIT Active Directory
topic_type:
- apiref
api_name:
- WM_ADSPROP_NOTIFY_PAGEINIT
api_location:
- Adsprop.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2718ee30cdbecec7c4e0954636aa14c75f13027
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508457"
---
# <a name="wm_adsprop_notify_pageinit-message"></a>\_Message WM ADSPROP \_ Notify \_ PAGEINIT

Une Active Directory extension de la feuille de propriétés appelle le [**ADsPropGetInitInfo**](/windows/desktop/api/Adsprop/nf-adsprop-adspropgetinitinfo) pour obtenir des informations sur l’objet d’annuaire auquel s’applique l’extension de la feuille de propriétés. La fonction **ADsPropGetInitInfo** envoie le message **WM \_ ADSPROP \_ Notify \_ PAGEINIT** à l’objet de notification pour obtenir ce résultat.


```C++
WM_ADSPROP_NOTIFY_PAGEINIT

    WPARAM wParam
    LPARAM pADsPropInitParams
    
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*HWND* 
</dt> <dd>

Handle de l’objet de notification. Il s’agit du paramètre *hNotifyObject* obtenu par un appel à [**ADsPropCreateNotifyObj**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj).

</dd> <dt>

*wParam* 
</dt> <dd>

Non utilisé.

</dd> <dt>

*pADsPropInitParams* 
</dt> <dd>

Pointeur vers une structure [**ADSPROPINITPARAMS**](/windows/desktop/api/Adsprop/ns-adsprop-adspropinitparams) qui reçoit les informations de l’objet d’annuaire. Il s’agit du paramètre *pInitParams* passé à [**ADsPropCreateNotifyObj**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Ce message n’a pas de valeur de retour.

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

[**ADsPropGetInitInfo**](/windows/desktop/api/Adsprop/nf-adsprop-adspropgetinitinfo)
</dt> <dt>

[**ADSPROPINITPARAMS**](/windows/desktop/api/Adsprop/ns-adsprop-adspropinitparams)
</dt> </dl>

 

 





