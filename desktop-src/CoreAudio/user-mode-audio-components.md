---
description: Composants audio User-Mode
ms.assetid: b240b629-5bb6-4b07-95be-8ca5a14a3567
title: Composants audio User-Mode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18715db2d32be3c4a70182571028acbfca411539
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861293"
---
# <a name="user-mode-audio-components"></a>Composants audio User-Mode

Dans Windows Vista, les API audio principales jouent le rôle de base du sous-système audio en mode utilisateur. Les API audio de base sont implémentées sous la forme d’une couche fine de composants système en mode utilisateur qui séparent les clients en mode utilisateur des pilotes audio en mode noyau et du matériel audio. Les API audio de niveau supérieur, telles que DirectSound et les fonctions multimédias de Windows, accèdent aux périphériques audio via les API audio de base. De plus, certaines applications audio communiquent directement avec les API audio de base.

Les API audio de base prennent en charge la notion conviviale d’un périphérique de point de terminaison audio. Un périphérique de point de terminaison audio est une abstraction logicielle qui représente un appareil physique que l’utilisateur manipule directement. Les haut-parleurs, les casques et les microphones sont des exemples d’appareils de point de terminaison audio. Pour plus d’informations, consultez [périphériques de point de terminaison audio](audio-endpoint-devices.md).

Le diagramme suivant montre les API audio principales et leurs relations avec les autres composants audio en mode utilisateur de Windows Vista.

![diagramme des composants de rendu audio en mode utilisateur](images/fig1.jpg)

Par souci de simplicité, le diagramme ci-dessus affiche uniquement un chemin de données de rendu audio vers l’appareil de point de terminaison : le diagramme n’affiche pas de chemin de données de capture audio. Les API audio principales incluent l' [API MMDevice](mmdevice-api.md), [WASAPI](wasapi.md), l' [API DeviceTopology](devicetopology-api.md)et l' [API EndpointVolume](endpointvolume-api.md), qui sont implémentées dans le Audioses.dll et Mmdevapi.dll les modules système en mode utilisateur.

Comme indiqué dans le diagramme précédent, les API audio principales constituent une base pour les API de niveau supérieur suivantes :

-   Media Foundation
-   Fonctions **waveXxx** et **mixerXxx** Windows Multimedia
-   DirectSound
-   DirectMusic

DirectSound, les fonctions audio Windows Multimedia et Media Foundation (via son convertisseur audio de streaming, ou le composant SAR) communiquent directement avec les API audio de base. DirectMusic communique avec les API audio de base indirectement via DirectSound.

Un client de WASAPI transmet des données à un appareil de point de terminaison par le biais d’une *mémoire tampon de point de terminaison*. Les composants matériels et logiciels système gèrent le déplacement des données de la mémoire tampon du point de terminaison vers l’appareil de point de terminaison d’une manière largement transparente pour le client. En outre, pour un périphérique de point de terminaison qui se connecte à un adaptateur audio avec la détection de présence jack-Jack, le client peut créer une mémoire tampon de point de terminaison uniquement pour un périphérique de point de terminaison qui est physiquement présent. Pour plus d’informations sur la détection de la présence des jacks, consultez [périphériques de point de terminaison audio](audio-endpoint-devices.md).

Le diagramme précédent montre deux types de tampons de point de terminaison. Si un client de WASAPI ouvre un flux en *mode partagé*, le client écrit des données audio dans le tampon de point de terminaison et le moteur audio Windows lit les données à partir de la mémoire tampon. Dans ce mode, le client partage le matériel audio avec d’autres applications qui s’exécutent dans d’autres processus. Le moteur audio mélange les flux de ces applications et lit le mélange résultant via le matériel. Le moteur audio est un composant système en mode utilisateur (Audiodg.dll) qui effectue toutes ses opérations de traitement de flux dans le logiciel. En revanche, si un client ouvre un flux en *mode exclusif*, le client dispose d’un accès exclusif au matériel audio. En règle générale, seul un petit nombre d’applications « Pro audio » ou RTC nécessitent le mode exclusif. Bien que le diagramme affiche à la fois les flux en mode partagé et en mode exclusif, un seul de ces deux flux (et sa mémoire tampon de point de terminaison correspondante) existe, selon que le client ouvre ou non le flux en mode partagé ou en mode exclusif.

En mode exclusif, le client peut choisir d’ouvrir le flux dans n’importe quel format audio pris en charge par l’appareil de point de terminaison. En mode partagé, le client doit ouvrir le flux au format Mix qui est actuellement utilisé par le moteur audio (ou un format similaire au format Mix). Les flux d’entrée du moteur audio et la combinaison de sortie du moteur sont tous dans ce format.

