---
description: Contient une alternative à la reconnaissance pour un InkWord. Les alternatives sont triées en fonction de la confiance du module de reconnaissance dans l’autre, avec la priorité la plus élevée.
ms.assetid: 6ec78ac9-c10c-4227-bead-5ddfc48ce27e
title: Élément Alternate (Wingdi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55dfb629aadea988a6aeec1cba1020c8ab47c994
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127196348"
---
# <a name="alternate-element"></a>Élément de remplacement

Contient une alternative à la reconnaissance pour un [**InkWord**](inkword-element.md). Les alternatives sont triées en fonction de la confiance du module de reconnaissance dans l’autre, avec la priorité la plus élevée.

## <a name="definition"></a>Définition

``` syntax
<xs:element name="Alternate" type="xs:string" minOccurs="0" maxOccurs="unbounded" />
```

## <a name="parent-elements"></a>Éléments parents

[**AlternateList**](alternatelist-element.md)

## <a name="child-elements"></a>Éléments enfants

Aucun.

## <a name="attributes"></a>Attributs

Aucun.

## <a name="element-information"></a>Informations sur les éléments



|                  | Valeur                                      |
|------------------|--------------------------------------------|
| **Type d’élément** | xs:string                                  |
| **Espace de noms**    | urn : schemas-microsoft-com : TabletPC : RichInk |
| **Nom du schéma**  | Lecteur de journal                             |



 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------|-------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>WinGDI. h</dt> </dl> |



 

 




