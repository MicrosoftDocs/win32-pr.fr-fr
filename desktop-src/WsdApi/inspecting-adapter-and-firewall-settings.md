---
description: Un pare-feu mal configuré peut provoquer l’échec des applications WSD.
ms.assetid: eba61235-29b4-463a-b7c5-d34d3b39b095
title: inspection des Paramètres de l’adaptateur et du pare-feu
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62ea14051ac65dbd0b749fa00566afc9ed82e5571f6027dafa003e12013888b7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119130781"
---
# <a name="inspecting-adapter-and-firewall-settings"></a>inspection des Paramètres de l’adaptateur et du pare-feu

Un pare-feu mal configuré peut provoquer l’échec des applications WSD. Cette rubrique fournit des procédures de dépannage à utiliser lorsque les clients et hôtes WSD ne peuvent pas s’afficher mutuellement sur le réseau. Les paramètres de pare-feu doivent être inspectés avant d’utiliser une autre procédure de résolution des problèmes d’application.

**Pour inspecter les paramètres de l’adaptateur et du pare-feu**

1.  Vérifiez que l’exception de **découverte du réseau** est activée.
2.  Vérifiez qu’aucune règle de pare-feu propre à l’application ne bloque l’application.
3.  Activez explicitement les ports utilisés pour la découverte et l’échange de métadonnées.
4.  Désactivez le pare-feu et retestez l’application.
    > [!Note]  
    > Une fois cette étape terminée, le pare-feu doit être réactivé.

     

## <a name="verifying-that-the-network-discovery-exception-is-enabled"></a>Vérification de l’activation de l’exception de découverte du réseau

Si des applications WS-Discovery sont en cours d’exécution, l’exception de pare-feu de **découverte du réseau** doit être autorisée.

**Pour activer l’exception de pare-feu de découverte du réseau**

1.  Cliquez sur **Démarrer**, sur **exécuter**, puis tapez **firewall.cpl**. l’applet du **panneau de configuration Windows pare-feu** s’ouvre.
2.  choisissez **autoriser un programme via le pare-feu Windows**.
3.  Sous l’onglet **exceptions** , activez la case à cocher **découverte du réseau** .
4.  Cliquez sur **OK** pour fermer l’applet de pare-feu.

Retestez le programme après avoir modifié ce pare-feu. Si le programme fonctionne correctement, la cause du problème a été identifiée et aucune étape de dépannage supplémentaire n’est nécessaire. Dans le cas contraire, passez à l’étape suivante.

## <a name="checking-for-application-specific-firewall-rules"></a>Recherche de règles de pare-feu spécifiques à l’application

la configuration avancée du pare-feu Windows peut avoir lieu dans un composant logiciel enfichable MMC (Microsoft Management Control) nommé **Windows pare-feu avec fonctions avancées de sécurité**. Ce composant logiciel enfichable peut être utilisé pour résoudre les problèmes de pare-feu suspects.

les développeurs peuvent utiliser les api [Windows pare-feu avec fonctions avancées de sécurité](/previous-versions/windows/desktop/ics/windows-firewall-with-advanced-security-reference) pour créer des règles de pare-feu qui s’appliquent à leurs applications WSD. Plus précisément, la méthode [**Add**](/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwrules-add) de l’interface [**INetFwRules**](/previous-versions/windows/desktop/api/netfw/nn-netfw-inetfwrules) peut être utilisée pour ajouter une nouvelle règle de pare-feu. Si les règles de pare-feu sont créées de manière incorrecte, les clients et les hôtes peuvent ne pas être en mesure de s’afficher mutuellement sur le réseau.

**Pour vérifier les règles de pare-feu spécifiques à l’application**

1.  Cliquez sur **Démarrer**, sur **exécuter**, puis tapez **WF. msc**.
2.  Recherchez les règles spécifiques à l’application susceptibles de bloquer le trafic. pour plus d’informations, consultez [Windows pare-feu avec fonctions avancées de sécurité-diagnostics et outils de dépannage](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc722062(v=ws.10)?ocid=fwlink).
3.  Supprimer les règles spécifiques à l’application.

Si aucune règle spécifique à l’application n’a été trouvée, passez à l’étape suivante. Si une règle spécifique à l’application a été trouvée et supprimée, retestez le programme après avoir modifié le pare-feu. Si le programme fonctionne correctement, la cause du problème a été identifiée et aucune étape de dépannage supplémentaire n’est nécessaire. Dans le cas contraire, passez à l’étape suivante.

## <a name="enabling-the-ports-used-for-discovery-and-metadata-exchange"></a>Activation des ports utilisés pour la découverte et l’échange de métadonnées

WS-Discovery utilise le port UDP 3702 pour l’échange de messages. En outre, les ports TCP 5357 et 5358 sont parfois utilisés pour l’échange de métadonnées. ces ports peuvent être ouverts explicitement sur le pare-feu à l’aide des procédures décrites dans [ouvrir un port dans Windows pare-feu](https://windowshelp.microsoft.com/Windows/Help/4da18300-9044-47b6-9038-595c78db81ab1033.mspx).

Retestez le programme après avoir modifié ce pare-feu. Si le programme fonctionne correctement, la cause du problème a été identifiée et aucune étape de dépannage supplémentaire n’est nécessaire. Dans le cas contraire, passez à l’étape suivante.

## <a name="disabling-the-firewall"></a>Désactivation du pare-feu

le pare-feu Windows peut être désactivé pour aider à résoudre les problèmes suspects. D’autres pare-feu applicables (tels que le pare-feu sur un routeur) peuvent également être désactivés à des fins de dépannage. pour plus d’informations sur l’activation et la désactivation du pare-feu Windows, consultez [activer ou désactiver le pare-feu Windows](https://windowshelp.microsoft.com/Windows/Help/bfe523a9-7eec-4d3f-add1-2f68b9cfa1c01033.mspx).

Retestez l’application après avoir désactivé les pare-feu applicables. Si le programme fonctionne maintenant correctement, le pare-feu bloque le trafic. Il existe plusieurs causes possibles de blocage du trafic.

-   Les exceptions spécifiques à l’application ont bloqué le trafic. Vérifiez les règles de pare-feu spécifiques à l’application, comme décrit ci-dessus.
-   L’appareil a mis trop de temps à répondre aux demandes UDP. le pare-feu Windows peut bloquer les réponses UDP qui renvoient plus de 4 secondes après l’envoi de la demande initiale. Poursuivez la résolution des problèmes en suivant les procédures indiquées dans [utilisation d’un hôte et d’un client génériques pour UDP WS-Discovery](using-a-generic-host-and-client-for-udp-ws-discovery.md) pour déterminer si le problème se reproduit avec un hôte qui répond en moins de 4 secondes.

Si l’application échoue toujours après la désactivation du pare-feu, le pare-feu n’est pas à l’origine de l’échec de l’application. Réactivez les pare-feu et poursuivez la résolution des problèmes en suivant les procédures indiquées dans [utilisation d’un hôte et d’un client génériques pour UDP WS-Discovery](using-a-generic-host-and-client-for-udp-ws-discovery.md).

Les pare-feu doivent toujours être réactivés une fois la résolution des problèmes terminée.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Procédures de diagnostic WSDAPI](wsdapi-diagnostic-procedures.md)
</dt> <dt>

[Résolution des problèmes de Prise en main avec WSDAPI](getting-started-with-wsdapi-troubleshooting.md)
</dt> </dl>

 

 
