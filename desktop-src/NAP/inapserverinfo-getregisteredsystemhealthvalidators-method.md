---
title: Méthode INapServerInfo GetRegisteredSystemHealthValidators (NapServerManagement. h)
description: Récupère une liste des validateurs d’intégrité inscrits.
ms.assetid: 029c7d5c-b397-415c-a530-0096de1ef771
keywords:
- Méthode GetRegisteredSystemHealthValidators NAP
- Méthode GetRegisteredSystemHealthValidators NAP, interface INapServerInfo
- INapServerInfo interface NAP, méthode GetRegisteredSystemHealthValidators
topic_type:
- apiref
api_name:
- INapServerInfo.GetRegisteredSystemHealthValidators
api_location:
- qsvrmgmt.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16ffdd4d363c994efbecdb57fe4ad7203393fd1f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127413776"
---
# <a name="inapserverinfogetregisteredsystemhealthvalidators-method"></a>INapServerInfo :: GetRegisteredSystemHealthValidators, méthode

> [!Note]  
> La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10

 

La méthode **INapServerInfo :: GetRegisteredSystemHealthValidators** récupère une liste des validateurs inscrits.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetRegisteredSystemHealthValidators(
  [out] SystemHealthEntityCount      *count,
  [out] NapComponentRegistrationInfo **validators,
  [out] CLSID                        **validatorClsids
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*nombre* \[ à\]
</dt> <dd>

Pointeur vers un [**SystemHealthEntityCount**](nap-type-constants.md) qui contient le nombre de validateurs d’intégrité du système inscrits.

</dd> <dt>

*validateurs* \[ à\]
</dt> <dd>

Pointeur vers un pointeur vers une structure [**NapComponentRegistrationInfo**](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo) qui contient les informations d’inscription SHV.

</dd> <dt>

*validatorClsids* \[ à\]
</dt> <dd>

Pointeur vers un tableau d’ID pour les validateurs d’intégrité inscrits.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

D’autres codes d’erreur spécifiques à COM peuvent également être retournés.



| Code de retour                                                                                     | Description                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | Opération réussie.<br/>                                    |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Erreur d’autorisation, accès refusé.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | Limite du système, impossible d’effectuer l’opération.<br/> |



 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                          |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                               |
| En-tête<br/>                   | <dl> <dt>NapServerManagement. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>NapServerManagement. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qsvrmgmt.dll</dt> </dl>            |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**NapComponentRegistrationInfo**](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo)
</dt> <dt>

[**INapServerInfo**](inapserverinfo.md)
</dt> </dl>

 

 





