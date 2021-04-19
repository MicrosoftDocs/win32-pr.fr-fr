---
description: Définit les informations d’identification à utiliser avec un serveur HTTP, qu’il s’agisse d’un serveur proxy ou d’un serveur d’origine.
ms.assetid: d96c6e76-92b8-4ad7-8ca7-a9acbed523ff
title: 'IWinHttpRequest :: SetCredentials, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWinHttpRequest.SetCredentials
- WinHttpRequest.SetCredentials
api_type:
- COM
api_location:
- Winhttp.dll
ms.openlocfilehash: 46b0dfb321763a3b3bfe622e116f2e76c5e59423
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106539103"
---
# <a name="iwinhttprequestsetcredentials-method"></a><span data-ttu-id="1e42b-103">IWinHttpRequest :: SetCredentials, méthode</span><span class="sxs-lookup"><span data-stu-id="1e42b-103">IWinHttpRequest::SetCredentials method</span></span>

<span data-ttu-id="1e42b-104">La méthode **SetCredentials** définit les informations d’identification à utiliser avec un serveur http, qu’il s’agisse d’un serveur proxy ou d’un serveur d’origine.</span><span class="sxs-lookup"><span data-stu-id="1e42b-104">The **SetCredentials** method sets credentials to be used with an HTTP server, whether it is a proxy server or an originating server.</span></span>

## <a name="syntax"></a><span data-ttu-id="1e42b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1e42b-105">Syntax</span></span>


```C++
HRESULT SetCredentials(
  [in] BSTR                             UserName,
  [in] BSTR                             Password,
  [in] HTTPREQUEST_SETCREDENTIALS_FLAGS Flags
);
```



## <a name="parameters"></a><span data-ttu-id="1e42b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1e42b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1e42b-107">*Nom d’utilisateur* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1e42b-107">*UserName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1e42b-108">Spécifie le nom d’utilisateur pour l’authentification.</span><span class="sxs-lookup"><span data-stu-id="1e42b-108">Specifies the user name for authentication.</span></span>

</dd> <dt>

<span data-ttu-id="1e42b-109">*Mot de passe* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1e42b-109">*Password* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1e42b-110">Spécifie le mot de passe pour l’authentification.</span><span class="sxs-lookup"><span data-stu-id="1e42b-110">Specifies the password for authentication.</span></span> <span data-ttu-id="1e42b-111">Ce paramètre est ignoré si *bstrUserName* est **null** ou manquant.</span><span class="sxs-lookup"><span data-stu-id="1e42b-111">This parameter is ignored if *bstrUserName* is **NULL** or missing.</span></span>

</dd> <dt>

<span data-ttu-id="1e42b-112">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="1e42b-112">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1e42b-113">Spécifie quand [**IWinHttpRequest**](iwinhttprequest-interface.md) utilise les informations d’identification.</span><span class="sxs-lookup"><span data-stu-id="1e42b-113">Specifies when [**IWinHttpRequest**](iwinhttprequest-interface.md) uses credentials.</span></span> <span data-ttu-id="1e42b-114">Il peut s’agir de l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="1e42b-114">Can be one of the following values.</span></span>



| <span data-ttu-id="1e42b-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="1e42b-115">Value</span></span>                                                                                                               | <span data-ttu-id="1e42b-116">Signification</span><span class="sxs-lookup"><span data-stu-id="1e42b-116">Meaning</span></span>                                        |
|---------------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="1e42b-117"><dt>\_SETCREDENTIALS HTTPREQUEST \_ pour le \_ serveur</dt></span><span class="sxs-lookup"><span data-stu-id="1e42b-117"><dt>HTTPREQUEST\_SETCREDENTIALS\_FOR\_SERVER</dt></span></span> </dl> | <span data-ttu-id="1e42b-118">Les informations d’identification sont transmises à un serveur.</span><span class="sxs-lookup"><span data-stu-id="1e42b-118">Credentials are passed to a server.</span></span><br/> |
| <dl> <span data-ttu-id="1e42b-119"><dt>\_SETCREDENTIALS HTTPREQUEST \_ pour le \_ proxy</dt></span><span class="sxs-lookup"><span data-stu-id="1e42b-119"><dt>HTTPREQUEST\_SETCREDENTIALS\_FOR\_PROXY</dt></span></span> </dl>  | <span data-ttu-id="1e42b-120">Les informations d’identification sont passées à un proxy.</span><span class="sxs-lookup"><span data-stu-id="1e42b-120">Credentials are passed to a proxy.</span></span><br/>  |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1e42b-121">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1e42b-121">Return value</span></span>

<span data-ttu-id="1e42b-122">La valeur de retour est **S \_ OK** en cas de réussite ou une valeur d’erreur dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="1e42b-122">The return value is **S\_OK** on success or an error value otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="1e42b-123">Notes</span><span class="sxs-lookup"><span data-stu-id="1e42b-123">Remarks</span></span>

