---
description: Un appareil peut potentiellement générer un grand nombre d’événements, et chaque événement peut être géré par un certain nombre de gestionnaires différents.
ms.assetid: C203B5AB-917C-4543-98D6-EDE02E0B5E49
title: Comment inscrire un gestionnaire d’événements
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f96aedc8b6b7944238938539a8fafa5d80c6dc7f1afd4dc5f818ecc91abd08c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120090559"
---
# <a name="how-to-register-an-event-handler"></a>Comment inscrire un gestionnaire d’événements

Un appareil peut potentiellement générer un grand nombre d’événements, et chaque événement peut être géré par un certain nombre de gestionnaires différents. dans Windows XP, les événements suivants sont définis :

-   DeviceArrival
-   DeviceRemoval
-   MediaArrival
-   MediaRemoval

## <a name="instructions"></a>Instructions


Les gestionnaires d’événements sont définis sous la clé **EventHandlers** . Les valeurs d’une clé de gestionnaire d’événements sont les noms de chaque gestionnaire que l’utilisateur doit choisir lorsque l’événement est détecté. Aucune valeur de données n’est associée à ces entrées. Voici un exemple de définition d’un gestionnaire d’événements personnalisé appelé **MyNewRemovalEventHandler**, qui présente ces possibilités de gestionnaire à l’utilisateur :

-   Gestionnaire à utiliser si l’événement est détecté sur un appareil effectué par la société nommée Contoso, Inc.
-   Gestionnaire à utiliser si l’événement est détecté sur un appareil effectué par l’entreprise nommée Fabrikam, Inc.
-   Gestionnaire à utiliser dans tous les autres cas.

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  AutoplayHandlers
                     EventHandlers
                        MyNewRemovalEventHandler
                           CompanyContosoHandler [REG_SZ]
                           CompanyFabrikamHandler [REG_SZ]
                           MyRemovalHandler [REG_SZ]
```

Une fois qu’un gestionnaire d’événements est défini, il doit être inscrit auprès d’un gestionnaire d’appareils pour l’une des possibilités d’événement : DeviceArrival, DeviceRemoval, MediaArrival ou MediaRemoval. MyNewRemovalEventHandler, défini précédemment, est utilisé pour DeviceRemoval sous un gestionnaire d’appareils personnalisé nommé MyDeviceHandler et est défini à cet effet dans l’exemple suivant. Là encore, la valeur de Registre n’a pas de composant de données.

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  AutoplayHandlers
                     DeviceHandlers
                        EventHandlers
                           DeviceRemoval
                              MyNewRemovalEventHandler
```

Windows XP prédéfinit l’ensemble suivant d’EventHandlers. 

| Clé EventHandlers        | Type de fichier ou de média                             |
|--------------------------|------------------------------------------------|
| HandleCDBurningOnArrival | CD-R/CD-RW vierge                               |
| ShowPicturesOnArrival    | Fichiers image                                  |
| PlayMusicFilesOnArrival  | fichiers Musique                                    |
| PlayVideoFilesOnArrival  | Fichiers vidéo                                    |
| PlayCDAudioOnArrival     | CD audio (format de CD de format REDBOOK avec pistes audio) |
| PlayDVDMovieOnArrival    | Films DVD                                     |



 

Windows Vista prédéfinit l’ensemble suivant d’EventHandlers, en plus de ceux ci-dessus. 

| Clé EventHandlers              | Type de fichier ou de média   |
|--------------------------------|----------------------|
| PlaySuperVideoCDMovieOnArrival | Films Super VideoCD |
| PlayVideoCDMovieOnArrival      | Films VideoCD       |



 

 

 



