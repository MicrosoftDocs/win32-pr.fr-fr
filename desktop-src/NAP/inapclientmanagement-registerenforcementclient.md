---
title: Méthode INapClientManagement RegisterEnforcementClient (NapManagement. h)
description: Inscrit un client de mise en œuvre auprès du système NAP.
ms.assetid: 26ea45ea-a366-4162-91dc-06bcd0261c56
keywords:
- Méthode RegisterEnforcementClient NAP
- Méthode RegisterEnforcementClient NAP, interface INapClientManagement
- INapClientManagement interface NAP, méthode RegisterEnforcementClient
topic_type:
- apiref
api_name:
- INapClientManagement.RegisterEnforcementClient
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e22deffb8f144e8f7176bd78fb18978228a26251be5591df61a322e5da17d3f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118134561"
---
# <a name="inapclientmanagementregisterenforcementclient-method"></a>INapClientManagement :: RegisterEnforcementClient, méthode

> [!Note]  
> La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10

 

La méthode **RegisterEnforcementClient** inscrit un client de mise en œuvre auprès du système NAP.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT RegisterEnforcementClient(
  [in] const NapComponentRegistrationInfo *enforcer
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*application* \[ dans\]
</dt> <dd>

Pointeur vers une structure de données [**NapComponentRegistrationInfo**](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo) qui contient les informations d’inscription associées au client de contrainte.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La méthode retourne un code d’État HRESULT incluant, sans s’y limiter, l’un des éléments suivants.



| Code de retour                                                                                            | Description                                                                       |
|--------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                   | L’opération a réussi.<br/>                                                  |
| <dl> <dt>**\_ACCESSDENIED E**</dt> </dl>         | Erreur d’autorisation, accès refusé.<br/>                                      |
| <dl> <dt>**\_OUTOFMEMORY E**</dt> </dl>          | Limite du système, impossible d’effectuer l’opération.<br/>                |
| <dl> <dt>**\_ID en \_ conflit NAP \_ E**</dt> </dl> | Un agent d’application utilisant l’identificateur donné est déjà inscrit.<br/> |



 

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

 

 





