---
description: Désactive la conversion de la fréquence des images dans la MFT du processeur vidéo.
ms.assetid: 98AA7B3A-281C-427D-805E-5C4EE1EFAE21
title: Attribut MF_XVP_DISABLE_FRC (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1922705514c51308138f9f301a3681e598ca6278
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951390"
---
# <a name="mf_xvp_disable_frc-attribute"></a>XVP MF- \_ \_ désactiver l' \_ attribut FRC

Désactive la conversion de la fréquence des images dans la [**MFT du processeur vidéo**](video-processor-mft.md).

## <a name="data-type"></a>Type de données

**Bool** stocké comme **UInt32**

## <a name="remarks"></a>Notes

Si cet attribut a la **valeur true**, le processeur vidéo n’effectue pas de conversion de la cadence d’images. Par défaut, le processeur vidéo convertit la fréquence d’images pour qu’elle corresponde au type de média de sortie.

Pour définir cet attribut :

1.  Appelez [**IMFTransform :: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) sur le processeur vidéo.
2.  Appelez [**IMFAttributes :: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

Définissez l’attribut avant le début de la diffusion en continu.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 8 uniquement\]<br/>                                         |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2012 \[ uniquement\]<br/>                               |
| En-tête<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




