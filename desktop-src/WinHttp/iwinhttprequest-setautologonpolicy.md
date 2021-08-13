---
description: Définit la stratégie d’ouverture de session automatique actuelle.
ms.assetid: bc8e8c9c-574e-4392-b336-2c06947022ee
title: 'IWinHttpRequest :: SetAutoLogonPolicy, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWinHttpRequest.SetAutoLogonPolicy
- WinHttpRequest.SetAutoLogonPolicy
api_type:
- COM
api_location:
- Winhttp.dll
ms.openlocfilehash: b6375d5c5b6c9b6c8acebcdd05a2ad778bb37e75c067a44100a5c67a92876248
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118562885"
---
# <a name="iwinhttprequestsetautologonpolicy-method"></a>IWinHttpRequest :: SetAutoLogonPolicy, méthode

La méthode **SetAutoLogonPolicy** définit la [stratégie d’ouverture de session automatique](authentication-in-winhttp.md)actuelle.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetAutoLogonPolicy(
  [in] WinHttpRequestAutoLogonPolicy AutoLogonPolicy
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*AutoLogonPolicy* \[ dans\]
</dt> <dd>

Spécifie la stratégie d’ouverture de session automatique actuelle.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La valeur de retour est **S \_ OK** en cas de réussite ou une valeur d’erreur dans le cas contraire.

## <a name="remarks"></a>Remarques

La stratégie par défaut est [**AutoLogonPolicy \_ OnlyIfBypassProxy**](winhttprequestautologonpolicy.md).

Appelez **SetAutoLogonPolicy** pour définir la stratégie d’ouverture de session automatique avant d’appeler [**Send**](iwinhttprequest-send.md) pour envoyer la demande.

> [!Note]  
> pour Windows XP et Windows 2000, consultez la section [configuration requise](winhttp-start-page.md) pour l’exécution de la Page de démarrage de WinHTTP.

 

## <a name="examples"></a>Exemples

L’exemple de script suivant montre comment définir la stratégie d’ouverture de session automatique pour ne jamais utiliser l’authentification NTLM ou Negotiate automatiquement.


```JScript
// Instantiate a WinHttpRequest object.
var HttpReq = new ActiveXObject("WinHttp.WinHttpRequest.5.1");
    
// Open an HTTP connection.
HttpReq.Open("GET", "https://www.fabrikam.com/", false);
    
// Do not automatically send user credentials.
HttpReq.SetAutoLogonPolicy(2);

// Send the HTTP Request.
HttpReq.Send();
```



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

[**IWinHttpRequest**](iwinhttprequest-interface.md)
</dt> <dt>

[**WinHttpRequest**](winhttprequest.md)
</dt> <dt>

[Authentification dans WinHTTP](authentication-in-winhttp.md)
</dt> <dt>

[Versions de WinHTTP](winhttp-versions.md)
</dt> </dl>

 

 




