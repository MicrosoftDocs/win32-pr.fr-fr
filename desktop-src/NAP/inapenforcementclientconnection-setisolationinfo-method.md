---
title: Méthode INapEnforcementClientConnection SetIsolationInfo (NapEnforcementClient. h)
description: Est utilisé par NapAgent pour définir les informations d’isolation du client.
ms.assetid: e92d8762-4ae9-40e5-a18e-7da757aa6f9e
keywords:
- Méthode SetIsolationInfo NAP
- Méthode SetIsolationInfo NAP, interface INapEnforcementClientConnection
- INapEnforcementClientConnection interface NAP, méthode SetIsolationInfo
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.SetIsolationInfo
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 042f0d7f6f6b36172b33cd681f2c605ff0f83b0eec987a71ee2643bf510f02ee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118133981"
---
# <a name="inapenforcementclientconnectionsetisolationinfo-method"></a>INapEnforcementClientConnection :: SetIsolationInfo, méthode

> [!Note]  
> La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10

 

La méthode **INapEnforcementClientConnection :: SetIsolationInfo** est utilisée par le NapAgent pour définir les informations d’isolation du client.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetIsolationInfo(
  [in] const IsolationInfo *isolationInfo
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*isolationInfo* \[ dans\]
</dt> <dd>

Pointeur vers une structure [**IsolationInfo**](/windows/win32/api/naptypes/ns-naptypes-isolationinfo) qui contient l’état de connectivité du client.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

D’autres codes d’erreur spécifiques à COM peuvent également être retournés.



| Code de retour                                                                                     | Description                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | Opération réussie.<br/>                                    |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Erreur d’autorisation, accès refusé.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | Limite du système, impossible d’effectuer l’opération.<br/> |



 

## <a name="remarks"></a>Remarques

Ces informations sont définies par NapAgent après le traitement d’un SoHResponse et ne doivent pas être définies par l’application.

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

 

 





