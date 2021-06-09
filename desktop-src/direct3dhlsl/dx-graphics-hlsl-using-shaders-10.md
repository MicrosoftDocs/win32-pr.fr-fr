---
title: Utilisation des nuanceurs dans Direct3D 10
description: Utilisation des nuanceurs dans Direct3D 10
ms.assetid: cff6f901-cb9b-44d5-a75b-9a4029a37215
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c0d6212851e4603aac4db7ec85dd20714dc87774
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/09/2021
ms.locfileid: "111826287"
---
# <a name="using-shaders-in-direct3d-10"></a><span data-ttu-id="a7ac2-103">Utilisation des nuanceurs dans Direct3D 10</span><span class="sxs-lookup"><span data-stu-id="a7ac2-103">Using Shaders in Direct3D 10</span></span>

<span data-ttu-id="a7ac2-104">Le pipeline a trois étapes de nuanceur et chacune d’entre elles est programmée avec un nuanceur HLSL.</span><span class="sxs-lookup"><span data-stu-id="a7ac2-104">The pipeline has three shader stages and each one is programmed with an HLSL shader.</span></span> <span data-ttu-id="a7ac2-105">Tous les nuanceurs Direct3D 10 sont écrits en HLSL, ciblant le nuanceur modèle 4.</span><span class="sxs-lookup"><span data-stu-id="a7ac2-105">All Direct3D 10 shaders are written in HLSL, targeting shader model 4.</span></span>


<span data-ttu-id="a7ac2-106">Différences entre Direct3D 9 et Direct3D 10 :</span><span class="sxs-lookup"><span data-stu-id="a7ac2-106">Differences between Direct3D 9 and Direct3D 10:</span></span>

- <span data-ttu-id="a7ac2-107">Contrairement aux modèles de nuanceur Direct3D 9 qui peuvent être créés dans un langage assembleur intermédiaire, les nuanceurs de modèle de nuanceur 4,0 sont uniquement créés en HLSL.</span><span class="sxs-lookup"><span data-stu-id="a7ac2-107">Unlike Direct3D 9 shader models which could be authored in an intermediate assembly language, shader model 4.0 shaders are only authored in HLSL.</span></span> <span data-ttu-id="a7ac2-108">La compilation hors connexion des nuanceurs dans le bytecode consommable par l’appareil est toujours prise en charge et recommandée pour la plupart des scénarios.</span><span class="sxs-lookup"><span data-stu-id="a7ac2-108">Offline compilation of shaders into device-consumable bytecode is still supported, and recommended for most scenarios.</span></span>



 

<span data-ttu-id="a7ac2-109">Cet exemple utilise uniquement un nuanceur de sommets.</span><span class="sxs-lookup"><span data-stu-id="a7ac2-109">This example uses only a vertex shader.</span></span> <span data-ttu-id="a7ac2-110">Étant donné que tous les nuanceurs sont générés à partir du Common Shader Core, l’utilisation d’un nuanceur vertex est très similaire à l’utilisation d’une géométrie ou d’un nuanceur de pixels.</span><span class="sxs-lookup"><span data-stu-id="a7ac2-110">Because all shaders are built from the common shader core, learning how to use a vertex shader is very similar to using a geometry or pixel shader.</span></span>

<span data-ttu-id="a7ac2-111">Une fois que vous avez créé un nuanceur HLSL (cet exemple utilise le nuanceur de vertex HLSLWithoutFX. vsh), vous devez le préparer pour l’étape de pipeline qui l’utilisera.</span><span class="sxs-lookup"><span data-stu-id="a7ac2-111">Once you have authored an HLSL shader (this example uses the vertex shader HLSLWithoutFX.vsh), you will need to prepare it for the particular pipeline stage that will use it.</span></span> <span data-ttu-id="a7ac2-112">Pour ce faire, vous devez :</span><span class="sxs-lookup"><span data-stu-id="a7ac2-112">To do this you need to:</span></span>

