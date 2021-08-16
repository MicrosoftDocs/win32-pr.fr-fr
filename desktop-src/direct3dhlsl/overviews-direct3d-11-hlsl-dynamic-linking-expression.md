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
ms.openlocfilehash: eae44bbdb93ab2b3ffa0d09385c56b463192cc68c17e0454f9edd3326f722d29
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119672559"
---
# <a name="interface-usage-restrictions"></a>Restrictions d’utilisation de l’interface

Le matériel GPU actuel ne prend pas en charge les informations d’emplacement variables au moment de l’exécution du nuanceur. En conséquence, les références d’interface ne peuvent pas être modifiées au sein d’une expression conditionnelle telle qu’une instruction if ou switch.

Le code de nuanceur suivant illustre le moment où cette restriction se produit et une autre approche possible.

Compte tenu des déclarations d’interface suivantes :


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



À partir des déclarations de classe suivantes :


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



Une référence d’interface ne peut pas être modifiée au sein de l’expression conditionnelle (instruction If) :


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



Étant donné la même interface et les mêmes déclarations de classe, vous pouvez utiliser un index pour fournir les mêmes fonctionnalités et éviter le déroulement forcé de la boucle.


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



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Liaison dynamique](overviews-direct3d-11-hlsl-dynamic-linking.md)
</dt> </dl>

 

 




