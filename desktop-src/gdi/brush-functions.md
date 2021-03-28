---
description: Les fonctions suivantes sont utilisées avec les pinceaux.
ms.assetid: 617eb778-876c-4bbb-90da-c5f13359becb
title: Fonctions de pinceau (Windows GDI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2170ff5c4b743e19da669bd76b340ca95ac2ef9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528395"
---
# <a name="brush-functions-windows-gdi"></a>Fonctions de pinceau (Windows GDI)

Les fonctions suivantes sont utilisées avec les pinceaux.



| Fonction                                                   | Description                                                |
|------------------------------------------------------------|------------------------------------------------------------|
| [**CreateBrushIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createbrushindirect)         | Crée un pinceau avec un style, une couleur et un motif spécifiés |
| [**CreateDIBPatternBrushPt**](/windows/desktop/api/Wingdi/nf-wingdi-createdibpatternbrushpt) | Crée un pinceau avec le modèle à partir d’un DIB                |
| [**CreateHatchBrush**](/windows/desktop/api/Wingdi/nf-wingdi-createhatchbrush)               | Crée un pinceau avec un motif hachuré et une couleur             |
| [**CreatePatternBrush**](/windows/desktop/api/Wingdi/nf-wingdi-createpatternbrush)           | Crée un pinceau avec un modèle bitmap                      |
| [**CreateSolidBrush**](/windows/desktop/api/Wingdi/nf-wingdi-createsolidbrush)               | Crée un pinceau avec une couleur unie                         |
| [**GetBrushOrgEx**](/windows/desktop/api/Wingdi/nf-wingdi-getbrushorgex)                     | Obtient l’origine du pinceau pour un contexte de périphérique (Device Context)                 |
| [**GetSysColorBrush**](/windows/desktop/api/Winuser/nf-winuser-getsyscolorbrush)               | Obtient un handle vers un pinceau qui correspond à un index de couleur |
| [**PatBlt**](/windows/desktop/api/Wingdi/nf-wingdi-patblt)                                   | Peint un rectangle                                         |
| [**SetBrushOrgEx**](/windows/desktop/api/Wingdi/nf-wingdi-setbrushorgex)                     | Définit l’origine du pinceau pour un contexte de périphérique (Device Context)                 |
| [**SetDCBrushColor**](/windows/desktop/api/Wingdi/nf-wingdi-setdcbrushcolor)                 | Définit la couleur actuelle du pinceau du contexte de périphérique.               |



 

## <a name="obsolete-functions"></a>Fonctions obsolètes

Les fonctions suivantes sont fournies uniquement à des fins de compatibilité avec les versions 16 bits de Windows.

[**CreateDIBPatternBrush**](/windows/desktop/api/Wingdi/nf-wingdi-createdibpatternbrush)

 

 



