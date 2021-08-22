---
description: Microsoft Windows HTTP Services (WinHTTP) est destiné aux applications de serveur principal et de niveau intermédiaire qui requièrent l’accès à une pile client HTTP.
ms.assetid: 5b0cf321-8f69-4526-a628-e6ca0f9d4a58
title: Portage d’applications WinINet vers WinHTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b111cd79e7ce7edfb09d43993ee2735ce09275f51c58bcfad319fb073dccc5b7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119052007"
---
# <a name="porting-wininet-applications-to-winhttp"></a>Portage d’applications WinINet vers WinHTTP

Microsoft Windows HTTP Services (WinHTTP) est destiné aux applications de serveur principal et de niveau intermédiaire qui requièrent l’accès à une pile client HTTP. [Microsoft Windows Internet (WinINet)](winhttp-start-page.md) fournit une pile client HTTP pour les applications clientes, ainsi que l’accès aux protocoles protocole FTP (FTP), SOCKSv4 et Gopher. Cette vue d’ensemble peut vous aider à déterminer si le portage de vos applications WinINet vers WinHTTP est bénéfique. Elle décrit également les exigences de conversion spécifiques.

-   [Éléments à prendre en compte avant de porter votre application WinINet](#things-to-consider-before-porting-your-wininet-application)
-   [Équivalents WinHTTP des fonctions WinINet](#winhttp-equivalents-to-wininet-functions)
-   [Gestion différente des requêtes asynchrones](#different-handling-of-asynchronous-requests)
-   [Différences dans les notifications de rappel WinHTTP](#differences-in-winhttp-callback-notifications)
-   [Différences d’authentification](#authentication-differences)
-   [Différences dans les transactions HTTP sécurisées](#differences-in-secure-http-transactions)

## <a name="things-to-consider-before-porting-your-wininet-application"></a>Éléments à prendre en compte avant de porter votre application WinINet

Envisagez de porter votre application WinINet sur WinHTTP si votre application peut tirer parti des éléments suivants :

-   Pile client HTTP sécurisée pour le serveur.
-   Utilisation réduite de la pile.
-   Extensibilité d’une application serveur.
-   Moins de dépendances sur les API liées à la plateforme.
-   Prise en charge de l’emprunt d’identité de thread.
-   Pile HTTP conviviale pour le service.
-   Accès à l’objet [**WinHttpRequest**](winhttprequest.md) scriptable.

N’envisagez pas de porter votre application WinINet sur WinHTTP si elle doit prendre en charge un ou plusieurs des éléments suivants :

-   Protocole FTP ou Gopher de la pile HTTP.
-   Prise en charge du protocole SOCKSv4 pour la communication avec les proxies SOCKS.
-   Services d’accès à distance automatiques.

Si vous décidez de déplacer votre application vers WinHTTP, les sections suivantes vous guident tout au long du processus de conversion.

Pour obtenir un exemple d’application pour WinINet et WinHTTP, comparez l’exemple AsyncDemo pour WinINet avec l’exemple AsyncDemo pour WinHTTP.

## <a name="winhttp-equivalents-to-wininet-functions"></a>Équivalents WinHTTP des fonctions WinINet

Le tableau suivant répertorie les fonctions WinINet associées à la pile cliente HTTP avec les équivalents WinHTTP.

Si votre application requiert des fonctions WinINet qui ne sont pas répertoriées, ne portez pas votre application vers WinHTTP.



| Fonction WinINet                                                       | Équivalent WinHTTP                                                                                                                                                                                     | Modifications notables                                                                                                                                                                                                                                                                                                                      |
|------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**HttpAddRequestHeaders**](/windows/desktop/api/wininet/nf-wininet-httpaddrequestheadersa)             | [**WinHttpAddRequestHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders)                                                                                                                                           | Aucun.                                                                                                                                                                                                                                                                                                                                |
| [**HttpEndRequest**](/windows/desktop/api/wininet/nf-wininet-httpendrequesta)                           | [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse)                                                                                                                                               | La valeur de contexte est définie avec [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) ou [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption). Les options de requête sont définies avec [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest). [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) doit être appelé après l’envoi d’une demande.                      |
| [**HttpOpenRequest**](/windows/desktop/api/wininet/nf-wininet-httpopenrequesta)                         | [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest)                                                                                                                                                       | La valeur de contexte est définie avec [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) ou [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption).                                                                                                                                                                                                      |
| [**HttpQueryInfo**](/windows/desktop/api/wininet/nf-wininet-httpqueryinfoa)                             | [**WinHttpQueryHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders)                                                                                                                                                     | Aucun.                                                                                                                                                                                                                                                                                                                                |
| [**HttpSendRequest**](/windows/desktop/api/wininet/nf-wininet-httpsendrequesta)                         | [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)                                                                                                                                                       | La valeur de contexte peut être définie avec [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest).                                                                                                                                                                                                                                                  |
| [**HttpSendRequestEx**](/windows/desktop/api/wininet/nf-wininet-httpsendrequestexa)                     | [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)                                                                                                                                                       | Les mémoires tampons ne peuvent pas être fournies.                                                                                                                                                                                                                                                                                                          |
| [**InternetCanonicalizeUrl**](/windows/desktop/api/wininet/nf-wininet-internetcanonicalizeurla)         | Pas d'équivalent                                                                                                                                                                                          | Les URL sont désormais sous forme canonique dans [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest).                                                                                                                                                                                                                                              |
| [**InternetCheckConnection**](/windows/desktop/api/wininet/nf-wininet-internetcheckconnectiona)         | Pas d'équivalent                                                                                                                                                                                          | Non implémenté dans WinHTTP.                                                                                                                                                                                                                                                                                                          |
| [**InternetCloseHandle**](/windows/desktop/api/wininet/nf-wininet-internetclosehandle)                 | [**WinHttpCloseHandle**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpclosehandle)                                                                                                                                                       | La fermeture d’un handle parent dans WinHTTP ne ferme pas de manière récursive les handles enfants.                                                                                                                                                                                                                                                         |
| [**InternetCombineUrl**](/windows/desktop/api/wininet/nf-wininet-internetcombineurla)                   | Pas d'équivalent                                                                                                                                                                                          | Les URL peuvent être assemblées avec la fonction [**WinHttpCreateUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcreateurl) .                                                                                                                                                                                                                                                |
| [**InternetConfirmZoneCrossing**](/windows/desktop/api/wininet/nf-wininet-internetconfirmzonecrossing) | Pas d'équivalent                                                                                                                                                                                          | Non implémenté dans WinHTTP.                                                                                                                                                                                                                                                                                                          |
| [**InternetConnect**](/windows/desktop/api/wininet/nf-wininet-internetconnecta)                         | [**WinHttpConnect**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpconnect)                                                                                                                                                               | La valeur de contexte est définie avec [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) ou [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption). Les options de requête sont définies avec [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest). Les informations d’identification de l’utilisateur sont définies avec [**WinHttpSetCredentials**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials).                                 |
| [**InternetCrackUrl**](/windows/desktop/api/wininet/nf-wininet-internetcrackurla)                       | [**WinHttpCrackUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl)                                                                                                                                                             | Comportement opposé de l' \_ indicateur d’échappement ICU : avec [**InternetCrackUrl**](/windows/desktop/api/wininet/nf-wininet-internetcrackurla), cet indicateur entraîne la conversion des séquences d’échappement (% XX) en caractères, mais avec [**WinHttpCrackUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl), les caractères qui doivent être échappés de dans une requête HTTP sont convertis en séquences d’échappement. |
| [**InternetCreateUrl**](/windows/desktop/api/wininet/nf-wininet-internetcreateurla)                     | [**WinHttpCreateUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcreateurl)                                                                                                                                                           | Aucun.                                                                                                                                                                                                                                                                                                                                |
| [**InternetErrorDlg**](/windows/desktop/api/wininet/nf-wininet-interneterrordlg)                       | Pas d'équivalent                                                                                                                                                                                          | Comme WinHTTP est destiné aux applications côté serveur, il n’implémente pas d’interface utilisateur.                                                                                                                                                                                                                                   |
| [**InternetGetCookie**](/windows/desktop/api/wininet/nf-wininet-internetgetcookiea)                     | Pas d'équivalent                                                                                                                                                                                          | WinHTTP ne rend pas les données persistantes entre les sessions et ne peut pas accéder aux cookies WinINet.                                                                                                                                                                                                                                                    |
| [**InternetOpen**](/windows/desktop/api/wininet/nf-wininet-internetopena)                               | [**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen)                                                                                                                                                                     | Aucun.                                                                                                                                                                                                                                                                                                                                |
| [**InternetOpenUrl**](/windows/desktop/api/wininet/nf-wininet-internetopenurla)                         | [**WinHttpConnect**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpconnect), [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest), [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest), [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) | Cette fonctionnalité est disponible dans les fonctions WinHTTP listées.                                                                                                                                                                                                                                                                     |
| [**InternetQueryDataAvailable**](/windows/desktop/api/wininet/nf-wininet-internetquerydataavailable)   | [**WinHttpQueryDataAvailable**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpquerydataavailable)                                                                                                                                         | Aucun paramètre réservé.                                                                                                                                                                                                                                                                                                              |
| [**InternetQueryOption**](/windows/desktop/api/wininet/nf-wininet-internetqueryoptiona)                 | [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption)                                                                                                                                                       | WinHTTP offre un ensemble d’options différent de WinINet. Pour plus d’informations et d’options proposées par WinHTTP, consultez [**indicateurs d’option**](option-flags.md).                                                                                                                                                                               |
| [**InternetReadFile**](/windows/desktop/api/wininet/nf-wininet-internetreadfile)                       | [**WinHttpReadData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreaddata)                                                                                                                                                             | Aucun.                                                                                                                                                                                                                                                                                                                                |
| [**InternetReadFileEx**](/windows/desktop/api/wininet/nf-wininet-internetreadfileexa)                   | [**WinHttpReadData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreaddata)                                                                                                                                                             | Au lieu d’une structure, la mémoire tampon est une région de mémoire traitée avec un pointeur.                                                                                                                                                                                                                                                  |
| [**InternetSetOption**](/windows/desktop/api/wininet/nf-wininet-internetsetoptiona)                     | [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption)                                                                                                                                                           | Aucun.                                                                                                                                                                                                                                                                                                                                |
| [**InternetSetStatusCallback**](/windows/desktop/api/wininet/nf-wininet-internetsetstatuscallback)     | [**WinHttpSetStatusCallback**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetstatuscallback)                                                                                                                                           | Pour plus d’informations, consultez « Gestion différente des requêtes asynchrones » dans cette rubrique.                                                                                                                                                                                                                                               |
| [**InternetTimeFromSystemTime**](/windows/desktop/api/wininet/nf-wininet-internettimefromsystemtime)   | [**WinHttpTimeFromSystemTime**](/windows/desktop/api/Winhttp/nf-winhttp-winhttptimefromsystemtime)                                                                                                                                         | Aucun.                                                                                                                                                                                                                                                                                                                                |
| [**InternetTimeToSystemTime**](/windows/desktop/api/wininet/nf-wininet-internettimetosystemtime)       | [**WinHttpTimeToSystemTime**](/windows/desktop/api/Winhttp/nf-winhttp-winhttptimetosystemtime)                                                                                                                                             | Aucun.                                                                                                                                                                                                                                                                                                                                |
| [**InternetWriteFile**](/windows/desktop/api/wininet/nf-wininet-internetwritefile)                     | [**WinHttpWriteData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpwritedata)                                                                                                                                                           | Aucun.                                                                                                                                                                                                                                                                                                                                |



 

## <a name="different-handling-of-asynchronous-requests"></a>Gestion différente des requêtes asynchrones

Sachez que dans WinINet et WinHTTP, certaines fonctions peuvent effectuer des requêtes asynchrones de manière synchrone ou asynchrone. Votre application doit gérer l’une ou l’autre des situations. Il existe des différences significatives dans la façon dont WinINet et WinHTTP gèrent ces fonctions potentiellement asynchrones.

WinINet

-   Achèvement synchrone : si un appel de fonction WinINet potentiellement asynchrone se termine de façon synchrone, les paramètres de sortie de la fonction retournent les résultats de l’opération. Lorsqu’une erreur se produit, récupérez le code d’erreur en appelant [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) après l’appel de la fonction wininet.

-   Achèvement asynchrone : si un appel de fonction potentiellement asynchrone se termine de façon asynchrone, les résultats de l’opération et toutes les erreurs sont accessibles dans la fonction de rappel. La fonction de rappel est exécutée sur un thread de travail, et non sur le thread qui a effectué l’appel de fonction initial.

En d’autres termes, votre application doit dupliquer la logique pour gérer les résultats de ces opérations à deux emplacements : immédiatement après l’appel de fonction et dans la fonction de rappel.

WinHTTP simplifie ce modèle en vous permettant d’implémenter la logique opérationnelle uniquement dans la fonction de rappel, qui reçoit une notification d’achèvement indépendamment du fait que l’opération s’est terminée de façon synchrone ou asynchrone. Lorsque l’opération asynchrone est activée, les paramètres de sortie des fonctions WinHTTP ne retournent pas de données significatives et doivent avoir la valeur **null**.

La seule différence significative entre l’achèvement asynchrone et synchrone dans WinHTTP, du point de vue de l’application, réside dans l’emplacement d’exécution de la fonction de rappel.

WinHTTP

-   Achèvement synchrone : quand une opération se termine de façon synchrone, les résultats sont retournés dans une fonction de rappel qui s’exécute dans le même thread que l’appel de fonction d’origine.

-   Achèvement asynchrone : quand une opération se termine de façon asynchrone, les résultats sont retournés dans une fonction de rappel qui s’exécute dans un thread de travail.

Même si la plupart des erreurs peuvent également être gérées entièrement dans la fonction de rappel, les applications WinHTTP doivent toujours être préparées pour qu’une fonction retourne la **valeur false** en raison d’une erreur de \_ paramètre non valide ou d’une \_ autre erreur similaire récupérée par l’appel de [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).

Contrairement à WinINet, qui peut exécuter plusieurs opérations asynchrones simultanément, WinHTTP applique une stratégie d’une opération asynchrone en attente par handle de demande. Si une opération est en attente et qu’une autre fonction WinHTTP est appelée, la deuxième fonction échoue et [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retourne une erreur d' \_ opération non valide \_ .

WinHTTP simplifie ce modèle en vous permettant d’implémenter la logique opérationnelle uniquement dans la fonction de rappel, qui reçoit une notification d’achèvement indépendamment du fait que l’opération s’est terminée de façon synchrone ou asynchrone. Lorsque l’opération asynchrone est activée, les paramètres de sortie des fonctions WinHTTP ne retournent pas de données significatives et doivent avoir la valeur **null**.

## <a name="differences-in-winhttp-callback-notifications"></a>Différences dans les notifications de rappel WinHTTP

La fonction de rappel d’État reçoit des mises à jour sur l’état des opérations via des indicateurs de notification. Dans WinHTTP, les notifications sont sélectionnées à l’aide du paramètre *dwNotificationFlags* de la fonction [**WinHttpSetStatusCallback**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetstatuscallback) . Utilisez l’indicateur de **\_ rappel de \_ \_ tous les \_ notifications WinHTTP** pour être informé de toutes les mises à jour d’État.

Les notifications indiquant qu’une opération particulière est terminée sont appelées notifications de fin d’exécution ou simplement saisies semi-automatiques. Dans WinINet, chaque fois que la fonction de rappel reçoit une achèvement, le paramètre *lpvStatusInformation* contient une structure de [**\_ \_ Résultat asynchrone Internet**](/windows/desktop/api/wininet/ns-wininet-internet_async_result) . Dans WinHTTP, cette structure n’est pas disponible pour toutes les saisies semi-automatiques. Il est important de consulter la page de référence pour le [**\_ \_ rappel d’État WinHTTP**](/windows/win32/api/winhttp/nc-winhttp-winhttp_status_callback), qui contient des informations sur les notifications et sur le type de données attendu pour chacune d’elles.

Dans WinHTTP, une seule et même **\_ erreur de \_ \_ demande d' \_ État de rappel WinHTTP** indique qu’une opération a échoué. Toutes les autres saisies semi-automatiques indiquent une opération réussie.

WinINet et WinHTTP utilisent tous deux une valeur de contexte définie par l’utilisateur pour passer des informations du thread principal à la fonction de rappel d’État, qui peut être exécutée sur un thread de travail. Dans WinINet, la valeur de contexte utilisée par la fonction de rappel d’État est définie en appelant l’une des différentes fonctions. Dans WinHTTP, la valeur de contexte est définie uniquement avec [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) ou [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption). Pour cette raison, il est possible dans WinHTTP d’avoir une notification qui se produit avant qu’une valeur de contexte soit définie. Si la fonction de rappel reçoit une notification avant que la valeur de contexte ne soit définie, l’application doit être préparée à recevoir la valeur **null** dans le paramètre *dwContext* de la fonction de rappel.

## <a name="authentication-differences"></a>Différences d’authentification

Dans WinINet, les informations d’identification de l’utilisateur sont définies en appelant la fonction [**InternetSetOption**](/windows/desktop/api/wininet/nf-wininet-internetsetoptiona) , à l’aide d’un code similaire à celui fourni dans l’exemple de code suivant.

``` syntax
// Use the WinINet InternetSetOption function to set the 
// user credentials to the user name contained in strUsername 
// and the password to the contents of strPassword.
       
InternetSetOption( hRequest, INTERNET_OPTION_PROXY_USERNAME, 
                   strUsername, strlen(strUsername) + 1 );

InternetSetOption( hRequest, INTERNET_OPTION_PROXY_PASSWORD, 
                   strPassword, strlen(strPassword) + 1 );
```

Pour des raisons de compatibilité, les informations d’identification de l’utilisateur peuvent être définies de la même manière dans WinHTTP à l’aide de la fonction [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) , mais cela n’est pas recommandé, car il peut présenter une faille de sécurité.

Au lieu de cela, quand une application reçoit un code d’état 401 dans WinHTTP, la méthode recommandée pour définir les informations d’identification est d’abord d’identifier un schéma d’authentification à l’aide de [**WinHttpQueryAuthSchemes**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryauthschemes) et, deuxièmement, de définir les informations d’identification à l’aide de [**WinHttpSetCredentials**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials). L’exemple de code suivant montre comment procéder.

``` syntax
DWORD dwSupportedSchemes;
DWORD dwPrefered;
DWORD dwTarget;

// Obtain the supported and first schemes.
WinHttpQueryAuthSchemes( hRequest, &dwSupportedSchemes, &dwPrefered, &dwTarget );

// Set the credentials before resending the request.
WinHttpSetCredentials( hRequest, dwTarget, dwPrefered, strUsername, strPassword, NULL );
```

Étant donné qu’il n’y a pas d’équivalent à [**InternetErrorDlg**](/windows/desktop/api/wininet/nf-wininet-interneterrordlg) dans WinHTTP, les applications qui obtiennent des informations d’identification via une interface utilisateur doivent fournir leur propre interface.

Contrairement à WinINet, WinHTTP ne met pas en cache les mots de passe. Les informations d’identification de l’utilisateur valides doivent être fournies pour chaque demande.

WinHTTP ne prend pas en charge le schéma d’authentification de mot de passe distribué (DPA) pris en charge par WinINet. Par contre, WinHTTP prend en charge Microsoft Passport 1,4. Pour plus d’informations sur l’utilisation de l’authentification Passport dans WinHTTP, consultez [authentification Passport dans WinHTTP](passport-authentication-in-winhttp.md).

WinHTTP ne repose pas sur les paramètres d’Internet Explorer pour déterminer la stratégie d’ouverture de session automatique. Au lieu de cela, la stratégie de connexion automatique est définie avec [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption). Pour plus d’informations sur l’authentification dans WinHTTP, y compris la stratégie de connexion automatique, consultez [authentification dans WinHTTP](authentication-in-winhttp.md).

## <a name="differences-in-secure-http-transactions"></a>Différences dans les transactions HTTP sécurisées

Dans WinINet, lancez une session sécurisée à l’aide de [**HttpOpenRequest**](/windows/desktop/api/wininet/nf-wininet-httpopenrequesta) ou [**internetconnect**](/windows/desktop/api/wininet/nf-wininet-internetconnecta), mais dans WinHTTP, vous devez appeler [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) à l’aide de l’indicateur de **\_ \_ sécurité d’indicateur WinHTTP** .

Dans une transaction HTTP sécurisée, les certificats de serveur peuvent être utilisés pour authentifier un serveur auprès du client. Dans WinINet, si un certificat de serveur contient des erreurs, [**HTTPSendRequest**](/windows/desktop/api/wininet/nf-wininet-httpsendrequesta) échoue et fournit des détails sur les erreurs de certificat.

Dans WinHttp, les erreurs de certificat de serveur sont gérées en fonction de la version, comme suit :

-   À partir de WinHttp 5,1, si un certificat de serveur échoue ou contient des erreurs, l’appel à [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) signale un **\_ \_ \_ \_ échec sécurisé de l’état du rappel WinHTTP** dans la fonction de rappel. Si l’erreur générée par **WinHttpSendRequest** est ignorée, les appels suivants à [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) échouent avec une erreur de l' \_ \_ opération WinHTTP \_ annulée.
-   Dans WinHTTP 5,0, les erreurs dans les certificats de serveur n’entraînent pas, par défaut, l’échec d’une demande. Au lieu de cela, les erreurs sont signalées dans la fonction de rappel avec la notification d' **\_ \_ \_ \_ échec sécurisé de l’état de rappel WinHTTP** .

sur certaines plateformes antérieures, WinINet prenait en charge les protocoles PCT (Private Communication Technology) et/ou Fortezza, bien qu’ils ne soient pas sur Windows XP.

WinHTTP ne prend pas en charge les protocoles PCT et Fortezza sur les plateformes, et s’appuie plutôt sur SSL (Secure Sockets Layer) (SSL) 2,0, SSL 3,0 ou TLS (Transport Layer Security) 1,0.

 

 
