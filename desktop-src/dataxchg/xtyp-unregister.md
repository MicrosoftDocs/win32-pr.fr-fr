---
title: XTYP_UNREGISTER transaction (Ddeml. h)
description: Une fonction de rappel échange dynamique de données (DDE), DdeCallback, reçoit la \_ transaction d’annulation d’inscription XTYP chaque fois qu’une application serveur de bibliothèque de gestion des échange dynamique de données (Ddeml) utilise la fonction DdeNameService pour annuler l’inscription d’un nom de service, ou chaque fois qu’une application non Ddeml qui prend en charge la rubrique système est terminée.
ms.assetid: a57a5d53-7919-4698-8c84-6142dd29bb2a
keywords:
- Échange de données de transaction XTYP_UNREGISTER
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
ms.openlocfilehash: eeba96b26c019aa0a3050a83f726745b749efa96
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742869"
---
# <a name="xtyp_unregister-transaction"></a>XTYP \_ Annuler l’inscription de la transaction

Une fonction de rappel échange dynamique de données (DDE), [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), reçoit la transaction d' **annulation d' \_ inscription XTYP** chaque fois qu’une application serveur de bibliothèque de gestion des échange dynamique de données (Ddeml) utilise la fonction [**DdeNameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice) pour annuler l’inscription d’un nom de service, ou chaque fois qu’une application non Ddeml qui prend en charge la rubrique système est terminée.


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

## <a name="remarks"></a>Notes

Cette transaction est filtrée si l’application a spécifié l’indicateur **\_ \_ d’omission des inscriptions CBF** dans la fonction [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) .

Une application ne peut pas bloquer ce type de transaction ; le \_ Code de retour de bloc CBR est ignoré.

Une application doit utiliser le paramètre *HSZ1* pour supprimer le nom du service de la liste des serveurs disponibles pour l’utilisateur. Une application doit utiliser le paramètre *hsz2* pour identifier l’instance d’application qui s’est arrêtée.

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

[**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)
</dt> <dt>

[**DdeNameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice)
</dt> <dt>

**Méthodologique**
</dt> <dt>

[Bibliothèque de gestion des échange dynamique de données](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

