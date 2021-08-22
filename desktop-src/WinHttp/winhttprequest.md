---
Description: Cette rubrique fournit des informations sur l’utilisation de l’objet WinHttpRequest COM WinHTTP avec les langages de script.
ms.assetid: 0bbbf3dc-84b8-41d8-8627-e3d80ddcb783
title: Objet WinHttpRequest
ms.topic: reference
ms.custom: snippet-project
ms.date: 07/22/2020
topic_type:
- APIRef
- kbSyntax
api_name:
- WinHttpRequest
api_type:
- COM
api_location:
- Winhttp.dll
ms.openlocfilehash: 92fdcb9c6eff502dc5f19cb62d92af5d4db60e15890667c894f96cfb55a9e5ff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119132912"
---
# <a name="winhttprequest-object"></a>Objet WinHttpRequest

Cette rubrique fournit des informations sur l’utilisation de l’objet **WinHttpRequest** com WinHTTP avec les langages de script. Pour plus d’informations, y compris l’API C++ (WinHTTP), consultez [à propos de WinHTTP](about-winhttp.md). Pour une comparaison de ces interfaces, consultez [choix d’une interface WinHTTP](choosing-a-winhttp-interface.md) .

## <a name="example"></a> Exemple

```javascript
// Instantiate a WinHttpRequest object.
var WinHttpReq = new ActiveXObject("WinHttp.WinHttpRequest.5.1");
```

```cpp
 IWinHttpRequest *  pIWinHttpRequest = NULL;
 \\..
    hr = CLSIDFromProgID(L"WinHttp.WinHttpRequest.5.1", &clsid);

    if (SUCCEEDED(hr))
    {
        hr = CoCreateInstance(clsid, NULL,
                              CLSCTX_INPROC_SERVER,
                              IID_IWinHttpRequest,
                              (void **)&pIWinHttpRequest);
    }
```

Exemples de code tirés de la [propriété IWinHttpRequest :: Status](iwinhttprequest-status.md).



## <a name="members"></a>Membres

L’objet **WinHttpRequest** possède les types de membres suivants :

-   [Événements](#events)
-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="events"></a>Événements

L’objet **WinHttpRequest** contient ces événements.



| Événement                                                                            | Description                                                          |
|:---------------------------------------------------------------------------------|:---------------------------------------------------------------------|
| [**OnError**](iwinhttprequestevents-onerror.md)                                 | Se produit lorsqu’une erreur d’exécution se produit dans l’application.<br/> |
| [**OnResponseDataAvailable**](iwinhttprequestevents-onresponsedataavailable.md) | Se produit lorsque des données sont disponibles à partir de la réponse.<br/>          |
| [**OnResponseFinished**](iwinhttprequestevents-onresponsefinished.md)           | Se produit lorsque les données de réponse sont terminées.<br/>                |
| [**OnResponseStart**](iwinhttprequestevents-onresponsestart.md)                 | Se produit lorsque les données de réponse commencent à être reçues.<br/>      |



 

### <a name="methods"></a>Méthodes

L’objet **WinHttpRequest** a ces méthodes.



| Méthode                                                                 | Description                                                                                                                                                |
|:-----------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Arrêté**](iwinhttprequest-abort.md)                                 | Abandonne une méthode d' [**envoi**](iwinhttprequest-send.md) [WinHTTP](about-winhttp.md) .<br/>                                                              |
| [**GetAllResponseHeaders**](iwinhttprequest-getallresponseheaders.md) | Récupère tous les en-têtes de réponse HTTP.<br/>                                                                                                            |
| [**GetResponseHeader**](iwinhttprequest-getresponseheader.md)         | Récupère les en-têtes de réponse HTTP.<br/>                                                                                                            |
| [**Afficher**](iwinhttprequest-open.md)                                   | Ouvre une connexion HTTP à une ressource HTTP.<br/>                                                                                                   |
| [**Envoyer**](iwinhttprequest-send.md)                                   | Envoie une requête HTTP à un serveur HTTP.<br/>                                                                                                        |
| [**SetAutoLogonPolicy**](iwinhttprequest-setautologonpolicy.md)       | Définit la [stratégie d’ouverture de session automatique](authentication-in-winhttp.md)actuelle.<br/>                                                |
| [**SetClientCertificate**](iwinhttprequest-setclientcertificate.md)   | Sélectionne un certificat client à envoyer à un serveur HTTPs (Secure Hypertext Transfer Protocol).<br/>                                                    |
| [**SetCredentials**](iwinhttprequest-setcredentials.md)               | Définit les informations d’identification à utiliser avec un serveur HTTP, qu’il s’agisse d’un serveur d’origine ou d’un serveur proxy.<br/>                                                             |
| [**SetProxy**](iwinhttprequest-setproxy.md)                           | Définit les informations du serveur proxy.<br/>                                                                                                                  |
| [**SetRequestHeader**](iwinhttprequest-setrequestheader.md)           | Ajoute, modifie ou supprime un en-tête de requête HTTP.<br/>                                                                                               |
| [**SetTimeouts**](iwinhttprequest-settimeouts.md)                     | Spécifie, en millisecondes, les composants de délai d’attente individuels d’une opération d’envoi/réception.<br/>                                                     |
| [**WaitForResponse**](iwinhttprequest-waitforresponse.md)             | Spécifie le temps d’attente, en secondes, pour qu’une méthode d' [**envoi**](iwinhttprequest-send.md) asynchrone se termine, avec une valeur de délai d’attente facultative.<br/> |



 

