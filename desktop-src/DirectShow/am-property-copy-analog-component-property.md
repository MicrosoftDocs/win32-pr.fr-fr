---
description: Recherche si la sortie vidéo est une vidéo de composant analogique de définition standard.
ms.assetid: bd4fc5bc-c45d-4228-9759-6300fdfff6a0
title: AM_PROPERTY_COPY_ANALOG_COMPONENT, propriété (dvdmedia. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6448bfbcc07be6ca37189c15c7c605887e6d22b3
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/22/2021
ms.locfileid: "107910307"
---
# <a name="am_property_copy_analog_component-property"></a>Propriété \_ du \_ \_ composant analogique de copie des propriétés am \_

Recherche si la sortie vidéo est une vidéo de composant analogique de définition standard.



| Étiquette | Valeur |
|-------------------|---------------------------------------|
| GUID de jeu de propriétés | AM \_ KSPROPSETID \_ CopyProt             |
| ID de propriété       | \_ \_ composant analogique de copie de propriétés am \_ \_ |
| Type de données         | **ULONG**                             |



 

## <a name="remarks"></a>Remarques

Cette propriété est en lecture seule.

La valeur de la propriété est **true** si la sortie vidéo est une vidéo de composant analogique dont la résolution n’est pas supérieure à 480p pour NTSC ou 540p pour PAL. Dans le cas contraire, la valeur est **false**.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|---------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Dvdmedia. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Jeu de propriétés protection de copie de DVD**](dvd-copy-protection-property-set.md)
</dt> </dl>

 

 




