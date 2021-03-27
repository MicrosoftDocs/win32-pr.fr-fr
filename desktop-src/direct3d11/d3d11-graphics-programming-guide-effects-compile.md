---
title: Compiler un effet (Direct3D 11)
description: Une fois qu’un effet a été créé, l’étape suivante consiste à compiler le code pour vérifier les problèmes de syntaxe.
ms.assetid: 7624d55e-6466-4156-8f31-30f0d25a2883
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3df304a7b657af19984008bd90a1be4bfe5219c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103941108"
---
# <a name="compile-an-effect-direct3d-11"></a><span data-ttu-id="c9e4a-103">Compiler un effet (Direct3D 11)</span><span class="sxs-lookup"><span data-stu-id="c9e4a-103">Compile an Effect (Direct3D 11)</span></span>

<span data-ttu-id="c9e4a-104">Une fois qu’un effet a été créé, l’étape suivante consiste à compiler le code pour vérifier les problèmes de syntaxe.</span><span class="sxs-lookup"><span data-stu-id="c9e4a-104">After an effect has been authored, the next step is to compile the code to check for syntax problems.</span></span>

<span data-ttu-id="c9e4a-105">Pour ce faire, appelez l’une des API de compilation ([**D3DX11CompileFromFile**](d3dx11compilefromfile.md), [**D3DX11CompileFromMemory**](d3dx11compilefrommemory.md)ou [**D3DX11CompileFromResource**](d3dx11compilefromresource.md) ).</span><span class="sxs-lookup"><span data-stu-id="c9e4a-105">You do so by calling one of the compile APIs ([**D3DX11CompileFromFile**](d3dx11compilefromfile.md), [**D3DX11CompileFromMemory**](d3dx11compilefrommemory.md), or [**D3DX11CompileFromResource**](d3dx11compilefromresource.md) ).</span></span> <span data-ttu-id="c9e4a-106">Ces API appellent le compilateur Effect fxc.exe, qui compile le code HLSL.</span><span class="sxs-lookup"><span data-stu-id="c9e4a-106">These APIs invoke the effect compiler fxc.exe, which compiles HLSL code.</span></span> <span data-ttu-id="c9e4a-107">C’est pour cette raison que la syntaxe du code dans un effet ressemble beaucoup à du code HLSL.</span><span class="sxs-lookup"><span data-stu-id="c9e4a-107">This is why the syntax for code in an effect looks very much like HLSL code.</span></span> <span data-ttu-id="c9e4a-108">(Il existe quelques exceptions qui seront gérées ultérieurement).</span><span class="sxs-lookup"><span data-stu-id="c9e4a-108">(There are a few exceptions that will be handled later).</span></span> <span data-ttu-id="c9e4a-109">Le compilateur Effect/compilateur HLSL, fxc.exe, est disponible dans le kit de développement logiciel (SDK) dans le dossier Utilities afin que les nuanceurs (ou effets) puissent être compilés hors connexion si vous le souhaitez.</span><span class="sxs-lookup"><span data-stu-id="c9e4a-109">The effect compiler/hlsl compiler, fxc.exe, is available in the SDK in the utilities folder so that shaders (or effects) can be compiled offline if you choose.</span></span> <span data-ttu-id="c9e4a-110">Consultez la documentation pour exécuter le compilateur à partir de la ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="c9e4a-110">See the documentation for running the compiler from the command line.</span></span>

