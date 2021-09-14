---
description: La méthode SetTimeouts spécifie les différents composants de délai d’attente d’une opération d’envoi/réception, en millisecondes.
ms.assetid: c2b6c432-5f3b-4361-8026-1b843c6697ae
title: 'IWinHttpRequest :: SetTimeouts, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWinHttpRequest.SetTimeouts
- WinHttpRequest.SetTimeouts
api_type:
- COM
api_location:
- Winhttp.dll
ms.openlocfilehash: 3f2f81585fdf444b6b5ab1795f183897687732ed
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127414530"
---
# <a name="iwinhttprequestsettimeouts-method"></a>IWinHttpRequest :: SetTimeouts, méthode

La méthode **SetTimeouts** spécifie les différents composants de délai d’attente d’une opération d’envoi/réception, en millisecondes.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetTimeouts(
  [in] long ResolveTimeout,
  [in] long ConnectTimeout,
  [in] long SendTimeout,
  [in] long ReceiveTimeout
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ResolveTimeout* \[ dans\]
</dt> <dd>

Valeur de délai d’attente appliquée lors de la résolution d’un nom d’hôte (tel que `www.microsoft.com` ) en adresse IP (par exemple, 192.168.131.199), en millisecondes. La valeur par défaut est zéro, ce qui signifie qu’il n’y a pas de délai d’attente (infini). Si le délai d’expiration DNS est spécifié à l’aide du \_ \_ délai de résolution de noms, il existe une surcharge d’un thread par demande.

</dd> <dt>

*ConnectTimeout* \[ dans\]
</dt> <dd>

Valeur de délai d’attente appliquée lors de l’établissement d’un socket de communication avec le serveur cible, en millisecondes. La valeur par défaut est 60,000 (60 secondes).

</dd> <dt>

*SendTimeout* \[ dans\]
</dt> <dd>

Valeur de délai d’attente appliquée lors de l’envoi d’un paquet individuel de données de demande sur le socket de communication vers le serveur cible, en millisecondes. Une demande volumineuse envoyée à un serveur HTTP est normalement divisée en plusieurs paquets ; le délai d’attente d’envoi s’applique à l’envoi individuel de chaque paquet. La valeur par défaut est 30 000 (30 secondes).

</dd> <dt>

*ReceiveTimeout* \[ dans\]
</dt> <dd>

Valeur de délai d’attente appliquée lors de la réception d’un paquet de données de réponse du serveur cible, en millisecondes. Les réponses volumineuses sont divisées en plusieurs paquets ; le délai d’attente de réception s’applique à la récupération de chaque paquet de données à partir du Socket. La valeur par défaut est 30 000 (30 secondes).

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

La valeur de retour est **S \_ OK** en cas de réussite ou une valeur d’erreur dans le cas contraire.

## <a name="remarks"></a>Notes

Tous les paramètres sont obligatoires. La valeur 0 ou-1 définit un délai d’attente à attendre de façon infinie. Une valeur supérieure à 0 définit la valeur du délai d’attente en millisecondes. Par exemple, 30 000 définit le délai d’expiration sur 30 secondes. Toutes les valeurs négatives autres que-1 provoquent l’échec de cette méthode.

Les valeurs de délai d’attente sont appliquées au niveau de la couche Winsock.

> [!Note]  
> pour Windows XP et Windows 2000, consultez la section [configuration requise](winhttp-start-page.md) pour l’exécution de la page de démarrage de WinHttp.

 

## <a name="examples"></a>Exemples

L’exemple suivant montre comment définir tous les délais d’expiration WinHTTP sur 30 secondes, ouvrir une connexion HTTP, envoyer une requête HTTP et lire le texte de la réponse.


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
    // variable for return value
    HRESULT    hr;

    // initialize COM
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
    {    // Set Time-outs.
        hr = pIWinHttpRequest->SetTimeouts(30000, 30000,
                                           30000, 30000);
    }
    if (SUCCEEDED(hr))
    {    // Open WinHttpRequest.
        BSTR bstrMethod  = SysAllocString(L"GET");
        BSTR bstrUrl = SysAllocString(L"https://microsoft.com");
        hr = pIWinHttpRequest->Open(bstrMethod,
                                    bstrUrl,
                                    varFalse);
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
    {    // Print response to console.
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



L’exemple de script suivant montre comment définir tous les délais d’expiration WinHTTP sur 30 secondes, ouvrir une connexion HTTP et envoyer une requête HTTP.


```JScript
// Instantiate a WinHttpRequest object.
var WinHttpReq = new ActiveXObject("WinHttp.WinHttpRequest.5.1");

// Set time-outs. If time-outs are set, they must 
// be set before open.
WinHttpReq.SetTimeouts(30000, 30000, 30000, 30000);

// Initialize an HTTP request.  
WinHttpReq.Open("GET", "https://www.microsoft.com", false);

// Send the HTTP request.
WinHttpReq.Send();
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

[Versions de WinHTTP](winhttp-versions.md)
</dt> </dl>

 

 