Dans Windows 7, une nouvelle fonctionnalité appelée *mode à faible latence* a été ajoutée pour les flux en mode partage. Dans ce mode, le moteur audio s’exécute en mode par extraction, ce qui réduit considérablement la latence. Cela est très utile pour les applications de communication qui nécessitent une faible latence de flux audio pour accélérer la diffusion en continu.

Les applications qui gèrent des flux audio à faible latence peuvent utiliser le service Planificateur de classes multimédias (MMCSS) dans Windows Vista pour augmenter la priorité des threads d’application qui accèdent aux mémoires tampons de point de terminaison. MMCSS permet aux applications audio de s’exécuter avec une priorité élevée sans refuser les ressources du processeur aux applications de faible priorité. MMCSS affecte une priorité à un thread en fonction de son nom de tâche. Par exemple, Windows Vista prend en charge les noms de tâches « audio » et « audio pro » pour les threads qui gèrent des flux audio. Par défaut, la priorité d’un thread « audio Pro » est supérieure à celle d’un thread « audio ». Pour plus d’informations sur MMCSS, consultez la documentation SDK Windows.

Les API audio principales prennent en charge les formats de flux PCM et non-PCM. Toutefois, le moteur audio ne peut mélanger que des flux PCM. Ainsi, seuls les flux en mode exclusif peuvent avoir des formats non-PCM. Pour plus d’informations, consultez [formats de périphérique](device-formats.md).

Le moteur audio s’exécute dans son propre processus protégé, qui est distinct du processus dans lequel l’application s’exécute. Pour prendre en charge un flux en mode partagé, le service audio Windows (la zone intitulée « service audio » dans le diagramme précédent) alloue un tampon de point de terminaison inter-processus accessible à la fois à l’application et au moteur audio. Pour le mode exclusif, la mémoire tampon du point de terminaison réside dans la mémoire qui est accessible à la fois à l’application et au matériel audio.

Le service audio Windows est le module qui implémente la stratégie audio Windows. La stratégie audio est un ensemble de règles internes que le système applique aux interactions entre les flux audio de plusieurs applications qui partagent et rivalisent pour l’utilisation du même matériel audio. Le service audio Windows implémente la stratégie audio en définissant les paramètres de contrôle du moteur audio. Les tâches du service audio sont les suivantes :

-   Assurer le suivi des périphériques audio que l’utilisateur ajoute ou supprime du système.
-   Surveillance des rôles affectés aux périphériques audio dans le système.
-   Gestion des flux audio à partir de groupes de tâches qui produisent des classes similaires de contenu audio (console, multimédia et communications).
-   Contrôle du niveau de volume du flux de sortie combiné (« mixage secondaire ») pour chacun des différents types de contenu audio.
-   En informant le moteur audio sur les éléments de traitement dans les chemins de données pour les flux audio.

Dans certaines versions de Windows, le service audio Windows est désactivé par défaut et doit être explicitement activé pour que le système puisse lire des données audio.

Dans l’exemple illustré dans le diagramme précédent, l’appareil de point de terminaison est un ensemble de haut-parleurs branchés dans la carte audio. L’application cliente écrit des données audio dans la mémoire tampon du point de terminaison, et le moteur audio gère les détails du transport des données de la mémoire tampon vers l’appareil de point de terminaison.

La zone nommée « pilote audio » dans le diagramme précédent peut être une combinaison de composants de pilote fournis par le système et fournis par le fournisseur. Dans le cas d’une carte audio sur un bus PCI ou PCI Express, le système fournit le pilote de système de classe de port (Portcls.sys), qui implémente un ensemble de pilotes de port pour les différentes fonctions audio de l’adaptateur, et le fabricant de matériel fournit un pilote de carte qui implémente un ensemble de pilotes miniport pour gérer les opérations spécifiques aux périphériques pour les pilotes de port Dans le cas d’un contrôleur audio haute définition et d’un codec sur un bus PCI ou PCI Express, le système fournit le pilote de carte (Hdaudio.sys) et aucun pilote fourni par le fournisseur n’est nécessaire. Dans le cas d’une carte audio sur un bus USB, le système fournit le pilote du système de classe AVStream (Ks.sys) et le pilote audio USB (Usbaudio.sys); là encore, aucun pilote fourni par le fournisseur n’est nécessaire.

Par souci de simplicité, le diagramme ci-dessus affiche uniquement les flux de rendu. Toutefois, les API audio principales prennent également en charge la capture de flux. En mode partagé, plusieurs clients peuvent partager le flux capturé à partir d’un périphérique matériel audio. En mode exclusif, un client dispose d’un accès exclusif au flux capturé à partir de l’appareil.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Guide de programmation](programming-guide.md)
</dt> </dl>

 

 



