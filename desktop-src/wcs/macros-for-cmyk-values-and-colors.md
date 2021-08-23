---
title: Macros pour les valeurs et couleurs CMJN
description: Les macros suivantes sont utiles pour manipuler des valeurs CMJN.
ms.assetid: e5d107fb-e010-400b-9ec5-90c2c0381dbe
keywords:
- Windows Système de couleurs (WCS), macros CMJN
- WCS (Windows Color System), macros cmjn
- gestion des couleurs des images, macros CMJN
- gestion des couleurs, macros CMJN
- couleurs, macros CMJN
- Référence WCS, macros CMJN
- référence pour les macros WCS, CMJN
- Macros CMJN
- cyan magenta jaune noir (CMJN)
- CMJN (cyan magenta jaune noir)
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 591c479686db45f1b0d6fc6097d5134de481307b144200604a15b360bcf2c146
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119593359"
---
# <a name="macros-for-cmyk-values-and-colors"></a>Macros pour les valeurs et couleurs CMJN

Les macros suivantes sont utiles pour manipuler des valeurs CMJN.



| Macro                          | Description                                                                  |
|--------------------------------|------------------------------------------------------------------------------|
| [**CMJN**](/windows/desktop/api/Wingdi/nf-wingdi-cmyk)           | Crée une valeur CMJN à partir de valeurs cyan, magenta, jaune et noir individuelles. |
| [**GetCValue**](/windows/desktop/api/Wingdi/nf-wingdi-getcvalue) | Récupère la valeur de couleur cyan à partir d’une valeur de couleur CMJN.                      |
| [**GetKValue**](/windows/desktop/api/Wingdi/nf-wingdi-getkvalue) | Récupère la valeur de couleur noire à partir d’une valeur de couleur CMJN.                     |
| [**GetMValue**](/windows/desktop/api/Wingdi/nf-wingdi-getmvalue) | Récupère la valeur magenta à partir d’une valeur de couleur CMJN.                         |
| [**GetYValue**](/windows/desktop/api/Wingdi/nf-wingdi-getyvalue) | Récupère la valeur de couleur jaune à partir d’une valeur de couleur CMJN.                    |



 

Les macros suivantes sont utilisées avec des couleurs.



| Macro                                | Description                                                                                                                                           |
|--------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetBValue**](/windows/win32/api/wingdi/nf-wingdi-getbvalue)       | Obtient une valeur bleu RVB.                                                                                                                               |
| [**GetGValue**](/windows/win32/api/wingdi/nf-wingdi-getgvalue)       | Obtient une valeur vert RVB.                                                                                                                              |
| [**GetRValue**](/windows/win32/api/wingdi/nf-wingdi-getrvalue)       | Obtient une valeur rouge RVB.                                                                                                                                |
| [**PALETTEINDEX**](/previous-versions//dd162770(v=vs.85)) | Accepte un index pour une entrée de palette de couleurs logiques et retourne un spécificateur de saisie de palette.                                                              |
| [**PALETTERGB**](/windows/win32/api/wingdi/nf-wingdi-palettergb)     | Accepte trois valeurs qui représentent les indizaines relatives de rouge, de vert et de bleu et retourne un spécificateur rouge, vert, bleu (RVB) relatif à la palette. |
| [RGB](/windows/win32/api/wingdi/nf-wingdi-rgb)                       | Sélectionne une couleur rouge, verte, bleue (RVB) en fonction des arguments fournis et des fonctionnalités de couleur du périphérique de sortie.                               |



 

 

 