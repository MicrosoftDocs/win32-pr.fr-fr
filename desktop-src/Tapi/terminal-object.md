---
description: Dans TAPI version 3,0 et versions ultérieures, le modèle objet TAPI utilise des objets terminaux pour représenter la source ou le récepteur d’un flux de média associé à une session d’appel ou de communication.
ms.assetid: 0d96f229-76c0-46a3-bc4b-6f558b9956c6
title: Objet terminal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2568d3c6f047fec8ca46b3b7d56e5026b61a1113
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106535716"
---
# <a name="terminal-object"></a>Objet terminal

Dans TAPI version 3,0 et versions ultérieures, le modèle objet TAPI utilise des objets terminaux pour représenter la source ou le récepteur d’un flux de média associé à une session d’appel ou de communication. Ce modèle objet permet à une application de spécifier, à un niveau détaillé, le mode de traitement des médias sur un appel. Ce modèle permet également de sélectionner simultanément plusieurs terminaux. par exemple, un appel peut être généré sur un haut-parleur et enregistré simultanément.

L’objet terminal représente une source ou un convertisseur, tel qu’un microphone ou un intervenant. Une application choisit parmi les terminaux disponibles en fonction de la direction du support et du type ou des types impliqués dans une session de communication. Chaque flux de média associé est ensuite sélectionné sur le terminal approprié afin de démarrer la diffusion en continu.

Les terminaux sont normalement implémentés par un fournisseur de services de média (MSP) et les objets Terminal Server ne sont pas disponibles si aucun MSP n’est associé à une session de communication. Une exception est qu’avec Windows 2000 SP1 et versions ultérieures, une application peut implémenter une forme de [Terminal enfichable](pluggable-terminals.md). Cela permet à un serveur de conférence de créer des terminaux de pontage afin que les clients H.323 non-Windows 2000 SP1 ou non multicast puissent être ajoutés aux conférences de multidiffusion SDP/IP multifournisseurs TAPI 3.

Chaque terminal appartient à une [classe de terminal](terminal-class.md). Une classe de terminal représente un ensemble de fonctionnalités source ou de rendu. Par exemple, un terminal mappé à un ensemble de haut-parleurs audio est identifié comme CLSID \_ SpeakersTerminal et le fournisseur de services devrait implémenter le contrôle du volume. TAPI 3 définit un ensemble de classes de terminal, un MSP peut définir des classes supplémentaires et une application peut inscrire de nouvelles classes de terminal. Un identificateur global unique (GUID) est affecté à chaque classe de terminal.

Du point de vue d’une application, un terminal est décrit par son type et son [sens](/windows/desktop/api/Tapi3if/ne-tapi3if-terminal_direction)de [Terminal](/windows/desktop/api/Tapi3if/ne-tapi3if-terminal_type) . Le type peut être statique ou dynamique. Un terminal statique est mappé au matériel, tel qu’un téléphone ou un microphone. Un terminal dynamique est mappé à un objet transitoire, tel qu’un fichier ou une fenêtre vidéo. La direction indique si un terminal donné est une source ou un convertisseur.

Les fonctionnalités d’un objet terminal donné peuvent varier considérablement en fonction de la paire de fournisseurs de services en cours d’utilisation. Le MSP d’un appareil spécialisé peut implémenter une interface avec des méthodes appropriées à cet appareil. Cette interface peut être agrégée sur l’objet terminal et les méthodes mises à la disposition d’une application. Pour plus d’informations et de documents de référence, consultez la documentation du fournisseur de services multimédia.

Pour plus d’informations sur les interfaces terminal et les méthodes implémentées par TAPI 3, consultez [interfaces d’objets Terminal Server](terminal-object-interfaces.md).

Si les auteurs d’un fournisseur de services multimédia utilisent les classes de base MSP, ils peuvent implémenter certaines fonctionnalités de terminal de diffusion multimédia en continu.

Pour plus d’informations et pour obtenir des exemples de code illustrant l’utilisation d’un objet terminal, consultez [passer un appel](make-a-call.md) et [recevoir un appel](receive-a-call.md).

**Windows XP :** Pour plus d’informations sur la façon dont l’objet Terminal Server a été développé sous Windows XP, consultez [terminaux de fichiers](file-terminals.md), [terminaux multipiste](multitrack-terminals.md)et [terminaux enfichables](pluggable-terminals.md).

Pour plus d’informations et d’exemples de code, consultez [utilisation de terminaux de fichiers](using-file-terminals.md), utilisation de [terminaux multipiste et mécanisme de sélection par défaut](using-multitrack-terminals-and-the-default-selection-mechanism.md), et [inscription de terminal enfichable](pluggable-terminal-registration.md).

 

 



