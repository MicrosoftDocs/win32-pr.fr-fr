---
title: Méthode INapClientManagement GetRegisteredEnforcementClients (NapManagement. h)
description: Récupère des informations sur les clients de mise en œuvre inscrits.
ms.assetid: aae7c57c-a7fe-4cb2-94f6-53e501e38054
keywords:
- Méthode GetRegisteredEnforcementClients NAP
- Méthode GetRegisteredEnforcementClients NAP, interface INapClientManagement
- INapClientManagement interface NAP, méthode GetRegisteredEnforcementClients
topic_type:
- apiref
api_name:
- INapClientManagement.GetRegisteredEnforcementClients
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae7854a36ffb1d313a1598764c5375a8146471c1b2fd930b4022948f147acc24
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118940207"
---
# <a name="inapclientmanagementgetregisteredenforcementclients-method"></a>INapClientManagement :: GetRegisteredEnforcementClients, méthode

> [!Note]  
> La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10

 

La méthode **GetRegisteredEnforcementClients** récupère des informations sur les clients de mise en œuvre inscrits.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetRegisteredEnforcementClients(
  [out] EnforcementEntityCount       *count,
  [out] NapComponentRegistrationInfo **enforcers
) const;
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*nombre* \[ à\]
</dt> <dd>

Pointeur vers un [**EnforcementEntityCount**](nap-datatypes.md) qui contient le nombre de clients de mise en œuvre inscrits.

</dd> <dt>

*application* \[ à\]
</dt> <dd>

Pointeur vers un tableau de structures [**NapComponentRegistrationInfo**](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo) qui décrivent les clients de mise en œuvre inscrits.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La méthode retourne un code d’État HRESULT incluant, sans s’y limiter, l’un des éléments suivants.



| Code de retour                                                                                         | Description                                                        |
|-----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                | L’opération a réussi.<br/>                                   |
| <dl> <dt>**\_ACCESSDENIED E**</dt> </dl>      | Erreur d’autorisation, accès refusé.<br/>                       |
| <dl> <dt>**\_OUTOFMEMORY E**</dt> </dl>       | Limite du système, impossible d’effectuer l’opération.<br/> |
| <dl> <dt>**RPC \_ E \_ déconnecté**</dt> </dl> | NapAgent n’est pas en cours d’exécution.<br/>                            |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                               |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                         |
| En-tête<br/>                   | <dl> <dt>NapManagement. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>NapManagement. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qagent.dll</dt> </dl>        |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**INapClientManagement**](inapclientmanagement.md)
</dt> </dl>

 

 





