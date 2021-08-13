---
description: Définit les informations du serveur proxy.
ms.assetid: 279d0557-2718-4c50-b84c-cc7c8def57a6
title: 'IWinHttpRequest :: SetProxy, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWinHttpRequest.SetProxy
- WinHttpRequest.SetProxy
api_type:
- COM
api_location:
- Winhttp.dll
ms.openlocfilehash: bb85466da6b7492d04bd2e69f4cd51c0c390e9595df13af8d7e6768596771822
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118562592"
---
# <a name="iwinhttprequestsetproxy-method"></a>IWinHttpRequest :: SetProxy, méthode

La méthode **SetProxy** définit les informations du serveur proxy.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetProxy(
  [in]           HTTPREQUEST_PROXY_SETTING ProxySetting,
  [in, optional] VARIANT                   ProxyServer,
  [in, optional] VARIANT                   BypassList
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ProxySetting* \[ dans\]
</dt> <dd>

Indicateurs qui contrôlent cette méthode. Il peut s’agir de l’une des valeurs suivantes.



| Valeur                                                                                                           | Signification                                                                                                                                                                                                                                                                                                                                               |
|-----------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>HTTPREQUEST \_ PROXYSETTING \_ par défaut</dt> </dl>   | Paramètre de proxy par défaut. Équivalent à **la \_ \_ préconfiguration de HTTPREQUEST PROXYSETTING**.<br/>                                                                                                                                                                                                                                                             |
| <dl> <dt>préconfiguration de HTTPREQUEST \_ PROXYSETTING \_</dt> </dl> | Indique que les paramètres de proxy doivent être obtenus à partir du Registre. Cela suppose que [Proxycfg.exe](proxycfg-exe--a-proxy-configuration-tool.md) a été exécutée. Si Proxycfg.exe n’a pas été exécuté et que la **\_ \_ préconfiguration HttpRequest PROXYSETTING** est spécifiée, le comportement est équivalent à **HTTPREQUEST \_ PROXYSETTING \_ direct**.<br/> |
| <dl> <dt>\_PROXYSETTING HTTPREQUEST \_ directe</dt> </dl>    | Indique que tous les serveurs HTTP et HTTPs doivent être accessibles directement. Utilisez cette commande s’il n’y a pas de serveur proxy.<br/>                                                                                                                                                                                                                       |
| <dl> <dt>\_proxy HTTPREQUEST PROXYSETTING \_</dt> </dl>     | Quand **le \_ \_ proxy PROXYSETTING HTTPREQUEST** est spécifié, *varProxyServer* doit être défini sur une chaîne de serveur proxy et *varBypassList* doit être défini sur une chaîne de liste de contournement de domaine. Cette configuration de proxy s’applique uniquement à l’instance actuelle de l’objet [**WinHttpRequest**](winhttprequest.md) .<br/>                                    |



 

</dd> <dt>

*ProxyServer* \[ dans, facultatif\]
</dt> <dd>

Défini sur une chaîne de serveur proxy lorsque *ProxySetting* est égal à **HTTPREQUEST \_ ProxySetting \_ proxy**.

</dd> <dt>

*BypassList* \[ dans, facultatif\]
</dt> <dd>

Défini sur une chaîne de liste de contournement de domaine lorsque *ProxySetting* est égal à **HTTPREQUEST \_ ProxySetting \_ proxy**.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La valeur de retour est **S \_ OK** en cas de réussite ou une valeur d’erreur dans le cas contraire.

## <a name="remarks"></a>Remarques

Permet à l’application appelante de spécifier l’utilisation des informations de proxy par défaut (configurées par l’outil de configuration de proxy) ou de substituer les [Proxycfg.exe](proxycfg-exe--a-proxy-configuration-tool.md). Cette méthode doit être appelée avant d’appeler la méthode [**Send**](iwinhttprequest-send.md) . Si cette méthode est appelée après la méthode [**Send**](iwinhttprequest-send.md) , elle n’a aucun effet.

[**IWinHttpRequest**](iwinhttprequest-interface.md) transmet ces paramètres à Microsoft Windows HTTP Services (WinHTTP).

> [!Note]  
> pour Windows XP et Windows 2000, consultez la section [configuration requise](winhttp-start-page.md) pour l’exécution de la Page de démarrage de WinHTTP.

 

## <a name="examples"></a>Exemples

L’exemple suivant montre comment définir les paramètres de proxy pour un serveur proxy particulier, ouvrir une connexion HTTP, envoyer une requête HTTP et lire le texte de la réponse. Cet exemple doit être exécuté à partir d’une invite de commandes. Ces paramètres de proxy ne fonctionnent que si vous disposez d’un serveur proxy nommé « \_ serveur proxy » qui utilise le port 80 et que votre ordinateur peut contourner le serveur proxy lorsque le nom d’hôte se termine par « . Microsoft.com ».


```C++
#include <windows.h>
#include <stdio.h>
#include <objbase.h>

#include "httprequest.h"

#pragma comment(lib, "ole32.lib")
#pragma comment(lib, "oleaut32.lib")

// IID for IWinHttpRequest.
const IID IID_IWinHttpRequest =
{
  0x06f29373,
  0x5c5a,
  0x4b54,
  {0xb0, 0x25, 0x6e, 0xf1, 0xbf, 0x8a, 0xbf, 0x0e}
};

int main()
{
    // Variable for return value
    HRESULT    hr;

    // Initialize COM
    hr = CoInitialize( NULL );

    IWinHttpRequest *  pIWinHttpRequest = NULL;

    BSTR            bstrResponse = NULL;
    VARIANT         varFalse;
    VARIANT         varEmpty;
    VARIANT         varProxy;
    VARIANT         varUrl;
    
    CLSID           clsid;

    VariantInit(&varFalse);
    V_VT(&varFalse)   = VT_BOOL;
    V_BOOL(&varFalse) = VARIANT_FALSE;

    VariantInit(&varEmpty);
    V_VT(&varEmpty) = VT_ERROR;

    VariantInit(&varProxy);
    VariantInit(&varUrl);

    hr = CLSIDFromProgID(L"WinHttp.WinHttpRequest.5.1", &clsid);

    if (SUCCEEDED(hr))
    {
        hr = CoCreateInstance(clsid, NULL, 
                              CLSCTX_INPROC_SERVER, 
                              IID_IWinHttpRequest, 
                              (void **)&pIWinHttpRequest);
    }
    if (SUCCEEDED(hr))
    {   // Specify proxy and URL.
                varProxy.vt = VT_BSTR;
                varProxy.bstrVal = SysAllocString(L"proxy_server:80");
                varUrl.vt = VT_BSTR;
                varUrl.bstrVal = SysAllocString(L"*.microsoft.com");
                hr = pIWinHttpRequest->SetProxy(HTTPREQUEST_PROXYSETTING_PROXY,
                                    varProxy, varUrl); 
        }
    if (SUCCEEDED(hr))
    {   // Open WinHttpRequest.
            BSTR bstrMethod  = SysAllocString(L"GET");
                BSTR bstrUrl = SysAllocString(L"https://microsoft.com");
        hr = pIWinHttpRequest->Open(bstrMethod, bstrUrl, varFalse);
                SysFreeString(bstrMethod);
                SysFreeString(bstrUrl);
    }
    if (SUCCEEDED(hr))
    {   // Send Request.
        hr = pIWinHttpRequest->Send(varEmpty);
    }
    if (SUCCEEDED(hr))
    {   // Get Response text.
                hr = pIWinHttpRequest->get_ResponseText(&bstrResponse);
    }
    if (SUCCEEDED(hr))
    {   // Print the response to a console.
                wprintf(L"%.256s",bstrResponse);
    }
        
        // Release memory.
    if (pIWinHttpRequest)
        pIWinHttpRequest->Release();
        if (varProxy.bstrVal)
                SysFreeString(varProxy.bstrVal);
        if (varUrl.bstrVal)
                SysFreeString(varUrl.bstrVal);
    if (bstrResponse)
        SysFreeString(bstrResponse);
        
        CoUninitialize();
        return 0;
}
```



L’exemple de script suivant montre comment définir les paramètres de proxy pour un serveur proxy particulier, ouvrir une connexion HTTP, envoyer une requête HTTP et lire le texte de la réponse. Ces paramètres de proxy ne fonctionnent que si vous disposez d’un serveur proxy nommé « \_ serveur proxy » qui utilise le port 80 et que votre ordinateur peut contourner le serveur proxy lorsque le nom d’hôte se termine par « . Microsoft.com ».


```JScript
// HttpRequest SetCredentials flags.
HTTPREQUEST_PROXYSETTING_DEFAULT   = 0;
HTTPREQUEST_PROXYSETTING_PRECONFIG = 0;
HTTPREQUEST_PROXYSETTING_DIRECT    = 1;
HTTPREQUEST_PROXYSETTING_PROXY     = 2;

// Instantiate a WinHttpRequest object.
var WinHttpReq = new ActiveXObject("WinHttp.WinHttpRequest.5.1");

// Use proxy_server for all requests outside of 
// the microsoft.com domain.
WinHttpReq.SetProxy( HTTPREQUEST_PROXYSETTING_PROXY, 
                     "proxy_server:80", 
                     "*.microsoft.com");

// Initialize an HTTP request.  
WinHttpReq.Open("GET", "https://www.microsoft.com", false);

// Send the HTTP request.
WinHttpReq.Send(); 

// Display the response text.
WScript.Echo( WinHttpReq.ResponseText);
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

[Versions de WinHTTP](winhttp-versions.md)
</dt> </dl>

 

 




