---
description: Retourne le type de connecteur physique de la sortie vidéo.
ms.assetid: c5862758-0125-4dbe-af72-5ed4a85bd702
title: OPM_GET_CONNECTOR_TYPE (Opmapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a95ca88b079aa93b4c2665fe7aa954eb58cfc1a9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201865"
---
# <a name="opm_get_connector_type"></a>\_type de \_ connecteur d’extraction OPM \_

Retourne le type de connecteur physique de la sortie vidéo.



| Condition requise | Valeur |
|--------------|-----------------------------------------------------------------------------|
| GUID de la demande | \_type de \_ connecteur d’extraction OPM \_                                                   |
| Données d’entrée   | Aucun                                                                        |
| Retourner les données  | Structure [**d' \_ \_ informations standard OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) |



 

## <a name="remarks"></a>Notes

Le type de connecteur est retourné dans le membre **ulInformation** de la structure d' [**\_ \_ informations standard OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) . La valeur de **ulInformation** est égale à l’un des types de connecteur listés dans les [**indicateurs de type de connecteur OPM**](opm-connector-type-flags.md).

En mode d’émulation COPP, le type de connecteur peut être combiné avec l’indicateur **\_ interne de \_ \_ \_ type \_ de connecteur compatible de OPM** . Utilisez une opération de bits **and** pour extraire le type de connecteur :

`ulInformation & ~OPM_COPP_COMPATIBLE_CONNECTOR_TYPE_INTERNAL`

Les applications doivent ignorer l’indicateur **\_ interne du \_ \_ \_ type \_ de connecteur compatible avec OPM Copp** . Pour plus d’informations, consultez la section Notes des [**indicateurs de type de connecteur OPM**](opm-connector-type-flags.md).

Cette requête est équivalente à la \_ requête DXVA COPPQueryConnectorType utilisée dans le protocole Copp (Certified Output Protection Protocol).

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

 

 




