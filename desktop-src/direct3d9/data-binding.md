---
description: Utilisez la collection SasHostParameterValue pour définir la collection de valeurs d’application hôte, ainsi que leur type et leurs membres, exposés aux effets.
ms.assetid: 3fef353d-323a-4cc1-a8c9-2bf154754835
title: Liaison de données
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b67305d4acc8a4ed9e0827203e4602db26a99da
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104317593"
---
# <a name="data-binding"></a><span data-ttu-id="ee032-103">Liaison de données</span><span class="sxs-lookup"><span data-stu-id="ee032-103">Data Binding</span></span>

<span data-ttu-id="ee032-104">Utilisez la [collection SasHostParameterValue](#sashostparametervalue-collection) pour définir la collection de valeurs d’application hôte, ainsi que leur type et leurs membres, exposés aux effets.</span><span class="sxs-lookup"><span data-stu-id="ee032-104">Use [SasHostParameterValue Collection](#sashostparametervalue-collection) to define the collection of host application values, as well as their type and members, exposed to effects.</span></span> <span data-ttu-id="ee032-105">Utilisez l’annotation [SasBindAddress](#sasbindaddress) dans un fichier Effect pour associer un paramètre Effect à son paramètre correspondant dans l’application hôte.</span><span class="sxs-lookup"><span data-stu-id="ee032-105">Use the [SasBindAddress](#sasbindaddress) annotation in an effect file to associate an effect parameter with its corresponding parameter in the host application.</span></span>

## <a name="sashostparametervalue-collection"></a><span data-ttu-id="ee032-106">Collection SasHostParameterValue</span><span class="sxs-lookup"><span data-stu-id="ee032-106">SasHostParameterValue Collection</span></span>

<span data-ttu-id="ee032-107">Le SasHostParameterValue est défini à l’aide de la syntaxe de fichier Effect (. FX).</span><span class="sxs-lookup"><span data-stu-id="ee032-107">The SasHostParameterValue is defined using effect file (.fx) syntax.</span></span> <span data-ttu-id="ee032-108">Bien que la syntaxe soit très similaire à la syntaxe des fichiers Effects, certaines différences existent.</span><span class="sxs-lookup"><span data-stu-id="ee032-108">While the syntax is very similar to the effect file syntax, some differences exist.</span></span> <span data-ttu-id="ee032-109">Par exemple, les types d’objets, tels que les Texture2D, les échantillonneurs et les chaînes, ne sont pas valides dans les fichiers d’effets réels, mais sont valides dans le SasHostParameterValue.</span><span class="sxs-lookup"><span data-stu-id="ee032-109">For example, object types, such as texture2d, samplers, and strings, are not valid in actual effect files, but are valid in the SasHostParameterValue.</span></span> <span data-ttu-id="ee032-110">Une application hôte peut implémenter SasHostParameterValue de quelque manière que ce soit, à condition qu’elle soit conforme à la description ci-dessous. la définition réelle se trouve dans le fichier include d’effet standard DXSAS ( \[ SDK racine \] /Utilities/source/SAS/SAS.FXH).</span><span class="sxs-lookup"><span data-stu-id="ee032-110">A host application can implement SasHostParameterValue in any way so long as it conforms to the description below; the actual definition is located in the DXSAS standard effect include file (\[SDK Root\]/Utilities/Source/Sas/Sas.fxh).</span></span>

<span data-ttu-id="ee032-111">Notez que les tableaux dans le SasHostParameterValue, tels que les lumières ou les caméras, ont une longueur illimitée.</span><span class="sxs-lookup"><span data-stu-id="ee032-111">Note that arrays in the SasHostParameterValue such as Lights or Cameras have unbounded length.</span></span> <span data-ttu-id="ee032-112">Cela signifie que les effets peuvent être liés à n’importe quel index arbitraire dans ces tableaux et que les applications hôtes doivent fournir des valeurs par défaut significatives dans les cas où aucune valeur d’application ne peut être fournie.</span><span class="sxs-lookup"><span data-stu-id="ee032-112">This means that effects can bind to any arbitrary index in those arrays and host applications must provide meaningful defaults in the cases where no application value can be provided.</span></span>

<span data-ttu-id="ee032-113">Certains types et constantes doivent être définis dans le DXSAS standard include, comme indiqué dans la définition de l’inclusion standard.</span><span class="sxs-lookup"><span data-stu-id="ee032-113">Some types and constants are required to be defined in the DXSAS standard include, as noted in the definition of the standard include.</span></span> <span data-ttu-id="ee032-114">Cela permet aux effets de lier facilement des valeurs agrégées des SasHostParameterValue à des paramètres d’effet structurés.</span><span class="sxs-lookup"><span data-stu-id="ee032-114">This allows effects to easily bind aggregated values from the SasHostParameterValue to structured effect parameters.</span></span>



| <span data-ttu-id="ee032-115">Collection SasHostParameterValue</span><span class="sxs-lookup"><span data-stu-id="ee032-115">SasHostParameterValue Collection</span></span>    | <span data-ttu-id="ee032-116">Type</span><span class="sxs-lookup"><span data-stu-id="ee032-116">Type</span></span>            | <span data-ttu-id="ee032-117">Membre</span><span class="sxs-lookup"><span data-stu-id="ee032-117">Member</span></span>                                       |
|-------------------------------------|-----------------|----------------------------------------------|
| [<span data-ttu-id="ee032-118">Time</span><span class="sxs-lookup"><span data-stu-id="ee032-118">Time</span></span>](#time)                       | <span data-ttu-id="ee032-119">float</span><span class="sxs-lookup"><span data-stu-id="ee032-119">float</span></span>           | <span data-ttu-id="ee032-120">SAS. Time. Now</span><span class="sxs-lookup"><span data-stu-id="ee032-120">Sas.Time.Now</span></span>                                 |
|                                     | <span data-ttu-id="ee032-121">float</span><span class="sxs-lookup"><span data-stu-id="ee032-121">float</span></span>           | <span data-ttu-id="ee032-122">SAS. Time. Last</span><span class="sxs-lookup"><span data-stu-id="ee032-122">Sas.Time.Last</span></span>                                |
|                                     | <span data-ttu-id="ee032-123">int</span><span class="sxs-lookup"><span data-stu-id="ee032-123">int</span></span>             | <span data-ttu-id="ee032-124">SAS. Time. FrameNumber</span><span class="sxs-lookup"><span data-stu-id="ee032-124">Sas.Time.FrameNumber</span></span>                         |
| [<span data-ttu-id="ee032-125">Mappage d’environnement</span><span class="sxs-lookup"><span data-stu-id="ee032-125">Environment Map</span></span>](#environment-map) | <span data-ttu-id="ee032-126">textureCUBE</span><span class="sxs-lookup"><span data-stu-id="ee032-126">textureCUBE</span></span>     | <span data-ttu-id="ee032-127">SAS. EnvironmentMap</span><span class="sxs-lookup"><span data-stu-id="ee032-127">Sas.EnvironmentMap</span></span>                           |
| [<span data-ttu-id="ee032-128">Appareil photo</span><span class="sxs-lookup"><span data-stu-id="ee032-128">Camera</span></span>](#camera)                   | <span data-ttu-id="ee032-129">SasCamera</span><span class="sxs-lookup"><span data-stu-id="ee032-129">SasCamera</span></span>       | <span data-ttu-id="ee032-130">SAS. Camera</span><span class="sxs-lookup"><span data-stu-id="ee032-130">Sas.Camera</span></span>                                   |
|                                     | <span data-ttu-id="ee032-131">float4x4</span><span class="sxs-lookup"><span data-stu-id="ee032-131">float4x4</span></span>        | <span data-ttu-id="ee032-132">SAS. Camera. WorldToView</span><span class="sxs-lookup"><span data-stu-id="ee032-132">Sas.Camera.WorldToView</span></span>                       |
|                                     | <span data-ttu-id="ee032-133">float4x4</span><span class="sxs-lookup"><span data-stu-id="ee032-133">float4x4</span></span>        | <span data-ttu-id="ee032-134">SAS. Camera. projection</span><span class="sxs-lookup"><span data-stu-id="ee032-134">Sas.Camera.Projection</span></span>                        |
|                                     | <span data-ttu-id="ee032-135">float2</span><span class="sxs-lookup"><span data-stu-id="ee032-135">float2</span></span>          | <span data-ttu-id="ee032-136">SAS. Camera. NearFarClipping</span><span class="sxs-lookup"><span data-stu-id="ee032-136">Sas.Camera.NearFarClipping</span></span>                   |
| [<span data-ttu-id="ee032-137">Clair</span><span class="sxs-lookup"><span data-stu-id="ee032-137">Light</span></span>](#light)                     | <span data-ttu-id="ee032-138">SasAmbientLight</span><span class="sxs-lookup"><span data-stu-id="ee032-138">SasAmbientLight</span></span> | <span data-ttu-id="ee032-139">AmbientLight \[ ZeroOrMore \] ;</span><span class="sxs-lookup"><span data-stu-id="ee032-139">AmbientLight\[ZeroOrMore\];</span></span>                  |
|                                     | <span data-ttu-id="ee032-140">int</span><span class="sxs-lookup"><span data-stu-id="ee032-140">int</span></span>             | <span data-ttu-id="ee032-141">SAS. NumAmbientLights</span><span class="sxs-lookup"><span data-stu-id="ee032-141">Sas.NumAmbientLights</span></span>                         |
|                                     | <span data-ttu-id="ee032-142">SasAmbientLight</span><span class="sxs-lookup"><span data-stu-id="ee032-142">SasAmbientLight</span></span> | <span data-ttu-id="ee032-143">DirectionalLight \[ ZeroOrMore \] ;</span><span class="sxs-lookup"><span data-stu-id="ee032-143">DirectionalLight\[ZeroOrMore\];</span></span>              |
|                                     | <span data-ttu-id="ee032-144">int</span><span class="sxs-lookup"><span data-stu-id="ee032-144">int</span></span>             | <span data-ttu-id="ee032-145">SAS. NumDirectionalLights</span><span class="sxs-lookup"><span data-stu-id="ee032-145">Sas.NumDirectionalLights</span></span>                     |
|                                     | <span data-ttu-id="ee032-146">SasAmbientLight</span><span class="sxs-lookup"><span data-stu-id="ee032-146">SasAmbientLight</span></span> | <span data-ttu-id="ee032-147">PointLight \[ ZeroOrMore \] ;</span><span class="sxs-lookup"><span data-stu-id="ee032-147">PointLight\[ZeroOrMore\];</span></span>                    |
|                                     | <span data-ttu-id="ee032-148">int</span><span class="sxs-lookup"><span data-stu-id="ee032-148">int</span></span>             | <span data-ttu-id="ee032-149">SAS. NumPointLights</span><span class="sxs-lookup"><span data-stu-id="ee032-149">Sas.NumPointLights</span></span>                           |
|                                     | <span data-ttu-id="ee032-150">SasAmbientLight</span><span class="sxs-lookup"><span data-stu-id="ee032-150">SasAmbientLight</span></span> | <span data-ttu-id="ee032-151">\[ZeroOrMore Spotlight \] ;</span><span class="sxs-lookup"><span data-stu-id="ee032-151">SpotLight\[ZeroOrMore\];</span></span>                     |
|                                     | <span data-ttu-id="ee032-152">int</span><span class="sxs-lookup"><span data-stu-id="ee032-152">int</span></span>             | <span data-ttu-id="ee032-153">SAS. NumSpotLights</span><span class="sxs-lookup"><span data-stu-id="ee032-153">Sas.NumSpotLights</span></span>                            |
| [<span data-ttu-id="ee032-154">Shadow</span><span class="sxs-lookup"><span data-stu-id="ee032-154">Shadow</span></span>](#shadow)                   | <span data-ttu-id="ee032-155">float4x4</span><span class="sxs-lookup"><span data-stu-id="ee032-155">float4x4</span></span>        | <span data-ttu-id="ee032-156">SAS. Shadow \[ ZeroOrMore \] . WorldToShadow</span><span class="sxs-lookup"><span data-stu-id="ee032-156">Sas.Shadow\[ZeroOrMore\].WorldToShadow</span></span>       |
|                                     | <span data-ttu-id="ee032-157">texture2D</span><span class="sxs-lookup"><span data-stu-id="ee032-157">texture2D</span></span>       | <span data-ttu-id="ee032-158">SAS. Shadow \[ ZeroOrMore \] . ShadowMap</span><span class="sxs-lookup"><span data-stu-id="ee032-158">Sas.Shadow\[ZeroOrMore\].ShadowMap</span></span>           |
| [<span data-ttu-id="ee032-159">Élémentaire</span><span class="sxs-lookup"><span data-stu-id="ee032-159">Skeleton</span></span>](#skeleton)               | <span data-ttu-id="ee032-160">float4x4</span><span class="sxs-lookup"><span data-stu-id="ee032-160">float4x4</span></span>        | <span data-ttu-id="ee032-161">SAS. Skeleton. MeshToJointToWorld \[ OneOrMore\]</span><span class="sxs-lookup"><span data-stu-id="ee032-161">Sas.Skeleton.MeshToJointToWorld\[OneOrMore\]</span></span> |
|                                     | <span data-ttu-id="ee032-162">int</span><span class="sxs-lookup"><span data-stu-id="ee032-162">int</span></span>             | <span data-ttu-id="ee032-163">SAS. squelette. NumJoints</span><span class="sxs-lookup"><span data-stu-id="ee032-163">Sas.Skeleton.NumJoints</span></span>                       |



 

### <a name="time"></a><span data-ttu-id="ee032-164">Temps</span><span class="sxs-lookup"><span data-stu-id="ee032-164">Time</span></span>

<span data-ttu-id="ee032-165">La valeur d’horloge virtuelle ou d’heure de l’application hôte.</span><span class="sxs-lookup"><span data-stu-id="ee032-165">The host application's virtual clock or time value.</span></span> <span data-ttu-id="ee032-166">Les membres sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="ee032-166">Members include:</span></span>

-   <span data-ttu-id="ee032-167">SAS. Time. Now : la valeur de l’horloge virtuelle de l’application hôte au point où l’effet sera rendu.</span><span class="sxs-lookup"><span data-stu-id="ee032-167">Sas.Time.Now - the value of the host application virtual clock at the point at which the effect will be rendered.</span></span>
-   <span data-ttu-id="ee032-168">SAS. Time. Last : la valeur de Now au rendu précédent.</span><span class="sxs-lookup"><span data-stu-id="ee032-168">Sas.Time.Last - the value of Now at the previous render.</span></span>
-   <span data-ttu-id="ee032-169">SAS. Time. FrameNumber : valeur de compteur incrémentée une fois par frame rendu.</span><span class="sxs-lookup"><span data-stu-id="ee032-169">Sas.Time.FrameNumber - the counter value that is incremented once per rendered frame.</span></span>

<span data-ttu-id="ee032-170">Les effets doivent correctement gérer le fait que les valeurs de ces membres peuvent éventuellement être encapsulées pendant des temps d’exécution très longs.</span><span class="sxs-lookup"><span data-stu-id="ee032-170">Effects must properly handle the fact that the values of these members can potentially wrap around during extremely long execution times.</span></span> <span data-ttu-id="ee032-171">Now et Last peuvent avoir des valeurs très élevées.</span><span class="sxs-lookup"><span data-stu-id="ee032-171">Now and Last may have very large values.</span></span>

### <a name="environment-map"></a><span data-ttu-id="ee032-172">Mappage d’environnement</span><span class="sxs-lookup"><span data-stu-id="ee032-172">Environment Map</span></span>

<span data-ttu-id="ee032-173">Carte d’environnement cubique.</span><span class="sxs-lookup"><span data-stu-id="ee032-173">A cubic environment map.</span></span> <span data-ttu-id="ee032-174">Les applications hôtes doivent fournir une texture de cube valide si un effet tente de se lier à SAS. EnvironmentMap.</span><span class="sxs-lookup"><span data-stu-id="ee032-174">Host applications must provide a valid cube texture if an effect attempts to bind to Sas.EnvironmentMap.</span></span>

### <a name="camera"></a><span data-ttu-id="ee032-175">Appareil photo</span><span class="sxs-lookup"><span data-stu-id="ee032-175">Camera</span></span>

<span data-ttu-id="ee032-176">Caméra actuellement affichée.</span><span class="sxs-lookup"><span data-stu-id="ee032-176">The camera currently being rendered.</span></span> <span data-ttu-id="ee032-177">Les membres sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="ee032-177">Members include:</span></span>

-   <span data-ttu-id="ee032-178">SAS. Camera. WorldToView : matrice de vue universelle composite pour l’appareil photo.</span><span class="sxs-lookup"><span data-stu-id="ee032-178">Sas.Camera.WorldToView - the composite world-view matrix for the camera.</span></span>
-   <span data-ttu-id="ee032-179">SAS. Camera. projection : matrice de projection pour l’appareil photo.</span><span class="sxs-lookup"><span data-stu-id="ee032-179">Sas.Camera.Projection - the projection matrix for the camera.</span></span>
-   <span data-ttu-id="ee032-180">SAS. Camera. NearFarClipping : valeurs des plans de découpage near et Far.</span><span class="sxs-lookup"><span data-stu-id="ee032-180">Sas.Camera.NearFarClipping - the values of the near and far clipping planes.</span></span>

### <a name="light"></a><span data-ttu-id="ee032-181">Clair</span><span class="sxs-lookup"><span data-stu-id="ee032-181">Light</span></span>

<span data-ttu-id="ee032-182">Une ou plusieurs lumières de scène.</span><span class="sxs-lookup"><span data-stu-id="ee032-182">One or more scene lights.</span></span> <span data-ttu-id="ee032-183">La collection d’éclairages est déclarée sous la forme d’un tableau où :</span><span class="sxs-lookup"><span data-stu-id="ee032-183">The collection of lights is declared as an array where:</span></span>

-   <span data-ttu-id="ee032-184">Color : couleur RVB.</span><span class="sxs-lookup"><span data-stu-id="ee032-184">Color - an RGB color.</span></span> <span data-ttu-id="ee032-185">La valeur par défaut est (0,0,0).</span><span class="sxs-lookup"><span data-stu-id="ee032-185">The default value is (0,0,0).</span></span>
-   <span data-ttu-id="ee032-186">Direction : direction de la lumière.</span><span class="sxs-lookup"><span data-stu-id="ee032-186">Direction - the light direction.</span></span> <span data-ttu-id="ee032-187">La valeur par défaut est (0,0,0).</span><span class="sxs-lookup"><span data-stu-id="ee032-187">The default value is (0,0,0).</span></span>
-   <span data-ttu-id="ee032-188">Plage : distance à partir de la lumière où les rayons lumineux n’ont aucun effet sur la scène.</span><span class="sxs-lookup"><span data-stu-id="ee032-188">Range - the distance from the light where the light rays have no effect on the scene.</span></span> <span data-ttu-id="ee032-189">La valeur par défaut est 0.</span><span class="sxs-lookup"><span data-stu-id="ee032-189">The default value is 0.</span></span>
-   <span data-ttu-id="ee032-190">Thêta-angle de cône interne d’une lumière concentrée, mesuré en radians.</span><span class="sxs-lookup"><span data-stu-id="ee032-190">Theta - the inner cone angle of a spotlight, measured in radians.</span></span> <span data-ttu-id="ee032-191">La valeur par défaut est 0.</span><span class="sxs-lookup"><span data-stu-id="ee032-191">The default value is 0.</span></span>
-   <span data-ttu-id="ee032-192">Phi : angle de cône externe d’une lumière concentrée, mesuré en radians.</span><span class="sxs-lookup"><span data-stu-id="ee032-192">Phi - the outer cone angle of a spotlight, measured in radians.</span></span> <span data-ttu-id="ee032-193">La valeur par défaut est 0.</span><span class="sxs-lookup"><span data-stu-id="ee032-193">The default value is 0.</span></span>

<span data-ttu-id="ee032-194">Le nombre d’indicateurs doit être défini sur le nombre d’éclairages liés au tableau associé.</span><span class="sxs-lookup"><span data-stu-id="ee032-194">The number of lights must be set to the number of lights bound into the associated array.</span></span> <span data-ttu-id="ee032-195">Les effets peuvent choisir d’ignorer le nombre d’éclairages et de se lier à n’importe quel élément de l’un des tableaux de la lumière.</span><span class="sxs-lookup"><span data-stu-id="ee032-195">Effects can choose to ignore the number of lights and bind to any element of one of the light arrays.</span></span> <span data-ttu-id="ee032-196">Par conséquent, les applications hôtes doivent fournir une liaison valide pour les éléments au-delà du nombre de lumières dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="ee032-196">Therefore, host applications must provide a valid binding for elements beyond the number of lights in the array.</span></span>

<span data-ttu-id="ee032-197">ZeroOrMore implique que le tableau peut avoir un nombre quelconque d’éléments.</span><span class="sxs-lookup"><span data-stu-id="ee032-197">ZeroOrMore implies that the array may have any number of elements.</span></span>

### <a name="shadow"></a><span data-ttu-id="ee032-198">Shadow</span><span class="sxs-lookup"><span data-stu-id="ee032-198">Shadow</span></span>

<span data-ttu-id="ee032-199">Les mémoires tampons secondaires qui se composent des éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="ee032-199">Shadow buffers which consists of:</span></span>

-   <span data-ttu-id="ee032-200">WorldToShadow : tableau de matrices.</span><span class="sxs-lookup"><span data-stu-id="ee032-200">WorldToShadow - an array of matrices.</span></span>
-   <span data-ttu-id="ee032-201">ShadowMap : fichier de texture 2D.</span><span class="sxs-lookup"><span data-stu-id="ee032-201">ShadowMap - a 2D texture file.</span></span>

<span data-ttu-id="ee032-202">ZeroOrMore implique que le tableau peut avoir n’importe quel nombre d’éléments (zéro correspond à un tableau vide).</span><span class="sxs-lookup"><span data-stu-id="ee032-202">ZeroOrMore implies that the array may have any number of elements (zero means an empty array).</span></span>

<span data-ttu-id="ee032-203">Un effet déclarerait un échantillonneur comme suit :</span><span class="sxs-lookup"><span data-stu-id="ee032-203">An effect would declare a sampler as follows:</span></span>


```
texture2D Shadow 
<
  string SasBindAddress = "Sas.Shadow[0].ShadowMap";
>;

sampler ShadowSampler = shadow_sampler(Shadow);
```



### <a name="skeleton"></a><span data-ttu-id="ee032-204">Élémentaire</span><span class="sxs-lookup"><span data-stu-id="ee032-204">Skeleton</span></span>

<span data-ttu-id="ee032-205">Ensemble des frames qui composent l’objet en cours de rendu.</span><span class="sxs-lookup"><span data-stu-id="ee032-205">The set of frames that compose the currently rendering object.</span></span> <span data-ttu-id="ee032-206">Les exemples de frame sont des segments et des transformations.</span><span class="sxs-lookup"><span data-stu-id="ee032-206">Frame examples are bones and transforms.</span></span> <span data-ttu-id="ee032-207">notamment :</span><span class="sxs-lookup"><span data-stu-id="ee032-207">This includes:</span></span>

-   <span data-ttu-id="ee032-208">MeshToJointToWorld : tableau de matrices.</span><span class="sxs-lookup"><span data-stu-id="ee032-208">MeshToJointToWorld - an array of matrices.</span></span>
-   <span data-ttu-id="ee032-209">NumJoints : nombre de jointures dans le squelette.</span><span class="sxs-lookup"><span data-stu-id="ee032-209">NumJoints - the number of joints in the skeleton.</span></span>

<span data-ttu-id="ee032-210">OneOrMore implique que le tableau a au moins un et peut contenir un nombre quelconque d’éléments.</span><span class="sxs-lookup"><span data-stu-id="ee032-210">OneOrMore implies that the array has at least one and may contain any number of elements.</span></span>

<span data-ttu-id="ee032-211">La définition prend en charge les objets de maillage rigides et dépouillés à l’aide du même ensemble de valeurs de [collection SasHostParameterValue](#sashostparametervalue-collection) avec une interprétation différente.</span><span class="sxs-lookup"><span data-stu-id="ee032-211">The definition supports both rigid and skinned mesh objects using the same set of [SasHostParameterValue Collection](#sashostparametervalue-collection) values with different interpretation.</span></span>

## <a name="sasbindaddress"></a><span data-ttu-id="ee032-212">SasBindAddress</span><span class="sxs-lookup"><span data-stu-id="ee032-212">SasBindAddress</span></span>

<span data-ttu-id="ee032-213">Cette annotation est ajoutée au début d’un fichier Effect pour associer un paramètre Effect à son paramètre correspondant défini dans la [collection SasHostParameterValue](#sashostparametervalue-collection).</span><span class="sxs-lookup"><span data-stu-id="ee032-213">This annotation is added to the top of an effect file to associate an effect parameter with its corresponding parameter defined in the [SasHostParameterValue Collection](#sashostparametervalue-collection).</span></span> <span data-ttu-id="ee032-214">L’annotation est déclarée comme suit :</span><span class="sxs-lookup"><span data-stu-id="ee032-214">The annotation is declared like this:</span></span>


```
string SasBindAddress = "SasHostParameterValue";
```



<span data-ttu-id="ee032-215">Cet exemple lie la matrice Effect World à la matrice MeshToJointToWorld :</span><span class="sxs-lookup"><span data-stu-id="ee032-215">This example binds the effect world matrix to the MeshToJointToWorld matrix:</span></span>


```
float4x3 World
<
  string SasBindAddress = "Sas.Skeleton.MeshToJointToWorld[0]";
>;
```



<span data-ttu-id="ee032-216">Cette annotation indique à l’application hôte qu’elle doit définir la valeur de la matrice d’effet universel à l’aide des données de la matrice MeshToJointToWorld.</span><span class="sxs-lookup"><span data-stu-id="ee032-216">This annotation tells the host application that it needs to set the value of the effect world matrix using the data in the MeshToJointToWorld matrix.</span></span>

<span data-ttu-id="ee032-217">La syntaxe d’annotation d’adresse de liaison a été définie pour être très similaire à la syntaxe utilisée par [**ID3DXEffect**](id3dxeffect.md) pour récupérer et définir des paramètres d’effet.</span><span class="sxs-lookup"><span data-stu-id="ee032-217">The bind address annotation syntax was defined to be very similar with the syntax used by [**ID3DXEffect**](id3dxeffect.md) to get and set effect parameters.</span></span> <span data-ttu-id="ee032-218">La seule différence entre les méthodes DXSAS et **ID3DXEffect** est l’ajout du jeton d’index astérisque.</span><span class="sxs-lookup"><span data-stu-id="ee032-218">The only difference between the DXSAS grammar and **ID3DXEffect** methods is the addition of the asterisk index token.</span></span> <span data-ttu-id="ee032-219">Voici un autre exemple d’utilisation de l’index d’astérisques :</span><span class="sxs-lookup"><span data-stu-id="ee032-219">Here is another example using the asterisk index:</span></span>


```
float3 LightColors[6]
<
  string SasBindAddress = "Sas.Light[*].Color";
>;
```



<span data-ttu-id="ee032-220">Le jeton d’index d’astérisque indique que tous les éléments du tableau de valeurs envirnmant de l’hôte particulier (couleur dans ce cas) doivent être liés dans le paramètre associé.</span><span class="sxs-lookup"><span data-stu-id="ee032-220">The asterisk index token denotes that all elements of the particular host envirnmant value array (color in this case) should be bound in the associated parameter.</span></span> <span data-ttu-id="ee032-221">Plusieurs jetons d’index d’astérisques permettent de lier des effets à des sous-éléments d’un tableau de structures sans avoir à lier la totalité de la structure elle-même.</span><span class="sxs-lookup"><span data-stu-id="ee032-221">Multiple asterisk index tokens allow effects to bind to sub-elements of an array of structures without the need to bind the entire structure itself.</span></span> <span data-ttu-id="ee032-222">Cet exemple lie les valeurs de couleur des six premières lumières à un paramètre d’effet.</span><span class="sxs-lookup"><span data-stu-id="ee032-222">This example binds the color values of the first six lights to an effect parameter.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ee032-223">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ee032-223">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ee032-224">Informations de référence sur les annotations et sémantiques DirectX standard</span><span class="sxs-lookup"><span data-stu-id="ee032-224">DirectX Standard Annotations and Semantics Reference</span></span>](dx9-graphics-reference-effects-dxsas.md)
</dt> </dl>

 

 



