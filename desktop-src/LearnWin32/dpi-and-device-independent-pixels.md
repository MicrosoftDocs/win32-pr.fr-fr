---
title: PPP et Device-Independent pixels
ms.assetid: d282de02-62f4-4a12-a77c-f602f6db0216
description: 'En savoir plus sur : PPP et Device-Independent pixels'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e6f04e1a056611fcdfe8b59ff65b38ecec99eaf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868661"
---
# <a name="dpi-and-device-independent-pixels"></a><span data-ttu-id="12240-103">PPP et Device-Independent pixels</span><span class="sxs-lookup"><span data-stu-id="12240-103">DPI and Device-Independent Pixels</span></span>

<span data-ttu-id="12240-104">Pour programmer efficacement avec les graphiques Windows, vous devez comprendre deux concepts connexes :</span><span class="sxs-lookup"><span data-stu-id="12240-104">To program effectively with Windows graphics, you must understand two related concepts:</span></span>

-   <span data-ttu-id="12240-105">Points par pouce (DPI)</span><span class="sxs-lookup"><span data-stu-id="12240-105">Dots per inch (DPI)</span></span>
-   <span data-ttu-id="12240-106">DIP (Device-Independent Pixel).</span><span class="sxs-lookup"><span data-stu-id="12240-106">Device-independent pixel (DIPs).</span></span>

<span data-ttu-id="12240-107">Commençons par PPP.</span><span class="sxs-lookup"><span data-stu-id="12240-107">Let's start with DPI.</span></span> <span data-ttu-id="12240-108">Cela nécessite un bref détournement dans la typographie.</span><span class="sxs-lookup"><span data-stu-id="12240-108">This will require a short detour into typography.</span></span> <span data-ttu-id="12240-109">Dans la typographie, la taille du type est mesurée en unités appelées *points*.</span><span class="sxs-lookup"><span data-stu-id="12240-109">In typography, the size of type is measured in units called *points*.</span></span> <span data-ttu-id="12240-110">Un point est égal à 1/72 de pouce.</span><span class="sxs-lookup"><span data-stu-id="12240-110">One point equals 1/72 of an inch.</span></span>

<dl> <span data-ttu-id="12240-111">1 PT = 1/72 pouces</span><span class="sxs-lookup"><span data-stu-id="12240-111">1 pt = 1/72 inch</span></span>  
</dl>

> [!Note]  
> <span data-ttu-id="12240-112">Il s’agit de la définition de la publication sur le Bureau du point.</span><span class="sxs-lookup"><span data-stu-id="12240-112">This is the desktop publishing definition of point.</span></span> <span data-ttu-id="12240-113">Historiquement, la mesure exacte d’un point a varié.</span><span class="sxs-lookup"><span data-stu-id="12240-113">Historically, the exact measure of a point has varied.</span></span>

 

<span data-ttu-id="12240-114">Par exemple, une police à 12 points est conçue pour tenir au sein d’une ligne de texte 1/6 "(12/72).</span><span class="sxs-lookup"><span data-stu-id="12240-114">For example, a 12-point font is designed to fit within a 1/6" (12/72) line of text.</span></span> <span data-ttu-id="12240-115">Évidemment, cela ne signifie pas que chaque caractère de la police correspond exactement à 1/6.</span><span class="sxs-lookup"><span data-stu-id="12240-115">Obviously, this does not mean that every character in the font is exactly 1/6" tall.</span></span> <span data-ttu-id="12240-116">En fait, certains caractères peuvent être plus grands que 1/6».</span><span class="sxs-lookup"><span data-stu-id="12240-116">In fact, some characters might be taller than 1/6".</span></span> <span data-ttu-id="12240-117">Par exemple, dans de nombreuses polices, le caractère Å est plus haut que la hauteur nominale de la police.</span><span class="sxs-lookup"><span data-stu-id="12240-117">For example, in many fonts the character Å is taller than the nominal height of the font.</span></span> <span data-ttu-id="12240-118">Pour s’afficher correctement, la police a besoin d’espace supplémentaire entre le texte.</span><span class="sxs-lookup"><span data-stu-id="12240-118">To display correctly, the font needs some additional space between the text.</span></span> <span data-ttu-id="12240-119">Cet espace est appelé le *début*.</span><span class="sxs-lookup"><span data-stu-id="12240-119">This space is called the *leading*.</span></span>

