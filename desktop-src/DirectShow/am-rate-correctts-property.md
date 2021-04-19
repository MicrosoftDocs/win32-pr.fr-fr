---
description: Le navigateur DVD utilise cette propriété pour informer le décodeur que le navigateur définit les horodatages corrects sur les exemples qu’il remet au décodeur.
ms.assetid: f04e8291-734f-483e-b756-5362beb68d9c
title: AM_RATE_CorrectTS, propriété (dvdmedia. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa410b079d3de63de364662c7d5465c82814d24a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539967"
---
# <a name="am_rate_correctts-property"></a>\_ \_ Propriété CORRECTTS rate AM

Le navigateur DVD utilise cette propriété pour informer le décodeur que le navigateur définit les horodatages corrects sur les exemples qu’il remet au décodeur.



|                   |                               |
|-------------------|-------------------------------|
| GUID de jeu de propriétés | AM \_ KSPROPSETID \_ TSRateChange |
| ID de propriété       | \_Taux am \_ CorrectTS           |
| Type de données         | **LONG**                      |



 

## <a name="remarks"></a>Notes

Les versions antérieures du navigateur DVD n’ont pas défini les horodatages corrects lorsque la vitesse de lecture était différente de 1,0. De nombreux décodeurs contournent ce problème en ignorant les horodatages pendant le rembobinage ou l’avance rapide, et en estimant les durées de présentation appropriées.

Ces problèmes ont été corrigés dans la version actuelle du navigateur DVD. Pour assurer la compatibilité descendante avec les décodeurs existants, le navigateur DVD indique que les horodatages sont corrects en définissant la \_ \_ propriété CorrectTS rate sur le décodeur avec la valeur **true**. Quand cette propriété est définie, le décodeur doit utiliser les horodatages réels au lieu d’estimer les temps de présentation.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|---------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Dvdmedia. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Définition de la propriété change rate**](rate-change-property-set.md)
</dt> </dl>

 

 




