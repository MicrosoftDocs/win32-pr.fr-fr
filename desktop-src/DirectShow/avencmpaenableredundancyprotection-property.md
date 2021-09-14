---
description: Spécifie s’il faut ajouter une vérification de redondance cyclique (CRC) à l’en-tête de trame. Cette propriété s’applique aux encodeurs audio MPEG.
ms.assetid: 55f0de8b-26dd-4d48-b7ed-2ddcef630227
title: Propriété AVEncMPAEnableRedundancyProtection (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2028b5adaad55d46cc53c61f9d65a73819cc899
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127111810"
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

 

 




