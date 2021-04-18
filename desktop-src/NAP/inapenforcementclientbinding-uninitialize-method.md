---
title: INapEnforcementClientBinding méthode Uninitialize (NapEnforcementClient. h)
description: Conclut le service NapAgent.
ms.assetid: 792600e5-586f-4858-8439-75761c928745
keywords:
- Uninitialize la méthode NAP
- Uninitialize Method NAP, interface INapEnforcementClientBinding
- INapEnforcementClientBinding interface NAP, Uninitialize, méthode
topic_type:
- apiref
api_name:
- INapEnforcementClientBinding.Uninitialize
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4132ff1a498a598483758623a588fa26e8b75021
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106512617"
---
# <a name="inapenforcementclientbindinguninitialize-method"></a>INapEnforcementClientBinding :: Uninitialize, méthode

> [!Note]  
> La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10

 

La méthode **INapEnforcementClientBinding :: Uninitialize** conclut le service NapAgent.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Uninitialize();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

D’autres codes d’erreur spécifiques à COM peuvent également être retournés.



| Code de retour                                                                                     | Description                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | L'opération a réussi.<br/>                            |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Erreur d’autorisation, accès refusé.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | Limite du système, impossible d’effectuer l’opération.<br/> |



 

## <a name="remarks"></a>Notes

NapAgent bloque le traitement jusqu’à ce que tous les appels existants sur les interfaces [**INapEnforcementClientBinding**](inapenforcementclientbinding.md) et [**INapEnforcementClientCallback**](inapenforcementclientcallback.md) soient terminés. À la fin de cet appel, NapAgent libère toutes ses références sur les pointeurs COM du client de mise en œuvre.

Avant que cette fonction soit appelée, l’application doit appeler [**INapEnforcementClientBinding :: NotifyConnectionStateDown**](inapenforcementclientbinding-notifyconnectionstatedown-method.md) sur toutes ses connexions actives, afin que l’SHA puisse être averti si l’un de leurs SoH-Requests était orphelin.

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

[**INapEnforcementClientBinding::NotifyConnectionStateDown**](inapenforcementclientbinding-notifyconnectionstatedown-method.md)
</dt> <dt>

[**INapEnforcementClientCallback**](inapenforcementclientcallback.md)
</dt> </dl>

 

 





