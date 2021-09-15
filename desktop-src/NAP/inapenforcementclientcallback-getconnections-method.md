---
title: Méthode INapEnforcementClientCallback GetConnections (NapEnforcementClient. h)
description: Est appelé par le NapAgent et implémenté par le client de mise en œuvre pour retourner un ensemble de connexions.
ms.assetid: 8f697217-5799-48e4-9f0b-715f516e48d9
keywords:
- Méthode GetConnections NAP
- Méthode GetConnections NAP, interface INapEnforcementClientCallback
- INapEnforcementClientCallback interface NAP, méthode GetConnections
topic_type:
- apiref
api_name:
- INapEnforcementClientCallback.GetConnections
api_location:
- NapEnforcementClient.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9acdc68dbc69cabe710414f3fa2501585f3e384e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127311978"
---
# <a name="inapenforcementclientcallbackgetconnections-method"></a>INapEnforcementClientCallback :: GetConnections, méthode

> [!Note]  
> La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10

 

La méthode de rappel **INapEnforcementClientCallback :: GetConnections** est appelée par le NapAgent et implémentée par le client de mise en œuvre pour retourner un ensemble de connexions.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetConnections(
  [out] Connections **connections
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*connexions* \[ à\]
</dt> <dd>

Pointeur vers l’ensemble actuel de [**connexions**](connections-struct.md)gérées.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Cette méthode de rappel doit retourner l’un des codes d’erreur suivants.



| Code de retour                                                                                                | Description                                                                                                                                                                                                           |
|------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                       | Retourne cette valeur si l’opération a réussi.<br/>                                                                                                                                                              |
| <dl> <dt>**\_serveur RPC \_ S \_ non disponible**</dt> </dl> | Si cette valeur est retournée, l’application est supprimée de la liste de l’algorithme de hachage des transactions et l’entrée de cache NapAgent correspondante est vidée. L’algorithme SHA défaillant peut alors se réinitialiser avec NapAgent.<br/> |



 

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

 

 





