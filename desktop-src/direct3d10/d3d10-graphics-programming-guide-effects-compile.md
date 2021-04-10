---
description: Une fois qu’un effet a été créé, la première étape consiste à compiler le code pour vérifier les problèmes de syntaxe.
ms.assetid: b8d8a0b7-b520-44e4-8691-6eb46202c092
title: Compiler un effet (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab6183f2f71b07c482fa24efc4f9fed199216d75
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104200922"
---
# <a name="compile-an-effect-direct3d-10"></a><span data-ttu-id="78653-103">Compiler un effet (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="78653-103">Compile an Effect (Direct3D 10)</span></span>

<span data-ttu-id="78653-104">Une fois qu’un effet a été créé, la première étape consiste à compiler le code pour vérifier les problèmes de syntaxe.</span><span class="sxs-lookup"><span data-stu-id="78653-104">Once an effect has been authored, the first step is to compile the code to check for syntax problems.</span></span> <span data-ttu-id="78653-105">Pour ce faire, appelez l’une des API de compilation (comme D3DX10CompileEffectFromFile, D3DX10CompileEffectFromResource, D3DX10CompileEffectFromMemory).</span><span class="sxs-lookup"><span data-stu-id="78653-105">This is done by calling one of the compile APIs (like D3DX10CompileEffectFromFile, D3DX10CompileEffectFromResource, D3DX10CompileEffectFromMemory).</span></span> <span data-ttu-id="78653-106">Ces API appellent le compilateur Effect fxc.exe qui est le compilateur utilisé pour compiler le code HLSL.</span><span class="sxs-lookup"><span data-stu-id="78653-106">These API's invoke the effect compiler fxc.exe which is the compiler used to compile HLSL code.</span></span> <span data-ttu-id="78653-107">C’est pour cette raison que la syntaxe du code dans un effet ressemble beaucoup à du code HLSL (il existe quelques exceptions qui seront gérées ultérieurement).</span><span class="sxs-lookup"><span data-stu-id="78653-107">This is why the syntax for code in an effect looks very much like HLSL code (there are a few exceptions that will be handled later).</span></span> <span data-ttu-id="78653-108">Au fait, le compilateur/HLSL Effects (fxc.exe) se trouve dans le kit de développement logiciel (SDK) dans le dossier Utilities afin que vous puissiez compiler vos nuanceurs (ou effets) hors connexion si vous le souhaitez.</span><span class="sxs-lookup"><span data-stu-id="78653-108">By the way, the effect compiler/hlsl compiler (fxc.exe) is in the SDK in the utilities folder so that you can compile your shaders (or effects) offline if you choose.</span></span> <span data-ttu-id="78653-109">Consultez la documentation pour exécuter le compilateur à partir de la ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="78653-109">See the documentation for running the compiler from the command line.</span></span>

-   [<span data-ttu-id="78653-110">Includes</span><span class="sxs-lookup"><span data-stu-id="78653-110">Includes</span></span>](#includes)
-   [<span data-ttu-id="78653-111">Macros</span><span class="sxs-lookup"><span data-stu-id="78653-111">Macros</span></span>](#macros)
-   [<span data-ttu-id="78653-112">Indicateurs de nuanceur HLSL</span><span class="sxs-lookup"><span data-stu-id="78653-112">HLSL Shader Flags</span></span>](#hlsl-shader-flags)
-   [<span data-ttu-id="78653-113">Indicateurs FX</span><span class="sxs-lookup"><span data-stu-id="78653-113">FX Flags</span></span>](#fx-flags)
-   [<span data-ttu-id="78653-114">Vérification des erreurs</span><span class="sxs-lookup"><span data-stu-id="78653-114">Checking Errors</span></span>](#checking-errors)
-   [<span data-ttu-id="78653-115">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="78653-115">Related topics</span></span>](#related-topics)

<span data-ttu-id="78653-116">Voici un exemple de compilation d’un fichier Effect (à partir de l’exemple BasicHLSL10).</span><span class="sxs-lookup"><span data-stu-id="78653-116">Here's an example of compiling an effect file (from the BasicHLSL10 sample).</span></span>


```
WCHAR str[MAX_PATH];
DXUTFindDXSDKMediaFileCch( str, MAX_PATH, L"BasicHLSL10.fx" );

hr = D3DX10CompileEffectFromFile( str, NULL, NULL, "fx_4_0", 
    D3D10_SHADER_ENABLE_STRICTNESS, 0, pd3dDevice, NULL, NULL, 
    &l_pBlob_Effect, &l_pBlob_Errors, NULL );
```



## <a name="includes"></a><span data-ttu-id="78653-117">Includes</span><span class="sxs-lookup"><span data-stu-id="78653-117">Includes</span></span>

<span data-ttu-id="78653-118">Un paramètre est une interface include.</span><span class="sxs-lookup"><span data-stu-id="78653-118">One parameter is an include interface.</span></span> <span data-ttu-id="78653-119">Générez l’une d’entre elles si vous souhaitez inclure un comportement personnalisé lors de la lecture d’un fichier include.</span><span class="sxs-lookup"><span data-stu-id="78653-119">Generate one of these if you want to include a customized behavior when reading an include file.</span></span> <span data-ttu-id="78653-120">Ce comportement personnalisé est exécuté chaque fois qu’un effet (qui utilise le pointeur include) est créé ou qu’un effet (qui utilise le pointeur include) est compilé.</span><span class="sxs-lookup"><span data-stu-id="78653-120">This custom behavior is executed each time an effect (that uses the include pointer) is created or when an effect (that uses the include pointer) is compiled.</span></span> <span data-ttu-id="78653-121">Pour implémenter un comportement include personnalisé, dérivez une classe de l’interface include.</span><span class="sxs-lookup"><span data-stu-id="78653-121">To implement customized include behavior, derive a class from the Include interface.</span></span> <span data-ttu-id="78653-122">Cela fournit vos méthodes de classe deux : Open et Close.</span><span class="sxs-lookup"><span data-stu-id="78653-122">This provides your class two methods: Open and Close.</span></span> <span data-ttu-id="78653-123">Implémentez le comportement personnalisé dans les méthodes Open et Close.</span><span class="sxs-lookup"><span data-stu-id="78653-123">Implement the custom behavior in the Open and Close methods.</span></span>

## <a name="macros"></a><span data-ttu-id="78653-124">Macros</span><span class="sxs-lookup"><span data-stu-id="78653-124">Macros</span></span>

<span data-ttu-id="78653-125">La compilation des effets peut également prendre un pointeur vers les macros définies ailleurs.</span><span class="sxs-lookup"><span data-stu-id="78653-125">Effect compilation can also take a pointer to macros that are defined elsewhere.</span></span> <span data-ttu-id="78653-126">Par exemple, supposons que vous deviez modifier l’effet dans BasicHLSL10 pour utiliser deux macros : zéro et un.</span><span class="sxs-lookup"><span data-stu-id="78653-126">For example, suppose you were to modify the effect in BasicHLSL10, to use two macros: zero and one.</span></span> <span data-ttu-id="78653-127">Le code d’effet qui utilise les deux macros est présenté ici.</span><span class="sxs-lookup"><span data-stu-id="78653-127">The effect code that uses the two macros is shown here.</span></span>


```
if( bAnimate )
    vAnimatedPos += float4(vNormal, zero) *  
        (sin(g_fTime+5.5)+0.5)*5;
        
    Output.Diffuse.a = one;         
```



<span data-ttu-id="78653-128">Voici la déclaration pour les deux macros.</span><span class="sxs-lookup"><span data-stu-id="78653-128">Here is the declaration for the two macros.</span></span>


```
D3D_SHADER_MACRO Shader_Macros[3] = { "zero", "0", "one", "1.0f", NULL, NULL };
```



<span data-ttu-id="78653-129">Les macros sont un tableau de macros terminé par un caractère NULL ; où chaque macro est définie avec un struct de [**\_ \_ macro de nuanceur D3D**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro) .</span><span class="sxs-lookup"><span data-stu-id="78653-129">The macros are a NULL terminated array of macros; where each macro is defined with a [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro) struct.</span></span>

<span data-ttu-id="78653-130">Enfin, modifiez l’appel de l’effet de compilation pour prendre un pointeur vers les macros.</span><span class="sxs-lookup"><span data-stu-id="78653-130">Lastly, modify the compile effect call to take a pointer to the macros.</span></span>


```
D3DX10CreateEffectFromFile( str, Shader_Macros, NULL, 
    D3D10_SHADER_ENABLE_STRICTNESS, 0, pd3dDevice, NULL, NULL, 
    &g_pEffect10, NULL );
```



## <a name="hlsl-shader-flags"></a><span data-ttu-id="78653-131">Indicateurs de nuanceur HLSL</span><span class="sxs-lookup"><span data-stu-id="78653-131">HLSL Shader Flags</span></span>

<span data-ttu-id="78653-132">Les indicateurs de nuanceur spécifient des contraintes de nuanceur pour le compilateur HLSL.</span><span class="sxs-lookup"><span data-stu-id="78653-132">Shader flags specify shader constraints to the HLSL compiler.</span></span> <span data-ttu-id="78653-133">Ces indicateurs ont un impact sur le code généré par le compilateur du nuanceur, y compris :</span><span class="sxs-lookup"><span data-stu-id="78653-133">These flags impact the code generated by the shader compiler including:</span></span>

-   <span data-ttu-id="78653-134">Considérations relatives à la taille : optimisez le code.</span><span class="sxs-lookup"><span data-stu-id="78653-134">Size considerations: optimize the code.</span></span>
-   <span data-ttu-id="78653-135">Considérations relatives au débogage : ajout d’informations de débogage, prévention du contrôle de Flow.</span><span class="sxs-lookup"><span data-stu-id="78653-135">Debug considerations: including debug information, preventing flow control.</span></span>
-   <span data-ttu-id="78653-136">Considérations matérielles : la cible de compilation et si un nuanceur peut ou non s’exécuter sur du matériel hérité.</span><span class="sxs-lookup"><span data-stu-id="78653-136">Hardware considerations: the compile target and whether or not a shader can run on legacy hardware.</span></span>

<span data-ttu-id="78653-137">En général, ces indicateurs peuvent être combinés de manière logique, en supposant que vous n’avez pas spécifié deux caractéristiques conflictuelles.</span><span class="sxs-lookup"><span data-stu-id="78653-137">In general, these flags can be logically combined, assuming you have not specified two conflicting characteristics.</span></span> <span data-ttu-id="78653-138">Pour obtenir la liste des indicateurs [, consultez constantes d’effet (Direct3D 10)](d3d10-graphics-reference-effect-constants.md).</span><span class="sxs-lookup"><span data-stu-id="78653-138">For a listing of the flags see [Effect Constants (Direct3D 10)](d3d10-graphics-reference-effect-constants.md).</span></span>

## <a name="fx-flags"></a><span data-ttu-id="78653-139">Indicateurs FX</span><span class="sxs-lookup"><span data-stu-id="78653-139">FX Flags</span></span>

<span data-ttu-id="78653-140">Ces indicateurs sont utilisés lors de la création d’un effet pour définir le comportement de compilation ou le comportement d’un effet d’exécution.</span><span class="sxs-lookup"><span data-stu-id="78653-140">These flags used when creating an effect to define either compilation behavior or runtime effect behavior.</span></span> <span data-ttu-id="78653-141">Pour obtenir la liste des indicateurs [, consultez constantes d’effet (Direct3D 10)](d3d10-graphics-reference-effect-constants.md).</span><span class="sxs-lookup"><span data-stu-id="78653-141">For a listing of the flags see [Effect Constants (Direct3D 10)](d3d10-graphics-reference-effect-constants.md).</span></span>

## <a name="checking-errors"></a><span data-ttu-id="78653-142">Vérification des erreurs</span><span class="sxs-lookup"><span data-stu-id="78653-142">Checking Errors</span></span>

<span data-ttu-id="78653-143">Si, au cours de la compilation, une erreur se produit, l’API retourne une interface qui contient les erreurs retournées par le compilateur d’effet.</span><span class="sxs-lookup"><span data-stu-id="78653-143">If during compilation, an error occurs, the API returns an interface which contains the errors returned from the effect compiler.</span></span> <span data-ttu-id="78653-144">Cette interface est appelée ID3D10Blob.</span><span class="sxs-lookup"><span data-stu-id="78653-144">This interface is called ID3D10Blob.</span></span> <span data-ttu-id="78653-145">Toutefois, il n’est pas directement lisible en retournant un pointeur vers la mémoire tampon qui contient les données (qui est une chaîne), vous pouvez voir toutes les erreurs de compilation.</span><span class="sxs-lookup"><span data-stu-id="78653-145">It is not directly readable, however, by returning a pointer to the buffer that contains the data (which is a string), you can see any compilation errors.</span></span>

<span data-ttu-id="78653-146">Dans cet exemple, une erreur a été introduite dans l’effet BasicHLSL. FX en copiant deux fois la première déclaration de variable.</span><span class="sxs-lookup"><span data-stu-id="78653-146">In this example, an error was introduced into the BasicHLSL.fx effect by copying the first variable declaration twice.</span></span>


```
//-------------------------------------------------------------------
// Global variables
//-------------------------------------------------------------------
float4 g_MaterialAmbientColor;      // Material's ambient color

// Declare the same variable twice
float4 g_MaterialAmbientColor;      // Material's ambient color
```



<span data-ttu-id="78653-147">Cette erreur a empêché le compilateur de retourner l’erreur suivante, comme illustré dans la capture d’écran suivante de la fenêtre Espion dans Microsoft Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="78653-147">This error caused the compiler to return the following error, as shown in the following screen shot of the watch window in Microsoft Visual Studio.</span></span>

![capture d’écran de la fenêtre Espion de Visual Studio](images/effect-compile-errors-2.jpg)

<span data-ttu-id="78653-149&quot;>Étant donné que l’erreur est retournée dans un pointeur LPVOID, effectuez un cast de celle-ci en une chaîne de caractères dans la fenêtre Espion.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;78653-149&quot;>Since the error is returned in a LPVOID pointer, cast it to a character string in the watch window.</span></span>

<span data-ttu-id=&quot;78653-150&quot;>Voici le code utilisé pour retourner l’erreur de la compilation qui a échoué.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;78653-150&quot;>Here is the code used to return the error from the failed compile.</span></span>


```
// Read the D3DX effect file
WCHAR str[MAX_PATH];
ID3D10Blob* l_pBlob_Effect = NULL;
ID3D10Blob* l_pBlob_Errors = NULL;
hr = DXUTFindDXSDKMediaFileCch( str, MAX_PATH, L&quot;BasicHLSL10.fx" );
hr = D3DX10CompileEffectFromFile( str, NULL, NULL, 
    D3D10_SHADER_ENABLE_STRICTNESS, 0, NULL, 
    &l_pBlob_Effect, &l_pBlob_Errors );

LPVOID l_pError = NULL;
if( l_pBlob_Errors )
{
    l_pError = l_pBlob_Errors->GetBufferPointer();
    // then cast to a char* to see it in the locals window
}
```



## <a name="related-topics"></a><span data-ttu-id="78653-151">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="78653-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="78653-152">Rendu d’un effet (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="78653-152">Rendering an Effect (Direct3D 10)</span></span>](d3d10-graphics-programming-guide-effects-render.md)
</dt> </dl>

 

 



