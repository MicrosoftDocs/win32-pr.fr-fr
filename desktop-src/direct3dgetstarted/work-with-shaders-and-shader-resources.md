---
title: Utiliser des nuanceurs et des ressources de nuanceur
description: Il est temps d’apprendre à utiliser des nuanceurs et des ressources de nuanceur dans le développement de votre jeu Microsoft DirectX pour Windows 8.
ms.assetid: 25a11983-e3f6-4bd3-86f1-d660edc4cd4b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26ac147971221b04b02f2a45af8e8d4f6855a5e3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382154"
---
# <a name="work-with-shaders-and-shader-resources"></a><span data-ttu-id="e827a-103">Utiliser des nuanceurs et des ressources de nuanceur</span><span class="sxs-lookup"><span data-stu-id="e827a-103">Work with shaders and shader resources</span></span>

<span data-ttu-id="e827a-104">Il est temps d’apprendre à utiliser des nuanceurs et des ressources de nuanceur dans le développement de votre jeu Microsoft DirectX pour Windows 8.</span><span class="sxs-lookup"><span data-stu-id="e827a-104">It's time to learn how to work with shaders and shader resources in developing your Microsoft DirectX game for Windows 8.</span></span> <span data-ttu-id="e827a-105">Nous avons vu comment configurer le périphérique graphique et les ressources, et peut-être même avoir commencé à modifier son pipeline.</span><span class="sxs-lookup"><span data-stu-id="e827a-105">We've seen how to set up the graphics device and resources, and perhaps you've even started modifying its pipeline.</span></span> <span data-ttu-id="e827a-106">Examinons maintenant les nuanceurs de pixels et vertex.</span><span class="sxs-lookup"><span data-stu-id="e827a-106">So now let's look at pixel and vertex shaders.</span></span>

<span data-ttu-id="e827a-107">Si vous n’êtes pas familiarisé avec les langages de nuanceur, une discussion rapide est dans l’ordre.</span><span class="sxs-lookup"><span data-stu-id="e827a-107">If you aren't familiar with shader languages, a quick discussion is in order.</span></span> <span data-ttu-id="e827a-108">Les nuanceurs sont de petits programmes de bas niveau qui sont compilés et exécutés à des étapes spécifiques du pipeline Graphics.</span><span class="sxs-lookup"><span data-stu-id="e827a-108">Shaders are small, low-level programs that are compiled and run at specific stages in the graphics pipeline.</span></span> <span data-ttu-id="e827a-109">Leurs spécialisations sont des opérations mathématiques à virgule flottante très rapides.</span><span class="sxs-lookup"><span data-stu-id="e827a-109">Their specialty is very fast floating-point mathematical operations.</span></span> <span data-ttu-id="e827a-110">Les programmes nuanceurs les plus courants sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="e827a-110">The most common shader programs are:</span></span>

-   <span data-ttu-id="e827a-111">**Vertex shader**— exécuté pour chaque vertex d’une scène.</span><span class="sxs-lookup"><span data-stu-id="e827a-111">**Vertex shader**—Executed for each vertex in a scene.</span></span> <span data-ttu-id="e827a-112">Ce nuanceur opère sur les éléments de mémoire tampon de vertex qui lui sont fournis par l’application appelante, et produit au minimum un vecteur de position à 4 composants qui sera pixellisé en position de pixel.</span><span class="sxs-lookup"><span data-stu-id="e827a-112">This shader operates on vertex buffer elements provided to it by the calling app, and minimally results in a 4-component position vector that will be rasterized into a pixel position.</span></span>
-   <span data-ttu-id="e827a-113">**Nuanceur de pixels**: exécution pour chaque pixel dans une cible de rendu.</span><span class="sxs-lookup"><span data-stu-id="e827a-113">**Pixel shader**—Executed for each pixel in a render target.</span></span> <span data-ttu-id="e827a-114">Ce nuanceur reçoit les coordonnées pixellisées des précédentes étapes de nuanceur (dans les pipelines les plus simples, il s’agit du nuanceur de sommets) et retourne une couleur (ou une autre valeur de 4 composants) pour cette position de pixel, qui est ensuite écrite dans une cible de rendu.</span><span class="sxs-lookup"><span data-stu-id="e827a-114">This shader receives rasterized coordinates from previous shader stages (in the simplest pipelines, this would be the vertex shader) and returns a color (or other 4-component value) for that pixel position, which is then written into a render target.</span></span>

<span data-ttu-id="e827a-115">Cet exemple comprend des nuanceurs de sommets et de pixels très basiques qui dessinent uniquement la géométrie et des nuanceurs plus complexes qui ajoutent des calculs d’éclairage de base.</span><span class="sxs-lookup"><span data-stu-id="e827a-115">This example includes very basic vertex and pixel shaders that only draw geometry, and more complex shaders that add basic lighting calculations.</span></span>

<span data-ttu-id="e827a-116">Les programmes de nuanceur sont écrits en HLSL (High Level Shader Language).</span><span class="sxs-lookup"><span data-stu-id="e827a-116">Shader programs are written in Microsoft High Level Shader Language (HLSL).</span></span> <span data-ttu-id="e827a-117">La syntaxe HLSL ressemble beaucoup à C, mais sans les pointeurs.</span><span class="sxs-lookup"><span data-stu-id="e827a-117">HLSL syntax looks a lot like C, but without the pointers.</span></span> <span data-ttu-id="e827a-118">Les programmes de nuanceur doivent être très compacts et efficaces.</span><span class="sxs-lookup"><span data-stu-id="e827a-118">Shader programs must be very compact and efficient.</span></span> <span data-ttu-id="e827a-119">Si votre nuanceur est compilé en trop d’instructions, il ne peut pas être exécuté et une erreur est retournée.</span><span class="sxs-lookup"><span data-stu-id="e827a-119">If your shader compiles to too many instructions, it cannot be run and an error is returned.</span></span> <span data-ttu-id="e827a-120">(Notez que le nombre exact d’instructions autorisées fait partie du [niveau de fonctionnalité Direct3D](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro).)</span><span class="sxs-lookup"><span data-stu-id="e827a-120">(Note that the exact number of instructions allowed is part of the [Direct3D feature level](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro).)</span></span>

