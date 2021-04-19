---
description: Ajoute, modifie ou supprime un en-tête de requête HTTP.
ms.assetid: 8cb4891d-0bdb-4dea-8ebe-d6ed26a50e41
title: 'IWinHttpRequest :: SetRequestHeader, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWinHttpRequest.SetRequestHeader
- WinHttpRequest.SetRequestHeader
api_type:
- COM
api_location:
- Winhttp.dll
ms.openlocfilehash: 9bc2ae6df420f38d11fb2f0f19d5fcbd0bcc0909
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106523054"
---
# <a name="iwinhttprequestsetrequestheader-method"></a><span data-ttu-id="48bb9-103">IWinHttpRequest :: SetRequestHeader, méthode</span><span class="sxs-lookup"><span data-stu-id="48bb9-103">IWinHttpRequest::SetRequestHeader method</span></span>

<span data-ttu-id="48bb9-104">La méthode **SetRequestHeader** ajoute, modifie ou supprime un en-tête de requête http.</span><span class="sxs-lookup"><span data-stu-id="48bb9-104">The **SetRequestHeader** method adds, changes, or deletes an HTTP request header.</span></span>

## <a name="syntax"></a><span data-ttu-id="48bb9-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="48bb9-105">Syntax</span></span>


```C++
HRESULT SetRequestHeader(
  [in] BSTR Header,
  [in] BSTR Value
);
```



## <a name="parameters"></a><span data-ttu-id="48bb9-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="48bb9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="48bb9-107">*En-tête* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="48bb9-107">*Header* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="48bb9-108">Spécifie le nom de l’en-tête à définir, par exemple « Depth ».</span><span class="sxs-lookup"><span data-stu-id="48bb9-108">Specifies the name of the header to be set, for example, "depth".</span></span> <span data-ttu-id="48bb9-109">Ce paramètre ne doit pas contenir de signe deux-points et doit être le texte réel de l’en-tête HTTP.</span><span class="sxs-lookup"><span data-stu-id="48bb9-109">This parameter should not contain a colon and must be the actual text of the HTTP header.</span></span>

</dd> <dt>

<span data-ttu-id="48bb9-110">*Valeur* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="48bb9-110">*Value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="48bb9-111">Spécifie la valeur de l’en-tête, par exemple "Infinity".</span><span class="sxs-lookup"><span data-stu-id="48bb9-111">Specifies the value of the header, for example, "infinity".</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="48bb9-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="48bb9-112">Return value</span></span>

<span data-ttu-id="48bb9-113">La valeur de retour est **S \_ OK** en cas de réussite ou une valeur d’erreur dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="48bb9-113">The return value is **S\_OK** on success or an error value otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="48bb9-114">Notes</span><span class="sxs-lookup"><span data-stu-id="48bb9-114">Remarks</span></span>

<span data-ttu-id="48bb9-115">Les en-têtes sont transférés entre les redirections.</span><span class="sxs-lookup"><span data-stu-id="48bb9-115">Headers are transferred across redirects.</span></span> <span data-ttu-id="48bb9-116">Cela peut créer une faille de sécurité.</span><span class="sxs-lookup"><span data-stu-id="48bb9-116">This can create a security vulnerability.</span></span> <span data-ttu-id="48bb9-117">Pour éviter que des en-têtes soient transférés si une redirection se produit, utilisez le rappel de [*\_ \_ rappel d’État WinHTTP*](/windows/win32/api/winhttp/nc-winhttp-winhttp_status_callback) pour corriger les en-têtes spécifiques lorsqu’une redirection se produit.</span><span class="sxs-lookup"><span data-stu-id="48bb9-117">To avoid having headers transferred if a redirect occurs, use the [*WINHTTP\_STATUS\_CALLBACK*](/windows/win32/api/winhttp/nc-winhttp-winhttp_status_callback) callback to correct the specific headers when a redirect occurs.</span></span>

