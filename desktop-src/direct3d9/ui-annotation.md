---
description: Utilisez cette annotation pour associer un paramètre d’effet à un contrôle d’interface utilisateur dans l’environnement hôte. Cela permet à un utilisateur de contrôler de manière interactive un paramètre d’effet par le biais de l’application hôte.
ms.assetid: 6d0b2450-7d90-4a24-b710-faed26969876
title: Annotation d’IU
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3e873c83a01c5c2214cb49a93e75167e58a3389
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104482680"
---
# <a name="ui-annotation"></a><span data-ttu-id="be6bd-104">Annotation d’IU</span><span class="sxs-lookup"><span data-stu-id="be6bd-104">UI Annotation</span></span>

<span data-ttu-id="be6bd-105">Utilisez cette annotation pour associer un paramètre d’effet à un contrôle d’interface utilisateur dans l’environnement hôte.</span><span class="sxs-lookup"><span data-stu-id="be6bd-105">Use this annotation to associate an effect parameter with a UI control in the host environment.</span></span> <span data-ttu-id="be6bd-106">Cela permet à un utilisateur de contrôler de manière interactive un paramètre d’effet par le biais de l’application hôte.</span><span class="sxs-lookup"><span data-stu-id="be6bd-106">This will allow a user to interactively control an effect parameter through the host application.</span></span>

<span data-ttu-id="be6bd-107">DXSAS définit un ensemble de contrôles standard en termes de modèle de données et de comportement de base que les auteurs peuvent attendre des applications hôtes.</span><span class="sxs-lookup"><span data-stu-id="be6bd-107">DXSAS defines a set of standard controls in terms of the data model and basic behavior that effect authors can expect from host applications.</span></span> <span data-ttu-id="be6bd-108">L’annotation de contrôle est utilisée comme suit :</span><span class="sxs-lookup"><span data-stu-id="be6bd-108">The control annotation is used like this:</span></span>


```
string SasUiControl = "ControlType";
```



<span data-ttu-id="be6bd-109">where</span><span class="sxs-lookup"><span data-stu-id="be6bd-109">where</span></span>


```
ControlType
```



<span data-ttu-id="be6bd-110">est l’un des éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="be6bd-110">is one of the following:</span></span>



