---
description: Si le client et l’hôte ne peuvent pas échanger de métadonnées, un hôte et un client génériques peuvent être remplacés par l’hôte et le client personnalisés pour aider à résoudre le problème.
ms.assetid: 7e5c8444-b3ee-4e9c-984f-13d54f2bbfc0
title: Utilisation d’un hôte et d’un client génériques pour les métadonnées HTTP Exchange
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10040f4834df1a77115a361d23d82ec3dfcc6c57
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122883173"
---
# <a name="using-a-generic-host-and-client-for-http-metadata-exchange"></a>Utilisation d’un hôte et d’un client génériques pour les métadonnées HTTP Exchange

Si le client et l’hôte ne peuvent pas échanger de métadonnées, un hôte et un client génériques peuvent être remplacés par l’hôte et le client personnalisés pour aider à résoudre le problème. Si l’adresse de l’appareil ou les métadonnées de l’appareil n’apparaissent pas dans la sortie du client de débogage WSD, les adresses de transport ou l’environnement réseau fournis peuvent être à l’origine de l’échec. Pour plus d’informations sur l’hôte et le client génériques, consultez [outils de débogage](debugging-tools.md).

S’il a été vérifié qu’un hôte et un client génériques peuvent exécuter à la fois les WS-Discovery et l’échange de métadonnées HTTP, cette procédure de diagnostic peut être ignorée et la résolution des problèmes peut être poursuivie en suivant les procédures de la section utilisation de la [journalisation WinHTTP pour vérifier la récupération du trafic](using-winhttp-logging-to-verify-get-traffic.md).

Si l’hôte ou le client est une application en cours d’exécution sur un PC, l’hôte ou le client générique doit être exécuté dans le même contexte de sécurité que l’hôte ou le client réel. Par exemple, si l’hôte ou le client réel s’exécute en tant qu’administrateur, l’hôte ou le client générique doit s’exécuter en tant qu’administrateur. En outre, si l’hôte ou le client est un appareil autonome, il doit être complètement remplacé par un PC exécutant un hôte ou un client générique dans un contexte de sécurité qui garantit un accès illimité au réseau (par exemple, l’exécution en tant qu’administrateur).

**Pour utiliser un hôte et un client génériques pour résoudre les problèmes liés à l’échange de métadonnées HTTP**

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
*****************************************************************************
Getting metadata for host at 02/28/07 15:16:51:
+ Endpoint reference:
  + Address:
    urn:uuid:37f86d35-e6ac-4241-964f-1d9ae46fb366
Using xAddr: https://[::1]:5357/37f86d35-e6ac-4241-964f-1d9ae46fb366
Client metadata>
*****************************************************************************
Metadata for host:
+ Endpoint reference:
  + Address:           urn:uuid:37f86d35-e6ac-4241-964f-1d9ae46fb366
Metadata section:
  + Dialect:
    https://schemas.xmlsoap.org/ws/2006/02/devprof/ThisDevice
  + Friendly name:
    [no lang]: Debugging Host
  + Firmware version:  1.0
  + Serial number:     00000000
Metadata section:
  + Dialect:
    https://schemas.xmlsoap.org/ws/2006/02/devprof/ThisModel
  + Manufacturer:
    [no lang]: Microsoft Corporation
  + Manufacturer URL:  https://www.microsoft.com/
  + Model names:
    [no lang]: Microsoft Debugging Host
  + Model number:      https://www.microsoft.com/
End of metadata
Client metadata>
```

Le client de débogage WSD peut générer un grand nombre de sorties sur un réseau avec de nombreux appareils DPWS. La sortie peut être redirigée vers un fichier pour faciliter l’analyse. Tapez **log tee** *&lt; filename &gt;* à l’invite du client de débogage WSD pour rediriger la sortie vers un fichier. La redirection de sortie peut être arrêtée en tapant **log tee Stop** à l’invite du client de débogage WSD.

Prenez note de l’adresse de référence du point de terminaison (EPR). Cette adresse EPR doit correspondre à l’ID d’appareil identifié à l’étape 2 ci-dessus. Vérifiez également que le client de débogage WSD a complètement imprimé les métadonnées de l’appareil. Les métadonnées de l’appareil commencent par `Metadata for host` et se terminent par `End of metadata` .

Si l’ID d’appareil et les métadonnées de l’appareil s’affichent correctement dans la sortie du client de débogage WSD, l’échec de l’application n’est probablement pas lié aux adresses de transport, au système d’exploitation ou à l’environnement réseau fournis. Remplacez l’hôte et le client génériques par l’hôte et le client personnalisés, puis poursuivez le dépannage en suivant les procédures de la section utilisation de la [journalisation WinHTTP pour vérifier la récupération du trafic](using-winhttp-logging-to-verify-get-traffic.md).

Si l’adresse de l’appareil et les métadonnées de l’appareil n’apparaissent pas dans la sortie du client de débogage WSD, l’échec peut avoir une ou plusieurs des causes suivantes :

-   L’adresse de transport publiée par l’hôte est incorrecte ou incorrecte. Le client de débogage WSD tente d’obtenir les métadonnées de l’appareil à partir de l’URL fournie dans l’élément **XAddrs** d’un message [messages ProbeMatches](probematches-message.md) ou [ResolveMatches](resolvematches-message.md) . L’URL utilisée pour l’échange de métadonnées s’affiche dans la sortie du client de débogage WSD, préfixée par l’expression `Using xAddr` . L’exemple suivant montre le XAddrs utilisé pour l’échange de métadonnées dans la sortie du client de débogage WSD ci-dessus.

    ``` syntax
    Using xAddr: https://[::1]:5357/37f86d35-e6ac-4241-964f-1d9ae46fb366
    ```

    Si les XAddrs spécifiés ne sont pas conformes aux [règles de validation XAddr](xaddr-validation-rules.md), le client de débogage WSD ne peut pas récupérer les métadonnées de l’appareil.

-   L’application s’exécute dans un contexte de sécurité incorrect. Vérifiez que l’application utilise les informations d’identification correctes et que le client et l’hôte disposent des autorisations suffisantes pour accéder au réseau.
-   La configuration du pare-feu est incorrecte. suivez les instructions de la section inspection des Paramètres de l' [adaptateur et du pare-feu](inspecting-adapter-and-firewall-settings.md) pour vérifier que les paramètres du pare-feu Windows sont corrects et qu’aucune autre règle ne supprime les paquets. Le client et l’hôte peuvent également être copiés sur un ordinateur « initial » (l’un avec une installation de système d’exploitation par défaut qui n’a jamais été jointe à un domaine) afin de tenter de reproduire l’échec.
-   Une stratégie IPSec bloque l’application. Copiez le client et l’hôte sur un ordinateur qui n’est pas soumis aux stratégies IPSec et essayez de reproduire l’échec.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Procédures de diagnostic WSDAPI](wsdapi-diagnostic-procedures.md)
</dt> <dt>

[Résolution des problèmes de Prise en main avec WSDAPI](getting-started-with-wsdapi-troubleshooting.md)
</dt> </dl>

 

 



