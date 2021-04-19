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
# <a name="iwinhttprequestwaitforresponse-method"></a><span data-ttu-id="79407-103">IWinHttpRequest :: WaitForResponse, méthode</span><span class="sxs-lookup"><span data-stu-id="79407-103">IWinHttpRequest::WaitForResponse method</span></span>

<span data-ttu-id="79407-104">La méthode **WaitForResponse** attend la fin d’une méthode d' [**envoi**](iwinhttprequest-send.md) asynchrone, avec une valeur de délai d’attente facultative, en secondes.</span><span class="sxs-lookup"><span data-stu-id="79407-104">The **WaitForResponse** method waits for an asynchronous [**Send**](iwinhttprequest-send.md) method to complete, with optional time-out value, in seconds.</span></span>

## <a name="syntax"></a><span data-ttu-id="79407-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="79407-105">Syntax</span></span>


```C++
HRESULT WaitForResponse(
  [in, optional] VARIANT      Timeout,
  [out, retval]  VARIANT_BOOL *Succeeded
);
```



## <a name="parameters"></a><span data-ttu-id="79407-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="79407-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="79407-107">*Délai d’expiration* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="79407-107">*Timeout* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="79407-108">Valeur du délai d’attente, en secondes.</span><span class="sxs-lookup"><span data-stu-id="79407-108">Time-out value, in seconds.</span></span> <span data-ttu-id="79407-109">Le délai d’attente par défaut est infini.</span><span class="sxs-lookup"><span data-stu-id="79407-109">Default time-out is infinite.</span></span> <span data-ttu-id="79407-110">Pour définir explicitement le délai d’attente sur Infinite, utilisez la valeur-1.</span><span class="sxs-lookup"><span data-stu-id="79407-110">To explicitly set time-out to infinite, use the value -1.</span></span>

</dd> <dt>

<span data-ttu-id="79407-111">Opération *réussie* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="79407-111">*Succeeded* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="79407-112">Reçoit l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="79407-112">Receives one of the following values.</span></span>



| <span data-ttu-id="79407-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="79407-113">Value</span></span>                                                                                                                                                         | <span data-ttu-id="79407-114">Signification</span><span class="sxs-lookup"><span data-stu-id="79407-114">Meaning</span></span>                                                |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <span id="VARIANT_TRUE"></span><span id="variant_true"></span><dl> <span data-ttu-id="79407-115"><dt>**VARIANTE \_ true**</dt></span><span class="sxs-lookup"><span data-stu-id="79407-115"><dt>**VARIANT\_TRUE**</dt></span></span> </dl>    | <span data-ttu-id="79407-116">Une réponse a été reçue.</span><span class="sxs-lookup"><span data-stu-id="79407-116">A response has been received.</span></span><br/>               |
| <span id="VARIANT_FALSE"></span><span id="variant_false"></span><dl> <span data-ttu-id="79407-117"><dt>**VARIANTE \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="79407-117"><dt>**VARIANT\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="79407-118">Le délai d’attente spécifié a été dépassé.</span><span class="sxs-lookup"><span data-stu-id="79407-118">The specified time-out period was exceeded.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="79407-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="79407-119">Return value</span></span>

<span data-ttu-id="79407-120">La valeur de retour est **S \_ OK** en cas de réussite ou une valeur d’erreur dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="79407-120">The return value is **S\_OK** on success or an error value otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="79407-121">Notes</span><span class="sxs-lookup"><span data-stu-id="79407-121">Remarks</span></span>

<span data-ttu-id="79407-122">Cette méthode interrompt l’exécution en attendant une réponse à une requête asynchrone.</span><span class="sxs-lookup"><span data-stu-id="79407-122">This method suspends execution while waiting for a response to an asynchronous request.</span></span> <span data-ttu-id="79407-123">Cette méthode doit être appelée après un [**envoi**](iwinhttprequest-send.md).</span><span class="sxs-lookup"><span data-stu-id="79407-123">This method should be called after a [**Send**](iwinhttprequest-send.md).</span></span> <span data-ttu-id="79407-124">L’appel d’applications peut spécifier une valeur de *délai d’attente* facultative, en secondes.</span><span class="sxs-lookup"><span data-stu-id="79407-124">Calling applications can specify an optional *Timeout* value, in seconds.</span></span> <span data-ttu-id="79407-125">Si cette méthode expire, la demande n’est pas abandonnée.</span><span class="sxs-lookup"><span data-stu-id="79407-125">If this method times out, the request is not aborted.</span></span> <span data-ttu-id="79407-126">De cette façon, l’application appelante peut continuer à attendre la demande, le cas échéant, dans un appel ultérieur à cette méthode.</span><span class="sxs-lookup"><span data-stu-id="79407-126">This way, the calling application can continue to wait for the request, if desired, in a subsequent call to this method.</span></span>

