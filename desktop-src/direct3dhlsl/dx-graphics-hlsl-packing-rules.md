---
title: Règles de compression pour les variables constantes
description: Les règles de compression déterminent la façon dont les données peuvent être réorganisées lors de leur stockage.
ms.assetid: 5c399342-06e1-47d2-8ecf-e093ed04be50
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d85566083dc9ead93a1a9e73fb06051b62178114
ms.sourcegitcommit: 004d7881dc9ff92ea394cd2331774e13b1e7f13c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/12/2020
ms.locfileid: "103724365"
---
# <a name="packing-rules-for-constant-variables"></a><span data-ttu-id="3a958-103">Règles de compression pour les variables constantes</span><span class="sxs-lookup"><span data-stu-id="3a958-103">Packing Rules for Constant Variables</span></span>

<span data-ttu-id="3a958-104">Les règles de compression déterminent la façon dont les données peuvent être réorganisées lors de leur stockage.</span><span class="sxs-lookup"><span data-stu-id="3a958-104">Packing rules dictate how tightly data can be arranged when it is stored.</span></span> <span data-ttu-id="3a958-105">Le langage HLSL implémente des règles de compression pour les données de sortie VS, les données d’entrée et de sortie GS, ainsi que les données d’entrée et de sortie PS.</span><span class="sxs-lookup"><span data-stu-id="3a958-105">HLSL implements packing rules for VS output data, GS input and output data, and PS input and output data.</span></span> <span data-ttu-id="3a958-106">(Les données ne sont pas compressées pour les entrées VS, car l’étape IA ne peut pas décompresser les données.)</span><span class="sxs-lookup"><span data-stu-id="3a958-106">(Data is not packed for VS inputs because the IA stage cannot unpack data.)</span></span>

<span data-ttu-id="3a958-107">Les règles de compression HLSL sont similaires à l’exécution d’un **\# pragma Pack 4** avec Visual Studio, qui compresse les données dans des limites de 4 octets.</span><span class="sxs-lookup"><span data-stu-id="3a958-107">HLSL packing rules are similar to performing a **\#pragma pack 4** with Visual Studio, which packs data into 4-byte boundaries.</span></span> <span data-ttu-id="3a958-108">En outre, le langage HLSL compresse les données afin qu’elles ne traversent pas une limite de 16 octets.</span><span class="sxs-lookup"><span data-stu-id="3a958-108">Additionally, HLSL packs data so that it does not cross a 16-byte boundary.</span></span> <span data-ttu-id="3a958-109">Les variables sont compressées dans un vecteur à quatre composants donné jusqu’à ce que la variable chevauche une limite de 4 vecteurs. les variables suivantes sont retournés au vecteur suivant de quatre composants.</span><span class="sxs-lookup"><span data-stu-id="3a958-109">Variables are packed into a given four-component vector until the variable will straddle a 4-vector boundary; the next variables will be bounced to the next four-component vector.</span></span>

<span data-ttu-id="3a958-110">Chaque structure force la variable suivante à démarrer sur le vecteur à quatre composants suivant.</span><span class="sxs-lookup"><span data-stu-id="3a958-110">Each structure forces the next variable to start on the next four-component vector.</span></span> <span data-ttu-id="3a958-111">Cela génère parfois un remplissage pour les tableaux de structures.</span><span class="sxs-lookup"><span data-stu-id="3a958-111">This sometimes generates padding for arrays of structures.</span></span> <span data-ttu-id="3a958-112">La taille résultante d’une structure est toujours divisible par **sizeof**(*vecteur à quatre composants*).</span><span class="sxs-lookup"><span data-stu-id="3a958-112">The resulting size of any structure will always be evenly divisible by **sizeof**(*four-component vector*).</span></span>

