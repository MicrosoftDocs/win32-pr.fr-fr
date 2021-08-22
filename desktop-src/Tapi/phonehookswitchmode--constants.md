---
description: Les \_ constantes d’indicateur de bit PHONEHOOKSWITCHMODE décrivent les composants de microphone et de haut-parleur d’un appareil hookswitch.
ms.assetid: 532bf089-d5ca-4a04-847d-69e48990ff5c
title: Constantes PHONEHOOKSWITCHMODE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff8f25b7126056690b0b1953065caff3e475ac00cb073c68c8200d056c0114b2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119404479"
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

## <a name="remarks"></a>Remarques

Aucune extensibilité. Tous les 32 bits sont réservés.

Ces constantes sont utilisées pour fournir un niveau individuel de contrôle sur les composants de microphone et de haut-parleur d’un appareil téléphonique.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------|-----------------------------------------------------------------------------------|
| Version TAPI<br/> | Nécessite TAPI 2,0 ou une version ultérieure<br/>                                             |
| En-tête<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




