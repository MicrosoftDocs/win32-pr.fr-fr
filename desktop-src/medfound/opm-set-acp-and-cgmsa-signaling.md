---
description: Spécifie des informations sur le signal vidéo, autres que le niveau de protection.
ms.assetid: ed78b7eb-bf15-4068-ab86-ae42a5e62096
title: OPM_SET_ACP_AND_CGMSA_SIGNALING (Opmapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 02247c48b89e61d49afe7f8f6f3821da68ff050b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527874"
---
# <a name="opm_set_acp_and_cgmsa_signaling"></a>\_ \_ \_ signaux ACP et \_ CGMSA de \_ l’ensemble OPM

Spécifie des informations sur le signal vidéo, autres que le niveau de protection.



| Condition requise | Valeur |
|--------------|---------------------------------------------------------------------------------------------------------------------|
| GUID de la commande | \_ \_ \_ signaux ACP et \_ CGMSA de \_ l’ensemble OPM                                                                                |
| Données d’entrée   | Une [**structure \_ \_ \_ de \_ \_ \_ paramètres de signalisation ACP et CGMSA de l’ensemble OPM**](/windows/desktop/api/opmapi/ns-opmapi-opm_set_acp_and_cgmsa_signaling_parameters) |



 

## <a name="remarks"></a>Notes

Cette commande est équivalente à la \_ commande DXVA COPPSetSignaling utilisée dans le protocole Copp (Certified Output Protection Protocol).

Pour CGMS-A, certaines normes de protection requièrent que le signal de télévision contienne des informations dans les mêmes paquets de forme d’onde VBI que les bits CGMS-A. Ces informations incluent, entre autres, les proportions de l’image. Les télévisions peuvent s’afficher mal si les informations sur les proportions ne sont pas cohérentes avec le flux vidéo. L’application peut utiliser cette commande pour spécifier les proportions afin que le pilote Graphics puisse générer les paquets VBI appropriés.

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

 

 




