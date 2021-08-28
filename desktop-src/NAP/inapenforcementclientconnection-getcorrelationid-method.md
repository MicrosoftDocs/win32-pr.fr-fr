---
title: Méthode INapEnforcementClientConnection GetCorrelationId (NapEnforcementClient. h)
description: Obtient l’ID utilisé pour corréler les demandes SoH et les réponses SoH.
ms.assetid: f59880d4-5de6-4163-ae01-1095ff52bf38
keywords:
- Méthode GetCorrelationId NAP
- Méthode GetCorrelationId NAP, interface INapEnforcementClientConnection
- INapEnforcementClientConnection interface NAP, méthode GetCorrelationId
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.GetCorrelationId
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a1045513d672afbbd4e53f956f03b1f4db2a925cf756c158303a17998bcf219
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118940075"
---
# <a name="inapenforcementclientconnectiongetcorrelationid-method"></a>INapEnforcementClientConnection :: GetCorrelationId, méthode

> [!Note]  
> La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10

 

La méthode **INapEnforcementClientConnection :: GetCorrelationId** obtient l’ID utilisé pour corréler les demandes SOH et les réponses SOH.

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

Structure d’ID de [**corrélation**](/windows/win32/api/naptypes/ns-naptypes-correlationid) unique qui identifie cet échange SOH.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

D’autres codes d’erreur spécifiques à COM peuvent également être retournés.



| Code de retour                                                                                     | Description                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | Opération réussie.<br/>                                    |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Erreur d’autorisation, accès refusé.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | Limite du système, impossible d’effectuer l’opération.<br/> |



 

## <a name="remarks"></a>Remarques

L’ID de corrélation est défini par NapAgent et basé sur l’ID de connexion.

Cet ID est utilisé pour corréler les demandes et les réponses, c.-à-d. il décrit de façon unique un échange SoH et contient toujours l’ID du dernier ensemble de déclaration d’intégrité de l’objet de connexion.

Lors de la réception d’un SoH-Response, NapAgent vérifie d’abord que les ID correspondent. Si ce n’est pas le cas, une erreur est retournée et l’application doit supprimer le paquet. Pour plus d’informations, consultez [**INapEnforcementClientBinding ::P rocesssohresponse**](inapenforcementclientbinding-processsohresponse-method.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                                      |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                                |
| En-tête<br/>                   | <dl> <dt>NapEnforcementClient. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>NapEnforcementClient. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qagent.dll</dt> </dl>               |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**INapEnforcementClientConnection**](inapenforcementclientconnection.md)
</dt> </dl>

 

 





