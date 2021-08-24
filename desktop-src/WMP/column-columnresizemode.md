---
title: COLUMN. columnResizeMode
description: L’attribut columnResizeMode spécifie ou récupère le mode de redimensionnement pour cette colonne.
ms.assetid: 95ece2a3-20a6-4b9d-a2eb-fc69fc612f29
keywords:
- COLUMN. columnResizeMode Lecteur Windows Media
topic_type:
- apiref
api_name:
- COLUMN.columnResizeMode
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c59046aa76c01a1439e5db8f0fb6850e7df74d874cba555d1f9c3829f09d9598
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119763999"
---
# <a name="columncolumnresizemode"></a>COLUMN. columnResizeMode

L’attribut **columnResizeMode** spécifie ou récupère le mode de redimensionnement pour cette colonne.

``` syntax
        elementID.columnResizeMode
```

## <a name="possible-values"></a>Valeurs possibles

Cet attribut est une **chaîne** en lecture/écriture contenant l’une des valeurs suivantes.



| Valeur          | Description                                                                                                    |
|----------------|----------------------------------------------------------------------------------------------------------------|
| AutosizeHeader | Par défaut. La colonne est redimensionnée pour s’adapter à toutes les données de la colonne et de l’en-tête.                         |
| AutosizeData   | La colonne est redimensionnée pour s’adapter à toutes les données de la colonne uniquement.                                                 |
| Fixe          | La colonne a une taille fixe.                                                                                    |
| S’étire      | La colonne se redimensionne pour utiliser l’espace restant dans le contrôle de **sélection** une fois que toutes les autres colonnes sont redimensionnées. |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------|
| Version<br/> | Lecteur Windows Media série 9 ou version ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Élément COLUMN**](column-element.md)
</dt> </dl>

 

 





