---
title: XTYP_CONNECT_CONFIRM transaction (Ddeml. h)
description: une fonction de rappel de serveur échange dynamique de données (DDE), DdeCallback, reçoit \_ la \_ transaction XTYP CONNECT CONFIRM pour confirmer qu’une conversation a été établie avec un client et pour fournir au serveur le descripteur de conversation.
ms.assetid: 4db67539-9322-44d7-bf2b-749bd6cfcbb4
keywords:
- XTYP_CONNECT_CONFIRM Exchange de données de transaction
topic_type:
- apiref
api_name:
- XTYP_CONNECT_CONFIRM
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e880dfffc7f7825c99ab9e4e3bf980baa978b786
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126922836"
---
# <a name="xtyp_connect_confirm-transaction"></a>Transaction de confirmation de \_ connexion XTYP \_

une fonction de rappel de serveur échange dynamique de données (DDE), [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), reçoit la transaction **XTYP \_ CONNECT \_ CONFIRM** pour confirmer qu’une conversation a été établie avec un client et pour fournir au serveur le descripteur de conversation. Le système envoie cette transaction à la suite d’une transaction [**XTYP \_ Connect**](xtyp-connect.md) ou [**XTYP \_ WILDCONNECT**](xtyp-wildconnect.md) précédente.


```C++
#define     XTYPF_NOBLOCK            0x0002
#define     XCLASS_NOTIFICATION      0x8000
#define     XTYP_CONNECT_CONFIRM    (0x0070 | XCLASS_NOTIFICATION | XTYPF_NOBLOCK)
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

Handle de la nouvelle conversation.

</dd> <dt>

*hsz1* 
</dt> <dd>

Handle vers le nom de la rubrique sur laquelle la conversation a été établie.

</dd> <dt>

*hsz2* 
</dt> <dd>

Handle vers le nom du service sur lequel la conversation a été établie.

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

Spécifie si le client est la même instance d’application que le serveur. Si le paramètre est égal à 1, le client est la même instance. Si le paramètre a la valeur 0, le client est une instance différente.

</dd> </dl>

## <a name="remarks"></a>Notes

Cette transaction est filtrée si l’application serveur a spécifié l’indicateur **CBF \_ Skip \_ Connect \_ Confirm** dans la fonction [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) .

Un serveur ne peut pas bloquer ce type de transaction ; le code de retour de **\_ bloc CBR** est ignoré.

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

[**DdeConnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect)
</dt> <dt>

[**DdeConnectList**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist)
</dt> <dt>

[**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)
</dt> <dt>

**Conceptuel**
</dt> <dt>

[bibliothèque de gestion des échange dynamique de données](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