<span data-ttu-id="12240-120">L’illustration suivante montre une police de point de 72.</span><span class="sxs-lookup"><span data-stu-id="12240-120">The following illustration shows a 72-point font.</span></span> <span data-ttu-id="12240-121">Les lignes pleines affichent un cadre englobant 1 de haut autour du texte.</span><span class="sxs-lookup"><span data-stu-id="12240-121">The solid lines show a 1" tall bounding box around the text.</span></span> <span data-ttu-id="12240-122">La ligne en pointillés est appelée ligne de *base*.</span><span class="sxs-lookup"><span data-stu-id="12240-122">The dashed line is called the *baseline*.</span></span> <span data-ttu-id="12240-123">La plupart des caractères d’une police se trouvent dans la ligne de base.</span><span class="sxs-lookup"><span data-stu-id="12240-123">Most of the characters in a font rest on the baseline.</span></span> <span data-ttu-id="12240-124">La hauteur de la police comprend la partie au-dessus de la ligne de base (le plus *haut) et* la partie au-dessous de la ligne de base (la *descente*).</span><span class="sxs-lookup"><span data-stu-id="12240-124">The height of the font includes the portion above the baseline (the *ascent*) and the portion below the baseline (the *descent*).</span></span> <span data-ttu-id="12240-125">Dans la police indiquée ici, la hauteur est de 56 points et la descente est de 16 points.</span><span class="sxs-lookup"><span data-stu-id="12240-125">In the font shown here, the ascent is 56 points and the descent is 16 points.</span></span>

![illustration qui montre une police de point de 72.](images/graphics11.png)

<span data-ttu-id="12240-127">Toutefois, en cas d’affichage d’un ordinateur, la mesure de la taille du texte est problématique, car les pixels ne sont pas tous de la même taille.</span><span class="sxs-lookup"><span data-stu-id="12240-127">When it comes to a computer display, however, measuring text size is problematic, because pixels are not all the same size.</span></span> <span data-ttu-id="12240-128">La taille d’un pixel dépend de deux facteurs : la résolution d’affichage et la taille physique de l’analyse.</span><span class="sxs-lookup"><span data-stu-id="12240-128">The size of a pixel depends on two factors: the display resolution, and the physical size of the monitor.</span></span> <span data-ttu-id="12240-129">Par conséquent, les pouces physiques ne sont pas une mesure utile, car il n’existe aucune relation fixe entre les pouces et les pixels physiques.</span><span class="sxs-lookup"><span data-stu-id="12240-129">Therefore, physical inches are not a useful measure, because there is no fixed relation between physical inches and pixels.</span></span> <span data-ttu-id="12240-130">Au lieu de cela, les polices sont mesurées en unités *logiques* .</span><span class="sxs-lookup"><span data-stu-id="12240-130">Instead, fonts are measured in *logical* units.</span></span> <span data-ttu-id="12240-131">Une police de point 72 est définie pour être d’une hauteur de pouce logique.</span><span class="sxs-lookup"><span data-stu-id="12240-131">A 72-point font is defined to be one logical inch tall.</span></span> <span data-ttu-id="12240-132">Les pouces logiques sont ensuite convertis en pixels.</span><span class="sxs-lookup"><span data-stu-id="12240-132">Logical inches are then converted to pixels.</span></span> <span data-ttu-id="12240-133">Pendant de nombreuses années, Windows a utilisé la conversion suivante : un pouce logique est égal à 96 pixels.</span><span class="sxs-lookup"><span data-stu-id="12240-133">For many years, Windows used the following conversion: One logical inch equals 96 pixels.</span></span> <span data-ttu-id="12240-134">À l’aide de ce facteur d’échelle, une police de 72 points est rendue sous la forme de 96 pixels de haut.</span><span class="sxs-lookup"><span data-stu-id="12240-134">Using this scaling factor, a 72-point font is rendered as 96 pixels tall.</span></span> <span data-ttu-id="12240-135">Une police de 12 points a une hauteur de 16 pixels.</span><span class="sxs-lookup"><span data-stu-id="12240-135">A 12-point font is 16 pixels tall.</span></span>

<dl> <span data-ttu-id="12240-136">12 points = 12/72 de pouce logique = 1/6 de pouce logique = 96/6 pixels = 16 pixels</span><span class="sxs-lookup"><span data-stu-id="12240-136">12 points = 12/72 logical inch = 1/6 logical inch = 96/6 pixels = 16 pixels</span></span>  
</dl>

<span data-ttu-id="12240-137">Ce facteur d’échelle est décrit comme étant de 96 points par pouce (DPI).</span><span class="sxs-lookup"><span data-stu-id="12240-137">This scaling factor is described as 96 dots per inch (DPI).</span></span> <span data-ttu-id="12240-138">Le terme « points » dérive de l’impression, où les points physiques de l’encre sont mis sur le papier.</span><span class="sxs-lookup"><span data-stu-id="12240-138">The term dots derives from printing, where physical dots of ink are put onto paper.</span></span> <span data-ttu-id="12240-139">Pour les écrans d’ordinateur, il serait plus précis d’indiquer 96 pixels par pouce logique, mais le terme PPP est bloqué.</span><span class="sxs-lookup"><span data-stu-id="12240-139">For computer displays, it would be more accurate to say 96 pixels per logical inch, but the term DPI has stuck.</span></span>

