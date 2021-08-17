---
title: Méthode INapSystemHealthAgentRequest GetSoHRequest (NapSystemHealthAgent. h)
description: Peut être utilisé par les SoHs de récupération d’intégrité du NapAgent précédemment mis en cache par le.
ms.assetid: 187a4513-79db-45cb-8d64-6a92a2d3b004
keywords:
- Méthode GetSoHRequest NAP
- Méthode GetSoHRequest NAP, interface INapSystemHealthAgentRequest
- INapSystemHealthAgentRequest interface NAP, méthode GetSoHRequest
topic_type:
- apiref
api_name:
- INapSystemHealthAgentRequest.GetSoHRequest
api_location:
- qagentrt.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c784ec520180f3524f49fa95644b03fa5f982651bd4c2322542dc46cc3f85a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118133518"
---
# <a name="inapsystemhealthagentrequestgetsohrequest-method"></a>INapSystemHealthAgentRequest :: GetSoHRequest, méthode

> [!Note]  
> La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10

 

La méthode **INapSystemHealthAgentRequest :: GetSoHRequest** peut être utilisée par les SoHs de récupération d’intégrité des précédemment mises en cache par NapAgent.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetSoHRequest(
  [out] SoHRequest **sohRequest
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*sohRequest* \[ à\]
</dt> <dd>

Pointeur vers un pointeur vers un [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

D’autres codes d’erreur spécifiques à COM peuvent également être retournés.



| Code de retour                                                                                            | Description                                                            |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                  | Opération réussie.<br/>                                        |
| <dl> <dt>**E/r NAP \_ \_ non \_ mis en cache \_**</dt> </dl> | SoH introuvable ; NapAgent n’a pas de copie mise en cache.<br/> |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl>        | Erreur d’autorisation, accès refusé.<br/>                           |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>         | Limite du système, impossible d’effectuer l’opération.<br/>     |



 

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

 

 





