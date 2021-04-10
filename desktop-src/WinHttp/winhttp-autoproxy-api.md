---
description: WinHTTP implémente le protocole WPAD à l’aide de la fonction WinHttpGetProxyForUrl, ainsi que deux fonctions utilitaires de prise en charge, WinHttpDetectAutoProxyConfigUrl et WinHttpGetIEProxyConfigForCurrentUser.
ms.assetid: d941e3c6-c1db-4de1-b640-4f582f86fc54
title: Fonctions de proxy AutoProxy WinHTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: afd4cf8289add4c72c2266df4bb9025e0b4c1aa0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951187"
---
# <a name="winhttp-autoproxy-functions"></a><span data-ttu-id="569c7-103">Fonctions de proxy AutoProxy WinHTTP</span><span class="sxs-lookup"><span data-stu-id="569c7-103">WinHTTP AutoProxy Functions</span></span>

<span data-ttu-id="569c7-104">WinHTTP implémente le protocole WPAD à l’aide de la fonction [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) , ainsi que deux fonctions utilitaires de prise en charge, [**WinHttpDetectAutoProxyConfigUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpdetectautoproxyconfigurl) et [**WinHttpGetIEProxyConfigForCurrentUser**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetieproxyconfigforcurrentuser).</span><span class="sxs-lookup"><span data-stu-id="569c7-104">WinHTTP implements the WPAD protocol using the [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) function along with two supporting utility functions, [**WinHttpDetectAutoProxyConfigUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpdetectautoproxyconfigurl) and [**WinHttpGetIEProxyConfigForCurrentUser**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetieproxyconfigforcurrentuser).</span></span>

<span data-ttu-id="569c7-105">La prise en charge d’AutoProxy n’est pas entièrement intégrée à la pile HTTP dans WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="569c7-105">AutoProxy support is not fully integrated into the HTTP stack in WinHTTP.</span></span> <span data-ttu-id="569c7-106">Avant d’envoyer une demande, l’application doit appeler [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) pour obtenir le nom d’un serveur proxy, puis appeler [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) à l’aide de l' **option WinHTTP \_ \_ proxy** pour définir la configuration du proxy sur le handle de demande WinHTTP créé par [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest).</span><span class="sxs-lookup"><span data-stu-id="569c7-106">Before sending a request, the application must call [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) to obtain the name of a proxy server and then call [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) using **WINHTTP\_OPTION\_PROXY** to set the proxy configuration on the WinHTTP request handle created by [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest).</span></span>

<span data-ttu-id="569c7-107">La fonction [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) peut exécuter les trois étapes du protocole WPAD décrit dans la vue d’ensemble précédente : (1) découvrir l’URL PAC, (2) Télécharger le fichier de script PAC, (3) exécuter le code de script et retourner la configuration du proxy dans une structure d' **\_ \_ informations de proxy WinHTTP** .</span><span class="sxs-lookup"><span data-stu-id="569c7-107">The [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) function can execute all three steps of the WPAD protocol described in the previous overview: (1) discover the PAC URL, (2) download the PAC script file, (3) execute the script code and return the proxy configuration in a **WINHTTP\_PROXY\_INFO** structure.</span></span> <span data-ttu-id="569c7-108">Éventuellement, si l’application sait à l’avance l’URL PAC, elle peut le spécifier à **WinHttpGetProxyForUrl**.</span><span class="sxs-lookup"><span data-stu-id="569c7-108">Optionally, if the application knows in advance the PAC URL it can specify this to **WinHttpGetProxyForUrl**.</span></span>

<span data-ttu-id="569c7-109">L’exemple de code suivant utilise le proxy AutoProxy.</span><span class="sxs-lookup"><span data-stu-id="569c7-109">The following example code uses autoproxy.</span></span> <span data-ttu-id="569c7-110">Il configure une requête HTTP d’extraction en créant d’abord les handles de connexion et de demande de session WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="569c7-110">It sets up an HTTP GET request by first creating the WinHTTP session connect and request handles.</span></span> <span data-ttu-id="569c7-111">L’appel [**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen) spécifie le **type d’accès WinHTTP \_ \_ \_ aucun \_ proxy** pour la configuration du proxy initial, pour indiquer que les demandes sont envoyées directement au serveur cible par défaut.</span><span class="sxs-lookup"><span data-stu-id="569c7-111">The [**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen) call specifies **WINHTTP\_ACCESS\_TYPE\_NO\_PROXY** for the initial proxy configuration, to indicate that requests are sent directly to the target server by default.</span></span> <span data-ttu-id="569c7-112">À l’aide de la fonction de proxy automatique, elle définit ensuite la configuration du proxy directement sur le handle de demande.</span><span class="sxs-lookup"><span data-stu-id="569c7-112">Using autoproxy, it then sets the proxy configuration directly on the request handle.</span></span>


