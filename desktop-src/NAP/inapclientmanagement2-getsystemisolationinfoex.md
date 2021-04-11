---
title: Méthode INapClientManagement2 GetSystemIsolationInfoEx (NapManagement. h)
description: Récupère des informations sur l’état d’isolement et l’état d’isolement étendu du NapClient.
ms.assetid: 614bcf19-873e-4043-98b2-dcb152bae3e2
keywords:
- Méthode GetSystemIsolationInfoEx NAP
- Méthode GetSystemIsolationInfoEx NAP, interface INapClientManagement2
- INapClientManagement2 interface NAP, méthode GetSystemIsolationInfoEx
topic_type:
- apiref
api_name:
- INapClientManagement2.GetSystemIsolationInfoEx
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e75a6554ea7e55c3bebe35b797f888494a55627
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032658"
---
# <a name="inapclientmanagement2getsystemisolationinfoex-method"></a>INapClientManagement2 :: GetSystemIsolationInfoEx, méthode

> [!Note]  
> La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10

 

La méthode **GetSystemIsolationInfoEx** récupère les informations relatives à l’état d’isolement et à l’état d’isolement étendu du NapClient.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetSystemIsolationInfoEx(
  [out] IsolationInfoEx **isolationInfo,
  [out] BOOL            *unknownConnections
) const;
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*isolationInfo* \[ à\]
</dt> <dd>

Pointeur vers un pointeur vers une structure [**IsolationInfoEx**](/windows/win32/api/naptypes/ns-naptypes-isolationinfoex) qui contient les informations d’état d’isolement.

</dd> <dt>

*unknownConnections* \[ à\]
</dt> <dd>

Pointeur vers une valeur BOOLÉENNE qui est **true** si l’une des connexions est dans un état inconnu et **false** dans le cas contraire.

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

L’algorithme SHA doit libérer la structure [**IsolationInfoEx**](/windows/win32/api/naptypes/ns-naptypes-isolationinfoex) en appelant [**FreeIsolationInfoEx**](freeisolationinfoex.md).

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

[**INapClientManagement2**](inapclientmanagement2.md)
</dt> </dl>

 

 





