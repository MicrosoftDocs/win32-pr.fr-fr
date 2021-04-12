---
description: Cet exemple d’application utilise les API audio de base pour modifier le volume de l’appareil, comme spécifié par l’utilisateur.
ms.assetid: 2597f3b1-5339-4fd4-9938-39ff917626b4
title: EndpointVolume
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e89efe89035ec272c68c6a9289672a249616e23
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483489"
---
# <a name="endpointvolume"></a>EndpointVolume

Cet exemple d’application utilise les API audio de base pour modifier le volume de l’appareil, comme spécifié par l’utilisateur.

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
-   [API EndpointVolume](endpointvolume-api.md) pour contrôler les niveaux de volume du point de terminaison de l’appareil.

## <a name="requirements"></a>Configuration requise



| Produit                                                        | Version   |
|----------------------------------------------------------------|-----------|
| [SDK Windows](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | Windows 7 |
| Visual Studio                                                  | 2008      |



 

## <a name="downloading-the-sample"></a>Téléchargement de l’exemple

Cet exemple est disponible aux emplacements suivants.



| Emplacement    | Chemin d’accès/URL                                                                                        |
|-------------|-------------------------------------------------------------------------------------------------|
| Kit de développement logiciel (SDK) Windows | \\Program Files \\ Microsoft SDK \\ Windows \\ v 7.0 \\ exemples \\ multimédia \\ audio \\ EndpointVolume \\ ... |



 

## <a name="building-the-sample"></a>Génération de l'exemple

Pour générer l’exemple x, procédez comme suit :

Pour générer l’exemple EndpointVolumeChanger, procédez comme suit :

1.  Ouvrez l’interpréteur de commandes pour le SDK Windows et accédez au répertoire d’exemple EndpointVolume.
2.  Exécutez la commande `start EndpointVolumeChanger.sln` dans le répertoire EndpointVolume pour ouvrir le projet EndpointVolumeChanger dans la fenêtre Visual Studio.
3.  À partir de la fenêtre, sélectionnez la configuration de la solution **Debug** ou **Release** , sélectionnez le menu **générer** dans la barre de menus, puis sélectionnez l’option **générer** . Si vous n’ouvrez pas Visual Studio à partir du shell CMD pour le kit de développement logiciel (SDK), Visual Studio n’aura pas accès à l’environnement de génération du kit de développement logiciel (SDK). Dans ce cas, l’exemple n’est pas généré, sauf si vous définissez explicitement la variable d’environnement MSSdk, qui est utilisée dans le fichier projet, WASAPIEndpointVolume. vcproj.

## <a name="running-the-sample"></a>Exécution de l'exemple

Si vous générez l’application de démonstration avec succès, un fichier exécutable, EndpointVolumeChanger.exe, est généré. Pour l’exécuter, tapez `EndpointVolumeChanger` dans une fenêtre de commande suivie d’arguments obligatoires ou facultatifs. L’exemple suivant montre comment basculer le paramètre muet sur l’appareil de la console par défaut.

`EndpointVolumeChanger.exe -console -m`

Le tableau suivant indique les arguments.

| Argument        | Description                                                         |
|-----------------|---------------------------------------------------------------------|
| -?              | Affiche l’aide.                                                         |
| -H              | Affiche l’aide.                                                         |
| -+              | Incrémente le niveau de volume sur l’appareil de point de terminaison audio d’une étape. . |
| vers le haut             | Incrémente le niveau de volume sur l’appareil de point de terminaison audio d’une étape.   |
| --              | Décrémente le niveau de volume sur l’appareil de point de terminaison audio d’une étape.   |
| -vers le           | Décrémente le niveau de volume sur l’appareil de point de terminaison audio d’une étape.   |
| -v              | Définit le niveau de volume maître sur l’appareil de point de terminaison audio.          |
| -Console        | Utilisez l’appareil de la console par défaut.                                     |
| -Communications | Utilisez l’appareil de communication par défaut.                               |
| -multimédia     | Utilisez l’appareil multimédia par défaut.                                  |
| -point de terminaison       | Utilisez l’identificateur de point de terminaison spécifié dans la valeur de commutateur.          |



 

Si l’application est exécutée sans arguments, elle énumère les périphériques disponibles et invite l’utilisateur à sélectionner un appareil. Une fois que l’utilisateur spécifie l’appareil, l’application affiche les paramètres actuels du volume pour le point de terminaison. Le volume peut être contrôlé à l’aide des commutateurs décrits dans le tableau précédent.

Pour plus d’informations sur le contrôle des niveaux de volume des appareils de point de terminaison audio, consultez [API EndpointVolume](endpointvolume-api.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Exemples de SDK qui utilisent les API audio principales](sdk-samples-that-use-the-core-audio-apis.md)
</dt> </dl>

 

 



