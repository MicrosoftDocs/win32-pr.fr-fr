---
title: Attribut WM/ContentDistributor
description: L’attribut WM/ContentDistributor est le nom du serveur de distribution de l’élément.
ms.assetid: 45f548a4-4059-464c-af93-1ba09e6b8d1e
keywords:
- Lecteur Windows Media de l’attribut WM/ContentDistributor
topic_type:
- apiref
api_name:
- WM/ContentDistributor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 420e3e05a68f89d8e37b8ef95dd1247802442700
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127404402"
---
# <a name="wmcontentdistributor-attribute"></a>Attribut WM/ContentDistributor

L’attribut **WM/ContentDistributor** est le nom du serveur de distribution de l’élément.

## <a name="applies-to"></a>S'applique à

-   [Éléments audio](audio-item-attributes.md)
-   [attributs de fichier multimédia Windows couramment utilisés](commonly-used-windows-media-file-attributes.md)
-   [Sélections](playlist-attributes-ref.md)
-   [Éléments vidéo](video-item-attributes.md)

## <a name="remarks"></a>Notes

Cet attribut est stocké à la fois dans la bibliothèque et dans le fichier multimédia numérique.

**ContentDistributor** est un alias pour cet attribut.

la constante du kit de développement logiciel (SDK) du Format multimédia Windows pour cet attribut est g \_ wszWMContentDistributor.

Pour déterminer si vous pouvez modifier la valeur de cet attribut, utilisez la méthode [Media. isReadOnlyItem](media-isreadonlyitem.md) .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|---------------------------------------------------|
| Version<br/> | Lecteur Windows Media série 9 ou version ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Référence d’attribut**](attribute-reference.md)
</dt> </dl>

 

 





