---
description: Demandes d’État OPM
ms.assetid: 428d08c6-e9f0-49fb-9ef9-d0f95416669d
title: Demandes d’État OPM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cdbf7338fe1309feb49fd191e3f4a1a22f3639b4
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120174"
---
# <a name="opm-status-requests"></a>Demandes d’État OPM

Cette section répertorie les demandes d’état disponibles pour le [Gestionnaire de protection de sortie](output-protection-manager.md) (OPM). Pour envoyer une demande d’État OPM, appelez [**IOPMVideoOutput :: GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation). Pour chaque demande, les informations suivantes sont affichées.



| Value             | Description                                                                                                                                                           |
|--------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| GUID de la demande | Identifie la requête. Définissez la valeur du membre **guidSetting** de la structure des paramètres de l' [**extraction d' \_ \_ informations \_ OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_info_parameters) égale à cette valeur. |
| Données d’entrée   | Spécifie comment interpréter le tableau **abParameters** dans la structure des paramètres de l' [**obtention d' \_ \_ informations \_ OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_info_parameters) .                      |
| Données de sortie  | Spécifie comment interpréter le tableau **abRequestedInformation** dans la structure d' [**\_ \_ informations demandée par OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_requested_information) .         |



 

Les demandes d’État suivantes sont définies :



| Demande d’État                                                                                      | Description                                                                                                                                           |
|-----------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_prise en \_ main \_ des signaux ACP et \_ CGMSA \_ pour OPM**](opm-get-acp-and-cgmsa-signaling.md)                     | Retourne les informations suivantes sur une sortie vidéo :                                                                                               |
| [**\_format de \_ \_ sortie OPM \_ obtenu**](opm-get-actual-output-format.md)                            | Retourne une description du signal vidéo qui est transmis sur le connecteur.                                                               |
| [**\_niveau de \_ \_ protection \_ de l’offre OPM**](opm-get-actual-protection-level.md)                      | Retourne le niveau de protection global pour un mécanisme de protection spécifié.                                                                             |
| [**TYPE de bus d’accès de l' \_ \_ adaptateur OPM \_ \_**](opm-get-adapter-bus-type.md)                                    | Retourne le type de bus d’e/s utilisé par la sortie vidéo.                                                                                                 |
| [**\_informations sur l’extraction de \_ codec OPM \_**](opm-get-codec-info.md)                                                 | Obtient la valeur mérite d’un codec matériel.                                                                                                             |
| [**\_ \_ \_ \_ informations sur l’appareil HDCP \_ connexion à OPM**](opm-get-connected-hdcp-device-information.md) | Obtient des informations sur un appareil High-Bandwidth Digital protection du contenu (HDCP) attaché à la sortie vidéo. Les informations suivantes sont retournées : |
| [**\_type de \_ connecteur d’extraction OPM \_**](opm-get-connector-type.md)                                         | Retourne le type de connecteur physique de la sortie vidéo.                                                                                              |
| [**Procurez-vous la \_ \_ \_ version actuelle HDCP \_ SRM \_**](opm-get-current-hdcp-srm-version.md)                   | Retourne le numéro de version du message de renouvellement du système (SRM) actuellement utilisé par la sortie vidéo.                                               |
| [**\_ \_ caractéristiques DVI de l’offre OPM \_**](opm-get-dvi-characteristics.md)                               | Demande si un connecteur DVI (Digital Video Interface) prend en charge DVI version 1,1 ou ultérieure.                                                          |
| [**ID de sortie de l' \_ extraction OPM \_ \_**](opm-get-output-id.md)                                                   | Retourne l’identificateur unique de l’analyseur associé à cette sortie vidéo.                                                                       |
| [**\_types de \_ \_ protection compatibles \_ avec OPM**](opm-get-supported-protection-types.md)                | Retourne la liste des mécanismes de protection pris en charge par le connecteur.                                                                        |
| [**\_niveau de \_ \_ protection \_ de l’offre OPM**](opm-get-virtual-protection-level.md)                    | Retourne le niveau de protection virtuel pour un mécanisme de protection spécifié.                                                                            |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Informations de référence sur la programmation OPM](opm-programming-reference.md)
</dt> <dt>

[Gestionnaire de protection de sortie](output-protection-manager.md)
</dt> </dl>

 

 