<span data-ttu-id="12240-140">Étant donné que les tailles réelles des pixels varient, le texte lisible sur un moniteur peut être trop petit sur un autre moniteur.</span><span class="sxs-lookup"><span data-stu-id="12240-140">Because actual pixel sizes vary, text that is readable on one monitor might be too small on another monitor.</span></span> <span data-ttu-id="12240-141">En outre, les utilisateurs ont des préférences différentes. certaines personnes préfèrent du texte plus grand.</span><span class="sxs-lookup"><span data-stu-id="12240-141">Also, people have different preferences—some people prefer larger text.</span></span> <span data-ttu-id="12240-142">C’est la raison pour laquelle Windows permet à l’utilisateur de modifier le paramètre PPP.</span><span class="sxs-lookup"><span data-stu-id="12240-142">For this reason, Windows enables the user to change the DPI setting.</span></span> <span data-ttu-id="12240-143">Par exemple, si l’utilisateur définit l’affichage sur 144 PPP, une police de 72 point est de 144 pixels de haut.</span><span class="sxs-lookup"><span data-stu-id="12240-143">For example, if the user sets the display to 144 DPI, a 72-point font is 144 pixels tall.</span></span> <span data-ttu-id="12240-144">Les paramètres ppp standard sont 100% (96 ppp), 125% (120 ppp) et 150% (144 PPP).</span><span class="sxs-lookup"><span data-stu-id="12240-144">The standard DPI settings are 100% (96 DPI), 125% (120 DPI), and 150% (144 DPI).</span></span> <span data-ttu-id="12240-145">L’utilisateur peut également appliquer un paramètre personnalisé.</span><span class="sxs-lookup"><span data-stu-id="12240-145">The user can also apply a custom setting.</span></span> <span data-ttu-id="12240-146">À partir de Windows 7, PPP est un paramètre par utilisateur.</span><span class="sxs-lookup"><span data-stu-id="12240-146">Starting in Windows 7, DPI is a per-user setting.</span></span>

## <a name="dwm-scaling"></a><span data-ttu-id="12240-147">Mise à l’échelle DWM</span><span class="sxs-lookup"><span data-stu-id="12240-147">DWM Scaling</span></span>

<span data-ttu-id="12240-148">Si un programme ne compte pas pour la résolution PPP, les erreurs suivantes peuvent être apparentes aux paramètres haute résolution :</span><span class="sxs-lookup"><span data-stu-id="12240-148">If a program does not account for DPI, the following defects might be apparent at high-DPI settings:</span></span>

-   <span data-ttu-id="12240-149">Éléments d’interface utilisateur découpés.</span><span class="sxs-lookup"><span data-stu-id="12240-149">Clipped UI elements.</span></span>
-   <span data-ttu-id="12240-150">Disposition incorrecte.</span><span class="sxs-lookup"><span data-stu-id="12240-150">Incorrect layout.</span></span>
-   <span data-ttu-id="12240-151">Bitmaps et icônes pixellisée.</span><span class="sxs-lookup"><span data-stu-id="12240-151">Pixelated bitmaps and icons.</span></span>
-   <span data-ttu-id="12240-152">Coordonnées de souris incorrectes, qui peuvent affecter le test de positionnement, le glisser-déplacer, etc.</span><span class="sxs-lookup"><span data-stu-id="12240-152">Incorrect mouse coordinates, which can affect hit testing, drag and drop, and so forth.</span></span>

<span data-ttu-id="12240-153">Pour vous assurer que les anciens programmes fonctionnent aux paramètres haute résolution, le DWM implémente un secours utile.</span><span class="sxs-lookup"><span data-stu-id="12240-153">To ensure that older programs work at high-DPI settings, the DWM implements a useful fallback.</span></span> <span data-ttu-id="12240-154">Si un programme n’est pas marqué comme prenant en charge DPI, le DWM met à l’échelle la totalité de l’interface utilisateur pour correspondre au paramètre PPP.</span><span class="sxs-lookup"><span data-stu-id="12240-154">If a program is not marked as being DPI aware, the DWM will scale the entire UI to match the DPI setting.</span></span> <span data-ttu-id="12240-155">Par exemple, à 144 PPP, l’interface utilisateur est mise à l’échelle de 150%, y compris du texte, des graphiques, des contrôles et des tailles de fenêtre.</span><span class="sxs-lookup"><span data-stu-id="12240-155">For example, at 144 DPI, the UI is scaled by 150%, including text, graphics, controls, and window sizes.</span></span> <span data-ttu-id="12240-156">Si le programme crée une fenêtre 500 × 500, la fenêtre s’affiche en réalité sous la forme 750 × 750 pixels et le contenu de la fenêtre est mis à l’échelle en conséquence.</span><span class="sxs-lookup"><span data-stu-id="12240-156">If the program creates a 500 × 500 window, the window actually appears as 750 × 750 pixels, and the contents of the window are scaled accordingly.</span></span>

<span data-ttu-id="12240-157">Ce comportement signifie que les anciens programmes « fonctionnent » dans les paramètres haute résolution.</span><span class="sxs-lookup"><span data-stu-id="12240-157">This behavior means that older programs "just work" at high-DPI settings.</span></span> <span data-ttu-id="12240-158">Toutefois, la mise à l’échelle aboutit également à une apparence légèrement floue, car la mise à l’échelle est appliquée après le dessin de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="12240-158">However, scaling also results in a somewhat blurry appearance, because the scaling is applied after the window is drawn.</span></span>

