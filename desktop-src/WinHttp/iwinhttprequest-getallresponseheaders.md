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
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106528305"
---
# <a name="iwinhttprequestgetallresponseheaders-method"></a><span data-ttu-id="09316-103">IWinHttpRequest :: GetAllResponseHeaders, méthode</span><span class="sxs-lookup"><span data-stu-id="09316-103">IWinHttpRequest::GetAllResponseHeaders method</span></span>

<span data-ttu-id="09316-104">La méthode **GetAllResponseHeaders** récupère tous les en-têtes de réponse http.</span><span class="sxs-lookup"><span data-stu-id="09316-104">The **GetAllResponseHeaders** method retrieves all HTTP response headers.</span></span>

## <a name="syntax"></a><span data-ttu-id="09316-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="09316-105">Syntax</span></span>


```C++
HRESULT GetAllResponseHeaders(
  [out, retval] BSTR *Headers
);
```



## <a name="parameters"></a><span data-ttu-id="09316-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="09316-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="09316-107">*En-têtes* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="09316-107">*Headers* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="09316-108">Reçoit les informations d’en-tête obtenues.</span><span class="sxs-lookup"><span data-stu-id="09316-108">Receives the resulting header information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="09316-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="09316-109">Return value</span></span>

<span data-ttu-id="09316-110">La valeur de retour est **S \_ OK** en cas de réussite ou une valeur d’erreur dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="09316-110">The return value is **S\_OK** on success or an error value otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="09316-111">Notes</span><span class="sxs-lookup"><span data-stu-id="09316-111">Remarks</span></span>

<span data-ttu-id="09316-112">Cette méthode retourne tous les en-têtes contenus dans la dernière réponse du serveur.</span><span class="sxs-lookup"><span data-stu-id="09316-112">This method returns all of the headers contained in the most recent server response.</span></span> <span data-ttu-id="09316-113">Les en-têtes individuels sont délimités par une combinaison de retour chariot et de saut de ligne (ASCII 13 et 10).</span><span class="sxs-lookup"><span data-stu-id="09316-113">The individual headers are delimited by a carriage return and line feed combination (ASCII 13 and 10).</span></span> <span data-ttu-id="09316-114">La dernière entrée est suivie de deux délimiteurs (13, 10, 13, 10).</span><span class="sxs-lookup"><span data-stu-id="09316-114">The last entry is followed by two delimiters (13, 10, 13, 10).</span></span> <span data-ttu-id="09316-115">Appelez cette méthode uniquement après l’appel de la méthode [**Send**](iwinhttprequest-send.md) .</span><span class="sxs-lookup"><span data-stu-id="09316-115">Invoke this method only after the [**Send**](iwinhttprequest-send.md) method has been called.</span></span>

> [!Note]  
> <span data-ttu-id="09316-116">Pour Windows XP et Windows 2000, consultez la section [Configuration requise](winhttp-start-page.md) pour l’exécution de la page de démarrage de WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="09316-116">For Windows XP and Windows 2000, see the [Run-Time Requirements](winhttp-start-page.md) section of the WinHTTP Start Page.</span></span>

 

## <a name="examples"></a><span data-ttu-id="09316-117">Exemples</span><span class="sxs-lookup"><span data-stu-id="09316-117">Examples</span></span>

<span data-ttu-id="09316-118">L’exemple suivant montre comment ouvrir une connexion HTTP, envoyer une requête HTTP et obtenir tous les en-têtes de la réponse.</span><span class="sxs-lookup"><span data-stu-id="09316-118">The following example shows how to open an HTTP connection, send an HTTP request, and get all of the headers from the response.</span></span> <span data-ttu-id="09316-119">Cet exemple doit être exécuté à partir d’une invite de commandes.</span><span class="sxs-lookup"><span data-stu-id="09316-119">This example should be run from a command prompt.</span></span>


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



<span data-ttu-id="09316-120">L’exemple de script suivant montre comment ouvrir une connexion HTTP, envoyer une requête HTTP et obtenir tous les en-têtes de la réponse.</span><span class="sxs-lookup"><span data-stu-id="09316-120">The following scripting example shows how to open an HTTP connection, send an HTTP request, and get all of the headers from the response.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="09316-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="09316-121">Requirements</span></span>



| <span data-ttu-id="09316-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="09316-122">Requirement</span></span> | <span data-ttu-id="09316-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="09316-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="09316-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="09316-124">Minimum supported client</span></span><br/> | <span data-ttu-id="09316-125">Windows XP, Windows 2000 Professionnel avec les \[ applications de bureau SP3 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="09316-125">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>            |
| <span data-ttu-id="09316-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="09316-126">Minimum supported server</span></span><br/> | <span data-ttu-id="09316-127">Windows Server 2003, Windows 2000 Server avec les \[ applications de bureau SP3 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="09316-127">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>         |
| <span data-ttu-id="09316-128">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="09316-128">Redistributable</span></span><br/>          | <span data-ttu-id="09316-129">WinHTTP 5,0 et Internet Explorer 5,01 ou version ultérieure sur Windows XP et Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="09316-129">WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.</span></span><br/> |
| <span data-ttu-id="09316-130">MIDL</span><span class="sxs-lookup"><span data-stu-id="09316-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="09316-131"><dt>HttpRequest. idl</dt></span><span class="sxs-lookup"><span data-stu-id="09316-131"><dt>HttpRequest.idl</dt></span></span> </dl> |
| <span data-ttu-id="09316-132">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="09316-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="09316-133"><dt>WinHTTP. lib</dt></span><span class="sxs-lookup"><span data-stu-id="09316-133"><dt>Winhttp.lib</dt></span></span> </dl>     |
| <span data-ttu-id="09316-134">DLL</span><span class="sxs-lookup"><span data-stu-id="09316-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="09316-135"><dt>Winhttp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="09316-135"><dt>Winhttp.dll</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="09316-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="09316-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="09316-137">**IWinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="09316-137">**IWinHttpRequest**</span></span>](iwinhttprequest-interface.md)
</dt> <dt>

[<span data-ttu-id="09316-138">**WinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="09316-138">**WinHttpRequest**</span></span>](winhttprequest.md)
</dt> <dt>

[<span data-ttu-id="09316-139">**GetResponseHeader**</span><span class="sxs-lookup"><span data-stu-id="09316-139">**GetResponseHeader**</span></span>](iwinhttprequest-getresponseheader.md)
</dt> <dt>

[<span data-ttu-id="09316-140">Versions de WinHTTP</span><span class="sxs-lookup"><span data-stu-id="09316-140">WinHTTP Versions</span></span>](winhttp-versions.md)
</dt> </dl>

 

 




