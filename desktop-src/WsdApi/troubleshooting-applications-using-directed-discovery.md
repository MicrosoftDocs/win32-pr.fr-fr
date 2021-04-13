---
description: Les applications qui utilisent la découverte dirigée envoient des messages de sondage via HTTP ou HTTPs pour découvrir des appareils.
ms.assetid: 599f5962-da91-4688-b333-a784f06581ed
title: Dépannage des applications WSDAPI à l’aide de la découverte dirigée
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a34ebec44c58545c65a4ff04941c5f98c9bc047d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528575"
---
# <a name="troubleshooting-wsdapi-applications-using-directed-discovery"></a>Dépannage des applications WSDAPI à l’aide de la découverte dirigée

Les applications qui utilisent la découverte dirigée envoient des messages de [sondage](probe-message.md) via HTTP ou HTTPS pour découvrir des appareils. Les messages [messages ProbeMatches](probematches-message.md) correspondants envoyés en réponse sont également envoyés via HTTP ou HTTPS. La découverte dirigée peut être lancée par l’Assistant Ajout d’imprimante, un client de découverte de fonction ou une application WSDAPI. Les messages de sonde et messages ProbeMatches sont structurellement identiques à ceux envoyés via UDP. Les messages sont préfixés avec les en-têtes HTTP ou HTTPs appropriés.

Les procédures de diagnostic suivantes doivent être utilisées (dans l’ordre) pour aider à identifier les problèmes liés à une application à l’aide de la découverte dirigée.

**Pour dépanner une application WSDAPI à l’aide de la découverte dirigée**

1.  [Inspectez les paramètres de l’adaptateur et du pare-feu](inspecting-adapter-and-firewall-settings.md).
2.  [Utilisez un hôte et un client génériques pour l’échange de métadonnées http](using-a-generic-host-and-client-for-http-metadata-exchange.md).
3.  [Utilisez la journalisation WinHTTP pour vérifier le trafic d’extraction](using-winhttp-logging-to-verify-get-traffic.md).
4.  [Inspectez les traces réseau d’une application à l’aide de la découverte dirigée](inspecting-network-traces-for-applications-using-directed-discovery.md).

Si la source du problème ne peut pas être identifiée à l’aide des procédures de diagnostic ci-dessus, suivez les instructions de la procédure d' [activation du suivi wsdapi](enabling-wsdapi-tracing.md) et contactez le support Microsoft.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Résolution des problèmes de Prise en main avec WSDAPI](getting-started-with-wsdapi-troubleshooting.md)
</dt> <dt>

[Résolution des problèmes liés à l’Assistant Ajout d’imprimante](troubleshooting-the-add-printer-wizard.md)
</dt> <dt>

[Dépannage des applications WSDAPI](troubleshooting-wsdapi-applications.md)
</dt> </dl>

 

 



