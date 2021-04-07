---
description: Effet d’accesseur Set alpha
ms.assetid: dd3ab119-328b-4782-811a-f06909c17dec
title: Effet d’accesseur Set alpha
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 372ec018a9cfb8fe15307ae44f5a905bf1eb3440
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103746372"
---
# <a name="alpha-setter-effect"></a>Effet d’accesseur Set alpha

> [!Note]  
> \[Action déconseillée. Cette API peut être supprimée dans les versions futures de Windows.\]

 

L’effet de l’accesseur Set alpha définit les bits alpha sur une image vidéo.

ID de classe (CLSID) : {506D89AE-909A-44f7-9444-ABD575896E35}

Nom de la variable CLSID : CLSID \_ DxtAlphaSetter

Nom convivial : « DxtAlphaSetter »

### <a name="properties"></a>Propriétés



| Propriété  | Type   | Default | Description                                                 |
|-----------|--------|---------|-------------------------------------------------------------|
| Alpha     | BYTE   | -1      | Définit l’alpha pour la totalité de l’image.                        |
| AlphaRamp | double | -1.0    | Définit le alpha comme pourcentage de la valeur alpha d’origine. |



 

## <a name="remarks"></a>Notes

Une propriété avec une valeur négative est ignorée. Une seule propriété peut avoir une valeur non négative. La propriété alpha spécifie une valeur alpha constante pour chaque pixel de l’image. Cette propriété remplace les valeurs alpha de l’image d’origine. La propriété AlphaRamp spécifie la valeur alpha de chaque pixel sous la forme d’un pourcentage de la valeur d’origine du pixel, de 0,0 à 1,0.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Fusion alpha](alpha-blending.md)
</dt> </dl>

 

 



