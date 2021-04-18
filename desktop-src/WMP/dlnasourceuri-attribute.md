---
title: Attribut DLNASourceURI
description: L’attribut DLNASourceURI est l’URI (Universal Resource Identifier) de l’élément.
ms.assetid: 323c897b-9b76-44f7-9313-c51595589583
keywords:
- Attribut DLNASourceURI lecteur Windows Media
topic_type:
- apiref
api_name:
- DLNASourceURI
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 96ebe21a39a67dec9356c5dd5360efb48f4ef029
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540419"
---
# <a name="dlnasourceuri-attribute"></a>Attribut DLNASourceURI

L’attribut **DLNASourceURI** est l’URI (Universal Resource Identifier) de l’élément.

## <a name="applies-to"></a>S'applique à

-   [**Éléments audio**](audio-item-attributes.md)
-   [**Autres éléments**](other-item-attributes.md)
-   [**Éléments de photo**](photo-item-attributes.md)
-   [**Éléments de sélection**](playlist-attributes-ref.md)
-   [**Éléments vidéo**](video-item-attributes.md)

## <a name="remarks"></a>Notes

Si l’élément se trouve dans la bibliothèque locale de l’utilisateur actuel, cet attribut, l’attribut [**SourceURL**](sourceurl-attribute.md) et la valeur retournée par [**IWMPMedia :: \_ SourceURL**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpmedia-get_sourceurl) sont tous identiques.

Si l’élément ne se trouve pas dans la bibliothèque locale de l’utilisateur actuel, mais appartient à une bibliothèque distante, cet attribut est un identificateur de la forme DLNA-playsingle://*xxx*.

Vous pouvez transmettre un URI DLNA-playsingle à la méthode [**IWMPCore3 :: newMedia**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcore3-newmedia) pour obtenir une interface [**IWMPMedia**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmedia) qui vous permet d’afficher les métadonnées de l’élément multimédia et éventuellement de modifier l’évaluation de l’étoile de l’élément multimédia. Notez, toutefois, que l’URI DLNA-playsingle doit être destiné à un service d’annuaire de contenu (CDS) déjà découvert par le lecteur Windows Media. La méthode **newMedia** ne lance pas la découverte UPnP et ne recherche pas les CDs.

Vous pouvez modifier l’évaluation de l’étoile d’un élément multimédia dans une bibliothèque distante uniquement si la bibliothèque distante prend en charge l’opération de modification. Les bibliothèques distantes hébergées sur un ordinateur exécutant Windows 7 prennent en charge l’opération de modification. Les bibliothèques distantes hébergées sur un ordinateur exécutant un système d’exploitation Windows antérieur à Windows 7 ne prennent pas en charge l’opération de modification.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------|
| Version<br/> | Lecteur Windows Media 12<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Référence d’attribut**](attribute-reference.md)
</dt> </dl>

 

 





