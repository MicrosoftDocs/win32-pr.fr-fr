---
description: La méthode Send envoie une requête HTTP à un serveur HTTP.
ms.assetid: 4f30d6b7-d1c3-43f1-9829-260b7c84518f
title: 'IWinHttpRequest :: Send, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWinHttpRequest.Send
- WinHttpRequest.Send
api_type:
- COM
api_location:
- Winhttp.dll
ms.openlocfilehash: 0040ed6c09814a2b2112a91173d84430b8130a30
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103758331"
---
# <a name="iwinhttprequestsend-method"></a><span data-ttu-id="7f938-103">IWinHttpRequest :: Send, méthode</span><span class="sxs-lookup"><span data-stu-id="7f938-103">IWinHttpRequest::Send method</span></span>

<span data-ttu-id="7f938-104">La méthode **Send** envoie une requête HTTP à un serveur http.</span><span class="sxs-lookup"><span data-stu-id="7f938-104">The **Send** method sends an HTTP request to an HTTP server.</span></span>

## <a name="syntax"></a><span data-ttu-id="7f938-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7f938-105">Syntax</span></span>


```C++
HRESULT Send(
  [in, optional] VARIANT Body
);
```



## <a name="parameters"></a><span data-ttu-id="7f938-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7f938-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7f938-107">*Corps du message* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="7f938-107">*Body* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="7f938-108">Données à envoyer au serveur.</span><span class="sxs-lookup"><span data-stu-id="7f938-108">Data to be sent to the server.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7f938-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7f938-109">Return value</span></span>

<span data-ttu-id="7f938-110">La valeur de retour est **S \_ OK** en cas de réussite ou une valeur d’erreur dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="7f938-110">The return value is **S\_OK** on success or an error value otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="7f938-111">Notes</span><span class="sxs-lookup"><span data-stu-id="7f938-111">Remarks</span></span>

<span data-ttu-id="7f938-112">La demande à envoyer a été définie dans un appel antérieur à la méthode [**Open**](iwinhttprequest-open.md) .</span><span class="sxs-lookup"><span data-stu-id="7f938-112">The request to be sent was defined in a prior call to the [**Open**](iwinhttprequest-open.md) method.</span></span> <span data-ttu-id="7f938-113">L’application appelante peut fournir des données à envoyer au serveur par le biais du paramètre *Body* .</span><span class="sxs-lookup"><span data-stu-id="7f938-113">The calling application can provide data to be sent to the server through the *Body* parameter.</span></span> <span data-ttu-id="7f938-114">Si le [*verbe http*](glossary.md) de l' [**ouverture**](iwinhttprequest-open.md) de l’objet est « obtenir », cette méthode envoie la demande sans *corps*, même si elle est fournie par l’application appelante.</span><span class="sxs-lookup"><span data-stu-id="7f938-114">If the [*HTTP verb*](glossary.md) of the object's [**Open**](iwinhttprequest-open.md) is "GET", this method sends the request without *Body*, even if it is provided by the calling application.</span></span>

> [!Note]  
> <span data-ttu-id="7f938-115">Pour Windows XP et Windows 2000, consultez la section [Configuration requise](winhttp-start-page.md) pour l’exécution de la page de démarrage de WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="7f938-115">For Windows XP and Windows 2000, see the [Run-Time Requirements](winhttp-start-page.md) section of the WinHttp start page.</span></span>

 

## <a name="examples"></a><span data-ttu-id="7f938-116">Exemples</span><span class="sxs-lookup"><span data-stu-id="7f938-116">Examples</span></span>

<span data-ttu-id="7f938-117">L’exemple suivant montre comment ouvrir une connexion HTTP, envoyer une requête HTTP et lire le texte de la réponse.</span><span class="sxs-lookup"><span data-stu-id="7f938-117">The following example shows how to open an HTTP connection, send an HTTP request, and read the response text.</span></span>


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
        hr = pIWinHttpRequest->get_ResponseText(&bstrResponse);
    }

    // Print response to console.
    wprintf(L"%.256s",bstrResponse);

    // Release memory.
    if (pIWinHttpRequest)
        pIWinHttpRequest->Release();
    if (bstrResponse)
        SysFreeString(bstrResponse);

    CoUninitialize();
    return 0;
}

