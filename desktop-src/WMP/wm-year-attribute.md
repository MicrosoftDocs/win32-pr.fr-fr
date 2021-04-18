---
title: Attribut WM/Year
description: L’attribut WM/Year est l’année de publication du contenu.
ms.assetid: b64e37f1-6f12-43a6-8a66-7d61b470853c
keywords:
- Attribut WM/Year lecteur Windows Media
topic_type:
- apiref
api_name:
- WM/Year
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10bf10d4e905e10c74cfaf9986445ce9a68dc9b3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533126"
---
# <a name="wmyear-attribute"></a>Attribut WM/Year

L’attribut **WM/Year** est l’année de publication du contenu.

## <a name="applies-to"></a>S'applique à

-   [Éléments audio](audio-item-attributes.md)
-   [Attributs de fichiers Windows Media couramment utilisés](commonly-used-windows-media-file-attributes.md)

## <a name="remarks"></a>Notes

Cet attribut est stocké uniquement dans le fichier multimédia numérique.

Pour déterminer si vous pouvez modifier la valeur de cet attribut, utilisez la méthode [Media. isReadOnlyItem](media-isreadonlyitem.md) .

Cet attribut ne doit pas être utilisé dans le cadre d’une condition de requête. Elle est dérivée d’un autre attribut et ne peut pas être interrogée directement dans une collection de supports.

La constante du kit de développement logiciel (SDK) du format Windows Media pour cet attribut est g \_ wszWMYear.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|-----------------------------------------------------------------------------------------------------------|
| Version<br/> | Le lecteur Windows Media série 9 Windows Media Player 10 ou version ultérieure ne prend pas en charge cet attribut<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Référence d’attribut**](attribute-reference.md)
</dt> </dl>

 

 





