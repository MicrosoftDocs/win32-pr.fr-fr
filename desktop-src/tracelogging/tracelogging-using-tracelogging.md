---
title: Utilisation de TraceLogging
description: Les rubriques suivantes fournissent un démarrage rapide TraceLogging pour le code natif et managé, avec des exemples.
ms.assetid: CEC57517-7A0E-45AA-85F7-F358AE51EF4A
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e331f5ebec3d7eb8ce9c50d3e9d92f747bf76414
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382704"
---
# <a name="using-tracelogging"></a>Utilisation de TraceLogging

Les rubriques suivantes fournissent un démarrage rapide TraceLogging pour le code natif et managé, avec des exemples.

## <a name="prerequisites"></a>Prérequis

-   Le kit de développement logiciel (SDK) Windows 10 est requis pour écrire un fournisseur en mode utilisateur
-   Windows Driver Kit (WDK) est requis pour écrire un fournisseur en mode noyau

## <a name="in-this-section"></a>Contenu de cette section



| Rubrique                                                                                                        | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|--------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [TraceLogging C/C++ Démarrage rapide](tracelogging-native-quick-start.md)<br/>                             | La section suivante décrit les étapes de base requises pour ajouter TraceLogging au code en mode utilisateur natif. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| [Démarrage rapide managé TraceLogging](tracelogging-managed-quick-start.md)<br/>                          | La section suivante décrit les étapes de base requises pour ajouter TraceLogging à du code managé.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| [Enregistrer et afficher les événements TraceLogging](tracelogging-record-and-display-tracelogging-events.md)<br/> | Enregistrez les événements TraceLogging avec l’enregistreur de performances Windows (WPR) et affichez-les à l’aide de l’analyseur de performances Windows (WPA).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| [Exemples de Tracelogging C/C++](tracelogging-c-cpp-tracelogging-examples.md)<br/>                       | Cette rubrique contient des exemples Tracelogging C/C++.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| [Exemples .NET Tracelogging](tracelogging-net-examples.md)<br/>                                       | Cette rubrique contient un exemple de code managé Tracelogging qui illustre comment enregistrer un événement uniquement lorsque le niveau de détail de la session est détaillé et comment enregistrer des données d’événement structurées.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                 |
| [Exemple de journalisation plateforme Windows universelle](universal-windows-platform-logging-examples.md)<br/>     | Cet exemple montre comment utiliser les API de journalisation dans l’espace de noms Windows. Foundation. Diagnostics, notamment LoggingChannel, LoggingActivity, LoggingSession et FileLoggingSession. Ces classes sont conçues pour la journalisation des diagnostics dans une application Windows. Ces API ont été ajoutées dans Windows 8.1. <br/> Les API LoggingChannel et LoggingActivity ont été étendues dans Windows 10 pour prendre en charge l’écriture d’événements complexes à l’aide de l’encodage d’événements TraceLogging.<br/> L’exemple de journalisation plateforme Windows universelle peut être téléchargé à partir de [GitHub](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/Logging).<br/> |



 

Exemples TraceLogging.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[TraceLogging pour les composants et les pilotes en mode noyau](/windows-hardware/drivers/devtest/tracelogging-for-kernel-mode-drivers-and-components)
</dt> </dl>

 

