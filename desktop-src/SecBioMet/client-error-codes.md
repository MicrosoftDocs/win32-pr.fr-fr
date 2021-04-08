---
title: Codes d’erreur du client (WinBio \_ Err. h)
description: Codes d’erreur définis dans le \_ fichier d’en-tête Err. h WinBio.
ms.assetid: fc1565d2-43f1-45cd-ab84-4e557cf78107
topic_type:
- apiref
api_name:
- WINBIO_E_UNSUPPORTED_FACTOR
- WINBIO_E_INVALID_UNIT
- WINBIO_E_UNKNOWN_ID
- WINBIO_E_CANCELED
- WINBIO_E_NO_MATCH
- WINBIO_E_CAPTURE_ABORTED
- WINBIO_E_ENROLLMENT_IN_PROGRESS
- WINBIO_E_BAD_CAPTURE
- WINBIO_E_INVALID_CONTROL_CODE
- WINBIO_E_DATA_COLLECTION_IN_PROGRESS
- WINBIO_E_UNSUPPORTED_DATA_FORMAT
- WINBIO_E_UNSUPPORTED_DATA_TYPE
- WINBIO_E_UNSUPPORTED_PURPOSE
- WINBIO_E_INVALID_DEVICE_STATE
- WINBIO_E_DEVICE_BUSY
- WINBIO_E_DATABASE_CANT_CREATE
- WINBIO_E_DATABASE_CANT_OPEN
- WINBIO_E_DATABASE_CANT_CLOSE
- WINBIO_E_DATABASE_CANT_ERASE
- WINBIO_E_DATABASE_CANT_FIND
- WINBIO_E_DATABASE_ALREADY_EXISTS
- WINBIO_E_DATABASE_FULL
- WINBIO_E_DATABASE_LOCKED
- WINBIO_E_DATABASE_CORRUPTED
- WINBIO_E_DATABASE_NO_SUCH_RECORD
- WINBIO_E_DUPLICATE_ENROLLMENT
- WINBIO_E_DATABASE_READ_ERROR
- WINBIO_E_DATABASE_WRITE_ERROR
- WINBIO_E_DATABASE_NO_RESULTS
- WINBIO_E_DATABASE_NO_MORE_RECORDS
- WINBIO_E_DATABASE_EOF
- WINBIO_E_DATABASE_BAD_INDEX_VECTOR
- WINBIO_E_INCORRECT_BSP
- WINBIO_E_INCORRECT_SENSOR_POOL
- WINBIO_E_NO_CAPTURE_DATA
- WINBIO_E_INVALID_SENSOR_MODE
- WINBIO_E_LOCK_VIOLATION
- WINBIO_E_DUPLICATE_TEMPLATE
- WINBIO_E_INVALID_OPERATION
- WINBIO_E_SESSION_BUSY
- WINBIO_E_CRED_PROV_DISABLED
- WINBIO_E_CRED_PROV_NO_CREDENTIAL
- WINBIO_E_DISABLED
- WINBIO_E_CONFIGURATION_FAILURE
- WINBIO_E_SENSOR_UNAVAILABLE
- WINBIO_E_SAS_ENABLED
- WINBIO_E_DEVICE_FAILURE
- WINBIO_E_FAST_USER_SWITCH_DISABLED
- WINBIO_E_NOT_ACTIVE_CONSOLE
- WINBIO_E_EVENT_MONITOR_ACTIVE
- WINBIO_E_INVALID_PROPERTY_TYPE
- WINBIO_E_INVALID_PROPERTY_ID
- WINBIO_E_UNSUPPORTED_PROPERTY
- WINBIO_E_ADAPTER_INTEGRITY_FAILURE
- WINBIO_I_MORE_DATA
api_location:
- Winbio_err.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 000723612a2f7f9f5575fc767924d4d6c697468a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104033164"
---
# <a name="client-error-codes"></a>Codes d’erreur du client

Les codes d’erreur suivants sont définis dans le \_ fichier d’en-tête Err. h WinBio.



