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
# <a name="direct3d-11-video-guids"></a><span data-ttu-id="73412-103">GUID vidéo Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="73412-103">Direct3D 11 Video GUIDs</span></span>

<span data-ttu-id="73412-104">Les GUID suivants prennent en charge les API vidéo Direct3D 11.</span><span class="sxs-lookup"><span data-stu-id="73412-104">The following GUIDs support Direct3D 11 Video APIs.</span></span>

<dl> <dt>

<span data-ttu-id="73412-105"><span id="D3D11_KEY_EXCHANGE_HW_PROTECTION"></span><span id="d3d11_key_exchange_hw_protection"></span>**\_Protection du \_ matériel d’échange de clés d3d11 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="73412-105"><span id="D3D11_KEY_EXCHANGE_HW_PROTECTION"></span><span id="d3d11_key_exchange_hw_protection"></span>**D3D11\_KEY\_EXCHANGE\_HW\_PROTECTION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="73412-106">Indique que le décodeur doit recevoir les données d’un composant DRM matériel</span><span class="sxs-lookup"><span data-stu-id="73412-106">Indicates that the decoder will receive data from a hardware-based DRM component</span></span>

<span data-ttu-id="73412-107">**D3d11 \_ La \_ \_ \_ protection du matériel d’échange de clés** peut être spécifiée dans le paramètre *pKeyExchangeType* de la fonction [**ID3D11VideoDevice :: CreateCryptoSession**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-createcryptosession) pour indiquer que l’interface [**ID3D11CryptoSession**](/windows/desktop/api/d3d11/nn-d3d11-id3d11cryptosession) sera utilisée uniquement pour la communication entre un composant DRM en mode utilisateur et l’environnement d’exécution sécurisé.</span><span class="sxs-lookup"><span data-stu-id="73412-107">**D3D11\_KEY\_EXCHANGE\_HW\_PROTECTION** can be specified in the *pKeyExchangeType* parameter of the [**ID3D11VideoDevice::CreateCryptoSession**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-createcryptosession) function to indicate that the [**ID3D11CryptoSession**](/windows/desktop/api/d3d11/nn-d3d11-id3d11cryptosession) interface will be used purely for communication between a user mode DRM component and the secure execution environment.</span></span>

<span data-ttu-id="73412-108">Quand ce GUID est spécifié, les méthodes suivantes ne doivent pas être appelées :</span><span class="sxs-lookup"><span data-stu-id="73412-108">When this GUID is specified, the following methods should not be called:</span></span>

-   [<span data-ttu-id="73412-109">**ID3D11CryptoSession::GetCertificateSize**</span><span class="sxs-lookup"><span data-stu-id="73412-109">**ID3D11CryptoSession::GetCertificateSize**</span></span>](/windows/desktop/api/d3d11/nf-d3d11-id3d11cryptosession-getcertificatesize)
-   [<span data-ttu-id="73412-110">**ID3D11CryptoSession :: GetCertificate**</span><span class="sxs-lookup"><span data-stu-id="73412-110">**ID3D11CryptoSession::GetCertificate**</span></span>](/windows/desktop/api/d3d11/nf-d3d11-id3d11cryptosession-getcertificate)
-   [<span data-ttu-id="73412-111">**ID3D11VideoContext::EncryptionBlt**</span><span class="sxs-lookup"><span data-stu-id="73412-111">**ID3D11VideoContext::EncryptionBlt**</span></span>](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-encryptionblt)
-   [<span data-ttu-id="73412-112">**ID3D11VideoContext ::D ecryptionBlt**</span><span class="sxs-lookup"><span data-stu-id="73412-112">**ID3D11VideoContext::DecryptionBlt**</span></span>](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-decryptionblt)
-   [<span data-ttu-id="73412-113">**ID3D11VideoContext::StartSessionKeyRefresh**</span><span class="sxs-lookup"><span data-stu-id="73412-113">**ID3D11VideoContext::StartSessionKeyRefresh**</span></span>](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-startsessionkeyrefresh)
-   [<span data-ttu-id="73412-114">**ID3D11VideoContext::FinishSessionKeyRefresh**</span><span class="sxs-lookup"><span data-stu-id="73412-114">**ID3D11VideoContext::FinishSessionKeyRefresh**</span></span>](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-finishsessionkeyrefresh)
-   [<span data-ttu-id="73412-115">**ID3D11VideoContext::GetEncryptionBltKey**</span><span class="sxs-lookup"><span data-stu-id="73412-115">**ID3D11VideoContext::GetEncryptionBltKey**</span></span>](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-getencryptionbltkey)


</dt> </dl> </dd> <dt>

