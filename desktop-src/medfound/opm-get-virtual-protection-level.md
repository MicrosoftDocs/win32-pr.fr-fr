---
description: Retourne le niveau de protection virtuel pour un mécanisme de protection spécifié.
ms.assetid: 635d54de-2735-4390-8bac-ba63b9503909
title: OPM_GET_VIRTUAL_PROTECTION_LEVEL (Opmapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c7ac36abd0a043a74a18401205bbb5e661ac17d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106529723"
---
# <a name="opm_get_virtual_protection_level"></a>\_niveau de \_ \_ protection \_ de l’offre OPM

Retourne le niveau de protection virtuel pour un mécanisme de protection spécifié.

Le niveau de protection *virtuel* est le niveau demandé par l’application lors de la session de la sortie de protection actuelle (OPM). Le pilote peut appliquer un niveau supérieur, en raison d’événements en dehors de cette session OPM. Pour trouver le niveau de protection réel en vigueur, envoyez la requête [**d' \_ extraction \_ de \_ \_ niveau de protection OPM**](opm-get-actual-protection-level.md) .



| Condition requise | Valeur |
|--------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| GUID de la demande | \_niveau de \_ \_ protection \_ de l’offre OPM                                                                                                                                          |
| Données d’entrée   | Mécanisme de protection à interroger, spécifié sous la forme d’un entier 32 bits. La valeur est interprétée comme un membre des [**indicateurs de type de protection OPM**](opm-protection-type-flags.md). |
| Retourner les données  | Structure [**d' \_ \_ informations standard OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information)                                                                                                   |



 

## <a name="remarks"></a>Notes

Le niveau de protection est retourné dans le membre **ulInformation** de la structure d' [**\_ \_ informations standard OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) . La signification de cette valeur dépend du mécanisme de protection qui est interrogé. Pour chaque mécanisme de protection, la valeur de **ulInformation** est un indicateur d’une énumération différente, comme indiqué dans le tableau suivant.



| Mécanisme de protection | Énumération                                                       |
|----------------------|-------------------------------------------------------------------|
| ACP                  | [**niveau de protection de l' \_ ACP OPM \_ \_**](/windows/desktop/api/opmapi/ne-opmapi-opm_acp_protection_level)   |
| CGMS-A               | [**Indicateurs de protection de CGMS-A**](cgms-a-protection-flags.md)        |
| DPCP                 | [**\_niveau de \_ protection \_ DPCP OPM**](/windows/desktop/api/opmapi/ne-opmapi-opm_dpcp_protection_level) |
| HDCP                 | [**niveau de protection pour OPM \_ HDCP \_ \_**](/windows/desktop/api/opmapi/ne-opmapi-opm_hdcp_protection_level) |



 

Cette requête est équivalente à la \_ requête DXVA COPPQueryLocalProtectionLevel utilisée dans le protocole Copp (Certified Output Protection Protocol).

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

 

 




