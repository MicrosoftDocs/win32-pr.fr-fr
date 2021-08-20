---
description: Spécifie si le codec doit utiliser le filtre de déblocage en boucle lors de l’encodage.
ms.assetid: 395a356a-5f58-46b4-b2ff-47f98106f487
title: MFPKEY_LOOPFILTER, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd157f6f473a40107d4a9a0958407795762df555946f08c030cc4f9ce4f36417
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117689895"
---
# <a name="mfpkey_loopfilter-property"></a>MFPKEY \_ propriété LOOPFILTER

Spécifie si le codec doit utiliser le filtre de déblocage en boucle lors de l’encodage.

## <a name="constant-for-ipropertybag"></a>Constante pour IPropertyBag

\_wszWMVCLoopFilter g

## <a name="data-type"></a>Type de données

VT \_ bool

## <a name="remarks"></a>Remarques

Le filtre en boucle est une méthode de déblocage appliquée lors de l’encodage et du décodage, afin de réduire les artefacts de blocage au moment de l’encodage (« dans la boucle ») afin que les futurs frames P et B-frames ne les transmettent pas en avant.

L’application du filtre en boucle a pour effet que les bords des blocs de macros dans les trames vidéo de sortie sont moins perceptibles. En même temps, l’image peut devenir plus douce en apparence.

Bien que le filtre en boucle puisse entraîner une réduction des détails de l’image dans certains frames, la qualité vidéo globale sera avantageuse. Le plus grand inconvénient de l’utilisation du filtrage en boucle est le coût supplémentaire de décodage des performances.

## <a name="requirements"></a>Conditions requises



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>                                             |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                    |
| En-tête<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés de la Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 




