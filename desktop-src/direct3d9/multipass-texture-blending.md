---
description: Les applications Direct3D peuvent obtenir de nombreux effets spéciaux en appliquant différentes textures à une primitive au cours de plusieurs passes de rendu.
ms.assetid: 884cc928-305e-46b9-acbf-ca58dfbc05e6
title: Fusion de texture multipasse (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df0a042088694f686003a6dc259cf1d914db2b59
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109150"
---
# <a name="multipass-texture-blending-direct3d-9"></a>Fusion de texture multipasse (Direct3D 9)

Les applications Direct3D peuvent obtenir de nombreux effets spéciaux en appliquant différentes textures à une primitive au cours de plusieurs passes de rendu. Le terme courant pour cela est la fusion de texture multipasse. Une utilisation classique de la fusion de texture multipasse consiste à émuler les effets des modèles d’éclairage et d’ombrage complexes en appliquant plusieurs couleurs à partir de différentes textures. Une telle application est appelée « mappage clair ». Pour plus d’informations, consultez [mappage de lumière avec des textures (Direct3D 9)](light-mapping-with-textures.md).

> [!Note]  
> Certains appareils peuvent appliquer plusieurs textures à des primitives en une seule passe. Pour plus d’informations, consultez [fusion de textures (Direct3D 9)](texture-blending.md).

 

Si le matériel de l’utilisateur ne prend pas en charge la fusion de plusieurs textures, votre application peut utiliser la fusion de texture multipasse pour obtenir les mêmes effets visuels. Toutefois, l’application ne peut pas supporter les fréquences d’images possibles lors de l’utilisation de plusieurs fusions de texture.

Pour effectuer une fusion de texture multipasse dans une application C/C++.

1.  Définissez une texture dans l’étape de texture 0 en appelant la méthode [**IDirect3DDevice9 :: SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) .
2.  Sélectionnez la couleur souhaitée et les arguments et opérations de fusion alpha à l’aide de la méthode [**IDirect3DDevice9 :: SetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate) . Les paramètres par défaut conviennent parfaitement pour la fusion de texture multipasse.
3.  Affichez les objets appropriés dans la scène.
4.  Définit la texture suivante dans l’étape de texture 0.
5.  Définissez les \_ États de rendu D3DRS SRCBLEND et D3DRS \_ DESTBLEND pour ajuster les facteurs de fusion source et de destination en fonction des besoins. Le système fusionne les nouvelles textures avec les pixels existants dans la surface de cible de rendu en fonction de ces paramètres.
6.  Répétez les étapes 3, 4 et 5 avec autant de textures que nécessaire.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Fusion de texture](texture-blending.md)
</dt> </dl>

 

 
