---
title: Attribut WM/UniqueFileIdentifier
description: L’attribut WM/UniqueFileIdentifier est une chaîne qui identifie de façon unique l’élément.
ms.assetid: 8196fc38-05dc-4c9e-98cb-1e160ce28a9a
keywords:
- Lecteur Windows Media de l’attribut WM/UniqueFileIdentifier
topic_type:
- apiref
api_name:
- WM/UniqueFileIdentifier
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d0a4297f299f6e7df64088066b3137d844a0c78
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127216892"
---
# <a name="wmuniquefileidentifier-attribute"></a>Attribut WM/UniqueFileIdentifier

L’attribut **WM/UniqueFileIdentifier** est une chaîne qui identifie de façon unique l’élément.

## <a name="applies-to"></a>S'applique à

-   [Éléments audio](audio-item-attributes.md)
-   [Sélections de CD](cd-playlist-attributes.md)
-   [Pistes de CD](cd-track-attributes.md)
-   [attributs de fichier multimédia Windows couramment utilisés](commonly-used-windows-media-file-attributes.md)

## <a name="remarks"></a>Notes

Cet attribut est stocké à la fois dans la bibliothèque (ou le cache) et dans le fichier multimédia numérique.

**UniqueFileIdentifier** est un alias pour cet attribut.

la constante du kit de développement logiciel (SDK) du Format multimédia Windows pour cet attribut est g \_ wszWMUniqueFileIdentifier.

Pour déterminer si vous pouvez modifier la valeur de cet attribut, utilisez la méthode [Media. isReadOnlyItem](media-isreadonlyitem.md) .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|---------------------------------------------------|
| Version<br/> | Lecteur Windows Media série 9 ou version ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Référence d’attribut**](attribute-reference.md)
</dt> </dl>

 

 





