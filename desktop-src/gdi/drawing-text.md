---
description: Dessiner du texte
ms.assetid: 8a06f659-4e08-4738-b7a9-956b599c1344
title: Texte de dessin (Windows GDI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7db44a756ff211bcae7605cb87bdac77005b34f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103754421"
---
# <a name="drawing-text-windows-gdi"></a><span data-ttu-id="358a8-103">Texte de dessin (Windows GDI)</span><span class="sxs-lookup"><span data-stu-id="358a8-103">Drawing Text (Windows GDI)</span></span>

<span data-ttu-id="358a8-104">Une fois qu’une application a sélectionné la police appropriée, définit les options de mise en forme de texte requises et calcule les valeurs de largeur et de hauteur de caractère nécessaires pour une chaîne de texte, elle peut commencer à dessiner des caractères et des symboles en appelant l’une des fonctions de sortie de texte :</span><span class="sxs-lookup"><span data-stu-id="358a8-104">After an application selects the appropriate font, sets the required text-formatting options, and computes the necessary character width and height values for a string of text, it can begin drawing characters and symbols by calling any of the text-output functions:</span></span>

-   [<span data-ttu-id="358a8-105">DrawText</span><span class="sxs-lookup"><span data-stu-id="358a8-105">DrawText</span></span>](/windows/desktop/api/Winuser/nf-winuser-drawtext)
-   [<span data-ttu-id="358a8-106">DrawTextEx</span><span class="sxs-lookup"><span data-stu-id="358a8-106">DrawTextEx</span></span>](/windows/desktop/api/Winuser/nf-winuser-drawtextexa)
-   [<span data-ttu-id="358a8-107">ExtTextOut</span><span class="sxs-lookup"><span data-stu-id="358a8-107">ExtTextOut</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-exttextouta)
-   [<span data-ttu-id="358a8-108">PolyTextOut</span><span class="sxs-lookup"><span data-stu-id="358a8-108">PolyTextOut</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-polytextouta)
-   [<span data-ttu-id="358a8-109">TabbedTextOut</span><span class="sxs-lookup"><span data-stu-id="358a8-109">TabbedTextOut</span></span>](/windows/desktop/api/Winuser/nf-winuser-tabbedtextouta)
-   [<span data-ttu-id="358a8-110">TextOut</span><span class="sxs-lookup"><span data-stu-id="358a8-110">TextOut</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-textouta)

<span data-ttu-id="358a8-111">Quand une application appelle l’une de ces fonctions, le système d’exploitation passe l’appel au moteur Graphics, qui à son tour passe l’appel au pilote de périphérique approprié.</span><span class="sxs-lookup"><span data-stu-id="358a8-111">When an application calls one of these functions, the operating system passes the call to the graphics engine, which in turn passes the call to the appropriate device driver.</span></span> <span data-ttu-id="358a8-112">Au niveau du pilote de périphérique, tous ces appels sont pris en charge par un ou plusieurs appels à la fonction [ExtTextOut](/windows/desktop/api/Wingdi/nf-wingdi-exttextouta) ou [TextOut](/windows/desktop/api/Wingdi/nf-wingdi-textouta) du pilote.</span><span class="sxs-lookup"><span data-stu-id="358a8-112">At the device driver level, all of these calls are supported by one or more calls to the driver's own [ExtTextOut](/windows/desktop/api/Wingdi/nf-wingdi-exttextouta) or [TextOut](/windows/desktop/api/Wingdi/nf-wingdi-textouta) function.</span></span> <span data-ttu-id="358a8-113">Une application effectue l’exécution la plus rapide en appelant [**ExtTextOut**](/windows/win32/api/wingdi/nf-wingdi-exttextouta), qui est rapidement converti en appel **ExtTextOut** pour l’appareil.</span><span class="sxs-lookup"><span data-stu-id="358a8-113">An application will achieve the fastest execution by calling [**ExtTextOut**](/windows/win32/api/wingdi/nf-wingdi-exttextouta), which is quickly converted into an **ExtTextOut** call for the device.</span></span> <span data-ttu-id="358a8-114">Toutefois, il existe des instances lorsqu’une application doit appeler l’une des trois autres fonctions ; par exemple, pour dessiner plusieurs lignes de texte dans les bordures d’une zone rectangulaire spécifiée, il est plus efficace d’appeler [**DrawText**](/windows/win32/api/winuser/nf-winuser-drawtext).</span><span class="sxs-lookup"><span data-stu-id="358a8-114">However, there are instances when an application should call one of the other three functions; for example, to draw multiple lines of text within the borders of a specified rectangular region, it is more efficient to call [**DrawText**](/windows/win32/api/winuser/nf-winuser-drawtext).</span></span> <span data-ttu-id="358a8-115">Pour créer une table multicolonne avec des colonnes de texte justifiées, il est plus efficace d’appeler [**TabbedTextOut**](/windows/win32/api/winuser/nf-winuser-tabbedtextouta).</span><span class="sxs-lookup"><span data-stu-id="358a8-115">To create a multicolumn table with justified columns of text, it is more efficient to call [**TabbedTextOut**](/windows/win32/api/winuser/nf-winuser-tabbedtextouta).</span></span>

 

 
