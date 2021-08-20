---
description: Demandez un jeton pour le point de terminaison du service à l’aide des informations d’identification spécifiées.
ms.assetid: 2CA0F826-9A05-4385-AF1A-A8C05B3DAFE2
title: 'IUpdateEndpointAuthProvider :: GetEndpointToken, méthode (UpdateEndpointAuth. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUpdateEndpointAuthProvider.GetEndpointToken
api_type:
- COM
api_location:
- UpdateEndpointAuth.dll
ms.openlocfilehash: 92220a804a63d3d533f272f3d37b128875792e4ab6d82cd4f860b34a102bf260
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117919764"
---
# <a name="iupdateendpointauthprovidergetendpointtoken-method"></a>IUpdateEndpointAuthProvider :: GetEndpointToken, méthode

Demandez un jeton pour le point de terminaison du service à l’aide des informations d’identification spécifiées.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetEndpointToken(
  [in]  GUID                        serviceId,
  [in]  UpdateEndpointType          endpointType,
  [in]  UpdateEndpointProxySettings proxySettings,
  [in]  HANDLE_PTR                  hUserToken,
  [in]  UpdateEndpointAuthTokenType tokenType,
  [in]  BOOL                        fRefreshOnline,
  [out] IUnknown                    **ppEndpointToken
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

Identifie le type de point de terminaison implémenté par le service.

</dd> <dt>

*proxySettings* \[ dans\]
</dt> <dd>

Paramètres à utiliser lors de la connexion à un serveur proxy. Pour plus d’informations, consultez la structure [**UpdateEndpointProxySettings**](updateendpointproxysettings.md) .

</dd> <dt>

*hUserToken* \[ dans\]
</dt> <dd></dd> <dt>

*TokenType* \[ dans\]
</dt> <dd>

Identifie le type de jeton d’authentification utilisé pour l’authentification.

</dd> <dt>

*fRefreshOnline* \[ dans\]
</dt> <dd>

Indique que Weather WUA demande un nouveau jeton. La valeur true indique qu’un nouveau jeton est demandé. False indique qu’un nouveau jeton ou un jeton mis en cache est demandé. Pour plus d'informations, consultez la section Notes.

</dd> <dt>

*ppEndpointToken* \[ à\]
</dt> <dd>

Spécifiez le jeton de point de terminaison à utiliser.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne S \_ OK en cas de réussite. sinon, retourne un code d’erreur COM ou Windows.

## <a name="remarks"></a>Remarques

WUA affecte généralement la valeur false au paramètre fRefreshOnline lorsque cette méthode est appelée pour la première fois, puis, si une erreur de connexion se produit, WUA définit ce paramètre sur true lorsque la méthode est à nouveau appelée. Toutefois, l’implémentation de cette méthode peut demander un nouveau jeton auprès d’un service d’émission de jeton de sécurité (STS) ou fournir un jeton mis en cache à tout moment.

## <a name="requirements"></a>Conditions requises



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
</dt> </dl>

 

 




