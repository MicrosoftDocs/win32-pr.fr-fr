---
description: Cette rubrique décrit les différences les plus importantes entre la version 5,1 de WinHTTP et la version 5,0.
ms.assetid: df3fcf27-3012-4818-b29c-b8a4dc409828
title: Nouveautés de WinHTTP 5,1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d63be0990b26d45cccb9677afdc8fd9b50154eb7bb2b19c47c85d7374303efb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119955729"
---
# <a name="whats-new-in-winhttp-51"></a>Nouveautés de WinHTTP 5,1

Cette rubrique décrit les différences les plus importantes entre la version 5,1 de WinHTTP et la version 5,0. La plupart de ces différences requièrent des modifications de code dans les applications qui migrent de la version 5,0 vers la version 5,1. certaines des fonctionnalités de la version 5,1 sont disponibles uniquement à partir de Windows Server 2003 et Windows XP avec Service Pack 2 (SP2), en particulier les fonctionnalités liées à l’amélioration de la sécurité du client contre les serveurs Web malveillants.

> [!IMPORTANT]
> Avec la publication de la version 5,1 de WinHTTP, le téléchargement de WinHTTP 5,0 n’est plus disponible. À compter du 1er octobre 2004, Microsoft a supprimé le téléchargement du kit de développement logiciel (SDK) WinHTTP 5,0 sur MSDN et a terminé le support technique de la version 5,0.

 

## <a name="dll-name-change"></a>Modification du nom de la DLL

Le nom de la nouvelle DLL WinHTTP 5,1 est Winhttp.dll, tandis que le nom de la DLL WinHTTP 5,0 est Winhttp5.dll.

WinHTTP 5,0 et 5,1 peuvent coexister sur le même système. WinHTTP 5,1 ne remplace pas ou ne s’installe pas sur WinHTTP 5,0.

## <a name="redistribution"></a>Redistribution

WinHTTP 5,1 est disponible uniquement avec Windows Server 2003, Windows 2000 Professional avec service pack 3 (SP3), Windows XP avec service pack 1 (SP1) et les systèmes d’exploitation ultérieurs. Un fichier de module de fusion (. msm) redistribuable n’est pas disponible pour WinHTTP 5,1.

## <a name="winhttprequest-progid"></a>ProgID WinHttpRequest

L’identificateur de programme (ProgID) du composant WinHttpRequest est passé de « WinHttp. WinHttpRequest. 5 » à « WinHttp. WinHttpRequest. 5.1 ». Le CLSID de la classe [**WinHttpRequest**](winhttprequest.md) a également changé.

## <a name="async-callback-behavior-change"></a>Modification du comportement de rappel asynchrone

Lors de l’appel des fonctions [**WinHttpWriteData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpwritedata), [**WinHttpQueryDataAvailable**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpquerydataavailable) et [**WinHttpReadData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreaddata) en mode asynchrone, ne comptez pas sur les paramètres *lpdwNumberOfBytesWritten*, *lpdwNumberOfBytesAvailable* et *lpdwNumberOfBytesRead* out respectifs à définir. Si l’appel de fonction se termine de façon asynchrone, WinHTTP n’écrit pas sur ces pointeurs fournis par le code d’application. Au lieu de cela, l’application doit récupérer ces valeurs à l’aide des paramètres *lpvStatusInformation* et *dwStatusInformationLength* à la fonction de rappel.

## <a name="changes-to-default-settings"></a>modifications apportées aux Paramètres par défaut

Les modifications apportées aux paramètres par défaut sont les suivantes :

