---
description: Les propriétés de sous-image de DVD contrôlent la couleur, le contraste et la sortie de l’affichage de la sous-image.
ms.assetid: ddbfb65c-7630-4e9f-8013-c5d65c62c628
title: Jeu de propriétés de sous-image de DVD (dvdmedia. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a45b83595e8657ee0c60f39cd67f2d0e4c71511
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909087"
---
# <a name="dvd-subpicture-property-set"></a>Jeu de propriétés de sous-image de DVD

Les propriétés de sous-image de DVD contrôlent la couleur, le contraste et la sortie de l’affichage de la sous-image.

Les informations suivantes présentent les constantes et types de données nécessaires à utiliser pour ce jeu de propriétés dans les appels aux méthodes [**IKsPropertySet**](ikspropertyset.md) . Il fournit des valeurs pour les paramètres **GUID** (*GUIDPROPSET*), ID de propriété (*dwPropID*) et type de données de propriété (*pPropData*).



| Étiquette | Valeur |
|-------------------|----------------------------|
| GUID de jeu de propriétés | AM \_ KSPROPSETID \_ DvdSubPic |



 



| ID de propriété                           | Description                                                                                                                                                                                                                                                                                                                                                              |
|---------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| la \_ \_ composition DVDSUBPIC de la propriété am \_ \_ sur | Propriété définie uniquement qui active ou désactive l’affichage de sous-image. DirectShow définit la **\_ \_ composition \_ de propriété AM sur** le type de données booléen pour cette propriété, ainsi que la \_ \_ composition de propriété PAM \_ sur en tant que pointeur vers ce type de données. **True** indique que afficher la sous-image, **false** indique la désactiver. Pour plus d’informations, consultez la partie WDM du DDK Windows. |
| AM, \_ propriété \_ DVDSUBPIC \_ HLI          | Propriété définie uniquement qui spécifie un rectangle de sous-image ou d’écran dont la couleur ou le contraste seront modifiés. Le type de données est la [**\_ propriété am \_ SPHLI**](/previous-versions/windows/desktop/api/Dvdmedia/ns-dvdmedia-am_property_sphli). Consultez la section Notes.                                                                                                                                                                                |
| \_DVDSUBPIC, propriété, \_ \_ palette      | Définit la palette pour une sous-image. Le type de données est la [**\_ propriété am \_ SPPAL**](/previous-versions/windows/desktop/api/Dvdmedia/ns-dvdmedia-am_property_sppal).                                                                                                                                                                                                                                                                        |



 

## <a name="remarks"></a>Remarques

La **propriété \_ \_ DVDSUBPIC \_ HLI** est définie sur la propriété am uniquement. Elle spécifie un rectangle de sous-image ou d’écran dont la couleur ou le contraste seront modifiés. Cela diffère de la spécification DVD-Video, dans le fait que le navigateur de DVD Microsoft analyse toutes les informations relatives aux boutons et au clavier et passe un seul rectangle de surbrillance au décodeur de sous-image à un moment donné. Par conséquent, les informations de mise en surbrillance sont envoyées au décodeur plus souvent qu’elles ne sont présentes dans le flux DVD.

Les informations de mise en surbrillance arrivent de manière asynchrone dans le flux de données. Le décodeur utilise les horodatages de début et de fin de mise en surbrillance pour mettre en corrélation les informations de surbrillance avec les informations de sous-image pertinentes, le cas échéant. Si le décodeur n’a reçu aucune information de flux de sous-image pour les horodatages demandés, le décodeur suppose que les informations de mise en surbrillance sont autonomes et ne s’appliquent pas à une sous-image. Dans ce cas, le décodeur suppose que les informations de couleur et de contraste sont toutes de la même couleur.

Les données ne sont pas entièrement au format de disque DVD. Microsoft fournit une structure supplémentaire de type [**am \_ Property \_ SPHLI**](/previous-versions/windows/desktop/api/Dvdmedia/ns-dvdmedia-am_property_sphli) qui est transmise en tant que paramètre à cette propriété. Cette structure décrit le bouton actuellement sélectionné à partir des informations de mise en surbrillance du DVD.

Le navigateur DVD traite toutes les informations de frappe et envoie de nouvelles informations de mise en surbrillance chaque fois qu’un état de bouton change. Les informations décrivent un seul mode d’un bouton à la fois. Il comprend un rectangle d’affichage en coordonnées de pixels de l’écran, ou un affichage de la sous-image, le cas échéant. La structure contient également des informations de couleur et de contraste, mais uniquement pour l’état actuel du bouton actuellement sélectionné. Le format est défini dans la spécification du DVD.

Les informations de mise en surbrillance contiennent des horodatages de début et de fin. Celles-ci se trouvent dans les mêmes unités que d’autres horodatages, à deux exceptions près : un horodatage de début 0xFFFFFFFF signifie que la propriété de surbrillance est effective lors de la réception et un horodatage de fin 0xFFFFFFFF signifie que la propriété de surbrillance est valide jusqu’à la prochaine sélection reçue.

Le champ HLISS est défini dans la spécification du DVD. La valeur zéro indique que toutes les mises en surbrillance ne sont pas valides et que le décodeur doit désactiver toutes les mises en surbrillance.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|---------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Dvdmedia. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Jeux de propriétés](property-sets.md)
</dt> </dl>

 

 




