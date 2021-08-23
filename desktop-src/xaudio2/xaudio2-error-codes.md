---
description: Codes d’erreur spécifiques à XAudio2 retournés par les méthodes XAudio2.
ms.assetid: 42a1c21c-4b14-114a-d79e-15a61eb2139b
title: Codes d’erreur XAudio2 (Xaudio2. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6bbfb29153ca55064c1019e9cfb8fd1019caaa0ffe17dfa103f123faa812f762
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119545399"
---
# <a name="xaudio2-error-codes"></a>Codes d’erreur XAudio2

Codes d’erreur spécifiques à XAudio2 retournés par les méthodes XAudio2.



| Constante/valeur                                                                                                                                                                                                                                                                      | Description                                                                                                                                                                                                                                                                                                                                                       |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="XAUDIO2_E_INVALID_CALL"></span><span id="xaudio2_e_invalid_call"></span><dl> <dt>**XAUDIO2 \_ E 0x88960001 d' \_ \_ appel non valide**</dt> <dt></dt> </dl>                          | Retourné par XAudio2 pour certaines erreurs d’utilisation de l’API (appels non valides, etc.) qui sont difficiles à éviter complètement et doivent être gérées par un titre au moment de l’exécution. (Les erreurs d’utilisation d’API qui sont entièrement évitables, telles que les paramètres non valides, provoquent une assertion dans les versions Debug et le comportement non défini dans les versions commerciales, de sorte qu’aucun code d’erreur n’est défini pour eux.)<br/> |
| <span id="XAUDIO2_E_XMA_DECODER_ERROR"></span><span id="xaudio2_e_xma_decoder_error"></span><dl> <dt>**XAUDIO2 \_ \_Erreur du \_ décodeur \_ E XMA**</dt> <dt>0x88960002</dt> </dl>          | Le matériel Xbox 360 XMA a subi une erreur irrécupérable.<br/>                                                                                                                                                                                                                                                                                             |
| <span id="XAUDIO2_E_XAPO_CREATION_FAILED"></span><span id="xaudio2_e_xapo_creation_failed"></span><dl> <dt>**XAUDIO2 \_ \_ \_ \_ Échec**</dt> de la création de XAPO <dt>0x88960003</dt> </dl> | Échec de l’instanciation d’un effet.<br/>                                                                                                                                                                                                                                                                                                                       |
| <span id="XAUDIO2_E_DEVICE_INVALIDATED"></span><span id="xaudio2_e_device_invalidated"></span><dl> <dt>**XAUDIO2 \_ 0x88960004 de l' \_ appareil \_ invalidée**</dt> <dt></dt> </dl>        | Un périphérique audio est devenu inutilisable par le biais d’un débranchement ou d’un autre événement.<br/>                                                                                                                                                                                                                                                                           |



## <a name="remarks"></a>Remarques

### <a name="platform-requirements"></a>Conditions requises par la plateforme

Windows 10 (xaudio 2.9); Windows 8, Windows Phone 8 (XAudio 2,8); SDK DirectX (XAudio 2,7)

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|--------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Xaudio2. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[XAudio2 :: constants](constants.md)
</dt> </dl>

 

 