<span data-ttu-id="3a958-113">Par défaut, les tableaux ne sont pas compressés en langage HLSL.</span><span class="sxs-lookup"><span data-stu-id="3a958-113">Arrays are not packed in HLSL by default.</span></span> <span data-ttu-id="3a958-114">Pour éviter de forcer le nuanceur à prendre la surcharge d’ALU pour les calculs de décalage, chaque élément d’un tableau est stocké dans un vecteur à quatre composants.</span><span class="sxs-lookup"><span data-stu-id="3a958-114">To avoid forcing the shader to take on ALU overhead for offset computations, every element in an array is stored in a four-component vector.</span></span> <span data-ttu-id="3a958-115">Notez que vous pouvez effectuer l’empaquetage pour les tableaux (et les calculs d’adressage) à l’aide de la conversion.</span><span class="sxs-lookup"><span data-stu-id="3a958-115">Note that you can achieve packing for arrays (and incur the addressing calculations) by using casting.</span></span>

<span data-ttu-id="3a958-116">Voici des exemples de structures et leurs tailles compressées correspondantes (données : un **float1** occupe 4 octets) :</span><span class="sxs-lookup"><span data-stu-id="3a958-116">Following are examples of structures and their corresponding packed sizes (given: a **float1** occupies 4 bytes):</span></span>


```
//  2 x 16byte elements
cbuffer IE
{
    float4 Val1;
    float2 Val2;  // starts a new vector
    float2 Val3;
};

//  3 x 16byte elements
cbuffer IE
{
    float2 Val1;
    float4 Val2;  // starts a new vector
    float2 Val3;  // starts a new vector
};

//  1 x 16byte elements
cbuffer IE
{
    float1 Val1;
    float1 Val2;
    float2 Val3;
};

//  1 x 16byte elements
cbuffer IE
{
    float1 Val1;
    float2 Val2;
    float1 Val3;
};

//  2 x 16byte elements
cbuffer IE
{
    float1 Val1;
    float1 Val1;
    float1 Val1;
    float2 Val2;    // starts a new vector
};


//  1 x 16byte elements
cbuffer IE
{
    float3 Val1;
    float1 Val2;
};

//  1 x 16byte elements
cbuffer IE
{
    float1 Val1;
    float3 Val2;
};

//  2 x 16byte elements
cbuffer IE
{
    float1 Val1;
    float1 Val1;
    float3 Val2;        // starts a new vector
};


// 3 x 16byte elements
cbuffer IE
{
    float1 Val1;

    struct     {
        float4 SVal1;    // starts a new vector
        float1 SVal2;    // starts a new vector
    } Val2;
};

// 3 x 16byte elements
cbuffer IE
{
    float1 Val1;  
    struct     {
        float1 SVal1;     // starts a new vector
        float4 SVal2;     // starts a new vector
    } Val2;
};

// 3 x 16byte elements
cbuffer IE
{
    struct     {
        float4 SVal1;
        float1 SVal2;    // starts a new vector
    } Val1;

    float1 Val2; 
};
```



## <a name="more-aggressive-packing"></a><span data-ttu-id="3a958-117">Compression plus agressive</span><span class="sxs-lookup"><span data-stu-id="3a958-117">More Aggressive Packing</span></span>

<span data-ttu-id="3a958-118">Vous pouvez empaqueter un tableau de manière plus agressive.</span><span class="sxs-lookup"><span data-stu-id="3a958-118">You could pack an array more aggressively.</span></span> <span data-ttu-id="3a958-119">Par exemple, à partir d’un tableau de variables float :</span><span class="sxs-lookup"><span data-stu-id="3a958-119">For instance, given an array of float variables:</span></span>


```
float4 array[16];
```



<span data-ttu-id="3a958-120">Vous pouvez choisir de l’empaqueter comme ceci, sans espace dans le tableau :</span><span class="sxs-lookup"><span data-stu-id="3a958-120">You could choose to pack it like this, without any spaces in the array:</span></span>


```
static float2 aggressivePackArray[32] = (float2[32])array;  
```



<span data-ttu-id="3a958-121">L’empaquetage plus étroit est un compromis par rapport au besoin d’instructions de nuanceur supplémentaires pour le calcul des adresses.</span><span class="sxs-lookup"><span data-stu-id="3a958-121">The tighter packing is a trade off versus the need for additional shader instructions for address computation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3a958-122">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="3a958-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3a958-123">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="3a958-123">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)
</dt> </dl>

 

 




