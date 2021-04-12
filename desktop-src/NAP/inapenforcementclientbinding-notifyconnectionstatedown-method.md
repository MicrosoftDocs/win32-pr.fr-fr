---
title: Méthode INapEnforcementClientBinding NotifyConnectionStateDown (NapEnforcementClient. h)
description: Est utilisé pour informer le NapAgent qu’une connexion à un client de contrainte s’est déroulée.
ms.assetid: 504c61c1-c8f9-46b8-87cd-c1f04846f0b3
keywords:
- Méthode NotifyConnectionStateDown NAP
- Méthode NotifyConnectionStateDown NAP, interface INapEnforcementClientBinding
- INapEnforcementClientBinding interface NAP, méthode NotifyConnectionStateDown
topic_type:
- apiref
api_name:
- INapEnforcementClientBinding.NotifyConnectionStateDown
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3129883342f493fd56a4cc81513910e8789ca4f1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104519281"
---
# <a name="inapenforcementclientbindingnotifyconnectionstatedown-method"></a>INapEnforcementClientBinding :: NotifyConnectionStateDown, méthode

> [!Note]  
> La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10

 

La méthode **INapEnforcementClientBinding :: NotifyConnectionStateDown** est utilisée pour informer le NapAgent qu’une connexion à un client de contrainte s’est déroulée.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT NotifyConnectionStateDown(
  [in] INapEnforcementClientConnection *downCxn
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*downCxn* \[ dans\]
</dt> <dd>

Pointeur COM vers l’interface [**INapEnforcementClientConnection**](inapenforcementclientconnection.md) de la connexion en aval.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

D’autres codes d’erreur spécifiques à COM peuvent également être retournés.



| Code de retour                                                                                             | Description                                                        |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                   | L'opération a réussi.<br/>                            |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl>         | Erreur d’autorisation, accès refusé.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>          | Limite du système, impossible d’effectuer l’opération.<br/> |
| <dl> <dt>**NAP \_ E \_ non \_ initialisé**</dt> </dl> | L’application n’a pas été précédemment initialisée.<br/>       |



 

## <a name="remarks"></a>Notes

Lorsque l’une des connexions établies par un client de mise en œuvre est arrêtée, le client de contrainte doit supprimer la connexion de sa liste active et informer le NapAgent à l’aide de cette méthode. Dès que cet appel est retourné, l’objet de connexion peut être libéré et libéré. NapAgent ne contient pas de références à l’objet de connexion.

À la suite de cette notification, NapAgent met à jour son état NAP du système en fonction des besoins.

Le client de contrainte doit appeler la méthode [**INapEnforcementClientBinding :: Initialize**](inapenforcementclientbinding-initialize-method.md) avant d’appeler cette méthode ou toute autre méthode de l’interface [**INapEnforcementClientBinding**](inapenforcementclientbinding.md) .

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


</dt> <dt>

[**INapEnforcementClientBinding**](inapenforcementclientbinding.md)
</dt> </dl>

 

 





