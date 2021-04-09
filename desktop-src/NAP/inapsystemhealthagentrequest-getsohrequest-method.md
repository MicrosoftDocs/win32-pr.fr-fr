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
ms.openlocfilehash: ab52e52c952c2dc1f891098e10c3ecb688052295
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104033186"
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
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                                      |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                                |
| En-tête<br/>                   | <dl> <dt>NapSystemHealthAgent. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>NapSystemHealthAgent. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qagentrt.dll</dt> </dl>             |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**INapSystemHealthAgentRequest**](inapsystemhealthagentrequest.md)
</dt> </dl>

 

 





