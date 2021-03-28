---
title: ByteAddressBuffer
description: ByteAddressBuffer
ms.assetid: 809b5ee8-0a25-402e-8cf2-f5e7a8094ec6
keywords:
- HLSL ByteAddressBuffer
topic_type:
- apiref
api_name:
- ByteAddressBuffer
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 03e89f56522d941db4447b33b55cbedc7c73303f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104971786"
---
# <a name="byteaddressbuffer"></a>ByteAddressBuffer

Mémoire tampon en lecture seule indexée en octets.



| Méthode                                                              | Description                   |
|---------------------------------------------------------------------|-------------------------------|
| [**GetDimensions**](sm5-object-byteaddressbuffer-getdimensions.md) | Obtient les dimensions de ressource. |
| [**Load**](byteaddressbuffer-load.md)                              | Obtient une valeur.               |
| [**Load2**](byteaddressbuffer-load2.md)                            | Obtient deux valeurs.              |
| [**Load3**](byteaddressbuffer-load3.md)                            | Obtient trois valeurs.            |
| [**Load4**](byteaddressbuffer-load4.md)                            | Obtient quatre valeurs.             |



 

Vous pouvez utiliser le type d’objet **ByteAddressBuffer** quand vous travaillez avec des mémoires tampons brutes. Pour plus d’informations sur l’affichage brut des tampons, consultez [affichages bruts de mémoires tampons](/windows/desktop/direct3d11/overviews-direct3d-11-resources-intro).

## <a name="minimum-shader-model"></a>Modèle de nuanceur minimal

Cet objet est pris en charge dans les modèles de nuanceur suivants.



| Modèle de nuanceur                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               | Prise en charge |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------|
| Nuanceur [modèle 5](d3d11-graphics-reference-sm5.md) et modèles de nuanceur plus élevés [nuanceur de modèle 4](dx-graphics-hlsl-sm4.md) (disponible par le biais de l’API Direct3D 11 en utilisant le niveau de fonctionnalité 10,0 ou 10,1 ([**\_ \_ niveau de fonctionnalité D3D**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_feature_level) \_ 10 \_ X) sur les appareils qui prennent en charge les nuanceurs de calcul. Pour plus d’informations sur la prise en charge du nuanceur de calcul sur du matériel de niveau inférieur, consultez [nuanceurs de calcul sur du matériel de niveau inférieur](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-compute-shaders).)<br/> | Oui       |



 

Cet objet est pris en charge pour les types de nuanceurs suivants :



| Sommet | Forme | Domain | Géométrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

Pour plus d’informations sur une mémoire tampon d’adresse en octets, consultez le [type de ressource adressable en octets](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-resources).

Le Shader Model 5 implémente également une [mémoire tampon d’adresse d’octets en lecture-écriture](sm5-object-rwbyteaddressbuffer.md).

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Objets Shader Model 5](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

