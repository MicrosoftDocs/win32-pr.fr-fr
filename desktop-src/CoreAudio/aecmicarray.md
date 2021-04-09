---
description: Cet exemple utilise les API audio de base pour capturer un flux vocal de haute qualité. L’exemple prend en charge l’annulation de l’écho acoustique et le traitement du tableau de microphone à l’aide de l’AEC DMO, également appelé DSP de capture vocale, fourni par Microsoft.
ms.assetid: 932d3442-1beb-4938-9382-031c61cd9b05
title: AECMicArray
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfe72351b9f8f61d939a9f73eaf85022d7f487bf
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111562"
---
# <a name="aecmicarray"></a>AECMicArray

Cet exemple utilise les API audio de base pour capturer un flux vocal de haute qualité. L’exemple prend en charge l’annulation de l’écho acoustique et le traitement du tableau de microphone à l’aide de l’AEC DMO, également appelé DSP de capture vocale, fourni par Microsoft.

Cette rubrique contient les sections suivantes.

-   [Description](#description)
-   [Configuration requise](#requirements)
-   [Téléchargement de l’exemple](#downloading-the-sample)
-   [Génération de l'exemple](#building-the-sample)
-   [Exécution de l’exemple](#running-the-sample)
-   [Rubriques connexes](#related-topics)

## <a name="description"></a>Description

Cet exemple illustre les fonctionnalités suivantes.

-   [MMDevice](mmdevice-api.md) pour l’énumération et la sélection des appareils multimédias.
-   [WASAPI](wasapi.md) pour les opérations de gestion de flux, telles que le démarrage et l’arrêt du flux, le basculement de flux.
-   [DeviceTopology](devicetopology-api.md) pour l’énumération des adaptateurs audio.
-   [EndpointVolume](endpointvolume-api.md) contrôle des niveaux de volume des [sessions audio](audio-sessions.md).

## <a name="requirements"></a>Configuration requise



| Produit                                                        | Version                     |
|----------------------------------------------------------------|-----------------------------|
| [SDK Windows](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | Windows Vista ou version ultérieure ;      |
| Visual Studio                                                  | 2005 (éditions non-Express) |



 

## <a name="downloading-the-sample"></a>Téléchargement de l’exemple

Cet exemple est disponible aux emplacements suivants.



| Emplacement    | Chemin d’accès/URL                                                                                     |
|-------------|----------------------------------------------------------------------------------------------|
| Kit de développement logiciel (SDK) Windows | \\Program Files \\ Microsoft SDK \\ Windows \\ v 7.0 \\ exemples \\ multimédia \\ audio \\ AECMicArray \\ ... |



 

## <a name="building-the-sample"></a>Génération de l'exemple

Pour générer l’exemple AecSDKDemo, procédez comme suit :

1.  Ouvrez une fenêtre de commande du kit de développement logiciel (SDK).
2.  Tapez **CD% MSSDK% \\ Setup**.
3.  Exécutez VCIntegrate.exe.

    À partir de ce point, les fenêtres de commande auront les paramètres d’environnement appropriés pour créer une application qui tire parti du kit de développement logiciel (SDK).

4.  Générez l’exemple.

## <a name="running-the-sample"></a>Exécution de l'exemple

Si vous générez l’application de démonstration avec succès, un fichier exécutable, AecSDKDemo.exe est généré. Pour l’exécuter, tapez `AecSDKDemo` dans une fenêtre de commande suivie d’arguments obligatoires ou facultatifs, comme décrit ci-dessous.

`AecSDKDemo -out mic_out.pcm -mod system_mode [-option value] `

Le tableau suivant indique les arguments.

| Argument  | Description                                                                                                                           |
|-----------|---------------------------------------------------------------------------------------------------------------------------------------|
| -out      | Obligatoire. Spécifie le nom du fichier de sortie.                                                                                                 |
| -mod      | Obligatoire. Spécifie le mode système de capture vocale. Pour plus d’informations, reportez-vous à la section « Configuration de la capture de la voix DMO » dans l’exemple de fichier Readme. |
| -Feature     | Optionnel. Active le mode de fonctionnalité sur (1) ou sur OFF (0).                                                                                       |
| -NS       | Optionnel. Désactive la suppression du bruit sur (1) ou sur OFF (0). Le mode de fonctionnalité doit être activé pour pouvoir être spécifié.                                     |
| -AGC      | Optionnel. Active Digital AGC sur (1) ou sur OFF (0). Le mode de fonctionnalité doit être activé pour pouvoir être spécifié.                                           |
| -cntrclip | Optionnel. Active ou désactive le découpage du Centre (0). Le mode de fonctionnalité doit être activé pour pouvoir être spécifié.                                       |
| -spkdev   | Optionnel. Spécifie l’index de l’appareil de l’intervenant. S’il n’est pas spécifié, l’utilisateur est invité à sélectionner.                                         |
| -micdev   | Optionnel. Spécifie l’index du périphérique microphone. S’il n’est pas spécifié, l’utilisateur est invité à sélectionner.                                      |
| -Duration | Optionnel. Spécifie la durée d’exécution de l’application.                                                                                    |



 

Cet exemple d’application ne joue aucun signal. Pour exécuter la démonstration correctement pour les modes activés AEC (mode 0 et 4), les utilisateurs doivent lire certains signaux audio via le même appareil d’orateur spécifié pour la solution DMO (c’est-à-dire l’appareil spécifié par l’option « -spkdev »), ce qui simule la voix de bout en bout dans un scénario de conversation bidirectionnel. Les utilisateurs peuvent utiliser n’importe quel joueur pour lire des signaux audio. S’il n’y a aucun flux de rendu actif sur le périphérique de l’orateur sélectionné, le traitement de DMO échoue.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Exemples de SDK qui utilisent les API audio principales](sdk-samples-that-use-the-core-audio-apis.md)
</dt> </dl>

 

 



