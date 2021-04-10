---
title: Méthode INapEnforcementClientConnection SetEnforcerPrivateData (NapEnforcementClient. h)
description: Est utilisé par l’application pour définir des données privées.
ms.assetid: 56f6fec7-47ec-4b2c-b8c8-a4d519ba0f91
keywords:
- Méthode SetEnforcerPrivateData NAP
- Méthode SetEnforcerPrivateData NAP, interface INapEnforcementClientConnection
- INapEnforcementClientConnection interface NAP, méthode SetEnforcerPrivateData
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.SetEnforcerPrivateData
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef5773294e229a59ff07db8ef546d9d691b369b2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032654"
---
# <a name="inapenforcementclientconnectionsetenforcerprivatedata-method"></a>INapEnforcementClientConnection :: SetEnforcerPrivateData, méthode

> [!Note]  
> La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10

 

La méthode **INapEnforcementClientConnection :: SetEnforcerPrivateData** est utilisée par l’application pour définir des données privées.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetEnforcerPrivateData(
  [in] const PrivateData *privateData
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*privateData* \[ dans\]
</dt> <dd>

Pointeur vers un objet blob de données opaques [**PrivateData**](/windows/win32/api/naptypes/ns-naptypes-privatedata) que seul l’application peut interpréter.

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
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                                      |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                                |
| En-tête<br/>                   | <dl> <dt>NapEnforcementClient. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>NapEnforcementClient. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qagent.dll</dt> </dl>               |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**INapEnforcementClientConnection**](inapenforcementclientconnection.md)
</dt> </dl>

 

 





