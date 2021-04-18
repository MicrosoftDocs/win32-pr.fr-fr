---
description: 'En savoir plus sur : OPM_GET_ACP_AND_CGMSA_SIGNALING'
ms.assetid: d477fe3e-4498-450b-93b7-ce74ae9ed005
title: OPM_GET_ACP_AND_CGMSA_SIGNALING (Opmapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5bf6294c3f1d90ac8a2292c65b3c1b8558e69220
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106536344"
---
# <a name="opm_get_acp_and_cgmsa_signaling"></a>\_prise en \_ main \_ des signaux ACP et \_ CGMSA \_ pour OPM

Retourne les informations suivantes sur une sortie vidéo :

-   Liste des normes de protection de la télévision prises en charge par le pilote.
-   Norme actuellement active.
-   Proportions actuelles ou autres données de signalisation.



| Condition requise | Valeur |
|--------------|-------------------------------------------------------------------------------------|
| GUID de la demande | \_prise en \_ main \_ des signaux ACP et \_ CGMSA \_ pour OPM                                                |
| Données d’entrée   | Aucun                                                                                |
| Retourner les données  | Une [**structure \_ \_ de \_ \_ signalisation ACP et CGMSA OPM**](/windows/desktop/api/opmapi/ns-opmapi-opm_acp_and_cgmsa_signaling) |



 

## <a name="remarks"></a>Notes

Cette requête est équivalente à la \_ requête DXVA COPPQuerySignaling utilisée dans le protocole Copp (Certified Output Protection Protocol).

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

 

 




