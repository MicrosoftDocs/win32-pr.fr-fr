---
title: Méthode INapClientManagement UnregisterSystemHealthAgent (NapManagement. h)
description: Annule l’inscription d’un SHA auprès du système NAP.
ms.assetid: c3ad6f2a-c39a-4590-8487-24c802433845
keywords:
- Méthode UnregisterSystemHealthAgent NAP
- Méthode UnregisterSystemHealthAgent NAP, interface INapClientManagement
- INapClientManagement interface NAP, méthode UnregisterSystemHealthAgent
topic_type:
- apiref
api_name:
- INapClientManagement.UnregisterSystemHealthAgent
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad43df1c7edeb2525ff5c8901278d082c4ba299ea78d56c67a4380f8a7bab019
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118134507"
---
# <a name="inapclientmanagementunregistersystemhealthagent-method"></a>INapClientManagement :: UnregisterSystemHealthAgent, méthode

> [!Note]  
> La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10

 

La méthode **UnregisterSystemHealthAgent** annule l’inscription d’un SHA auprès du système NAP.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT UnregisterSystemHealthAgent(
  [in] SystemHealthEntityId id
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ID* \[ dans\]
</dt> <dd>

[**SystemHealthEntityId**](nap-datatypes.md) qui identifie l’agent d’intégrité système dont l’inscription doit être annulée.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La méthode retourne un code d’État HRESULT incluant, sans s’y limiter, l’un des éléments suivants.



| Code de retour                                                                                         | Description                                                        |
|-----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                | L’opération a réussi.<br/>                                   |
| <dl> <dt>**\_ACCESSDENIED E**</dt> </dl>      | Erreur d’autorisation, accès refusé.<br/>                       |
| <dl> <dt>**\_OUTOFMEMORY E**</dt> </dl>       | Limite du système, impossible d’effectuer l’opération.<br/> |
| <dl> <dt>**la protection NAP est \_ \_ toujours \_ liée**</dt> </dl> | L’algorithme SHA reste lié et ne peut pas être annulé.<br/>    |



 

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

 

 





