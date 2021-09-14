---
title: Effet Atlas
description: Vous pouvez utiliser cet effet pour sortir une partie d’une image tout en conservant la région en dehors de la partie pour une utilisation dans les opérations suivantes.
ms.assetid: D35E32CB-4DF7-408F-A717-1E421DDC8763
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f9e1d4c6df0698d47a35eb2cbdaf670b98ed125
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127114201"
---
# <a name="atlas-effect"></a>Effet Atlas

Vous pouvez utiliser cet effet pour sortir une partie d’une image tout en conservant la région en dehors de la partie pour une utilisation dans les opérations suivantes.

Le CLSID de cet effet est CLSID \_ D2D1Atlas.

L’effet Atlas est utile si vous souhaitez charger une grande image composée de nombreuses images plus petites, telles que des images différentes d’un sprite.

Pour créer la sortie, l’effet :

1.  Découpe l’entrée vers la propriété *InputRect* donnée.
2.  Convertit l’origine du résultat en (0,0).

> [!Note]  
> La propriété *InputPaddingRect* doit être supérieure uniquement si et seulement si les pixels entre les deux rectangles sont transparents en noir sur l’entrée. Cela peut entraîner l’exécution de Direct2D de manière plus optimale sur le graphique.

 

Voici un exemple de l’effet. Cette image est petite et simple à des fins d’illustration.

![image d’entrée.](images/atlas.png)

L’image précédente est l’entrée de l’effet. Le code suivant crée un effet Atlas, définit l’entrée, définit le rectangle de saisie, puis dessine la sortie.


```C++
ComPtr<ID2D1Effect> atlasEffect;

// Create the Atlas Effect.
DX::ThrowIfFailed(m_d2dContext->CreateEffect(CLSID_D2D1Atlas, &atlasEffect));

// Set the input.
atlasEffect->SetInputEffect(0, inputImage.Get());

// The images here are 150 x 150 pixels.
float size = 150.0f;

// Compensate for the padding between images.
float padding = 10.0f;

// The input rectangle.  150 x 150 pixels with 10 pixel padding
D2D1_Vector_4F inputRect = D2D1::Vector4F(size + (padding * 2), padding, size, size);

DX::ThrowIfFailed(atlasEffect->SetValue(D2D1_ATLAS_PROP_INPUT_RECT, inputRect));

// Draw the image
m_d2dContext->DrawImage(atlasEffect.Get());
```



Le code précédent sélectionne un rectangle autour du deuxième triangle. La marge autour est ignorée. Voici l’image résultante.

![image de sortie.](images/atlas2.png)

> [!Note]  
> Il s’agit d’une situation dans laquelle vous pouvez choisir de spécifier un *InputPaddingRect* , car le remplissage est transparent. Le rectangle est `D2D1::Vector4F(size + (padding * 2), 0, size + padding, size + padding);` .

 

## <a name="effect-properties"></a>Propriétés d’effet



| Nom complet et énumération d’index                                             | Description                                                                                                                                                                  |
|--------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| InputRect<br/> \_ \_ \_ Recto d’entrée d2d1 Atlas prop \_<br/>                 | Partie de l’image passée à l’effet suivant.<br/> Le type est D2D1 \_ Vector \_ 4F.<br/> La valeur par défaut est (-FLT \_ Max,-FLT \_ Max, FLT \_ Max, FLT \_ Max). <br/> |
| InputPaddingRect<br/> D2D1 \_ Atlas \_ prop \_ de \_ remplissage d' \_ entrée<br/> | Taille maximale échantillonnée pour le rectangle de sortie.<br/> Le type est D2D1 \_ Vector \_ 4F.<br/> La valeur par défaut est (-FLT \_ Max,-FLT \_ Max, FLT \_ Max, FLT \_ Max).<br/>   |



 

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

 

