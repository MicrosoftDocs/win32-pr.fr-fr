---
description: À propos des API audio Windows Core
ms.assetid: 657cf75f-3d72-4a5f-ae29-299e826b2b86
title: À propos des API audio Windows Core
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30763d70bae4340436145a303763c0aad57171f5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861694"
---
# <a name="about-the-windows-core-audio-apis"></a>À propos des API audio Windows Core

Cette documentation fournit des informations sur les API audio principales pour la famille de systèmes d’exploitation Microsoft Windows.

Les API audio de base ont été introduites dans Windows Vista. Il s’agit d’un nouvel ensemble de composants audio en mode utilisateur qui fournit aux applications clientes des fonctionnalités audio améliorées. Ces fonctionnalités sont les suivantes :

-   Diffusion en continu de données audio résistante aux problèmes et à faible latence.
-   Fiabilité améliorée (de nombreuses fonctions audio ont été déplacées du mode noyau au mode utilisateur).
-   Amélioration de la sécurité (le traitement du contenu audio protégé s’effectue dans un processus sécurisé et à faibles privilèges).
-   Attribution de rôles spécifiques à l’ensemble du système (console, multimédia et communications) à des périphériques audio individuels.
-   Abstraction logicielle des appareils de point de terminaison audio (par exemple, haut-parleurs, casque et microphones) manipulés directement par l’utilisateur.

Les API audio de base ont été améliorées dans Windows 7. Pour plus d’informations sur les améliorations et les nouvelles fonctionnalités ajoutées, consultez [Nouveautés des API audio principales dans Windows 7](what-s-new-for-core-audio-apis-in-windows-7.md).

Cette documentation décrit les principales API audio. Ces API servent de base aux API de niveau supérieur suivantes :

-   DirectSound
-   DirectMusic
-   Fonctions **waveXxx** et **mixerXxx** Windows Multimedia
-   Media Foundation

Ces API de niveau supérieur utilisent les API audio de base pour partager l’accès aux périphériques audio. Media Foundation est une nouveauté de Windows Vista, tandis que DirectSound, DirectMusic et les fonctions **waveXxx** et **mixerXxx** sont prises en charge dans Windows 98, Windows Millennium Edition et Windows 2000 et versions ultérieures.

La plupart des applications audio communiquent avec les API de niveau supérieur au lieu de communiquer directement avec les API audio de base. Voici quelques exemples d’applications qui utilisent des API de niveau supérieur :

-   Lecteurs multimédias
-   Lecteurs de DVD
-   Jeux
-   Applications d’entreprise, telles que Microsoft Office PowerPoint, qui lisent des fichiers audio

En règle générale, ces applications communiquent avec les API DirectSound ou Media Foundation.

La communication directe avec les API audio de base peut ne pas convenir à de nombreuses applications audio à usage général. Par exemple, les API audio de base requièrent des flux audio pour utiliser des formats de données natifs d’un périphérique audio. Toutefois, les développeurs de logiciels tiers qui développent les types de produits suivants peuvent nécessiter les fonctionnalités spéciales des API audio de base :

-   Applications audio professionnelles (« Pro Audio »)
-   Applications de communication en temps réel (RTC)
-   API audio tierces

Une application « Pro audio » ou RTC peut avoir besoin d’un accès direct aux fonctionnalités de bas niveau des API audio de base pour atteindre une latence minimale en obtenant un accès exclusif au matériel audio. Une API audio tierce peut nécessiter un accès direct aux API audio de base pour implémenter un ensemble de fonctionnalités qui ne sont peut-être pas entièrement prises en charge par une seule API audio de haut niveau fournie avec Windows.

Une application qui utilise une API audio héritée pour lire ou enregistrer du contenu audio peut nécessiter des fonctionnalités supplémentaires qui ne sont pas prises en charge par l’API audio héritée, mais qui sont prises en charge par les API audio de base. Dans de nombreux cas, l’application peut accéder à ces fonctionnalités directement par le biais des API audio de base, qui peuvent être utilisées conjointement avec l’API audio héritée.

Les API audio principales sont les suivantes :

-   [API de périphérique multimédia (MMDevice)](mmdevice-api.md). Les clients utilisent cette API pour énumérer les périphériques de point de terminaison audio dans le système.
-   [API de session audio Windows (WASAPI)](wasapi.md). Les clients utilisent cette API pour créer et gérer des flux audio vers et depuis des appareils de point de terminaison audio.
-   [API DeviceTopology](devicetopology-api.md). Les clients utilisent cette API pour accéder directement aux fonctionnalités topologiques (par exemple, les contrôles de volume et les multiplexeurs) qui se trouvent le long des chemins de données à l’intérieur des périphériques matériels des adaptateurs audio.
-   [API EndpointVolume](endpointvolume-api.md). Les clients utilisent cette API pour accéder directement aux contrôles du volume sur les périphériques de point de terminaison audio. Cette API est principalement utilisée par les applications qui gèrent des flux audio en mode exclusif.

Ces API prennent en charge la notion conviviale d’un périphérique de point de terminaison, qui est décrite dans [périphériques de point de terminaison audio](audio-endpoint-devices.md).

Microsoft ne prévoit pas de créer les API audio de base décrites ici pour une utilisation avec les versions antérieures de Windows, notamment Microsoft Windows Server 2003, Windows XP, Windows Millennium Edition, Windows 2000 et Windows 98.

Cette vue d’ensemble contient les rubriques suivantes.



| **Rubrique**                                                                                      | **Description**                                                                           |
|------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [Nouveautés des API audio principales dans Windows 7](what-s-new-for-core-audio-apis-in-windows-7.md) | Résume les nouvelles fonctionnalités et les améliorations apportées aux API audio principales.                   |
| [Fichiers d’en-tête et composants système](header-files-and-system-components.md)                   | Décrit les fichiers d’en-tête et les composants système pour les API audio principales.                 |
| [Exemples de SDK qui utilisent les API audio principales](sdk-samples-that-use-the-core-audio-apis.md)       | Répertorie les exemples de la SDK Windows qui utilisent les API audio de base.                        |




 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[API audio principales](core-audio-apis-in-windows-vista.md)
</dt> </dl>

 

 



