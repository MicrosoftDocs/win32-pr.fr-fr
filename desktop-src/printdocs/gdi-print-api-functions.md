---
description: Fonctions de l’API d’impression GDI
ms.assetid: cf3f4a61-8858-4c91-a778-d2a65998ef70
title: Fonctions de l’API d’impression GDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 125e5feef16a64433dadd11e830a09241877a453
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864757"
---
# <a name="gdi-print-api-functions"></a>Fonctions de l’API d’impression GDI

## <a name="in-this-section"></a>Dans cette section



| Fonction                                                                    | Description                                                                                                                                                                                                                                                                                                                                                                    |
|-----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AbortDoc**](/windows/desktop/api/Wingdi/nf-wingdi-abortdoc)<br/>                                     | La fonction [**AbortDoc**](/windows/desktop/api/wingdi/nf-wingdi-abortdoc) arrête le travail d’impression en cours et efface tout ce qui est dessiné depuis le dernier appel à la fonction [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca) .<br/>                                                                                                                                                                                                 |
| [*AbortProc*](/windows/desktop/api/Wingdi/nc-wingdi-abortproc)<br/>                                     | La fonction [**AbortProc**](/windows/desktop/api/wingdi/nc-wingdi-abortproc) est une fonction de rappel définie par l’application utilisée avec la fonction [**SETABORTPROC**](/windows/desktop/api/Wingdi/nf-wingdi-setabortproc) . Elle est appelée lorsqu’un travail d’impression doit être annulé pendant la mise en file d’attente. Le type **AbortProc** définit un pointeur vers cette fonction de rappel. **AbortProc** est un espace réservé pour le nom de la fonction définie par l’application.<br/> |
| [**DeviceCapabilities**](/windows/desktop/api/WinGdi/nf-wingdi-devicecapabilitiesa)<br/>                 | La fonction [**DeviceCapabilities**](/windows/desktop/api/wingdi/nf-wingdi-devicecapabilitiesa) récupère les fonctionnalités d’un pilote d’imprimante.<br/>                                                                                                                                                                                                                                                       |
| [**EndDoc**](/windows/desktop/api/Wingdi/nf-wingdi-enddoc)<br/>                                         | La fonction [**EndDoc**](/windows/desktop/api/wingdi/nf-wingdi-enddoc) met fin à un travail d’impression.<br/>                                                                                                                                                                                                                                                                                                             |
| [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage)<br/>                                       | La fonction **EndPage** informe l’appareil que l’application a fini d’écrire sur une page. Cette fonction est généralement utilisée pour indiquer au pilote de périphérique d’avancer vers une nouvelle page.<br/>                                                                                                                                                                             |
| [**Caractère d'échappement**](/windows/desktop/api/Wingdi/nf-wingdi-escape)<br/>                                         | permet à une application d’accéder aux fonctionnalités de périphérique définies par le système qui ne sont pas disponibles via GDI.<br/>                                                                                                                                                                                                                                                         |
| [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape)<br/>                                   | La fonction [**ExtEscape**](/windows/desktop/api/wingdi/nf-wingdi-extescape) permet à une application d’accéder aux fonctionnalités de l’appareil qui ne sont pas disponibles via GDI.<br/>                                                                                                                                                                                                                                |
| [**IsWindowRedirectedForPrint**](iswindowredirectedforprint.md)<br/> | La fonction [**IsWindowRedirectedForPrint**](iswindowredirectedforprint.md) détermine si la fenêtre spécifiée est actuellement redirigée pour l’impression.<br/>                                                                                                                                                                                                         |
| [**PrintWindow**](/windows/desktop/api/Winuser/nf-winuser-printwindow)<br/>                               | La fonction [**PrintWindow**](/windows/desktop/api/winuser/nf-winuser-printwindow) copie une fenêtre visuelle dans le contexte de périphérique (DC) spécifié, généralement un DC d’imprimante.<br/>                                                                                                                                                                                                                              |
| [**SetAbortProc**](/windows/desktop/api/Wingdi/nf-wingdi-setabortproc)<br/>                             | La fonction [**SETABORTPROC**](/windows/desktop/api/wingdi/nf-wingdi-setabortproc) définit la fonction d’abandon définie par l’application qui permet d’annuler un travail d’impression pendant la mise en file d’attente.<br/>                                                                                                                                                                                                               |
| [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca)<br/>                                     | La fonction [**StartDoc**](/windows/desktop/api/wingdi/nf-wingdi-startdoca) démarre un travail d’impression.<br/>                                                                                                                                                                                                                                                                                                       |
| [**StartPage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage)<br/>                                   | La fonction [**StartPage**](/windows/desktop/api/wingdi/nf-wingdi-startpage) prépare le pilote d’imprimante à accepter les données.<br/>                                                                                                                                                                                                                                                                             |



 

 

