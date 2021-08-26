---
description: Retourne le type de jeton d’authentification par défaut pour le point de terminaison du service.
ms.assetid: DF60C49A-89FE-4EEB-8E82-C2C43F2D2F2A
title: 'IUpdateEndpointAuthProvider :: GetPreferredEndpointTokenType, méthode (UpdateEndpointAuth. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUpdateEndpointAuthProvider.GetPreferredEndpointTokenType
api_type:
- COM
api_location:
- UpdateEndpointAuth.dll
ms.openlocfilehash: a9b7d15d6d27170106118c720d25567389884c50e27aac202adedf00290236c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119994579"
---
# <a name="iupdateendpointauthprovidergetpreferredendpointtokentype-method"></a>IUpdateEndpointAuthProvider :: GetPreferredEndpointTokenType, méthode

Retourne le type de jeton d’authentification par défaut pour le point de terminaison du service.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetPreferredEndpointTokenType(
  [in]  GUID               serviceId,
  [in]  UpdateEndpointType endpointType,
  [in]  ULONG              ulRequestedTypes,
  [out] ULONG              *pulPreferredTokenTypes
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ServiceId* \[ dans\]
</dt> <dd>

Identifie le service à mettre à jour.

</dd> <dt>

*endpointType* \[ dans\]
</dt> <dd>

Identifie le type de point de terminaison tneeded pour se connecter au service.

</dd> <dt>

*ulRequestedTypes* \[ dans\]
</dt> <dd>

Identifie l’ensemble de jetons qui sont pris en charge par le point de terminaison.

</dd> <dt>

*pulPreferredTokenTypes* \[ à\]
</dt> <dd>

Spécifiez l’ensemble de types de jetons d’authentification par défaut. (Défini sur 0 pour indiquer qu’aucun jeton d’authentification n’est nécessaire).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne S \_ OK en cas de réussite. sinon, retourne un code d’erreur COM ou Windows.

## <a name="remarks"></a>Remarques

Lorsque cette méthode est retournée, WUA choisit un type de jeton parmi les types préférés et le transmet au paramètre tokenType de la méthode [**GetEndpointToken**](iupdateendpointauthprovider-getendpointtoken.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows XP, Windows 2000 Professional avec les \[ applications de bureau SP3 uniquement\]<br/>                   |
| Serveur minimal pris en charge<br/> | Windows server 2003, Windows 2000 server avec des \[ applications de bureau SP3 uniquement\]<br/>                |
| En-tête<br/>                   | <dl> <dt>UpdateEndpointAuth. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>UpdateEndpointAuth. idl</dt> </dl> |
| Bibliothèque<br/>                  | <dl> <dt>UpdateEndpointAuth. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>UpdateEndpointAuth.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IUpdateEndpointAuthProvider**](iupdateendpointauthprovider.md)
</dt> <dt>

[**GetEndpointToken**](iupdateendpointauthprovider-getendpointtoken.md)
</dt> </dl>

 

 