<span data-ttu-id="e827a-121">Dans Direct3D, les nuanceurs ne sont pas compilés au moment de l’exécution ; elles sont compilées lors de la compilation du reste du programme.</span><span class="sxs-lookup"><span data-stu-id="e827a-121">In Direct3D, shaders are not compiled at run time; they are compiled when the rest of the program is compiled.</span></span> <span data-ttu-id="e827a-122">Quand vous compilez votre application avec Microsoft Visual Studio 2013, les fichiers HLSL sont compilés en fichiers CSO (. CSO) que votre application doit charger et placer dans la mémoire GPU avant le dessin.</span><span class="sxs-lookup"><span data-stu-id="e827a-122">When you compile your app with Microsoft Visual Studio 2013, the HLSL files are compiled to CSO (.cso) files that your app must load and place in GPU memory prior to drawing.</span></span> <span data-ttu-id="e827a-123">Veillez à inclure ces fichiers CSO avec votre application lorsque vous l’Empaquetez ; Il s’agit de ressources, comme les maillages et les textures.</span><span class="sxs-lookup"><span data-stu-id="e827a-123">Make sure you include these CSO files with your app when you package it; they are assets just like meshes and textures.</span></span>

## <a name="understand-hlsl-semantics"></a><span data-ttu-id="e827a-124">Comprendre la sémantique HLSL</span><span class="sxs-lookup"><span data-stu-id="e827a-124">Understand HLSL semantics</span></span>

<span data-ttu-id="e827a-125">Il est important de prendre un moment pour aborder la sémantique HLSL avant de continuer, car ils sont souvent un point de confusion pour les nouveaux développeurs Direct3D.</span><span class="sxs-lookup"><span data-stu-id="e827a-125">It's important to take a moment to discuss HLSL semantics before we continue, because they are often a point of confusion for new Direct3D developers.</span></span> <span data-ttu-id="e827a-126">La sémantique HLSL est une chaîne qui identifie une valeur transmise entre l’application et un programme Shader.</span><span class="sxs-lookup"><span data-stu-id="e827a-126">HLSL semantics are strings that identify a value passed between the app and a shader program.</span></span> <span data-ttu-id="e827a-127">Bien qu’il puisse s’agir de l’une des nombreuses chaînes possibles, il est recommandé d’utiliser une chaîne comme `POSITION` ou `COLOR` qui indique l’utilisation.</span><span class="sxs-lookup"><span data-stu-id="e827a-127">Although they can be any of a variety of possible strings, the best practice is to use a string like `POSITION` or `COLOR` that indicates the usage.</span></span> <span data-ttu-id="e827a-128">Vous assignez ces sémantiques lorsque vous construisez une mémoire tampon constante ou une disposition d’entrée.</span><span class="sxs-lookup"><span data-stu-id="e827a-128">You assign these semantics when you are constructing a constant buffer or input layout.</span></span> <span data-ttu-id="e827a-129">Vous pouvez aussi ajouter un nombre compris entre 0 et 7 à la sémantique afin d’utiliser des registres séparés pour des valeurs similaires.</span><span class="sxs-lookup"><span data-stu-id="e827a-129">You can also append a number between 0 and 7 to the semantic so that you use separate registers for similar values.</span></span> <span data-ttu-id="e827a-130">Par exemple : COLOR0, COLOR1, COLOR2…</span><span class="sxs-lookup"><span data-stu-id="e827a-130">For example: COLOR0, COLOR1, COLOR2...</span></span>

<span data-ttu-id="e827a-131">Les sémantiques précédées de « SV \_ » sont des sémantiques de *valeurs système* qui sont écrites par votre programme de nuanceur ; votre jeu (en cours d’exécution sur le processeur) ne peut pas les modifier.</span><span class="sxs-lookup"><span data-stu-id="e827a-131">Semantics that are prefixed with "SV\_" are *system value* semantics that are written to by your shader program; your game itself (running on the CPU) cannot modify them.</span></span> <span data-ttu-id="e827a-132">En règle générale, ces sémantiques contiennent des valeurs qui sont des entrées ou sorties d’une autre étape de nuanceur dans le pipeline graphique, ou qui sont entièrement générées par le GPU.</span><span class="sxs-lookup"><span data-stu-id="e827a-132">Typically, these semantics contain values that are inputs or outputs from another shader stage in the graphics pipeline, or that are generated entirely by the GPU.</span></span>

<span data-ttu-id="e827a-133">En outre, `SV_` la sémantique a des comportements différents lorsqu’ils sont utilisés pour spécifier une entrée ou une sortie à partir d’une étape de nuanceur.</span><span class="sxs-lookup"><span data-stu-id="e827a-133">Additionally, `SV_` semantics have different behaviors when they are used to specify input to or output from a shader stage.</span></span> <span data-ttu-id="e827a-134">Par exemple, `SV_POSITION` (output) contient les données de vertex transformées pendant l’étape du nuanceur de sommets, et `SV_POSITION` (*Input*) contient les valeurs de position de pixel interpolées par le GPU pendant l’étape de pixellisation.</span><span class="sxs-lookup"><span data-stu-id="e827a-134">For example, `SV_POSITION` (output) contains the vertex data transformed during the vertex shader stage, and `SV_POSITION` (*input*) contains the pixel position values that were interpolated by the GPU during the rasterization stage.</span></span>

<span data-ttu-id="e827a-135">Voici quelques sémantiques HLSL courantes :</span><span class="sxs-lookup"><span data-stu-id="e827a-135">Here are a few common HLSL semantics:</span></span>

