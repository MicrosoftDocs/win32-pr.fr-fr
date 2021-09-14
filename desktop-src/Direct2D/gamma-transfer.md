---
title: Effet de transfert gamma
description: Utilisez l’effet transfert gamma pour mapper les intensités de couleur d’une image à l’aide d’une fonction gamma créée à l’aide d’une amplitude, d’un exposant et d’un décalage que vous fournissez pour chaque canal.
ms.assetid: 0E0455CA-CFCA-4C4F-9DFA-1DB6A5205F6A
keywords:
- effet de transfert gamma
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b806ac8f59efe1b3fad3b61edc7f88f72b143f9c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127113217"
---
# <a name="gamma-transfer-effect"></a>Effet de transfert gamma

Utilisez l’effet transfert gamma pour mapper les intensités de couleur d’une image à l’aide d’une fonction gamma créée à l’aide d’une amplitude, d’un exposant et d’un décalage que vous fournissez pour chaque canal.

Le CLSID de cet effet est CLSID \_ D2D1GammaTransfer. Pour utiliser cet effet, ajoutez dxguid. lib aux dépendances de l’éditeur de liens.

-   [Exemple d’image](#example-image)
-   [Propriétés d’effet](#effect-properties)
-   [Bitmap de sortie](#output-bitmap)
-   [Configuration requise](#requirements)
-   [Rubriques connexes](#related-topics)

## <a name="example-image"></a>Exemple d’image



| Avant                                                         |
|----------------------------------------------------------------|
| ![image avant l’effet.](images/default-before.jpg)     |
| After                                                          |
| ![image après la transformation.](images/14-gammatransfer.png) |



 


```C++
ComPtr<ID2D1Effect> gammaTransferEffect;
m_d2dContext->CreateEffect(CLSID_D2D1GammaTransfer, &gammaTransferEffect);

gammaTransferEffect->SetInput(0, bitmap);

gammaTransferEffect->SetValue(D2D1_GAMMATRANSFER_PROP_RED_EXPONENT, 0.25f);
gammaTransferEffect->SetValue(D2D1_GAMMATRANSFER_PROP_GREEN_EXPONENT, 0.25f);
gammaTransferEffect->SetValue(D2D1_GAMMATRANSFER_PROP_BLUE_EXPONENT, 0.25f);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(gammaTransferEffect.Get());
m_d2dContext->EndDraw();
```



Cet effet applique une fonction de transfert gamma basée sur l’équation ici.

L’intensité en pixels d’entrée est représentée par C et l’intensité en pixels de sortie en tant que C. C' = \* <sup>exposant</sup> c amplitude + décalage

Cet effet fonctionne sur les images alpha directes et prémultipliées. L’effet génère des bitmaps alpha prémultipliés.

## <a name="effect-properties"></a>Propriétés d’effet

> [!Note]  
> Pour tous les canaux des propriétés de transfert gamma :
>
> -   La valeur d’amplitude n’est pas limitée et est sans unité.
> -   La valeur d’exposant n’est pas limitée et est sans unité.
> -   La valeur de décalage n’est pas limitée et est sans unité.

 



| Nom complet et énumération d’index                                               | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| RedAmplitude<br/> \_ \_ \_ Amplitude rouge d2d1 GAMMATRANSFER \_ prop<br/>     | Amplitude de la fonction de transfert gamma pour le canal rouge. Le type est FLOAT.<br/> La valeur par défaut est 1,0 f.<br/>                                                                                                                                                                                                                                                                                                                                                                                             |
| RedExponent<br/> \_ \_ \_ Exposant rouge d2d1 GAMMATRANSFER \_ prop<br/>       | Exposant de la fonction de transfert gamma pour le canal rouge. Le type est FLOAT.<br/> La valeur par défaut est 1,0 f.<br/>                                                                                                                                                                                                                                                                                                                                                                                              |
| RedOffset<br/> \_ \_ \_ Décalage rouge d2d1 GAMMATRANSFER \_ prop<br/>           | Décalage de la fonction de transfert gamma pour le canal rouge. Le type est FLOAT.<br/> La valeur par défaut est 0.0 f.<br/>                                                                                                                                                                                                                                                                                                                                                                                                |
| RedDisable<br/> D2D1 \_ GAMMATRANSFER \_ prop \_ rouge \_ Disable<br/>         | Si vous définissez cette valeur sur TRUE, elle n’applique pas la fonction de transfert au canal rouge. Une fonction de transfert d’identité est utilisée. Si vous définissez cette valeur sur FALSe, elle applique la fonction de transfert gamma au canal rouge. Le type est BOOL.<br/> La valeur par défaut est FALSE.<br/>                                                                                                                                                                                                                                                |
| GreenAmplitude<br/> \_ \_ \_ Amplitude vert d2d1 GAMMATRANSFER \_ prop<br/> | Amplitude de la fonction de transfert gamma pour le canal vert. Le type est FLOAT.<br/> La valeur par défaut est 1,0 f.<br/>                                                                                                                                                                                                                                                                                                                                                                                           |
| GreenExponent<br/> \_ \_ \_ Exposant vert d2d1 GAMMATRANSFER \_ prop<br/>   | Exposant de la fonction de transfert gamma pour le canal vert. Le type est FLOAT.<br/> La valeur par défaut est 1,0 f.<br/>                                                                                                                                                                                                                                                                                                                                                                                            |
| GreenOffset<br/> \_ \_ \_ Décalage vert d2d1 GAMMATRANSFER \_ prop<br/>       | Décalage de la fonction de transfert gamma pour le canal vert. Le type est FLOAT.<br/> La valeur par défaut est 0.0 f.<br/>                                                                                                                                                                                                                                                                                                                                                                                              |
| GreenDisable<br/> D2D1 \_ GAMMATRANSFER \_ prop \_ vert \_ Disable<br/>     | Si vous définissez cette valeur sur TRUE, elle n’applique pas la fonction de transfert au canal vert. Une fonction de transfert d’identité est utilisée. Si vous définissez cette valeur sur FALSe, elle applique la fonction de transfert gamma au canal vert. Le type est BOOL.<br/> La valeur par défaut est FALSE.<br/>                                                                                                                                                                                                                                            |
| BlueAmplitude<br/> \_ \_ \_ Amplitude bleue d2d1 GAMMATRANSFER \_ prop<br/>   | Amplitude de la fonction de transfert gamma pour le canal bleu. Le type est FLOAT.<br/> La valeur par défaut est 1,0 f.<br/>                                                                                                                                                                                                                                                                                                                                                                                            |
| BlueExponent<br/> \_ \_ \_ Exposant bleu d2d1 GAMMATRANSFER \_ prop<br/>     | Exposant de la fonction de transfert gamma pour le canal bleu. Le type est FLOAT.<br/> La valeur par défaut est 1,0 f.<br/>                                                                                                                                                                                                                                                                                                                                                                                             |
| BlueOffset<br/> Décalage bleu de D2D1 \_ GAMMATRANSFER \_ prop \_ \_<br/>         | Décalage de la fonction de transfert gamma pour le canal bleu. Le type est FLOAT.<br/> La valeur par défaut est 0.0 f.<br/>                                                                                                                                                                                                                                                                                                                                                                                               |
| BlueDisable<br/> D2D1 \_ GAMMATRANSFER \_ prop \_ bleu \_ Disable<br/>       | Si vous définissez cette valeur sur TRUE, elle n’applique pas la fonction de transfert au canal bleu. Une fonction de transfert d’identité est utilisée. Si vous définissez cette valeur sur FALSe, elle applique la fonction de transfert gamma au canal bleu. Le type est BOOL.<br/> La valeur par défaut est FALSE.<br/>                                                                                                                                                                                                                                              |
| AlphaAmplitude<br/> \_ \_ \_ Amplitude alpha d2d1 GAMMATRANSFER \_ prop<br/> | Amplitude de la fonction de transfert gamma pour le canal alpha. Le type est FLOAT.<br/> La valeur par défaut est 1,0 f.<br/>                                                                                                                                                                                                                                                                                                                                                                                           |
| AlphaExponent<br/> \_ \_ \_ Exposant alpha d2d1 GAMMATRANSFER \_ prop<br/>   | Exposant de la fonction de transfert gamma pour le canal alpha. Le type est FLOAT.<br/> La valeur par défaut est 1,0 f.<br/>                                                                                                                                                                                                                                                                                                                                                                                            |
| AlphaOffset<br/> \_ \_ \_ Décalage alpha d2d1 GAMMATRANSFER \_ prop<br/>       | Décalage de la fonction de transfert gamma pour le canal alpha. Le type est FLOAT.<br/> La valeur par défaut est 0.0 f.<br/>                                                                                                                                                                                                                                                                                                                                                                                              |
| AlphaDisable<br/> D2D1 \_ GAMMATRANSFER \_ prop \_ alpha \_ Disable<br/>     | Si vous définissez cette valeur sur TRUE, elle n’applique pas la fonction de transfert au canal alpha. Une fonction de transfert d’identité est utilisée. Si vous définissez cette valeur sur FALSe, elle applique la fonction de transfert gamma au canal alpha. Le type est BOOL.<br/> La valeur par défaut est FALSE.<br/>                                                                                                                                                                                                                                            |
| ClampOutput<br/> \_Sortie de Clamp d2d1 GAMMATRANSFER \_ prop \_ \_<br/>       | Si l’effet fixe les valeurs de couleur entre 0 et 1 avant que l’effet ne passe les valeurs à l’effet suivant dans le graphique. L’effet serre les valeurs avant de prémultiplier le alpha.<br/> Si vous affectez la valeur TRUE à cet effet, les valeurs sont ancrées. Si vous définissez cette valeur sur FALSe, l’effet n’attache pas les valeurs de couleur, mais d’autres effets et la surface de sortie peuvent fixer les valeurs si elles n’ont pas une précision suffisamment élevée.<br/> Le type est BOOL.<br/> La valeur par défaut est FALSE.<br/> |



 

## <a name="output-bitmap"></a>Bitmap de sortie

La taille de la bitmap de sortie est la même que la taille de la bitmap d’entrée.

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

 

