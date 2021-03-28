---
description: L’anticrénelage Microsoft ClearType est une méthode de lissage qui améliore la résolution d’affichage des polices par rapport à l’anticrénelage traditionnel.
ms.assetid: b9896934-1e4f-4ae1-922a-ef30e0edf94f
title: Anticrénelage ClearType
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffbe7ae1a6c99fcee826c576b7671aea6e9ce6c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972759"
---
# <a name="cleartype-antialiasing"></a><span data-ttu-id="c9b04-103">Anticrénelage ClearType</span><span class="sxs-lookup"><span data-stu-id="c9b04-103">ClearType Antialiasing</span></span>

<span data-ttu-id="c9b04-104">L’anticrénelage Microsoft ClearType est une méthode de lissage qui améliore la résolution d’affichage des polices par rapport à l’anticrénelage traditionnel.</span><span class="sxs-lookup"><span data-stu-id="c9b04-104">Microsoft ClearType antialiasing is a smoothing method that improves font display resolution over traditional antialiasing.</span></span> <span data-ttu-id="c9b04-105">Cela améliore considérablement la lisibilité sur les moniteurs LCD couleur avec une interface numérique, tels que ceux des ordinateurs portables et des écrans plats de haute qualité.</span><span class="sxs-lookup"><span data-stu-id="c9b04-105">It dramatically improves readability on color LCD monitors with a digital interface, such as those in laptops and high-quality flat desktop displays.</span></span> <span data-ttu-id="c9b04-106">La lisibilité sur les écrans CRT est également un peu améliorée.</span><span class="sxs-lookup"><span data-stu-id="c9b04-106">Readability on CRT screens is also somewhat improved.</span></span>

<span data-ttu-id="c9b04-107">Toutefois, ClearType dépend de l’orientation et de l’ordre des bandes LCD.</span><span class="sxs-lookup"><span data-stu-id="c9b04-107">However, ClearType is dependent on the orientation and ordering of the LCD stripes.</span></span> <span data-ttu-id="c9b04-108">À l’heure actuelle, ClearType est implémenté uniquement pour les écrans LCD avec des bandes verticales classées RVB.</span><span class="sxs-lookup"><span data-stu-id="c9b04-108">Currently, ClearType is implemented only for LCDs with vertical stripes that are ordered RGB.</span></span> <span data-ttu-id="c9b04-109">En particulier, cela affecte les Tablet PC, où l’affichage peut être orienté dans n’importe quelle direction et les écrans qui peuvent être remplacés par le mode portrait.</span><span class="sxs-lookup"><span data-stu-id="c9b04-109">In particular, this affects tablet PCs, where the display can be oriented in any direction, and those screens that can be turned from landscape to portrait.</span></span>

<span data-ttu-id="c9b04-110">L’anticrénelage ClearType est autorisé :</span><span class="sxs-lookup"><span data-stu-id="c9b04-110">ClearType antialiasing is allowed:</span></span>

-   <span data-ttu-id="c9b04-111">Pour les couleurs 16, 24 et 32 bits (désactivées pour 256 couleurs ou moins)</span><span class="sxs-lookup"><span data-stu-id="c9b04-111">For 16-, 24-, and 32-bit color (disabled for 256 colors or less)</span></span>
-   <span data-ttu-id="c9b04-112">Pour le contrôleur de l’écran et la mémoire DC (pas pour l’imprimante DC)</span><span class="sxs-lookup"><span data-stu-id="c9b04-112">For screen DC and memory DC (not for printer DC)</span></span>
-   <span data-ttu-id="c9b04-113">Pour les polices TrueType et OpenType avec des contours TrueType</span><span class="sxs-lookup"><span data-stu-id="c9b04-113">For TrueType fonts and OpenType fonts with TrueType outlines</span></span>

<span data-ttu-id="c9b04-114">L’anticrénelage ClearType est désactivé :</span><span class="sxs-lookup"><span data-stu-id="c9b04-114">ClearType antialiasing is disabled:</span></span>

