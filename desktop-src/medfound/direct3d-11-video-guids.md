---
description: Les GUID suivants prennent en charge les API vidéo Direct3D 11.
ms.assetid: CF2F3058-328A-4128-B5C6-29723B49AB1E
title: GUID vidéo Direct3D 11 (D3d11. h)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d97a43285a59cf5196584b9be04fc36b02e5243f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104033807"
---
# <a name="direct3d-11-video-guids"></a>GUID vidéo Direct3D 11

Les GUID suivants prennent en charge les API vidéo Direct3D 11.

<dl> <dt>

<span id="D3D11_KEY_EXCHANGE_HW_PROTECTION"></span><span id="d3d11_key_exchange_hw_protection"></span>**\_Protection du \_ matériel d’échange de clés d3d11 \_ \_**
</dt> <dd> <dl> <dt>



Indique que le décodeur doit recevoir les données d’un composant DRM matériel

**D3d11 \_ La \_ \_ \_ protection du matériel d’échange de clés** peut être spécifiée dans le paramètre *pKeyExchangeType* de la fonction [**ID3D11VideoDevice :: CreateCryptoSession**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-createcryptosession) pour indiquer que l’interface [**ID3D11CryptoSession**](/windows/desktop/api/d3d11/nn-d3d11-id3d11cryptosession) sera utilisée uniquement pour la communication entre un composant DRM en mode utilisateur et l’environnement d’exécution sécurisé.

Quand ce GUID est spécifié, les méthodes suivantes ne doivent pas être appelées :

-   [**ID3D11CryptoSession::GetCertificateSize**](/windows/desktop/api/d3d11/nf-d3d11-id3d11cryptosession-getcertificatesize)
-   [**ID3D11CryptoSession :: GetCertificate**](/windows/desktop/api/d3d11/nf-d3d11-id3d11cryptosession-getcertificate)
-   [**ID3D11VideoContext::EncryptionBlt**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-encryptionblt)
-   [**ID3D11VideoContext ::D ecryptionBlt**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-decryptionblt)
-   [**ID3D11VideoContext::StartSessionKeyRefresh**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-startsessionkeyrefresh)
-   [**ID3D11VideoContext::FinishSessionKeyRefresh**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-finishsessionkeyrefresh)
-   [**ID3D11VideoContext::GetEncryptionBltKey**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-getencryptionbltkey)


</dt> </dl> </dd> <dt>

<span id="D3D11_DECODER_ENCRYPTION_HW_CENC"></span><span id="d3d11_decoder_encryption_hw_cenc"></span>**D3D11 du \_ chiffrement du DÉcodeur \_ \_ \_ Cenc**
</dt> <dd> <dl> <dt>



Indique que le décodeur doit recevoir les données d’un composant DRM matériel

La définition de ce GUID dans le membre **guidConfigBitstreamEncryption** de la structure de [**\_ \_ \_ configuration de décodeur vidéo d3d11**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_video_decoder_config) transmise à l’API [**ID3D11VideoDevice :: CreateVideoDecoder**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-createvideodecoder) indique que les paramètres suivants seront passés dans l’appel ID3D11VideoDevice [**::D ecoderbeginframe**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-decoderbeginframe) :



|                  |                                                                                                                                                                                                                                                     |
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *ContentKeySize* | Contient la taille de la structure de [**\_ \_ \_ \_ \_ \_ session de chiffrement de l’image de décodage vidéo d3d11**](/windows/desktop/api/d3d11_1/ns-d3d11_1-d3d11_video_decoder_begin_frame_crypto_session) .                                                                                                  |
| *pContentKey*    | Pointeur vers une [**\_ \_ \_ \_ \_ \_ session de chiffrement de l’image de décodage vidéo d3d11**](/windows/desktop/api/d3d11_1/ns-d3d11_1-d3d11_video_decoder_begin_frame_crypto_session) , qui fournit le [**ID3D11CryptoSession**](/windows/desktop/api/d3d11/nn-d3d11-id3d11cryptosession) et les informations clés nécessaires pour déchiffrer le frame. |



 


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 10 uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2016 \[ uniquement\]<br/>                               |
| En-tête<br/>                   | <dl> <dt>D3d11. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[API vidéo Direct3D 11](direct3d-11-video-apis.md)
</dt> </dl>

 

 




