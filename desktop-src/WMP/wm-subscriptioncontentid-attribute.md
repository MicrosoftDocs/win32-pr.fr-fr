---
title: Attribut WM/SubscriptionContentID
description: L’attribut WM/SubscriptionContentID est l’identificateur de contenu de l’abonnement.
ms.assetid: ef0fe575-3cea-4442-950b-40c60378364b
keywords:
- Attribut WM/SubscriptionContentID lecteur Windows Media
topic_type:
- apiref
api_name:
- WM/SubscriptionContentID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9f10448686e299c20fc1cd44f716b805910e8f5d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540540"
---
# <a name="wmsubscriptioncontentid-attribute"></a>Attribut WM/SubscriptionContentID

L’attribut **WM/SubscriptionContentID** est l’identificateur de contenu de l’abonnement.

## <a name="applies-to"></a>S'applique à

-   [Éléments audio](audio-item-attributes.md)
-   [Attributs de fichiers Windows Media couramment utilisés](commonly-used-windows-media-file-attributes.md)
-   [Éléments vidéo](video-item-attributes.md)

## <a name="remarks"></a>Notes

Cet attribut est stocké à la fois dans la bibliothèque et dans le fichier multimédia numérique.

**SubscriptionContentID** est un alias pour cet attribut.

La constante du kit de développement logiciel (SDK) du format Windows Media pour cet attribut est g \_ wszWMSubscriptionContentID.

Pour déterminer si vous pouvez modifier la valeur de cet attribut, utilisez la méthode [Media. isReadOnlyItem](media-isreadonlyitem.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------|
| Version<br/> | Lecteur Windows Media série 9 ou version ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Référence d’attribut**](attribute-reference.md)
</dt> </dl>

 

 





