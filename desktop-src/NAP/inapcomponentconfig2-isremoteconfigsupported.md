---
title: Méthode INapComponentConfig2 IsRemoteConfigSupported (NapCommon. h)
description: Est implémenté par les validateurs d’intégrité système (SHV) pour indiquer si la configuration distante est prise en charge.
ms.assetid: c4b8e60b-ed60-49ec-b4d6-4e1575e4d1a5
keywords:
- Méthode IsRemoteConfigSupported NAP
- Méthode IsRemoteConfigSupported NAP, interface INapComponentConfig2
- INapComponentConfig2 interface NAP, méthode IsRemoteConfigSupported
topic_type:
- apiref
api_name:
- INapComponentConfig2.IsRemoteConfigSupported
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a42ae316063fc14054c8ffeb6e3987794bc33021441621ee231c9e839fc00248
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118621766"
---
# <a name="inapcomponentconfig2isremoteconfigsupported-method"></a>INapComponentConfig2 :: IsRemoteConfigSupported, méthode

> [!Note]  
> La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10

 

La méthode **IsRemoteConfigSupported** est implémentée par les validateurs d’intégrité système (SHV) pour indiquer si la configuration distante est prise en charge.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT IsRemoteConfigSupported(
  [out] BOOL  *isSupported,
  [out] UINT8 *remoteConfigType
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*IsSupported* \[ à\]
</dt> <dd>

Pointeur vers un booléen dont la valeur est **true** si le composant prend en charge la configuration distante, et **false** dans le cas contraire.

</dd> <dt>

*remoteConfigType* \[ à\]
</dt> <dd>

Indique le type de configuration à distance pris en charge à l’aide de la valeur de l’énumération [**RemoteConfigurationType**](/windows/win32/api/naptypes/ne-naptypes-remoteconfigurationtype) :



| Valeur                                                                                                 | Signification                                                                                                                                                                                                                                                                                         |
|-------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>remoteConfigTypeMachine</dt> </dl>    | [**InvokeUIForMachine**](inapcomponentconfig2-invokeuiformachine.md) est implémenté.<br/>                                                                                                                                                                                                |
| <dl> <dt>remoteConfigTypeConfigBlob</dt> </dl> | [**InvokeUIFromConfigBlob**](inapcomponentconfig2-invokeuifromconfigblob.md) est implémenté. [**INapComponentConfig :: GetConfig**](inapcomponentconfig-getconfig.md) et [**INapComponentConfig :: setconfig**](inapcomponentconfig-setconfig.md) peuvent être appelés à distance à l’aide de DCOM.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

retourne \_ la valeur OK si l’opération réussit ou l’un des codes d’erreur Windows standard.

## <a name="remarks"></a>Remarques

Si ni [**InvokeUIForMachine**](inapcomponentconfig2-invokeuiformachine.md) ni [**InvokeUIFromConfigBlob**](inapcomponentconfig2-invokeuifromconfigblob.md) n’est implémentée, la configuration distante de la SHV n’est pas possible.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                     |
| En-tête<br/>                   | <dl> <dt>NapCommon. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>NapCommon. idl</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**INapComponentConfig2**](inapcomponentconfig2.md)
</dt> </dl>

 

 





