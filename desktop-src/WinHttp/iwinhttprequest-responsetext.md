---
description: Récupère le corps d’entité de réponse sous forme de texte.
ms.assetid: 87caf64f-be11-45c9-af1e-997a55c5e76e
title: 'IWinHttpRequest :: ResponseText, propriété'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWinHttpRequest.ResponseText
- IWinHttpRequest.get_ResponseText
- WinHttpRequest.ResponseText
api_type:
- COM
api_location:
- Winhttp.dll
ms.openlocfilehash: 93e0a9b17ba356f9ce6b038be114f5f2c9804eab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106522137"
---
# <a name="iwinhttprequestresponsetext-property"></a><span data-ttu-id="8b956-103">IWinHttpRequest :: ResponseText, propriété</span><span class="sxs-lookup"><span data-stu-id="8b956-103">IWinHttpRequest::ResponseText property</span></span>

<span data-ttu-id="8b956-104">La propriété **responseText** récupère le corps d’entité de réponse sous forme de texte.</span><span class="sxs-lookup"><span data-stu-id="8b956-104">The **ResponseText** property retrieves the response entity body as text.</span></span>

<span data-ttu-id="8b956-105">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="8b956-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="8b956-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8b956-106">Syntax</span></span>


```C++
HRESULT get_ResponseText(
  [out, retval] BSTR *Body
);
```


```JScript

strResponseText = WinHttpRequest.ResponseText
```





## <a name="property-value"></a><span data-ttu-id="8b956-107">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="8b956-107">Property value</span></span>

<span data-ttu-id="8b956-108">**BSTR** qui reçoit le corps d’entité de la réponse sous forme de texte.</span><span class="sxs-lookup"><span data-stu-id="8b956-108">**BSTR** that receives the entity body of the response as text.</span></span>

## <a name="error-codes"></a><span data-ttu-id="8b956-109">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="8b956-109">Error codes</span></span>

<span data-ttu-id="8b956-110">La valeur de retour est **S \_ OK** en cas de réussite ou une valeur d’erreur dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="8b956-110">The return value is **S\_OK** on success or an error value otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="8b956-111">Notes</span><span class="sxs-lookup"><span data-stu-id="8b956-111">Remarks</span></span>

<span data-ttu-id="8b956-112">Cette propriété ne peut être appelée qu’une fois que la méthode [**Send**](iwinhttprequest-send.md) a été appelée.</span><span class="sxs-lookup"><span data-stu-id="8b956-112">This property can only be invoked after the [**Send**](iwinhttprequest-send.md) method has been called.</span></span>

<span data-ttu-id="8b956-113">Lors de l’utilisation de cette propriété en mode synchrone, la limite du nombre de caractères renvoyés est d’environ 2 169 895.</span><span class="sxs-lookup"><span data-stu-id="8b956-113">When using this property in synchronous mode, the limit to the number of characters it returns is approximately 2,169,895.</span></span>

> [!Note]  
> <span data-ttu-id="8b956-114">Pour Windows XP et Windows 2000, consultez la section [Configuration requise](winhttp-start-page.md) pour l’exécution de la page de démarrage de WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="8b956-114">For Windows XP and Windows 2000, see the [Run-Time Requirements](winhttp-start-page.md) section of the WinHTTP Start Page.</span></span>

 

## <a name="examples"></a><span data-ttu-id="8b956-115">Exemples</span><span class="sxs-lookup"><span data-stu-id="8b956-115">Examples</span></span>

<span data-ttu-id="8b956-116">L’exemple suivant montre comment ouvrir une connexion HTTP, envoyer une requête HTTP et lire le texte de la réponse.</span><span class="sxs-lookup"><span data-stu-id="8b956-116">The following example shows how to open an HTTP connection, send an HTTP request, and read the response text.</span></span> <span data-ttu-id="8b956-117">Cet exemple doit être exécuté à partir d’une invite de commandes.</span><span class="sxs-lookup"><span data-stu-id="8b956-117">This example must be run from a command prompt.</span></span>


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

    // Print the response to a console.
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



<span data-ttu-id="8b956-118">L’exemple de script suivant montre comment ouvrir une connexion HTTP, envoyer une requête HTTP et lire le texte de la réponse.</span><span class="sxs-lookup"><span data-stu-id="8b956-118">The following scripting example shows how to open an HTTP connection, send an HTTP request, and read the response text.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="8b956-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8b956-119">Requirements</span></span>



| <span data-ttu-id="8b956-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8b956-120">Requirement</span></span> | <span data-ttu-id="8b956-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="8b956-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="8b956-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8b956-122">Minimum supported client</span></span><br/> | <span data-ttu-id="8b956-123">Windows XP, Windows 2000 Professionnel avec les \[ applications de bureau SP3 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8b956-123">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>            |
| <span data-ttu-id="8b956-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8b956-124">Minimum supported server</span></span><br/> | <span data-ttu-id="8b956-125">Windows Server 2003, Windows 2000 Server avec les \[ applications de bureau SP3 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8b956-125">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>         |
| <span data-ttu-id="8b956-126">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="8b956-126">Redistributable</span></span><br/>          | <span data-ttu-id="8b956-127">WinHTTP 5,0 et Internet Explorer 5,01 ou version ultérieure sur Windows XP et Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="8b956-127">WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.</span></span><br/> |
| <span data-ttu-id="8b956-128">MIDL</span><span class="sxs-lookup"><span data-stu-id="8b956-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="8b956-129"><dt>HttpRequest. idl</dt></span><span class="sxs-lookup"><span data-stu-id="8b956-129"><dt>HttpRequest.idl</dt></span></span> </dl> |
| <span data-ttu-id="8b956-130">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="8b956-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="8b956-131"><dt>WinHTTP. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8b956-131"><dt>Winhttp.lib</dt></span></span> </dl>     |
| <span data-ttu-id="8b956-132">DLL</span><span class="sxs-lookup"><span data-stu-id="8b956-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8b956-133"><dt>Winhttp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8b956-133"><dt>Winhttp.dll</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="8b956-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8b956-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b956-135">**IWinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="8b956-135">**IWinHttpRequest**</span></span>](iwinhttprequest-interface.md)
</dt> <dt>

[<span data-ttu-id="8b956-136">**WinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="8b956-136">**WinHttpRequest**</span></span>](winhttprequest.md)
</dt> <dt>

[<span data-ttu-id="8b956-137">**ResponseBody**</span><span class="sxs-lookup"><span data-stu-id="8b956-137">**ResponseBody**</span></span>](iwinhttprequest-responsebody.md)
</dt> <dt>

[<span data-ttu-id="8b956-138">**ResponseStream**</span><span class="sxs-lookup"><span data-stu-id="8b956-138">**ResponseStream**</span></span>](iwinhttprequest-responsestream.md)
</dt> <dt>

[<span data-ttu-id="8b956-139">Versions de WinHTTP</span><span class="sxs-lookup"><span data-stu-id="8b956-139">WinHTTP Versions</span></span>](winhttp-versions.md)
</dt> </dl>

 

 




