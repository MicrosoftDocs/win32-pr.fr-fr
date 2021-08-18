---
description: Les indicateurs figurant dans le tableau suivant spécifient les mécanismes de protection de sortie pour la sortie de la protection des informations (OPM).
ms.assetid: 484dfea9-301d-4b2b-b5d1-d785ebaa8c8f
title: Indicateurs de type de protection OPM (Opmapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ee61b17ee1708f8c2fc7e2f91b33d966b17f8fd2e198e2772c30ccccf837d04
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119101888"
---
# <a name="opm-protection-type-flags"></a>Indicateurs de type de protection OPM

Les indicateurs figurant dans le tableau suivant spécifient les mécanismes de protection de sortie pour la sortie de la protection des informations (OPM).



| Constante/valeur                                                                                                                                                                                                                                                                                                     | Description                                                                                                                                                                                                                 |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="OPM_PROTECTION_TYPE_OTHER"></span><span id="opm_protection_type_other"></span><dl> <dt>**OPM \_ TYPE de PROTECTION \_ \_ autre**</dt> <dt>0x80000000</dt> </dl>                                                | Mécanisme de protection inconnu.<br/>                                                                                                                                                                                    |
| <span id="OPM_PROTECTION_TYPE_NONE"></span><span id="opm_protection_type_none"></span><dl> <dt>**OPM \_ TYPE de PROTECTION \_ \_ aucun**</dt> <dt>0x00000000</dt> </dl>                                                   | Aucun mécanisme de protection.<br/>                                                                                                                                                                                        |
| <span id="OPM_PROTECTION_TYPE_COPP_COMPATIBLE_HDCP"></span><span id="opm_protection_type_copp_compatible_hdcp"></span><dl> <dt>**OPM \_ TYPE de PROTECTION \_ \_ Copp \_ compatible avec \_**</dt> la technologie HDCP <dt>0x00000001</dt> </dl> | High-Bandwidth protection du contenu numérique (HDCP). Cet indicateur est utilisé lors de l’émulation du protocole COPP (Certified Output Protection Protocol). Pour plus d'informations, consultez la section Notes. Cet indicateur n’est pas pris en charge pour la sémantique OPM.<br/> |
| <span id="OPM_PROTECTION_TYPE_ACP"></span><span id="opm_protection_type_acp"></span><dl> <dt>**OPM \_ TYPE de PROTECTION \_ \_ ACP**</dt> <dt>0x00000002</dt> </dl>                                                      | Protection contre la copie analogique (ACP).<br/>                                                                                                                                                                                    |
| <span id="OPM_PROTECTION_TYPE_CGMSA"></span><span id="opm_protection_type_cgmsa"></span><dl> <dt>**OPM \_ TYPE de PROTECTION \_ \_ CGMSA**</dt> <dt>0x00000004</dt> </dl>                                                | Système de gestion de la génération de copie — analogique (CGMS-A).<br/>                                                                                                                                                               |
| <span id="OPM_PROTECTION_TYPE_HDCP"></span><span id="opm_protection_type_hdcp"></span><dl> <dt>**OPM \_ TYPE de PROTECTION \_ \_ HDCP**</dt> <dt>0x00000008</dt> </dl>                                                   | HDCP. Cet indicateur est utilisé lorsque l’objet OPM a une sémantique OPM. Elle n’est pas prise en charge pour la sémantique COPP.<br/>                                                                                                           |
| <span id="OPM_PROTECTION_TYPE_DPCP"></span><span id="opm_protection_type_dpcp"></span><dl> <dt>**OPM \_ TYPE de PROTECTION \_ \_ DPCP**</dt> <dt>0x00000010</dt> </dl>                                                   | DisplayPort protection du contenu (DPCP).<br/>                                                                                                                                                                           |



## <a name="remarks"></a>Remarques

Ces indicateurs sont utilisés dans les commandes et les demandes d’État OPM suivantes.

-   [niveau de protection de l' \_ ensemble OPM \_ \_](opm-set-protection-level.md)
-   [\_niveau de \_ \_ protection \_ de l’offre OPM](opm-get-virtual-protection-level.md)
-   [\_niveau de \_ \_ protection \_ de l’offre OPM](opm-get-actual-protection-level.md)

### <a name="hdcp"></a>HDCP

Les deux indicateurs suivants sont définis pour HDCP.



| Valeur                                         | Description                                                                                                                                                                    |
|-----------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_type de protection OPM \_ \_ HDCP                   | Utilisez cet indicateur si le pointeur [**IOPMVideoOutput**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) a été créé avec la sémantique OPM.                                                                        |
| \_type de protection OPM \_ \_ \_ compatible avec le \_ HDCP | Utilisez cet indicateur si le pointeur [**IOPMVideoOutput**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) a été créé avec la sémantique COPP. Cet indicateur correspond à l' \_ indicateur ProtectionType \_ HDCP de COPP dans COPP. |



 

Les deux modes (sémantique OPM et sémantique COPP) prennent en charge les opérations suivantes pour HDCP :

-   Activez ou désactivez HDCP à l’aide de la commande [OPM \_ Set \_ protection \_ Level](opm-set-protection-level.md) .
-   Demandez si HDCP est activé à l’aide de la demande d’état de [ \_ \_ \_ protection virtuelle \_ ](opm-get-virtual-protection-level.md) ou de niveau de protection OPM obtenir le niveau de [ \_ \_ \_ protection \_ ](opm-get-actual-protection-level.md) .

La sémantique OPM prend également en charge les éléments suivants :

-   Répéteurs HDCP. Un *répétiteur HDCP* est un appareil HDCP qui peut recevoir du contenu HDCP et également rechiffrer et transmettre le même contenu.
-   Révocation HDCP. Si un appareil HDCP révoqué est attaché à la sortie vidéo OPM, la sortie vidéo ne transmet pas la vidéo. L’application n’a pas besoin d’analyser les messages de renouvellement du système HDCP (SRMs) ou de déterminer si le périphérique de sortie a été révoqué. Pour plus d’informations, consultez la commande [**OPM \_ Set \_ HDCP \_ SRM**](opm-set-hdcp-srm.md) .

Lorsque la sémantique COPP est utilisée, l’interface [**IOPMVideoOutput**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) ne prend pas en charge les répéteurs HDCP. En outre, elle ne gère pas la révocation HDCP. Au lieu de cela, l’application doit analyser le SRM pour déterminer si un appareil HDCP a été révoqué.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                      |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>Opmapi. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Énumérations OPM](opm-enumerations.md)
</dt> </dl>

 

 




