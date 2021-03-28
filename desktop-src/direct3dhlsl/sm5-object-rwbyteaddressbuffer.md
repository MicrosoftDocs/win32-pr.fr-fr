---
title: RWByteAddressBuffer
description: Mémoire tampon de lecture/écriture qui indexe en octets.
ms.assetid: 8370c14c-5822-4240-942d-565aa223d48c
keywords:
- HLSL RWByteAddressBuffer
topic_type:
- apiref
api_name:
- RWByteAddressBuffer
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4d065926b0769e15284cbe705783be012d82554b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104381984"
---
# <a name="rwbyteaddressbuffer"></a>RWByteAddressBuffer

Mémoire tampon de lecture/écriture qui indexe en octets.



| Méthode                                                                                          | Description                         |
|-------------------------------------------------------------------------------------------------|-------------------------------------|
| [**GetDimensions**](sm5-object-rwbyteaddressbuffer-getdimensions.md)                           | Obtient les dimensions de ressource.       |
| [**InterlockedAdd**](sm5-object-rwbyteaddressbuffer-interlockedadd.md)                         | Ajoute, atomiquement.                   |
| [**InterlockedAnd**](sm5-object-rwbyteaddressbuffer-interlockedand.md)                         | ANDs, atomiquement.                   |
| [**InterlockedCompareExchange**](sm5-object-rwbyteaddressbuffer-interlockedcompareexchange.md) | Compare et échange, de manière atomique. |
| [**InterlockedCompareStore**](sm5-object-rwbyteaddressbuffer-interlockedcomparestore.md)       | Compare et stocke atomiquement.    |
| [**Interlockedexchang**](sm5-object-rwbyteaddressbuffer-interlockedexchange.md)               | Les échanges, de manière atomique.              |
| [**InterlockedMax**](sm5-object-rwbyteaddressbuffer-interlockedmax.md)                         | Recherche le nombre maximal, atomique.          |
| [**InterlockedMin**](sm5-object-rwbyteaddressbuffer-interlockedmin.md)                         | Rechercher le minimum, atomiquement.           |
| [**Interverrouiller**](sm5-object-rwbyteaddressbuffer-interlockedor.md)                           | ORs, atomiquement.                    |
| [**InterlockedXor**](sm5-object-rwbyteaddressbuffer-interlockedxor.md)                         | XORs, atomiquement.                   |
| [**Load**](rwbyteaddressbuffer-load.md)                                                        | Obtient une valeur.                     |
| [**Load2**](rwbyteaddressbuffer-load2.md)                                                      | Obtient deux valeurs.                    |
| [**Load3**](rwbyteaddressbuffer-load3.md)                                                      | Obtient trois valeurs.                  |
| [**Load4**](rwbyteaddressbuffer-load4.md)                                                      | Obtient quatre valeurs.                   |
| [**Store**](sm5-object-rwbyteaddressbuffer-store.md)                                           | Définit une valeur.                     |
| [**Banque**](sm5-object-rwbyteaddressbuffer-store2.md)                                         | Définit deux valeurs.                    |
| [**Store3**](sm5-object-rwbyteaddressbuffer-store3.md)                                         | Définit trois valeurs.                  |
| [**Store4**](sm5-object-rwbyteaddressbuffer-store4.md)                                         | Définit quatre valeurs.                   |



 

Les objets RWByteAddressBuffer peuvent être précédés de la classe de stockage **globallycoherent**. Cette classe de stockage entraîne des barrières et des synchronisations de la mémoire pour vider les données sur l’ensemble du GPU, de telle sorte que les autres groupes puissent voir les écritures. Sans ce spécificateur, une barrière de mémoire ou une synchronisation vide un UAV uniquement dans le groupe actuel.

Le format UAV lié à cette ressource doit être créé avec le format DXGI \_ \_ R32 sans \_ type.

Le UAV lié à cette ressource doit avoir été créé avec l' [**\_ indicateur UAV de mémoire tampon d3d11 \_ \_ \_ RAW**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_buffer_uav_flag).

Vous pouvez utiliser le type d’objet **RWByteAddressBuffer** quand vous travaillez avec des mémoires tampons brutes. Pour plus d’informations sur l’affichage brut des tampons, consultez [affichages bruts de mémoires tampons](/windows/desktop/direct3d11/overviews-direct3d-11-resources-intro).

## <a name="minimum-shader-model"></a>Modèle de nuanceur minimal

Cet objet est pris en charge dans les modèles de nuanceur suivants.



| Modèle de nuanceur                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      | Prise en charge |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------|
| Nuanceur [modèle 5](d3d11-graphics-reference-sm5.md) et modèles de nuanceur plus élevés [nuanceur de modèle 4](dx-graphics-hlsl-sm4.md) (disponible par le biais de l’API Direct3D 11 en utilisant le niveau de fonctionnalité 10,0 ou 10,1 ([**\_ \_ niveau de fonctionnalité D3D**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_feature_level) \_ 10 \_ X) sur les appareils qui prennent en charge les nuanceurs de calcul. Pour plus d’informations sur la prise en charge du nuanceur de calcul sur du matériel de niveau inférieur, consultez [nuanceurs de calcul sur du matériel de niveau inférieur](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-compute-shaders).)<br/> | Oui       |



 

Cet objet est pris en charge pour les types de nuanceurs suivants :



| Sommet | Forme | Domain | Géométrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Objets Shader Model 5](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

