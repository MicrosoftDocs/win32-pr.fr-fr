---
title: EQUALIZERSETTINGS. normalisation
description: L’attribut de normalisation spécifie ou récupère une valeur indiquant si la normalisation est activée.
ms.assetid: d0819624-7bc5-447a-b890-c8af94faa7b0
keywords:
- EQUALIZERSETTINGS. normalisation du lecteur Windows Media
topic_type:
- apiref
api_name:
- EQUALIZERSETTINGS.normalization
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9714359e5d5e2af0c82a0d687555f7cfcbf1cf70
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528677"
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

 

 





