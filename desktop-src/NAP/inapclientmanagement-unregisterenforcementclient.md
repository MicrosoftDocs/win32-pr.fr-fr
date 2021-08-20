---
title: Méthode INapClientManagement UnregisterEnforcementClient (NapManagement. h)
description: Annule l’inscription d’un client de contrainte auprès du système NAP.
ms.assetid: 549683de-7f2c-4da6-9616-862e0e99d21f
keywords:
- Méthode UnregisterEnforcementClient NAP
- Méthode UnregisterEnforcementClient NAP, interface INapClientManagement
- INapClientManagement interface NAP, méthode UnregisterEnforcementClient
topic_type:
- apiref
api_name:
- INapClientManagement.UnregisterEnforcementClient
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0298b55a5552f2a3ce7a40e048874076729f7e506475c8626de9e9e343da3b8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118134551"
---
# <a name="inapclientmanagementunregisterenforcementclient-method"></a>INapClientManagement :: UnregisterEnforcementClient, méthode

> [!Note]  
> La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10

 

La méthode **UnregisterEnforcementClient** annule l’inscription d’un client de contrainte auprès du système NAP.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT UnregisterEnforcementClient(
  [in] EnforcementEntityId id
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ID* \[ dans\]
</dt> <dd>

Valeur [**EnforcementEntityId**](nap-datatypes.md) qui identifie le client de mise en œuvre dont l’inscription doit être annulée.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La méthode retourne un code d’État HRESULT incluant, sans s’y limiter, l’un des éléments suivants.



| Code de retour                                                                                         | Description                                                                    |
|-----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                | L’opération a réussi.<br/>                                               |
| <dl> <dt>**\_ACCESSDENIED E**</dt> </dl>      | Erreur d’autorisation, accès refusé.<br/>                                   |
| <dl> <dt>**\_OUTOFMEMORY E**</dt> </dl>       | Limite du système, impossible d’effectuer l’opération.<br/>             |
| <dl> <dt>**la protection NAP est \_ \_ toujours \_ liée**</dt> </dl> | Le client de contrainte n’a pas pu être désinscrit et reste lié.<br/> |



 

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

 

 





