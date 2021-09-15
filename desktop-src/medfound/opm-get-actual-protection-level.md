---
description: Retourne le niveau de protection global pour un mécanisme de protection spécifié.
ms.assetid: 3dd4f6f0-2305-4470-bbd4-7737fa2d8eae
title: OPM_GET_ACTUAL_PROTECTION_LEVEL (Opmapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 960d704fd44ca779f128795b26603698bb0ad622
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127525692"
---
# <a name="opm_get_actual_protection_level"></a>\_niveau de \_ \_ protection \_ de l’offre OPM

Retourne le niveau de protection global pour un mécanisme de protection spécifié.



| Condition requise | Valeur |
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| GUID de la demande | \_niveau de \_ \_ protection \_ de l’offre OPM                                                                                                                                       |
| Données d’entrée   | Mécanisme de protection à interroger, spécifié sous la forme d’un entier 32 bits. La valeur est interprétée comme un membre des [indicateurs de type de protection OPM](opm-protection-type-flags.md). |
| Retourner les données  | Structure [**d' \_ \_ informations standard OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information)                                                                                               |



 

## <a name="remarks"></a>Notes

Le niveau de protection global est le niveau de protection en cours d’application sur le connecteur, quelle que soit la façon dont le pilote Graphics a été invité à appliquer la protection. Par exemple, une application peut définir le niveau de protection ACP en appelant la fonction **ChangeDisplaySettingsEx** . Dans ce cas, le niveau de protection global reflète ce paramètre, même s’il n’a pas été demandé par le biais de Output Protection Manager (OPM).

Le niveau de protection est retourné dans le membre **ulInformation** de la structure d' [**\_ \_ informations standard OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) . La signification de cette valeur dépend du mécanisme de protection qui est interrogé. Pour chaque mécanisme de protection, la valeur de **ulInformation** est un indicateur d’une énumération différente, comme indiqué dans le tableau suivant.



| Mécanisme de protection | Énumération                                                       |
|----------------------|-------------------------------------------------------------------|
| ACP                  | [**niveau de protection de l' \_ ACP OPM \_ \_**](/windows/desktop/api/opmapi/ne-opmapi-opm_acp_protection_level)   |
| CGMS-A               | [Indicateurs de protection de CGMS-A](cgms-a-protection-flags.md)            |
| DPCP                 | [**\_niveau de \_ protection \_ DPCP OPM**](/windows/desktop/api/opmapi/ne-opmapi-opm_dpcp_protection_level) |
| HDCP                 | [**niveau de protection pour OPM \_ HDCP \_ \_**](/windows/desktop/api/opmapi/ne-opmapi-opm_hdcp_protection_level) |



 

Cette requête est équivalente à la \_ requête DXVA COPPQueryGlobalProtectionLevel utilisée dans le protocole Copp (Certified Output Protection Protocol).

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

[**IOPMVideoOutput :: GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation)
</dt> <dt>

[Demandes d’État OPM](opm-status-requests.md)
</dt> </dl>

 

 




