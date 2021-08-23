---
description: Retourne le numéro de version du message de renouvellement du système (SRM) actuellement utilisé par la sortie vidéo.
ms.assetid: 65d4b98b-369f-4863-a28c-f9e3b4c2b55d
title: OPM_GET_CURRENT_HDCP_SRM_VERSION (Opmapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee36516510d04fec067bbc692387e2e36b9da083db1a6daae0f51948a992cc83
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119887489"
---
# <a name="opm_get_current_hdcp_srm_version"></a>Procurez-vous la \_ \_ \_ version actuelle HDCP \_ SRM \_

Retourne le numéro de version du message de renouvellement du système (SRM) actuellement utilisé par la sortie vidéo.



| Condition requise | Valeur |
|--------------|-----------------------------------------------------------------------------|
| GUID de la demande | Procurez-vous la \_ \_ \_ version actuelle HDCP \_ SRM \_                                       |
| Données d’entrée   | Aucun                                                                        |
| Retourner les données  | Structure [**d' \_ \_ informations standard OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) |



 

## <a name="remarks"></a>Remarques

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
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                      |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>Opmapi. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IOPMVideoOutput :: GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation)
</dt> <dt>

[Demandes d’État OPM](opm-status-requests.md)
</dt> </dl>

 

 




