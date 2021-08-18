---
description: Attributs ASF
ms.assetid: c1570669-6e9c-4614-af4d-2a148f12e36f
title: Attributs ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: babbb8697126ae6882c11526ed9e6cb31e2233b81685c820d200fbd21bab08c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118975028"
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
| [**\_LEAKYBUCKET1 ASFSTREAMCONFIG \_ MF**](mf-asfstreamconfig-leakybucket1-attribute.md) | définit les paramètres de la « plage de fuite » moyenne pour l’encodage d’un fichier multimédia Windows. |
| [**\_LEAKYBUCKET2 ASFSTREAMCONFIG \_ MF**](mf-asfstreamconfig-leakybucket2-attribute.md) | définit le pic des paramètres de « compartiment perdu » pour l’encodage d’un fichier multimédia Windows.    |



 

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

 

 



