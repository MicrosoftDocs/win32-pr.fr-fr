---
description: Contient les méthodes utilisées pour négocier le type de jeton utilisé pour authentifier le point de terminaison d’un service.
ms.assetid: F6177B24-C166-4BEC-83D6-3AD5B5B3CF08
title: Interface IUpdateEndpointAuthProvider (UpdateEndpointAuth. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUpdateEndpointAuthProvider
api_type:
- COM
api_location:
- UpdateEndpointAuth.dll
ms.openlocfilehash: 3cbc51ab0f1192e20612829532b907e3644a7da3f99fdedd8e3dbd45a780c54d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119994569"
---
# <a name="iupdateendpointauthprovider-interface"></a>Interface IUpdateEndpointAuthProvider

L’interface **IUpdateEndpointAuthProvider** contient les méthodes utilisées pour négocier le type de jeton utilisé pour authentifier le point de terminaison d’un service.

## <a name="members"></a>Membres

L’interface **IUpdateEndpointAuthProvider** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IUpdateEndpointAuthProvider** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **IUpdateEndpointAuthProvider** possède ces méthodes.



| Méthode                                                                                             | Description                                                                                    |
|:---------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------|
| [**GetEndpointToken**](iupdateendpointauthprovider-getendpointtoken.md)                           | Demandez un jeton pour le point de terminaison du service à l’aide des informations d’identification spécifiées.<br/>    |
| [**GetPreferredEndpointTokenType**](iupdateendpointauthprovider-getpreferredendpointtokentype.md) | Retourne le type de jeton d’authentification par défaut pour le point de terminaison du service.<br/> |



 

## <a name="remarks"></a>Remarques

WUA appelle la méthode [**GetPreferredEndpointTokenType**](iupdateendpointauthprovider-getpreferredendpointtokentype.md) de cette interface pour démarrer le processus de négociation. Lorsque l’appel est effectué, WUA passe dans l’identificateur de service, le type de point de terminaison implémenté par le service et les types de jetons disponibles. L’implémentation de cette interface retourne ensuite les types de jetons qu’elle préfère utiliser.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows XP, Windows 2000 Professional avec les \[ applications de bureau SP3 uniquement\]<br/>                   |
| Serveur minimal pris en charge<br/> | Windows server 2003, Windows 2000 server avec des \[ applications de bureau SP3 uniquement\]<br/>                |
| En-tête<br/>                   | <dl> <dt>UpdateEndpointAuth. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>UpdateEndpointAuth. idl</dt> </dl> |
| Bibliothèque<br/>                  | <dl> <dt>UpdateEndpointAuth. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>UpdateEndpointAuth.dll</dt> </dl> |



 

 
