---
description: Récupère le texte d’état HTTP.
ms.assetid: 480babbd-432c-4722-98df-a73ba5928e1f
title: 'IWinHttpRequest :: StatusText, propriété'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWinHttpRequest.StatusText
- IWinHttpRequest.get_StatusText
- WinHttpRequest.StatusText
api_type:
- COM
api_location:
- Winhttp.dll
ms.openlocfilehash: 41288d87b8194caf3a2a14cc89cd5acbffec902c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042843"
---
# <a name="iwinhttprequeststatustext-property"></a><span data-ttu-id="a30bc-103">IWinHttpRequest :: StatusText, propriété</span><span class="sxs-lookup"><span data-stu-id="a30bc-103">IWinHttpRequest::StatusText property</span></span>

<span data-ttu-id="a30bc-104">La propriété **StatusText** récupère le texte d’État http.</span><span class="sxs-lookup"><span data-stu-id="a30bc-104">The **StatusText** property retrieves the HTTP status text.</span></span>

<span data-ttu-id="a30bc-105">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="a30bc-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="a30bc-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a30bc-106">Syntax</span></span>


```C++
HRESULT get_StatusText(
  [out, retval] BSTR *Status
);
```


```JScript

StatusText = WinHttpRequest.StatusText
```





## <a name="property-value"></a><span data-ttu-id="a30bc-107">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="a30bc-107">Property value</span></span>

<span data-ttu-id="a30bc-108">**BSTR** qui reçoit le texte d’État http.</span><span class="sxs-lookup"><span data-stu-id="a30bc-108">**BSTR** that receives the HTTP status text.</span></span>

## <a name="error-codes"></a><span data-ttu-id="a30bc-109">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="a30bc-109">Error codes</span></span>

<span data-ttu-id="a30bc-110">La valeur de retour est **S \_ OK** en cas de réussite ou une valeur d’erreur dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="a30bc-110">The return value is **S\_OK** on success or an error value otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="a30bc-111">Notes</span><span class="sxs-lookup"><span data-stu-id="a30bc-111">Remarks</span></span>

<span data-ttu-id="a30bc-112">Récupère la partie de texte de la ligne de réponse du serveur, ce qui rend disponible l’équivalent « convivial » du code d’état HTTP numérique.</span><span class="sxs-lookup"><span data-stu-id="a30bc-112">Retrieves the text portion of the server response line, making available the "user-friendly" equivalent to the numeric HTTP status code.</span></span> <span data-ttu-id="a30bc-113">Les résultats de cette propriété ne sont valides qu’une fois que la méthode [**Send**](iwinhttprequest-send.md) s’est terminée avec succès.</span><span class="sxs-lookup"><span data-stu-id="a30bc-113">The results of this property are valid only after the [**Send**](iwinhttprequest-send.md) method has successfully completed.</span></span>

> [!Note]  
> <span data-ttu-id="a30bc-114">Pour Windows XP et Windows 2000, consultez la section [Configuration requise](winhttp-start-page.md) pour l’exécution de la page de démarrage de WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="a30bc-114">For Windows XP and Windows 2000, see the [Run-Time Requirements](winhttp-start-page.md) section of the WinHTTP Start Page.</span></span>

 

## <a name="examples"></a><span data-ttu-id="a30bc-115">Exemples</span><span class="sxs-lookup"><span data-stu-id="a30bc-115">Examples</span></span>

<span data-ttu-id="a30bc-116">L’exemple suivant montre comment ouvrir une connexion HTTP, envoyer une requête HTTP, afficher l' [**État**](iwinhttprequest-status.md) et **StatusText**, et lire le texte de la réponse.</span><span class="sxs-lookup"><span data-stu-id="a30bc-116">The following example shows how to open an HTTP connection, send an HTTP request, display the [**Status**](iwinhttprequest-status.md) and **StatusText**, and read the response text.</span></span> <span data-ttu-id="a30bc-117">Cet exemple doit être exécuté à partir d’une invite de commandes.</span><span class="sxs-lookup"><span data-stu-id="a30bc-117">This example must be run from a command prompt.</span></span>


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
    LONG            lStatus = 0;
    BSTR            bstrStatusText = NULL;

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
    {    // Send Request.
        hr = pIWinHttpRequest->get_Status(&lStatus);
        hr = pIWinHttpRequest->get_StatusText(&bstrStatusText);
    }
    if (SUCCEEDED(hr))
    {    // Get Response text.
        hr = pIWinHttpRequest->GetAllResponseHeaders(&bstrResponse);
    }
    if (SUCCEEDED(hr))
    {    // Print response to console.
        wprintf(L"%s\n\n", bstrResponse);
        wprintf(L"%u - %s\n\n", lStatus, bstrStatusText);
    }

    // Release memory.
    if (pIWinHttpRequest)
        pIWinHttpRequest->Release();
    if (bstrStatusText)
        SysFreeString(bstrStatusText);
    if (bstrResponse)
        SysFreeString(bstrResponse);

    CoUninitialize();
    return 0;
}

