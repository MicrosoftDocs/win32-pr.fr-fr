---
title: Méthode INapEnforcementClientCallback NotifySoHChange (NapEnforcementClient. h)
description: Est utilisé par le NapAgent pour informer le client de contrainte des modifications de déclaration d’intégrité.
ms.assetid: da8b9238-6371-4a6a-a9e7-ab791391ffc2
keywords:
- Méthode NotifySoHChange NAP
- Méthode NotifySoHChange NAP, interface INapEnforcementClientCallback
- INapEnforcementClientCallback interface NAP, méthode NotifySoHChange
topic_type:
- apiref
api_name:
- INapEnforcementClientCallback.NotifySoHChange
api_location:
- NapEnforcementClient.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b405bca5ae27a68eea780dfcb922d1f986f475c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127311977"
---
# <a name="inapenforcementclientcallbacknotifysohchange-method"></a>INapEnforcementClientCallback :: NotifySoHChange, méthode

> [!Note]  
> La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10

 

La méthode de rappel **INapEnforcementClientCallback :: NotifySoHChange** est utilisée par le NapAgent pour informer le client de contrainte des modifications de SOH.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT NotifySoHChange();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur de retour

Cette méthode de rappel doit retourner l’un des codes d’erreur suivants.



| Code de retour                                                                                                | Description                                                                                                                                                                                                           |
|------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                       | Retourne cette valeur si l’opération a réussi.<br/>                                                                                                                                                              |
| <dl> <dt>**\_serveur RPC \_ S \_ non disponible**</dt> </dl> | Si cette valeur est retournée, l’application est supprimée de la liste de l’algorithme de hachage des transactions et l’entrée de cache NapAgent correspondante est vidée. L’algorithme SHA défaillant peut alors se réinitialiser avec NapAgent.<br/> |



 

## <a name="remarks"></a>Remarques

L’achèvement de la correction du système est un événement de modification de l’intégrité du système. Cela signifie que vous devez appeler **NotifySoHChange** quand une notification [**INapSystemHealthAgentCallback :: GetFixupInfo**](inapsystemhealthagentcallback-getfixupinfo-method.md) indique que le client est corrigé. Lorsqu’un client est résolu, le membre d' **État** de la structure [**FixupInfo**](/windows/win32/api/naptypes/ns-naptypes-fixupinfo) retournée par **GetFixupInfo** a la valeur **fixupStateSuccess**.

Après avoir été appelé par le NapAgent via ce rappel, l’agent d’application doit ensuite appeler [**INapEnforcementClientBinding :: GetSoHRequest**](inapenforcementclientbinding-getsohrequest-method.md) pour récupérer la nouvelle requête. Cet appel peut être effectué sur le même thread que **INapEnforcementClientCallback :: NotifySoHChange**.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                                      |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                                |
| En-tête<br/>                   | <dl> <dt>NapEnforcementClient. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>NapEnforcementClient. idl</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**INapEnforcementClientCallback**](inapenforcementclientcallback.md)
</dt> </dl>

 

 