<span data-ttu-id="48bb9-118">La méthode **SetRequestHeader** permet à l’application appelante d’ajouter ou de supprimer un en-tête de requête http avant l’envoi de la demande.</span><span class="sxs-lookup"><span data-stu-id="48bb9-118">The **SetRequestHeader** method enables the calling application to add or delete an HTTP request header prior to sending the request.</span></span> <span data-ttu-id="48bb9-119">Le nom d’en-tête est fourni dans l' *en-tête* et le jeton d’en-tête ou la valeur est donné dans la *valeur*.</span><span class="sxs-lookup"><span data-stu-id="48bb9-119">The header name is given in *Header*, and the header token or value is given in *Value*.</span></span> <span data-ttu-id="48bb9-120">Pour ajouter un en-tête, fournissez un nom et une valeur d’en-tête.</span><span class="sxs-lookup"><span data-stu-id="48bb9-120">To add a header, supply a header name and value.</span></span> <span data-ttu-id="48bb9-121">Si un autre en-tête portant ce nom existe déjà, il est remplacé.</span><span class="sxs-lookup"><span data-stu-id="48bb9-121">If another header already exists with this name, it is replaced.</span></span> <span data-ttu-id="48bb9-122">Pour supprimer un en-tête, définissez l' *en-tête* sur le nom de l’en-tête à supprimer et définissez la *valeur* sur **null**.</span><span class="sxs-lookup"><span data-stu-id="48bb9-122">To delete a header, set *Header* to the name of the header to delete and set *Value* to **NULL**.</span></span>

<span data-ttu-id="48bb9-123">Le nom et la valeur des en-têtes de demande ajoutés avec cette méthode sont validés.</span><span class="sxs-lookup"><span data-stu-id="48bb9-123">The name and value of request headers added with this method are validated.</span></span> <span data-ttu-id="48bb9-124">Les en-têtes doivent être correctement formés.</span><span class="sxs-lookup"><span data-stu-id="48bb9-124">Headers must be well formed.</span></span> <span data-ttu-id="48bb9-125">Pour plus d’informations sur les en-têtes HTTP valides, consultez [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt).</span><span class="sxs-lookup"><span data-stu-id="48bb9-125">For more information about valid HTTP headers, see [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt).</span></span> <span data-ttu-id="48bb9-126">Si un en-tête non valide est utilisé, une erreur se produit et l’en-tête n’est pas ajouté.</span><span class="sxs-lookup"><span data-stu-id="48bb9-126">If an invalid header is used, an error occurs and the header is not added.</span></span>

> [!Note]  
> <span data-ttu-id="48bb9-127">Pour Windows XP et Windows 2000, consultez la section [Configuration requise](winhttp-start-page.md) pour l’exécution de la page de démarrage de WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="48bb9-127">For Windows XP and Windows 2000, see the [Run-Time Requirements](winhttp-start-page.md) section of the WinHTTP Start Page.</span></span>

 

## <a name="examples"></a><span data-ttu-id="48bb9-128">Exemples</span><span class="sxs-lookup"><span data-stu-id="48bb9-128">Examples</span></span>

