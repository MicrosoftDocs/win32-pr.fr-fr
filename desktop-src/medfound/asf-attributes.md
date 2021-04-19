---
description: Attributs ASF
ms.assetid: c1570669-6e9c-4614-af4d-2a148f12e36f
title: Attributs ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5ccf09542c8b96cc262cbe029111d3cb74e5b53
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517216"
---
# <a name="asf-attributes"></a>Attributs ASF

### <a name="profile-attributes"></a>Attributs de profil

Les attributs suivants s’appliquent aux profils ASF.



| Attribut                                                                      | Description                                                  |
|--------------------------------------------------------------------------------|--------------------------------------------------------------|
| [**\_ASFPROFILE \_ MaxPacketSize**](mf-asfprofile-maxpacketsize-attribute.md) | Spécifie la taille maximale des paquets pour un fichier ASF, en octets. |
| [**\_MINPACKETSIZE ASFPROFILE \_ MF**](mf-asfprofile-minpacketsize-attribute.md) | Spécifie la taille minimale des paquets pour un fichier ASF, en octets. |



 

### <a name="stream-configuration-attributes"></a>Attributs de configuration de flux

Les attributs suivants s’appliquent à l’objet de configuration de flux ASF.



| Attribut                                                                              | Description                                                                   |
|----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| [**\_LEAKYBUCKET1 ASFSTREAMCONFIG \_ MF**](mf-asfstreamconfig-leakybucket1-attribute.md) | Définit les paramètres de « compartiment perdu » moyens pour l’encodage d’un fichier Windows Media. |
| [**\_LEAKYBUCKET2 ASFSTREAMCONFIG \_ MF**](mf-asfstreamconfig-leakybucket2-attribute.md) | Définit le pic des paramètres « compartiment perdu » pour l’encodage d’un fichier Windows Media.    |



 

### <a name="media-buffer-attributes"></a>Attributs du tampon de média

Les attributs suivants s’appliquent aux mémoires tampons de média pour les paquets ASF.



| Attribut                                                                          | Description                                                                               |
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [**\_limite du paquet MFASFSPLITTER \_**](mfasfsplitter-packet-boundary-attribute.md) | Spécifie si une mémoire tampon contient le début d’un paquet ASF (Advanced Systems Format). |



 

### <a name="presentation-descriptor-attributes"></a>Attributs du descripteur de présentation

Pour obtenir la liste des attributs qui s’appliquent aux descripteurs de présentation ASF, consultez attributs du descripteur de [Présentation](presentation-descriptor-attributes.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**IMFASFProfile**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfprofile)
</dt> <dt>

[**IMFASFStreamConfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig)
</dt> <dt>

[Attributs Media Foundation](media-foundation-attributes.md)
</dt> </dl>

 

 



