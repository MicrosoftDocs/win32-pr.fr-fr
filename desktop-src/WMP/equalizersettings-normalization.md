---
title: EQUALIZERSETTINGS. normalisation
description: L’attribut de normalisation spécifie ou récupère une valeur indiquant si la normalisation est activée.
ms.assetid: d0819624-7bc5-447a-b890-c8af94faa7b0
keywords:
- EQUALIZERSETTINGS. normalization Lecteur Windows Media
topic_type:
- apiref
api_name:
- EQUALIZERSETTINGS.normalization
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b6f2befdd62f0508822d5547cb3b894b93ea095f52db4cf9bbdb4a444d99251c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118578164"
---
# <a name="equalizersettingsnormalization"></a>EQUALIZERSETTINGS. normalisation

L’attribut de **normalisation** spécifie ou récupère une valeur indiquant si la normalisation est activée.

``` syntax
        elementID.normalization
```

## <a name="possible-values"></a>Valeurs possibles

Cet attribut est une **valeur booléenne** en lecture/écriture.



| Valeur | Description                         |
|-------|-------------------------------------|
| true  | La normalisation est activée.           |
| false | Par défaut. La normalisation est désactivée. |



 

## <a name="remarks"></a>Notes

Lorsque la normalisation est activée, le signal audio d’un fichier multimédia numérique entier est mis à l’échelle jusqu’à la valeur maximale. Cela permet à plusieurs fichiers d’être lus à peu près du même volume sans nécessiter de réglages de volume.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------|
| Version<br/> | Lecteur Windows Media série 9 ou version ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Élément EQUALIZERSETTINGS**](equalizersettings-element.md)
</dt> <dt>

[**EQUALIZERSETTINGS.normalizationAverage**](equalizersettings-normalizationaverage.md)
</dt> <dt>

[**EQUALIZERSETTINGS.normalizationPeak**](equalizersettings-normalizationpeak.md)
</dt> </dl>

 

 





