---
description: Les fonctions suivantes sont utilisées avec l’arrêt du système.
ms.assetid: 6a08a769-1acf-49eb-ba95-beaf56a374bf
title: Fonctions d’arrêt du système
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd457c86129b3e5f80d6359018c1474f837b9e33
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952104"
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



 

 

 



