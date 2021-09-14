---
description: Les mappages de déplacement sont similaires aux cartes de texture, mais sont accessibles par le moteur de vertex.
ms.assetid: d6f16ff2-5a66-48a3-82c4-523faaafa6ae
title: Mappage de déplacement (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b687583b0109223d8c2dac807425e235ddf280e4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126916615"
---
# <a name="displacement-mapping-direct3d-9"></a>Mappage de déplacement (Direct3D 9)

Les mappages de déplacement sont similaires aux cartes de texture, mais sont accessibles par le moteur de vertex.

## <a name="block-diagram"></a>Diagramme de blocs

Une étape supplémentaire de l’échantillonneur est présente dans la partie précoce du canal de vertex, comme illustré dans le diagramme suivant, qui peut échantillonner un mappage de déplacement pour fournir des données de déplacement de vertex.

![diagramme de l’étape de l’échantillonneur dans le canal de vertex](images/tessellatordx9.png)

L’état de l’échantillonneur de mappage de décalage peut être défini par [**SetSamplerState**](/windows/desktop/api) à l’aide du numéro de phase 256, qui est un nouveau numéro de phase. La texture de la carte de déplacement est définie par [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture).

La carte peut être prééchantillonnée ou non, ce qui signifie qu’elle peut être classée de façon à permettre la recherche des valeurs de déplacement sans filtrage.

-   Les mappages de déplacements sont analogues aux cartes de texture, mais sont accessibles par le moteur de vertex.
-   Une étape supplémentaire de l’échantillonneur est présente dans la partie précoce du canal de vertex qui peut échantillonner un mappage de déplacement. Cette étape est accessible par l’API SetSamplerState habituelle, mais le numéro intermédiaire est D3DDMAPSAMPLER = 256.
-   L’état de l’échantillonneur de mappage de décalage peut être défini par SetSamplerState (D3DDMAPSAMPLER,...) MobileVBActiveX.
-   La texture de la carte de déplacement est définie par l’API SetTexture (D3DDMAPSAMPLER, texture).
-   La carte peut être prééchantillonnée ou non. Cela signifie qu’elle peut être ordonnée d’une manière particulière qui permet la recherche des valeurs de déplacement sans filtrage.
-   Les modifications apportées à la structure de la déclaration autorisent la spécification de la coordonnée de texture utilisée pour rechercher la carte de texture. Par exemple, Stream0, offset, FLOAT2, LOOKUP, valeur de déplacement \_ . Cela indique à du paveur d’utiliser le vecteur de virgule flottante 2D dans stream0 à un certain décalage comme une coordonnée de texture pour rechercher la carte de décalage et associer la \_ sémantique d’utilisation de la valeur de remplacement à celle-ci. La déclaration du nuanceur de sommets contient une ligne similaire à {DCL \_ Texture0, V0} indiquant que la sémantique Texture0 doit être associée au registre d’entrée v0. La valeur de déplacement recherchée est copiée dans le registre d’entrée v0.
-   Il existe un type spécial de mappage de déplacement, lorsque la carte de texture est prééchantillonnée. L’index séquentiel des vertex générés est utilisé comme coordonnée de texture sur une carte de texture. Par exemple, 0, 0, (D3DDECLTYPE) 0, D3DDECLMETHOD \_ LOOKUPPRESAMPLED, usage, UsageIndex.
-   La sortie de la recherche est de 4 valeurs à virgule flottante.
-   Le mappage de déplacement est pris en charge uniquement avec N-patchs.
-   Les pilotes doivent ignorer D3DDMAPSAMPLER dans SetTextureStageState s’ils ne gèrent pas les mappages de déplacement.
-   Le \_ mode de filtre anisotrope D3DTEXF n’est pas pris en charge.
-   Lorsque D3DSAMP \_ MIPFILTER dans l’échantillonneur de mappage de déplacement n’est pas D3DTEXF \_ aucun, le niveau de détail est calculé comme suit (Notez que l’état de pavage adaptatif est utilisé même si le D3DRS \_ ENABLEADAPTIVETESSELLATION est **false**) : Tmax = état de rendu D3DRS \_ MAXTESSELLATIONLEVEL
-   Calculer le niveau de pavage pour un vertex VI : (XI, Yi, ZI) de la même façon que décrit dans la section « pavage adaptative ». Niveau de détail L = Log2 (Tmax)-Log2 (te).
-   Les opérations de filtrage et d’échantillonnage de texture suivent les mêmes règles que le pipeline de pixel (le niveau de détail (LOD) est appliqué, etc.).
-   Tous les formats ne peuvent pas être utilisés comme mappages de déplacement, mais uniquement ceux qui prennent en charge le \_ DMAP D3DUSAGE. L’application peut interroger avec le [**CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat)CheckDeviceFormat.
-   D3DUSAGE \_ DMAP doit être spécifié dans [**CreateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createtexture) pour indiquer au pilote que cette texture doit être utilisée comme mappage de déplacement.
-   D3DUSAGE \_ DMAP peut uniquement être utilisé avec des textures. Elle ne peut pas être utilisée avec des mappages ou des volumes de cube.
-   Les textures et les cibles de rendu créées avec D3DUSAGE \_ DMAP peuvent être définies au niveau des étapes d’échantillonnage normales et en tant que cibles de rendu.
-   Les États de rendu permettant de définir le mode de renvoi à la ligne pour les coordonnées de texture sont ignorés dans le mappage de déplacement. En général, il n’y a pas de mode de retour à la ligne pour le moteur du paveur.
-   Un échantillonneur de mappage de déplacement a un comportement identique à celui des échantillonneurs de texture de pixels. Si une texture avec moins de quatre canaux (comme R32f) est recherchée, les valeurs recherchées sont dirigées vers les canaux appropriés du registre de destination (le registre d’entrée du nuanceur de sommets marqué avec l' \_ exemple de sémantique), tandis que les autres canaux ont par défaut la valeur (1, 1, 1). Lors de \_ la recherche, D3DFMT N8 est diffusé dans les canaux R, G, B et A une valeur par défaut de 1. Le rastériseur de référence contient les détails de l’implémentation complète.

## <a name="pre-sampled-displacement-mapping"></a>Mappage de déplacement pré-échantillonné

-   Nouvel état de l’échantillonneur introduit : D3DSAMP \_ DMAPOFFSET (DWORD)-offset (en vertex) dans un mappage de déplacement pré-échantillonné.
-   Nouvelle méthode de déclaration introduite : D3DDECLMETHOD \_ LOOKUPPRESAMPLED.
-   Le pavage adaptatif doit être désactivé.
-   Les paramètres de filtre de texture sont ignorés. L’échantillonnage des points est effectué. Le filtre de texture MIP est supposé être D3DTEXF \_ aucun. Tous les autres modes de filtre de texture sont supposés être D3DTEXF \_ point.
-   Les coordonnées de la texture sont calculées comme suit : U = (index% TextureWidthInPixeles)/(float) (TextureWidthInPixeles) V = (index/TextureWidthInPixeles)/(float) (TextureHeightInPixeles), où index est un index séquentiel des vertex générés plus TSS D3DSAMP DMAPOFFSET \[ \_ \] . L’index séquentiel est défini à zéro au début de chaque primitive et est augmenté après la génération d’un vertex.

Il s’agit des modifications d’API qui prennent en charge le mappage de déplacement.

-   Un format de canal unique ajouté, D3DFMT \_ L16.
-   Un nouvel indicateur d’utilisation, D3DUSAGE \_ DMAP.
-   Étape de texture spéciale, utilisée pour définir une texture de mappage de déplacement, D3DDMAPSAMPLER.
-   De nouvelles extrémités matérielles ont été ajoutées, D3DDEVCAPS2 \_ DMAPNPATCH et D3DDEVCAPS2 \_ PRESAMPLEDDMAPNPATCH. Consultez [D3DDEVCAPS2](d3ddevcaps2.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Pipeline de vertex](vertex-pipeline.md)
</dt> </dl>

 

 
