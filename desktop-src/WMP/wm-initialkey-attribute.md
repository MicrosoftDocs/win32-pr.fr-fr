---
title: Attribut WM/InitialKey
description: L’attribut WM/InitialKey est la clé initiale de la musique.
ms.assetid: 1458f1a2-3d46-4491-8b89-731276d7c024
keywords:
- Lecteur Windows Media de l’attribut WM/InitialKey
topic_type:
- apiref
api_name:
- WM/InitialKey
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89dd4daeabe2971615518b0a3cf37223a4c623c3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127404387"
---
# <a name="wminitialkey-attribute"></a>Attribut WM/InitialKey

L’attribut **WM/InitialKey** est la clé initiale de la musique.

## <a name="applies-to"></a>S'applique à

-   [Éléments audio](audio-item-attributes.md)
-   [attributs de fichier multimédia Windows couramment utilisés](commonly-used-windows-media-file-attributes.md)

## <a name="remarks"></a>Notes

Cet attribut est stocké à la fois dans la bibliothèque et dans le fichier multimédia numérique.

la constante du kit de développement logiciel (SDK) du Format multimédia Windows pour cet attribut est g \_ wszWMInitialKey.

**InitialKey** est un alias pour cet attribut.

Pour déterminer si vous pouvez modifier la valeur de cet attribut, utilisez la méthode [Media. isReadOnlyItem](media-isreadonlyitem.md) .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|---------------------------------------------------|
| Version<br/> | Lecteur Windows Media série 9 ou version ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Référence d’attribut**](attribute-reference.md)
</dt> </dl>

 

 





