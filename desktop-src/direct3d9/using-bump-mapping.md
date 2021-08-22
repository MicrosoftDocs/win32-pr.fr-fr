---
description: Utilisation du mappage de relief (Direct3D 9)
ms.assetid: ded07764-1a11-42df-9a16-e4c3a328fb23
title: Utilisation du mappage de relief (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 195a99ffaa29d416aea93c5599f1fb461cd78a9961bd9c69f3f02ae3e8fe4719
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120025829"
---
# <a name="using-bump-mapping-direct3d-9"></a>Utilisation du mappage de relief (Direct3D 9)

## <a name="detecting-support-for-bump-mapping"></a>Détection de la prise en charge du mappage de relief

Un appareil peut effectuer un mappage de relief s’il prend en charge l' \_ opération de fusion de texture D3DTOP BUMPENVMAP ou D3DTOP \_ BUMPENVMAPLUMINANCE. Utilisez [**IDirect3D9 :: CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) avec \_ la requête D3DUSAGE \_ LEGACYBUMPMAP pour voir si un format est pris en charge pour le mappage de relief.

En outre, les applications doivent vérifier les fonctionnalités de l’appareil pour s’assurer que l’appareil prend en charge un nombre approprié d’étapes de fusion, en général au moins trois, et expose au moins un format de pixel de mappage de rugosité.

L’exemple de code suivant vérifie les fonctionnalités de l’appareil pour détecter la prise en charge du mappage de relief dans le périphérique actuel, à l’aide des critères spécifiés.


```
BOOL SupportsBumpMapping()
{
    D3DCAPS9 d3dCaps;

    d3dDevice->GetDeviceCaps( &d3dCaps );

    // Does this device support the two bump mapping blend operations?
    if ( 0 == d3dCaps.TextureOpCaps & ( D3DTEXOPCAPS_BUMPENVMAP |
                                            D3DTEXOPCAPS_BUMPENVMAPLUMINANCE ))
        return FALSE;

    // Does this device support up to three blending stages?
    if( d3dCaps.MaxTextureBlendStages < 3 )
        return FALSE;

    return TRUE;
}
```



## <a name="creating-a-bump-map-texture"></a>Création d’une texture de placage de relief

Vous créez une texture de placage de relief comme n’importe quelle autre texture. Votre application vérifie la prise en charge du mappage de relief et récupère un format de pixel valide, comme indiqué dans détection de la prise en charge du mappage de relief.

Une fois la surface créée, vous pouvez charger chaque pixel avec les valeurs Delta appropriées et la luminance, si le format de surface comprend la luminance. Les valeurs de chaque composant de pixel sont décrites dans formats de pixel de la [carte de relief (Direct3D 9)](bump-map-pixel-formats.md).

## <a name="configuring-bump-mapping-parameters"></a>Configuration des paramètres de mappage de relief

Lorsque votre application a créé une carte de relief et défini le contenu de chaque pixel, vous pouvez préparer le rendu en configurant des paramètres de mappage de relief. Les paramètres de mappage de relief incluent la définition des textures requises et leurs opérations de fusion, ainsi que des contrôles de transformation et de luminance pour le placage de relief lui-même.

1.  Définir la carte de texture de base si elle est utilisée, le mappage de relief et les textures de la carte d’environnement en étapes de fusion de texture.
2.  Définissez la couleur et les opérations de fusion alpha pour chaque étape de texture.
3.  Définissez la matrice de transformation de la carte de relief.
4.  Définissez les valeurs de l’échelle de luminance et du décalage en fonction des besoins.

L’exemple de code suivant définit trois textures (la carte de texture de base, la carte de relief et une carte d’environnement spéculaire) sur les étapes de fusion de texture appropriées.


```
// Set the three textures.
d3dDevice->SetTexture( 0, d3dBaseTexture );
d3dDevice->SetTexture( 1, d3dBumpMap );
d3dDevice->SetTexture( 2, d3dEnvMap );
```



Après avoir défini les textures à leurs étapes de fusion, l’exemple de code suivant prépare les opérations de fusion et les arguments pour chaque étape.


```
// Set the color operations and arguments to prepare for
//   bump mapping.

// Stage 0: The base texture
d3dDevice->SetTextureStageState( 0, D3DTSS_COLOROP, D3DTOP_MODULATE );
d3dDevice->SetTextureStageState( 0, D3DTSS_COLORARG1, D3DTA_TEXTURE );
d3dDevice->SetTextureStageState( 0, D3DTSS_COLORARG2, D3DTA_DIFFUSE );
d3dDevice->SetTextureStageState( 0, D3DTSS_ALPHAOP, D3DTOP_SELECTARG1 );
d3dDevice->SetTextureStageState( 0, D3DTSS_ALPHAARG1, D3DTA_TEXTURE ); 
d3dDevice->SetTextureStageState( 0, D3DTSS_TEXCOORDINDEX, 1 );

// Stage 1: The bump map - Use luminance for this example.
d3dDevice->SetTextureStageState( 1, D3DTSS_TEXCOORDINDEX, 1 );
d3dDevice->SetTextureStageState( 1, D3DTSS_COLOROP, D3DTOP_BUMPENVMAPLUMINANCE);
d3dDevice->SetTextureStageState( 1, D3DTSS_COLORARG1, D3DTA_TEXTURE );
d3dDevice->SetTextureStageState( 1, D3DTSS_COLORARG2, D3DTA_CURRENT );

// Stage 2: A specular environment map
d3dDevice->SetTextureStageState( 2, D3DTSS_TEXCOORDINDEX, 0 );
d3dDevice->SetTextureStageState( 2, D3DTSS_COLOROP, D3DTOP_ADD );
d3dDevice->SetTextureStageState( 2, D3DTSS_COLORARG1, D3DTA_TEXTURE );
d3dDevice->SetTextureStageState( 2, D3DTSS_COLORARG2, D3DTA_CURRENT );
```



Lorsque les arguments et opérations de fusion sont définis, l’exemple de code suivant définit la matrice de mappage de rugosité 2x2 sur la matrice d’identité en définissant les \_ membres D3DTSS BUMPENVMAPMAT00 et D3DTSS \_ BUMPENVMAPMAT11 de [**D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md) sur 1,0. Si vous affectez à la matrice l’identité, le système utilise les valeurs Delta de la carte de relief non modifiées, mais cela n’est pas obligatoire.


```
// Set the bump mapping matrix.
//
// Note  These calls rely on the following inline shortcut function:
//   inline DWORD F2DW( FLOAT f ) { return *((DWORD*)&f); }
d3dDevice->SetTextureStageState( 1, D3DTSS_BUMPENVMAT00, F2DW(1.0f) );
d3dDevice->SetTextureStageState( 1, D3DTSS_BUMPENVMAT01, F2DW(0.0f) );
d3dDevice->SetTextureStageState( 1, D3DTSS_BUMPENVMAT10, F2DW(0.0f) );
d3dDevice->SetTextureStageState( 1, D3DTSS_BUMPENVMAT11, F2DW(1.0f) );
```



Si vous définissez l’opération de mappage de bosselage pour inclure la luminance (D3DTOP \_ BUMPENVMAPLUMINANCE), vous devez définir les contrôles de luminance. Les commandes de luminance configurent la façon dont le système calcule la luminance avant de moduler la couleur à partir de la texture à l’étape suivante. Pour plus d’informations, consultez [formules de mappage de relief (Direct3D 9)](bump-mapping-formulas.md).


```
// Set luminance controls. This is only needed when using
// a bump map that contains luminance, and when the 
// D3DTOP_BUMPENVMAPLUMINANCE texture blending operation is
// being used.
//
// Note  These calls rely on the following inline shortcut function:
//   inline DWORD F2DW( FLOAT f ) { return *((DWORD*)&f); }
d3dDevice->SetTextureStageState( 1, D3DTSS_BUMPENVLSCALE, F2DW(0.5f) );
d3dDevice->SetTextureStageState( 1, D3DTSS_BUMPENVLOFFSET, F2DW(0.0f) );
```



Une fois que votre application a configuré les paramètres de mappage de bosselage, elle peut s’afficher normalement, et les polygones rendus en relief.

Notez que l’exemple précédent montre les paramètres définis pour le mappage d’environnement spéculaire. Lors de l’exécution d’un mappage de lumière diffuse, les applications définissent l’opération de fusion de texture pour la dernière étape en \_ modulant D3DTOP. pour plus d’informations, consultez [diffusion en clair Cartes (Direct3D 9)](diffuse-light-maps.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Placage de relief](bump-mapping.md)
</dt> </dl>

 

 
