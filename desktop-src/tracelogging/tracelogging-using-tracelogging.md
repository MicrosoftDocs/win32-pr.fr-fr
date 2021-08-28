---
title: Utilisation de TraceLogging
description: Les rubriques suivantes fournissent un démarrage rapide TraceLogging pour le code natif et managé, avec des exemples.
ms.assetid: CEC57517-7A0E-45AA-85F7-F358AE51EF4A
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be48ff03e1efe37b2ed18314557514c81715ea7e36dacfda309f473522dac39a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118966488"
---
# <a name="using-tracelogging"></a>Utilisation de TraceLogging

Les rubriques suivantes fournissent un démarrage rapide TraceLogging pour le code natif et managé, avec des exemples.

## <a name="prerequisites"></a>Prérequis

-   Windows 10 Le kit de développement logiciel (SDK) est requis pour écrire un fournisseur en mode utilisateur
-   Windows Driver Kit (WDK) est requis pour écrire un fournisseur en mode noyau

## <a name="in-this-section"></a>Contenu de cette section



| Rubrique                                                                                                        | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|--------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [TraceLogging C/C++ Démarrage rapide](tracelogging-native-quick-start.md)<br/>                             | La section suivante décrit les étapes de base requises pour ajouter TraceLogging au code en mode utilisateur natif. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| [Démarrage rapide managé TraceLogging](tracelogging-managed-quick-start.md)<br/>                          | La section suivante décrit les étapes de base requises pour ajouter TraceLogging à du code managé.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| [Enregistrer et afficher les événements TraceLogging](tracelogging-record-and-display-tracelogging-events.md)<br/> | enregistrez les événements TraceLogging avec l’enregistreur de performances Windows (WPR) et affichez-les à l’aide de l’analyseur de performances Windows (WPA).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| [Exemples de Tracelogging C/C++](tracelogging-c-cpp-tracelogging-examples.md)<br/>                       | Cette rubrique contient des exemples Tracelogging C/C++.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| [Exemples .NET Tracelogging](tracelogging-net-examples.md)<br/>                                       | Cette rubrique contient un exemple de code managé Tracelogging qui illustre comment enregistrer un événement uniquement lorsque le niveau de détail de la session est détaillé et comment enregistrer des données d’événement structurées.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                 |
| [exemple de journalisation plateforme Windows universelle](universal-windows-platform-logging-examples.md)<br/>     | Cet exemple montre comment utiliser les API de journalisation dans le Windows. L’espace de noms Foundation. Diagnostics, notamment LoggingChannel, LoggingActivity, LoggingSession et FileLoggingSession. ces classes sont conçues pour la journalisation des diagnostics au sein d’une application Windows. Ces API ont été ajoutées dans Windows 8.1. <br/> les api LoggingChannel et LoggingActivity ont été étendues dans Windows 10 pour prendre en charge l’écriture d’événements complexes à l’aide de l’encodage d’événements TraceLogging.<br/> l’exemple de journalisation plateforme Windows universelle peut être téléchargé à partir de [GitHub](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/Logging).<br/> |



 

Exemples TraceLogging.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[TraceLogging pour les composants et les pilotes en mode noyau](/windows-hardware/drivers/devtest/tracelogging-for-kernel-mode-drivers-and-components)
</dt> </dl>

 

