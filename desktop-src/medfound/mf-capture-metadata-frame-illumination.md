---
description: Valeur indiquant si une image a été capturée à l’aide de l’éclairage infrarouge (active Infrared).
ms.assetid: D84772C8-902F-4302-8288-0430892A1896
title: Attribut MF_CAPTURE_METADATA_FRAME_ILLUMINATION (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb9aa60b5e921e99ac4f4c56cb4643af8389aa91
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514212"
---
# <a name="mf_capture_metadata_frame_illumination-attribute"></a>\_Attribut d' \_ \_ éclairage de trame de métadonnées de capture MF \_

\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation. Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]

Valeur indiquant si une image a été capturée à l’aide de l’éclairage infrarouge (active Infrared).

## <a name="data-type"></a>Type de données

**UINT64**

## <a name="remarks"></a>Notes

Cet attribut est un masque de masque. Il s’agit d’une valeur de bit de 64 pour la compatibilité descendante.

L’éclairage actif est lorsqu’un appareil a un émetteur de lumière proche de la caméra IR émettant un faisceau de lumière pour éclairer la scène, émettant généralement une lumière IR pour ne pas perturber les yeux humains. Affectez la valeur (valeur & 0x1) ! = 0 si le frame a été capturé quand l’éclairage actif était activé et défini (valeur & 0x1) = = 0 si l’éclairage actif était désactivé.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de bureau Windows 10, version 1709 \[ uniquement\]<br/>                          |
| Serveur minimal pris en charge<br/> | Windows Server, version 1709, \[ applications de bureau uniquement\]<br/>                      |
| En-tête<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



 

 




