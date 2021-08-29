---
description: Pour un type de média qui décrit un flux de transport MPEG-2 (TS), spécifie si les paquets de transport contiennent des en-têtes de paquets de contenu.
ms.assetid: 527B965D-4330-4DCB-B6DA-32D6BCDF5515
title: Attribut MF_MT_MPEG2_CONTENT_PACKET (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fc650c28b6d02fdcbdedafcd2e173a501a763fbcfe4fa86a17c5cc98e0cdceba
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120012909"
---
# <a name="mf_mt_mpeg2_content_packet-attribute"></a>\_Attribut de \_ \_ paquet de contenu MPEG2 MT MT \_

Pour un type de média qui décrit un flux de transport MPEG-2 (TS), spécifie si les paquets de transport contiennent des en-têtes de paquets de contenu.

## <a name="data-type"></a>Type de données

**UINT32**



| Valeur                                                                                                | Signification                                                                                                                                                                                                            |
|------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="0"></span><dl> <dt>**entre**</dt> </dl> | Aucun en-tête de paquet de contenu n’est ajouté.<br/>                                                                                                                                                                    |
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | À des intervalles de 200 à 1 000 millisecondes, un en-tête de paquet de contenu de 14 octets est ajouté au début du paquet de transport, tel que défini par l’Association de la norme ARIB (Radio Industries and Business).<br/> |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8 \[ applications de bureau \| UWP apps\]<br/>                                  |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[ applications de bureau \| UWP apps\]<br/>                        |
| En-tête<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




