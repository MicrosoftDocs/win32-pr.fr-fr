---
title: General, constantes (WinBio \_ types. h)
description: Spécifiez la longueur maximale des SID, des descripteurs, des ID, la longueur de chaîne maximale et la taille de mémoire tampon d’échantillon maximale.
ms.assetid: 62e87bd8-a708-4d00-aaa8-9cac8e3736a7
topic_type:
- apiref
api_name:
- SECURITY_MAX_SID_SIZE
- WINBIO_UNIT_ID
- WINBIO_SESSION_HANDLE
- WINBIO_FRAMEWORK_HANDLE
- WINBIO_UUID
- WINBIO_STRING
- WINBIO_MAX_STRING_LEN
- WINBIO_MAX_SAMPLE_BUFFER_SIZE
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5e35aa4c2cc676935cfb80fdec8729daf64d5f3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942125"
---
# <a name="general-constants-winbio_typesh"></a>General, constantes (WinBio \_ types. h)

Les constantes suivantes sont utilisées dans l’ensemble du Windows Biometric Framework.



| Constante/valeur                                                                                                                                                                                                                                                                   | Description                                                                                 |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------|
| <span id="SECURITY_MAX_SID_SIZE"></span><span id="security_max_sid_size"></span><dl> <dt>**\_taille maximale de \_ sid \_ de sécurité**</dt> </dl>                                                                                          | Longueur maximale d’une valeur d’identificateur de sécurité (SID). Actuellement, il s’agit de 68.<br/>   |
| <span id="WINBIO_UNIT_ID"></span><span id="winbio_unit_id"></span><dl> <dt>**\_ID d’unité WINBIO \_**</dt> </dl>                                                                                                                | Numéro d’identification d’une unité biométrique.<br/>                                                   |
| <span id="WINBIO_SESSION_HANDLE"></span><span id="winbio_session_handle"></span><dl> <dt>**\_handle de session WINBIO \_**</dt> </dl>                                                                                           | Entier long non signé qui contient le handle d’une session biométrique ouverte.<br/> |
| <span id="WINBIO_FRAMEWORK_HANDLE"></span><span id="winbio_framework_handle"></span><dl> <dt>**\_handle de Framework WINBIO \_**</dt> </dl>                                                                                     | Entier long non signé qui contient le handle d’une session Open Framework.<br/> |
| <span id="WINBIO_UUID"></span><span id="winbio_uuid"></span><dl> <dt>**\_UUID WINBIO**</dt> </dl>                                                                                                                          | GUID.<br/>                                                                          |
| <span id="WINBIO_STRING"></span><span id="winbio_string"></span><dl> <dt>**\_chaîne WINBIO**</dt> </dl>                                                                                                                    | Tableau d’octets qui contient une chaîne Unicode terminée par le caractère null.<br/>                     |
| <span id="WINBIO_MAX_STRING_LEN_"></span><span id="winbio_max_string_len_"></span><dl> <dt>**WINBIO \_ \_ \_ longueur maximale** de la chaîne</dt> </dl>                                                                                       | Longueur maximale d’une valeur **de \_ chaîne WINBIO** . Actuellement, il s’agit de 256.<br/>         |
| <span id="WINBIO_MAX_SAMPLE_BUFFER_SIZE"></span><span id="winbio_max_sample_buffer_size"></span><dl> <dt>**WINBIO \_ Taille maximale de la \_ \_ mémoire \_ tampon d’échantillonnage**</dt> <dt>0x7FFFFFFF</dt> </dl> | Nombre maximal d’octets dans une seule capture de données biométriques.<br/>                  |



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

 

 





