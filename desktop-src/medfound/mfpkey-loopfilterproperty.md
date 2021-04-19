---
description: Spécifie si le codec doit utiliser le filtre de déblocage en boucle lors de l’encodage.
ms.assetid: 395a356a-5f58-46b4-b2ff-47f98106f487
title: MFPKEY_LOOPFILTER, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1fbb723c4145f9769cc157d5db8eb7893d89b389
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106531883"
---
# <a name="mfpkey_loopfilter-property"></a>MFPKEY \_ propriété LOOPFILTER

Spécifie si le codec doit utiliser le filtre de déblocage en boucle lors de l’encodage.

## <a name="constant-for-ipropertybag"></a>Constante pour IPropertyBag

\_wszWMVCLoopFilter g

## <a name="data-type"></a>Type de données

VT \_ bool

## <a name="remarks"></a>Notes

Le filtre en boucle est une méthode de déblocage appliquée lors de l’encodage et du décodage, afin de réduire les artefacts de blocage au moment de l’encodage (« dans la boucle ») afin que les futurs frames P et B-frames ne les transmettent pas en avant.

L’application du filtre en boucle a pour effet que les bords des blocs de macros dans les trames vidéo de sortie sont moins perceptibles. En même temps, l’image peut devenir plus douce en apparence.

Bien que le filtre en boucle puisse entraîner une réduction des détails de l’image dans certains frames, la qualité vidéo globale sera avantageuse. Le plus grand inconvénient de l’utilisation du filtrage en boucle est le coût supplémentaire de décodage des performances.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows XP uniquement\]<br/>                                             |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                    |
| En-tête<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés de la Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 




