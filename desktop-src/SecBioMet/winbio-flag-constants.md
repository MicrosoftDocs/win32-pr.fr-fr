---
title: Constantes WINBIO_FLAG ( \_ types WINBIO. h)
description: Spécifiez la configuration de l’unité biométrique et les caractéristiques d’accès pour la nouvelle session.
ms.assetid: 82b57023-6c27-433d-bf13-f136f501fc60
topic_type:
- apiref
api_name:
- WINBIO_FLAG_DEFAULT
- WINBIO_FLAG_BASIC
- WINBIO_FLAG_ADVANCED
- WINBIO_FLAG_RAW
- WINBIO_FLAG_MAINTENANCE
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ed632b5f15cc3d6a7ac6b0c6c70a2b3431b73db
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127416535"
---
# <a name="winbio_flag-constants"></a>\_Constantes d’indicateur WINBIO

Les constantes suivantes peuvent être utilisées dans la fonction [**WinBioOpenSession**](/windows/desktop/api/Winbio/nf-winbio-winbioopensession) pour spécifier la configuration de l’unité biométrique et les caractéristiques d’accès pour la nouvelle session.



| Constante                                                                                                                                                                                     | Description                                                                                                                                                                              |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_FLAG_DEFAULT"></span><span id="winbio_flag_default"></span><dl> <dt>**\_indicateur WINBIO \_ par défaut**</dt> </dl>             | Indicateur de configuration du capteur. Les unités biométriques fonctionnent de la manière spécifiée pendant l’installation.<br/>                                                                           |
| <span id="WINBIO_FLAG_BASIC"></span><span id="winbio_flag_basic"></span><dl> <dt>**indicateur WINBIO de \_ \_ base**</dt> </dl>                   | Indicateur de configuration du capteur. Les unités biométriques fonctionnent uniquement comme des périphériques de capture de base.<br/>                                                                                         |
| <span id="WINBIO_FLAG_ADVANCED"></span><span id="winbio_flag_advanced"></span><dl> <dt>**\_indicateur WINBIO \_ avancé**</dt> </dl>          | Indicateur de configuration du capteur. Les unités biométriques utilisent les capacités de traitement et de stockage interne.<br/>                                                                              |
| <span id="WINBIO_FLAG_RAW"></span><span id="winbio_flag_raw"></span><dl> <dt>**\_indicateur WINBIO \_ RAW**</dt> </dl>                         | Indicateur d’accès souhaité. L’application cliente capture les données biométriques brutes à l’aide de [**WinBioCaptureSample**](/windows/desktop/api/Winbio/nf-winbio-winbiocapturesample).<br/>                                             |
| <span id="WINBIO_FLAG_MAINTENANCE"></span><span id="winbio_flag_maintenance"></span><dl> <dt>**MAINTENANCE de l' \_ indicateur WINBIO \_**</dt> </dl> | Indicateur d’accès souhaité. Le client effectue des opérations de contrôle définies par le fournisseur sur une unité biométrique en appelant [**WinBioControlUnitPrivileged**](/windows/desktop/api/Winbio/nf-winbio-winbiocontrolunitprivileged).<br/> |



## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 uniquement\]<br/>                                                                    |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 R2, \[ applications de bureau uniquement\]<br/>                                                       |
| En-tête<br/>                   | <dl> <dt>WinBio \_ types. h (include WinBio. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Constantes d’application cliente](client-application-constants.md)
</dt> </dl>

 

 





