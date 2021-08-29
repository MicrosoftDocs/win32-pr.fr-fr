---
title: Attribut WM/SubscriptionContentID
description: L’attribut WM/SubscriptionContentID est l’identificateur de contenu de l’abonnement.
ms.assetid: ef0fe575-3cea-4442-950b-40c60378364b
keywords:
- Lecteur Windows Media de l’attribut WM/SubscriptionContentID
topic_type:
- apiref
api_name:
- WM/SubscriptionContentID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c976ca7bcd9eed8e29e7be3d818a3f8fd5fe5d5904dfa5e058faa55ce06d301
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120000889"
---
# <a name="wmsubscriptioncontentid-attribute"></a>Attribut WM/SubscriptionContentID

L’attribut **WM/SubscriptionContentID** est l’identificateur de contenu de l’abonnement.

## <a name="applies-to"></a>S'applique à

-   [Éléments audio](audio-item-attributes.md)
-   [attributs de fichier multimédia Windows couramment utilisés](commonly-used-windows-media-file-attributes.md)
-   [Éléments vidéo](video-item-attributes.md)

## <a name="remarks"></a>Remarques

Cet attribut est stocké à la fois dans la bibliothèque et dans le fichier multimédia numérique.

**SubscriptionContentID** est un alias pour cet attribut.

la constante du kit de développement logiciel (SDK) du Format multimédia Windows pour cet attribut est g \_ wszWMSubscriptionContentID.

Pour déterminer si vous pouvez modifier la valeur de cet attribut, utilisez la méthode [Media. isReadOnlyItem](media-isreadonlyitem.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------|
| Version<br/> | Lecteur Windows Media série 9 ou version ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Référence d’attribut**](attribute-reference.md)
</dt> </dl>

 

 





