---
title: Méthode INapServerManagement UnregisterSystemHealthValidator (NapServerManagement. h)
description: Permet d’annuler l’inscription d’un SHV auprès du serveur NAP.
ms.assetid: f4148df1-a230-4845-ac8b-9e04be9e0d6c
keywords:
- Méthode UnregisterSystemHealthValidator NAP
- Méthode UnregisterSystemHealthValidator NAP, interface INapServerManagement
- INapServerManagement interface NAP, méthode UnregisterSystemHealthValidator
topic_type:
- apiref
api_name:
- INapServerManagement.UnregisterSystemHealthValidator
api_location:
- qsvrmgmt.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0715445504b862d9ae9e8478b543f8e80378f08
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127413769"
---
# <a name="inapservermanagementunregistersystemhealthvalidator-method"></a>INapServerManagement :: UnregisterSystemHealthValidator, méthode

> [!Note]  
> La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10

 

La méthode **INapServerManagement :: UnregisterSystemHealthValidator** est utilisée pour annuler l’inscription d’un SHV auprès du serveur NAP.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT UnregisterSystemHealthValidator(
  [in] SystemHealthEntityId id
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ID* \[ dans\]
</dt> <dd>

[**SystemHealthEntityId**](nap-type-constants.md) qui contient l’identificateur unique de la SHV dont l’inscription doit être annulée.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

D’autres codes d’erreur spécifiques à COM peuvent également être retournés.



| Code de retour                                                                                     | Description                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | Opération réussie.<br/>                                    |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Erreur d’autorisation, accès refusé.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | Limite du système, impossible d’effectuer l’opération.<br/> |



 

## <a name="remarks"></a>Notes

Si des appels asynchrones sont en attente sur le SHV, ils seront terminés plus tard et seront ignorés.

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

[**INapServerManagement**](inapservermanagement.md)
</dt> </dl>

 

 





