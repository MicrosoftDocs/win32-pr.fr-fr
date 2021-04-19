---
description: Ouvre une connexion HTTP à une ressource HTTP.
ms.assetid: 5207e873-44c0-4eeb-9db8-d8b69432070c
title: 'IWinHttpRequest :: Open, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWinHttpRequest.Open
- WinHttpRequest.Open
api_type:
- COM
api_location:
- Winhttp.dll
ms.openlocfilehash: 5543832eb1ebc3df210237eff71d415de14b2f62
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106536710"
---
# <a name="iwinhttprequestopen-method"></a><span data-ttu-id="5749a-103">IWinHttpRequest :: Open, méthode</span><span class="sxs-lookup"><span data-stu-id="5749a-103">IWinHttpRequest::Open method</span></span>

<span data-ttu-id="5749a-104">La méthode **Open** ouvre une connexion http à une ressource http.</span><span class="sxs-lookup"><span data-stu-id="5749a-104">The **Open** method opens an HTTP connection to an HTTP resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="5749a-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5749a-105">Syntax</span></span>


```C++
HRESULT Open(
  [in]           BSTR    Method,
  [in]           BSTR    Url,
  [in, optional] VARIANT Async
);
```



## <a name="parameters"></a><span data-ttu-id="5749a-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5749a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5749a-107">*Méthode* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5749a-107">*Method* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5749a-108">Spécifie le [*verbe http*](glossary.md) utilisé pour la méthode **Open** , par exemple « obtenir » ou « put ».</span><span class="sxs-lookup"><span data-stu-id="5749a-108">Specifies the [*HTTP verb*](glossary.md) used for the **Open** method, such as "GET" or "PUT".</span></span> <span data-ttu-id="5749a-109">Utilisez toujours des majuscules, car certains serveurs ignorent les minuscules *http* s.</span><span class="sxs-lookup"><span data-stu-id="5749a-109">Always use uppercase as some servers ignore lowercase *HTTP verb* s.</span></span>

</dd> <dt>

<span data-ttu-id="5749a-110">*URL* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5749a-110">*Url* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5749a-111">Spécifie le nom de la ressource.</span><span class="sxs-lookup"><span data-stu-id="5749a-111">Specifies the name of the resource.</span></span> <span data-ttu-id="5749a-112">Il doit s’agir d’une URL absolue.</span><span class="sxs-lookup"><span data-stu-id="5749a-112">This must be an absolute URL.</span></span>

</dd> <dt>

<span data-ttu-id="5749a-113">*Asynchrone* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="5749a-113">*Async* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="5749a-114">Indique s’il faut ouvrir en mode asynchrone.</span><span class="sxs-lookup"><span data-stu-id="5749a-114">Indicates whether to open in asynchronous mode.</span></span>



| <span data-ttu-id="5749a-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="5749a-115">Value</span></span>                                                                                                                                                         | <span data-ttu-id="5749a-116">Signification</span><span class="sxs-lookup"><span data-stu-id="5749a-116">Meaning</span></span>                                                                                                                                                                                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="VARIANT_FALSE"></span><span id="variant_false"></span><dl> <span data-ttu-id="5749a-117"><dt>**VARIANTE \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="5749a-117"><dt>**VARIANT\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="5749a-118">Ouvre la connexion HTTP en mode synchrone.</span><span class="sxs-lookup"><span data-stu-id="5749a-118">Opens the HTTP connection in synchronous mode.</span></span> <span data-ttu-id="5749a-119">Un appel à [**Send**](iwinhttprequest-send.md) n’est pas retourné tant que [WinHTTP](about-winhttp.md) n’a pas complètement reçu la réponse.</span><span class="sxs-lookup"><span data-stu-id="5749a-119">A call to [**Send**](iwinhttprequest-send.md) does not return until [WinHTTP](about-winhttp.md) has completely received the response.</span></span><br/> |
| <span id="VARIANT_TRUE"></span><span id="variant_true"></span><dl> <span data-ttu-id="5749a-120"><dt>**VARIANTE \_ true**</dt></span><span class="sxs-lookup"><span data-stu-id="5749a-120"><dt>**VARIANT\_TRUE**</dt></span></span> </dl>    | <span data-ttu-id="5749a-121">Ouvre la connexion HTTP en mode asynchrone.</span><span class="sxs-lookup"><span data-stu-id="5749a-121">Opens the HTTP connection in asynchronous mode.</span></span><br/>                                                                                                                                        |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5749a-122">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5749a-122">Return value</span></span>

