---
title: Contrôle de police
description: Pour simplifier l’intégration et la configuration de la prise en charge des polices dans les applications qui requièrent des fonctionnalités de traitement de texte et d’édition de texte, l’infrastructure de ruban Windows fournit un contrôle de police spécialisé qui expose un large éventail de propriétés de police, telles que le nom de type de caractères, le style, la taille des points et les effets.
ms.assetid: 6052f2e3-2c9e-432e-9ed6-c1e3a50843d9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e179296ae03163bf03e08d2fbf7287264792e6e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382214"
---
# <a name="font-control"></a><span data-ttu-id="3abbb-103">Contrôle de police</span><span class="sxs-lookup"><span data-stu-id="3abbb-103">Font Control</span></span>

<span data-ttu-id="3abbb-104">Pour simplifier l’intégration et la configuration de la prise en charge des polices dans les applications qui requièrent des fonctionnalités de traitement de texte et d’édition de texte, l’infrastructure de ruban Windows fournit un contrôle de police spécialisé qui expose un large éventail de propriétés de police, telles que le nom de type de caractères, le style, la taille des points et les effets.</span><span class="sxs-lookup"><span data-stu-id="3abbb-104">To simplify the integration and configuration of font support in applications that require word processing and text editing capabilities, the Windows Ribbon framework provides a specialized Font Control that exposes a wide range of font properties such as typeface name, style, point size, and effects.</span></span>

