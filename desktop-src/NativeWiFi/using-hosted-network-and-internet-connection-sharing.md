---
title: Utiliser un réseau hébergé sans fil, partage de connexion Internet
description: Utilisation du partage de connexion Internet et d’un réseau hébergé sans fil
ms.assetid: 56e86ef8-f759-4e56-a591-74e03430125a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 972774e921199e32eb70841c74c7478e2178cda9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127229734"
---
# <a name="use-wireless-hosted-network-internet-connection-sharing"></a>Utiliser un réseau hébergé sans fil, partage de connexion Internet

le réseau hébergé sans fil est une nouvelle fonctionnalité WLAN prise en charge sur Windows 7 et Windows 8. il est également pris en charge sur Windows Server 2012 et Windows Server 2008 R2 avec le Service de réseau local sans fil installé. Cette fonctionnalité implémente deux fonctions principales :

-   La virtualisation d’un adaptateur sans fil physique dans plusieurs cartes sans fil virtuelles, parfois appelées « Wi-Fi virtuel ».
-   Un point d’accès sans fil (AP) basé sur des logiciels, parfois appelé SoftAP qui utilise un adaptateur sans fil virtuel désigné.

le partage de connexion Internet (ICS) est une fonctionnalité de Windows fournie par le biais du Service SharedAccess. À proprement parler, SharedAccess autorise le partage réseau via un ordinateur où l’accès réseau partagé ne fournit pas nécessairement un accès à Internet. Nous utilisons le terme ICS et SharedAccess de manière interchangeable dans cette section, puisque le partage de connexion Internet est un scénario majeur pour le réseau hébergé sans fil et le terme ICS est mieux connu de la communauté des utilisateurs.

Le réseau hébergé sans fil est étroitement lié à ICS pour activer à la fois le réseau personnel sans fil et les scénarios de partage Internet. Cette section fournit des recommandations générales aux développeurs d’applications sur la façon d’intégrer un réseau et un partage de connexion Internet hébergés à l’aide du réseau public sans fil hébergé et des API ICS.

## <a name="internet-connection-sharing"></a>Partage de connexion Internet

Le service ICS fonctionne dans l’un des deux modes possibles :

-   Mode autonome

    Seule la fonction serveur DHCPv4 fonctionne lorsque le service ICS est appelé. Il s’agit d’un mode d’opération spécial pour le partage de connexion Internet et n’est disponible que par le biais du réseau hébergé sans fil. Un utilisateur ou une application n’est pas en mesure de démarrer et d’arrêter directement le partage de connexion Internet autonome via des API de partage de connexion Internet publiques ou des commandes **netsh** . Le démarrage du réseau hébergé sans fil implique généralement le démarrage du partage de connexion Internet en mode autonome pour utiliser la fonction de serveur DHCPv4 afin de fournir des adresses IPv4 privées pour les appareils connectés. La communication réseau pour les appareils connectés est limitée à l’envoi et à la réception de paquets réseau entre un appareil connecté et l’ordinateur local qui héberge le réseau sans fil hébergé et entre les appareils connectés eux-mêmes. Cela active efficacement le scénario Wireless Personal Area Network pour le réseau hébergé sans fil.

-   Mode complet

    Toutes les fonctionnalités de l’ICS fonctionnent lorsque le service est appelé, comme la traduction d’adresses réseau et les fonctions de serveur DHCP pour IPv4 et IPv6. Il s’agit du mode de fonctionnement normal pour le partage de connexion Internet. Un utilisateur ou une application peut démarrer et arrêter le mode ICS complet via des API publiques ou des commandes NetShell. Par exemple, ce service peut être arrêté à l’aide de net stop SharedAccess à partir d’une invite de commandes avec élévation de privilèges. En associant un réseau hébergé sans fil à un partage de connexion complet, la communication réseau pour les appareils connectés n’est pas limitée au PAN sans fil. Tout appareil connecté a accès au réseau (par exemple, Internet) via la connexion réseau partagée de l’ordinateur qui exécute le réseau hébergé sans fil. Cela active efficacement le scénario de partage réseau pour le réseau hébergé sans fil.

