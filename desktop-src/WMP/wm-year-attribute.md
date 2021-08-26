---
title: Attribut WM/Year
description: L’attribut WM/Year est l’année de publication du contenu.
ms.assetid: b64e37f1-6f12-43a6-8a66-7d61b470853c
keywords:
- attribut WM/Year Lecteur Windows Media
topic_type:
- apiref
api_name:
- WM/Year
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bec0b76fbf54a53a7ae09728fe34d75fff5c232de9ecfa13a77edaa97cd37e05
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119900189"
---
# <a name="wmyear-attribute"></a>Attribut WM/Year

L’attribut **WM/Year** est l’année de publication du contenu.

## <a name="applies-to"></a>S'applique à

-   [Éléments audio](audio-item-attributes.md)
-   [attributs de fichier multimédia Windows couramment utilisés](commonly-used-windows-media-file-attributes.md)

## <a name="remarks"></a>Remarques

Cet attribut est stocké uniquement dans le fichier multimédia numérique.

Pour déterminer si vous pouvez modifier la valeur de cet attribut, utilisez la méthode [Media. isReadOnlyItem](media-isreadonlyitem.md) .

Cet attribut ne doit pas être utilisé dans le cadre d’une condition de requête. Elle est dérivée d’un autre attribut et ne peut pas être interrogée directement dans une collection de supports.

la constante du kit de développement logiciel (SDK) du Format multimédia Windows pour cet attribut est g \_ wszWMYear.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|-----------------------------------------------------------------------------------------------------------|
| Version<br/> | Lecteur Windows Media série 9 Lecteur Windows Media 10 ou version ultérieure ne prend pas en charge cet attribut<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Référence d’attribut**](attribute-reference.md)
</dt> </dl>

 

 





