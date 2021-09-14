---
description: Pour un type de média qui décrit un flux de transport MPEG-2 (TS), spécifie que les paquets de transport contiennent un code d’heure de 4 octets.
ms.assetid: B172E7A8-5757-49B7-A784-FAFC7E904A4C
title: Attribut MF_MT_MPEG2_TIMECODE (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8bc9db5d7b3c6e94f7845bec2bd98c569d1b1f9c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127227712"
---
# <a name="mf_mt_mpeg2_timecode-attribute"></a>\_ \_ \_ Attribut code temporel MPEG2 MT

Pour un type de média qui décrit un flux de transport MPEG-2 (TS), spécifie que les paquets de transport contiennent un code d’heure de 4 octets.

## <a name="data-type"></a>Type de données

**UINT32**



| Valeur                                                                                                | Signification                                                                                                                                        |
|------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="0"></span><dl> <dt>**entre**</dt> </dl> | Aucun code d’heure n’est ajouté.<br/>                                                                                                              |
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | Un code d’heure de 4 octets est ajouté au début de chaque paquet de transport. Ce code de temps est requis par certaines normes de télévision numérique.<br/> |



 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8 \[ applications de bureau \| UWP apps\]<br/>                                  |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[ applications de bureau \| UWP apps\]<br/>                        |
| En-tête<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