```C++
  HINTERNET hHttpSession = NULL;
  HINTERNET hConnect     = NULL;
  HINTERNET hRequest     = NULL;
  
  WINHTTP_AUTOPROXY_OPTIONS  AutoProxyOptions;
  WINHTTP_PROXY_INFO         ProxyInfo;
  DWORD                      cbProxyInfoSize = sizeof(ProxyInfo);
  
  ZeroMemory( &AutoProxyOptions, sizeof(AutoProxyOptions) );
  ZeroMemory( &ProxyInfo, sizeof(ProxyInfo) );
  
//
// Create the WinHTTP session.
//
  hHttpSession = WinHttpOpen( L"WinHTTP AutoProxy Sample/1.0",
                              WINHTTP_ACCESS_TYPE_NO_PROXY,
                              WINHTTP_NO_PROXY_NAME,
                              WINHTTP_NO_PROXY_BYPASS,
                              0 );
  
// Exit if WinHttpOpen failed.
  if( !hHttpSession )
    goto Exit;
  
//
// Create the WinHTTP connect handle.
//
  hConnect = WinHttpConnect( hHttpSession,
                             L"www.microsoft.com",
                             INTERNET_DEFAULT_HTTP_PORT,
                             0 );
  
// Exit if WinHttpConnect failed.
  if( !hConnect )
    goto Exit;
  
//
// Create the HTTP request handle.
//
  hRequest = WinHttpOpenRequest( hConnect,
                                 L"GET",
                                 L"ms.htm",
                                 L"HTTP/1.1",
                                 WINHTTP_NO_REFERER,
                                 WINHTTP_DEFAULT_ACCEPT_TYPES,
                                 0 );
  
// Exit if WinHttpOpenRequest failed.
  if( !hRequest )
    goto Exit;
  
//
// Set up the autoproxy call.
//

// Use auto-detection because the Proxy 
// Auto-Config URL is not known.
  AutoProxyOptions.dwFlags = WINHTTP_AUTOPROXY_AUTO_DETECT;

// Use DHCP and DNS-based auto-detection.
  AutoProxyOptions.dwAutoDetectFlags = 
                             WINHTTP_AUTO_DETECT_TYPE_DHCP |
                             WINHTTP_AUTO_DETECT_TYPE_DNS_A;

// If obtaining the PAC script requires NTLM/Negotiate
// authentication, then automatically supply the client
// domain credentials.
  AutoProxyOptions.fAutoLogonIfChallenged = TRUE;

//
// Call WinHttpGetProxyForUrl with our target URL. If 
// auto-proxy succeeds, then set the proxy info on the 
// request handle. If auto-proxy fails, ignore the error 
// and attempt to send the HTTP request directly to the 
// target server (using the default WINHTTP_ACCESS_TYPE_NO_PROXY 
// configuration, which the requesthandle will inherit 
// from the session).
//
  if( WinHttpGetProxyForUrl( hHttpSession,
                             L"https://www.microsoft.com/ms.htm",
                             &AutoProxyOptions,
                             &ProxyInfo))
  {
  // A proxy configuration was found, set it on the
  // request handle.
    
    if( !WinHttpSetOption( hRequest, 
                           WINHTTP_OPTION_PROXY,
                           &ProxyInfo,
                           cbProxyInfoSize ) )
    {
      // Exit if setting the proxy info failed.
      goto Exit;
    }
  }

//
// Send the request.
//
  if( !WinHttpSendRequest( hRequest,
                           WINHTTP_NO_ADDITIONAL_HEADERS,
                           0,
                           WINHTTP_NO_REQUEST_DATA,
                           0,
                           0,
                           NULL ) )
  {
    // Exit if WinHttpSendRequest failed.
    goto Exit;
  }

//
// Wait for the response.
//

  if( !WinHttpReceiveResponse( hRequest, NULL ) )
    goto Exit;

//
// A response has been received, then process it.
// (omitted)
//


  Exit:
  //
  // Clean up the WINHTTP_PROXY_INFO structure.
  //
    if( ProxyInfo.lpszProxy != NULL )
      GlobalFree(ProxyInfo.lpszProxy);

    if( ProxyInfo.lpszProxyBypass != NULL )
      GlobalFree( ProxyInfo.lpszProxyBypass );

  //
  // Close the WinHTTP handles.
  //
    if( hRequest != NULL )
      WinHttpCloseHandle( hRequest );
  
    if( hConnect != NULL )
      WinHttpCloseHandle( hConnect );
  
    if( hHttpSession != NULL )
      WinHttpCloseHandle( hHttpSession );

```



