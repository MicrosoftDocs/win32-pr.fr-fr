---
description: Si le client et l’hôte ne peuvent pas se voir mutuellement sur le réseau, un hôte et un client génériques peuvent être remplacés par l’hôte et le client personnalisés pour aider à résoudre le problème.
ms.assetid: e82ce911-b2a7-4a57-a2f0-9aca6b74478f
title: Utilisation d’un hôte et d’un client génériques pour les WS-Discovery UDP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a7b9f42cd76e54c3ee04a3299e9f23eecbfdd73
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122883076"
---
# <a name="using-a-generic-host-and-client-for-udp-ws-discovery"></a>Utilisation d’un hôte et d’un client génériques pour les WS-Discovery UDP

Si le client et l’hôte ne peuvent pas se voir mutuellement sur le réseau, un hôte et un client génériques peuvent être remplacés par l’hôte et le client personnalisés pour aider à résoudre le problème. Si l’adresse de l’appareil n’apparaît pas dans la sortie du client de débogage WSD, l’environnement réseau est probablement à l’origine de l’échec. Pour plus d’informations sur l’hôte et le client génériques, consultez [outils de débogage](debugging-tools.md).

Si l’hôte ou le client est une application en cours d’exécution sur un PC, l’hôte ou le client générique doit être exécuté dans le même contexte de sécurité que l’hôte ou le client réel. Par exemple, si l’hôte ou le client réel s’exécute en tant qu’administrateur, l’hôte ou le client générique doit s’exécuter en tant qu’administrateur. En outre, si l’hôte ou le client est un appareil autonome, il doit être complètement remplacé par un PC exécutant un hôte ou un client générique.

**Pour utiliser un hôte et un client génériques afin de résoudre les problèmes liés à UDP WS-Discovery**

1.  Ouvrez une fenêtre d’invite de commandes.
2.  Exécutez la commande suivante : **WSDDebug \_host.exe/mode Metadata/Start**

    > [!Note]  
    > une boîte de dialogue d' **alerte Sécurité Windows** peut s’afficher. Dans ce cas, cliquez sur **débloquer** pour permettre l’exécution de l’hôte de débogage WSD.

     

    Cette commande génère une sortie similaire à ce qui suit. Prenez note de l’ID de l’appareil.

    ``` syntax
    WSDAPI Debug Host
    Copyright (C) Microsoft Corporation 2007.  All rights reserved.
    Device ID is urn:uuid:37f86d35-e6ac-4241-964f-1d9ae46fb366
    Host metadata>
    ```

3.  Exécutez la commande suivante : **WSDDebug \_client.exe/mode Metadata/Hello not/Resolve** *&lt; ID &gt;*. Remplacez *&lt; ID &gt;* par l’ID d’appareil identifié à l’étape 2.
    > [!Note]  
    > une boîte de dialogue d' **alerte Sécurité Windows** peut s’afficher. Dans ce cas, cliquez sur **débloquer** pour permettre l’exécution du client de débogage WSD.

     

Le client de débogage WSD génère une sortie similaire à ce qui suit.

``` syntax
WSDAPI Debug Client
Copyright (C) Microsoft Corporation 2007.  All rights reserved.
Client ID is urn:uuid:0f571af7-6b0e-4daf-8054-f2233ac27910
Hello mode is disabled
Client metadata>
*****************************************************************************
Add at 02/28/07 15:16:51
+ EPR:
  + Address:                 urn:uuid:37f86d35-e6ac-4241-964f-1d9ae46fb366
+ Types:
    (wsdp) https://schemas.xmlsoap.org/ws/2006/02/devprof:Device
+ XAddrs:
  https://[::1]:5357/37f86d35-e6ac-4241-964f-1d9ae46fb366
+ Metadata version:          2
+ Instance ID:               1
+ Probe/Resolve tag:         WSDAPI debug_client
+ Remote transport address:  [::1]:3702
+ Local transport address:   ::1
+ Local interface GUID:      42133cd4-6a70-11db-bbc9-806e6f6e6963
Client metadata>
```

Le client de débogage WSD peut générer un grand nombre de sorties sur un réseau avec de nombreux appareils DPWS. La sortie peut être redirigée vers un fichier pour faciliter l’analyse. Tapez **log tee** *&lt; filename &gt;* à l’invite du client de débogage WSD pour rediriger la sortie vers un fichier. La redirection de sortie peut être arrêtée en tapant **log tee Stop** à l’invite du client de débogage WSD.

Prenez note de l’adresse de référence du point de terminaison (EPR). Cette adresse EPR doit correspondre à l’ID d’appareil identifié à l’étape 2 ci-dessus. Si c’est le cas, l’échec de l’application n’est probablement pas lié au système d’exploitation ou à l’environnement réseau. Remplacez l’hôte et le client génériques par l’hôte et le client personnalisés, puis poursuivez le dépannage en suivant les procédures de la section [utilisation du client de débogage WSD pour vérifier le trafic de multidiffusion](using-wsddebug-client-to-verify-multicast-traffic.md).

Si l’ID de l’appareil ne correspond pas à l’adresse du EPR, l’échec de l’application est probablement lié au système d’exploitation ou à l’environnement réseau. L’échec peut avoir une ou plusieurs des causes suivantes :

-   L’application s’exécute dans un contexte de sécurité incorrect. Vérifiez que l’application utilise les informations d’identification correctes et que le client et l’hôte disposent des autorisations suffisantes pour accéder au réseau.
-   La configuration du pare-feu est incorrecte. suivez les instructions de la section inspection des Paramètres de l' [adaptateur et du pare-feu](inspecting-adapter-and-firewall-settings.md) pour vérifier que les paramètres du pare-feu Windows sont corrects et qu’aucune autre règle ne supprime les paquets. Le client et l’hôte peuvent également être copiés sur un ordinateur « initial » (l’un avec une installation de système d’exploitation par défaut qui n’a jamais été jointe à un domaine) afin de tenter de reproduire l’échec.
-   Une stratégie IPSec bloque l’application. Copiez le client et l’hôte sur un ordinateur qui n’est pas soumis aux stratégies IPSec et essayez de reproduire l’échec.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Procédures de diagnostic WSDAPI](wsdapi-diagnostic-procedures.md)
</dt> <dt>

[Résolution des problèmes de Prise en main avec WSDAPI](getting-started-with-wsdapi-troubleshooting.md)
</dt> </dl>

 

 



