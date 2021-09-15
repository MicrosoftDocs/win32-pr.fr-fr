---
description: Demande si un connecteur DVI (Digital Video Interface) prend en charge DVI version 1,1 ou ultérieure.
ms.assetid: b6c450c0-e97f-472d-ae09-fa1e062aeb9e
title: OPM_GET_DVI_CHARACTERISTICS (Opmapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55a6f996b0397db509a45af6e243359c581df333
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127525681"
---
# <a name="opm_get_dvi_characteristics"></a>\_ \_ caractéristiques DVI de l’offre OPM \_

Demande si un connecteur DVI (Digital Video Interface) prend en charge DVI version 1,1 ou ultérieure.



| Condition requise | Valeur |
|--------------|-----------------------------------------------------------------------------|
| GUID de la demande | \_ \_ caractéristiques DVI de l’offre OPM \_                                              |
| Données d’entrée   | None                                                                        |
| Retourner les données  | Structure [**d' \_ \_ informations standard OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) |



 

## <a name="remarks"></a>Notes

Si cette requête est réussie, le membre **ulInformation** de la structure d' [**\_ \_ informations standard OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) contient l’une des valeurs suivantes.



| Valeur                                     | Description               |
|-------------------------------------------|---------------------------|
| \_Caractéristique DVI \_ OPM \_ 1 \_ 0            | Version DVI 1,0.          |
| \_Caractéristique DVI \_ OPM \_ 1 \_ 1 \_ ou \_ supérieure | DVI version 1,1 ou ultérieure. |



 

Cette requête est prise en charge uniquement lorsque le type de connecteur physique est le type de \_ connecteur OPM \_ \_ DVI. Pour obtenir le type de connecteur, envoyez la requête de [**\_ \_ \_ type obtenir le connecteur OPM**](opm-get-connector-type.md) .

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

 

 




