---
title: XTYP_MONITOR transaction (Ddeml. h)
description: Une fonction de rappel DDE du débogueur échange dynamique de données (DDE), DdeCallback, reçoit la \_ transaction XTYP Monitor à chaque fois qu’un événement DDE se produit dans le système.
ms.assetid: a27791b1-c1b4-4516-b050-71da164fa80a
keywords:
- Échange de données de transaction XTYP_MONITOR
topic_type:
- apiref
api_name:
- XTYP_MONITOR
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e6a1cb86a1cbf7e0c02c082719e0a7d302d03975
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384435"
---
# <a name="xtyp_monitor-transaction"></a>XTYP \_ surveiller la transaction

Une fonction de rappel DDE du débogueur échange dynamique de données (DDE), [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), reçoit la transaction **XTYP \_ Monitor** à chaque fois qu’un événement DDE se produit dans le système. Pour recevoir cette transaction, une application doit spécifier la valeur du **\_ moniteur APPCLASS** quand elle appelle la fonction [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) .


```C++
#define     XCLASS_NOTIFICATION      0x8000
#define     XTYPF_NOBLOCK            0x0002
#define     XTYP_MONITOR            (0x00F0 | XCLASS_NOTIFICATION | XTYPF_NOBLOCK)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*uType* 
</dt> <dd>

Type de transaction.

</dd> <dt>

*uFmt* 
</dt> <dd>

Non utilisé.

</dd> <dt>

*hconv* 
</dt> <dd>

Non utilisé.

</dd> <dt>

*hsz1* 
</dt> <dd>

Non utilisé.

</dd> <dt>

*hsz2* 
</dt> <dd>

Non utilisé.

</dd> <dt>

*hdata* 
</dt> <dd>

Handle d’un objet DDE qui contient des informations sur l’événement DDE. L’application doit utiliser la fonction [**DdeAccessData**](/windows/desktop/api/Ddeml/nf-ddeml-ddeaccessdata) pour obtenir un pointeur vers l’objet.

</dd> <dt>

*dwData1* 
</dt> <dd>

Non utilisé.

</dd> <dt>

*dwData2* 
</dt> <dd>

Événement DDE. Ce paramètre peut prendre les valeurs suivantes.



| Valeur                                                                                                                                                                                                                      | Signification                                                                                                                                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MF_CALLBACKS"></span><span id="mf_callbacks"></span><dl> <dt>**MF \_ RAPPELs**</dt> <dt>0x08000000</dt> </dl> | Le système a envoyé une transaction à une fonction de rappel DDE. L’objet DDE contient une structure [**MONCBSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-moncbstruct) qui fournit des informations sur la transaction.<br/>                                                                                                                                               |
| <span id="MF_CONV"></span><span id="mf_conv"></span><dl> <dt>**MF \_ CONV**</dt> <dt>0x40000000</dt> </dl>                | Une conversation DDE a été établie ou terminée. L’objet DDE contient une structure [**MONCONVSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-monconvstruct) qui fournit des informations sur la conversation.<br/>                                                                                                                                                  |
| <span id="MF_ERRORS"></span><span id="mf_errors"></span><dl> <dt>**MF \_ Erreurs**</dt> <dt>0x10000000</dt> </dl>          | Une erreur DDE s’est produite. L’objet DDE contient une structure [**MONERRSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-monerrstruct) qui fournit des informations sur l’erreur.<br/>                                                                                                                                                                                       |
| <span id="MF_HSZ_INFO"></span><span id="mf_hsz_info"></span><dl> <dt>**MF \_ HSZ \_ info**</dt> <dt>0x01000000</dt> </dl>   | Une application DDE a créé, libérée ou incrémentée le nombre d’utilisations d’un handle de chaîne, ou un descripteur de chaîne a été libéré à la suite d’un appel à la fonction [**DdeUninitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeuninitialize) . L’objet DDE contient une structure [**MONHSZSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-monhszstructa) qui fournit des informations sur le handle de chaîne.<br/> |
| <span id="MF_LINKS"></span><span id="mf_links"></span><dl> <dt>**MF \_ Liens**</dt> <dt>0x20000000</dt> </dl>             | Une application DDE a démarré ou arrêté une boucle de notification. L’objet DDE contient une structure [**MONLINKSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-monlinkstruct) qui fournit des informations sur la boucle de notification.<br/>                                                                                                                                                |
| <span id="MF_POSTMSGS"></span><span id="mf_postmsgs"></span><dl> <dt>**MF \_ POSTMSGS**</dt> <dt>0x04000000</dt> </dl>    | Le système ou une application a publié un message DDE. L’objet DDE contient une structure [**MONMSGSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-monmsgstruct) qui fournit des informations sur le message.<br/>                                                                                                                                                        |
| <span id="MF_SENDMSGS"></span><span id="mf_sendmsgs"></span><dl> <dt>**MF \_ SENDMSGS**</dt> <dt>0x02000000</dt> </dl>    | Le système ou une application a envoyé un message DDE. L’objet DDE contient une structure [**MONMSGSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-monmsgstruct) qui fournit des informations sur le message.<br/>                                                                                                                                                          |



 

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction de rappel traite cette transaction, elle doit retourner 0.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                             |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                   |
| En-tête<br/>                   | <dl> <dt>Ddeml. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Référence**
</dt> <dt>

[**DdeAccessData**](/windows/desktop/api/Ddeml/nf-ddeml-ddeaccessdata)
</dt> <dt>

[**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)
</dt> <dt>

[**DdeUninitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeuninitialize)
</dt> <dt>

[**MONCBSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-moncbstruct)
</dt> <dt>

[**MONCONVSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-monconvstruct)
</dt> <dt>

[**MONERRSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-monerrstruct)
</dt> <dt>

[**MONHSZSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-monhszstructa)
</dt> <dt>

[**MONLINKSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-monlinkstruct)
</dt> <dt>

[**MONMSGSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-monmsgstruct)
</dt> <dt>

**Méthodologique**
</dt> <dt>

[Bibliothèque de gestion des échange dynamique de données](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

