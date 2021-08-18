---
title: INapEnforcementClientConnection Initialize, méthode (NapEnforcementClient. h)
description: Initialise la connexion cliente.
ms.assetid: da72bfc3-9551-4fb0-b9a5-2931c14f618f
keywords:
- Initialiser la méthode NAP
- Méthode Initialize NAP, interface INapEnforcementClientConnection
- INapEnforcementClientConnection interface NAP, Initialize, méthode
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.Initialize
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 034fd83ac9337f6b2529b4035e6daa1b9bd06c3022ed30dbce0af74e5f6ef6cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118939660"
---
# <a name="inapenforcementclientconnectioninitialize-method"></a>INapEnforcementClientConnection :: Initialize, méthode

> [!Note]  
> La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10

 

La méthode **INapEnforcementClientConnection :: Initialize** initialise la connexion cliente.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Initialize(
  [in] EnforcementEntityId id
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ID* \[ dans\]
</dt> <dd>

Pointeur vers un [**EnforementEntityId**](nap-datatypes.md) qui identifie le client de contrainte qui demande la connexion. Cette valeur est définie par le NapAgent lors de la création de la connexion.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

D’autres codes d’erreur spécifiques à COM peuvent également être retournés.



| Code de retour                                                                                     | Description                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | Opération réussie.<br/>                                    |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Erreur d’autorisation, accès refusé.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | Limite du système, impossible d’effectuer l’opération.<br/> |



 

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

[**INapEnforcementClientConnection**](inapenforcementclientconnection.md)
</dt> </dl>

 

 