```



<span data-ttu-id="7f938-118">L’exemple de script suivant montre comment ouvrir une connexion HTTP, envoyer une requête HTTP et lire le texte de la réponse.</span><span class="sxs-lookup"><span data-stu-id="7f938-118">The following scripting example shows how to open an HTTP connection, send an HTTP request, and read the response text.</span></span>


```JScript
// Instantiate a WinHttpRequest object.
var WinHttpReq = new ActiveXObject("WinHttp.WinHttpRequest.5.1");

// Initialize an HTTP request.  
WinHttpReq.Open("GET", "https://www.microsoft.com", false);

// Send the HTTP request.
WinHttpReq.Send(); 

// Display the response text.
WScript.Echo( WinHttpReq.ResponseText);
```



<span data-ttu-id="7f938-119">L’exemple de script suivant montre comment envoyer des données vers un serveur HTTP.</span><span class="sxs-lookup"><span data-stu-id="7f938-119">The following scripting example shows how to post data to an HTTP server.</span></span>


```JScript
// Instantiate a WinHttpRequest object.
var WinHttpReq = new ActiveXObject("WinHttp.WinHttpRequest.5.1");

// Initialize an HTTP request.  
WinHttpReq.Open("PUT", "https://postserver/newdoc.htm", false);

// Post data to the HTTP server.
WinHttpReq.Send("Post data");
```



## <a name="requirements"></a><span data-ttu-id="7f938-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7f938-120">Requirements</span></span>



| <span data-ttu-id="7f938-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7f938-121">Requirement</span></span> | <span data-ttu-id="7f938-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="7f938-122">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="7f938-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7f938-123">Minimum supported client</span></span><br/> | <span data-ttu-id="7f938-124">Windows XP, Windows 2000 Professionnel avec les \[ applications de bureau SP3 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7f938-124">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>            |
| <span data-ttu-id="7f938-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7f938-125">Minimum supported server</span></span><br/> | <span data-ttu-id="7f938-126">Windows Server 2003, Windows 2000 Server avec les \[ applications de bureau SP3 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7f938-126">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>         |
| <span data-ttu-id="7f938-127">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="7f938-127">Redistributable</span></span><br/>          | <span data-ttu-id="7f938-128">WinHTTP 5,0 et Internet Explorer 5,01 ou version ultérieure sur Windows XP et Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="7f938-128">WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.</span></span><br/> |
| <span data-ttu-id="7f938-129">MIDL</span><span class="sxs-lookup"><span data-stu-id="7f938-129">IDL</span></span><br/>                      | <dl> <span data-ttu-id="7f938-130"><dt>HttpRequest. idl</dt></span><span class="sxs-lookup"><span data-stu-id="7f938-130"><dt>HttpRequest.idl</dt></span></span> </dl> |
| <span data-ttu-id="7f938-131">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="7f938-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="7f938-132"><dt>WinHTTP. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7f938-132"><dt>Winhttp.lib</dt></span></span> </dl>     |
| <span data-ttu-id="7f938-133">DLL</span><span class="sxs-lookup"><span data-stu-id="7f938-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7f938-134"><dt>Winhttp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7f938-134"><dt>Winhttp.dll</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="7f938-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7f938-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f938-136">**IWinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="7f938-136">**IWinHttpRequest**</span></span>](iwinhttprequest-interface.md)
</dt> <dt>

[<span data-ttu-id="7f938-137">**WinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="7f938-137">**WinHttpRequest**</span></span>](winhttprequest.md)
</dt> <dt>

[<span data-ttu-id="7f938-138">Versions de WinHTTP</span><span class="sxs-lookup"><span data-stu-id="7f938-138">WinHTTP Versions</span></span>](winhttp-versions.md)
</dt> </dl>

 

 




