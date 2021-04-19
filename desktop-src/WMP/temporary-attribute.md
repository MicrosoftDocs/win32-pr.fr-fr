---
title: Attribut temporaire
description: L’attribut Temporary spécifie si une sélection est temporaire.
ms.assetid: 0d967a70-97d1-4918-8068-fe2868ab41d2
keywords:
- Attribut temporaire lecteur Windows Media
topic_type:
- apiref
api_name:
- Temporary
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a70ae8f3ae06ae44077cce3d8fa3fdf67dc853eb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542245"
---
# <a name="temporary-attribute"></a>Attribut temporaire

L’attribut **Temporary** spécifie si une sélection est temporaire.

**Remarques**

Si vous avez récupéré une sélection à partir de la bibliothèque, les modifications apportées à la sélection sont reflétées dans la bibliothèque de l’utilisateur. Pour éviter cela, appelez [IWMPPlaylist :: setItemInfo](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpplaylist-setiteminfo) en passant le nom d’attribut « Temporary » et la valeur « true ». Cela convertit votre instance de playlist en sélection temporaire, qui peut être modifiée en toute sécurité sans modifier la sélection d’origine.

**S’applique à**

-   [Sélections](playlist-attributes-ref.md)

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------|
| Version<br/> | Lecteur Windows Media 11<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Référence d’attribut**](attribute-reference.md)
</dt> </dl>

 

 





