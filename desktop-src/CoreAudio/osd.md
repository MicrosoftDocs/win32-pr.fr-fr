---
description: Cet exemple utilise les API audio de base pour implémenter un affichage à l’écran qui affiche les modifications de volume du flux de sortie qui s’exécutent via l’appareil de point de terminaison de rendu audio par défaut.
ms.assetid: 33a1e843-f7c7-4da9-a51e-83a3f0a6ac70
title: DÉPLOIEMENT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17bc0b93214cc547f0491d568abb88d696f76b494f2c562f4805f425acdcfd89
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119077513"
---
# <a name="osd"></a>DÉPLOIEMENT

Cet exemple utilise les API audio de base pour implémenter un affichage à l’écran qui affiche les modifications de volume du flux de sortie qui s’exécutent via l’appareil de point de terminaison de rendu audio par défaut. l’affichage à l’écran s’affiche lorsque l’utilisateur ajuste le niveau de volume dans le programme de contrôle de volume Windows, Sndvol.exe et disparaît une fois que le niveau de volume reste inchangé pendant une brève période.

Cette rubrique contient les sections suivantes.

-   [Description](#description)
-   [Requirements](#requirements)
-   [Téléchargement de l’exemple](#downloading-the-sample)
-   [Génération de l'exemple](#building-the-sample)
-   [Exécution de l’exemple](#running-the-sample)
-   [Rubriques connexes](#related-topics)

## <a name="description"></a>Description

Cet exemple illustre les fonctionnalités suivantes.

-   [API MMDevice](mmdevice-api.md) pour l’énumération et la sélection des appareils multimédias.
-   [API EndpointVolume](endpointvolume-api.md) audio

## <a name="requirements"></a>Configuration requise



| Produit                                                        | Version                |
|----------------------------------------------------------------|------------------------|
| [SDK Windows](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | Windows Vista ou version ultérieure ; |
| Visual Studio                                                  | 2005 ou version ultérieure          |



 

## <a name="downloading-the-sample"></a>Téléchargement de l’exemple

Cet exemple est disponible aux emplacements suivants.



| Emplacement    | Chemin d’accès/URL                                                                             |
|-------------|--------------------------------------------------------------------------------------|
| Kit de développement logiciel (SDK) Windows | \\Program Files \\ Microsoft sdk \\ Windows \\ v 7.0 \\ samples \\ \\ Audio Multimedia \\ OSD \\ ... |



 

## <a name="building-the-sample"></a>Génération de l'exemple

1.  ouvrez l’interpréteur de commandes pour le SDK Windows et accédez au répertoire de l’exemple OSD.
2.  exécutez la commande « start OSD. sln » dans le répertoire osd pour ouvrir le projet osd dans la fenêtre de Visual Studio.
3.  À partir de la fenêtre, sélectionnez la configuration de la solution **Debug** ou **Release** , sélectionnez le menu **générer** dans la barre de menus, puis sélectionnez l’option **générer** . si vous n’ouvrez pas Visual Studio à partir du shell CMD pour le kit de développement logiciel (sdk), Visual Studio n’aura pas accès à l’environnement de génération du kit de développement logiciel (sdk). Dans ce cas, l’exemple n’est pas généré, sauf si vous définissez explicitement la variable d’environnement MSSdk, qui est utilisée dans le fichier projet, OSD. vcproj.

## <a name="running-the-sample"></a>Exécution de l'exemple

1.  exécutez le fichier exécutable OSD, OSD.exe, dans Windows Vista ou version ultérieure. Notez que vous ne verrez pas une icône de barre d’état système ou une fenêtre pour l’application, mais vous pouvez voir le processus en cours d’exécution à l’aide de TaskMgr.exe.
2.  Exécutez sndvol.exe pour modifier le volume ou le sourdine, ou modifiez le volume à l’aide de contrôles de clavier ou d’un contrôle HID. L’interface utilisateur OSD s’affiche.
3.  Pour quitter l’application, exécutez TaskMgr.exe, mettez en surbrillance le processus OSD.exe et cliquez sur **terminer le processus**.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Exemples de SDK qui utilisent les API audio principales](sdk-samples-that-use-the-core-audio-apis.md)
</dt> </dl>

 

 



