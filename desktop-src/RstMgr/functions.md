---
title: Fonctions du gestionnaire de redémarrage
description: L’API du gestionnaire de redémarrage utilise les fonctions identifiées dans le tableau suivant.
ms.assetid: ed39695a-1eb6-42fe-87a0-bd690bbce028
keywords:
- Restart Manager restart Mgr, référence, fonctions
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33187bff8522bfa347dc852f2cac157c2c3966a5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839850"
---
# <a name="restart-manager-functions"></a>Fonctions du gestionnaire de redémarrage

L’API du gestionnaire de redémarrage utilise les fonctions identifiées dans le tableau suivant.



| Fonction                                           | Description                                                                                                                                                                                  |
|----------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**RmAddFilter**](/windows/desktop/api/RestartManager/nf-restartmanager-rmaddfilter)                 | Modifie les actions d’arrêt ou de redémarrage.                                                                                                                                                        |
| [**RmStartSession**](/windows/desktop/api/RestartManager/nf-restartmanager-rmstartsession)           | Démarre une nouvelle session du gestionnaire de redémarrage.                                                                                                                                                        |
| [**RmJoinSession**](/windows/desktop/api/RestartManager/nf-restartmanager-rmjoinsession)             | Joint le processus d’une application à une session de gestionnaire de redémarrage existante.                                                                                                                  |
| [**RmEndSession**](/windows/desktop/api/RestartManager/nf-restartmanager-rmendsession)               | Met fin à la session du gestionnaire de redémarrage.                                                                                                                                                            |
| [**RmRegisterResources**](/windows/desktop/api/RestartManager/nf-restartmanager-rmregisterresources) | Inscrit des ressources, telles que des noms de fichiers, des noms courts de service ou des structures de [**\_ \_ processus uniques RM**](/windows/desktop/api/RestartManager/ns-restartmanager-rm_unique_process) , dans une session du gestionnaire de redémarrage.                                   |
| [**RmGetList**](/windows/desktop/api/RestartManager/nf-restartmanager-rmgetlist)                     | Utilisé par les programmes d’installation pour obtenir la liste de toutes les applications affectées par les ressources inscrites et leur état actuel.                                                                              |
| [**RmGetFilterList**](/windows/desktop/api/RestartManager/nf-restartmanager-rmgetfilterlist)         | Interroge l’état des modifications d’arrêt et de redémarrage qui ont déjà été appliquées.                                                                                                     |
| [**RmShutdown**](/windows/desktop/api/RestartManager/nf-restartmanager-rmshutdown)                   | Lance l’arrêt des applications et des services.                                                                                                                                        |
| [**RmRemoveFilter**](/windows/desktop/api/RestartManager/nf-restartmanager-rmremovefilter)           | Supprime les modifications d’arrêt et de redémarrage qui ont déjà été appliquées.                                                                                                                   |
| [**RmRestart**](/windows/desktop/api/RestartManager/nf-restartmanager-rmrestart)                     | Redémarre les applications et les services qui ont été arrêtés par la fonction [**RmShutdown**](/windows/desktop/api/RestartManager/nf-restartmanager-rmshutdown) et qui ont été inscrits pour le redémarrage à l’aide de **RegisterApplicationRestart**. |
| [**RmCancelCurrentTask**](/windows/desktop/api/RestartManager/nf-restartmanager-rmcancelcurrenttask) | Annule la fonction [**RmGetList**](/windows/desktop/api/RestartManager/nf-restartmanager-rmgetlist), [**RmShutdown**](/windows/desktop/api/RestartManager/nf-restartmanager-rmshutdown)ou [**RmRestart**](/windows/desktop/api/RestartManager/nf-restartmanager-rmrestart) actuelle.                                                            |



 

 

 




