---
title: Constantes WINBIO_REJECT_DETAIL ( \_ types WINBIO. h)
description: Spécifiez la raison pour laquelle une procédure d’identification ou de capture d’empreinte digitale biométrique a échoué.
ms.assetid: b1ae4e65-9e53-42dd-99ba-1910b72688dd
topic_type:
- apiref
api_name:
- WINBIO_FP_TOO_HIGH
- WINBIO_FP_TOO_LOW
- WINBIO_FP_TOO_LEFT
- WINBIO_FP_TOO_RIGHT
- WINBIO_FP_TOO_FAST
- WINBIO_FP_TOO_SLOW
- WINBIO_FP_POOR_QUALITY
- WINBIO_FP_TOO_SKEWED
- WINBIO_FP_TOO_SHORT
- WINBIO_FP_MERGE_FAILURE
- WINBIO_REJECT_DETAIL_ANTI_SPOOF_MASK
- WINBIO_REJECT_DETAIL_POSITION_MASK
- WINBIO_REJECT_DETAIL_REASON_MASK
- WINBIO_IRIS_POOR_QUALITY
- WINBIO_IRIS_TOO_BRIGHT
- WINBIO_IRIS_TOO_DARK
- WINBIO_IRIS_SPOOF_DETECTED
- WINBIO_IRIS_TOO_SKEWED
- WINBIO_IRIS_TOO_CLOSED
- WINBIO_IRIS_GLARE
- WINBIO_IRIS_DIRTY_LENS
- WINBIO_IRIS_POOR_FOCUS
- WINBIO_IRIS_WRONG_ORIENTATION
- WINBIO_IRIS_TOO_HIGH
- WINBIO_IRIS_TOO_LOW
- WINBIO_IRIS_TOO_LEFT
- WINBIO_IRIS_TOO_RIGHT
- WINBIO_IRIS_TOO_NEAR
- WINBIO_IRIS_TOO_FAR
- WINBIO_FACE_POOR_QUALITY
- WINBIO_FACE_TOO_BRIGHT
- WINBIO_FACE_TOO_DARK
- WINBIO_FACE_SPOOF_DETECTED
- WINBIO_FACE_AMBIGUOUS_TARGET
- WINBIO_FACE_EYES_OCCLUDED
- WINBIO_FACE_WRONG_ORIENTATION
- WINBIO_FACE_TOO_HIGH
- WINBIO_FACE_TOO_LOW
- WINBIO_FACE_TOO_LEFT
- WINBIO_FACE_TOO_RIGHT
- WINBIO_FACE_TOO_NEAR
- WINBIO_FACE_TOO_FAR
api_location:
- winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad5ac7a2f96555aa8ccfb305c66061ba4e0ffd468f18a1a93be215c367f034be
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118909347"
---
# <a name="winbio_reject_detail-constants"></a>WINBIO \_ rejeter les \_ constantes de détail

Les constantes suivantes peuvent être utilisées pour spécifier la raison de l’échec d’une procédure d’identification ou de capture d’empreintes digitales biométriques.