|             |                                                                                                                                                                                 |                                                                                                    |                                                                                                              |
|-------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="be6bd-111">ControlType</span><span class="sxs-lookup"><span data-stu-id="be6bd-111">ControlType</span></span> | <span data-ttu-id="be6bd-112">Description</span><span class="sxs-lookup"><span data-stu-id="be6bd-112">Description</span></span>                                                                                                                                                                     | <span data-ttu-id="be6bd-113">Type de données interne</span><span class="sxs-lookup"><span data-stu-id="be6bd-113">Internal Data Type</span></span>                                                                                 | <span data-ttu-id="be6bd-114">Annotations de propriété de contrôle</span><span class="sxs-lookup"><span data-stu-id="be6bd-114">Control Property Annotations</span></span>                                                                                 |
| <span data-ttu-id="be6bd-115">Aucun</span><span class="sxs-lookup"><span data-stu-id="be6bd-115">None</span></span>        | <span data-ttu-id="be6bd-116">Aucun contrôle ne doit être affiché.</span><span class="sxs-lookup"><span data-stu-id="be6bd-116">No control should be shown.</span></span> <span data-ttu-id="be6bd-117">Notez qu’un contrôle est visible si [SasUiVisible](#sasuivisible) a la valeur true et que le type de contrôle est un type autre que None.</span><span class="sxs-lookup"><span data-stu-id="be6bd-117">Note that a control is visible if [SasUiVisible](#sasuivisible) is True and the control type is any type other than None.</span></span>                           | <span data-ttu-id="be6bd-118">n/a</span><span class="sxs-lookup"><span data-stu-id="be6bd-118">n/a</span></span>                                                                                                | <span data-ttu-id="be6bd-119">n/a</span><span class="sxs-lookup"><span data-stu-id="be6bd-119">n/a</span></span>                                                                                                          |
| <span data-ttu-id="be6bd-120">Quelconque</span><span class="sxs-lookup"><span data-stu-id="be6bd-120">Any</span></span>         | <span data-ttu-id="be6bd-121">Cela implique qu’aucun contrôle spécial n’est demandé.</span><span class="sxs-lookup"><span data-stu-id="be6bd-121">This implies that no special control is requested.</span></span> <span data-ttu-id="be6bd-122">Le contrôle présenté est le résultat d’un comportement défini par l’application.</span><span class="sxs-lookup"><span data-stu-id="be6bd-122">The control presented is the result of application-defined behavior.</span></span>                                                         | <span data-ttu-id="be6bd-123">n/a</span><span class="sxs-lookup"><span data-stu-id="be6bd-123">n/a</span></span>                                                                                                | <span data-ttu-id="be6bd-124">n/a</span><span class="sxs-lookup"><span data-stu-id="be6bd-124">n/a</span></span>                                                                                                          |
| <span data-ttu-id="be6bd-125">ColorPicker</span><span class="sxs-lookup"><span data-stu-id="be6bd-125">ColorPicker</span></span> | <span data-ttu-id="be6bd-126">Représente une valeur de couleur sous la forme d’un échantillon de couleur.</span><span class="sxs-lookup"><span data-stu-id="be6bd-126">Represent a color value as a color swatch.</span></span> <span data-ttu-id="be6bd-127">La valeur est compressée dans les composants XYZ du vecteur associé.</span><span class="sxs-lookup"><span data-stu-id="be6bd-127">The value is packed into the XYZ components of the associated vector.</span></span> <span data-ttu-id="be6bd-128">Le composant W du vecteur associé est toujours défini sur un.</span><span class="sxs-lookup"><span data-stu-id="be6bd-128">The W component of the associated vector is always set to one.</span></span> | <span data-ttu-id="be6bd-129">float *n* , où *n* est compris entre 1 et 4.</span><span class="sxs-lookup"><span data-stu-id="be6bd-129">float *N* where *N* is 1 to 4 inclusive.</span></span>                                                            | [<span data-ttu-id="be6bd-130">SasUiEnum</span><span class="sxs-lookup"><span data-stu-id="be6bd-130">SasUiEnum</span></span>](#sasuienum)                                                                                      |
| <span data-ttu-id="be6bd-131">Sens</span><span class="sxs-lookup"><span data-stu-id="be6bd-131">Direction</span></span>   | <span data-ttu-id="be6bd-132">Vecteur de direction.</span><span class="sxs-lookup"><span data-stu-id="be6bd-132">A direction vector.</span></span>                                                                                                                                                             | <span data-ttu-id="be6bd-133">float *n* , où *n* est compris entre 2 et 4.</span><span class="sxs-lookup"><span data-stu-id="be6bd-133">float *N* where *N* is 2 to 4 inclusive.</span></span>                                                            | <span data-ttu-id="be6bd-134">Aucun</span><span class="sxs-lookup"><span data-stu-id="be6bd-134">None</span></span>                                                                                                         |
| <span data-ttu-id="be6bd-135">FilePicker</span><span class="sxs-lookup"><span data-stu-id="be6bd-135">FilePicker</span></span>  | <span data-ttu-id="be6bd-136">Boîte de dialogue qui permet à l’utilisateur de parcourir et de sélectionner un fichier.</span><span class="sxs-lookup"><span data-stu-id="be6bd-136">A dialog box that allows the user to browse and select a file.</span></span>                                                                                                                  | <span data-ttu-id="be6bd-137">string</span><span class="sxs-lookup"><span data-stu-id="be6bd-137">string</span></span>                                                                                             | <span data-ttu-id="be6bd-138">Aucun</span><span class="sxs-lookup"><span data-stu-id="be6bd-138">None</span></span>                                                                                                         |
| <span data-ttu-id="be6bd-139">ListPicker</span><span class="sxs-lookup"><span data-stu-id="be6bd-139">ListPicker</span></span>  | <span data-ttu-id="be6bd-140">Liste de valeurs de chaîne à partir de laquelle l’utilisateur peut sélectionner une entrée.</span><span class="sxs-lookup"><span data-stu-id="be6bd-140">A list of string values from which the user can select one entry.</span></span> <span data-ttu-id="be6bd-141">Les valeurs sont générées à partir de l’annotation [SasUiEnum](#sasuienum) .</span><span class="sxs-lookup"><span data-stu-id="be6bd-141">The values are generated from the [SasUiEnum](#sasuienum) annotation.</span></span>                                         | <span data-ttu-id="be6bd-142">Tableau de chaînes avec une valeur entière contenant l’index de la valeur de chaîne sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="be6bd-142">An array of strings along with an integer value containing the index of the selected string value.</span></span> | [<span data-ttu-id="be6bd-143">SasUiEnum</span><span class="sxs-lookup"><span data-stu-id="be6bd-143">SasUiEnum</span></span>](#sasuienum)                                                                                      |
| <span data-ttu-id="be6bd-144">Numérique</span><span class="sxs-lookup"><span data-stu-id="be6bd-144">Numeric</span></span>     | <span data-ttu-id="be6bd-145">Ensemble de contrôles d’entrée numériques (tels que des zones de texte).</span><span class="sxs-lookup"><span data-stu-id="be6bd-145">A set of numerical input controls (such as text boxes).</span></span>                                                                                                                         | <span data-ttu-id="be6bd-146">float *m* x *N* où *M* et *N* sont compris entre 1 et 4.</span><span class="sxs-lookup"><span data-stu-id="be6bd-146">float *M* x *N* where *M* and *N* are 1 to 4 inclusive.</span></span>                                               | <span data-ttu-id="be6bd-147">[SasUiMin](#sasuimin), [SasUiMax](#sasuimax), [SasUiStride](#sasuistride)</span><span class="sxs-lookup"><span data-stu-id="be6bd-147">[SasUiMin](#sasuimin), [SasUiMax](#sasuimax), [SasUiStride](#sasuistride)</span></span>                                    |
| <span data-ttu-id="be6bd-148">Curseur</span><span class="sxs-lookup"><span data-stu-id="be6bd-148">Slider</span></span>      | <span data-ttu-id="be6bd-149">Ensemble de curseurs.</span><span class="sxs-lookup"><span data-stu-id="be6bd-149">A set of sliders.</span></span>                                                                                                                                                               | <span data-ttu-id="be6bd-150">float *m* x *N* où *M* et *N* sont compris entre 1 et 4</span><span class="sxs-lookup"><span data-stu-id="be6bd-150">float *M* x *N* where *M* and *N* are 1 to 4 inclusive</span></span>                                                | <span data-ttu-id="be6bd-151">[SasUiMin](#sasuimin), [SasUiMax](#sasuimax), [SasUiSteps](#sasuisteps), [SasUiStepsPower](#sasuistepspower)</span><span class="sxs-lookup"><span data-stu-id="be6bd-151">[SasUiMin](#sasuimin), [SasUiMax](#sasuimax), [SasUiSteps](#sasuisteps), [SasUiStepsPower](#sasuistepspower)</span></span> |
| <span data-ttu-id="be6bd-152">String</span><span class="sxs-lookup"><span data-stu-id="be6bd-152">String</span></span>      | <span data-ttu-id="be6bd-153">Zone de texte pour modifier le contenu de la chaîne.</span><span class="sxs-lookup"><span data-stu-id="be6bd-153">An text box for editing string content.</span></span>                                                                                                                                         | <span data-ttu-id="be6bd-154">string</span><span class="sxs-lookup"><span data-stu-id="be6bd-154">string</span></span>                                                                                             | <span data-ttu-id="be6bd-155">Aucun</span><span class="sxs-lookup"><span data-stu-id="be6bd-155">None</span></span>                                                                                                         |



 

<span data-ttu-id="be6bd-156">Si le type de données interne n’est pas identique au type du paramètre associé, la conversion se produit lorsque les données sont transférées du paramètre de l’application hôte vers le paramètre Effect.</span><span class="sxs-lookup"><span data-stu-id="be6bd-156">If the internal data type is not identical to the associated parameter's type, casting will occur when data is transferred from the host application parameter to the effect parameter.</span></span>

<span data-ttu-id="be6bd-157">La valeur par défaut est la chaîne « None ».</span><span class="sxs-lookup"><span data-stu-id="be6bd-157">The default is the string "None".</span></span>

## <a name="ui-common-properties"></a><span data-ttu-id="be6bd-158">Propriétés communes de l’interface utilisateur</span><span class="sxs-lookup"><span data-stu-id="be6bd-158">UI Common Properties</span></span>

### <a name="sasuidescription"></a><span data-ttu-id="be6bd-159">SasUiDescription</span><span class="sxs-lookup"><span data-stu-id="be6bd-159">SasUiDescription</span></span>

<span data-ttu-id="be6bd-160">Utilisez cette annotation pour spécifier une chaîne afin de décrire un outil.</span><span class="sxs-lookup"><span data-stu-id="be6bd-160">Use this annotation to specify a string to describe a tool.</span></span> <span data-ttu-id="be6bd-161">Cela peut être utilisé pour les éléments d’interface utilisateur tels que les info-bulles.</span><span class="sxs-lookup"><span data-stu-id="be6bd-161">This could be used for UI elements such as tool tips.</span></span>


```
string SasUiDescription = "descriptive string";
```



<span data-ttu-id="be6bd-162">Exemple :</span><span class="sxs-lookup"><span data-stu-id="be6bd-162">For instance:</span></span>


```
float3 UpNormal
<
  string SasUiDescription = "The normalized up vector";
>;
```



<span data-ttu-id="be6bd-163">La valeur par défaut est une chaîne vide.</span><span class="sxs-lookup"><span data-stu-id="be6bd-163">The default is an empty string.</span></span>

### <a name="sasuilabel"></a><span data-ttu-id="be6bd-164">SasUiLabel</span><span class="sxs-lookup"><span data-stu-id="be6bd-164">SasUiLabel</span></span>

<span data-ttu-id="be6bd-165">Utilisez cette annotation pour spécifier une chaîne pour étiqueter un contrôle d’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="be6bd-165">Use this annotation to specify a string to label any UI control.</span></span>


```
string SasUiLabel = "some label;
```



<span data-ttu-id="be6bd-166">Voici un exemple :</span><span class="sxs-lookup"><span data-stu-id="be6bd-166">Here is an example:</span></span>


```
float3 UpNormal
<
  string SasUiLabel = "Normal that points up.";
>;
```



<span data-ttu-id="be6bd-167">La valeur par défaut est une chaîne vide.</span><span class="sxs-lookup"><span data-stu-id="be6bd-167">The default is an empty string.</span></span>

### <a name="sasuivisible"></a><span data-ttu-id="be6bd-168">SasUiVisible</span><span class="sxs-lookup"><span data-stu-id="be6bd-168">SasUiVisible</span></span>

<span data-ttu-id="be6bd-169">Utilisez cette annotation pour indiquer si le paramètre associé doit être affiché à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="be6bd-169">Use this annotation to specify whether the associated parameter should be displayed to the user.</span></span>


```
bool SasUiVisible = false;
```



<span data-ttu-id="be6bd-170">Si la valeur est true, l’application hôte doit afficher un contrôle d’interface utilisateur pour la modification du paramètre d’effet annoté.</span><span class="sxs-lookup"><span data-stu-id="be6bd-170">If set to True, the host application should display a UI control for editing the annotated effect parameter.</span></span> <span data-ttu-id="be6bd-171">Si la valeur est false, aucune interface utilisateur n’est affichée dans l’application hôte.</span><span class="sxs-lookup"><span data-stu-id="be6bd-171">If false, no UI is displayed in the host application.</span></span>

<span data-ttu-id="be6bd-172">Voici un exemple :</span><span class="sxs-lookup"><span data-stu-id="be6bd-172">Here is an example:</span></span>


```
float3 UpNormal
<
  string SasUiVisible = false;
>;
```



<span data-ttu-id="be6bd-173">La valeur par défaut est True.</span><span class="sxs-lookup"><span data-stu-id="be6bd-173">The default is True.</span></span>

## <a name="ui-control-properties"></a><span data-ttu-id="be6bd-174">Propriétés de contrôle d’IU</span><span class="sxs-lookup"><span data-stu-id="be6bd-174">UI Control Properties</span></span>

<span data-ttu-id="be6bd-175">Les annotations de propriété de contrôle sont des modificateurs supplémentaires qui permettent de déterminer la façon dont un contrôle particulier fonctionne.</span><span class="sxs-lookup"><span data-stu-id="be6bd-175">Control property annotations are additional modifiers that help determine how a particular control operates.</span></span>

### <a name="sasuienum"></a><span data-ttu-id="be6bd-176">SasUiEnum</span><span class="sxs-lookup"><span data-stu-id="be6bd-176">SasUiEnum</span></span>

<span data-ttu-id="be6bd-177">Cette annotation vous permet de limiter la plage de valeurs d’un contrôle.</span><span class="sxs-lookup"><span data-stu-id="be6bd-177">This annotation allows you to restrict the range of values for a control.</span></span> <span data-ttu-id="be6bd-178">L’annotation contient une chaîne de valeurs séparées par des virgules.</span><span class="sxs-lookup"><span data-stu-id="be6bd-178">The annotation contains a string of values delimited by commas.</span></span>

<span data-ttu-id="be6bd-179">La valeur par défaut est une chaîne vide.</span><span class="sxs-lookup"><span data-stu-id="be6bd-179">The default is an empty string.</span></span>

### <a name="sasuimax"></a><span data-ttu-id="be6bd-180">SasUiMax</span><span class="sxs-lookup"><span data-stu-id="be6bd-180">SasUiMax</span></span>

<span data-ttu-id="be6bd-181">Cette annotation spécifie la valeur maximale du paramètre associé.</span><span class="sxs-lookup"><span data-stu-id="be6bd-181">This annotation specifies the maximum value of the associated parameter.</span></span> <span data-ttu-id="be6bd-182">Elle ne peut être associée qu’à un paramètre de type numérique.</span><span class="sxs-lookup"><span data-stu-id="be6bd-182">It can only be associated with a numerically-typed parameter.</span></span> <span data-ttu-id="be6bd-183">La valeur maximale du paramètre sera calculée comme suit :</span><span class="sxs-lookup"><span data-stu-id="be6bd-183">The maximum value of the parameter will actually be calculated as:</span></span>


```
MaxValue = min(FLT_MAX, PARAMETER_TYPE_MAX);
```



<span data-ttu-id="be6bd-184">Le \_ type \_ de paramètre Max est la valeur maximale pour le type utilisé par le paramètre associé.</span><span class="sxs-lookup"><span data-stu-id="be6bd-184">PARAMETER\_TYPE\_MAX is the maximum value for the type used by the associated parameter.</span></span> <span data-ttu-id="be6bd-185">Cela signifie que la valeur du paramètre, prenant en compte l’annotation [SasUiMax](#sasuimax) , est calculée comme suit :</span><span class="sxs-lookup"><span data-stu-id="be6bd-185">This means that the value of the parameter, taking into account the [SasUiMax](#sasuimax) annotation is calculated as:</span></span>


```
ParameterValue = min(NewParameterValue, MaxValue);
```



<span data-ttu-id="be6bd-186">La valeur par défaut est FLT \_ Max comme défini dans Math. h.</span><span class="sxs-lookup"><span data-stu-id="be6bd-186">The default value is FLT\_MAX as defined in Math.h.</span></span>

### <a name="sasuimin"></a><span data-ttu-id="be6bd-187">SasUiMin</span><span class="sxs-lookup"><span data-stu-id="be6bd-187">SasUiMin</span></span>

<span data-ttu-id="be6bd-188">Cette annotation spécifie la valeur minimale du paramètre associé.</span><span class="sxs-lookup"><span data-stu-id="be6bd-188">This annotation specifies the minimum value of the associated parameter.</span></span> <span data-ttu-id="be6bd-189">Elle ne peut être associée qu’à un paramètre de type numérique.</span><span class="sxs-lookup"><span data-stu-id="be6bd-189">It can only be associated with any numerically-typed parameter.</span></span> <span data-ttu-id="be6bd-190">La valeur minimale du paramètre sera calculée comme suit :</span><span class="sxs-lookup"><span data-stu-id="be6bd-190">The minimum value of the parameter will actually be calculated as:</span></span>


```
MinValue = max(-FLT_MAX, PARAMETER_TYPE_MIN);
```



<span data-ttu-id="be6bd-191">Le \_ type \_ de paramètre min est la valeur minimale pour le type utilisé par le paramètre associé.</span><span class="sxs-lookup"><span data-stu-id="be6bd-191">PARAMETER\_TYPE\_MIN is the minimum value for the type used by the associated parameter.</span></span> <span data-ttu-id="be6bd-192">Cela signifie que la valeur du paramètre, prenant en compte l’annotation [SasUiMin](#sasuimin) , est calculée comme suit :</span><span class="sxs-lookup"><span data-stu-id="be6bd-192">This means that the value of the parameter, taking into account the [SasUiMin](#sasuimin) annotation is calculated as:</span></span>


```
ParameterValue = max(NewParameterValue, MinValue);
```



<span data-ttu-id="be6bd-193">La valeur par défaut est-FLT \_ Max, comme défini dans Math. h.</span><span class="sxs-lookup"><span data-stu-id="be6bd-193">The default value is -FLT\_MAX as defined in Math.h.</span></span>

### <a name="sasuisteps"></a><span data-ttu-id="be6bd-194">SasUiSteps</span><span class="sxs-lookup"><span data-stu-id="be6bd-194">SasUiSteps</span></span>

<span data-ttu-id="be6bd-195">Cette annotation spécifie le nombre d’étapes qui peuvent être utilisées lors de l’incrémentation ou de la décrémentation de la valeur de paramètre associée.</span><span class="sxs-lookup"><span data-stu-id="be6bd-195">This annotation specifies the number of steps that can be used when incrementing or decrementing the associated parameter value.</span></span> <span data-ttu-id="be6bd-196">L’annotation n’est significative que sur un paramètre de type numérique.</span><span class="sxs-lookup"><span data-stu-id="be6bd-196">The annotation is only meaningful on a numerically-typed parameter.</span></span> <span data-ttu-id="be6bd-197">La valeur zéro indique que l’application hôte choisira un nombre raisonnable d’étapes.</span><span class="sxs-lookup"><span data-stu-id="be6bd-197">Zero specifies that the host application will choose a reasonable number of steps.</span></span>

<span data-ttu-id="be6bd-198">La valeur par défaut est 0.</span><span class="sxs-lookup"><span data-stu-id="be6bd-198">The default value is 0.</span></span>

### <a name="sasuistepspower"></a><span data-ttu-id="be6bd-199">SasUiStepsPower</span><span class="sxs-lookup"><span data-stu-id="be6bd-199">SasUiStepsPower</span></span>

<span data-ttu-id="be6bd-200">Cette annotation spécifie l’exposant dans la fonction Power, qui a la plage \[ 0.0 f, 1.0 f \] .</span><span class="sxs-lookup"><span data-stu-id="be6bd-200">This annotation specifies the exponent in the power function, which has the range \[0.0f, 1.0f\].</span></span> <span data-ttu-id="be6bd-201">Les applications hôtes doivent implémenter la méthode suivante lors du calcul des valeurs de paramètre :</span><span class="sxs-lookup"><span data-stu-id="be6bd-201">Host applications must implement the following method when calculating parameter values:</span></span>


```
ParameterValue = ((SasUiMax - SasUiMin) x pow(UI_VALUE, SasUiStepsPower) + SasUiMin
```



<span data-ttu-id="be6bd-202">La valeur par défaut est 1,0 f.</span><span class="sxs-lookup"><span data-stu-id="be6bd-202">The default value is 1.0f.</span></span>

### <a name="sasuistride"></a><span data-ttu-id="be6bd-203">SasUiStride</span><span class="sxs-lookup"><span data-stu-id="be6bd-203">SasUiStride</span></span>

<span data-ttu-id="be6bd-204">Cette annotation spécifie l’incrément qui doit être utilisé lors de l’incrémentation ou de la décrémentation de cette valeur.</span><span class="sxs-lookup"><span data-stu-id="be6bd-204">This annotation specifies the increment that should be used when incrementing or decrementing this value.</span></span> <span data-ttu-id="be6bd-205">Contrairement à [SasUiSteps](#sasuisteps), [SasUiStride](#sasuistride) est utile avec un contrôle Spinner, par exemple, où les données sont illimitées et l’utilisateur doit plutôt incrémenter la valeur de paramètre par Stride plutôt que par un nombre prédéfini d’étapes.</span><span class="sxs-lookup"><span data-stu-id="be6bd-205">Unlike [SasUiSteps](#sasuisteps), [SasUiStride](#sasuistride) is useful with a spinner control, for instance, where the data is unbounded and the user would rather increment the parameter value by stride rather than by a pre-defined number of steps.</span></span> <span data-ttu-id="be6bd-206">Les applications hôtes doivent incrémenter (ou décrémenter selon le comportement du contrôle) la valeur de SasUiStride, comme suit :</span><span class="sxs-lookup"><span data-stu-id="be6bd-206">Host applications should increment (or decrement depending on the control behavior) by the value of SasUiStride as follows:</span></span>


```
ParameterValue = ParameterValue +/- SasUiStride
```



<span data-ttu-id="be6bd-207">La valeur par défaut est 1,0 f.</span><span class="sxs-lookup"><span data-stu-id="be6bd-207">The default value is 1.0f.</span></span>

## <a name="related-topics"></a><span data-ttu-id="be6bd-208">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="be6bd-208">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="be6bd-209">Informations de référence sur les annotations et sémantiques DirectX standard</span><span class="sxs-lookup"><span data-stu-id="be6bd-209">DirectX Standard Annotations and Semantics Reference</span></span>](dx9-graphics-reference-effects-dxsas.md)
</dt> </dl>

 

 



