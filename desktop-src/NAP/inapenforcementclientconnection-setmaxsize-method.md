---
title: Méthode INapEnforcementClientConnection SetMaxSize (NapEnforcementClient. h)
description: Définit la taille maximale du paquet SoH pour ce client.
ms.assetid: 30d3747d-bcf8-41b3-b0af-29f20d48417b
keywords:
- Méthode SetMaxSize NAP
- Méthode SetMaxSize NAP, interface INapEnforcementClientConnection
- INapEnforcementClientConnection interface NAP, méthode SetMaxSize
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.SetMaxSize
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b10d7bc1a023371683f17bb3e6e12cd578fa964
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384387"
---
# <a name="inapenforcementclientconnectionsetmaxsize-method"></a>INapEnforcementClientConnection :: SetMaxSize, méthode

> [!Note]  
> La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10

 

La méthode **INapEnforcementClientConnection :: SetMaxSize** définit la taille maximale du paquet SOH pour ce client.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetMaxSize(
  [in] ProtocolMaxSize maxSize
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*MaxSize* \[ dans\]
</dt> <dd>

Structure [**ProtocolMaxSize**](nap-datatypes.md) qui indique la taille maximale, en octets, du paquet SOH.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

D’autres codes d’erreur spécifiques à COM peuvent également être retournés.



| Code de retour                                                                                     | Description                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | Opération réussie.<br/>                                    |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Erreur d’autorisation, accès refusé.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | Limite du système, impossible d’effectuer l’opération.<br/> |



 

## <a name="remarks"></a>Notes

Cette valeur est définie par le client de mise en œuvre.

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

[**INapEnforcementClientConnection**](inapenforcementclientconnection.md)
</dt> </dl>

 

 





