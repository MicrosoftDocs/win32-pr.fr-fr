---
title: Paramètres de ligne de commande
description: Paramètres de ligne de commande
ms.assetid: c4af8a03-2cab-4ecd-bbd8-c83869822901
keywords:
- Lecteur Windows Media, paramètres
- Lecteur Windows Media, paramètres de ligne de commande
- Lecteur Windows Media, Wmplayer
- Lecteur Windows Media, Wmpconfig
- Lecteur Windows Media, Wmpnscfg
- paramètres de ligne de commande
- Wmplayer
- Wmpconfig
- Wmpnscfg
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2240040453bc60a7a03ca56f205643f97202eb840a501fd13aa417b86aef060d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118341949"
---
# <a name="command-line-parameters"></a>Paramètres de ligne de commande

## <a name="command-line-parameters-for-wmplayer"></a>Paramètres de ligne de commande pour wmplayer

Lecteur Windows Media prend en charge un ensemble de paramètres de ligne de commande qui spécifient le comportement du joueur au démarrage. Le tableau suivant détaille les paramètres et leurs comportements.



| Syntaxe                                                                                                              | Comportement                                                                                                                                                                                                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| «*path \\ filename*» (par exemple : `wmplayer "c:\filename.wma"` )<br/>                                            | Démarrez le lecteur et lisez le fichier.                                                                                                                                                                                                                                                                                                        |
| "*path \\ filename*"/fullscreen (par exemple : `wmplayer "c:\filename.wmv" /fullscreen` )<br/>                    | Lire le fichier spécifié en mode plein écran. Vous devez spécifier le chemin d’accès et le nom de fichier du contenu à lire.<br/>                                                                                                                                                                                                                     |
| /Device : {DVD \| AudioCD} (par exemple : `wmplayer /device:audio CD` )<br/>                                         | Lire un DVD ou un CD audio.                                                                                                                                                                                                                                                                                                                    |
| «*chemin d’accès au \\ fichier*? WMPSkin =*nom* de l’apparence», par exemple : `wmplayer "c:\filename.wma?wmpskin=headspace"`<br/>        | Ouvre le lecteur, en appliquant l’apparence spécifiée.                                                                                                                                                                                                                                                                                              |
| /Service :*keyName*                                                                                                  | Ouvrez le lecteur qui affiche la Banque en ligne spécifiée par *keyName*. requiert Lecteur Windows Media 10 ou version ultérieure.<br/>                                                                                                                                                                                                                      |
| /Task NowPlaying                                                                                                    | Ouvrez le lecteur dans la fonctionnalité **lecture** en cours.                                                                                                                                                                                                                                                                                            |
| /Task MediaGuide                                                                                                    | ouvrez le lecteur dans la fonctionnalité du **Guide multimédia** (actuellement active store online dans Lecteur Windows Media 10 ou version ultérieure).                                                                                                                                                                                                                          |
| /Task CDAudio                                                                                                       | ouvrez le lecteur dans la fonctionnalité **copier à partir du CD** (fonctionnalité **Rip** dans Lecteur Windows Media 10 ou Lecteur Windows Media 11). ce paramètre n’est pas pris en charge dans Lecteur Windows Media 12.                                                                                                                                                       |
| /Task CDWrite                                                                                                       | Ouvrez le lecteur dans la fonctionnalité de **gravure** . requiert Lecteur Windows Media 10.<br/>                                                                                                                                                                                                                                                       |
| /Task MediaLibrary                                                                                                  | Ouvrez le lecteur dans la fonctionnalité de la **bibliothèque** .                                                                                                                                                                                                                                                                                                |
| Radioréglage d'/Task                                                                                                    | ouvrez le lecteur dans la fonctionnalité **Tuner Radio** (actuellement active store online dans Lecteur Windows Media 10 ou version ultérieure).                                                                                                                                                                                                                          |
| /Task PortableDevice                                                                                                | ouvrez le lecteur dans la fonctionnalité **copier sur un CD ou un appareil** (fonctionnalité de **synchronisation** dans Lecteur Windows Media 10 ou version ultérieure).                                                                                                                                                                                                                            |
| /Task services/service *ServiceName*                                                                               | ouvrez le lecteur dans la fonctionnalité **Services Premium** , en présentant le service spécifié par le paramètre *servicename* . Cette valeur est le nom unique du service. Si le service spécifié n’a pas été affiché précédemment, le paramètre *ServiceName* est ignoré. (ouvre le magasin en ligne spécifié dans Lecteur Windows Media 10 ou version ultérieure.) |
| /Task ServiceTask *X*                                                                                                | Ouvrez le lecteur dans le volet de tâches du service de magasin en ligne spécifié par *X*. Par exemple,/Task ServiceTask1 ouvre le lecteur dans le premier volet de tâches du service de magasin en ligne.                                                                                                                                                                      |
| /Task SkinViewer                                                                                                    | Ouvrez le lecteur dans la fonctionnalité **Sélecteur d’apparence** .                                                                                                                                                                                                                                                                                           |
| /Playlist *PlaylistName*                                                                                            | Ouvrez le lecteur et lisez la sélection spécifiée.                                                                                                                                                                                                                                                                                           |
| /Schema : {Musique \| images \| \| TV vidéo \| autre} par exemple :`wmplayer /Schema:Pictures /Task:PortableDevice`<br/> | Ouvre le lecteur, qui affiche la catégorie de médias spécifiée. requiert Lecteur Windows Media 11.                                                                                                                                                                                                                                                   |



 

