---
title: XTYP_POKE transaction (Ddeml. h)
description: Un client utilise la \_ transaction d’XTYPe pour envoyer des données non sollicitées au serveur. Une fonction de rappel de serveur échange dynamique de données (DDE), DdeCallback, reçoit cette transaction lorsqu’un client spécifie XTYP \_ dans la fonction DdeClientTransaction.
ms.assetid: 63c6115e-24f8-4f35-8397-8be63110b21f
keywords:
- Échange de données de transaction XTYP_POKE
topic_type:
- apiref
api_name:
- XTYP_POKE
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e538f72b7a736ed9be5cf3e1d83e8729f42ef83d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942039"
---
# <a name="xtyp_poke-transaction"></a>XTYP \_ transaction de journalisation

Un client utilise la **transaction \_ d’XTYPe** pour envoyer des données non sollicitées au serveur. Une fonction de rappel de serveur échange dynamique de données (DDE), [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), reçoit cette transaction lorsqu’un client spécifie **XTYP \_** dans la fonction [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction) .


```C++
#define     XCLASS_FLAGS             0x4000
#define     XTYP_POKE               (0x0090 | XCLASS_FLAGS         )
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*uType* 
</dt> <dd>

Type de transaction.

</dd> <dt>

*uFmt* 
</dt> <dd>

Format des données envoyées à partir du serveur.

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

Handle vers les données que le client envoie au serveur.

</dd> <dt>

*dwData1* 
</dt> <dd>

Non utilisé.

</dd> <dt>

*dwData2* 
</dt> <dd>

Non utilisé.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Une fonction de rappel de serveur doit retourner l’indicateur **\_ Fack DDE** si elle traite cette transaction, l’indicateur **DDE \_ FBUSY** s’il est trop occupé pour traiter cette transaction, ou l’indicateur **DDE \_ FNOTPROCESSED** s’il rejette cette transaction.

## <a name="remarks"></a>Notes

Cette transaction est filtrée si l’application serveur a spécifié l’indicateur d' **\_ \_ échec** de l’CBF dans la fonction [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) .

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

[**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction)
</dt> <dt>

[**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)
</dt> <dt>

**Méthodologique**
</dt> <dt>

[Bibliothèque de gestion des échange dynamique de données](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

