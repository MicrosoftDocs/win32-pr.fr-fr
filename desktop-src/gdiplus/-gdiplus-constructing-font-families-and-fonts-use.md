---
description: Windows GDI+ regroupe des polices avec la même police mais des styles différents dans des familles de polices.
ms.assetid: 57428fae-6af4-47a5-a499-717dc378767a
title: Construction des familles de polices et des polices
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2761923847a15be6b1ad51eec0d683129b70b349
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104991372"
---
# <a name="constructing-font-families-and-fonts"></a><span data-ttu-id="8bd29-103">Construction des familles de polices et des polices</span><span class="sxs-lookup"><span data-stu-id="8bd29-103">Constructing Font Families and Fonts</span></span>

<span data-ttu-id="8bd29-104">Windows GDI+ regroupe des polices avec la même police mais des styles différents dans des familles de polices.</span><span class="sxs-lookup"><span data-stu-id="8bd29-104">Windows GDI+ groups fonts with the same typeface but different styles into font families.</span></span> <span data-ttu-id="8bd29-105">Par exemple, la famille de polices Arial contient les polices suivantes :</span><span class="sxs-lookup"><span data-stu-id="8bd29-105">For example, the Arial font family contains the following fonts:</span></span>

-   <span data-ttu-id="8bd29-106">Arial normal</span><span class="sxs-lookup"><span data-stu-id="8bd29-106">Arial Regular</span></span>
-   <span data-ttu-id="8bd29-107">Arial gras</span><span class="sxs-lookup"><span data-stu-id="8bd29-107">Arial Bold</span></span>
-   <span data-ttu-id="8bd29-108">Arial italique</span><span class="sxs-lookup"><span data-stu-id="8bd29-108">Arial Italic</span></span>
-   <span data-ttu-id="8bd29-109">Arial gras italique</span><span class="sxs-lookup"><span data-stu-id="8bd29-109">Arial Bold Italic</span></span>

<span data-ttu-id="8bd29-110">GDI+ utilise quatre styles pour former les familles : normal, gras, italique et gras italique.</span><span class="sxs-lookup"><span data-stu-id="8bd29-110">GDI+ uses four styles to form families: regular, bold, italic, and bold italic.</span></span> <span data-ttu-id="8bd29-111">Les adjectifs tels que *Narrow* et *Rounded* ne sont pas considérés comme des styles ; ils font plutôt partie du nom de famille.</span><span class="sxs-lookup"><span data-stu-id="8bd29-111">Adjectives such as *narrow* and *rounded* are not considered styles; rather they are part of the family name.</span></span> <span data-ttu-id="8bd29-112">Par exemple, Arial Narrow est une famille de polices dont les membres sont les membres suivants :</span><span class="sxs-lookup"><span data-stu-id="8bd29-112">For example, Arial Narrow is a font family whose members are the following:</span></span>

-   <span data-ttu-id="8bd29-113">Arial étroit normal</span><span class="sxs-lookup"><span data-stu-id="8bd29-113">Arial Narrow Regular</span></span>
-   <span data-ttu-id="8bd29-114">Arial étroit gras</span><span class="sxs-lookup"><span data-stu-id="8bd29-114">Arial Narrow Bold</span></span>
-   <span data-ttu-id="8bd29-115">Arial étroit italique</span><span class="sxs-lookup"><span data-stu-id="8bd29-115">Arial Narrow Italic</span></span>
-   <span data-ttu-id="8bd29-116">Arial étroit gras italique</span><span class="sxs-lookup"><span data-stu-id="8bd29-116">Arial Narrow Bold Italic</span></span>

<span data-ttu-id="8bd29-117">Avant de pouvoir dessiner du texte avec GDI+, vous devez construire un objet [**FontFamily**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) et un objet [**font**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font) .</span><span class="sxs-lookup"><span data-stu-id="8bd29-117">Before you can draw text with GDI+, you need to construct a [**FontFamily**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) object and a [**Font**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font) object.</span></span> <span data-ttu-id="8bd29-118">Les objets **FontFamily** spécifient le type de caractères (par exemple, Arial) et l’objet **font** spécifie la taille, le style et les unités.</span><span class="sxs-lookup"><span data-stu-id="8bd29-118">The **FontFamily** objects specifies the typeface (for example, Arial), and the **Font** object specifies the size, style, and units.</span></span>

<span data-ttu-id="8bd29-119">L’exemple suivant construit une police Arial de style standard d’une taille de 16 pixels :</span><span class="sxs-lookup"><span data-stu-id="8bd29-119">The following example constructs a regular style Arial font with a size of 16 pixels:</span></span>


```
FontFamily fontFamily(L"Arial");
Font font(&fontFamily, 16, FontStyleRegular, UnitPixel);
            
```



<span data-ttu-id="8bd29-120">Dans le code précédent, le premier argument passé au constructeur [**font**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font) est l’adresse de l’objet [**FontFamily**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) .</span><span class="sxs-lookup"><span data-stu-id="8bd29-120">In the preceding code, the first argument passed to the [**Font**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font) constructor is the address of the [**FontFamily**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) object.</span></span> <span data-ttu-id="8bd29-121">Le deuxième argument spécifie la taille de la police mesurée en unités identifiées par le quatrième argument.</span><span class="sxs-lookup"><span data-stu-id="8bd29-121">The second argument specifies the size of the font measured in units identified by the fourth argument.</span></span> <span data-ttu-id="8bd29-122">Le troisième argument identifie le style.</span><span class="sxs-lookup"><span data-stu-id="8bd29-122">The third argument identifies the style.</span></span>

<span data-ttu-id="8bd29-123">[\* \* \* \* UnitPixel \* \*](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-unit) \* \* est un membre de l’énumération d' **unité** , et [\* \* \* \* FontStyleRegular \* \* \* \*](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-fontstyle) est un membre de l’énumération **FontStyle** .</span><span class="sxs-lookup"><span data-stu-id="8bd29-123">[\*\*\*\*UnitPixel\*\*\*\*](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-unit) is a member of the **Unit** enumeration, and [\*\*\*\*FontStyleRegular\*\*\*\*](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-fontstyle) is a member of the **FontStyle** enumeration.</span></span> <span data-ttu-id="8bd29-124">Les deux énumérations sont déclarées dans Gdiplusenums. h.</span><span class="sxs-lookup"><span data-stu-id="8bd29-124">Both enumerations are declared in Gdiplusenums.h.</span></span>

 

 