Dans cette section, nous utilisons le terme de partage de la connexion Internet (ICS) pour signifier le cas où toutes les fonctions de partage de connexion Internet sont appelées dans le service ICS pour fournir l’accès à toutes les fonctionnalités de l’ICS complet avec le réseau hébergé sans fil.

Les deux modes d’opération ICS s’excluent mutuellement avec une priorité plus élevée pour le partage de connexion Internet. Le service ICS peut passer du mode autonome au mode complet, mais pas du mode plein au mode autonome. le mode autonome ICS a été introduit dans Windows 7 et sur Windows Server 2008 R2 avec le Service de réseau local sans fil installé conjointement avec la fonctionnalité de réseau hébergé sans fil. Elle n’est pas disponible dans les versions précédentes de Windows.

Toute opération ICS complète implique deux cartes réseau différentes dans le système :

-   Interface publique. Il s’agit de l’interface réseau avec accès à Internet. C’est cette interface que l’ordinateur local qui exécute ICS utilise pour partager Internet avec les clients et les appareils qui se connectent à ce dernier via SoftAP.
-   Interface privée. Il s’agit de l’interface réseau que d’autres appareils utilisent pour se connecter à l’ordinateur local qui exécute le partage de connexion Internet. Un serveur DHCPv4 s’exécute sur cette interface privée pour fournir des adresses IP locales privées aux autres ordinateurs distants.

Lorsque l’interface publique n’a pas accès à Internet, le serveur DHCP sur l’interface privée continue de fournir des adresses IP locales aux appareils connectés. Le partage de connexion Internet autonome implique uniquement l’interface privée sur laquelle SoftAP est exécuté ; elle n’implique aucune interface publique.

À tout moment, il y a au plus une instance de l’intégralité du partage de connexion Internet en cours d’exécution sur l’ordinateur local. Si le partage de connexion Internet complet est déjà en cours d’exécution sur l’ordinateur local, le démarrage d’un autre partage de connexion Internet présente les comportements fonctionnels suivants :

-   Si les interfaces publiques et privées du nouveau partage de partage de la connexion (ICS) complète sont identiques à celles du partage de connexion Internet complet existant, le fait de démarrer la deuxième ICS complète équivaut à une absence d’opération.
-   Si la nouvelle interface publique est différente de l’ancienne interface publique, mais que la nouvelle interface privée est la même que l’ancienne interface privée, le démarrage d’un deuxième partage de connexion Internet n’a que peu d’impact sur les périphériques connectés sur la même interface privée. La possibilité d’accéder à Internet peut changer avec la nouvelle interface publique.
-   Si la nouvelle interface privée est différente de l’ancienne interface privée, les fonctions ICS cesseront de fonctionner sur l’ancienne interface privée et commenceront à s’appliquer à la nouvelle interface privée. Tout appareil distant qui se connecte à l’ordinateur local à l’aide de l’ancienne interface privée perd la connectivité IP à l’ordinateur local.

Lorsque le partage de connexion Internet complet est déjà en cours d’exécution, l’appel d’un deuxième partage de connexion Internet complet entraîne une interruption des appareils connectés à distance à l’aide de l’ancienne interface privée, à condition que la deuxième intégration ICS utilise une nouvelle interface privée différente.

