---
description: Cet exemple d’application utilise les API audio de base pour capturer des données audio à partir d’un périphérique d’entrée spécifié par l’utilisateur et les écrit dans un fichier. wav portant un nom unique dans le répertoire actif. Cet exemple illustre la mise en mémoire tampon pilotée par une minuterie.
ms.assetid: 06124b99-89b3-4dfa-b989-a54746ecd697
title: CaptureSharedTimerDriven
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b635462767f22d3e31fe6deaa79b5c00911b378b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127115073"
---
# <a name="capturesharedtimerdriven"></a>CaptureSharedTimerDriven

Cet exemple d’application utilise les API audio de base pour capturer des données audio à partir d’un périphérique d’entrée spécifié par l’utilisateur et les écrit dans un fichier. wav portant un nom unique dans le répertoire actif. Cet exemple illustre la mise en mémoire tampon pilotée par une minuterie.

Cette rubrique contient les sections suivantes.

-   [Description](#description)
-   [Configuration requise](#requirements)
-   [Téléchargement de l’exemple](#downloading-the-sample)
-   [Génération de l'exemple](#building-the-sample)
-   [Exécution de l’exemple](#running-the-sample)
-   [Rubriques connexes](#related-topics)

## <a name="description"></a>Description

Cet exemple illustre les fonctionnalités suivantes.

-   [API MMDevice](mmdevice-api.md) pour l’énumération et la sélection des appareils multimédias.
-   [WASAPI](wasapi.md) pour les opérations de gestion de flux.

## <a name="requirements"></a>Spécifications



| Produit                                                        | Version   |
|----------------------------------------------------------------|-----------|
| [SDK Windows](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | Windows 7 |
| Visual Studio                                                  | 2008      |



 

## <a name="downloading-the-sample"></a>Téléchargement de l’exemple

Cet exemple est disponible aux emplacements suivants.



| Emplacement    | Chemin d’accès/URL                                                                                                  |
|-------------|-----------------------------------------------------------------------------------------------------------|
| Kit de développement logiciel (SDK) Windows | \\Program Files \\ Microsoft sdk \\ Windows \\ v 7.0 \\ samples \\ \\ Audio Multimedia \\ CaptureSharedTimerDriven \\ ... |



 

## <a name="building-the-sample"></a>Génération de l'exemple

Pour générer l’exemple CaptureSharedTimerDriven, procédez comme suit :

1.  ouvrez l’interpréteur de commandes pour le SDK Windows et accédez au répertoire d’exemple CaptureSharedTimerDriven.
2.  exécutez la commande `start WASAPICaptureSharedTimerDriven.sln` dans le répertoire CaptureSharedTimerDriven pour ouvrir le projet WASAPICaptureSharedTimerDriven dans la fenêtre Visual Studio.
3.  À partir de la fenêtre, sélectionnez la configuration de la solution **Debug** ou **Release** , sélectionnez le menu **générer** dans la barre de menus, puis sélectionnez l’option **générer** . si vous n’ouvrez pas Visual Studio à partir du shell CMD pour le kit de développement logiciel (sdk), Visual Studio n’aura pas accès à l’environnement de génération du kit de développement logiciel (sdk). Dans ce cas, l’exemple n’est pas généré, sauf si vous définissez explicitement la variable d’environnement MSSdk, qui est utilisée dans le fichier projet, WASAPICaptureSharedTimerDriven. vcproj.

## <a name="running-the-sample"></a>Exécution de l'exemple

Si vous générez l’application de démonstration avec succès, un fichier exécutable, WASAPICaptureSharedTimerDriven.exe, est généré. Pour l’exécuter, tapez `WASAPICaptureSharedTimerDriven` dans une fenêtre de commande suivie d’arguments obligatoires ou facultatifs. L’exemple suivant montre comment exécuter l’exemple en spécifiant la durée de capture sur le périphérique multimédia par défaut.

`WASAPICaptureSharedTimerDriven.exe -d 20 -multimedia`

Le tableau suivant indique les arguments.

| Argument        | Description                                                |
|-----------------|------------------------------------------------------------|
| -?              | Affiche l’aide.                                                |
| -H              | Affiche l’aide.                                                |
| -l              | Latence de capture audio en millisecondes.                     |
| -d              | Durée de capture audio en secondes.                         |
| -M              | Désactive l’utilisation de MMCSS.                                 |
| -Console        | Utilisez l’appareil de la console par défaut.                            |
| -Communications | Utilisez l’appareil de communication par défaut.                      |
| -multimédia     | Utilisez l’appareil multimédia par défaut.                         |
| -point de terminaison       | Utilisez l’identificateur de point de terminaison spécifié dans la valeur de commutateur. |



 

Si l’application est exécutée sans arguments, elle énumère les périphériques disponibles et invite l’utilisateur à sélectionner un appareil pour la session de capture. La console, la communication et les périphériques multimédias par défaut sont répertoriés suivis des appareils et des identificateurs de point de terminaison. Si aucune durée n’est spécifiée, le flux audio de l’appareil spécifié est capturé pendant 10 secondes. L’application écrit les données capturées dans un fichier. wav portant un nom unique.

CaptureSharedTimerDriven illustre la mise en mémoire tampon pilotée par une minuterie. Dans ce mode, le client doit attendre pendant une période donnée (la moitié de la latence, spécifiée par la valeur du commutateur-d, en millisecondes). Lorsque le client sort de la période de traitement, il extrait le jeu d’exemples suivant du moteur. Avant chaque passage de traitement dans la boucle de mise en mémoire tampon, le client doit déterminer la quantité de données de capture disponibles afin que les données ne saturent pas le tampon de capture. Les données audio capturées à partir de l’appareil spécifié peuvent être traitées en activant la mise en mémoire tampon pilotée par les événements. Ce mode est illustré dans l’exemple [CaptureSharedEventDriven](capturesharedeventdriven.md) .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Exemples de SDK qui utilisent les API audio principales](sdk-samples-that-use-the-core-audio-apis.md)
</dt> </dl>

 

 



