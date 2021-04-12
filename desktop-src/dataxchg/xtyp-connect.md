---
title: XTYP_CONNECT transaction (Ddeml. h)
description: Un client utilise la \_ transaction XTYP Connect pour établir une conversation.
ms.assetid: 74f43b10-f7ac-4370-9caa-7b9ddf3413ed
keywords:
- Échange de données de transaction XTYP_CONNECT
topic_type:
- apiref
api_name:
- XTYP_CONNECT
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e2268994f1be000373691d6c25dbb7220d3e109e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104077"
---
# <a name="xtyp_connect-transaction"></a>\_Transaction XTYP Connect

Un client utilise la transaction **XTYP \_ Connect** pour établir une conversation. Une fonction de rappel de serveur échange dynamique de données (DDE), [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), reçoit cette transaction lorsqu’un client spécifie un nom de service que le serveur prend en charge (et un nom de rubrique qui n’a pas la **valeur null**) dans un appel à la fonction [**DdeConnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect) .


```C++
#define     XCLASS_BOOL              0x1000
#define     XTYPF_NOBLOCK            0x0002
#define     XTYP_CONNECT            (0x0060 | XCLASS_BOOL | XTYPF_NOBLOCK)
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

Handle vers le nom de la rubrique.

</dd> <dt>

*hsz2* 
</dt> <dd>

Handle vers le nom du service.

</dd> <dt>

*hdata* 
</dt> <dd>

Non utilisé.

</dd> <dt>

*dwData1* 
</dt> <dd>

Pointeur vers une structure [**CONVCONTEXT**](/windows/win32/api/ddeml/ns-ddeml-convcontext) qui contient des informations de contexte pour la conversation. Si le client n’est pas une application DDEML, ce paramètre est 0.

</dd> <dt>

*dwData2* 
</dt> <dd>

Spécifie si le client est la même instance d’application que le serveur. Si le paramètre est égal à 1, le client est la même instance. Si le paramètre a la valeur 0, le client est une instance différente.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Une fonction de rappel de serveur doit retourner la **valeur true** pour permettre au client d’établir une conversation sur la paire de noms de services et de rubriques spécifiée, ou la fonction doit retourner **false** pour refuser la conversation. Si la fonction de rappel retourne la **valeur true** et qu’une conversation est correctement établie, le système transmet le descripteur de conversation au serveur en émettant une transaction [**\_ \_ Confirm XTYP Connect**](xtyp-connect-confirm.md) à la fonction de rappel du serveur (à moins que le serveur n’ait spécifié l’indicateur **CBF \_ Skip \_ Connect \_ Confirm** dans la fonction [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) ).

## <a name="remarks"></a>Notes

Cette transaction est filtrée si l’application serveur a spécifié l’indicateur **CBF \_ Fail \_ connections** dans la fonction [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) .

Un serveur ne peut pas bloquer ce type de transaction ; le code de retour de **\_ bloc CBR** est ignoré.

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

[**CONVCONTEXT**](/windows/win32/api/ddeml/ns-ddeml-convcontext)
</dt> <dt>

[**DdeConnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect)
</dt> <dt>

[**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)
</dt> <dt>

**Méthodologique**
</dt> <dt>

[Bibliothèque de gestion des échange dynamique de données](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

