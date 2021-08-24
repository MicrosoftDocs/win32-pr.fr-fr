---
title: Station Windows et fonctions de bureau
description: Les applications peuvent utiliser les fonctions suivantes avec des objets de station Windows.
ms.assetid: 6214c28f-1035-446c-8c79-5d1dd638af2a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ccda67841508081444f7025e457c9a778195b99d0ab67ebb585362d7a3b22cd0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119810399"
---
# <a name="window-station-and-desktop-functions"></a>Station Windows et fonctions de bureau

Les applications peuvent utiliser les fonctions suivantes avec des objets de [station Windows](window-stations.md) .



| Fonction                                                     | Description                                                                                                     |
|--------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [**CloseWindowStation**](/windows/win32/api/winuser/nf-winuser-closewindowstation)             | Ferme un handle de station Windows ouverte.                                                                           |
| [**CreateWindowStation**](/windows/win32/api/winuser/nf-winuser-createwindowstationa)           | Crée un objet de station Windows, l’associe au processus en cours et l’assigne à la session active. |
| [**EnumWindowStations**](/windows/win32/api/winuser/nf-winuser-enumwindowstationsa)             | Énumère toutes les stations de fenêtre de la session active.                                                          |
| [**GetProcessWindowStation**](/windows/win32/api/winuser/nf-winuser-getprocesswindowstation)   | Récupère un handle vers la station de fenêtre active pour le processus appelant.                                       |
| [**GetUserObjectInformation**](/windows/win32/api/winuser/nf-winuser-getuserobjectinformationa) | Récupère des informations sur la station de fenêtre ou l’objet de bureau spécifié.                                     |
| [**GetUserObjectSecurity**](/windows/desktop/api/winuser/nf-winuser-getuserobjectsecurity)  | Récupère des informations de sécurité pour la station de fenêtre ou l’objet de bureau spécifié.                              |
| [**OpenWindowStation**](/windows/win32/api/winuser/nf-winuser-openwindowstationa)               | Ouvre la station de fenêtre spécifiée.                                                                             |
| [**SetProcessWindowStation**](/windows/win32/api/winuser/nf-winuser-setprocesswindowstation)   | Assigne la station de fenêtre spécifiée au processus appelant.                                                    |
| [**SetUserObjectInformation**](/windows/win32/api/winuser/nf-winuser-setuserobjectinformationa) | Définit des informations sur la station de fenêtre ou l’objet de bureau spécifié.                                          |
| [**SetUserObjectSecurity**](/windows/desktop/api/winuser/nf-winuser-setuserobjectsecurity)  | Définit les informations de sécurité pour la station de fenêtre ou l’objet de bureau spécifié.                                   |



 

Les applications peuvent utiliser les fonctions suivantes avec des objets de [Bureau](desktops.md) .



| Fonction                                                     | Description                                                                                                                        |
|--------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [**CloseDesktop**](/windows/win32/api/winuser/nf-winuser-closedesktop)                         | Ferme un handle ouvert sur un objet de bureau.                                                                                         |
| [**CreateDesktop**](/windows/win32/api/winuser/nf-winuser-createdesktopa)                       | Crée un bureau, l’associe à la station de fenêtre active du processus appelant et l’assigne au thread appelant. |
| [**CreateDesktopEx**](/windows/win32/api/winuser/nf-winuser-createdesktopexa)                   | Crée un bureau, l’associe à la station de fenêtre active du processus appelant et l’assigne au thread appelant. |
| [**EnumDesktops**](/windows/win32/api/winuser/nf-winuser-enumdesktopsa)                         | Énumère tous les postes de travail associés à la station de fenêtre active du processus appelant.                                         |
| [**EnumDesktopWindows**](/windows/win32/api/winuser/nf-winuser-enumdesktopwindows)             | Énumère toutes les fenêtres de niveau supérieur associées au bureau spécifié.                                                            |
| [**GetThreadDesktop**](/windows/win32/api/winuser/nf-winuser-getthreaddesktop)                 | Récupère un handle vers le bureau affecté au thread spécifié.                                                                |
| [**GetUserObjectInformation**](/windows/win32/api/winuser/nf-winuser-getuserobjectinformationa) | Obtient des informations sur une station de fenêtre ou un objet de bureau.                                                                         |
| [**GetUserObjectSecurity**](/windows/desktop/api/winuser/nf-winuser-getuserobjectsecurity)  | Obtient des informations de sécurité pour un objet de station de travail ou de bureau.                                                                  |
| [**OpenDesktop**](/windows/win32/api/winuser/nf-winuser-opendesktopa)                           | Ouvre l’objet de bureau spécifié.                                                                                                |
| [**OpenInputDesktop**](/windows/win32/api/winuser/nf-winuser-openinputdesktop)                 | Ouvre le bureau qui reçoit l’entrée d’utilisateur.                                                                                        |
| [**SetThreadDesktop**](/windows/win32/api/winuser/nf-winuser-setthreaddesktop)                 | Assigne le bureau spécifié au thread appelant.                                                                               |
| [**SetUserObjectInformation**](/windows/win32/api/winuser/nf-winuser-setuserobjectinformationa) | Définit des informations sur une station de travail ou un objet de bureau.                                                                         |
| [**SetUserObjectSecurity**](/windows/desktop/api/winuser/nf-winuser-setuserobjectsecurity)  | Définit les informations de sécurité pour un objet station de travail ou de bureau.                                                                  |
| [**SwitchDesktop**](/windows/win32/api/winuser/nf-winuser-switchdesktop)                       | Rend un bureau visible et l’active. Cela permet au bureau de recevoir l’entrée de l’utilisateur.                                 |



 

 

 