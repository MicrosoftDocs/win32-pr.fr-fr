---
description: Suivi Winsock
ms.assetid: 0c430fc2-28e7-4537-a887-4c36d24fedee
title: Suivi Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb2d9593f4c2cea47e722075f1611151fb276cdf2646a2c9898a9c8d7d156098
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118321669"
---
# <a name="winsock-tracing"></a>Suivi Winsock

## <a name="introduction"></a>Introduction

le suivi Winsock est une fonctionnalité de résolution des problèmes qui peut être activée dans les binaires de la version commerciale pour suivre certains événements de socket Windows avec une surcharge minimale. l’objectif de l’ajout d’un suivi de la vente au détail à Windows sockets permet d’améliorer les fonctionnalités de diagnostic pour les développeurs et le support technique. Le suivi d’événements réseau Winsock prend en charge le suivi des opérations de socket pour les applications IPv4 et IPv6. Le suivi des modifications du catalogue Winsock prend en charge le suivi des modifications apportées au catalogue Winsock par les fournisseurs de services en couche (LSP). le suivi Winsock est pris en charge sur Windows Vista et versions ultérieures.

> [!Note]  
> Les fournisseurs de services en couche sont déconseillés. à partir de Windows 8 et Windows Server 2012, utilisez la [plateforme de filtrage Windows](../fwp/windows-filtering-platform-start-page.md).

 

Lorsqu’une erreur inattendue se produit sur un socket, le principal indice pour diagnostiquer le problème est le code d’erreur renvoyé. Très souvent, le code d’erreur retourné n’explique pas pourquoi l’erreur s’est produite, en particulier lorsque l’erreur est initiée par le transport réseau sous-jacent. Le suivi Winsock fournit un niveau de suivi plus détaillé qui peut consigner des informations supplémentaires pour détecter la corruption de la mémoire tampon et les applications mal écrites.

le suivi Winsock utilise Suivi d’v nements pour Windows (ETW), une fonctionnalité de traçage à usage général et à haut débit fournie par le système d’exploitation. À l’aide d’un mécanisme de mise en mémoire tampon et de journalisation implémenté dans le noyau, ETW fournit un mécanisme de suivi pour les événements déclenchés par les applications en mode utilisateur et les pilotes de périphérique en mode noyau. En outre, ETW vous donne la possibilité d’activer et de désactiver la journalisation dynamique, ce qui facilite l’exécution du suivi détaillé dans les environnements de production sans nécessiter de redémarrage ou de redémarrage de l’application. Le mécanisme de journalisation utilise des mémoires tampons écrites sur le disque par un thread d’écriture asynchrone. Cela permet aux applications serveur à grande échelle d’écrire des événements avec une perturbation minimale. ETW a été introduit pour la première fois sur Windows 2000. la prise en charge du suivi Winsock à l’aide d’ETW a été ajoutée sur Windows Vista et versions ultérieures. Pour obtenir des informations générales sur ETW, consultez [améliorer le débogage et le réglage des performances avec ETW](/archive/msdn-magazine/2007/april/event-tracing-improve-debugging-and-performance-tuning-with-etw).

Le suivi Winsock ne peut être activé qu’au niveau du système d’exploitation pour tous les processus et threads exécutés sur un ordinateur. Le suivi Winsock ne peut actuellement pas être activé pour un seul processus ou thread. Lorsque le suivi d’événements réseau Winsock est activé, toutes les applications de socket (IPv4 et IPv6) sont suivies sur un ordinateur.

Les rubriques suivantes décrivent le suivi Winsock plus en détail :

-   [Niveaux de suivi Winsock](winsock-tracing-levels.md)
-   [Contrôle du suivi Winsock](control-of-winsock-tracing.md)
-   [Détails du suivi d’événements réseau Winsock](winsock-tracing-event-details.md)
-   [Détails du suivi de modification du catalogue Winsock](winsock-layered-service-provider-tracing-event-details.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Améliorer le débogage et le réglage des performances à l'aide du suivi ETW](/archive/msdn-magazine/2007/april/event-tracing-improve-debugging-and-performance-tuning-with-etw)
</dt> <dt>

[Fonctionnalités de débogage et de suivi](debug-and-trace-facilities-2.md)
</dt> </dl>

 

 
