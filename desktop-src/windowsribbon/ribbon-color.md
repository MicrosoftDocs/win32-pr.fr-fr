---
title: Personnalisation des couleurs du ruban
description: L’infrastructure de ruban Windows expose un jeu de propriétés de couleur qui permettent à une application de personnaliser l’apparence de divers éléments d’interface utilisateur du ruban au moment de l’exécution.
ms.assetid: e070aaca-d350-4336-8e5d-d5d9c8167287
keywords:
- Ruban Windows, personnalisation des couleurs
- Ruban, personnalisation des couleurs
- personnalisation des couleurs du ruban Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55ff6527dc67ee18df4723fc33e4b764e20127e8
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/20/2020
ms.locfileid: "103723819"
---
# <a name="customizing-ribbon-colors"></a><span data-ttu-id="895be-106">Personnalisation des couleurs du ruban</span><span class="sxs-lookup"><span data-stu-id="895be-106">Customizing Ribbon Colors</span></span>

<span data-ttu-id="895be-107">L’infrastructure de ruban Windows expose un jeu de propriétés de couleur qui permettent à une application de personnaliser l’apparence de divers éléments d’interface utilisateur du ruban au moment de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="895be-107">The Windows Ribbon framework exposes a set of color properties that allow an application to customize the appearance of various Ribbon UI elements at run time.</span></span>