Pour gérer et utiliser le service ICS afin de prendre en charge l’intégration du partage de connexion Internet avec un réseau hébergé sans fil, une application logicielle doit d’abord obtenir une interface [**INetSharingManager**](/windows/win32/api/netcon/nn-netcon-inetsharingmanager) . L’interface **INetSharingManager** fournit l’accès directement ou indirectement à toutes les autres interfaces COM de l’API ICS. La [**méthode \_ SharingInstalled**](/windows/win32/api/netcon/nf-netcon-inetsharingmanager-get_sharinginstalled) sur l’interface **INetSharingManager** indique si l’ordinateur local prend en charge le partage de connexion. La méthode [**obtenir \_ EnumEveryConnection**](/windows/win32/api/netcon/nf-netcon-inetsharingmanager-get_enumeveryconnection) sur l’interface **INetSharingManager** récupère une interface d’énumération pour toutes les connexions dans le dossier connexions. La méthode [**obtenir \_ INetSharingConfigurationForINetConnection**](/windows/win32/api/netcon/nf-netcon-inetsharingmanager-get_inetsharingconfigurationforinetconnection) récupère une interface [**INetSharingConfiguration**](/windows/win32/api/netcon/nn-netcon-inetsharingconfiguration) pour la connexion spécifiée. Les méthodes de l’interface **INetSharingConfiguration** peuvent être utilisées pour interroger et modifier les paramètres du partage de connexion Internet.

Le réseau hébergé sans fil doit être démarré avant d’appeler la méthode [**\_ EnumEveryConnection**](/windows/win32/api/netcon/nf-netcon-inetsharingmanager-get_enumeveryconnection) sur l’interface [**INetSharingManager**](/windows/win32/api/netcon/nn-netcon-inetsharingmanager) pour énumérer toutes les connexions dans le dossier connexions.

Pour plus d’informations sur le partage de connexion Internet et les interfaces et méthodes publiques qui peuvent être utilisées pour interroger et modifier les paramètres ICS, consultez la documentation sur le [partage de connexion Internet et le pare-feu de connexion Internet](/previous-versions/windows/desktop/ics/about-internet-connection-sharing-and-internet-connection-firewall).

## <a name="hosted-network-and-ics-integration"></a>Intégration du réseau hébergé et du partage de connexion Internet

Lorsque le partage de connexion Internet complet n’est pas en cours d’exécution, le démarrage d’un réseau hébergé sans fil démarre également en interne le service ICS en mode autonome avec uniquement la fonction serveur DHCPv4 pour allouer des adresses IP pour les appareils connectés sur l’interface réseau hébergée sans fil. La plage d’adresses de sous-réseau pour le serveur DHCPv4 autonome est 192.168.173.0/24. Cela diffère de la plage de sous-réseau de 192.168.137.0/24 qui est utilisée avec le partage de connexion Internet complet.

Le démarrage d’un réseau hébergé sans fil avec l’accès au partage de la connexion complète utilise la logique suivante :

-   Si le partage de connexion Internet complet n’est pas déjà en cours d’exécution, le démarrage d’un réseau hébergé sans fil démarre également le service ICS avec un serveur DHCPv4 autonome.
-   Si le partage de connexion Internet complet est déjà en cours d’exécution et que l’interface privée est l’interface réseau hébergée sans fil, démarrez simplement le réseau sans fil hébergé.
-   Si le partage de connexion Internet complet est déjà en cours d’exécution mais que l’interface privée n’est pas l’interface réseau hébergée sans fil, le réseau sans fil hébergé est démarré sans la fonction serveur DHCPv4 sur l’interface réseau hébergée sans fil.

L’impact de la logique ci-dessus met en évidence les faits suivants :

-   Le partage de connexion Internet ne passe pas du mode plein au mode autonome.
-   Le mode autonome ne peut être appelé que par le réseau hébergé sans fil lorsque le partage de connexion Internet n’est pas exécuté en mode complet.
-   Si le partage de connexion Internet s’exécute en mode autonome, il est reporté en mode complet si un utilisateur ou une application démarre ICS en mode complet.
-   La transition du mode autonome vers le mode plein dans le partage de connexion Internet entraîne une interruption des appareils connectés dans le PAN sans fil si l’interface privée de l’accès à Internet complet n’est pas la même que celle de SoftAP.

