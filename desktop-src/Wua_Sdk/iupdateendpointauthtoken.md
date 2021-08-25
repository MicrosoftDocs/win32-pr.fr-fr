---
description: Fournit les méthodes que WUA peut utiliser pour collecter des informations sur le jeton de point de terminaison.
ms.assetid: 52D22909-B926-426F-98C7-643C4469D021
title: Interface IUpdateEndpointAuthToken (UpdateEndpointAuth. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUpdateEndpointAuthToken
api_type:
- COM
api_location:
- UpdateEndpointAuth.dll
ms.openlocfilehash: 7b5afa1e9039b7f210dfbf71c8bceff4a7b438b413844a7a7e55dec0fd9fea8d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119855759"
---
# <a name="iupdateendpointauthtoken-interface"></a>Interface IUpdateEndpointAuthToken

Fournit les méthodes que WUA peut utiliser pour collecter des informations sur le jeton de point de terminaison.

## <a name="members"></a>Membres

L’interface **IUpdateEndpointAuthToken** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IUpdateEndpointAuthToken** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **IUpdateEndpointAuthToken** possède ces méthodes.



| Méthode                                                                                | Description                                                                                                                 |
|:--------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------|
| [**ServiceID**](iupdateendpointauthtoken-serviceid.md)                               | Obtient l’identificateur du service à authentifier.<br/>                                                          |
| [**SigningKey**](iupdateendpointauthtoken-signingkey.md)                             | Obtient la clé utilisée pour signer les messages sortants entre l’ordinateur client et le Sercvice.<br/>                        |
| [**TokenData**](iupdateendpointauthtoken-tokendata.md)                               | Obtient les données XML (envoyées sur le réseau) qui représentent le jeton. <br/>                                               |
| [**TokenReferenceAttached**](iupdateendpointauthtoken-tokenreferenceattached.md)     | Obtient le format XML d’une référence jointe au jeton.<br/>                                                       |
| [**TokenReferenceUnattached**](iupdateendpointauthtoken-tokenreferenceunattached.md) | Obtient le format XML d’une référence non attachée au jeton.<br/>                                                     |
| [**TokenType**](iupdateendpointauthtoken-tokentype.md)                               | Obtient le type du jeton de point de terminaison, tel qu’un jeton WS-Security SAML (Security Assertion Markup Language) 1,1. <br/> |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows XP, Windows 2000 Professional avec les \[ applications de bureau SP3 uniquement\]<br/>                   |
| Serveur minimal pris en charge<br/> | Windows server 2003, Windows 2000 server avec des \[ applications de bureau SP3 uniquement\]<br/>                |
| En-tête<br/>                   | <dl> <dt>UpdateEndpointAuth. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>UpdateEndpointAuth. idl</dt> </dl> |
| Bibliothèque<br/>                  | <dl> <dt>UpdateEndpointAuth. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>UpdateEndpointAuth.dll</dt> </dl> |



 

 
