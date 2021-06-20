---
description: Découvrez les concepts et les fonctionnalités des API audio de base de Windows Vista et comment les utiliser dans la programmation d’applications.
ms.assetid: 825c7cd7-dc66-47b6-a1b6-d10101daebb3
title: Guide de programmation audio de base
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02f02e27206c70cca69abf263cfa49dfd439c480
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112405872"
---
# <a name="core-audio-programming-guide"></a>Guide de programmation audio de base

Cette section du guide explique les concepts et les fonctionnalités des API audio de base de Windows Vista et décrit comment les utiliser dans la programmation d’applications.

Cette section contient les rubriques suivantes :



| Rubrique                                                                                                                      | Description                                                                                                                                                                                                  |
|----------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Composants audio en mode utilisateur](user-mode-audio-components.md)                                                               | Via les interfaces de bas niveau dans les API audio de base, un client peut accéder aux composants système qui gèrent et combinent des flux audio.                                                                        |
| [PUMA (Protected user mode audio)](protected-user-mode-audio--puma-.md)                                                   | Décrit les mises à jour apportées à PUMA (Protected user mode audio), le moteur audio en mode utilisateur dans l’environnement protégé (PE), qui fournit un environnement plus sûr pour le traitement et le rendu audio.              |
| [Périphériques de point de terminaison audio](audio-endpoint-devices.md)                                                                       | Un périphérique de point de terminaison audio est une abstraction logicielle qui permet des interactions conviviales avec les périphériques audio tels que les microphones et les orateurs.                                                              |
| [Sessions audio](audio-sessions.md)                                                                                       | Une session audio est une abstraction logicielle qui permet à un client de gérer une collection de flux audio associés en tant qu’unité unique.                                                                           |
| [Contrôles de volume](volume-controls.md)                                                                                     | Le système intègre ses paramètres de volume basés sur des stratégies avec les paramètres de volume de l’utilisateur de manière logique et cohérente.                                                                                      |
| [Gestion de flux](stream-management.md)                                                                                 | L’API de session audio Windows (WASAPI) fournit à un client un ensemble complet de méthodes pour créer et gérer des flux audio.                                                                             |
| [Topologies d’appareils](device-topologies.md)                                                                                 | L’API DeviceTopology permet à un client de découvrir les contrôles audio qui se trouvent le long des différents chemins de données dans le matériel audio.                                                                          |
| [Utilisation de l’interface IKsControl pour accéder aux propriétés audio](using-the-ikscontrol-interface-to-access-audio-properties.md) | Une application audio spécialisée peut nécessiter l’utilisation de l’interface IKsControl pour accéder aux propriétés d’un adaptateur audio.                                                                                     |
| [Interopérabilité avec les API audio héritées](interoperability-with-legacy-audio-apis.md)                                     | Les principales fonctionnalités des API audio de base dans Windows Vista peuvent être incorporées dans des applications existantes qui utilisent DirectSound, DirectShow et les fonctions **waveOutXxx** et **waveInXxx** de Windows Multimedia. |
| [Son spatial](spatial-sound.md)                                                                                         | Fournit des conseils pour l’utilisation de Windows Sonic, la solution au niveau de la plate-forme de Microsoft pour la prise en charge des sons spatiaux sur Xbox et Windows, ce qui permet l’entourage et l’élévation (au-dessus ou en dessous de l’écouteur) des signaux audio. |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[API audio principales](core-audio-apis-in-windows-vista.md)
</dt> </dl>

 

 



