---
title: XTYP_DISCONNECT transaction (Ddeml. h)
description: La fonction de rappel échange dynamique de données (DDE) d’une application, DdeCallback, reçoit la \_ transaction de déconnexion XTYP lorsque le partenaire de l’application dans une conversation utilise la fonction DdeDisconnect pour mettre fin à la conversation.
ms.assetid: 22a9ec63-8a74-4829-ad02-d07dd0e8fa9b
keywords:
- Échange de données de transaction XTYP_DISCONNECT
topic_type:
- apiref
api_name:
- XTYP_DISCONNECT
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 38e73bc0446989ac572a27f394e594924573711d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740332"
---
# <a name="xtyp_disconnect-transaction"></a>XTYP \_ déconnecter la transaction

La fonction de rappel échange dynamique de données (DDE) d’une application, [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), reçoit la transaction de **\_ déconnexion XTYP** lorsque le partenaire de l’application dans une conversation utilise la fonction [**DdeDisconnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddedisconnect) pour mettre fin à la conversation.


```C++
#define     XCLASS_NOTIFICATION      0x8000
#define     XTYPF_NOBLOCK            0x0002
#define     XTYP_DISCONNECT         (0x00C0 | XCLASS_NOTIFICATION | XTYPF_NOBLOCK)
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

Handle vers la fin de la conversation.

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

Non utilisé.

</dd> <dt>

*dwData1* 
</dt> <dd>

Non utilisé.

</dd> <dt>

*dwData2* 
</dt> <dd>

Spécifie si les partenaires de la conversation sont la même instance d’application. Si ce paramètre est égal à 1, les partenaires sont la même instance. Si ce paramètre a la valeur 0, les partenaires sont des instances différentes.

</dd> </dl>

## <a name="remarks"></a>Notes

Cette transaction est filtrée si l’application a spécifié l’indicateur **CBF \_ Skip \_ deconnections** dans la fonction [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) .

L’application peut obtenir l’état de la conversation terminée en appelant la fonction [**DdeQueryConvInfo**](/windows/desktop/api/Ddeml/nf-ddeml-ddequeryconvinfo) lors du traitement de cette transaction. Le descripteur de conversation devient non valide après le retour de la fonction de rappel.

Une application ne peut pas bloquer ce type de transaction ; le code de retour de **\_ bloc CBR** est ignoré.

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

[**DdeDisconnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddedisconnect)
</dt> <dt>

[**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)
</dt> <dt>

[**DdeQueryConvInfo**](/windows/desktop/api/Ddeml/nf-ddeml-ddequeryconvinfo)
</dt> <dt>

**Méthodologique**
</dt> <dt>

[Bibliothèque de gestion des échange dynamique de données](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

