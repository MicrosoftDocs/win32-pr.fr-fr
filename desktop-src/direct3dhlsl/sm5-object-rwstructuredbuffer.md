---
title: RWStructuredBuffer
description: Mémoire tampon de lecture/écriture qui peut accepter un type T qui est une structure.
ms.assetid: 8dd93b81-135d-4f28-898f-38510dc39af1
keywords:
- HLSL RWStructuredBuffer
topic_type:
- apiref
api_name:
- RWStructuredBuffer
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f921ca795e761522828de14ede61894defe44f6e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127292659"
---
# <a name="rwstructuredbuffer"></a>RWStructuredBuffer

Mémoire tampon de lecture/écriture qui peut accepter un type T qui est une structure.



| Méthode                                                                     | Description                             |
|----------------------------------------------------------------------------|-----------------------------------------|
| [**DecrementCounter**](sm5-object-rwstructuredbuffer-decrementcounter.md) | Décrémente le compteur masqué de l’objet. |
| [**GetDimensions**](sm5-object-rwstructuredbuffer-getdimensions.md)       | Obtient les dimensions de ressource.           |
| [**IncrementCounter**](sm5-object-rwstructuredbuffer-incrementcounter.md) | Incrémente le compteur masqué de l’objet. |
| [**Chargera**](rwstructuredbuffer-load.md)                                    | Lit les données de la mémoire tampon.                      |
| [**Opérateur\[\]**](sm5-object-rwstructuredbuffer-operatorindex.md)        | Retourne une variable de ressource.            |



 

Une variable de ressource peut également être passée dans une opération non ordonnée ou verrouillée.

Les objets RWStructuredBuffer peuvent être précédés de la classe de stockage **globallycoherent**. Cette classe de stockage entraîne des barrières et des synchronisations de la mémoire pour vider les données sur l’ensemble du GPU, de telle sorte que les autres groupes puissent voir les écritures. Sans ce spécificateur, une barrière de mémoire ou une synchronisation vide uniquement un UAV dans le groupe actuel.

Le format UAV lié à cette ressource doit être créé avec le format DXGI \_ \_ inconnu.

Pour en savoir plus sur les [mémoires tampons structurées](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-resources), consultez la documentation de présentation.

## <a name="minimum-shader-model"></a>Modèle de nuanceur minimal

Cet objet est pris en charge dans les modèles de nuanceur suivants.



| Modèle de nuanceur                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      | Prise en charge |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------|
| Nuanceur [modèle 5](d3d11-graphics-reference-sm5.md) et modèles de nuanceur plus élevés [nuanceur de modèle 4](dx-graphics-hlsl-sm4.md) (disponible par le biais de l’API Direct3D 11 en utilisant le niveau de fonctionnalité 10,0 ou 10,1 ([**\_ \_ niveau de fonctionnalité D3D**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_feature_level) \_ 10 \_ X) sur les appareils qui prennent en charge les nuanceurs de calcul. Pour plus d’informations sur la prise en charge du nuanceur de calcul sur du matériel de niveau inférieur, consultez [nuanceurs de calcul sur du matériel de niveau inférieur](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-compute-shaders).)<br/> | Oui       |



 

Cet objet est pris en charge pour les types de nuanceurs suivants :



| Sommet | Forme | Domain | Géométrie | Pixel | Calcul |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Objets Shader Model 5](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

