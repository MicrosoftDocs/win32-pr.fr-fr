---
description: Les fonctions suivantes sont utilisées avec l’arrêt du système.
ms.assetid: 6a08a769-1acf-49eb-ba95-beaf56a374bf
title: Fonctions d’arrêt du système
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36b1304a2333d817be7cbb51ee599f37cda8b3e185f56cfc5959f1646e9ab639
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119664339"
---
# <a name="system-shutdown-functions"></a>Fonctions d’arrêt du système

Les fonctions suivantes sont utilisées avec l’arrêt du système.



| Fonction                                                         | Description                                                                                                                         |
|------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [**AbortSystemShutdown**](/windows/desktop/api/Winreg/nf-winreg-abortsystemshutdowna)               | Arrête un arrêt du système qui a été initié.                                                                                    |
| [**ExitWindows**](/windows/desktop/api/Winuser/nf-winuser-exitwindows)                               | Déconnecte l’utilisateur interactif.                                                                                                      |
| [**ExitWindowsEx**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex)                           | Déconnecte l’utilisateur interactif, arrête le système ou arrête et redémarre le système.                                        |
| [**InitiateShutdown**](/windows/desktop/api/Winreg/nf-winreg-initiateshutdowna)                     | Lance un arrêt et un redémarrage de l’ordinateur spécifié, puis redémarre toutes les applications qui ont été inscrites pour le redémarrage.    |
| [**InitiateSystemShutdown**](/windows/desktop/api/Winreg/nf-winreg-initiatesystemshutdowna)         | Lance un arrêt et un redémarrage facultatif de l’ordinateur spécifié.                                                                |
| [**InitiateSystemShutdownEx**](/windows/desktop/api/Winreg/nf-winreg-initiatesystemshutdownexa)     | Lance un arrêt et un redémarrage facultatif de l’ordinateur spécifié et enregistre éventuellement la raison de l’arrêt.            |
| [**LockWorkStation**](/windows/desktop/api/Winuser/nf-winuser-lockworkstation)                       | Verrouille l’affichage de la station de travail.                                                                                                    |
| [**ShutdownBlockReasonCreate**](/windows/desktop/api/Winuser/nf-winuser-shutdownblockreasoncreate)   | Indique que le système ne peut pas être arrêté et définit une chaîne de motif à afficher à l’utilisateur si l’arrêt du système est initié. |
| [**ShutdownBlockReasonDestroy**](/windows/desktop/api/Winuser/nf-winuser-shutdownblockreasondestroy) | Indique que le système peut être arrêté et libère la chaîne de raison.                                                             |
| [**ShutdownBlockReasonQuery**](/windows/desktop/api/Winuser/nf-winuser-shutdownblockreasonquery)     | Récupère la chaîne de raison définie par la fonction [**ShutdownBlockReasonCreate**](/windows/desktop/api/Winuser/nf-winuser-shutdownblockreasoncreate) .                     |



 

 

 



