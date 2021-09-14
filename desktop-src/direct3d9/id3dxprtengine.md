---
description: L’interface ID3DXPRTEngine est utilisée pour calculer une simulation de transfert de luminance précalculée (PRT). Ses méthodes sont généralement utilisées en mode hors connexion pour calculer les vecteurs de transfert par sommet ou par Texel à l’avance de la modélisation 3D en temps réel.
ms.assetid: d5be657f-2b0c-48fd-a7f0-ddb90107772f
title: Interface ID3DXPRTEngine (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5507a79a60b2ffcb3cf801ea0454c7306bcde056
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126941215"
---
# <a name="id3dxprtengine-interface"></a>Interface ID3DXPRTEngine

L’interface ID3DXPRTEngine est utilisée pour calculer une simulation de transfert de luminance précalculée (PRT). Ses méthodes sont généralement utilisées en mode hors connexion pour calculer les vecteurs de transfert par sommet ou par Texel à l’avance de la modélisation 3D en temps réel.

## <a name="members"></a>Membres

L’interface **ID3DXPRTEngine** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **ID3DXPRTEngine** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **ID3DXPRTEngine** possède ces méthodes.



| Méthode                                                                                     | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|:-------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ClosestRayIntersects**](id3dxprtengine--closestrayintersects.md)                       | Utilise l’efficacité du traçage de rayon dans les simulations de transfert luminance (PRT) précalculées pour déterminer si un rayon croise une maille. Si une intersection est trouvée, la méthode retourne l’index du trait de filet le plus proche atteint par le rayon et les coordonnées Barycentric du point d’intersection.<br/>                                                                                                                                                                                |
| [**ComputeBounce**](id3dxprtengine--computebounce.md)                                     | Calcule le luminance source résultant d’un rebond unique de la lumière interreflete. Cette méthode peut être utilisée pour n’importe quelle scène éclairée, y compris un modèle de transfert luminance (PRT) à base d’harmonique sphérique (SH).<br/>                                                                                                                                                                                                                                                    |
| [**ComputeBounceAdaptive**](id3dxprtengine--computebounceadaptive.md)                     | Calcule le luminance source résultant d’un rebond unique de la lumière interreflet, à l’aide de l’échantillonnage adaptatif. Cette méthode génère de nouveaux vertex et des visages sur la maille pour rapprocher plus précisément le signal de transfert luminance (PRT) précalculé. Cette méthode peut être utilisée pour toute scène éclairée, y compris un modèle PRT basé sur l’harmonique sphérique (SH).<br/>                                                                                                                   |
| [**ComputeDirectLightingSH**](id3dxprtengine--computedirectlightingsh.md)                 | Calcule la contribution de l’éclairage direct aux objets 3D où le luminance source est représenté par une approximation de l’harmonique sphérique (SH).<br/>                                                                                                                                                                                                                                                                                                                            |
| [**ComputeDirectLightingSHAdaptive**](id3dxprtengine--computedirectlightingshadaptive.md) | Calcule la contribution de l’éclairage direct aux objets 3D où le luminance source est représenté par une approximation d’harmonique sphérique (SH), à l’aide de l’échantillonnage adaptatif. Cette méthode génère de nouveaux vertex et des visages sur la maille pour rapprocher plus précisément le signal de transfert luminance (PRT) précalculé.<br/>                                                                                                                                                           |
| [**ComputeDirectLightingSHGPU**](id3dxprtengine--computedirectlightingshgpu.md)           | Utilise le GPU pour calculer la contribution de l’éclairage direct aux objets 3D où le luminance source est représenté par une approximation de l’harmonique sphérique (SH). Le calcul de l’éclairage sur le GPU sera généralement beaucoup plus rapide que sur le processeur.<br/>                                                                                                                                                                                                                            |
| [**ComputeLDPRTCoeffs**](id3dxprtengine--computeldprtcoeffs.md)                           | Calcule les coefficients de transfert de luminance précalculés (LDPRT) déformables localement par rapport aux vecteurs normaux par échantillon pour réduire l’erreur des moindres carrés en ce qui concerne les données d’entrée [**ID3DXPRTBuffer**](id3dxprtbuffer.md) . Ces coefficients peuvent être utilisés avec des vecteurs normaux dépouillés ou transformés pour modéliser les effets globaux sur les objets dynamiques.<br/>                                                                                                                     |
| [**Les honorer**](id3dxprtengine--computess.md)                                             | Calcule le luminance source résultant de la diffusion sous-surface, à l’aide des propriétés de matériau définies par [**ID3DXPRTEngine :: SetMeshMaterials**](id3dxprtengine--setmeshmaterials.md). Cette méthode peut être utilisée uniquement pour les matériaux définis par vertex dans un objet de maillage.<br/>                                                                                                                                                                                                       |
| [**ComputeSSAdaptive**](id3dxprtengine--computessadaptive.md)                             | Calcule un vecteur de transfert qui mappe les luminance sources pour quitter les luminance résultant de la diffusion sous-surface, à l’aide de l’échantillonnage adaptatif et des propriétés de matériau définies par [**ID3DXPRTEngine :: SetMeshMaterials**](id3dxprtengine--setmeshmaterials.md). La méthode génère de nouveaux vertex et des visages sur la maille pour rapprocher plus précisément le signal de transfert luminance (PRT) précalculé. Cette méthode peut être utilisée uniquement pour les matériaux définis par vertex dans un objet de maillage.<br/> |
| [**ComputeSurfSamplesBounce**](id3dxprtengine--computesurfsamplesbounce.md)               | Calcule les exemples de transfert luminance (PRT) précalculés pour un point arbitraire (et vecteur normal).<br/>                                                                                                                                                                                                                                                                                                                                                                        |
| [**ComputeSurfSamplesDirectSH**](id3dxprtengine--computesurfsamplesdirectsh.md)           | Calcule, à un point arbitraire qui ne se trouve pas sur un maillage, un vecteur de transfert qui mappe les luminance sources (représentés par une approximation d’harmoniques sphériques) pour quitter luminance.<br/>                                                                                                                                                                                                                                                                                                   |
| [**ComputeVolumeSamples**](id3dxprtengine--computevolumesamples.md)                       | Calcule une projection de l’éclairage direct de la lumière précédente dans les vecteurs de base d’harmoniques sphériques (SH) qui représentent des luminance d’incident aux emplacements spécifiés.<br/>                                                                                                                                                                                                                                                                                         |
| [**ComputeVolumeSamplesDirectSH**](id3dxprtengine--computevolumesamplesdirectsh.md)       | Calcule une projection d’éclairage distant dans des vecteurs d’harmoniques sphériques (SH) qui représentent des luminance d’incident aux emplacements spécifiés.<br/>                                                                                                                                                                                                                                                                                                                           |
| [**ExtractPerVertexAlbedo**](id3dxprtengine--extractpervertexalbedo.md)                   | Copie les valeurs Albedo par vertex d’une maille.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                            |
| [**FreeBounceData**](id3dxprtengine--freebouncedata.md)                                   | Libère la mémoire utilisée pour les données de simulation de lumière rebondée temporaire.<br/>                                                                                                                                                                                                                                                                                                                                                                                                          |
| [**FreeSSData**](id3dxprtengine--freessdata.md)                                           | Libère la mémoire utilisée pour les données de simulation de diffusion de lumière de la sous-surface temporaire.<br/>                                                                                                                                                                                                                                                                                                                                                                                            |
| [**GetAdaptedMesh**](id3dxprtengine--getadaptedmesh.md)                                   | Retourne un maillage avec les modifications résultant de l’échantillonnage spatial adaptatif. Le maillage retourné contient uniquement des positions, des normales et des coordonnées de texture (s’il est défini).<br/>                                                                                                                                                                                                                                                                                                   |
| [**GetNumFaces**](id3dxprtengine--getnumfaces.md)                                         | Récupère le nombre de faces de la maille, y compris les nouvelles faces ajoutées à la suite d’un échantillonnage spatial adaptatif.<br/>                                                                                                                                                                                                                                                                                                                                                      |
| [**GetNumVerts**](id3dxprtengine--getnumverts.md)                                         | Récupère le nombre de vertex de la maille, y compris les nouveaux vertex ajoutés à la suite d’un échantillonnage spatial adaptatif.<br/>                                                                                                                                                                                                                                                                                                                                                |
| [**GetVertexAlbedo**](id3dxprtengine--getvertexalbedo.md)                                 | Récupère les valeurs Albedo des vertex de maillage.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**MultiplyAlbedo**](id3dxprtengine--multiplyalbedo.md)                                   | Multiplie chaque vecteur de transfert luminance (PRT) précalculé par le Albedo par vertex.<br/>                                                                                                                                                                                                                                                                                                                                                                                    |
| [**ResampleBuffer**](id3dxprtengine--resamplebuffer.md)                                   | Rééchantillonne une mémoire tampon d’entrée [**ID3DXPRTBuffer**](id3dxprtbuffer.md) et l’enregistre dans une mémoire tampon de sortie. Cette méthode peut être utilisée pour convertir une mémoire tampon de vertex en une mémoire tampon de texture et vice versa. Il peut également être utilisé pour convertir des mémoires tampons à canal unique en mémoires tampons de 3 canaux et vice versa.<br/>                                                                                                                                                                                  |
| [**RobustMeshRefine**](id3dxprtengine--robustmeshrefine.md)                               | Sous-divise les visages sur une maille, ce qui permet un échantillonnage adaptatif prudent qui n’élimine pas les caractéristiques de la maille.<br/>                                                                                                                                                                                                                                                                                                                                                   |
| [**ScaleMeshChunk**](id3dxprtengine--scalemeshchunk.md)                                   | Met à l’échelle tous les échantillons associés à un sous-maillage donné. La méthode est utile pour le calcul de la diffusion sous-surface.<br/>                                                                                                                                                                                                                                                                                                                                                       |
| [**SetCallBack**](id3dxprtengine--setcallback.md)                                         | Définit un pointeur vers une fonction de rappel facultative qui calcule le pourcentage de calculs de l’harmonique sphérique (SH) terminé et donne à l’appelant la possibilité d’abandonner le simulateur.<br/>                                                                                                                                                                                                                                                                               |
| [**SetMeshMaterials**](id3dxprtengine--setmeshmaterials.md)                               | Définit les propriétés de matériau de maillage dans la scène 3D. Utilisez cette méthode pour spécifier les paramètres de diffusion de sous-surface.<br/>                                                                                                                                                                                                                                                                                                                                                             |
| [**SetMinMaxIntersection**](id3dxprtengine--setminmaxintersection.md)                     | Définit les distances minimale et maximale de l’intersection entre les objets 3D. Ces valeurs de distance peuvent être utilisées pour contrôler la distance minimale ou maximale que les objets peuvent ombrer ou pour refléter la lumière. Par exemple, la méthode peut être utilisée pour limiter l’occultation des fonctionnalités avoisinantes d’un modèle 3D.<br/>                                                                                                                                                                          |
| [**SetPerTexelAlbedo**](id3dxprtengine--setpertexelalbedo.md)                             | Définit une valeur Albedo pour chaque Texel, en remplaçant les valeurs Albedo précédentes.<br/>                                                                                                                                                                                                                                                                                                                                                                                                |
| [**SetPerTexelNormal**](id3dxprtengine--setpertexelnormal.md)                             | Définit un vecteur normal pour chaque Texel dans un objet texture. Cette méthode est utilisée pour stocker des vecteurs normaux de vertex à partir d’une maille (ou des normales de vertex interpolées si le transfert de luminance précalculé basé sur les pixels (PRT) est calculé).<br/>                                                                                                                                                                                                                                          |
| [**SetPerVertexAlbedo**](id3dxprtengine--setpervertexalbedo.md)                           | Définit une valeur Albedo pour chaque vertex de maillage, en remplaçant les valeurs Albedo précédentes.<br/>                                                                                                                                                                                                                                                                                                                                                                                          |
| [**SetSamplingInfo**](id3dxprtengine--setsamplinginfo.md)                                 | Définit les propriétés d’échantillonnage utilisées par le simulateur de transfert luminance (PRT) précalculé.<br/>                                                                                                                                                                                                                                                                                                                                                                                     |
| [**ShadowRayIntersects**](id3dxprtengine--shadowrayintersects.md)                         | Utilise l’efficacité du traçage de rayon dans les simulations de transfert luminance (PRT) précalculées pour déterminer si un rayon croise une maille. Généralement utilisé pour déterminer si un point donné se trouve dans une ombre.<br/>                                                                                                                                                                                                                                                                             |



 

## <a name="remarks"></a>Notes

Pour convertir des valeurs RVB en valeurs de luminance, utilisez la formule suivante :


```
Luminance = R * 0.2125 + G * 0.7154 + B * 0.0721
```



L’interface **ID3DXPRTEngine** est obtenue en appelant la fonction [**D3DXCreatePRTEngine**](d3dxcreateprtengine.md) .

Le type LPD3DXPRTENGINE est défini comme un pointeur vers l’interface **ID3DXPRTEngine** .


```
typedef interface ID3DXPRTEngine ID3DXPRTEngine;
typedef interface ID3DXPRTEngine *LPD3DXPRTENGINE;
```



## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Interfaces D3DX](dx9-graphics-reference-d3dx-interfaces.md)
</dt> <dt>

[**D3DXCreatePRTEngine**](d3dxcreateprtengine.md)
</dt> <dt>

[Transfert de luminance précalculé (Direct3D 9)](precomputed-radiance-transfer.md)
</dt> </dl>

 

 
