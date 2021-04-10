---
description: Les services HTTP Microsoft Windows (WinHTTP) exposent un ensemble de fonctions C/C++ qui permettent à votre application d’accéder aux ressources HTTP sur le Web. Cette rubrique fournit une vue d’ensemble de la façon dont ces fonctions sont utilisées pour interagir avec un serveur HTTP.
ms.assetid: 66a1616b-0cf3-45c7-880b-e36728b5a9c4
title: Vue d’ensemble des sessions WinHTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98dc8116dff75f279b87cb5f5ee6af607034176f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113142"
---
# <a name="winhttp-sessions-overview"></a>Vue d’ensemble des sessions WinHTTP

Les services HTTP Microsoft Windows (WinHTTP) exposent un ensemble de fonctions C/C++ qui permettent à votre application d’accéder aux ressources HTTP sur le Web. Cette rubrique fournit une vue d’ensemble de la façon dont ces fonctions sont utilisées pour interagir avec un serveur HTTP.

-   [Utilisation de l’API WinHTTP pour accéder au Web](#using-the-winhttp-api-to-access-the-web)
-   [Initialisation de WinHTTP](#initializing-winhttp)
-   [Ouverture d’une demande](#opening-a-request)
-   [Ajout d’en-têtes de demande](#adding-request-headers)
-   [Envoi d’une demande](#sending-a-request)
-   [Publication des données sur le serveur](#posting-data-to-the-server)
-   [Obtention d’informations sur une demande](#getting-information-about-a-request)
-   [Téléchargement de ressources à partir du Web](#downloading-resources-from-the-web)

## <a name="using-the-winhttp-api-to-access-the-web"></a>Utilisation de l’API WinHTTP pour accéder au Web

Le diagramme suivant montre l’ordre dans lequel les fonctions WinHTTP sont généralement appelées lors de l’interaction avec un serveur HTTP. Les zones grisées représentent des fonctions qui génèrent un descripteur [HINTERNET](hinternet-handles-in-winhttp.md) , tandis que les zones simples représentent des fonctions qui utilisent ces handles.

![fonctions qui créent des handles](images/art-winhttp3.png)

## <a name="initializing-winhttp"></a>Initialisation de WinHTTP

Avant d’interagir avec un serveur, WinHTTP doit être initialisé en appelant [**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen). [**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen) crée un contexte de session pour conserver des détails sur la session http et retourne un descripteur de session. À l’aide de ce handle, la fonction [**WinHttpConnect**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpconnect) est alors en mesure de spécifier un serveur http ou HTTPS (Secure Hypertext Transfer Protocol) cible.

> [!Note]  
> Un appel à [**WinHttpConnect**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpconnect) n’entraîne pas de connexion réelle au serveur http tant qu’une demande n’est pas effectuée pour une ressource spécifique.

 

## <a name="opening-a-request"></a>Ouverture d’une demande

La fonction [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) ouvre une requête HTTP pour une ressource particulière et retourne un descripteur [HINTERNET](hinternet-handles-in-winhttp.md) qui peut être utilisé par les autres fonctions http. [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) n’envoie pas la requête au serveur lorsqu’il est appelé. La fonction [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) établit en fait une connexion sur le réseau et envoie la demande.

L’exemple suivant montre un exemple d’appel à [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) qui utilise les options par défaut.

`HINTERNET hRequest = WinHttpOpenRequest( hConnect, L"GET", NULL, NULL, NULL, NULL, 0);`

## <a name="adding-request-headers"></a>Ajout d’en-têtes de demande

La fonction [**WinHttpAddRequestHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders) permet à une application d’ajouter des en-têtes de demande de format libre supplémentaires au descripteur de requête http. Il est destiné à être utilisé par des applications sophistiquées qui requièrent un contrôle précis sur les demandes envoyées au serveur HTTP.

La fonction [**WinHttpAddRequestHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders) nécessite un handle de requête http créé par [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest), une chaîne qui contient les en-têtes, la longueur des en-têtes et les modificateurs éventuels.

Les modificateurs suivants peuvent être utilisés avec [**WinHttpAddRequestHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders).



| Modificateur                                                                                         | Description                                                                                                                                                                                                                                                                                                                                   |
|--------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ajout de l' \_ indicateur ADDREQ WinHTTP \_ \_**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders)                       | Ajoute l’en-tête s’il n’existe pas. Utilisé avec [**l' \_ indicateur ADDREQ WinHTTP \_ \_ Replace**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders).                                                                                                                                                                                                               |
| [**\_indicateur ADDREQ \_ WinHTTP \_ ajouter \_ si \_ nouveau**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders)              | Ajoute l’en-tête uniquement s’il n’existe pas déjà ; dans le cas contraire, une erreur est retournée.                                                                                                                                                                                                                                                           |
| [**ADDREQ de l' \_ \_ indicateur de \_ fusion WinHTTP**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders)                  | Fusionne les en-têtes du même nom.                                                                                                                                                                                                                                                                                                              |
| [**\_ADDREQ \_ de l’indicateur \_ de fusion WinHTTP \_ avec \_ virgule**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders)     | Fusionne les en-têtes du même nom à l’aide d’une virgule. Par exemple, l’ajout de « Accept : Text/ \* » suivi de « Accept : audio/ \* » avec cet indicateur forme l’en-tête unique « Accept : Text/ \* , audio/ \* », ce qui a pour effet de fusionner le premier en-tête. Il revient à l’application appelante de garantir un schéma cohésif en ce qui concerne les en-têtes fusionnés/séparés. |
| [**\_ADDREQ \_ de l’indicateur \_ de fusion WinHTTP \_ avec \_ point-virgule**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders) | Fusionne les en-têtes du même nom à l’aide d’un point-virgule.                                                                                                                                                                                                                                                                                            |
| [**remplacement de l' \_ indicateur ADDREQ WinHTTP \_ \_**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders)                   | Remplace ou supprime un en-tête. Si la valeur d’en-tête est vide et que l’en-tête est trouvé, elle est supprimée. Si la valeur d’en-tête n’est pas vide, la valeur d’en-tête est remplacée.                                                                                                                                                                            |



 

## <a name="sending-a-request"></a>Envoi d’une demande

La fonction [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) établit une connexion au serveur et envoie la demande au site spécifié. Cette fonction requiert un handle [HINTERNET](hinternet-handles-in-winhttp.md) créé par [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest). [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) peut également envoyer des en-têtes supplémentaires ou des informations facultatives. Les informations facultatives sont généralement utilisées pour les opérations qui écrivent des informations sur le serveur, telles que PUT et poster.

Une fois que la fonction [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) a envoyé la demande, l’application peut utiliser les fonctions [**WinHttpReadData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreaddata) et [**WinHttpQueryDataAvailable**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpquerydataavailable) sur le handle [HINTERNET](hinternet-handles-in-winhttp.md) pour télécharger les ressources du serveur.

## <a name="posting-data-to-the-server"></a>Publication des données sur le serveur

Pour la publication de données sur un serveur, le [*verbe http*](glossary.md) dans l’appel à [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) doit être de type « publication » ou « put ». Quand [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) est appelé, le paramètre *dwTotalLength* doit être défini sur la taille des données en octets. Utilisez ensuite [**WinHttpWriteData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpwritedata) pour envoyer les données sur le serveur.

Vous pouvez également définir le paramètre *lpOptional* de [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) sur l’adresse d’une mémoire tampon qui contient les données à poster sur le serveur. Lorsque vous utilisez cette technique, vous devez définir les paramètres *dwOptionalLength* et *dwTotalLength* de [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) à la taille des données publiées. L’appel de [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) de cette manière élimine la nécessité d’appeler [**WinHttpWriteData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpwritedata).

## <a name="getting-information-about-a-request"></a>Obtention d’informations sur une demande

La fonction [**WinHttpQueryHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders) permet à une application de récupérer des informations sur une requête http. La fonction requiert un handle [HINTERNET](hinternet-handles-in-winhttp.md) créé par [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest), une valeur de niveau d’information et une longueur de mémoire tampon. [**WinHttpQueryHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders) accepte également une mémoire tampon qui stocke les informations et un index d’en-tête de base zéro qui énumère plusieurs en-têtes portant le même nom.

Utilisez l’une des valeurs de niveau d’informations trouvées dans la page des indicateurs d’informations de [**requête**](query-info-flags.md) avec un modificateur pour contrôler le format dans lequel les informations sont stockées dans le paramètre *lpvBuffer* de [**WinHttpQueryHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders).

## <a name="downloading-resources-from-the-web"></a>Téléchargement de ressources à partir du Web

Après l’ouverture d’une demande avec la fonction [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) , son envoi au serveur avec [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)et la préparation du descripteur de demande pour recevoir une réponse avec [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse), l’application peut utiliser les fonctions [**WinHttpReadData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreaddata) et [**WINHTTPQUERYDATAAVAILABLE**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpquerydataavailable) pour télécharger la ressource à partir du serveur http.

L’exemple de code suivant montre comment télécharger une ressource avec la sémantique des transactions sécurisées. L’exemple de code initialise l’interface de programmation d’applications (API) WinHTTP, sélectionne un serveur HTTPs cible, puis ouvre et envoie une demande pour cette ressource sécurisée. [**WinHttpQueryDataAvailable**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpquerydataavailable) est utilisé avec le handle de demande pour déterminer la quantité de données disponibles pour le téléchargement, puis [**WinHttpReadData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreaddata) est utilisé pour lire ces données. Ce processus est répété jusqu’à ce que l’intégralité du document ait été extraite et affichée.


```C++
  DWORD dwSize = 0;
  DWORD dwDownloaded = 0;
  LPSTR pszOutBuffer;
  BOOL  bResults = FALSE;
  HINTERNET  hSession = NULL, 
             hConnect = NULL,
             hRequest = NULL;

  // Use WinHttpOpen to obtain a session handle.
  hSession = WinHttpOpen( L"WinHTTP Example/1.0",  
                          WINHTTP_ACCESS_TYPE_DEFAULT_PROXY,
                          WINHTTP_NO_PROXY_NAME, 
                          WINHTTP_NO_PROXY_BYPASS, 0 );

  // Specify an HTTP server.
  if( hSession )
    hConnect = WinHttpConnect( hSession, L"www.microsoft.com",
                               INTERNET_DEFAULT_HTTPS_PORT, 0 );

  // Create an HTTP request handle.
  if( hConnect )
    hRequest = WinHttpOpenRequest( hConnect, L"GET", NULL,
                                   NULL, WINHTTP_NO_REFERER, 
                                   WINHTTP_DEFAULT_ACCEPT_TYPES, 
                                   WINHTTP_FLAG_SECURE );

  // Send a request.
  if( hRequest )
    bResults = WinHttpSendRequest( hRequest,
                                   WINHTTP_NO_ADDITIONAL_HEADERS, 0,
                                   WINHTTP_NO_REQUEST_DATA, 0, 
                                   0, 0 );


  // End the request.
  if( bResults )
    bResults = WinHttpReceiveResponse( hRequest, NULL );

  // Keep checking for data until there is nothing left.
  if( bResults )
  {
    do 
    {
      // Check for available data.
      dwSize = 0;
      if( !WinHttpQueryDataAvailable( hRequest, &dwSize ) )
        printf( "Error %u in WinHttpQueryDataAvailable.\n",
                GetLastError( ) );

      // Allocate space for the buffer.
      pszOutBuffer = new char[dwSize+1];
      if( !pszOutBuffer )
      {
        printf( "Out of memory\n" );
        dwSize=0;
      }
      else
      {
        // Read the data.
        ZeroMemory( pszOutBuffer, dwSize+1 );

        if( !WinHttpReadData( hRequest, (LPVOID)pszOutBuffer, 
                              dwSize, &dwDownloaded ) )
          printf( "Error %u in WinHttpReadData.\n", GetLastError( ) );
        else
          printf( "%s", pszOutBuffer );

        // Free the memory allocated to the buffer.
        delete [] pszOutBuffer;
      }
    } while( dwSize > 0 );
  }


  // Report any errors.
  if( !bResults )
    printf( "Error %d has occurred.\n", GetLastError( ) );

  // Close any open handles.
  if( hRequest ) WinHttpCloseHandle( hRequest );
  if( hConnect ) WinHttpCloseHandle( hConnect );
  if( hSession ) WinHttpCloseHandle( hSession );
```



 

 



