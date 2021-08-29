---
description: Spécifie si une application est autorisée à accéder à des trames vidéo non compressées.
ms.assetid: 7D2A9003-B36E-4082-877E-8AC7F5645E89
title: Attribut MFPROTECTION_VIDEO_FRAMES (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 35d8756ed823b110d2ca7834016183e6a1cecf5c8c2731f68a81fa4c9224fdb8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119355409"
---
# <a name="mfprotection_video_frames-attribute"></a>\_Attribut de \_ trames vidéo MFPROTECTION

Spécifie si une application est autorisée à accéder à des trames vidéo non compressées.

## <a name="data-type"></a>Type de données

**UINT32**

## <a name="remarks"></a>Remarques

La valeur 0 indique que l’application est autorisée à accéder aux frames. Cela peut être déterminé à la suite d’un accord privé entre l’application et le système de protection de contenu particulier en cours d’utilisation.

La valeur 1 indique que l’application est autorisée à accéder aux frames si un certificat d’application valide est fourni par l’application (voir [**IMFMediaEngineProtectedContent :: SetApplicationCertificate**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineprotectedcontent-setapplicationcertificate)).

La valeur 0xFFFFFFFF, qui est la valeur par défaut, indique qu’aucune application n’est autorisée à accéder à des frames non compressés.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8 \[ Applications UWP uniquement\]<br/>                                             |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[ Applications UWP uniquement\]<br/>                                   |
| En-tête<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Attributs du type de média](media-type-attributes.md)
</dt> </dl>

 

 