Il faut du temps pour démarrer ou arrêter le service ICS sur l’ordinateur local en mode complet ou autonome. Une application doit vérifier l’état du service ICS à l’aide de la fonction **NotifyServiceStatusChange** pour s’assurer que le service ICS n’est pas dans l’état d’attente démarrer/arrêter avant de démarrer ou d’arrêter le réseau sans fil hébergé pour une utilisation avec l’intégration ICS.

## <a name="starting-and-stopping-the-wireless-hosted-network"></a>Démarrage et arrêt du réseau hébergé sans fil

Windows fournit une plateforme dans laquelle plusieurs applications simultanées sont autorisées à gérer un réseau hébergé sans fil en même temps. Plus précisément, chaque application peut démarrer et arrêter le réseau hébergé sans fil proprement dit, sans connaissance préalable des autres applications.

Il existe deux ensembles de fonctions permettant de démarrer et d’arrêter un réseau hébergé.

Plusieurs applications peuvent nécessiter l’utilisation du réseau hébergé sans fil. Les fonctions [**WlanHostedNetworkStartUsing**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkstartusing) et [**WlanHostedNetworkStopUsing**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkstopusing) démarrent et arrêtent une entrée réseau hébergée sans fil d’une manière compatible avec d’autres applications simultanées. Les fonctions **WlanHostedNetworkStartUsing** et **WlanHostedNetworkStopUsing** permettent à une application d’avoir une référence au réseau hébergé sans fil. Ce mécanisme maintient le réseau hébergé sans fil en cours d’exécution, à condition qu’au moins une autre application ait une référence actuelle au réseau hébergé sans fil. N’importe quel utilisateur peut appeler ces fonctions. Les appels réussis à **WlanHostedNetworkStartUsing** doivent être mis en correspondance par des appels à la fonction **WlanHostedNetworkStopUsing** . Toute modification de l’état du réseau hébergé provoquée par la fonction **WlanHostedNetworkStartUsing** est automatiquement annulée si l’application appelante ferme son handle appelant (en appelant [**WlanCloseHandle**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanclosehandle) avec le même paramètre *hClientHandle* passé à **WlanHostedNetworkStartUsing**) ou si le processus se termine.

Les fonctions [**WlanHostedNetworkForceStart**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkforcestart) et [**WlanHostedNetworkForceStop**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkforcestop) forcent le démarrage et l’arrêt d’un réseau hébergé sans fil. Ces fonctions ne peuvent être appelées que si l’utilisateur dispose des privilèges élevés appropriés. Les appels réussis à **WlanHostedNetworkForceStart** peuvent éventuellement être mis en correspondance par un appel à la fonction **WlanHostedNetworkForceStop** , selon la conception de l’application. Ces fonctions migrent l’état du réseau hébergé sans fil sans associer la demande au descripteur appelant de l’application. Toute modification de l’état du réseau hébergé provoquée par la fonction **WlanHostedNetworkForceStart** n’est pas automatiquement annulée si l’application appelante ferme son handle appelant (en appelant [**WlanCloseHandle**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanclosehandle) avec le même paramètre *hClientHandle* passé à [**WlanHostedNetworkStartUsing**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkstartusing)) ou si le processus se termine. Si l’application qui a appelé la fonction **WlanHostedNetworkForceStart** se ferme sans appeler l’une des fonctions pour arrêter le réseau hébergé sans fil, le réseau hébergé reste en cours d’exécution. Une application peut appeler la fonction **WlanHostedNetworkForceStart** après avoir vérifié qu’un utilisateur système avec des privilèges élevés accepte les exigences d’alimentation accrues inhérentes à l’exécution du réseau hébergé sans fil pendant des périodes prolongées.

Les recommandations générales sur les fonctions à appeler pour démarrer et arrêter un réseau hébergé sans fil sont les suivantes :