-   [<span data-ttu-id="895be-108">Introduction</span><span class="sxs-lookup"><span data-stu-id="895be-108">Introduction</span></span>](#introduction)
-   [<span data-ttu-id="895be-109">Spécifier les couleurs du ruban</span><span class="sxs-lookup"><span data-stu-id="895be-109">Specify Ribbon Colors</span></span>](#specify-ribbon-colors)
-   [<span data-ttu-id="895be-110">Convertir RVB en TSL</span><span class="sxs-lookup"><span data-stu-id="895be-110">Convert RGB to HSB</span></span>](#convert-rgb-to-hsb)
-   [<span data-ttu-id="895be-111">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="895be-111">Related topics</span></span>](#related-topics)

## <a name="introduction"></a><span data-ttu-id="895be-112">Introduction</span><span class="sxs-lookup"><span data-stu-id="895be-112">Introduction</span></span>

<span data-ttu-id="895be-113">Les [clés de propriété de Framework](windowsribbon-reference-properties-framework.md) répertoriées dans le tableau suivant sont utilisées pour définir la couleur des différents éléments d’interface utilisateur dans une application de ruban.</span><span class="sxs-lookup"><span data-stu-id="895be-113">The [framework property keys](windowsribbon-reference-properties-framework.md) listed in the following table are used to set the color of various UI elements in a Ribbon application.</span></span> <span data-ttu-id="895be-114">Ces propriétés permettent à l’infrastructure du ruban de prendre en charge les spécifications de personnalisation, d’identité et de personnalisation entre les applications.</span><span class="sxs-lookup"><span data-stu-id="895be-114">These properties allow the Ribbon framework to support personalization, identity requirements, and branding specifications across applications.</span></span>

| <span data-ttu-id="895be-115">Couleur du ruban</span><span class="sxs-lookup"><span data-stu-id="895be-115">Ribbon Color</span></span>                     | <span data-ttu-id="895be-116">Clé de propriété du Framework</span><span class="sxs-lookup"><span data-stu-id="895be-116">Framework Property Key</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|----------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="895be-117">Couleur d’arrière-plan</span><span class="sxs-lookup"><span data-stu-id="895be-117">Background color</span></span>                 | [<span data-ttu-id="895be-118">IU \_ \_ GlobalBackgroundColor</span><span class="sxs-lookup"><span data-stu-id="895be-118">UI\_PKEY\_GlobalBackgroundColor</span></span>](windowsribbon-reference-properties-uipkey-globalbackgroundcolor.md)                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="895be-119">Couleur de surbrillance (Windows 7 uniquement)</span><span class="sxs-lookup"><span data-stu-id="895be-119">Highlight color (Windows 7 only)</span></span> | <span data-ttu-id="895be-120">[Interface utilisateur \_ Le \_ ](windowsribbon-reference-properties-uipkey-globalhighlightcolor.md)jeu de GlobalHighlightColor \* \* \* \* introduit dans Windows 8 \* \* : \* \* [UI \_ \_ GlobalHighlightColor](windowsribbon-reference-properties-uipkey-globalhighlightcolor.md) ne peut pas être défini indépendamment de [l’interface utilisateur \_ \_ GlobalBackgroundColor](windowsribbon-reference-properties-uipkey-globalbackgroundcolor.md).</span><span class="sxs-lookup"><span data-stu-id="895be-120">[UI\_PKEY\_GlobalHighlightColor](windowsribbon-reference-properties-uipkey-globalhighlightcolor.md)\*\*\*\*Introduced in Windows 8\*\*:  \*\* [UI\_PKEY\_GlobalHighlightColor](windowsribbon-reference-properties-uipkey-globalhighlightcolor.md) cannot be set independently of [UI\_PKEY\_GlobalBackgroundColor](windowsribbon-reference-properties-uipkey-globalbackgroundcolor.md).</span></span><br/> <br/>                                                              |
| <span data-ttu-id="895be-121">Couleur du texte</span><span class="sxs-lookup"><span data-stu-id="895be-121">Text color</span></span>                       | <span data-ttu-id="895be-122">[Interface utilisateur \_ \_GlobalTextColor](windowsribbon-reference-properties-uipkey-globaltextcolor.md)de l’interface utilisateur \* \* \* \* introduit dans Windows 8 **:** les modifications apportées à la valeur par défaut de l' [UI « \_ \_ GlobalBackgroundColor](windowsribbon-reference-properties-uipkey-globalbackgroundcolor.md) » dans Windows 8 peuvent nécessiter un ajustement de l' [interface utilisateur de l’IU \_ \_ GlobalTextColor](windowsribbon-reference-properties-uipkey-globaltextcolor.md) dans les applications de ruban conçues pour Windows 7.</span><span class="sxs-lookup"><span data-stu-id="895be-122">[UI\_PKEY\_GlobalTextColor](windowsribbon-reference-properties-uipkey-globaltextcolor.md)\*\*\*\*Introduced in Windows 8 **:** Changes to the default value of [UI\_PKEY\_GlobalBackgroundColor](windowsribbon-reference-properties-uipkey-globalbackgroundcolor.md) in Windows 8 might require an adjustment to [UI\_PKEY\_GlobalTextColor](windowsribbon-reference-properties-uipkey-globaltextcolor.md) in Ribbon apps designed for Windows 7.</span></span><br/> <br/> |



 

## <a name="specify-ribbon-colors"></a><span data-ttu-id="895be-123">Spécifier les couleurs du ruban</span><span class="sxs-lookup"><span data-stu-id="895be-123">Specify Ribbon Colors</span></span>

<span data-ttu-id="895be-124">L’infrastructure du ruban utilise un modèle de couleurs teinte, saturation, luminosité (TSL), qui diffère des espaces de couleurs teinte, saturation, luminosité (TSL) ou teinte, saturation, valeur (HSV) les plus courants.</span><span class="sxs-lookup"><span data-stu-id="895be-124">The Ribbon framework uses a Hue, Saturation, Brightness (HSB) color model, which differs from the more common hue, saturation, luminosity (HSL) or hue, saturation, value (HSV) color spaces.</span></span> <span data-ttu-id="895be-125">En particulier, B représente un niveau de luminosité ou de luminosité global plutôt que la clarté d’une couleur particulière.</span><span class="sxs-lookup"><span data-stu-id="895be-125">In particular, B represents an overall brightness or luminosity level rather than the lightness of a particular color.</span></span>

<span data-ttu-id="895be-126">Pour spécifier la couleur des éléments d’interface utilisateur dans l’infrastructure du ruban, une application assigne des valeurs TSL à chacune des propriétés de couleur globale.</span><span class="sxs-lookup"><span data-stu-id="895be-126">To specify the color of UI elements in the Ribbon framework, an application assigns HSB values to each of the global color properties.</span></span> <span data-ttu-id="895be-127">Ces valeurs sont ensuite appliquées universellement à tous les éléments de ruban comme requis par l’application ruban (l’infrastructure ne prend pas en charge l’affectation de valeurs TSL à des éléments et des contrôles individuels).</span><span class="sxs-lookup"><span data-stu-id="895be-127">These values are then applied universally across all Ribbon elements as required by the Ribbon application (the framework does not support assigning HSB values to individual elements and controls).</span></span>

<span data-ttu-id="895be-128">Introduite dans Windows 8 \* \* : \* \*[l’UI \_ \_ GlobalHighlightColor](windowsribbon-reference-properties-uipkey-globalhighlightcolor.md) a la même valeur que [l' \_ UI \_ GlobalBackgroundColor](windowsribbon-reference-properties-uipkey-globalbackgroundcolor.md).</span><span class="sxs-lookup"><span data-stu-id="895be-128">\*\*\*\*Introduced in Windows 8\*\*:  \*\*[UI\_PKEY\_GlobalHighlightColor](windowsribbon-reference-properties-uipkey-globalhighlightcolor.md) is assigned the same value as [UI\_PKEY\_GlobalBackgroundColor](windowsribbon-reference-properties-uipkey-globalbackgroundcolor.md).</span></span>

<span data-ttu-id="895be-129">Le tableau suivant décrit les paramètres TSL de l’infrastructure du ruban.</span><span class="sxs-lookup"><span data-stu-id="895be-129">The following table describes the Ribbon framework HSB parameters.</span></span>



<span data-ttu-id="895be-130">Composant</span><span class="sxs-lookup"><span data-stu-id="895be-130">Component</span></span>

<span data-ttu-id="895be-131">Description</span><span class="sxs-lookup"><span data-stu-id="895be-131">Description</span></span>

<span data-ttu-id="895be-132">Valeurs ajustées\*</span><span class="sxs-lookup"><span data-stu-id="895be-132">Adjusted Values\*</span></span>

<span data-ttu-id="895be-133">Teinte (H)</span><span class="sxs-lookup"><span data-stu-id="895be-133">Hue (H)</span></span>

<span data-ttu-id="895be-134">Le pigment, ou la couleur réelle, est généralement identifié en tant que valeur d’une plage circlular comprise entre 0 et 359 degrés.</span><span class="sxs-lookup"><span data-stu-id="895be-134">The pigment, or actual, color is typically identified as a value from a circlular range of 0 to 359 degrees.</span></span>

<span data-ttu-id="895be-135">0 (rouge) à 255 (rouge)</span><span class="sxs-lookup"><span data-stu-id="895be-135">0 (red) to 255 (red)</span></span>

<span data-ttu-id="895be-136">Saturation (S)</span><span class="sxs-lookup"><span data-stu-id="895be-136">Saturation (S)</span></span>

<span data-ttu-id="895be-137">Pureté, ou saturation, de la couleur mesurée en pourcentage de 0 à 100%.</span><span class="sxs-lookup"><span data-stu-id="895be-137">The purity, or saturation, of the color measured as a percentage from 0 to 100%.</span></span>

<span data-ttu-id="895be-138">0 (gris) à 255 (saturé entièrement)</span><span class="sxs-lookup"><span data-stu-id="895be-138">0 (grey) to 255 (fully saturated)</span></span>

<span data-ttu-id="895be-139">Luminosité (B)</span><span class="sxs-lookup"><span data-stu-id="895be-139">Brightness (B)</span></span>

<span data-ttu-id="895be-140">Luminosité ou obscurité globale de la couleur mesurée en pourcentage de 0 à 100%.</span><span class="sxs-lookup"><span data-stu-id="895be-140">The overall brightness or darkness of the color measured as a percentage from 0 to 100%.</span></span>

<span data-ttu-id="895be-141">0 (sombre) à 255 (clair)</span><span class="sxs-lookup"><span data-stu-id="895be-141">0 (dark) to 255 (light)</span></span>

<span data-ttu-id="895be-142">\* La plage d’origine de chaque valeur de paramètre est traduite dans une plage comprise entre 0 et 255 pour le Framework.</span><span class="sxs-lookup"><span data-stu-id="895be-142">\* The original range for each parameter value is translated into a range of 0 to 255 for the framework.</span></span>



 

<span data-ttu-id="895be-143">Les valeurs TSL n’identifient pas les couleurs spécifiques.</span><span class="sxs-lookup"><span data-stu-id="895be-143">HSB values do not identify specific colors.</span></span> <span data-ttu-id="895be-144">Au lieu de cela, la combinaison des valeurs de propriété TSL influence la manière dont les dégradés de couleur dans l’interface utilisateur sont ajustés l’un par rapport à l’autre.</span><span class="sxs-lookup"><span data-stu-id="895be-144">Instead, the combination of HSB property values influences how color gradients throughout the UI are adjusted relative to each other.</span></span>

<span data-ttu-id="895be-145">Quand vous assignez des valeurs TSL personnalisées à [l’interface utilisateur \_ \_ GlobalTextColor](windowsribbon-reference-properties-uipkey-globaltextcolor.md) et à [l’interface utilisateur \_ \_ GlobalBackgroundColor](windowsribbon-reference-properties-uipkey-globalbackgroundcolor.md), il est recommandé que ces valeurs soient suffisamment grandes pour garantir la lisibilité.</span><span class="sxs-lookup"><span data-stu-id="895be-145">When assigning custom HSB values to [UI\_PKEY\_GlobalTextColor](windowsribbon-reference-properties-uipkey-globaltextcolor.md) and [UI\_PKEY\_GlobalBackgroundColor](windowsribbon-reference-properties-uipkey-globalbackgroundcolor.md), it is recommended that these values be of high enough contrast to ensure readability.</span></span> <span data-ttu-id="895be-146">Plus précisément, la couleur de texte doit être plus sombre que la nuance la plus légère de l’interface ruban.</span><span class="sxs-lookup"><span data-stu-id="895be-146">Specifically, the text color should be darker than the lightest shade of the ribbon UI.</span></span> <span data-ttu-id="895be-147">Le cas échéant, l’infrastructure ajuste automatiquement la \_ valeur TSL de l’interface utilisateur GlobalTextColor de l’interface utilisateur \_ pour fournir un contraste suffisant par rapport à n’importe quel dégradé ou nuance d’arrière-plan dérivé de l’interface utilisateur \_ \_ GlobalBackgroundColor.</span><span class="sxs-lookup"><span data-stu-id="895be-147">Where necessary, the framework automatically adjusts the UI\_PKEY\_GlobalTextColor HSB value to provide sufficient contrast against any background shade or gradient derived from UI\_PKEY\_GlobalBackgroundColor.</span></span>

> [!Note]  
> <span data-ttu-id="895be-148">Dans Windows 7, [l’interface utilisateur \_ \_ GlobalHighlightColor](windowsribbon-reference-properties-uipkey-globalhighlightcolor.md) peut être définie indépendamment de [l’interface utilisateur \_ \_ GlobalBackgroundColor](windowsribbon-reference-properties-uipkey-globalbackgroundcolor.md).</span><span class="sxs-lookup"><span data-stu-id="895be-148">In Windows 7, [UI\_PKEY\_GlobalHighlightColor](windowsribbon-reference-properties-uipkey-globalhighlightcolor.md) can be set independently of [UI\_PKEY\_GlobalBackgroundColor](windowsribbon-reference-properties-uipkey-globalbackgroundcolor.md).</span></span>

 

<span data-ttu-id="895be-149">L’exemple suivant montre comment spécifier une couleur personnalisée pour les propriétés de l' [interface utilisateur \_ \_ GlobalTextColor](windowsribbon-reference-properties-uipkey-globaltextcolor.md), de l' [interface utilisateur \_ \_ GlobalBackgroundColor](windowsribbon-reference-properties-uipkey-globalbackgroundcolor.md)et de l' [interface utilisateur de \_ \_ GlobalHighlightColor](windowsribbon-reference-properties-uipkey-globalhighlightcolor.md) .</span><span class="sxs-lookup"><span data-stu-id="895be-149">The following example demonstrates how to specify a custom color for the [UI\_PKEY\_GlobalTextColor](windowsribbon-reference-properties-uipkey-globaltextcolor.md), [UI\_PKEY\_GlobalBackgroundColor](windowsribbon-reference-properties-uipkey-globalbackgroundcolor.md), and [UI\_PKEY\_GlobalHighlightColor](windowsribbon-reference-properties-uipkey-globalhighlightcolor.md) properties.</span></span>


```C++
CComPtr<IPropertyStore> spPropertyStore;

// _spFramework is a pointer to the IUIFramework interface that is assigned 
// when the Ribbon is initialized.
if (SUCCEEDED(_spFramework->QueryInterface(&spPropertyStore)))
{
  PROPVARIANT propvarBackground;
  PROPVARIANT propvarHighlight;
  PROPVARIANT propvarText;
 
  // UI_HSBCOLOR is a type defined in UIRibbon.h that is composed of 
  // three component values: hue, saturation and brightness, respectively.
  UI_HSBCOLOR BackgroundColor = UI_HSB(0x14, 0x38, 0x54);
  UI_HSBCOLOR HighlightColor = UI_HSB(0x00, 0x36, 0x87);
  UI_HSBCOLOR TextColor = UI_HSB(0x2B, 0xD6, 0x00);

  InitPropVariantFromUInt32(BackgroundColor, &propvarBackground);
  InitPropVariantFromUInt32(HighlightColor, &propvarHighlight);
  InitPropVariantFromUInt32(TextColor, &propvarText);
 
  spPropertyStore->SetValue(UI_PKEY_GlobalBackgroundColor, propvarBackground);
  spPropertyStore->SetValue(UI_PKEY_GlobalTextColor, propvarText);
 
  spPropertyStore->Commit();
}
```



## <a name="convert-rgb-to-hsb"></a><span data-ttu-id="895be-150">Convertir RVB en TSL</span><span class="sxs-lookup"><span data-stu-id="895be-150">Convert RGB to HSB</span></span>

<span data-ttu-id="895be-151">Cette section décrit la formule requise pour la correspondance dynamique d’une valeur TSL de l’infrastructure du ruban, le [ \_ \_ GlobalBackgroundColor de l’interface utilisateur](windowsribbon-reference-properties-uipkey-globalbackgroundcolor.md) , dans cet exemple, à une couleur RVB spécifique au moment de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="895be-151">This section describes the formula that is required for dynamically matching a Ribbon framework HSB value, the [UI\_PKEY\_GlobalBackgroundColor](windowsribbon-reference-properties-uipkey-globalbackgroundcolor.md) in this example, to a specific RGB color at run time.</span></span>

<span data-ttu-id="895be-152">L’arrière-plan de la ligne d’onglet est utilisé comme point de référence, car il est rendu sous la forme d’une surface de couleur plate par rapport au dégradé de luminosité de l’arrière-plan du ruban.</span><span class="sxs-lookup"><span data-stu-id="895be-152">The tab row background is used as a reference point because it is rendered as a flat color surface compared to the brightness gradient of the ribbon background.</span></span>

<span data-ttu-id="895be-153">Une conversion préliminaire est nécessaire pour obtenir une valeur TSL intermédiaire.</span><span class="sxs-lookup"><span data-stu-id="895be-153">A preliminary conversion is necessary to obtain an intermediate HSL value.</span></span> <span data-ttu-id="895be-154">Cette valeur TSL peut ensuite être convertie en valeur TSL.</span><span class="sxs-lookup"><span data-stu-id="895be-154">This HSL value can then be converted to an HSB value.</span></span>

> [!Note]  
> <span data-ttu-id="895be-155">La conversion de RVB en TSL est facilement effectuée avec la plupart des logiciels de modification de photos.</span><span class="sxs-lookup"><span data-stu-id="895be-155">The conversion from RGB to HSL is easily accomplished with most photo editing software.</span></span>

 

<span data-ttu-id="895be-156">La conversion de TSL (avec chaque composant de la plage comprise entre 0,0 et 1,0) en un paramètre TSL du ruban est effectuée à l’aide des formules suivantes :</span><span class="sxs-lookup"><span data-stu-id="895be-156">Conversion of HSL (with each component in the range of 0.0 to 1.0) to a Ribbon HSB setting is accomplished through the following formulas:</span></span>

-   <span data-ttu-id="895be-157">H<sub>Background</sub> = Round (255.0 H)</span><span class="sxs-lookup"><span data-stu-id="895be-157">H<sub>background</sub> = Round(255.0 H)</span></span>
-   <span data-ttu-id="895be-158">S<sub>arrière-plan</sub> = Round (255.0 S)</span><span class="sxs-lookup"><span data-stu-id="895be-158">S<sub>background</sub> = Round(255.0 S)</span></span>
-   <span data-ttu-id="895be-159">B<sub>Background</sub> = Round (257.7 + 149,9 ln (L)) si 0,1793 <= L <= 0,9821</span><span class="sxs-lookup"><span data-stu-id="895be-159">B<sub>background</sub> = Round(257.7 + 149.9 ln(L)) if 0.1793 <= L <= 0.9821</span></span>

## <a name="related-topics"></a><span data-ttu-id="895be-160">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="895be-160">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="895be-161">Recommandations relatives aux couleurs</span><span class="sxs-lookup"><span data-stu-id="895be-161">Color Guidelines</span></span>](https://msdn.microsoft.com/library/aa511283.aspx)
</dt> <dt>

[<span data-ttu-id="895be-162">Propriétés du Framework</span><span class="sxs-lookup"><span data-stu-id="895be-162">Framework Properties</span></span>](windowsribbon-reference-properties-framework.md)
</dt> </dl>

 

 





