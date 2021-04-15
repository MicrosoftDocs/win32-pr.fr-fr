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
ms.openlocfilehash: a5902b3c91b3ab12b311121bd7dcd8c415a68d6b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104485137"
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
| Client minimal pris en charge<br/> | Windows XP, Windows 2000 Professionnel avec les \[ applications de bureau SP3 uniquement\]<br/>                   |
| Serveur minimal pris en charge<br/> | Windows Server 2003, Windows 2000 Server avec les \[ applications de bureau SP3 uniquement\]<br/>                |
| En-tête<br/>                   | <dl> <dt>UpdateEndpointAuth. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>UpdateEndpointAuth. idl</dt> </dl> |
| Bibliothèque<br/>                  | <dl> <dt>UpdateEndpointAuth. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>UpdateEndpointAuth.dll</dt> </dl> |



 

 
