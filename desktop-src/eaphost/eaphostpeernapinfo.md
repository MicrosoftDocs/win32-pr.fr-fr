---
title: EapHostPeerNapInfo, structure (Eaphostpeerapis. h)
description: Contient les informations de protection d’accès réseau (NAP) sur un demandeur EAP.
ms.assetid: 703eda56-5932-44d5-ae7f-0a6328d82237
keywords:
- EapHostPeerNapInfo, structure EAPHost
topic_type:
- apiref
api_name:
- EapHostPeerNapInfo
api_location:
- eaphostpeerapis.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5fe91c88f633f2e42599938e45e1291c90f1ec9c08559a84f132f3af9269de39
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118274535"
---
# <a name="eaphostpeernapinfo-structure"></a>EapHostPeerNapInfo, structure

La structure **EapHostPeerNapInfo** contient les informations de protection d’accès réseau (NAP) sur un demandeur EAP.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _tagEapHostPeerNapInfo {
  ISOLATION_STATE isolationState;
  ProbationTime   probationTime;
  UINT32          stringCorrelationIdLength;
} EapHostPeerNapInfo;
```



## <a name="members"></a>Membres

<dl> <dt>

**isolationState**
</dt> <dd>

Structure [**d' \_ État d’isolement**](/windows/desktop/api/eaphostpeertypes/ne-eaphostpeertypes-isolation_state) qui spécifie l’état d’isolement NAP d’un ordinateur. L’état d’isolement détermine le niveau d’accès réseau accordé.

</dd> <dt>

**probationTime**
</dt> <dd>

Structure **ProbationTime** qui spécifie le temps nécessaire à la connexion pour sortir de la mise en quarantaine après laquelle la connexion sera supprimée. Une structure **ProbationTime** est identique à une structure [fileTime](/windows/win32/api/minwinbase/ns-minwinbase-filetime) .

</dd> <dt>

**stringCorrelationIdLength**
</dt> <dd>

Longueur, en octets, du [STRINGCORRELATIONID](/windows/desktop/NAP/nap-datatypes) NAP qui suit cette structure.

</dd> </dl>

## <a name="remarks"></a>Notes

La structure **EapHostPeerNapInfo** précède le [stringCorrelationId](/windows/desktop/NAP/nap-datatypes) NAP du type de données **WCHAR** dans le flux d’octets RPC.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 uniquement\]<br/>                                                   |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 R2, \[ applications de bureau uniquement\]<br/>                                      |
| En-tête<br/>                   | <dl> <dt>Eaphostpeerapis. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Structures du demandeur EAPHost](eap-host-supplicant-structures.md)
</dt> <dt>

[**EapHostPeerGetAuthStatus**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetauthstatus)
</dt> <dt>

[**EapHostPeerMethodAuthParams**](/windows/win32/api/eaphostpeertypes/ne-eaphostpeertypes-eaphostpeerauthparams)
</dt> </dl>

 

