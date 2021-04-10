---
description: Cette page vous indique comment générer et utiliser un effet.
ms.assetid: d9fdafed-5958-4995-a1b5-8881feca1291
title: Utilisation d’un effet (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1170fde625e5eee5e9665f0759d302b5f5450a41
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109883"
---
# <a name="using-an-effect-direct3d-9"></a><span data-ttu-id="53a86-103">Utilisation d’un effet (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="53a86-103">Using an Effect (Direct3D 9)</span></span>

<span data-ttu-id="53a86-104">Cette page vous indique comment générer et utiliser un effet.</span><span class="sxs-lookup"><span data-stu-id="53a86-104">This page will show you how to generate and use an effect.</span></span> <span data-ttu-id="53a86-105">Les sujets abordés sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="53a86-105">The topics covered include how to:</span></span>

-   [<span data-ttu-id="53a86-106">Créer un effet</span><span class="sxs-lookup"><span data-stu-id="53a86-106">Create an Effect</span></span>](#create-an-effect)
-   [<span data-ttu-id="53a86-107">Rendu d’un effet</span><span class="sxs-lookup"><span data-stu-id="53a86-107">Render an Effect</span></span>](#render-an-effect)
-   [<span data-ttu-id="53a86-108">Utiliser la sémantique pour rechercher les paramètres d’effet</span><span class="sxs-lookup"><span data-stu-id="53a86-108">Use Semantics to Find Effect Parameters</span></span>](#use-semantics-to-find-effect-parameters)
-   [<span data-ttu-id="53a86-109">Utiliser des handles pour récupérer et définir des paramètres efficacement</span><span class="sxs-lookup"><span data-stu-id="53a86-109">Use Handles to Get and Set Parameters Efficiently</span></span>](#use-handles-to-get-and-set-parameters-efficiently)
-   [<span data-ttu-id="53a86-110">Ajouter des informations sur les paramètres avec des annotations</span><span class="sxs-lookup"><span data-stu-id="53a86-110">Add Parameter Information with Annotations</span></span>](#add-parameter-information-with-annotations)
-   [<span data-ttu-id="53a86-111">Paramètres d’effet de partage</span><span class="sxs-lookup"><span data-stu-id="53a86-111">Share Effect Parameters</span></span>](#share-effect-parameters)
-   [<span data-ttu-id="53a86-112">Compiler un effet hors connexion</span><span class="sxs-lookup"><span data-stu-id="53a86-112">Compile an Effect Offline</span></span>](#compile-an-effect-offline)
-   [<span data-ttu-id="53a86-113">Améliorer les performances avec des prénuanceurs</span><span class="sxs-lookup"><span data-stu-id="53a86-113">Improve Performance with Preshaders</span></span>](#improve-performance-with-preshaders)
-   [<span data-ttu-id="53a86-114">Utiliser des blocs de paramètres pour gérer les paramètres d’effet</span><span class="sxs-lookup"><span data-stu-id="53a86-114">Use Parameter Blocks to Manage Effect Parameters</span></span>](#use-parameter-blocks-to-manage-effect-parameters)

## <a name="create-an-effect"></a><span data-ttu-id="53a86-115">Créer un effet</span><span class="sxs-lookup"><span data-stu-id="53a86-115">Create an Effect</span></span>

<span data-ttu-id="53a86-116">Voici un exemple de création d’un effet tiré de l' [exemple BasicHLSL](../directx-sdk--august-2009-.md).</span><span class="sxs-lookup"><span data-stu-id="53a86-116">Here is an example of creating an effect taken from the [BasicHLSL Sample](../directx-sdk--august-2009-.md).</span></span> <span data-ttu-id="53a86-117">Le code de création de l’effet pour la création d’un nuanceur de débogage provient de **OnCreateDevice**:</span><span class="sxs-lookup"><span data-stu-id="53a86-117">The effect creation code for creating a debug shader is from **OnCreateDevice**:</span></span>


```
ID3DXEffect* g_pEffect = NULL;
DWORD dwShaderFlags = 0;

    dwShaderFlags |= D3DXSHADER_FORCE_VS_SOFTWARE_NOOPT;
    dwShaderFlags |= D3DXSHADER_FORCE_PS_SOFTWARE_NOOPT;
    dwShaderFlags |= D3DXSHADER_NO_PRESHADER;

    // Read the D3DX effect file
    WCHAR str[MAX_PATH];
    DXUTFindDXSDKMediaFileCch( str, MAX_PATH, L"BasicHLSL.fx" );

    D3DXCreateEffectFromFile( 
        pd3dDevice, 
        str, 
        NULL, // CONST D3DXMACRO* pDefines,
        NULL, // LPD3DXINCLUDE pInclude,
        dwShaderFlags, 
        NULL, // LPD3DXEFFECTPOOL pPool,
        &g_pEffect, 
        NULL );
```



<span data-ttu-id="53a86-118">Cette fonction accepte les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="53a86-118">This function takes these arguments:</span></span>

-   <span data-ttu-id="53a86-119">Périphérique.</span><span class="sxs-lookup"><span data-stu-id="53a86-119">The device.</span></span>
-   <span data-ttu-id="53a86-120">Nom de fichier du fichier d’effet.</span><span class="sxs-lookup"><span data-stu-id="53a86-120">The file name of the effect file.</span></span>
-   <span data-ttu-id="53a86-121">Pointeur vers une liste de définitions se terminant par un caractère NULL \# , à utiliser lors de l’analyse du nuanceur.</span><span class="sxs-lookup"><span data-stu-id="53a86-121">A pointer to a NULL-terminated list of \#defines, to be used while parsing the shader.</span></span>
-   <span data-ttu-id="53a86-122">Pointeur facultatif vers un gestionnaire d’inclusion écrit par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="53a86-122">An optional pointer to a user-written include handler.</span></span> <span data-ttu-id="53a86-123">Le gestionnaire est appelé par le processeur à chaque fois qu’il doit résoudre un \# include.</span><span class="sxs-lookup"><span data-stu-id="53a86-123">The handler is called by the processor whenever it needs to resolve a \#include.</span></span>
-   <span data-ttu-id="53a86-124">Indicateur de compilation de nuanceur qui fournit aux indicateurs du compilateur la manière dont le nuanceur sera utilisé.</span><span class="sxs-lookup"><span data-stu-id="53a86-124">A shader compile flag that gives the compiler hints about how the shader will be used.</span></span> <span data-ttu-id="53a86-125">Ces options sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="53a86-125">The options include:</span></span>
    -   <span data-ttu-id="53a86-126">La validation est ignorée, si des nuanceurs corrects connus sont en cours de compilation.</span><span class="sxs-lookup"><span data-stu-id="53a86-126">Skipping validation, if known good shaders are being compiled.</span></span>
    -   <span data-ttu-id="53a86-127">L’optimisation est ignorée (parfois utilisée lorsque les optimisations compliquent le débogage).</span><span class="sxs-lookup"><span data-stu-id="53a86-127">Skipping optimization (sometimes used when optimizations make debugging harder).</span></span>
    -   <span data-ttu-id="53a86-128">Demande d’inclure des informations de débogage dans le nuanceur afin de pouvoir les déboguer.</span><span class="sxs-lookup"><span data-stu-id="53a86-128">Requesting debug information to be included in the shader so it can be debugged.</span></span>
-   <span data-ttu-id="53a86-129">Pool d’effets.</span><span class="sxs-lookup"><span data-stu-id="53a86-129">The effect pool.</span></span> <span data-ttu-id="53a86-130">Si plusieurs effets utilisent le même pointeur de pool de mémoire, les variables globales dans les effets sont partagées les unes avec les autres.</span><span class="sxs-lookup"><span data-stu-id="53a86-130">If more than one effect uses the same memory pool pointer, the global variables in the effects are shared with each other.</span></span> <span data-ttu-id="53a86-131">Si vous n’avez pas besoin de partager des variables d’effet, le pool de mémoire peut être défini sur la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="53a86-131">If there is no need to share effect variables, the memory pool can be set to **NULL**.</span></span>
-   <span data-ttu-id="53a86-132">Pointeur vers le nouvel effet.</span><span class="sxs-lookup"><span data-stu-id="53a86-132">A pointer to the new effect.</span></span>
-   <span data-ttu-id="53a86-133">Pointeur vers une mémoire tampon dans laquelle les erreurs de validation peuvent être envoyées.</span><span class="sxs-lookup"><span data-stu-id="53a86-133">A pointer to a buffer to which validation errors can be sent.</span></span> <span data-ttu-id="53a86-134">Dans cet exemple, le paramètre a la valeur **null** et n’est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="53a86-134">In this example, the parameter was set to **NULL** and not used.</span></span>

> [!Note]  
> <span data-ttu-id="53a86-135">À partir du kit de développement logiciel (SDK) 2006 du mois de décembre, le compilateur HLSL DirectX 10 est désormais le compilateur par défaut dans DirectX 9 et DirectX 10.</span><span class="sxs-lookup"><span data-stu-id="53a86-135">Beginning with the December 2006 SDK, the DirectX 10 HLSL compiler is now the default compiler in both DirectX 9 and DirectX 10.</span></span> <span data-ttu-id="53a86-136">Pour plus d’informations [, consultez outil de compilateur Effect](../direct3dtools/fxc.md) .</span><span class="sxs-lookup"><span data-stu-id="53a86-136">See [Effect-Compiler Tool](../direct3dtools/fxc.md) for details.</span></span>

 

## <a name="render-an-effect"></a><span data-ttu-id="53a86-137">Rendu d’un effet</span><span class="sxs-lookup"><span data-stu-id="53a86-137">Render an Effect</span></span>

<span data-ttu-id="53a86-138">La séquence d’appels pour l’application de l’état d’effet à un appareil est la suivante :</span><span class="sxs-lookup"><span data-stu-id="53a86-138">The sequence of calls for applying effect state to a device is:</span></span>

-   <span data-ttu-id="53a86-139">[**ID3DXEffect :: Begin**](id3dxeffect--begin.md) définit la technique active.</span><span class="sxs-lookup"><span data-stu-id="53a86-139">[**ID3DXEffect::Begin**](id3dxeffect--begin.md) sets the active technique.</span></span>
-   <span data-ttu-id="53a86-140">[**ID3DXEffect :: BeginPass**](id3dxeffect--beginpass.md) définit la passe active.</span><span class="sxs-lookup"><span data-stu-id="53a86-140">[**ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md) sets the active pass.</span></span>
-   <span data-ttu-id="53a86-141">[**ID3DXEffect :: CommitChanges**](id3dxeffect--commitchanges.md) met à jour les modifications apportées aux appels définis dans la passe.</span><span class="sxs-lookup"><span data-stu-id="53a86-141">[**ID3DXEffect::CommitChanges**](id3dxeffect--commitchanges.md) updates changes to any set calls in the pass.</span></span> <span data-ttu-id="53a86-142">Cette méthode doit être appelée avant tout appel de dessin.</span><span class="sxs-lookup"><span data-stu-id="53a86-142">This should be called before any draw call.</span></span>
-   <span data-ttu-id="53a86-143">[**ID3DXEffect :: EndPass**](id3dxeffect--endpass.md) termine une passe.</span><span class="sxs-lookup"><span data-stu-id="53a86-143">[**ID3DXEffect::EndPass**](id3dxeffect--endpass.md) ends a pass.</span></span>
-   <span data-ttu-id="53a86-144">[**ID3DXEffect :: end**](id3dxeffect--end.md) termine la technique active.</span><span class="sxs-lookup"><span data-stu-id="53a86-144">[**ID3DXEffect::End**](id3dxeffect--end.md) ends the active technique.</span></span>

<span data-ttu-id="53a86-145">Le code d’effet de rendu est également plus simple que le code de rendu correspondant sans effet.</span><span class="sxs-lookup"><span data-stu-id="53a86-145">Effect render code is also simpler than the corresponding render code without an effect.</span></span> <span data-ttu-id="53a86-146">Voici le code de rendu ayant un effet :</span><span class="sxs-lookup"><span data-stu-id="53a86-146">Here's the render code with an effect:</span></span>


```
// Apply the technique contained in the effect 
g_pEffect->Begin(&cPasses, 0);

for (iPass = 0; iPass < cPasses; iPass++)
{
    g_pEffect->BeginPass(iPass);

    // Only call CommitChanges if any state changes have happened
    // after BeginPass is called
    g_pEffect->CommitChanges();

    // Render the mesh with the applied technique
    g_pMesh->DrawSubset(0);

    g_pEffect->EndPass();
}
g_pEffect->End();
```



<span data-ttu-id="53a86-147">La boucle de rendu consiste à interroger l’effet pour voir le nombre de passes qu’il contient, puis à appeler toutes les passes pour une technique.</span><span class="sxs-lookup"><span data-stu-id="53a86-147">The render loop consists of querying the effect to see how many passes it contains, and then calling all the passes for a technique.</span></span> <span data-ttu-id="53a86-148">La boucle de rendu peut être développée pour appeler plusieurs techniques, chacune avec plusieurs passes.</span><span class="sxs-lookup"><span data-stu-id="53a86-148">The render loop could be expanded to call multiple techniques, each with multiple passes.</span></span>

## <a name="use-semantics-to-find-effect-parameters"></a><span data-ttu-id="53a86-149">Utiliser la sémantique pour rechercher les paramètres d’effet</span><span class="sxs-lookup"><span data-stu-id="53a86-149">Use Semantics to Find Effect Parameters</span></span>

<span data-ttu-id="53a86-150">Une sémantique est un identificateur attaché à un paramètre Effect pour permettre à une application de rechercher le paramètre.</span><span class="sxs-lookup"><span data-stu-id="53a86-150">A semantic is an identifier that is attached to an effect parameter to allow an application to search for the parameter.</span></span> <span data-ttu-id="53a86-151">Un paramètre ne peut avoir qu’une seule sémantique.</span><span class="sxs-lookup"><span data-stu-id="53a86-151">A parameter can have at most one semantic.</span></span> <span data-ttu-id="53a86-152">La sémantique se trouve à la suite d’un signe deux-points ( :) après le nom du paramètre.</span><span class="sxs-lookup"><span data-stu-id="53a86-152">The semantic is located following a colon (:) after the parameter name.</span></span> <span data-ttu-id="53a86-153">Exemple :</span><span class="sxs-lookup"><span data-stu-id="53a86-153">For instance:</span></span>


```
float4x4 matWorldViewProj : WORLDVIEWPROJ;
```



<span data-ttu-id="53a86-154">Si vous avez déclaré la variable globale Effect sans utiliser de sémantique, elle ressemble à ceci :</span><span class="sxs-lookup"><span data-stu-id="53a86-154">If you declared the effect global variable without using a semantic, it would look like this instead:</span></span>


```
float4x4 matWorldViewProj;
```



<span data-ttu-id="53a86-155">L’interface Effect peut utiliser une sémantique pour obtenir un handle à un paramètre d’effet particulier.</span><span class="sxs-lookup"><span data-stu-id="53a86-155">The effect interface can use a semantic to get a handle to a particular effect parameter.</span></span> <span data-ttu-id="53a86-156">Par exemple, le code suivant retourne le handle de la matrice :</span><span class="sxs-lookup"><span data-stu-id="53a86-156">For instance, the following returns the handle of the matrix:</span></span>


```
D3DHANDLE handle = 
    m_pEffect->GetParameterBySemantic(NULL, "WORLDVIEWPROJ");
```



<span data-ttu-id="53a86-157">En plus de la recherche par nom sémantique, l’interface Effect possède de nombreuses autres méthodes pour rechercher des paramètres.</span><span class="sxs-lookup"><span data-stu-id="53a86-157">In addition to searching by semantic name, the effect interface has many other methods to search for parameters.</span></span>

## <a name="use-handles-to-get-and-set-parameters-efficiently"></a><span data-ttu-id="53a86-158">Utiliser des handles pour récupérer et définir des paramètres efficacement</span><span class="sxs-lookup"><span data-stu-id="53a86-158">Use Handles to Get and Set Parameters Efficiently</span></span>

<span data-ttu-id="53a86-159">Les handles offrent un moyen efficace de faire référence à des paramètres d’effet, des techniques, des passes et des annotations avec un effet.</span><span class="sxs-lookup"><span data-stu-id="53a86-159">Handles provide an efficient means for referencing effect parameters, techniques, passes, and annotations with an effect.</span></span> <span data-ttu-id="53a86-160">Les handles (qui sont de type D3DXHANDLE) sont des pointeurs de chaîne.</span><span class="sxs-lookup"><span data-stu-id="53a86-160">Handles (which are of type D3DXHANDLE) are string pointers.</span></span> <span data-ttu-id="53a86-161">Les handles passés dans des fonctions telles que GetParameterxxx ou GetAnnotationxxx peuvent se présenter sous l’une des trois formes suivantes :</span><span class="sxs-lookup"><span data-stu-id="53a86-161">The handles that are passed into functions such as GetParameterxxx or GetAnnotationxxx can be in one of three forms:</span></span>

-   <span data-ttu-id="53a86-162">Handle retourné par une fonction telle que GetParameterxxx.</span><span class="sxs-lookup"><span data-stu-id="53a86-162">A handle returned by a function such as GetParameterxxx.</span></span>
-   <span data-ttu-id="53a86-163">Chaîne contenant le nom du paramètre, de la technique, de la passe ou de l’annotation.</span><span class="sxs-lookup"><span data-stu-id="53a86-163">A string containing the name of the parameter, technique, pass, or annotation.</span></span>
-   <span data-ttu-id="53a86-164">Handle ayant la valeur **null**.</span><span class="sxs-lookup"><span data-stu-id="53a86-164">A handle set to **NULL**.</span></span>

<span data-ttu-id="53a86-165">Cet exemple retourne un handle au paramètre auquel la sémantique WORLDVIEWPROJ est attachée :</span><span class="sxs-lookup"><span data-stu-id="53a86-165">This example returns a handle to the parameter that has the WORLDVIEWPROJ semantic attached to it:</span></span>


```
D3DHANDLE handle = 
    m_pEffect->GetParameterBySemantic(NULL, "WORLDVIEWPROJ");
```



## <a name="add-parameter-information-with-annotations"></a><span data-ttu-id="53a86-166">Ajouter des informations sur les paramètres avec des annotations</span><span class="sxs-lookup"><span data-stu-id="53a86-166">Add Parameter Information with Annotations</span></span>

<span data-ttu-id="53a86-167">Les annotations sont des données spécifiques à l’utilisateur qui peuvent être attachées à n’importe quelle technique, passe ou paramètre.</span><span class="sxs-lookup"><span data-stu-id="53a86-167">Annotations are user-specific data that can be attached to any technique, pass, or parameter.</span></span> <span data-ttu-id="53a86-168">Une annotation est un moyen flexible d’ajouter des informations à des paramètres individuels.</span><span class="sxs-lookup"><span data-stu-id="53a86-168">An annotation is a flexible way to add information to individual parameters.</span></span> <span data-ttu-id="53a86-169">Les informations peuvent être lues et utilisées de la manière choisie par l’application.</span><span class="sxs-lookup"><span data-stu-id="53a86-169">The information can be read back and used any way the application chooses.</span></span> <span data-ttu-id="53a86-170">Une annotation peut être de n’importe quel type de données et peut être ajoutée dynamiquement.</span><span class="sxs-lookup"><span data-stu-id="53a86-170">An annotation can be of any data type and can be added dynamically.</span></span> <span data-ttu-id="53a86-171">Les déclarations d’annotation sont délimitées par des crochets pointus.</span><span class="sxs-lookup"><span data-stu-id="53a86-171">Annotation declarations are delimited by angle brackets.</span></span> <span data-ttu-id="53a86-172">Une annotation contient les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="53a86-172">An annotation contains:</span></span>

-   <span data-ttu-id="53a86-173">Type de données.</span><span class="sxs-lookup"><span data-stu-id="53a86-173">A data type.</span></span>
-   <span data-ttu-id="53a86-174">Nom de variable.</span><span class="sxs-lookup"><span data-stu-id="53a86-174">A variable name.</span></span>
-   <span data-ttu-id="53a86-175">Signe égal (=).</span><span class="sxs-lookup"><span data-stu-id="53a86-175">An equals sign (=).</span></span>
-   <span data-ttu-id="53a86-176">Valeur de données.</span><span class="sxs-lookup"><span data-stu-id="53a86-176">The data value.</span></span>
-   <span data-ttu-id="53a86-177">Point-virgule de fin (;).</span><span class="sxs-lookup"><span data-stu-id="53a86-177">A ending semicolon (;).</span></span>

<span data-ttu-id="53a86-178">Par exemple, les deux exemples précédents de ce document contiennent cette annotation :</span><span class="sxs-lookup"><span data-stu-id="53a86-178">For instance, both of the previous examples in this paper contain this annotation:</span></span>


```
texture Tex0 < string name = "tiger.bmp"; >;
```



<span data-ttu-id="53a86-179">L’annotation est attachée à l’objet texture et spécifie le fichier de texture qui doit être utilisé pour initialiser l’objet texture.</span><span class="sxs-lookup"><span data-stu-id="53a86-179">The annotation is attached to the texture object and specifies the texture file that should be used to initialize the texture object.</span></span> <span data-ttu-id="53a86-180">L’annotation n’initialise pas l’objet texture, il s’agit simplement d’une partie des informations utilisateur jointes à la variable.</span><span class="sxs-lookup"><span data-stu-id="53a86-180">The annotation does not initialize the texture object, it is simply a piece of user information that is attached to the variable.</span></span> <span data-ttu-id="53a86-181">Une application peut lire l’annotation avec [**ID3DXBaseEffect :: GetAnnotation**](id3dxbaseeffect--getannotation.md) ou [**ID3DXBaseEffect :: GetAnnotationByName**](id3dxbaseeffect--getannotationbyname.md) pour retourner la chaîne.</span><span class="sxs-lookup"><span data-stu-id="53a86-181">An application can read the annotation with either [**ID3DXBaseEffect::GetAnnotation**](id3dxbaseeffect--getannotation.md) or [**ID3DXBaseEffect::GetAnnotationByName**](id3dxbaseeffect--getannotationbyname.md) to return the string.</span></span> <span data-ttu-id="53a86-182">Les annotations peuvent également être ajoutées par l’application.</span><span class="sxs-lookup"><span data-stu-id="53a86-182">Annotations can also be added by the application.</span></span>

<span data-ttu-id="53a86-183">Chaque annotation :</span><span class="sxs-lookup"><span data-stu-id="53a86-183">Each annotation:</span></span>

-   <span data-ttu-id="53a86-184">Doit être de type numeric ou Strings.</span><span class="sxs-lookup"><span data-stu-id="53a86-184">Must be either numeric or strings.</span></span>
-   <span data-ttu-id="53a86-185">Doit toujours être initialisé avec une valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="53a86-185">Must always be initialized with a default value.</span></span>
-   <span data-ttu-id="53a86-186">Peut être associé à des [techniques et des passes (Direct3D 9)](techniques-and-passes.md) et à des [paramètres d’effet](/previous-versions/windows/desktop/ee417539(v=vs.85))de niveau supérieur.</span><span class="sxs-lookup"><span data-stu-id="53a86-186">Can be associated with [Techniques and Passes (Direct3D 9)](techniques-and-passes.md) and top-level [Effect Parameters](/previous-versions/windows/desktop/ee417539(v=vs.85)).</span></span>
-   <span data-ttu-id="53a86-187">Peut être écrit et lu à l’aide de [**ID3DXEffect**](id3dxeffect.md) ou de [**ID3DXEffectCompiler**](id3dxeffectcompiler.md).</span><span class="sxs-lookup"><span data-stu-id="53a86-187">Can be written to and read from with either [**ID3DXEffect**](id3dxeffect.md) or [**ID3DXEffectCompiler**](id3dxeffectcompiler.md).</span></span>
-   <span data-ttu-id="53a86-188">Peut être ajouté avec [**ID3DXEffect**](id3dxeffect.md).</span><span class="sxs-lookup"><span data-stu-id="53a86-188">Can be added with [**ID3DXEffect**](id3dxeffect.md).</span></span>
-   <span data-ttu-id="53a86-189">Ne peut pas être référencé à l’intérieur de l’effet.</span><span class="sxs-lookup"><span data-stu-id="53a86-189">Cannot be referenced inside the effect.</span></span>
-   <span data-ttu-id="53a86-190">Impossible d’avoir des sous-sémantiques ou des sous-annotations.</span><span class="sxs-lookup"><span data-stu-id="53a86-190">Cannot have sub-semantics or sub-annotations.</span></span>

## <a name="share-effect-parameters"></a><span data-ttu-id="53a86-191">Paramètres d’effet de partage</span><span class="sxs-lookup"><span data-stu-id="53a86-191">Share Effect Parameters</span></span>

<span data-ttu-id="53a86-192">Les paramètres Effects sont toutes les variables non statiques déclarées dans un effet.</span><span class="sxs-lookup"><span data-stu-id="53a86-192">Effect parameters are all the non-static variables declared in an effect.</span></span> <span data-ttu-id="53a86-193">Cela peut inclure des variables globales et des annotations.</span><span class="sxs-lookup"><span data-stu-id="53a86-193">This can include global variables and annotations.</span></span> <span data-ttu-id="53a86-194">Les paramètres Effects peuvent être partagés entre différents effets en déclarant des paramètres avec le mot clé « Shared », puis en créant l’effet avec un pool d’effets.</span><span class="sxs-lookup"><span data-stu-id="53a86-194">Effect parameters can be shared between different effects by declaring parameters with the "shared" keyword and then creating the effect with an effect pool.</span></span>

<span data-ttu-id="53a86-195">Un pool d’effets contient des paramètres d’effet partagé.</span><span class="sxs-lookup"><span data-stu-id="53a86-195">An effect pool contains shared effect parameters.</span></span> <span data-ttu-id="53a86-196">Le pool est créé en appelant [**D3DXCreateEffectPool**](d3dxcreateeffectpool.md), qui retourne une interface [**ID3DXEffectPool**](id3dxeffectpool.md) .</span><span class="sxs-lookup"><span data-stu-id="53a86-196">The pool is created by calling [**D3DXCreateEffectPool**](d3dxcreateeffectpool.md), which returns an [**ID3DXEffectPool**](id3dxeffectpool.md) interface.</span></span> <span data-ttu-id="53a86-197">L’interface peut être fournie en tant qu’entrée à l’une des fonctions D3DXCreateEffectxxx lors de la création d’un effet.</span><span class="sxs-lookup"><span data-stu-id="53a86-197">The interface can be supplied as an input to any of the D3DXCreateEffectxxx functions when an effect is created.</span></span> <span data-ttu-id="53a86-198">Pour qu’un paramètre soit partagé entre plusieurs effets, le paramètre doit avoir le même nom, le même type et la même sémantique dans chacun des effets partagés.</span><span class="sxs-lookup"><span data-stu-id="53a86-198">For a parameter to be shared across multiple effects, the parameter must have the same name, type, and semantic in each of the shared effects.</span></span>


```
ID3DXEffectPool* g_pEffectPool = NULL;   // Effect pool for sharing parameters

    D3DXCreateEffectPool( &g_pEffectPool );
```



<span data-ttu-id="53a86-199">Les effets qui partagent des paramètres doivent utiliser le même appareil.</span><span class="sxs-lookup"><span data-stu-id="53a86-199">Effects that share parameters must use the same device.</span></span> <span data-ttu-id="53a86-200">Cela est appliqué pour empêcher le partage des paramètres dépendants du périphérique (tels que les nuanceurs ou les textures) sur différents appareils.</span><span class="sxs-lookup"><span data-stu-id="53a86-200">This is enforced to prevent the sharing of device-dependent parameters (such as shaders or textures) across different devices.</span></span> <span data-ttu-id="53a86-201">Les paramètres sont supprimés du pool chaque fois que les effets qui contiennent les paramètres partagés sont libérés.</span><span class="sxs-lookup"><span data-stu-id="53a86-201">Parameters are deleted from the pool whenever the effects that contain the shared parameters are released.</span></span> <span data-ttu-id="53a86-202">Si les paramètres de partage ne sont pas nécessaires, fournissez la **valeur null** pour le pool d’effets lorsqu’un effet est créé.</span><span class="sxs-lookup"><span data-stu-id="53a86-202">If sharing parameters is not necessary, supply **NULL** for the effect pool when an effect is created.</span></span>

<span data-ttu-id="53a86-203">Les effets clonés utilisent le même pool d’effets que l’effet à partir duquel ils sont clonés.</span><span class="sxs-lookup"><span data-stu-id="53a86-203">Cloned effects use the same effect pool as the effect from which they are cloned.</span></span> <span data-ttu-id="53a86-204">Le clonage d’un effet fait une copie exacte d’un effet, y compris les variables globales, les techniques, les passes et les annotations.</span><span class="sxs-lookup"><span data-stu-id="53a86-204">Cloning an effect makes an exact copy of an effect, including global variables, techniques, passes, and annotations.</span></span>

## <a name="compile-an-effect-offline"></a><span data-ttu-id="53a86-205">Compiler un effet hors connexion</span><span class="sxs-lookup"><span data-stu-id="53a86-205">Compile an Effect Offline</span></span>

<span data-ttu-id="53a86-206">Vous pouvez compiler un effet au moment de l’exécution avec [**D3DXCreateEffect**](d3dxcreateeffect.md), ou vous pouvez compiler un effet hors connexion à l’aide de l’outil de compilateur de ligne de commande fxc.exe.</span><span class="sxs-lookup"><span data-stu-id="53a86-206">You can compile an effect at run time with [**D3DXCreateEffect**](d3dxcreateeffect.md), or you can compile an effect offline using the command-line compiler tool fxc.exe.</span></span> <span data-ttu-id="53a86-207">L’effet de l' [exemple CompiledEffect](https://msdn.microsoft.com/library/Ee416326(v=VS.85).aspx) contient un nuanceur de sommets, un nuanceur de pixels et une technique :</span><span class="sxs-lookup"><span data-stu-id="53a86-207">The effect in the [CompiledEffect Sample](https://msdn.microsoft.com/library/Ee416326(v=VS.85).aspx) contains a vertex shader, a pixel shader, and one technique:</span></span>


```
// File: CompiledEffect.fx

// Global variables
float4 g_MaterialAmbientColor;    // Material's ambient color
...

// Texture samplers
sampler RenderTargetSampler = 
   ...

// Type: Vertex shader                                      
VS_OUTPUT RenderSceneVS( float4 vPos : POSITION, 
                         float3 vNormal : NORMAL,
                         float2 vTexCoord0 : TEXCOORD0 )
{
   ...
};
// Type: Pixel shader
PS_OUTPUT RenderScenePS( VS_OUTPUT In ) 
{ 
   ...
}

// Type: Technique                                     
technique RenderScene
{
    pass P0
    {          
        ZENABLE = true;
        VertexShader = compile vs_1_1 RenderSceneVS();
        PixelShader  = compile ps_1_1 RenderScenePS();
    }
}
```



<span data-ttu-id="53a86-208">L’utilisation de l' [outil Effect-compiler Tool](../direct3dtools/fxc.md) pour compiler le nuanceur pour vs \_ 1 \_ 1 a généré les instructions de nuanceur d’assembly suivantes :</span><span class="sxs-lookup"><span data-stu-id="53a86-208">Using [Effect-Compiler Tool](../direct3dtools/fxc.md) to compile the shader for vs\_1\_1 generated the following assembly shader instructions:</span></span>


```
//
// Generated by Microsoft (R) D3DX9 Shader Compiler 4.09.02.1188
//
//   fxc /T vs_1_1 /E RenderSceneVS /Fc CompiledEffect.txt CompiledEffect.fx
//
//
// Parameters:
//
//   float4 g_LightAmbient;
//   float4 g_LightDiffuse;
//   float3 g_LightDir;
//   float4 g_MaterialAmbientColor;
//   float4 g_MaterialDiffuseColor;
//   float g_fTime;
//   float4x4 g_mWorld;
//   float4x4 g_mWorldViewProjection;
//
//
// Registers:
//
//   Name                   Reg   Size
//   ---------------------- ----- ----
//   g_mWorldViewProjection c0       4
//   g_mWorld               c4       3
//   g_MaterialAmbientColor c7       1
//   g_MaterialDiffuseColor c8       1
//   g_LightDir             c9       1
//   g_LightAmbient         c10      1
//   g_LightDiffuse         c11      1
//   g_fTime                c12      1
//
//
// Default values:
//
//   g_LightDir
//     c9   = { 0.57735, 0.57735, 0.57735, 0 };
//
//   g_LightAmbient
//     c10  = { 1, 1, 1, 1 };
//
//   g_LightDiffuse
//     c11  = { 1, 1, 1, 1 };
//

    vs_1_1
    def c13, 0.159154937, 0.25, 6.28318548, -3.14159274
    def c14, -2.52398507e-007, 2.47609005e-005, -0.00138883968, 0.0416666418
    def c15, -0.5, 1, 0.5, 0
    dcl_position v0
    dcl_normal v1
    dcl_texcoord v2
    mov r0.w, c12.x
    mad r0.w, r0.w, c13.x, c13.y
    expp r3.y, r0.w
    mov r0.w, r3.y
    mad r0.w, r0.w, c13.z, c13.w
    mul r0.w, r0.w, r0.w
    mad r1.w, r0.w, c14.x, c14.y
    mad r1.w, r0.w, r1.w, c14.z
    mad r1.w, r0.w, r1.w, c14.w
    mad r1.w, r0.w, r1.w, c15.x
    mad r0.w, r0.w, r1.w, c15.y
    mul r0.w, r0.w, v0.x
    mul r0.x, r0.w, c15.z
    dp3 r1.x, v1, c4
    dp3 r1.y, v1, c5
    dp3 r1.z, v1, c6
    mov r0.yzw, c15.w
    dp3 r2.x, r1, r1
    add r0, r0, v0
    rsq r1.w, r2.x
    dp4 oPos.x, r0, c0
    mul r1.xyz, r1, r1.w
    dp4 oPos.y, r0, c1
    dp3 r1.x, r1, c9
    dp4 oPos.z, r0, c2
    max r1.w, r1.x, c15.w
    mov r1.xyz, c8
    mul r1.xyz, r1, c11
    mov r2.xyz, c7
    mul r2.xyz, r2, c10
    dp4 oPos.w, r0, c3
    mad oD0.xyz, r1, r1.w, r2
    mov oD0.w, c15.y
    mov oT0.xy, v2

// approximately 34 instruction slots used
```



## <a name="improve-performance-with-preshaders"></a><span data-ttu-id="53a86-209">Améliorer les performances avec des prénuanceurs</span><span class="sxs-lookup"><span data-stu-id="53a86-209">Improve Performance with Preshaders</span></span>

<span data-ttu-id="53a86-210">Un prénuanceur est une technique permettant d’accroître l’efficacité du nuanceur en précalculant les expressions de nuanceur constantes.</span><span class="sxs-lookup"><span data-stu-id="53a86-210">A preshader is a technique for increasing shader efficiency by pre-calculating constant shader expressions.</span></span> <span data-ttu-id="53a86-211">Le compilateur d’effet extrait automatiquement les calculs du nuanceur à partir du corps d’un nuanceur et les exécute sur le processeur avant l’exécution du nuanceur.</span><span class="sxs-lookup"><span data-stu-id="53a86-211">The effect compiler automatically pulls out shader computations from the body of a shader and executes them on the CPU prior to the shader running.</span></span> <span data-ttu-id="53a86-212">Par conséquent, les prénuanceurs fonctionnent uniquement avec les effets.</span><span class="sxs-lookup"><span data-stu-id="53a86-212">Consequently, preshaders only work with effects.</span></span> <span data-ttu-id="53a86-213">Par exemple, ces deux expressions peuvent être évaluées en dehors du nuanceur avant d’être exécutées.</span><span class="sxs-lookup"><span data-stu-id="53a86-213">For instance, these two expressions can be evaluated outside of the shader before it runs.</span></span>


```
mul(World,mul(View, Projection));
sin(time)
```



<span data-ttu-id="53a86-214">Les calculs de nuanceur qui peuvent être déplacés sont ceux associés à des paramètres uniformes. autrement dit, les calculs ne changent pas pour chaque vertex ou pixel.</span><span class="sxs-lookup"><span data-stu-id="53a86-214">Shader computations that can be moved are those associated with uniform parameters; that is, the computations do not change for each vertex or pixel.</span></span> <span data-ttu-id="53a86-215">Si vous utilisez Effects, le compilateur d’effet génère et exécute automatiquement un préombrage pour vous. aucun indicateur à activer.</span><span class="sxs-lookup"><span data-stu-id="53a86-215">If you are using effects, the effect compiler automatically generates and runs a preshader for you; there are no flags to enable.</span></span> <span data-ttu-id="53a86-216">Les prénuanceurs peuvent réduire le nombre d’instructions par nuanceur et peuvent également réduire le nombre de registres constants consommés par un nuanceur.</span><span class="sxs-lookup"><span data-stu-id="53a86-216">Preshaders can reduce the number of instructions per shader and can also reduce the number of constant registers a shader consumes.</span></span>

<span data-ttu-id="53a86-217">Imaginez le compilateur Effects comme une sorte de compilateur multiprocesseur, car il compile le code du nuanceur pour deux types de processeurs : un processeur et un GPU.</span><span class="sxs-lookup"><span data-stu-id="53a86-217">Think of the effect compiler as a sort of multi-processor compiler because it compiles shader code for two types of processors: a CPU and a GPU.</span></span> <span data-ttu-id="53a86-218">En outre, le compilateur d’effet est conçu pour déplacer le code du GPU vers le processeur et, par conséquent, améliorer les performances du nuanceur.</span><span class="sxs-lookup"><span data-stu-id="53a86-218">In addition, the effect compiler is designed to move code from the GPU to the CPU and therefore improve shader performance.</span></span> <span data-ttu-id="53a86-219">Cela est très similaire à l’extraction d’une expression statique à partir d’une boucle.</span><span class="sxs-lookup"><span data-stu-id="53a86-219">This is very similar to pulling a static expression out of a loop.</span></span> <span data-ttu-id="53a86-220">Un nuanceur qui transforme la position à partir de l’espace universel en espace de projection, et qui copie des coordonnées de texture ressemble à ceci en HLSL :</span><span class="sxs-lookup"><span data-stu-id="53a86-220">A shader that transforms position from world space to projection space, and copies texture coordinates would look like this in HLSL:</span></span>


```
float4x4 g_mWorldViewProjection;    // World * View * Projection matrix
float4x4 g_mWorldInverse;           // Inverse World matrix
float3 g_LightDir;                  // Light direction in world space
float4 g_LightDiffuse;              // Diffuse color of the light

struct VS_OUTPUT
{
    float4 Position   : POSITION;   // vertex position 
    float2 TextureUV  : TEXCOORD0;  // vertex texture coords 
    float4 Diffuse    : COLOR0;     // vertex diffuse color
};

VS_OUTPUT RenderSceneVS( float4 vPos : POSITION, 
                         float3 vNormal : NORMAL,
                         float2 vTexCoord0 : TEXCOORD0)
{
    VS_OUTPUT Output;
    
    // Transform the position from object space to projection space
    Output.Position = mul(vPos, g_mWorldViewProjection);

    // Transform the light from world space to object space    
    float3 vLightObjectSpace = normalize(mul(g_LightDir, (float3x3)g_mWorldInverse)); 

    // N dot L lighting
    Output.Diffuse = max(0,dot(vNormal, vLightObjectSpace));
    
    // Copy the texture coordinate
    Output.TextureUV = vTexCoord0; 
    
    return Output;    
}
technique RenderVS
{
    pass P0
    {          
        VertexShader = compile vs_1_1 RenderSceneVS();
    }
}
```



<span data-ttu-id="53a86-221">L’utilisation de l' [outil Effect-compiler Tool](../direct3dtools/fxc.md) pour compiler le nuanceur pour vs \_ 1 \_ 1 génère les instructions d’assembly suivantes :</span><span class="sxs-lookup"><span data-stu-id="53a86-221">Using [Effect-Compiler Tool](../direct3dtools/fxc.md) to compile the shader for vs\_1\_1 generates the following assembly instructions:</span></span>


```
technique RenderVS
{
    pass P0
    {
        vertexshader = 
            asm {
            //
            // Generated by Microsoft (R) D3DX9 Shader Compiler 9.15.779.0000
            //
            // Parameters:
            //
            //   float3 g_LightDir;
            //   float4x4 g_mWorldInverse;
            //   float4x4 g_mWorldViewProjection;
            //
            //
            // Registers:
            //
            //   Name                   Reg   Size
            //   ---------------------- ----- ----
            //   g_mWorldViewProjection c0       4
            //   g_mWorldInverse        c4       3
            //   g_LightDir             c7       1
            //
            
                vs_1_1
                def c8, 0, 0, 0, 0
                dcl_position v0
                dcl_normal v1
                dcl_texcoord v2
                mov r1.xyz, c7
                dp3 r0.x, r1, c4
                dp3 r0.y, r1, c5
                dp3 r0.z, r1, c6
                dp4 oPos.x, v0, c0
                dp3 r1.x, r0, r0
                dp4 oPos.y, v0, c1
                rsq r0.w, r1.x
                dp4 oPos.z, v0, c2
                mul r0.xyz, r0, r0.w
                dp4 oPos.w, v0, c3
                dp3 r0.x, v1, r0
                max oD0, r0.x, c8.x
                mov oT0.xy, v2
            
            // approximately 14 instruction slots used
            };

        //No embedded pixel shader
    }
}
```



<span data-ttu-id="53a86-222">Cela utilise environ 14 emplacements et utilise 9 registres constants.</span><span class="sxs-lookup"><span data-stu-id="53a86-222">This uses up approximately 14 slots and consumes 9 constant registers.</span></span> <span data-ttu-id="53a86-223">Avec un prénuancier, le compilateur déplace les expressions statiques hors du nuanceur et dans le prénuancier.</span><span class="sxs-lookup"><span data-stu-id="53a86-223">With a preshader, the compiler moves the static expressions out of the shader and into the preshader.</span></span> <span data-ttu-id="53a86-224">Le même nuanceur doit ressembler à ceci avec un prénuanceur :</span><span class="sxs-lookup"><span data-stu-id="53a86-224">The same shader would look like this with a preshader:</span></span>


```
technique RenderVS
{
    pass P0
    {
        vertexshader = 
            asm {
            //
            // Generated by Microsoft (R) D3DX9 Shader Compiler 9.15.779.0000
            //
            // Parameters:
            //
            //   float3 g_LightDir;
            //   float4x4 g_mWorldInverse;
            //
            //
            // Registers:
            //
            //   Name            Reg   Size
            //   --------------- ----- ----
            //   g_mWorldInverse c0       3
            //   g_LightDir      c3       1
            //
            
                preshader
                dot r0.x, c3.xyz, c0.xyz
                dot r0.y, c3.xyz, c1.xyz
                dot r0.z, c3.xyz, c2.xyz
                dot r1.w, r0.xyz, r0.xyz
                rsq r0.w, r1.w
                mul c4.xyz, r0.w, r0.xyz
            
            // approximately 6 instructions used
            //
            // Generated by Microsoft (R) D3DX9 Shader Compiler 9.15.779.0000
            //
            // Parameters:
            //
            //   float4x4 g_mWorldViewProjection;
            //
            //
            // Registers:
            //
            //   Name                   Reg   Size
            //   ---------------------- ----- ----
            //   g_mWorldViewProjection c0       4
            //
            
                vs_1_1
                def c5, 0, 0, 0, 0
                dcl_position v0
                dcl_normal v1
                dcl_texcoord v2
                dp4 oPos.x, v0, c0
                dp4 oPos.y, v0, c1
                dp4 oPos.z, v0, c2
                dp4 oPos.w, v0, c3
                dp3 r0.x, v1, c4
                max oD0, r0.x, c5.x
                mov oT0.xy, v2
            
            // approximately 7 instruction slots used
            };

        //No embedded pixel shader
    }
}
```



<span data-ttu-id="53a86-225">Un effet exécute un préombrage juste avant d’exécuter un nuanceur.</span><span class="sxs-lookup"><span data-stu-id="53a86-225">An effect executes a preshader just before executing a shader.</span></span> <span data-ttu-id="53a86-226">Le résultat est la même fonctionnalité avec des performances de nuanceur accrues, car le nombre d’instructions qui doivent être exécutées (pour chaque vertex ou pixel selon le type de nuanceur) a été réduit.</span><span class="sxs-lookup"><span data-stu-id="53a86-226">The result is the same functionality with increased shader performance because the number of instructions that need to be executed (for each vertex or pixel depending on the type of shader) has been reduced.</span></span> <span data-ttu-id="53a86-227">En outre, moins de registres constants sont consommés par le nuanceur en raison des expressions statiques déplacées dans le prénuancier.</span><span class="sxs-lookup"><span data-stu-id="53a86-227">In addition, fewer constant registers are consumed by the shader as a result of the static expressions being moved to the preshader.</span></span> <span data-ttu-id="53a86-228">Cela signifie que les nuanceurs précédemment limités par le nombre de registres de constantes qu’ils avaient nécessaires peuvent maintenant être compilés, car ils nécessitent moins de registres constants.</span><span class="sxs-lookup"><span data-stu-id="53a86-228">This means that shaders previously limited by the number of constant registers they required may now compile because they require fewer constant registers.</span></span> <span data-ttu-id="53a86-229">Il est raisonnable d’attendre 5% et une amélioration des performances de 20% par rapport aux prénuanceurs.</span><span class="sxs-lookup"><span data-stu-id="53a86-229">It is reasonable to expect a 5 percent and a 20 percent performance improvement from preshaders.</span></span>

<span data-ttu-id="53a86-230">Gardez à l’esprit que les constantes d’entrée sont différentes des constantes de sortie dans un prénuancier.</span><span class="sxs-lookup"><span data-stu-id="53a86-230">Keep in mind that the input constants are different from the output constants in a preshader.</span></span> <span data-ttu-id="53a86-231">La sortie C1 n’est pas la même que le registre d’entrée C1.</span><span class="sxs-lookup"><span data-stu-id="53a86-231">The output c1 is not the same as the input c1 register.</span></span> <span data-ttu-id="53a86-232">L’écriture dans un registre de constante dans un prénuanceur écrit en fait dans l’emplacement d’entrée (constante) du nuanceur correspondant.</span><span class="sxs-lookup"><span data-stu-id="53a86-232">Writing to a constant register in a preshader actually writes into the corresponding shader's input (constant) slot.</span></span>


```
// BaseDelta c0 1
// Refinements c1 1
preshader
mul c1.x, c0.x, (-2)
add c0.x, c0.x, c0.x
cmp c5.x, c1.x, (1), (0)
```



<span data-ttu-id="53a86-233">L’instruction CMP ci-dessus lira la valeur C1 du prénuancier, tandis que l’instruction mul écrira dans les registres de nuanceur de matériel pour être utilisée par le nuanceur de sommets.</span><span class="sxs-lookup"><span data-stu-id="53a86-233">The cmp instruction above will read the preshader c1 value, while the mul instruction will write to the hardware shader registers to be used by the vertex shader.</span></span>

## <a name="use-parameter-blocks-to-manage-effect-parameters"></a><span data-ttu-id="53a86-234">Utiliser des blocs de paramètres pour gérer les paramètres d’effet</span><span class="sxs-lookup"><span data-stu-id="53a86-234">Use Parameter Blocks to Manage Effect Parameters</span></span>

<span data-ttu-id="53a86-235">Les blocs de paramètres sont des blocs de modifications de l’état d’effet.</span><span class="sxs-lookup"><span data-stu-id="53a86-235">Parameter blocks are blocks of effect state changes.</span></span> <span data-ttu-id="53a86-236">Un bloc de paramètres peut enregistrer des modifications d’État afin qu’elles puissent être appliquées ultérieurement avec un seul appel.</span><span class="sxs-lookup"><span data-stu-id="53a86-236">A parameter block can record state changes, so that they can be applied later on with a single call.</span></span> <span data-ttu-id="53a86-237">Créez un bloc de paramètres en appelant [**ID3DXEffect :: BeginParameterBlock**](id3dxeffect--beginparameterblock.md):</span><span class="sxs-lookup"><span data-stu-id="53a86-237">Create a parameter block by calling [**ID3DXEffect::BeginParameterBlock**](id3dxeffect--beginparameterblock.md):</span></span>


```
    m_pEffect->SetTechnique( "RenderScene" );

    m_pEffect->BeginParameterBlock();
    D3DXVECTOR4 v4( Diffuse.r, Diffuse.g, Diffuse.b, Diffuse.a );
    m_pEffect->SetVector( "g_vDiffuse", &v4 );
    m_pEffect->SetFloat( "g_fReflectivity", fReflectivity );
    m_pEffect->SetFloat( "g_fAnimSpeed", fAnimSpeed );
    m_pEffect->SetFloat( "g_fSizeMul", fSize );
    m_hParameters = m_pEffect->EndParameterBlock();
```



<span data-ttu-id="53a86-238">Le bloc de paramètres enregistre quatre modifications appliquées par les appels d’API.</span><span class="sxs-lookup"><span data-stu-id="53a86-238">The parameter block saves four changes applied by the API calls.</span></span> <span data-ttu-id="53a86-239">L’appel de [**ID3DXEffect :: BeginParameterBlock**](id3dxeffect--beginparameterblock.md) démarre l’enregistrement des modifications d’État.</span><span class="sxs-lookup"><span data-stu-id="53a86-239">Calling [**ID3DXEffect::BeginParameterBlock**](id3dxeffect--beginparameterblock.md) starts recording the state changes.</span></span> <span data-ttu-id="53a86-240">[**ID3DXEffect :: EndParameterBlock**](id3dxeffect--endparameterblock.md) arrête l’ajout des modifications au bloc de paramètres et retourne un handle.</span><span class="sxs-lookup"><span data-stu-id="53a86-240">[**ID3DXEffect::EndParameterBlock**](id3dxeffect--endparameterblock.md) stops adding the changes to the parameter block and returns a handle.</span></span> <span data-ttu-id="53a86-241">Le descripteur est utilisé lors de l’appel de [**ID3DXEffect :: ApplyParameterBlock**](id3dxeffect--applyparameterblock.md).</span><span class="sxs-lookup"><span data-stu-id="53a86-241">The handle will be used when calling [**ID3DXEffect::ApplyParameterBlock**](id3dxeffect--applyparameterblock.md).</span></span>

<span data-ttu-id="53a86-242">Dans l' [exemple EffectParam](https://msdn.microsoft.com/library/Ee417535(v=VS.85).aspx), le bloc de paramètres est appliqué dans la séquence de rendu :</span><span class="sxs-lookup"><span data-stu-id="53a86-242">In the [EffectParam Sample](https://msdn.microsoft.com/library/Ee417535(v=VS.85).aspx), the parameter block is applied in the render sequence:</span></span>


```
CObj g_aObj[NUM_OBJS];       // Object instances

    if( SUCCEEDED( pd3dDevice->BeginScene() ) )
    {
        // Set the shared parameters using the first mesh's effect.

        // Render the mesh objects
        for( int i = 0; i < NUM_OBJS; ++i )
        {
            ID3DXEffect *pEffect = g_aObj[i].m_pEffect;

            // Apply the parameters
            pEffect->ApplyParameterBlock( g_aObj[i].m_hParameters );

            ...

            pEffect->Begin( &cPasses, 0 );
            for( iPass = 0; iPass < cPasses; iPass++ )
            {
              ...
            }
            pEffect->End();
        }

        ...
        pd3dDevice->EndScene();
    }
```



<span data-ttu-id="53a86-243">Le bloc de paramètres définit la valeur des quatre modifications d’État juste avant l’appel de [**ID3DXEffect :: Begin**](id3dxeffect--begin.md) .</span><span class="sxs-lookup"><span data-stu-id="53a86-243">The parameter block sets the value of all four of the state changes just before [**ID3DXEffect::Begin**](id3dxeffect--begin.md) is called.</span></span> <span data-ttu-id="53a86-244">Les blocs de paramètres sont un moyen pratique de définir plusieurs modifications d’État avec un seul appel d’API.</span><span class="sxs-lookup"><span data-stu-id="53a86-244">Parameter blocks are a handy way to set multiple state changes with a single API call.</span></span>

## <a name="related-topics"></a><span data-ttu-id="53a86-245">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="53a86-245">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="53a86-246">Effets</span><span class="sxs-lookup"><span data-stu-id="53a86-246">Effects</span></span>](effects.md)
</dt> </dl>

 

 
