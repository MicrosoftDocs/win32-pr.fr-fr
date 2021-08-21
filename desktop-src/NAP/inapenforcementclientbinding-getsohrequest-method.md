---
title: Méthode INapEnforcementClientBinding GetSoHRequest (NapEnforcementClient. h)
description: Est utilisé par le client de mise en œuvre pour récupérer une requête SoH pour une connexion particulière.
ms.assetid: 6fce6e84-ce03-48f2-957b-a41efe044fc5
keywords:
- Méthode GetSoHRequest NAP
- Méthode GetSoHRequest NAP, interface INapEnforcementClientBinding
- INapEnforcementClientBinding interface NAP, méthode GetSoHRequest
topic_type:
- apiref
api_name:
- INapEnforcementClientBinding.GetSoHRequest
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 780f144c6f4613006940069896aa8382006b179631acd83283121ee3c64ec0d8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118134335"
---
# <a name="inapenforcementclientbindinggetsohrequest-method"></a>INapEnforcementClientBinding :: GetSoHRequest, méthode

> [!Note]  
> La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10

 

La méthode **INapEnforcementClientBinding :: GetSoHRequest** est utilisée par le client de mise en œuvre pour récupérer une requête SOH pour une connexion particulière.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetSoHRequest(
  [in]  INapEnforcementClientConnection *connection,
  [out] BOOL                            *retriggerHint
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*connexion* \[ dans\]
</dt> <dd>

Pointeur COM vers une interface [**INapEnforcementClientConnection**](inapenforcementclientconnection.md) . NapAgent ne contient pas de références à l’objet associé à cette interface une fois la méthode terminée.

</dd> <dt>

*retriggerHint* \[ à\]
</dt> <dd>

Pointeur vers un **booléen** qui indique si la connexion doit être redéclenchée. Elle a la **valeur true** si le [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) a changé depuis le dernier appel à cette fonction ou si [**ProbationTime**](nap-datatypes.md) a expiré. Sinon, la **valeur false** est retournée.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

D’autres codes d’erreur spécifiques à COM peuvent également être retournés.



| Code de retour                                                                                             | Description                                                        |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                   | L'opération a réussi.<br/>                            |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl>         | Erreur d’autorisation, accès refusé.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>          | Limite du système, impossible d’effectuer l’opération.<br/> |
| <dl> <dt>**NAP \_ E \_ non \_ initialisé**</dt> </dl> | L’application n’a pas été précédemment initialisée.<br/>       |



 

## <a name="remarks"></a>Remarques

NapAgent définit [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) sur l’objet de connexion.

Si une [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) était en attente sur cette connexion, elle est ignorée et les Sha sont avertis du **SoHRequests** orphelin.

Le client de contrainte doit appeler la méthode [**INapEnforcementClientBinding :: Initialize**](inapenforcementclientbinding-initialize-method.md) avant d’appeler cette méthode ou toute autre méthode de l’interface [**INapEnforcementClientBinding**](inapenforcementclientbinding.md) .

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


</dt> <dt>

[**INapEnforcementClientBinding**](inapenforcementclientbinding.md)
</dt> </dl>

 

 





