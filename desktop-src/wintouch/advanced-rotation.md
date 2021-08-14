---
title: Rotation avancée
description: Cette section explique comment faire pivoter un objet en fonction de l’endroit où l’utilisateur effectue la manipulation de rotation.
ms.assetid: 56b339b1-a062-4c0e-91c8-aec08a17bc65
keywords:
- Windows Toucher, rotation
- Windows Tactile, rotation avancée
- Windows Toucher, manipulations
- manipulations, rotation
- manipulations, rotation avancée
- rotation, avancé
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a6dda17ae8076061f7b5b7b935afb2b7f8e5fb10cb270280f7edbb8c23aa896
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118199515"
---
# <a name="advanced-rotation"></a>Rotation avancée

Cette section explique comment faire pivoter un objet en fonction de l’endroit où l’utilisateur effectue la manipulation de rotation.

L’illustration suivante montre deux façons différentes de faire pivoter un objet.

![Illustration montrant deux types de rotation à un seul doigt : autour du centre ou autour du bord, avec la périphérie qui implique à la fois la rotation et la translation](images/rotation.png)

Dans l’exemple A, l’objet est manipulé autour du point central de l’objet. Dans l’exemple B, l’objet pivote autour du point central de la manipulation. Pour prendre en charge la manipulation autour d’un point autre que le point central de l’objet, vous devez effectuer une manipulation composée qui effectue à la fois la rotation et la translation. Le code suivant montre comment cette manipulation est effectuée et calculée.


```C++
RotateVector(FLOAT *vector, FLOAT *tVector, FLOAT fAngle) {
    FLOAT fAngleRads = fAngle / 180.0f * 3.14159f;
    FLOAT fSin = sin(fAngleRads);
    FLOAT fCos = cos(fAngleRads);

    FLOAT fNewX = (vector[0]*fCos) - (vector[1]*fSin);
    FLOAT fNewY = (vector[0]*fSin) + (vector[1]*fCos);

    tVector[0] = fNewX;
    tVector[1] = fNewY;
}
     
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Manipulations avancées](advanced-manipulations.md)
</dt> <dt>

[Manipulations](getting-started-with-manipulations.md)
</dt> </dl>

 

 




