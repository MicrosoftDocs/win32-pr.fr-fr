---
description: Le brouillard de pixel obtient son nom du fait qu’il est calculé en fonction de chaque pixel dans le pilote de périphérique.
ms.assetid: 6fcfb9fa-cacc-4dbc-bfc6-85d533dbfbf8
title: Brouillard de pixel (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f62a597820fa009207d8dda7836d161cdf34c88
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103845734"
---
# <a name="pixel-fog-direct3d-9"></a>Brouillard de pixel (Direct3D 9)

Le brouillard de pixel obtient son nom du fait qu’il est calculé en fonction de chaque pixel dans le pilote de périphérique. Cela est différent du brouillard de vertex, qui est calculé par le pipeline pendant les calculs de transformation et d’éclairage. Le brouillard de pixel est parfois appelé « voile de table », car certains pilotes utilisent une table de recherche précalculée pour déterminer le facteur de brouillard, en utilisant la profondeur de chaque pixel à appliquer dans le calcul de la fusion. Elle peut être appliquée à l’aide de toute formule de brouillard identifiée par les membres du type énuméré [**D3DFOGMODE**](./d3dfogmode.md) . Les implémentations de ces formules sont spécifiques au pilote. Si un pilote ne prend pas en charge une formule de brouillard complexe, il doit se dégrader par une formule moins complexe.

## <a name="eye-relative-vs-z-based-depth"></a>Eye-Relative différences par rapport à la profondeur Z

Pour atténuer les artefacts graphiques liés au brouillard provoqués par une répartition inégale des valeurs z dans un tampon de profondeur, la plupart des périphériques matériels utilisent une profondeur relative à l’oeil au lieu des valeurs de profondeur basées sur z pour le brouillard de pixel. La profondeur relative à l’oeil est essentiellement l’élément w d’un jeu de coordonnées homogène. Microsoft Direct3D prend la réciproque de l’élément RHW à partir d’un jeu de coordonnées de l’espace de l’appareil pour reproduire true w. Si un appareil prend en charge le brouillard relatif à Eye, il définit l’indicateur **D3DPRASTERCAPS \_ WFOG** dans le membre RasterCaps de la structure [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) lorsque vous appelez la méthode [**IDirect3DDevice9 :: GetDeviceCaps**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdevicecaps) . À l’exception du rastériseur de référence, les périphériques logiciels utilisent toujours z pour calculer les effets de brouillard de pixel.

Lorsque le brouillard relatif à l’oeil est pris en charge, le système utilise automatiquement la profondeur relative à l’oeil plutôt que la profondeur basée sur z Si la matrice de projection fournie produit des valeurs z dans l’espace universel qui sont équivalentes aux valeurs w dans l’espace de l’appareil. Vous définissez la matrice de projection en appelant la méthode [**IDirect3DDevice9 :: setTransform**](/windows/desktop/api) , en utilisant la \_ valeur de projection D3DTS et en passant une structure [**D3DMATRIX**](d3dmatrix.md) qui représente la matrice souhaitée. Si la matrice de projection n’est pas conforme à cette exigence, les effets de brouillard ne sont pas appliqués correctement. Pour plus d’informations sur la génération d’une matrice conforme, consultez [projection Transform (Direct3D 9)](projection-transform.md).

Direct3D utilise la matrice de projection actuellement définie dans ses calculs de profondeur basés sur w. Par conséquent, une application doit définir une matrice de projection conforme pour recevoir les fonctionnalités w souhaitées, même si elle n’utilise pas le pipeline de transformation Direct3D.

Direct3D vérifie la quatrième colonne de la matrice de projection. Si les coefficients sont 0, 0, \[ 0, 1 \] (pour une projection affine), le système utilise des valeurs de profondeur basées sur z pour le brouillard. Dans ce cas, vous devez également spécifier les distances de début et de fin pour les effets de brouillard linéaires dans l’espace de l’appareil, qui s’étend de 0,0 au point le plus proche de l’utilisateur, et 1,0 au point le plus éloigné.

## <a name="using-pixel-fog"></a>Utilisation du brouillard de pixel

Utilisez les étapes suivantes pour activer le brouillard de pixel dans votre application.

1.  Activez la fusion de brouillard en affectant \_ à l’état de rendu D3DRS FOGENABLE la **valeur true**.
2.  Définissez la couleur de brouillard souhaitée dans l' \_ État de rendu D3DRS FOGCOLOR.
3.  Choisissez la formule de brouillard à utiliser en affectant \_ à l’état de rendu D3DRS FOGTABLEMODE le membre correspondant du type énuméré [**D3DFOGMODE**](./d3dfogmode.md) .
4.  Définissez les paramètres de brouillard comme vous le souhaitez pour le mode de brouillard sélectionné dans les États de rendu associés. Cela comprend les distances de début et de fin pour le brouillard linéaire et la densité de brouillard pour le mode de brouillard exponentiel.

L’exemple suivant montre à quoi ces étapes peuvent ressembler dans le code.


```
// For brevity, error values in this example are not checked 
//   after each call. A real-world application should check 
//   these values appropriately.
//
// For the purposes of this example, g_pDevice is a valid
//   pointer to an IDirect3DDevice9 interface.
void SetupPixelFog(DWORD Color, DWORD Mode)
{
    float Start   = 0.5f;    // For linear mode
    float End     = 0.8f;
    float Density = 0.66f;   // For exponential modes
 
    // Enable fog blending.
    g_pDevice->SetRenderState(D3DRS_FOGENABLE, TRUE);
 
    // Set the fog color.
    g_pDevice->SetRenderState(D3DRS_FOGCOLOR, Color);
    
    // Set fog parameters.
    if( Mode == D3DFOG_LINEAR )
    {
        g_pDevice->SetRenderState(D3DRS_FOGTABLEMODE, Mode);
        g_pDevice->SetRenderState(D3DRS_FOGSTART, *(DWORD *)(&Start));
        g_pDevice->SetRenderState(D3DRS_FOGEND,   *(DWORD *)(&End));
    }
    else
    {
        g_pDevice->SetRenderState(D3DRS_FOGTABLEMODE, Mode);
        g_pDevice->SetRenderState(D3DRS_FOGDENSITY, *(DWORD *)(&Density));
    }
```



Certains paramètres de brouillard sont requis comme valeurs à virgule flottante, même si la méthode [**IDirect3DDevice9 :: SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) accepte uniquement des valeurs DWORD dans le deuxième paramètre. L’exemple précédent fournit les valeurs à virgule flottante à **IDirect3DDevice9 :: SetRenderState** sans traduction de données en convertissant les adresses des variables à virgule flottante en pointeurs DWORD, puis en les déréférençant.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Types de brouillard](fog-types.md)
</dt> </dl>

 

 
