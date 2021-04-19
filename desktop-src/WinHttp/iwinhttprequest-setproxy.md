---
description: Définit les informations du serveur proxy.
ms.assetid: 279d0557-2718-4c50-b84c-cc7c8def57a6
title: 'IWinHttpRequest :: SetProxy, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWinHttpRequest.SetProxy
- WinHttpRequest.SetProxy
api_type:
- COM
api_location:
- Winhttp.dll
ms.openlocfilehash: 7af3c7c33b17e14c3adbdd70f3d2031e7438747a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106545151"
---
# <a name="iwinhttprequestsetproxy-method"></a><span data-ttu-id="4bd8b-103">IWinHttpRequest :: SetProxy, méthode</span><span class="sxs-lookup"><span data-stu-id="4bd8b-103">IWinHttpRequest::SetProxy method</span></span>

<span data-ttu-id="4bd8b-104">La méthode **SetProxy** définit les informations du serveur proxy.</span><span class="sxs-lookup"><span data-stu-id="4bd8b-104">The **SetProxy** method sets proxy server information.</span></span>

## <a name="syntax"></a><span data-ttu-id="4bd8b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4bd8b-105">Syntax</span></span>


```C++
HRESULT SetProxy(
  [in]           HTTPREQUEST_PROXY_SETTING ProxySetting,
  [in, optional] VARIANT                   ProxyServer,
  [in, optional] VARIANT                   BypassList
);
```



## <a name="parameters"></a><span data-ttu-id="4bd8b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4bd8b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4bd8b-107">*ProxySetting* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4bd8b-107">*ProxySetting* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4bd8b-108">Indicateurs qui contrôlent cette méthode.</span><span class="sxs-lookup"><span data-stu-id="4bd8b-108">The flags that control this method.</span></span> <span data-ttu-id="4bd8b-109">Il peut s’agir de l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="4bd8b-109">Can be one of the following values.</span></span>



| <span data-ttu-id="4bd8b-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="4bd8b-110">Value</span></span>                                                                                                           | <span data-ttu-id="4bd8b-111">Signification</span><span class="sxs-lookup"><span data-stu-id="4bd8b-111">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                               |
|-----------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="4bd8b-112"><dt>HTTPREQUEST \_ PROXYSETTING \_ par défaut</dt></span><span class="sxs-lookup"><span data-stu-id="4bd8b-112"><dt>HTTPREQUEST\_PROXYSETTING\_DEFAULT</dt></span></span> </dl>   | <span data-ttu-id="4bd8b-113">Paramètre de proxy par défaut.</span><span class="sxs-lookup"><span data-stu-id="4bd8b-113">Default proxy setting.</span></span> <span data-ttu-id="4bd8b-114">Équivalent à **la \_ \_ préconfiguration de HTTPREQUEST PROXYSETTING**.</span><span class="sxs-lookup"><span data-stu-id="4bd8b-114">Equivalent to **HTTPREQUEST\_PROXYSETTING\_PRECONFIG**.</span></span><br/>                                                                                                                                                                                                                                                             |
| <dl> <span data-ttu-id="4bd8b-115"><dt>préconfiguration de HTTPREQUEST \_ PROXYSETTING \_</dt></span><span class="sxs-lookup"><span data-stu-id="4bd8b-115"><dt>HTTPREQUEST\_PROXYSETTING\_PRECONFIG</dt></span></span> </dl> | <span data-ttu-id="4bd8b-116">Indique que les paramètres de proxy doivent être obtenus à partir du Registre.</span><span class="sxs-lookup"><span data-stu-id="4bd8b-116">Indicates that the proxy settings should be obtained from the registry.</span></span> <span data-ttu-id="4bd8b-117">Cela suppose que [Proxycfg.exe](proxycfg-exe--a-proxy-configuration-tool.md) a été exécutée.</span><span class="sxs-lookup"><span data-stu-id="4bd8b-117">This assumes that [Proxycfg.exe](proxycfg-exe--a-proxy-configuration-tool.md) has been run.</span></span> <span data-ttu-id="4bd8b-118">Si Proxycfg.exe n’a pas été exécuté et que la **\_ \_ préconfiguration HttpRequest PROXYSETTING** est spécifiée, le comportement est équivalent à **HTTPREQUEST \_ PROXYSETTING \_ direct**.</span><span class="sxs-lookup"><span data-stu-id="4bd8b-118">If Proxycfg.exe has not been run and **HTTPREQUEST\_PROXYSETTING\_PRECONFIG** is specified, then the behavior is equivalent to **HTTPREQUEST\_PROXYSETTING\_DIRECT**.</span></span><br/> |
| <dl> <span data-ttu-id="4bd8b-119"><dt>\_PROXYSETTING HTTPREQUEST \_ directe</dt></span><span class="sxs-lookup"><span data-stu-id="4bd8b-119"><dt>HTTPREQUEST\_PROXYSETTING\_DIRECT</dt></span></span> </dl>    | <span data-ttu-id="4bd8b-120">Indique que tous les serveurs HTTP et HTTPs doivent être accessibles directement.</span><span class="sxs-lookup"><span data-stu-id="4bd8b-120">Indicates that all HTTP and HTTPS servers should be accessed directly.</span></span> <span data-ttu-id="4bd8b-121">Utilisez cette commande s’il n’y a pas de serveur proxy.</span><span class="sxs-lookup"><span data-stu-id="4bd8b-121">Use this command if there is no proxy server.</span></span><br/>                                                                                                                                                                                                                       |
| <dl> <span data-ttu-id="4bd8b-122"><dt>\_proxy HTTPREQUEST PROXYSETTING \_</dt></span><span class="sxs-lookup"><span data-stu-id="4bd8b-122"><dt>HTTPREQUEST\_PROXYSETTING\_PROXY</dt></span></span> </dl>     | <span data-ttu-id="4bd8b-123">Quand **le \_ \_ proxy PROXYSETTING HTTPREQUEST** est spécifié, *varProxyServer* doit être défini sur une chaîne de serveur proxy et *varBypassList* doit être défini sur une chaîne de liste de contournement de domaine.</span><span class="sxs-lookup"><span data-stu-id="4bd8b-123">When **HTTPREQUEST\_PROXYSETTING\_PROXY** is specified, *varProxyServer* should be set to a proxy server string and *varBypassList* should be set to a domain bypass list string.</span></span> <span data-ttu-id="4bd8b-124">Cette configuration de proxy s’applique uniquement à l’instance actuelle de l’objet [**WinHttpRequest**](winhttprequest.md) .</span><span class="sxs-lookup"><span data-stu-id="4bd8b-124">This proxy configuration applies only to the current instance of the [**WinHttpRequest**](winhttprequest.md) object.</span></span><br/>                                    |



 

