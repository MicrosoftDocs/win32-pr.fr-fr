---
description: Spécifie s’il faut ajouter une vérification de redondance cyclique (CRC) à l’en-tête de trame. Cette propriété s’applique aux encodeurs audio MPEG.
ms.assetid: 55f0de8b-26dd-4d48-b7ed-2ddcef630227
title: Propriété AVEncMPAEnableRedundancyProtection (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b50e010b0b088e8817eca4dae1989cd6f623f55a9616c4449df62f115f98ff7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119824109"
---
# <a name="avencmpaenableredundancyprotection-property"></a>Propriété AVEncMPAEnableRedundancyProtection

Spécifie s’il faut ajouter une vérification de redondance cyclique (CRC) à l’en-tête de trame. Cette propriété s’applique aux encodeurs audio MPEG.

Cette propriété est en lecture/écriture.

## <a name="data-type"></a>Type de données

**Variante \_ BOOL** (**VT \_ bool**)

## <a name="property-guid"></a>Guid de propriété

**CODECAPI \_ AVEncMPAEnableRedundancyProtection**

## <a name="property-value"></a>Valeur de la propriété

Cette propriété peut avoir les valeurs suivantes.



| Valeur          | Description                |
|----------------|----------------------------|
| VARIANTE \_ false | N’ajoutez pas de somme de contrôle CRC. |
| VARIANTE \_ true  | Ajoutez une somme de contrôle CRC.        |



 

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

 

 