## <a name="dpi-aware-applications"></a><span data-ttu-id="12240-159">Applications DPI-Aware</span><span class="sxs-lookup"><span data-stu-id="12240-159">DPI-Aware Applications</span></span>

<span data-ttu-id="12240-160">Pour éviter la mise à l’échelle DWM, un programme peut se marquer comme prenant en charge DPI.</span><span class="sxs-lookup"><span data-stu-id="12240-160">To avoid DWM scaling, a program can mark itself as DPI-aware.</span></span> <span data-ttu-id="12240-161">Cela indique au DWM de ne pas effectuer de mise à l’échelle DPI automatique.</span><span class="sxs-lookup"><span data-stu-id="12240-161">This tells the DWM not to perform any automatic DPI scaling.</span></span> <span data-ttu-id="12240-162">Toutes les nouvelles applications doivent être conçues pour être compatibles DPI, car la reconnaissance DPI améliore l’apparence de l’interface utilisateur à des paramètres ppp plus élevés.</span><span class="sxs-lookup"><span data-stu-id="12240-162">All new applications should be designed to be DPI-aware, because DPI awareness improves the appearance of the UI at higher DPI settings.</span></span>

<span data-ttu-id="12240-163">Un programme déclare lui-même la prise en charge DPI par le biais de son manifeste d’application.</span><span class="sxs-lookup"><span data-stu-id="12240-163">A program declares itself DPI-aware through its application manifest.</span></span> <span data-ttu-id="12240-164">Un *manifeste* est un simple fichier XML qui décrit une dll ou une application.</span><span class="sxs-lookup"><span data-stu-id="12240-164">A *manifest* is a simply an XML file that describes a DLL or application.</span></span> <span data-ttu-id="12240-165">Le manifeste est généralement incorporé dans le fichier exécutable, bien qu’il puisse être fourni sous la forme d’un fichier distinct.</span><span class="sxs-lookup"><span data-stu-id="12240-165">The manifest is typically embedded in the executable file, although it can be provided as a separate file.</span></span> <span data-ttu-id="12240-166">Un manifeste contient des informations telles que les dépendances de DLL, le niveau de privilège demandé et la version de Windows pour laquelle le programme a été conçu.</span><span class="sxs-lookup"><span data-stu-id="12240-166">A manifest contains information such as DLL dependencies, the requested privilege level, and what version of Windows the program was designed for.</span></span>

<span data-ttu-id="12240-167">Pour déclarer que votre programme prend en charge DPI, incluez les informations suivantes dans le manifeste.</span><span class="sxs-lookup"><span data-stu-id="12240-167">To declare that your program is DPI-aware, include the following information in the manifest.</span></span>

``` syntax
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0" xmlns:asmv3="urn:schemas-microsoft-com:asm.v3" >
  <asmv3:application>
    <asmv3:windowsSettings xmlns="http://schemas.microsoft.com/SMI/2005/WindowsSettings">
      <dpiAware>true</dpiAware>
    </asmv3:windowsSettings>
  </asmv3:application>
</assembly>
```

<span data-ttu-id="12240-168">La liste présentée ici n’est qu’un manifeste partiel, mais l’éditeur de liens de Visual Studio génère automatiquement le reste du manifeste.</span><span class="sxs-lookup"><span data-stu-id="12240-168">The listing shown here is only a partial manifest, but the Visual Studio linker generates the rest of the manifest for you automatically.</span></span> <span data-ttu-id="12240-169">Pour inclure un manifeste partiel dans votre projet, procédez comme suit dans Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="12240-169">To include a partial manifest in your project, perform the following steps in Visual Studio.</span></span>

1.  <span data-ttu-id="12240-170">Dans le menu **projet** , cliquez sur **propriété**.</span><span class="sxs-lookup"><span data-stu-id="12240-170">On the **Project** menu, click **Property**.</span></span>
2.  <span data-ttu-id="12240-171">Dans le volet gauche, développez **Propriétés de configuration**, développez **outil manifeste**, puis cliquez sur **entrée et sortie**.</span><span class="sxs-lookup"><span data-stu-id="12240-171">In the left pane, expand **Configuration Properties**, expand **Manifest Tool**, and then click **Input and Output**.</span></span>
3.  <span data-ttu-id="12240-172">Dans la zone de texte **fichiers manifeste supplémentaires** , tapez le nom du fichier manifeste, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="12240-172">In the **Additional Manifest Files** text box, type the name of the manifest file, and then click **OK**.</span></span>

<span data-ttu-id="12240-173">En marquant votre programme comme prenant en charge DPI, vous indiquez au DWM de ne pas mettre à l’échelle la fenêtre de votre application.</span><span class="sxs-lookup"><span data-stu-id="12240-173">By marking your program as DPI-aware, you are telling the DWM not to scale your application window.</span></span> <span data-ttu-id="12240-174">Maintenant, si vous créez une fenêtre 500 × 500, la fenêtre occupe 500 × 500 pixels, quel que soit le paramètre PPP de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="12240-174">Now if you create a 500 × 500 window, the window will occupy 500 × 500 pixels, regardless of the user's DPI setting.</span></span>

