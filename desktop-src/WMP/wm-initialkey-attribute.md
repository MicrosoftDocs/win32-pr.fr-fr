---
title: Attribut WM/InitialKey
description: L’attribut WM/InitialKey est la clé initiale de la musique.
ms.assetid: 1458f1a2-3d46-4491-8b89-731276d7c024
keywords:
- Attribut WM/InitialKey lecteur Windows Media
topic_type:
- apiref
api_name:
- WM/InitialKey
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89dd4daeabe2971615518b0a3cf37223a4c623c3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106523974"
---
# <a name="wminitialkey-attribute"></a>Attribut WM/InitialKey

L’attribut **WM/InitialKey** est la clé initiale de la musique.

## <a name="applies-to"></a>S'applique à

-   [Éléments audio](audio-item-attributes.md)
-   [Attributs de fichiers Windows Media couramment utilisés](commonly-used-windows-media-file-attributes.md)

## <a name="remarks"></a>Notes

Cet attribut est stocké à la fois dans la bibliothèque et dans le fichier multimédia numérique.

La constante du kit de développement logiciel (SDK) du format Windows Media pour cet attribut est g \_ wszWMInitialKey.

**InitialKey** est un alias pour cet attribut.

Pour déterminer si vous pouvez modifier la valeur de cet attribut, utilisez la méthode [Media. isReadOnlyItem](media-isreadonlyitem.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------|
| Version<br/> | Lecteur Windows Media série 9 ou version ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Référence d’attribut**](attribute-reference.md)
</dt> </dl>

 

 