-   Utilisez les fonctions [**WlanHostedNetworkStartUsing**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkstartusing) et [**WlanHostedNetworkStopUsing**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkstopusing) dans une application pour démarrer et arrêter un réseau hébergé sans fil.
-   N’utilisez pas la fonction [**WlanHostedNetworkForceStart**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkforcestart) pour démarrer un réseau hébergé sans fil à moins qu’il soit absolument requis par l’application. La fonction **WlanHostedNetworkForceStart** nécessite également des privilèges élevés.
-   Utilisez uniquement la fonction [**WlanHostedNetworkForceStop**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkforcestop) comme méthode de récupération. La fonction **WlanHostedNetworkForceStop** provoque l’arrêt immédiat d’un réseau hébergé sans fil. D’autres applications qui écoutent les notifications de réseau hébergé sans fil peuvent avoir besoin de prendre des mesures de récupération. Pour plus d’informations, consultez la discussion ci-dessous sur la séquence de récupération pour un réseau hébergé sans fil.

## <a name="start-sequence-for-wireless-hosted-network"></a>Démarrer la séquence pour un réseau hébergé sans fil

Pour une application qui démarre un réseau hébergé sans fil avec un partage de connexion complet, il est recommandé de démarrer le réseau sans fil hébergé, puis de démarrer le partage de connexion Internet complet. Si un réseau hébergé sans fil est déjà en cours d’exécution, une application doit utiliser la fonction [**WlanHostedNetworkForceStop**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkforcestop) pour arrêter le réseau sans fil hébergé uniquement si le partage de connexion Internet complet est requis mais n’a pas été activé avant le démarrage du réseau hébergé. Cela permettra à d’autres applications de récupérer des interruptions potentielles provoquées par le démarrage du partage de connexion Internet complet. Pour plus d’informations, consultez la discussion ci-dessous sur la séquence de récupération pour un réseau hébergé sans fil. L’opération combinée doit réussir et échouer dans son ensemble.

> [!Note]  
> Le réseau hébergé sans fil doit être démarré avant toute tentative d’énumération de l’adaptateur correspondant à l’aide de l’interface [**IEnumNetSharingEveryConnection**](/windows/win32/api/netcon/nn-netcon-ienumnetsharingeveryconnection) .

 

Les étapes ordonnées suivantes sont la séquence de démarrage recommandée dans une application utilisant un réseau hébergé sans fil avec le partage de connexion Internet complet :

-   Appelez la fonction [**WlanHostedNetworkInitSettings**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkinitsettings) pour vous assurer que le réseau hébergé sans fil est configuré et prêt à être utilisé.
-   Appelez les fonctions [**WlanHostedNetworkQueryStatus**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkquerystatus) et [**WlanHostedNetworkQueryProperty**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkqueryproperty) pour déterminer si le réseau hébergé sans fil est autorisé et disponible. Si le réseau hébergé sans fil n’est pas autorisé et n’est pas disponible, retourne une erreur.
-   Vérifiez si le service ICS utilisé pour le partage de connexion Internet complet est autorisé. Si le service ICS ne peut pas être démarré, retourne une erreur.
-   Appelez la fonction [**WlanHostedNetworkForceStop**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkforcestop) pour forcer l’arrêt du réseau hébergé sans fil.
-   Appelez la fonction [**WlanHostedNetworkStartUsing**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkstartusing) pour démarrer le réseau hébergé sans fil.
-   Si le réseau hébergé sans fil ne parvient pas à démarrer, retournez une erreur.
-   Si le partage de connexion Internet complet est déjà en cours d’exécution et que l’interface publique ou privée actuelle est différente de la nouvelle interface à utiliser, mettez en cache les interfaces publiques et privées actuelles. Une application peut également choisir de retourner une erreur ou d’inviter l’utilisateur si l’intégration ICS est déjà en cours d’exécution.
-   Démarrez le partage de connexion Internet complet avec les nouveaux paramètres pour les interfaces publiques et privées.
-   Si le partage de connexion Internet complet ne parvient pas à démarrer avec ces paramètres, essayez de démarrer le service ICS complet avec les interfaces publiques et privées mises en cache si le partage de connexion Internet complet était en cours d’exécution. Appelez la fonction [**WlanHostedNetworkForceStop**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkforcestop) pour arrêter le réseau hébergé sans fil et retourner une erreur.
-   Retourne la réussite du succès du réseau hébergé sans fil et du partage de connexion Internet complet.

