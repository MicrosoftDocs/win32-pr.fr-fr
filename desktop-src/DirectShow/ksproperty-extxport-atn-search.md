---
description: Cette propriété envoie une commande à l’appareil pour rechercher un numéro de piste absolu (ATN). Le pilote de périphérique UVC prend en charge cette propriété.
ms.assetid: 209e0aa3-d7a3-4b5c-ae5a-5063a3804a9d
title: KSPROPERTY_EXTXPORT_ATN_SEARCH
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f4115c7ff1c4bc878b4ee80e284f11821c37909a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126999026"
---
# <a name="ksproperty_extxport_atn_search"></a>\_recherche KSPROPERTY EXTXPORT \_ ATN \_

Cette propriété envoie une commande à l’appareil pour rechercher un numéro de piste absolu (ATN). Le pilote de périphérique UVC prend en charge cette propriété.



| Étiquette | Valeur |
|-------------------|---------------------------------------|
| GUID de jeu de propriétés | \_transport PROPSETID ext \_             |
| ID de propriété       | \_recherche KSPROPERTY EXTXPORT \_ ATN \_     |
| Type de données         | **KSPROPERTY \_ Structure EXTXPORT \_ S** |



 

## <a name="remarks"></a>Notes

Définissez le membre **dwAbsTrackNumber** de la structure **KSPROPERTY \_ EXTXPORT \_ S** sur la valeur suivante :


```
(absolute track number << 1) + continuity bit
```



La spécification UVC ne définit pas la manière dont l’appareil utilise le bit de continuité. la structure **KSPROPERTY \_ EXTXPORT \_ S** est décrite dans le Windows DDK.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Ensemble de propriétés de transport d’appareil externe](external-device-transport-property-set.md)
</dt> </dl>

 

 



