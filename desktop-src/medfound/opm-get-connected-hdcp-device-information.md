---
description: 'En savoir plus sur : OPM_GET_CONNECTED_HDCP_DEVICE_INFORMATION'
ms.assetid: 71fa9a99-83e4-4b27-9fd1-5a9dc3070820
title: OPM_GET_CONNECTED_HDCP_DEVICE_INFORMATION (Opmapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7561a348588b1244a6763eb447affa2b330e9c51
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127525688"
---
# <a name="opm_get_connected_hdcp_device_information"></a>\_ \_ \_ \_ informations sur l’appareil HDCP \_ connexion à OPM

Obtient des informations sur un appareil High-Bandwidth Digital protection du contenu (HDCP) attaché à la sortie vidéo. Les informations suivantes sont retournées :

-   Le vecteur de sélection de clé HDCP de l’appareil (KSV).
-   Indique si l’appareil est un répétiteur HDCP.



| Condition requise | Valeur |
|--------------|---------------------------------------------------------------------------------------------------------|
| GUID de la demande | \_ \_ \_ \_ informations sur l’appareil HDCP \_ connexion à OPM                                                          |
| Données d’entrée   | None                                                                                                    |
| Retourner les données  | Structure [**d' \_ \_ informations d' \_ appareil \_ HDCP connectée à OPM**](/windows/desktop/api/opmapi/ns-opmapi-opm_connected_hdcp_device_information) |



 

## <a name="remarks"></a>Notes

Cette requête peut être utilisée uniquement avec le *mode d’émulation Copp*. Si l’interface [**IOPMVideoOutput**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) utilise la sémantique de sortie Protection Manager (OPM), cette demande d’État n’est pas prise en charge.

KSV est un identificateur fourni au fabricant de l’appareil et est utilisé dans le processus d’authentification et d’installation HDCP. En mode émulation COPP, l’application utilise KSV pour déterminer si l’appareil HDCP est révoqué. Si c’est le cas, l’application ne doit pas lire de contenu protégé. En outre, l’application ne doit pas lire de contenu protégé si l’appareil est un répétiteur HDCP, car COPP ne prend pas en charge les répéteurs HDCP.

Cette requête n’est pas nécessaire lorsque la sémantique OPM est utilisée, car OPM prend en charge la révocation des appareils et les répéteurs HDCP.

Cette requête est équivalente à la \_ requête DXVA COPPQueryHDCPKeyData utilisée dans le protocole Copp (Certified Output Protection Protocol).

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                      |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>Opmapi. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IOPMVideoOutput :: COPPCompatibleGetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-coppcompatiblegetinformation)
</dt> <dt>

[Demandes d’État OPM](opm-status-requests.md)
</dt> </dl>

 

 