</dd> <dt>

<span data-ttu-id="4bd8b-125">*ProxyServer* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="4bd8b-125">*ProxyServer* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="4bd8b-126">Défini sur une chaîne de serveur proxy lorsque *ProxySetting* est égal à **HTTPREQUEST \_ ProxySetting \_ proxy**.</span><span class="sxs-lookup"><span data-stu-id="4bd8b-126">Set to a proxy server string when *ProxySetting* equals **HTTPREQUEST\_PROXYSETTING\_PROXY**.</span></span>

</dd> <dt>

<span data-ttu-id="4bd8b-127">*BypassList* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="4bd8b-127">*BypassList* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="4bd8b-128">Défini sur une chaîne de liste de contournement de domaine lorsque *ProxySetting* est égal à **HTTPREQUEST \_ ProxySetting \_ proxy**.</span><span class="sxs-lookup"><span data-stu-id="4bd8b-128">Set to a domain bypass list string when *ProxySetting* equals **HTTPREQUEST\_PROXYSETTING\_PROXY**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4bd8b-129">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4bd8b-129">Return value</span></span>

<span data-ttu-id="4bd8b-130">La valeur de retour est **S \_ OK** en cas de réussite ou une valeur d’erreur dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="4bd8b-130">The return value is **S\_OK** on success or an error value otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="4bd8b-131">Notes</span><span class="sxs-lookup"><span data-stu-id="4bd8b-131">Remarks</span></span>

<span data-ttu-id="4bd8b-132">Permet à l’application appelante de spécifier l’utilisation des informations de proxy par défaut (configurées par l’outil de configuration de proxy) ou de substituer les [Proxycfg.exe](proxycfg-exe--a-proxy-configuration-tool.md).</span><span class="sxs-lookup"><span data-stu-id="4bd8b-132">Enables the calling application to specify use of default proxy information (configured by the proxy configuration tool) or to override [Proxycfg.exe](proxycfg-exe--a-proxy-configuration-tool.md).</span></span> <span data-ttu-id="4bd8b-133">Cette méthode doit être appelée avant d’appeler la méthode [**Send**](iwinhttprequest-send.md) .</span><span class="sxs-lookup"><span data-stu-id="4bd8b-133">This method must be called before calling the [**Send**](iwinhttprequest-send.md) method.</span></span> <span data-ttu-id="4bd8b-134">Si cette méthode est appelée après la méthode [**Send**](iwinhttprequest-send.md) , elle n’a aucun effet.</span><span class="sxs-lookup"><span data-stu-id="4bd8b-134">If this method is called after the [**Send**](iwinhttprequest-send.md) method, it has no effect.</span></span>

