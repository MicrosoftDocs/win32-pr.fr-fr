---
title: Attribut WM/ContentDistributorType
description: L’attribut WM/ContentDistributorType est le type du serveur de distribution de l’élément.
ms.assetid: 3be711a2-51b0-4b61-8009-f97394207b1c
keywords:
- Lecteur Windows Media de l’attribut WM/ContentDistributorType
topic_type:
- apiref
api_name:
- WM/ContentDistributorType
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1c9d44ad64cf860f1ad70827b51dd2cda28717fd6531d1e570a52a1ac070304
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119862119"
---
# <a name="wmcontentdistributortype-attribute"></a>Attribut WM/ContentDistributorType

L’attribut **WM/ContentDistributorType** est le type du serveur de distribution de l’élément.

## <a name="applies-to"></a>S'applique à

-   [Éléments audio](audio-item-attributes.md)
-   [attributs de fichier multimédia Windows couramment utilisés](commonly-used-windows-media-file-attributes.md)
-   [Sélections](playlist-attributes-ref.md)
-   [Éléments vidéo](video-item-attributes.md)

## <a name="remarks"></a>Remarques

La valeur de cet attribut sera « List » ou « radio ». Cet attribut est stocké à la fois dans la bibliothèque et dans le fichier multimédia numérique.

**ContentDistributorType** est un alias pour cet attribut.

la constante du kit de développement logiciel (SDK) du Format multimédia Windows pour cet attribut est g \_ wszWMContentDistributorType.

Pour déterminer si vous pouvez modifier la valeur de cet attribut, utilisez la méthode [Media. isReadOnlyItem](media-isreadonlyitem.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------|
| Version<br/> | Lecteur Windows Media 11<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Référence d’attribut**](attribute-reference.md)
</dt> </dl>

 

 