-   <span data-ttu-id="e827a-136">`POSITION`(*n*) pour les données de mémoire tampon de vertex.</span><span class="sxs-lookup"><span data-stu-id="e827a-136">`POSITION`(*n*) for vertex buffer data.</span></span> <span data-ttu-id="e827a-137">`SV_POSITION` fournit une position de pixel au nuanceur de pixels et ne peut pas être écrite par votre jeu.</span><span class="sxs-lookup"><span data-stu-id="e827a-137">`SV_POSITION` provides a pixel position to the pixel shader and cannot be written by your game.</span></span>
-   <span data-ttu-id="e827a-138">`NORMAL`(*n*) pour les données normales fournies par la mémoire tampon de vertex.</span><span class="sxs-lookup"><span data-stu-id="e827a-138">`NORMAL`(*n*) for normal data provided by the vertex buffer.</span></span>
-   <span data-ttu-id="e827a-139">`TEXCOORD`(*n*) pour les données de coordonnée UV de texture fournies à un nuanceur.</span><span class="sxs-lookup"><span data-stu-id="e827a-139">`TEXCOORD`(*n*) for texture UV coordinate data supplied to a shader.</span></span>
-   <span data-ttu-id="e827a-140">`COLOR`(n) pour les données de couleur RVBA fournies à un nuanceur.</span><span class="sxs-lookup"><span data-stu-id="e827a-140">`COLOR`(n) for RGBA color data supplied to a shader.</span></span> <span data-ttu-id="e827a-141">Notez qu’elle est traitée de la même façon pour coordonner les données, y compris l’interpolation de la valeur lors de la pixellisation. la sémantique vous aide simplement à identifier qu’il s’agit de données de couleur.</span><span class="sxs-lookup"><span data-stu-id="e827a-141">Note that it is treated identically to coordinate data, including interpolating the value during rasterization; the semantic simply helps you identify that it is color data.</span></span>
-   <span data-ttu-id="e827a-142">`SV_Target`\[n \] pour écrire à partir d’un nuanceur de pixels vers une texture cible ou une autre mémoire tampon de pixels.</span><span class="sxs-lookup"><span data-stu-id="e827a-142">`SV_Target`\[n\] for writing from a pixel shader to a target texture or other pixel buffer.</span></span>

<span data-ttu-id="e827a-143">Nous verrons des exemples de sémantique HLSL à mesure que nous examinerons l’exemple.</span><span class="sxs-lookup"><span data-stu-id="e827a-143">We'll see some examples of HLSL semantics as we review the example.</span></span>

## <a name="read-from-the-constant-buffers"></a><span data-ttu-id="e827a-144">Lire à partir des mémoires tampons constantes</span><span class="sxs-lookup"><span data-stu-id="e827a-144">Read from the constant buffers</span></span>

<span data-ttu-id="e827a-145">Tout nuanceur peut lire à partir d’une mémoire tampon constante si ce tampon est attaché à son étape en tant que ressource.</span><span class="sxs-lookup"><span data-stu-id="e827a-145">Any shader can read from a constant buffer if that buffer is attached to its stage as a resource.</span></span> <span data-ttu-id="e827a-146">Dans cet exemple, seul le nuanceur vertex reçoit une mémoire tampon constante.</span><span class="sxs-lookup"><span data-stu-id="e827a-146">In this example, only the vertex shader is assigned a constant buffer.</span></span>

<span data-ttu-id="e827a-147">La mémoire tampon constante est déclarée à deux emplacements : dans le code C++, et dans les fichiers HLSL correspondants qui y accèdent.</span><span class="sxs-lookup"><span data-stu-id="e827a-147">The constant buffer is declared in two places: in the C++ code, and in the corresponding HLSL files that will access it.</span></span>

<span data-ttu-id="e827a-148">Voici comment la structure de mémoire tampon constante est déclarée dans le code C++.</span><span class="sxs-lookup"><span data-stu-id="e827a-148">Here's how the constant buffer struct is declared in the C++ code.</span></span>


```C++
typedef struct _constantBufferStruct {
    DirectX::XMFLOAT4X4 world;
    DirectX::XMFLOAT4X4 view;
    DirectX::XMFLOAT4X4 projection;
} ConstantBufferStruct;
```



<span data-ttu-id="e827a-149">Lors de la déclaration de la structure pour la mémoire tampon constante dans votre code C++, assurez-vous que toutes les données sont correctement alignées sur des limites de 16 octets.</span><span class="sxs-lookup"><span data-stu-id="e827a-149">When declaring the structure for the constant buffer in your C++ code, ensure that all of the data is correctly aligned along 16-byte boundaries.</span></span> <span data-ttu-id="e827a-150">Le moyen le plus simple consiste à utiliser des types [DirectXMath](/windows/desktop/dxmath/directxmath-portal) , comme **XMFLOAT4** ou **XMFLOAT4X4**, comme indiqué dans l’exemple de code.</span><span class="sxs-lookup"><span data-stu-id="e827a-150">The easiest way to do this is to use [DirectXMath](/windows/desktop/dxmath/directxmath-portal) types, like **XMFLOAT4** or **XMFLOAT4X4**, as seen in the example code.</span></span> <span data-ttu-id="e827a-151">Vous pouvez également vous prémunir contre les mémoires tampons mal alignées en déclarant une assertion statique :</span><span class="sxs-lookup"><span data-stu-id="e827a-151">You can also guard against misaligned buffers by declaring a static assert:</span></span>


```C++
// Assert that the constant buffer remains 16-byte aligned.
static_assert((sizeof(ConstantBufferStruct) % 16) == 0, "Constant Buffer size must be 16-byte aligned");
```



<span data-ttu-id="e827a-152">Cette ligne de code génère une erreur au moment de la compilation si **ConstantBufferStruct** n’est pas aligné sur 16 octets.</span><span class="sxs-lookup"><span data-stu-id="e827a-152">This line of code will cause an error at compile time if **ConstantBufferStruct** is not 16-byte aligned.</span></span> <span data-ttu-id="e827a-153">Pour plus d’informations sur l’alignement et la compression de la mémoire tampon constante, consultez [règles de compression pour les variables constantes](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-packing-rules).</span><span class="sxs-lookup"><span data-stu-id="e827a-153">For more information about constant buffer alignment and packing, see [Packing Rules for Constant Variables](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-packing-rules).</span></span>

