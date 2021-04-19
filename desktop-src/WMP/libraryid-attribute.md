---
title: Id_bibliothèque (attribut)
description: L’attribut Id_bibliothèque est l’identificateur de la bibliothèque à laquelle l’élément appartient.
ms.assetid: 680d9374-8729-4258-8672-b4b93b65e20a
keywords:
- Attribut Id_bibliothèque lecteur Windows Media
topic_type:
- apiref
api_name:
- LibraryID Attribute
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 47ae9e5ad097bc188b8de1e76a09448c57aa9b83
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106545924"
---
# <a name="libraryid-attribute"></a>Id_bibliothèque (attribut)

L’attribut **ID_bibliothèque** est l’identificateur de la bibliothèque à laquelle l’élément appartient.

## <a name="applies-to"></a>S'applique à

-   [**Éléments audio**](audio-item-attributes.md)
-   [**Éléments de photo**](photo-item-attributes.md)
-   [**Éléments de sélection**](playlist-attributes-ref.md)
-   [**Éléments vidéo**](video-item-attributes.md)

## <a name="remarks"></a>Notes

Un élément multimédia peut appartenir à la bibliothèque locale de l’utilisateur actuel ou il peut appartenir à une bibliothèque qui a été mise à la disposition d’un autre utilisateur sur le réseau local ou sur Internet.

La valeur de cet attribut est la même que la valeur retournée par la méthode [**IWMPLibrary2 :: getItemInfo**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmplibrary-get_name) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------|
| Version<br/> | Lecteur Windows Media 12<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Référence d’attribut**](attribute-reference.md)
</dt> </dl>

 

 





