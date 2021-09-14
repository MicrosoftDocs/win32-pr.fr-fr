---
title: Méthode INapSystemHealthAgentRequest GetCacheSoHFlag (NapSystemHealthAgent. h)
description: Est utilisé uniquement par NapAgent.
ms.assetid: 97dd4e95-30c2-48e2-9359-b1019299581d
keywords:
- Méthode GetCacheSoHFlag NAP
- Méthode GetCacheSoHFlag NAP, interface INapSystemHealthAgentRequest
- INapSystemHealthAgentRequest interface NAP, méthode GetCacheSoHFlag
topic_type:
- apiref
api_name:
- INapSystemHealthAgentRequest.GetCacheSoHFlag
api_location:
- qagentrt.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53d8b458e4a49b690fe1f0f53482a72dd253c7c7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127011631"
---
# <a name="inapsystemhealthagentrequestgetcachesohflag-method"></a>INapSystemHealthAgentRequest :: GetCacheSoHFlag, méthode

> [!Note]  
> La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10

 

La méthode **INapSystemHealthAgentRequest :: GetCacheSoHFlag** est utilisée uniquement par le NapAgent.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetCacheSoHFlag(
   BOOL *cacheSohForLaterUse
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*cacheSohForLaterUse* 
</dt> <dd>

Valeur **booléenne** qui est **true** si NapAgent doit mettre en cache la [**SOH**](/windows/win32/api/naptypes/ns-naptypes-soh) et **false** dans le cas contraire.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

D’autres codes d’erreur spécifiques à COM peuvent également être retournés.



| Code de retour                                                                                     | Description                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | Opération réussie.<br/>                                    |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Erreur d’autorisation, accès refusé.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | Limite du système, impossible d’effectuer l’opération.<br/> |



 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                                      |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                                |
| En-tête<br/>                   | <dl> <dt>NapSystemHealthAgent. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>NapSystemHealthAgent. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qagentrt.dll</dt> </dl>             |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**INapSystemHealthAgentRequest**](inapsystemhealthagentrequest.md)
</dt> </dl>

 

 





