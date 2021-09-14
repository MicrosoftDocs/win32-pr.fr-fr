---
description: L’élément Group définit un groupe, l’objet de niveau supérieur dans une chronologie.
ms.assetid: db2f1fdd-bcb1-4401-91f4-5e167e4da215
title: Group, élément (DirectShow)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31502cef89c8383e935f409d76b9e31ca53a2da1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127195391"
---
# <a name="group-element"></a>Group, élément

> [!Note]  
> \[Déconseillé. Cette API peut être supprimée des futures versions de Windows.\]

 

L’élément **Group** définit un groupe, l’objet de niveau supérieur dans une chronologie.

## <a name="attributes"></a>Attributs

[**bitdepth**](bitdepth-attribute.md), [**mise en mémoire tampon**](buffering-attribute.md), [**fréquence**](framerate-attribute.md)d’images, [**hauteur**](height-attribute.md), [**verrouillage**](lock-attribute.md), [**muet**](mute-attribute.md), [**nom**](name-attribute.md), [**PreviewMode**](previewmode-attribute.md), [**samplingrate**](samplingrate-attribute.md), [**type**](type-attribute.md), [**UserData**](userdata-attribute.md), [**userid**](userid-attribute.md), [**nom d’utilisateur**](username-attribute.md), [**largeur**](width-attribute.md)

## <a name="parentchild-information"></a>Informations parent/enfant



| Étiquette | Valeur |
|----------|----------------------------------------------------------------------------------------------------------|
| Parent   | [**actualité**](timeline-element.md)                                                                     |
| Children | [**composite**](composite-element.md), [**Effect**](effect-element.md), [**Track**](track-element.md) |



 

## <a name="remarks"></a>Notes

Dans un `group` élément, la priorité des couches imbriquées est déterminée implicitement par l’ordre dans lequel elles apparaissent dans l’élément. La première couche a la priorité 0 et les couches suivantes comportent des valeurs de priorité accrues.

## <a name="examples"></a>Exemples


```XML
<group type="video" width="640" height="480" framerate="30"> </group>
```



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Éléments XTL](xtl-elements.md)
</dt> </dl>

 

 