| Constante/valeur                                                                                                                                                                                                                                                                                         | Description                                                                                                       |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_E_UNSUPPORTED_FACTOR"></span><span id="winbio_e_unsupported_factor"></span><dl> <dt>**WINBIO \_ 0x80098001 \_ \_ facteur non pris en charge**</dt> <dt></dt> </dl>                              | Le facteur biométrique spécifié n’est pas pris en charge.<br/>                                                       |
| <span id="WINBIO_E_INVALID_UNIT"></span><span id="winbio_e_invalid_unit"></span><dl> <dt>**WINBIO \_ E 0x80098002 d' \_ \_ unité non valide**</dt> <dt></dt> </dl>                                                | Le numéro d’ID d’unité ne correspond pas à un appareil biométrique valide.<br/>                                    |
| <span id="WINBIO_E_UNKNOWN_ID"></span><span id="winbio_e_unknown_id"></span><dl> <dt>**WINBIO \_ E \_ \_ ID inconnu**</dt> <dt>0x80098003</dt> </dl>                                                      | L’exemple biométrique ne correspond à aucune identité connue.<br/>                                                |
| <span id="WINBIO_E_CANCELED"></span><span id="winbio_e_canceled"></span><dl> <dt>**WINBIO \_ E \_ annulée**</dt> <dt>0x80098004</dt> </dl>                                                             | L’opération biométrique a été annulée avant d’être terminée.<br/>                                         |
| <span id="WINBIO_E_NO_MATCH"></span><span id="winbio_e_no_match"></span><dl> <dt>**WINBIO \_ E \_ ne \_ correspond pas à**</dt> <dt>0x80098005</dt> </dl>                                                            | L’exemple biométrique ne correspond pas à l’identité ou au sous-facteur spécifié.<br/>                              |
| <span id="WINBIO_E_CAPTURE_ABORTED"></span><span id="winbio_e_capture_aborted"></span><dl> <dt>**WINBIO \_ 0x80098006 \_ \_ abandonnée par la capture E**</dt> <dt></dt> </dl>                                       | Impossible de capturer un échantillon biométrique, car l’opération de capture a été abandonnée.<br/>                    |
| <span id="WINBIO_E_ENROLLMENT_IN_PROGRESS"></span><span id="winbio_e_enrollment_in_progress"></span><dl> <dt>**WINBIO \_ \_Inscription E \_ en \_ cours**</dt> <dt>0x80098007</dt> </dl>                 | Une transaction d’inscription n’a pas pu être démarrée, car une autre inscription est déjà en cours.<br/>      |
| <span id="WINBIO_E_BAD_CAPTURE"></span><span id="winbio_e_bad_capture"></span><dl> <dt>**WINBIO \_ E 0x80098008 de \_ \_ capture incorrecte**</dt> <dt></dt> </dl>                                                   | L’exemple capturé ne peut pas être utilisé pour d’autres opérations biométriques.<br/>                                   |
| <span id="WINBIO_E_INVALID_CONTROL_CODE"></span><span id="winbio_e_invalid_control_code"></span><dl> <dt>**WINBIO \_ E \_ \_ \_ Code de contrôle non valide**</dt> <dt>0x80098009</dt> </dl>                       | L’unité biométrique ne prend pas en charge le code de contrôle d’unité spécifié.<br/>                                   |
| <span id="WINBIO_E_DATA_COLLECTION_IN_PROGRESS"></span><span id="winbio_e_data_collection_in_progress"></span><dl> <dt>**WINBIO \_ 0x8009800B \_ \_ de la collecte \_ des données en \_ cours**</dt> <dt></dt> </dl> | Une opération de collecte de données en attente est déjà en cours.<br/>                                            |
| <span id="WINBIO_E_UNSUPPORTED_DATA_FORMAT"></span><span id="winbio_e_unsupported_data_format"></span><dl> <dt>**WINBIO \_ E \_ \_ \_ format de données non pris en charge**</dt> <dt>0x8009800C</dt> </dl>              | Le pilote de capteur biométrique ne prend pas en charge le format de données demandé.<br/>                                |
| <span id="WINBIO_E_UNSUPPORTED_DATA_TYPE"></span><span id="winbio_e_unsupported_data_type"></span><dl> <dt>**WINBIO \_ E \_ \_ \_ type de données non pris en charge**</dt> <dt>0x8009800D</dt> </dl>                    | Le pilote de capteur biométrique ne prend pas en charge le type de données demandé.<br/>                                  |
| <span id="WINBIO_E_UNSUPPORTED_PURPOSE"></span><span id="winbio_e_unsupported_purpose"></span><dl> <dt>**WINBIO \_ E \_ 0x8009800E \_ objet non pris en charge**</dt> <dt></dt> </dl>                           | Le pilote de capteur biométrique ne prend pas en charge l’objectif de données demandé.<br/>                               |
| <span id="WINBIO_E_INVALID_DEVICE_STATE"></span><span id="winbio_e_invalid_device_state"></span><dl> <dt>**WINBIO \_ E \_ 0x8009800F \_ \_ État de l’appareil non valide**</dt> <dt></dt> </dl>                       | L’unité biométrique n’est pas dans l’état approprié pour effectuer l’opération spécifiée.<br/>                      |
| <span id="WINBIO_E_DEVICE_BUSY"></span><span id="winbio_e_device_busy"></span><dl> <dt>**WINBIO \_ 0x80098010 de l' \_ appareil \_ occupé**</dt> <dt></dt> </dl>                                                   | L’opération n’a pas pu être effectuée car le périphérique capteur était occupé.<br/>                               |
| <span id="WINBIO_E_DATABASE_CANT_CREATE"></span><span id="winbio_e_database_cant_create"></span><dl> <dt>**WINBIO \_ E \_ base de données E \_ Impossible de \_ créer**</dt> <dt>0x80098011</dt> </dl>                       | La carte de stockage n’a pas pu créer une nouvelle base de données.<br/>                                             |
| <span id="WINBIO_E_DATABASE_CANT_OPEN"></span><span id="winbio_e_database_cant_open"></span><dl> <dt>**WINBIO \_ E \_ base de données E \_ Impossible d' \_ ouvrir**</dt> <dt>0x80098012</dt> </dl>                             | L’adaptateur de stockage n’a pas pu ouvrir une base de données existante.<br/>                                         |
| <span id="WINBIO_E_DATABASE_CANT_CLOSE"></span><span id="winbio_e_database_cant_close"></span><dl> <dt>**WINBIO \_ E \_ base de données E \_ Impossible de \_ Fermer**</dt> <dt>0x80098013</dt> </dl>                          | La carte de stockage n’a pas pu fermer une base de données.<br/>                                                  |
| <span id="WINBIO_E_DATABASE_CANT_ERASE"></span><span id="winbio_e_database_cant_erase"></span><dl> <dt>**WINBIO \_ E \_ base de données E \_ Impossible d' \_ Effacer**</dt> <dt>0x80098014</dt> </dl>                          | L’adaptateur de stockage n’a pas pu effacer une base de données.<br/>                                                  |
| <span id="WINBIO_E_DATABASE_CANT_FIND"></span><span id="winbio_e_database_cant_find"></span><dl> <dt>**WINBIO \_ E \_ \_ Impossible de \_ trouver la base de données**</dt> <dt>0x80098015</dt> </dl>                             | La carte de stockage n’a pas pu trouver de base de données.<br/>                                                   |
| <span id="WINBIO_E_DATABASE_ALREADY_EXISTS"></span><span id="winbio_e_database_already_exists"></span><dl> <dt>**WINBIO \_ La \_ base de données E \_ \_ existe déjà**</dt> <dt>0x80098016</dt> </dl>              | L’adaptateur de stockage n’a pas pu créer une base de données, car la base de données spécifiée existe déjà.<br/>   |
| <span id="WINBIO_E_DATABASE_FULL"></span><span id="winbio_e_database_full"></span><dl> <dt>**WINBIO \_ E. 0x80098018 \_ \_ complète de la base de données**</dt> <dt></dt> </dl>                                             | La carte de stockage n’a pas pu ajouter un enregistrement à la base de données, car celle-ci est pleine.<br/>         |
| <span id="WINBIO_E_DATABASE_LOCKED"></span><span id="winbio_e_database_locked"></span><dl> <dt>**WINBIO \_ E \_ base de données \_ verrouillée**</dt> <dt>0x80098019</dt> </dl>                                       | La base de données est verrouillée et son contenu n’est pas accessible.<br/>                                              |
| <span id="WINBIO_E_DATABASE_CORRUPTED"></span><span id="winbio_e_database_corrupted"></span><dl> <dt>**WINBIO \_ \_Base de données E \_ endommagée**</dt> <dt>0x8009801A</dt> </dl>                              | Le contenu de la base de données est endommagé et n’est pas accessible.<br/>                               |
| <span id="WINBIO_E_DATABASE_NO_SUCH_RECORD"></span><span id="winbio_e_database_no_such_record"></span><dl> <dt>**WINBIO \_ E \_ base de données \_ sans \_ \_ enregistrement de ce type**</dt> <dt>0x8009801B</dt> </dl>             | Aucun enregistrement n’a été supprimé, car l’identité et le sous-facteur spécifiés ne sont pas présents dans la base de données.<br/> |
| <span id="WINBIO_E_DUPLICATE_ENROLLMENT"></span><span id="winbio_e_duplicate_enrollment"></span><dl> <dt>**WINBIO \_ E \_ en \_ double**</dt> <dt>0x8009801C</dt> d’inscription </dl>                        | L’identité et le sous-facteur spécifiés sont déjà inscrits dans la base de données.<br/>                            |
| <span id="WINBIO_E_DATABASE_READ_ERROR"></span><span id="winbio_e_database_read_error"></span><dl> <dt>**WINBIO \_ E \_ . \_ \_ erreur de lecture de la base de données**</dt> <dt>0x8009801D</dt> </dl>                          | Une erreur s’est produite lors de la tentative de lecture de la base de données.<br/>                                              |
| <span id="WINBIO_E_DATABASE_WRITE_ERROR"></span><span id="winbio_e_database_write_error"></span><dl> <dt>**WINBIO \_ \_Erreur d' \_ écriture \_ de la base de données E**</dt> <dt>0x8009801E</dt> </dl>                       | Une erreur s'est produite lors de la tentative d'écriture dans la base de données.<br/>                                               |
| <span id="WINBIO_E_DATABASE_NO_RESULTS"></span><span id="winbio_e_database_no_results"></span><dl> <dt>**WINBIO \_ E \_ base de données \_ sans \_ résultats**</dt> <dt>0x8009801F</dt> </dl>                          | Aucun enregistrement de la base de données ne correspond à la requête.<br/>                                                          |
| <span id="WINBIO_E_DATABASE_NO_MORE_RECORDS"></span><span id="winbio_e_database_no_more_records"></span><dl> <dt>**WINBIO \_ E \_ base de données \_ sans \_ plus d' \_ enregistrements**</dt> <dt>0x80098020</dt> </dl>          | Tous les enregistrements de la requête de base de données la plus récente ont été récupérés.<br/>                                   |
| <span id="WINBIO_E_DATABASE_EOF"></span><span id="winbio_e_database_eof"></span><dl> <dt>**WINBIO \_ E \_ . \_ EOF base de données**</dt> <dt>0x80098021</dt> </dl>                                                | Une opération de base de données a été effectuée de manière inattendue à la fin du fichier.<br/>                                     |
| <span id="WINBIO_E_DATABASE_BAD_INDEX_VECTOR"></span><span id="winbio_e_database_bad_index_vector"></span><dl> <dt>**WINBIO \_ E \_ base de données 0x80098022 \_ \_ \_ vecteur d’index incorrect**</dt> <dt></dt> </dl>       | Une opération de base de données a échoué en raison d’un vecteur d’index incorrect.<br/>                                           |
| <span id="WINBIO_E_INCORRECT_BSP"></span><span id="winbio_e_incorrect_bsp"></span><dl> <dt>**WINBIO \_ E \_ 0x80098024 \_ BSP incorrect**</dt> <dt></dt> </dl>                                             | L’unité biométrique n’appartient pas au fournisseur de services spécifié.<br/>                                  |
| <span id="WINBIO_E_INCORRECT_SENSOR_POOL"></span><span id="winbio_e_incorrect_sensor_pool"></span><dl> <dt>**WINBIO \_ E \_ \_ \_ pool de capteurs incorrect**</dt> <dt>0x80098025</dt> </dl>                    | L’unité biométrique n’appartient pas au pool de capteurs spécifié.<br/>                                       |
| <span id="WINBIO_E_NO_CAPTURE_DATA"></span><span id="winbio_e_no_capture_data"></span><dl> <dt>**WINBIO \_ E \_ aucun \_ \_**</dt> <dt>0x80098026</dt> de données de capture </dl>                                      | La mémoire tampon de capture de l’adaptateur du capteur est vide.<br/>                                                            |
| <span id="WINBIO_E_INVALID_SENSOR_MODE"></span><span id="winbio_e_invalid_sensor_mode"></span><dl> <dt>**WINBIO \_ E \_ \_ \_ mode de capteur non valide**</dt> <dt>0x80098027</dt> </dl>                          | L’adaptateur de capteur ne prend pas en charge le mode de capteur spécifié dans la configuration.<br/>                    |
| <span id="WINBIO_E_LOCK_VIOLATION"></span><span id="winbio_e_lock_violation"></span><dl> <dt>**WINBIO \_ \_ \_ Violation de verrouillage E**</dt> <dt>0x8009802A</dt> </dl>                                          | Impossible d’effectuer l’opération demandée en raison d’un conflit de verrouillage.<br/>                                 |
| <span id="WINBIO_E_DUPLICATE_TEMPLATE"></span><span id="winbio_e_duplicate_template"></span><dl> <dt>**WINBIO \_ E \_ dupliquer le \_ modèle**</dt> <dt>0x8009802B</dt> </dl>                              | Les données d’un modèle biométrique correspondent à celles d’un autre modèle déjà présent dans la base de données.<br/>             |
| <span id="WINBIO_E_INVALID_OPERATION"></span><span id="winbio_e_invalid_operation"></span><dl> <dt>**WINBIO \_ E 0x8009802C d' \_ \_ opération non valide**</dt> <dt></dt> </dl>                                 | L’opération demandée n’est pas valide pour l’état actuel de la session ou de l’unité biométrique.<br/>       |
| <span id="WINBIO_E_SESSION_BUSY"></span><span id="winbio_e_session_busy"></span><dl> <dt>**WINBIO \_ E \_ session \_ occupée**</dt> <dt>0x8009802D</dt> </dl>                                                | La session ne peut pas commencer une nouvelle opération, car une autre opération est déjà en cours.<br/>             |
| <span id="WINBIO_E_CRED_PROV_DISABLED"></span><span id="winbio_e_cred_prov_disabled"></span><dl> <dt>**WINBIO \_ E \_ cred \_ Prov \_ désactivé**</dt> <dt>0x80098030</dt> </dl>                             | Les paramètres de stratégie système ont désactivé le fournisseur d’informations d’identification biométrique.<br/>                                |
| <span id="WINBIO_E_CRED_PROV_NO_CREDENTIAL"></span><span id="winbio_e_cred_prov_no_credential"></span><dl> <dt>**WINBIO \_ E \_ cred \_ prouver \_ aucune \_ information d’identification**</dt> <dt>0x80098031</dt> </dl>             | Les informations d’identification demandées sont introuvables.<br/>                                                                |
| <span id="WINBIO_E_DISABLED"></span><span id="winbio_e_disabled"></span><dl> <dt>**WINBIO \_ E \_ désactivé**</dt> <dt>0x80098032</dt> </dl>                                                             | Les paramètres de stratégie système ont désactivé le service biométrique.<br/>                                            |
| <span id="WINBIO_E_CONFIGURATION_FAILURE"></span><span id="winbio_e_configuration_failure"></span><dl> <dt>**WINBIO \_ \_ \_ Échec**</dt> de la configuration d’E <dt>0x80098033</dt> </dl>                     | L’unité biométrique n’a pas pu être configurée.<br/>                                                            |
| <span id="WINBIO_E_SENSOR_UNAVAILABLE"></span><span id="winbio_e_sensor_unavailable"></span><dl> <dt>**WINBIO \_ \_Capteur E \_ non disponible**</dt> <dt>0x80098034</dt> </dl>                              | Impossible de créer un pool privé, car une ou plusieurs unités biométriques ne sont pas disponibles.<br/>                |
| <span id="WINBIO_E_SAS_ENABLED"></span><span id="winbio_e_sas_enabled"></span><dl> <dt>**WINBIO \_ 0x80098035 \_ \_ activée pour SAS**</dt> <dt></dt> </dl>                                                   | Une séquence de vigilance sécurisée (CTRL-ALT-SUPPR) est nécessaire pour l’ouverture de session.<br/>                                   |
| <span id="WINBIO_E_DEVICE_FAILURE"></span><span id="winbio_e_device_failure"></span><dl> <dt>**WINBIO \_ 0x80098036 \_ d' \_ échec**</dt> de l’appareil <dt></dt> </dl>                                          | Un capteur biométrique a échoué.<br/>                                                                         |
| <span id="WINBIO_E_FAST_USER_SWITCH_DISABLED"></span><span id="winbio_e_fast_user_switch_disabled"></span><dl> <dt>**WINBIO \_ E \_ \_ commutateur d’utilisateur rapide \_ \_ désactivé**</dt> <dt>0x80098037</dt> </dl>       | >le changement rapide d’utilisateur est désactivé.<br/>                                                                   |
| <span id="WINBIO_E_NOT_ACTIVE_CONSOLE"></span><span id="winbio_e_not_active_console"></span><dl> <dt>**WINBIO \_ E \_ non \_ active \_**</dt> <dt>0x80098038</dt> de la console </dl>                             | Impossible d’ouvrir le pool de capteurs système à partir de sessions clientes Terminal Server.<br/>                          |
| <span id="WINBIO_E_EVENT_MONITOR_ACTIVE"></span><span id="winbio_e_event_monitor_active"></span><dl> <dt>**WINBIO \_ 0x80098039 \_ \_ \_ actif du moniteur d’événements E**</dt> <dt></dt> </dl>                      | Un moniteur d’événements actif est déjà associé à la session spécifiée.<br/>                        |
| <span id="WINBIO_E_INVALID_PROPERTY_TYPE"></span><span id="winbio_e_invalid_property_type"></span><dl> <dt>**WINBIO \_ 0x8009803A \_ de \_ \_ type de propriété non valide**</dt> <dt></dt> </dl>                    | La valeur spécifiée n’est pas un type de propriété valide.<br/>                                                      |
| <span id="WINBIO_E_INVALID_PROPERTY_ID"></span><span id="winbio_e_invalid_property_id"></span><dl> <dt>**WINBIO \_ E \_ \_ \_ ID de propriété non valide**</dt> <dt>0x8009803B</dt> </dl>                          | La valeur spécifiée n’est pas un ID de propriété valide.<br/>                                                        |
| <span id="WINBIO_E_UNSUPPORTED_PROPERTY"></span><span id="winbio_e_unsupported_property"></span><dl> <dt>**WINBIO \_ 0x8009803C \_ \_ propriété non prise en charge**</dt> <dt></dt> </dl>                        | L’unité biométrique ne prend pas en charge la propriété spécifiée.<br/>                                            |
| <span id="WINBIO_E_ADAPTER_INTEGRITY_FAILURE"></span><span id="winbio_e_adapter_integrity_failure"></span><dl> <dt>**WINBIO \_ \_Échec de \_ l' \_ intégrité de l’adaptateur E**</dt> <dt>0x8009803D</dt> </dl>        | L’adaptateur n’a pas réussi à vérifier son intégrité.<br/>                                                          |
| <span id="WINBIO_I_MORE_DATA"></span><span id="winbio_i_more_data"></span><dl> <dt>**WINBIO \_ \_ \_ Autres**</dt> <dt>0x00090001</dt> de données </dl>                                                         | Un autre exemple est nécessaire pour le modèle d’inscription en cours.<br/>                                          |



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 7 uniquement\]<br/>                                               |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 R2 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>WinBio \_ Err. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Constantes d’application cliente](client-application-constants.md)
</dt> </dl>

 

 





