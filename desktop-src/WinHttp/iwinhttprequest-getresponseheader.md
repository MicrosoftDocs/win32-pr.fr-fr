---
description: Récupère les en-têtes de réponse HTTP.
ms.assetid: 3d59ee83-280c-4074-82e1-ded203fa1049
title: 'IWinHttpRequest :: GetResponseHeader, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWinHttpRequest.GetResponseHeader
- WinHttpRequest.GetResponseHeader
api_type:
- COM
api_location:
- Winhttp.dll
ms.openlocfilehash: 6e51b0973c7b078c7de592565db19bf6e029c5a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106535542"
---
# <a name="iwinhttprequestgetresponseheader-method"></a><span data-ttu-id="a254b-103">IWinHttpRequest :: GetResponseHeader, méthode</span><span class="sxs-lookup"><span data-stu-id="a254b-103">IWinHttpRequest::GetResponseHeader method</span></span>

<span data-ttu-id="a254b-104">La méthode **getResponseHeader** récupère les en-têtes de réponse http.</span><span class="sxs-lookup"><span data-stu-id="a254b-104">The **GetResponseHeader** method retrieves the HTTP response headers.</span></span>

## <a name="syntax"></a><span data-ttu-id="a254b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a254b-105">Syntax</span></span>


```C++
HRESULT GetResponseHeader(
  [in]          BSTR Header,
  [out, retval] BSTR *Value
);
```



## <a name="parameters"></a><span data-ttu-id="a254b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a254b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a254b-107">*En-tête* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a254b-107">*Header* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a254b-108">Spécifie le nom d’en-tête qui ne respecte pas la casse.</span><span class="sxs-lookup"><span data-stu-id="a254b-108">Specifies the case-insensitive header name.</span></span>

</dd> <dt>

<span data-ttu-id="a254b-109">*Valeur* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="a254b-109">*Value* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="a254b-110">Reçoit les informations d’en-tête obtenues.</span><span class="sxs-lookup"><span data-stu-id="a254b-110">Receives the resulting header information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a254b-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a254b-111">Return value</span></span>

<span data-ttu-id="a254b-112">La valeur de retour est **S \_ OK** en cas de réussite ou une valeur d’erreur dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="a254b-112">The return value is **S\_OK** on success or an error value otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="a254b-113">Notes</span><span class="sxs-lookup"><span data-stu-id="a254b-113">Remarks</span></span>

<span data-ttu-id="a254b-114">Cette méthode retourne la valeur de l’en-tête de réponse nommé dans l' *en-tête*.</span><span class="sxs-lookup"><span data-stu-id="a254b-114">This method returns the value of the response header named in *Header*.</span></span> <span data-ttu-id="a254b-115">N’oubliez pas que les clients Automation, tels que le script, obtiennent les données d’en-tête comme valeur de retour de l’appel de fonction, et non par le biais d’un paramètre de fonction.</span><span class="sxs-lookup"><span data-stu-id="a254b-115">Be aware that automation clients, such as script, get the header data as the return value of the function call, not through a function parameter.</span></span> <span data-ttu-id="a254b-116">Appelez cette méthode uniquement après l’appel de la méthode [**Send**](iwinhttprequest-send.md) .</span><span class="sxs-lookup"><span data-stu-id="a254b-116">Invoke this method only after the [**Send**](iwinhttprequest-send.md) method has been called.</span></span>

> [!Note]  
> <span data-ttu-id="a254b-117">Pour Windows XP et Windows 2000, consultez la section [Configuration requise](winhttp-start-page.md) pour l’exécution de la page de démarrage de WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="a254b-117">For Windows XP and Windows 2000, see the [Run-Time Requirements](winhttp-start-page.md) section of the WinHTTP Start Page.</span></span>

 

## <a name="examples"></a><span data-ttu-id="a254b-118">Exemples</span><span class="sxs-lookup"><span data-stu-id="a254b-118">Examples</span></span>

