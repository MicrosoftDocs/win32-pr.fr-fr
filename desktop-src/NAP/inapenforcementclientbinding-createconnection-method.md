---
title: INapEnforcementClientBinding CreateConnection, méthode (NapEnforcementClient. h)
description: Est utilisé par les enforceurs pour créer des objets de connexion.
ms.assetid: 4d31928f-1a10-4168-a53c-256cbbf3e5c9
keywords:
- CreateConnection, méthode NAP
- CreateConnection, méthode NAP, interface INapEnforcementClientBinding
- INapEnforcementClientBinding interface NAP, CreateConnection, méthode
topic_type:
- apiref
api_name:
- INapEnforcementClientBinding.CreateConnection
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4bf530b9fefd0e5b361f4f86ef2421712c750be9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032656"
---
# <a name="inapenforcementclientbindingcreateconnection-method"></a>INapEnforcementClientBinding :: CreateConnection, méthode

> [!Note]  
> La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10

 

La méthode de fabrique **INapEnforcementClientBinding :: CreateConnection** est utilisée par les enforceurs pour créer des objets de connexion.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT CreateConnection(
  [out] INapEnforcementClientConnection **connection
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*connexion* \[ à\]
</dt> <dd>

Pointeur COM vers une nouvelle interface [**INapEnforcementClientConnection**](inapenforcementclientconnection.md) retournée par le système NAP.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

D’autres codes d’erreur spécifiques à COM peuvent également être retournés.



| Code de retour                                                                                     | Description                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | L'opération a réussi.<br/>                            |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Erreur d’autorisation, accès refusé.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | Limite du système, impossible d’effectuer l’opération.<br/> |



 

## <a name="remarks"></a>Notes

Le client de contrainte doit appeler la méthode [**INapEnforcementClientBinding :: Initialize**](inapenforcementclientbinding-initialize-method.md) avant d’appeler cette méthode ou toute autre méthode de l’interface [**INapEnforcementClientBinding**](inapenforcementclientbinding.md) .

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


</dt> <dt>

[**INapEnforcementClientBinding**](inapenforcementclientbinding.md)
</dt> <dt>

[**INapEnforcementClientConnection**](inapenforcementclientconnection.md)
</dt> </dl>

 

 





