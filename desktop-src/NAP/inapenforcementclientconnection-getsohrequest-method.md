---
title: Méthode INapEnforcementClientConnection GetSoHRequest (NapEnforcementClient. h)
description: Obtient la demande d’intégrité actuelle.
ms.assetid: 21397a0d-ef18-494e-9c5a-43d7f6216a67
keywords:
- Méthode GetSoHRequest NAP
- Méthode GetSoHRequest NAP, interface INapEnforcementClientConnection
- INapEnforcementClientConnection interface NAP, méthode GetSoHRequest
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.GetSoHRequest
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d4cef3fc1368e3973a4643d1130cb10dbe307f102cb195a341332476bb42c691
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118939927"
---
# <a name="inapenforcementclientconnectiongetsohrequest-method"></a>INapEnforcementClientConnection :: GetSoHRequest, méthode

> [!Note]  
> La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10

 

La méthode **INapEnforcementClientConnection :: GetSoHRequest** obtient la requête SOH actuelle.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetSoHRequest(
  [out] NetworkSoHRequest **sohRequest
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*sohRequest* \[ à\]
</dt> <dd>

Pointeur vers un pointeur vers une structure [**NetworkSoHRequest**](/windows/win32/api/naptypes/ns-naptypes-networksoh) , qui est un objet blob de données opaque pour l’application.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

D’autres codes d’erreur spécifiques à COM peuvent également être retournés.



| Code de retour                                                                                     | Description                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | Opération réussie.<br/>                                    |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Erreur d’autorisation, accès refusé.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | Limite du système, impossible d’effectuer l’opération.<br/> |



 

## <a name="remarks"></a>Remarques

Cette valeur est définie par le NapAgent et interrogée par les enforceurs à envoyer sur le câble.

Un paquet SoH de longueur zéro octet n’est pas valide.

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

 

 





