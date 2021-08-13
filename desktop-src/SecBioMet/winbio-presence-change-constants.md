---
title: Constantes WINBIO_PRESENCE_CHANGE ( \_ types WINBIO. h)
description: décrit les types de modifications qui peuvent se produire lorsque le Windows Biometric Framework surveille la présence de personnes.
ms.assetid: 1E0B65D8-A38F-46BA-A99A-18666729FA30
topic_type:
- apiref
api_name:
- WINBIO_PRESENCE_CHANGE_TYPE_UNKNOWN
- WINBIO_PRESENCE_CHANGE_TYPE_UPDATE_ALL
- WINBIO_PRESENCE_CHANGE_TYPE_ARRIVE
- WINBIO_PRESENCE_CHANGE_TYPE_RECOGNIZE
- WINBIO_PRESENCE_CHANGE_TYPE_DEPART
- WINBIO_PRESENCE_CHANGE_TYPE_TRACK
api_location:
- winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08cce9cc74bafdba6cf8d1aa11abccdaf7315370223ff6edf47eaba167af84f0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118909718"
---
# <a name="winbio_presence_change-constants"></a>\_Constantes de modification de présence WINBIO \_

décrit les types de modifications qui peuvent se produire lorsque le Windows Biometric Framework surveille la présence de personnes.



| Constante/valeur                                                                                                                                                                                                                                                                                      | Description                                                                                                                                               |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_PRESENCE_CHANGE_TYPE_UNKNOWN"></span><span id="winbio_presence_change_type_unknown"></span><dl> <dt>**WINBIO \_ TYPE de modification de présence \_ \_ \_ inconnu**</dt> <dt>0</dt> </dl>           | Le type d’événement est inconnu. Cette valeur est utilisée pour la structure non initialisée.<br/>                                                              |
| <span id="WINBIO_PRESENCE_CHANGE_TYPE_UPDATE_ALL"></span><span id="winbio_presence_change_type_update_all"></span><dl> <dt>**WINBIO \_ TYPE de modification de présence \_ \_ \_ mettre à jour \_ tous les**</dt> <dt>1</dt> </dl> | Fournit des informations sur toutes les faces actuelles dans le cadre de l’appareil photo.<br/>                                                                       |
| <span id="WINBIO_PRESENCE_CHANGE_TYPE_ARRIVE"></span><span id="winbio_presence_change_type_arrive"></span><dl> <dt>**WINBIO \_ \_Type de \_ modification \_ de présence**</dt> <dt>2</dt> </dl>              | Une nouvelle face est entrée dans le cadre de l’appareil photo.<br/>                                                                                                           |
| <span id="WINBIO_PRESENCE_CHANGE_TYPE_RECOGNIZE"></span><span id="winbio_presence_change_type_recognize"></span><dl> <dt>**WINBIO \_ \_Reconnaissance du \_ type \_ de modification de présence**</dt> <dt>3</dt> </dl>     | Un visage a été mis en correspondance avec un utilisateur inscrit.<br/>                                                                                                        |
| <span id="WINBIO_PRESENCE_CHANGE_TYPE_DEPART"></span><span id="winbio_presence_change_type_depart"></span><dl> <dt>**WINBIO \_ TYPE de modification de présence- \_ \_ \_ DEPART**</dt> <dt>4</dt> </dl>              | Un visage précédemment détecté est sorti du cadre de l’appareil photo pendant un certain temps.<br/>                                                              |
| <span id="WINBIO_PRESENCE_CHANGE_TYPE_TRACK"></span><span id="winbio_presence_change_type_track"></span><dl> <dt>**WINBIO \_ TYPE de modification de présence- \_ \_ \_ piste**</dt> <dt>5</dt> </dl>                 | Fournit des informations de mise à jour sur le cadre englobant et rejettent les valeurs de détails pour un sous-ensemble des visages qui se trouvent actuellement dans le cadre de l’appareil photo.<br/> |



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 10 \[ applications de bureau uniquement\]<br/>                                                                                                                              |
| Serveur minimal pris en charge<br/> | Windows Server 2016 \[ applications de bureau uniquement\]<br/>                                                                                                                     |
| En-tête<br/>                   | <dl> <dt>WinBio \_ types. h (inclure WinBio. h pour les applications clientes ou les \_ cartes WinBio. h pour les adaptateurs)</dt> </dl> |



 

 





