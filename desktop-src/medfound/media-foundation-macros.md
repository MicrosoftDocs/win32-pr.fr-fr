---
description: Macros Media Foundation
ms.assetid: c460b1cd-13d7-4b65-a755-23b2ea87864d
title: Macros Media Foundation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bed83710f41957edc1b945fecd5d68b5550b4ed
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "103953356"
---
# <a name="media-foundation-macros"></a>Macros Media Foundation

## <a name="in-this-section"></a>Dans cette section



| Attribut                                                                                              | Description                                                                                                                                                                  |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DÉFINIR \_ le \_ GUID du MediaType**](/windows/desktop/api/mfapi/nf-mfapi-define_mediatype_guid)<br/>                              | Définit un GUID de sous-type de média à partir d’un code FOURCC, d’une valeur **D3DFORMAT** ou d’un type de format audio.<br/>                                                                       |
| [**\_ \_ événement d’obtention \_ des \_ informations d’identification \_ de l’utilisateur**](/windows/desktop/api/mfplay/nf-mfplay-mfp_get_acquire_user_credential_event)<br/> | Effectue un cast d’un pointeur d' [**\_ \_ en-tête d’événement MFP**](/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header) en pointeur d' [**\_ \_ \_ \_ événement d’informations d’identification d’utilisateur**](/windows/desktop/api/mfplay/ns-mfplay-mfp_acquire_user_credential_event) de type MFP.<br/> |
| [**\_événement d' \_ erreur d’extraction de MFP \_**](/windows/desktop/api/mfplay/nf-mfplay-mfp_get_error_event)<br/>                                       | Effectue un cast d’un pointeur d' [**\_ \_ en-tête d’événement MFP**](/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header) en pointeur d' [**\_ \_ événement d’erreur MFP**](/windows/desktop/api/mfplay/ns-mfplay-mfp_error_event) .<br/>                                       |
| [**\_événement d’étape d’extraction de \_ Frame MFP \_ \_**](/windows/desktop/api/mfplay/nf-mfplay-mfp_get_frame_step_event)<br/>                            | Effectue un cast d’un pointeur d' [**\_ \_ en-tête d’événement MFP**](/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header) en pointeur d' [**événement d' \_ \_ étape \_ de trame MFP**](/windows/desktop/api/mfplay/ns-mfplay-mfp_frame_step_event) .<br/>                            |
| [**\_événement d' \_ \_ effacement de l’MEDIAITEM MFP \_**](/windows/desktop/api/mfplay/nf-mfplay-mfp_get_mediaitem_cleared_event)<br/>              | Effectue un cast d’un pointeur d' [**\_ \_ en-tête d’événement MFP**](/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header) en pointeur d' [**\_ \_ événement MEDIAITEM effacé**](/windows/desktop/api/mfplay/ns-mfplay-mfp_mediaitem_cleared_event) .<br/>                   |
| [**\_événement de \_ création de MEDIAITEM \_ \_ MFP**](/windows/desktop/api/mfplay/nf-mfplay-mfp_get_mediaitem_created_event)<br/>              | Effectue un cast d’un pointeur d' [**\_ \_ en-tête d’événement MFP**](/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header) en pointeur d' [**\_ \_ \_ événement MEDIAITEM créé par MFP**](/windows/desktop/api/mfplay/ns-mfplay-mfp_mediaitem_created_event) .<br/>              |
| [**\_événement de \_ jeu de MEDIAITEM de prise en main \_ \_**](/windows/desktop/api/mfplay/nf-mfplay-mfp_get_mediaitem_set_event)<br/>                      | Effectue un cast d’un pointeur d' [**\_ \_ en-tête d’événement MFP**](/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header) en pointeur d' [**\_ \_ \_ événement Set MFP MEDIAITEM**](/windows/desktop/api/mfplay/ns-mfplay-mfp_mediaitem_set_event) .<br/>                      |
| [**événement de prise en main de MFP \_ \_ MF \_**](/windows/desktop/api/mfplay/nf-mfplay-mfp_get_mf_event)<br/>                                             | Effectue un cast d’un pointeur d' [**\_ \_ en-tête d’événement MFP**](/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header) vers un pointeur d' [**\_ \_ événement MFP MF**](/windows/win32/api/mfplay/ns-mfplay-mfp_mf_event) .<br/>                                              |
| [**événement d’interruption de la prise en main de MFP \_ \_ \_**](/windows/desktop/api/mfplay/nf-mfplay-mfp_get_pause_event)<br/>                                       | Effectue un cast d’un pointeur d' [**\_ \_ en-tête d’événement MFP**](/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header) en pointeur d' [**\_ \_ événement de pause MFP**](/windows/desktop/api/mfplay/ns-mfplay-mfp_pause_event) .<br/>                                       |
| [**\_événement de \_ lecture \_ MFP**](/windows/desktop/api/mfplay/nf-mfplay-mfp_get_play_event)<br/>                                         | Effectue un cast d’un pointeur d' [**\_ \_ en-tête d’événement MFP**](/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header) en pointeur d' [**\_ \_ événement de lecture MFP**](/windows/desktop/api/mfplay/ns-mfplay-mfp_play_event) .<br/>                                         |
| [**événement MFP d' \_ extraction de \_ lecture \_ terminée \_**](/windows/desktop/api/mfplay/nf-mfplay-mfp_get_playback_ended_event)<br/>                    | Effectue un cast d’un pointeur d' [**\_ \_ en-tête d’événement MFP**](/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header) en pointeur d' [**événement de \_ lecture MFP \_ terminé \_**](/windows/desktop/api/mfplay/ns-mfplay-mfp_playback_ended_event) .<br/>                    |
| [**événement de l’ensemble de positions d' \_ extraction de MFP \_ \_ \_**](/windows/desktop/api/mfplay/nf-mfplay-mfp_get_position_set_event)<br/>                        | Effectue un cast d’un pointeur d' [**\_ \_ en-tête d’événement MFP**](/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header) en pointeur d' [**événement de \_ jeu de positions \_ \_ MFP**](/windows/desktop/api/mfplay/ns-mfplay-mfp_position_set_event) .<br/>                        |
| [**\_événement d' \_ ensemble de taux d’extraction de MFP \_ \_**](/windows/desktop/api/mfplay/nf-mfplay-mfp_get_rate_set_event)<br/>                                | Convertit un pointeur d' [**\_ \_ en-tête d’événement MFP**](/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header) en pointeur d' [**événement d' \_ ensemble de taux \_ \_ MFP**](/windows/desktop/api/mfplay/ns-mfplay-mfp_rate_set_event) .<br/>                                |
| [**\_événement d' \_ arrêt de MFP \_**](/windows/desktop/api/mfplay/nf-mfplay-mfp_get_stop_event)<br/>                                         | Effectue un cast d’un pointeur d' [**\_ \_ en-tête d’événement MFP**](/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header) vers un pointeur d' [**\_ \_ événement d’arrêt MFP**](/windows/desktop/api/mfplay/ns-mfplay-mfp_stop_event) .<br/>                                         |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Référence de programmation Media Foundation](media-foundation-programming-reference.md)
</dt> </dl>

 

 
