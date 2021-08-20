---
title: XTYP_UNREGISTER transaction (Ddeml. h)
description: une fonction de rappel échange dynamique de données (DDE), DdeCallback, reçoit la \_ transaction d’annulation d’inscription XTYP chaque fois qu’une application serveur de bibliothèque de gestion des échange dynamique de données (DDEML) utilise la fonction DdeNameService pour annuler l’inscription d’un nom de service, ou chaque fois qu’une application non DDEML qui prend en charge la rubrique système est terminée.
ms.assetid: a57a5d53-7919-4698-8c84-6142dd29bb2a
keywords:
- XTYP_UNREGISTER Exchange de données de transaction
topic_type:
- apiref
api_name:
- XTYP_UNREGISTER
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c3ddce7528f24c5ee9e6f4364448ebaf473a48e1be5547d71338cee4fc45d688
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118102005"
---
# <a name="xtyp_unregister-transaction"></a>XTYP \_ Annuler l’inscription de la transaction

une fonction de rappel échange dynamique de données (DDE), [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), reçoit la transaction d' **annulation d' \_ inscription XTYP** chaque fois qu’une application serveur de bibliothèque de gestion des échange dynamique de données (DDEML) utilise la fonction [**DdeNameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice) pour annuler l’inscription d’un nom de service, ou chaque fois qu’une application non DDEML qui prend en charge la rubrique système est terminée.


```C++
#define     XCLASS_NOTIFICATION      0x8000
#define     XTYPF_NOBLOCK            0x0002
#define     XTYP_UNREGISTER         (0x00D0 | XCLASS_NOTIFICATION | XTYPF_NOBLOCK)
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

Handle vers le nom du service de base en cours d’annulation de l’inscription.

</dd> <dt>

*hsz2* 
</dt> <dd>

Handle vers le nom de service spécifique à l’instance qui est désinscrit.

</dd> <dt>

*hdata* 
</dt> <dd>

Non utilisé.

</dd> <dt>

*dwData1* 
</dt> <dd>

Non utilisé.

</dd> <dt>

*dwData2* 
</dt> <dd>

Non utilisé.

</dd> </dl>

## <a name="remarks"></a>Remarques

Cette transaction est filtrée si l’application a spécifié l’indicateur **\_ \_ d’omission des inscriptions CBF** dans la fonction [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) .

Une application ne peut pas bloquer ce type de transaction ; le \_ Code de retour de bloc CBR est ignoré.

Une application doit utiliser le paramètre *HSZ1* pour supprimer le nom du service de la liste des serveurs disponibles pour l’utilisateur. Une application doit utiliser le paramètre *hsz2* pour identifier l’instance d’application qui s’est arrêtée.

## <a name="requirements"></a>Conditions requises



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                             |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                   |
| En-tête<br/>                   | <dl> <dt>Ddeml. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Référence**
</dt> <dt>

[**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)
</dt> <dt>

[**DdeNameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice)
</dt> <dt>

**Méthodologique**
</dt> <dt>

[bibliothèque de gestion des échange dynamique de données](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

