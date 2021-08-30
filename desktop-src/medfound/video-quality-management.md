---
description: Gestion de la qualité vidéo
ms.assetid: 3617adf2-ed7b-4788-abce-58bc22a14511
title: Gestion de la qualité vidéo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d441178cd5b360bb9f8fb9bfc4d903fd9a5a3848
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122479845"
---
# <a name="video-quality-management"></a>Gestion de la qualité vidéo

cette rubrique décrit certaines améliorations apportées au pipeline vidéo dans Windows 7, pour Microsoft Media Foundation et Microsoft DirectShow.

Dans un monde parfait, la vidéo ne se détournerait jamais, quelle que soit la résolution vidéo ou la charge de l’UC/GPU. En réalité, bien entendu, le pipeline vidéo doit être capable de faire face aux ressources matérielles limitées et il doit pouvoir adapter la lecture à l’environnement système de manière adaptative. Les objectifs de la gestion de la qualité vidéo sont les suivants :

-   Réduire les problèmes (images abandonnées ou tardives).
-   Réduisez l’utilisation de la mémoire, en particulier dans le GPU.
-   Réduisez la consommation d’énergie, en particulier sur les ordinateurs portables fonctionnant sur batterie.
-   Obtenir la meilleure qualité d’image possible, en fonction des contraintes de ressources.
-   Conservez la vidéo synchronisée avec l’audio.

Certains de ces objectifs sont contraires, en particulier sur les systèmes bas de gamme. En général, il existe un compromis entre la vitesse et la qualité. Le problème est plus répréhensible que la réduction modérée de la qualité visuelle. L’importance relative de la consommation d’énergie varie en fonction de l’environnement. sur un ordinateur portable fonctionnant sur batterie, il est très important.

dans Windows 7, le rendu vidéo amélioré (EVR) offre une meilleure prise en charge de la gestion de la qualité vidéo. le pipeline Media Foundation et le pipeline DirectShow ont été mis à jour pour tirer parti de ces fonctionnalités. Une approche à deux branches est utilisée :

-   Avant le démarrage de la lecture, le pipeline peut effectuer des optimisations statiques, en fonction des paramètres de gestion de l’alimentation de l’utilisateur et des informations sur le matériel.
-   Après le démarrage de la lecture, le pipeline peut appliquer des optimisations dynamiques, en fonction des performances d’exécution.

## <a name="quality-management-in-media-foundation"></a>Gestion de la qualité dans Media Foundation

Pour activer les optimisations statiques, définissez l’attribut [ \_ \_ \_ \_ optimisations de la lecture statique de la topologie MF](mf-topology-static-playback-optimizations.md) sur la topologie partielle avant de résoudre la topologie. Le chargeur de topologie interroge cet attribut dans sa méthode [**IMFTopoLoader :: Load**](/windows/desktop/api/mfidl/nf-mfidl-imftopoloader-load) .

Si vous activez les optimisations statiques, vous devez définir deux autres attributs sur la topologie :



| Attribut                                                                                                                                      | Description                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <span id="MF_TOPOLOGY_PLAYBACK_MAX_DIMS"></span><span id="mf_topology_playback_max_dims"></span>\_ \_ nombre maximal de lectures de la topologie \_ MF \_<br/>   | Spécifie la taille maximale de la fenêtre de lecture vidéo.<br/> |
| <span id="MF_TOPOLOGY_PLAYBACK_FRAMERATE"></span><span id="mf_topology_playback_framerate"></span>\_fréquence de lecture de \_ la topologie MF \_<br/> | Spécifie la fréquence d’actualisation du moniteur.<br/>                      |



 

Ces deux attributs aident le pipeline à calculer le paramètre le plus efficace pour la gestion de la qualité.

Les optimisations dynamiques sont effectuées par le gestionnaire de qualité. Vous n’avez rien à faire pour activer le gestionnaire de qualité ; elle est automatiquement activée. le gestionnaire de qualité existait dans Windows Vista ; dans Windows 7, EVR peut répondre mieux aux messages du gestionnaire de qualité.

## <a name="quality-management-in-directshow"></a>Gestion de la qualité dans DirectShow

DirectShow prend en charge les optimisations statiques et dynamiques pour la lecture des DVD. Pour activer ces optimisations dans une application de lecture de DVD, définissez les indicateurs suivants dans le paramètre *dwFlags* de la méthode **IDvdGraphBuilder :: RenderDvdVideoVolume** :



| Indicateur                  | Description                    |
|-----------------------|--------------------------------|
| \_graphique des \_ adaptateurs de DVD am \_ | Active les optimisations statiques.  |
| AM \_ DVD \_ EVR \_ QoS     | Active les optimisations dynamiques. |



 

