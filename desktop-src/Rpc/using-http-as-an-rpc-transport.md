---
title: Utilisation de HTTP comme transport RPC
description: RPC sur HTTP permet aux programmes clients d’utiliser Internet pour exécuter des procédures fournies par les programmes serveur sur des réseaux distants.
ms.assetid: b5062d70-7625-4a9f-a8c1-025ef8342fcb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8775aab1771dcc6da9cade97d36c7141d6d66d8bc8172a20c8263ef64b8ed7ce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119010781"
---
# <a name="using-http-as-an-rpc-transport"></a>Utilisation de HTTP comme transport RPC

RPC sur HTTP permet aux programmes clients d’utiliser Internet pour exécuter des procédures fournies par les programmes serveur sur des réseaux distants. RPC sur HTTP tunnele ses appels via un port HTTP établi. Par conséquent, ses appels peuvent traverser des pare-feu réseau sur les réseaux client et serveur.

RPC sur HTTP achemine ses appels vers le proxy RPC situé sur le réseau du serveur RPC. Le proxy RPC établit et maintient une connexion au serveur RPC. Il sert de proxy, en rétribuant les appels de procédure distante au serveur RPC et en renvoyant les réponses du serveur sur Internet à l’application cliente. Ce processus est illustré dans le diagramme suivant.

![interaction entre un serveur RPC et Internet Information Server pour RPC http](images/httprpc1.png)

Le diagramme montre un pare-feu sur le réseau de l’application cliente. Cela n’est pas nécessaire pour que RPC sur HTTP fonctionne. Toutefois, si le réseau client dispose d’un pare-feu, il aura également besoin d’un programme serveur proxy tel que Microsoft Proxy Server.

Lorsque le programme client émet un appel de procédure distante en utilisant le protocole HTTP comme transport, la bibliothèque Runtime RPC sur le client contacte le proxy RPC. Selon que le client RPC a été invité à utiliser HTTP ou HTTPs (HTTP avec SSL), le port 80 ou le port 443 est utilisé, respectivement. Le proxy RPC contacte le programme serveur RPC et établit une connexion TCP/IP. Le client et le proxy RPC maintiennent leur connexion HTTP ou HTTPs sur Internet. La connexion HTTP ou HTTPs du client au proxy RPC peut traverser un pare-feu (sous réserve d’autorisations d’accès appropriées), le cas échéant. Le serveur peut ensuite exécuter l’appel de procédure distante et utiliser la connexion via le proxy RPC pour répondre au client. Le proxy RPC est une extension ISAPI qui s’exécute dans le contexte d’IIS.

Si le client ou le serveur se déconnecte pour une raison quelconque, le proxy RPC le détecte et met fin à la session RPC. Tant que la session continue, le proxy RPC conserve ses connexions au client et au serveur. Il transmet les appels de procédure distante du client au serveur et envoie les réponses du serveur au client.

Le programme client RPC peut acheminer ses appels RPC via Internet en créant une liaison de chaîne au format suivant :

``` syntax
[object_uuid@]ncacn_http:rpc_server[endpoint,HttpProxy=proxy_server:http_port,RpcProxy=rpc_proxy:rpc_port,HttpConnectionOption=UseHttpProxy]
```

Où :

