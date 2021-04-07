---
title: Applications auxiliaires HLSL
description: Pour aider les auteurs d’effet à écrire des nuanceurs de pixels pouvant être liés, d2d1effecthelpers. hlsli définit un ensemble d’extensions de langage HLSL sous la forme de méthodes d’assistance et de macros.
ms.assetid: 5D0BB99E-7C77-4D45-82E6-F038E4B752A4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec8f43447c16d93ef9e1839ac319c761b975222a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103939730"
---
# <a name="hlsl-helpers"></a><span data-ttu-id="ea99f-103">Applications auxiliaires HLSL</span><span class="sxs-lookup"><span data-stu-id="ea99f-103">HLSL Helpers</span></span>

<span data-ttu-id="ea99f-104">Pour aider les auteurs d’effet à écrire des nuanceurs de pixels pouvant être liés, d2d1effecthelpers. hlsli définit un ensemble d’extensions de langage HLSL sous la forme de méthodes d’assistance et de macros.</span><span class="sxs-lookup"><span data-stu-id="ea99f-104">To assist effect authors in writing linkable pixel shaders, d2d1effecthelpers.hlsli defines a set of HLSL language extensions in the form of helper methods and macros.</span></span>

<span data-ttu-id="ea99f-105">Pour ajouter d2d1effecthelpers. hlsli à votre projet, ajoutez une \# instruction include dans le fichier HLSL.</span><span class="sxs-lookup"><span data-stu-id="ea99f-105">To add d2d1effecthelpers.hlsli to your project, add an \#include statement in the HLSL file.</span></span> <span data-ttu-id="ea99f-106">d2d1effecthelpers. hlsli se trouve au même emplacement que les autres en-têtes Direct2D tels que d2d1. h ; elle peut être référencée à partir de la page de propriétés du fichier HLSL en ajoutant la macro $ (WindowsSDK \_ INCLUDEPATH) à la propriété autres répertoires Include.</span><span class="sxs-lookup"><span data-stu-id="ea99f-106">d2d1effecthelpers.hlsli is located in the same location as other Direct2D headers such as d2d1.h; it can be referenced from the HLSL file's property page by adding the macro $(WindowsSDK\_IncludePath) to the Additional Include Directories property.</span></span> <span data-ttu-id="ea99f-107">Notez que l' \# instruction include doit venir après toutes les directives de préprocesseur \_ . ce nombre d’entrées D2D \_ a été défini.</span><span class="sxs-lookup"><span data-stu-id="ea99f-107">Note that the \#include statement must come after any preprocessor directives such D2D\_INPUT\_COUNT have been defined.</span></span>

``` syntax
#include <d2d1effecthelpers.hlsli>
```

<span data-ttu-id="ea99f-108">Direct2D ne prend pas en charge la liaison des nuanceurs de calcul ou de vertex.</span><span class="sxs-lookup"><span data-stu-id="ea99f-108">Direct2D does not support linking compute or vertex shaders.</span></span> <span data-ttu-id="ea99f-109">Toutefois, si votre effet utilise à la fois un nuanceur de sommets et un nuanceur de pixels, la sortie du nuanceur de pixels peut toujours être liée.</span><span class="sxs-lookup"><span data-stu-id="ea99f-109">However, if your effect uses both a vertex shader and pixel shader, the output of the pixel shader can still be linked.</span></span>

## <a name="preprocessor-directives"></a><span data-ttu-id="ea99f-110">Directives de préprocesseur</span><span class="sxs-lookup"><span data-stu-id="ea99f-110">Preprocessor Directives</span></span>

<span data-ttu-id="ea99f-111">Des directives de préprocesseur sont requises pour communiquer des informations sur l’effet.</span><span class="sxs-lookup"><span data-stu-id="ea99f-111">Preprocessor directives are required to communicate information about the effect.</span></span> <span data-ttu-id="ea99f-112">Cela comprend le nombre d’entrées et le type d’échantillonnage de chaque entrée.</span><span class="sxs-lookup"><span data-stu-id="ea99f-112">This includes the number of inputs and sampling type of each input.</span></span> <span data-ttu-id="ea99f-113">Les valeurs suivantes doivent être définies dans le code du nuanceur d’effet au-dessus du point d’entrée du nuanceur approprié, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="ea99f-113">The following values should be defined in the effect shader code above the relevant shader entry point when applicable.</span></span>

