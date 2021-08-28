---
title: Constantes WINBIO_BIR_FIELD ( \_ types WINBIO. h)
description: Spécifiez un masque de masque.
ms.assetid: D8D12BCF-FEB3-4E02-B751-9F3AE5048BC1
topic_type:
- apiref
api_name:
- WINBIO_BIR_FIELD_SUBHEAD_COUNT
- WINBIO_BIR_FIELD_PRODUCT_ID
- WINBIO_BIR_FIELD_PATRON_ID
- WINBIO_BIR_FIELD_INDEX
- WINBIO_BIR_FIELD_CREATION_DATE
- WINBIO_BIR_FIELD_VALIDITY_PERIOD
- WINBIO_BIR_FIELD_BIOMETRIC_TYPE
- WINBIO_BIR_FIELD_BIOMETRIC_SUBTYPE
- WINBIO_BIR_FIELD_CBEFF_HEADER_VERSION
- WINBIO_BIR_FIELD_PATRON_HEADER_VERSION
- WINBIO_BIR_FIELD_BIOMETRIC_PURPOSE
- WINBIO_BIR_FIELD_BIOMETRIC_CONDITION
- WINBIO_BIR_FIELD_QUALITY
- WINBIO_BIR_FIELD_CREATOR
- WINBIO_BIR_FIELD_CHALLENGE
- WINBIO_BIR_FIELD_PAYLOAD
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a354f3119fcef6da3ff204f833616eeb2ac9570cdad0712a87686904ad528958
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120035089"
---
# <a name="winbio_bir_field-constants"></a>\_ \_ Constantes de champ WINBIO Bir

Les constantes suivantes sont utilisées pour créer un masque de masque pour le membre **ValidFields** de la structure d' [**\_ \_ en-tête Bir WINBIO**](winbio-bir-header.md) .



