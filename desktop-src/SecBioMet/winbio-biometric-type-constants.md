---
title: Constantes WINBIO_BIOMETRIC_TYPE ( \_ types WINBIO. h)
description: types biométriques Standard définis par le National Institute of Standards and Technology Information (NISTIR) 6529-A, également connu sous le nom de CBEFF (Common biometric Exchange Formats).
ms.assetid: DCBDB5F9-FF81-44C1-B439-2B8C02483212
topic_type:
- apiref
api_name:
- WINBIO_STANDARD_TYPE_MASK
- WINBIO_NO_TYPE_AVAILABLE
- WINBIO_TYPE_MULTIPLE
- WINBIO_TYPE_FACIAL_FEATURES
- WINBIO_TYPE_VOICE
- WINBIO_TYPE_FINGERPRINT
- WINBIO_TYPE_IRIS
- WINBIO_TYPE_RETINA
- WINBIO_TYPE_HAND_GEOMETRY
- WINBIO_TYPE_SIGNATURE_DYNAMICS
- WINBIO_TYPE_KEYSTROKE_DYNAMICS
- WINBIO_TYPE_LIP_MOVEMENT
- WINBIO_TYPE_THERMAL_FACE_IMAGE
- WINBIO_TYPE_THERMAL_HAND_IMAGE
- WINBIO_TYPE_GAIT
- WINBIO_TYPE_SCENT
- WINBIO_TYPE_DNA
- WINBIO_TYPE_EAR_SHAPE
- WINBIO_TYPE_FINGER_GEOMETRY
- WINBIO_TYPE_PALM_PRINT
- WINBIO_TYPE_VEIN_PATTERN
- WINBIO_TYPE_FOOT_PRINT
- WINBIO_TYPE_OTHER
- WINBIO_TYPE_PASSWORD
- WINBIO_TYPE_ANY
api_location:
- winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c1b6475433d2c0d1432e7501e6cbda46436c5a54fd13d5f254f79b678b3f7bb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118911068"
---
# <a name="winbio_biometric_type-constants"></a>\_Constantes de type de biométrie WINBIO \_

les constantes suivantes représentent les types biométriques standard définis par le National Institute of Standards and Technology Information (NISTIR) 6529-A, également connu sous le nom de CBEFF (Common biometric Exchange formates). Seule **une \_ \_ empreinte digitale de type WINBIO** est actuellement prise en charge.