-   <span data-ttu-id="ea99f-114">`D2D_INPUT_COUNT <N>` : Déclare le nombre d’entrées de texture à l’effet.</span><span class="sxs-lookup"><span data-stu-id="ea99f-114">`D2D_INPUT_COUNT <N>` : Declares the number of texture inputs to the effect.</span></span> <span data-ttu-id="ea99f-115">Si l’effet a un nombre variable d’entrées, cette valeur doit être étendue de manière appropriée à chaque point d’entrée du nuanceur.</span><span class="sxs-lookup"><span data-stu-id="ea99f-115">If the effect has a variable number of inputs, this value must be scoped appropriately to each shader entry point.</span></span> <span data-ttu-id="ea99f-116">La définition de cette valeur est obligatoire.</span><span class="sxs-lookup"><span data-stu-id="ea99f-116">Defining this value is mandatory.</span></span>
-   <span data-ttu-id="ea99f-117">`D2D_INPUT<N>_SIMPLE` : Déclare la nième entrée pour utiliser l’échantillonnage simple.</span><span class="sxs-lookup"><span data-stu-id="ea99f-117">`D2D_INPUT<N>_SIMPLE` : Declares the Nth input to use simple sampling.</span></span> <span data-ttu-id="ea99f-118">S’il n’est pas défini, l’entrée nth est par défaut complexe.</span><span class="sxs-lookup"><span data-stu-id="ea99f-118">If not defined, the Nth input defaults to complex.</span></span> <span data-ttu-id="ea99f-119">La définition de cette valeur est facultative.</span><span class="sxs-lookup"><span data-stu-id="ea99f-119">Defining this value is optional.</span></span>
-   <span data-ttu-id="ea99f-120">`D2D_INPUT<N>_COMPLEX` : Déclare la nième entrée pour utiliser un échantillonnage complexe.</span><span class="sxs-lookup"><span data-stu-id="ea99f-120">`D2D_INPUT<N>_COMPLEX` : Declares the Nth input to use complex sampling.</span></span> <span data-ttu-id="ea99f-121">S’il n’est pas défini, l’entrée nth est par défaut complexe.</span><span class="sxs-lookup"><span data-stu-id="ea99f-121">If not defined, the Nth input defaults to complex.</span></span> <span data-ttu-id="ea99f-122">La définition de cette valeur est facultative.</span><span class="sxs-lookup"><span data-stu-id="ea99f-122">Defining this value is optional.</span></span>
-   <span data-ttu-id="ea99f-123">`D2D_REQUIRES_SCENE_POSITION` : Indique que la fonction de nuanceur appelle les méthodes d’assistance qui utilisent la valeur de position de la scène (à savoir, la fonction d’assistance [D2DGetScenePosition](d2dgetsceneposition.md) ).</span><span class="sxs-lookup"><span data-stu-id="ea99f-123">`D2D_REQUIRES_SCENE_POSITION` : Indicates that the shader function calls helper methods that use the scene position value (namely, the [D2DGetScenePosition](d2dgetsceneposition.md) helper function).</span></span> <span data-ttu-id="ea99f-124">Ce paramètre doit être inclus uniquement lorsque cela est nécessaire, car une seule fonction par nuanceur lié peut utiliser ce paramètre.</span><span class="sxs-lookup"><span data-stu-id="ea99f-124">This parameter should only be included when necessary, since only one function per linked shader can utilize this parameter.</span></span> <span data-ttu-id="ea99f-125">La définition de cette valeur est facultative.</span><span class="sxs-lookup"><span data-stu-id="ea99f-125">Defining this value is optional.</span></span>
-   <span data-ttu-id="ea99f-126">`D2D_CUSTOM_ENTRY` : Indique que la fonction de nuanceur de pixels consomme la sortie d’un nuanceur de sommets personnalisé, et déclare donc ses paramètres d’entrée.</span><span class="sxs-lookup"><span data-stu-id="ea99f-126">`D2D_CUSTOM_ENTRY` : Indicates that the pixel shader function consumes the output of a custom vertex shader, and thus will declare its input parameters.</span></span> <span data-ttu-id="ea99f-127">Toutes les entrées de nuanceur de vertex personnalisées utilisent un échantillonnage complexe et ne peuvent pas consommer la sortie d’une autre fonction de nuanceur (c’est-à-dire qu’elles ne sont qu’après liaison).</span><span class="sxs-lookup"><span data-stu-id="ea99f-127">All custom vertex shader inputs use complex sampling, and cannot consume the output of another shader function (i.e. they are only post-linkable).</span></span> <span data-ttu-id="ea99f-128">La définition de cette valeur est facultative.</span><span class="sxs-lookup"><span data-stu-id="ea99f-128">Defining this value is optional.</span></span>

