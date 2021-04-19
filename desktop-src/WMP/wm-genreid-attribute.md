---
title: Attribut WM/GenreID
description: L’attribut WM/GenreID est un identificateur de genre conforme à la balise TCON dans ID3v2.
ms.assetid: 9b68f9be-1f02-4b14-b052-90657b8800e3
keywords:
- Attribut WM/GenreID lecteur Windows Media
topic_type:
- apiref
api_name:
- WM/GenreID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d31e54805f778a51f345c84654056391ec4052e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106530486"
---
# <a name="wmgenreid-attribute"></a>Attribut WM/GenreID

L’attribut **WM/GenreID** est un identificateur de genre conforme à la balise TCON dans ID3v2.

## <a name="applies-to"></a>S'applique à

-   [Éléments audio](audio-item-attributes.md)
-   [Attributs de fichiers Windows Media couramment utilisés](commonly-used-windows-media-file-attributes.md)

## <a name="remarks"></a>Notes

Cet attribut est stocké uniquement dans le fichier multimédia numérique.

ID3 version 2 est une convention d’étiquetage conçue à l’origine pour le format MP3. Pour plus d’informations, consultez le [site Web de l’organisation ID3](https://id3.org/).

La constante du kit de développement logiciel (SDK) du format Windows Media pour cet attribut est g \_ wszGenreID.

Pour déterminer si vous pouvez modifier la valeur de cet attribut, utilisez la méthode [Media. isReadOnlyItem](media-isreadonlyitem.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|-----------------------------------------------------------------------------------------------------------|
| Version<br/> | Le lecteur Windows Media série 9 Windows Media Player 10 ou version ultérieure ne prend pas en charge cet attribut<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Référence d’attribut**](attribute-reference.md)
</dt> </dl>

 

 





