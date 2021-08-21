---
description: Spécifiez les niveaux de protection pour le système de gestion de la génération de copie&\# 8212 ; Analogique (CGMS-A).
ms.assetid: 739e2f9e-b8f1-4ee1-8706-9a069773a3de
title: Indicateurs de protection de CGMS-A (Opmapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cfe52f6b6f8c282e9dacebd6528373fc8ba7b7717a8e721d7d414117585bb188
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118065138"
---
# <a name="cgms-a-protection-flags"></a>Indicateurs de protection de CGMS-A

Les constantes dans le tableau suivant spécifient les niveaux de protection pour la version analogique du système de gestion de la génération de copie (CGMS-A).



| Constante/valeur                                                                                                                                                                                                                                                                                                 | Description                                                                                                                       |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------|
| <span id="OPM_CGMSA_OFF"></span><span id="opm_cgmsa_off"></span><dl> <dt>**OPM \_ CGMSA \_ désactivé**</dt> <dt>0x00</dt> </dl>                                                                                       | CGMS-A est désactivé. <br/>                                                                                                   |
| <span id="OPM_CGMSA_COPY_FREELY"></span><span id="opm_cgmsa_copy_freely"></span><dl> <dt>**OPM \_ CGMSA \_ copier \_ librement**</dt> <dt>0x01</dt> </dl>                                                              | Le niveau de protection est copie libre.<br/>                                                                                   |
| <span id="OPM_CGMSA_COPY_NO_MORE"></span><span id="opm_cgmsa_copy_no_more"></span><dl> <dt>**OPM \_ CGMSA \_ Copy \_ n’a \_ plus**</dt> de <dt>0x02</dt> </dl>                                                          | Le niveau de protection n’est pas copié. <br/>                                                                                 |
| <span id="OPM_CGMSA_COPY_ONE_GENERATION"></span><span id="opm_cgmsa_copy_one_generation"></span><dl> <dt>**OPM \_ CGMSA \_ copier \_ une \_**</dt> <dt>0x03</dt> de génération </dl>                                     | Le niveau de protection est copier une génération. <br/>                                                                          |
| <span id="OPM_CGMSA_COPY_NEVER"></span><span id="opm_cgmsa_copy_never"></span><dl> <dt>**OPM \_ CGMSA \_ \_ ne jamais**</dt> <dt>0x04</dt> </dl>                                                                 | Le niveau de protection est ne jamais copier.<br/>                                                                                    |
| <span id="OPM_CGMSA_REDISTRIBUTION_CONTROL_REQUIRED"></span><span id="opm_cgmsa_redistribution_control_required"></span><dl> <dt>**OPM \_ \_Le contrôle de redistribution CGMSA \_ \_ requis**</dt> <dt>0x08</dt> </dl> | Le contrôle de redistribution (également appelé *indicateur de diffusion*) est requis. Cet indicateur peut être combiné avec les autres indicateurs.<br/> |



## <a name="remarks"></a>Remarques

Ces indicateurs sont équivalents aux constantes d’énumération de **\_ niveau de \_ protection \_ Copp CGMSA** utilisées dans le protocole Copp (Certified Output Protection Protocol).

## <a name="requirements"></a>Conditions requises



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                      |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>Opmapi. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Constantes Media Foundation](media-foundation-constants.md)
</dt> </dl>

 

 




