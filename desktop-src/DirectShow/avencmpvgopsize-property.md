---
description: Spécifie le nombre maximal d’images d’un en-tête de groupe d’images (GOP) à l’en-tête de GOP suivant.
ms.assetid: 90433df4-5a96-4bc2-a780-93306abcb0a4
title: Propriété AVEncMPVGOPSize (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c8907d0992153039b1af9a9a0e82ee5782b525d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104033518"
---
# <a name="avencmpvgopsize-property"></a>Propriété AVEncMPVGOPSize

Spécifie le nombre maximal d’images d’un en-tête de groupe d’images (GOP) à l’en-tête de GOP suivant.

Cette propriété est en lecture/écriture.

## <a name="data-type"></a>Type de données

**UInt32** (**VT \_ UI4**)

## <a name="property-guid"></a>Guid de propriété

**CODECAPI \_ AVEncMPVGOPSize**

## <a name="property-value"></a>Valeur de la propriété

Les encodeurs peuvent implémenter cette propriété en tant que jeu énuméré ou en tant que plage linéaire.

## <a name="remarks"></a>Notes

Définissez cette propriété avant de démarrer un enregistrement.

**S’applique à Windows 8 :** La taille de groupe d’images encodée doit être inférieure ou égale au nombre spécifié par le biais de cette propriété, afin de conserver le même modèle de frame B défini par [CODECAPI \_ AVEncMPVDefaultBPictureCount](avencmpvdefaultbpicturecount-property.md) dans le groupe d’images ou en raison de la modification de la scène. Par exemple, lorsque le nombre de frames B dans un groupe d’images est spécifié sur 2, et que la taille du groupe d’images est de 11, l’encodeur produit une taille de groupe d’images de 10 images ou moins. Lorsque la modification de la scène se produit au milieu d’un groupe d’images, l’encodeur peut également insérer une image clé et produire un groupe d’images plus petit.

La taille de GOP 0 est dépendante de l’encodeur et les encodeurs peuvent choisir différentes tailles de groupe d’images en fonction de leur implémentation/qualité/performance. Les encodeurs doivent honorer la taille de groupe d’images et tronquer les frames B dans ce cas.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de bureau Windows 2000 professionnel- \[ \| applications UWP\]<br/>                     |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows 2000 Server \[ apps- \| applications UWP\]<br/>                           |
| En-tête<br/>                   | <dl> <dt>Codecapi. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés de l’API codec](codec-api-properties.md)
</dt> <dt>

[**Interface ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




