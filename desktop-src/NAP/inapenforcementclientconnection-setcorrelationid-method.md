---
title: Méthode INapEnforcementClientConnection SetCorrelationId (NapEnforcementClient. h)
description: Définit l’ID utilisé pour corréler les demandes SoH et les réponses SoH.
ms.assetid: 8f9d5bde-95b1-4566-84ee-31c6ed5e8986
keywords:
- Méthode SetCorrelationId NAP
- Méthode SetCorrelationId NAP, interface INapEnforcementClientConnection
- INapEnforcementClientConnection interface NAP, méthode SetCorrelationId
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.SetCorrelationId
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9be8a7fbcbe9e2accd074768b8a0e50d6ce2dcaa2bda53e063cb76d294ff92c5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118368259"
---
# <a name="inapenforcementclientconnectionsetcorrelationid-method"></a>INapEnforcementClientConnection :: SetCorrelationId, méthode

> [!Note]  
> La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10

 

La méthode **INapEnforcementClientConnection :: SetCorrelationId** définit l’ID utilisé pour corréler les demandes SOH et les réponses SOH.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetCorrelationId(
  [in] CorrelationId correlationId
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*CorrelationId* \[ dans\]
</dt> <dd>

Structure d’ID de [**corrélation**](/windows/win32/api/naptypes/ns-naptypes-correlationid) unique qui identifie un échange SOH spécifique.

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

 

 





