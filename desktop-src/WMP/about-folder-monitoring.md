---
title: À propos de la surveillance des dossiers
description: À propos de la surveillance des dossiers
ms.assetid: d3d83e60-ecc7-4501-a6dd-15f7680a6ec9
keywords:
- Lecteur Windows Media, surveillance des dossiers
- Lecteur Windows Media modèle objet, surveillance des dossiers
- modèle objet, surveillance des dossiers
- contrôle de ActiveX Lecteur Windows Media, surveillance des dossiers
- contrôle de ActiveX, surveillance des dossiers
- Lecteur Windows Media contrôle des ActiveX mobiles, surveillance des dossiers
- Lecteur Windows Media Mobile, surveillance des dossiers
- surveillance des dossiers
- dossiers d’analyse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1206defcdc387659567ceedcf7347a3ab99ca45d9926a9bd32c4f75280a8a46
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119055507"
---
# <a name="about-folder-monitoring"></a>À propos de la surveillance des dossiers

Lecteur Windows Media pouvez surveiller les dossiers qui contiennent des fichiers multimédias numériques et mettre à jour la bibliothèque lorsque des fichiers sont ajoutés ou supprimés. Cette fonctionnalité d’analyse des dossiers est fournie par l’interface [IWMPFolderMonitorServices](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpfoldermonitorservices) .

Pour utiliser les services de surveillance des dossiers, vous devez créer l’objet lecteur dans un État distant. pour plus d’informations sur la communication à distance, consultez [communication à distance du contrôle Lecteur Windows Media](remoting-the-windows-media-player-control.md). Après avoir créé une instance distante du lecteur, obtenez un pointeur vers l’interface **IWMPFolderMonitorServices** en appelant **QueryInterface** sur l’interface [IWMPPlayer](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplayer) .

Lecteur Windows Media conserve une liste des dossiers en cours d’analyse. Pour obtenir la liste des dossiers analysés, utilisez les méthodes [IWMPFolderMonitorServices :: obtenir \_ Count](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-get_count) et [IWMPFolderMonitorServices :: Item](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-item) . Pour ajouter des dossiers à la liste ou les supprimer de la liste, utilisez respectivement les méthodes [IWMPFolderMonitorServices :: Add](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-add) et [Remove](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-remove) .

**Démarrage d’une analyse**

L’analyse des dossiers est normalement un processus en arrière-plan qui n’a pas besoin d’être appelé explicitement. Si vous souhaitez analyser activement un dossier, appelez [IWMPFolderMonitorServices :: startScan](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-startscan). Vous pouvez arrêter une analyse en cours à l’aide de la méthode [IWMPFolderMonitorServices :: stopScan](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-stopscan) .

**Récupération de l’état d’analyse des dossiers**

**IWMPFolderMonitorServices** fournit des fonctionnalités permettant de récupérer l’état du processus de surveillance du dossier.

L’analyse des dossiers est effectuée en deux étapes. Lors du premier passage, le lecteur analyse les dossiers nommés un par un dans la liste des dossiers analysés et génère une liste de fichiers à ajouter à la bibliothèque. Au cours de la deuxième passe, il parcourt la liste des fichiers et ajoute les fichiers à la bibliothèque, et supprime également tous les éléments multimédias de la bibliothèque dont les fichiers physiques correspondants ont été supprimés du système de fichiers.

L’événement [FolderScanStateChange](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents3-folderscanstatechange) est utilisé pour notifier votre programme chaque fois que le lecteur passe à un nouvel État. Vous pouvez également récupérer l’état actuel en appelant la [récupération \_ scanState](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-get_scanstate). Lors du démarrage de la première passe, la valeur de l’état actuel est wmpfssScanning. Pendant la deuxième passe, l’état passe à wmpfssUpdating. Une fois le processus terminé, l’état passe à wmpfssStopped.

Pendant que le lecteur analyse les dossiers analysés lors de la première passe, appelez la méthode [obtenir \_ scannedFilesCount](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-get_scannedfilescount) pour vérifier le nombre de fichiers analysés. La méthode [Obtient \_ currentFolder](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-get_currentfolder) vous indique quel dossier est actuellement en cours d’analyse.

Après le démarrage de la deuxième passe, appelez la méthode [obtenir \_ addedFilesCount](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-get_addedfilescount) pour vérifier le nombre de fichiers qui ont été ajoutés à la bibliothèque. La méthode [obtenir \_ UpdateProgress](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-get_updateprogress) vous indiquera la progression de la deuxième passe, sous la forme d’un pourcentage compris entre 0 et 100.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**À propos du modèle objet Player**](about-the-player-object-model.md)
</dt> <dt>

[**Interface IWMPFolderMonitorServices**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpfoldermonitorservices)
</dt> </dl>

 

 




