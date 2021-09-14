---
description: Les structures suivantes sont utilisées avec le gestionnaire de protection de sortie (OPM).
ms.assetid: 676a60ca-393e-4b5d-89d3-50cf4b771492
title: Structures OPM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b62bc7cbc13b987a2cfdda5d210cddd2fd05b8fa
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127414054"
---
# <a name="opm-structures"></a>Structures OPM

Les structures suivantes sont utilisées avec le [Gestionnaire de protection de sortie](output-protection-manager.md) (OPM).



| Structure                                                                                              | Description                                                                                                                                                |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_en-tête GRL**](grl-header.md)                                                                      | Contient l’en-tête GRL (liste de révocation globale).                                                                                                          |
| [**\_signature MF**](mf-signature.md)                                                                  | Contient une signature de liste de révocation globale (GRL).                                                                                                         |
| [**\_signalisation ACP \_ et \_ CGMSA \_ OPM**](/windows/desktop/api/opmapi/ns-opmapi-opm_acp_and_cgmsa_signaling)                                 | Contient le résultat d’une requête de signalisation de l' [**\_ offre OPM \_ \_ et \_ CGMSA \_**](opm-get-acp-and-cgmsa-signaling.md) .                                         |
| [**\_format de \_ sortie \_ réel OPM**](/windows/desktop/api/opmapi/ns-opmapi-opm_actual_output_format)                                        | Contient le résultat d’une requête [**OPM \_ obtenir le \_ \_ \_ format de sortie réel**](opm-get-actual-output-format.md) dans le gestionnaire de protection de sortie (OPM).               |
| [**\_paramètres de configuration de OPM \_**](/windows/desktop/api/opmapi/ns-opmapi-opm_configure_parameters)                                         | Contient une commande OPM ou Validal Protection Manager (COPP) certifiée.                                                                                     |
| [**\_ \_ \_ informations sur l’appareil \_ HDCP connecté à OPM**](/windows/desktop/api/opmapi/ns-opmapi-opm_connected_hdcp_device_information)             | Contient le résultat d’une requête [**OPM \_ obtenir des \_ \_ \_ \_ informations de périphérique HDCP connecté**](opm-get-connected-hdcp-device-information.md) .                     |
| [**\_paramètres d' \_ extraction \_ des \_ informations \_ compatibles pour OPM Copp**](/windows/desktop/api/opmapi/ns-opmapi-opm_copp_compatible_get_info_parameters)        | Contient des paramètres pour la méthode [**IOPMVideoOutput :: COPPCompatibleGetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-coppcompatiblegetinformation) . |
| [**\_ \_ paramètres d’initialisation du CHIFFREment OPM \_**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_encrypted_initialization_parameters)          | Contient les paramètres d’initialisation d’une session OPM.                                                                                                     |
| [**informations sur l' \_ extraction de \_ codec OPM \_ \_**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_codec_info_information)                           | Contient le résultat d’une requête d' [**\_ obtenir des \_ \_ informations de codec OPM**](opm-get-codec-info.md) .                                                                     |
| [**\_paramètres d' \_ informations de codec \_ \_ pour la récupération OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_codec_info_parameters)                             | Contient des informations pour la commande OPM obtenir les informations du [**\_ \_ codec \_**](opm-get-codec-info.md) .                                                                  |
| [**\_paramètres d’extraction d' \_ informations OPM \_**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_info_parameters)                                          | Contient des paramètres pour la méthode [**IOPMVideoOutput :: GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation) .                             |
| [**\_vecteur de \_ sélection de clé OPM HDCP \_ \_**](/windows/desktop/api/opmapi/ns-opmapi-opm_hdcp_key_selection_vector)                             | Contient le vecteur de sélection de clé (KSV) pour un récepteur HDCP (High-Bandwidth Digital protection du contenu).                                                   |
| [**\_OMAC OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_omac)                                                                          | Contient un code d’authentification de message (MAC) pour un message OPM.                                                                                           |
| [**données de l' \_ ID de sortie OPM \_ \_**](/windows/desktop/api/opmapi/ns-opmapi-opm_output_id_data)                                                    | Contient le résultat d’une demande de l’état de l’ID de sortie de la [**\_ récupération \_ \_ OPM**](opm-get-output-id.md) .                                                              |
| [**\_nombre aléatoire \_ OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_random_number)                                                       | Contient un nombre aléatoire 128 bits à utiliser avec OPM.                                                                                                         |
| [**\_informations demandées pour OPM \_**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_requested_information)                                       | Contient le résultat d’une demande d’État OPM.                                                                                                              |
| [**\_ \_ \_ paramètres de signalisation ACP et \_ CGMSA de \_ \_ l’ensemble OPM**](/windows/desktop/api/opmapi/ns-opmapi-opm_set_acp_and_cgmsa_signaling_parameters) | Contient des informations relatives à la commande de [**\_ \_ \_ \_ \_ signalisation ACP et CGMSA de l’ensemble OPM**](opm-set-acp-and-cgmsa-signaling.md) dans OPM.                               |
| [**paramètres de gestion de la gestion des risques de l' \_ ensemble OPM \_ \_ \_**](/windows/desktop/api/opmapi/ns-opmapi-opm_set_hdcp_srm_parameters)                                 | Contient les paramètres de la commande [**OPM \_ Set \_ HDCP \_ SRM**](opm-set-hdcp-srm.md) .                                                                       |
| [**\_paramètres du \_ niveau de protection \_ \_ de l’ensemble OPM**](/windows/desktop/api/opmapi/ns-opmapi-opm_set_protection_level_parameters)                 | Contient des données pour la commande de niveau de protection de l' [ \_ ensemble \_ \_ OPM](opm-set-protection-level.md) dans OPM.                                                          |
| [**\_informations standard \_ OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information)                                         | Contient le résultat d’une demande d’État OPM.                                                                                                            |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Informations de référence sur la programmation OPM](opm-programming-reference.md)
</dt> <dt>

[Gestionnaire de protection de sortie](output-protection-manager.md)
</dt> </dl>

 

 



