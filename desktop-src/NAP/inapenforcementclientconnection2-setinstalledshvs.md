---
title: Méthode INapEnforcementClientConnection2 SetInstalledShvs (NapEnforcementClient. h)
description: Utilisé par l’agent NAP pour définir les programmes de validation d’intégrité système (SHV) installés sur le client.
ms.assetid: 38aa99b9-a15a-414d-91fc-128de8f5a654
keywords:
- Méthode SetInstalledShvs NAP
- Méthode SetInstalledShvs NAP, interface INapEnforcementClientConnection2
- INapEnforcementClientConnection2 interface NAP, méthode SetInstalledShvs
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection2.SetInstalledShvs
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6651cd5248094f82d9faa1862492f82648e94125
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127413789"
---
# <a name="inapenforcementclientconnection2setinstalledshvs-method"></a>INapEnforcementClientConnection2 :: SetInstalledShvs, méthode

> [!Note]  
> La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10

 

La méthode **SetInstalledShvs** est utilisée par l’agent NAP pour définir les validateurs d’intégrité du système installés sur le client.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetInstalledShvs(
  [in] SystemHealthEntityCount count,
  [in] SystemHealthEntityId    *ids
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*nombre* \[ dans\]
</dt> <dd>

Valeur [SystemHealthEntityCount](nap-datatypes.md) qui spécifie le nombre de validateurs d’intégrité de l’installation dans *IDS*.

</dd> <dt>

*ID* \[ dans\]
</dt> <dd>

Pointeur vers une valeur [SystemHealthEntityId](nap-datatypes.md) qui contient une liste d’ID SHV à installer.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

D’autres codes d’erreur spécifiques à COM peuvent également être retournés.



| Code de retour                                                                                  | Description                                    |
|----------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>        | La méthode a réussi.<br/>          |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Le paramètre *Count* était 0 (zéro).<br/> |



 

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

[**INapEnforcementClientConnection2**](inapenforcementclientconnection2.md)
</dt> </dl>

 

 





