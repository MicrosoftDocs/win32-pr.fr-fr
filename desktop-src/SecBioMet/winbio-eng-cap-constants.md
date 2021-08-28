---
title: Constantes WINBIO_ENG_CAP ( \_ types WINBIO. h)
description: Spécifiez des fonctionnalités de moteur génériques.
ms.assetid: 31C4E8AF-6EF8-43FF-A944-D7363A26BB1A
topic_type:
- apiref
api_name:
- WINBIO_ENG_CAP_ITERATIVE_IMPROVEMENT
- WINBIO_ENG_CAP_SPOOF_DETECTION
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5be1099b6ad555b0547dc975c1446740f43359792c1643d155322095ad26dd4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119867949"
---
# <a name="winbio_eng_cap-constants"></a>\_ \_ Constantes WINBIO ENG

Les constantes suivantes sont des valeurs de **\_ fonctionnalités WINBIO** qui peuvent être utilisées pour spécifier des fonctionnalités génériques du composant moteur qui est connecté à une unité biométrique spécifique. Vous spécifiez ces fonctionnalités dans le membre **GenericEngineCapabilities** de la structure [**WINBIO \_ Extended \_ Engine \_ info**](winbio-extended-engine-info.md) .



| Constante/valeur                                                                                                                                                                                                                                                                                        | Description                                                                  |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------|
| <span id="WINBIO_ENG_CAP_ITERATIVE_IMPROVEMENT"></span><span id="winbio_eng_cap_iterative_improvement"></span><dl> <dt>**WINBIO \_ \_ \_ \_ Amélioration itérative du eng-Cap**</dt> - <dt>0x00000001</dt> </dl> | Le composant de moteur biométrique peut effectuer une amélioration itérative.<br/> |
| <span id="WINBIO_ENG_CAP_SPOOF_DETECTION"></span><span id="winbio_eng_cap_spoof_detection"></span><dl> <dt>**WINBIO \_ \_Détection d' \_ usurpation \_ d’adresse eng Cap**</dt> <dt>0x00000002</dt> </dl>                   | Le composant de moteur biométrique peut effectuer une détection d’usurpation d’identité.<br/>       |



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 10 \[ applications de bureau uniquement\]<br/>                                                                   |
| Serveur minimal pris en charge<br/> | Windows Server 2016 \[ applications de bureau uniquement\]<br/>                                                          |
| En-tête<br/>                   | <dl> <dt>WinBio \_ types. h (include WinBio. h)</dt> </dl> |



 

 





