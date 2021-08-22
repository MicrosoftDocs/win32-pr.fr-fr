---
title: Méthode INapSystemHealthAgentRequest GetSoHResponse (NapSystemHealthAgent. h)
description: Est utilisé par l’agent d’intégrité pour récupérer son objet BLOB SoHResponse lorsque le NapAgent appelle INapSystemHealthAgentCallback ProcessSoHResponse.
ms.assetid: 60319256-d5c2-46cc-a59b-f81732e21a7f
keywords:
- Méthode GetSoHResponse NAP
- Méthode GetSoHResponse NAP, interface INapSystemHealthAgentRequest
- INapSystemHealthAgentRequest interface NAP, méthode GetSoHResponse
topic_type:
- apiref
api_name:
- INapSystemHealthAgentRequest.GetSoHResponse
api_location:
- qagentrt.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d78b67c38f54cfe1e7d342212be897ba1825b619324e6fc4cb5ab9ae4f5c4a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118621160"
---
# <a name="inapsystemhealthagentrequestgetsohresponse-method"></a>INapSystemHealthAgentRequest :: GetSoHResponse, méthode

> [!Note]  
> La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10

 

La méthode **INapSystemHealthAgentRequest :: GetSoHResponse** est utilisée par l’agent d’intégrité pour récupérer son objet BLOB SoHResponse lorsque le NapAgent appelle [**INapSystemHealthAgentCallback ::P rocesssohresponse**](inapsystemhealthagentcallback-processsohresponse-method.md).

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetSoHResponse(
  [out] SoHResponse **sohResponse,
  [out] UINT8       *flags
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*sohResponse* \[ à\]
</dt> <dd>

Pointeur vers un pointeur vers un paquet [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh) .

</dd> <dt>

*indicateurs* \[ à\]
</dt> <dd>

Pointeur vers un indicateur qui active la correction par l’algorithme SHA si le bit [**shaFixup**](nap-type-constants.md) est défini ; sinon, la correction est désactivée.



| Valeurs possibles                                                                                                                                                          | Signification                                                                                                                                                                                                                   |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="shaFixup"></span><span id="shafixup"></span><span id="SHAFIXUP"></span><dl> <dt>**shaFixup**</dt> </dl> | L’algorithme SHA est supposé effectuer la correction en fonction de la réponse. Si cet indicateur n’est pas défini, l’agent SHA ne doit pas effectuer de correction même si le [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh) indique qu’il n’est pas sain.<br/> |



 

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

 

 