<span data-ttu-id="569c7-113">Dans l’exemple de code fourni, l’appel à [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) indique à la fonction de détecter automatiquement le fichier de configuration automatique de proxy en spécifiant l’indicateur de **\_ \_ \_ détection automatique de proxy WinHTTP** dans la structure des [**\_ \_ options de proxy automatique WinHTTP**](/windows/win32/api/winhttp/ns-winhttp-winhttp_autoproxy_options) .</span><span class="sxs-lookup"><span data-stu-id="569c7-113">In the provided example code, the call to [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) instructs the function to discover the proxy auto-config file automatically by specifying the **WINHTTP\_AUTOPROXY\_AUTO\_DETECT** flag in the [**WINHTTP\_AUTOPROXY\_OPTIONS**](/windows/win32/api/winhttp/ns-winhttp-winhttp_autoproxy_options) structure.</span></span> <span data-ttu-id="569c7-114">L’utilisation de l’indicateur de détection automatique de PROXY pour WinHTTP requiert que le code spécifie l’un des indicateurs de détection automatique (ou les deux) (le type de détection automatique **WinHTTP \_ \_ \_ \_ DHCP** et **le type de détection \_ automatique WinHTTP \_ \_ \_ DNS \_ A**). **\_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="569c7-114">Use of the **WINHTTP\_AUTOPROXY\_AUTO\_DETECT** flag requires the code to specify one or both of the auto-detection flags (**WINHTTP\_AUTO\_DETECT\_TYPE\_DHCP**, **WINHTTP\_AUTO\_DETECT\_TYPE\_DNS\_A**).</span></span> <span data-ttu-id="569c7-115">L’exemple de code utilise la fonctionnalité de détection automatique de **WinHttpGetProxyForUrl** , car l’URL PAC n’est pas connue à l’avance.</span><span class="sxs-lookup"><span data-stu-id="569c7-115">The example code uses the auto-detection feature of **WinHttpGetProxyForUrl** because the PAC URL is not known in advance.</span></span> <span data-ttu-id="569c7-116">Si une URL PAC ne peut pas être localisée sur le réseau dans ce scénario, **WinHttpGetProxyForUrl** échoue ([**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retourne une **erreur la détection automatique \_ WinHTTP \_ \_ a échoué**).</span><span class="sxs-lookup"><span data-stu-id="569c7-116">If a PAC URL cannot be located on the network in this scenario, **WinHttpGetProxyForUrl** fails ([**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns **ERROR\_WINHTTP\_AUTODETECTION\_FAILED**).</span></span>

## <a name="if-the-pac-url-is-known-in-advance"></a><span data-ttu-id="569c7-117">Si l’URL PAC est connue à l’avance</span><span class="sxs-lookup"><span data-stu-id="569c7-117">If the PAC URL is Known in Advance</span></span>

<span data-ttu-id="569c7-118">Si l’application connaît l’URL PAC, elle peut la spécifier dans la structure des \_ options de proxy \_ automatique WinHTTP et configurer [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) pour ignorer la phase de détection automatique.</span><span class="sxs-lookup"><span data-stu-id="569c7-118">If the application does know the PAC URL, it can specify it in the WINHTTP\_AUTOPROXY\_OPTIONS structure and configure [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) to skip the auto-detection phase.</span></span>

<span data-ttu-id="569c7-119">Par exemple, si un fichier PAC est disponible sur le réseau local à l’URL « https://InternalSite/proxy-config.pac », l’appel à [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) se présente comme suit.</span><span class="sxs-lookup"><span data-stu-id="569c7-119">For example, if a PAC file is available on the local network at the URL, "https://InternalSite/proxy-config.pac", the call to [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) would look the following.</span></span>


```C++
//
// Set up the autoproxy call.
//

// The proxy auto-config URL is known. Auto-detection
// is not required.
  AutoProxyOptions.dwFlags = WINHTTP_AUTOPROXY_CONFIG_URL;

// Set the proxy auto-config URL.
  AutoProxyOptions. lpszAutoConfigUrl =  L"https://InternalSite/proxy-config.pac";

// If obtaining the PAC script requires NTLM/Negotiate
// authentication, then automatically supply the client
// domain credentials.
  AutoProxyOptions.fAutoLogonIfChallenged = TRUE;

//
// Call WinHttpGetProxyForUrl with our target URL. If auto-proxy
// succeeds, then set the proxy info on the request handle.
// If auto-proxy fails, ignore the error and attempt to send the
// HTTP request directly to the target server (using the default
// WINHTTP_ACCESS_TYPE_NO_PROXY configuration, which the request
// handle will inherit from the session).
//
  if( WinHttpGetProxyForUrl( hHttpSession,
                             L"https://www.microsoft.com/ms.htm",
                             &AutoProxyOptions,
                             &ProxyInfo ) )
{
  //...

```



<span data-ttu-id="569c7-120">Si la structure des [**\_ \_ options de proxy automatique WinHTTP**](/windows/win32/api/winhttp/ns-winhttp-winhttp_autoproxy_options) spécifie les indicateurs d’URL de la configuration automatique de proxy **\_ \_ automatique \_ WinHTTP** et de la configuration de proxy automatique WinHTTP (et SPÉCIFIe les indicateurs auto-detction et une URL de configuration automatique), [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) tente d’abord la détection automatique, puis, si la détection automatique ne parvient pas à localiser une URL PAC, « revient » à l’URL de configuration **\_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="569c7-120">If the [**WINHTTP\_AUTOPROXY\_OPTIONS**](/windows/win32/api/winhttp/ns-winhttp-winhttp_autoproxy_options) structure specifies both **WINHTTP\_AUTOPROXY\_AUTO\_DETECT** and **WINHTTP\_AUTOPROXY\_CONFIG\_URL** flags (and specifies auto-detction flags and an auto-config URL), [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) first attempts auto-detection, and then, if auto-detection fails to locate a PAC URL, "falls back" to the auto-config URL supplied by the application.</span></span>

## <a name="the-winhttpdetectautoproxyconfigurl-function"></a><span data-ttu-id="569c7-121">Fonction WinHttpDetectAutoProxyConfigUrl</span><span class="sxs-lookup"><span data-stu-id="569c7-121">The WinHttpDetectAutoProxyConfigUrl Function</span></span>

<span data-ttu-id="569c7-122">La fonction [**WinHttpDetectAutoProxyConfigUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpdetectautoproxyconfigurl) implémente un sous-ensemble du protocole WPAD : elle tente de détecter automatiquement l’URL du fichier de configuration automatique de proxy, sans télécharger ou exécuter le fichier PAC.</span><span class="sxs-lookup"><span data-stu-id="569c7-122">The [**WinHttpDetectAutoProxyConfigUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpdetectautoproxyconfigurl) function implements a subset of the WPAD protocol: it attempts to auto-detect the URL for the proxy auto-config file, without downloading or executing the PAC file.</span></span> <span data-ttu-id="569c7-123">Cette fonction est utile dans les cas particuliers où une application cliente Web doit gérer le téléchargement et l’exécution du fichier PAC lui-même.</span><span class="sxs-lookup"><span data-stu-id="569c7-123">This function is useful in special situations where a Web client application must handle the download and execution of the PAC file itself.</span></span>

## <a name="the-winhttpgetieproxyconfigforcurrentuser-function"></a><span data-ttu-id="569c7-124">Fonction WinHttpGetIEProxyConfigForCurrentUser</span><span class="sxs-lookup"><span data-stu-id="569c7-124">The WinHttpGetIEProxyConfigForCurrentUser Function</span></span>

<span data-ttu-id="569c7-125">La fonction [**WinHttpGetIEProxyConfigForCurrentUser**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetieproxyconfigforcurrentuser) retourne les paramètres de proxy Internet Explorer actuels de l’utilisateur pour la connexion réseau active actuelle, sans appeler « WinInet.dll ».</span><span class="sxs-lookup"><span data-stu-id="569c7-125">The [**WinHttpGetIEProxyConfigForCurrentUser**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetieproxyconfigforcurrentuser) function returns the current user Internet Explorer proxy settings for the current active network connection, without calling into "WinInet.dll".</span></span> <span data-ttu-id="569c7-126">Cette fonction est utile uniquement lorsqu’elle est appelée dans un processus qui s’exécute sous une identité de compte d’utilisateur interactif, car aucune configuration de proxy Internet Explorer n’est susceptible d’être disponible dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="569c7-126">This function is only useful when called within a process that is running under an interactive user account identity, because no Internet Explorer proxy configuration is likely to be available otherwise.</span></span> <span data-ttu-id="569c7-127">Par exemple, il n’est pas utile d’appeler cette fonction à partir d’une DLL ISAPI s’exécutant dans le processus de service IIS.</span><span class="sxs-lookup"><span data-stu-id="569c7-127">For example, it would not be useful to call this function from an ISAPI DLL running in the IIS service process.</span></span> <span data-ttu-id="569c7-128">Pour plus d’informations et pour un scénario dans lequel une application basée sur WinHTTP utilise **WinHttpGetIEProxyConfigForCurrentUser**, consultez [découverte sans fichier de configuration automatique](discovery-without-an-auto-config-file.md).</span><span class="sxs-lookup"><span data-stu-id="569c7-128">For more information and a scenario in which a WinHTTP-based application would use **WinHttpGetIEProxyConfigForCurrentUser**, see [Discovery Without an Auto-Config File](discovery-without-an-auto-config-file.md).</span></span>

 

 