<span data-ttu-id="e827a-154">Voici à présent comment la mémoire tampon constante est déclarée dans le nuanceur de vertex HLSL.</span><span class="sxs-lookup"><span data-stu-id="e827a-154">Now, here's how the constant buffer is declared in the vertex shader HLSL.</span></span>


```C++
cbuffer ModelViewProjectionConstantBuffer : register(b0)
{
    matrix mWorld;      // world matrix for object
    matrix View;        // view matrix
    matrix Projection;  // projection matrix
};
```



<span data-ttu-id="e827a-155">Toutes les mémoires tampons (constante, texture, échantillonneur ou autre) doivent avoir un registre défini pour que le GPU puisse y accéder.</span><span class="sxs-lookup"><span data-stu-id="e827a-155">All buffers—constant, texture, sampler, or other—must have a register defined so the GPU can access them.</span></span> <span data-ttu-id="e827a-156">Chaque étape de nuanceur autorise jusqu’à 15 mémoires tampons constantes, et chaque mémoire tampon peut contenir jusqu’à 4 096 variables constantes.</span><span class="sxs-lookup"><span data-stu-id="e827a-156">Each shader stage allows up to 15 constant buffers, and each buffer can hold up to 4,096 constant variables.</span></span> <span data-ttu-id="e827a-157">La syntaxe de la déclaration d’utilisation des registres est la suivante :</span><span class="sxs-lookup"><span data-stu-id="e827a-157">The register-usage declaration syntax is as follows:</span></span>

-   <span data-ttu-id="e827a-158">**b \* \* *\#* : Registre pour une mémoire tampon constante (** CBuffer \* \*).</span><span class="sxs-lookup"><span data-stu-id="e827a-158">**b\*\**\#*: A register for a constant buffer (** cbuffer\*\*).</span></span>
-   <span data-ttu-id="e827a-159">**t \* \* *\#* : Registre pour une mémoire tampon de texture (** tbuffer \* \*).</span><span class="sxs-lookup"><span data-stu-id="e827a-159">**t\*\**\#*: A register for a texture buffer (** tbuffer\*\*).</span></span>
-   <span data-ttu-id="e827a-160">**s \* \#** \* : registre d’un échantillonneur.</span><span class="sxs-lookup"><span data-stu-id="e827a-160">\**s\*\*\*\#*: A register for a sampler.</span></span> <span data-ttu-id="e827a-161">(Un échantillonneur définit le comportement de recherche des texels dans la ressource de texture.)</span><span class="sxs-lookup"><span data-stu-id="e827a-161">(A sampler defines the lookup behavior for texels in the texture resource.)</span></span>

<span data-ttu-id="e827a-162">Par exemple, le HLSL pour un nuanceur de pixels peut prendre une texture et un échantillonneur comme entrée avec une déclaration comme celle-ci.</span><span class="sxs-lookup"><span data-stu-id="e827a-162">For example, the HLSL for a pixel shader might take a texture and a sampler as input with a declaration like this.</span></span>

``` syntax
Texture2D simpleTexture : register(t0);
SamplerState simpleSampler : register(s0);
```

<span data-ttu-id="e827a-163">C’est à vous d’assigner des mémoires tampons constantes aux registres : lorsque vous configurez le pipeline, vous attachez une mémoire tampon constante au même emplacement que celui auquel vous l’avez attribuée dans le fichier HLSL.</span><span class="sxs-lookup"><span data-stu-id="e827a-163">It's up to you to assign constant buffers to registers—when you set up the pipeline, you attach a constant buffer to the same slot you assigned it to in the HLSL file.</span></span> <span data-ttu-id="e827a-164">Par exemple, dans la rubrique précédente, l’appel à [**VSSetConstantBuffers**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-vssetconstantbuffers) indique « 0 » pour le premier paramètre.</span><span class="sxs-lookup"><span data-stu-id="e827a-164">For example, in the previous topic the call to [**VSSetConstantBuffers**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-vssetconstantbuffers) indicates '0' for the first parameter.</span></span> <span data-ttu-id="e827a-165">Cela indique à Direct3D d’attacher la ressource de mémoire tampon constante pour inscrire 0, ce qui correspond à l’affectation de la mémoire tampon à **Register (B0)** dans le fichier HLSL.</span><span class="sxs-lookup"><span data-stu-id="e827a-165">That tells Direct3D to attach the constant buffer resource to register 0, which matches the buffer's assignment to **register(b0)** in the HLSL file.</span></span>

## <a name="read-from-the-vertex-buffers"></a><span data-ttu-id="e827a-166">Lire à partir des mémoires tampons de vertex</span><span class="sxs-lookup"><span data-stu-id="e827a-166">Read from the vertex buffers</span></span>

<span data-ttu-id="e827a-167">La mémoire tampon de vertex fournit les données de triangle pour les objets de scène aux nuanceurs de sommets.</span><span class="sxs-lookup"><span data-stu-id="e827a-167">The vertex buffer supplies the triangle data for the scene objects to the vertex shader(s).</span></span> <span data-ttu-id="e827a-168">Comme avec la mémoire tampon constante, le struct de mémoire tampon de vertex est déclaré dans le code C++, à l’aide de règles de compression similaires.</span><span class="sxs-lookup"><span data-stu-id="e827a-168">As with the constant buffer, the vertex buffer struct is declared in the C++ code, using similar packing rules.</span></span>


```C++
typedef struct _vertexPositionColor
{
    DirectX::XMFLOAT3 pos;
    DirectX::XMFLOAT3 color;
} VertexPositionColor;
```



<span data-ttu-id="e827a-169">Il n’existe pas de format standard pour les données de vertex dans Direct3D 11.</span><span class="sxs-lookup"><span data-stu-id="e827a-169">There is no standard format for vertex data in Direct3D 11.</span></span> <span data-ttu-id="e827a-170">Au lieu de cela, nous définissons notre propre disposition des données de vertex à l’aide d’un descripteur. les champs de données sont définis à l’aide d’un tableau d' [**\_ éléments d’entrée d3d11 structures \_ \_ desc**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_input_element_desc) .</span><span class="sxs-lookup"><span data-stu-id="e827a-170">Instead, we define our own vertex data layout using a descriptor; the data fields are defined using an array of [**D3D11\_INPUT\_ELEMENT\_DESC**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_input_element_desc) structures.</span></span> <span data-ttu-id="e827a-171">Ici, nous affichons une disposition d’entrée simple qui décrit le même format de vertex que le struct précédent :</span><span class="sxs-lookup"><span data-stu-id="e827a-171">Here, we show a simple input layout that describes the same vertex format as the preceding struct:</span></span>


