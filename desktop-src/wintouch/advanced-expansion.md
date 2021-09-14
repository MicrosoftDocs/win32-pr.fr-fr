---
title: Expansion avancée
description: Expansion avancée
ms.assetid: 29db15a1-fa56-441a-af99-9e858d143804
keywords:
- Windows Toucher, expansion
- Windows Toucher, développement avancé
- Windows Toucher, manipulations
- manipulations, expansion
- manipulations, expansion avancée
- expansion, avancé
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b81a3a395da053b7d0e8f79a115a2489f3e63190
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127404483"
---
# <a name="advanced-expansion"></a>Expansion avancée

L’illustration suivante montre deux façons d’étendre un objet.

![Illustration montrant une expansion simple autour du point central d’un objet et une expansion avancée autour du point central de la manipulation](images/expansion.png)

Dans l’exemple A, l’exemple d’expansion simple, l’objet est développé autour de son point central. Dans l’exemple B, l’objet est développé autour du point central de la manipulation. Pour ce faire, vous devez traduire l’objet pendant son développement. La valeur de conversion de l’objet est identique à la distance entre le centre de l’objet et le point central du mouvement. Intuitivement, c’est comme si vous développiez l’objet à partir du point central de votre mouvement d’expansion, puis que vous le déplaciez de manière à ce qu’il se trouve toujours au même centre que sa position initiale. Le code suivant illustre une façon dont ce concept peut être appliqué pour permettre l’expansion autour d’un point central.


```C++
    if(m_fFactor != 1.0f)
    {
        // We represent our vectors as an array.
        // x: vx[0], y: vx[1]

        FLOAT v1[2];
        v1[0] = this->get_CenterX() - fOffset[0];
        v1[1] = this->get_CenterY() - fOffset[1];

        FLOAT v2[2];
        v2[0] = v1[0] * m_fFactor;
        v2[1] = v1[1] * m_fFactor;
        
        m_fdX += v2[0] - v1[0];
        m_fdY += v2[1] - v1[1];
    }
   
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Manipulations](getting-started-with-manipulations.md)
</dt> </dl>

 

 




