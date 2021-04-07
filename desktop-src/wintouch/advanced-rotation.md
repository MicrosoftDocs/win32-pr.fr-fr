---
title: Rotation avancée
description: Cette section explique comment faire pivoter un objet en fonction de l’endroit où l’utilisateur effectue la manipulation de rotation.
ms.assetid: 56b339b1-a062-4c0e-91c8-aec08a17bc65
keywords:
- Tactile Windows, rotation
- Tactile Windows, rotation avancée
- Tactile Windows, manipulations
- manipulations, rotation
- manipulations, rotation avancée
- rotation, avancé
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc3a84679f4189d28941262cda2585887b0932c5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103939681"
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

 

 