```C++
D3D11_INPUT_ELEMENT_DESC iaDesc [] =
{
    { "POSITION", 0, DXGI_FORMAT_R32G32B32_FLOAT,
    0, 0, D3D11_INPUT_PER_VERTEX_DATA, 0 },

    { "COLOR", 0, DXGI_FORMAT_R32G32B32_FLOAT,
    0, 12, D3D11_INPUT_PER_VERTEX_DATA, 0 },
};

hr = device->CreateInputLayout(
    iaDesc,
    ARRAYSIZE(iaDesc),
    bytes,
    bytesRead,
    &m_pInputLayout
    );
```



<span data-ttu-id="e827a-172">Si vous ajoutez des données au format de vertex lorsque vous modifiez l’exemple de code, veillez à mettre à jour également la disposition d’entrée, sinon le nuanceur ne pourra pas l’interpréter.</span><span class="sxs-lookup"><span data-stu-id="e827a-172">If you add data to the vertex format when modifying the example code, be sure to update the input layout as well, or the shader will not be able to interpret it.</span></span> <span data-ttu-id="e827a-173">Vous pouvez modifier la disposition du vertex comme suit :</span><span class="sxs-lookup"><span data-stu-id="e827a-173">You might modify the vertex layout like this:</span></span>


```C++
typedef struct _vertexPositionColorTangent
{
    DirectX::XMFLOAT3 pos;
    DirectX::XMFLOAT3 normal;
    DirectX::XMFLOAT3 tangent;
} VertexPositionColorTangent;
```



<span data-ttu-id="e827a-174">Dans ce cas, vous devez modifier la définition de la disposition d’entrée comme suit.</span><span class="sxs-lookup"><span data-stu-id="e827a-174">In that case, you'd modify the input-layout definition as follows.</span></span>


```C++
D3D11_INPUT_ELEMENT_DESC iaDescExtended[] =
{
    { "POSITION", 0, DXGI_FORMAT_R32G32B32_FLOAT,
    0, 0, D3D11_INPUT_PER_VERTEX_DATA, 0 },

    { "NORMAL", 0, DXGI_FORMAT_R32G32B32_FLOAT,
    0, 12, D3D11_INPUT_PER_VERTEX_DATA, 0 },

    { "TANGENT", 0, DXGI_FORMAT_R32G32B32_FLOAT,
    0, 12, D3D11_INPUT_PER_VERTEX_DATA, 0 },
};

hr = device->CreateInputLayout(
    iaDesc,
    ARRAYSIZE(iaDesc),
    bytes,
    bytesRead,
    &m_pInputLayoutExtended
    );
```



<span data-ttu-id="e827a-175">Chacune des définitions d’élément de disposition d’entrée est précédée d’une chaîne, telle que « POSITION » ou « normale », qui est la sémantique que nous avons abordée précédemment dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="e827a-175">Each of the input-layout element definitions is prefixed with a string, like "POSITION" or "NORMAL"—that is the semantic we discussed earlier in this topic.</span></span> <span data-ttu-id="e827a-176">C’est comme un handle qui aide le GPU à identifier cet élément lors du traitement du vertex.</span><span class="sxs-lookup"><span data-stu-id="e827a-176">It's like a handle that helps the GPU identify that element when processing the vertex.</span></span> <span data-ttu-id="e827a-177">Choisissez des noms communs et explicites pour vos éléments vertex.</span><span class="sxs-lookup"><span data-stu-id="e827a-177">Choose common, meaningful names for your vertex elements.</span></span>

<span data-ttu-id="e827a-178">Tout comme avec la mémoire tampon constante, le nuanceur de sommets a une définition de tampon correspondante pour les éléments de vertex entrants.</span><span class="sxs-lookup"><span data-stu-id="e827a-178">Just as with the constant buffer, the vertex shader has a corresponding buffer definition for incoming vertex elements.</span></span> <span data-ttu-id="e827a-179">(C’est pourquoi nous avons fourni une référence à la ressource de nuanceur de vertex lors de la création de la disposition d’entrée-Direct3D valide la disposition des données par vertex avec le struct d’entrée du nuanceur.) Notez comment la sémantique correspond à la définition de la disposition d’entrée et à cette déclaration de tampon HLSL.</span><span class="sxs-lookup"><span data-stu-id="e827a-179">(That's why we provided a reference to the vertex shader resource when creating the input layout - Direct3D validates the per-vertex data layout with the shader's input struct.) Note how the semantics match between the input layout definition and this HLSL buffer declaration.</span></span> <span data-ttu-id="e827a-180">Toutefois, `COLOR` a un « 0 » ajouté.</span><span class="sxs-lookup"><span data-stu-id="e827a-180">However, `COLOR` has a "0" appended to it.</span></span> <span data-ttu-id="e827a-181">Il n’est pas nécessaire d’ajouter le 0 si vous n’avez qu’un seul `COLOR` élément déclaré dans la disposition, mais il est recommandé de l’ajouter au cas où vous choisiriez d’ajouter d’autres éléments de couleur à l’avenir.</span><span class="sxs-lookup"><span data-stu-id="e827a-181">It isn't necessary to add the 0 if you have only one `COLOR` element declared in the layout, but it's a good practice to append it in case you you choose to add more color elements in the future.</span></span>


```C++
struct VS_INPUT
{
    float3 vPos   : POSITION;
    float3 vColor : COLOR0;
};
```



## <a name="pass-data-between-shaders"></a><span data-ttu-id="e827a-182">Transmettre des données entre les nuanceurs</span><span class="sxs-lookup"><span data-stu-id="e827a-182">Pass data between shaders</span></span>

