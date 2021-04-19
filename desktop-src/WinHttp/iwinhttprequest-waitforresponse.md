---
description: La méthode WaitForResponse attend la fin d’une méthode d’envoi asynchrone, avec une valeur de délai d’attente facultative, en secondes.
ms.assetid: 33265710-ecdc-4eae-8822-161dffbd03fc
title: 'IWinHttpRequest :: WaitForResponse, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWinHttpRequest.WaitForResponse
- WinHttpRequest.WaitForResponse
api_type:
- COM
api_location:
- Winhttp.dll
ms.openlocfilehash: fe9e3508273a3ee52d72ede65fd6575d72decb8f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106545060"
---
# <a name="iwinhttprequestwaitforresponse-method"></a>IWinHttpRequest :: WaitForResponse, méthode

La méthode **WaitForResponse** attend la fin d’une méthode d' [**envoi**](iwinhttprequest-send.md) asynchrone, avec une valeur de délai d’attente facultative, en secondes.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT WaitForResponse(
  [in, optional] VARIANT      Timeout,
  [out, retval]  VARIANT_BOOL *Succeeded
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Délai d’expiration* \[ dans, facultatif\]
</dt> <dd>

Valeur du délai d’attente, en secondes. Le délai d’attente par défaut est infini. Pour définir explicitement le délai d’attente sur Infinite, utilisez la valeur-1.

</dd> <dt>

Opération *réussie* \[ out, retval\]
</dt> <dd>

Reçoit l’une des valeurs suivantes.



| Valeur                                                                                                                                                         | Signification                                                |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <span id="VARIANT_TRUE"></span><span id="variant_true"></span><dl> <dt>**VARIANTE \_ true**</dt> </dl>    | Une réponse a été reçue.<br/>               |
| <span id="VARIANT_FALSE"></span><span id="variant_false"></span><dl> <dt>**VARIANTE \_ false**</dt> </dl> | Le délai d’attente spécifié a été dépassé.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La valeur de retour est **S \_ OK** en cas de réussite ou une valeur d’erreur dans le cas contraire.

## <a name="remarks"></a>Notes

Cette méthode interrompt l’exécution en attendant une réponse à une requête asynchrone. Cette méthode doit être appelée après un [**envoi**](iwinhttprequest-send.md). L’appel d’applications peut spécifier une valeur de *délai d’attente* facultative, en secondes. Si cette méthode expire, la demande n’est pas abandonnée. De cette façon, l’application appelante peut continuer à attendre la demande, le cas échéant, dans un appel ultérieur à cette méthode.

L’appel de cette propriété après une méthode d' [**envoi**](iwinhttprequest-send.md) synchrone retourne immédiatement et n’a aucun effet.

> [!Note]  
> Pour Windows XP et Windows 2000, consultez la section [Configuration requise](winhttp-start-page.md) pour l’exécution de la page de démarrage de WinHTTP.

 

## <a name="examples"></a>Exemples

L’exemple suivant montre comment ouvrir une connexion HTTP asynchrone, envoyer une requête HTTP, attendre la réponse et lire le texte de la réponse.


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

    // Initialize COM.
    hr = CoInitialize( NULL );

    IWinHttpRequest *  pIWinHttpRequest = NULL;

    BSTR            bstrResponse = NULL;
    VARIANT         varTrue;
    VARIANT         varEmpty;

    CLSID           clsid;

    VariantInit(&varTrue);
    V_VT(&varTrue)   = VT_BOOL;
    V_BOOL(&varTrue) = VARIANT_TRUE;

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
        hr = pIWinHttpRequest->Open(bstrMethod, bstrUrl, varTrue);
        SysFreeString(bstrMethod);
        SysFreeString(bstrUrl);
    }
    if (SUCCEEDED(hr))
    {    // Send Request.
        hr = pIWinHttpRequest->Send(varEmpty);
    }
    if (SUCCEEDED(hr))
    {    // Wait for response.
        VARIANT_BOOL varResult;
        hr = pIWinHttpRequest->WaitForResponse(varEmpty, &varResult);
    }
    if (SUCCEEDED(hr))
    {    // Get Response text.
        hr = pIWinHttpRequest->get_ResponseText(&bstrResponse);
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



L’exemple de script suivant montre comment ouvrir une connexion HTTP asynchrone, envoyer une requête HTTP, attendre une réponse et lire le texte de la réponse.


```JScript
// Instantiate a WinHttpRequest object.
var WinHttpReq = new ActiveXObject("WinHttp.WinHttpRequest.5.1");

// Initialize an HTTP request.  
WinHttpReq.Open("GET", "https://www.microsoft.com", true);

// Send the HTTP request.
WinHttpReq.Send(); 

// Wait for the response.
WinHttpReq.WaitForResponse();

// Display the response text.
WScript.Echo( WinHttpReq.ResponseText);
```



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

[**IWinHttpRequest**](iwinhttprequest-interface.md)
</dt> <dt>

[**WinHttpRequest**](winhttprequest.md)
</dt> <dt>

[**Afficher**](iwinhttprequest-open.md)
</dt> <dt>

[Versions de WinHTTP](winhttp-versions.md)
</dt> </dl>

 

 




