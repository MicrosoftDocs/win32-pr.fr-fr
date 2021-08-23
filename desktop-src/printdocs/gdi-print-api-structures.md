---
description: Structures de l’API d’impression GDI
ms.assetid: 7753a54d-5136-4e46-a5ba-024bcfb961dc
title: Structures de l’API d’impression GDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e5af0087ed47123b29d6712df2c842a7f05c0d77997df7c3049cc42e0677a0e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118971468"
---
# <a name="gdi-print-api-structures"></a>Structures de l’API d’impression GDI

## <a name="in-this-section"></a>Dans cette section



| Structure                                                      | Description                                                                                                                                                                                                                                                            |
|----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea)<br/>                          | La structure de données [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) contient des informations sur l’initialisation et l’environnement d’une imprimante ou d’un périphérique d’affichage. <br/>                                                                                                              |
| [**DOCINFO**](/windows/desktop/api/Wingdi/ns-wingdi-docinfoa)<br/>                          | La structure [**docinfo**](/windows/desktop/api/wingdi/ns-wingdi-docinfoa) contient les noms de fichiers d’entrée et de sortie, ainsi que d’autres informations utilisées par la fonction [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca) .<br/>                                                                                                  |
| [**DRAWPATRECT**](/windows/desktop/api/Wingdi/ns-wingdi-drawpatrect)<br/>                  | La structure [**DRAWPATRECT**](/windows/desktop/api/wingdi/ns-wingdi-drawpatrect) définit un rectangle à créer.<br/>                                                                                                                                                                         |
| [**PSFEATURE \_ CUSTPAPER**](/windows/desktop/api/Wingdi/ns-wingdi-psfeature_custpaper)<br/> | la structure [**PSFEATURE \_ CUSTPAPER**](/windows/desktop/api/wingdi/ns-wingdi-psfeature_custpaper) contient des informations sur un format de papier personnalisé pour un pilote PostScript. Cette structure est utilisée avec la fonction d’échappement de l’imprimante [**\_ \_ FEATURESETTING PS**](/previous-versions/windows/desktop/legacy/dd144954(v=vs.85)) .<br/> |
| [**\_sortie PSFEATURE**](/windows/desktop/api/Wingdi/ns-wingdi-psfeature_output)<br/>       | la structure de [**\_ sortie PSFEATURE**](/windows/desktop/api/wingdi/ns-wingdi-psfeature_output) contient des informations sur les options de sortie du pilote PostScript. Cette structure est utilisée avec la fonction d’échappement de l’imprimante [**\_ \_ FEATURESETTING PS**](/previous-versions/windows/desktop/legacy/dd144954(v=vs.85)) .<br/>                  |
| [**PSINJECTDATA**](/windows/desktop/api/Wingdi/ns-wingdi-psinjectdata)<br/>                | La structure [**PSINJECTDATA**](/windows/desktop/api/wingdi/ns-wingdi-psinjectdata) est un en-tête pour la mémoire tampon d’entrée utilisée avec la fonction d’échappement de l’imprimante d' [**\_ injection PostScript**](/previous-versions/windows/desktop/legacy/dd162830(v=vs.85)) .<br/>                                                                            |



 

 

