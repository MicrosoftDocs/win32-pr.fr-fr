---
title: Méthode INapClientManagement GetRegisteredSystemHealthAgents (NapManagement. h)
description: Récupère des informations sur les Sha enregistrés.
ms.assetid: c38d2d23-62d4-49f0-81a3-52394866f0c4
keywords:
- Méthode GetRegisteredSystemHealthAgents NAP
- Méthode GetRegisteredSystemHealthAgents NAP, interface INapClientManagement
- INapClientManagement interface NAP, méthode GetRegisteredSystemHealthAgents
topic_type:
- apiref
api_name:
- INapClientManagement.GetRegisteredSystemHealthAgents
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57d9c2792282245ad4903d77700f5413bef0d2f769a65753aed60f50ba759707
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117800109"
---
# <a name="inapclientmanagementgetregisteredsystemhealthagents-method"></a>INapClientManagement :: GetRegisteredSystemHealthAgents, méthode

> [!Note]  
> La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10

 

La méthode **GetRegisteredSystemHealthAgents** récupère des informations sur l’intégrité des données inscrite.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetRegisteredSystemHealthAgents(
  [out] SystemHealthEntityCount      *count,
  [out] NapComponentRegistrationInfo **agents
) const;
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*nombre* \[ à\]
</dt> <dd>

Pointeur vers un [**SystemHealthEntityCount**](nap-datatypes.md) qui décrit le nombre de Sha inscrits.

</dd> <dt>

*agents* \[ à\]
</dt> <dd>

Pointeur vers un tableau de structures [**NapComponentRegistrationInfo**](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo) qui décrivent les Sha inscrits.

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

 

 