| Constante                                                                                                                                                                                                                                        | Description                                                                                                                                                                                                                                                                                       |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_FP_TOO_HIGH"></span><span id="winbio_fp_too_high"></span><dl> <dt>**WINBIO \_ FP \_ trop \_ élevé**</dt> </dl>                                                                  | L’analyse Finger a commencé trop haut sur le doigt.<br/>                                                                                                                                                                                                                                          |
| <span id="WINBIO_FP_TOO_LOW"></span><span id="winbio_fp_too_low"></span><dl> <dt>**WINBIO \_ FP \_ trop \_ faible**</dt> </dl>                                                                     | L’analyse Finger a commencé trop bas sur le doigt.<br/>                                                                                                                                                                                                                                           |
| <span id="WINBIO_FP_TOO_LEFT"></span><span id="winbio_fp_too_left"></span><dl> <dt>**WINBIO \_ FP \_ trop à \_ gauche**</dt> </dl>                                                                  | Le doigt était trop éloigné au cours de l’analyse.<br/>                                                                                                                                                                                                                                           |
| <span id="WINBIO_FP_TOO_RIGHT"></span><span id="winbio_fp_too_right"></span><dl> <dt>**WINBIO \_ FP \_ trop à \_ droite**</dt> </dl>                                                               | Le doigt était trop bien au cours de l’analyse.<br/>                                                                                                                                                                                                                                          |
| <span id="WINBIO_FP_TOO_FAST"></span><span id="winbio_fp_too_fast"></span><dl> <dt>**WINBIO \_ FP \_ trop \_ Fast**</dt> </dl>                                                                  | Le doigt a été balayé trop rapidement sur le capteur.<br/>                                                                                                                                                                                                                                       |
| <span id="WINBIO_FP_TOO_SLOW"></span><span id="winbio_fp_too_slow"></span><dl> <dt>**WINBIO \_ FP \_ trop \_ lent**</dt> </dl>                                                                  | Le doigt a été balayé trop lentement sur le capteur.<br/>                                                                                                                                                                                                                                        |
| <span id="WINBIO_FP_POOR_QUALITY"></span><span id="winbio_fp_poor_quality"></span><dl> <dt>**\_ \_ qualité médiocre de WINBIO FP \_**</dt> </dl>                                                      | La qualité de l’analyse est trop médiocre.<br/>                                                                                                                                                                                                                                                         |
| <span id="WINBIO_FP_TOO_SKEWED"></span><span id="winbio_fp_too_skewed"></span><dl> <dt>**WINBIO \_ FP \_ trop \_ incliné**</dt> </dl>                                                            | Le doigt n’a pas réussi à traverser le capteur.<br/>                                                                                                                                                                                                                                    |
| <span id="WINBIO_FP_TOO_SHORT"></span><span id="winbio_fp_too_short"></span><dl> <dt>**WINBIO \_ FP \_ trop \_ petit**</dt> </dl>                                                               | Le doigt n’a pas été analysé.<br/>                                                                                                                                                                                                                                                  |
| <span id="WINBIO_FP_MERGE_FAILURE"></span><span id="winbio_fp_merge_failure"></span><dl> <dt>**échec de la \_ fusion WINBIO FP \_ \_**</dt> </dl>                                                   | Les captures d’empreintes digitales n’ont pas pu être combinées.<br/>                                                                                                                                                                                                                                        |
| <span id="WINBIO_REJECT_DETAIL_ANTI_SPOOF_MASK____"></span><span id="winbio_reject_detail_anti_spoof_mask____"></span><dl> <dt>**WINBIO \_ REFUSER \_ le \_ \_ \_ masque anti-usurpation des détails**</dt> </dl> | Ce masque couvre les 8 bits de poids fort de la valeur de rejet des détails où se trouvent les comportements de preuve de l’activité. Cette valeur est prise en charge à partir de Windows 10.<br/>                                                                                                                        |
| <span id="WINBIO_REJECT_DETAIL_POSITION_MASK______"></span><span id="winbio_reject_detail_position_mask______"></span><dl> <dt>**WINBIO \_ REJETER \_ le \_ \_ masque de position de détail**</dt> </dl>    | Ce masque couvre la plage de bits consacrée aux erreurs de position. Cette valeur est prise en charge à partir de Windows 10.<br/>                                                                                                                                                                         |
| <span id="WINBIO_REJECT_DETAIL_REASON_MASK"></span><span id="winbio_reject_detail_reason_mask"></span><dl> <dt>**\_masque de \_ \_ motif de refus WINBIO \_**</dt> </dl>                       | Ce masque couvre les 16 bits inférieurs où se trouve la raison énumérée du rejet. Cette valeur est prise en charge à partir de Windows 10.<br/>                                                                                                                                           |
| <span id="WINBIO_IRIS_POOR_QUALITY"></span><span id="winbio_iris_poor_quality"></span><dl> <dt>**WINBIO \_ Iris \_ - \_ qualité médiocre**</dt> </dl>                                                | Les conditions ont entraîné la capture d’une image médiocre par l’appareil photo. Demandez à l’utilisateur de nettoyer le capteur et de relancer l’analyse. Cette valeur est prise en charge à partir de Windows 10.<br/>                                                                                                                        |
| <span id="WINBIO_IRIS_TOO_BRIGHT"></span><span id="winbio_iris_too_bright"></span><dl> <dt>**WINBIO \_ Iris \_ trop \_ brillant**</dt> </dl>                                                      | L’image comprend une lumière ambiante trop importante pour obtenir une bonne correspondance. Demandez à l’utilisateur de s’assurer qu’il ne se trouve pas face à une autre source de lumière brillante. Cette valeur est prise en charge à partir de Windows 10.<br/>                                                                                        |
| <span id="WINBIO_IRIS_TOO_DARK"></span><span id="winbio_iris_too_dark"></span><dl> <dt>**WINBIO \_ Iris \_ trop \_ sombre**</dt> </dl>                                                            | L’image est trop sombre pour obtenir une correspondance correcte. Demandez à l’utilisateur de s’assurer que son Iris n’est pas masqué par des éléments tels qu’un voile, des verres sombres ou des contacts colorés. Cette valeur est prise en charge à partir de Windows 10.<br/>                                                                     |
| <span id="WINBIO_IRIS_SPOOF_DETECTED"></span><span id="winbio_iris_spoof_detected"></span><dl> <dt>**\_usurpation d’IRIS WINBIO \_ \_ détectée**</dt> </dl>                                          | Le composant reconnaissance estime que le diaphragme n’est pas en ligne, mais provient d’un flux vidéo relu, d’une photo ou d’un sculpture 3D. Cette valeur est prise en charge à partir de Windows 10.<br/>                                                                                                   |
| <span id="WINBIO_IRIS_TOO_SKEWED"></span><span id="winbio_iris_too_skewed"></span><dl> <dt>**\_Iris WINBIO \_ trop \_ incliné**</dt> </dl>                                                      | L’utilisateur ne regarde pas directement à l’appareil photo. Demandez à l’utilisateur de regarder directement à l’appareil photo et de relancer l’analyse. Cette valeur est prise en charge à partir de Windows 10.<br/>                                                                                                                       |
| <span id="WINBIO_IRIS_TOO_CLOSED"></span><span id="winbio_iris_too_closed"></span><dl> <dt>**\_Iris WINBIO \_ trop \_ fermé**</dt> </dl>                                                      | Le eyelids de l’utilisateur masque l’iris. Demandez à l’utilisateur d’ouvrir ses yeux un peu plus et de relancer l’analyse. Cette valeur est prise en charge à partir de Windows 10.<br/>                                                                                                                          |
| <span id="WINBIO_IRIS_GLARE"></span><span id="winbio_iris_glare"></span><dl> <dt>**WINBIO \_ Iris \_ reflet**</dt> </dl>                                                                      | L’image comprend un reflet de la lentille. Demandez à l’utilisateur de supprimer ses verres et de relancer l’analyse. Cette valeur est prise en charge à partir de Windows 10.<br/>                                                                                                                                               |
| <span id="WINBIO_IRIS_DIRTY_LENS"></span><span id="winbio_iris_dirty_lens"></span><dl> <dt>**WINBIO \_ Iris- \_ lentille incorrecte \_**</dt> </dl>                                                      | L’objectif de l’appareil photo a été modifié. Demandez à l’utilisateur de nettoyer la lentille et de relancer l’analyse. Cette valeur est prise en charge à partir de Windows 10.<br/>                                                                                                                                                         |
| <span id="WINBIO_IRIS_POOR_FOCUS"></span><span id="winbio_iris_poor_focus"></span><dl> <dt>**WINBIO \_ Iris \_ - \_ focus faible**</dt> </dl>                                                      | Ce Iris est prêt à l’emploi. Cette valeur est prise en charge à partir de Windows 10.<br/>                                                                                                                                                                                                             |
| <span id="WINBIO_IRIS_WRONG_ORIENTATION"></span><span id="winbio_iris_wrong_orientation"></span><dl> <dt>**\_ \_ orientation incorrecte de WINBIO Iris \_**</dt> </dl>                                 | L’orientation de la caméra ne correspond pas à l’orientation obligatoire que spécifie la structure d' [**\_ \_ \_ informations sur le capteur étendu WINBIO**](winbio-extended-sensor-info.md) . Demandez à l’utilisateur de modifier l’orientation de l’appareil photo et de relancer l’analyse. Cette valeur est prise en charge à partir de Windows 10.<br/> |
| <span id="WINBIO_IRIS_TOO_HIGH"></span><span id="winbio_iris_too_high"></span><dl> <dt>**WINBIO \_ Iris \_ trop \_ élevé**</dt> </dl>                                                            | Le diaphragme est orienté vers le haut. Demandez à l’utilisateur de rechercher un peu moins de choses et de relancer l’analyse. Cette valeur est prise en charge à partir de Windows 10.<br/>                                                                                                                                                     |
| <span id="WINBIO_IRIS_TOO_LOW"></span><span id="winbio_iris_too_low"></span><dl> <dt>**WINBIO \_ Iris \_ trop \_ bas**</dt> </dl>                                                               | Le diaphragme est orienté vers le dessous. Demandez à l’utilisateur de rechercher un petit bit et de relancer l’analyse. Cette valeur est prise en charge à partir de Windows 10.<br/>                                                                                                                                                     |
| <span id="WINBIO_IRIS_TOO_LEFT"></span><span id="winbio_iris_too_left"></span><dl> <dt>**WINBIO \_ Iris \_ trop à \_ gauche**</dt> </dl>                                                            | L’iris est trop éloigné de la gauche. Demandez à l’utilisateur d’afficher un peu plus à droite et de relancer l’analyse. Cette valeur est prise en charge à partir de Windows 10.<br/>                                                                                                                                  |
| <span id="WINBIO_IRIS_TOO_RIGHT"></span><span id="winbio_iris_too_right"></span><dl> <dt>**WINBIO \_ Iris \_ trop à \_ droite**</dt> </dl>                                                         | L’iris est trop à droite. Demandez à l’utilisateur d’examiner un peu plus à gauche et de relancer l’analyse. Cette valeur est prise en charge à partir de Windows 10.<br/>                                                                                                                                  |
| <span id="WINBIO_IRIS_TOO_NEAR"></span><span id="winbio_iris_too_near"></span><dl> <dt>**WINBIO \_ Iris \_ trop \_ proche**</dt> </dl>                                                            | L’iris est trop près de l’appareil photo. Demandez à l’utilisateur de déplacer un peu plus loin et d’effectuer une nouvelle analyse. Cette valeur est prise en charge à partir de Windows 10.<br/>                                                                                                                                   |
| <span id="WINBIO_IRIS_TOO_FAR"></span><span id="winbio_iris_too_far"></span><dl> <dt>**WINBIO \_ Iris \_ trop \_ éloigné**</dt> </dl>                                                               | L’iris est trop éloigné de l’appareil photo. Demandez à l’utilisateur de déplacer un peu plus près et de relancer l’analyse. Cette valeur est prise en charge à partir de Windows 10.<br/>                                                                                                                                         |
| <span id="WINBIO_FACE_POOR_QUALITY"></span><span id="winbio_face_poor_quality"></span><dl> <dt>**WINBIO \_ de \_ \_ qualité médiocre**</dt> </dl>                                                | Les conditions ont entraîné la capture d’une image médiocre par l’appareil photo. Demandez à l’utilisateur de nettoyer le capteur et de relancer l’analyse. Cette valeur est prise en charge à partir de Windows 10.<br/>                                                                                                                        |
| <span id="WINBIO_FACE_TOO_BRIGHT"></span><span id="winbio_face_too_bright"></span><dl> <dt>**WINBIO \_ \_ trop \_ brillant**</dt> </dl>                                                      | L’image comprend une lumière ambiante trop importante pour obtenir une bonne correspondance. Demandez à l’utilisateur de s’assurer qu’il ne se trouve pas face à une autre source de lumière brillante. Cette valeur est prise en charge à partir de Windows 10.<br/>                                                                                        |
| <span id="WINBIO_FACE_TOO_DARK"></span><span id="winbio_face_too_dark"></span><dl> <dt>**WINBIO d’un \_ visage \_ trop \_ sombre**</dt> </dl>                                                            | L’image est trop sombre pour obtenir une correspondance correcte. Cette valeur est prise en charge à partir de Windows 10.<br/>                                                                                                                                                                                             |
| <span id="WINBIO_FACE_SPOOF_DETECTED"></span><span id="winbio_face_spoof_detected"></span><dl> <dt>**\_usurpation de visage WINBIO \_ \_ détectée**</dt> </dl>                                          | Le composant reconnaissance pense que la face n’est pas active, mais provient d’un flux vidéo relu, d’une photo ou d’un sculpture 3D. Cette valeur est prise en charge à partir de Windows 10.<br/>                                                                                                   |
| <span id="WINBIO_FACE_AMBIGUOUS_TARGET"></span><span id="winbio_face_ambiguous_target"></span><dl> <dt>**\_cible WINBIO face \_ ambiguë \_**</dt> </dl>                                    | Au moins deux visages se chevauchent dans le cadre de l’appareil photo. Cette valeur est prise en charge à partir de Windows 10.<br/>                                                                                                                                                                                     |
| <span id="WINBIO_FACE_EYES_OCCLUDED"></span><span id="winbio_face_eyes_occluded"></span><dl> <dt>**WINBIO \_ \_ yeux \_ bloqués**</dt> </dl>                                             | Les yeux de l’utilisateur sont bloqués. Demandez à l’utilisateur de s’assurer que ses yeux ne sont pas obscurcis par des éléments tels qu’un voile, des verres sombres ou des contacts colorés. Cette valeur est prise en charge à partir de Windows 10.<br/>                                                                                 |
| <span id="WINBIO_FACE_WRONG_ORIENTATION"></span><span id="winbio_face_wrong_orientation"></span><dl> <dt>**\_ \_ orientation incorrecte de la face WINBIO \_**</dt> </dl>                                 | L’orientation de la caméra ne correspond pas à l’orientation obligatoire que spécifie la structure d' [**\_ \_ \_ informations sur le capteur étendu WINBIO**](winbio-extended-sensor-info.md) . Demandez à l’utilisateur de modifier l’orientation de l’appareil photo et de relancer l’analyse. Cette valeur est prise en charge à partir de Windows 10.<br/> |
| <span id="WINBIO_FACE_TOO_HIGH"></span><span id="winbio_face_too_high"></span><dl> <dt>**WINBIO \_ face \_ trop \_ élevée**</dt> </dl>                                                            | Le visage est orienté vers le haut. Demandez à l’utilisateur de rechercher un peu moins de choses et de relancer l’analyse. Cette valeur est prise en charge à partir de Windows 10.<br/>                                                                                                                                                     |
| <span id="WINBIO_FACE_TOO_LOW"></span><span id="winbio_face_too_low"></span><dl> <dt>**\_visage WINBIO \_ trop \_ faible**</dt> </dl>                                                               | Le visage est orienté vers le dessous. Demandez à l’utilisateur de rechercher un petit bit et de relancer l’analyse. Cette valeur est prise en charge à partir de Windows 10.<br/>                                                                                                                                                     |
| <span id="WINBIO_FACE_TOO_LEFT"></span><span id="winbio_face_too_left"></span><dl> <dt>**WINBIO \_ face \_ \_ gauche**</dt> </dl>                                                            | La face est trop éloignée de la gauche. Demandez à l’utilisateur de déplacer un peu plus vers la droite et de relancer l’analyse. Cette valeur est prise en charge à partir de Windows 10.<br/>                                                                                                                                  |
| <span id="WINBIO_FACE_TOO_RIGHT"></span><span id="winbio_face_too_right"></span><dl> <dt>**WINBIO \_ la \_ face \_ droite**</dt> </dl>                                                         | Le visage est trop loin vers la droite. Demandez à l’utilisateur de déplacer un peu plus vers la gauche et de relancer l’analyse. Cette valeur est prise en charge à partir de Windows 10.<br/>                                                                                                                                  |
| <span id="WINBIO_FACE_TOO_NEAR"></span><span id="winbio_face_too_near"></span><dl> <dt>**WINBIO \_ face \_ trop \_ proche**</dt> </dl>                                                            | Le visage est trop près de l’appareil photo. Demandez à l’utilisateur de déplacer un peu plus loin et d’effectuer une nouvelle analyse. Cette valeur est prise en charge à partir de Windows 10.<br/>                                                                                                                                   |
| <span id="WINBIO_FACE_TOO_FAR"></span><span id="winbio_face_too_far"></span><dl> <dt>**WINBIO \_ visage \_ trop \_ loin**</dt> </dl>                                                               | Le visage est trop éloigné de l’appareil photo. Demandez à l’utilisateur de déplacer un peu plus près et de relancer l’analyse. Cette valeur est prise en charge à partir de Windows 10.<br/>                                                                                                                                         |



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 uniquement\]<br/>                                                                                                                               |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 R2, \[ applications de bureau uniquement\]<br/>                                                                                                                  |
| En-tête<br/>                   | <dl> <dt>WinBio \_ types. h (inclure WinBio. h pour les applications clientes ou les \_ cartes WinBio. h pour les adaptateurs)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Constantes d’application cliente](client-application-constants.md)
</dt> </dl>

 

 