<span data-ttu-id="1e42b-124">Cette méthode retourne une valeur d’erreur si un appel à l' [**ouverture**](iwinhttprequest-open.md) ne s’est pas terminé correctement.</span><span class="sxs-lookup"><span data-stu-id="1e42b-124">This method returns an error value if a call to [**Open**](iwinhttprequest-open.md) has not completed successfully.</span></span> <span data-ttu-id="1e42b-125">Il est supposé qu’une certaine mesure d’interaction avec un serveur proxy ou un serveur d’origine doit se produire pour que les utilisateurs puissent définir des informations d’identification pour la session.</span><span class="sxs-lookup"><span data-stu-id="1e42b-125">It is assumed that some measure of interaction with a proxy server or origin server must occur before users can set credentials for the session.</span></span> <span data-ttu-id="1e42b-126">En outre, jusqu’à ce que les utilisateurs sachent quels schémas d’authentification sont pris en charge, ils ne peuvent pas formater les informations d’identification.</span><span class="sxs-lookup"><span data-stu-id="1e42b-126">Moreover, until users know which authentication scheme(s) are supported, they cannot format the credentials.</span></span>

> [!Note]  
> <span data-ttu-id="1e42b-127">Pour Windows XP et Windows 2000, consultez la section [Configuration requise](winhttp-start-page.md) pour l’exécution de la page de démarrage de WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="1e42b-127">For Windows XP and Windows 2000, see the [Run-Time Requirements](winhttp-start-page.md) section of the WinHTTP Start Page.</span></span>

 

<span data-ttu-id="1e42b-128">Pour s’authentifier avec le serveur et le proxy, l’application doit appeler **SetCredentials** deux fois. tout d’abord, avec le paramètre *Flags* défini sur **HttpRequest \_ SETCREDENTIALS \_ pour \_ Server** et second, avec le paramètre *Flags* défini sur **HttpRequest \_ SETCREDENTIALS \_ pour \_ proxy**.</span><span class="sxs-lookup"><span data-stu-id="1e42b-128">To authenticate with both the server and the proxy, the application must call **SetCredentials** twice; first with the *Flags* parameter set to **HTTPREQUEST\_SETCREDENTIALS\_FOR\_SERVER**, and second, with the *Flags* parameter set to **HTTPREQUEST\_SETCREDENTIALS\_FOR\_PROXY**.</span></span>

## <a name="examples"></a><span data-ttu-id="1e42b-129">Exemples</span><span class="sxs-lookup"><span data-stu-id="1e42b-129">Examples</span></span>