-   <span data-ttu-id="c9b04-115">Sous client Terminal Server</span><span class="sxs-lookup"><span data-stu-id="c9b04-115">Under terminal server client</span></span>
-   <span data-ttu-id="c9b04-116">Pour les polices bitmap, les polices vectorielles, les polices de périphérique, les polices de type 1 ou les polices PostScript OpenType sans les contours TrueType</span><span class="sxs-lookup"><span data-stu-id="c9b04-116">For bitmap fonts, vector fonts, device fonts, Type 1 fonts, or Postscript OpenType fonts without TrueType outlines</span></span>
-   <span data-ttu-id="c9b04-117">Si la police a réglé des bitmaps incorporées, uniquement pour les tailles de police qui contiennent les bitmaps incorporées</span><span class="sxs-lookup"><span data-stu-id="c9b04-117">If the font has tuned embedded bitmaps, only for those font sizes that contain the embedded bitmaps</span></span>

<span data-ttu-id="c9b04-118">Pour activer l’anticrénelage ClearType, appelez [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) une fois pour activer le lissage des polices, puis une deuxième fois pour définir le type de lissage sur Fe \_ FONTSMOOTHINGCLEARTYPE, comme illustré dans l’exemple de code suivant :</span><span class="sxs-lookup"><span data-stu-id="c9b04-118">To activate ClearType antialiasing, call [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) once to turn on font smoothing and then a second time to set the smoothing type to FE\_FONTSMOOTHINGCLEARTYPE, as shown in the following code sample:</span></span>


```C++
SystemParametersInfo(SPI_SETFONTSMOOTHING,
                     TRUE,
                     0,
                     SPIF_UPDATEINIFILE | SPIF_SENDCHANGE);
SystemParametersInfo(SPI_SETFONTSMOOTHINGTYPE,
                     0,
                     (PVOID)FE_FONTSMOOTHINGCLEARTYPE,
                     SPIF_UPDATEINIFILE | SPIF_SENDCHANGE); 
```



<span data-ttu-id="c9b04-119">Vous pouvez ajuster l’apparence du texte en modifiant la valeur de contraste utilisée dans l’algorithme ClearType.</span><span class="sxs-lookup"><span data-stu-id="c9b04-119">You can adjust the appearance of text by changing the contrast value used in the ClearType algorithm.</span></span> <span data-ttu-id="c9b04-120">La valeur par défaut est 1 400, mais il peut s’agir de n’importe quelle valeur comprise entre 1 000 et 2 200.</span><span class="sxs-lookup"><span data-stu-id="c9b04-120">The default is 1,400, but it can be any value from 1,000 to 2,200.</span></span> <span data-ttu-id="c9b04-121">En fonction du périphérique d’affichage et de la sensibilité de l’utilisateur aux couleurs, une valeur de contraste supérieure ou inférieure peut améliorer la lisibilité.</span><span class="sxs-lookup"><span data-stu-id="c9b04-121">Depending on the display device and the user's sensitivity to colors, a higher or lower contrast value may improve readability.</span></span> <span data-ttu-id="c9b04-122">Pour modifier le contraste, appelez [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) avec SPI \_ SETFONTSMOOTHINGCONTRAST.</span><span class="sxs-lookup"><span data-stu-id="c9b04-122">To change the contrast, call [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) with SPI\_SETFONTSMOOTHINGCONTRAST.</span></span> <span data-ttu-id="c9b04-123">Le code suivant définit la valeur de contraste sur 1 600.</span><span class="sxs-lookup"><span data-stu-id="c9b04-123">The following code sets the contrast value to 1,600.</span></span>


```C++
SystemParametersInfo(SPI_SETFONTSMOOTHINGCONTRAST,
                     0,
                     (PVOID)1600,
                     SPIF_UPDATEINIFILE | SPIF_SENDCHANGE); 
```



<span data-ttu-id="c9b04-124">Vous devez prendre en compte les détails suivants pour la compatibilité des applications :</span><span class="sxs-lookup"><span data-stu-id="c9b04-124">You should consider the following details for application compatibility:</span></span>

