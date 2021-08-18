---
title: Méthode INapEnforcementClientConnection SetSoHResponse (NapEnforcementClient. h)
description: Définit le SoH-Response et est utilisé par le client de mise en œuvre lors de la réception d’un paquet.
ms.assetid: 718669c7-73cf-44f4-8463-c59fdbe215cc
keywords:
- Méthode SetSoHResponse NAP
- Méthode SetSoHResponse NAP, interface INapEnforcementClientConnection
- INapEnforcementClientConnection interface NAP, méthode SetSoHResponse
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.SetSoHResponse
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97a86c1a0fc86fcef9189f9d575063cee9abdf627e1cf3c58e68d669358142f4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119626229"
---
# <a name="inapenforcementclientconnectionsetsohresponse-method"></a>INapEnforcementClientConnection :: SetSoHResponse, méthode

> [!Note]  
> La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10

 

La méthode **INapEnforcementClientConnection :: SetSoHResponse** définit la SoH-Response et est utilisée par le client de mise en œuvre lors de la réception d’un paquet.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetSoHResponse(
  [in] const NetworkSoHResponse *sohResponse
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*sohResponse* \[ dans\]
</dt> <dd>

Pointeur vers une structure [**NetworkSoHResponse**](/windows/win32/api/naptypes/ns-naptypes-networksoh) unique, qui est un objet blob de données opaque pour l’application.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

D’autres codes d’erreur spécifiques à COM peuvent également être retournés.



| Code de retour                                                                                     | Description                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | Le paquet SoH est valide.<br/>                                |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Erreur d’autorisation, accès refusé.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | Limite du système, impossible d’effectuer l’opération.<br/> |



 

## <a name="remarks"></a>Remarques

Un paquet de taille zéro est valide.

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

 

 





