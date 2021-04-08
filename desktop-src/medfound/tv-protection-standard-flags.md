---
description: Les constantes dans le tableau ci-dessous spécifient les normes et formats de télévision pour la sortie de protection des informations (OPM).
ms.assetid: 8f26aa92-ed40-483e-ac78-c071619f0e12
title: Indicateurs standard de protection TV (Opmapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 28fc4db73bb68fd1aeb0749134d8d6cf998cec40
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104034293"
---
# <a name="tv-protection-standard-flags"></a>Indicateurs standard de la protection TV

Les constantes dans le tableau ci-dessous spécifient les normes et formats de télévision pour la sortie de protection des informations (OPM).



| Constante/valeur                                                                                                                                                                                                                                                                                                              | Description                                                    |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------|
| <span id="OPM_PROTECTION_STANDARD_OTHER"></span><span id="opm_protection_standard_other"></span><dl> <dt>**OPM \_ PROTECTION \_ standard \_ autre**</dt> <dt>0x80000000</dt> </dl>                                             | La norme de protection est inconnue.<br/>                 |
| <span id="OPM_PROTECTION_STANDARD_NONE"></span><span id="opm_protection_standard_none"></span><dl> <dt>**OPM \_ PROTECTION \_ standard \_ None**</dt> <dt>0x00000000</dt> </dl>                                                | Aucune norme de protection n’est en place.<br/>                 |
| <span id="OPM_PROTECTION_STANDARD_IEC61880_525I"></span><span id="opm_protection_standard_iec61880_525i"></span><dl> <dt>**OPM \_ PROTECTION \_ standard \_ IEC61880 \_ 525I**</dt> <dt>0x00000001</dt> </dl>                    | La norme de protection est IEC 61880, 525i.<br/>         |
| <span id="OPM_PROTECTION_STANDARD_IEC61880_2_525I"></span><span id="opm_protection_standard_iec61880_2_525i"></span><dl> <dt>**OPM \_ PROTECTION \_ standard \_ IEC61880 \_ 2 \_ 525I**</dt> <dt>0x00000002</dt> </dl>             | La norme de protection est IEC 61880-2, 525i.<br/>       |
| <span id="OPM_PROTECTION_STANDARD_IEC62375_625P"></span><span id="opm_protection_standard_iec62375_625p"></span><dl> <dt>**OPM \_ PROTECTION \_ standard \_ IEC62375 \_ 625P**</dt> <dt>0x00000004</dt> </dl>                    | La norme de protection est IEC 62375, 625p.<br/>         |
| <span id="OPM_PROTECTION_STANDARD_EIA608B_525"></span><span id="opm_protection_standard_eia608b_525"></span><dl> <dt>**OPM \_ PROTECTION \_ standard \_ EIA608B \_ 525**</dt> <dt>0x00000008</dt> </dl>                          | La norme de protection est EIA/CEA-608-B, 525i.<br/>     |
| <span id="OPM_PROTECTION_STANDARD_EN300294_625I"></span><span id="opm_protection_standard_en300294_625i"></span><dl> <dt>**OPM \_ PROTECTION \_ standard \_ EN300294 \_ 625I**</dt> <dt>0x00000010</dt> </dl>                    | La norme de protection est ETSI en 300 294, 625i.<br/>   |
| <span id="OPM_PROTECTION_STANDARD_CEA805A_TYPEA_525P"></span><span id="opm_protection_standard_cea805a_typea_525p"></span><dl> <dt>**OPM \_ PROTECTION \_ standard \_ CEA805A \_ TypeA \_ 525p**</dt> <dt>0x00000020</dt> </dl>    | La norme de protection est CEA-805-A type A, 525p.<br/>  |
| <span id="OPM_PROTECTION_STANDARD_CEA805A_TYPEA_750P"></span><span id="opm_protection_standard_cea805a_typea_750p"></span><dl> <dt>**OPM \_ PROTECTION \_ standard \_ CEA805A \_ TypeA \_ 750P**</dt> <dt>0x00000040</dt> </dl>    | La norme de protection est CEA-805-A type A, 750P.<br/>  |
| <span id="OPM_PROTECTION_STANDARD_CEA805A_TYPEA_1125I"></span><span id="opm_protection_standard_cea805a_typea_1125i"></span><dl> <dt>**OPM \_ PROTECTION \_ standard \_ CEA805A \_ TypeA \_ 1125i**</dt> <dt>0x00000080</dt> </dl> | La norme de protection est CEA-805-A type A, 1125i.<br/> |
| <span id="OPM_PROTECTION_STANDARD_CEA805A_TYPEB_525P"></span><span id="opm_protection_standard_cea805a_typeb_525p"></span><dl> <dt>**OPM \_ PROTECTION \_ standard \_ CEA805A \_ TYPEB \_ 525p**</dt> <dt>0x00000100</dt> </dl>    | La norme de protection est CEA-805-A type B, 525p.<br/>  |
| <span id="OPM_PROTECTION_STANDARD_CEA805A_TYPEB_750P"></span><span id="opm_protection_standard_cea805a_typeb_750p"></span><dl> <dt>**OPM \_ PROTECTION \_ standard \_ CEA805A \_ TYPEB \_ 750P**</dt> <dt>0x00000200</dt> </dl>    | La norme de protection est CEA-805-A type B, 750P.<br/>  |
| <span id="OPM_PROTECTION_STANDARD_CEA805A_TYPEB_1125I"></span><span id="opm_protection_standard_cea805a_typeb_1125i"></span><dl> <dt>**OPM \_ PROTECTION \_ standard \_ CEA805A \_ TYPEB \_ 1125i**</dt> <dt>0x00000400</dt> </dl> | La norme de protection est CEA-805-A type B, 1125i.<br/> |
| <span id="OPM_PROTECTION_STANDARD_ARIBTRB15_525I"></span><span id="opm_protection_standard_aribtrb15_525i"></span><dl> <dt>**OPM \_ PROTECTION \_ standard \_ ARIBTRB15 \_ 525I**</dt> <dt>0x00000800</dt> </dl>                 | La norme de protection est ARIB TR-B15, 525i.<br/>       |
| <span id="OPM_PROTECTION_STANDARD_ARIBTRB15_525P"></span><span id="opm_protection_standard_aribtrb15_525p"></span><dl> <dt>**OPM \_ PROTECTION \_ standard \_ ARIBTRB15 \_ 525p**</dt> <dt>0x00001000</dt> </dl>                 | La norme de protection est ARIB TR-B15, 525p.<br/>       |
| <span id="OPM_PROTECTION_STANDARD_ARIBTRB15_750P"></span><span id="opm_protection_standard_aribtrb15_750p"></span><dl> <dt>**OPM \_ PROTECTION \_ standard \_ ARIBTRB15 \_ 750P**</dt> <dt>0x00002000</dt> </dl>                 | La norme de protection est ARIB TR-B15, 750P.<br/>       |
| <span id="OPM_PROTECTION_STANDARD_ARIBTRB15_1125I"></span><span id="opm_protection_standard_aribtrb15_1125i"></span><dl> <dt>**OPM \_ PROTECTION \_ standard \_ ARIBTRB15 \_ 1125i**</dt> <dt>0x00004000</dt> </dl>              | La norme de protection est ARIB TR-B15, 1125i.<br/>      |



## <a name="remarks"></a>Notes

Ces indicateurs sont numériquement équivalents à l’énumération **\_ TVProtectionStandard Copp** utilisée dans le protocole Copp (Certified Output Protection Protocol).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                      |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>Opmapi. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Constantes Media Foundation](media-foundation-constants.md)
</dt> <dt>

[**\_ \_ \_ signaux ACP et \_ CGMSA de \_ l’ensemble OPM**](opm-set-acp-and-cgmsa-signaling.md)
</dt> <dt>

[\_prise en \_ main \_ des signaux ACP et \_ CGMSA \_ pour OPM](opm-get-acp-and-cgmsa-signaling.md)
</dt> </dl>

 

 




