---
title: Constantes WINBIO_BIR_DATA_FLAGS ( \_ types WINBIO. h)
description: Spécifiez la condition des données.
ms.assetid: F6F7F68A-3294-4AF8-A1A7-C6A869A2CC3C
topic_type:
- apiref
api_name:
- WINBIO_DATA_FLAG_PRIVACY
- WINBIO_DATA_FLAG_INTEGRITY
- WINBIO_DATA_FLAG_SIGNED
- WINBIO_DATA_FLAG_RAW
- WINBIO_DATA_FLAG_INTERMEDIATE
- WINBIO_DATA_FLAG_PROCESSED
- WINBIO_DATA_FLAG_OPTION_MASK_PRESENT
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 87769500de02dedc7247b15e94064a43b7c6d528234c27ad700d4a336f42a092
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119622629"
---
# <a name="winbio_bir_data_flags-constants"></a>\_ \_ Constantes d’indicateurs de données WINBIO Bir \_

Les constantes suivantes sont utilisées par le membre **DataFlags** de la structure d' [**\_ \_ en-tête Bir WINBIO**](winbio-bir-header.md) .



| Constante/valeur                                                                                                                                                                                                                                                                                   | Description                                                                                                                                                                                                       |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_DATA_FLAG_PRIVACY"></span><span id="winbio_data_flag_privacy"></span><dl> <dt>**WINBIO \_ \_ \_ Confidentialité**</dt> de l’indicateur de données <dt>0x02</dt> </dl>                                       | Les données sont chiffrées.<br/>                                                                                                                                                                                 |
| <span id="WINBIO_DATA_FLAG_INTEGRITY"></span><span id="winbio_data_flag_integrity"></span><dl> <dt>**WINBIO \_ \_ \_ Intégrité des indicateurs de données**</dt> <dt>0x01</dt> </dl>                                 | Les données sont signées numériquement ou sont protégées par un code d’authentification de message (MAC).<br/>                                                                                                                   |
| <span id="WINBIO_DATA_FLAG_SIGNED"></span><span id="winbio_data_flag_signed"></span><dl> <dt>**WINBIO \_ Indicateur de données \_ \_ signé**</dt> <dt>0x04</dt> </dl>                                          | Si cet indicateur et l’indicateur d’intégrité de l' **\_ indicateur de données \_ \_ WINBIO** sont définis, les données sont signées. Si cet indicateur n’est pas défini, mais que l’indicateur d’intégrité de l' **\_ indicateur de données \_ \_ WINBIO** est défini, un Mac est calculé sur les données.<br/> |
| <span id="WINBIO_DATA_FLAG_RAW"></span><span id="winbio_data_flag_raw"></span><dl> <dt>**WINBIO \_ \_Indicateur de \_ données**</dt> - <dt>0x20</dt> brut </dl>                                                   | Les données sont au format avec lequel elles ont été capturées.<br/>                                                                                                                                                  |
| <span id="WINBIO_DATA_FLAG_INTERMEDIATE"></span><span id="winbio_data_flag_intermediate"></span><dl> <dt>**WINBIO \_ \_Indicateur de \_ données**</dt> - <dt>0x40</dt> intermédiaire </dl>                        | Les données ne sont pas brutes, mais elles n’ont pas été complètement traitées.<br/>                                                                                                                                             |
| <span id="WINBIO_DATA_FLAG_PROCESSED"></span><span id="winbio_data_flag_processed"></span><dl> <dt>**WINBIO \_ Indicateur de données \_ \_ traité**</dt> à <dt>0x80</dt> </dl>                                 | Les données ont été traitées.<br/>                                                                                                                                                                           |
| <span id="WINBIO_DATA_FLAG_OPTION_MASK_PRESENT"></span><span id="winbio_data_flag_option_mask_present"></span><dl> <dt>**WINBIO \_ Masque d’option de l’indicateur de données \_ \_ \_ \_ actuel**</dt> <dt>0x08</dt> </dl> | Masque de l’indicateur. Cette valeur est toujours un (1).<br/>                                                                                                                                                           |



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

 

 





