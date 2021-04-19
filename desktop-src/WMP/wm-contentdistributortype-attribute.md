---
title: Attribut WM/ContentDistributorType
description: L’attribut WM/ContentDistributorType est le type du serveur de distribution de l’élément.
ms.assetid: 3be711a2-51b0-4b61-8009-f97394207b1c
keywords:
- Attribut WM/ContentDistributorType lecteur Windows Media
topic_type:
- apiref
api_name:
- WM/ContentDistributorType
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 855deecf09759edb3e0f61c16f8b5d4692171fec
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528482"
---
# <a name="wmcontentdistributortype-attribute"></a>Attribut WM/ContentDistributorType

L’attribut **WM/ContentDistributorType** est le type du serveur de distribution de l’élément.

## <a name="applies-to"></a>S'applique à

-   [Éléments audio](audio-item-attributes.md)
-   [Attributs de fichiers Windows Media couramment utilisés](commonly-used-windows-media-file-attributes.md)
-   [Sélections](playlist-attributes-ref.md)
-   [Éléments vidéo](video-item-attributes.md)

## <a name="remarks"></a>Notes

La valeur de cet attribut sera « List » ou « radio ». Cet attribut est stocké à la fois dans la bibliothèque et dans le fichier multimédia numérique.

**ContentDistributorType** est un alias pour cet attribut.

La constante du kit de développement logiciel (SDK) du format Windows Media pour cet attribut est g \_ wszWMContentDistributorType.

Pour déterminer si vous pouvez modifier la valeur de cet attribut, utilisez la méthode [Media. isReadOnlyItem](media-isreadonlyitem.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------|
| Version<br/> | Lecteur Windows Media 11<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Référence d’attribut**](attribute-reference.md)
</dt> </dl>

 

 