## <a name="gdi-and-dpi"></a><span data-ttu-id="12240-175">GDI et PPP</span><span class="sxs-lookup"><span data-stu-id="12240-175">GDI and DPI</span></span>

<span data-ttu-id="12240-176">Le dessin GDI est mesuré en pixels.</span><span class="sxs-lookup"><span data-stu-id="12240-176">GDI drawing is measured in pixels.</span></span> <span data-ttu-id="12240-177">Cela signifie que si votre programme est marqué comme prenant en charge DPI et que vous demandez à GDI de dessiner un rectangle 200 × 100, le rectangle résultant sera 200 pixels de largeur et 100 pixels de haut sur l’écran.</span><span class="sxs-lookup"><span data-stu-id="12240-177">That means if your program is marked as DPI-aware, and you ask GDI to draw a 200 × 100 rectangle, the resulting rectangle will be 200 pixels wide and 100 pixels tall on the screen.</span></span> <span data-ttu-id="12240-178">Toutefois, les tailles de police GDI sont mises à l’échelle au paramètre PPP actuel.</span><span class="sxs-lookup"><span data-stu-id="12240-178">However, GDI font sizes are scaled to the current DPI setting.</span></span> <span data-ttu-id="12240-179">En d’autres termes, si vous créez une police de point de 72, la taille de la police sera de 96 pixels à 96 ppp, mais 144 pixels à 144 DPI.</span><span class="sxs-lookup"><span data-stu-id="12240-179">In other words, if you create a 72-point font, the size of the font will be 96 pixels at 96 DPI, but 144 pixels at 144 DPI.</span></span> <span data-ttu-id="12240-180">Voici une police de 72 points rendue à 144 PPP à l’aide de GDI.</span><span class="sxs-lookup"><span data-stu-id="12240-180">Here is a 72 point font rendered at 144 DPI using GDI.</span></span>

![diagramme qui affiche la mise à l’échelle des polices en DPI dans GDI.](images/graphics12.png)

<span data-ttu-id="12240-182">Si votre application prend en charge DPI et que vous utilisez GDI pour le dessin, mettez à l’échelle toutes vos coordonnées de dessin pour qu’elles correspondent aux PPP.</span><span class="sxs-lookup"><span data-stu-id="12240-182">If your application is DPI-aware and you use GDI for drawing, scale all of your drawing coordinates to match the DPI.</span></span>

## <a name="direct2d-and-dpi"></a><span data-ttu-id="12240-183">Direct2D et PPP</span><span class="sxs-lookup"><span data-stu-id="12240-183">Direct2D and DPI</span></span>

<span data-ttu-id="12240-184">Direct2D effectue automatiquement une mise à l’échelle pour correspondre au paramètre PPP.</span><span class="sxs-lookup"><span data-stu-id="12240-184">Direct2D automatically performs scaling to match the DPI setting.</span></span> <span data-ttu-id="12240-185">Dans Direct2D, les coordonnées sont mesurées en unités appelées *pixels indépendants du périphérique* (DIP).</span><span class="sxs-lookup"><span data-stu-id="12240-185">In Direct2D, coordinates are measured in units called *device-independent pixels* (DIPs).</span></span> <span data-ttu-id="12240-186">Une DIP est définie comme 1/96ème d’un pouce *logique* .</span><span class="sxs-lookup"><span data-stu-id="12240-186">A DIP is defined as 1/96th of a *logical* inch.</span></span> <span data-ttu-id="12240-187">Dans Direct2D, toutes les opérations de dessin sont spécifiées dans des DIP, puis mises à l’échelle avec le paramètre PPP actuel.</span><span class="sxs-lookup"><span data-stu-id="12240-187">In Direct2D, all drawing operations are specified in DIPs and then scaled to the current DPI setting.</span></span>



| <span data-ttu-id="12240-188">Paramètre PPP</span><span class="sxs-lookup"><span data-stu-id="12240-188">DPI setting</span></span> | <span data-ttu-id="12240-189">Taille d’adresse DIP</span><span class="sxs-lookup"><span data-stu-id="12240-189">DIP size</span></span>    |
|-------------|-------------|
| <span data-ttu-id="12240-190">96</span><span class="sxs-lookup"><span data-stu-id="12240-190">96</span></span>          | <span data-ttu-id="12240-191">1 pixel</span><span class="sxs-lookup"><span data-stu-id="12240-191">1 pixel</span></span>     |
| <span data-ttu-id="12240-192">120</span><span class="sxs-lookup"><span data-stu-id="12240-192">120</span></span>         | <span data-ttu-id="12240-193">1,25 pixels</span><span class="sxs-lookup"><span data-stu-id="12240-193">1.25 pixels</span></span> |
| <span data-ttu-id="12240-194">144</span><span class="sxs-lookup"><span data-stu-id="12240-194">144</span></span>         | <span data-ttu-id="12240-195">1,5 pixels</span><span class="sxs-lookup"><span data-stu-id="12240-195">1.5 pixels</span></span>  |



 

