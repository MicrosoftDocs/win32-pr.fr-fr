---
description: Les GUID suivants définissent les types de l’objet d’exclusion mutuelle pour les flux ASF (Advanced Systems Format).
ms.assetid: 3db8eebd-2e26-4c77-8f66-7d08436c9e42
title: GUID de type d’exclusion mutuelle ASF (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a6fedc766e26c35bb967054a704b732ca03e8a8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201183"
---
# <a name="asf-mutual-exclusion-type-guids"></a>GUID de type d’exclusion mutuelle ASF

Les GUID suivants définissent les types de l’objet d’exclusion mutuelle pour les flux ASF (Advanced Systems Format).



| Constante                                                                                                                                                                                                                                              | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MFASFMutexType_Language"></span><span id="mfasfmutextype_language"></span><span id="MFASFMUTEXTYPE_LANGUAGE"></span><dl> <dt>**\_Langue MFASFMutexType**</dt> </dl>                 | Les flux sont mutuellement exclusifs par langue. Ce type d’exclusion mutuelle est similaire à celui des pistes audio sur un DVD.<br/>                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="MFASFMutexType_Bitrate"></span><span id="mfasfmutextype_bitrate"></span><span id="MFASFMUTEXTYPE_BITRATE"></span><dl> <dt>**\_Débit binaire MFASFMutexType**</dt> </dl>                     | Les flux sont mutuellement exclusifs par vitesse de transmission. Ce type d’exclusion mutuelle est également appelé exclusion de la vitesse de transmission multiple (MBR).<br/>                                                                                                                                                                                                                                                                                                                                                        |
| <span id="MFASFMutexType_Presentation"></span><span id="mfasfmutextype_presentation"></span><span id="MFASFMUTEXTYPE_PRESENTATION"></span><dl> <dt>**\_Présentation MFASFMutexType**</dt> </dl> | Les flux sont mutuellement exclusifs par présentation. Ce type peut être utilisé pour de nombreux scénarios, mais il ne doit être utilisé que lorsque le contenu est identique, mais qu’il prend une forme différente. Par exemple, deux flux contenant la même vidéo, l’un mis en forme pour remplir l’écran et l’autre qui conserve les proportions d’un grand écran d’origine, doivent être rendus mutuellement exclusifs à l’aide de ce type. Un autre exemple est l’affichage de flux contenant des vidéos de la même scène à partir de différents angles.<br/> |
| <span id="MFASFMutexType_Unknown"></span><span id="mfasfmutextype_unknown"></span><span id="MFASFMUTEXTYPE_UNKNOWN"></span><dl> <dt>**MFASFMutexType \_ inconnu**</dt> </dl>                     | Les flux s’excluent mutuellement en fonction de critères personnalisés.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                           |



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                           |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                     |
| En-tête<br/>                   | <dl> <dt>Wmcontainer. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IMFASFMutualExclusion :: GetType**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmutualexclusion-gettype)
</dt> <dt>

[**IMFASFMutualExclusion::SetType**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmutualexclusion-settype)
</dt> <dt>

[Constantes Media Foundation](media-foundation-constants.md)
</dt> </dl>

 

 




