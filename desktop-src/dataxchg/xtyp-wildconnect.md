---
title: XTYP_WILDCONNECT transaction (Ddeml. h)
description: Permet à un client d’établir une conversation sur chacune des paires nom de service et nom de rubrique du serveur qui correspondent au nom du service et au nom de la rubrique spécifiés.
ms.assetid: 4651e14f-ca13-412e-853d-326a13db78e4
keywords:
- Échange de données de transaction XTYP_WILDCONNECT
topic_type:
- apiref
api_name:
- XTYP_WILDCONNECT
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc63d6c367aebc440418beaabb0a06f05b0df967
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510140"
---
# <a name="xtyp_wildconnect-transaction"></a>\_Transaction WILDCONNECT XTYP

Permet à un client d’établir une conversation sur chacune des paires nom de service et nom de rubrique du serveur qui correspondent au nom du service et au nom de la rubrique spécifiés. Une fonction de rappel de serveur échange dynamique de données (DDE), [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), reçoit cette transaction lorsqu’un client spécifie un nom de service **null** , un nom de rubrique **null** ou les deux dans un appel à la fonction [**DdeConnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect) ou [**DdeConnectList**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist) .


```C++
#define     XCLASS_DATA              0x2000
#define     XTYPF_NOBLOCK            0x0002
#define     XTYP_WILDCONNECT        (0x00E0 | XCLASS_DATA | XTYPF_NOBLOCK)
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

Handle vers le nom de la rubrique. Si ce paramètre a la **valeur null**, le client demande une conversation sur tous les noms de rubriques que le serveur prend en charge.

</dd> <dt>

*hsz2* 
</dt> <dd>

Handle vers le nom du service. Si ce paramètre a la **valeur null**, le client demande une conversation sur tous les noms de service pris en charge par le serveur.

</dd> <dt>

*hdata* 
</dt> <dd>

Non utilisé.

</dd> <dt>

*dwData1* 
</dt> <dd>

Pointeur vers une structure [**CONVCONTEXT**](/windows/win32/api/ddeml/ns-ddeml-convcontext) qui contient des informations de contexte pour la conversation. Si le client n’est pas une application DDEML, ce paramètre a la valeur 0.

</dd> <dt>

*dwData2* 
</dt> <dd>

Spécifie si le client est la même instance d’application que le serveur. Si le paramètre est 1, le client est la même instance. Si le paramètre a la valeur 0, le client est une instance différente.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Le serveur doit retourner un handle de données qui identifie un tableau de structures [**HSZPAIR**](/windows/win32/api/ddeml/ns-ddeml-hszpair) . Le tableau doit contenir une structure pour chaque paire Service-Name et Topic-Name qui correspond à la paire Service-Name et Topic-Name demandée par le client. Le tableau doit se terminer par un handle de chaîne **null** . Le système envoie la [**transaction \_ \_ Confirm XTYP Connect**](xtyp-connect-confirm.md) au serveur pour confirmer chaque conversation et transmettre les descripteurs de conversation au serveur. Le serveur ne recevra pas ces confirmations s’il a spécifié l’indicateur **CBF \_ Skip \_ Connect \_ Confirm** dans la fonction [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) .

Le serveur doit retourner la **valeur null** pour refuser la transaction **XTYP \_ WILDCONNECT** .

## <a name="remarks"></a>Notes

Cette transaction est filtrée si l’application serveur a spécifié l’indicateur **CBF \_ Fail \_ connections** dans la fonction [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) .

Un serveur ne peut pas bloquer ce type de transaction ; le \_ Code de retour de bloc CBR est ignoré.

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

[**HSZPAIR**](/windows/win32/api/ddeml/ns-ddeml-hszpair)
</dt> <dt>

**Méthodologique**
</dt> <dt>

[Bibliothèque de gestion des échange dynamique de données](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