<span data-ttu-id="79407-127">L’appel de cette propriété après une méthode d' [**envoi**](iwinhttprequest-send.md) synchrone retourne immédiatement et n’a aucun effet.</span><span class="sxs-lookup"><span data-stu-id="79407-127">Calling this property after a synchronous [**Send**](iwinhttprequest-send.md) method returns immediately and has no effect.</span></span>

> [!Note]  
> <span data-ttu-id="79407-128">Pour Windows XP et Windows 2000, consultez la section [Configuration requise](winhttp-start-page.md) pour l’exécution de la page de démarrage de WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="79407-128">For Windows XP and Windows 2000, see the [Run-Time Requirements](winhttp-start-page.md) section of the WinHTTP Start Page.</span></span>

 

## <a name="examples"></a><span data-ttu-id="79407-129">Exemples</span><span class="sxs-lookup"><span data-stu-id="79407-129">Examples</span></span>

<span data-ttu-id="79407-130">L’exemple suivant montre comment ouvrir une connexion HTTP asynchrone, envoyer une requête HTTP, attendre la réponse et lire le texte de la réponse.</span><span class="sxs-lookup"><span data-stu-id="79407-130">The following example shows how to open an asynchronous HTTP connection, send an HTTP request, wait for the response and read the response text.</span></span>


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



<span data-ttu-id="79407-131">L’exemple de script suivant montre comment ouvrir une connexion HTTP asynchrone, envoyer une requête HTTP, attendre une réponse et lire le texte de la réponse.</span><span class="sxs-lookup"><span data-stu-id="79407-131">The following scripting example shows how to open an asynchronous HTTP connection, send an HTTP request, wait for a response, and read the response text.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="79407-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="79407-132">Requirements</span></span>



| <span data-ttu-id="79407-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="79407-133">Requirement</span></span> | <span data-ttu-id="79407-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="79407-134">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="79407-135">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="79407-135">Minimum supported client</span></span><br/> | <span data-ttu-id="79407-136">Windows XP, Windows 2000 Professionnel avec les \[ applications de bureau SP3 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="79407-136">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>            |
| <span data-ttu-id="79407-137">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="79407-137">Minimum supported server</span></span><br/> | <span data-ttu-id="79407-138">Windows Server 2003, Windows 2000 Server avec les \[ applications de bureau SP3 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="79407-138">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>         |
| <span data-ttu-id="79407-139">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="79407-139">Redistributable</span></span><br/>          | <span data-ttu-id="79407-140">WinHTTP 5,0 et Internet Explorer 5,01 ou version ultérieure sur Windows XP et Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="79407-140">WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.</span></span><br/> |
| <span data-ttu-id="79407-141">MIDL</span><span class="sxs-lookup"><span data-stu-id="79407-141">IDL</span></span><br/>                      | <dl> <span data-ttu-id="79407-142"><dt>HttpRequest. idl</dt></span><span class="sxs-lookup"><span data-stu-id="79407-142"><dt>HttpRequest.idl</dt></span></span> </dl> |
| <span data-ttu-id="79407-143">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="79407-143">Library</span></span><br/>                  | <dl> <span data-ttu-id="79407-144"><dt>WinHTTP. lib</dt></span><span class="sxs-lookup"><span data-stu-id="79407-144"><dt>Winhttp.lib</dt></span></span> </dl>     |
| <span data-ttu-id="79407-145">DLL</span><span class="sxs-lookup"><span data-stu-id="79407-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="79407-146"><dt>Winhttp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="79407-146"><dt>Winhttp.dll</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="79407-147">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="79407-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79407-148">**IWinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="79407-148">**IWinHttpRequest**</span></span>](iwinhttprequest-interface.md)
</dt> <dt>

[<span data-ttu-id="79407-149">**WinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="79407-149">**WinHttpRequest**</span></span>](winhttprequest.md)
</dt> <dt>

[<span data-ttu-id="79407-150">**Afficher**</span><span class="sxs-lookup"><span data-stu-id="79407-150">**Open**</span></span>](iwinhttprequest-open.md)
</dt> <dt>

[<span data-ttu-id="79407-151">Versions de WinHTTP</span><span class="sxs-lookup"><span data-stu-id="79407-151">WinHTTP Versions</span></span>](winhttp-versions.md)
</dt> </dl>

 

 