-   La vérification du certificat de serveur SSL est activée par défaut dans WinHTTP 5,1. WinHTTP 5,0 ne gère pas les échecs rencontrés lors de la validation du certificat de serveur comme des erreurs irrécupérables ; elles sont signalées à l’application à l’aide d’une notification de rappel d' **\_ échec sécurisé** , mais n’entraîne pas l’abandon de la requête. WinHTTP 5,1, sinon, gère les échecs de validation de certificat de serveur comme des erreurs irrécupérables qui abandonnent la demande. L’application peut demander à WinHTTP d’ignorer un petit sous-ensemble d’erreurs de certificat, telles qu’une autorité de certification inconnue, une date de certificat non valide/expirée ou un nom d’objet de certificat non valide, à l’aide de l’option des indicateurs de sécurité de l' **\_ option \_ \_ WinHTTP** .
-   La prise en charge de l’authentification Passport est désactivée par défaut dans WinHTTP 5,1. La prise en charge de Passport peut être activée avec l’option **WinHTTP \_ configurer l' \_ \_ \_ authentification Passport** . La recherche automatique des informations d’identification Passport dans le porte-clés est également désactivée par défaut.
-   Changement de comportement de redirection : les redirections HTTP d’une URL sécurisée **https** vers une URL **http** standard ne sont plus suivies automatiquement par défaut pour des raisons de sécurité. Il existe une nouvelle option, **la \_ \_ \_ stratégie de redirection des options WinHTTP**, pour remplacer le comportement de redirection par défaut dans WinHTTP 5,1. Avec le composant COM **WinHttpRequest** , utilisez l’option New **WinHttpRequestOption \_ EnableHttpsToHttpRedirects** pour activer les redirections à partir de https : vers https : URL.
-   Lorsqu’un fichier de trace WinHTTP est créé, l’accès est limité à une liste de contrôle d’accès, de sorte que seuls les administrateurs peuvent lire ou écrire le fichier. Le compte d’utilisateur sous lequel le tracefile a été créé peut également modifier la liste de contrôle d’accès pour accorder l’accès aux autres utilisateurs. Cette protection est disponible uniquement sur les systèmes de fichiers qui prennent en charge la sécurité. autrement dit, NTFS, et non FAT32).
-   à compter de Windows Server 2003 et Windows XP avec SP2, l’envoi de demandes aux ports connus, non HTTP et connus suivants est limité pour des raisons de sécurité : 21 (FTP), 25 (SMTP), 70 (GOPHER), 110 (POP3), 119 (NNTP), 143 (IMAP).
-   à compter de Windows Server 2003 et Windows XP avec SP2, la quantité maximale de données d’en-tête que WinHTTP accepte dans une réponse HTTP est de 64 ko par défaut. Si la réponse HTTP du serveur contient plus de 64 Ko de données d’en-tête totales, WinHTTP échoue à la demande avec une erreur WinHTTP erreur de **\_ \_ \_ \_ réponse du serveur non valide** . Cette limite de 64 Ko peut être remplacée à l’aide de l’option **\_ \_ taille maximale d' \_ \_ en-tête \_ de réponse de l’option WinHTTP** .

## <a name="ipv6-support"></a>Prise en charge D’ipv6

WinHTTP 5,1 ajoute la prise en charge du protocole IPv6 (Internet Protocol version 6). winhttp peut envoyer des requêtes HTTP à un serveur dont le nom DNS est résolu en une adresse IPv6, et à partir de Windows server 2003 et Windows XP avec SP2, winhttp prend également en charge les adresses littérales ipv6.

## <a name="new-options-in-the-cc-api-for-winhttp"></a>Nouvelles options de l’API C/C++ pour WinHTTP

WinHTTP 5,1 implémente les nouvelles options suivantes :

<dl> « \# définir l' \_ option \_ WinHTTP \_ déconnecter Passport \_ 86 »  
« \# définir l' \_ option \_ WinHTTP \_ URL de retour Passport \_ 87 »  
« \# définir \_ la stratégie de redirection de l’OPTION WinHTTP \_ \_ 88 »  
</dl>

à compter de Windows Server 2003 et Windows XP avec SP2, WinHTTP 5,1 implémente les nouvelles options suivantes. sur Windows 2000 Professional avec SP3 ou Windows XP avec SP1, toutefois, les appels à [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) ou [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) avec ces id d’option échouent :

<dl> « \# définir l' \_ option WinHTTP \_ recevoir le \_ \_ délai d’expiration de la réponse 7 »  
« \# définir l' \_ option WinHTTP \_ nombre maximal de \_ \_ \_ redirections automatiques http 89 »  
« \# définir l' \_ option WinHTTP \_ Max \_ HTTP \_ Status \_ continue 90 »  
« \# définir l' \_ option \_ WinHTTP \_ \_ -taille maximale d’en-tête de réponse \_ 91 »  
« \# définir l' \_ option WinHTTP \_ taille maximale de drainage de la \_ réponse \_ \_ 92 »  
</dl>

