---
description: Détails des événements de suivi Winsock.
ms.assetid: 246AE0BE-E8E2-4291-8BF4-577F889F055B
title: Événements de suivi Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aeabd2d06741f8dfa1f47b513a09c941ee1490b6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112987"
---
# <a name="winsock-tracing-events"></a>Événements de suivi Winsock

Cette section fournit des informations détaillées sur les détails spécifiques des événements de suivi Winsock.

Le suivi Winsock est une fonctionnalité de résolution des problèmes qui peut être activée dans les binaires de la version commerciale pour suivre certains événements Windows Socket avec une surcharge minimale. Cette fonctionnalité permet de meilleures fonctionnalités de diagnostic pour les développeurs et le support technique. Le suivi d’événements réseau Winsock prend en charge le suivi des opérations de socket pour les applications IPv4 et IPv6. Le suivi des modifications du catalogue Winsock prend en charge le suivi des modifications apportées au catalogue Winsock par les fournisseurs de services en couche (LSP).

> [!Note]  
> Les fournisseurs de services en couche sont déconseillés. À compter de Windows 8 et de Windows Server 2012, utilisez la [plateforme de filtrage Windows](../fwp/windows-filtering-platform-start-page.md).

 

Le suivi Winsock utilise Suivi d’v nements pour Windows (ETW), une fonctionnalité de traçage à usage général et à haut débit fournie par le système d’exploitation. ETW fournit un mécanisme de suivi pour les événements déclenchés par les applications en mode utilisateur et les pilotes de périphérique en mode noyau. ETW permet d’activer et de désactiver la journalisation dynamique, ce qui facilite l’exécution du suivi détaillé dans les environnements de production sans nécessiter de redémarrage ou de redémarrage de l’application. La prise en charge du suivi Winsock à l’aide d’ETW a été ajoutée sur Windows Vista et les versions ultérieures. Pour obtenir des informations générales sur ETW, consultez [améliorer le débogage et le réglage des performances avec ETW](/archive/msdn-magazine/2007/april/event-tracing-improve-debugging-and-performance-tuning-with-etw).

La liste suivante fournit des informations détaillées pour chaque événement de suivi Winsock. Pour plus d’informations sur les événements, cliquez sur le nom de l’événement.



| Nom de l'événement                                                            | Description                                                                               |
|-----------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [**\_création d’événement AFD \_**](afd-event-create.md)                        | Événement de traçage réseau Winsock pour une opération de création de Socket.                            |
| [**fermeture de l' \_ événement AFD \_**](afd-event-close.md)                          | Événement de traçage réseau Winsock pour l’opération de fermeture du Socket.                                 |
| [**\_Installation de ws2help \_ LSP \_ Winsock**](winsock-ws2help-lsp-install.md) | Événement de modification du catalogue Winsock pour une opération d’installation d’un fournisseur de services en couche (LSP). |
| [**Désinstallation de WINSOCK \_ ws2help \_ LSP \_**](winsock-ws2help-lsp-remove.md)   | Événement de modification du catalogue Winsock pour une opération de suppression du fournisseur de services en couche (LSP).      |
| [**Désactivation de WINSOCK \_ ws2help \_ LSP \_**](winsock-ws2help-lsp-disable.md) | Événement de modification du catalogue Winsock pour une opération de désactivation du fournisseur de services en couche (LSP).      |
| [**Réinitialisation de WINSOCK \_ ws2help \_ LSP \_**](winsock-ws2help-lsp-reset.md)     | Événement de modification du catalogue Winsock pour une opération de réinitialisation du catalogue Winsock.                       |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Améliorer le débogage et le réglage des performances à l'aide du suivi ETW](/archive/msdn-magazine/2007/april/event-tracing-improve-debugging-and-performance-tuning-with-etw)
</dt> <dt>

[Suivi Winsock](winsock-tracing.md)
</dt> <dt>

[Niveaux de suivi Winsock](winsock-tracing-levels.md)
</dt> <dt>

[Contrôle du suivi Winsock](control-of-winsock-tracing.md)
</dt> <dt>

[Détails du suivi d’événements réseau Winsock](winsock-tracing-event-details.md)
</dt> <dt>

[Détails du suivi de modification du catalogue Winsock](winsock-layered-service-provider-tracing-event-details.md)
</dt> </dl>

 

 
