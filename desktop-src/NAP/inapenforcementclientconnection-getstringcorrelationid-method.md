---
title: Méthode INapEnforcementClientConnection GetStringCorrelationId (NapEnforcementClient. h)
description: Obtient la version de chaîne de l’ID utilisé pour corréler les demandes et les réponses.
ms.assetid: d744fa4e-5e30-429e-810d-7326047bb3f8
keywords:
- Méthode GetStringCorrelationId NAP
- Méthode GetStringCorrelationId NAP, interface INapEnforcementClientConnection
- INapEnforcementClientConnection interface NAP, méthode GetStringCorrelationId
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.GetStringCorrelationId
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6a01ca16bffb627f4ca5be38ef547980951c0ee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508442"
---
# <a name="inapenforcementclientconnectiongetstringcorrelationid-method"></a>INapEnforcementClientConnection :: GetStringCorrelationId, méthode

> [!Note]  
> La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10

 

La méthode **INapEnforcementClientConnection :: GetStringCorrelationId** obtient la version de chaîne de l’ID utilisé pour corréler les demandes et les réponses.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetStringCorrelationId(
  [out] CountedString **correlationId
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*CorrelationId* \[ à\]
</dt> <dd>

Pointeur vers une structure [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) qui contient la version sous forme de chaîne de l’ID de [**corrélation**](/windows/win32/api/naptypes/ns-naptypes-correlationid)de la connexion.

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

 

 





