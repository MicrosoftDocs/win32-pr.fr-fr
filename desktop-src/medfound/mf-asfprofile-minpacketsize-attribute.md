---
description: Spécifie la taille minimale des paquets pour un fichier ASF, en octets.
ms.assetid: 22e5725d-de55-4a0c-a6cc-1ed9f20e7663
title: Attribut MF_ASFPROFILE_MINPACKETSIZE (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d8e1aaea4fe1dfc2c6e01e969bc8b588ac21e50
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106521824"
---
# <a name="mf_asfprofile_minpacketsize-attribute"></a>\_ \_ Attribut MINPACKETSIZE ASFPROFILE MF

Spécifie la taille minimale des paquets pour un fichier ASF, en octets.

## <a name="data-type"></a>Type de données

**UINT32**

## <a name="remarks"></a>Notes

Cet attribut s’applique aux objets de profil ASF. Pour définir cet attribut, utilisez l’interface [**IMFASFProfile**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfprofile) .

La constante GUID de cet attribut est exportée à partir de mfuuid. lib.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                           |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                     |
| En-tête<br/>                   | <dl> <dt>Wmcontainer. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Attributs ASF](asf-attributes.md)
</dt> <dt>

[**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> </dl>

 

 




