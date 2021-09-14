---
title: XTYP_ADVSTOP transaction (Ddeml. h)
description: Un client utilise la \_ transaction XTYP ADVSTOP pour mettre fin à une boucle de notification avec un serveur. une fonction de rappel de serveur échange dynamique de données (DDE), DdeCallback, reçoit cette transaction lorsqu’un client spécifie XTYP \_ ADVSTOP dans la fonction DdeClientTransaction.
ms.assetid: 67dfa463-6a44-43a5-93be-a39c19c87c1c
keywords:
- XTYP_ADVSTOP Exchange de données de transaction
topic_type:
- apiref
api_name:
- XTYP_ADVSTOP
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61292683377cd6c7243c3e41c5dbd9332a671163
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126922839"
---
# <a name="xtyp_advstop-transaction"></a>\_Transaction ADVSTOP XTYP

Un client utilise la transaction **XTYP \_ ADVSTOP** pour mettre fin à une boucle de notification avec un serveur. une fonction de rappel de serveur échange dynamique de données (DDE), [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), reçoit cette transaction lorsqu’un client spécifie **XTYP \_ ADVSTOP** dans la fonction [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction) .


```C++
#define     XCLASS_NOTIFICATION      0x8000
#define     XTYP_ADVSTOP            (0x0040 | XCLASS_NOTIFICATION)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*uType* 
</dt> <dd>

Type de transaction.

</dd> <dt>

*uFmt* 
</dt> <dd>

Le format de données associé à la boucle de notification est terminé.

</dd> <dt>

*hconv* 
</dt> <dd>

Handle de la conversation.

</dd> <dt>

*hsz1* 
</dt> <dd>

Handle vers le nom de la rubrique.

</dd> <dt>

*hsz2* 
</dt> <dd>

Handle du nom de l’élément.

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

Cette transaction est filtrée si l’application serveur a spécifié l’indicateur de **\_ \_ notifications d’échec CBF** dans la fonction [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                             |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                   |
| En-tête<br/>                   | <dl> <dt>Ddeml. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Référence**
</dt> <dt>

[**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction)
</dt> <dt>

[**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)
</dt> <dt>

[**DdePostAdvise**](/windows/desktop/api/Ddeml/nf-ddeml-ddepostadvise)
</dt> <dt>

**Conceptuel**
</dt> <dt>

[bibliothèque de gestion des échange dynamique de données](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

