---
description: Les applications peuvent optimiser le sous-ensemble d’une texture qui est copiée en spécifiant &\# 0034 ; sale&\# 0034 ; régions sur les textures.
ms.assetid: 102081bc-d5d5-4ec1-b935-00d4eda8f470
title: Régions de modification de texture (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35e3f1ce350a2728c99c49455b5fb8b638c47d10
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106515746"
---
# <a name="texture-dirty-regions-direct3d-9"></a>Régions de modification de texture (Direct3D 9)

Les applications peuvent optimiser le sous-ensemble d’une texture qui est copiée en spécifiant des régions « modifiées » sur les textures. Seules les régions marquées comme modifiées sont copiées par un appel à [**IDirect3DDevice9 :: UpdateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatetexture). Toutefois, les régions modifiées peuvent être développées pour optimiser l’alignement. Quand une texture est créée, la texture entière est considérée comme modifiée. Seules les opérations suivantes affectent l’état de modification d’une texture :

-   Ajout d’une région modifiée à une texture.
-   Verrouillage d’une mémoire tampon dans la texture. Cette opération ajoute la région verrouillée en tant que région modifiée. L’application peut désactiver cette mise à jour automatique de la région de modification s’il a une meilleure connaissance des régions de modification réelles.
-   L’utilisation d’un niveau de surface de la texture comme destination dans [**IDirect3DDevice9 :: UpdateSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatesurface) marque l’intégralité de la texture comme étant modifiée.
-   L’utilisation de la texture comme source dans [**IDirect3DDevice9 :: UpdateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatetexture) efface toutes les régions modifiées sur la texture source.
-   Utilisation de [**IDirect3DSurface9 :: GetDC**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dsurface9-getdc) pour retourner un contexte de périphérique.
-   L’appel de [**IDirect3DBaseTexture9 :: GenerateMipSubLevels**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dbasetexture9-generatemipsublevels) marque l’intégralité de la texture comme étant modifiée.
-   L’appel de [**IDirect3DBaseTexture9 :: SetAutoGenFilterType**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dbasetexture9-setautogenfiltertype) marque l’intégralité de la texture comme étant modifiée.

Les régions modifiées sont définies au niveau supérieur d’une texture mipmapped et [**IDirect3DDevice9 :: UpdateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatetexture) peut développer la région modifiée vers le haut de la chaîne MIP afin de réduire le nombre d’octets copiés pour chaque sous-niveau. Notez que les coordonnées de la région de modification de niveau inférieur sont arrondies vers l’extérieur, c’est-à-dire que leurs parties fractionnaires sont arrondies vers le bord le plus proche de la texture.

Étant donné que chaque type de texture a des types différents de régions modifiées, il existe des méthodes sur chaque type de texture. les textures 2D utilisent le rectangle sale et les zones d’utilisation des textures de volume.

-   [**IDirect3DCubeTexture9::AddDirtyRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-adddirtyrect)
-   [**IDirect3DTexture9::AddDirtyRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-adddirtyrect)
-   [**IDirect3DVolumeTexture9::AddDirtyBox**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolumetexture9-adddirtybox)

Si vous transmettez la **valeur null** pour les paramètres PDirtyRect ou pDirtyBox des méthodes ci-dessus, la zone modifiée est développée pour couvrir la texture entière.

Chaque méthode de verrouillage peut prendre \_ D3DLOCK \_ aucune \_ mise à jour incorrecte, ce qui empêche toute modification de l’état de modification de la texture. Pour plus d’informations, consultez [verrouillage des ressources (Direct3D 9)](locking-resources.md).

Lorsque des informations sur l’ensemble réel des régions modifiées pendant une opération de verrouillage sont disponibles, les applications doivent utiliser D3DLOCK \_ aucune \_ \_ mise à jour incorrecte. Notez qu’un verrou ou une copie vers un sous-niveau de texture uniquement (autrement dit, sans verrouillage ou copie au niveau supérieur) ne met pas à jour les régions modifiées pour cette texture. Les applications assument la même responsabilité pour la mise à jour des régions modifiées lorsqu’elles verrouillent des niveaux inférieurs sans verrouiller le niveau le plus élevé.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Concepts de base de la texturation](basic-texturing-concepts.md)
</dt> </dl>

 

 
