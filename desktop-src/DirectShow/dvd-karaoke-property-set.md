---
description: Lorsque le filtre de navigateur DVD passe en mode karaoké, il informe le décodeur audio via la propriété AM \_ \_ DVDKARAOKE \_ Enable Property.
ms.assetid: 78b2998b-d8b3-424d-85bc-872e64eb4a4f
title: Jeu de propriétés Karaoké DVD (dvdmedia. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 396e9fe53ad35dac0c3c0f54a8e04a6fbe698fc1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541319"
---
# <a name="dvd-karaoke-property-set"></a>Jeu de propriétés Karaoké DVD

Lorsque le filtre de [navigateur DVD](dvd-navigator-filter.md) passe en mode karaoké, il informe le décodeur audio via la propriété **am \_ \_ DVDKARAOKE \_ Enable** Property. Le décodeur doit ensuite désactiver les canaux audio de 2 à 5 jusqu’à ce qu’il reçoive du navigateur DVD une propriété de **\_ \_ \_ données DVDKARAOKE de la propriété am** avec un pointeur vers une structure de données [**am \_ DvdKaraokeData**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdkaraokedata) indiquant comment les canaux auxiliaires doivent être mélangés.



|                   |                             |
|-------------------|-----------------------------|
| GUID de jeu de propriétés | AM \_ KSPROPSETID \_ DvdKaraoke |



 



| ID de propriété                      | Description                                                                                                                                                                                                                                                                                                 |
|----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| AM, \_ propriété \_ DVDKARAOKE \_ activer | Valeur BOOLÉENNE. Le navigateur DVD envoie au décodeur une \_ propriété am \_ DVDKARAOKE \_ Enable avec la valeur **true** pour activer karaoké downmixing ou **false** pour le désactiver.                                                                                                                                    |
| AM, \_ propriété \_ DVDKARAOKE \_ données   | Le navigateur DVD envoie au décodeur une propriété \_ de \_ données DVDKARAOKE de propriété am \_ avec un pointeur vers une structure [**am \_ DvdKaraokeData**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdkaraokedata) pour modifier la configuration downmix ; autrement dit, pour activer ou désactiver certains canaux karaoké et les diriger vers le canal de sortie de droite ou de gauche. |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|---------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Dvdmedia. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Jeux de propriétés](property-sets.md)
</dt> </dl>

 

 