-   *\_ UUID* de l’objet spécifie un UUID d’objet RPC. Pour plus d’informations, consultez [génération d’UUID d’interface](generating-interface-uuids.md) et de [chaîne UUID](string-uuid.md).
-   **ncacn \_ http** sélectionne la spécification de séquence de protocole pour RPC sur http. Pour plus d’informations, consultez [constantes de séquence de protocole](protocol-sequence-constants.md) et liaison de [chaîne](string-binding.md).
-   *le \_ serveur RPC* est l’adresse réseau de l’ordinateur qui exécute le processus serveur RPC. L’adresse du serveur doit être spécifiée dans un formulaire visible et compréhensible par l’ordinateur proxy RPC, et non par le client. Étant donné que le client ne se connecte pas directement au serveur, il n’a pas besoin d’être en mesure de résoudre le nom du serveur ou d’établir une connexion à celui-ci. Le proxy RPC établit la connexion au nom du client et, par conséquent, le *\_ serveur RPC* doit être un nom reconnu par le proxy RPC.
-   *point de terminaison* spécifie le port TCP/IP que le processus serveur RPC écoute pour les appels de procédure distante. Pour plus d’informations, consultez [recherche de points de terminaison](finding-endpoints.md).
-   **Httpproxy** spécifie éventuellement un serveur proxy http sur le réseau du client RPC, tel que Microsoft Proxy Server. Si un serveur proxy est sélectionné, aucun numéro de port n’est spécifié, le stub RPC utilise le port 80 par défaut si le protocole SSL n’est pas demandé, et le port 443 si le protocole SSL est spécifié.
-   **RpcProxy** spécifie l’adresse et le numéro de port de l’ordinateur IIS qui joue le rôle de proxy pour le serveur RPC. Vous ne devez spécifier cette valeur que si le processus du serveur RPC réside sur un autre ordinateur que le proxy RPC. Si vous ne spécifiez pas de numéro de port, le stub client RPC utilise par défaut le port 80 si le protocole SSL n’est pas spécifié et utilise le port 443 si le protocole SSL (HTTPs) est spécifié.
-   **HttpConnectionOption** vous permet éventuellement de diriger le comportement d’un appel RPC lors de l’établissement de connexions http. La valeur **UseHttpProxy** indique à RPC de router le trafic via le proxy http à tout moment, y compris lorsque les options Internet du client sont définies dans Internet Explorer sur « ne pas utiliser de serveur proxy pour les adresses locales ».

    cette option est prise en charge sur Windows 7, Windows Server 2008 R2, Windows 8.1 et Windows Server 2012 R2 avec KB2916915 installé. cette option n’est pas prise en charge sur les Windows 8 et les Windows Server 2012. Les applications peuvent déterminer si cette option est prise en charge par le runtime RPC en vérifiant la valeur de Registre **ConnectionOptionsFlag** située sous la clé de Registre suivante :

    **HKEY \_ local \_ machine \\ Software \\ Microsoft \\ RPC**

    Si le bit 0 (LSB) de cette valeur de Registre est défini, cette option spécifique est prise en charge ; dans le cas contraire, cette option n’est pas prise en charge par le runtime RPC dans le système.

Pour plus d’informations sur la création de liaisons de chaînes, consultez [liaison et Handles](binding-and-handles.md).

Le programme serveur RPC peut accepter les appels RPC en tunnel en écoutant sur la \_ séquence de protocole http ncacn.

Microsoft a deux implémentations majeures de RPC sur HTTP : la version 1 et la version 2.

la Version 1 (appelée RPC sur HTTP v1) est prise en charge via Windows XP. la Version 1 du proxy RPC est prise en charge via Windows 2000.

La version 2 (appelée RPC sur HTTP v2) est la version actuelle.

Les deux versions ont des fonctionnalités différentes et une interopérabilité limitée. Un résumé des différences est fourni ici. Pour plus d’informations sur l’interopérabilité, consultez [Configuration système requise et interopérabilité pour RPC sur http](system-requirements-and-interoperability-for-rpc-over-http.md).

-   RPC sur HTTP v1 requiert l’activation du tunnel SSL sur tous les proxys/pare-feu HTTP entre le client RPC sur HTTP et le proxy RPC. RPC sur HTTP v1 tente de générer un Tunnel ssl sur le port 80, même si les données qu’il envoie ne sont pas réellement chiffrées par le protocole ssl. Les proxies et les pare-feu rejettent généralement ces demandes, sauf s’ils sont explicitement configurés pour les autoriser. RPC sur HTTP v2 n’a pas cette exigence.
-   RPC sur HTTP v1 ne peut pas établir une session SSL pour le proxy RPC. Le RPC sur HTTP v2 peut envoyer tout le trafic RPC sur HTTP au sein d’une session SSL. par défaut, v2 exige que les données soient envoyées au sein d’une session SSL.
-   RPC sur HTTP v1 ne peut pas s’authentifier auprès du proxy RPC. RPC sur HTTP v2 peut s’authentifier ; par défaut, v2 requiert l’authentification auprès du proxy RPC.
-   Le proxy RPC v1 ne fonctionne pas correctement lorsque l’ordinateur IIS sur lequel il est installé fait partie d’une batterie de serveurs Web. Le proxy RPC v2 fonctionne correctement lorsque l’ordinateur IIS sur lequel il est installé fait partie d’une batterie de serveurs Web.

