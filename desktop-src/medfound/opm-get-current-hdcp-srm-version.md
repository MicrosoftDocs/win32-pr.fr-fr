---
description: Retourne le numéro de version du message de renouvellement du système (SRM) actuellement utilisé par la sortie vidéo.
ms.assetid: 65d4b98b-369f-4863-a28c-f9e3b4c2b55d
title: OPM_GET_CURRENT_HDCP_SRM_VERSION (Opmapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e05ad53ae58e2141c63179c84a90f90cea86fb4a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517580"
---
# <a name="opm_get_current_hdcp_srm_version"></a>Procurez-vous la \_ \_ \_ version actuelle HDCP \_ SRM \_

Retourne le numéro de version du message de renouvellement du système (SRM) actuellement utilisé par la sortie vidéo.



| Condition requise | Valeur |
|--------------|-----------------------------------------------------------------------------|
| GUID de la demande | Procurez-vous la \_ \_ \_ version actuelle HDCP \_ SRM \_                                       |
| Données d’entrée   | Aucun                                                                        |
| Retourner les données  | Structure [**d' \_ \_ informations standard OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) |



 

## <a name="remarks"></a>Notes

Si cette requête est réussie, le membre **ulInformation** de la structure d' [**\_ \_ informations standard OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) contient le numéro de version de SRM, au format Little endian.

Les SRMs sont utilisés pour mettre à jour la liste des appareils révoqués High-Bandwidth Digital protection du contenu (HDCP). Les SRMs sont fournis avec le contenu vidéo. Pour définir le SRM, envoyez la commande [**OPM \_ Set \_ HDCP \_ SRM**](opm-set-hdcp-srm.md) .

Cette requête peut provoquer la méthode [**IOPMVideoOutput :: GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation) pour retourner l’un des codes d’erreur suivants.



| Code de retour                                            | Description                             |
|--------------------------------------------------------|-----------------------------------------|
| ERREUR \_ Graphics \_ OPM \_ HDCP \_ SRM \_ jamais \_ défini            | L’application n’a pas défini de SRM.     |
| ERREUR \_ Graphics la \_ \_ sortie OPM \_ ne \_ \_ prend pas en charge \_ HDCP | La sortie vidéo ne prend pas en charge HDCP. |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                      |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>Opmapi. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IOPMVideoOutput :: GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation)
</dt> <dt>

[Demandes d’État OPM](opm-status-requests.md)
</dt> </dl>

 

 




