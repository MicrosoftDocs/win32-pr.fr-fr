---
description: S’applique à Windows Vista et versions ultérieures.
ms.assetid: 4f170736-516d-4420-a215-e0e414f036cd
title: AM_RATE_ReverseMaxFullDataRate, propriété (dvdmedia. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31e376c6e95160c6a6c3c6637a765d868e282d33
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/22/2021
ms.locfileid: "107910237"
---
# <a name="am_rate_reversemaxfulldatarate-property"></a>\_ \_ Propriété REVERSEMAXFULLDATARATE rate AM

S’applique à Windows Vista et versions ultérieures.

Retourne la vitesse de lecture inversée maximale du décodeur. La valeur de la propriété est la valeur absolue de la vitesse inversée maximale x 10000. Par exemple, si la vitesse inversée maximale est-2,0, la valeur de cette propriété est 20000.

Le type de données de cette propriété **est \_ MaxFullDataRate**, qui est `typedef` de type **long**.

Cette propriété est en lecture seule.



| Étiquette | Valeur |
|-------------------|----------------------------------|
| GUID de jeu de propriétés | AM \_ KSPROPSETID \_ TSRateChange    |
| ID de propriété       | \_Taux am \_ ReverseMaxFullDataRate |
| Type de données         | **AM \_ MaxFullDataRate**          |



 

## <a name="remarks"></a>Remarques

Les décodeurs qui prennent en charge la lecture inversée en douceur doivent exposer cette propriété. Pour plus d’informations, consultez [améliorations de la lecture de DVD dans Windows Vista](dvd-playback-enhancements-in-windows-vista.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|---------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Dvdmedia. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Définition de la propriété change rate**](rate-change-property-set.md)
</dt> </dl>

 

 




