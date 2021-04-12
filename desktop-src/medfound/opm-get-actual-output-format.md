---
description: Retourne une description du signal vidéo qui est transmis sur le connecteur.
ms.assetid: 8464470f-49db-4559-80b2-02cfc473e30e
title: OPM_GET_ACTUAL_OUTPUT_FORMAT (Opmapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12eeca9bcf8fde670447afe4268a86ffa31b6a94
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318745"
---
# <a name="opm_get_actual_output_format"></a>\_format de \_ \_ sortie OPM \_ obtenu

Retourne une description du signal vidéo qui est transmis sur le connecteur.



| Condition requise | Valeur |
|--------------|------------------------------------------------------------------------------|
| GUID de la demande | \_format de \_ \_ sortie OPM \_ obtenu                                             |
| Données d’entrée   | Aucun                                                                         |
| Retourner les données  | Structure [**de \_ \_ \_ format de sortie réel OPM**](/windows/desktop/api/opmapi/ns-opmapi-opm_actual_output_format) |



 

## <a name="remarks"></a>Notes

Le signal vidéo transmis sur le connecteur n’a pas nécessairement le même format que le mode d’affichage du bureau. Par exemple, le mode d’affichage du Bureau peut être de 1024 x 768 pixels à 85 Hz, tandis que le connecteur peut être un connecteur S-Video qui transmet un signal vidéo à 720 x 480 pixels, 60/1.01 Hz entrelacé. Dans ce cas, le pilote retourne la résolution du signal S-Video, et non la résolution du bureau.

Cette requête est équivalente à la \_ requête DXVA COPPQueryDisplayData utilisée dans le protocole Copp (Certified Output Protection Protocol).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                      |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>Opmapi. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IOPMVideoOutput :: COPPCompatibleGetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-coppcompatiblegetinformation)
</dt> <dt>

[**IOPMVideoOutput :: GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation)
</dt> <dt>

[Demandes d’État OPM](opm-status-requests.md)
</dt> </dl>

 

 




