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
# <a name="printing-gdi"></a><span data-ttu-id="ff7e2-103">Impression (GDI+)</span><span class="sxs-lookup"><span data-stu-id="ff7e2-103">Printing (GDI+)</span></span>

<span data-ttu-id="ff7e2-104">Avec quelques ajustements mineurs à votre code, vous pouvez envoyer la sortie Windows GDI+ à une imprimante plutôt qu’à un écran.</span><span class="sxs-lookup"><span data-stu-id="ff7e2-104">With a few minor adjustments to your code, you can send Windows GDI+ output to a printer rather than to a screen.</span></span> <span data-ttu-id="ff7e2-105">Pour dessiner sur une imprimante, obtenez un handle de contexte de périphérique pour l’imprimante et transmettez ce handle à un constructeur [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) .</span><span class="sxs-lookup"><span data-stu-id="ff7e2-105">To draw on a printer, obtain a device context handle for the printer and pass that handle to a [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) constructor.</span></span> <span data-ttu-id="ff7e2-106">Placez vos commandes de dessin GDI+ entre les appels à [StartDoc](/windows/win32/api/wingdi/nf-wingdi-startdocw) et [EndDoc](/windows/win32/api/wingdi/nf-wingdi-enddoc).</span><span class="sxs-lookup"><span data-stu-id="ff7e2-106">Place your GDI+ drawing commands in between calls to [StartDoc](/windows/win32/api/wingdi/nf-wingdi-startdocw) and [EndDoc](/windows/win32/api/wingdi/nf-wingdi-enddoc).</span></span>

<span data-ttu-id="ff7e2-107">Les rubriques suivantes traitent de l’envoi de la sortie GDI+ aux imprimantes plus en détail :</span><span class="sxs-lookup"><span data-stu-id="ff7e2-107">The following topics cover sending GDI+ output to printers in more detail:</span></span>

-   [<span data-ttu-id="ff7e2-108">Envoi d’une sortie GDI+ vers une imprimante</span><span class="sxs-lookup"><span data-stu-id="ff7e2-108">Sending GDI+ Output to a Printer</span></span>](-gdiplus-sending-gdi-output-to-a-printer-use.md)
-   [<span data-ttu-id="ff7e2-109">Affichage d’une boîte de dialogue Imprimer</span><span class="sxs-lookup"><span data-stu-id="ff7e2-109">Displaying a Print Dialog Box</span></span>](-gdiplus-displaying-a-print-dialog-box-use.md)
-   [<span data-ttu-id="ff7e2-110">Optimisation de l’impression en fournissant un handle d’imprimante</span><span class="sxs-lookup"><span data-stu-id="ff7e2-110">Optimizing Printing by Providing a Printer Handle</span></span>](-gdiplus-optimizing-printing-by-providing-a-printer-handle-use.md)

 

 



