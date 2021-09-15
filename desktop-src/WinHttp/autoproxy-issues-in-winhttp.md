---
description: Tenez compte des points importants suivants lors de l’utilisation de la fonctionnalité de proxy AutoProxy WinHTTP.
ms.assetid: 9bae89b7-8f54-42ec-a240-998c97e26d25
title: Problèmes liés au proxy AutoProxy dans WinHTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22c6edbf56ec1ffc4dfac930a5d4858429cc6447
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127531521"
---
# <a name="autoproxy-issues-in-winhttp"></a>Problèmes liés au proxy AutoProxy dans WinHTTP

Tenez compte des points importants suivants lors de l’utilisation de la fonctionnalité de proxy AutoProxy WinHTTP.

## <a name="only-one-proxy-server-is-currently-supported"></a>Un seul serveur proxy est actuellement pris en charge

WinHTTP ne prend actuellement pas en charge les configurations de proxy qui spécifient plusieurs serveurs proxy. Si [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) retourne une structure d' [**\_ \_ informations de proxy WinHTTP**](/windows/win32/api/winhttp/ns-winhttp-winhttp_proxy_info) qui contient une liste de serveurs proxy, que l’application définit ensuite sur le handle de demande à l’aide de l’option de proxy de l' **\_ option \_ WinHTTP** , WinHTTP utilise uniquement le premier serveur proxy de la liste. Si ce serveur proxy n’est pas accessible, WinHTTP n’effectue pas de basculement vers les autres serveurs proxy de la liste. Il revient à l’application de gérer ce cas en redéfinissant l’option de **\_ \_ proxy de l’option WinHTTP** avec le serveur proxy suivant dans la liste et en renvoyant la demande.

## <a name="security-risk-mitigation"></a>Atténuation des risques de sécurité

Le traitement du fichier de configuration automatique de proxy requiert l’exécution du code de script téléchargé. Voici quelques problèmes de sécurité à prendre en compte : si le serveur sur lequel réside le fichier PAC a été compromis, il est possible que le code de script PAC soit malveillant. Par conséquent, WinHTTP utilise les précautions suivantes pour protéger le client :

1.  le code de script ne peut pas instancier des objets ActiveX. Cela bloque un grand nombre de fonctionnalités potentiellement dangereuses, telles que la possibilité d’accéder à des fichiers et d’effectuer des e/s réseau.
2.  * * Windows Server 2003 : * *[**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) délègue l’intégralité du traitement WPAD à un service hors processus externe, le service de découverte automatique de Proxy Web WinHTTP, qui s’exécute sous le compte d’utilisateur intégré du service Local à faibles privilèges.

3.  **Windows XP avec SP2 et Windows Server 2003 :** Un script PAC n’est pas autorisé à s’exécuter pendant plus de 60 secondes, après quoi l’exécution du script est terminée.

4.  **Windows XP avec SP2 et Windows Server 2003 :** WinHTTP rejette les fichiers PAC d’une taille supérieure à 1 Mo. La taille d’un fichier PAC type est généralement inférieure à quelques kilo-octets.

sachez que le traitement du code de script PAC requiert l’utilisation de COM, car WinHTTP utilise le composant Microsoft JScript pour exécuter le script. Si WinHTTP ne peut pas déléguer le traitement du protocole WPAD à un service de découverte automatique de proxy Web externe hors processus, [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) charge le runtime com dans le processus d’application pour la durée de l’appel. Si l’application elle-même utilise déjà COM, cela ne devrait pas poser de problème.

## <a name="performance-considerations"></a>Considérations relatives aux performances

Le processus de détection automatique peut être lent, peut-être pendant plusieurs secondes. Les fonctions [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) et [WinHttpDetectAutoProxyConfigUrl](/windows/desktop/api/Winhttp/nf-winhttp-winhttpdetectautoproxyconfigurl) sont des fonctions de blocage et synchrones. Il peut s’agir d’un mécanisme de détection automatique particulier (tel que DHCP) qui est beaucoup plus lent que l’autre (par exemple, DNS). Si le type de détection automatique WinHTTP de type détection automatique **\_ \_ \_ \_ DHCP** et **WinHTTP \_ détecte automatiquement les \_ \_ types \_ DNS \_** , les indicateurs de détection automatique sont spécifiés, WinHTTP utilise le protocole DHCP en premier, conformément à la spécification WPAD. Si aucune URL PAC n’est détectée en émettant une requête DHCP, WinHTTP tente de localiser le fichier PAC à une adresse DNS connue.

[**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) utilise le paramètre de handle de session WinHTTP pour la mise en cache du fichier PAC et les résultats de la détection automatique. Il est préférable d’utiliser le même handle de session pour plusieurs appels **WinHttpGetProxyForUrl** , si possible, afin d’éviter la détection répétée d’URL PAC et le téléchargement de fichiers. Le fichier PAC est mis en cache en mémoire uniquement et est ignoré lorsque l’application ferme le descripteur de session.

En raison de l’impact sur les performances de la fonction de proxy, il est recommandé que seuls les applications ou les services du client de bureau utilisent la fonctionnalité. les applications basées sur le serveur doivent s’appuyer sur l’administrateur du serveur à l’aide de l’utilitaire « ProxyCfg.exe ».

 

 



