---
description: Spécifie le paramètre par défaut pour le bit de copyright dans le flux audio MPEG-1. Cette propriété s’applique aux encodeurs audio MPEG.
ms.assetid: 6029c96f-b1dd-402f-9bac-9021bd897ee4
title: Propriété AVEncMPACopyright (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fbd747de4f4351e5d540fcf8235194308457e0dcc985500f2743209061cedbdb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119824269"
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



 

## <a name="remarks"></a>Remarques

L’encodeur peut remplacer ce paramètre en fonction du contenu du flux d’entrée.

## <a name="requirements"></a>Configuration requise



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

 

 




