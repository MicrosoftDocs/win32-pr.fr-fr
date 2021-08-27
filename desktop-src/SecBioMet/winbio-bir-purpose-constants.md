---
title: Constantes WINBIO_BIR_PURPOSE ( \_ types WINBIO. h)
description: Spécifiez l’objectif pour lequel l’enregistrement d’informations biométriques (BIR) est prévu ou pour lequel il convient.
ms.assetid: AAFD3203-4D3D-43B5-A833-1258E1E281D3
topic_type:
- apiref
api_name:
- WINBIO_NO_PURPOSE_AVAILABLE
- WINBIO_PURPOSE_VERIFY
- WINBIO_PURPOSE_IDENTIFY
- WINBIO_PURPOSE_ENROLL
- WINBIO_PURPOSE_ENROLL_FOR_VERIFICATION
- WINBIO_PURPOSE_ENROLL_FOR_IDENTIFICATION
- WINBIO_PURPOSE_AUDIT
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 19cffe266cf30155be3c299b0d1b5e6a3d45f9991aa83fd66e62e705ddc4850f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120080789"
---
# <a name="winbio_bir_purpose-constants"></a>\_ \_ Constantes WINBIO Bir Purpose

Les indicateurs suivants sont utilisés par le membre **Purpose** de la structure d' [**\_ \_ en-tête Bir WINBIO**](winbio-bir-header.md) pour spécifier l’objectif pour lequel l’enregistrement d’informations biométriques (Bir) est destiné ou pour lequel il convient.



| Constante                                                                                                                                                                                                                                          | Description                                                                                                                                                                                                                                                                                                                                 |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_NO_PURPOSE_AVAILABLE"></span><span id="winbio_no_purpose_available"></span><dl> <dt>**WINBIO \_ aucun \_ objet \_ disponible**</dt> </dl>                                         | Aucun objet n’est spécifié.<br/>                                                                                                                                                                                                                                                                                                         |
| <span id="WINBIO_PURPOSE_VERIFY"></span><span id="winbio_purpose_verify"></span><dl> <dt>**vérification de l' \_ objectif WINBIO \_**</dt> </dl>                                                            | Vérifiez l’identité d’un utilisateur.<br/>                                                                                                                                                                                                                                                                                                   |
| <span id="WINBIO_PURPOSE_IDENTIFY"></span><span id="winbio_purpose_identify"></span><dl> <dt>**identification de l’objectif de WINBIO \_ \_**</dt> </dl>                                                      | Identifiez un utilisateur.<br/>                                                                                                                                                                                                                                                                                                                 |
| <span id="WINBIO_PURPOSE_ENROLL"></span><span id="winbio_purpose_enroll"></span><dl> <dt>**inscription à l’objectif de WINBIO \_ \_**</dt> </dl>                                                            | Inscrire un utilisateur.<br/>                                                                                                                                                                                                                                                                                                                   |
| <span id="WINBIO_PURPOSE_ENROLL_FOR_VERIFICATION"></span><span id="winbio_purpose_enroll_for_verification"></span><dl> <dt>**\_inscription de l’objectif WINBIO \_ pour la \_ \_ vérification**</dt> </dl>       | Capturez un échantillon biométrique et déterminez si l’échantillon correspond à l’identité de l’utilisateur spécifié.<br/>                                                                                                                                                                                                                          |
| <span id="WINBIO_PURPOSE_ENROLL_FOR_IDENTIFICATION"></span><span id="winbio_purpose_enroll_for_identification"></span><dl> <dt>**\_inscription de l’objectif WINBIO \_ pour l' \_ \_ identification**</dt> </dl> | Capturez un échantillon biométrique et déterminez s’il correspond à un modèle biométrique existant.<br/>                                                                                                                                                                                                                                      |
| <span id="WINBIO_PURPOSE_AUDIT"></span><span id="winbio_purpose_audit"></span><dl> <dt>**\_ \_ audit d’objectif WINBIO**</dt> </dl>                                                               | Informations supplémentaires qui peuvent être utilisées pour la journalisation ou l’affichage. Cette valeur est ignorée à l’entrée par toutes les fonctions. À la sortie, elle est disponible uniquement si elle est prise en charge par l’unité biométrique et que vous spécifiez **WINBIO \_ Data \_ Flag \_ RAW** dans le paramètre *Flags* de la fonction [**WinBioCaptureSample**](/windows/desktop/api/Winbio/nf-winbio-winbiocapturesample) .<br/> |



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 uniquement\]<br/>                                                                    |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 R2, \[ applications de bureau uniquement\]<br/>                                                       |
| En-tête<br/>                   | <dl> <dt>WinBio \_ types. h (include WinBio. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Constantes d’application cliente](client-application-constants.md)
</dt> <dt>

[**\_ \_ en-tête Bir WINBIO**](winbio-bir-header.md)
</dt> </dl>

 

 