<span data-ttu-id="ea99f-129">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="ea99f-129">For example:</span></span>

``` syntax
#define D2D_INPUT_COUNT 3
#define D2D_INPUT0_SIMPLE
#define D2D_INPUT1_SIMPLE
#define D2D_INPUT2_COMPLEX
#include <d2d1effecthelpers.hlsli>
          
```

## <a name="helper-functions"></a><span data-ttu-id="ea99f-130">Fonctions d’assistance</span><span class="sxs-lookup"><span data-stu-id="ea99f-130">Helper Functions</span></span>

<span data-ttu-id="ea99f-131">Les fonctions d’assistance sont utilisées comme remplacement pour certaines fonctions intrinsèques HLSL natives.</span><span class="sxs-lookup"><span data-stu-id="ea99f-131">Helper functions are used as a replacement for some native HLSL intrinsic functions.</span></span> <span data-ttu-id="ea99f-132">Au moment de la compilation, ces fonctions d’assistance sont redéfinies par Direct2D dans la version appropriée en fonction du type de cible de compilation (nuanceur complet ou fonction d’exportation).</span><span class="sxs-lookup"><span data-stu-id="ea99f-132">At compile time, these helper functions are redefined by Direct2D into the appropriate version depending on the compilation target type (full shader or export function).</span></span>

<span data-ttu-id="ea99f-133">Fonctions d’assistance :</span><span class="sxs-lookup"><span data-stu-id="ea99f-133">The helper functions:</span></span>

<dl>

[<span data-ttu-id="ea99f-134">D2DGetInput</span><span class="sxs-lookup"><span data-stu-id="ea99f-134">D2DGetInput</span></span>](d2dgetinput.md)  
[<span data-ttu-id="ea99f-135">D2DSampleInput</span><span class="sxs-lookup"><span data-stu-id="ea99f-135">D2DSampleInput</span></span>](d2dsampleinput.md)  
[<span data-ttu-id="ea99f-136">D2DSampleInputAtOffset</span><span class="sxs-lookup"><span data-stu-id="ea99f-136">D2DSampleInputAtOffset</span></span>](d2dsampleinputatoffset.md)  
[<span data-ttu-id="ea99f-137">D2DSampleInputAtPosition</span><span class="sxs-lookup"><span data-stu-id="ea99f-137">D2DSampleInputAtPosition</span></span>](d2dsampleinputatposition.md)  
[<span data-ttu-id="ea99f-138">D2DGetInputCoordinate</span><span class="sxs-lookup"><span data-stu-id="ea99f-138">D2DGetInputCoordinate</span></span>](d2dgetinputcoordinate.md)  
[<span data-ttu-id="ea99f-139">D2DGetScenePosition</span><span class="sxs-lookup"><span data-stu-id="ea99f-139">D2DGetScenePosition</span></span>](d2dgetsceneposition.md)  
[<span data-ttu-id="ea99f-140">Entrée de la \_ PS D2D \_</span><span class="sxs-lookup"><span data-stu-id="ea99f-140">D2D\_PS\_ENTRY</span></span>](d2d-ps-entry.md)  
</dl>

## <a name="related-topics"></a><span data-ttu-id="ea99f-141">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ea99f-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ea99f-142">Liaison de nuanceurs d’effet</span><span class="sxs-lookup"><span data-stu-id="ea99f-142">Effect Shader Linking</span></span>](effect-shader-linking.md)
</dt> </dl>

 

 




