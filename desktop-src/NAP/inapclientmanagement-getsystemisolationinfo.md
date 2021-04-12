---
title: Méthode INapClientManagement GetSystemIsolationInfo (NapManagement. h)
description: Récupère des informations sur l’état d’isolement du NapClient.
ms.assetid: e1f69e66-71ca-402e-9c94-8af159d00b21
keywords:
- Méthode GetSystemIsolationInfo NAP
- Méthode GetSystemIsolationInfo NAP, interface INapClientManagement
- INapClientManagement interface NAP, méthode GetSystemIsolationInfo
topic_type:
- apiref
api_name:
- INapClientManagement.GetSystemIsolationInfo
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73b3d446e0a8068353be6656c16f0e6796df8922
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104385016"
---
# <a name="inapclientmanagementgetsystemisolationinfo-method"></a>INapClientManagement :: GetSystemIsolationInfo, méthode

> [!Note]  
> La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10

 

La méthode **GetSystemIsolationInfo** récupère les informations sur l’état d’isolement du NapClient.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetSystemIsolationInfo(
  [out] IsolationInfo **isolationInfo,
  [out] BOOL          *unknownConnections
) const;
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*isolationInfo* \[ à\]
</dt> <dd>

Pointeur vers un pointeur vers une structure [**IsolationInfo**](/windows/win32/api/naptypes/ns-naptypes-isolationinfo) qui contient les informations d’état d’isolement.

</dd> <dt>

*unknownConnections* \[ à\]
</dt> <dd>

Pointeur vers un indicateur qui indique si l’une des connexions est dans un état inconnu. Si l’un d’eux est, l’indicateur a la valeur **true**; Sinon, l’indicateur a la valeur **false**.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La méthode retourne un code d’État HRESULT incluant, sans s’y limiter, l’un des éléments suivants.



| Code de retour                                                                                         | Description                                                        |
|-----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                | L’opération a réussi.<br/>                                   |
| <dl> <dt>**\_ACCESSDENIED E**</dt> </dl>      | Erreur d’autorisation, accès refusé.<br/>                       |
| <dl> <dt>**\_OUTOFMEMORY E**</dt> </dl>       | Limite du système, impossible d’effectuer l’opération.<br/> |
| <dl> <dt>**RPC \_ E \_ déconnecté**</dt> </dl> | NapAgent n’est pas en cours d’exécution.<br/>                            |



 

## <a name="remarks"></a>Notes

Les informations d’isolation récupérées ne reflètent pas les États inconnus.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                               |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                         |
| En-tête<br/>                   | <dl> <dt>NapManagement. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>NapManagement. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qagent.dll</dt> </dl>        |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**INapClientManagement**](inapclientmanagement.md)
</dt> </dl>

 

 