## <a name="stop-sequence-for-wireless-hosted-network"></a>Arrêter la séquence pour le réseau hébergé sans fil

Lorsque vous utilisez un réseau hébergé sans fil avec un partage de connexion Internet complet, une application qui a terminé son travail peut arrêter le réseau hébergé sans fil et le service ICS utilisé pour le partage de connexion Internet complet. Dans ce cas, il est recommandé d’appeler la fonction [**WlanHostedNetworkForceStop**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkforcestop) pour arrêter le réseau hébergé au lieu d’appeler la fonction [**WlanHostedNetworkStopUsing**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkstopusing) . La fonction **WlanHostedNetworkForceStop** arrête le réseau hébergé sans fil et sert également à permettre à d’autres applications de récupérer. Pour plus d’informations, consultez la discussion ci-dessous sur la séquence de récupération pour un réseau hébergé sans fil.

Les étapes ordonnées suivantes sont la séquence d’arrêt recommandée dans une application utilisant un réseau hébergé sans fil et le partage de connexion Internet complet :

-   Arrêtez le partage de connexion Internet complet.
-   Appelez la fonction [**WlanHostedNetworkForceStop**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkforcestop) pour arrêter le réseau hébergé sans fil.

Une application qui utilise un réseau hébergé sans fil sans partage de connexion Internet complet avec son travail doit simplement appeler la fonction [**WlanHostedNetworkStopUsing**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkstopusing) ou [**WlanHostedNetworkForceStop**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkforcestop) pour arrêter le réseau hébergé sans fil. Si la fonction [**WlanHostedNetworkStartUsing**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkstartusing) a été appelée pour démarrer le réseau hébergé sans fil, l’application doit appeler la fonction **WlanHostedNetworkStopUsing** pour arrêter le réseau hébergé sans fil. Si le réseau hébergé sans fil a déjà été démarré avant que l’application ou l’application a appelé la fonction [**WlanHostedNetworkForceStart**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkforcestart) pour forcer le démarrage du réseau hébergé sans fil, l’application peut appeler la fonction **WlanHostedNetworkForceStop** pour arrêter le réseau hébergé sans fil ou ne rien faire (laissez le réseau hébergé sans fil démarré) en fonction du scénario.

## <a name="recovery-sequence-for-wireless-hosted-network"></a>Séquence de récupération pour un réseau hébergé sans fil

Une application utilisant le réseau hébergé sans fil peut être affectée par les actions d’autres applications. Le service ICS et les interfaces de gestion du partage de connexion Internet ne fournissent aucune méthode permettant à une application de s’inscrire pour les notifications de modification ICS. Si une autre application appelle les méthodes [**EnableSharing**](/windows/win32/api/netcon/nf-netcon-inetsharingconfiguration-enablesharing) ou [**DisableSharing**](/windows/win32/api/netcon/nf-netcon-inetsharingconfiguration-disablesharing) sur l’interface [**INetSharingConfiguration**](/windows/win32/api/netcon/nn-netcon-inetsharingconfiguration) pour activer ou désactiver le partage sur une connexion, un message est envoyé à l’interface utilisateur (l’écran) sur l’ordinateur local et non à d’autres applications. Par conséquent, une application doit s’appuyer sur les notifications de réseau hébergé sans fil pour effectuer des actions de récupération lorsque des modifications de réseau sans fil ou d’ICS sont effectuées.

