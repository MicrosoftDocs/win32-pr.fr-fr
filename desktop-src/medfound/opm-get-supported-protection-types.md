---
description: Retourne la liste des mécanismes de protection pris en charge par le connecteur.
ms.assetid: dd4cdd3c-6bb5-4427-827d-f3e909e752e5
title: OPM_GET_SUPPORTED_PROTECTION_TYPES (Opmapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1dc79b33673e34d00914b84165d915baa0d8f56
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127235908"
---
# <a name="opm_get_supported_protection_types"></a>\_types de \_ \_ protection compatibles \_ avec OPM

Retourne la liste des mécanismes de protection pris en charge par le connecteur.



| Condition requise | Valeur |
|--------------|-----------------------------------------------------------------------------|
| GUID de la demande | \_types de \_ \_ protection compatibles \_ avec OPM                                      |
| Données d’entrée   | None                                                                        |
| Retourner les données  | Structure [**d' \_ \_ informations standard OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) |



 

## <a name="remarks"></a>Notes

Les mécanismes de protection sont retournés dans le membre **ulInformation** de la structure d' [**\_ \_ informations standard OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) . La valeur est **une opération or** au niveau du bit des indicateurs de type de [protection OPM](opm-protection-type-flags.md).

Cette requête est équivalente à la \_ requête DXVA COPPQueryProtectionType utilisée dans le protocole Copp (Certified Output Protection Protocol).

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

 

 