-   [<span data-ttu-id="c9e4a-111">Exemple</span><span class="sxs-lookup"><span data-stu-id="c9e4a-111">Example</span></span>](#example)
-   [<span data-ttu-id="c9e4a-112">Includes</span><span class="sxs-lookup"><span data-stu-id="c9e4a-112">Includes</span></span>](#includes)
-   [<span data-ttu-id="c9e4a-113">Recherche de fichiers include</span><span class="sxs-lookup"><span data-stu-id="c9e4a-113">Searching for Include Files</span></span>](#searching-for-include-files)
-   [<span data-ttu-id="c9e4a-114">Macros</span><span class="sxs-lookup"><span data-stu-id="c9e4a-114">Macros</span></span>](#macros)
-   [<span data-ttu-id="c9e4a-115">Indicateurs de nuanceur HLSL</span><span class="sxs-lookup"><span data-stu-id="c9e4a-115">HLSL Shader Flags</span></span>](#hlsl-shader-flags)
-   [<span data-ttu-id="c9e4a-116">Indicateurs FX</span><span class="sxs-lookup"><span data-stu-id="c9e4a-116">FX Flags</span></span>](#fx-flags)
-   [<span data-ttu-id="c9e4a-117">Vérification des erreurs</span><span class="sxs-lookup"><span data-stu-id="c9e4a-117">Checking Errors</span></span>](#checking-errors)
-   [<span data-ttu-id="c9e4a-118">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c9e4a-118">Related topics</span></span>](#related-topics)

## <a name="example"></a><span data-ttu-id="c9e4a-119">Exemple</span><span class="sxs-lookup"><span data-stu-id="c9e4a-119">Example</span></span>

<span data-ttu-id="c9e4a-120">Voici un exemple de compilation d’un fichier Effect.</span><span class="sxs-lookup"><span data-stu-id="c9e4a-120">Here's an example of compiling an effect file.</span></span>


```
WCHAR str[MAX_PATH];
DXUTFindDXSDKMediaFileCch( str, MAX_PATH, L"BasicHLSL10.fx" );

hr = D3DX11CompileFromFile( str, NULL, NULL, pFunctionName, pProfile, D3D10_SHADER_ENABLE_STRICTNESS, NULL, NULL, &pBlob, &pErrorBlob, NULL );
```



## <a name="includes"></a><span data-ttu-id="c9e4a-121">Includes</span><span class="sxs-lookup"><span data-stu-id="c9e4a-121">Includes</span></span>

<span data-ttu-id="c9e4a-122">L’un des paramètres des API de compilation est une interface include.</span><span class="sxs-lookup"><span data-stu-id="c9e4a-122">One parameter of the compile APIs is an include interface.</span></span> <span data-ttu-id="c9e4a-123">Générez l’une de ces si vous souhaitez inclure un comportement personnalisé lorsque le compilateur lit un fichier include.</span><span class="sxs-lookup"><span data-stu-id="c9e4a-123">Generate one of these if you want to include a customized behavior when the compiler reads an include file.</span></span> <span data-ttu-id="c9e4a-124">Le compilateur exécute ce comportement personnalisé chaque fois qu’il crée ou compile un effet (qui utilise le pointeur include).</span><span class="sxs-lookup"><span data-stu-id="c9e4a-124">The compiler executes this custom behavior each time it creates or compiles an effect (that uses the include pointer).</span></span> <span data-ttu-id="c9e4a-125">Pour implémenter un comportement include personnalisé, dérivez une classe de l’interface [**ID3DInclude**](/windows/desktop/api/D3Dcommon/nn-d3dcommon-id3dinclude) .</span><span class="sxs-lookup"><span data-stu-id="c9e4a-125">To implement customized include behavior, derive a class from the [**ID3DInclude**](/windows/desktop/api/D3Dcommon/nn-d3dcommon-id3dinclude) interface.</span></span> <span data-ttu-id="c9e4a-126">Cela fournit à votre classe deux méthodes : [**Open**](/windows/desktop/api/D3DCommon/nf-d3dcommon-id3dinclude-open) et [**Close**](/windows/desktop/api/D3DCommon/nf-d3dcommon-id3dinclude-close).</span><span class="sxs-lookup"><span data-stu-id="c9e4a-126">This provides your class with two methods: [**Open**](/windows/desktop/api/D3DCommon/nf-d3dcommon-id3dinclude-open) and [**Close**](/windows/desktop/api/D3DCommon/nf-d3dcommon-id3dinclude-close).</span></span> <span data-ttu-id="c9e4a-127">Implémentez le comportement personnalisé dans ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="c9e4a-127">Implement the custom behavior in these methods.</span></span>

## <a name="searching-for-include-files"></a><span data-ttu-id="c9e4a-128">Recherche de fichiers include</span><span class="sxs-lookup"><span data-stu-id="c9e4a-128">Searching for Include Files</span></span>

<span data-ttu-id="c9e4a-129">Le pointeur que le compilateur transmet dans le paramètre *pParentData* à la méthode [**Open**](/windows/desktop/api/D3DCommon/nf-d3dcommon-id3dinclude-open) de votre gestionnaire include peut ne pas pointer vers le conteneur qui inclut le \# fichier include dont le compilateur a besoin pour compiler le code de votre nuanceur.</span><span class="sxs-lookup"><span data-stu-id="c9e4a-129">The pointer that the compiler passes in the *pParentData* parameter to your include handler's [**Open**](/windows/desktop/api/D3DCommon/nf-d3dcommon-id3dinclude-open) method might not point to the container that includes the \#include file that the compiler needs to compile your shader code.</span></span> <span data-ttu-id="c9e4a-130">Autrement dit, le compilateur peut passer **null** dans *pParentData*.</span><span class="sxs-lookup"><span data-stu-id="c9e4a-130">That is, the compiler might pass **NULL** in *pParentData*.</span></span> <span data-ttu-id="c9e4a-131">Par conséquent, nous recommandons que votre gestionnaire d’inclusion recherche sa propre liste d’emplacements include pour le contenu.</span><span class="sxs-lookup"><span data-stu-id="c9e4a-131">Therefore, we recommend that your include handler search its own list of include locations for content.</span></span> <span data-ttu-id="c9e4a-132">Votre gestionnaire include peut ajouter dynamiquement de nouveaux emplacements include lorsqu’il reçoit ces emplacements dans les appels à sa méthode **Open** .</span><span class="sxs-lookup"><span data-stu-id="c9e4a-132">Your include handler can dynamically add new include locations as it receives those locations in calls to its **Open** method.</span></span>

<span data-ttu-id="c9e4a-133">Dans l’exemple suivant, supposons que les fichiers include du code du nuanceur sont tous deux stockés dans le répertoire *somewhereelse* .</span><span class="sxs-lookup"><span data-stu-id="c9e4a-133">In the following example, suppose that the shader code's include files are both stored in the *somewhereelse* directory.</span></span> <span data-ttu-id="c9e4a-134">Lorsque le compilateur appelle la méthode [**Open**](/windows/desktop/api/D3DCommon/nf-d3dcommon-id3dinclude-open) du gestionnaire include pour ouvrir et lire le contenu de *somewhereelse \\ foo. h*, le gestionnaire include peut enregistrer l’emplacement du répertoire **somewhereelse** .</span><span class="sxs-lookup"><span data-stu-id="c9e4a-134">When the compiler calls the include handler's [**Open**](/windows/desktop/api/D3DCommon/nf-d3dcommon-id3dinclude-open) method to open and read the contents of *somewhereelse\\foo.h*, the include handler can save the location of the **somewhereelse** directory.</span></span> <span data-ttu-id="c9e4a-135">Plus tard, lorsque le compilateur appelle la méthode **Open** du gestionnaire include pour ouvrir et lire le contenu de *bar. h*, le gestionnaire include peut effectuer une recherche automatique dans le répertoire *somewhereelse* pour *bar. h*.</span><span class="sxs-lookup"><span data-stu-id="c9e4a-135">Later, when the compiler calls the include handler's **Open** method to open and read the contents of *bar.h*, the include handler can automatically search in the *somewhereelse* directory for *bar.h*.</span></span>


```
Main.hlsl:
#include "somewhereelse\foo.h"

Foo.h:
#include "bar.h"
```



## <a name="macros"></a><span data-ttu-id="c9e4a-136">Macros</span><span class="sxs-lookup"><span data-stu-id="c9e4a-136">Macros</span></span>

<span data-ttu-id="c9e4a-137">La compilation des effets peut également prendre un pointeur vers les macros définies ailleurs.</span><span class="sxs-lookup"><span data-stu-id="c9e4a-137">Effect compilation can also take a pointer to macros that are defined elsewhere.</span></span> <span data-ttu-id="c9e4a-138">Par exemple, supposons que vous souhaitiez modifier l’effet dans BasicHLSL10 pour utiliser deux macros : zéro et un.</span><span class="sxs-lookup"><span data-stu-id="c9e4a-138">For example, suppose you want to modify the effect in BasicHLSL10, to use two macros: zero and one.</span></span> <span data-ttu-id="c9e4a-139">Le code d’effet qui utilise les deux macros est présenté ici.</span><span class="sxs-lookup"><span data-stu-id="c9e4a-139">The effect code that uses the two macros is shown here.</span></span>


```
if( bAnimate )
    vAnimatedPos += float4(vNormal, zero) *  
        (sin(g_fTime+5.5)+0.5)*5;
        
    Output.Diffuse.a = one;         
```



<span data-ttu-id="c9e4a-140">Voici la déclaration pour les deux macros.</span><span class="sxs-lookup"><span data-stu-id="c9e4a-140">Here is the declaration for the two macros.</span></span>


```
D3D10_SHADER_MACRO Shader_Macros[3] = { "zero", "0", "one", "1.0f", NULL, NULL };
```



<span data-ttu-id="c9e4a-141">Les macros sont un tableau de macros se terminant par un caractère NULL ; où chaque macro est définie à l’aide d’un struct de [**\_ \_ macro de nuanceur D3D10**](/windows/desktop/api/d3dcommon/ns-d3dcommon-d3d_shader_macro) .</span><span class="sxs-lookup"><span data-stu-id="c9e4a-141">The macros are a NULL-terminated array of macros; where each macro is defined by using a [**D3D10\_SHADER\_MACRO**](/windows/desktop/api/d3dcommon/ns-d3dcommon-d3d_shader_macro) struct.</span></span>

<span data-ttu-id="c9e4a-142">Modifiez l’appel de l’effet de compilation pour prendre un pointeur vers les macros.</span><span class="sxs-lookup"><span data-stu-id="c9e4a-142">Modify the compile effect call to take a pointer to the macros.</span></span>


```
D3DX11CompileFromFile( str, Shader_Macros, NULL, pFunctionName, 
                       pProfile, D3D10_SHADER_ENABLE_STRICTNESS, NULL, 
                       NULL, &pBlob, &pErrorBlob, NULL );    
```



## <a name="hlsl-shader-flags"></a><span data-ttu-id="c9e4a-143">Indicateurs de nuanceur HLSL</span><span class="sxs-lookup"><span data-stu-id="c9e4a-143">HLSL Shader Flags</span></span>

<span data-ttu-id="c9e4a-144">Les indicateurs de nuanceur spécifient des contraintes de nuanceur pour le compilateur HLSL.</span><span class="sxs-lookup"><span data-stu-id="c9e4a-144">Shader flags specify shader constraints to the HLSL compiler.</span></span> <span data-ttu-id="c9e4a-145">Ces indicateurs affectent le code généré par le compilateur du nuanceur des manières suivantes :</span><span class="sxs-lookup"><span data-stu-id="c9e4a-145">These flags affect the code generated by the shader compiler in the following ways:</span></span>

-   <span data-ttu-id="c9e4a-146">Optimisez la taille du code.</span><span class="sxs-lookup"><span data-stu-id="c9e4a-146">Optimize the code size.</span></span>
-   <span data-ttu-id="c9e4a-147">Y compris les informations de débogage, qui empêchent le contrôle de Flow.</span><span class="sxs-lookup"><span data-stu-id="c9e4a-147">Including debug information, which prevents flow control.</span></span>
-   <span data-ttu-id="c9e4a-148">Affecte la cible de compilation et si un nuanceur peut s’exécuter sur du matériel hérité.</span><span class="sxs-lookup"><span data-stu-id="c9e4a-148">Affects the compile target and whether a shader can run on legacy hardware.</span></span>

<span data-ttu-id="c9e4a-149">Ces indicateurs peuvent être combinés de manière logique si vous n’avez pas spécifié deux caractéristiques conflictuelles.</span><span class="sxs-lookup"><span data-stu-id="c9e4a-149">These flags can be logically combined if you have not specified two conflicting characteristics.</span></span> <span data-ttu-id="c9e4a-150">Pour obtenir la liste des indicateurs, [consultez \_ constantes de nuanceur D3D10](/windows/desktop/direct3d10/d3d10-shader).</span><span class="sxs-lookup"><span data-stu-id="c9e4a-150">For a listing of the flags see [D3D10\_SHADER Constants](/windows/desktop/direct3d10/d3d10-shader).</span></span>

## <a name="fx-flags"></a><span data-ttu-id="c9e4a-151">Indicateurs FX</span><span class="sxs-lookup"><span data-stu-id="c9e4a-151">FX Flags</span></span>

<span data-ttu-id="c9e4a-152">Utilisez ces indicateurs quand vous créez un effet pour définir le comportement de la compilation ou le comportement de l’effet d’exécution.</span><span class="sxs-lookup"><span data-stu-id="c9e4a-152">Use these flags when you create an effect to define either compilation behavior or runtime effect behavior.</span></span> <span data-ttu-id="c9e4a-153">Pour obtenir la liste des indicateurs, [consultez \_ constantes Effect D3D10](/windows/desktop/direct3d10/d3d10-effect).</span><span class="sxs-lookup"><span data-stu-id="c9e4a-153">For a listing of the flags see [D3D10\_EFFECT Constants](/windows/desktop/direct3d10/d3d10-effect).</span></span>

## <a name="checking-errors"></a><span data-ttu-id="c9e4a-154">Vérification des erreurs</span><span class="sxs-lookup"><span data-stu-id="c9e4a-154">Checking Errors</span></span>

<span data-ttu-id="c9e4a-155">Si, au cours de la compilation, une erreur se produit, l’API retourne une interface qui contient les erreurs du compilateur d’effet.</span><span class="sxs-lookup"><span data-stu-id="c9e4a-155">If during compilation an error occurs, the API returns an interface that contains the errors from the effect compiler.</span></span> <span data-ttu-id="c9e4a-156">Cette interface est appelée [**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="c9e4a-156">This interface is called [**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85)).</span></span> <span data-ttu-id="c9e4a-157">Elle n’est pas directement lisible ; Toutefois, en retournant un pointeur vers la mémoire tampon qui contient les données (qui est une chaîne), vous pouvez voir toutes les erreurs de compilation.</span><span class="sxs-lookup"><span data-stu-id="c9e4a-157">It is not directly readable; however, by returning a pointer to the buffer that contains the data (which is a string), you can see any compilation errors.</span></span>

<span data-ttu-id="c9e4a-158">Cet exemple contient une erreur dans BasicHLSL. FX, la première déclaration de variable se produit deux fois.</span><span class="sxs-lookup"><span data-stu-id="c9e4a-158">This example contains an error in the BasicHLSL.fx, the first variable declaration occurs twice.</span></span>


```
//-------------------------------------------------------------------
// Global variables
//-------------------------------------------------------------------
float4 g_MaterialAmbientColor;      // Material's ambient color

// Declare the same variable twice
float4 g_MaterialAmbientColor;      // Material's ambient color
```



<span data-ttu-id="c9e4a-159">Cette erreur force le compilateur à retourner l’erreur suivante, comme illustré dans la capture d’écran suivante du Fenêtre Espion dans Microsoft Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="c9e4a-159">This error causes the compiler to return the following error, as shown in the following screen shot of the Watch window in Microsoft Visual Studio.</span></span>

![capture d’écran de la fenêtre Espion de Visual Studio avec une erreur 0x01997fb8](images/effect-compile-errors-2.jpg)

<span data-ttu-id="c9e4a-161">Étant donné que le compilateur retourne l’erreur dans un pointeur LPVOID, effectuez un cast de celui-ci en une chaîne de caractères dans le Fenêtre Espion.</span><span class="sxs-lookup"><span data-stu-id="c9e4a-161">Because the compiler returns the error in a LPVOID pointer, cast it to a character string in the Watch window.</span></span>

<span data-ttu-id="c9e4a-162">Voici le code qui retourne l’erreur de la compilation ayant échoué.</span><span class="sxs-lookup"><span data-stu-id="c9e4a-162">Here is the code that returns the error from the failed compile.</span></span>


```
// Read the D3DX effect file
WCHAR str[MAX_PATH];
ID3DBlob*   l_pBlob_Effect = NULL;
ID3DBlob*   l_pBlob_Errors = NULL;
hr = DXUTFindDXSDKMediaFileCch( str, MAX_PATH, L"BasicHLSL10.fx" );
hr = D3DX11CompileFromFile( str, NULL, NULL, pFunctionName, 
                       pProfile, D3D10_SHADER_ENABLE_STRICTNESS, NULL, 
                       NULL, &pBlob, &pErrorBlob, NULL );      

LPVOID l_pError = NULL;
if( pErrorBlob )
{
    l_pError = pErrorBlob->GetBufferPointer();
    // then cast to a char* to see it in the locals window
}
```



## <a name="related-topics"></a><span data-ttu-id="c9e4a-163">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c9e4a-163">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c9e4a-164">Rendu d’un effet (Direct3D 11)</span><span class="sxs-lookup"><span data-stu-id="c9e4a-164">Rendering an Effect (Direct3D 11)</span></span>](d3d11-graphics-programming-guide-effects-render.md)
</dt> </dl>

 

 