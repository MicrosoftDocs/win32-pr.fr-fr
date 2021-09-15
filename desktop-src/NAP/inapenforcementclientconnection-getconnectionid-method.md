---
title: Méthode INapEnforcementClientConnection GetConnectionID, (NapEnforcementClient. h)
description: Est utilisé pour récupérer l’ID de connexion unique du client.
ms.assetid: bf744aa6-5786-473f-9508-db4ee0c75578
keywords:
- Méthode GetConnectionID, NAP
- Méthode GetConnectionID, NAP, interface INapEnforcementClientConnection
- INapEnforcementClientConnection interface NAP, méthode GetConnectionID,
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.GetConnectionId
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f3ca16aea3c77ccf78359c3cdf5ab6461bc2219e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127311969"
---
# <a name="inapenforcementclientconnectiongetconnectionid-method"></a>INapEnforcementClientConnection :: GetConnectionID,, méthode

> [!Note]  
> La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10

 

La méthode **INapEnforcementClientConnection :: GetConnectionID,** permet d’accéder à l’ID de connexion unique du client.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetConnectionId(
  [out] ConnectionId **connectionId
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ID* \[ de la à\]
</dt> <dd>

Pointeur vers un pointeur vers un [**ID**](nap-datatypes.md) de connexion qui identifie de façon unique cette connexion.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

D’autres codes d’erreur spécifiques à COM peuvent également être retournés.



| Code de retour                                                                                     | Description                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | Opération réussie.<br/>                                    |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Erreur d’autorisation, accès refusé.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | Limite du système, impossible d’effectuer l’opération.<br/> |



 

## <a name="remarks"></a>Remarques

L’ID de connexion est principalement utilisé à des fins de journalisation.

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

 

 





