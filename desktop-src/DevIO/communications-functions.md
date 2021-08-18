---
description: Les fonctions suivantes sont utilisées avec les ressources de communication.
ms.assetid: ba7d1a9e-6906-4923-a8eb-db58050ba699
title: Fonctions de communication
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc1f49efccf2ff93ea18710ea4d6647e45f1135cf8a5fed542a65192f0abda6b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119768959"
---
# <a name="communications-functions"></a>Fonctions de communication

Les fonctions suivantes sont utilisées avec les ressources de communication.



| Fonction                                                   | Description                                                                                                                    |
|------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| [**BuildCommDCB**](/windows/desktop/api/Winbase/nf-winbase-buildcommdcba)                       | Remplit une structure [**DCB**](/windows/desktop/api/Winbase/ns-winbase-dcb) spécifiée avec les valeurs spécifiées dans une chaîne de contrôle d’appareil.                           |
| [**BuildCommDCBAndTimeouts**](/windows/desktop/api/Winbase/nf-winbase-buildcommdcbandtimeoutsa) | Convertit une chaîne de définition d’appareil en codes de bloc de contrôle d’appareil appropriés et les place dans un bloc de contrôle de périphérique. |
| [**ClearCommBreak**](/windows/desktop/api/Winbase/nf-winbase-clearcommbreak)                   | Restaure la transmission de caractères pour un appareil de communication spécifié et place la ligne de transmission dans un état de non-arrêt.    |
| [**ClearCommError**](/windows/desktop/api/Winbase/nf-winbase-clearcommerror)                   | Récupère des informations sur une erreur de communication et signale l’état actuel d’un appareil de communication.                  |
| [**CommConfigDialog**](/windows/desktop/api/Winbase/nf-winbase-commconfigdialoga)               | Affiche une boîte de dialogue de configuration fournie par le pilote.                                                                           |
| [**EscapeCommFunction**](/windows/desktop/api/Winbase/nf-winbase-escapecommfunction)           | Indique à un appareil de communication spécifié d’exécuter une fonction étendue.                                                     |
| [**GetCommConfig**](/windows/desktop/api/Winbase/nf-winbase-getcommconfig)                     | Récupère la configuration actuelle d’un appareil de communication.                                                                |
| [**GetCommMask**](/windows/desktop/api/Winbase/nf-winbase-getcommmask)                         | Récupère la valeur du masque d’événement pour un appareil de communication spécifié.                                                   |
| [**GetCommModemStatus**](/windows/desktop/api/Winbase/nf-winbase-getcommmodemstatus)           | Récupère les valeurs du registre de contrôle du modem.                                                                                       |
| [**GetCommProperties**](/windows/desktop/api/Winbase/nf-winbase-getcommproperties)             | Récupère des informations sur les propriétés de communication pour un appareil de communication spécifié.                               |
| [**GetCommState**](/windows/desktop/api/Winbase/nf-winbase-getcommstate)                       | Récupère les paramètres de contrôle actuels pour un appareil de communication spécifié.                                                  |
| [**GetCommTimeouts**](/windows/desktop/api/Winbase/nf-winbase-getcommtimeouts)                 | Récupère les paramètres de délai d’attente pour toutes les opérations de lecture et d’écriture sur un appareil de communication spécifié.                      |
| [**GetDefaultCommConfig**](/windows/desktop/api/Winbase/nf-winbase-getdefaultcommconfiga)       | Récupère la configuration par défaut pour l’appareil de communication spécifié.                                                   |
| [**PurgeComm**](/windows/desktop/api/Winbase/nf-winbase-purgecomm)                             | Ignore tous les caractères de la mémoire tampon d’entrée ou de sortie d’une ressource de communication spécifiée.                                |
| [**SetCommBreak**](/windows/desktop/api/Winbase/nf-winbase-setcommbreak)                       | Suspend la transmission de caractères pour un appareil de communication spécifié et place la ligne de transmission dans un état d’arrêt.       |
| [**SetCommConfig**](/windows/desktop/api/Winbase/nf-winbase-setcommconfig)                     | Définit la configuration actuelle d’un appareil de communication.                                                                     |
| [**SetCommMask**](/windows/desktop/api/Winbase/nf-winbase-setcommmask)                         | Spécifie un ensemble d’événements à surveiller pour un appareil de communication.                                                         |
| [**SetCommState**](/windows/desktop/api/Winbase/nf-winbase-setcommstate)                       | Configure un appareil de communication conformément aux spécifications d’un bloc de contrôle d’appareil.                                  |
| [**SetCommTimeouts**](/windows/desktop/api/Winbase/nf-winbase-setcommtimeouts)                 | Définit les paramètres de délai d’attente pour toutes les opérations de lecture et d’écriture sur un appareil de communication spécifié.                           |
| [**SetDefaultCommConfig**](/windows/desktop/api/Winbase/nf-winbase-setdefaultcommconfiga)       | Définit la configuration par défaut d’un appareil de communication.                                                                    |
| [**SetupComm**](/windows/desktop/api/Winbase/nf-winbase-setupcomm)                             | Initialise les paramètres de communication pour un appareil de communication spécifié.                                               |
| [**TransmitCommChar**](/windows/desktop/api/Winbase/nf-winbase-transmitcommchar)               | Transmet un caractère spécifié à l’avant de toutes les données en attente dans la mémoire tampon de sortie de l’appareil de communication spécifié.         |
| [**WaitCommEvent**](/windows/desktop/api/Winbase/nf-winbase-waitcommevent)                     | Attend qu’un événement se produise pour un appareil de communication spécifié.                                                             |



 

 

 



