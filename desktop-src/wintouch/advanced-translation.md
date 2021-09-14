---
title: Traduction avancée
description: Traduction avancée
ms.assetid: 48a1bdd5-8b7b-4460-9b7b-1ab8969a28f8
keywords:
- Windows Toucher, traduction
- Windows Saisie tactile, traduction avancée
- Windows Toucher, manipulations
- manipulations, traduction
- manipulations, traduction avancée
- translation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc383c71e1f1417d30b64db18aa627039602b942
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127219681"
---
# <a name="advanced-translation"></a>Traduction avancée

L’illustration suivante montre deux interprétations de la traduction.

![Illustration montrant tout d’abord une traduction simple, dans laquelle un objet est déplacé sans rotation, puis affiche une traduction avancée, qui implique le déplacement avec la rotation](images/translation.png)

Dans l’exemple A, l’exemple de traduction simple, l’objet est déplacé sans rotation. Dans l’exemple B, l’objet est pivoté pendant la traduction, en fonction de l’emplacement du point de contact de l’objet. Si vous activez la rotation à un seul doigt comme décrit dans [rotation à un seul doigt](single-finger-rotation.md), vous pouvez activer la traduction complexe. Le diagramme suivant montre les différents composants de la rotation à un seul doigt lorsque vous effectuez une traduction.

![Illustration montrant les composants de rotation à un seul doigt : pivotpointx, pivotpointy et pivotradius](images/translation-complex-components.png)

Lorsque l’objet est déplacé, le rayon est recalculé et le point pivot est déplacé.

Le code suivant illustre une méthode permettant d’effectuer cette opération dans une implémentation de [**ManipulationDelta**](/windows/win32/api/manipulations/nf-manipulations-_imanipulationevents-manipulationdelta) qui permet une traduction complexe.


```C++
    //Apply transformation based on rotationDelta (in radians)
    FLOAT rads = 180.0f / 3.14159f;
    m_dObj->Rotate(rotationDelta*rads, x, y);

    // Apply translation based on scaleDelta
    m_dObj->Scale(scaleDelta);

    // Apply translation based on translationDelta
    m_dObj->Translate(translationDeltaX, translationDeltaY);

    // Set values for one finger rotations
    FLOAT fPivotRadius = (FLOAT)(m_dObj->get_Width() + m_dObj->get_Height())/8.0f;
    FLOAT fPivotPtX = m_dObj->get_CenterX();
    FLOAT fPivotPtY = m_dObj->get_CenterY();
        
    m_manip->put_PivotPointX(fPivotPtX);
    m_manip->put_PivotPointY(fPivotPtY);
    m_manip->put_PivotRadius(fPivotRadius);       
   
```



> [!Note]  
> Les transformations d’objet se produisent avant le calcul des points pivot et du rayon. De cette façon, l’objet se déplace correctement si l’utilisateur effectue une expansion sur l’objet pendant son déplacement.

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Manipulations](getting-started-with-manipulations.md)
</dt> </dl>

 

 




