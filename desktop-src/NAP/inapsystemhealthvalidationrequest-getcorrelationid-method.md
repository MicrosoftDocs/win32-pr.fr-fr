---
title: Méthode INapSystemHealthValidationRequest GetCorrelationId (NapSystemHealthValidator. h)
description: Est utilisé par les programmes de validation d’intégrité système (SHV) pour récupérer l’ID de corrélation. Le SHV doit ensuite consigner ces informations.
ms.assetid: 72603d24-219e-4bb0-9b2b-b58d42939da8
keywords:
- Méthode GetCorrelationId NAP
- Méthode GetCorrelationId NAP, interface INapSystemHealthValidationRequest
- INapSystemHealthValidationRequest interface NAP, méthode GetCorrelationId
topic_type:
- apiref
api_name:
- INapSystemHealthValidationRequest.GetCorrelationId
api_location:
- qshvhost.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1095a2c3eec90ff33613b6d37b43f31fdabd107
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465142"
---
# <a name="inapsystemhealthvalidationrequestgetcorrelationid-method"></a>INapSystemHealthValidationRequest :: GetCorrelationId, méthode

> [!Note]  
> La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10

 

La méthode **INapSystemHealthValidationRequest :: GetCorrelationId** est utilisée par les programmes de validation d’intégrité système (SHV) pour récupérer l’ID de corrélation. Le SHV doit ensuite consigner ces informations.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetCorrelationId(
  [out] CorrelationId *correlationId
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*CorrelationId* \[ à\]
</dt> <dd>

Pointeur vers un ID de [**corrélation**](/windows/win32/api/naptypes/ns-naptypes-correlationid) unique pour l’échange de déclaration d’intégrité.

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
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                               |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                                    |
| En-tête<br/>                   | <dl> <dt>NapSystemHealthValidator. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>NapSystemHealthValidator. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qshvhost.dll</dt> </dl>                 |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**INapSystemHealthValidationRequest**](inapsystemhealthvalidationrequest.md)
</dt> </dl>

 

 