-   <span data-ttu-id="c9b04-125">Le rendu du texte avec ClearType est légèrement plus lent qu’avec l’anticrénelage standard.</span><span class="sxs-lookup"><span data-stu-id="c9b04-125">Text rendering with ClearType is slightly slower than with standard antialiasing.</span></span>
-   <span data-ttu-id="c9b04-126">Les applications ne doivent pas utiliser XOR pour afficher le texte sélectionné.</span><span class="sxs-lookup"><span data-stu-id="c9b04-126">Applications should not use XOR to display selected text.</span></span> <span data-ttu-id="c9b04-127">Les applications doivent définir la couleur d’arrière-plan et afficher à nouveau le texte sélectionné.</span><span class="sxs-lookup"><span data-stu-id="c9b04-127">Applications should set the background color and redisplay the selected text.</span></span>
-   <span data-ttu-id="c9b04-128">Les applications ne doivent pas peindre le même texte sur lui-même en mode transparent.</span><span class="sxs-lookup"><span data-stu-id="c9b04-128">Applications should not paint the same text on top of itself in transparent mode.</span></span> <span data-ttu-id="c9b04-129">Si cela se produit, les pixels de bord qui sont anticrénelages sont fusionnés avec eux-mêmes et non avec la couleur d’arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="c9b04-129">If this occurs, the edge pixels that are antialiased will color merge with themselves instead of with the background color.</span></span> <span data-ttu-id="c9b04-130">Cela donne des bords sombres et colorés.</span><span class="sxs-lookup"><span data-stu-id="c9b04-130">This results in darkened and colorful edges.</span></span>
-   <span data-ttu-id="c9b04-131">Les applications ne doivent pas peindre du texte en peignant les caractères individuellement en mode opaque, car le bord d’un caractère peut être coupé par le caractère suivant.</span><span class="sxs-lookup"><span data-stu-id="c9b04-131">Applications should not paint text by painting the characters individually when in opaque mode because the edge of a character may be clipped by the following character.</span></span> <span data-ttu-id="c9b04-132">Cela est dû au fait qu’un caractère lissé avec ClearType peut avoir une largeur A ou C négative, où le caractère normal a une largeur positive a ou C.</span><span class="sxs-lookup"><span data-stu-id="c9b04-132">This occurs because a character that is smoothed with ClearType may have a negative A or C width where the regular character has a positive A or C width.</span></span> <span data-ttu-id="c9b04-133">Seule la largeur B du caractère est garantie comme étant identique.</span><span class="sxs-lookup"><span data-stu-id="c9b04-133">Only the B width of the character is guaranteed to be the same.</span></span> <span data-ttu-id="c9b04-134">De même, les applications doivent faire attention si le texte lissé est en regard de texte non lissé.</span><span class="sxs-lookup"><span data-stu-id="c9b04-134">Likewise, applications should be careful if smoothed text is next to unsmoothed text.</span></span>
-   <span data-ttu-id="c9b04-135">Si une application restitue le texte, puis manipule la bitmap, le lissage des polices doit être désactivé en définissant le membre **lfQuality** de la structure [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) sur la \_ qualité NONANTIALIASED.</span><span class="sxs-lookup"><span data-stu-id="c9b04-135">If an application renders text and then manipulates the bitmap, font smoothing should be turned off by setting the **lfQuality** member of the [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) structure to NONANTIALIASED\_QUALITY.</span></span> <span data-ttu-id="c9b04-136">Par exemple, un jeu peut ajouter un effet d’ombre bitmap, ou le texte rendu dans une bitmap peut être mis à l’échelle pour produire un Thumbview.</span><span class="sxs-lookup"><span data-stu-id="c9b04-136">For example, a game may add a bitmap shadow effect, or text rendered into a bitmap may be scaled to produce a thumbview.</span></span>
-   <span data-ttu-id="c9b04-137">Si l’utilisateur s’exécute en mode Portrait (c’est-à-dire que l’entrelacement est horizontal), l’anticrénelage ClearType doit être désactivé.</span><span class="sxs-lookup"><span data-stu-id="c9b04-137">If the user is running in portrait mode (that is, monitor striping is horizontal) ClearType antialiasing should be disabled.</span></span>

<span data-ttu-id="c9b04-138">Le paramètre *fdwQuality* dans [**CreateFont**](/windows/desktop/api/Wingdi/nf-wingdi-createfonta) et le membre **lfQuality** de [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) acceptent l’indicateur de \_ qualité CLEARTYPE.</span><span class="sxs-lookup"><span data-stu-id="c9b04-138">The *fdwQuality* parameter in [**CreateFont**](/windows/desktop/api/Wingdi/nf-wingdi-createfonta) and the **lfQuality** member of [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) accept the CLEARTYPE\_QUALITY flag.</span></span> <span data-ttu-id="c9b04-139">La pixellisation des polices créées avec cet indicateur utilise le rastériseur ClearType.</span><span class="sxs-lookup"><span data-stu-id="c9b04-139">Rasterization of fonts created with this flag will use the ClearType rasterizer.</span></span> <span data-ttu-id="c9b04-140">Cet indicateur n’a aucun effet sur les versions précédentes du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="c9b04-140">This flag has no effect on previous versions of the operating system.</span></span>

 

 
