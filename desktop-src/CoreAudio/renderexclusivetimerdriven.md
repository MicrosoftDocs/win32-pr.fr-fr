---
description: Cet exemple d’application utilise les API audio de base pour afficher les données audio sur un périphérique de sortie spécifié par l’utilisateur. Cet exemple illustre la mise en mémoire tampon pilotée par minuterie pour un client de rendu en mode exclusif.
ms.assetid: 9dcfccd2-a709-4b4e-bbb3-4c68a15cce03
title: RenderExclusiveTimerDriven
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb6145f65de3de9425f7ba2f023a669ec0b57a3c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127114785"
---
# <a name="renderexclusivetimerdriven"></a>RenderExclusiveTimerDriven

Cet exemple d’application utilise les API audio de base pour afficher les données audio sur un périphérique de sortie spécifié par l’utilisateur. Cet exemple illustre la mise en mémoire tampon pilotée par minuterie pour un client de rendu en mode exclusif. Pour un flux en mode exclusif, le client partage la mémoire tampon du point de terminaison avec le périphérique audio.

Cette rubrique contient les sections suivantes.

-   [Description](#description)
-   [Configuration requise](#requirements)
-   [Téléchargement de l’exemple](#downloading-the-sample)
-   [Génération de l'exemple](#building-the-sample)
-   [Afficher les fichiers d’exemple](#view-the-sample-files)
-   [Rubriques connexes](#related-topics)

## <a name="description"></a>Description

Cet exemple illustre les fonctionnalités suivantes.

-   [API MMDevice](mmdevice-api.md) pour l’énumération et la sélection des appareils multimédias.
-   WASAPI pour les opérations de gestion de flux.

## <a name="requirements"></a>Spécifications



| Produit                                                        | Version   |
|----------------------------------------------------------------|-----------|
| [SDK Windows](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | Windows 7 |
| Visual Studio                                                  | 2008      |



 

## <a name="downloading-the-sample"></a>Téléchargement de l’exemple

Cet exemple est disponible aux emplacements suivants.



| Emplacement    | Chemin d’accès/URL                                                                                                    |
|-------------|-------------------------------------------------------------------------------------------------------------|
| Kit de développement logiciel (SDK) Windows | \\Program Files \\ Microsoft sdk \\ Windows \\ v 7.0 \\ samples \\ \\ Audio Multimedia \\ RenderExclusiveTimerDriven \\ ... |



 

## <a name="building-the-sample"></a>Génération de l'exemple

Pour générer l’exemple RenderExclusiveTimerDriven, procédez comme suit :

1.  ouvrez l’interpréteur de commandes pour le SDK Windows et accédez au répertoire d’exemple RenderExclusiveTimerDriven.
2.  exécutez la commande `start WASAPIRenderExclusiveTimerDriven.sln` dans le répertoire RenderExclusiveTimerDriven pour ouvrir le projet WASAPIRenderExclusiveTimerDriven dans la fenêtre Visual Studio.
3.  À partir de la fenêtre, sélectionnez la configuration de la solution **Debug** ou **Release** , sélectionnez le menu **générer** dans la barre de menus, puis sélectionnez l’option **générer** . si vous n’ouvrez pas Visual Studio à partir du shell CMD pour le kit de développement logiciel (sdk), Visual Studio n’aura pas accès à l’environnement de génération du kit de développement logiciel (sdk). Dans ce cas, l’exemple n’est pas généré, sauf si vous définissez explicitement la variable d’environnement MSSdk, qui est utilisée dans le fichier projet, WASAPIRenderExclusiveTimerDriven. vcproj.

## <a name="view-the-sample-files"></a>Afficher les fichiers d’exemple

Si vous générez l’application de démonstration avec succès, un fichier exécutable, WASAPIRenderExclusiveTimerDriven.exe, est généré. Pour l’exécuter, tapez `WASAPIRenderExclusiveTimerDriven` dans une fenêtre de commande suivie d’arguments obligatoires ou facultatifs. L’exemple suivant montre comment exécuter l’exemple en spécifiant une durée de lecture sur l’appareil de la console par défaut.

`WASAPIRenderExclusiveTimerDriven.exe -d 20 -console`

Le tableau suivant indique les arguments.

| Argument        | Description                                                |
|-----------------|------------------------------------------------------------|
| -?              | Affiche l’aide.                                                |
| -H              | Affiche l’aide.                                                |
| -f              | Fréquence des vagues sinusoïdales en Hz.                                 |
| -l              | Latence du rendu audio en millisecondes.                      |
| -d              | Durée de l’onde sinusoïdale en secondes.                             |
| -M              | Désactive l’utilisation de MMCSS.                                 |
| -Console        | Utilisez l’appareil de la console par défaut.                            |
| -Communications | Utilisez l’appareil de communication par défaut.                      |
| -multimédia     | Utilisez l’appareil multimédia par défaut.                         |
| -point de terminaison       | Utilisez l’identificateur de point de terminaison spécifié dans la valeur de commutateur. |



 

Si l’application est exécutée sans arguments, elle énumère les périphériques disponibles et invite l’utilisateur à sélectionner un appareil pour la session de rendu. Une fois que l’utilisateur a spécifié un appareil, l’application affiche une vague sinusoïdale à 440 Hz pendant 10 secondes. Ces valeurs peuvent être modifiées en spécifiant des valeurs de commutateur-f et-d.

RenderExclusiveTimerDriven illustre la mise en mémoire tampon pilotée par une minuterie. Dans ce mode, le client doit attendre pendant une période donnée (la moitié de la latence, spécifiée par la valeur du commutateur-d, en millisecondes). Lorsque le client sort de la période de traitement, il extrait le jeu d’exemples suivant du moteur. Avant chaque passage de traitement dans la boucle de mise en mémoire tampon, le client doit déterminer la quantité de données à afficher afin que les données ne saturent pas la mémoire tampon.

Les données audio à lire sur l’appareil spécifié peuvent être traitées en activant la mise en mémoire tampon pilotée par les événements. Ce mode est illustré dans l’exemple RenderExclusiveTimerDriven.

Pour plus d’informations sur le rendu d’un flux, consultez [rendu d’un flux](rendering-a-stream.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Exemples de SDK qui utilisent les API audio principales](sdk-samples-that-use-the-core-audio-apis.md)
</dt> </dl>

 

 



