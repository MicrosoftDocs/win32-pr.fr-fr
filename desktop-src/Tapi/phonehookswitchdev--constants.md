---
description: Les \_ constantes d’indicateur de bit PHONEHOOKSWITCHDEV décrivent différents périphériques d’e/s audio, chacun avec son propre hookswitch contrôlable à partir de l’ordinateur.
ms.assetid: b3272a75-87b0-4afc-b2e2-2d65e4b49300
title: Constantes PHONEHOOKSWITCHDEV_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a77e6b776b89adf6224d6feaef8deeef1f9f71b9888929f3aea08b5342adc1dd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119796749"
---
# <a name="phonehookswitchdev_-constants"></a>\_Constantes PHONEHOOKSWITCHDEV

Les constantes d’indicateur de bit **PHONEHOOKSWITCHDEV \_** décrivent différents périphériques d’e/s audio, chacun avec son propre hookswitch contrôlable à partir de l’ordinateur.

<dl> <dt>

<span id="PHONEHOOKSWITCHDEV_HANDSET"></span><span id="phonehookswitchdev_handset"></span>**\_téléphone PHONEHOOKSWITCHDEV**
</dt> <dd> <dl> <dt>



Il s’agit d’un téléphone auriculaire standard et embout.


</dt> </dl> </dd> <dt>

<span id="PHONEHOOKSWITCHDEV_HEADSET"></span><span id="phonehookswitchdev_headset"></span>**\_casque PHONEHOOKSWITCHDEV**
</dt> <dd> <dl> <dt>



Il s’agit d’un casque connecté à l’ensemble téléphonique.


</dt> </dl> </dd> <dt>

<span id="PHONEHOOKSWITCHDEV_SPEAKER"></span><span id="phonehookswitchdev_speaker"></span>**PHONEHOOKSWITCHDEV \_ Speaker**
</dt> <dd> <dl> <dt>



Il s’agit d’un haut-parleur et d’un microphone intégrés. Il peut également s’agir d’un orateur complémentaire connecté en externe au jeu de téléphones.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Remarques

Aucune extensibilité. Tous les 32 bits sont réservés.

Ces constantes sont utilisées dans la structure de données [**PHONECAPS**](/windows/desktop/api/Tapi/ns-tapi-phonecaps) pour indiquer les fonctionnalités de l’appareil hookswitch d’un appareil téléphonique. La structure [**PHONESTATUS**](/windows/desktop/api/Tapi/ns-tapi-phonestatus) signale l’état des appareils hookswitch du téléphone. La fonction [**phoneSetHookSwitch**](/windows/desktop/api/Tapi/nf-tapi-phonesethookswitch) et [**phoneGetHookSwitch**](/windows/desktop/api/Tapi/nf-tapi-phonegethookswitch) l’utilisent en tant que paramètre pour sélectionner le périphérique d’e/s du téléphone.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------|-----------------------------------------------------------------------------------|
| Version TAPI<br/> | Nécessite TAPI 2,0 ou une version ultérieure<br/>                                             |
| En-tête<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