-   [<span data-ttu-id="3abbb-105">Introduction</span><span class="sxs-lookup"><span data-stu-id="3abbb-105">Introduction</span></span>](#introduction)
-   [<span data-ttu-id="3abbb-106">Une expérience cohérente</span><span class="sxs-lookup"><span data-stu-id="3abbb-106">A Consistent Experience</span></span>](#a-consistent-experience)
-   [<span data-ttu-id="3abbb-107">Intégration et configuration faciles</span><span class="sxs-lookup"><span data-stu-id="3abbb-107">Easy Integration and Configuration</span></span>](#easy-integration-and-configuration)
-   [<span data-ttu-id="3abbb-108">Alignement avec les structures de texte GDI courantes</span><span class="sxs-lookup"><span data-stu-id="3abbb-108">Alignment with Common GDI Text Structures</span></span>](#alignment-with-common-gdi-text-structures)
-   [<span data-ttu-id="3abbb-109">Ajouter un FontControl</span><span class="sxs-lookup"><span data-stu-id="3abbb-109">Add a FontControl</span></span>](#add-a-fontcontrol)
    -   [<span data-ttu-id="3abbb-110">Déclaration d’un FontControl dans le balisage</span><span class="sxs-lookup"><span data-stu-id="3abbb-110">Declaring a FontControl in Markup</span></span>](#declaring-a-fontcontrol-in-markup)
    -   [<span data-ttu-id="3abbb-111">Propriétés du contrôle de police</span><span class="sxs-lookup"><span data-stu-id="3abbb-111">Font Control Properties</span></span>](#font-control-properties)
-   [<span data-ttu-id="3abbb-112">Définir un gestionnaire de commandes FontControl</span><span class="sxs-lookup"><span data-stu-id="3abbb-112">Define a FontControl Command Handler</span></span>](#define-a-fontcontrol-command-handler)
-   [<span data-ttu-id="3abbb-113">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="3abbb-113">Related topics</span></span>](#related-topics)

## <a name="introduction"></a><span data-ttu-id="3abbb-114">Introduction</span><span class="sxs-lookup"><span data-stu-id="3abbb-114">Introduction</span></span>

<span data-ttu-id="3abbb-115">Le contrôle de police est un contrôle composite qui se compose de boutons, de boutons bascule, de zones de liste déroulante et de zones de liste déroulante, qui sont toutes utilisées pour spécifier une propriété de police ou une option de mise en forme particulière.</span><span class="sxs-lookup"><span data-stu-id="3abbb-115">The Font Control is a composite control that consists of buttons, toggle buttons, drop-down list boxes, and combo boxes, all of which are used to specify a particular font property or formatting option.</span></span>

<span data-ttu-id="3abbb-116">La capture d’écran suivante montre le contrôle de police du ruban dans WordPad pour Windows 7.</span><span class="sxs-lookup"><span data-stu-id="3abbb-116">The following screen shot shows the Ribbon Font Control in WordPad for Windows 7.</span></span>

![capture d’écran de l’élément fontcontrol avec l’attribut richfont défini sur true.](images/controls/fontcontrol.png)

## <a name="a-consistent-experience"></a><span data-ttu-id="3abbb-118">Une expérience cohérente</span><span class="sxs-lookup"><span data-stu-id="3abbb-118">A Consistent Experience</span></span>

<span data-ttu-id="3abbb-119">En tant que contrôle de ruban intégré, le contrôle de police améliore la gestion globale des polices, la fonctionnalité de sélection et de mise en forme et offre une expérience utilisateur riche et cohérente pour toutes les applications de ruban.</span><span class="sxs-lookup"><span data-stu-id="3abbb-119">As a built-in Ribbon control, the Font Control improves overall font management, selection and formatting functionality, and provides a rich, consistent user experience across all Ribbon applications.</span></span>

<span data-ttu-id="3abbb-120">Cette expérience cohérente comprend</span><span class="sxs-lookup"><span data-stu-id="3abbb-120">This consistent experience includes</span></span>

-   <span data-ttu-id="3abbb-121">Mise en forme standardisée et sélection des polices dans les applications du ruban.</span><span class="sxs-lookup"><span data-stu-id="3abbb-121">Standardized formatting and selection of fonts across Ribbon applications.</span></span>
-   <span data-ttu-id="3abbb-122">Représentation de police standardisée dans les applications de ruban.</span><span class="sxs-lookup"><span data-stu-id="3abbb-122">Standardized font representation across Ribbon applications.</span></span>
-   <span data-ttu-id="3abbb-123">Automatique, dans Windows 7, activation de la police basée sur le paramètre **Afficher** ou **Masquer** pour chaque police dans le panneau de configuration **polices** .</span><span class="sxs-lookup"><span data-stu-id="3abbb-123">Automatic, in Windows 7, font activation that is based on the **Show** or **Hide** setting for each font in the **Fonts** control panel.</span></span> <span data-ttu-id="3abbb-124">Le contrôle de police affiche uniquement les polices qui sont définies pour s' **Afficher**.</span><span class="sxs-lookup"><span data-stu-id="3abbb-124">The Font Control only displays those fonts that are set to **Show**.</span></span>
    > [!Note]  
    > <span data-ttu-id="3abbb-125">Dans Windows Vista, le panneau de configuration des **polices** n’offre pas la fonctionnalité d' **affichage** ou de **masquage** , donc toutes les polices sont activées.</span><span class="sxs-lookup"><span data-stu-id="3abbb-125">In Windows Vista, the **Fonts** control panel does not offer the **Show** or **Hide** functionality, so all fonts are activated.</span></span>

     

-   <span data-ttu-id="3abbb-126">Gestion des polices qui est disponible directement à partir du contrôle.</span><span class="sxs-lookup"><span data-stu-id="3abbb-126">Font management that is available directly from the control.</span></span>

    <span data-ttu-id="3abbb-127">La capture d’écran suivante montre que le panneau de configuration des **polices** est accessible directement à partir du contrôle font.</span><span class="sxs-lookup"><span data-stu-id="3abbb-127">The following screen shot shows that the **Fonts** control panel can be accessed directly from the Font Control.</span></span>

    ![capture d’écran de la liste des familles de polices dans WordPad pour Windows 7.](images/controls/fontcontrol-fontcpl.png)

-   <span data-ttu-id="3abbb-129">Prise en charge de l’aperçu automatique.</span><span class="sxs-lookup"><span data-stu-id="3abbb-129">Support for auto-preview.</span></span>
-   <span data-ttu-id="3abbb-130">Exposition des polices les plus pertinentes pour un utilisateur, telles que</span><span class="sxs-lookup"><span data-stu-id="3abbb-130">Exposure of fonts that are most relevant to a user, such as</span></span>
    -   <span data-ttu-id="3abbb-131">Listes de polices localisées pour les utilisateurs internationaux.</span><span class="sxs-lookup"><span data-stu-id="3abbb-131">Localized font lists for international users.</span></span>
    -   <span data-ttu-id="3abbb-132">Listes de polices basées sur le périphérique d’entrée.</span><span class="sxs-lookup"><span data-stu-id="3abbb-132">Font lists based on input device.</span></span>

    > [!Note]  
    > <span data-ttu-id="3abbb-133">La prise en charge de cette fonctionnalité n’est pas disponible sur les plateformes antérieures à Windows 7.</span><span class="sxs-lookup"><span data-stu-id="3abbb-133">Support for this functionality is not available on any platform older than Windows 7.</span></span>

     

## <a name="easy-integration-and-configuration"></a><span data-ttu-id="3abbb-134">Intégration et configuration faciles</span><span class="sxs-lookup"><span data-stu-id="3abbb-134">Easy Integration and Configuration</span></span>

<span data-ttu-id="3abbb-135">En fournissant des fonctionnalités standard, réutilisables et faciles à utiliser, le contrôle de police du ruban facilite l’intégration de la prise en charge des polices dans une application.</span><span class="sxs-lookup"><span data-stu-id="3abbb-135">By providing standard, reusable, and easily consumed functionality, the Ribbon Font Control eases the burden of integrating font support into an application.</span></span>

<span data-ttu-id="3abbb-136">Les détails de la sélection et de la mise en forme des polices sont encapsulés dans un élément logique autonome qui</span><span class="sxs-lookup"><span data-stu-id="3abbb-136">The details of font selection and formatting are wrapped in one, self-contained logical element that</span></span>

-   <span data-ttu-id="3abbb-137">Élimine la gestion complexe des interdépendances de contrôle typiques des implémentations de contrôle de police.</span><span class="sxs-lookup"><span data-stu-id="3abbb-137">Eliminates the complex management of control interdependencies typical of font control implementations.</span></span>
-   <span data-ttu-id="3abbb-138">Requiert un gestionnaire de commandes unique pour toutes les fonctionnalités exposées par les sous-contrôles de contrôle de police.</span><span class="sxs-lookup"><span data-stu-id="3abbb-138">Requires a single Command handler for all functionality exposed by the Font Control sub-controls.</span></span>

<span data-ttu-id="3abbb-139">Ce gestionnaire de commandes unique permet au contrôle de police de gérer les fonctionnalités de différents sous-contrôles en interne ; un sous-contrôle n’interagit jamais directement avec l’application, quelle que soit sa fonction.</span><span class="sxs-lookup"><span data-stu-id="3abbb-139">This single Command handler allows the Font Control to manage the functionality of various sub-controls internally; a sub-control never interacts directly with the application, regardless of its function.</span></span>

<span data-ttu-id="3abbb-140">Les autres fonctionnalités du contrôle de police incluent</span><span class="sxs-lookup"><span data-stu-id="3abbb-140">Other features of the Font Control include</span></span>

-   <span data-ttu-id="3abbb-141">La génération automatique, compatible DPI, d’une représentation de type WYSIWYG (ce que vous obtenez) de l’image bitmap pour chaque police du menu **famille de polices** .</span><span class="sxs-lookup"><span data-stu-id="3abbb-141">Automatic, DPI-aware generation of a WYSIWYG (what you see is what you get) bitmap representation for each font in the **Font family** menu.</span></span>
-   <span data-ttu-id="3abbb-142">Intégration [de Windows Graphics Device Interface (GDI)](../gdi/windows-gdi.md) .</span><span class="sxs-lookup"><span data-stu-id="3abbb-142">[Windows Graphics Device Interface (GDI)](../gdi/windows-gdi.md) integration.</span></span>
-   <span data-ttu-id="3abbb-143">Bitmaps et info-bulles de la famille de polices localisées.</span><span class="sxs-lookup"><span data-stu-id="3abbb-143">Localized font family bitmaps and tooltips.</span></span>
-   <span data-ttu-id="3abbb-144">Énumération des polices, regroupement et métadonnées pour la gestion et la présentation des polices.</span><span class="sxs-lookup"><span data-stu-id="3abbb-144">Font enumeration, grouping, and metadata for managing and presenting fonts.</span></span>
    > [!Note]  
    > <span data-ttu-id="3abbb-145">La prise en charge de cette fonctionnalité n’est pas disponible sur les plateformes antérieures à Windows 7.</span><span class="sxs-lookup"><span data-stu-id="3abbb-145">Support for this functionality is not available on any platform older than Windows 7 .</span></span>

     

-   <span data-ttu-id="3abbb-146">Sélecteurs de couleurs de la couleur de **texte** et de la couleur de **mise en surbrillance du texte** qui reflètent le comportement du sélecteur de couleurs de la [zone de liste déroulante](windowsribbon-controls-dropdowncolorpicker.md) du ruban.</span><span class="sxs-lookup"><span data-stu-id="3abbb-146">The **Text color** and **Text highlight color** drop-down color pickers that mirror the Ribbon [Drop-Down Color Picker](windowsribbon-controls-dropdowncolorpicker.md) behavior.</span></span>
-   <span data-ttu-id="3abbb-147">Prise en charge de l’aperçu automatique par tous les sous-contrôles basés sur la Galerie de contrôles de police : **famille de polices**, **taille de police**, couleur de **texte** et **couleur de surbrillance du texte**.</span><span class="sxs-lookup"><span data-stu-id="3abbb-147">Support of auto-previewing by all Font Control gallery-based sub-controls: **Font family**, **Font size**, **Text color**, and **Text highlight color**.</span></span>

## <a name="alignment-with-common-gdi-text-structures"></a><span data-ttu-id="3abbb-148">Alignement avec les structures de texte GDI courantes</span><span class="sxs-lookup"><span data-stu-id="3abbb-148">Alignment with Common GDI Text Structures</span></span>

<span data-ttu-id="3abbb-149">Les composants de pile de texte [Windows Graphics Device Interface (GDI)](../gdi/windows-gdi.md) sont utilisés pour exposer les fonctionnalités de sélection et de mise en forme des polices par le biais du contrôle de police du ruban.</span><span class="sxs-lookup"><span data-stu-id="3abbb-149">[Windows Graphics Device Interface (GDI)](../gdi/windows-gdi.md) text stack components are used to expose font selection and formatting functionality through the Ribbon Font Control.</span></span> <span data-ttu-id="3abbb-150">Les différentes fonctionnalités de police prises en charge par la structure [LOGFONT](/windows/win32/api/wingdi/ns-wingdi-logfonta), la [structure CHOOSEFONT](/windows/win32/api/commdlg/ns-commdlg-choosefonta)et la [structure CHARFORMAT2](/windows/win32/api/richedit/ns-richedit-charformat2a) sont exposées par le biais des sous-contrôles inclus dans le contrôle font.</span><span class="sxs-lookup"><span data-stu-id="3abbb-150">The various font features supported by the [LOGFONT Structure](/windows/win32/api/wingdi/ns-wingdi-logfonta), [CHOOSEFONT Structure](/windows/win32/api/commdlg/ns-commdlg-choosefonta), and [CHARFORMAT2 Structure](/windows/win32/api/richedit/ns-richedit-charformat2a) are exposed through the sub-controls that are included in the Font Control.</span></span>

<span data-ttu-id="3abbb-151">Les sous-contrôles affichés dans le contrôle font dépendent du modèle *FontType* déclaré dans le balisage du ruban.</span><span class="sxs-lookup"><span data-stu-id="3abbb-151">The sub-controls that are displayed in the Font Control depend on the *FontType* template declared in the Ribbon markup.</span></span> <span data-ttu-id="3abbb-152">Les modèles *FontType* (décrits plus en détail dans la section suivante) sont conçus pour s’aligner sur les structures de texte [Windows Graphics Device Interface (GDI)](../gdi/windows-gdi.md) courantes.</span><span class="sxs-lookup"><span data-stu-id="3abbb-152">The *FontType* templates (discussed in further detail in the following section) are designed to align with the common [Windows Graphics Device Interface (GDI)](../gdi/windows-gdi.md) text structures.</span></span>

## <a name="add-a-fontcontrol"></a><span data-ttu-id="3abbb-153">Ajouter un FontControl</span><span class="sxs-lookup"><span data-stu-id="3abbb-153">Add a FontControl</span></span>

<span data-ttu-id="3abbb-154">Cette section décrit les étapes de base pour ajouter un contrôle de police à une application de ruban.</span><span class="sxs-lookup"><span data-stu-id="3abbb-154">This section outlines the basic steps for adding a Font Control to a Ribbon application.</span></span>

### <a name="declaring-a-fontcontrol-in-markup"></a><span data-ttu-id="3abbb-155">Déclaration d’un FontControl dans le balisage</span><span class="sxs-lookup"><span data-stu-id="3abbb-155">Declaring a FontControl in Markup</span></span>

<span data-ttu-id="3abbb-156">Comme les autres contrôles de ruban, le contrôle de police est déclaré dans le balisage avec un élément [**FontControl**](windowsribbon-element-fontcontrol.md) et associé à une déclaration de commande via un ID de commande.</span><span class="sxs-lookup"><span data-stu-id="3abbb-156">Like other Ribbon controls, the Font Control is declared in markup with a [**FontControl**](windowsribbon-element-fontcontrol.md) element and associated with a Command declaration through a Command ID.</span></span> <span data-ttu-id="3abbb-157">Lorsque l’application est compilée, l’ID de commande est utilisé pour lier la commande à un gestionnaire de commandes dans l’application hôte.</span><span class="sxs-lookup"><span data-stu-id="3abbb-157">When the application is compiled, the Command ID is used to bind the Command to a Command handler in the host application.</span></span>

> [!Note]  
> <span data-ttu-id="3abbb-158">Si aucun ID de commande n’est déclaré avec [**FontControl**](windowsribbon-element-fontcontrol.md) dans le balisage, alors l’un est généré par l’infrastructure.</span><span class="sxs-lookup"><span data-stu-id="3abbb-158">If no Command ID is declared with the [**FontControl**](windowsribbon-element-fontcontrol.md) in markup, then one is generated by the framework.</span></span>

 

<span data-ttu-id="3abbb-159">Étant donné que les sous-contrôles du contrôle font ne sont pas exposés directement, la personnalisation du contrôle font est limitée à trois modèles de disposition *FontType* définis par l’infrastructure.</span><span class="sxs-lookup"><span data-stu-id="3abbb-159">Because the sub-controls of the Font Control are not exposed directly, customization of the Font Control is limited to three *FontType* layout templates defined by the framework.</span></span>

<span data-ttu-id="3abbb-160">Une personnalisation plus poussée du contrôle de police peut être effectuée en combinant le modèle de disposition avec des attributs [**FontControl**](windowsribbon-element-fontcontrol.md) tels que *IsHighlightButtonVisible*, *IsStrikethroughButtonVisible* et *IsUnderlineButtonVisible*.</span><span class="sxs-lookup"><span data-stu-id="3abbb-160">Further customization of the Font Control can be accomplished by combining the layout template with [**FontControl**](windowsribbon-element-fontcontrol.md) attributes such as *IsHighlightButtonVisible*, *IsStrikethroughButtonVisible*, and *IsUnderlineButtonVisible*.</span></span>

> [!Note]  
> <span data-ttu-id="3abbb-161">Les fonctionnalités de police au-delà de celles exposées par les attributs et les modèles de contrôle de police standard nécessitent une implémentation de contrôle de police personnalisée qui n’est pas traitée dans cet article.</span><span class="sxs-lookup"><span data-stu-id="3abbb-161">Font functionality beyond that exposed by the standard Font Control templates and attributes requires a custom font control implementation that is outside the scope of this article.</span></span>

 

<span data-ttu-id="3abbb-162">Le tableau suivant répertorie les modèles de contrôle de police et le type de contrôle d’édition avec lesquels chaque modèle est aligné.</span><span class="sxs-lookup"><span data-stu-id="3abbb-162">The following table lists the Font Control templates and the edit control type that each template is aligned with.</span></span>



| <span data-ttu-id="3abbb-163">Modèle</span><span class="sxs-lookup"><span data-stu-id="3abbb-163">Template</span></span>      | <span data-ttu-id="3abbb-164">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="3abbb-164">Supports</span></span>                                                                 |
|---------------|--------------------------------------------------------------------------|
| <span data-ttu-id="3abbb-165">FontOnly</span><span class="sxs-lookup"><span data-stu-id="3abbb-165">FontOnly</span></span>      | [<span data-ttu-id="3abbb-166">LOGFONT, structure</span><span class="sxs-lookup"><span data-stu-id="3abbb-166">LOGFONT Structure</span></span>](/windows/win32/api/wingdi/ns-wingdi-logfonta)     |
| <span data-ttu-id="3abbb-167">FontWithColor</span><span class="sxs-lookup"><span data-stu-id="3abbb-167">FontWithColor</span></span> | [<span data-ttu-id="3abbb-168">CHOOSEFONT, structure</span><span class="sxs-lookup"><span data-stu-id="3abbb-168">CHOOSEFONT Structure</span></span>](/windows/win32/api/commdlg/ns-commdlg-choosefonta)  |
| <span data-ttu-id="3abbb-169">RichFont</span><span class="sxs-lookup"><span data-stu-id="3abbb-169">RichFont</span></span>      | [<span data-ttu-id="3abbb-170">CHARFORMAT2, structure</span><span class="sxs-lookup"><span data-stu-id="3abbb-170">CHARFORMAT2 Structure</span></span>](/windows/win32/api/richedit/ns-richedit-charformat2a) |



 

<span data-ttu-id="3abbb-171">Le tableau suivant répertorie les contrôles qui sont associés à chaque modèle et identifie les contrôles qui sont facultatifs pour un modèle associé.</span><span class="sxs-lookup"><span data-stu-id="3abbb-171">The following table lists the controls that are associated with each template and identifies the controls that are optional for an associated template.</span></span>



<span data-ttu-id="3abbb-172">Commandes</span><span class="sxs-lookup"><span data-stu-id="3abbb-172">Controls</span></span>

<span data-ttu-id="3abbb-173">Modèles</span><span class="sxs-lookup"><span data-stu-id="3abbb-173">Templates</span></span>

<span data-ttu-id="3abbb-174">**RichFont**</span><span class="sxs-lookup"><span data-stu-id="3abbb-174">**RichFont**</span></span>

<span data-ttu-id="3abbb-175">**FontWithColor**</span><span class="sxs-lookup"><span data-stu-id="3abbb-175">**FontWithColor**</span></span>

<span data-ttu-id="3abbb-176">**FontOnly**</span><span class="sxs-lookup"><span data-stu-id="3abbb-176">**FontOnly**</span></span>

<span data-ttu-id="3abbb-177">Default</span><span class="sxs-lookup"><span data-stu-id="3abbb-177">Default</span></span>

<span data-ttu-id="3abbb-178">Facultatif</span><span class="sxs-lookup"><span data-stu-id="3abbb-178">Optional</span></span>

<span data-ttu-id="3abbb-179">Default</span><span class="sxs-lookup"><span data-stu-id="3abbb-179">Default</span></span>

<span data-ttu-id="3abbb-180">Facultatif</span><span class="sxs-lookup"><span data-stu-id="3abbb-180">Optional</span></span>

<span data-ttu-id="3abbb-181">Default</span><span class="sxs-lookup"><span data-stu-id="3abbb-181">Default</span></span>

<span data-ttu-id="3abbb-182">Facultatif</span><span class="sxs-lookup"><span data-stu-id="3abbb-182">Optional</span></span>

<span data-ttu-id="3abbb-183">Zone de liste déroulante **taille de police**</span><span class="sxs-lookup"><span data-stu-id="3abbb-183">**Font size** combo box</span></span>

<span data-ttu-id="3abbb-184">Oui</span><span class="sxs-lookup"><span data-stu-id="3abbb-184">Yes</span></span>

<span data-ttu-id="3abbb-185">Non</span><span class="sxs-lookup"><span data-stu-id="3abbb-185">No</span></span>

<span data-ttu-id="3abbb-186">Oui</span><span class="sxs-lookup"><span data-stu-id="3abbb-186">Yes</span></span>

<span data-ttu-id="3abbb-187">Non</span><span class="sxs-lookup"><span data-stu-id="3abbb-187">No</span></span>

<span data-ttu-id="3abbb-188">Oui</span><span class="sxs-lookup"><span data-stu-id="3abbb-188">Yes</span></span>

<span data-ttu-id="3abbb-189">Non</span><span class="sxs-lookup"><span data-stu-id="3abbb-189">No</span></span>

<span data-ttu-id="3abbb-190">Zone de liste déroulante **famille de polices**</span><span class="sxs-lookup"><span data-stu-id="3abbb-190">**Font family** combo box</span></span>

<span data-ttu-id="3abbb-191">Oui</span><span class="sxs-lookup"><span data-stu-id="3abbb-191">Yes</span></span>

<span data-ttu-id="3abbb-192">Non</span><span class="sxs-lookup"><span data-stu-id="3abbb-192">No</span></span>

<span data-ttu-id="3abbb-193">Oui</span><span class="sxs-lookup"><span data-stu-id="3abbb-193">Yes</span></span>

<span data-ttu-id="3abbb-194">Non</span><span class="sxs-lookup"><span data-stu-id="3abbb-194">No</span></span>

<span data-ttu-id="3abbb-195">Oui</span><span class="sxs-lookup"><span data-stu-id="3abbb-195">Yes</span></span>

<span data-ttu-id="3abbb-196">Non</span><span class="sxs-lookup"><span data-stu-id="3abbb-196">No</span></span>

<span data-ttu-id="3abbb-197">Bouton **agrandir la police**</span><span class="sxs-lookup"><span data-stu-id="3abbb-197">**Grow font** button</span></span>

<span data-ttu-id="3abbb-198">Oui</span><span class="sxs-lookup"><span data-stu-id="3abbb-198">Yes</span></span>

<span data-ttu-id="3abbb-199">Oui</span><span class="sxs-lookup"><span data-stu-id="3abbb-199">Yes</span></span>

<span data-ttu-id="3abbb-200">Oui</span><span class="sxs-lookup"><span data-stu-id="3abbb-200">Yes</span></span>

<span data-ttu-id="3abbb-201">Oui</span><span class="sxs-lookup"><span data-stu-id="3abbb-201">Yes</span></span>

\-

\-

<span data-ttu-id="3abbb-202">Bouton **réduire la police**</span><span class="sxs-lookup"><span data-stu-id="3abbb-202">**Shrink font** button</span></span>

<span data-ttu-id="3abbb-203">Oui</span><span class="sxs-lookup"><span data-stu-id="3abbb-203">Yes</span></span>

<span data-ttu-id="3abbb-204">Oui</span><span class="sxs-lookup"><span data-stu-id="3abbb-204">Yes</span></span>

<span data-ttu-id="3abbb-205">Oui</span><span class="sxs-lookup"><span data-stu-id="3abbb-205">Yes</span></span>

<span data-ttu-id="3abbb-206">Oui</span><span class="sxs-lookup"><span data-stu-id="3abbb-206">Yes</span></span>

\-

\-

<span data-ttu-id="3abbb-207">Bouton **gras**</span><span class="sxs-lookup"><span data-stu-id="3abbb-207">**Bold** button</span></span>

<span data-ttu-id="3abbb-208">Oui</span><span class="sxs-lookup"><span data-stu-id="3abbb-208">Yes</span></span>

<span data-ttu-id="3abbb-209">Non</span><span class="sxs-lookup"><span data-stu-id="3abbb-209">No</span></span>

<span data-ttu-id="3abbb-210">Oui</span><span class="sxs-lookup"><span data-stu-id="3abbb-210">Yes</span></span>

<span data-ttu-id="3abbb-211">Non</span><span class="sxs-lookup"><span data-stu-id="3abbb-211">No</span></span>

<span data-ttu-id="3abbb-212">Oui</span><span class="sxs-lookup"><span data-stu-id="3abbb-212">Yes</span></span>

<span data-ttu-id="3abbb-213">Non</span><span class="sxs-lookup"><span data-stu-id="3abbb-213">No</span></span>

<span data-ttu-id="3abbb-214">Bouton **italique**</span><span class="sxs-lookup"><span data-stu-id="3abbb-214">**Italic** button</span></span>

<span data-ttu-id="3abbb-215">Oui</span><span class="sxs-lookup"><span data-stu-id="3abbb-215">Yes</span></span>

<span data-ttu-id="3abbb-216">Non</span><span class="sxs-lookup"><span data-stu-id="3abbb-216">No</span></span>

<span data-ttu-id="3abbb-217">Oui</span><span class="sxs-lookup"><span data-stu-id="3abbb-217">Yes</span></span>

<span data-ttu-id="3abbb-218">Non</span><span class="sxs-lookup"><span data-stu-id="3abbb-218">No</span></span>

<span data-ttu-id="3abbb-219">Oui</span><span class="sxs-lookup"><span data-stu-id="3abbb-219">Yes</span></span>

<span data-ttu-id="3abbb-220">Non</span><span class="sxs-lookup"><span data-stu-id="3abbb-220">No</span></span>

<span data-ttu-id="3abbb-221">Bouton **souligné**</span><span class="sxs-lookup"><span data-stu-id="3abbb-221">**Underline** button</span></span>

<span data-ttu-id="3abbb-222">Oui</span><span class="sxs-lookup"><span data-stu-id="3abbb-222">Yes</span></span>

<span data-ttu-id="3abbb-223">Non</span><span class="sxs-lookup"><span data-stu-id="3abbb-223">No</span></span>

<span data-ttu-id="3abbb-224">Oui</span><span class="sxs-lookup"><span data-stu-id="3abbb-224">Yes</span></span>

<span data-ttu-id="3abbb-225">Oui</span><span class="sxs-lookup"><span data-stu-id="3abbb-225">Yes</span></span>

<span data-ttu-id="3abbb-226">Oui</span><span class="sxs-lookup"><span data-stu-id="3abbb-226">Yes</span></span>

<span data-ttu-id="3abbb-227">Oui</span><span class="sxs-lookup"><span data-stu-id="3abbb-227">Yes</span></span>

<span data-ttu-id="3abbb-228">Bouton **barré**</span><span class="sxs-lookup"><span data-stu-id="3abbb-228">**Strikethrough** button</span></span>

<span data-ttu-id="3abbb-229">Oui</span><span class="sxs-lookup"><span data-stu-id="3abbb-229">Yes</span></span>

<span data-ttu-id="3abbb-230">Non</span><span class="sxs-lookup"><span data-stu-id="3abbb-230">No</span></span>

<span data-ttu-id="3abbb-231">Oui</span><span class="sxs-lookup"><span data-stu-id="3abbb-231">Yes</span></span>

<span data-ttu-id="3abbb-232">Oui</span><span class="sxs-lookup"><span data-stu-id="3abbb-232">Yes</span></span>

<span data-ttu-id="3abbb-233">Oui</span><span class="sxs-lookup"><span data-stu-id="3abbb-233">Yes</span></span>

<span data-ttu-id="3abbb-234">Oui</span><span class="sxs-lookup"><span data-stu-id="3abbb-234">Yes</span></span>

<span data-ttu-id="3abbb-235">Bouton d' **indice**</span><span class="sxs-lookup"><span data-stu-id="3abbb-235">**Subscript** button</span></span>

<span data-ttu-id="3abbb-236">Oui</span><span class="sxs-lookup"><span data-stu-id="3abbb-236">Yes</span></span>

<span data-ttu-id="3abbb-237">Non</span><span class="sxs-lookup"><span data-stu-id="3abbb-237">No</span></span>

\-

\-

\-

\-

<span data-ttu-id="3abbb-238">Bouton **exposant**</span><span class="sxs-lookup"><span data-stu-id="3abbb-238">**Superscript** button</span></span>

<span data-ttu-id="3abbb-239">Oui</span><span class="sxs-lookup"><span data-stu-id="3abbb-239">Yes</span></span>

<span data-ttu-id="3abbb-240">Non</span><span class="sxs-lookup"><span data-stu-id="3abbb-240">No</span></span>

\-

\-

\-

\-

<span data-ttu-id="3abbb-241">Bouton **couleur de surbrillance du texte**</span><span class="sxs-lookup"><span data-stu-id="3abbb-241">**Text highlight color** button</span></span>

<span data-ttu-id="3abbb-242">Oui</span><span class="sxs-lookup"><span data-stu-id="3abbb-242">Yes</span></span>

<span data-ttu-id="3abbb-243">Non</span><span class="sxs-lookup"><span data-stu-id="3abbb-243">No</span></span>

<span data-ttu-id="3abbb-244">Oui</span><span class="sxs-lookup"><span data-stu-id="3abbb-244">Yes</span></span>

<span data-ttu-id="3abbb-245">Oui</span><span class="sxs-lookup"><span data-stu-id="3abbb-245">Yes</span></span>

\-

\-

<span data-ttu-id="3abbb-246">Bouton **couleur du texte**</span><span class="sxs-lookup"><span data-stu-id="3abbb-246">**Text color** button</span></span>

<span data-ttu-id="3abbb-247">Oui</span><span class="sxs-lookup"><span data-stu-id="3abbb-247">Yes</span></span>

<span data-ttu-id="3abbb-248">Non</span><span class="sxs-lookup"><span data-stu-id="3abbb-248">No</span></span>

<span data-ttu-id="3abbb-249">Oui</span><span class="sxs-lookup"><span data-stu-id="3abbb-249">Yes</span></span>

<span data-ttu-id="3abbb-250">Non</span><span class="sxs-lookup"><span data-stu-id="3abbb-250">No</span></span>

\-

\-



 

<span data-ttu-id="3abbb-251">Lorsque le comportement de disposition d’un contrôle de police est déclaré, l’infrastructure du ruban fournit un modèle de disposition *SizeDefinition* facultatif, `OneFontControl` , qui définit deux configurations de sous-contrôle en fonction de la taille du ruban et de l’espace disponible pour le contrôle de police.</span><span class="sxs-lookup"><span data-stu-id="3abbb-251">When the layout behavior of a Font Control is declared, the Ribbon framework provides an optional *SizeDefinition* layout template, `OneFontControl`, that defines two sub-control configurations based on the size of the Ribbon and the space available for the Font Control.</span></span> <span data-ttu-id="3abbb-252">Pour plus d’informations, consultez [Personnalisation d’un ruban à l’aide de définitions de taille et de stratégies de mise à l’échelle](windowsribbon-templates.md).</span><span class="sxs-lookup"><span data-stu-id="3abbb-252">For more information, see [Customizing a Ribbon Through Size Definitions and Scaling Policies](windowsribbon-templates.md).</span></span>

### <a name="adding-a-fontcontrol-to-a-ribbon"></a><span data-ttu-id="3abbb-253">Ajout d’un FontControl à un ruban</span><span class="sxs-lookup"><span data-stu-id="3abbb-253">Adding a FontControl to a Ribbon</span></span>

<span data-ttu-id="3abbb-254">Les exemples de code suivants illustrent les exigences de balisage de base pour l’ajout d’un contrôle font à un ruban :</span><span class="sxs-lookup"><span data-stu-id="3abbb-254">The following code examples demonstrate the basic markup requirements for adding a Font Control to a Ribbon:</span></span>

<span data-ttu-id="3abbb-255">Cette section de code montre le balisage de déclaration de commande [**FontControl**](windowsribbon-element-fontcontrol.md) , y compris les commandes de [**tabulation**](windowsribbon-element-tab.md) et de [**groupe**](windowsribbon-element-group.md) requises pour afficher un contrôle dans le [**ruban**](windowsribbon-element-ribbon.md).</span><span class="sxs-lookup"><span data-stu-id="3abbb-255">This section of code shows the [**FontControl**](windowsribbon-element-fontcontrol.md) Command declaration markup, including the [**Tab**](windowsribbon-element-tab.md) and [**Group**](windowsribbon-element-group.md) Commands that are required for displaying a control in the [**Ribbon**](windowsribbon-element-ribbon.md).</span></span>


```C++
<Command Name="cmdTab1"
  Comment="These comments are optional and are inserted into the header file."
  Symbol="cmdTab1" Id="10000" >
  <Command.LabelTitle>Tab 1</Command.LabelTitle>
</Command>
<Command Name="cmdGroup1" Comment="Group #1" Symbol="cmdGroup1" Id="20000">
  <!-- This image is used when the group scales to a pop-up. -->
  <Command.SmallImages>
    <Image>res/Button_Image.bmp</Image>
  </Command.SmallImages>
</Command>
<Command Name="cmdFontControl" Symbol="cmdFontControl" Comment="FontControl" Id="25001" Keytip="F" />
```



<span data-ttu-id="3abbb-256">Cette section de code montre le balisage requis pour déclarer et associer un [**FontControl**](windowsribbon-element-fontcontrol.md) à une [**commande**](windowsribbon-element-command.md) via un ID de commande.</span><span class="sxs-lookup"><span data-stu-id="3abbb-256">This section of code shows the markup required to declare and associate a [**FontControl**](windowsribbon-element-fontcontrol.md) with a [**Command**](windowsribbon-element-command.md) through a Command ID.</span></span> <span data-ttu-id="3abbb-257">Cet exemple particulier comprend les déclarations de [**tabulation**](windowsribbon-element-tab.md) et de [**groupe**](windowsribbon-element-group.md) , avec des préférences de mise à l’échelle.</span><span class="sxs-lookup"><span data-stu-id="3abbb-257">This particular example includes the [**Tab**](windowsribbon-element-tab.md) and [**Group**](windowsribbon-element-group.md) declarations, with scaling preferences.</span></span>


```C++
<Ribbon.Tabs>
  <Tab CommandName="cmdTab1">
    <Tab.ScalingPolicy>
      <ScalingPolicy>
        <ScalingPolicy.IdealSizes>
          <Scale Group="cmdGroup1" Size="Large" />
        </ScalingPolicy.IdealSizes>
        <!-- Describe how the FontControl group scales. -->
        <Scale Group="cmdGroup1" Size="Medium" />
        <Scale Group="cmdGroup1" Size="Popup" />
      </ScalingPolicy>
    <Group CommandName="cmdGroup1" SizeDefinition="OneFontControl">
      <FontControl CommandName="cmdFontControl" FontType="RichFont" />
    </Group>
  </Tab>
</Ribbon.Tabs>
```



### <a name="adding-a-fontcontrol-to-a-contextpopup"></a><span data-ttu-id="3abbb-258">Ajout d’un FontControl à un ContextPopup</span><span class="sxs-lookup"><span data-stu-id="3abbb-258">Adding a FontControl to a ContextPopup</span></span>

<span data-ttu-id="3abbb-259">L’ajout d’un contrôle de police à un menu contextuel de [contexte](windowsribbon-controls-contextpopup.md) requiert une procédure similaire à celle qui consiste à ajouter un contrôle de police au ruban.</span><span class="sxs-lookup"><span data-stu-id="3abbb-259">Adding a Font Control to a [Context Popup](windowsribbon-controls-contextpopup.md) requires a procedure similar to that of adding a Font Control to the Ribbon.</span></span> <span data-ttu-id="3abbb-260">Toutefois, un contrôle de police dans un [**MiniToolbar**](windowsribbon-element-minitoolbar.md) est limité à l’ensemble de sous-contrôles par défaut qui sont communs à tous les modèles de contrôle de police : **famille de polices**, taille de **police**, **gras** et **italique**.</span><span class="sxs-lookup"><span data-stu-id="3abbb-260">However, a Font Control in a [**MiniToolbar**](windowsribbon-element-minitoolbar.md) is restricted to the set of default sub-controls that are common to all Font Control templates: **Font family**, **Font size**, **Bold**, and **Italic**.</span></span>

<span data-ttu-id="3abbb-261">Les exemples de code suivants illustrent les exigences de balisage de base pour l’ajout d’un contrôle de police à une [fenêtre contextuelle](windowsribbon-controls-contextpopup.md):</span><span class="sxs-lookup"><span data-stu-id="3abbb-261">The following code examples demonstrate the basic markup requirements for adding a Font Control to a [Context Popup](windowsribbon-controls-contextpopup.md):</span></span>

<span data-ttu-id="3abbb-262">Cette section de code montre le balisage de déclaration de commande [**FontControl**](windowsribbon-element-fontcontrol.md) nécessaire pour afficher un **FontControl** dans le [**ContextPopup**](windowsribbon-element-contextpopup.md).</span><span class="sxs-lookup"><span data-stu-id="3abbb-262">This section of code shows the [**FontControl**](windowsribbon-element-fontcontrol.md) Command declaration markup that is required for displaying a **FontControl** in the [**ContextPopup**](windowsribbon-element-contextpopup.md).</span></span>


```C++
<Command Name="cmdFontControl" Symbol="cmdFontControl" Comment="FontControl" Id="25001" />
```



<span data-ttu-id="3abbb-263">Cette section de code montre le balisage requis pour déclarer et associer un [**FontControl**](windowsribbon-element-fontcontrol.md) à une commande via un ID de commande.</span><span class="sxs-lookup"><span data-stu-id="3abbb-263">This section of code shows the markup required to declare and associate a [**FontControl**](windowsribbon-element-fontcontrol.md) with a Command through a Command ID.</span></span>


```C++
<ContextPopup.MiniToolbars>
  <MiniToolBar Name="MiniToolbar1">
    <MenuCategory Class="StandardItems">
      <FontControl CommandName="cmdFontControl" />
    </MenuCategory>
  </MiniToolBar>
</ContextPopup.MiniToolbars>
```



### <a name="keytips"></a><span data-ttu-id="3abbb-264">Touches d’accès</span><span class="sxs-lookup"><span data-stu-id="3abbb-264">Keytips</span></span>

<span data-ttu-id="3abbb-265">Chaque sous-contrôle du contrôle de police du ruban est accessible par le biais d’un raccourci clavier ou d’une touche d’accès.</span><span class="sxs-lookup"><span data-stu-id="3abbb-265">Each sub-control in the Ribbon Font Control is accessible through a keyboard shortcut, or keytip.</span></span> <span data-ttu-id="3abbb-266">Ce KeyTip est prédéfini et affecté à chaque sous-contrôle par l’infrastructure.</span><span class="sxs-lookup"><span data-stu-id="3abbb-266">This keytip is predefined and assigned to each sub-control by the framework.</span></span>

<span data-ttu-id="3abbb-267">Si une valeur d’attribut *KeyTip* est assignée à l’élément [**FontControl**](windowsribbon-element-fontcontrol.md) dans le balisage, cette valeur est ajoutée en tant que préfixe à la touche d’appel définie par l’infrastructure.</span><span class="sxs-lookup"><span data-stu-id="3abbb-267">If a *Keytip* attribute value is assigned to the [**FontControl**](windowsribbon-element-fontcontrol.md) element in markup, this value is added as a prefix to the framework-defined keytip.</span></span>

> [!Note]  
> <span data-ttu-id="3abbb-268">L’application doit appliquer une règle à un seul caractère pour ce préfixe.</span><span class="sxs-lookup"><span data-stu-id="3abbb-268">The application should enforce a single-character rule for this prefix.</span></span>

 

<span data-ttu-id="3abbb-269">Le tableau suivant répertorie les touches accélératrices définies par l’infrastructure.</span><span class="sxs-lookup"><span data-stu-id="3abbb-269">The following table lists the keytips defined by the framework.</span></span> 

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3abbb-270">Sous-contrôle</span><span class="sxs-lookup"><span data-stu-id="3abbb-270">Sub-control</span></span></th>
<th><span data-ttu-id="3abbb-271">KeyTip</span><span class="sxs-lookup"><span data-stu-id="3abbb-271">Keytip</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3abbb-272">Famille de polices</span><span class="sxs-lookup"><span data-stu-id="3abbb-272">Font family</span></span></td>
<td><span data-ttu-id="3abbb-273">F</span><span class="sxs-lookup"><span data-stu-id="3abbb-273">F</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3abbb-274">Style de police</span><span class="sxs-lookup"><span data-stu-id="3abbb-274">Font style</span></span></td>
<td><span data-ttu-id="3abbb-275">T</span><span class="sxs-lookup"><span data-stu-id="3abbb-275">T</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3abbb-276">Taille de police</span><span class="sxs-lookup"><span data-stu-id="3abbb-276">Font size</span></span></td>
<td><span data-ttu-id="3abbb-277">S</span><span class="sxs-lookup"><span data-stu-id="3abbb-277">S</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3abbb-278">Agrandir la police</span><span class="sxs-lookup"><span data-stu-id="3abbb-278">Grow font</span></span></td>
<td><span data-ttu-id="3abbb-279">G</span><span class="sxs-lookup"><span data-stu-id="3abbb-279">G</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3abbb-280">Réduire la police</span><span class="sxs-lookup"><span data-stu-id="3abbb-280">Shrink font</span></span></td>
<td><span data-ttu-id="3abbb-281">K</span><span class="sxs-lookup"><span data-stu-id="3abbb-281">K</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3abbb-282">Gras</span><span class="sxs-lookup"><span data-stu-id="3abbb-282">Bold</span></span></td>
<td><span data-ttu-id="3abbb-283">B</span><span class="sxs-lookup"><span data-stu-id="3abbb-283">B</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3abbb-284">Italique</span><span class="sxs-lookup"><span data-stu-id="3abbb-284">Italic</span></span></td>
<td><span data-ttu-id="3abbb-285">I</span><span class="sxs-lookup"><span data-stu-id="3abbb-285">I</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3abbb-286">Souligner</span><span class="sxs-lookup"><span data-stu-id="3abbb-286">Underline</span></span></td>
<td><span data-ttu-id="3abbb-287">U</span><span class="sxs-lookup"><span data-stu-id="3abbb-287">U</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3abbb-288">Barré</span><span class="sxs-lookup"><span data-stu-id="3abbb-288">Strikethrough</span></span></td>
<td><span data-ttu-id="3abbb-289">X</span><span class="sxs-lookup"><span data-stu-id="3abbb-289">X</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3abbb-290">Exposant</span><span class="sxs-lookup"><span data-stu-id="3abbb-290">Superscript</span></span></td>
<td><span data-ttu-id="3abbb-291">Y ou Z</span><span class="sxs-lookup"><span data-stu-id="3abbb-291">Y or Z</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="3abbb-292">Si l’attribut <em>KeyTip</em> n’est pas déclaré dans le balisage, la touche d’option par défaut est Y ; dans le cas contraire, la touche d’option par défaut est <em>KeyTip</em> + Z.</span><span class="sxs-lookup"><span data-stu-id="3abbb-292">If the <em>Keytip</em> attribute is not declared in markup, the default keytip is Y; otherwise, the default keytip is <em>Keytip</em> + Z.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3abbb-293">Indice</span><span class="sxs-lookup"><span data-stu-id="3abbb-293">Subscript</span></span></td>
<td><span data-ttu-id="3abbb-294">Un</span><span class="sxs-lookup"><span data-stu-id="3abbb-294">A</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3abbb-295">Couleur de police</span><span class="sxs-lookup"><span data-stu-id="3abbb-295">Font color</span></span></td>
<td><span data-ttu-id="3abbb-296">C</span><span class="sxs-lookup"><span data-stu-id="3abbb-296">C</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3abbb-297">Mise en surbrillance de police</span><span class="sxs-lookup"><span data-stu-id="3abbb-297">Font highlight</span></span></td>
<td><span data-ttu-id="3abbb-298">H</span><span class="sxs-lookup"><span data-stu-id="3abbb-298">H</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="3abbb-299">Le préfixe recommandé pour un ruban en-US de l’interface utilisateur multilingue (MUI) est « F », comme le montre l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="3abbb-299">The recommended prefix for a Multilingual User Interface (MUI) EN-US Ribbon is 'F', as shown in the following example.</span></span>


```C++
<Command Name="cmdFontControl" Symbol="cmdFontControl" Comment="FontControl" Id="25001" Keytip="F" />
```



<span data-ttu-id="3abbb-300">La capture d’écran suivante illustre les info-bulles de contrôle de police telles qu’elles sont définies dans l’exemple précédent.</span><span class="sxs-lookup"><span data-stu-id="3abbb-300">The following screen shot illustrates the Font Control keytips as they are defined in the previous example.</span></span>

![capture d’écran des info-bulles fontcontrol dans WordPad pour Windows 7.](images/controls/fontcontrol-keytips.png)

### <a name="the-ribbon-resource-file"></a><span data-ttu-id="3abbb-302">Fichier de ressources du ruban</span><span class="sxs-lookup"><span data-stu-id="3abbb-302">The Ribbon Resource File</span></span>

<span data-ttu-id="3abbb-303">Lorsque le fichier de balisage est compilé, un fichier de ressources qui contient toutes les références de ressources pour l’application ruban est généré.</span><span class="sxs-lookup"><span data-stu-id="3abbb-303">When the markup file is compiled, a resource file that contains all resource references for the Ribbon application is generated.</span></span>

<span data-ttu-id="3abbb-304">Exemple de fichier de ressources simple :</span><span class="sxs-lookup"><span data-stu-id="3abbb-304">Example of a simple resource file:</span></span>


```C++
// ******************************************************************************
// * This is an automatically generated file containing the ribbon resource for *
// * your application.                                                          *
// ******************************************************************************

#include ".\ids.h"

STRINGTABLE 
BEGIN
  cmdTab1_LabelTitle_RESID L"Tab 1" 
    /* LabelTitle cmdTab1_LabelTitle_RESID: These comments are optional and are 
       inserted into the header file. */
END

cmdGroup1_SmallImages_RESID    BITMAP    "res\\Button_Image.bmp" 
  /* SmallImages cmdGroup1_SmallImages_RESID: Group #1 */
STRINGTABLE 
BEGIN
  cmdFontControl_Keytip_RESID L"F" /* Keytip cmdFontControl_Keytip_RESID: FontControl */
END

FCSAMPLE_RIBBON    UIFILE    "Debug\\FCSample.bml"

```



### <a name="font-control-properties"></a><span data-ttu-id="3abbb-305">Propriétés du contrôle de police</span><span class="sxs-lookup"><span data-stu-id="3abbb-305">Font Control Properties</span></span>

<span data-ttu-id="3abbb-306">L’infrastructure du ruban définit une collection de [clés de propriété](windowsribbon-reference-properties.md) pour le contrôle de police et ses sous-contrôles constitutifs.</span><span class="sxs-lookup"><span data-stu-id="3abbb-306">The Ribbon framework defines a collection of [property keys](windowsribbon-reference-properties.md) for the Font Control and its constituent sub-controls.</span></span>

<span data-ttu-id="3abbb-307">En général, une propriété de contrôle de police est mise à jour dans l’interface utilisateur du ruban en invalidant la commande associée au contrôle via un appel à la méthode [**IUIFramework :: InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) .</span><span class="sxs-lookup"><span data-stu-id="3abbb-307">Typically, a Font Control property is updated in the ribbon UI by invalidating the Command associated with the control through a call to the [**IUIFramework::InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) method.</span></span> <span data-ttu-id="3abbb-308">L’événement d’invalidation est géré, et les mises à jour de la propriété sont définies par la méthode de rappel [**IUICommandHandler :: UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) .</span><span class="sxs-lookup"><span data-stu-id="3abbb-308">The invalidation event is handled, and the property updates defined, by the [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method.</span></span>

<span data-ttu-id="3abbb-309">La méthode de rappel [**IUICommandHandler :: UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) n’est pas exécutée et l’application a interrogé une valeur de propriété mise à jour, jusqu’à ce que la propriété soit requise par le Framework.</span><span class="sxs-lookup"><span data-stu-id="3abbb-309">The [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method is not executed, and the application queried for an updated property value, until the property is required by the framework.</span></span> <span data-ttu-id="3abbb-310">Par exemple, lorsqu’un onglet est activé et qu’un contrôle est affiché dans l’interface ruban, ou lorsqu’une info-bulle est affichée.</span><span class="sxs-lookup"><span data-stu-id="3abbb-310">For example, when a tab is activated and a control revealed in the ribbon UI, or when a tooltip is displayed.</span></span>

> [!Note]  
> <span data-ttu-id="3abbb-311">Dans certains cas, une propriété peut être récupérée par le biais de la méthode [**IUIFramework :: GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) et définie avec la méthode [**IUIFramework :: SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) .</span><span class="sxs-lookup"><span data-stu-id="3abbb-311">In some cases, a property can be retrieved through the [**IUIFramework::GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) method and set with the [**IUIFramework::SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) method.</span></span>

 

<span data-ttu-id="3abbb-312">Le tableau suivant répertorie les clés de propriété associées au contrôle font.</span><span class="sxs-lookup"><span data-stu-id="3abbb-312">The following table lists the property keys that are associated with the Font Control.</span></span>



| <span data-ttu-id="3abbb-313">Clé de propriété</span><span class="sxs-lookup"><span data-stu-id="3abbb-313">Property Key</span></span>                                                                                                                  | <span data-ttu-id="3abbb-314">Notes</span><span class="sxs-lookup"><span data-stu-id="3abbb-314">Notes</span></span>                                                                                                                                                                                                                                                                                                                                                                                          |
|-------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3abbb-315">IU \_ \_ FontProperties</span><span class="sxs-lookup"><span data-stu-id="3abbb-315">UI\_PKEY\_FontProperties</span></span>](windowsribbon-reference-properties-uipkey-fontproperties.md)                                      | <span data-ttu-id="3abbb-316">Expose, dans l’agrégat comme un objet [IPropertyStore](/windows/win32/api/propsys/nn-propsys-ipropertystore) , toutes les propriétés de sous-contrôle de contrôle de police.</span><span class="sxs-lookup"><span data-stu-id="3abbb-316">Exposes, in aggregate as an [IPropertyStore](/windows/win32/api/propsys/nn-propsys-ipropertystore) object, all Font Control sub-control properties.</span></span><br/> <span data-ttu-id="3abbb-317">L’infrastructure interroge cette propriété lorsque `UI_INVALIDATIONS_VALUE` est passé comme valeur des *indicateurs* dans l’appel à [**IUIFramework :: InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand).</span><span class="sxs-lookup"><span data-stu-id="3abbb-317">The framework queries this property when `UI_INVALIDATIONS_VALUE` is passed as the value of *flags* in the call to [**IUIFramework::InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand).</span></span><br/> |
| [<span data-ttu-id="3abbb-318">IU \_ \_ FontProperties \_ ChangedProperties</span><span class="sxs-lookup"><span data-stu-id="3abbb-318">UI\_PKEY\_FontProperties\_ChangedProperties</span></span>](windowsribbon-reference-properties-uipkey-fontproperties-changedproperties.md) | <span data-ttu-id="3abbb-319">Expose, dans l’agrégat comme un objet [**IUISimplePropertySet**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) , uniquement les propriétés de sous-contrôle de police qui ont changé.</span><span class="sxs-lookup"><span data-stu-id="3abbb-319">Exposes, in aggregate as an [**IUISimplePropertySet**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) object, only Font Control sub-control properties that have changed.</span></span><br/>                                                                                                                                                                                                        |
| [<span data-ttu-id="3abbb-320">KeyTip de l’interface utilisateur \_ \_</span><span class="sxs-lookup"><span data-stu-id="3abbb-320">UI\_PKEY\_Keytip</span></span>](windowsribbon-reference-properties-uipkey-keytip.md)                                                      | <span data-ttu-id="3abbb-321">Peut uniquement être mis à jour par le biais d’une invalidation.</span><span class="sxs-lookup"><span data-stu-id="3abbb-321">Can only be updated through invalidation.</span></span>                                                                                                                                                                                                                                                                                                                                                      |
| [<span data-ttu-id="3abbb-322">IU-au-dessus \_ \_ activé</span><span class="sxs-lookup"><span data-stu-id="3abbb-322">UI\_PKEY\_Enabled</span></span>](windowsribbon-reference-properties-uipkey-enabled.md)                                                    | <span data-ttu-id="3abbb-323">Prend en charge [**IUIFramework :: GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) et [**IUIFramework :: SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty).</span><span class="sxs-lookup"><span data-stu-id="3abbb-323">Supports [**IUIFramework::GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) and [**IUIFramework::SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty).</span></span>                                                                                                                                                                  |



 

<span data-ttu-id="3abbb-324">Outre les propriétés prises en charge par le contrôle de police lui-même, l’infrastructure du ruban définit également une [clé de propriété](windowsribbon-reference-properties.md) pour chaque sous-contrôle de contrôle de police.</span><span class="sxs-lookup"><span data-stu-id="3abbb-324">In addition to the properties supported by the Font Control itself, the Ribbon framework also defines a [property key](windowsribbon-reference-properties.md) for each Font Control sub-control.</span></span> <span data-ttu-id="3abbb-325">Ces clés de propriété et leurs valeurs sont exposées par l’infrastructure par le biais d’une implémentation d’interface [IPropertyStore](/windows/win32/api/propsys/nn-propsys-ipropertystore) qui définit les méthodes de gestion d’une collection, également appelées « conteneurs de propriétés », de paires nom/valeur.</span><span class="sxs-lookup"><span data-stu-id="3abbb-325">These property keys and their values are exposed by the framework through an [IPropertyStore](/windows/win32/api/propsys/nn-propsys-ipropertystore) interface implementation that defines the methods for managing a collection, also called a property bag, of name and value pairs.</span></span>

<span data-ttu-id="3abbb-326">L’application convertit les structures de police en propriétés accessibles par le biais des méthodes de l’interface [IPropertyStore](/windows/win32/api/propsys/nn-propsys-ipropertystore) .</span><span class="sxs-lookup"><span data-stu-id="3abbb-326">The application translates the font structures to properties that are accessible through the [IPropertyStore](/windows/win32/api/propsys/nn-propsys-ipropertystore) interface methods.</span></span> <span data-ttu-id="3abbb-327">Ce modèle met en évidence la distinction entre le contrôle de police et les composants de pile de texte Windows Graphics Device Interface (GDI) ([structure LogFont](/windows/win32/api/wingdi/ns-wingdi-logfonta), [structure CHOOSEFONT](/windows/win32/api/commdlg/ns-commdlg-choosefonta)et [structure CHARFORMAT2](/windows/win32/api/richedit/ns-richedit-charformat2a)) qui sont pris en charge par l’infrastructure.</span><span class="sxs-lookup"><span data-stu-id="3abbb-327">This model emphasizes the distinction between the Font Control and the Windows Graphics Device Interface (GDI) text stack components ([LOGFONT Structure](/windows/win32/api/wingdi/ns-wingdi-logfonta), [CHOOSEFONT Structure](/windows/win32/api/commdlg/ns-commdlg-choosefonta), and [CHARFORMAT2 Structure](/windows/win32/api/richedit/ns-richedit-charformat2a)) that are supported by the framework.</span></span>

<span data-ttu-id="3abbb-328">Le tableau suivant répertorie les contrôles individuels et leurs clés de propriété associées.</span><span class="sxs-lookup"><span data-stu-id="3abbb-328">The following table lists the individual controls and their associated property keys.</span></span>



| <span data-ttu-id="3abbb-329">Commandes</span><span class="sxs-lookup"><span data-stu-id="3abbb-329">Controls</span></span>                 | <span data-ttu-id="3abbb-330">Clé de propriété</span><span class="sxs-lookup"><span data-stu-id="3abbb-330">Property Key</span></span>                                                                                                                                                                                                                                                           | <span data-ttu-id="3abbb-331">Notes</span><span class="sxs-lookup"><span data-stu-id="3abbb-331">Notes</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|--------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3abbb-332">**Taille de la police**</span><span class="sxs-lookup"><span data-stu-id="3abbb-332">**Font size**</span></span>            | [<span data-ttu-id="3abbb-333">\_Taille de \_ FontProperties de l’interface utilisateur \_</span><span class="sxs-lookup"><span data-stu-id="3abbb-333">UI\_PKEY\_FontProperties\_Size</span></span>](windowsribbon-reference-properties-uipkey-fontproperties-size.md)                                                                                                                                                                    | <span data-ttu-id="3abbb-334">Lorsqu’une exécution de texte de taille hétérogène est mise en surbrillance, l’infrastructure du ruban définit le contrôle de la **taille** de la police sur vide et la valeur de l' [interface utilisateur \_ \_ FontProperties \_ taille](windowsribbon-reference-properties-uipkey-fontproperties-size.md) sur 0.</span><span class="sxs-lookup"><span data-stu-id="3abbb-334">When a run of heterogeneously sized text is highlighted, the Ribbon framework sets the **Font size** control to blank and the value of [UI\_PKEY\_FontProperties\_Size](windowsribbon-reference-properties-uipkey-fontproperties-size.md) to 0.</span></span> <span data-ttu-id="3abbb-335">Lorsque l’utilisateur clique sur le bouton **agrandir la police** ou **réduire la police** , tout le texte mis en surbrillance est redimensionné, mais la différence relative dans les tailles de texte est conservée.</span><span class="sxs-lookup"><span data-stu-id="3abbb-335">When the **Grow font** or **Shrink font** button is clicked, all highlighted text is resized but the relative difference in text sizes is preserved.</span></span>                                                                                                                                                    |
| <span data-ttu-id="3abbb-336">**Famille de polices**</span><span class="sxs-lookup"><span data-stu-id="3abbb-336">**Font family**</span></span>          | [<span data-ttu-id="3abbb-337">\_Famille de \_ FontProperties de l’interface utilisateur \_</span><span class="sxs-lookup"><span data-stu-id="3abbb-337">UI\_PKEY\_FontProperties\_Family</span></span>](windowsribbon-reference-properties-uipkey-fontproperties-family.md)                                                                                                                                                                | <span data-ttu-id="3abbb-338">Les noms des familles de polices GDI varient selon les paramètres régionaux système.</span><span class="sxs-lookup"><span data-stu-id="3abbb-338">GDI font family names vary with system locale.</span></span> <span data-ttu-id="3abbb-339">Par conséquent, si la valeur de [la \_ \_ \_ famille FontProperties de l’interface utilisateur](windowsribbon-reference-properties-uipkey-fontproperties-family.md) est conservée entre les sessions d’application, cette valeur doit être récupérée sur chaque nouvelle session.</span><span class="sxs-lookup"><span data-stu-id="3abbb-339">As such, if the value of [UI\_PKEY\_FontProperties\_Family](windowsribbon-reference-properties-uipkey-fontproperties-family.md) is preserved across application sessions, that value should be retrieved on each new session.</span></span>                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="3abbb-340">**Agrandir la police**</span><span class="sxs-lookup"><span data-stu-id="3abbb-340">**Grow font**</span></span>            | [<span data-ttu-id="3abbb-341">\_Taille de \_ FontProperties de l’interface utilisateur \_</span><span class="sxs-lookup"><span data-stu-id="3abbb-341">UI\_PKEY\_FontProperties\_Size</span></span>](windowsribbon-reference-properties-uipkey-fontproperties-size.md)                                                                                                                                                                    | <span data-ttu-id="3abbb-342">Consultez **taille de police**.</span><span class="sxs-lookup"><span data-stu-id="3abbb-342">See **Font size**.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="3abbb-343">**Réduire la police**</span><span class="sxs-lookup"><span data-stu-id="3abbb-343">**Shrink font**</span></span>          | [<span data-ttu-id="3abbb-344">\_Taille de \_ FontProperties de l’interface utilisateur \_</span><span class="sxs-lookup"><span data-stu-id="3abbb-344">UI\_PKEY\_FontProperties\_Size</span></span>](windowsribbon-reference-properties-uipkey-fontproperties-size.md)                                                                                                                                                                    | <span data-ttu-id="3abbb-345">Consultez **taille de police**.</span><span class="sxs-lookup"><span data-stu-id="3abbb-345">See **Font size**.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="3abbb-346">**Gras**</span><span class="sxs-lookup"><span data-stu-id="3abbb-346">**Bold**</span></span>                 | [<span data-ttu-id="3abbb-347">IU \_ \_ FontProperties \_ gras</span><span class="sxs-lookup"><span data-stu-id="3abbb-347">UI\_PKEY\_FontProperties\_Bold</span></span>](windowsribbon-reference-properties-uipkey-fontproperties-bold.md)                                                                                                                                                                    |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="3abbb-348">**Italique**</span><span class="sxs-lookup"><span data-stu-id="3abbb-348">**Italic**</span></span>               | [<span data-ttu-id="3abbb-349">IU \_ \_ FontProperties \_ italique</span><span class="sxs-lookup"><span data-stu-id="3abbb-349">UI\_PKEY\_FontProperties\_Italic</span></span>](windowsribbon-reference-properties-uipkey-fontproperties-italic.md)                                                                                                                                                                |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="3abbb-350">**Souligner**</span><span class="sxs-lookup"><span data-stu-id="3abbb-350">**Underline**</span></span>            | [<span data-ttu-id="3abbb-351">IU \_ \_ FontProperties \_ souligné</span><span class="sxs-lookup"><span data-stu-id="3abbb-351">UI\_PKEY\_FontProperties\_Underline</span></span>](windowsribbon-reference-properties-uipkey-fontproperties-underline.md)                                                                                                                                                          |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="3abbb-352">**Barré**</span><span class="sxs-lookup"><span data-stu-id="3abbb-352">**Strikethrough**</span></span>        | [<span data-ttu-id="3abbb-353">IU \_ \_ FontProperties \_ barré</span><span class="sxs-lookup"><span data-stu-id="3abbb-353">UI\_PKEY\_FontProperties\_Strikethrough</span></span>](windowsribbon-reference-properties-uipkey-fontproperties-strikethrough.md)                                                                                                                                                  |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="3abbb-354">**Indice**</span><span class="sxs-lookup"><span data-stu-id="3abbb-354">**Subscript**</span></span>            | [<span data-ttu-id="3abbb-355">IU \_ \_ FontProperties \_ VerticalPositioning</span><span class="sxs-lookup"><span data-stu-id="3abbb-355">UI\_PKEY\_FontProperties\_VerticalPositioning</span></span>](windowsribbon-reference-properties-uipkey-fontproperties-verticalpositioning.md)                                                                                                                                      | <span data-ttu-id="3abbb-356">Si le bouton d' **indice** est défini, l' **exposant** ne peut pas être défini.</span><span class="sxs-lookup"><span data-stu-id="3abbb-356">If the **Subscript** button is set, then the **Superscript** cannot also be set.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="3abbb-357">**Exposant**</span><span class="sxs-lookup"><span data-stu-id="3abbb-357">**Superscript**</span></span>          | [<span data-ttu-id="3abbb-358">IU \_ \_ FontProperties \_ VerticalPositioning</span><span class="sxs-lookup"><span data-stu-id="3abbb-358">UI\_PKEY\_FontProperties\_VerticalPositioning</span></span>](windowsribbon-reference-properties-uipkey-fontproperties-verticalpositioning.md)                                                                                                                                      | <span data-ttu-id="3abbb-359">Si le bouton **exposant** est défini, l' **indice** ne peut pas être également défini.</span><span class="sxs-lookup"><span data-stu-id="3abbb-359">If the **Superscript** button is set, then the **Subscript** cannot also be set.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="3abbb-360">**Couleur de mise en surbrillance du texte**</span><span class="sxs-lookup"><span data-stu-id="3abbb-360">**Text highlight color**</span></span> | <span data-ttu-id="3abbb-361">[Interface utilisateur \_ \_FontProperties \_ backgroundColor](/windows/desktop/windowsribbon/windowsribbon-reference-properties-uipkey-fontproperties-backgroundcolor), [IU \_ \_ FontProperties \_ BackgroundColorType](windowsribbon-reference-properties-uipkey-fontproperties-backgroundcolortype.md)</span><span class="sxs-lookup"><span data-stu-id="3abbb-361">[UI\_PKEY\_FontProperties\_BackgroundColor](/windows/desktop/windowsribbon/windowsribbon-reference-properties-uipkey-fontproperties-backgroundcolor), [UI\_PKEY\_FontProperties\_BackgroundColorType](windowsribbon-reference-properties-uipkey-fontproperties-backgroundcolortype.md)</span></span> | <span data-ttu-id="3abbb-362">Fournit les mêmes fonctionnalités que le `HighlightColors` modèle de l’élément [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md) .</span><span class="sxs-lookup"><span data-stu-id="3abbb-362">Provides the same functionality as the `HighlightColors` template of the [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md) element.</span></span><br/> <span data-ttu-id="3abbb-363">Nous vous recommandons vivement de définir uniquement une valeur de **couleur de mise en surbrillance du texte** initiale par l’application.</span><span class="sxs-lookup"><span data-stu-id="3abbb-363">We highly recommend that only an initial **Text highlight color** value be set by the application.</span></span> <span data-ttu-id="3abbb-364">La dernière valeur sélectionnée doit être conservée et non définie lorsque le curseur est repositionné dans un document.</span><span class="sxs-lookup"><span data-stu-id="3abbb-364">The last selected value should be preserved and not set when the cursor is repositioned within a document.</span></span> <span data-ttu-id="3abbb-365">Cela permet d’accéder rapidement à la dernière sélection de l’utilisateur, et il n’est pas nécessaire de rouvrir le sélecteur de couleurs.</span><span class="sxs-lookup"><span data-stu-id="3abbb-365">This allows quick access to the user's last selection, and the color picker does not have to be reopened.</span></span><br/> <span data-ttu-id="3abbb-366">Les échantillons de couleurs ne peuvent pas être personnalisés.</span><span class="sxs-lookup"><span data-stu-id="3abbb-366">Color swatches cannot be customized.</span></span><br/> |
| <span data-ttu-id="3abbb-367">**Couleur du texte**</span><span class="sxs-lookup"><span data-stu-id="3abbb-367">**Text color**</span></span>           | <span data-ttu-id="3abbb-368">[Interface utilisateur \_ \_FontProperties \_ ForegroundColor](windowsribbon-reference-properties-uipkey-fontproperties-foregroundcolor.md), [IU # \_ \_ FontProperties \_ ForegroundColorType](windowsribbon-reference-properties-uipkey-fontproperties-foregroundcolortype.md)</span><span class="sxs-lookup"><span data-stu-id="3abbb-368">[UI\_PKEY\_FontProperties\_ForegroundColor](windowsribbon-reference-properties-uipkey-fontproperties-foregroundcolor.md), [UI\_PKEY\_FontProperties\_ForegroundColorType](windowsribbon-reference-properties-uipkey-fontproperties-foregroundcolortype.md)</span></span>           | <span data-ttu-id="3abbb-369">Fournit les mêmes fonctionnalités que le `StandardColors` modèle de l’élément [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md) .</span><span class="sxs-lookup"><span data-stu-id="3abbb-369">Provides the same functionality as the `StandardColors` template of the [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md) element.</span></span><br/> <span data-ttu-id="3abbb-370">Nous vous recommandons vivement de définir uniquement une valeur de **couleur de texte** initiale par l’application.</span><span class="sxs-lookup"><span data-stu-id="3abbb-370">We highly recommend that only an initial **Text color** value be set by the application.</span></span> <span data-ttu-id="3abbb-371">La dernière valeur sélectionnée doit être conservée et non définie lorsque le curseur est repositionné dans un document.</span><span class="sxs-lookup"><span data-stu-id="3abbb-371">The last selected value should be preserved and not set when the cursor is repositioned within a document.</span></span> <span data-ttu-id="3abbb-372">Cela permet d’accéder rapidement à la dernière sélection de l’utilisateur, et il n’est pas nécessaire de rouvrir le sélecteur de couleurs.</span><span class="sxs-lookup"><span data-stu-id="3abbb-372">This allows quick access to the user's last selection, and the color picker does not have to be reopened.</span></span><br/> <span data-ttu-id="3abbb-373">Les échantillons de couleurs ne peuvent pas être personnalisés.</span><span class="sxs-lookup"><span data-stu-id="3abbb-373">Color swatches cannot be customized.</span></span><br/>            |



 

## <a name="define-a-fontcontrol-command-handler"></a><span data-ttu-id="3abbb-374">Définir un gestionnaire de commandes FontControl</span><span class="sxs-lookup"><span data-stu-id="3abbb-374">Define a FontControl Command Handler</span></span>

<span data-ttu-id="3abbb-375">Cette section décrit les étapes nécessaires pour lier un contrôle de police à un gestionnaire de commandes.</span><span class="sxs-lookup"><span data-stu-id="3abbb-375">This section describes the steps required to bind a Font Control to a Command handler.</span></span>

> [!WARNING]
> <span data-ttu-id="3abbb-376">Toute tentative de sélection d’un échantillon de couleur dans le sélecteur de couleurs d’un contrôle de police peut entraîner une violation d’accès si aucun gestionnaire de commandes n’est associé au contrôle.</span><span class="sxs-lookup"><span data-stu-id="3abbb-376">Any attempt to select a color swatch from the color picker of a Font Control may result in an access violation if no Command handler is associated with the control.</span></span>

 

<span data-ttu-id="3abbb-377">L’exemple de code suivant montre comment lier des commandes qui sont déclarées dans le balisage à un gestionnaire de commandes.</span><span class="sxs-lookup"><span data-stu-id="3abbb-377">The following code example demonstrates how to bind Commands that are declared in markup to a Command handler.</span></span>


```C++
//
//  FUNCTION: OnCreateUICommand(UINT, UI_COMMANDTYPE, IUICommandHandler)
//
//  PURPOSE: Called by the Ribbon framework for each command specified in markup, to allow
//           the host application to bind a command handler to that command.
//
STDMETHODIMP CApplication::OnCreateUICommand(
  UINT nCmdID,
  __in UI_COMMANDTYPE typeID,
  __deref_out IUICommandHandler** ppCommandHandler)
{
  UNREFERENCED_PARAMETER(typeID);
  UNREFERENCED_PARAMETER(nCmdID);

  if (NULL == m_pCommandHandler)
  {
    HRESULT hr = CCommandHandler::CreateInstance(&m_pCommandHandler);
    if (FAILED(hr))
    {
      return hr;
    }
  }

  return m_pCommandHandler->QueryInterface(IID_PPV_ARGS(ppCommandHandler));
}
```



<span data-ttu-id="3abbb-378">L’exemple de code suivant montre comment implémenter la méthode [**IUICommandHandler :: Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) pour un contrôle font.</span><span class="sxs-lookup"><span data-stu-id="3abbb-378">The following code example illustrates how to implement the [**IUICommandHandler::Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) method for a Font Control.</span></span>


```C++
//
//  FUNCTION: Execute()
//
//  PURPOSE: Called by the Ribbon framework when a command is executed 
//           by the user. For example, when a button is pressed.
//
STDMETHODIMP CCommandHandler::Execute(
  UINT nCmdID,
  UI_EXECUTIONVERB verb,
  __in_opt const PROPERTYKEY* key,
  __in_opt const PROPVARIANT* ppropvarValue,
  __in_opt IUISimplePropertySet* pCommandExecutionProperties)
{
  UNREFERENCED_PARAMETER(nCmdID);

  HRESULT hr = E_NOTIMPL;
  if ((key) && (*key == UI_PKEY_FontProperties))
  {
    // Font properties have changed.
    switch (verb)
    {
      case UI_EXECUTIONVERB_EXECUTE:
      {
        hr = E_POINTER;
        if (pCommandExecutionProperties != NULL)
        {
          // Get the changed properties.
          PROPVARIANT varChanges;
          hr = pCommandExecutionProperties->GetValue(UI_PKEY_FontProperties_ChangedProperties, &varChanges);
          if (SUCCEEDED(hr))
          {
            IPropertyStore *pChanges;
            hr = UIPropertyToInterface(UI_PKEY_FontProperties, varChanges, &pChanges);
            if (SUCCEEDED(hr))
            {
              // Using the changed properties, set the new font on the selection on RichEdit control.
              g_pFCSampleAppManager->SetValues(pChanges);
              pChanges->Release();
            }
            PropVariantClear(&varChanges);
          }
        }
        break;
      }
      case UI_EXECUTIONVERB_PREVIEW:
      {
        hr = E_POINTER;
        if (pCommandExecutionProperties != NULL)
        {
          // Get the changed properties for the preview event.
          PROPVARIANT varChanges;
          hr = pCommandExecutionProperties->GetValue(UI_PKEY_FontProperties_ChangedProperties, &varChanges);
          if (SUCCEEDED(hr))
          {
            IPropertyStore *pChanges;
            hr = UIPropertyToInterface(UI_PKEY_FontProperties, varChanges, &pChanges);
            if (SUCCEEDED(hr))
            {
              // Set the previewed values on the RichEdit control.
              g_pFCSampleAppManager->SetPreviewValues(pChanges);
              pChanges->Release();
            }
            PropVariantClear(&varChanges);
          }
        }
        break;
      }
      case UI_EXECUTIONVERB_CANCELPREVIEW:
      {
        hr = E_POINTER;
        if (ppropvarValue != NULL)
        {
          // Cancel the preview.
          IPropertyStore *pValues;
          hr = UIPropertyToInterface(UI_PKEY_FontProperties, *ppropvarValue, &pValues);
          if (SUCCEEDED(hr))
          {   
            g_pFCSampleAppManager->CancelPreview(pValues);
            pValues->Release();
          }
        }
        break;
      }
    }
  }

  return hr;
}
```



<span data-ttu-id="3abbb-379">L’exemple de code suivant montre comment implémenter la méthode [**IUICommandHandler :: UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) pour un contrôle font.</span><span class="sxs-lookup"><span data-stu-id="3abbb-379">The following code example illustrates how to implement the [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) method for a Font Control.</span></span>


```C++
//
//  FUNCTION: UpdateProperty()
//
//  PURPOSE: Called by the Ribbon framework when a command property (PKEY) needs to be updated.
//
//  COMMENTS:
//
//    This function is used to provide new command property values, such as labels, icons, or
//    tooltip information, when requested by the Ribbon framework.  
//    
//
STDMETHODIMP CCommandHandler::UpdateProperty(
  UINT nCmdID,
  __in REFPROPERTYKEY key,
  __in_opt const PROPVARIANT* ppropvarCurrentValue,
  __out PROPVARIANT* ppropvarNewValue)
{
  UNREFERENCED_PARAMETER(nCmdID);

  HRESULT hr = E_NOTIMPL;
  if (key == UI_PKEY_FontProperties)
  {
    hr = E_POINTER;
    if (ppropvarCurrentValue != NULL)
    {
      // Get the font values for the selected text in the font control.
      IPropertyStore *pValues;
      hr = UIPropertyToInterface(UI_PKEY_FontProperties, *ppropvarCurrentValue, &pValues);
      if (SUCCEEDED(hr))
      {
        g_pFCSampleAppManager->GetValues(pValues);

        // Provide the new values to the font control.
        hr = UIInitPropertyFromInterface(UI_PKEY_FontProperties, pValues, ppropvarNewValue);
        pValues->Release();
      }
    }
  }

  return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="3abbb-380">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="3abbb-380">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3abbb-381">Bibliothèque de contrôles de l’infrastructure du ruban Windows</span><span class="sxs-lookup"><span data-stu-id="3abbb-381">Windows Ribbon Framework Control Library</span></span>](windowsribbon-controls-entry.md)
</dt> <dt>

[<span data-ttu-id="3abbb-382">**Élément FontControl**</span><span class="sxs-lookup"><span data-stu-id="3abbb-382">**FontControl element**</span></span>](windowsribbon-element-fontcontrol.md)
</dt> <dt>

[<span data-ttu-id="3abbb-383">Propriétés du contrôle de police</span><span class="sxs-lookup"><span data-stu-id="3abbb-383">Font Control Properties</span></span>](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[<span data-ttu-id="3abbb-384">Exemple FontControl</span><span class="sxs-lookup"><span data-stu-id="3abbb-384">FontControl Sample</span></span>](windowsribbon-fontcontrolsample.md)
</dt> </dl>

 

