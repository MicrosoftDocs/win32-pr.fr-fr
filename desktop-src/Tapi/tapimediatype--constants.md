---
description: Les constantes de type de média sont définies ci-dessous.
ms.assetid: 3e418c9a-a008-4b94-b5d2-7c2eccb3bf87
title: Constantes TAPIMEDIATYPE_ (Tapi3. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d71a7d7ffb411d84e99863bb89274e43200b319d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127311146"
---
# <a name="tapimediatype_-constants"></a>\_Constantes TAPIMEDIATYPE

Les types de média suivants sont définis :



| Constante/valeur                                                                                                                                                                                                                                              | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TAPIMEDIATYPE_AUDIO"></span><span id="tapimediatype_audio"></span><dl> <dt>**TAPIMEDIATYPE \_ AUDIO**</dt> <dt>0x8</dt> </dl>                    | Flux multimédia audio qui entre ou quitte l’ordinateur. Une entrée de flux multimédia est généralement lue sur les intervenants, ou envoyée à un appareil combiné et un flux de sortie est généralement capturé via un microphone ou un appareil combiné.<br/>                                                                                                                                                                                                                                      |
| <span id="TAPIMEDIATYPE_VIDEO"></span><span id="tapimediatype_video"></span><dl> <dt>**TAPIMEDIATYPE \_ VIDÉO**</dt> <dt>0x8000</dt> </dl>                 | Flux de média vidéo qui entre ou quitte l’ordinateur. Une entrée de flux multimédia est généralement rendue dans une fenêtre vidéo et un flux multimédia de sortie est généralement capturé avec une caméra vidéo.<br/>                                                                                                                                                                                                                                                                         |
| <span id="TAPIMEDIATYPE_DATAMODEM"></span><span id="tapimediatype_datamodem"></span><dl> <dt>**TAPIMEDIATYPE \_ DATAMODEM**</dt> <dt>0x10</dt> </dl>       | Flux de données multimédia qui est associé à un modem de données.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="TAPIMEDIATYPE_G3FAX"></span><span id="tapimediatype_g3fax"></span><dl> <dt>**TAPIMEDIATYPE \_ G3FAX**</dt> <dt>0x20</dt> </dl>                   | Flux de données multimédia associé à une télécopie de protocole G3.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="TAPIMEDIATYPE_MULTITRACK"></span><span id="tapimediatype_multitrack"></span><dl> <dt>**TAPIMEDIATYPE \_**</dt> <dt>0x10000</dt> multipiste </dl> | Un flux se trouve sur un terminal multipiste.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| <span id="MEDIATYPE_RTP_Single_Stream"></span><span id="mediatype_rtp_single_stream"></span><span id="MEDIATYPE_RTP_SINGLE_STREAM"></span><dl> <dt>**\_ \_ Flux unique de MediaType RTP \_**</dt> </dl>     | Ce GUID est utilisé entre un terminal fourni par une application et le flux du MSP. Si le code pin du terminal prend en charge ce type de média, le flux échangera des données RTP brutes avec le terminal. ce mode est pris en charge uniquement par les flux vidéo sur le msp H323 et IPConf msp pour Windows 2000 SP1 ou version ultérieure.<br/> **En-tête :** Déclaré dans ipmsp. h. l’en-tête ipmsp. h n’est pas disponible dans dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation. <br/> |



## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------|------------------------------------------------------------------------------------|
| Version TAPI<br/> | Nécessite TAPI 3,0 ou une version ultérieure<br/>                                              |
| En-tête<br/>       | <dl> <dt>Tapi3. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ITQOSEvent :: obtient le \_ MediaType**](/windows/desktop/api/tapi3if/nf-tapi3if-itqosevent-get_mediatype)
</dt> <dt>

[**ITAMMediaFormat :: obtient \_ MediaFormat**](/windows/win32/api/tapi3/nf-tapi3-itammediaformat-get_mediaformat)
</dt> <dt>

[**ITAMMediaFormat ::p ut \_ MediaFormat**](/windows/win32/api/tapi3/nf-tapi3-itammediaformat-put_mediaformat)
</dt> <dt>

[**ITCallInfo :: obtient \_ CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong)
</dt> <dt>

[**ITMediaSupport :: obtient \_ MediaTypes**](/windows/desktop/api/tapi3if/nf-tapi3if-itmediasupport-get_mediatypes)
</dt> <dt>

[**ITTerminalSupport::CreateTerminal**](/windows/win32/api/tapi3if/nf-tapi3if-itterminalsupport-createterminal)
</dt> </dl>

 

