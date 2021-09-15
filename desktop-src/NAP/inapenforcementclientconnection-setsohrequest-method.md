---
title: Méthode INapEnforcementClientConnection SetSoHRequest (NapEnforcementClient. h)
description: Définit la requête SoH.
ms.assetid: 87dbb982-a337-4644-a2fe-970bfdd6c140
keywords:
- Méthode SetSoHRequest NAP
- Méthode SetSoHRequest NAP, interface INapEnforcementClientConnection
- INapEnforcementClientConnection interface NAP, méthode SetSoHRequest
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.SetSoHRequest
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 92559d532e99bfa29d7f62fd29b279db20f2c0a3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127413799"
---
# <a name="inapenforcementclientconnectionsetsohrequest-method"></a>INapEnforcementClientConnection :: SetSoHRequest, méthode

> [!Note]  
> La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10

 

La méthode **INapEnforcementClientConnection :: SetSoHRequest** définit la requête SOH.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetSoHRequest(
  [in, unique] const NetworkSoHRequest *sohRequest
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*sohRequest* \[ dans\]
</dt> <dd>

Pointeur vers une structure [**NetworkSoHRequest**](/windows/win32/api/naptypes/ns-naptypes-networksoh) unique, qui est un objet blob de données opaque pour l’application.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

D’autres codes d’erreur spécifiques à COM peuvent également être retournés.



| Code de retour                                                                                     | Description                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | Le paquet SoH est valide.<br/>                                |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Erreur d’autorisation, accès refusé.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | Limite du système, impossible d’effectuer l’opération.<br/> |



 

## <a name="remarks"></a>Notes

Cette valeur est définie par le NapAgent et interrogée par les enforceurs à envoyer sur le câble.

Un paquet SoH de longueur zéro octet n’est pas valide.

## <a name="requirements"></a>Spécifications



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

 

 





