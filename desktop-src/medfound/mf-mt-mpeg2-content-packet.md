---
description: Pour un type de média qui décrit un flux de transport MPEG-2 (TS), spécifie si les paquets de transport contiennent des en-têtes de paquets de contenu.
ms.assetid: 527B965D-4330-4DCB-B6DA-32D6BCDF5515
title: Attribut MF_MT_MPEG2_CONTENT_PACKET (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: acb297081a150ab3aa5b842be9b5792d849e2457
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866573"
---
# <a name="mf_mt_mpeg2_content_packet-attribute"></a>\_Attribut de \_ \_ paquet de contenu MPEG2 MT MT \_

Pour un type de média qui décrit un flux de transport MPEG-2 (TS), spécifie si les paquets de transport contiennent des en-têtes de paquets de contenu.

## <a name="data-type"></a>Type de données

**UINT32**



| Valeur                                                                                                | Signification                                                                                                                                                                                                            |
|------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="0"></span><dl> <dt>**0**</dt> </dl> | Aucun en-tête de paquet de contenu n’est ajouté.<br/>                                                                                                                                                                    |
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | À des intervalles de 200 à 1 000 millisecondes, un en-tête de paquet de contenu de 14 octets est ajouté au début du paquet de transport, tel que défini par l’Association de la norme ARIB (Radio Industries and Business).<br/> |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications Windows 8 \[ Desktop Apps \| UWP\]<br/>                                  |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2012 \[ \| apps UWP\]<br/>                        |
| En-tête<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




