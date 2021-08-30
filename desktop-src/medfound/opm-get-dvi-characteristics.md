---
description: Demande si un connecteur DVI (Digital Video Interface) prend en charge DVI version 1,1 ou ultérieure.
ms.assetid: b6c450c0-e97f-472d-ae09-fa1e062aeb9e
title: OPM_GET_DVI_CHARACTERISTICS (Opmapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f507d9d9c1f1df0efe1b3c5b0696c178ed6fdfe5d285fde2eb5d1def62e8d007
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119887429"
---
# <a name="opm_get_dvi_characteristics"></a>\_ \_ caractéristiques DVI de l’offre OPM \_

Demande si un connecteur DVI (Digital Video Interface) prend en charge DVI version 1,1 ou ultérieure.



| Condition requise | Valeur |
|--------------|-----------------------------------------------------------------------------|
| GUID de la demande | \_ \_ caractéristiques DVI de l’offre OPM \_                                              |
| Données d’entrée   | Aucun                                                                        |
| Retourner les données  | Structure [**d' \_ \_ informations standard OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) |



 

## <a name="remarks"></a>Remarques

Si cette requête est réussie, le membre **ulInformation** de la structure d' [**\_ \_ informations standard OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) contient l’une des valeurs suivantes.



| Valeur                                     | Description               |
|-------------------------------------------|---------------------------|
| \_Caractéristique DVI \_ OPM \_ 1 \_ 0            | Version DVI 1,0.          |
| \_Caractéristique DVI \_ OPM \_ 1 \_ 1 \_ ou \_ supérieure | DVI version 1,1 ou ultérieure. |



 

Cette requête est prise en charge uniquement lorsque le type de connecteur physique est le type de \_ connecteur OPM \_ \_ DVI. Pour obtenir le type de connecteur, envoyez la requête de [**\_ \_ \_ type obtenir le connecteur OPM**](opm-get-connector-type.md) .

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

 

 




