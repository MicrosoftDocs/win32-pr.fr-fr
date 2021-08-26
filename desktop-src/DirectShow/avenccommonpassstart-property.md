---
description: Démarre la première passe d’encodage.
ms.assetid: a062be3f-7806-4f1c-b98e-2c9ed31f010c
title: Propriété AVEncCommonPassStart (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7830537e6345d43927c7009e0e3ec9148505217818e981d7354a100a4ff2d68e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120000139"
---
# <a name="avenccommonpassstart-property"></a>Propriété AVEncCommonPassStart

Démarre la première passe d’encodage.

Cette propriété est en écriture seule.

## <a name="data-type"></a>Type de données

**UInt32** (**VT \_ UI4**)

## <a name="property-guid"></a>Guid de propriété

**CODECAPI \_ AVEncCommonPassStart**

## <a name="property-value"></a>Valeur de la propriété

La valeur de cette propriété est l’étape d’encodage à démarrer. Pour obtenir la plage des valeurs prises en charge, interrogez la propriété [**AVEncCommonMultipassMode**](avenccommonmultipassmode-property.md) de l’encodeur.

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

 

 




