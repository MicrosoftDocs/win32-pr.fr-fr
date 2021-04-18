---
title: Personnalisation d’un ruban à l’aide de définitions de taille et de stratégies de mise à l’échelle
description: Les contrôles hébergés dans la barre de commandes du ruban sont soumis aux règles de disposition appliquées par l’infrastructure du ruban Windows et basées sur une combinaison de comportements par défaut et de modèles de disposition (à la fois définis par l’infrastructure et personnalisées) comme déclaré dans le balisage du ruban. Ces règles définissent les comportements de disposition adaptative de l’infrastructure du ruban qui influencent la manière dont les contrôles de la barre de commandes s’adaptent aux différentes tailles de ruban au moment de l’exécution.
ms.assetid: b5869394-3fa9-4817-add9-54487434fc4f
keywords:
- Ruban Windows, personnalisation
- Ruban, personnalisation
- Ruban Windows, modèles SizeDefinition
- Ruban, modèles SizeDefinition
- Ruban Windows, modèles personnalisés
- Ruban, modèles personnalisés
- personnalisation du ruban Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b12618f88576cddeff119534215e501216193c3
ms.sourcegitcommit: 2387bc0339a1764564c1509e72ed5f2e8ae60b36
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/30/2020
ms.locfileid: "104568675"
---
# <a name="customizing-a-ribbon-through-size-definitions-and-scaling-policies"></a><span data-ttu-id="9b03a-111">Personnalisation d’un ruban à l’aide de définitions de taille et de stratégies de mise à l’échelle</span><span class="sxs-lookup"><span data-stu-id="9b03a-111">Customizing a Ribbon Through Size Definitions and Scaling Policies</span></span>

<span data-ttu-id="9b03a-112">Les contrôles hébergés dans la barre de commandes du ruban sont soumis aux règles de disposition appliquées par l’infrastructure du ruban Windows et basées sur une combinaison de comportements par défaut et de modèles de disposition (à la fois définis par l’infrastructure et personnalisées) comme déclaré dans le balisage du ruban.</span><span class="sxs-lookup"><span data-stu-id="9b03a-112">Controls hosted in the ribbon Command bar are subject to layout rules that are enforced by the Windows Ribbon framework and based on a combination of default behaviors and layout templates (both framework-defined and custom) as declared in the Ribbon markup.</span></span> <span data-ttu-id="9b03a-113">Ces règles définissent les comportements de disposition adaptative de l’infrastructure du ruban qui influencent la manière dont les contrôles de la barre de commandes s’adaptent aux différentes tailles de ruban au moment de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="9b03a-113">These rules define the adaptive layout behaviors of the Ribbon framework that influence how controls in the Command bar adapt to various ribbon sizes at run time.</span></span>

