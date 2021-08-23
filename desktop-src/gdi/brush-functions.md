---
description: Les fonctions suivantes sont utilisées avec les pinceaux.
ms.assetid: 617eb778-876c-4bbb-90da-c5f13359becb
title: fonctions de pinceau (Windows GDI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c44f122592e1f13186253b349089706686d352460a364e405c404fd326f64989
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119849289"
---
# <a name="brush-functions-windows-gdi"></a>fonctions de pinceau (Windows GDI)

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

 

 



