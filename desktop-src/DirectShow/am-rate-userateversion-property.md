---
description: Cette propriété est utilisée pour indiquer la version de la propriété de modification de taux que le décodeur doit utiliser.
ms.assetid: 49d1bfda-749b-4614-9a75-1f76fa8b320d
title: AM_RATE_UseRateVersion, propriété (dvdmedia. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4dd33ef96c50ecc3da0711f08f0c7ffbf0a20825
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127112285"
---
# <a name="am_rate_userateversion-property"></a>\_ \_ Propriété USERATEVERSION rate AM

Cette propriété est utilisée pour indiquer la version de la propriété de modification de taux que le décodeur doit utiliser. La valeur est un type de **mot** . L’octet de poids fort contient le numéro de version mineure et l’octet de poids faible contient l’octet de poids faible. Par conséquent, la version 1,1 est signalée par la valeur 0x0101.

Si le décodeur ne prend pas en charge la version spécifiée, il doit faire échouer l’appel à [**IKsPropertySet :: Set**](ikspropertyset-set.md) et retourner E \_ nointerface. Si le filtre source ne définit pas la version, le décodeur doit avoir la valeur par défaut version 1,0.



| Étiquette | Valeur |
|-------------------|-------------------------------|
| GUID de jeu de propriétés | AM \_ KSPROPSETID \_ TSRateChange |
| ID de propriété       | \_Taux am \_ UseRateVersion      |
| Type de données         | **WORD**                      |



 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------|---------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Dvdmedia. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Définition de la propriété change rate**](rate-change-property-set.md)
</dt> </dl>

 

 




