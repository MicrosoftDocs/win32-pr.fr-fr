---
title: Constantes WINBIO_SETTING_SOURCE ( \_ types WINBIO. h)
description: Déterminez si la Windows Biometric Framework est actuellement activée.
ms.assetid: d95aa6cc-ddff-40fb-ab82-eac78dc0cb6b
topic_type:
- apiref
api_name:
- WINBIO_SETTING_SOURCE_INVALID
- WINBIO_SETTING_SOURCE_DEFAULT
- WINBIO_SETTING_SOURCE_POLICY
- WINBIO_SETTING_SOURCE_LOCAL
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b54723612c7e0948e09baddf22ad4f4703ca5c38
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942816"
---
# <a name="winbio_setting_source-constants"></a>\_Constantes de la source de paramètre WINBIO \_

Les constantes suivantes sont utilisées par la fonction [**WinBioGetEnabledSetting**](/windows/desktop/api/Winbio/nf-winbio-winbiogetenabledsetting) pour déterminer si la Windows Biometric Framework est actuellement activée. Les constantes spécifient l’origine du paramètre.



| Constante                                                                                                                                                                                                        | Description                                                       |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------|
| <span id="WINBIO_SETTING_SOURCE_INVALID"></span><span id="winbio_setting_source_invalid"></span><dl> <dt>**\_source du paramètre WINBIO \_ \_ non valide**</dt> </dl> | Le paramètre n’est pas valide.<br/>                              |
| <span id="WINBIO_SETTING_SOURCE_DEFAULT"></span><span id="winbio_setting_source_default"></span><dl> <dt>**\_ \_ \_ valeur par défaut de la source du paramètre WINBIO**</dt> </dl> | Le paramètre provient de la stratégie intégrée.<br/>           |
| <span id="WINBIO_SETTING_SOURCE_POLICY"></span><span id="winbio_setting_source_policy"></span><dl> <dt>**\_stratégie de \_ source du paramètre WINBIO \_**</dt> </dl>    | Le paramètre provient du registre de l’ordinateur local.<br/> |
| <span id="WINBIO_SETTING_SOURCE_LOCAL"></span><span id="winbio_setting_source_local"></span><dl> <dt>**\_ \_ source locale du paramètre WINBIO \_**</dt> </dl>       | Le paramètre a été créé par stratégie de groupe<br/>                |



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 7 uniquement\]<br/>                                                                    |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 R2 \[ uniquement\]<br/>                                                       |
| En-tête<br/>                   | <dl> <dt>WinBio \_ types. h (include WinBio. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Constantes d’application cliente](client-application-constants.md)
</dt> </dl>

 

 





