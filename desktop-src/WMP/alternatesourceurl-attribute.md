---
title: Attribut AlternateSourceURL
description: L’attribut AlternateSourceURL est un localisateur de ressources uniforme pour l’élément multimédia qui sert d’alternative aux attributs DLNASourceURI et SourceURL.
ms.assetid: 2be88d9b-4fd8-4e70-9a4d-114a2bf8b23c
keywords:
- Lecteur Windows Media de l’attribut AlternateSourceURL
topic_type:
- apiref
api_name:
- AlternateSourceURL Attribute
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 765c7a3945224e82a0112c0f4dd7249e4340ec13e0d78adbd59039d25f234aaf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119055237"
---
# <a name="alternatesourceurl-attribute"></a>Attribut AlternateSourceURL

L’attribut **AlternateSourceURL** est un localisateur de ressources uniforme pour l’élément multimédia qui sert d’alternative aux attributs [**DLNASourceURI**](dlnasourceuri-attribute.md) et [**SourceURL**](sourceurl-attribute.md) .

## <a name="applies-to"></a>S'applique à

-   [**Éléments audio**](audio-item-attributes.md)
-   [**Éléments de photo**](photo-item-attributes.md)
-   [**Éléments de sélection**](playlist-attributes-ref.md)
-   [**Éléments vidéo**](video-item-attributes.md)

## <a name="remarks"></a>Remarques

Cet attribut n’est pas disponible pour les éléments multimédias dans la bibliothèque locale de l’utilisateur actuel. Elle est disponible uniquement pour les éléments multimédias appartenant à une bibliothèque distante ; autrement dit, une bibliothèque qui a été mise à la disposition d’un autre utilisateur sur le réseau privé. Pour déterminer si une bibliothèque multimédia est distante, appelez [**IWMPLibrary :: obtenir le \_ type**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmplibrary-get_type).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------|
| Version<br/> | Lecteur Windows Media 12<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Référence d’attribut**](attribute-reference.md)
</dt> </dl>

 

 