Une application utilisant le réseau hébergé sans fil doit s’inscrire pour les notifications de réseau hébergé sans fil en appelant [**WlanRegisterNotification**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanregisternotification). Si vous avez besoin de notifications uniquement pour un réseau hébergé sans fil, l’application doit transmettre la **\_ source de notification WLAN \_ \_ HNWK** dans le paramètre *dwNotifSource* passé à **WlanRegisterNotification**. Si d’autres notifications sans fil sont également nécessaires, la **\_ source de notification WLAN \_ \_ HNWK** doit être associée aux constantes de la source de notification pour d’autres types de notifications sans fil souhaitées et transmettre cette valeur dans le paramètre *dwNotifSource* .

La séquence de récupération est la même pour les applications avec ou sans partage de connexion Internet complet, en supposant que les applications ne souhaitent pas redémarrer le service ICS. Lors de la réception d’une notification de réseau hébergé sans fil que le réseau hébergé a arrêté, procédez comme suit :

-   Si l’application appelée [**WlanHostedNetworkForceStart**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkforcestart) démarre le réseau hébergé sans fil, redémarrez le réseau hébergé en appelant **WlanHostedNetworkForceStart**. Sinon, appelez [**WlanHostedNetworkStartUsing**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkstartusing) pour redémarrer le réseau hébergé sans fil.

## <a name="recovery-sequence-for-connected-devices"></a>Séquence de récupération pour les appareils connectés

Les appareils distants ou les ordinateurs connectés au réseau hébergé sans fil peuvent être affectés par les actions d’autres applications qui ont un impact sur le partage de connexion Internet et le réseau hébergé sans fil. Heureusement, la plupart des appareils ont une logique de nouvelle tentative intégrée dans l’application de l’appareil pour traiter une perte temporaire de signal ou d’itinérance.

Une séquence de récupération possible pour les appareils ou les ordinateurs connectés au réseau sans fil hébergé qui perdent le contact est la suivante :

-   Le pilote de périphérique sans fil indique qu’un support se déconnecte aux couches supérieures de la pile réseau sur l’appareil.
-   L’application de l’appareil démarre des vérifications périodiques pour la disponibilité du réseau hébergé sans fil.
-   Une fois que l’application de l’appareil détecte à nouveau le réseau hébergé sans fil, l’appareil établit une connexion sans fil.
-   Une fois la connexion établie avec le réseau hébergé sans fil, l’application de l’appareil met à jour ses paramètres IP en conséquence.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[À propos du réseau hébergé sans fil](about-the-wireless-hosted-network.md)
</dt> <dt>

[Exemple de réseau hébergé sans fil](wireless-hosted-network-sample.md)
</dt> <dt>

[**WlanHostedNetworkForceStart**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkforcestart)
</dt> <dt>

[**WlanHostedNetworkInitSettings**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkinitsettings)
</dt> <dt>

[**WlanHostedNetworkQueryProperty**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkqueryproperty)
</dt> <dt>

[**WlanHostedNetworkQuerySecondaryKey**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkquerysecondarykey)
</dt> <dt>

[**WlanHostedNetworkQueryStatus**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkquerystatus)
</dt> <dt>

[**WlanHostedNetworkRefreshSecuritySettings**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkrefreshsecuritysettings)
</dt> <dt>

[**WlanHostedNetworkSetProperty**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworksetproperty)
</dt> <dt>

[**WlanHostedNetworkSetSecondaryKey**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworksetsecondarykey)
</dt> <dt>

[**WlanHostedNetworkStartUsing**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkstartusing)
</dt> <dt>

[**WlanHostedNetworkStopUsing**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkstopusing)
</dt> <dt>

[**WlanRegisterVirtualStationNotification**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanregistervirtualstationnotification)
</dt> </dl>

 

 