```



<span data-ttu-id="a30bc-118">L’exemple de script suivant montre comment ouvrir une connexion HTTP, envoyer une requête HTTP, afficher l' [**État**](iwinhttprequest-status.md) et **StatusText**, et lire les en-têtes de réponse.</span><span class="sxs-lookup"><span data-stu-id="a30bc-118">The following scripting example shows how to open an HTTP connection, send an HTTP request, display the [**Status**](iwinhttprequest-status.md) and **StatusText**, and read the response headers.</span></span>


```JScript
// Instantiate a WinHttpRequest object.
var WinHttpReq = new ActiveXObject("WinHttp.WinHttpRequest.5.1");

// Initialize an HTTP request.  
WinHttpReq.Open("GET", "https://www.microsoft.com", false);

// Send the HTTP request.
WinHttpReq.Send(); 

// Display the status.
WScript.Echo( WinHttpReq.Status + " - " + WinHttpReq.StatusText);

// Display the date header.
WScript.Echo( WinHttpReq.GetAllResponseHeaders());
```



## <a name="requirements"></a><span data-ttu-id="a30bc-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a30bc-119">Requirements</span></span>



| <span data-ttu-id="a30bc-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a30bc-120">Requirement</span></span> | <span data-ttu-id="a30bc-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="a30bc-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="a30bc-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a30bc-122">Minimum supported client</span></span><br/> | <span data-ttu-id="a30bc-123">Windows XP, Windows 2000 Professionnel avec les \[ applications de bureau SP3 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a30bc-123">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>            |
| <span data-ttu-id="a30bc-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a30bc-124">Minimum supported server</span></span><br/> | <span data-ttu-id="a30bc-125">Windows Server 2003, Windows 2000 Server avec les \[ applications de bureau SP3 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a30bc-125">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>         |
| <span data-ttu-id="a30bc-126">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="a30bc-126">Redistributable</span></span><br/>          | <span data-ttu-id="a30bc-127">WinHTTP 5,0 et Internet Explorer 5,01 ou version ultérieure sur Windows XP et Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="a30bc-127">WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.</span></span><br/> |
| <span data-ttu-id="a30bc-128">MIDL</span><span class="sxs-lookup"><span data-stu-id="a30bc-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a30bc-129"><dt>HttpRequest. idl</dt></span><span class="sxs-lookup"><span data-stu-id="a30bc-129"><dt>HttpRequest.idl</dt></span></span> </dl> |
| <span data-ttu-id="a30bc-130">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="a30bc-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="a30bc-131"><dt>WinHTTP. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a30bc-131"><dt>Winhttp.lib</dt></span></span> </dl>     |
| <span data-ttu-id="a30bc-132">DLL</span><span class="sxs-lookup"><span data-stu-id="a30bc-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a30bc-133"><dt>Winhttp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a30bc-133"><dt>Winhttp.dll</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="a30bc-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a30bc-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a30bc-135">**IWinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="a30bc-135">**IWinHttpRequest**</span></span>](iwinhttprequest-interface.md)
</dt> <dt>

[<span data-ttu-id="a30bc-136">**WinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="a30bc-136">**WinHttpRequest**</span></span>](winhttprequest.md)
</dt> <dt>

[<span data-ttu-id="a30bc-137">**Statu**</span><span class="sxs-lookup"><span data-stu-id="a30bc-137">**Status**</span></span>](iwinhttprequest-status.md)
</dt> <dt>

[<span data-ttu-id="a30bc-138">Versions de WinHTTP</span><span class="sxs-lookup"><span data-stu-id="a30bc-138">WinHTTP Versions</span></span>](winhttp-versions.md)
</dt> </dl>

 

 