<span data-ttu-id="4bd8b-135">[**IWinHttpRequest**](iwinhttprequest-interface.md) transmet ces paramètres aux services http Microsoft Windows (WinHTTP).</span><span class="sxs-lookup"><span data-stu-id="4bd8b-135">[**IWinHttpRequest**](iwinhttprequest-interface.md) passes these parameters to Microsoft Windows HTTP Services (WinHTTP).</span></span>

> [!Note]  
> <span data-ttu-id="4bd8b-136">Pour Windows XP et Windows 2000, consultez la section [Configuration requise](winhttp-start-page.md) pour l’exécution de la page de démarrage de WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="4bd8b-136">For Windows XP and Windows 2000, see the [Run-Time Requirements](winhttp-start-page.md) section of the WinHTTP Start Page.</span></span>

 

## <a name="examples"></a><span data-ttu-id="4bd8b-137">Exemples</span><span class="sxs-lookup"><span data-stu-id="4bd8b-137">Examples</span></span>

<span data-ttu-id="4bd8b-138">L’exemple suivant montre comment définir les paramètres de proxy pour un serveur proxy particulier, ouvrir une connexion HTTP, envoyer une requête HTTP et lire le texte de la réponse.</span><span class="sxs-lookup"><span data-stu-id="4bd8b-138">The following example shows how to set the proxy settings for a particular proxy server, open an HTTP connection, send an HTTP request, and read the response text.</span></span> <span data-ttu-id="4bd8b-139">Cet exemple doit être exécuté à partir d’une invite de commandes.</span><span class="sxs-lookup"><span data-stu-id="4bd8b-139">This example must be run from a command prompt.</span></span> <span data-ttu-id="4bd8b-140">Ces paramètres de proxy ne fonctionnent que si vous disposez d’un serveur proxy nommé « \_ serveur proxy » qui utilise le port 80 et que votre ordinateur peut contourner le serveur proxy lorsque le nom d’hôte se termine par « . Microsoft.com ».</span><span class="sxs-lookup"><span data-stu-id="4bd8b-140">These proxy settings work only if you have a proxy server named "proxy\_server" that uses port 80 and your computer can bypass the proxy server when the host name ends with ".microsoft.com".</span></span>


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
    VARIANT         varProxy;
    VARIANT         varUrl;
    
    CLSID           clsid;

    VariantInit(&varFalse);
    V_VT(&varFalse)   = VT_BOOL;
    V_BOOL(&varFalse) = VARIANT_FALSE;

    VariantInit(&varEmpty);
    V_VT(&varEmpty) = VT_ERROR;

    VariantInit(&varProxy);
    VariantInit(&varUrl);

    hr = CLSIDFromProgID(L"WinHttp.WinHttpRequest.5.1", &clsid);

    if (SUCCEEDED(hr))
    {
        hr = CoCreateInstance(clsid, NULL, 
                              CLSCTX_INPROC_SERVER, 
                              IID_IWinHttpRequest, 
                              (void **)&pIWinHttpRequest);
    }
    if (SUCCEEDED(hr))
    {   // Specify proxy and URL.
                varProxy.vt = VT_BSTR;
                varProxy.bstrVal = SysAllocString(L"proxy_server:80");
                varUrl.vt = VT_BSTR;
                varUrl.bstrVal = SysAllocString(L"*.microsoft.com");
                hr = pIWinHttpRequest->SetProxy(HTTPREQUEST_PROXYSETTING_PROXY,
                                    varProxy, varUrl); 
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
    if (SUCCEEDED(hr))
    {   // Print the response to a console.
                wprintf(L"%.256s",bstrResponse);
    }
        
        // Release memory.
    if (pIWinHttpRequest)
        pIWinHttpRequest->Release();
        if (varProxy.bstrVal)
                SysFreeString(varProxy.bstrVal);
        if (varUrl.bstrVal)
                SysFreeString(varUrl.bstrVal);
    if (bstrResponse)
        SysFreeString(bstrResponse);
        
        CoUninitialize();
        return 0;
}
```



<span data-ttu-id="4bd8b-141">L’exemple de script suivant montre comment définir les paramètres de proxy pour un serveur proxy particulier, ouvrir une connexion HTTP, envoyer une requête HTTP et lire le texte de la réponse.</span><span class="sxs-lookup"><span data-stu-id="4bd8b-141">The following scripting example shows how to set the proxy settings for a particular proxy server, open an HTTP connection, send an HTTP request, and read the response text.</span></span> <span data-ttu-id="4bd8b-142">Ces paramètres de proxy ne fonctionnent que si vous disposez d’un serveur proxy nommé « \_ serveur proxy » qui utilise le port 80 et que votre ordinateur peut contourner le serveur proxy lorsque le nom d’hôte se termine par « . Microsoft.com ».</span><span class="sxs-lookup"><span data-stu-id="4bd8b-142">These proxy settings work only if you have a proxy server named "proxy\_server" that uses port 80 and your computer can bypass the proxy server when the host name ends with ".microsoft.com".</span></span>


```JScript
// HttpRequest SetCredentials flags.
HTTPREQUEST_PROXYSETTING_DEFAULT   = 0;
HTTPREQUEST_PROXYSETTING_PRECONFIG = 0;
HTTPREQUEST_PROXYSETTING_DIRECT    = 1;
HTTPREQUEST_PROXYSETTING_PROXY     = 2;