-   [<span data-ttu-id="a7ac2-113">Compiler un nuanceur</span><span class="sxs-lookup"><span data-stu-id="a7ac2-113">Compile a Shader</span></span>](#compile-a-shader)
-   [<span data-ttu-id="a7ac2-114">Créer un objet Shader</span><span class="sxs-lookup"><span data-stu-id="a7ac2-114">Create a Shader Object</span></span>](#create-a-shader-object)
-   [<span data-ttu-id="a7ac2-115">Définir l’objet Shader</span><span class="sxs-lookup"><span data-stu-id="a7ac2-115">Set the Shader Object</span></span>](#set-the-shader-object)
-   [<span data-ttu-id="a7ac2-116">Répéter pour les 3 étapes de nuanceur</span><span class="sxs-lookup"><span data-stu-id="a7ac2-116">Repeat for all 3 Shader Stages</span></span>](#repeat-for-all-3-shader-stages)

<span data-ttu-id="a7ac2-117">Ces étapes doivent être répétées pour chaque nuanceur dans le pipeline.</span><span class="sxs-lookup"><span data-stu-id="a7ac2-117">These steps need to be repeated for each shader in the pipeline.</span></span>

## <a name="compile-a-shader"></a><span data-ttu-id="a7ac2-118">Compiler un nuanceur</span><span class="sxs-lookup"><span data-stu-id="a7ac2-118">Compile a Shader</span></span>

<span data-ttu-id="a7ac2-119">La première étape consiste à compiler le nuanceur, afin de vérifier que vous avez correctement codé les instructions HLSL.</span><span class="sxs-lookup"><span data-stu-id="a7ac2-119">The first step is to compile the shader, to check to see that you have coded the HLSL statements correctly.</span></span> <span data-ttu-id="a7ac2-120">Pour ce faire, appelez D3D10CompileShader et fournissez-lui plusieurs paramètres, comme indiqué ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="a7ac2-120">This is done by calling D3D10CompileShader and supplying it with several parameters as shown here:</span></span>


```
    IPD3D10Blob * pBlob;
    
        
    // Compile the vertex shader from the file
    D3D10CompileShader( strPath, strlen( strPath ), "HLSLWithoutFX.vsh", 
        NULL, NULL, "Ripple", "vs_4_0", dwShaderFlags, &pBlob, NULL );
```



<span data-ttu-id="a7ac2-121">Cette fonction accepte les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="a7ac2-121">This function takes the following parameters:</span></span>

-   <span data-ttu-id="a7ac2-122">Nom du fichier (et longueur de la chaîne de nom en octets) qui contient le nuanceur.</span><span class="sxs-lookup"><span data-stu-id="a7ac2-122">The name of the file ( and length of the name string in bytes ) that contains the shader.</span></span> <span data-ttu-id="a7ac2-123">Cet exemple utilise un nuanceur de sommets uniquement (dans le fichier HLSLWithoutFX. vsh dans lequel l’extension de fichier. vsh est l’abréviation de vertex shader).</span><span class="sxs-lookup"><span data-stu-id="a7ac2-123">This example uses a vertex shader only (in the file HLSLWithoutFX.vsh file where the file extension .vsh is an abbreviation for vertex shader).</span></span>
-   <span data-ttu-id="a7ac2-124">Nom de la fonction de nuanceur.</span><span class="sxs-lookup"><span data-stu-id="a7ac2-124">The shader function name.</span></span> <span data-ttu-id="a7ac2-125">Cet exemple compile un nuanceur de sommets à partir de la fonction ondulation qui prend une seule entrée et retourne un struct de sortie (la fonction provient de l’exemple HLSLWithoutFX) :</span><span class="sxs-lookup"><span data-stu-id="a7ac2-125">This example compiles a vertex shader from the Ripple function which takes a single input and returns an output struct (the function is from the HLSLWithoutFX sample):</span></span>
    ```
    VS_OUTPUT Ripple( in float2 vPosition : POSITION )
    ```

    

-   <span data-ttu-id="a7ac2-126">Pointeur vers toutes les macros utilisées par le nuanceur.</span><span class="sxs-lookup"><span data-stu-id="a7ac2-126">A pointer to all macros used by the shader.</span></span> <span data-ttu-id="a7ac2-127">Utilisez \_ \_ la macro D3D10 Shader pour faciliter la définition de vos macros. créez simplement une chaîne de nom qui contient tous les noms de macros (chaque nom étant séparé par un espace) et une chaîne de définition (chaque corps de macro étant séparé par un espace).</span><span class="sxs-lookup"><span data-stu-id="a7ac2-127">Use D3D10\_SHADER\_MACRO to help define your macros; simply create a name string that contains all the macro names (with each name separated by a space) and a definition string (with each macro body separated by a space).</span></span> <span data-ttu-id="a7ac2-128">Les deux chaînes doivent se terminer par une valeur NULL.</span><span class="sxs-lookup"><span data-stu-id="a7ac2-128">Both strings need to be NULL terminated.</span></span>
-   <span data-ttu-id="a7ac2-129">Pointeur vers les autres fichiers dont vous avez besoin pour que vos nuanceurs soient compilés.</span><span class="sxs-lookup"><span data-stu-id="a7ac2-129">A pointer to any other files that you need included to get your shaders to compile.</span></span> <span data-ttu-id="a7ac2-130">Utilise l’interface ID3D10Include qui a deux méthodes implémentées par l’utilisateur : Open et Close.</span><span class="sxs-lookup"><span data-stu-id="a7ac2-130">This uses the ID3D10Include interface which has two user-implemented methods: Open and Close.</span></span> <span data-ttu-id="a7ac2-131">Pour que cela fonctionne, vous devez implémenter le corps des méthodes Open et Close. dans la méthode Open, ajoutez le code que vous utiliseriez pour ouvrir les fichiers include de votre choix. dans la fonction Close, ajoutez le code pour fermer les fichiers lorsque vous n’en avez plus besoin.</span><span class="sxs-lookup"><span data-stu-id="a7ac2-131">To make this work, you will need to implement the body of the Open and Close methods; in the Open method add the code you would use to open whatever include files you want, in the Close function add the code to close the files when you are done with them.</span></span>
-   <span data-ttu-id="a7ac2-132">Nom de la fonction de nuanceur à compiler.</span><span class="sxs-lookup"><span data-stu-id="a7ac2-132">The name of the shader function to compile.</span></span> <span data-ttu-id="a7ac2-133">Ce nuanceur compile la fonction ondulation.</span><span class="sxs-lookup"><span data-stu-id="a7ac2-133">This shader compiles the Ripple function.</span></span>
-   <span data-ttu-id="a7ac2-134">Profil de nuanceur à cibler lors de la compilation.</span><span class="sxs-lookup"><span data-stu-id="a7ac2-134">The shader profile to target when compiling.</span></span> <span data-ttu-id="a7ac2-135">Étant donné que vous pouvez compiler une fonction en un vertex, une géométrie ou un nuanceur de pixels, le profil indique au compilateur le type de nuanceur et le modèle de nuanceur à comparer au code.</span><span class="sxs-lookup"><span data-stu-id="a7ac2-135">Since you can compile a function into a vertex, geometry, or pixel shader, the profile tells the compiler which type of shader and which shader model to compare the code against.</span></span>
-   <span data-ttu-id="a7ac2-136">Indicateurs du compilateur du nuanceur.</span><span class="sxs-lookup"><span data-stu-id="a7ac2-136">Shader compiler flags.</span></span> <span data-ttu-id="a7ac2-137">Ces indicateurs indiquent au compilateur les informations à placer dans la sortie compilée et la manière dont vous souhaitez optimiser le code de sortie : pour la vitesse, pour le débogage, etc. Pour obtenir la liste des indicateurs disponibles, consultez [constantes Effect (Direct3D 10)](/windows/desktop/direct3d10/d3d10-graphics-reference-effect-constants) .</span><span class="sxs-lookup"><span data-stu-id="a7ac2-137">These flags tell the compiler what information to put into the compiled output and how you want the output code optimized: for speed, for debug, etc. See [Effect Constants (Direct3D 10)](/windows/desktop/direct3d10/d3d10-graphics-reference-effect-constants) for a listing of the available flags.</span></span> <span data-ttu-id="a7ac2-138">L’exemple contient du code que vous pouvez utiliser pour définir les valeurs de l’indicateur de compilateur pour votre projet. il s’agit principalement d’une question indiquant si vous souhaitez ou non générer des informations de débogage.</span><span class="sxs-lookup"><span data-stu-id="a7ac2-138">The sample contains some code you can use to set the compiler flag values for your project - this is mainly a question of whether or not you want to generate debug information.</span></span>
-   <span data-ttu-id="a7ac2-139">Pointeur vers la mémoire tampon qui contient le code de nuanceur compilé.</span><span class="sxs-lookup"><span data-stu-id="a7ac2-139">A pointer to the buffer that contains the compiled shader code.</span></span> <span data-ttu-id="a7ac2-140">La mémoire tampon contient également les informations de débogage et de table de symboles incorporées demandées par les indicateurs du compilateur.</span><span class="sxs-lookup"><span data-stu-id="a7ac2-140">The buffer also contains any embedded debug and symbol table information requested by the compiler flags.</span></span>
-   <span data-ttu-id="a7ac2-141">Pointeur vers une mémoire tampon qui contient une liste d’erreurs et d’avertissements qui ont été rencontrés pendant la compilation, qui sont les mêmes messages que ceux que vous pouvez voir dans la sortie de débogage si vous exécutiez le débogueur lors de la compilation du nuanceur.</span><span class="sxs-lookup"><span data-stu-id="a7ac2-141">A pointer to a buffer that contains a listing of errors and warnings that were encountered during the compile, which are the same messages you would see in the debug output if you were running the debugger while compiling the shader.</span></span> <span data-ttu-id="a7ac2-142">**Null** est une valeur acceptable lorsque vous ne voulez pas que les erreurs soient retournées à une mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="a7ac2-142">**NULL** is an acceptable value when you don't want the errors returned to a buffer.</span></span>

<span data-ttu-id="a7ac2-143">Si le nuanceur se compile correctement, un pointeur vers le code du nuanceur est retourné en tant qu’interface ID3D10Blob.</span><span class="sxs-lookup"><span data-stu-id="a7ac2-143">If the shader compiles successfully, a pointer to the shader code is returned as a ID3D10Blob interface.</span></span> <span data-ttu-id="a7ac2-144">Il s’agit de l’interface d’objet BLOB, car le pointeur se trouve à un emplacement dans la mémoire qui est constitué d’un tableau de DWORD.</span><span class="sxs-lookup"><span data-stu-id="a7ac2-144">It is called the Blob interface because the pointer is to a location in memory that is made up of an array of DWORD's.</span></span> <span data-ttu-id="a7ac2-145">L’interface est fournie afin que vous puissiez obtenir un pointeur vers le nuanceur compilé dont vous aurez besoin à l’étape suivante.</span><span class="sxs-lookup"><span data-stu-id="a7ac2-145">The interface is provided so that you can get a pointer to the compiled shader which you will need in the next step.</span></span>

<span data-ttu-id="a7ac2-146">À partir du kit de développement logiciel (SDK) 2006 du mois de décembre, le compilateur HLSL DirectX 10 est désormais le compilateur par défaut dans DirectX 9 et DirectX 10.</span><span class="sxs-lookup"><span data-stu-id="a7ac2-146">Beginning with the December 2006 SDK, the DirectX 10 HLSL compiler is now the default compiler in both DirectX 9 and DirectX 10.</span></span> <span data-ttu-id="a7ac2-147">Pour plus d’informations [, consultez outil de compilateur Effect](/windows/desktop/direct3dtools/fxc) .</span><span class="sxs-lookup"><span data-stu-id="a7ac2-147">See [Effect-Compiler Tool](/windows/desktop/direct3dtools/fxc) for details.</span></span>

### <a name="get-a-pointer-to-a-compiled-shader"></a><span data-ttu-id="a7ac2-148">Obtenir un pointeur vers un nuanceur compilé</span><span class="sxs-lookup"><span data-stu-id="a7ac2-148">Get a Pointer to a Compiled Shader</span></span>

<span data-ttu-id="a7ac2-149">Plusieurs méthodes d’API requièrent un pointeur vers un nuanceur compilé.</span><span class="sxs-lookup"><span data-stu-id="a7ac2-149">Several API methods require a pointer to a compiled shader.</span></span> <span data-ttu-id="a7ac2-150">Cet argument est généralement appelé *pShaderBytecode* , car il pointe vers un nuanceur compilé représenté sous la forme d’une séquence de codes d’octet.</span><span class="sxs-lookup"><span data-stu-id="a7ac2-150">This argument is usually called *pShaderBytecode* because it points to a compiled shader represented as a sequence of byte codes.</span></span> <span data-ttu-id="a7ac2-151">Pour obtenir un pointeur vers un nuanceur compilé, commencez par compiler le nuanceur en appelant [**D3D10CompileShader**](/windows/desktop/api/d3d10shader/nf-d3d10shader-d3d10compileshader) ou une fonction similaire.</span><span class="sxs-lookup"><span data-stu-id="a7ac2-151">To get a pointer to a compiled shader, first compile the shader by calling [**D3D10CompileShader**](/windows/desktop/api/d3d10shader/nf-d3d10shader-d3d10compileshader) or a similar function.</span></span> <span data-ttu-id="a7ac2-152">Si la compilation réussit, le nuanceur compilé est retourné dans une interface [**ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob) .</span><span class="sxs-lookup"><span data-stu-id="a7ac2-152">If compilation is successful, the compiled shader is returned in an [**ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob) interface.</span></span> <span data-ttu-id="a7ac2-153">Enfin, utilisez la méthode [**GetBufferPointer**](/windows/desktop/api/d3dcommon/nf-d3dcommon-id3d10blob-getbufferpointer) pour retourner le pointeur.</span><span class="sxs-lookup"><span data-stu-id="a7ac2-153">Finally, use the [**GetBufferPointer**](/windows/desktop/api/d3dcommon/nf-d3dcommon-id3d10blob-getbufferpointer) method to return the pointer.</span></span>

## <a name="create-a-shader-object"></a><span data-ttu-id="a7ac2-154">Créer un objet Shader</span><span class="sxs-lookup"><span data-stu-id="a7ac2-154">Create a Shader Object</span></span>

<span data-ttu-id="a7ac2-155">Une fois le nuanceur compilé, appelez CreateVertexShader pour créer l’objet de nuanceur :</span><span class="sxs-lookup"><span data-stu-id="a7ac2-155">Once the shader is compiled, call CreateVertexShader to create the shader object:</span></span>


```
    ID3D10VertexShader ** ppVertexShader
    ID3D10Blob pBlob;


    // Create the vertex shader
    hr = pd3dDevice->CreateVertexShader( (DWORD*)pBlob->GetBufferPointer(),
        pBlob->GetBufferSize(), &ppVertexShader );

    // Release the pointer to the compiled shader once you are done with it
    pBlob->Release();
```



<span data-ttu-id="a7ac2-156">Pour créer l’objet Shader, transmettez le pointeur au nuanceur compilé dans CreateVertexShader.</span><span class="sxs-lookup"><span data-stu-id="a7ac2-156">To create the shader object, pass the pointer to the compiled shader into CreateVertexShader.</span></span> <span data-ttu-id="a7ac2-157">Dans la mesure où vous deviez tout d’abord compiler le nuanceur, cet appel sera presque certainement réussi, sauf si vous rencontrez un problème de mémoire sur votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="a7ac2-157">Since you had to successfully compile the shader first, this call will almost certainly pass, unless you have a memory problem on your machine.</span></span>

<span data-ttu-id="a7ac2-158">Vous pouvez créer autant d’objets de nuanceur que vous le souhaitez et y conserver simplement des pointeurs.</span><span class="sxs-lookup"><span data-stu-id="a7ac2-158">You can create as many shader objects as you like and simply keep pointers to them.</span></span> <span data-ttu-id="a7ac2-159">Ce même mécanisme fonctionne pour les nuanceurs de géométrie et de pixels, en supposant que vous faites correspondre les profils de nuanceur (lorsque vous appelez la méthode Compile) aux noms d’interface (lorsque vous appelez la méthode Create).</span><span class="sxs-lookup"><span data-stu-id="a7ac2-159">This same mechanism works for geometry and pixel shaders assuming you match the shader profiles (when you call the compile method) to the interface names (when you call the create method).</span></span>

## <a name="set-the-shader-object"></a><span data-ttu-id="a7ac2-160">Définir l’objet Shader</span><span class="sxs-lookup"><span data-stu-id="a7ac2-160">Set the Shader Object</span></span>

<span data-ttu-id="a7ac2-161">La dernière étape consiste à définir le nuanceur sur l’étape de pipeline.</span><span class="sxs-lookup"><span data-stu-id="a7ac2-161">The last step is set the shader to the pipeline stage.</span></span> <span data-ttu-id="a7ac2-162">Comme il existe trois étapes de nuanceur dans le pipeline, vous devrez effectuer trois appels d’API, un pour chaque étape.</span><span class="sxs-lookup"><span data-stu-id="a7ac2-162">Since there are three shader stages in the pipeline, you will need to make three API calls, one for each stage.</span></span>


```
    // Set a vertex shader
    pd3dDevice->VSSetShader( g_pVS10 );
```



<span data-ttu-id="a7ac2-163">L’appel à VSSetShader prend le pointeur vers le nuanceur de sommets créé à l’étape 1.</span><span class="sxs-lookup"><span data-stu-id="a7ac2-163">The call to VSSetShader takes the pointer to the vertex shader created in step 1.</span></span> <span data-ttu-id="a7ac2-164">Cela définit le nuanceur dans l’appareil.</span><span class="sxs-lookup"><span data-stu-id="a7ac2-164">This sets the shader in the device.</span></span> <span data-ttu-id="a7ac2-165">L’étape du nuanceur de sommets est maintenant initialisée avec son code de nuanceur vertex, tout ce qui reste est l’initialisation des variables de nuanceur.</span><span class="sxs-lookup"><span data-stu-id="a7ac2-165">The vertex shader stage is now initialized with its vertex shader code, all that remains is initializing any shader variables.</span></span>

## <a name="repeat-for-all-3-shader-stages"></a><span data-ttu-id="a7ac2-166">Répéter pour les 3 étapes de nuanceur</span><span class="sxs-lookup"><span data-stu-id="a7ac2-166">Repeat for all 3 Shader Stages</span></span>

<span data-ttu-id="a7ac2-167">Répétez ces mêmes étapes pour créer un nuanceur de vertex ou de pixels, voire un nuanceur de géométrie qui génère le nuanceur de pixels.</span><span class="sxs-lookup"><span data-stu-id="a7ac2-167">Repeat these same set of steps to build any vertex or pixel shader or even a geometry shader that outputs to the pixel shader.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a7ac2-168">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a7ac2-168">Related Topics</span></span>

[<span data-ttu-id="a7ac2-169">Compilation des nuanceurs</span><span class="sxs-lookup"><span data-stu-id="a7ac2-169">Compiling Shaders</span></span>](dx-graphics-hlsl-part1.md)


## <a name="related-topics"></a><span data-ttu-id="a7ac2-170">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a7ac2-170">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a7ac2-171">Guide de programmation pour HLSL</span><span class="sxs-lookup"><span data-stu-id="a7ac2-171">Programming Guide for HLSL</span></span>](dx-graphics-hlsl-pguide.md)
</dt> </dl>

 

