---
title: Annulation de l’opération de redémarrage du gestionnaire en cours
description: Lorsqu’une action de l’utilisateur indique au programme d’installation d’effectuer une action différente, la méthode suivante peut être utilisée pour annuler l’opération du gestionnaire de redémarrage en cours.
ms.assetid: 87c8cf27-cd77-46fb-8298-cccbf4b1071a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 633882cc723f19823c6b832ee6927c5a3aacaab7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103675973"
---
# <a name="canceling-the-current-restart-manager-operation"></a>Annulation de l’opération de redémarrage du gestionnaire en cours

Lorsqu’une action de l’utilisateur indique au programme d’installation d’effectuer une action différente, la méthode suivante peut être utilisée pour annuler l’opération du gestionnaire de redémarrage en cours.

**Pour annuler l’opération du gestionnaire de redémarrage en cours**

-   Le programme d’installation peut appeler la fonction [**RMCancelCurrentTask**](/windows/desktop/api/RestartManager/nf-restartmanager-rmcancelcurrenttask) à partir d’un autre thread pour annuler l’opération [**RmShutdown**](/windows/desktop/api/RestartManager/nf-restartmanager-rmshutdown) ou [**RmRestart**](/windows/desktop/api/RestartManager/nf-restartmanager-rmrestart) en cours. Le gestionnaire de redémarrage peut annuler l’opération en fonction de la mesure dans laquelle l’opération est terminée lorsque la fonction **RMCancelCurrentTask** est appelée.

 

 




