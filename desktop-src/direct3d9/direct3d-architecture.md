---
description: 'Cette rubrique fournit deux vues de haut niveau de l’architecture de Direct3D :'
ms.assetid: ed08b4c8-fdd9-46fb-a2be-c2fb15af2dc6
title: Architecture Direct3D (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e557b7a36aadcaa8b96899047a721741ecef2156
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126916636"
---
# <a name="direct3d-architecture-direct3d-9"></a>Architecture Direct3D (Direct3D 9)

Cette rubrique fournit deux vues de haut niveau de l’architecture de Direct3D :

-   [Pipeline de graphiques Direct3D](#direct3d-graphics-pipeline) : vue de l’architecture de traitement interne du système de rendu Direct3D.
-   [Intégration du système Direct3D](#direct3d-system-integration) : vue de la façon dont Direct3D entre une application et le matériel graphique.

## <a name="direct3d-graphics-pipeline"></a>Pipeline graphique Direct3D

Le pipeline graphique offre la puissance nécessaire pour traiter et restituer efficacement les scènes Direct3D à un affichage, en tirant parti du matériel disponible. Le diagramme suivant montre les blocs de construction du pipeline :

![diagramme du pipeline de graphiques Direct3D](images/blockdiag-graphics.png)



| Composant de pipeline  | Description                                                                                                                                                                                      | Rubriques connexes                                                                                                                                                                                             |
|---------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Données de vertex         | Les vertex de modèle non transformés sont stockés dans des mémoires tampons de mémoire de vertex.                                                                                                                                | [Mémoires tampons de vertex (Direct3D 9)](vertex-buffers.md), [ **IDirect3DVertexBuffer9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexbuffer9)                                                                                                |
| Données Primitives      | Les primitives géométriques, y compris les points, lignes, triangles et polygones, sont référencées dans les données de vertex avec des mémoires tampons d’index.                                                                    | [Mémoires tampons d’index (Direct3D 9)](index-buffers.md), [**IDirect3DIndexBuffer9**](/windows/desktop/api), [primitives](primitives.md), [primitifs d’ordre supérieur (Direct3D 9)](higher-order-primitives.md) |
| Pavage        | L’unité Tesselator convertit les primitives d’ordre supérieur, les mappages de déplacement et les correctifs de maillage en emplacements de vertex et les stocke dans les mémoires tampons de vertex.                                      | [Pavage (Direct3D 9)](tessellation.md)                                                                                                                                                              |
| Traitement des vertex   | Les transformations Direct3D sont appliquées aux vertex stockés dans la mémoire tampon de vertex.                                                                                                                    | [Pipeline de vertex (Direct3D 9)](vertex-pipeline.md)                                                                                                                                                        |
| Traitement de la géométrie | Le découpage, l’élimination des faces arrière, l’évaluation des attributs et la pixellisation sont appliqués aux sommets transformés.                                                                                    | [Pipeline de pixels (Direct3D 9)](pixel-pipeline.md)                                                                                                                                                          |
| Surface texturée    | Les coordonnées de texture des surfaces Direct3D sont fournies à Direct3D via l’interface [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) .                                                         | [Textures Direct3D (Direct3D 9)](direct3d-textures.md), [ **IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)                                                                                                    |
| Échantillonneur de texture     | Le filtrage du niveau de détail de la texture est appliqué aux valeurs de texture d’entrée.                                                                                                                            | [Textures Direct3D (Direct3D 9)](direct3d-textures.md)                                                                                                                                                    |
| Traitement des pixels    | Les opérations de nuanceur de pixels utilisent les données géométriques pour modifier les données de texture et de vertex d’entrée, ce qui produit des valeurs de couleur de pixel de                                                                           | [Pipeline de pixels (Direct3D 9)](pixel-pipeline.md)                                                                                                                                                          |
| Rendu de pixel     | Les processus de rendu finaux modifient les valeurs de couleur de Pixel avec le test alpha, de profondeur ou de stencil, ou en appliquant la fusion alpha ou le brouillard. Toutes les valeurs de pixels résultantes sont présentées à l’affichage de sortie. | [Pipeline de pixels (Direct3D 9)](pixel-pipeline.md)                                                                                                                                                          |



 

## <a name="direct3d-system-integration"></a>Intégration du système Direct3D

Le diagramme suivant montre les relations entre une application Windows, Direct3D, GDI et le matériel :

![diagramme de la relation entre Direct3D et d’autres composants système](images/d3dsysint.png)

Direct3D expose une interface indépendante de l’appareil à une application. Les applications Direct3D peuvent exister avec les applications GDI, et elles ont toutes les deux accès au matériel graphique de l’ordinateur par le biais du pilote de périphérique de la carte graphique. Contrairement à GDI, Direct3D peut tirer parti des fonctionnalités matérielles en créant un appareil Hal.

Un périphérique Hal offre une accélération matérielle aux fonctions de pipeline graphique, en fonction de l’ensemble de fonctionnalités pris en charge par la carte graphique. Des méthodes Direct3D sont fournies pour récupérer les fonctionnalités d’affichage des appareils au moment de l’exécution. (Voir [**IDirect3DDevice9 :: GetDeviceCaps**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdevicecaps).) Si une fonctionnalité n’est pas fournie par le matériel, la couche HAL ne la signale pas comme une fonctionnalité matérielle.

Pour plus d’informations sur la HAL et les périphériques de référence pris en charge par Direct3D, voir [types d’appareils (Direct3D 9)](device-types.md).

## <a name="related-topics"></a>Rubriques connexes

[Prise en main](getting-started.md)