<span data-ttu-id="1e42b-130">L’exemple suivant montre comment ouvrir une connexion HTTP, définir des informations d’identification pour le serveur, envoyer une requête HTTP et lire le texte de la réponse.</span><span class="sxs-lookup"><span data-stu-id="1e42b-130">The following example shows how to open an HTTP connection, set credentials for the server, send an HTTP request, and read the response text.</span></span> <span data-ttu-id="1e42b-131">Cet exemple doit être exécuté à partir d’une invite de commandes.</span><span class="sxs-lookup"><span data-stu-id="1e42b-131">This example must be run from a command prompt.</span></span>


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
        BSTR bstrMethod = SysAllocString(L"GET");
        BSTR bstrUrl = SysAllocString(L"https://microsoft.com");
        hr = pIWinHttpRequest->Open(bstrMethod, bstrUrl, varFalse);
        SysFreeString(bstrMethod);
        SysFreeString(bstrUrl);
    }
    if (SUCCEEDED(hr))
    {    // Set Credentials.
        BSTR bstrUserName = SysAllocString(L"User Name");
        BSTR bstrPassword = SysAllocString(L"Password");
        hr = pIWinHttpRequest->SetCredentials(
                               bstrUserName,
                               bstrPassword,
                               HTTPREQUEST_SETCREDENTIALS_FOR_SERVER);
        SysFreeString(bstrUserName);
        SysFreeString(bstrPassword);
    }
    if (SUCCEEDED(hr))
    {    // Send Request.
        hr = pIWinHttpRequest->Send(varEmpty);
    }
    if (SUCCEEDED(hr))
    {    // Get Response text.
        hr = pIWinHttpRequest->get_ResponseText(&bstrResponse);
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



<span data-ttu-id="1e42b-132">L’exemple de script suivant montre comment ouvrir une connexion HTTP, définir des informations d’identification pour le serveur, définir des informations d’identification pour un proxy, le cas échéant, envoyer une requête HTTP et lire le texte de la réponse.</span><span class="sxs-lookup"><span data-stu-id="1e42b-132">The following scripting example shows how to open an HTTP connection, set credentials for the server, set credentials for a proxy if one is used, send an HTTP request, and read the response text.</span></span>


```JScript
// HttpRequest SetCredentials flags
HTTPREQUEST_SETCREDENTIALS_FOR_SERVER = 0;
HTTPREQUEST_SETCREDENTIALS_FOR_PROXY = 1;

// Instantiate a WinHttpRequest object.
var WinHttpReq = new ActiveXObject("WinHttp.WinHttpRequest.5.1");

// Specify the target resource.
var targURL = "https://msdn.microsoft.com/downloads/samples/"+
              "internet/winhttp/auth/authenticate.asp";    
WinHttpReq.open("GET", targURL, false);

var Done = false;
var LastStatus=0;
do {
    // Send a request to the server and wait for a response.                               
    WinHttpReq.send(); 
    
    // Obtain the status code from the response.
    var Status = WinHttpReq.Status;

    switch (Status){
        // A 200 status indicates that the resource was retrieved.
        case 200:
            Done = true;
            break;
                
        // A 401 status indicates that the server 
        // requires authentication.    
        case 401:
            WScript.Echo("Requires Server UserName and Password.");

            // Specify the target resource.
            WinHttpReq.open("GET", targURL, false);
                            
            // Set credentials for the server.
            WinHttpReq.SetCredentials("User Name", "Password", 
                        HTTPREQUEST_SETCREDENTIALS_FOR_SERVER);

            // If the same credentials are requested twice, abort 
            // the request.  For simplicity, this sample does not 
            // check for a repeated sequence of status codes.
            if (LastStatus==401)
                Done = true;
            break;

        // A 407 status indicates that the proxy 
        // requires authentication.    
        case 407:
            WScript.Echo("Requires Proxy UserName and Password.");
                
            // Specify the target resource.
            WinHttpReq.open("GET", targURL, false);
    
            // Set credentials for the proxy.
            WinHttpReq.SetCredentials("User Name", "Password", 
                HTTPREQUEST_SETCREDENTIALS_FOR_PROXY);

            // If the same credentials are requested twice, abort 
            // the request.  For simplicity, this sample does not 
            // check for a repeated sequence of status codes.
            if (LastStatus==407)
                Done = true;
            break;
        
        // Any other status is unexpected.
        default:
            WScript.Echo("Unexpected Status: "+Status);
            Done = true;
            break;
    }
    
    // Keep track of the last status code.
    LastStatus = Status;
    
} while (!Done);

// Display the results of the request.
WScript.Echo(WinHttpReq.Status + "   " + WinHttpReq.StatusText);
WScript.Echo(WinHttpReq.GetAllResponseHeaders());
```



## <a name="requirements"></a><span data-ttu-id="1e42b-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1e42b-133">Requirements</span></span>



| <span data-ttu-id="1e42b-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1e42b-134">Requirement</span></span> | <span data-ttu-id="1e42b-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="1e42b-135">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="1e42b-136">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1e42b-136">Minimum supported client</span></span><br/> | <span data-ttu-id="1e42b-137">Windows XP, Windows 2000 Professionnel avec les \[ applications de bureau SP3 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1e42b-137">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>            |
| <span data-ttu-id="1e42b-138">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1e42b-138">Minimum supported server</span></span><br/> | <span data-ttu-id="1e42b-139">Windows Server 2003, Windows 2000 Server avec les \[ applications de bureau SP3 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1e42b-139">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>         |
| <span data-ttu-id="1e42b-140">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="1e42b-140">Redistributable</span></span><br/>          | <span data-ttu-id="1e42b-141">WinHTTP 5,0 et Internet Explorer 5,01 ou version ultérieure sur Windows XP et Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="1e42b-141">WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.</span></span><br/> |
| <span data-ttu-id="1e42b-142">MIDL</span><span class="sxs-lookup"><span data-stu-id="1e42b-142">IDL</span></span><br/>                      | <dl> <span data-ttu-id="1e42b-143"><dt>HttpRequest. idl</dt></span><span class="sxs-lookup"><span data-stu-id="1e42b-143"><dt>HttpRequest.idl</dt></span></span> </dl> |
| <span data-ttu-id="1e42b-144">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="1e42b-144">Library</span></span><br/>                  | <dl> <span data-ttu-id="1e42b-145"><dt>WinHTTP. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1e42b-145"><dt>Winhttp.lib</dt></span></span> </dl>     |
| <span data-ttu-id="1e42b-146">DLL</span><span class="sxs-lookup"><span data-stu-id="1e42b-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1e42b-147"><dt>Winhttp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1e42b-147"><dt>Winhttp.dll</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="1e42b-148">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1e42b-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e42b-149">**IWinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="1e42b-149">**IWinHttpRequest**</span></span>](iwinhttprequest-interface.md)
</dt> <dt>

[<span data-ttu-id="1e42b-150">**WinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="1e42b-150">**WinHttpRequest**</span></span>](winhttprequest.md)
</dt> <dt>

[<span data-ttu-id="1e42b-151">Versions de WinHTTP</span><span class="sxs-lookup"><span data-stu-id="1e42b-151">WinHTTP Versions</span></span>](winhttp-versions.md)
</dt> </dl>

 

 