### <a name="properties"></a>Propriétés

L’objet **WinHttpRequest** a ces propriétés.



| Propriété                                                            | Type d’accès           | Description                                                                     |
|:--------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------|
| [**Option**](iwinhttprequest-option.md)<br/>                 | Lecture/écriture<br/> | Définit ou récupère une valeur d’option WinHTTP.<br/>                            |
| [**ResponseBody**](iwinhttprequest-responsebody.md)<br/>     | Lecture seule<br/>  | Récupère le corps d’entité de réponse sous la forme d’un tableau d’octets non signés.<br/>    |
| [**ResponseStream**](iwinhttprequest-responsestream.md)<br/> | Lecture seule<br/>  | Récupère le corps d’entité de réponse en tant qu' [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream).<br/> |
| [**ResponseText**](iwinhttprequest-responsetext.md)<br/>     | Lecture seule<br/>  | Récupère le corps d’entité de réponse sous forme de texte.<br/>                          |
| [**Statut**](iwinhttprequest-status.md)<br/>                 | Lecture seule<br/>  | Récupère le code d’état HTTP de la dernière réponse.<br/>               |
| [**StatusText**](iwinhttprequest-statustext.md)<br/>         | Lecture seule<br/>  | Récupère le texte d’état HTTP.<br/>                                          |



 

## <a name="remarks"></a>Remarques

L’objet **WinHttpRequest** utilise l’interface [**IErrorInfo**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-ierrorinfo) pour fournir les données d’erreur. une description et une valeur d’erreur numérique peuvent être obtenues avec l’objet [Err](/previous-versions//sbf5ze0e(v=vs.85)) dans microsoft Visual Basic scripting Edition (VBScript) et l’objet [error](https://msdn.microsoft.com/library/dww52sbt.aspx) dans microsoft JScript. Les 16 bits inférieurs d’un numéro d’erreur correspondent aux valeurs figurant dans les [**messages d’erreur**](error-messages.md).

> [!Note]  
> pour plus d’Windows XP et Windows 2000, consultez [configuration requise](winhttp-start-page.md)pour l’exécution.

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows XP, Windows 2000 Professional avec les \[ applications de bureau SP3 uniquement\]<br/>            |
| Serveur minimal pris en charge<br/> | Windows server 2003, Windows 2000 server avec des \[ applications de bureau SP3 uniquement\]<br/>         |
| Composant redistribuable<br/>          | WinHTTP 5,0 et Internet Explorer 5,01 ou version ultérieure sur Windows XP et Windows 2000.<br/> |
| MIDL<br/>                      | <dl> <dt>HttpRequest. idl</dt> </dl> |
| Bibliothèque<br/>                  | <dl> <dt>WinHTTP. lib</dt> </dl>     |
| DLL<br/>                      | <dl> <dt>Winhttp.dll</dt> </dl>     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Versions de WinHTTP](winhttp-versions.md)
</dt> </dl>

 