<span data-ttu-id="e827a-183">Les nuanceurs prennent des types d’entrée et retournent des types de sortie à partir de leurs fonctions principales lors de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="e827a-183">Shaders take input types and return output types from their main functions upon execution.</span></span> <span data-ttu-id="e827a-184">Pour le nuanceur de sommets défini dans la section précédente, le type d’entrée était la \_ structure d’entrée de Visual Studio et nous avons défini une disposition d’entrée correspondante et un struct C++.</span><span class="sxs-lookup"><span data-stu-id="e827a-184">For the vertex shader defined in the previous section, the input type was the VS\_INPUT structure, and we defined a matching input layout and C++ struct.</span></span> <span data-ttu-id="e827a-185">Un tableau de ce struct est utilisé pour créer une mémoire tampon de vertex dans la méthode **CreateCube** .</span><span class="sxs-lookup"><span data-stu-id="e827a-185">An array of this struct is used to create a vertex buffer in the **CreateCube** method.</span></span>

<span data-ttu-id="e827a-186">Le nuanceur vertex retourne une \_ structure d’entrée PS, qui doit contenir au minimum la position du vertex final à 4 composants (float4).</span><span class="sxs-lookup"><span data-stu-id="e827a-186">The vertex shader returns a PS\_INPUT structure, which must minimally contain the 4-component (float4) final vertex position.</span></span> <span data-ttu-id="e827a-187">Cette valeur de position doit avoir la sémantique de valeur système, `SV_POSITION` , déclarée pour celle-ci, afin que le GPU dispose des données dont il a besoin pour effectuer l’étape de dessin suivante.</span><span class="sxs-lookup"><span data-stu-id="e827a-187">This position value must have the system value semantic, `SV_POSITION`, declared for it so the GPU has the data it needs to perform the next drawing step.</span></span> <span data-ttu-id="e827a-188">Notez qu’il n’y a pas de correspondance 1:1 entre la sortie du nuanceur de sommets et l’entrée de nuanceur de pixels ; le nuanceur vertex retourne une structure pour chaque vertex auquel il est donné, mais le nuanceur de pixels s’exécute une fois pour chaque pixel.</span><span class="sxs-lookup"><span data-stu-id="e827a-188">Notice that there is not a 1:1 correspondence between vertex shader output and pixel shader input; the vertex shader returns one structure for each vertex it is given, but the pixel shader runs once for each pixel.</span></span> <span data-ttu-id="e827a-189">Cela est dû au fait que les données par vertex passent d’abord par l’étape de pixellisation.</span><span class="sxs-lookup"><span data-stu-id="e827a-189">That's because the per-vertex data first passes through the rasterization stage.</span></span> <span data-ttu-id="e827a-190">Cette étape détermine les pixels qui « couvrent » la géométrie que vous dessinez, calcule les données interpolées par vertex pour chaque pixel, puis appelle le nuanceur de pixels une fois pour chacun de ces pixels.</span><span class="sxs-lookup"><span data-stu-id="e827a-190">This stage decides which pixels "cover" the geometry you're drawing, computes interpolated per-vertex data for each pixel, and then calls the pixel shader once for each of those pixels.</span></span> <span data-ttu-id="e827a-191">L’interpolation est le comportement par défaut lors de la pixellisation des valeurs de sortie et est essentielle en particulier pour le traitement correct des données de vecteur de sortie (vecteurs légers, normales et tangentes par vertex, etc.).</span><span class="sxs-lookup"><span data-stu-id="e827a-191">Interpolation is the default behavior when rasterizing output values, and is essential in particular for the correct processing of output vector data (light vectors, per-vertex normals and tangents, and others).</span></span>


```C++
struct PS_INPUT
{
    float4 Position : SV_POSITION;  // interpolated vertex position (system value)
    float4 Color    : COLOR0;       // interpolated diffuse color
};
```



## <a name="review-the-vertex-shader"></a><span data-ttu-id="e827a-192">Examiner le nuanceur de sommets</span><span class="sxs-lookup"><span data-stu-id="e827a-192">Review the vertex shader</span></span>

<span data-ttu-id="e827a-193">L’exemple de nuanceur vertex est très simple : prenez un vertex (position et couleur), transformez la position des coordonnées de modèle en coordonnées projetées de perspective, puis retournez-la (avec la couleur) au rastériseur.</span><span class="sxs-lookup"><span data-stu-id="e827a-193">The example vertex shader is very simple: take in a vertex (position and color), transform the position from model coordinates into perspective projected coordinates, and return it (along with the color) to the rasterizer.</span></span> <span data-ttu-id="e827a-194">Notez que la valeur de couleur est interpolée avec les données de position, fournissant une valeur différente pour chaque pixel, même si le nuanceur vertex n’a pas effectué de calculs sur la valeur de couleur.</span><span class="sxs-lookup"><span data-stu-id="e827a-194">Notice that the color value is interpolated right along with the position data, providing a different value for each pixel even though the vertex shader didn't perform any calculations on the color value.</span></span>


```C++
VS_OUTPUT main(VS_INPUT input) // main is the default function name
{
    VS_OUTPUT Output;

    float4 pos = float4(input.vPos, 1.0f);

    // Transform the position from object space to homogeneous projection space
    pos = mul(pos, mWorld);
    pos = mul(pos, View);
    pos = mul(pos, Projection);
    Output.Position = pos;

    // Just pass through the color data
    Output.Color = float4(input.vColor, 1.0f);

    return Output;
}
```



<span data-ttu-id="e827a-195">Un nuanceur de sommets plus complexe, comme celui qui configure les sommets d’un objet pour l’ombrage Phong, peut ressembler à ce qui suit.</span><span class="sxs-lookup"><span data-stu-id="e827a-195">A more complex vertex shader, such as one that sets up an object's vertices for Phong shading, might look more like this.</span></span> <span data-ttu-id="e827a-196">Dans ce cas, nous tirant parti du fait que les vecteurs et les normales sont interpolés pour se rapprocher d’une surface lisse.</span><span class="sxs-lookup"><span data-stu-id="e827a-196">In this case, we're taking advantage of the fact that the vectors and normals are interpolated to approximate a smooth-looking surface.</span></span>

