---
title: Accès aux ressources
description: Il existe plusieurs façons d’accéder aux ressources.
ms.assetid: 83950c4d-5df2-4ed1-9d8f-222a62791c18
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e69ab7bffd22b2271c4d648c3a95ec8d98656973
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104990972"
---
# <a name="accessing-resources"></a><span data-ttu-id="5c1de-103">Accès aux ressources</span><span class="sxs-lookup"><span data-stu-id="5c1de-103">Accessing Resources</span></span>

<span data-ttu-id="5c1de-104">Il existe plusieurs façons d’accéder aux [ressources](overviews-direct3d-11-resources-types.md).</span><span class="sxs-lookup"><span data-stu-id="5c1de-104">There are several ways to access [resources](overviews-direct3d-11-resources-types.md).</span></span> <span data-ttu-id="5c1de-105">Indépendamment, Direct3D garantit de retourner zéro pour toute ressource qui est accessible à partir de limites.</span><span class="sxs-lookup"><span data-stu-id="5c1de-105">Regardless, Direct3D guarantees to return zero for any resource that is accessed out of bounds.</span></span>

-   [<span data-ttu-id="5c1de-106">Accès par décalage d’octet</span><span class="sxs-lookup"><span data-stu-id="5c1de-106">Access By Byte Offset</span></span>](#access-by-byte-offset)
-   [<span data-ttu-id="5c1de-107">Accès par index</span><span class="sxs-lookup"><span data-stu-id="5c1de-107">Access By Index</span></span>](#access-by-index)
-   [<span data-ttu-id="5c1de-108">Accès par méthode mips</span><span class="sxs-lookup"><span data-stu-id="5c1de-108">Access By Mips Method</span></span>](#access-by-mips-method)
-   [<span data-ttu-id="5c1de-109">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="5c1de-109">Related topics</span></span>](#related-topics)

## <a name="access-by-byte-offset"></a><span data-ttu-id="5c1de-110">Accès par décalage d’octet</span><span class="sxs-lookup"><span data-stu-id="5c1de-110">Access By Byte Offset</span></span>

<span data-ttu-id="5c1de-111">Il est possible d’accéder à deux nouveaux types de tampons à l’aide d’un décalage d’octet :</span><span class="sxs-lookup"><span data-stu-id="5c1de-111">Two new buffer types can be accessed using a byte offset:</span></span>

-   <span data-ttu-id="5c1de-112">[**ByteAddressBuffer**](/windows/desktop/direct3dhlsl/sm5-object-byteaddressbuffer) est un tampon en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="5c1de-112">[**ByteAddressBuffer**](/windows/desktop/direct3dhlsl/sm5-object-byteaddressbuffer) is a read-only buffer.</span></span>
-   <span data-ttu-id="5c1de-113">[**RWByteAddressBuffer**](/windows/desktop/direct3dhlsl/sm5-object-rwbyteaddressbuffer) est un tampon de lecture ou d’écriture.</span><span class="sxs-lookup"><span data-stu-id="5c1de-113">[**RWByteAddressBuffer**](/windows/desktop/direct3dhlsl/sm5-object-rwbyteaddressbuffer) is a read or write buffer.</span></span>

## <a name="access-by-index"></a><span data-ttu-id="5c1de-114">Accès par index</span><span class="sxs-lookup"><span data-stu-id="5c1de-114">Access By Index</span></span>

<span data-ttu-id="5c1de-115">Les types de ressources peuvent utiliser un index pour faire référence à un emplacement spécifique dans la ressource.</span><span class="sxs-lookup"><span data-stu-id="5c1de-115">Resource types can use an index to reference a specific location in the resource.</span></span> <span data-ttu-id="5c1de-116">Prenons l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="5c1de-116">Consider this example:</span></span>


```
uint2 pos;
Texture2D<float4> myTexture;
float4 myVar = myTexture[pos];
```



<span data-ttu-id="5c1de-117">Cet exemple affecte les 4 valeurs float qui sont stockées au Texel situé à la position *pos* dans la ressource de texture 2D *myTexture* à la variable *MyVar* .</span><span class="sxs-lookup"><span data-stu-id="5c1de-117">This example assigns the 4 float values that are stored at the texel located at the *pos* position in the *myTexture* 2D texture resource to the *myVar* variable.</span></span>

> [!Note]  
> <span data-ttu-id="5c1de-118">La valeur par défaut pour accéder à une texture de cette façon est le niveau mipmap zéro (le niveau le plus détaillé).</span><span class="sxs-lookup"><span data-stu-id="5c1de-118">The default for accessing a texture in this way is mipmap level zero (the most detailed level).</span></span>

 

> [!Note]  
> <span data-ttu-id="5c1de-119">La ligne « float4 myVar = myTexture \[ pos \] ; » équivaut à « float4 MyVar = MyTexture. Load (uint3 (POS, 0)); ».</span><span class="sxs-lookup"><span data-stu-id="5c1de-119">The "float4 myVar = myTexture\[pos\];" line is equivalent to "float4 myVar = myTexture.Load(uint3(pos,0));".</span></span> <span data-ttu-id="5c1de-120">L’accès par index est une nouvelle amélioration de la syntaxe HLSL.</span><span class="sxs-lookup"><span data-stu-id="5c1de-120">Access by index is a new HLSL syntax enhancement.</span></span>

 

> [!Note]  
> <span data-ttu-id="5c1de-121">Le compilateur dans la version de juin 2010 du kit de développement logiciel (SDK) DirectX et ultérieur vous permet d’indexer tous les types de ressources, à l’exception des [mémoires tampons d’adresse d’octets](direct3d-11-advanced-stages-cs-resources.md).</span><span class="sxs-lookup"><span data-stu-id="5c1de-121">The compiler in the June 2010 version of the DirectX SDK and later lets you index all resource types except for [byte address buffers](direct3d-11-advanced-stages-cs-resources.md).</span></span>

 

> [!Note]  
> <span data-ttu-id="5c1de-122">Le compilateur 2010 de juin et les versions ultérieures vous permettent de déclarer des variables de ressource locales.</span><span class="sxs-lookup"><span data-stu-id="5c1de-122">The June 2010 compiler and later lets you declare local resource variables.</span></span> <span data-ttu-id="5c1de-123">Vous pouvez assigner des ressources globalement définies (comme *myTexture*) à ces variables et les utiliser de la même façon que leurs équivalents globaux.</span><span class="sxs-lookup"><span data-stu-id="5c1de-123">You can assign globally defined resources (like *myTexture*) to these variables and use them the same way as their global counterparts.</span></span>

 

## <a name="access-by-mips-method"></a><span data-ttu-id="5c1de-124">Accès par méthode mips</span><span class="sxs-lookup"><span data-stu-id="5c1de-124">Access By Mips Method</span></span>

<span data-ttu-id="5c1de-125">Les objets texture ont une méthode **mips** (par exemple, [**Texture2D. mips**](/previous-versions/windows/desktop/legacy/ff471560(v=vs.85))), que vous pouvez utiliser pour spécifier le niveau de mipmap.</span><span class="sxs-lookup"><span data-stu-id="5c1de-125">Texture objects have a **mips** method (for example, [**Texture2D.mips**](/previous-versions/windows/desktop/legacy/ff471560(v=vs.85))), which you can use to specify the mipmap level.</span></span> <span data-ttu-id="5c1de-126">Cet exemple lit la couleur stockée sur (7, 16) sur le mipmap niveau 2 dans une texture 2D :</span><span class="sxs-lookup"><span data-stu-id="5c1de-126">This example reads the color stored at (7,16) on mipmap level 2 in a 2D texture:</span></span>


```
uint x = 7;
uint y = 16;
float4 myColor = myTexture.mips[2][uint2(x,y)];
```



<span data-ttu-id="5c1de-127">Il s’agit d’une amélioration du compilateur 2010 de juin et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="5c1de-127">This is an enhancement from the June 2010 compiler and later.</span></span> <span data-ttu-id="5c1de-128">L’expression « myTexture. mips \[ 2 \] \[ uint2 (x, y) \] » est équivalente à « myTexture. Load (uint3 (x, y, 2)) ».</span><span class="sxs-lookup"><span data-stu-id="5c1de-128">The "myTexture.mips\[2\]\[uint2(x,y)\]" expression is equivalent to "myTexture.Load(uint3(x,y,2))".</span></span>

## <a name="related-topics"></a><span data-ttu-id="5c1de-129">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="5c1de-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5c1de-130">Vue d’ensemble du nuanceur de calcul</span><span class="sxs-lookup"><span data-stu-id="5c1de-130">Compute Shader Overview</span></span>](direct3d-11-advanced-stages-compute-shader.md)
</dt> </dl>

 

 