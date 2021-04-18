---
description: Retourne le type de bus d’e/s utilisé par la sortie vidéo.
ms.assetid: 1aff4c81-ffa0-4116-b7ea-60b1b83042df
title: OPM_GET_ADAPTER_BUS_TYPE (Opmapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: acde3611eb00977670c59c4326f793c1cb9037fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519583"
---
# <a name="opm_get_adapter_bus_type"></a>TYPE de bus d’accès de l' \_ \_ adaptateur OPM \_ \_

Retourne le type de bus d’e/s utilisé par la sortie vidéo.



| Condition requise | Valeur |
|--------------|-----------------------------------------------------------------------------|
| GUID de la demande | TYPE de bus d’accès de l' \_ \_ adaptateur OPM \_ \_                                                |
| Données d’entrée   | Aucun                                                                        |
| Retourner les données  | Structure [**d' \_ \_ informations standard OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) |



 

## <a name="remarks"></a>Notes

Le type de bus est retourné dans le membre **ulInformation** de la structure d' [**\_ \_ informations standard OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) . La valeur est **un or au niveau du** bit des indicateurs de type de [**bus OPM**](opm-bus-type-flags.md).

Cette requête est équivalente à la \_ requête DXVA COPPQueryBusData utilisée dans le protocole Copp (Certified Output Protection Protocol).

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

 

 




