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
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/10/2021
ms.locfileid: "104211663"
---
# <a name="iwinhttprequestsettimeouts-method"></a><span data-ttu-id="16f41-103">IWinHttpRequest :: SetTimeouts, méthode</span><span class="sxs-lookup"><span data-stu-id="16f41-103">IWinHttpRequest::SetTimeouts method</span></span>

<span data-ttu-id="16f41-104">La méthode **SetTimeouts** spécifie les différents composants de délai d’attente d’une opération d’envoi/réception, en millisecondes.</span><span class="sxs-lookup"><span data-stu-id="16f41-104">The **SetTimeouts** method specifies the individual time-out components of a send/receive operation, in milliseconds.</span></span>

## <a name="syntax"></a><span data-ttu-id="16f41-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="16f41-105">Syntax</span></span>


```C++
HRESULT SetTimeouts(
  [in] long ResolveTimeout,
  [in] long ConnectTimeout,
  [in] long SendTimeout,
  [in] long ReceiveTimeout
);
```



## <a name="parameters"></a><span data-ttu-id="16f41-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="16f41-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="16f41-107">*ResolveTimeout* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="16f41-107">*ResolveTimeout* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="16f41-108">Valeur de délai d’attente appliquée lors de la résolution d’un nom d’hôte (tel que `www.microsoft.com` ) en adresse IP (par exemple, 192.168.131.199), en millisecondes.</span><span class="sxs-lookup"><span data-stu-id="16f41-108">Time-out value applied when resolving a host name (such as `www.microsoft.com`) to an IP address (such as 192.168.131.199), in milliseconds.</span></span> <span data-ttu-id="16f41-109">La valeur par défaut est zéro, ce qui signifie qu’il n’y a pas de délai d’attente (infini).</span><span class="sxs-lookup"><span data-stu-id="16f41-109">The default value is zero, meaning no time-out (infinite).</span></span> <span data-ttu-id="16f41-110">Si le délai d’expiration DNS est spécifié à l’aide du \_ \_ délai de résolution de noms, il existe une surcharge d’un thread par demande.</span><span class="sxs-lookup"><span data-stu-id="16f41-110">If DNS timeout is specified using NAME\_RESOLUTION\_TIMEOUT, there is an overhead of one thread per request.</span></span>

</dd> <dt>

<span data-ttu-id="16f41-111">*ConnectTimeout* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="16f41-111">*ConnectTimeout* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="16f41-112">Valeur de délai d’attente appliquée lors de l’établissement d’un socket de communication avec le serveur cible, en millisecondes.</span><span class="sxs-lookup"><span data-stu-id="16f41-112">Time-out value applied when establishing a communication socket with the target server, in milliseconds.</span></span> <span data-ttu-id="16f41-113">La valeur par défaut est 60,000 (60 secondes).</span><span class="sxs-lookup"><span data-stu-id="16f41-113">The default value is 60,000 (60 seconds).</span></span>

</dd> <dt>

<span data-ttu-id="16f41-114">*SendTimeout* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="16f41-114">*SendTimeout* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="16f41-115">Valeur de délai d’attente appliquée lors de l’envoi d’un paquet individuel de données de demande sur le socket de communication vers le serveur cible, en millisecondes.</span><span class="sxs-lookup"><span data-stu-id="16f41-115">Time-out value applied when sending an individual packet of request data on the communication socket to the target server, in milliseconds.</span></span> <span data-ttu-id="16f41-116">Une demande volumineuse envoyée à un serveur HTTP est normalement divisée en plusieurs paquets ; le délai d’attente d’envoi s’applique à l’envoi individuel de chaque paquet.</span><span class="sxs-lookup"><span data-stu-id="16f41-116">A large request sent to an HTTP server are normally be broken up into multiple packets; the send time-out applies to sending each packet individually.</span></span> <span data-ttu-id="16f41-117">La valeur par défaut est 30 000 (30 secondes).</span><span class="sxs-lookup"><span data-stu-id="16f41-117">The default value is 30,000 (30 seconds).</span></span>

</dd> <dt>

<span data-ttu-id="16f41-118">*ReceiveTimeout* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="16f41-118">*ReceiveTimeout* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="16f41-119">Valeur de délai d’attente appliquée lors de la réception d’un paquet de données de réponse du serveur cible, en millisecondes.</span><span class="sxs-lookup"><span data-stu-id="16f41-119">Time-out value applied when receiving a packet of response data from the target server, in milliseconds.</span></span> <span data-ttu-id="16f41-120">Les réponses volumineuses sont divisées en plusieurs paquets ; le délai d’attente de réception s’applique à la récupération de chaque paquet de données à partir du Socket.</span><span class="sxs-lookup"><span data-stu-id="16f41-120">Large responses are be broken up into multiple packets; the receive time-out applies to fetching each packet of data off the socket.</span></span> <span data-ttu-id="16f41-121">La valeur par défaut est 30 000 (30 secondes).</span><span class="sxs-lookup"><span data-stu-id="16f41-121">The default value is 30,000 (30 seconds).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="16f41-122">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="16f41-122">Return value</span></span>

<span data-ttu-id="16f41-123">La valeur de retour est **S \_ OK** en cas de réussite ou une valeur d’erreur dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="16f41-123">The return value is **S\_OK** on success or an error value otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="16f41-124">Notes</span><span class="sxs-lookup"><span data-stu-id="16f41-124">Remarks</span></span>

