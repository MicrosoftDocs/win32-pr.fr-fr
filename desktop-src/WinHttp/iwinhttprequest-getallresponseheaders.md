---
description: Récupère tous les en-têtes de réponse HTTP.
ms.assetid: 68b13d4c-5afd-486d-8b78-a7eef0f59a24
title: 'IWinHttpRequest :: GetAllResponseHeaders, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWinHttpRequest.GetAllResponseHeaders
- WinHttpRequest.GetAllResponseHeaders
api_type:
- COM
api_location:
- Winhttp.dll
ms.openlocfilehash: 74c113216cf41e2f9816176dd28ba5e84208c635
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127228317"
---
# <a name="iwinhttprequestgetallresponseheaders-method"></a>IWinHttpRequest :: GetAllResponseHeaders, méthode

La méthode **GetAllResponseHeaders** récupère tous les en-têtes de réponse http.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetAllResponseHeaders(
  [out, retval] BSTR *Headers
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*En-têtes* \[ out, retval\]
</dt> <dd>

Reçoit les informations d’en-tête obtenues.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

La valeur de retour est **S \_ OK** en cas de réussite ou une valeur d’erreur dans le cas contraire.

## <a name="remarks"></a>Notes

Cette méthode retourne tous les en-têtes contenus dans la dernière réponse du serveur. Les en-têtes individuels sont délimités par une combinaison de retour chariot et de saut de ligne (ASCII 13 et 10). La dernière entrée est suivie de deux délimiteurs (13, 10, 13, 10). Appelez cette méthode uniquement après l’appel de la méthode [**Send**](iwinhttprequest-send.md) .

> [!Note]  
> pour Windows XP et Windows 2000, consultez la section [configuration requise](winhttp-start-page.md) pour l’exécution de la Page de démarrage de WinHTTP.

 

## <a name="examples"></a>Exemples

L’exemple suivant montre comment ouvrir une connexion HTTP, envoyer une requête HTTP et obtenir tous les en-têtes de la réponse. Cet exemple doit être exécuté à partir d’une invite de commandes.


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

int main(int argc, char* argv[])
{
    UNREFERENCED_PARAMETER(argc);
    UNREFERENCED_PARAMETER(argv);

    // Variable for return value
    HRESULT    hr;

    // Initialize COM
    hr = CoInitialize( NULL );

    IWinHttpRequest *  pIWinHttpRequest = NULL;

    BSTR            bstrResponse = NULL;
    VARIANT         varFalse;
    VARIANT         varEmpty;

    CLSID           clsid;

    VariantInit(&varFalse);
    V_VT(&varFalse)   = VT_BOOL;
    V_BOOL(&varFalse) = VARIANT_FALSE;

    VariantInit(&varEmpty);
    V_VT(&varEmpty) = VT_ERROR;

    hr = CLSIDFromProgID(L"WinHttp.WinHttpRequest.5.1", &clsid);

    if (SUCCEEDED(hr))
    {
        hr = CoCreateInstance(clsid, NULL,
                              CLSCTX_INPROC_SERVER,
                              IID_IWinHttpRequest,
                              (void **)&pIWinHttpRequest);
    }
    if (SUCCEEDED(hr))
    {    // Open WinHttpRequest.
        BSTR bstrMethod  = SysAllocString(L"GET");
        BSTR bstrUrl = SysAllocString(L"https://microsoft.com");
        hr = pIWinHttpRequest->Open(bstrMethod, bstrUrl, varFalse);
        SysFreeString(bstrMethod);
        SysFreeString(bstrUrl);
    }
    if (SUCCEEDED(hr))
    {    // Send Request.
        hr = pIWinHttpRequest->Send(varEmpty);
    }
    if (SUCCEEDED(hr))
    {    // Get Response text.
        hr = pIWinHttpRequest->GetAllResponseHeaders(&bstrResponse);
    }
    if (SUCCEEDED(hr))
    {    // Print the response to a console.
        wprintf(L"%.256s",bstrResponse);
    }

    // Release memory.
    if (pIWinHttpRequest)
        pIWinHttpRequest->Release();
    if (bstrResponse)
        SysFreeString(bstrResponse);

    CoUninitialize();
    return 0;
}

```



L’exemple de script suivant montre comment ouvrir une connexion HTTP, envoyer une requête HTTP et obtenir tous les en-têtes de la réponse.


```JScript
// Instantiate a WinHttpRequest object.
var WinHttpReq = new ActiveXObject("WinHttp.WinHttpRequest.5.1");

// Initialize an HTTP request.  
WinHttpReq.Open("GET", "https://www.microsoft.com", false);

// Send the HTTP request.
WinHttpReq.Send(); 

// Get all response headers.
WScript.Echo( WinHttpReq.GetAllResponseHeaders());
```



## <a name="requirements"></a>Spécifications



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

[**GetResponseHeader**](iwinhttprequest-getresponseheader.md)
</dt> <dt>

[Versions de WinHTTP](winhttp-versions.md)
</dt> </dl>

 

 