<span data-ttu-id="73412-116"><span id="D3D11_DECODER_ENCRYPTION_HW_CENC"></span><span id="d3d11_decoder_encryption_hw_cenc"></span>**D3D11 du \_ chiffrement du DÉcodeur \_ \_ \_ Cenc**</span><span class="sxs-lookup"><span data-stu-id="73412-116"><span id="D3D11_DECODER_ENCRYPTION_HW_CENC"></span><span id="d3d11_decoder_encryption_hw_cenc"></span>**D3D11\_DECODER\_ENCRYPTION\_HW\_CENC**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="73412-117">Indique que le décodeur doit recevoir les données d’un composant DRM matériel</span><span class="sxs-lookup"><span data-stu-id="73412-117">Indicates that the decoder will receive data from a hardware-based DRM component</span></span>

<span data-ttu-id="73412-118">La définition de ce GUID dans le membre **guidConfigBitstreamEncryption** de la structure de [**\_ \_ \_ configuration de décodeur vidéo d3d11**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_video_decoder_config) transmise à l’API [**ID3D11VideoDevice :: CreateVideoDecoder**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-createvideodecoder) indique que les paramètres suivants seront passés dans l’appel ID3D11VideoDevice [**::D ecoderbeginframe**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-decoderbeginframe) :</span><span class="sxs-lookup"><span data-stu-id="73412-118">Setting this GUID in the **guidConfigBitstreamEncryption** member of the [**D3D11\_VIDEO\_DECODER\_CONFIG**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_video_decoder_config) structure passed to the [**ID3D11VideoDevice::CreateVideoDecoder**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-createvideodecoder) API indicates that the following parameters will be passed in the [**ID3D11VideoDevice::DecoderBeginFrame**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-decoderbeginframe) call:</span></span>



|                  |                                                                                                                                                                                                                                                     |
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="73412-119">*ContentKeySize*</span><span class="sxs-lookup"><span data-stu-id="73412-119">*ContentKeySize*</span></span> | <span data-ttu-id="73412-120">Contient la taille de la structure de [**\_ \_ \_ \_ \_ \_ session de chiffrement de l’image de décodage vidéo d3d11**](/windows/desktop/api/d3d11_1/ns-d3d11_1-d3d11_video_decoder_begin_frame_crypto_session) .</span><span class="sxs-lookup"><span data-stu-id="73412-120">Contains the size of the [**D3D11\_VIDEO\_DECODER\_BEGIN\_FRAME\_CRYPTO\_SESSION**](/windows/desktop/api/d3d11_1/ns-d3d11_1-d3d11_video_decoder_begin_frame_crypto_session) structure.</span></span>                                                                                                  |
| <span data-ttu-id="73412-121">*pContentKey*</span><span class="sxs-lookup"><span data-stu-id="73412-121">*pContentKey*</span></span>    | <span data-ttu-id="73412-122">Pointeur vers une [**\_ \_ \_ \_ \_ \_ session de chiffrement de l’image de décodage vidéo d3d11**](/windows/desktop/api/d3d11_1/ns-d3d11_1-d3d11_video_decoder_begin_frame_crypto_session) , qui fournit le [**ID3D11CryptoSession**](/windows/desktop/api/d3d11/nn-d3d11-id3d11cryptosession) et les informations clés nécessaires pour déchiffrer le frame.</span><span class="sxs-lookup"><span data-stu-id="73412-122">A pointer to a [**D3D11\_VIDEO\_DECODER\_BEGIN\_FRAME\_CRYPTO\_SESSION**](/windows/desktop/api/d3d11_1/ns-d3d11_1-d3d11_video_decoder_begin_frame_crypto_session) providing the [**ID3D11CryptoSession**](/windows/desktop/api/d3d11/nn-d3d11-id3d11cryptosession) and the key information needed to decrypt the frame.</span></span> |



 


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="73412-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="73412-123">Requirements</span></span>



| <span data-ttu-id="73412-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="73412-124">Requirement</span></span> | <span data-ttu-id="73412-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="73412-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="73412-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="73412-126">Minimum supported client</span></span><br/> | <span data-ttu-id="73412-127">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="73412-127">Windows 10 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="73412-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="73412-128">Minimum supported server</span></span><br/> | <span data-ttu-id="73412-129">Applications de bureau Windows Server 2016 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="73412-129">Windows Server 2016 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="73412-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="73412-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="73412-131"><dt>D3d11. h</dt></span><span class="sxs-lookup"><span data-stu-id="73412-131"><dt>D3d11.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="73412-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="73412-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73412-133">API vidéo Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="73412-133">Direct3D 11 Video APIs</span></span>](direct3d-11-video-apis.md)
</dt> </dl>

 

 




