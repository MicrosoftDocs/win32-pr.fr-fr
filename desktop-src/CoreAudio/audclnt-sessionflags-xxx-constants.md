---
description: Les \_ \_ constantes AUDCLNT SESSIONFLAGS xxx indiquent les caractéristiques d’une session audio associée au flux.
ms.assetid: 5745d5bc-71e8-4b33-8227-c1c84226b6ee
title: Constantes AUDCLNT_SESSIONFLAGS_XXX (Audiosessiontypes. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15423d24d48a98b69c4ab1651941fba639885c03e27cf9df8b1834aab830bb6a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119018497"
---
# <a name="audclnt_sessionflags_xxx-constants"></a>AUDCLNT \_ SESSIONFLAGS \_ xxx, constantes

Les \_ \_ constantes AUDCLNT SESSIONFLAGS xxx indiquent les caractéristiques d’une session audio associée au flux. Un client peut spécifier ces options lors de l’initialisation du flux par le biais du paramètre *StreamFlags* de la méthode [**IAudioClient :: Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) .



| Constante/valeur                                                                                                                                                                                                                                                                                                                   | Description                                                                                                                                                                                                                                                                                                      |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="AUDCLNT_SESSIONFLAGS_EXPIREWHENUNOWNED"></span><span id="audclnt_sessionflags_expirewhenunowned"></span><dl> <dt>**AUDCLNT \_ SESSIONFLAGS \_ EXPIREWHENUNOWNED**</dt> <dt>0x10000000</dt> </dl>                       | La session expire lorsqu’il n’y a aucun flux associé et que les objets de contrôle de session propriétaire contiennent des références.<br/>                                                                                                                                                                                       |
| <span id="AUDCLNT_SESSIONFLAGS_DISPLAY_HIDE"></span><span id="audclnt_sessionflags_display_hide"></span><dl> <dt>**AUDCLNT \_ \_Affichage SESSIONFLAGS \_ Masquer**</dt> <dt>0x20000000</dt> </dl>                                     | Le contrôle du volume est masqué dans l’interface utilisateur du mélangeur de volume lors de la création de la session audio. Si la session associée au flux existe déjà avant que [**IAudioClient :: Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) ouvre le flux, le contrôle du volume est affiché dans le mélangeur de volume.<br/> |
| <span id="_AUDCLNT_SESSIONFLAGS_DISPLAY_HIDEWHENEXPIRED"></span><span id="_audclnt_sessionflags_display_hidewhenexpired"></span><dl> <dt> **AUDCLNT \_ SESSIONFLAGS \_ Display \_ HIDEWHENEXPIRED**</dt> <dt>0x40000000</dt> </dl> | Le contrôle du volume est masqué dans l’interface utilisateur du mélangeur de volume après l’expiration de la session. <br/>                                                                                                                                                                                                           |



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 uniquement\]<br/>                                                     |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 R2, \[ applications de bureau uniquement\]<br/>                                        |
| En-tête<br/>                   | <dl> <dt>Audiosessiontypes. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Constantes audio principales](core-audio-constants.md)
</dt> <dt>

[**IAudioSessionControl**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol)
</dt> </dl>

 

 




