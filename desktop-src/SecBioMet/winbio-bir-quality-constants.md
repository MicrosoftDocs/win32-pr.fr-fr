---
title: Constantes WINBIO_BIR_QUALITY ( \_ types WINBIO. h)
description: Spécifiez la qualité relative des données biométriques dans le BIR si une valeur entière comprise entre 0 et 100 n’a pas été spécifiée.
ms.assetid: A42AA21B-9AA5-4DB6-B58F-0776BEC63E6C
topic_type:
- apiref
api_name:
- WINBIO_DATA_QUALITY_NOT_SET
- WINBIO_DATA_QUALITY_NOT_SUPPORTED
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1eb0881672c9e3bf51214cff93cb3f68d802b04
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106192"
---
# <a name="winbio_bir_quality-constants"></a>\_ \_ Constantes de qualité WINBIO Bir

Les indicateurs suivants sont utilisés par le membre **DataQuality** de la structure d' [**\_ \_ en-tête Bir WINBIO**](winbio-bir-header.md) pour spécifier la qualité relative des données biométriques dans le Bir si une valeur entière comprise entre 0 et 100 n’a pas été spécifiée.



| Constante/valeur                                                                                                                                                                                                                                                                       | Description                                                                                       |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------|
| <span id="WINBIO_DATA_QUALITY_NOT_SET"></span><span id="winbio_data_quality_not_set"></span><dl> <dt>**WINBIO \_ Qualité des données \_ \_ non \_ définie**</dt> <dt> 1</dt> </dl>                   | Les mesures de qualité sont prises en charge par le créateur BIR, mais aucune valeur n’est définie dans BIR.<br/> |
| <span id="WINBIO_DATA_QUALITY_NOT_SUPPORTED"></span><span id="winbio_data_quality_not_supported"></span><dl> <dt>**WINBIO \_ Qualité des données \_ \_ non \_ prise en charge**</dt> <dt> 2</dt> </dl> | Les mesures de qualité ne sont pas prises en charge par le créateur BIR.<br/>                             |



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

 

 





