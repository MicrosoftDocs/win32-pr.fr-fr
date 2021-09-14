---
description: Spécifie si l’encodeur produit des groupes d’images ouverts (GOP secondes) ou des GOP secondes fermés. Cette propriété s’applique aux encodeurs vidéo MPEG.
ms.assetid: 424751cd-65d2-4cab-9f7b-cad50c09c767
title: Propriété AVEncMPVGOPOpen (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6dd971a6cc9926245b97794868f58758af814803
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127111750"
---
# <a name="avencmpvgopopen-property"></a>Propriété AVEncMPVGOPOpen

Spécifie si l’encodeur produit des groupes d’images ouverts (GOP secondes) ou des GOP secondes fermés. Cette propriété s’applique aux encodeurs vidéo MPEG.

Cette propriété est en lecture/écriture.

## <a name="data-type"></a>Type de données

**Variante \_ BOOL** (**VT \_ bool**)

## <a name="property-guid"></a>Guid de propriété

**CODECAPI \_ AVEncMPVGOPOpen**

## <a name="property-value"></a>Valeur de la propriété



| Valeur          | Description |
|----------------|-------------|
| VARIANTE \_ false | GOP secondes fermé |
| VARIANTE \_ true  | Ouvrir GOP secondes   |



 

## <a name="remarks"></a>Notes

Un groupe d’images ouvert contient des frames Delta qui référencent des frames du groupe d’images précédent. Un groupe d’images fermé ne contient pas de frame Delta qui référencent le groupe d’images précédent.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | applications Windows 2000 Professional \[ desktop apps \| UWP\]<br/>                     |
| Serveur minimal pris en charge<br/> | applications de bureau Windows 2000 Server apps-applications \[ \| UWP\]<br/>                           |
| En-tête<br/>                   | <dl> <dt>Codecapi. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés de l’API codec](codec-api-properties.md)
</dt> <dt>

[**Interface ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




