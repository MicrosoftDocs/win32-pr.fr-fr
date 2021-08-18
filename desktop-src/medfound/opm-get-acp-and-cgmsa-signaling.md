---
description: 'En savoir plus sur : OPM_GET_ACP_AND_CGMSA_SIGNALING'
ms.assetid: d477fe3e-4498-450b-93b7-ce74ae9ed005
title: OPM_GET_ACP_AND_CGMSA_SIGNALING (Opmapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a6c06da78ea9ae1a4f0ea58f0fb8770dffadff6a34d577fd2328816ffc100e4c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119102063"
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



 

## <a name="remarks"></a>Remarques

Cette requête est équivalente à la \_ requête DXVA COPPQuerySignaling utilisée dans le protocole Copp (Certified Output Protection Protocol).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                      |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>Opmapi. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IOPMVideoOutput :: COPPCompatibleGetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-coppcompatiblegetinformation)
</dt> <dt>

[**IOPMVideoOutput :: GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation)
</dt> <dt>

[Demandes d’État OPM](opm-status-requests.md)
</dt> </dl>

 

 




