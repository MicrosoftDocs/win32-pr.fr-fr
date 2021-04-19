---
title: NomBibliothèque (attribut)
description: L’attribut NomBibliothèque est le nom de la bibliothèque à laquelle l’élément appartient.
ms.assetid: 70ce2de1-6c7b-427a-ba48-a9f69bacd015
keywords:
- L’attribut NomBibliothèque lecteur Windows Media
topic_type:
- apiref
api_name:
- LibraryName
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 263023c9881e109efe77ec30c1e37091200c051b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106520913"
---
# <a name="libraryname-attribute"></a>NomBibliothèque (attribut)

L’attribut NomBibliothèque est le nom de la bibliothèque à laquelle l’élément appartient.

## <a name="applies-to"></a>S'applique à

-   [**Éléments audio**](audio-item-attributes.md)
-   [**Éléments de photo**](photo-item-attributes.md)
-   [**Éléments de sélection**](playlist-attributes-ref.md)
-   [**Éléments vidéo**](video-item-attributes.md)

## <a name="remarks"></a>Notes

Un élément multimédia peut appartenir à la bibliothèque locale de l’utilisateur actuel ou il peut appartenir à une bibliothèque qui a été mise à la disposition d’un autre utilisateur sur un réseau privé.

La valeur de cet attribut est la même que la valeur retournée par la méthode [**IWMPLibrary :: obten \_ Name**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmplibrary-get_name) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------|
| Version<br/> | Lecteur Windows Media 12<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Référence d’attribut**](attribute-reference.md)
</dt> </dl>

 

 