<span data-ttu-id="5749a-123">La valeur de retour est **S \_ OK** en cas de réussite ou une valeur d’erreur dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="5749a-123">The return value is **S\_OK** on success or an error value otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="5749a-124">Notes</span><span class="sxs-lookup"><span data-stu-id="5749a-124">Remarks</span></span>

<span data-ttu-id="5749a-125">Cette méthode ouvre une connexion à la ressource identifiée dans l' *URL* à l’aide du [*verbe http*](glossary.md) fourni dans la *méthode*.</span><span class="sxs-lookup"><span data-stu-id="5749a-125">This method opens a connection to the resource identified in *Url* using the [*HTTP verb*](glossary.md) given in *Method*.</span></span>

> [!Note]  
> <span data-ttu-id="5749a-126">Pour Windows XP et Windows 2000, consultez la section [Configuration requise](winhttp-start-page.md) pour l’exécution de la page de démarrage de WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="5749a-126">For Windows XP and Windows 2000, see the [Run-Time Requirements](winhttp-start-page.md) section of the WinHTTP Start Page.</span></span>

 

## <a name="examples"></a><span data-ttu-id="5749a-127">Exemples</span><span class="sxs-lookup"><span data-stu-id="5749a-127">Examples</span></span>

<span data-ttu-id="5749a-128">L’exemple suivant montre comment ouvrir une connexion HTTP, envoyer une requête HTTP et lire le texte de la réponse.</span><span class="sxs-lookup"><span data-stu-id="5749a-128">The following example shows how to open an HTTP connection, send an HTTP request, and read the response text.</span></span>


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
        hr = pIWinHttpRequest->get_ResponseText(&bstrResponse);
    }
    if (SUCCEEDED(hr))
    {
        // Print the response to a console.
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



<span data-ttu-id="5749a-129">L’exemple de script suivant montre comment ouvrir une connexion HTTP, envoyer une requête HTTP et lire le texte de la réponse.</span><span class="sxs-lookup"><span data-stu-id="5749a-129">The following scripting example shows how to open an HTTP connection, send an HTTP request, and read the response text.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="5749a-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5749a-130">Requirements</span></span>



| <span data-ttu-id="5749a-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5749a-131">Requirement</span></span> | <span data-ttu-id="5749a-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="5749a-132">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="5749a-133">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5749a-133">Minimum supported client</span></span><br/> | <span data-ttu-id="5749a-134">Windows XP, Windows 2000 Professionnel avec les \[ applications de bureau SP3 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5749a-134">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>            |
| <span data-ttu-id="5749a-135">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5749a-135">Minimum supported server</span></span><br/> | <span data-ttu-id="5749a-136">Windows Server 2003, Windows 2000 Server avec les \[ applications de bureau SP3 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5749a-136">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>         |
| <span data-ttu-id="5749a-137">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="5749a-137">Redistributable</span></span><br/>          | <span data-ttu-id="5749a-138">WinHTTP 5,0 et Internet Explorer 5,01 ou version ultérieure sur Windows XP et Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="5749a-138">WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.</span></span><br/> |
| <span data-ttu-id="5749a-139">MIDL</span><span class="sxs-lookup"><span data-stu-id="5749a-139">IDL</span></span><br/>                      | <dl> <span data-ttu-id="5749a-140"><dt>HttpRequest. idl</dt></span><span class="sxs-lookup"><span data-stu-id="5749a-140"><dt>HttpRequest.idl</dt></span></span> </dl> |
| <span data-ttu-id="5749a-141">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="5749a-141">Library</span></span><br/>                  | <dl> <span data-ttu-id="5749a-142"><dt>WinHTTP. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5749a-142"><dt>Winhttp.lib</dt></span></span> </dl>     |
| <span data-ttu-id="5749a-143">DLL</span><span class="sxs-lookup"><span data-stu-id="5749a-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5749a-144"><dt>Winhttp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5749a-144"><dt>Winhttp.dll</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="5749a-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5749a-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5749a-146">**IWinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="5749a-146">**IWinHttpRequest**</span></span>](iwinhttprequest-interface.md)
</dt> <dt>

[<span data-ttu-id="5749a-147">**WinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="5749a-147">**WinHttpRequest**</span></span>](winhttprequest.md)
</dt> <dt>

[<span data-ttu-id="5749a-148">Versions de WinHTTP</span><span class="sxs-lookup"><span data-stu-id="5749a-148">WinHTTP Versions</span></span>](winhttp-versions.md)
</dt> </dl>

 

 