<span data-ttu-id="a254b-119">L’exemple suivant montre comment ouvrir une connexion HTTP, envoyer une requête HTTP et obtenir l’en-tête de date à partir de la réponse.</span><span class="sxs-lookup"><span data-stu-id="a254b-119">The following example shows how to open an HTTP connection, send an HTTP request, and get the date header from the response.</span></span> <span data-ttu-id="a254b-120">Cet exemple doit être exécuté à partir d’une invite de commandes.</span><span class="sxs-lookup"><span data-stu-id="a254b-120">This example must be run from a command prompt.</span></span>


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

    CLSID           clsid;

    VariantInit(&varFalse);
    V_VT(&varFalse)   = VT_BOOL;
    V_BOOL(&varFalse) = VARIANT_FALSE;

    VariantInit(&varEmpty);
    V_VT(&varEmpty) = VT_ERROR;

    hr = CLSIDFromProgID(L"WinHttp.WinHttpRequest.5.1",
                         &clsid);

    if (SUCCEEDED(hr))
    {
        hr = CoCreateInstance(clsid,
                              NULL,
                              CLSCTX_INPROC_SERVER,
                              IID_IWinHttpRequest,
                              (void **)&pIWinHttpRequest);
    }
    if (SUCCEEDED(hr))
    {
        // Open WinHttpRequest.
        BSTR bstrMethod  = SysAllocString(L"GET");
        BSTR bstrUrl = SysAllocString(L"https://microsoft.com");
        hr = pIWinHttpRequest->Open(bstrMethod,
                                    bstrUrl,
                                    varFalse);
        SysFreeString(bstrMethod);
        SysFreeString(bstrUrl);
    }
    if (SUCCEEDED(hr))
    {
        // Send Request.
        hr = pIWinHttpRequest->Send(varEmpty);
    }
    if (SUCCEEDED(hr))
    {
        // Get Response text.
        BSTR bstrName = SysAllocString(L"Date");
        hr = pIWinHttpRequest->GetResponseHeader(bstrName,
                                             &bstrResponse);
    }
    if (SUCCEEDED(hr))
    {
        // Print response to console.
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



<span data-ttu-id="a254b-121">L’exemple de script suivant montre comment ouvrir une connexion HTTP, envoyer une requête HTTP et obtenir l’en-tête de date à partir de la réponse.</span><span class="sxs-lookup"><span data-stu-id="a254b-121">The following scripting example shows how to open an HTTP connection, send an HTTP request, and get the date header from the response.</span></span>


```JScript
// Instantiate a WinHttpRequest object.
var WinHttpReq = new ActiveXObject("WinHttp.WinHttpRequest.5.1");

// Initialize an HTTP request.  
WinHttpReq.Open("GET", 
                "https://www.microsoft.com", 
                 false);

// Send the HTTP request.
WinHttpReq.Send(); 

// Display the date header.
WScript.Echo( WinHttpReq.GetResponseHeader("Date"));
```



## <a name="requirements"></a><span data-ttu-id="a254b-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a254b-122">Requirements</span></span>



| <span data-ttu-id="a254b-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a254b-123">Requirement</span></span> | <span data-ttu-id="a254b-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="a254b-124">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="a254b-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a254b-125">Minimum supported client</span></span><br/> | <span data-ttu-id="a254b-126">Windows XP, Windows 2000 Professionnel avec les \[ applications de bureau SP3 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a254b-126">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>            |
| <span data-ttu-id="a254b-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a254b-127">Minimum supported server</span></span><br/> | <span data-ttu-id="a254b-128">Windows Server 2003, Windows 2000 Server avec les \[ applications de bureau SP3 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a254b-128">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>         |
| <span data-ttu-id="a254b-129">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="a254b-129">Redistributable</span></span><br/>          | <span data-ttu-id="a254b-130">WinHTTP 5,0 et Internet Explorer 5,01 ou version ultérieure sur Windows XP et Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="a254b-130">WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.</span></span><br/> |
| <span data-ttu-id="a254b-131">MIDL</span><span class="sxs-lookup"><span data-stu-id="a254b-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a254b-132"><dt>HttpRequest. idl</dt></span><span class="sxs-lookup"><span data-stu-id="a254b-132"><dt>HttpRequest.idl</dt></span></span> </dl> |
| <span data-ttu-id="a254b-133">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="a254b-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="a254b-134"><dt>WinHTTP. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a254b-134"><dt>Winhttp.lib</dt></span></span> </dl>     |
| <span data-ttu-id="a254b-135">DLL</span><span class="sxs-lookup"><span data-stu-id="a254b-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a254b-136"><dt>Winhttp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a254b-136"><dt>Winhttp.dll</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="a254b-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a254b-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a254b-138">**IWinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="a254b-138">**IWinHttpRequest**</span></span>](iwinhttprequest-interface.md)
</dt> <dt>

[<span data-ttu-id="a254b-139">**WinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="a254b-139">**WinHttpRequest**</span></span>](winhttprequest.md)
</dt> <dt>

[<span data-ttu-id="a254b-140">**GetAllResponseHeaders**</span><span class="sxs-lookup"><span data-stu-id="a254b-140">**GetAllResponseHeaders**</span></span>](iwinhttprequest-getallresponseheaders.md)
</dt> <dt>

[<span data-ttu-id="a254b-141">Versions de WinHTTP</span><span class="sxs-lookup"><span data-stu-id="a254b-141">WinHTTP Versions</span></span>](winhttp-versions.md)
</dt> </dl>

 

 




