---
title: Effet d’histogramme
description: Utilisez l’effet histogramme pour générer un histogramme pour l’image bitmap d’entrée en fonction du nombre spécifié d’emplacements.
ms.assetid: 458E2334-F383-41DE-9479-601AC3007BF3
keywords:
- effet d’histogramme
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b654ffb2b830914b00a59490ceb429b5de9c51cb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127113177"
---
# <a name="histogram-effect"></a>Effet d’histogramme

Utilisez l’effet histogramme pour générer un histogramme pour l’image bitmap d’entrée en fonction du nombre spécifié d’emplacements.

Le CLSID de cet effet est CLSID \_ D2D1Histogram.

-   [Exemple](#example)
-   [Propriétés d’effet](#effect-properties)
-   [Sélecteurs de canaux](#channel-selectors)
-   [Sortie des données](#data-output)
-   [Remarques](#remarks)
-   [Configuration requise](#requirements)
-   [Rubriques connexes](#related-topics)

## <a name="example"></a>Exemple



| Avant                                                     |
|------------------------------------------------------------|
| ![image avant l’effet.](images/default-before.jpg) |
| Graph des données de sortie de l’histogramme                         |
| ![image après la transformation.](images/33-histogram.png) |



 


```C++
ComPtr<ID2D1Effect> histogramEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Histogram, &histogramEffect);

histogramEffect->SetInputEffect(0, m_2DAffineTransformEffectRight.Get());
histogramEffect->SetValue(D2D1_HISTOGRAM_PROP_CHANNEL_SELECT, D2D1_CHANNEL_SELECTOR_G);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(histogramEffect.Get());
m_d2dContext->EndDraw();

// The histogram data is only available once the effect has been 'drawn'.
int histogramBinCount;

HRESULT hr = histogramEffect->GetValue(D2D1_HISTOGRAM_PROP_NUM_BINS, &histogramBinCount);

float *histogramData = new float[histogramBinCount];
hr = histogramEffect->GetValue(D2D1_HISTOGRAM_PROP_HISTOGRAM_OUTPUT, 
                               reinterpret_cast<BYTE*>(histogramData), 
                               histogramBinCount * sizeof(float));
```



## <a name="effect-properties"></a>Propriétés d’effet

Voici l’équation permettant de générer la sortie.

![équation permettant de générer la sortie de l’effet de l’histogramme.](images/histogram-formula.png)

la valeur de *i* est comprise entre 0 et le nombre d’emplacements. L’effet génère un histogramme pour les valeurs de pixel comprises entre 0 et 1. Les valeurs en dehors de cette plage sont ancrées à la plage. La plage d’un compartiment particulier dépend du nombre de compartiments. Cet effet fonctionne sur des pixels de bitmap droits. Les canaux de couleur de la bitmap d’entrée sont divisés par le canal alpha pour calculer cet effet.



| Nom complet et énumération d’index                                             | Type et valeur par défaut                                                   | Description                                                                                                                                                                                   |
|--------------------------------------------------------------------------------|--------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| NumBins<br/> D2D1 de l' \_ histogramme \_ prop \_ nombre d' \_ emplacements<br/>                 | UINT32<br/> 256<br/>                                         | Spécifie le nombre d’emplacements utilisés pour l’histogramme. La plage de valeurs d’intensité qui se trouvent dans un compartiment particulier dépend du nombre de compartiments spécifiés.                              |
| ChannelSelect<br/> \_Sélection du \_ \_ canal \_ d2d1 de l’histogramme<br/>     | \_Sélecteur de canal d2d1 \_<br/> \_Sélecteur de canal d2d1 \_ \_ R<br/> | Spécifie le canal utilisé pour générer l’histogramme. Cet effet a une sortie de données unique correspondant au canal spécifié. Pour plus d’informations, consultez [sélecteurs de canaux](#channel-selectors) . |
| HistogramOutput<br/> Sortie de l’histogramme D2D1 de l' \_ histogramme \_ \_ \_<br/> | DISSOCIÉ\[\]<br/> Propriété de sortie uniquement.<br/>                    | Tableau de sortie.                                                                                                                                                                             |



 

## <a name="channel-selectors"></a>Sélecteurs de canaux



| Énumération                | Description                                                           |
|----------------------------|-----------------------------------------------------------------------|
| \_Sélecteur de canal d2d1 \_ \_ R | L’effet génère la sortie de l’histogramme en fonction du canal rouge.   |
| \_Sélecteur de canal d2d1 \_ \_ G | L’effet génère la sortie de l’histogramme en fonction du canal vert. |
| \_Sélecteur de canal d2d1 \_ \_ B | L’effet génère la sortie de l’histogramme en fonction du canal bleu.  |
| \_ \_ Sélecteur de canal d2d1 \_ A | L’effet génère la sortie de l’histogramme en fonction du canal alpha. |



 

## <a name="data-output"></a>Sortie des données

Cet effet génère une valeur FLOAT \[ \] , avec le nombre d’éléments correspondant au nombre d’emplacements spécifiés. Chaque élément de la \[ \] valeur float est un float. La valeur de l’élément correspond au nombre d’éléments dans cet emplacement.

## <a name="remarks"></a>Notes

> [!Note]  
> La méthode [**CreateEffect**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createeffect) échoue si l’appareil ne prend pas en charge DirectCompute et retourne HRESULT = D2DERR \_ fonctionnalités d’appareil insuffisantes \_ \_ . Toutes les cartes DirectX11 et DirectX10 qui prennent en charge DirectCompute peuvent utiliser l’effet.

 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge | mise à jour Windows 8 et de plateforme pour les applications de bureau Windows 7 Windows les applications du windows \[ \| Store\] |
| Serveur minimal pris en charge | mise à jour Windows 8 et de plateforme pour les applications de bureau Windows 7 Windows les applications du windows \[ \| Store\] |
| En-tête                   | d2d1effects. h                                                                      |
| Bibliothèque                  | d2d1. lib, dxguid. lib                                                               |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

