---
description: WinHTTP implémente le protocole WPAD à l’aide de la fonction WinHttpGetProxyForUrl, ainsi que deux fonctions utilitaires de prise en charge, WinHttpDetectAutoProxyConfigUrl et WinHttpGetIEProxyConfigForCurrentUser.
ms.assetid: d941e3c6-c1db-4de1-b640-4f582f86fc54
title: Fonctions de proxy AutoProxy WinHTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8443567e12d7a0f3b75d09fc284dc634315ec635ff8b630821bb84031e39781b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119955709"
---
# <a name="winhttp-autoproxy-functions"></a>Fonctions de proxy AutoProxy WinHTTP

WinHTTP implémente le protocole WPAD à l’aide de la fonction [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) , ainsi que deux fonctions utilitaires de prise en charge, [**WinHttpDetectAutoProxyConfigUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpdetectautoproxyconfigurl) et [**WinHttpGetIEProxyConfigForCurrentUser**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetieproxyconfigforcurrentuser).

La prise en charge d’AutoProxy n’est pas entièrement intégrée à la pile HTTP dans WinHTTP. Avant d’envoyer une demande, l’application doit appeler [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) pour obtenir le nom d’un serveur proxy, puis appeler [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) à l’aide de l' **option WinHTTP \_ \_ proxy** pour définir la configuration du proxy sur le handle de demande WinHTTP créé par [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest).

La fonction [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) peut exécuter les trois étapes du protocole WPAD décrit dans la vue d’ensemble précédente : (1) découvrir l’URL PAC, (2) Télécharger le fichier de script PAC, (3) exécuter le code de script et retourner la configuration du proxy dans une structure d' **\_ \_ informations de proxy WinHTTP** . Éventuellement, si l’application sait à l’avance l’URL PAC, elle peut le spécifier à **WinHttpGetProxyForUrl**.

L’exemple de code suivant utilise le proxy AutoProxy. Il configure une requête HTTP d’extraction en créant d’abord les handles de connexion et de demande de session WinHTTP. L’appel [**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen) spécifie le **type d’accès WinHTTP \_ \_ \_ aucun \_ proxy** pour la configuration du proxy initial, pour indiquer que les demandes sont envoyées directement au serveur cible par défaut. À l’aide de la fonction de proxy automatique, elle définit ensuite la configuration du proxy directement sur le handle de demande.


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



Dans l’exemple de code fourni, l’appel à [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) indique à la fonction de détecter automatiquement le fichier de configuration automatique de proxy en spécifiant l’indicateur de **\_ \_ \_ détection automatique de proxy WinHTTP** dans la structure des [**\_ \_ options de proxy automatique WinHTTP**](/windows/win32/api/winhttp/ns-winhttp-winhttp_autoproxy_options) . L’utilisation de l’indicateur de détection automatique de PROXY pour WinHTTP requiert que le code spécifie l’un des indicateurs de détection automatique (ou les deux) (le type de détection automatique **WinHTTP \_ \_ \_ \_ DHCP** et **le type de détection \_ automatique WinHTTP \_ \_ \_ DNS \_ A**). **\_ \_ \_** L’exemple de code utilise la fonctionnalité de détection automatique de **WinHttpGetProxyForUrl** , car l’URL PAC n’est pas connue à l’avance. Si une URL PAC ne peut pas être localisée sur le réseau dans ce scénario, **WinHttpGetProxyForUrl** échoue ([**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retourne une **erreur la détection automatique \_ WinHTTP \_ \_ a échoué**).

## <a name="if-the-pac-url-is-known-in-advance"></a>Si l’URL PAC est connue à l’avance

Si l’application connaît l’URL PAC, elle peut la spécifier dans la structure des \_ options de proxy \_ automatique WinHTTP et configurer [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) pour ignorer la phase de détection automatique.

Par exemple, si un fichier PAC est disponible sur le réseau local à l’URL « https://InternalSite/proxy-config.pac », l’appel à [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) se présente comme suit.


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



Si la structure des [**\_ \_ options de proxy automatique WinHTTP**](/windows/win32/api/winhttp/ns-winhttp-winhttp_autoproxy_options) spécifie les indicateurs d’URL de la configuration automatique de proxy **\_ \_ automatique \_ WinHTTP** et de la configuration de proxy automatique WinHTTP (et SPÉCIFIe les indicateurs auto-detction et une URL de configuration automatique), [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) tente d’abord la détection automatique, puis, si la détection automatique ne parvient pas à localiser une URL PAC, « revient » à l’URL de configuration **\_ \_ \_**

## <a name="the-winhttpdetectautoproxyconfigurl-function"></a>Fonction WinHttpDetectAutoProxyConfigUrl

La fonction [**WinHttpDetectAutoProxyConfigUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpdetectautoproxyconfigurl) implémente un sous-ensemble du protocole WPAD : elle tente de détecter automatiquement l’URL du fichier de configuration automatique de proxy, sans télécharger ou exécuter le fichier PAC. Cette fonction est utile dans les cas particuliers où une application cliente Web doit gérer le téléchargement et l’exécution du fichier PAC lui-même.

## <a name="the-winhttpgetieproxyconfigforcurrentuser-function"></a>Fonction WinHttpGetIEProxyConfigForCurrentUser

La fonction [**WinHttpGetIEProxyConfigForCurrentUser**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetieproxyconfigforcurrentuser) retourne les paramètres de proxy Internet Explorer actuels de l’utilisateur pour la connexion réseau active actuelle, sans appeler « WinInet.dll ». Cette fonction est utile uniquement lorsqu’elle est appelée dans un processus qui s’exécute sous une identité de compte d’utilisateur interactif, car aucune configuration de proxy Internet Explorer n’est susceptible d’être disponible dans le cas contraire. Par exemple, il n’est pas utile d’appeler cette fonction à partir d’une DLL ISAPI s’exécutant dans le processus de service IIS. Pour plus d’informations et pour un scénario dans lequel une application basée sur WinHTTP utilise **WinHttpGetIEProxyConfigForCurrentUser**, consultez [découverte sans fichier de configuration automatique](discovery-without-an-auto-config-file.md).

 

 
