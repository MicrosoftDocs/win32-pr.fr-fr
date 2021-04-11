---
title: Méthode INapEnforcementClientConnection SetPrivateData (NapEnforcementClient. h)
description: Est utilisé par NapAgent pour définir des données privées.
ms.assetid: 2559a612-8857-4e60-b5bc-dd8235ff69f9
keywords:
- Méthode SetPrivateData NAP
- Méthode SetPrivateData NAP, interface INapEnforcementClientConnection
- INapEnforcementClientConnection interface NAP, méthode SetPrivateData
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.SetPrivateData
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3e73248e546b1f0e48438553877f0523bd30b56
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032652"
---
# <a name="inapenforcementclientconnectionsetprivatedata-method"></a>INapEnforcementClientConnection :: SetPrivateData, méthode

> [!Note]  
> La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10

 

La méthode **INapEnforcementClientConnection :: SetPrivateData** est utilisée par le NapAgent pour définir des données privées.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetPrivateData(
  [in] const PrivateData *privateData
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*privateData* \[ dans\]
</dt> <dd>

Pointeur vers un objet blob de données [**PrivateData**](/windows/win32/api/naptypes/ns-naptypes-privatedata) que seul le NapAgent peut interpréter.

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

 

 





