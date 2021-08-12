---
description: Le clip epecifies une source de média.
ms.assetid: 40323e64-ad5f-4646-bad7-2a4e7d0ddcf6
title: Élément clip
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b94ffdbd3d9b49d961cdefdd64de9a212858c5da4859c3beddb77db0ab732d4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118655513"
---
# <a name="clip-element"></a>Élément clip

> [!Note]  
> \[Action déconseillée. Cette API peut être supprimée des futures versions de Windows.\]

 

`clip`Epecifies une source de média.

## <a name="attributes"></a>Attributs

[**CLSID**](clsid-attribute.md), [**cadence**](framerate-attribute.md), [**Lock**](lock-attribute.md), [**mlength**](mlength-attribute.md), [**mstart**](mstart-attribute.md), [**mstop**](mstop-attribute.md), [**muet**](mute-attribute.md), [**src**](src-attribute.md), [**Start**](start-attribute.md), [**Stop**](stop-attribute.md), [**Stream**](stream-attribute.md), [**stretchmode**](stretchmode-attribute.md), [**UserData**](userdata-attribute.md), [**userid**](userid-attribute.md), [**username**](username-attribute.md)

## <a name="parentchild-information"></a>Informations parent/enfant



| Étiquette | Valeur |
|----------|----------------------------------|
| Parent   | [**track**](track-element.md)   |
| Children | [**résultat**](effect-element.md) |



 

## <a name="remarks"></a>Remarques

L’attribut **CLSID** spécifie le CLSID d’un filtre source à utiliser comme source. Ne spécifiez pas les attributs **src** et **CLSID** dans le même `clip` élément.

Spécifiez au moins un attribut Start-Time (**Start** ou **mstart**) et un attribut Stop-Time (**Stop** ou **mstop**). Si l’un des attributs de démarrage n’est pas spécifié, la valeur par défaut est 0 (le début de la chronologie pour **Start** ou le début de la séquence pour **mstart**). Si l’un des attributs d’arrêt n’est pas spécifié, l’algorithme DES prend une vitesse de lecture normale et calcule l’heure d’arrêt non spécifiée en conséquence. Si les deux temps d’arrêt sont spécifiés, la lecture est plus rapide ou plus lente que la normale, si nécessaire.

Dans l’exemple suivant, la durée de la chronologie est de sept secondes (**Stop** moins **Start**). La vitesse de lecture normale est supposée. par conséquent, l’heure d’arrêt du support est par défaut de 10 secondes (durée plus **mstart**).


```
<clip start="2" stop="9" mstart="3" />
```



Dans l’exemple suivant, l’heure de début du média est définie par défaut sur 0, ce qui force la durée du support à être de 10 secondes. La durée de la chronologie est de cinq secondes, de sorte que le clip est lu à deux fois la vitesse normale.


```
<clip start="5" stop="10" mstop="10" />  
```



Si l’attribut **src** spécifie une image continue, des tentatives de chargement d’une série d’images fixes pour créer une animation. Par exemple, si l’attribut **src** est IMAGE001.BMP, le recherche des IMAGE002.BMP, IMAGE003.BMP, IMAGE004.BMP, etc. En supposant qu’elles existent, elles sont affichées dans l’ordre numérique séquentiel, à la vitesse spécifiée par l’attribut **cadence** .

## <a name="examples"></a>Exemples


```XML
<clip src="sample.avi" start="1:05" stop="1:42.5" mstart="30" />
```



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Éléments XTL](xtl-elements.md)
</dt> </dl>

 

 



