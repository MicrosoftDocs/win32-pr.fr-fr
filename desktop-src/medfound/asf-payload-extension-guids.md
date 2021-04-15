---
description: Les GUID suivants définissent les extensions de charge utile pour les flux ASF (Advanced Systems Format).
ms.assetid: db973b41-1e5c-4bc8-921d-5e9312eb21cb
title: GUID d’extension de charge utile ASF (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb7dbd27212c8f4812360ba22f89a717659307f6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524663"
---
# <a name="asf-payload-extension-guids"></a>GUID d’extension de charge utile ASF

Les GUID suivants définissent les extensions de charge utile pour les flux ASF (Advanced Systems Format).



| Constante                                                                                                                                                                                                                                                                                      | Description                                                                                                                                                                      |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MFASFSampleExtension_SampleDuration"></span><span id="mfasfsampleextension_sampleduration"></span><span id="MFASFSAMPLEEXTENSION_SAMPLEDURATION"></span><dl> <dt>**MFASFSampleExtension \_ SampleDuration**</dt> </dl>         | Les données indiquent la durée, en millisecondes, de l’échantillon contenu dans l’objet buffer.<br/>                                                                       |
| <span id="MFASFSampleExtension_OutputCleanPoint"></span><span id="mfasfsampleextension_outputcleanpoint"></span><span id="MFASFSAMPLEEXTENSION_OUTPUTCLEANPOINT"></span><dl> <dt>**MFASFSampleExtension \_ OutputCleanPoint**</dt> </dl> | Les données indiquent si l’échantillon est une image clé. La valeur zéro indique que l’exemple n’est pas une image clé. Une valeur différente de zéro indique qu’il s’agit d’une image clé.<br/> |
| <span id="MFASFSampleExtension_SMPTE"></span><span id="mfasfsampleextension_smpte"></span><span id="MFASFSAMPLEEXTENSION_SMPTE"></span><dl> <dt>**\_SMPTE MFASFSampleExtension**</dt> </dl>                                             | Les données sont un code temporel SMPTE.<br/>                                                                                                                                        |
| <span id="MFASFSampleExtension_FileName"></span><span id="mfasfsampleextension_filename"></span><span id="MFASFSAMPLEEXTENSION_FILENAME"></span><dl> <dt>**\_Nom de fichier MFASFSampleExtension**</dt> </dl>                                 | Les données de l’exemple d’extension spécifient le nom du fichier à partir duquel le contenu de l’échantillon a été pris.<br/>                                                       |
| <span id="MFASFSampleExtension_ContentType"></span><span id="mfasfsampleextension_contenttype"></span><span id="MFASFSAMPLEEXTENSION_CONTENTTYPE"></span><dl> <dt>**\_ContentType MFASFSampleExtension**</dt> </dl>                     | Les données identifient le type de contenu que l’exemple contient.<br/>                                                                                                     |
| <span id="MFASFSampleExtension_PixelAspectRatio"></span><span id="mfasfsampleextension_pixelaspectratio"></span><span id="MFASFSAMPLEEXTENSION_PIXELASPECTRATIO"></span><dl> <dt>**MFASFSampleExtension \_ PixelAspectRatio**</dt> </dl> | Les données indiquent les proportions de pixels du contenu de l’échantillon.<br/>                                                                                               |



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                           |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                     |
| En-tête<br/>                   | <dl> <dt>Wmcontainer. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IMFASFStreamConfig::AddPayloadExtension**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-addpayloadextension)
</dt> <dt>

[**IMFASFStreamConfig::GetPayloadExtension**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-getpayloadextension)
</dt> <dt>

[Constantes Media Foundation](media-foundation-constants.md)
</dt> </dl>

 

 