<span data-ttu-id="16f41-125">Tous les paramètres sont obligatoires.</span><span class="sxs-lookup"><span data-stu-id="16f41-125">All parameters are required.</span></span> <span data-ttu-id="16f41-126">La valeur 0 ou-1 définit un délai d’attente à attendre de façon infinie.</span><span class="sxs-lookup"><span data-stu-id="16f41-126">A value of 0 or -1 sets a time-out to wait infinitely.</span></span> <span data-ttu-id="16f41-127">Une valeur supérieure à 0 définit la valeur du délai d’attente en millisecondes.</span><span class="sxs-lookup"><span data-stu-id="16f41-127">A value greater than 0 sets the time-out value in milliseconds.</span></span> <span data-ttu-id="16f41-128">Par exemple, 30 000 définit le délai d’expiration sur 30 secondes.</span><span class="sxs-lookup"><span data-stu-id="16f41-128">For example, 30,000 would set the time-out to 30 seconds.</span></span> <span data-ttu-id="16f41-129">Toutes les valeurs négatives autres que-1 provoquent l’échec de cette méthode.</span><span class="sxs-lookup"><span data-stu-id="16f41-129">All negative values other than -1 cause this method to fail.</span></span>

<span data-ttu-id="16f41-130">Les valeurs de délai d’attente sont appliquées au niveau de la couche Winsock.</span><span class="sxs-lookup"><span data-stu-id="16f41-130">Time-out values are applied at the Winsock layer.</span></span>

> [!Note]  
> <span data-ttu-id="16f41-131">Pour Windows XP et Windows 2000, consultez la section [Configuration requise](winhttp-start-page.md) pour l’exécution de la page de démarrage de WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="16f41-131">For Windows XP and Windows 2000, see the [Run-Time Requirements](winhttp-start-page.md) section of the WinHttp start page.</span></span>

 

## <a name="examples"></a><span data-ttu-id="16f41-132">Exemples</span><span class="sxs-lookup"><span data-stu-id="16f41-132">Examples</span></span>

<span data-ttu-id="16f41-133">L’exemple suivant montre comment définir tous les délais d’expiration WinHTTP sur 30 secondes, ouvrir une connexion HTTP, envoyer une requête HTTP et lire le texte de la réponse.</span><span class="sxs-lookup"><span data-stu-id="16f41-133">The following example shows how to set all WinHTTP time-outs to 30 seconds, open an HTTP connection, send an HTTP request, and read the response text.</span></span>


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



<span data-ttu-id="16f41-134">L’exemple de script suivant montre comment définir tous les délais d’expiration WinHTTP sur 30 secondes, ouvrir une connexion HTTP et envoyer une requête HTTP.</span><span class="sxs-lookup"><span data-stu-id="16f41-134">The following scripting example shows how to set all WinHTTP time-outs to 30 seconds, open an HTTP connection, and send an HTTP request.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="16f41-135">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="16f41-135">Requirements</span></span>



| <span data-ttu-id="16f41-136">Condition requise</span><span class="sxs-lookup"><span data-stu-id="16f41-136">Requirement</span></span> | <span data-ttu-id="16f41-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="16f41-137">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="16f41-138">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="16f41-138">Minimum supported client</span></span><br/> | <span data-ttu-id="16f41-139">Windows XP, Windows 2000 Professionnel avec les \[ applications de bureau SP3 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="16f41-139">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>            |
| <span data-ttu-id="16f41-140">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="16f41-140">Minimum supported server</span></span><br/> | <span data-ttu-id="16f41-141">Windows Server 2003, Windows 2000 Server avec les \[ applications de bureau SP3 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="16f41-141">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>         |
| <span data-ttu-id="16f41-142">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="16f41-142">Redistributable</span></span><br/>          | <span data-ttu-id="16f41-143">WinHTTP 5,0 et Internet Explorer 5,01 ou version ultérieure sur Windows XP et Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="16f41-143">WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.</span></span><br/> |
| <span data-ttu-id="16f41-144">MIDL</span><span class="sxs-lookup"><span data-stu-id="16f41-144">IDL</span></span><br/>                      | <dl> <span data-ttu-id="16f41-145"><dt>HttpRequest. idl</dt></span><span class="sxs-lookup"><span data-stu-id="16f41-145"><dt>HttpRequest.idl</dt></span></span> </dl> |
| <span data-ttu-id="16f41-146">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="16f41-146">Library</span></span><br/>                  | <dl> <span data-ttu-id="16f41-147"><dt>WinHTTP. lib</dt></span><span class="sxs-lookup"><span data-stu-id="16f41-147"><dt>Winhttp.lib</dt></span></span> </dl>     |
| <span data-ttu-id="16f41-148">DLL</span><span class="sxs-lookup"><span data-stu-id="16f41-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="16f41-149"><dt>Winhttp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="16f41-149"><dt>Winhttp.dll</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="16f41-150">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="16f41-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16f41-151">**IWinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="16f41-151">**IWinHttpRequest**</span></span>](iwinhttprequest-interface.md)
</dt> <dt>

[<span data-ttu-id="16f41-152">**WinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="16f41-152">**WinHttpRequest**</span></span>](winhttprequest.md)
</dt> <dt>

[<span data-ttu-id="16f41-153">Versions de WinHTTP</span><span class="sxs-lookup"><span data-stu-id="16f41-153">WinHTTP Versions</span></span>](winhttp-versions.md)
</dt> </dl>

 

 




