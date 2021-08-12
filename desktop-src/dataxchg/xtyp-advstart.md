---
title: XTYP_ADVSTART transaction (Ddeml. h)
description: Un client utilise la \_ transaction XTYP ADVSTART pour établir une boucle de notification avec un serveur.
ms.assetid: 8911e722-5656-4ca6-8b0a-6bdf8281611a
keywords:
- XTYP_ADVSTART Exchange de données de transaction
topic_type:
- apiref
api_name:
- XTYP_ADVSTART
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb18bda3dce4db465045991e26cdc2d97ddd87ddc69c494ffaf103c566955da1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118544758"
---
# <a name="xtyp_advstart-transaction"></a>\_Transaction ADVSTART XTYP

Un client utilise la transaction **XTYP \_ ADVSTART** pour établir une boucle de notification avec un serveur. une fonction de rappel de serveur échange dynamique de données (DDE), [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), reçoit cette transaction lorsqu’un client spécifie **XTYP \_ ADVSTART** comme paramètre *wType* de la fonction [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction) .


```C++
#define     XCLASS_BOOL              0x1000
#define     XTYP_ADVSTART           (0x0030 | XCLASS_BOOL          )
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*uType* 
</dt> <dd>

Type de transaction.

</dd> <dt>

*uFmt* 
</dt> <dd>

Format de données demandé par le client.

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

## <a name="return-value"></a>Valeur retournée

Une fonction de rappel de serveur doit retourner **true** pour autoriser une boucle de notification sur le nom de rubrique et la paire de noms d’élément spécifiés, ou **false** pour refuser la boucle de notification. Si la fonction de rappel retourne la **valeur true**, tous les appels suivants à la fonction [**DdePostAdvise**](/windows/desktop/api/Ddeml/nf-ddeml-ddepostadvise) par le serveur sur les mêmes paires nom de rubrique et nom d’élément provoquent l’envoi de transactions [**\_ ADVREQ XTYP**](xtyp-advreq.md) au serveur par le système.

## <a name="remarks"></a>Remarques

si un client demande une boucle de notification sur un nom de rubrique, un nom d’élément et un format de données pour une boucle de notification déjà établie, la bibliothèque de gestion échange dynamique de données (DDEML) ne crée pas de boucle de notification en double, mais modifie à la place les indicateurs de boucle de notification (**XTYPF \_ ACKREQ** et **XTYPF \_ nodata**) pour qu’ils correspondent à la dernière requête.

Cette transaction est filtrée si l’application serveur a spécifié l’indicateur de **\_ \_ notifications d’échec CBF** dans la fonction [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) .

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

[**DdePostAdvise**](/windows/desktop/api/Ddeml/nf-ddeml-ddepostadvise)
</dt> <dt>

**Méthodologique**
</dt> <dt>

[bibliothèque de gestion des échange dynamique de données](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

