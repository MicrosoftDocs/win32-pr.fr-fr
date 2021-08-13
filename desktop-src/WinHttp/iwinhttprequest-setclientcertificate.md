---
description: Sélectionne un certificat client à envoyer à un serveur HTTPs (Secure Hypertext Transfer Protocol).
ms.assetid: e76f1e76-5efe-46f2-9a21-064aa06fb3a8
title: 'IWinHttpRequest :: SetClientCertificate, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWinHttpRequest.SetClientCertificate
- WinHttpRequest.SetClientCertificate
api_type:
- COM
api_location:
- Winhttp.dll
ms.openlocfilehash: 1f878b93fe0db24334f406c2a6c85663e7f37a05095998f157cbf44878b39daf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118562895"
---
# <a name="iwinhttprequestsetclientcertificate-method"></a>IWinHttpRequest :: SetClientCertificate, méthode

La méthode **SetClientCertificate** sélectionne un certificat client à envoyer à un serveur HTTPS (Secure Hypertext Transfer Protocol).

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetClientCertificate(
  [in] BSTR ClientCertificate
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ClientCertificate* \[ dans\]
</dt> <dd>

Spécifie l’emplacement, le [*magasin de certificats*](glossary.md)et l’objet d’un certificat client.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La valeur de retour est **S \_ OK** en cas de réussite ou une valeur d’erreur dans le cas contraire.

## <a name="remarks"></a>Remarques

La chaîne spécifiée dans le paramètre *ClientCertificate* se compose de l’emplacement du certificat, du magasin de certificats et du nom d’objet délimités par des barres obliques inverses. Pour plus d’informations sur les composants de la chaîne de certificat, consultez [certificats clients](ssl-in-winhttp.md).

Le nom et l’emplacement du magasin de certificats sont facultatifs. Toutefois, si vous spécifiez un magasin de certificats, vous devez également spécifier l’emplacement de ce magasin de certificats. L’emplacement par défaut est \_ utilisateur actuel et le magasin de certificats par défaut est « My ». Un objet vide indique que le premier certificat du magasin de certificats doit être utilisé.

Appelez **SetClientCertificate** pour sélectionner un certificat avant d’appeler [**Send**](iwinhttprequest-send.md) pour envoyer la demande.

Microsoft Windows HTTP Services (WinHTTP) ne fournit pas de certificats clients aux serveurs proxy qui demandent des certificats pour l’authentification.

> [!Note]  
> pour Windows XP et Windows 2000, consultez la section [configuration requise](winhttp-start-page.md) pour l’exécution de la Page de démarrage de WinHTTP.

 

## <a name="examples"></a>Exemples

L’exemple de script suivant montre comment sélectionner un certificat client à envoyer avec une demande. Un certificat avec le sujet « My Middle-Tier Certificate » est choisi dans le magasin de certificats « personnel » dans le Registre sous **HKEY \_ local \_ machine**. étant donné que cet exemple de code est spécifique à Microsoft JScript, qui utilise la barre oblique inverse comme caractère d’échappement, deux barres obliques inverses contiguës sont nécessaires pour délimiter les composants de la chaîne de certificat.


```JScript
// Instantiate a WinHttpRequest object.
var HttpReq = new ActiveXObject("WinHttp.WinHttpRequest.5.1");
    
// Open an HTTP connection.
HttpReq.Open("GET", "https://www.fabrikam.com/", false);
    
// Select a client certificate.
HttpReq.SetClientCertificate(
            "LOCAL_MACHINE\\Personal\\My Middle-Tier Certificate");

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

[SSL dans WinHTTP](ssl-in-winhttp.md)
</dt> <dt>

[Versions de WinHTTP](winhttp-versions.md)
</dt> </dl>

 

 




