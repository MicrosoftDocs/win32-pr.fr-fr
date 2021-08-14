---
description: Le tableau suivant répertorie les classes pour les consommateurs permanents préinstallés par WMI.
ms.assetid: 1239ea25-2835-4546-b66d-20a83704653e
ms.tgt_platform: multiple
title: Classes de consommateur standard
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f89463a459adb3dd800f77564002366c7500a2abbaa6010444ba7890802d5a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118315276"
---
# <a name="standard-consumer-classes"></a>Classes de consommateur standard

Le tableau suivant répertorie les classes pour les consommateurs permanents préinstallés par WMI. Vous pouvez créer des instances de ces classes pour fournir à la classe de consommateur permanente la possibilité de fournir le consommateur logique qui répond lorsqu’il est déclenché par les événements spécifiés dans le filtre. Par exemple, utilisez la classe [**ActiveScriptEventConsumer**](activescripteventconsumer.md) pour définir le script qui s’exécute lorsqu’un événement spécifié se produit.

Pour plus d’informations, consultez [surveillance et réponse aux événements avec des consommateurs standard](monitoring-and-responding-to-events-with-standard-consumers.md) et [surveillance des événements](monitoring-events.md).



| Classe                                                                        | Description                                                                                                                                                                                                                                           |
|------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ActiveScriptEventConsumer**](activescripteventconsumer.md)               | Exécute un script prédéfini dans un langage de script arbitraire lorsqu’un événement lui est remis.<br/> Exemple : [exécution d’un script basé sur un événement](running-a-script-based-on-an-event.md)<br/>                                         |
| [**CommandLineEventConsumer**](commandlineeventconsumer.md)                 | Lance un processus arbitraire dans le contexte du système local lorsqu’un événement lui est remis.<br/> Exemple : [exécution d’un programme à partir de la ligne de commande en fonction d’un événement](running-a-program-from-the-command-line-based-on-an-event.md)<br/> |
| [**LogFileEventConsumer**](logfileeventconsumer.md)                         | Écrit des chaînes personnalisées dans un fichier journal texte lorsque des événements lui sont remis.<br/> Exemple : [écriture dans un fichier journal basé sur un événement](writing-to-a-log-file-based-on-an-event.md)<br/>                                                   |
| [**NTEventLogEventConsumer**](nteventlogeventconsumer.md)                   | enregistre un message spécifique dans le journal des événements Windows lorsqu’un événement lui est remis.<br/> Exemple : [journalisation dans le journal des événements NT en fonction d’un événement](logging-to-nt-event-log-based-on-an-event.md)<br/>                                          |
| [**ScriptingStandardConsumerSetting**](scriptingstandardconsumersetting.md) | Fournit des données d’inscription communes à toutes les instances de la classe [**ActiveScriptEventConsumer**](activescripteventconsumer.md) .<br/>                                                                                                            |
| [**SMTPEventConsumer**](smtpeventconsumer.md)                               | Envoie un message électronique à l’aide du protocole SMTP à chaque fois qu’un événement lui est remis.<br/> Exemple : [envoi d’un E-mail basé sur un événement](sending-e-mail-based-on-an-event.md)<br/>                                                                       |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Événements d’analyse](monitoring-events.md)
</dt> <dt>

[Réception d’événements à tout moment](receiving-events-at-all-times.md)
</dt> <dt>

[Exécution d’un script basé sur un événement](running-a-script-based-on-an-event.md)
</dt> <dt>

[Envoi de courrier électronique à partir d’un événement](sending-e-mail-based-on-an-event.md)
</dt> </dl>

 

 