``` syntax
// A constant buffer that stores the three basic column-major matrices for composing geometry.
cbuffer ModelViewProjectionConstantBuffer : register(b0)
{
    matrix model;
    matrix view;
    matrix projection;
};

cbuffer LightConstantBuffer : register(b1)
{
    float4 lightPos;
};

struct VertexShaderInput
{
    float3 pos : POSITION;
    float3 normal : NORMAL;
};

// Per-pixel color data passed through the pixel shader.

struct PixelShaderInput
{
    float4 position : SV_POSITION; 
    float3 outVec : POSITION0;
    float3 outNormal : NORMAL0;
    float3 outLightVec : POSITION1;
};

PixelShaderInput main(VertexShaderInput input)
{
    // Inefficient -- doing this only for instruction. Normally, you would
 // premultiply them on the CPU and place them in the cbuffer.
    matrix mvMatrix = mul(model, view);
    matrix mvpMatrix = mul(mvMatrix, projection);

    PixelShaderInput output;

    float4 pos = float4(input.pos, 1.0f);
    float4 normal = float4(input.normal, 1.0f);
    float4 light = float4(lightPos.xyz, 1.0f);

    // 
    float4 eye = float4(0.0f, 0.0f, -2.0f, 1.0f);

    // Transform the vertex position into projected space.
    output.gl_Position = mul(pos, mvpMatrix);
    output.outNormal = mul(normal, mvMatrix).xyz;
    output.outVec = -(eye - mul(pos, mvMatrix)).xyz;
    output.outLightVec = mul(light, mvMatrix).xyz;

    return output;
}
```

## <a name="review-the-pixel-shader"></a><span data-ttu-id="e827a-197">Examiner le nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="e827a-197">Review the pixel shader</span></span>

<span data-ttu-id="e827a-198">Ce nuanceur de pixels dans cet exemple est très probablement la quantité minimale absolue de code que vous pouvez avoir dans un nuanceur de pixels.</span><span class="sxs-lookup"><span data-stu-id="e827a-198">This pixel shader in this example is quite possibly the absolute minimum amount of code you can have in a pixel shader.</span></span> <span data-ttu-id="e827a-199">Elle prend les données de couleur de pixel interpolées générées pendant la pixellisation et les retourne en sortie, où elles sont écrites dans une cible de rendu.</span><span class="sxs-lookup"><span data-stu-id="e827a-199">It takes the interpolated pixel color data generated during rasterization and returns it as output, where it will be written to a render target.</span></span> <span data-ttu-id="e827a-200">Comment l’alésage !</span><span class="sxs-lookup"><span data-stu-id="e827a-200">How boring!</span></span>


```C++
PS_OUTPUT main(PS_INPUT In)
{
    PS_OUTPUT Output;

    Output.RGBColor = In.Color;

    return Output;
}
```



<span data-ttu-id="e827a-201">La partie importante est la `SV_TARGET` sémantique de valeur système sur la valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="e827a-201">The important part is the `SV_TARGET` system-value semantic on the return value.</span></span> <span data-ttu-id="e827a-202">Elle indique que la sortie doit être écrite dans la cible de rendu principale, qui est la mémoire tampon de texture fournie à la chaîne de permutation pour l’affichage.</span><span class="sxs-lookup"><span data-stu-id="e827a-202">It indicates that the output is to be written to the primary render target, which is the texture buffer supplied to the swap chain for display.</span></span> <span data-ttu-id="e827a-203">Cette opération est requise pour les nuanceurs de pixels : sans les données de couleur du nuanceur de pixels, Direct3D n’aurait rien à afficher !</span><span class="sxs-lookup"><span data-stu-id="e827a-203">This is required for pixel shaders - without the color data from the pixel shader, Direct3D wouldn't have anything to display!</span></span>

<span data-ttu-id="e827a-204">Un exemple de nuanceur de pixels plus complexe pour effectuer un ombrage Phong peut ressembler à ceci.</span><span class="sxs-lookup"><span data-stu-id="e827a-204">An example of a more complex pixel shader to perform Phong shading might look like this.</span></span> <span data-ttu-id="e827a-205">Étant donné que les vecteurs et les normales ont été interpolés, nous n’avons pas besoin de les calculer sur une base par pixel.</span><span class="sxs-lookup"><span data-stu-id="e827a-205">Since the vectors and normals were interpolated, we don't have to compute them on a per-pixel basis.</span></span> <span data-ttu-id="e827a-206">Toutefois, nous devons les rénormaliser en raison du fonctionnement de l’interpolation. d’un point de vue conceptuel, nous devons progressivement « faire tourner » le vecteur de la direction du sommet A à la direction du sommet B, en conservant sa longueur (l’interpolation wheras est déplacée sur une ligne droite entre les deux points de terminaison vectoriels).</span><span class="sxs-lookup"><span data-stu-id="e827a-206">However, we do have to re-normalize them because of how interpolation works; conceptually, we need to gradually "spin" the vector from direction at vertex A to direction at vertex B, maintaining its length—wheras interpolation instead cuts across a straight line between the two vector endpoints.</span></span>

``` syntax
cbuffer MaterialConstantBuffer : register(b2)
{
    float4 lightColor;
    float4 Ka;
    float4 Kd;
    float4 Ks;
    float4 shininess;
};

struct PixelShaderInput
{
    float4 position : SV_POSITION;
    float3 outVec : POSITION0;
    float3 normal : NORMAL0;
    float3 light : POSITION1;
};

float4 main(PixelShaderInput input) : SV_TARGET
{
    float3 L = normalize(input.light);
    float3 V = normalize(input.outVec);
    float3 R = normalize(reflect(L, input.normal));

    float4 diffuse = Ka + (lightColor * Kd * max(dot(input.normal, L), 0.0f));
    diffuse = saturate(diffuse);

    float4 specular = Ks * pow(max(dot(R, V), 0.0f), shininess.x - 50.0f);
    specular = saturate(specular);

    float4 finalColor = diffuse + specular;

    return finalColor;
}
```