## <a name="new-options-in-the-winhttprequest-51-component"></a>Nouvelles options dans le composant WinHttpRequest 5,1

Le composant WinHttpRequest 5,1 implémente les nouvelles options suivantes :

<dl> « WinHttpRequestOption \_ RevertImpersonationOverSsl »  
« WinHttpRequestOption \_ EnableHttpsToHttpRedirects »  
« WinHttpRequestOption \_ EnablePassportAuthentication »  
</dl>

les nouvelles options WinHttpRequest 5,1 suivantes sont disponibles à partir de Windows Server 2003 et Windows XP avec SP2 :

<dl> « WinHttpRequestOption \_ MaxAutomaticRedirects »  
« WinHttpRequestOption \_ MaxResponseHeaderSize »  
« WinHttpRequestOption \_ MaxResponseDrainSize »  
« WinHttpRequestOptions \_ EnableHttp1 \_ 1 »  
</dl>

## <a name="proxies-are-not-trusted-when-auto-logon-security-is-set-to-high"></a>Les proxies ne sont pas approuvés lorsque la sécurité d’ouverture de session automatique est définie sur élevée

Dans WinHTTP 5,0, les serveurs proxy sont toujours approuvés pour la connexion automatique. cette valeur n’est plus valide pour WinHTTP 5,1 s’exécutant sur Windows Server 2003 et Windows XP avec SP2 lorsque l’option de stratégie niveau de sécurité d’ouverture de session automatique WinHTTP est définie. **\_ \_ \_ \_**

## <a name="web-proxy-auto-discovery-autoproxy-api"></a>API de détection automatique de proxy Web (AutoProxy)

Pour faciliter la configuration des paramètres de proxy pour les applications basées sur WinHTTP, WinHTTP implémente désormais le protocole WPAD (Web Proxy Auto-Discovery), également appelé « *proxy* automatique ». Il s’agit du même protocole que celui utilisé par les navigateurs Web, tels qu’Internet Explorer, pour détecter automatiquement la configuration du proxy sans obliger l’utilisateur final à spécifier un serveur proxy manuellement. Pour prendre en charge le proxy AutoProxy, WinHTTP 5,1 implémente une nouvelle fonction C/C++, [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl), ainsi que deux fonctions de prise en charge, [**WinHttpDetectAutoProxyConfigUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpdetectautoproxyconfigurl) et [**WinHttpGetIEProxyConfigForCurrentUser**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetieproxyconfigforcurrentuser).

## <a name="known-issues"></a>Problèmes connus

les problèmes suivants sont connus pour exister dans WinHTTP 5,1 sur Windows 2000 Professional avec SP3 et Windows XP avec SP1. ces problèmes sont résolus pour WinHTTP à partir de Windows Server 2003 et Windows XP avec SP2 :

-   Si l’application utilise la fonction [**WinHttpSetTimeouts**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsettimeouts) ou la méthode [**SetTimeouts**](iwinhttprequest-settimeouts.md) sur le composant [**WinHttpRequest**](iwinhttprequest-interface.md) pour définir un délai d’expiration de résolution DNS non infini, tel que le paramètre *dwResolveTimeout* , une fuite de handle de thread se produit chaque fois que WinHTTP résout un nom DNS. Sur un grand nombre de requêtes HTTP, cela entraîne une fuite de mémoire importante. La solution de contournement consiste à conserver le paramètre de délai de résolution infini par défaut comme étant inchangé (une valeur de 0 spécifie un délai d’expiration infini). Cela est fortement recommandé dans tous les cas, car la prise en charge des délais d’attente sur les résolutions de noms DNS dans WinHTTP est coûteuse en termes de performances. pour Windows 2000 et versions ultérieures, la définition d’un délai de résolution DNS dans WinHTTP est inutile, car le service client DNS sous-jacent implémente son propre délai de résolution.
-   Lors du traitement de requêtes asynchrones, WinHTTP ne gère pas correctement l’emprunt d’identité de thread. Cela entraîne l’échec des demandes qui requièrent l’authentification NTLM/Negotiate, sauf si les informations d’identification sont fournies explicitement à l’aide des fonctions [**WinHttpSetCredentials**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials) ou [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) .

 

 