| Constante                                                                                                                                                                                                            | Description                                                                                                                              |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_STANDARD_TYPE_MASK"></span><span id="winbio_standard_type_mask"></span><dl> <dt>**\_masque de \_ type \_ standard WINBIO**</dt> </dl>                 | Masque de masque qui spécifie l’ensemble de facteurs biométriques pris en charge.<br/>                                                                |
| <span id="WINBIO_NO_TYPE_AVAILABLE"></span><span id="winbio_no_type_available"></span><dl> <dt>**WINBIO \_ aucun \_ type \_ disponible**</dt> </dl>                    | Aucun type biométrique n’est disponible.<br/>                                                                                               |
| <span id="WINBIO_TYPE_MULTIPLE"></span><span id="winbio_type_multiple"></span><dl> <dt>**TYPE de WINBIO \_ \_ multiple**</dt> </dl>                                 | Plusieurs types sont spécifiés.<br/>                                                                                                 |
| <span id="WINBIO_TYPE_FACIAL_FEATURES"></span><span id="winbio_type_facial_features"></span><dl> <dt>**\_caractéristiques du \_ visage de type WINBIO \_**</dt> </dl>           | Les fonctionnalités faciales sont utilisées pour déterminer l’identité d’un individu.<br/>                                                          |
| <span id="WINBIO_TYPE_VOICE"></span><span id="winbio_type_voice"></span><dl> <dt>**WINBIO \_ type \_ vocal**</dt> </dl>                                          | La fréquence et les modèles de volume dans la voix d’un individu sont utilisés pour déterminer l’identité d’un individu.<br/>              |
| <span id="WINBIO_TYPE_FINGERPRINT"></span><span id="winbio_type_fingerprint"></span><dl> <dt>**\_empreinte digitale de type WINBIO \_**</dt> </dl>                        | Les modèles d’empreintes digitales permettent de déterminer l’identité d’un individu.<br/>                                                     |
| <span id="WINBIO_TYPE_IRIS"></span><span id="winbio_type_iris"></span><dl> <dt>**WINBIO \_ type \_ IRIS**</dt> </dl>                                             | Les modèles d’IRIS sont utilisés pour déterminer l’identité d’un individu. Cette valeur est prise en charge à partir de Windows 10.<br/>            |
| <span id="WINBIO_TYPE_RETINA"></span><span id="winbio_type_retina"></span><dl> <dt>**WINBIO de \_ type \_ RETINE**</dt> </dl>                                       | Les modèles de veine dans la rétine sont utilisés pour déterminer l’identité d’un individu.<br/>                                              |
| <span id="WINBIO_TYPE_HAND_GEOMETRY"></span><span id="winbio_type_hand_geometry"></span><dl> <dt>**WINBIO \_ géométrie de type \_ main \_**</dt> </dl>                 | La forme d’une main d’un individu est utilisée pour déterminer l’identité d’un individu.<br/>                                      |
| <span id="WINBIO_TYPE_SIGNATURE_DYNAMICS"></span><span id="winbio_type_signature_dynamics"></span><dl> <dt>**WINBIO de \_ type de \_ signature \_ Dynamics**</dt> </dl>  | Les modèles de force que l’individu utilise lorsqu’ils signent leur nom sont utilisés pour déterminer l’identité d’un individu.<br/> |
| <span id="WINBIO_TYPE_KEYSTROKE_DYNAMICS"></span><span id="winbio_type_keystroke_dynamics"></span><dl> <dt>**WINBIO \_ de \_ frappe de frappe de type \_**</dt> </dl>  | Les modèles de vitesse et d’erreur utilisés pour la saisie par un individu permettent de déterminer l’identité d’un individu.<br/>                  |
| <span id="WINBIO_TYPE_LIP_MOVEMENT"></span><span id="winbio_type_lip_movement"></span><dl> <dt>**WINBIO \_ TYPE \_ de \_ mouvement LIP**</dt> </dl>                    | Les modifications apportées aux lèvres d’une personne qui se produisent quand elles parlent sont utilisées pour déterminer l’identité d’un individu.<br/>      |
| <span id="WINBIO_TYPE_THERMAL_FACE_IMAGE"></span><span id="winbio_type_thermal_face_image"></span><dl> <dt>**\_image de \_ \_ face thermique de type \_ WINBIO**</dt> </dl> | Les modèles de température en face d’un individu sont utilisés pour déterminer l’identité d’un individu.<br/>                    |
| <span id="WINBIO_TYPE_THERMAL_HAND_IMAGE"></span><span id="winbio_type_thermal_hand_image"></span><dl> <dt>**\_image de \_ la \_ main \_ thermique de type WINBIO**</dt> </dl> | Les modèles de température de la part d’un individu sont utilisés pour déterminer l’identité d’un individu.<br/>                    |
| <span id="WINBIO_TYPE_GAIT"></span><span id="winbio_type_gait"></span><dl> <dt>**TYPE de WINBIO \_ \_**</dt> </dl>                                             | Les modèles de mouvement qui se produisent lorsque les parcours individuels sont utilisés pour déterminer l’identité d’un individu.<br/>            |
| <span id="WINBIO_TYPE_SCENT"></span><span id="winbio_type_scent"></span><dl> <dt>**\_odeur de type WINBIO \_**</dt> </dl>                                          | L’odeur d’un individu est utilisée pour déterminer l’identité d’un individu.<br/>                                                |
| <span id="WINBIO_TYPE_DNA"></span><span id="winbio_type_dna"></span><dl> <dt>**WINBIO \_ type \_ DNA**</dt> </dl>                                                | Les séquences d’acide deoxyribonucleic (DNA) sont utilisées pour déterminer l’identité d’un individu.<br/>                                    |
| <span id="WINBIO_TYPE_EAR_SHAPE"></span><span id="winbio_type_ear_shape"></span><dl> <dt>**WINBIO \_ forme de type \_ Ear \_**</dt> </dl>                             | La forme d’une languette de l’individu est utilisée pour déterminer l’identité d’un individu.<br/>                                     |
| <span id="WINBIO_TYPE_FINGER_GEOMETRY"></span><span id="winbio_type_finger_geometry"></span><dl> <dt>**WINBIO de \_ type \_ doigt \_ Geometry**</dt> </dl>           | Les formes des doigts d’un individu sont utilisées pour déterminer l’identité d’un individu.<br/>                               |
| <span id="WINBIO_TYPE_PALM_PRINT"></span><span id="winbio_type_palm_print"></span><dl> <dt>**\_tirage WINBIO type \_ Palm \_**</dt> </dl>                          | La forme de la paume est utilisée pour déterminer l’identité d’un individu.<br/>                                                     |
| <span id="WINBIO_TYPE_VEIN_PATTERN"></span><span id="winbio_type_vein_pattern"></span><dl> <dt>**\_modèle de \_ veine de type WINBIO \_**</dt> </dl>                    | Les modèles dans les veines sous l’apparence de la main d’un individu sont utilisés pour déterminer l’identité d’un individu.<br/>   |
| <span id="WINBIO_TYPE_FOOT_PRINT"></span><span id="winbio_type_foot_print"></span><dl> <dt>**\_imprimer le \_ pied de type WINBIO \_**</dt> </dl>                          | La forme du pied est utilisée pour déterminer l’identité d’un individu.<br/>                                                     |
| <span id="WINBIO_TYPE_OTHER"></span><span id="winbio_type_other"></span><dl> <dt>**\_type WINBIO \_ autre**</dt> </dl>                                          | Les données biométriques prises en charge ne sont pas définies par les constantes actuelles.<br/>                                                         |
| <span id="WINBIO_TYPE_PASSWORD"></span><span id="winbio_type_password"></span><dl> <dt>**\_ \_ mot de passe de type WINBIO**</dt> </dl>                                 | Les données de mot de passe sont utilisées pour déterminer l’identité d’un individu.<br/>                                                             |
| <span id="WINBIO_TYPE_ANY"></span><span id="winbio_type_any"></span><dl> <dt>**WINBIO \_ type \_ any**</dt> </dl>                                                | Tout type de données est utilisé pour déterminer l’identité d’un individu.<br/>                                                          |



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

 

 





