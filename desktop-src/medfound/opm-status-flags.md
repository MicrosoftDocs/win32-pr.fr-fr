---
description: Les indicateurs figurant dans le tableau suivant spécifient l’état d’une session Protection Manager (OPM) de sortie.
ms.assetid: d6d85fd4-e735-4610-93e0-bb2b1782f11b
title: Indicateurs d’État OPM (Opmapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: edc044d9159ad6e6a6e957c4be0228a8e2531164
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122480195"
---
# <a name="opm-status-flags"></a>Indicateurs d’État OPM

Les indicateurs figurant dans le tableau suivant spécifient l’état d’une session Protection Manager (OPM) de sortie.




| Constante/valeur | Description | 
|----------------|-------------|
| <span id="OPM_STATUS_NORMAL"></span><span id="opm_status_normal"></span><dl><dt><strong>OPM_STATUS_NORMAL</strong></dt><dt>0x00</dt></dl> | État normal.<br /> | 
| <span id="OPM_STATUS_LINK_LOST"></span><span id="opm_status_link_lost"></span><dl><dt><strong>OPM_STATUS_LINK_LOST</strong></dt><dt>0x01</dt></dl> | L’intégrité de la connexion a été compromise. Voici quelques exemples d’événements qui obligent le pilote à définir cet indicateur :<br /><ul><li>Le pilote ne peut plus appliquer le niveau de protection actuel.</li><li>Le pilote a détecté une erreur d’intégrité interne.</li><li>Le connecteur entre l’ordinateur et le périphérique d’affichage a été débranché.</li></ul> | 
| <span id="OPM_STATUS_RENEGOTIATION_REQUIRED"></span><span id="opm_status_renegotiation_required"></span><dl><dt><strong>OPM_STATUS_RENEGOTIATION_REQUIRED</strong></dt><dt>0x02</dt></dl> | La configuration de la connexion a été modifiée. Par exemple, l’utilisateur a modifié le mode d’affichage du bureau.<br /> | 
| <span id="OPM_STATUS_TAMPERING_DETECTED"></span><span id="opm_status_tampering_detected"></span><dl><dt><strong>OPM_STATUS_TAMPERING_DETECTED</strong></dt><dt>0x04</dt></dl> | La carte graphique ou le pilote a été falsifié.<br /> Cet indicateur n’est pas utilisé en <em>mode émulation Copp</em>. Au lieu de cela, la sortie vidéo définit l’indicateur OPM_STATUS_LINK_LOST s’il détecte une falsification.<br /> | 
| <span id="OPM_STATUS_REVOKED_HDCP_DEVICE_ATTACHED"></span><span id="opm_status_revoked_hdcp_device_attached"></span><dl><dt><strong>OPM_STATUS_REVOKED_HDCP_DEVICE_ATTACHED</strong></dt><dt>0x08</dt></dl> | Un appareil révoqué High-Bandwidth Digital protection du contenu (HDCP) est attaché à la sortie vidéo.<br /> Cet indicateur d’État peut être retourné à partir d’une requête <a href="opm-get-virtual-protection-level.md">OPM_GET_VIRTUAL_PROTECTION_LEVEL</a> ou <a href="opm-get-actual-protection-level.md">OPM_GET_ACTUAL_PROTECTION_LEVEL</a> . <br /> L’appareil révoqué peut être directement attaché à la sortie vidéo ou indirectement par le biais d’un Repeater HDCP. Une sortie vidéo est nécessaire pour détecter cette condition alors que HDCP est activé, mais pas dans le cas contraire.<br /> Cet indicateur n’est pas utilisé en <em>mode émulation Copp</em>, car la sortie vidéo ne détecte pas les appareils révoqués dans ce mode.<br /> | 




## <a name="remarks"></a>Remarques

Certaines de ces constantes sont équivalentes aux valeurs de l’énumération **Copp \_ StatusFlags** utilisée dans le protocole Copp (Certified Output Protection Protocol).

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

 

 




