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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127228173"
---
# <a name="packing-rules-for-constant-variables"></a>Règles de compression pour les variables constantes

Les règles de compression déterminent la façon dont les données peuvent être réorganisées lors de leur stockage. Le langage HLSL implémente des règles de compression pour les données de sortie VS, les données d’entrée et de sortie GS, ainsi que les données d’entrée et de sortie PS. (Les données ne sont pas compressées pour les entrées VS, car l’étape IA ne peut pas décompresser les données.)

les règles de compression HLSL sont similaires à l’exécution d’un **\# pragma pack 4** avec Visual Studio, qui compresse les données en limites de 4 octets. En outre, le langage HLSL compresse les données afin qu’elles ne traversent pas une limite de 16 octets. Les variables sont compressées dans un vecteur à quatre composants donné jusqu’à ce que la variable chevauche une limite de 4 vecteurs. les variables suivantes sont retournés au vecteur suivant de quatre composants.

Chaque structure force la variable suivante à démarrer sur le vecteur à quatre composants suivant. Cela génère parfois un remplissage pour les tableaux de structures. La taille résultante d’une structure est toujours divisible par **sizeof**(*vecteur à quatre composants*).

Par défaut, les tableaux ne sont pas compressés en langage HLSL. Pour éviter de forcer le nuanceur à prendre la surcharge d’ALU pour les calculs de décalage, chaque élément d’un tableau est stocké dans un vecteur à quatre composants. Notez que vous pouvez effectuer l’empaquetage pour les tableaux (et les calculs d’adressage) à l’aide de la conversion.

Voici des exemples de structures et leurs tailles compressées correspondantes (données : un **float1** occupe 4 octets) :


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



## <a name="more-aggressive-packing"></a>Compression plus agressive

Vous pouvez empaqueter un tableau de manière plus agressive. Par exemple, à partir d’un tableau de variables float :


```
float4 array[16];
```



Vous pouvez choisir de l’empaqueter comme ceci, sans espace dans le tableau :


```
static float2 aggressivePackArray[32] = (float2[32])array;  
```



L’empaquetage plus étroit est un compromis par rapport au besoin d’instructions de nuanceur supplémentaires pour le calcul des adresses.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Nuanceur modèle 4](dx-graphics-hlsl-sm4.md)
</dt> </dl>

 

 




