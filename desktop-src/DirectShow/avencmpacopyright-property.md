---
description: Spécifie le paramètre par défaut pour le bit de copyright dans le flux audio MPEG-1. Cette propriété s’applique aux encodeurs audio MPEG.
ms.assetid: 6029c96f-b1dd-402f-9bac-9021bd897ee4
title: Propriété AVEncMPACopyright (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f4449c41448d59ce673e667be7400d4a713236dd
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104392759"
---
# <a name="avencmpacopyright-property"></a>Propriété AVEncMPACopyright

Spécifie le paramètre par défaut pour le bit de copyright dans le flux audio MPEG-1. Cette propriété s’applique aux encodeurs audio MPEG.

Cette propriété est en lecture/écriture.

## <a name="data-type"></a>Type de données

**Variante \_ BOOL** (**VT \_ bool**)

## <a name="property-guid"></a>Guid de propriété

**CODECAPI \_ AVEncMPACopyright**

## <a name="property-value"></a>Valeur de la propriété

Cette propriété peut avoir les valeurs suivantes.



| Valeur          | Description           |
|----------------|-----------------------|
| VARIANTE \_ false | Le bit de copyright est désactivé. |
| VARIANTE \_ true  | Le bit de copyright est activé.  |



 

## <a name="remarks"></a>Notes

L’encodeur peut remplacer ce paramètre en fonction du contenu du flux d’entrée.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de bureau Windows 2000 professionnel- \[ \| applications UWP\]<br/>                     |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows 2000 Server \[ apps- \| applications UWP\]<br/>                           |
| En-tête<br/>                   | <dl> <dt>Codecapi. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés de l’API codec](codec-api-properties.md)
</dt> <dt>

[**Interface ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