<span data-ttu-id="12240-196">Par exemple, si le paramètre PPP de l’utilisateur est de 144 PPP et que vous demandez à Direct2D de dessiner un rectangle 200 × 100, le rectangle sera 300 × 150 pixels physiques.</span><span class="sxs-lookup"><span data-stu-id="12240-196">For example, if the user's DPI setting is 144 DPI, and you ask Direct2D to draw a 200 × 100 rectangle, the rectangle will be 300 × 150 physical pixels.</span></span> <span data-ttu-id="12240-197">De plus, DirectWrite mesure les tailles de police dans des DIP, plutôt que des points.</span><span class="sxs-lookup"><span data-stu-id="12240-197">In addition, DirectWrite measures font sizes in DIPs, rather than points.</span></span> <span data-ttu-id="12240-198">Pour créer une police de 12 points, spécifiez 16 DIP (12 points = 1/6 de pouce logique = 96/6 DIP).</span><span class="sxs-lookup"><span data-stu-id="12240-198">To create a 12-point font, specify 16 DIPs (12 points = 1/6 logical inch = 96/6 DIPs).</span></span> <span data-ttu-id="12240-199">Lorsque le texte est dessiné à l’écran, Direct2D convertit les DIP en pixels physiques.</span><span class="sxs-lookup"><span data-stu-id="12240-199">When the text is drawn on the screen, Direct2D converts the DIPs to physical pixels.</span></span> <span data-ttu-id="12240-200">L’avantage de ce système est que les unités de mesure sont cohérentes pour le texte et le dessin, quel que soit le paramètre PPP actuel.</span><span class="sxs-lookup"><span data-stu-id="12240-200">The benefit of this system is that the units of measurement are consistent for both text and drawing, regardless of the current DPI setting.</span></span>

<span data-ttu-id="12240-201">Un mot de prudence : les coordonnées de la souris et de la fenêtre sont toujours données en pixels physiques, et non en DIP.</span><span class="sxs-lookup"><span data-stu-id="12240-201">A word of caution: Mouse and window coordinates are still given in physical pixels, not DIPs.</span></span> <span data-ttu-id="12240-202">Par exemple, si vous traitez le message [**WM \_ LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown) , la position de la souris est indiquée en pixels physiques.</span><span class="sxs-lookup"><span data-stu-id="12240-202">For example, if you process the [**WM\_LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown) message, the mouse-down position is given in physical pixels.</span></span> <span data-ttu-id="12240-203">Pour dessiner un point à cette position, vous devez convertir les coordonnées en pixels en DIP.</span><span class="sxs-lookup"><span data-stu-id="12240-203">To draw a point at that position, you must convert the pixel coordinates to DIPs.</span></span>

## <a name="converting-physical-pixels-to-dips"></a><span data-ttu-id="12240-204">Conversion de pixels physiques en DIP</span><span class="sxs-lookup"><span data-stu-id="12240-204">Converting Physical Pixels to DIPs</span></span>

<span data-ttu-id="12240-205">La conversion de pixels physiques en DIP utilise la formule suivante.</span><span class="sxs-lookup"><span data-stu-id="12240-205">The conversion from physical pixels to DIPs uses the following formula.</span></span>

<dl> <span data-ttu-id="12240-206">DIP = pixels/(DPI/96.0)</span><span class="sxs-lookup"><span data-stu-id="12240-206">DIPs = pixels / (DPI/96.0)</span></span>  
</dl>

<span data-ttu-id="12240-207">Pour connaître le paramètre ppp, appelez la méthode [**ID2D1Factory :: GetDesktopDpi**](/windows/desktop/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) .</span><span class="sxs-lookup"><span data-stu-id="12240-207">To get the DPI setting, call the [**ID2D1Factory::GetDesktopDpi**](/windows/desktop/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) method.</span></span> <span data-ttu-id="12240-208">La valeur PPP est retournée sous la forme de deux valeurs à virgule flottante, une pour l’axe des x et une pour l’axe des y.</span><span class="sxs-lookup"><span data-stu-id="12240-208">The DPI is returned as two floating-point values, one for the x-axis and one for the y-axis.</span></span> <span data-ttu-id="12240-209">En théorie, ces valeurs peuvent différer.</span><span class="sxs-lookup"><span data-stu-id="12240-209">In theory, these values can differ.</span></span> <span data-ttu-id="12240-210">Calculez un facteur d’échelle distinct pour chaque axe.</span><span class="sxs-lookup"><span data-stu-id="12240-210">Calculate a separate scaling factor for each axis.</span></span>


```C++
float g_DPIScaleX = 1.0f;
float g_DPIScaleY = 1.0f;

void InitializeDPIScale(ID2D1Factory *pFactory)
{
    FLOAT dpiX, dpiY;

    pFactory->GetDesktopDpi(&dpiX, &dpiY);

    g_DPIScaleX = dpiX/96.0f;
    g_DPIScaleY = dpiY/96.0f;
}

template <typename T>
float PixelsToDipsX(T x)
{
    return static_cast<float>(x) / g_DPIScaleX;
}

template <typename T>
float PixelsToDipsY(T y)
{
    return static_cast<float>(y) / g_DPIScaleY;
}
```