// Instantiate a WinHttpRequest object.
var WinHttpReq = new ActiveXObject("WinHttp.WinHttpRequest.5.1");

// Use proxy_server for all requests outside of 
// the microsoft.com domain.
WinHttpReq.SetProxy( HTTPREQUEST_PROXYSETTING_PROXY, 
                     "proxy_server:80", 
                     "*.microsoft.com");

// Initialize an HTTP request.  
WinHttpReq.Open("GET", "https://www.microsoft.com", false);

// Send the HTTP request.
WinHttpReq.Send(); 

// Display the response text.
WScript.Echo( WinHttpReq.ResponseText);
```



## <a name="requirements"></a><span data-ttu-id="4bd8b-143">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4bd8b-143">Requirements</span></span>



| <span data-ttu-id="4bd8b-144">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4bd8b-144">Requirement</span></span> | <span data-ttu-id="4bd8b-145">Valeur</span><span class="sxs-lookup"><span data-stu-id="4bd8b-145">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="4bd8b-146">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4bd8b-146">Minimum supported client</span></span><br/> | <span data-ttu-id="4bd8b-147">Windows XP, Windows 2000 Professionnel avec les \[ applications de bureau SP3 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4bd8b-147">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>            |
| <span data-ttu-id="4bd8b-148">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4bd8b-148">Minimum supported server</span></span><br/> | <span data-ttu-id="4bd8b-149">Windows Server 2003, Windows 2000 Server avec les \[ applications de bureau SP3 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4bd8b-149">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>         |
| <span data-ttu-id="4bd8b-150">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="4bd8b-150">Redistributable</span></span><br/>          | <span data-ttu-id="4bd8b-151">WinHTTP 5,0 et Internet Explorer 5,01 ou version ultérieure sur Windows XP et Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="4bd8b-151">WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.</span></span><br/> |
| <span data-ttu-id="4bd8b-152">MIDL</span><span class="sxs-lookup"><span data-stu-id="4bd8b-152">IDL</span></span><br/>                      | <dl> <span data-ttu-id="4bd8b-153"><dt>HttpRequest. idl</dt></span><span class="sxs-lookup"><span data-stu-id="4bd8b-153"><dt>HttpRequest.idl</dt></span></span> </dl> |
| <span data-ttu-id="4bd8b-154">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="4bd8b-154">Library</span></span><br/>                  | <dl> <span data-ttu-id="4bd8b-155"><dt>WinHTTP. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4bd8b-155"><dt>Winhttp.lib</dt></span></span> </dl>     |
| <span data-ttu-id="4bd8b-156">DLL</span><span class="sxs-lookup"><span data-stu-id="4bd8b-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4bd8b-157"><dt>Winhttp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4bd8b-157"><dt>Winhttp.dll</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="4bd8b-158">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4bd8b-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4bd8b-159">**IWinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="4bd8b-159">**IWinHttpRequest**</span></span>](iwinhttprequest-interface.md)
</dt> <dt>

[<span data-ttu-id="4bd8b-160">**WinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="4bd8b-160">**WinHttpRequest**</span></span>](winhttprequest.md)
</dt> <dt>

[<span data-ttu-id="4bd8b-161">Versions de WinHTTP</span><span class="sxs-lookup"><span data-stu-id="4bd8b-161">WinHTTP Versions</span></span>](winhttp-versions.md)
</dt> </dl>

 

 