<span data-ttu-id="e827a-207">Dans un autre exemple, le nuanceur de pixels utilise ses propres mémoires tampons constantes qui contiennent des informations de lumière et de matériau.</span><span class="sxs-lookup"><span data-stu-id="e827a-207">In another example, the pixel shader takes its own constant buffers that contain light and material information.</span></span> <span data-ttu-id="e827a-208">La disposition d’entrée dans le nuanceur vertex est développée de façon à inclure des données normales, et la sortie de ce nuanceur de vertex est supposée inclure les vecteurs transformés pour le vertex, la lumière et le vertex normal dans le système de coordonnées de la vue.</span><span class="sxs-lookup"><span data-stu-id="e827a-208">The input layout in the vertex shader would be expanded to include normal data, and the output from that vertex shader is expected to include transformed vectors for the vertex, the light, and the vertex normal in the view coordinate system.</span></span>

<span data-ttu-id="e827a-209">Si vous avez des tampons de texture et des échantillonneurs avec des registres affectés (**t** et **s**, respectivement), vous pouvez également y accéder dans le nuanceur de pixels.</span><span class="sxs-lookup"><span data-stu-id="e827a-209">If you have texture buffers and samplers with assigned registers (**t** and **s**, respectively), you can access them in the pixel shader also.</span></span>

``` syntax
Texture2D simpleTexture : register(t0);
SamplerState simpleSampler : register(s0);

struct PixelShaderInput
{
    float4 pos : SV_POSITION;
    float3 norm : NORMAL;
    float2 tex : TEXCOORD0;
};

float4 SimplePixelShader(PixelShaderInput input) : SV_TARGET
{
    float3 lightDirection = normalize(float3(1, -1, 0));
    float4 texelColor = simpleTexture.Sample(simpleSampler, input.tex);
    float lightMagnitude = 0.8f * saturate(dot(input.norm, -lightDirection)) + 0.2f;
    return texelColor * lightMagnitude;
}
```

<span data-ttu-id="e827a-210">Les nuanceurs sont des outils très puissants qui peuvent être utilisés pour générer des ressources procédurales telles que des clichés instantanés ou des textures de bruit.</span><span class="sxs-lookup"><span data-stu-id="e827a-210">Shaders are very powerful tools that can be used to generate procedural resources like shadow maps or noise textures.</span></span> <span data-ttu-id="e827a-211">En fait, les techniques avancées requièrent que vous considériez les textures de manière plus abstraite, et non comme des éléments visuels, mais comme des tampons.</span><span class="sxs-lookup"><span data-stu-id="e827a-211">In fact, advanced techniques require that you think of textures more abstractly, not as visual elements but as buffers.</span></span> <span data-ttu-id="e827a-212">Elles contiennent des données telles que des informations de hauteur, ou d’autres données qui peuvent être échantillonnées dans le test de nuanceur de pixels final ou dans ce frame particulier dans le cadre d’un passage à plusieurs étages.</span><span class="sxs-lookup"><span data-stu-id="e827a-212">They hold data like height information, or other data that can be sampled in the final pixel shader pass or in that particular frame as part of a multi-stage effects pass.</span></span> <span data-ttu-id="e827a-213">L’échantillonnage multiple est un outil puissant et l’épine dorsale de nombreux effets visuels modernes.</span><span class="sxs-lookup"><span data-stu-id="e827a-213">Multi-sampling is a powerful tool and the backbone of many modern visual effects.</span></span>

## <a name="next-steps"></a><span data-ttu-id="e827a-214">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="e827a-214">Next steps</span></span>

<span data-ttu-id="e827a-215">Nous espérons que vous êtes familiarisé avec DirectX 11at ce point et que vous êtes prêt à commencer à travailler sur votre projet.</span><span class="sxs-lookup"><span data-stu-id="e827a-215">Hopefully, you're comfortable with DirectX 11at this point and are ready to start working on your project.</span></span> <span data-ttu-id="e827a-216">Voici quelques liens pour vous aider à répondre à d’autres questions que vous pouvez vous poser concernant le développement avec DirectX et C++ :</span><span class="sxs-lookup"><span data-stu-id="e827a-216">Here are some links to help answer other questions you may have about development with DirectX and C++:</span></span>

-   <span data-ttu-id="e827a-217">[Développement de jeux](/previous-versions/windows/apps/hh452744(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="e827a-217">[Developing games](/previous-versions/windows/apps/hh452744(v=win.10))</span></span>
-   <span data-ttu-id="e827a-218">[Utiliser Visual Studio Tools pour la programmation de jeux DirectX](/previous-versions/windows/apps/dn166877(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="e827a-218">[Use Visual Studio tools for DirectX game programming](/previous-versions/windows/apps/dn166877(v=win.10))</span></span>
-   <span data-ttu-id="e827a-219">[Développement de jeux DirectX et exemples de procédures pas à pas](/previous-versions/windows/apps/hh465149(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="e827a-219">[DirectX game development and sample walkthroughs](/previous-versions/windows/apps/hh465149(v=win.10))</span></span>
-   <span data-ttu-id="e827a-220">[Ressources supplémentaires pour la programmation de jeux](/previous-versions/windows/apps/dn194515(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="e827a-220">[Additional game programming resources](/previous-versions/windows/apps/dn194515(v=win.10))</span></span>

## <a name="related-topics"></a><span data-ttu-id="e827a-221">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e827a-221">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e827a-222">Utiliser les ressources de l’appareil DirectX</span><span class="sxs-lookup"><span data-stu-id="e827a-222">Work with DirectX device resources</span></span>](work-with-dxgi.md)
</dt> <dt>

[<span data-ttu-id="e827a-223">Comprendre le pipeline de rendu Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="e827a-223">Understand the Direct3D 11 rendering pipeline</span></span>](understand-the-directx-11-2-graphics-pipeline.md)
</dt> </dl>

 

 