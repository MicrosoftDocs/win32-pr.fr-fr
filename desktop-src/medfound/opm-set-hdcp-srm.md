---
description: Met à jour le message de renouvellement du système (SRM) pour High-Bandwidth protection du contenu numérique (HDCP).
ms.assetid: ea18baba-0e03-4471-af0e-a588773c98d2
title: OPM_SET_HDCP_SRM (Opmapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9283c493598f22a1715f687eccea985a27e0e6f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201860"
---
# <a name="opm_set_hdcp_srm"></a>\_SRM Set \_ HDCP \_

Met à jour le message de renouvellement du système (SRM) pour High-Bandwidth protection du contenu numérique (HDCP).



| Condition requise | Valeur |
|--------------|-------------------------------------------------------------------------------------|
| GUID de la commande | \_SRM Set \_ HDCP \_                                                                 |
| Données d’entrée   | Une structure de [**\_ \_ \_ \_ paramètres SRM Set HDCP**](/windows/desktop/api/opmapi/ns-opmapi-opm_set_hdcp_srm_parameters) |



 

Le paramètre *pbAdditionalParameters* de [**IOPMVideoOutput :: configure**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-configure) doit pointer vers une mémoire tampon qui contient le SRM. Le format d’un SRM HDCP est documenté dans la spécification HDCP. Définissez le paramètre *ulAdditionalParametersSize* sur la taille de la mémoire tampon, en octets.

## <a name="remarks"></a>Notes

Les SRMs sont utilisés pour mettre à jour la liste des appareils HDCP révoqués. Les SRMs sont fournis avec le contenu vidéo.

Cette commande met à jour le SRM actuel de la sortie vidéo. Si la technologie HDCP est activée au moment de la commande, la sortie vidéo utilise le nouveau SRM pour vérifier si l’un des périphériques HDCP connectés est révoqué. Si la sortie vidéo détecte un appareil révoqué, elle cesse d’afficher la vidéo. Si vous envoyez cette commande alors que HDCP est désactivé, la sortie vidéo valide le SRM et le stocke. Plus tard, si l’application active HDCP, la sortie vidéo utilise le nouveau SRM pour vérifier l’état de révocation de l’appareil.

Cette commande peut faire en sorte que la méthode **configure** retourne l’un des codes d’erreur suivants.



| Code de retour                                            | Description                             |
|--------------------------------------------------------|-----------------------------------------|
| ERREUR \_ Graphics de \_ \_ SRM non valide \_                     | Le SRM n’est pas valide.                   |
| ERREUR \_ Graphics la \_ \_ sortie OPM \_ ne \_ \_ prend pas en charge \_ HDCP | La sortie vidéo ne prend pas en charge HDCP. |



 

Cette commande n’est pas prise en charge lorsque l’interface **IOPMVideoOutput** émule le protocole Copp (Certified Output Protection Protocol). Lorsque la sémantique COPP est utilisée, l’application est responsable de l’analyse de SRMs et de la vérification de l’état de révocation de l’appareil HDCP. Utilisez la demande d’état des [ \_ \_ \_ \_ \_ informations sur l’appareil OPM obtenir une connexion HDCP](opm-get-connected-hdcp-device-information.md) pour obtenir le vecteur de sélection de clé de l’appareil (KSV), qui est nécessaire pour vérifier l’état de révocation. Pour plus d’informations sur SRMs, reportez-vous à la spécification HDCP.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                      |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>Opmapi. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IOPMVideoOutput :: configure**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-configure)
</dt> <dt>

[Commandes OPM](opm-commands.md)
</dt> </dl>

 

 




