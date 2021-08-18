---
title: Attribut Duration
description: L’attribut duration correspond à la durée d’exécution de l’élément, en secondes.
ms.assetid: 0a59a7b6-4536-4197-9f4a-1877ef42f828
keywords:
- Lecteur Windows Media de l’attribut Duration
topic_type:
- apiref
api_name:
- Duration
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a4136f6abc72be2bda03873bf8d9ecfa74076c3fdb0b46c5c218e937283da26a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118996939"
---
# <a name="duration-attribute"></a>Attribut Duration

L’attribut **Duration** correspond à la durée d’exécution de l’élément, en secondes.

## <a name="applies-to"></a>S'applique à

-   [Éléments audio](audio-item-attributes.md)
-   [fichiers multimédias Windows couramment utilisés](commonly-used-windows-media-file-attributes.md)
-   [Autres éléments](other-item-attributes.md)
-   [Éléments vidéo](video-item-attributes.md)

## <a name="remarks"></a>Remarques

Cet attribut est stocké à la fois dans la bibliothèque et dans le fichier multimédia numérique.

la constante du kit de développement logiciel (SDK) du Format multimédia Windows pour cet attribut est g \_ wszWMDuration.

Pour déterminer si vous pouvez modifier la valeur de cet attribut, utilisez la méthode [Media. isReadOnlyItem](media-isreadonlyitem.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------|
| Version<br/> | Lecteur Windows Media série 9 ou version ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Référence d’attribut**](attribute-reference.md)
</dt> </dl>

 

 