<span data-ttu-id="12240-211">Voici une autre façon d’utiliser le paramètre PPP si vous n’utilisez pas Direct2D :</span><span class="sxs-lookup"><span data-stu-id="12240-211">Here is an alternate way to get the DPI setting if you are not using Direct2D:</span></span>


```C++
void InitializeDPIScale(HWND hwnd)
{
    HDC hdc = GetDC(hwnd);
    g_DPIScaleX = GetDeviceCaps(hdc, LOGPIXELSX) / 96.0f;
    g_DPIScaleY = GetDeviceCaps(hdc, LOGPIXELSY) / 96.0f;
    ReleaseDC(hwnd, hdc);
}
```
> [!Note]  
> <span data-ttu-id="12240-212">Sur Windows 10, la version 1903,  [**ID2D1Factory :: GetDesktopDpi**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) est dépréciée et la recommandation est [**DisplayInformation :: LogicalDpi**](/uwp/api/windows.graphics.display.displayinformation.logicaldpi?view=winrt-19041) pour les applications du Windows Store ou [**GetDpiForWindow**](/windows/win32/api/winuser/nf-winuser-getdpiforwindow) pour les applications de bureau.</span><span class="sxs-lookup"><span data-stu-id="12240-212">On Windows 10, version 1903,  [**ID2D1Factory::GetDesktopDpi**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) is deprecated and the recommendation is [**DisplayInformation::LogicalDpi**](/uwp/api/windows.graphics.display.displayinformation.logicaldpi?view=winrt-19041) for Windows Store Apps or [**GetDpiForWindow**](/windows/win32/api/winuser/nf-winuser-getdpiforwindow) for desktop apps.</span></span> <span data-ttu-id="12240-213">Si vous souhaitez toujours l’utiliser, supprimez le message d’erreur du compilateur en écrivant la ligne [**#pragma avertissement (supprimer : 4996)**](/cpp/error-messages/compiler-warnings/compiler-warning-level-3-c4996?view=vs-2019) juste avant l’appel de [**ID2D1Factory :: GetDesktopDpi**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) .</span><span class="sxs-lookup"><span data-stu-id="12240-213">If you still want to use it, suppress the compiler error message by writing the line [**#pragma warning(suppress: 4996)**](/cpp/error-messages/compiler-warnings/compiler-warning-level-3-c4996?view=vs-2019) just before the [**ID2D1Factory::GetDesktopDpi**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) call.</span></span> <span data-ttu-id="12240-214">Bien qu’il ne soit pas recommandé, il est possible de définir la reconnaissance par défaut des PPP par programmation à l’aide de [**SetProcessDpiAwarenessContext**](/windows/win32/api/winuser/nf-winuser-setprocessdpiawarenesscontext).</span><span class="sxs-lookup"><span data-stu-id="12240-214">Although it is not recommended, it is possible to set the default DPI awareness programmatically using [**SetProcessDpiAwarenessContext**](/windows/win32/api/winuser/nf-winuser-setprocessdpiawarenesscontext).</span></span> <span data-ttu-id="12240-215">Une fois qu’une fenêtre (HWND) a été créée dans votre processus, la modification du mode de reconnaissance PPP n’est plus prise en charge.</span><span class="sxs-lookup"><span data-stu-id="12240-215">Once a window (an HWND) has been created in your process, changing the DPI awareness mode is no longer supported.</span></span> <span data-ttu-id="12240-216">Si vous définissez le mode de prise en forme des PPP par défaut du processus par programme, vous devez appeler l’API correspondante avant la création de tous les HWND.</span><span class="sxs-lookup"><span data-stu-id="12240-216">If you are setting the process-default DPI awareness mode programmatically, you must call the corresponding API before any HWNDs have been created.</span></span> <span data-ttu-id="12240-217">Pour plus d’informations, consultez [définition de la prise en face PPP par défaut d’un processus](../hidpi/setting-the-default-dpi-awareness-for-a-process.md).</span><span class="sxs-lookup"><span data-stu-id="12240-217">For information see [Setting the default DPI awareness for a process](../hidpi/setting-the-default-dpi-awareness-for-a-process.md).</span></span>

## <a name="resizing-the-render-target"></a><span data-ttu-id="12240-218">Redimensionnement de la cible de rendu</span><span class="sxs-lookup"><span data-stu-id="12240-218">Resizing the Render Target</span></span>

<span data-ttu-id="12240-219">Si la taille de la fenêtre change, vous devez redimensionner la cible de rendu pour qu’elle corresponde.</span><span class="sxs-lookup"><span data-stu-id="12240-219">If the size of the window changes, you must resize the render target to match.</span></span> <span data-ttu-id="12240-220">Dans la plupart des cas, vous devrez également mettre à jour la disposition et redessiner la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="12240-220">In most cases, you will also need to update the layout and repaint the window.</span></span> <span data-ttu-id="12240-221">Le code suivant illustre ces étapes.</span><span class="sxs-lookup"><span data-stu-id="12240-221">The following code shows these steps.</span></span>


```C++
void MainWindow::Resize()
{
    if (pRenderTarget != NULL)
    {
        RECT rc;
        GetClientRect(m_hwnd, &rc);

        D2D1_SIZE_U size = D2D1::SizeU(rc.right, rc.bottom);

        pRenderTarget->Resize(size);
        CalculateLayout();
        InvalidateRect(m_hwnd, NULL, FALSE);
    }
}
```



<span data-ttu-id="12240-222">La fonction [**GetClientRect**](/windows/desktop/api/winuser/nf-winuser-getclientrect) obtient la nouvelle taille de la zone cliente, en pixels physiques (et non en DIP).</span><span class="sxs-lookup"><span data-stu-id="12240-222">The [**GetClientRect**](/windows/desktop/api/winuser/nf-winuser-getclientrect) function gets the new size of the client area, in physical pixels (not DIPs).</span></span> <span data-ttu-id="12240-223">La méthode [**ID2D1HwndRenderTarget :: Resize**](../direct2d/id2d1hwndrendertarget-resize.md) met à jour la taille de la cible de rendu, également spécifiée en pixels.</span><span class="sxs-lookup"><span data-stu-id="12240-223">The [**ID2D1HwndRenderTarget::Resize**](../direct2d/id2d1hwndrendertarget-resize.md) method updates the size of the render target, also specified in pixels.</span></span> <span data-ttu-id="12240-224">La fonction [**InvalidateRect**](/windows/desktop/api/winuser/nf-winuser-invalidaterect) force une redessine en ajoutant la zone cliente entière à la région de mise à jour de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="12240-224">The [**InvalidateRect**](/windows/desktop/api/winuser/nf-winuser-invalidaterect) function forces a repaint by adding the entire client area to the window's update region.</span></span> <span data-ttu-id="12240-225">(Consultez [peinture de la fenêtre](painting-the-window.md), dans le module 1.)</span><span class="sxs-lookup"><span data-stu-id="12240-225">(See [Painting the Window](painting-the-window.md), in Module 1.)</span></span>

<span data-ttu-id="12240-226">À mesure que la fenêtre s’agrandit ou rétrécit, vous devez généralement recalculer la position des objets que vous dessinez.</span><span class="sxs-lookup"><span data-stu-id="12240-226">As the window grows or shrinks, you will typically need to recalculate the position of the objects that you draw.</span></span> <span data-ttu-id="12240-227">Par exemple, dans le programme Circle, le rayon et le point central doivent être mis à jour :</span><span class="sxs-lookup"><span data-stu-id="12240-227">For example, in the circle program, the radius and center point must be updated:</span></span>


```C++
void MainWindow::CalculateLayout()
{
    if (pRenderTarget != NULL)
    {
        D2D1_SIZE_F size = pRenderTarget->GetSize();
        const float x = size.width / 2;
        const float y = size.height / 2;
        const float radius = min(x, y);
        ellipse = D2D1::Ellipse(D2D1::Point2F(x, y), radius, radius);
    }
}
```



<span data-ttu-id="12240-228">La méthode [**ID2D1RenderTarget ::**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-getsize) Desize retourne la taille de la cible de rendu dans des DIP (et non des pixels), qui est l’unité appropriée pour le calcul de la disposition.</span><span class="sxs-lookup"><span data-stu-id="12240-228">The [**ID2D1RenderTarget::GetSize**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-getsize) method returns the size of the render target in DIPs (not pixels), which is the appropriate unit for calculating layout.</span></span> <span data-ttu-id="12240-229">Il existe une méthode étroitement liée, [**ID2D1RenderTarget :: GetPixelSize**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-getpixelsize), qui retourne la taille en pixels physiques.</span><span class="sxs-lookup"><span data-stu-id="12240-229">There is a closely related method, [**ID2D1RenderTarget::GetPixelSize**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-getpixelsize), that returns the size in physical pixels.</span></span> <span data-ttu-id="12240-230">Pour une cible de rendu **HWND** , cette valeur correspond à la taille retournée par [**GetClientRect**](/windows/desktop/api/winuser/nf-winuser-getclientrect).</span><span class="sxs-lookup"><span data-stu-id="12240-230">For an **HWND** render target, this value matches the size returned by [**GetClientRect**](/windows/desktop/api/winuser/nf-winuser-getclientrect).</span></span> <span data-ttu-id="12240-231">Mais souvenez-vous que le dessin est effectué en DIP, et non en pixels.</span><span class="sxs-lookup"><span data-stu-id="12240-231">But remember that drawing is performed in DIPs, not pixels.</span></span>

## <a name="next"></a><span data-ttu-id="12240-232">Suivant</span><span class="sxs-lookup"><span data-stu-id="12240-232">Next</span></span>

[<span data-ttu-id="12240-233">Utilisation de Color dans Direct2D</span><span class="sxs-lookup"><span data-stu-id="12240-233">Using Color in Direct2D</span></span>](using-color-in-direct2d.md)

 

 