<span data-ttu-id="48bb9-129">L’exemple suivant montre comment ouvrir une connexion HTTP, définir un en-tête de demande, envoyer une requête HTTP et lire le texte de la réponse.</span><span class="sxs-lookup"><span data-stu-id="48bb9-129">The following example shows how to open an HTTP connection, set a request header, send an HTTP request, and read the response text.</span></span> <span data-ttu-id="48bb9-130">Cet exemple doit être exécuté à partir d’une invite de commandes.</span><span class="sxs-lookup"><span data-stu-id="48bb9-130">This example must be run from a command prompt.</span></span>


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
    {    // Open WinHttpRequest.
        BSTR bstrMethod  = SysAllocString(L"GET");
        BSTR bstrUrl = SysAllocString(L"https://microsoft.com");
        hr = pIWinHttpRequest->Open(bstrMethod, bstrUrl, varFalse);
        SysFreeString(bstrMethod);
        SysFreeString(bstrUrl);
    }
    if (SUCCEEDED(hr))
    {    // Set request header.
        BSTR bstrName  = SysAllocString(L"Date");
        BSTR bstrValue = SysAllocString(L"Fri, 16 Mar 2001 00:25:54 GMT");
        hr = pIWinHttpRequest->SetRequestHeader(bstrName, bstrValue);
        SysFreeString(bstrName);
        SysFreeString(bstrValue);
    }
    if (SUCCEEDED(hr))
    {    // Send Request.
        hr = pIWinHttpRequest->Send(varEmpty);
    }
    if (SUCCEEDED(hr))
    {    // Get Response headers.
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



<span data-ttu-id="48bb9-131">L’exemple de script suivant montre comment ouvrir une connexion HTTP, définir un en-tête de demande et envoyer une requête HTTP.</span><span class="sxs-lookup"><span data-stu-id="48bb9-131">The following scripting example shows how to open an HTTP connection, set a request header, and send an HTTP request.</span></span>


```JScript
// Instantiate a WinHttpRequest object.
var WinHttpReq = new ActiveXObject("WinHttp.WinHttpRequest.5.1");

// Initialize an HTTP request.  
WinHttpReq.Open("GET", "https://www.microsoft.com", false);

// Add/replace a request header.
WinHttpReq.SetRequestHeader("Date", Date());

// Send the HTTP request.
WinHttpReq.Send();
```



## <a name="requirements"></a><span data-ttu-id="48bb9-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="48bb9-132">Requirements</span></span>



| <span data-ttu-id="48bb9-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="48bb9-133">Requirement</span></span> | <span data-ttu-id="48bb9-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="48bb9-134">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="48bb9-135">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="48bb9-135">Minimum supported client</span></span><br/> | <span data-ttu-id="48bb9-136">Windows XP, Windows 2000 Professionnel avec les \[ applications de bureau SP3 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="48bb9-136">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>            |
| <span data-ttu-id="48bb9-137">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="48bb9-137">Minimum supported server</span></span><br/> | <span data-ttu-id="48bb9-138">Windows Server 2003, Windows 2000 Server avec les \[ applications de bureau SP3 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="48bb9-138">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>         |
| <span data-ttu-id="48bb9-139">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="48bb9-139">Redistributable</span></span><br/>          | <span data-ttu-id="48bb9-140">WinHTTP 5,0 et Internet Explorer 5,01 ou version ultérieure sur Windows XP et Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="48bb9-140">WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.</span></span><br/> |
| <span data-ttu-id="48bb9-141">MIDL</span><span class="sxs-lookup"><span data-stu-id="48bb9-141">IDL</span></span><br/>                      | <dl> <span data-ttu-id="48bb9-142"><dt>HttpRequest. idl</dt></span><span class="sxs-lookup"><span data-stu-id="48bb9-142"><dt>HttpRequest.idl</dt></span></span> </dl> |
| <span data-ttu-id="48bb9-143">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="48bb9-143">Library</span></span><br/>                  | <dl> <span data-ttu-id="48bb9-144"><dt>WinHTTP. lib</dt></span><span class="sxs-lookup"><span data-stu-id="48bb9-144"><dt>Winhttp.lib</dt></span></span> </dl>     |
| <span data-ttu-id="48bb9-145">DLL</span><span class="sxs-lookup"><span data-stu-id="48bb9-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="48bb9-146"><dt>Winhttp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="48bb9-146"><dt>Winhttp.dll</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="48bb9-147">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="48bb9-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48bb9-148">**IWinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="48bb9-148">**IWinHttpRequest**</span></span>](iwinhttprequest-interface.md)
</dt> <dt>

[<span data-ttu-id="48bb9-149">**WinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="48bb9-149">**WinHttpRequest**</span></span>](winhttprequest.md)
</dt> <dt>

[<span data-ttu-id="48bb9-150">Versions de WinHTTP</span><span class="sxs-lookup"><span data-stu-id="48bb9-150">WinHTTP Versions</span></span>](winhttp-versions.md)
</dt> </dl>

 

