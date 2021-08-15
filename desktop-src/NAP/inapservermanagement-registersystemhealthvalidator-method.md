---
title: Méthode INapServerManagement RegisterSystemHealthValidator (NapServerManagement. h)
description: Inscrit un SHV.
ms.assetid: 23f147d5-3c4e-48ca-940a-c4350ad6ecb3
keywords:
- Méthode RegisterSystemHealthValidator NAP
- Méthode RegisterSystemHealthValidator NAP, interface INapServerManagement
- INapServerManagement interface NAP, méthode RegisterSystemHealthValidator
topic_type:
- apiref
api_name:
- INapServerManagement.RegisterSystemHealthValidator
api_location:
- qsvrmgmt.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bdb5dc93c5bb927ffb25df20f37e5b2c30560153efb006f3c91bf7e97efec360
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119012567"
---
# <a name="inapservermanagementregistersystemhealthvalidator-method"></a>INapServerManagement :: RegisterSystemHealthValidator, méthode

> [!Note]  
> La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10

 

La méthode **INapServerManagement :: RegisterSystemHealthValidator** inscrit un SHV.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT RegisterSystemHealthValidator(
  [in] const NapComponentRegistrationInfo *validator,
  [in] const CLSID                        *validatorClsid
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*validateur* \[ dans\]
</dt> <dd>

Pointeur vers une structure [**NapComponentRegistrationInfo**](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo) qui contient les informations d’inscription SHV.

</dd> <dt>

*validatorClsid* \[ dans\]
</dt> <dd>

Pointeur vers le CLSID de la classe COM qui implémente l’interface [**INapSystemHealthValidator**](inapsystemhealthvalidator.md) .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

D’autres codes d’erreur spécifiques à COM peuvent également être retournés.



| Code de retour                                                                                            | Description                                                        |
|--------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                  | Opération réussie.<br/>                                    |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl>        | Erreur d’autorisation, accès refusé.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>         | Limite du système, impossible d’effectuer l’opération.<br/> |
| <dl> <dt>**\_ID en \_ conflit NAP \_ E**</dt> </dl> | L’ID SHV est déjà inscrit.<br/>                           |



 

## <a name="requirements"></a>Configuration requise



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

 

 





