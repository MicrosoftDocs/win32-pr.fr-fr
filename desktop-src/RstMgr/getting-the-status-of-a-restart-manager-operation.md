---
title: Obtention de l’état d’une opération du gestionnaire de redémarrage
description: Lorsque de nombreuses applications et services doivent être arrêtés ou redémarrés, l’opération du gestionnaire de redémarrage peut prendre un certain temps. La méthode suivante peut être utilisée pour obtenir l’état de l’opération en cours.
ms.assetid: 0df9de1f-df37-46a5-8010-6c8b34429376
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7afa5f329a8f21aa625c5c7b61a3e65b2c907bbf
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104102176"
---
# <a name="getting-the-status-of-a-restart-manager-operation"></a>Obtention de l’état d’une opération du gestionnaire de redémarrage

Lorsque de nombreuses applications et services doivent être arrêtés ou redémarrés, l’opération du gestionnaire de redémarrage peut prendre un certain temps. La méthode suivante peut être utilisée pour obtenir l’état de l’opération en cours.

**Pour connaître l’état de l’opération du gestionnaire de redémarrage en cours**

1.  Le programme d’installation doit implémenter une fonction de [**\_ rappel d' \_ état \_ d’écriture RM**](/windows/win32/api/restartmanager/nc-restartmanager-rm_write_status_callback) qui détermine l’état des applications qui ont été arrêtées ou redémarrées. La fonction peut fournir les informations à l’interface utilisateur ou au journal.
2.  Le programme d’installation passe le pointeur vers la fonction de [**rappel d’état d' \_ écriture \_ \_ RM**](/windows/win32/api/restartmanager/nc-restartmanager-rm_write_status_callback) lors de l’appel de la fonction [**RmShutdown**](/windows/desktop/api/RestartManager/nf-restartmanager-rmshutdown) ou [**RmRestart**](/windows/desktop/api/RestartManager/nf-restartmanager-rmrestart) .

 

 