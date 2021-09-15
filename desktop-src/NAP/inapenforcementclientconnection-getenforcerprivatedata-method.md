---
title: Méthode INapEnforcementClientConnection GetEnforcerPrivateData (NapEnforcementClient. h)
description: Est utilisé par l’application pour recevoir des données privées.
ms.assetid: a1f5b5a7-c862-4e5b-bf9c-b137f99f6165
keywords:
- Méthode GetEnforcerPrivateData NAP
- Méthode GetEnforcerPrivateData NAP, interface INapEnforcementClientConnection
- INapEnforcementClientConnection interface NAP, méthode GetEnforcerPrivateData
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.GetEnforcerPrivateData
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d592ad0b11abf2b349b0810d67b05f2ee4086060
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127311954"
---
# <a name="inapenforcementclientconnectiongetenforcerprivatedata-method"></a>INapEnforcementClientConnection :: GetEnforcerPrivateData, méthode

> [!Note]  
> La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10

 

La méthode **INapEnforcementClientConnection :: GetEnforcerPrivateData** est utilisée par l’application pour récupérer des données privées.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetEnforcerPrivateData(
  [out] PrivateData **privateData
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*privateData* \[ à\]
</dt> <dd>

Pointeur vers un pointeur vers un objet blob de données opaques [**PrivateData**](/windows/win32/api/naptypes/ns-naptypes-privatedata) que seul l’application peut interpréter.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

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
| En-tête<br/>                   | <dl> <dt>NapEnforcementClient. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>NapEnforcementClient. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qagent.dll</dt> </dl>               |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**INapEnforcementClientConnection**](inapenforcementclientconnection.md)
</dt> </dl>

 

 





