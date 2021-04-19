---
title: Attribut WM/WMCollectionGroupID
description: L’attribut WM/WMCollectionGroupID est un GUID identifiant le groupe contenant la collection à laquelle l’élément appartient.
ms.assetid: 5383fb12-fc16-474e-b9a0-c1e69b86a057
keywords:
- Attribut WM/WMCollectionGroupID lecteur Windows Media
topic_type:
- apiref
api_name:
- WM/WMCollectionGroupID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c681ad7049520ed77de3ebb385e74efcfef66b4c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539726"
---
# <a name="wmwmcollectiongroupid-attribute"></a>Attribut WM/WMCollectionGroupID

L’attribut **WM/WMCollectionGroupID** est un GUID identifiant le groupe contenant la collection à laquelle l’élément appartient.

## <a name="applies-to"></a>S'applique à

-   [Éléments audio](audio-item-attributes.md)
-   [Sélections de CD](cd-playlist-attributes.md)
-   [Pistes de CD](cd-track-attributes.md)
-   [Attributs de fichiers Windows Media couramment utilisés](commonly-used-windows-media-file-attributes.md)

## <a name="remarks"></a>Notes

Cet attribut est stocké à la fois dans la bibliothèque (ou le cache) et dans le fichier multimédia numérique.

**WMCollectionGroupID** est un alias pour cet attribut.

La constante du kit de développement logiciel (SDK) du format Windows Media pour cet attribut est g \_ wszWMCollectionGroupID.

Pour déterminer si vous pouvez modifier la valeur de cet attribut, utilisez la méthode [Media. isReadOnlyItem](media-isreadonlyitem.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------|
| Version<br/> | Lecteur Windows Media série 9 ou version ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Référence d’attribut**](attribute-reference.md)
</dt> </dl>

 

 





