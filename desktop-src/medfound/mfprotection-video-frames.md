---
description: Spécifie si une application est autorisée à accéder à des trames vidéo non compressées.
ms.assetid: 7D2A9003-B36E-4082-877E-8AC7F5645E89
title: Attribut MFPROTECTION_VIDEO_FRAMES (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67a8ccfc56fb1c1b52b14e16d8e702111f3d8564
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106534189"
---
# <a name="mfprotection_video_frames-attribute"></a>\_Attribut de \_ trames vidéo MFPROTECTION

Spécifie si une application est autorisée à accéder à des trames vidéo non compressées.

## <a name="data-type"></a>Type de données

**UINT32**

## <a name="remarks"></a>Notes

La valeur 0 indique que l’application est autorisée à accéder aux frames. Cela peut être déterminé à la suite d’un accord privé entre l’application et le système de protection de contenu particulier en cours d’utilisation.

La valeur 1 indique que l’application est autorisée à accéder aux frames si un certificat d’application valide est fourni par l’application (voir [**IMFMediaEngineProtectedContent :: SetApplicationCertificate**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineprotectedcontent-setapplicationcertificate)).

La valeur 0xFFFFFFFF, qui est la valeur par défaut, indique qu’aucune application n’est autorisée à accéder à des frames non compressés.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | \[Applications UWP Windows 8 uniquement\]<br/>                                             |
| Serveur minimal pris en charge<br/> | Applications UWP Windows Server 2012 \[ uniquement\]<br/>                                   |
| En-tête<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Attributs du type de média](media-type-attributes.md)
</dt> </dl>

 

 