d’autres applications de DirectShow peuvent activer des optimisations dynamiques en appelant la méthode [**IEVRFilterConfigEx :: SetConfigPrefs**](/windows/desktop/api/evr/nf-evr-ievrfilterconfigex-setconfigprefs) directement sur le filtre EVR. Spécifiez l’indicateur **EVRFilterConfigPrefs \_ EnableQoS** .

> [!Note]  
> les optimisations statiques dans DirectShow sont limitées à la lecture des DVD.

 

## <a name="quality-management-in-the-evr"></a>Gestion de la qualité dans le EVR

EVR prend en charge de nouveaux indicateurs de configuration pour la gestion de la qualité. Si vous activez les optimisations de gestion de la qualité décrites précédemment, vous n’êtes pas obligé de définir ces indicateurs directement. Toutefois, elles sont documentées pour les applications qui souhaitent un contrôle plus granulaire sur les EVR.

Définissez les indicateurs suivants sur le mélangeur EVR en appelant la méthode [**IMFVideoMixerControl2 :: SetMixingPrefs**](/windows/desktop/api/evr/nf-evr-imfvideomixercontrol2-setmixingprefs) :




| Indicateurs | Description | 
|-------|-------------|
| <ul><li><strong>MFVideoMixPrefs_ForceHalfInterlace</strong></li><li><strong>MFVideoMixPrefs_AllowDropToHalfInterlace</strong></li></ul> | Ignorez le deuxième champ de chaque trame entrelacée. | 
| <ul><li><strong>MFVideoMixPrefs_AllowDropToBob</strong></li><li><strong>MFVideoMixPrefs_ForceBob</strong></li></ul> | Utilisez la désentrelacement Bob, même si le pilote prend en charge un mode de désentrelacement de qualité supérieure. | 




 

Définissez les indicateurs suivants sur le présentateur EVR en appelant la méthode [**IMFVideoDisplayControl :: SetRenderingPrefs**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setrenderingprefs) :




| Indicateurs | Description | 
|-------|-------------|
| <ul><li><strong>MFVideoRenderPrefs_ForceOutputThrottling</strong></li><li><strong>MFVideoRenderPrefs_AllowOutputThrottling</strong></li></ul> | Limiter la sortie pour correspondre à la bande passante GPU. | 
| <ul><li><strong>MFVideoRenderPrefs_ForceBatching</strong></li><li><strong>MFVideoRenderPrefs_AllowBatching</strong></li></ul> | Batch Direct3D présente des appels. Cette optimisation permet au système d’entrer les États inactifs plus fréquemment, ce qui peut réduire la consommation d’énergie. | 
| <ul><li>MFVideoRenderPrefs_ForceScaling</li><li>MFVideoRenderPrefs_AllowScaling</li></ul> | Effectue un mixage vidéo à l’aide d’un rectangle plus petit que le rectangle de sortie. Mettez à l’échelle le résultat avec la taille de sortie correcte. | 




 

En outre, le récepteur multimédia EVR prend en charge les attributs de configuration qui correspondent à chacun de ces indicateurs :

-   [EVRConfig \_ AllowBatching](evrconfig-allowbatching.md)
-   [EVRConfig \_ AllowDropToBob](evrconfig-allowdroptobob.md)
-   [EVRConfig \_ AllowDropToHalfInterlace](evrconfig-allowdroptohalfinterlace.md)
-   [EVRConfig \_ AllowScaling](evrconfig-allowscaling.md)
-   [EVRConfig \_ AllowDropToThrottle](evrconfig-allowdroptothrottle.md)
-   [EVRConfig \_ ForceBatching](evrconfig-forcebatching.md)
-   [EVRConfig \_ ForceBob](evrconfig-forcebob.md)
-   [EVRConfig \_ ForceHalfInterlace](evrconfig-forcehalfinterlace.md)
-   [EVRConfig \_ ForceScaling](evrconfig-forcescaling.md)
-   [EVRConfig \_ ForceThrottle](evrconfig-forcethrottle.md)

Avant le démarrage de la lecture, vous pouvez définir ces attributs directement sur le récepteur multimédia EVR, au lieu d’appeler les méthodes [**IMFVideoMixerControl2**](/windows/desktop/api/evr/nn-evr-imfvideomixercontrol2) et [**IMFVideoDisplayControl**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol) . Pour définir ces attributs, interrogez le récepteur multimédia EVR pour [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Session multimédia](media-session.md)
</dt> </dl>

 

 




