---
description: Retourne l’identificateur unique de l’analyseur associé à cette sortie vidéo.
ms.assetid: d34d68ff-c513-483e-8619-4a9baa2a40ba
title: OPM_GET_OUTPUT_ID (Opmapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6146c07be3467e513b33f636bde78e699f3e0d6d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127296267"
---
# <a name="opm_get_output_id"></a>ID de sortie de l' \_ extraction OPM \_ \_

Retourne l’identificateur unique de l’analyseur associé à cette sortie vidéo.



| Condition requise | Valeur |
|--------------|------------------------------------------------------------------|
| GUID de la demande | ID de sortie de l' \_ extraction OPM \_ \_                                             |
| Données d’entrée   | None                                                             |
| Retourner les données  | Structure de données de l' [**\_ ID de sortie \_ \_ OPM**](/windows/desktop/api/opmapi/ns-opmapi-opm_output_id_data) |



 

## <a name="remarks"></a>Notes

Le pilote vidéo attribue un identificateur unique à chaque analyse. Cette requête retourne l’identificateur pour l’analyse associée au pointeur [**IOPMVideoOutput**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) actuel.

## <a name="requirements"></a>Spécifications



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

 

 