## <a name="command-line-parameters-for-wmpconfig"></a>Paramètres de ligne de commande pour Wmpconfig

Wmpconfig.exe est utilisé pour exécuter certaines commandes dans Lecteur Windows Media qui requièrent une autorisation d’administrateur. les exemples incluent le démarrage et l’arrêt des services de navigation et de partage, ainsi que l’activation des exceptions dans le pare-feu Windows. Le tableau suivant décrit les valeurs possibles pour les paramètres de ligne de commande.



| Syntaxe                                                                                    | Comportement                                                                   |
|-------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| DisableHMEDevice *Mac*                                                                    | Désactive l’appareil spécifié par un identificateur de Access Control de média (MAC).  |
| Exemple HMEOff :<br/> wmpconfig HMEOff<br/>                                    | désactive le Service de partage réseau Lecteur Windows Media.                 |
| Exemple HMEOn :<br/> wmpconfig HMEOn<br/>                                      | Active le partage, la navigation et l’exception de pare-feu.                     |
| RemoveHMEDevice *Mac*                                                                     | Supprime l’appareil spécifié par un identificateur MAC.                          |
| RestoreHMEDevice *Mac*                                                                    | Restaure l’appareil spécifié par un identificateur MAC.                         |
| Exemple de *niveau* SetDVDParentalLevel :<br/> wmpconfig SetDVDParentalLevel 3<br/> | Définit le niveau de contrôle parental du DVD. Le niveau est spécifié sous la forme d’un entier. |



 

## <a name="command-line-parameters-for-wmpnscfg"></a>Paramètres de ligne de commande pour WMPNSCFG

Microsoft Windows utilise wmpnscfg.exe pour alerter les utilisateurs lorsque des périphériques de rendu de média sont détectés sur le réseau. Wmpnscfg démarre le service de partage réseau Lecteur Windows Media, puis attend les notifications du service. Quand WMPNSCFG est informé qu’un nouveau périphérique multimédia est disponible sur le réseau, il affiche une fenêtre contextuelle dans la barre d’état système qui informe l’utilisateur de la disponibilité du nouvel appareil. si l’utilisateur clique sur la fenêtre contextuelle, wmpnscfg lance Lecteur Windows Media, qui affiche une boîte de dialogue qui demande à l’utilisateur d’autoriser ou de refuser le partage avec le nouvel appareil.

en général, Windows appelle wmpnscfg sans paramètres de ligne de commande. Toutefois, il existe un paramètre disponible, décrit dans le tableau suivant.



| Paramètre | Comportement                         |
|-----------|----------------------------------|
| /Close    | Fermez toutes les instances de WMPNSCFG. |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Lecteur Windows Media**](windows-media-player.md)
</dt> </dl>

 

 





