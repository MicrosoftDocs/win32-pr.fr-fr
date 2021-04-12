---
description: Définit une couleur matérielle de base qui peut être appliquée à un maillage complet ou à des visages individuels d’un maillage. La puissance est l’exposant spéculaire du matériau.
ms.assetid: vs|directx_sdk|~\material.htm
title: Matériau
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54c13d201152350a8a61950bb609f73cbdb2a3aa
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104480704"
---
# <a name="material"></a>Matériau

Définit une couleur matérielle de base qui peut être appliquée à un maillage complet ou à des visages individuels d’un maillage. La puissance est l’exposant spéculaire du matériau.

``` syntax
template Material
{
    < 3D82AB4D-62DA-11CF-AB39-0020AF71E433 >
    ColorRGBA faceColor;
    FLOAT power;
    ColorRGB specularColor;
    ColorRGB emissiveColor;
    [...]
} 
```

Où :

-   faceColor : couleur de face. Modèle ColorRGBA. Consultez [**ColorRGBA**](colorrgba.md).
-   exposant de couleur spéculaire de l’alimentation.
-   specularColor : couleur spéculaire. Modèle ColorRGB. Consultez [**ColorRGB**](colorrgb.md).
-   emissiveColor : couleur de matériau émissif. Modèle ColorRGB. Consultez [**ColorRGB**](colorrgb.md).

> [!Note]  
> La couleur ambiante requiert un composant alpha.

 

[**TextureFilename**](texturefilename.md) est un objet de données facultatif. Si cet objet n’est pas présent, la face n’est pas texturée.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Modèles](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



