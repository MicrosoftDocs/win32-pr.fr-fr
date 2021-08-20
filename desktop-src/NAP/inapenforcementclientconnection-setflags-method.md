---
title: Méthode INapEnforcementClientConnection SetFlags (NapEnforcementClient. h)
description: Est utilisé pour différencier les réponses premières des réponses en raison des SoHRequests mises en cache par les enforceurs. | Méthode INapEnforcementClientConnection SetFlags (NapEnforcementClient. h)
ms.assetid: 2f35bcdf-662c-431f-a39e-a7c758f35603
keywords:
- Méthode SetFlags NAP
- Méthode SetFlags NAP, interface INapEnforcementClientConnection
- INapEnforcementClientConnection interface NAP, méthode SetFlags
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.SetFlags
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 306ab4312138136dc00aec701d322ed82e95a731c8c4f418fb2cfaddd921ed50
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118133991"
---
# <a name="inapenforcementclientconnectionsetflags-method"></a>INapEnforcementClientConnection :: SetFlags, méthode

> [!Note]  
> La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10

 

La méthode **INapEnforcementClientConnection :: SetFlags** est utilisée pour différencier les réponses premières des réponses en raison des SoHRequests mises en cache par les enforceurs.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetFlags(
  [in] UINT8 flags
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*indicateurs* \[ dans\]
</dt> <dd>

Indicateurs qui déterminent si le [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh) est dû à un **SoHRequest** mis en cache. Si *Flags* a la valeur [**freshSoHRequest**](nap-type-constants.md), il s’agit d’une nouvelle demande ; dans le cas contraire, il s’agit d’une demande mise en cache.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

D’autres codes d’erreur spécifiques à COM peuvent également être retournés.



| Code de retour                                                                                     | Description                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | Opération réussie.<br/>                                    |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Erreur d’autorisation, accès refusé.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | Limite du système, impossible d’effectuer l’opération.<br/> |



 

## <a name="remarks"></a>Remarques

Cette valeur est définie par NapAgent.

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

 

 





