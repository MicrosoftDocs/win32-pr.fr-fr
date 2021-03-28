---
description: Avec quelques ajustements mineurs à votre code, vous pouvez envoyer la sortie Windows GDI+ à une imprimante plutôt qu’à un écran.
ms.assetid: be6286e9-d125-40ad-b33e-b4e734ac2709
title: Impression (GDI+)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e3b60010bcb63c553a96c5d70826f3fe0d3d4aa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972850"
---
# <a name="printing-gdi"></a>Impression (GDI+)

Avec quelques ajustements mineurs à votre code, vous pouvez envoyer la sortie Windows GDI+ à une imprimante plutôt qu’à un écran. Pour dessiner sur une imprimante, obtenez un handle de contexte de périphérique pour l’imprimante et transmettez ce handle à un constructeur [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) . Placez vos commandes de dessin GDI+ entre les appels à [StartDoc](/windows/win32/api/wingdi/nf-wingdi-startdocw) et [EndDoc](/windows/win32/api/wingdi/nf-wingdi-enddoc).

Les rubriques suivantes traitent de l’envoi de la sortie GDI+ aux imprimantes plus en détail :

-   [Envoi d’une sortie GDI+ vers une imprimante](-gdiplus-sending-gdi-output-to-a-printer-use.md)
-   [Affichage d’une boîte de dialogue Imprimer](-gdiplus-displaying-a-print-dialog-box-use.md)
-   [Optimisation de l’impression en fournissant un handle d’imprimante](-gdiplus-optimizing-printing-by-providing-a-printer-handle-use.md)

 

 



