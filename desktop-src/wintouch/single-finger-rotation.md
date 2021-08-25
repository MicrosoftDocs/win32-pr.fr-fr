---
title: Rotation Single-Finger
description: Cette section explique comment faire pivoter un objet à l’aide d’un point pivot.
ms.assetid: b9c19009-8ac0-4168-bf26-393280fc589f
keywords:
- Windows Toucher, rotation
- Windows Toucher, manipulations
- Windows Rotation à un seul doigt
- Windows Toucher, rotation de point pivot
- manipulations, rotation
- rotation, points pivot
- rotation, à un seul doigt
- mouvements, rotation à un seul doigt
- rotation à un seul doigt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36fe7e92f6d68515e1d13b39c32ee4af5b6b03e675479242210fe302b84e6395
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120110647"
---
# <a name="single-finger-rotation"></a>Rotation Single-Finger

Cette section explique comment faire pivoter un objet à l’aide d’un point pivot.

L’image suivante illustre la rotation à un seul doigt.

![Illustration montrant deux types de rotation à un seul doigt : autour du centre ou autour du bord](images/sfrotation.png)

Dans l’exemple A, l’objet pivote autour du point central de l’objet à l’aide du mouvement de rotation. Dans l’exemple B, l’objet est pivoté en déplaçant un seul doigt autour du bord de l’objet. Le processeur de manipulation active cette rotation à l’aide des valeurs de point pivot et de rayon pivot. L’image suivante illustre les composants de la rotation à un seul doigt.

![Illustration montrant les composants de rotation à un seul doigt : pivotpointx, pivotpointy et pivotradius](images/sfrotation-components.png)

Une fois que vous avez défini les valeurs [**PivotPointX**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotpointx), [**PivotPointY**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotpointy)et [**PivotRadius**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotradius) , les messages de traduction suivants incorporent la rotation. Plus le rayon pivot est grand, plus la modification de x et y doit être importante. Le code suivant montre comment ces valeurs peuvent être définies dans le processeur de manipulation.


```C++
HRESULT STDMETHODCALLTYPE CManipulationEventSink::ManipulationDelta( 
    /* [in] */ FLOAT x,
    /* [in] */ FLOAT y)
{
    m_cStartedEventCount ++;

    // Set the pivot point to the object's center and then set the radius 
    // to the distance from the center to the edge of the object.
    m_pManip->put_PivotPointX(m_objectRef->xPos);
    m_pManip->put_PivotPointY(m_objectRef->yPos);
    
    float fPivotRadius = (FLOAT)(sqrt(pow(m_dObj->get_Width()/2, 2) + pow(m_dObj->get_Height()/2, 2)))*0.4f;
    
    m_pManip->put_PivotRadius(fPivotRadius);
  

    return S_OK;
}    
     
```



Dans l’exemple précédent, la distance au bord de l’objet (mise à l’échelle à 40 pour cent) est utilisée comme rayon pivot. Étant donné que la taille de l’objet est prise en compte, ce calcul est valide pour chaque Delta de l’objet. À mesure que l’objet est mis à l’échelle, le rayon pivot augmente. Cette valeur et les valeurs Center x et y de l’objet sont passées au processeur de manipulation pour faire pivoter l’objet autour du point pivot.

> [!Note]  
> La valeur [**PivotRadius**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotradius) ne doit jamais être comprise entre 0,0 et 1,0.

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Manipulations](getting-started-with-manipulations.md)
</dt> <dt>

[**PivotRadius**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotradius)
</dt> <dt>

[**PivotPointX**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotpointx)
</dt> <dt>

[**PivotPointY**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotpointy)
</dt> </dl>

 

 




