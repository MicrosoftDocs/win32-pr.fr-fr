---
title: Méthode INapEnforcementClientBinding NotifySoHChangeFailure (NapEnforcementClient. h)
description: Est utilisé par le client de mise en œuvre pour informer NapAgent qu’il n’a pas pu traiter un NotifySoHChange INapEnforcementClientCallback précédent.
ms.assetid: 2de1626c-ffda-4191-90c4-72d0275965d9
keywords:
- Méthode NotifySoHChangeFailure NAP
- Méthode NotifySoHChangeFailure NAP, interface INapEnforcementClientBinding
- INapEnforcementClientBinding interface NAP, méthode NotifySoHChangeFailure
topic_type:
- apiref
api_name:
- INapEnforcementClientBinding.NotifySoHChangeFailure
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f91ae79656ec8909a8bff041e3ddc2714f1cbd17a65362e08731e9ca411d57f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118134217"
---
# <a name="inapenforcementclientbindingnotifysohchangefailure-method"></a>INapEnforcementClientBinding :: NotifySoHChangeFailure, méthode

> [!Note]  
> La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10

 

La méthode **INapEnforcementClientBinding :: NotifySoHChangeFailure** est utilisée par le client de mise en œuvre pour informer le NapAgent qu’il n’a pas pu traiter un [**INapEnforcementClientCallback :: NotifySoHChange**](inapenforcementclientcallback-notifysohchange-method.md)précédent.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT NotifySoHChangeFailure();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

D’autres codes d’erreur spécifiques à COM peuvent également être retournés.



| Code de retour                                                                                             | Description                                                        |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                   | L'opération a réussi.<br/>                            |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl>         | Erreur d’autorisation, accès refusé.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>          | Limite du système, impossible d’effectuer l’opération.<br/> |
| <dl> <dt>**NAP \_ E \_ non \_ initialisé**</dt> </dl> | L’application n’a pas été précédemment initialisée.<br/>       |



 

## <a name="remarks"></a>Remarques

À la suite de cette méthode, l’appel de NapAgent tente d’appliquer la modification de SoH ultérieurement en appelant [**INapEnforcementClientCallback :: NotifySoHChange**](inapenforcementclientcallback-notifysohchange-method.md) . Une fois que le client de contrainte a appelé [**INapEnforcementClientBinding :: GetSoHRequest**](inapenforcementclientbinding-getsohrequest-method.md), il doit ensuite appliquer la modification, ce qui signifie qu’aucune défaillance n’est gérée par le NapAgent après ce point.

Le client de contrainte doit appeler la méthode [**INapEnforcementClientBinding :: Initialize**](inapenforcementclientbinding-initialize-method.md) avant d’appeler cette méthode ou toute autre méthode de l’interface [**INapEnforcementClientBinding**](inapenforcementclientbinding.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                                      |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                                |
| En-tête<br/>                   | <dl> <dt>NapEnforcementClient. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>NapEnforcementClient. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qagent.dll</dt> </dl>               |



## <a name="see-also"></a>Voir aussi

<dl> <dt>


</dt> <dt>

[**INapEnforcementClientBinding**](inapenforcementclientbinding.md)
</dt> <dt>

[**INapEnforcementClientBinding::GetSoHRequest**](inapenforcementclientbinding-getsohrequest-method.md)
</dt> <dt>

[**INapEnforcementClientCallback::NotifySoHChange**](inapenforcementclientcallback-notifysohchange-method.md)
</dt> </dl>

 

 





