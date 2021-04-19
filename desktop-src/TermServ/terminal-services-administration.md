---
title: Administration de Services Bureau à distance
description: L’API Services Bureau à distance vous permet d’énumérer et de gérer Bureau à distance serveurs hôtes de session Bureau à distance, des sessions client et des processus.
ms.assetid: 85a9ed9d-79d6-4011-93a4-00847c689747
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e763a652335c85931225746334bc21db0e6e086d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106543414"
---
# <a name="remote-desktop-services-administration"></a>Administration de Services Bureau à distance

L’API Services Bureau à distance vous permet d’énumérer et de gérer Bureau à distance serveurs hôtes de session Bureau à distance, des sessions client et des processus.

Pour récupérer les noms de tous les serveurs hôtes de session Bureau à distance d’un domaine, appelez la fonction [**NetServerEnum**](/windows/desktop/api/lmserver/nf-lmserver-netserverenum) pour énumérer les serveurs de type TERMINALSERVER de SV \_ \_ . Pour ouvrir un handle vers un serveur hôte de session Bureau à distance spécifique, transmettez le nom du serveur dans un appel à la fonction [**WTSOpenServer**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsopenservera) . Lorsque vous avez terminé d’utiliser le handle, libérez-le en appelant la fonction [**WTSCloseServer**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtscloseserver) .

Vous pouvez utiliser le handle retourné par **WTSOpenServer** pour effectuer les opérations suivantes sur le serveur.



| Fonction                                                         | Opération                                                                                                                                                                                                         |
|------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WTSDisconnectSession**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsdisconnectsession)             | Déconnecte le client d’une session spécifiée. La session reste active et l’utilisateur peut se reconnecter pour se connecter à la même session.                                                                         |
| [**WTSEnumerateSessions**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsenumeratesessionsa)             | Retourne une liste de sessions sur le serveur hôte de session Bureau à distance spécifié.                                                                                                                                               |
| [**WTSEnumerateProcesses**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsenumerateprocessesa)           | Retourne une liste de processus sur le serveur hôte de session Bureau à distance spécifié.                                                                                                                                              |
| [**WTSLogoffSession**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtslogoffsession)                     | Déconnecte la session spécifiée.                                                                                                                                                                                   |
| [**WTSQuerySessionInformation**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsquerysessioninformationa) | Retourne des informations sur la session spécifiée sur le serveur hôte de session Bureau à distance spécifié.                                                                                                                          |
| [**WTSSendMessage**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtssendmessagea)                         | Affiche une boîte de message sur l’affichage du client d’une session spécifiée.                                                                                                                                                 |
| [**WTSShutdownSystem**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsshutdownsystem)                   | Arrête et éventuellement redémarre un serveur hôte de session Bureau à distance spécifié.                                                                                                                                            |
| [**WTSTerminateProcess**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsterminateprocess)               | Met fin à un processus spécifié sur un serveur hôte de session Bureau à distance spécifié.                                                                                                                                             |
| [**WTSVirtualChannelOpen**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelopen)           | Ouvre un handle vers l’extrémité serveur d’un canal virtuel spécifié. Pour plus d’informations sur les canaux virtuels, consultez [utilisation de services Bureau à distance canaux virtuels](using-terminal-services-virtual-channels.md). |
| [**WTSWaitSystemEvent**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtswaitsystemevent)                 | Attend un événement, tel que la création d’une session cliente ou l’ouverture de session par un utilisateur sur le serveur hôte de session Bureau à distance.                                                                                                  |



 

Plusieurs de ces fonctions allouent des tampons pour retourner des informations à l’appelant. Lorsque vous avez fini d’utiliser la mémoire tampon, libérez-la en appelant la fonction [**WTSFreeMemory**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsfreememory) .

 

 