---
title: XTYP_REGISTER transaction (Ddeml. h)
description: une fonction de rappel échange dynamique de données (DDE), DdeCallback, reçoit le \_ type de transaction XTYP REGISTER chaque fois qu’une application serveur de bibliothèque de gestion des échange dynamique de données (DDEML) utilise la fonction DdeNameService pour inscrire un nom de service, ou chaque fois qu’une application non DDEML qui prend en charge la rubrique système est démarrée.
ms.assetid: 465e9c10-1526-4e2a-8a46-5984043f5a93
keywords:
- XTYP_REGISTER Exchange de données de transaction
topic_type:
- apiref
api_name:
- XTYP_REGISTER
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79c4ffdb48b7a69109659e65d816b4ab146a1f38bde976e7f8330746f564bc64
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118544748"
---
# <a name="xtyp_register-transaction"></a>\_Transaction Register XTYP

une fonction de rappel échange dynamique de données (DDE), [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), reçoit le type de transaction **XTYP \_ REGISTER** chaque fois qu’une application serveur de bibliothèque de gestion des échange dynamique de données (DDEML) utilise la fonction [**DdeNameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice) pour inscrire un nom de service, ou chaque fois qu’une application non DDEML qui prend en charge la rubrique système est démarrée.


```C++
#define     XCLASS_NOTIFICATION      0x8000
#define     XTYPF_NOBLOCK            0x0002
#define     XTYP_REGISTER           (0x00A0 | XCLASS_NOTIFICATION | XTYPF_NOBLOCK)
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

Handle vers le nom de service de base en cours d’enregistrement.

</dd> <dt>

*hsz2* 
</dt> <dd>

Handle vers le nom de service spécifique à l’instance en cours d’enregistrement.

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

Une application ne peut pas bloquer ce type de transaction ; le code de retour de **\_ bloc CBR** est ignoré.

Une application doit utiliser le paramètre *HSZ1* pour ajouter le nom du service à la liste des serveurs disponibles pour l’utilisateur. Une application doit utiliser le paramètre *hsz2* pour identifier l’instance d’application qui a démarré.

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

[bibliothèque de gestion des échange dynamique de données](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