-   [<span data-ttu-id="9b03a-114">Introduction</span><span class="sxs-lookup"><span data-stu-id="9b03a-114">Introduction</span></span>](#introduction)
    -   [<span data-ttu-id="9b03a-115">Modèles SizeDefinition du ruban</span><span class="sxs-lookup"><span data-stu-id="9b03a-115">Ribbon SizeDefinition Templates</span></span>](#customizing-a-ribbon-through-size-definitions-and-scaling-policies)
    -   [<span data-ttu-id="9b03a-116">Modèles personnalisés</span><span class="sxs-lookup"><span data-stu-id="9b03a-116">Custom Templates</span></span>](#custom-templates)
-   [<span data-ttu-id="9b03a-117">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="9b03a-117">Related topics</span></span>](#related-topics)

## <a name="introduction"></a><span data-ttu-id="9b03a-118">Introduction</span><span class="sxs-lookup"><span data-stu-id="9b03a-118">Introduction</span></span>

<span data-ttu-id="9b03a-119">La disposition adaptative, telle que définie par l’infrastructure du ruban, est la capacité de tous les contrôles dans l’interface utilisateur du ruban à ajuster dynamiquement leur organisation, leur taille, leur format et leur échelle relative en fonction des modifications apportées à la taille du ruban au moment de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="9b03a-119">Adaptive layout, as defined by the Ribbon framework, is the ability of all controls within the ribbon UI to dynamically adjust their organization, size, format, and relative scale based on changes to the size of the ribbon at run time.</span></span>

<span data-ttu-id="9b03a-120">L’infrastructure expose les fonctionnalités de disposition adaptative via un ensemble d’éléments de balisage dédiés à la spécification et à la personnalisation de divers comportements de disposition.</span><span class="sxs-lookup"><span data-stu-id="9b03a-120">The framework exposes adaptive layout functionality through a set of markup elements that are dedicated to specifying and customizing various layout behaviors.</span></span> <span data-ttu-id="9b03a-121">Une collection de modèles, appelée [**SizeDefinitions**](windowsribbon-element-sizedefinition.md), est définie par l’infrastructure, qui prend en charge différents scénarios de contrôle et de mise en page.</span><span class="sxs-lookup"><span data-stu-id="9b03a-121">A collection of templates, called [**SizeDefinitions**](windowsribbon-element-sizedefinition.md), is defined by the framework, each of which support various control and layout scenarios.</span></span> <span data-ttu-id="9b03a-122">Toutefois, le Framework prend également en charge les modèles personnalisés si les modèles prédéfinis ne fournissent pas l’expérience de l’interface utilisateur ou les dispositions requises par une application.</span><span class="sxs-lookup"><span data-stu-id="9b03a-122">However, the framework also supports custom templates should the predefined templates not provide the UI experience or layouts required by an application.</span></span>

<span data-ttu-id="9b03a-123">Pour afficher les contrôles dans une disposition par défaut à une taille de ruban particulière, les modèles prédéfinis et les modèles personnalisés fonctionnent conjointement avec l’élément [**ScalingPolicy**](windowsribbon-element-scalingpolicy.md) .</span><span class="sxs-lookup"><span data-stu-id="9b03a-123">To display controls in a preferred layout at a particular ribbon size, both predefined templates and custom templates work in conjunction with the [**ScalingPolicy**](windowsribbon-element-scalingpolicy.md) element.</span></span> <span data-ttu-id="9b03a-124">Cet élément contient un manifeste des préférences de taille que l’infrastructure utilise comme guide lors du rendu du ruban.</span><span class="sxs-lookup"><span data-stu-id="9b03a-124">This element contains a manifest of size preferences that the framework uses as a guide when rendering the ribbon.</span></span>

> [!Note]  
> <span data-ttu-id="9b03a-125">L’infrastructure du ruban fournit des comportements de disposition par défaut basés sur un ensemble d’heuristiques intégrées pour l’organisation et la présentation des contrôles au moment de l’exécution sans avoir besoin des modèles [**SizeDefinition**](windowsribbon-element-sizedefinition.md) prédéfinis.</span><span class="sxs-lookup"><span data-stu-id="9b03a-125">The Ribbon framework provides default layout behaviors based on a set of built-in heuristics for the organization and presentation of controls at run time without the need for the predefined [**SizeDefinition**](windowsribbon-element-sizedefinition.md) templates.</span></span> <span data-ttu-id="9b03a-126">Toutefois, cette fonctionnalité est destinée uniquement à des fins de prototypage.</span><span class="sxs-lookup"><span data-stu-id="9b03a-126">However, this capability is intended for prototyping purposes only.</span></span>

 

### <a name="ribbon-sizedefinition-templates"></a><span data-ttu-id="9b03a-127">Modèles SizeDefinition du ruban</span><span class="sxs-lookup"><span data-stu-id="9b03a-127">Ribbon SizeDefinition Templates</span></span>

<span data-ttu-id="9b03a-128">L’infrastructure du ruban fournit un ensemble complet de modèles [**SizeDefinition**](windowsribbon-element-sizedefinition.md) qui spécifient le comportement de taille et de disposition pour un [Groupe](windowsribbon-controls-group.md) de contrôles de ruban.</span><span class="sxs-lookup"><span data-stu-id="9b03a-128">The Ribbon framework provides a comprehensive set of [**SizeDefinition**](windowsribbon-element-sizedefinition.md) templates that specify size and layout behavior for a [Group](windowsribbon-controls-group.md) of Ribbon controls.</span></span> <span data-ttu-id="9b03a-129">Ces modèles couvrent la plupart des scénarios courants d’organisation des contrôles dans une application de ruban.</span><span class="sxs-lookup"><span data-stu-id="9b03a-129">These templates cover most common scenarios for organizing controls in a Ribbon application.</span></span>

<span data-ttu-id="9b03a-130">Pour garantir une expérience utilisateur cohérente entre les applications du ruban, chaque modèle [**SizeDefinition**](windowsribbon-element-sizedefinition.md) impose des restrictions sur les contrôles ou la famille de contrôles qu’il prend en charge.</span><span class="sxs-lookup"><span data-stu-id="9b03a-130">To enforce a consistent user experience across Ribbon applications, each [**SizeDefinition**](windowsribbon-element-sizedefinition.md) template imposes restrictions on the controls or the family of controls it supports.</span></span>

<span data-ttu-id="9b03a-131">Par exemple, la famille de contrôles Button comprend les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="9b03a-131">For example, the button family of controls includes:</span></span>

-   [<span data-ttu-id="9b03a-132">Button</span><span class="sxs-lookup"><span data-stu-id="9b03a-132">Button</span></span>](windowsribbon-controls-button.md)
-   [<span data-ttu-id="9b03a-133">Bouton bascule</span><span class="sxs-lookup"><span data-stu-id="9b03a-133">Toggle Button</span></span>](windowsribbon-controls-togglebutton.md)
-   [<span data-ttu-id="9b03a-134">Bouton déroulant</span><span class="sxs-lookup"><span data-stu-id="9b03a-134">Drop-Down Button</span></span>](windowsribbon-controls-dropdownbutton.md)
-   [<span data-ttu-id="9b03a-135">Bouton partagé</span><span class="sxs-lookup"><span data-stu-id="9b03a-135">Split Button</span></span>](windowsribbon-controls-splitbutton.md)
-   [<span data-ttu-id="9b03a-136">Galerie déroulante</span><span class="sxs-lookup"><span data-stu-id="9b03a-136">Drop-Down Gallery</span></span>](windowsribbon-controls-dropdowngallery.md)
-   [<span data-ttu-id="9b03a-137">Galerie de boutons partagés</span><span class="sxs-lookup"><span data-stu-id="9b03a-137">Split Button Gallery</span></span>](windowsribbon-controls-splitbuttongallery.md)
-   [<span data-ttu-id="9b03a-138">Sélecteur de couleurs déroulantes</span><span class="sxs-lookup"><span data-stu-id="9b03a-138">Drop-Down Color Picker</span></span>](windowsribbon-controls-dropdowncolorpicker.md)

<span data-ttu-id="9b03a-139">La famille de contrôles d’entrée comprend les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="9b03a-139">While the input family of controls includes:</span></span>

-   [<span data-ttu-id="9b03a-140">Zone de liste déroulante</span><span class="sxs-lookup"><span data-stu-id="9b03a-140">Combo Box</span></span>](windowsribbon-controls-combobox.md)
-   [<span data-ttu-id="9b03a-141">Spinner</span><span class="sxs-lookup"><span data-stu-id="9b03a-141">Spinner</span></span>](windowsribbon-controls-spinner.md)

<span data-ttu-id="9b03a-142">La case [à cocher](windowsribbon-controls-checkbox.md) et la [Galerie dans le ruban](windowsribbon-controls-inribbongallery.md) n’appartiennent ni à la famille de boutons, ni à la famille d’entrée.</span><span class="sxs-lookup"><span data-stu-id="9b03a-142">[Check Box](windowsribbon-controls-checkbox.md) and [In-Ribbon Gallery](windowsribbon-controls-inribbongallery.md) do not belong to either the button family or the input family.</span></span> <span data-ttu-id="9b03a-143">Ces deux contrôles peuvent être utilisés uniquement lorsqu’ils sont explicitement indiqués dans un modèle [**SizeDefinition**](windowsribbon-element-sizedefinition.md) .</span><span class="sxs-lookup"><span data-stu-id="9b03a-143">These two controls can be used only where explicitly indicated in a [**SizeDefinition**](windowsribbon-element-sizedefinition.md) template.</span></span>

<span data-ttu-id="9b03a-144">La liste suivante répertorie les modèles [**SizeDefinition**](windowsribbon-element-sizedefinition.md) avec une description de la disposition et des contrôles autorisés par chaque modèle.</span><span class="sxs-lookup"><span data-stu-id="9b03a-144">The following is a list of the [**SizeDefinition**](windowsribbon-element-sizedefinition.md) templates with a description of the layout and controls allowed by each template.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="9b03a-145">Si les contrôles déclarés dans le balisage ne sont pas mappés exactement au type de contrôle, à l’ordre et à la quantité définis dans le modèle associé, une [erreur de validation](windowsribbon-compilationerrors.md) est journalisée par le [compilateur de balisage](windowsribbon-intentcl.md) et la compilation est terminée.</span><span class="sxs-lookup"><span data-stu-id="9b03a-145">If the controls declared in markup do not map exactly to control type, order, and quantity defined in the associated template, a [validation error](windowsribbon-compilationerrors.md) is logged by the [markup compiler](windowsribbon-intentcl.md) and compilation is terminated.</span></span>

 



<span data-ttu-id="9b03a-146">OneButton</span><span class="sxs-lookup"><span data-stu-id="9b03a-146">OneButton</span></span>

<span data-ttu-id="9b03a-147">Un contrôle de famille de bouton.</span><span class="sxs-lookup"><span data-stu-id="9b03a-147">One button-family control.</span></span><br/> <span data-ttu-id="9b03a-148">Seule la taille de groupe importante est prise en charge.</span><span class="sxs-lookup"><span data-stu-id="9b03a-148">Only Large group size is supported.</span></span><br/>

![image du modèle oneButton sizedefinition.](images/overviews/sizedefinition-onebutton.png)

<span data-ttu-id="9b03a-150">TwoButtons</span><span class="sxs-lookup"><span data-stu-id="9b03a-150">TwoButtons</span></span>

<span data-ttu-id="9b03a-151">Deux contrôles de famille de boutons.</span><span class="sxs-lookup"><span data-stu-id="9b03a-151">Two button-family controls.</span></span><br/> <span data-ttu-id="9b03a-152">Seules les tailles de groupe de taille moyenne et moyenne sont prises en charge.</span><span class="sxs-lookup"><span data-stu-id="9b03a-152">Only Large and Medium group sizes are supported.</span></span><br/>

![image du modèle twobuttons large sizedefinition.](images/overviews/sizedefinition-twobuttons-large.png)

![image du modèle twobuttons Medium sizedefinition.](images/overviews/sizedefinition-twobuttons-medium.png)

<span data-ttu-id="9b03a-155">ThreeButtons</span><span class="sxs-lookup"><span data-stu-id="9b03a-155">ThreeButtons</span></span>

<span data-ttu-id="9b03a-156">Trois contrôles de la famille de boutons.</span><span class="sxs-lookup"><span data-stu-id="9b03a-156">Three button-family controls.</span></span><br/> <span data-ttu-id="9b03a-157">Seules les tailles de groupe de taille moyenne et moyenne sont prises en charge.</span><span class="sxs-lookup"><span data-stu-id="9b03a-157">Only Large and Medium group sizes are supported.</span></span><br/>

![image du modèle threebuttons large sizedefinition.](images/overviews/sizedefinition-threebuttons-large.png)

![image du modèle threebuttons Medium sizedefinition.](images/overviews/sizedefinition-threebuttons-medium.png)

<span data-ttu-id="9b03a-160">ThreeButtons-OneBigAndTwoSmall</span><span class="sxs-lookup"><span data-stu-id="9b03a-160">ThreeButtons-OneBigAndTwoSmall</span></span>

<span data-ttu-id="9b03a-161">Trois contrôles de la famille de boutons.</span><span class="sxs-lookup"><span data-stu-id="9b03a-161">Three button-family controls.</span></span><br/> <span data-ttu-id="9b03a-162">Le premier bouton est présenté de façon visible dans les trois tailles.</span><span class="sxs-lookup"><span data-stu-id="9b03a-162">The first button is presented prominently in all three sizes.</span></span><br/>

![image du modèle de grand sizedefinition threebuttons-onebigandtwosmall.](images/overviews/sizedefinition-threebuttons-onebigandtwosmall-large.png)

![image du modèle threebuttons-onebigandtwosmall Medium sizedefinition.](images/overviews/sizedefinition-threebuttons-onebigandtwosmall-medium.png)

![image du modèle threebuttons-onebigandtwosmall Small sizedefinition.](images/overviews/sizedefinition-threebuttons-onebigandtwosmall-small.png)

<span data-ttu-id="9b03a-166">ThreeButtonsAndOneCheckBox</span><span class="sxs-lookup"><span data-stu-id="9b03a-166">ThreeButtonsAndOneCheckBox</span></span>

<span data-ttu-id="9b03a-167">Trois contrôles de famille de boutons accompagnés d’un seul contrôle CheckBox.</span><span class="sxs-lookup"><span data-stu-id="9b03a-167">Three button-family controls accompanied by a single CheckBox control.</span></span><br/> <span data-ttu-id="9b03a-168">Seules les tailles de groupe de taille moyenne et moyenne sont prises en charge.</span><span class="sxs-lookup"><span data-stu-id="9b03a-168">Only Large and Medium group sizes are supported.</span></span><br/>

![image du modèle threebuttonsandonecheckbox large sizedefinition.](images/overviews/sizedefinition-threebuttonsandonecheckbox-large.png)

![image du modèle threebuttonsandonecheckbox Medium sizedefinition.](images/overviews/sizedefinition-threebuttonsandonecheckbox-medium.png)

<span data-ttu-id="9b03a-171">FourButtons</span><span class="sxs-lookup"><span data-stu-id="9b03a-171">FourButtons</span></span>

<span data-ttu-id="9b03a-172">Quatre contrôles de la famille de boutons.</span><span class="sxs-lookup"><span data-stu-id="9b03a-172">Four button-family controls.</span></span><br/>

![image du modèle fourbuttons large sizedefinition.](images/overviews/sizedefinition-fourbuttons-large.png)

![image du modèle fourbuttons Medium sizedefinition.](images/overviews/sizedefinition-fourbuttons-medium.png)

![image du modèle fourbuttons Small sizedefinition.](images/overviews/sizedefinition-fourbuttons-small.png)

<span data-ttu-id="9b03a-176">FiveButtons</span><span class="sxs-lookup"><span data-stu-id="9b03a-176">FiveButtons</span></span>

<span data-ttu-id="9b03a-177">Cinq contrôles de famille de boutons.</span><span class="sxs-lookup"><span data-stu-id="9b03a-177">Five button-family controls.</span></span><br/>

![image du modèle fivebuttons large sizedefinition.](images/overviews/sizedefinition-fivebuttons-large.png)

![image du modèle fivebuttons Medium sizedefinition.](images/overviews/sizedefinition-fivebuttons-medium.png)

![image du modèle fivebuttons Small sizedefinition.](images/overviews/sizedefinition-fivebuttons-small.png)

<span data-ttu-id="9b03a-181">FiveOrSixButtons</span><span class="sxs-lookup"><span data-stu-id="9b03a-181">FiveOrSixButtons</span></span>

<span data-ttu-id="9b03a-182">Cinq contrôles de famille de boutons et un sixième bouton facultatif.</span><span class="sxs-lookup"><span data-stu-id="9b03a-182">Five button-family controls and an optional sixth button.</span></span><br/>

![image du modèle fiveorsixbuttons large sizedefinition.](images/overviews/sizedefinition-fiveorsixbuttons-large.png)

![image du modèle fiveorsixbuttons Medium sizedefinition.](images/overviews/sizedefinition-fiveorsixbuttons-medium.png)

![image du modèle fiveorsixbuttons Small sizedefinition.](images/overviews/sizedefinition-fiveorsixbuttons-small.png)

<span data-ttu-id="9b03a-186">SixButtons</span><span class="sxs-lookup"><span data-stu-id="9b03a-186">SixButtons</span></span>

<span data-ttu-id="9b03a-187">Six contrôles de famille de boutons.</span><span class="sxs-lookup"><span data-stu-id="9b03a-187">Six button-family controls.</span></span><br/>

![image du modèle sixbuttons large sizedefinition.](images/overviews/sizedefinition-sixbuttons-large.png)

![image du modèle sixbuttons Medium sizedefinition.](images/overviews/sizedefinition-sixbuttons-medium.png)

![image du modèle sixbuttons Small sizedefinition.](images/overviews/sizedefinition-sixbuttons-small.png)

<span data-ttu-id="9b03a-191">SixButtons-TwoColumns</span><span class="sxs-lookup"><span data-stu-id="9b03a-191">SixButtons-TwoColumns</span></span>

<span data-ttu-id="9b03a-192">Six contrôles de famille de boutons (autre présentation).</span><span class="sxs-lookup"><span data-stu-id="9b03a-192">Six button-family controls (alternate presentation).</span></span><br/>

![image du modèle de grand sizedefinition sixbuttons-twocolumns.](images/overviews/sizedefinition-sixbuttons-twocolumns-large.png)

![modèle sixbuttons-twocolumns Medium sizedefinition.](images/overviews/sizedefinition-sixbuttons-twocolumns-medium.png)

![image du modèle sixbuttons-twocolumns Small sizedefinition.](images/overviews/sizedefinition-sixbuttons-twocolumns-small.png)

<span data-ttu-id="9b03a-196">SevenButtons</span><span class="sxs-lookup"><span data-stu-id="9b03a-196">SevenButtons</span></span>

<span data-ttu-id="9b03a-197">Sept contrôles de la famille de boutons.</span><span class="sxs-lookup"><span data-stu-id="9b03a-197">Seven button-family controls.</span></span><br/>

![image du modèle sevenbuttons large sizedefinition.](images/overviews/sizedefinition-sevenbuttons-large.png)

![image du modèle sevenbuttons mediumsizedefinition.](images/overviews/sizedefinition-sevenbuttons-medium.png)

![image du modèle sevenbuttons Small sizedefinition.](images/overviews/sizedefinition-sevenbuttons-small.png)

<span data-ttu-id="9b03a-201">EightButtons</span><span class="sxs-lookup"><span data-stu-id="9b03a-201">EightButtons</span></span>

<span data-ttu-id="9b03a-202">Huit contrôles de la famille de boutons.</span><span class="sxs-lookup"><span data-stu-id="9b03a-202">Eight button-family controls.</span></span><br/>

![image du modèle de grand sizedefinition eightbuttons-lastthreesmall.](images/overviews/sizedefinition-eightbuttons-lastthreesmall-large.png)

![image du modèle eightbuttons-lastthreesmall Medium sizedefinition.](images/overviews/sizedefinition-eightbuttons-lastthreesmall-medium.png)

![image du modèle eightbuttons-lastthreesmall Small sizedefinition.](images/overviews/sizedefinition-eightbuttons-lastthreesmall-small.png)

<span data-ttu-id="9b03a-206">EightButtons-LastThreeSmall</span><span class="sxs-lookup"><span data-stu-id="9b03a-206">EightButtons-LastThreeSmall</span></span>

<span data-ttu-id="9b03a-207">Huit contrôles de la famille de boutons (autre présentation).</span><span class="sxs-lookup"><span data-stu-id="9b03a-207">Eight button-family controls (alternate presentation).</span></span><br/>

> [!Note]  
> <span data-ttu-id="9b03a-208">Tous les éléments de contrôle déclarés avec ce modèle doivent être contenus dans deux éléments [**ControlGroup**](windowsribbon-element-controlgroup.md) : un pour les cinq premiers éléments et un pour les trois derniers éléments.</span><span class="sxs-lookup"><span data-stu-id="9b03a-208">All control elements declared with this template must be contained in two [**ControlGroup**](windowsribbon-element-controlgroup.md) elements: one for the first five elements and one for the last three elements.</span></span>

<br/> <span data-ttu-id="9b03a-209">L’exemple suivant illustre le balisage requis pour ce modèle.</span><span class="sxs-lookup"><span data-stu-id="9b03a-209">The following example demonstrates the markup required for this template.</span></span><br/>

```
<Group CommandName="cmdSizeDefinitionsGroup" 
       SizeDefinition="EightButtons-LastThreeSmall">
  <ControlGroup>
    <Button CommandName="cmdSDButton1" />
    <Button CommandName="cmdSDButton2" />
    <Button CommandName="cmdSDButton3" />
    <Button CommandName="cmdSDButton4" />
    <Button CommandName="cmdSDButton5" />
  </ControlGroup>
  <ControlGroup>
    <Button CommandName="cmdSDButton6" />
    <Button CommandName="cmdSDButton7" />
    <Button CommandName="cmdSDButton8" />
  </ControlGroup>
</Group>
```



![image du modèle eightbuttons large sizedefinition.](images/overviews/sizedefinition-eightbuttons-large.png)

![image du modèle eightbuttons Medium sizedefinition.](images/overviews/sizedefinition-eightbuttons-medium.png)

![image du modèle eightbuttons Small sizedefinition.](images/overviews/sizedefinition-eightbuttons-small.png)

<span data-ttu-id="9b03a-213">NineButtons</span><span class="sxs-lookup"><span data-stu-id="9b03a-213">NineButtons</span></span>

<span data-ttu-id="9b03a-214">Neuf contrôles de la famille de boutons.</span><span class="sxs-lookup"><span data-stu-id="9b03a-214">Nine button-family controls.</span></span>

![image du modèle ninebuttons large sizedefinition.](images/overviews/sizedefinition-ninebuttons-large.png)

![image du modèle ninebuttons Medium sizedefinition.](images/overviews/sizedefinition-ninebuttons-medium.png)

![image du modèle ninebuttons Small sizedefinition.](images/overviews/sizedefinition-ninebuttons-small.png)

<span data-ttu-id="9b03a-218">TenButtons</span><span class="sxs-lookup"><span data-stu-id="9b03a-218">TenButtons</span></span>

<span data-ttu-id="9b03a-219">Dix contrôles de la famille de boutons.</span><span class="sxs-lookup"><span data-stu-id="9b03a-219">Ten button-family controls.</span></span>

![image du modèle tenbuttons large sizedefinition.](images/overviews/sizedefinition-tenbuttons-large.png)

![image du modèle tenbuttons Medium sizedefinition.](images/overviews/sizedefinition-tenbuttons-medium.png)

![image du modèle tenbuttons Small sizedefinition.](images/overviews/sizedefinition-tenbuttons-small.png)

<span data-ttu-id="9b03a-223">ElevenButtons</span><span class="sxs-lookup"><span data-stu-id="9b03a-223">ElevenButtons</span></span>

<span data-ttu-id="9b03a-224">Onze contrôles de la famille de boutons.</span><span class="sxs-lookup"><span data-stu-id="9b03a-224">Eleven button-family controls.</span></span>

![image du modèle elevenbuttons large sizedefinition.](images/overviews/sizedefinition-elevenbuttons-large.png)

![image du modèle elevenbuttons Medium sizedefinition.](images/overviews/sizedefinition-elevenbuttons-medium.png)

![image du modèle elevenbuttons Small sizedefinition.](images/overviews/sizedefinition-elevenbuttons-small.png)

<span data-ttu-id="9b03a-228">OneFontControl</span><span class="sxs-lookup"><span data-stu-id="9b03a-228">OneFontControl</span></span>

<span data-ttu-id="9b03a-229">Un [**FontControl**](windowsribbon-element-fontcontrol.md).</span><span class="sxs-lookup"><span data-stu-id="9b03a-229">One [**FontControl**](windowsribbon-element-fontcontrol.md).</span></span>

<span data-ttu-id="9b03a-230">Seules les tailles de groupe de taille moyenne et moyenne sont prises en charge.</span><span class="sxs-lookup"><span data-stu-id="9b03a-230">Only Large and Medium group sizes are supported.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="9b03a-231">L’inclusion d’un [**FontControl**](windowsribbon-element-fontcontrol.md) dans une définition de modèle personnalisé n’est pas prise en charge par l’infrastructure.</span><span class="sxs-lookup"><span data-stu-id="9b03a-231">Including a [**FontControl**](windowsribbon-element-fontcontrol.md) within a custom template definition is not supported by the framework.</span></span>

 

![image du modèle onefontcontrol large sizedefinition.](images/overviews/sizedefinition-onefontcontrol-large.png)

![image du modèle onefontcontrol Medium sizedefinition.](images/overviews/sizedefinition-onefontcontrol-medium.png)

<span data-ttu-id="9b03a-234">OneInRibbonGallery</span><span class="sxs-lookup"><span data-stu-id="9b03a-234">OneInRibbonGallery</span></span>

<span data-ttu-id="9b03a-235">Un contrôle [**InRibbonGallery**](windowsribbon-element-inribbongallery.md) .</span><span class="sxs-lookup"><span data-stu-id="9b03a-235">One [**InRibbonGallery**](windowsribbon-element-inribbongallery.md) control.</span></span>

<span data-ttu-id="9b03a-236">Seules les tailles de groupe de grande et de petite taille sont prises en charge.</span><span class="sxs-lookup"><span data-stu-id="9b03a-236">Only Large and Small group sizes are supported.</span></span>

![image du modèle oneinribbongallery large sizedefinition.](images/overviews/sizedefinition-oneinribbongallery-large.png)

![image du modèle oneinribbongallery Small sizedefinition.](images/overviews/sizedefinition-oneinribbongallery-small.png)

<span data-ttu-id="9b03a-239">InRibbonGalleryAndBigButton</span><span class="sxs-lookup"><span data-stu-id="9b03a-239">InRibbonGalleryAndBigButton</span></span>

<span data-ttu-id="9b03a-240">Un contrôle [**InRibbonGallery**](windowsribbon-element-inribbongallery.md) et un contrôle de famille de boutons.</span><span class="sxs-lookup"><span data-stu-id="9b03a-240">One [**InRibbonGallery**](windowsribbon-element-inribbongallery.md) control and a button-family control.</span></span>

<span data-ttu-id="9b03a-241">Seules les tailles de groupe de grande et de petite taille sont prises en charge.</span><span class="sxs-lookup"><span data-stu-id="9b03a-241">Only Large and Small group sizes are supported.</span></span>

![image du modèle inribbongalleryandbigbutton large sizedefinition.](images/overviews/sizedefinition-inribbongalleryandbigbutton-large.png)

![image du modèle inribbongalleryandbigbutton Small sizedefinition.](images/overviews/sizedefinition-inribbongalleryandbigbutton-small.png)

<span data-ttu-id="9b03a-244">InRibbonGalleryAndButtons-GalleryScalesFirst</span><span class="sxs-lookup"><span data-stu-id="9b03a-244">InRibbonGalleryAndButtons-GalleryScalesFirst</span></span>

<span data-ttu-id="9b03a-245">Un contrôle [de galerie dans le ruban](windowsribbon-controls-inribbongallery.md) et deux ou trois contrôles de la famille de boutons.</span><span class="sxs-lookup"><span data-stu-id="9b03a-245">One [In-Ribbon Gallery](windowsribbon-controls-inribbongallery.md) control and two or three button-family controls.</span></span>

<span data-ttu-id="9b03a-246">La Galerie est réduite à une représentation contextuelle dans des tailles de groupes de taille moyenne et petite.</span><span class="sxs-lookup"><span data-stu-id="9b03a-246">The gallery collapses to Popup representation in Medium and Small group sizes.</span></span>

![image du modèle de grand sizedefinition inribbongalleryandbuttons-galleryscalesfirst.](images/overviews/sizedefinition-inribbongalleryandbuttons-galleryscalesfirst-large.png)

![image du modèle inribbongalleryandbuttons-galleryscalesfirst Medium sizedefinition.](images/overviews/sizedefinition-inribbongalleryandbuttons-galleryscalesfirst-medium.png)

![image du modèle inribbongalleryandbuttons-galleryscalesfirst Small sizedefinition.](images/overviews/sizedefinition-inribbongalleryandbuttons-galleryscalesfirst-small.png)

<span data-ttu-id="9b03a-250">ButtonGroups</span><span class="sxs-lookup"><span data-stu-id="9b03a-250">ButtonGroups</span></span>

<span data-ttu-id="9b03a-251">Disposition complexe des contrôles de famille de boutons 32 (la plupart sont facultatifs).</span><span class="sxs-lookup"><span data-stu-id="9b03a-251">A complex arrangement of 32 button-family controls (most of which are optional).</span></span>

> [!Note]  
> <span data-ttu-id="9b03a-252">À part le bouton en pleine taille facultatif du modèle ButtonGroups de grande taille, tous les éléments de contrôle déclarés avec ce modèle doivent être contenus dans les éléments [**ControlGroup**](windowsribbon-element-controlgroup.md) .</span><span class="sxs-lookup"><span data-stu-id="9b03a-252">Aside from the optional full-sized button of the large ButtonGroups template, all control elements declared with this template must be contained in [**ControlGroup**](windowsribbon-element-controlgroup.md) elements.</span></span>

 

<span data-ttu-id="9b03a-253">L’exemple suivant illustre le balisage requis pour afficher tous les éléments de contrôle 32 (obligatoires et facultatifs) avec ce modèle.</span><span class="sxs-lookup"><span data-stu-id="9b03a-253">The following example demonstrates the markup required to display all 32 control elements (required and optional) with this template.</span></span>


```
<Group CommandName="cmdSizeDefinitionsGroup"
       SizeDefinition="ButtonGroups">
  <!-- Row 1 -->
  <ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton1" />
      <Button CommandName="cmdSDButton2" />
      <Button CommandName="cmdSDButton3" />
      <Button CommandName="cmdSDButton4" />
      <Button CommandName="cmdSDButton5" />
      <Button CommandName="cmdSDButton6" />
      <Button CommandName="cmdSDButton7" />
      <Button CommandName="cmdSDButton8" />
      <Button CommandName="cmdSDButton9" />
      <Button CommandName="cmdSDButton10" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton11" />
      <Button CommandName="cmdSDButton12" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton13" />
      <Button CommandName="cmdSDButton14" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton15" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton16" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton17" />
      <Button CommandName="cmdSDButton18" />
    </ControlGroup>
  </ControlGroup>
  <!-- Row 2 -->
  <ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton19" />
      <Button CommandName="cmdSDButton20" />
      <Button CommandName="cmdSDButton21" />
      <Button CommandName="cmdSDButton22" />
      <Button CommandName="cmdSDButton23" />
      <Button CommandName="cmdSDButton24" />
      <Button CommandName="cmdSDButton25" />
      <Button CommandName="cmdSDButton26" />
      <Button CommandName="cmdSDButton27" />
      <Button CommandName="cmdSDButton28" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton29" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton30" />
      <Button CommandName="cmdSDButton31" />
    </ControlGroup>
  </ControlGroup>
  <Button CommandName="cmdSDButton32" />            
</Group>
```



![image du modèle ButtonGroups large sizedefinition.](images/overviews/sizedefinition-buttongroups-large.png)

![image du modèle ButtonGroups Medium sizedefinition.](images/overviews/sizedefinition-buttongroups-medium.png)

![image du modèle ButtonGroups Small sizedefinition.](images/overviews/sizedefinition-buttongroups-small.png)

<span data-ttu-id="9b03a-257">ButtonGroupsAndInputs</span><span class="sxs-lookup"><span data-stu-id="9b03a-257">ButtonGroupsAndInputs</span></span>

<span data-ttu-id="9b03a-258">Deux contrôles de la famille d’entrée (le second est facultatif) suivis d’une disposition complexe de 29 contrôles de famille de boutons (la plupart sont facultatifs).</span><span class="sxs-lookup"><span data-stu-id="9b03a-258">Two input-family controls (the second is optional) followed by a complex arrangement of 29 button-family controls (most of which are optional).</span></span>

<span data-ttu-id="9b03a-259">Seules les tailles de groupe de taille moyenne et moyenne sont prises en charge.</span><span class="sxs-lookup"><span data-stu-id="9b03a-259">Only Large and Medium group sizes are supported.</span></span>

> [!Note]  
> <span data-ttu-id="9b03a-260">Tous les éléments de contrôle déclarés avec ce modèle doivent être contenus dans les éléments [**ControlGroup**](windowsribbon-element-controlgroup.md) .</span><span class="sxs-lookup"><span data-stu-id="9b03a-260">All control elements declared with this template must be contained in [**ControlGroup**](windowsribbon-element-controlgroup.md) elements.</span></span>

 

<span data-ttu-id="9b03a-261">L’exemple suivant illustre le balisage requis pour afficher tous les éléments de contrôle (obligatoires et facultatifs) avec ce modèle.</span><span class="sxs-lookup"><span data-stu-id="9b03a-261">The following example demonstrates the markup required to display all control elements (required and optional) with this template.</span></span>


```
<Group CommandName="cmdSizeDefinitionsGroup" 
       SizeDefinition="ButtonGroupsAndInputs">
  <!-- Row 1 -->
  <ControlGroup>
    <ControlGroup>
      <ComboBox CommandName="cmdSDComboBox" />
      <Spinner CommandName="cmdSDSpinner" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton1" />
      <Button CommandName="cmdSDButton2" />
      <Button CommandName="cmdSDButton3" />
      <Button CommandName="cmdSDButton4" />
      <Button CommandName="cmdSDButton5" />
      <Button CommandName="cmdSDButton6" />
      <Button CommandName="cmdSDButton7" />
      <Button CommandName="cmdSDButton8" />
      <Button CommandName="cmdSDButton9" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton10" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton11" />
      <Button CommandName="cmdSDButton12" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton13" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton14" />
    </ControlGroup>
  </ControlGroup>
  <!-- Row 2 -->  
  <ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton15" />
      <Button CommandName="cmdSDButton16" />
      <Button CommandName="cmdSDButton17" />
      <Button CommandName="cmdSDButton18" />
      <Button CommandName="cmdSDButton19" />
      <Button CommandName="cmdSDButton20" />
      <Button CommandName="cmdSDButton21" />
      <Button CommandName="cmdSDButton22" />
      <Button CommandName="cmdSDButton23" />
      <Button CommandName="cmdSDButton24" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton25" />
      <Button CommandName="cmdSDButton26" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton27" />
      <Button CommandName="cmdSDButton28" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton29" />
    </ControlGroup>
  </ControlGroup>
</Group>
```



![image du modèle buttongroupsandinputs large sizedefinition.](images/overviews/sizedefinition-buttongroupsandinputs-large.png)

![image du modèle buttongroupsandinputs Medium sizedefinition.](images/overviews/sizedefinition-buttongroupsandinputs-medium.png)

<span data-ttu-id="9b03a-264">BigButtonsAndSmallButtonsOrInputs</span><span class="sxs-lookup"><span data-stu-id="9b03a-264">BigButtonsAndSmallButtonsOrInputs</span></span>

<span data-ttu-id="9b03a-265">Deux contrôles de famille de boutons (à la fois facultatifs) suivis de deux ou trois contrôles Button ou Family.</span><span class="sxs-lookup"><span data-stu-id="9b03a-265">Two button-family controls (both optional) followed by two or three button or input-family controls.</span></span>

<span data-ttu-id="9b03a-266">Seules les tailles de groupe de taille moyenne et moyenne sont prises en charge.</span><span class="sxs-lookup"><span data-stu-id="9b03a-266">Only Large and Medium group sizes are supported.</span></span>

![image du modèle bigbuttonsandsmallbuttonsorinputs large sizedefinition.](images/overviews/sizedefinition-bigbuttonsandsmallbuttonsorinputs-large.png)

![image du modèle bigbuttonsandsmallbuttonsorinputs Medium sizedefinition.](images/overviews/sizedefinition-bigbuttonsandsmallbuttonsorinputs-medium.png)



 

### <a name="basic-sizedefinition-example"></a><span data-ttu-id="9b03a-269">Exemple de SizeDefinition de base</span><span class="sxs-lookup"><span data-stu-id="9b03a-269">Basic SizeDefinition Example</span></span>

<span data-ttu-id="9b03a-270">L’exemple de code suivant fournit une démonstration de base sur la façon de déclarer un modèle [**SizeDefinition**](windowsribbon-element-sizedefinition.md) dans le balisage du ruban.</span><span class="sxs-lookup"><span data-stu-id="9b03a-270">The following code example provides a basic demonstration of how to declare a [**SizeDefinition**](windowsribbon-element-sizedefinition.md) template in Ribbon markup.</span></span>

<span data-ttu-id="9b03a-271">L' *OneInRibbonGallery* [**SizeDefinition**](windowsribbon-element-sizedefinition.md) est utilisé pour cet exemple particulier, mais tous les modèles d’infrastructure sont spécifiés de manière similaire.</span><span class="sxs-lookup"><span data-stu-id="9b03a-271">The *OneInRibbonGallery* [**SizeDefinition**](windowsribbon-element-sizedefinition.md) is used for this particular example, but all framework templates are specified in a similar fashion.</span></span>


```XML
<!-- InRibbonGallery -->
<Group CommandName="cmdInRibbonGalleryGroup" SizeDefinition="OneInRibbonGallery">
  <InRibbonGallery CommandName="cmdInRibbonGallery"
                   MaxColumns="10"
                   MaxColumnsMedium="5"
                   MinColumnsLarge="5"
                   MinColumnsMedium="3"
                   Type="Items">
    <InRibbonGallery.MenuLayout>
      <VerticalMenuLayout Rows="2"
                          Gripper="Vertical"/>
    </InRibbonGallery.MenuLayout>
    <InRibbonGallery.MenuGroups>
      <MenuGroup>
        <Button CommandName="cmdButton1"></Button>
        <Button CommandName="cmdButton2"></Button>
      </MenuGroup>
      <MenuGroup>
        <Button CommandName="cmdButton3"></Button>
      </MenuGroup>
    </InRibbonGallery.MenuGroups>            
  </InRibbonGallery>
</Group>
```



### <a name="complex-sizedefinition-example-with-scaling-policies"></a><span data-ttu-id="9b03a-272">Exemple de SizeDefinition complexe avec des stratégies de mise à l’échelle</span><span class="sxs-lookup"><span data-stu-id="9b03a-272">Complex SizeDefinition Example with Scaling Policies</span></span>

<span data-ttu-id="9b03a-273">Le comportement de réduction des modèles [**SizeDefinition**](windowsribbon-element-sizedefinition.md) peut être contrôlé à l’aide de stratégies de mise à l’échelle dans le balisage du ruban.</span><span class="sxs-lookup"><span data-stu-id="9b03a-273">The collapsing behavior of [**SizeDefinition**](windowsribbon-element-sizedefinition.md) templates can be controlled through the use of scaling policies in the Ribbon markup.</span></span>

<span data-ttu-id="9b03a-274">L’élément [**ScalingPolicy**](windowsribbon-element-scalingpolicy.md) contient un manifeste de [**ScalingPolicy. IdealSizes**](windowsribbon-element-scalingpolicy-idealsizes.md) et des déclarations de mise à l' [**échelle**](windowsribbon-element-scale.md) qui spécifient des préférences de disposition adaptative pour un ou plusieurs éléments de [**groupe**](windowsribbon-element-group.md) lorsque le ruban est redimensionné.</span><span class="sxs-lookup"><span data-stu-id="9b03a-274">The [**ScalingPolicy**](windowsribbon-element-scalingpolicy.md) element contains a manifest of [**ScalingPolicy.IdealSizes**](windowsribbon-element-scalingpolicy-idealsizes.md) and [**Scale**](windowsribbon-element-scale.md) declarations that specify adaptive layout preferences for one or more [**Group**](windowsribbon-element-group.md) elements when the Ribbon is resized.</span></span>

> [!Note]  
> <span data-ttu-id="9b03a-275">Il est fortement recommandé de spécifier des détails de stratégie de mise à l’échelle adéquats de sorte que la plupart des éléments de [**groupe**](windowsribbon-element-group.md) soient associés à un élément d' [**échelle**](windowsribbon-element-scale.md) où l’attribut de *taille* est égal à `Popup` .</span><span class="sxs-lookup"><span data-stu-id="9b03a-275">It is highly recommended that adequate scaling policy detail be specified such that most, if not all, [**Group**](windowsribbon-element-group.md) elements are associated with a [**Scale**](windowsribbon-element-scale.md) element where the *Size* attribute is equal to `Popup`.</span></span> <span data-ttu-id="9b03a-276">Cela permet à l’infrastructure d’afficher le ruban à la plus petite taille possible et de prendre en charge la plus large gamme de périphériques d’affichage, avant d’introduire automatiquement un mécanisme de défilement.</span><span class="sxs-lookup"><span data-stu-id="9b03a-276">Doing so allows the framework to render the ribbon at the smallest size possible, and support the broadest range of display devices, before automatically introducing a scrolling mechanism.</span></span>

 

<span data-ttu-id="9b03a-277">L’exemple de code suivant montre un manifeste [**ScalingPolicy**](windowsribbon-element-scalingpolicy.md) qui spécifie une préférence [**ScalingPolicy. IdealSizes**](windowsribbon-element-scalingpolicy-idealsizes.md) [**SizeDefinition**](windowsribbon-element-sizedefinition.md) pour chacun des quatre groupes de contrôles sur un onglet de **démarrage** . En outre, les éléments de mise à l' [**échelle**](windowsribbon-element-scale.md) sont spécifiés pour influencer le comportement de réduction, dans l’ordre de la taille décroissant, de chaque groupe.</span><span class="sxs-lookup"><span data-stu-id="9b03a-277">The following code example demonstrates a [**ScalingPolicy**](windowsribbon-element-scalingpolicy.md) manifest that specifies a [**ScalingPolicy.IdealSizes**](windowsribbon-element-scalingpolicy-idealsizes.md) [**SizeDefinition**](windowsribbon-element-sizedefinition.md) preference for each of four groups of controls on a **Home** tab. In addition, [**Scale**](windowsribbon-element-scale.md) elements are specified to influence the collapsing behavior, in descending size order, of each group.</span></span>


```C++
<Tab CommandName="Home">
  <Tab.ScalingPolicy>
    <ScalingPolicy>
      <ScalingPolicy.IdealSizes>
        <Scale Group="GroupClipboard" Size="Medium"/>
        <Scale Group="GroupView" Size="Large"/>
        <Scale Group="GroupFont" Size="Large"/>
        <Scale Group="GroupParagraph" Size="Large"/>
      </ScalingPolicy.IdealSizes>
      <Scale Group="GroupClipboard" Size="Small"/>
      <Scale Group="GroupClipboard" Size="Popup"/>
      <Scale Group="GroupFont" Size="Medium"/>
      <Scale Group="GroupFont" Size="Popup"/>
      <Scale Group="GroupParagraph" Size="Medium"/>
      <Scale Group="GroupParagraph" Size="Popup"/>
      <!-- 
        GroupView group is associated with the OneButton SizeDefinition.
        Since this template is constrained to one size (Large) there
        is no need to declare further scaling preferences.
      -->
    </ScalingPolicy>
  </Tab.ScalingPolicy>

  <Group CommandName="GroupClipboard" SizeDefinition="FourButtons">
    <Button CommandName="Paste"/>
    <Button CommandName="Cut"/>
    <Button CommandName="Copy"/>
    <Button CommandName="SelectAll"/>
  </Group>

  <Group CommandName="GroupFont"  ApplicationModes="1">
    <FontControl CommandName="Font" FontType="FontWithColor" />
  </Group>

  <Group CommandName="GroupParagraph"  ApplicationModes="1" SizeDefinition="ButtonGroups">
    <ControlGroup>
      <ControlGroup>
        <ToggleButton CommandName="Numbered" />
        <ToggleButton CommandName="Bulleted" />
      </ControlGroup>
    </ControlGroup>
    <ControlGroup>
      <ControlGroup>
        <ToggleButton CommandName="LeftJustify" />
        <ToggleButton CommandName="CenterJustify" />
        <ToggleButton CommandName="RightJustify" />
      </ControlGroup>
      <ControlGroup/>
      <ControlGroup>
        <Button CommandName="Outdent" />
        <Button CommandName="Indent" />
      </ControlGroup>
    </ControlGroup>
  </Group>

  <Group CommandName="GroupView" SizeDefinition="OneButton" >
    <ToggleButton CommandName="ViewSource"/>
  </Group>

</Tab>
```



### <a name="custom-templates"></a><span data-ttu-id="9b03a-278">Modèles personnalisés</span><span class="sxs-lookup"><span data-stu-id="9b03a-278">Custom Templates</span></span>

<span data-ttu-id="9b03a-279">Si les comportements de disposition par défaut et les modèles [**SizeDefinition**](windowsribbon-element-sizedefinition.md) prédéfinis n’offrent pas la flexibilité ou la prise en charge d’un scénario de disposition particulier, les modèles personnalisés sont pris en charge par l’infrastructure du ruban via l’élément [**Ribbon. SizeDefinitions**](windowsribbon-element-ribbon-sizedefinitions.md) .</span><span class="sxs-lookup"><span data-stu-id="9b03a-279">If the default layout behaviors and the predefined [**SizeDefinition**](windowsribbon-element-sizedefinition.md) templates do not offer the flexibility or support for a particular layout scenario, custom templates are supported by the Ribbon framework through the [**Ribbon.SizeDefinitions**](windowsribbon-element-ribbon-sizedefinitions.md) element.</span></span>

<span data-ttu-id="9b03a-280">Les modèles personnalisés peuvent être déclarés de deux façons : une méthode autonome à l’aide de l’élément [**Ribbon. SizeDefinitions**](windowsribbon-element-ribbon-sizedefinitions.md) pour la déclaration de modèles réutilisables, nommés ou une méthode Inline spécifique à un [**groupe**](windowsribbon-element-group.md).</span><span class="sxs-lookup"><span data-stu-id="9b03a-280">Custom templates can be declared in two ways: a standalone method using the [**Ribbon.SizeDefinitions**](windowsribbon-element-ribbon-sizedefinitions.md) element for declaring reusable, named templates or an inline method that is [**Group**](windowsribbon-element-group.md)-specific.</span></span>

### <a name="standalone-template"></a><span data-ttu-id="9b03a-281">Modèle autonome</span><span class="sxs-lookup"><span data-stu-id="9b03a-281">Standalone Template</span></span>

<span data-ttu-id="9b03a-282">L’exemple de code suivant illustre un modèle personnalisé de base, réutilisable.</span><span class="sxs-lookup"><span data-stu-id="9b03a-282">The following code example illustrates a basic, reusable custom template.</span></span>


```
<Ribbon.SizeDefinitions>
  <SizeDefinition Name="CustomTemplate">
    <GroupSizeDefinition Size="Large">
      <ControlSizeDefinition ImageSize="Large" IsLabelVisible="true" />
    </GroupSizeDefinition>
    <GroupSizeDefinition Size="Medium">
      <ControlSizeDefinition ImageSize="Small" IsLabelVisible="false" />
    </GroupSizeDefinition>
    <GroupSizeDefinition Size="Small">
      <ControlSizeDefinition ImageSize="Small" IsLabelVisible="false" />
    </GroupSizeDefinition>
  </SizeDefinition>
</Ribbon.SizeDefinitions>
```



### <a name="inline-template"></a><span data-ttu-id="9b03a-283">Modèle Inline</span><span class="sxs-lookup"><span data-stu-id="9b03a-283">Inline Template</span></span>

<span data-ttu-id="9b03a-284">Les exemples de code suivants illustrent un modèle personnalisé inline de base pour un groupe de quatre boutons.</span><span class="sxs-lookup"><span data-stu-id="9b03a-284">The following code examples illustrate a basic inline custom template for a group of four buttons.</span></span>

<span data-ttu-id="9b03a-285">Cette section de code montre les déclarations de commande pour un groupe de boutons.</span><span class="sxs-lookup"><span data-stu-id="9b03a-285">This section of code shows the Command declarations for a group of buttons.</span></span> <span data-ttu-id="9b03a-286">Les grandes et les petites ressources d’images sont également spécifiées ici.</span><span class="sxs-lookup"><span data-stu-id="9b03a-286">Large and small image resources are also specified here.</span></span>


```XML
<!-- Button -->
<Command Name="cmdButtonGroup"
         Symbol="cmdButtonGroup"
         Comment="Button Group"
         LabelTitle="ButtonGroup"/>
<Command Name="cmdButton1"
         Symbol="cmdButton1"
         Comment="Button1"
         LabelTitle="Button1"/>
<Command Name="cmdButton2"
         Symbol="cmdButton2"
         Comment="Button2"
         LabelTitle="Button2"/>
<Command Name="cmdButton3"
         Symbol="cmdButton3"
         Comment="Button3"
         LabelTitle="Button3"/>
<Command Name="cmdButtonGroup2"
         Symbol="cmdButtonGroup2"
         Comment="Button Group2"
         LabelTitle="ButtonGroup2"/>
<Command Name="cmdButtonG21"
         Symbol="cmdButtonG21"
         Comment="ButtonG21"
         LabelTitle="ButtonG21">
  <Command.LargeImages>
    <Image Source="res/large.bmp"/>
  </Command.LargeImages>
  <Command.SmallImages>
    <Image Source="res/small.bmp"/>
  </Command.SmallImages>
</Command>
<Command Name="cmdButtonG22"
         Symbol="cmdButtonG22"
         Comment="ButtonG22"
         LabelTitle="ButtonG22">
  <Command.LargeImages>
    <Image Source="res/large.bmp"/>
  </Command.LargeImages>
  <Command.SmallImages>
    <Image Source="res/small.bmp"/>
  </Command.SmallImages>
</Command>
<Command Name="cmdButtonG23"
         Symbol="cmdButtonG23"
         Comment="ButtonG23"
         LabelTitle="ButtonG23">
  <Command.LargeImages>
    <Image Source="res/large.bmp"/>
  </Command.LargeImages>
  <Command.SmallImages>
    <Image Source="res/small.bmp"/>
  </Command.SmallImages>
</Command>
<Command Name="cmdButtonG24"
         Symbol="cmdButtonG24"
         Comment="ButtonG24"
         LabelTitle="ButtonG24">
  <Command.LargeImages>
    <Image Source="res/large.bmp"/>
  </Command.LargeImages>
  <Command.SmallImages>
    <Image Source="res/small.bmp"/>
  </Command.SmallImages>
</Command>
```



<span data-ttu-id="9b03a-287">Cette section de code montre comment définir des modèles [**GroupSizeDefinition**](windowsribbon-element-groupsizedefinition.md) volumineux, moyens et petits pour afficher les quatre boutons à différentes tailles et dispositions.</span><span class="sxs-lookup"><span data-stu-id="9b03a-287">This section of code demonstrates how to define large, medium, and small [**GroupSizeDefinition**](windowsribbon-element-groupsizedefinition.md) templates to display the four buttons at various sizes and layouts.</span></span> <span data-ttu-id="9b03a-288">La Déclaration [**ScalingPolicy**](windowsribbon-element-scalingpolicy.md) pour l’onglet définit le modèle utilisé pour un groupe de contrôles en fonction de la taille du ruban et de l’espace requis par l’onglet actif.</span><span class="sxs-lookup"><span data-stu-id="9b03a-288">The [**ScalingPolicy**](windowsribbon-element-scalingpolicy.md) declaration for the tab defines which template is used for a group of controls based on the ribbon size and space required by the active tab.</span></span>


```XML
        <Tab CommandName="cmdTab6">
          <Tab.ScalingPolicy>
            <ScalingPolicy>
              <ScalingPolicy.IdealSizes>
                <Scale Group="cmdButtonGroup"
                       Size="Large"/>
                <Scale Group="cmdButtonGroup2"
                       Size="Large"/>
                <Scale Group="cmdToggleButtonGroup"
                       Size="Large"/>
              </ScalingPolicy.IdealSizes>
              <Scale Group="cmdButtonGroup"
                     Size="Medium"/>
              <Scale Group="cmdButtonGroup2"
                     Size="Medium"/>
              <Scale Group="cmdButtonGroup2"
                     Size="Small"/>
              <Scale Group="cmdButtonGroup2"
                     Size="Popup"/>
            </ScalingPolicy>
          </Tab.ScalingPolicy>

          <Group CommandName="cmdButtonGroup2">
            <SizeDefinition>
              <ControlNameMap>
                <ControlNameDefinition Name="button1"/>
                <ControlNameDefinition Name="button2"/>
                <ControlNameDefinition Name="button3"/>
                <ControlNameDefinition Name="button4"/>
              </ControlNameMap>
              <GroupSizeDefinition Size="Large">
                <ControlGroup>
                  <ControlSizeDefinition ControlName="button1"
                                         ImageSize="Large"
                                         IsLabelVisible="true" />
                  <ControlSizeDefinition ControlName="button2"
                                         ImageSize="Large"
                                         IsLabelVisible="true" />
                </ControlGroup>
                <ColumnBreak ShowSeparator="true"/>
                <ControlGroup>
                  <ControlSizeDefinition ControlName="button3"
                                         ImageSize="Large"
                                        IsLabelVisible="true" />
                  <ControlSizeDefinition ControlName="button4"
                                        ImageSize="Large"
                                        IsLabelVisible="true" />
                </ControlGroup>
              </GroupSizeDefinition>
              <GroupSizeDefinition Size="Medium">
                <Row>
                  <ControlSizeDefinition ControlName="button1"
                                         ImageSize="Small"
                                         IsLabelVisible="true" />
                  <ControlSizeDefinition ControlName="button3"
                                         ImageSize="Small"
                                         IsLabelVisible="true" />
                </Row>
                <Row>
                  <ControlSizeDefinition ControlName="button2"
                                         ImageSize="Small"
                                         IsLabelVisible="true" />
                  <ControlSizeDefinition ControlName="button4"
                                         ImageSize="Small"
                                         IsLabelVisible="true" />
                </Row>
              </GroupSizeDefinition>
              <GroupSizeDefinition Size="Small">
                <Row>
                  <ControlSizeDefinition ControlName="button1"
                                         ImageSize="Small"
                                         IsLabelVisible="true" />
                  <ControlSizeDefinition ControlName="button3"
                                         ImageSize="Small"
                                         IsLabelVisible="false" />
                </Row>
                <Row>
                  <ControlSizeDefinition ControlName="button2"
                                         ImageSize="Small"
                                         IsLabelVisible="true" />
                  <ControlSizeDefinition ControlName="button4"
                                         ImageSize="Small"
                                         IsLabelVisible="false" />
                </Row>
              </GroupSizeDefinition>
            </SizeDefinition>
            <Button CommandName="cmdButtonG21"></Button>
            <Button CommandName="cmdButtonG22"></Button>
            <Button CommandName="cmdButtonG23"></Button>
            <Button CommandName="cmdButtonG24"></Button>
          </Group>
          <Group CommandName="cmdCheckBoxGroup">
            <CheckBox CommandName="cmdCheckBox"></CheckBox>
          </Group>
          <Group CommandName="cmdToggleButtonGroup"
                 SizeDefinition="OneButton">
            <ToggleButton CommandName="cmdToggleButton"></ToggleButton>
          </Group>
          <Group CommandName="cmdButtonGroup"
                 SizeDefinition="ThreeButtons">
            <Button CommandName="cmdButton1"></Button>
            <Button CommandName="cmdButton2"></Button>
            <Button CommandName="cmdButton3"></Button>
          </Group>
        </Tab>
```



<span data-ttu-id="9b03a-289">Les images suivantes montrent comment les modèles de l’exemple précédent sont appliqués à l’interface ruban pour s’adapter à une diminution de la taille du ruban.</span><span class="sxs-lookup"><span data-stu-id="9b03a-289">The following images show how the templates from the previous example are applied to the ribbon UI to accommodate a decrease in ribbon size.</span></span>



|        |                                                                                                    |
|--------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9b03a-290">Grande</span><span class="sxs-lookup"><span data-stu-id="9b03a-290">Large</span></span>  | ![image d’un modèle personnalisé de grande taille en ligne.](images/overviews/sizedefinition-custom-large.png)   |
| <span data-ttu-id="9b03a-292">Moyenne</span><span class="sxs-lookup"><span data-stu-id="9b03a-292">Medium</span></span> | ![image d’un modèle personnalisé de moyenne en ligne.](images/overviews/sizedefinition-custom-medium.png) |
| <span data-ttu-id="9b03a-294">Petite</span><span class="sxs-lookup"><span data-stu-id="9b03a-294">Small</span></span>  | ![image d’un petit modèle personnalisé en ligne.](images/overviews/sizedefinition-custom-small.png)   |
| <span data-ttu-id="9b03a-296">Fenêtre contextuelle</span><span class="sxs-lookup"><span data-stu-id="9b03a-296">Popup</span></span>  | ![image d’un modèle personnalisé contextuelle en ligne.](images/overviews/sizedefinition-custom-popup.png)   |



 

## <a name="related-topics"></a><span data-ttu-id="9b03a-298">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="9b03a-298">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9b03a-299">**SizeDefinition**</span><span class="sxs-lookup"><span data-stu-id="9b03a-299">**SizeDefinition**</span></span>](windowsribbon-element-sizedefinition.md)
</dt> <dt>

[<span data-ttu-id="9b03a-300">**Scale**</span><span class="sxs-lookup"><span data-stu-id="9b03a-300">**Scale**</span></span>](windowsribbon-element-scale.md)
</dt> <dt>

[<span data-ttu-id="9b03a-301">**Groupe**</span><span class="sxs-lookup"><span data-stu-id="9b03a-301">**Group**</span></span>](windowsribbon-element-group.md)
</dt> </dl>

 

 





