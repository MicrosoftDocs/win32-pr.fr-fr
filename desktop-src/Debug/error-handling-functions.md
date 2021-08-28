---
description: Les fonctions suivantes sont utilisées avec la gestion des erreurs.
ms.assetid: ae8ad3a2-1f1a-46d6-adaa-74c50c07dcc5
title: Fonctions de gestion d'erreur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60fdc25327bed4966336571c20580b0bfdc22b38858d3edad560359eaf0710e6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119912759"
---
# <a name="error-handling-functions"></a>Fonctions de gestion d'erreur

Les fonctions suivantes sont utilisées avec la gestion des erreurs.



| Fonction                                                 | Description                                                                                                                   |
|----------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| [**Associé**](/windows/win32/api/utilapiset/nf-utilapiset-beep)                                     | Génère des tonalités simples sur le haut-parleur.                                                                                        |
| [**CaptureStackbackTrace**](/previous-versions/windows/desktop/legacy/bb204633(v=vs.85))   | Capture une trace arrière de la pile en parcourant la pile et en enregistrant les informations pour chaque frame.                             |
| [**FatalAppExit**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-fatalappexita)                     | Affiche une boîte de message et met fin à l’application lorsque la boîte de message est fermée.                                         |
| [**FlashWindow**](/windows/desktop/api/Winuser/nf-winuser-flashwindow)                       | Clignote une fois la fenêtre spécifiée.                                                                                        |
| [**FlashWindowEx**](/windows/desktop/api/Winuser/nf-winuser-flashwindowex)                   | Clignote la fenêtre spécifiée.                                                                                                 |
| [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage)                   | Met en forme une chaîne de message.                                                                                                     |
| [**GetErrorMode**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-geterrormode)                     | Récupère le mode d’erreur pour le processus en cours.                                                                             |
| [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)                     | Récupère la dernière valeur de code d’erreur du thread appelant.                                                                         |
| [**GetThreadErrorMode**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getthreaderrormode)         | Récupère le mode d’erreur pour le thread appelant.                                                                              |
| [**MessageBeep**](/windows/desktop/api/WinUser/nf-winuser-messagebeep)                       | Émet un son de forme d’onde.                                                                                                       |
| [**RtlLookupFunctionEntry**](/windows/desktop/api/WinNT/nf-winnt-rtllookupfunctionentry) | Recherche dans les tables de fonctions actives une entrée qui correspond à la valeur de PC spécifiée.                                  |
| [**RtlNtStatusToDosError**](/windows/desktop/api/Winternl/nf-winternl-rtlntstatustodoserror)   | Récupère le code d’erreur système qui correspond au code d’erreur NT spécifié.                                              |
| [**RtlPcToFileHeader**](/windows/desktop/api/WinNT/nf-winnt-rtlpctofileheader)           | Récupère l’adresse de base de l’image qui contient la valeur de PC spécifiée.                                                 |
| [**RtlUnwind**](/windows/desktop/api/WinNT/nf-winnt-rtlunwind)                           | Lance un déroulement des frames d’appels de procédure.                                                                                 |
| [**RtlUnwind2**](/windows/desktop/api/WinNT/nf-winnt-rtlunwind2)                         | Lance un déroulement des frames d’appels de procédure.                                                                                 |
| [**RtlUnwindEx**](/windows/desktop/api/WinNT/nf-winnt-rtlunwindex)                       | Lance un déroulement des frames d’appels de procédure.                                                                                 |
| [**RtlVirtualUnwind**](/windows/desktop/api/WinNT/nf-winnt-rtlvirtualunwind)             | Récupère le contexte d’invocation de la fonction qui précède le contexte de fonction spécifié.                                |
| [**SetErrorMode**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-seterrormode)                     | Contrôle si le système gère les types spécifiés d’erreurs graves ou si le processus les gère.       |
| [**SetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-setlasterror)                     | Définit le dernier code d’erreur du thread appelant.                                                                              |
| [**SetLastErrorEx**](/windows/desktop/api/Winuser/nf-winuser-setlasterrorex)                 | Définit le dernier code d’erreur du thread appelant.                                                                              |
| [**SetThreadErrorMode**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-setthreaderrormode)         | Contrôle si le système gère les types spécifiés d’erreurs graves ou si le thread appelant les gère. |



 

 

 
