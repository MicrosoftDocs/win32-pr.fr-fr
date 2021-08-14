---
title: Id_bibliothèque (attribut)
description: L’attribut Id_bibliothèque est l’identificateur de la bibliothèque à laquelle l’élément appartient.
ms.assetid: 680d9374-8729-4258-8672-b4b93b65e20a
keywords:
- attribut id_bibliothèque Lecteur Windows Media
topic_type:
- apiref
api_name:
- LibraryID Attribute
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a011db4e18509761c232bcf5439e33445128ef77c50945f84662a7b7956f607f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119468219"
---
# <a name="libraryid-attribute"></a>Id_bibliothèque (attribut)

L’attribut **ID_bibliothèque** est l’identificateur de la bibliothèque à laquelle l’élément appartient.

## <a name="applies-to"></a>S'applique à

-   [**Éléments audio**](audio-item-attributes.md)
-   [**Éléments de photo**](photo-item-attributes.md)
-   [**Éléments de sélection**](playlist-attributes-ref.md)
-   [**Éléments vidéo**](video-item-attributes.md)

## <a name="remarks"></a>Remarques

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

 

 