| Constante/valeur                                                                                                                                                                                                                                                                                           | Description                                                                                                                                   |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_BIR_FIELD_SUBHEAD_COUNT"></span><span id="winbio_bir_field_subhead_count"></span><dl> <dt>**WINBIO \_ BIR \_ \_ \_ nombre**</dt> de sous-valeur de champ <dt>0x0001</dt> </dl>                          | fourni pour la conformité avec NISTIR 6529-A, le CBEFF (Common biometrics formates Exchange Framework formate), mais n’est pas utilisé.<br/> |
| <span id="WINBIO_BIR_FIELD_PRODUCT_ID"></span><span id="winbio_bir_field_product_id"></span><dl> <dt>**WINBIO \_ BIR \_ champ \_ \_ ID produit**</dt> <dt>0x0002</dt> </dl>                                   | Le membre **ProductID** est valide.<br/>                                                                                                 |
| <span id="WINBIO_BIR_FIELD_PATRON_ID"></span><span id="winbio_bir_field_patron_id"></span><dl> <dt>**WINBIO \_ \_ID d' \_ \_ acheteur du champ Bir**</dt> <dt>0x0004</dt> </dl>                                      | Fourni pour la conformité avec NISTIR 6529-A, CBEFF patron format A, mais n’est pas utilisé.<br/>                                                   |
| <span id="WINBIO_BIR_FIELD_INDEX"></span><span id="winbio_bir_field_index"></span><dl> <dt>**WINBIO \_ BIR \_ \_ index de champ**</dt> <dt>0x0008</dt> </dl>                                                   | Fourni pour la conformité avec NISTIR 6529-A, CBEFF patron format A, mais n’est pas utilisé.<br/>                                                   |
| <span id="WINBIO_BIR_FIELD_CREATION_DATE"></span><span id="winbio_bir_field_creation_date"></span><dl> <dt>**WINBIO \_ \_Date de \_ création \_ du champ Bir**</dt> <dt>0x0010</dt> </dl>                          | Le membre **CreationDate** est valide.<br/>                                                                                              |
| <span id="WINBIO_BIR_FIELD_VALIDITY_PERIOD"></span><span id="winbio_bir_field_validity_period"></span><dl> <dt>**WINBIO \_ \_Période de \_ validité \_ du champ Bir**</dt> <dt>0x0020</dt> </dl>                    | Le membre **ValidityPeriod** est valide.<br/>                                                                                            |
| <span id="WINBIO_BIR_FIELD_BIOMETRIC_TYPE"></span><span id="winbio_bir_field_biometric_type"></span><dl> <dt>**WINBIO \_ \_ \_ \_ Type biométrique du champ Bir**</dt> <dt>0x0040</dt> </dl>                       | Le membre de **type** est valide.<br/>                                                                                                      |
| <span id="WINBIO_BIR_FIELD_BIOMETRIC_SUBTYPE"></span><span id="winbio_bir_field_biometric_subtype"></span><dl> <dt>**WINBIO \_ BIR, \_ champ de \_ sous- \_ type biométrique**</dt> <dt>0x0080</dt> </dl>              | Le membre de **sous-type** est valide.<br/>                                                                                                   |
| <span id="WINBIO_BIR_FIELD_CBEFF_HEADER_VERSION"></span><span id="winbio_bir_field_cbeff_header_version"></span><dl> <dt>**WINBIO \_ BIR \_ champ \_ CBEFF \_ \_ version d’en-tête**</dt> <dt>0x0100</dt> </dl>    | Le membre **HeaderVersion** est valide.<br/>                                                                                             |
| <span id="WINBIO_BIR_FIELD_PATRON_HEADER_VERSION"></span><span id="winbio_bir_field_patron_header_version"></span><dl> <dt>**WINBIO \_ BIR \_ d' \_ en-tête d’un champ d' \_ en-tête \_**</dt> <dt>0x0200</dt> </dl> | Le membre **PatronHeaderVersion** est valide.<br/>                                                                                       |
| <span id="WINBIO_BIR_FIELD_BIOMETRIC_PURPOSE"></span><span id="winbio_bir_field_biometric_purpose"></span><dl> <dt>**WINBIO \_ \_Champ Bir \_ \_ objet biométrique**</dt> <dt>0x0400</dt> </dl>              | Le membre **objectif** est valide.<br/>                                                                                                   |
| <span id="WINBIO_BIR_FIELD_BIOMETRIC_CONDITION"></span><span id="winbio_bir_field_biometric_condition"></span><dl> <dt>**WINBIO \_ \_ \_ \_ Condition biométrique du champ Bir**</dt> <dt>0x0800</dt> </dl>        | Fourni pour la conformité avec NISTIR 6529-A, CBEFF patron format A, mais n’est pas utilisé.<br/>                                                   |
| <span id="WINBIO_BIR_FIELD_QUALITY"></span><span id="winbio_bir_field_quality"></span><dl> <dt>**WINBIO \_ BIR \_ \_ qualité du champ**</dt> <dt>0x1000</dt> </dl>                                             | Le membre **DataQuality** est valide.<br/>                                                                                               |
| <span id="WINBIO_BIR_FIELD_CREATOR"></span><span id="winbio_bir_field_creator"></span><dl> <dt>**WINBIO \_ BIR \_ du \_ créateur du champ**</dt> <dt></dt> </dl>                                             | Fourni pour la conformité avec NISTIR 6529-A, CBEFF patron format A, mais n’est pas utilisé.<br/>                                                   |
| <span id="WINBIO_BIR_FIELD_CHALLENGE"></span><span id="winbio_bir_field_challenge"></span><dl> <dt>**WINBIO \_ BIR \_ de \_ stimulation de champ**</dt> <dt>0x4000</dt> </dl>                                       | Fourni pour la conformité avec NISTIR 6529-A, CBEFF patron format A, mais n’est pas utilisé.<br/>                                                   |
| <span id="WINBIO_BIR_FIELD_PAYLOAD"></span><span id="winbio_bir_field_payload"></span><dl> <dt>**WINBIO \_ \_ \_ Charge utile du champ Bir**</dt> <dt>0x8000</dt> </dl>                                             | Fourni pour la conformité avec NISTIR 6529-A, CBEFF patron format A, mais n’est pas utilisé.<br/>                                                   |



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 uniquement\]<br/>                                                                    |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 R2, \[ applications de bureau uniquement\]<br/>                                                       |
| En-tête<br/>                   | <dl> <dt>WinBio \_ types. h (include WinBio. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Constantes d’application cliente](client-application-constants.md)
</dt> </dl>

 

 