> [!Note]  
> Si Microsoft Internet Explorer est installé sur l’ordinateur du programme client et que votre client ne spécifie pas de **httpproxy** dans sa liaison de chaîne, le stub client RPC recherche une entrée **httpproxy** dans le registre de l’ordinateur client. S’il en trouve un, il utilisera le proxy spécifié dans l’entrée de registre.

 

Supposons, par exemple, que votre programme client doit se connecter via Internet à un serveur RPC sur un ordinateur appelé Server7.microsoft.com. En outre, supposons que le proxy RPC s’exécute sur Major7.microsoft.com. Le programme serveur RPC écoute le port 2225. Votre client utilise la liaison de chaîne :

``` syntax
ncacn_http:Server7.microsoft.com[2225, RpcProxy=Major7.microsoft.com]
```

Si le proxy RPC peut résoudre le nom du serveur en tant que Server7, sans exiger un nom de domaine complet, vous pouvez également spécifier :

``` syntax
ncacn_http:Server7 [2225, RpcProxy=Major7.microsoft.com]
```

Si le réseau client utilise un pare-feu et un serveur proxy Internet appelé MyProxy, et qu’Internet Explorer sur le client n’est pas configuré pour utiliser ce proxy, vous devez modifier la liaison de chaîne du client en :

``` syntax
ncacn_http:Server7.microsoft.com[,HttpProxy=myproxy:80,RpcProxy=Major7.microsoft.com:80]
```

Cela indique au client de se connecter au programme serveur RPC sur Server7.microsoft.com. Pour ce faire, le client utilise tout d’abord le port 80 (ou le port 443 si SSL est utilisé) pour se connecter à MyProxy. Cela permettra au programme client d’accéder à Internet. À l’aide d’Internet, le programme client se connecte ensuite au proxy RPC sur Major7.microsoft.com. Le proxy RPC établit une connexion au programme serveur RPC s’exécutant sur Server7.microsoft.com.

Si le réseau client utilise un pare-feu et si le proxy RPC ne peut pas être contacté directement, pour qu’une connexion soit établie plus rapidement, la liaison de chaîne du client peut être modifiée comme suit :

``` syntax
ncacn_http:Server7.microsoft.com[RpcProxy=Major7.microsoft.com:80,HttpConnectionOption=UseHttpProxy]
```

Le **HttpConnectionOption** vous permet de diriger le comportement d’un RPC lors de l’établissement de connexions http. La valeur **UseHttpProxy** indique à RPC de router le trafic via le proxy http à tout moment, y compris lorsque les options Internet du client sont définies dans Internet Explorer sur « ne pas utiliser de serveur proxy pour les adresses locales ». Cela force le client à se connecter au proxy RPC via le proxy http. Cela accélère le temps nécessaire à l’établissement d’une connexion, car il ignore les retards de recherche du serveur RPC directement avant l’utilisation du proxy HTTP.

Si l’option **HttpConnectionOption** est utilisée et qu’Internet Explorer sur le client n’est pas configuré pour utiliser ce proxy http, les connexions peuvent échouer avec les **\_ \_ \_ \_ options réseau non valides RPC**.

La grande majorité des ordinateurs actuels est configurée pour la navigation Web. Par conséquent, la plupart des clients n’ont pas besoin de spécifier **httpproxy**, car ils seront récupérés à partir des paramètres de connectivité Internet.

 

 




