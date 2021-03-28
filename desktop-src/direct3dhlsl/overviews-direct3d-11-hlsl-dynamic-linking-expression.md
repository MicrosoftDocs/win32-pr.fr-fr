---
title: Restrictions d’utilisation de l’interface
description: Le matériel GPU actuel ne prend pas en charge les informations d’emplacement variables au moment de l’exécution du nuanceur. En conséquence, les références d’interface ne peuvent pas être modifiées au sein d’une expression conditionnelle telle qu’une instruction if ou switch.
ms.assetid: 95a505d8-3ec4-49b7-bb2b-f29a655e4225
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 8825d192dcb874ce8b148c4ade5c579a55857311
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309722"
---
# <a name="interface-usage-restrictions"></a><span data-ttu-id="b26f7-104">Restrictions d’utilisation de l’interface</span><span class="sxs-lookup"><span data-stu-id="b26f7-104">Interface Usage Restrictions</span></span>

<span data-ttu-id="b26f7-105">Le matériel GPU actuel ne prend pas en charge les informations d’emplacement variables au moment de l’exécution du nuanceur.</span><span class="sxs-lookup"><span data-stu-id="b26f7-105">Current GPU hardware does not support varying slot information at shader runtime.</span></span> <span data-ttu-id="b26f7-106">En conséquence, les références d’interface ne peuvent pas être modifiées au sein d’une expression conditionnelle telle qu’une instruction if ou switch.</span><span class="sxs-lookup"><span data-stu-id="b26f7-106">As a consequence interface references cannot be modified within a conditional expression such as an if or switch statement.</span></span>

<span data-ttu-id="b26f7-107">Le code de nuanceur suivant illustre le moment où cette restriction se produit et une autre approche possible.</span><span class="sxs-lookup"><span data-stu-id="b26f7-107">The following shader code illustrates when this restriction will occur and a possible alternate approach.</span></span>

<span data-ttu-id="b26f7-108">Compte tenu des déclarations d’interface suivantes :</span><span class="sxs-lookup"><span data-stu-id="b26f7-108">Given the following interface declarations:</span></span>


```
interface A
{
    float GetRatio();
    bool IsGood();
};

interface B
{
    float GetValue();
};

A arrayA[6];
B arrayB[6];
```



<span data-ttu-id="b26f7-109">À partir des déclarations de classe suivantes :</span><span class="sxs-lookup"><span data-stu-id="b26f7-109">Given the following class declarations:</span></span>


```
class C1 : A
{
    float var;
    float GetRatio() { return 1.0f; }
    bool IsGood() { return true; }
};

class C2 : C1, B
{
    float GetRatio() { return C1::GetRatio() * 0.33f; }
    float GetValue() { return 5.0f; }
    bool IsGood() { return false; }
};

class C3 : B
{
    float var;
    float GetValue() { return -1.0f; }
};

class C4 : A, B
{
    float var;
    float GetRatio() { return var; }
    float GetValue() { return var * 2.0f; }
    bool IsGood() { return var > 0.0f; }
};
```



<span data-ttu-id="b26f7-110">Une référence d’interface ne peut pas être modifiée au sein de l’expression conditionnelle (instruction If) :</span><span class="sxs-lookup"><span data-stu-id="b26f7-110">An interface reference cannot be modified within the conditional expression (an if statement):</span></span>


```
float main() : wicked
{
    float rev;
    {
        A a = arrayA[0];
        for( uint i = 0; i < 6; ++i )
        {
            if( arrayA[i].IsGood() )
            {
                // This forces the loop to be unrolled, 
                // since the slot information is changing.
                a = arrayA[i]; 
                rev -= arrayA[i-2].GetRatio();
            }
            else
            {
                // This causes an error since the compiler is
                // unable to determine the interface slot
                rev += arrayB[i].GetValue() + a.GetRatio(); 
            }
        }
    }
    return rev;
}
```



<span data-ttu-id="b26f7-111">Étant donné la même interface et les mêmes déclarations de classe, vous pouvez utiliser un index pour fournir les mêmes fonctionnalités et éviter le déroulement forcé de la boucle.</span><span class="sxs-lookup"><span data-stu-id="b26f7-111">Given the same interface and class declarations, you could use an index to provide the same functionality and avoid the forced loop unroll.</span></span>


```
float main() : wicked
{
    float rev;
    {
        uint index = 0;
        for( uint i = 0; i < 6; ++i )
        {
            if( arrayA[i].IsGood() )
            {
                index = i;
                rev -= arrayA[i-2].GetRatio();
            }
            else
            {
                rev += arrayB[i].GetValue() + arrayA[index].GetRatio();
            }
        }
    }
    return rev;
}
```



## <a name="related-topics"></a><span data-ttu-id="b26f7-112">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b26f7-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b26f7-113">Liaison dynamique</span><span class="sxs-lookup"><span data-stu-id="b26f7-113">Dynamic Linking</span></span>](overviews-direct3d-11-hlsl-dynamic-linking.md)
</dt> </dl>

 

 




