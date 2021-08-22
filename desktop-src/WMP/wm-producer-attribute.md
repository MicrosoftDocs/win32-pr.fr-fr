---
title: Attribut WM/Producer
description: L’attribut WM/Producer est le nom du producteur du contenu.
ms.assetid: b7c0dbea-ed57-4243-be76-90b2998304ba
keywords:
- Lecteur Windows Media de l’attribut WM/producer
topic_type:
- apiref
api_name:
- WM/Producer
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5f51c0e995e69d63cd21338704a8ad4a3a602d7e805dd39139373c9bd9b68c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119053797"
---
# <a name="wmproducer-attribute"></a>Attribut WM/Producer

L’attribut **WM/Producer** est le nom du producteur du contenu.

## <a name="applies-to"></a>S'applique à

-   [attributs de fichier multimédia Windows couramment utilisés](commonly-used-windows-media-file-attributes.md)
-   [Éléments vidéo](video-item-attributes.md)

## <a name="remarks"></a>Remarques

Cet attribut est stocké à la fois dans la bibliothèque et dans le fichier multimédia numérique.

**ProducedBy** est un alias pour cet attribut.

la constante du kit de développement logiciel (SDK) du Format multimédia Windows pour cet attribut est g \_ wszWMProducer.

Pour déterminer si vous pouvez modifier la valeur de cet attribut, utilisez la méthode [Media. isReadOnlyItem](media-isreadonlyitem.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------|
| Version<br/> | Lecteur Windows Media série 9 ou version ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Référence d’attribut**](attribute-reference.md)
</dt> </dl>

 

 





