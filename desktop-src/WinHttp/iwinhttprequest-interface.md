---
description: L’interface IWinHttpRequest fournit toutes les méthodes inégales pour les services HTTP Microsoft Windows (WinHTTP).
ms.assetid: 6417b3b5-b74a-4c7b-acf9-87e2e814a4df
title: Interface IWinHttpRequest
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWinHttpRequest
api_type:
- COM
api_location:
- Winhttp.dll
ms.openlocfilehash: 77ebc8947ad36d2dc9efba121cdd6da2d6de359b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203166"
---
# <a name="iwinhttprequest-interface"></a>Interface IWinHttpRequest

L’interface **IWinHttpRequest** fournit toutes les méthodes inégales pour les [services http Microsoft Windows (WinHTTP)](about-winhttp.md).

## <a name="members"></a>Membres

L’interface **IWinHttpRequest** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IWinHttpRequest** a également les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

L’interface **IWinHttpRequest** possède ces méthodes.



| Méthode                                                                 | Description                                                                                                                             |
|:-----------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------|
| [**Abandon**](iwinhttprequest-abort.md)                                 | Abandonne une méthode d' [**envoi**](iwinhttprequest-send.md) [WinHTTP](about-winhttp.md) .<br/>                                           |
| [**GetAllResponseHeaders**](iwinhttprequest-getallresponseheaders.md) | Récupère tous les en-têtes de réponse HTTP.<br/>                                                                                         |
| [**GetResponseHeader**](iwinhttprequest-getresponseheader.md)         | Récupère les en-têtes de réponse HTTP.<br/>                                                                                         |
| [**Afficher**](iwinhttprequest-open.md)                                   | Ouvre une connexion HTTP à une ressource HTTP.<br/>                                                                                |
| [**Envoyer**](iwinhttprequest-send.md)                                   | Envoie une requête HTTP à un serveur HTTP.<br/>                                                                                     |
| [**SetAutoLogonPolicy**](iwinhttprequest-setautologonpolicy.md)       | Définit la [stratégie d’ouverture de session automatique](authentication-in-winhttp.md)actuelle.<br/>                             |
| [**SetClientCertificate**](iwinhttprequest-setclientcertificate.md)   | Sélectionne un certificat client à envoyer à un serveur HTTPs (Secure Hypertext Transfer Protocol).<br/>                                 |
| [**SetCredentials**](iwinhttprequest-setcredentials.md)               | Définit les informations d’identification à utiliser avec un serveur HTTP, un serveur proxy ou un serveur d’origine.<br/>                             |
| [**SetProxy**](iwinhttprequest-setproxy.md)                           | Définit les informations du serveur proxy.<br/>                                                                                               |
| [**SetRequestHeader**](iwinhttprequest-setrequestheader.md)           | Ajoute, modifie ou supprime un en-tête de requête HTTP.<br/>                                                                            |
| [**SetTimeouts**](iwinhttprequest-settimeouts.md)                     | Spécifie les différents composants de délai d’attente d’une opération d’envoi/réception, en millisecondes.<br/>                                   |
| [**WaitForResponse**](iwinhttprequest-waitforresponse.md)             | Attend la fin d’une méthode d' [**envoi**](iwinhttprequest-send.md) asynchrone, avec une valeur de délai d’attente facultative, en secondes.<br/> |



 

### <a name="properties"></a>Propriétés

L’interface **IWinHttpRequest** possède les propriétés suivantes.



| Propriété                                                            | Type d’accès           | Description                                                           |
|:--------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------|
| [**Option**](iwinhttprequest-option.md)<br/>                 | Lecture/écriture<br/> | Valeur d’option WinHTTP.<br/>                                    |
| [**ResponseBody**](iwinhttprequest-responsebody.md)<br/>     | Lecture seule<br/>  | Corps d’entité de réponse sous la forme d’un tableau d’octets non signés.<br/>    |
| [**ResponseStream**](iwinhttprequest-responsestream.md)<br/> | Lecture seule<br/>  | Corps d’entité de réponse en tant qu' [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream).<br/> |
| [**ResponseText**](iwinhttprequest-responsetext.md)<br/>     | Lecture seule<br/>  | Corps d’entité de réponse.<br/>                                  |
| [**Statu**](iwinhttprequest-status.md)<br/>                 | Lecture seule<br/>  | Code d’état HTTP de la dernière réponse.<br/>               |
| [**StatusText**](iwinhttprequest-statustext.md)<br/>         | Lecture seule<br/>  | Texte d’état HTTP.<br/>                                      |



 

## <a name="remarks"></a>Notes

L’interface **IWinHttpRequest** définie dans HttpRequest. idl est implémentée par une classe avec l’ID **CLSID \_ WinHttpRequest**. Une application obtient cette interface en appelant [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) avec l’ID de classe **CLSID \_ WinHttpRequest** et l’ID d’interface **\_ IWinHttpRequest IID**.

> [!Note]  
> Pour Windows XP et Windows 2000, consultez la section [Configuration requise](winhttp-start-page.md) pour l’exécution de la page de démarrage de WinHTTP.

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows XP, Windows 2000 Professionnel avec les \[ applications de bureau SP3 uniquement\]<br/>            |
| Serveur minimal pris en charge<br/> | Windows Server 2003, Windows 2000 Server avec les \[ applications de bureau SP3 uniquement\]<br/>         |
| Composant redistribuable<br/>          | WinHTTP 5,0 et Internet Explorer 5,01 ou version ultérieure sur Windows XP et Windows 2000.<br/> |
| MIDL<br/>                      | <dl> <dt>HttpRequest. idl</dt> </dl> |
| Bibliothèque<br/>                  | <dl> <dt>WinHTTP. lib</dt> </dl>     |
| DLL<br/>                      | <dl> <dt>Winhttp.dll</dt> </dl>     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IWinHttpRequestEvents**](iwinhttprequestevents-interface.md)
</dt> <dt>

[Versions de WinHTTP](winhttp-versions.md)
</dt> </dl>

 

