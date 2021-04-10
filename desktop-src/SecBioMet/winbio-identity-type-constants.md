---
title: Constantes WINBIO_IDENTITY_TYPE ( \_ types WINBIO. h)
description: Spécifiez le format des informations d’identité contenues dans la \_ structure d’identité WINBIO.
ms.assetid: 27A01538-9B26-4A29-8ADB-ED9C5D5808B3
topic_type:
- apiref
api_name:
- WINBIO_ID_TYPE_NULL
- WINBIO_ID_TYPE_WILDCARD
- WINBIO_ID_TYPE_GUID
- WINBIO_ID_TYPE_SID
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dad068c6838f0a3a675970b7c9359b12ea8faa2c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941901"
---
# <a name="winbio_identity_type-constants"></a>\_Constantes de type d’identité WINBIO \_

Les constantes de **\_ \_ type d’identité WINBIO** suivantes peuvent être utilisées pour spécifier le format des informations d’identité contenues dans la structure d' [**\_ identité WINBIO**](winbio-identity.md) .



| Constante                                                                                                                                                                                      | Description                                               |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------|
| <span id="WINBIO_ID_TYPE_NULL"></span><span id="winbio_id_type_null"></span><dl> <dt>**\_type d’ID WINBIO \_ \_ null**</dt> </dl>             | Le modèle n’a pas d’ID associé. <br/>            |
| <span id="WINBIO_ID_TYPE_WILDCARD"></span><span id="winbio_id_type_wildcard"></span><dl> <dt>**\_ \_ caractère générique de type d’ID WINBIO \_**</dt> </dl> | La structure correspond à toutes les identités de modèle.<br/> |
| <span id="WINBIO_ID_TYPE_GUID"></span><span id="winbio_id_type_guid"></span><dl> <dt>**\_GUID du \_ type d’ID WINBIO \_**</dt> </dl>             | Un GUID identifie le modèle.<br/>                |
| <span id="WINBIO_ID_TYPE_SID"></span><span id="winbio_id_type_sid"></span><dl> <dt>**\_ID \_ sid type \_ WINBIO**</dt> </dl>                | Un SID de compte identifie le modèle.<br/>        |



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 7 uniquement\]<br/>                                                                    |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 R2 \[ uniquement\]<br/>                                                       |
| En-tête<br/>                   | <dl> <dt>WinBio \_ types. h (include WinBio. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Constantes d’application cliente](client-application-constants.md)
</dt> <dt>

[**\_identité WINBIO**](winbio-identity.md)
</dt> </dl>

 

 





