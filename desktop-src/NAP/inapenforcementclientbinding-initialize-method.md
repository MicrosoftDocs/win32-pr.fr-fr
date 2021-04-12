---
title: INapEnforcementClientBinding Initialize, méthode (NapEnforcementClient. h)
description: Démarre automatiquement le service NapAgent.
ms.assetid: 6b51043d-a8e7-41e4-9da9-e7f18f9bd068
keywords:
- Initialiser la méthode NAP
- Méthode Initialize NAP, interface INapEnforcementClientBinding
- INapEnforcementClientBinding interface NAP, Initialize, méthode
topic_type:
- apiref
api_name:
- INapEnforcementClientBinding.Initialize
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee4d385e47bbbfe2e315d0a93d1f92542e8328e2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464830"
---
# <a name="inapenforcementclientbindinginitialize-method"></a>INapEnforcementClientBinding :: Initialize, méthode

> [!Note]  
> La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10

 

La méthode **INapEnforcementClientBinding :: Initialize** démarre automatiquement le service NapAgent.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Initialize(
  [in] EnforcementEntityId           id,
  [in] INapEnforcementClientCallback *callback
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ID* \[ dans\]
</dt> <dd>

[**EnforcementEntityId**](nap-datatypes.md) qui identifie le client de mise en œuvre et sa version.

</dd> <dt>

*rappel* \[ dans\]
</dt> <dd>

Pointeur COM vers une interface [**INapEnforcementClientCallback**](inapenforcementclientcallback.md) utilisée par le NapAgent pour rappeler les clients de mise en œuvre avec Notify/Process. Le NapAgent contient une référence à l’objet associé à cette interface jusqu’à ce que [**INapEnforcementClientBinding :: Uninitialize**](inapenforcementclientbinding-uninitialize-method.md) soit appelé.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

D’autres codes d’erreur spécifiques à COM peuvent également être retournés.



| Code de retour                                                                                                         | Description                                                                              |
|---------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                               | L'opération a réussi.<br/>                                                  |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl>                     | Erreur d’autorisation, accès refusé.<br/>                                             |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>                      | Limite du système, impossible d’effectuer l’opération.<br/>                       |
| <dl> <dt>**HRESULT (erreur \_ déjà \_ initialisée)**</dt> </dl> | Si l’application d’application a été précédemment initialisée, ce code d’erreur est retourné.<br/> |
| <dl> <dt>**NAP \_ E \_ non \_ inscrit**</dt> </dl>              | Si l’application n’a pas été inscrite précédemment, ce code d’erreur est retourné.<br/>      |



 

## <a name="remarks"></a>Notes

Le client de contrainte doit appeler la méthode **INapEnforcementClientBinding :: Initialize** avant d’appeler toute autre méthode de l’interface [**INapEnforcementClientBinding**](inapenforcementclientbinding.md) .

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

[**INapEnforcementClientBinding :: Uninitialize**](inapenforcementclientbinding-uninitialize-method.md)
</dt> </dl>

 

 





