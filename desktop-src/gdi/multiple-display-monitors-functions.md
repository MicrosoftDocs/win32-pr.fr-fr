---
description: Les fonctions suivantes assurent la prise en charge de plusieurs analyses.
ms.assetid: a64b256c-e7a1-4ee2-a346-4b7abcab9e90
title: Fonctions d’analyse de plusieurs affichages
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d0bb4477b325d0e9c79cbb7ba6d22683e31bf4b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972639"
---
# <a name="multiple-display-monitors-functions"></a>Fonctions d’analyse de plusieurs affichages

Les fonctions suivantes assurent la prise en charge de plusieurs analyses.



| Fonction                                           | Description                                                                                                                                                  |
|----------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**EnumDisplayMonitors**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaymonitors) | Énumère les moniteurs d’affichage qui croisent une région formée par l’intersection d’un rectangle de découpage spécifié et la région visible d’un contexte de périphérique. |
| [**GetMonitorInfo**](/windows/desktop/api/Winuser/nf-winuser-getmonitorinfoa)           | Récupère des informations sur un moniteur d’affichage.                                                                                                               |
| [**MonitorEnumProc**](/windows/desktop/api/Winuser/nc-winuser-monitorenumproc)         | Fonction de rappel définie par l’application qui est appelée par la fonction [**EnumDisplayMonitors**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaymonitors) .                                  |
| [**MonitorFromPoint**](/windows/desktop/api/Winuser/nf-winuser-monitorfrompoint)       | Récupère un handle vers l’écran d’affichage qui contient un point spécifié.                                                                                   |
| [**MonitorFromRect**](/windows/desktop/api/Winuser/nf-winuser-monitorfromrect)         | Récupère un handle vers le moniteur d’affichage qui a la plus grande zone d’intersection avec un rectangle spécifié.                                              |
| [**MonitorFromWindow**](/windows/desktop/api/Winuser/nf-winuser-monitorfromwindow)     | Récupère un handle vers l’écran d’affichage qui a la plus grande zone d’intersection avec le rectangle englobant d’une fenêtre spécifiée.                       |



 

 

 



