---
title: Méthode INapSystemHealthAgentRequest SetSoHRequest (NapSystemHealthAgent. h)
description: Est utilisé par les agents d’intégrité pour écrire leur demande d’intégrité résultant de l’appel à INapSystemHealthAgentCallback GetSoHRequest.
ms.assetid: 76471cf2-e5df-4e07-b872-ccac0fd45998
keywords:
- Méthode SetSoHRequest NAP
- Méthode SetSoHRequest NAP, interface INapSystemHealthAgentRequest
- INapSystemHealthAgentRequest interface NAP, méthode SetSoHRequest
topic_type:
- apiref
api_name:
- INapSystemHealthAgentRequest.SetSoHRequest
api_location:
- qagentrt.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6945e8fcc8e53398067cfb7f26bd6029d8920876d23d35aab676b9fb197e64e2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119686139"
---
# <a name="inapsystemhealthagentrequestsetsohrequest-method"></a>INapSystemHealthAgentRequest :: SetSoHRequest, méthode

> [!Note]  
> La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10

 

La méthode **INapSystemHealthAgentRequest :: SetSoHRequest** est utilisée par les agents d’intégrité pour écrire leur demande d’intégrité résultant de l’appel à [**INapSystemHealthAgentCallback :: GetSoHRequest**](inapsystemhealthagentcallback-getsohrequest-method.md).

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetSoHRequest(
  [in] const SoHRequest *sohRequest,
  [in]       BOOL       cacheSohForLaterUse
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*sohRequest* \[ dans\]
</dt> <dd>

Pointeur vers un paquet [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) .

</dd> <dt>

*cacheSohForLaterUse* \[ dans\]
</dt> <dd>

Valeur **booléenne** qui est **true** si NapAgent doit mettre en cache la [**SOH**](/windows/win32/api/naptypes/ns-naptypes-soh) et **false** dans le cas contraire.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

D’autres codes d’erreur spécifiques à COM peuvent également être retournés.



| Code de retour                                                                                     | Description                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | Opération réussie.<br/>                                    |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Erreur d’autorisation, accès refusé.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | Limite du système, impossible d’effectuer l’opération.<br/> |



 

## <a name="requirements"></a>Configuration requise



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

 

 





