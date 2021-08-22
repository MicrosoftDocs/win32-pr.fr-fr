---
title: Attribut WM/MCDI
description: L’attribut WM/MCDI est l’identificateur de CD de musique du CD à partir duquel le fichier ou la piste a été copié.
ms.assetid: f0bec14d-416c-477f-98df-dece0bf85ea4
keywords:
- Lecteur Windows Media de l’attribut WM/MCDI
topic_type:
- apiref
api_name:
- WM/MCDI
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 738ce8d5af7351b30fd986323db01d4dd335fa7307d2da88e48f4b2456eba1f1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119053847"
---
# <a name="wmmcdi-attribute"></a>Attribut WM/MCDI

L’attribut **WM/MCDI** est l’identificateur de CD de musique du CD à partir duquel le fichier ou la piste a été copié.

## <a name="applies-to"></a>S'applique à

-   [Éléments audio](audio-item-attributes.md)
-   [Pistes de CD](cd-track-attributes.md)
-   [attributs de fichier multimédia Windows couramment utilisés](commonly-used-windows-media-file-attributes.md)

## <a name="remarks"></a>Remarques

Cet attribut est stocké à la fois dans la bibliothèque (ou le cache) et dans le fichier multimédia numérique.

**TOC** est un alias pour cet attribut.

la constante du kit de développement logiciel (SDK) du Format multimédia Windows pour cet attribut est g \_ wszWMMCDI.

Pour déterminer si vous pouvez modifier la valeur de cet attribut, utilisez la méthode [Media. isReadOnlyItem](media-isreadonlyitem.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------|
| Version<br/> | Lecteur Windows Media série 9 ou version ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Référence d’attribut**](attribute-reference.md)
</dt> </dl>

 

 





