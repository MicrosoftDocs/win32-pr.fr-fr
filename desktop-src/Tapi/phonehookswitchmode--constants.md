---
description: Les \_ constantes d’indicateur de bit PHONEHOOKSWITCHMODE décrivent les composants de microphone et de haut-parleur d’un appareil hookswitch.
ms.assetid: 532bf089-d5ca-4a04-847d-69e48990ff5c
title: Constantes PHONEHOOKSWITCHMODE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8028cb531d5b38185edf75ae58e4c3c855398f2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127008732"
---
# <a name="phonehookswitchmode_-constants"></a>\_Constantes PHONEHOOKSWITCHMODE

Les constantes d’indicateur de bit **PHONEHOOKSWITCHMODE \_** décrivent les composants de microphone et de haut-parleur d’un appareil hookswitch.

<dl> <dt>

<span id="PHONEHOOKSWITCHMODE_MIC"></span><span id="phonehookswitchmode_mic"></span>**\_MIC PHONEHOOKSWITCHMODE**
</dt> <dd> <dl> <dt>



Le microphone de l’appareil est actif, le haut-parleur est muet.


</dt> </dl> </dd> <dt>

<span id="PHONEHOOKSWITCHMODE_MICSPEAKER"></span><span id="phonehookswitchmode_micspeaker"></span>**PHONEHOOKSWITCHMODE \_ MICSPEAKER**
</dt> <dd> <dl> <dt>



Le microphone et le haut-parleur de l’appareil sont tous deux actifs.


</dt> </dl> </dd> <dt>

<span id="PHONEHOOKSWITCHMODE_ONHOOK"></span><span id="phonehookswitchmode_onhook"></span>**PHONEHOOKSWITCHMODE \_ ONHOOK**
</dt> <dd> <dl> <dt>



Le microphone et le haut-parleur de l’appareil sont tous deux OnHook.


</dt> </dl> </dd> <dt>

<span id="PHONEHOOKSWITCHMODE_SPEAKER"></span><span id="phonehookswitchmode_speaker"></span>**PHONEHOOKSWITCHMODE \_ Speaker**
</dt> <dd> <dl> <dt>



Le haut-parleur de l’appareil est actif, le microphone est muet.


</dt> </dl> </dd> <dt>

<span id="PHONEHOOKSWITCHMODE_UNKNOWN"></span><span id="phonehookswitchmode_unknown"></span>**PHONEHOOKSWITCHMODE \_ inconnu**
</dt> <dd> <dl> <dt>



Le mode hookswitch de l’appareil est actuellement inconnu.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Notes

Aucune extensibilité. Tous les 32 bits sont réservés.

Ces constantes sont utilisées pour fournir un niveau individuel de contrôle sur les composants de microphone et de haut-parleur d’un appareil téléphonique.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------|-----------------------------------------------------------------------------------|
| Version TAPI<br/> | Nécessite TAPI 2,0 ou une version ultérieure<br/>                                             |
| En-tête<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




