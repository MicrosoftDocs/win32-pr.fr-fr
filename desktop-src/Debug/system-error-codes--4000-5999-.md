---
description: Décrit les codes d’erreur 4000-5999 définis dans le fichier d’en-tête WinError. h et est destiné aux développeurs.
ms.assetid: 1d2f7160-6322-4c75-abbc-4a882bbdf7ce
title: Codes d’erreur système (4000-5999) (WinError. h)
ms.topic: reference
ms.date: 07/18/2019
ms.openlocfilehash: bfd39042489f2a92ff2eb13df92a22e392c5405e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110775"
---
# <a name="system-error-codes-4000-5999"></a>Codes d’erreur système (4000-5999)

> [!NOTE]
> Ces informations sont destinées aux développeurs qui déboguent les erreurs système. Pour les autres erreurs, telles que les problèmes de Windows Update, il existe une liste de ressources dans la page [codes d’erreur](system-error-codes.md) .

La liste suivante décrit les [codes d’erreur système](system-error-codes.md) pour les erreurs 4000 à 5999. Elles sont retournées par la fonction [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) lorsque de nombreuses fonctions échouent. Pour récupérer le texte de description de l’erreur dans votre application, utilisez la fonction [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) avec le **format \_ message \_ de \_** l’indicateur système.

<dl> <dt>

<span id="ERROR_WINS_INTERNAL"></span><span id="error_wins_internal"></span>**ERREUR de \_ WINS \_ interne**
</dt> <dd> <dl> <dt>

4000 (0xFA0)
</dt> <dt>



WINS a rencontré une erreur lors du traitement de la commande.


</dt> </dl> </dd> <dt>

<span id="ERROR_CAN_NOT_DEL_LOCAL_WINS"></span><span id="error_can_not_del_local_wins"></span>**ERREUR \_ \_ Impossible de \_ del \_ \_ WINS local**
</dt> <dd> <dl> <dt>

4001 (0xFA1)
</dt> <dt>



Le WINS local ne peut pas être supprimé.


</dt> </dl> </dd> <dt>

<span id="ERROR_STATIC_INIT"></span><span id="error_static_init"></span>**\_init statique d’erreur \_**
</dt> <dd> <dl> <dt>

4002 (0xFA2)
</dt> <dt>



L’importation à partir du fichier a échoué.


</dt> </dl> </dd> <dt>

<span id="ERROR_INC_BACKUP"></span><span id="error_inc_backup"></span>**sauvegarde d’erreur \_ Inc. \_**
</dt> <dd> <dl> <dt>

4003 (0xFA3)
</dt> <dt>



La sauvegarde a échoué. Une sauvegarde complète a-t-elle été effectuée avant ?


</dt> </dl> </dd> <dt>

<span id="ERROR_FULL_BACKUP"></span><span id="error_full_backup"></span>**\_sauvegarde complète de l’erreur \_**
</dt> <dd> <dl> <dt>

4004 (0xFA4)
</dt> <dt>



La sauvegarde a échoué. Vérifiez le répertoire dans lequel vous sauvegardez la base de données.


</dt> </dl> </dd> <dt>

<span id="ERROR_REC_NON_EXISTENT"></span><span id="error_rec_non_existent"></span>**enregistrement d’erreur \_ \_ non \_ existant**
</dt> <dd> <dl> <dt>

4005 (0xFA5)
</dt> <dt>



Le nom n’existe pas dans la base de données WINS.


</dt> </dl> </dd> <dt>

<span id="ERROR_RPL_NOT_ALLOWED"></span><span id="error_rpl_not_allowed"></span>**ERREUR \_ RPL \_ non \_ autorisée**
</dt> <dd> <dl> <dt>

4006 (0xFA6)
</dt> <dt>



La réplication avec un partenaire non configuré n’est pas autorisée.


</dt> </dl> </dd> <dt>

<span id="PEERDIST_ERROR_CONTENTINFO_VERSION_UNSUPPORTED"></span><span id="peerdist_error_contentinfo_version_unsupported"></span>**erreur PEERDIST- \_ \_ version de CONTENTINFO \_ \_ non prise en charge**
</dt> <dd> <dl> <dt>

4050 (0xFD2)
</dt> <dt>



La version des informations de contenu fournies n’est pas prise en charge.


</dt> </dl> </dd> <dt>

<span id="PEERDIST_ERROR_CANNOT_PARSE_CONTENTINFO"></span><span id="peerdist_error_cannot_parse_contentinfo"></span>**\_erreur PEERDIST \_ Impossible d' \_ analyser \_ CONTENTINFO**
</dt> <dd> <dl> <dt>

4051 (0xFD3)
</dt> <dt>



Les informations de contenu fournies sont incorrectes.


</dt> </dl> </dd> <dt>

<span id="PEERDIST_ERROR_MISSING_DATA"></span><span id="peerdist_error_missing_data"></span>**\_erreur PEERDIST \_ données manquantes \_**
</dt> <dd> <dl> <dt>

4052 (0xFD4)
</dt> <dt>



Les données demandées sont introuvables dans les caches locaux ou d’homologue.


</dt> </dl> </dd> <dt>

<span id="PEERDIST_ERROR_NO_MORE"></span><span id="peerdist_error_no_more"></span>**\_erreur PEERDIST \_ - \_ plus**
</dt> <dd> <dl> <dt>

4053 (0xFD5)
</dt> <dt>



Aucune donnée supplémentaire n’est disponible ou requise.


</dt> </dl> </dd> <dt>

<span id="PEERDIST_ERROR_NOT_INITIALIZED"></span><span id="peerdist_error_not_initialized"></span>**\_erreur PEERDIST \_ non \_ initialisée**
</dt> <dd> <dl> <dt>

4054 (0xFD6)
</dt> <dt>



L’objet fourni n’a pas été initialisé.


</dt> </dl> </dd> <dt>

<span id="PEERDIST_ERROR_ALREADY_INITIALIZED"></span><span id="peerdist_error_already_initialized"></span>**\_erreur PEERDIST \_ déjà \_ initialisée**
</dt> <dd> <dl> <dt>

4055 (0xFD7)
</dt> <dt>



L’objet fourni a déjà été initialisé.


</dt> </dl> </dd> <dt>

<span id="PEERDIST_ERROR_SHUTDOWN_IN_PROGRESS"></span><span id="peerdist_error_shutdown_in_progress"></span>**\_ \_ arrêt \_ de l’erreur PEERDIST en \_ cours**
</dt> <dd> <dl> <dt>

4056 (0xFD8)
</dt> <dt>



Une opération d’arrêt est déjà en cours.


</dt> </dl> </dd> <dt>

<span id="PEERDIST_ERROR_INVALIDATED"></span><span id="peerdist_error_invalidated"></span>**\_erreur PEERDIST \_ invalidée**
</dt> <dd> <dl> <dt>

4057 (0xFD9)
</dt> <dt>



L’objet fourni a déjà été invalidé.


</dt> </dl> </dd> <dt>

<span id="PEERDIST_ERROR_ALREADY_EXISTS"></span><span id="peerdist_error_already_exists"></span>**l' \_ erreur \_ PEERDIST \_ existe déjà**
</dt> <dd> <dl> <dt>

4058 (0xFDA)
</dt> <dt>



Un élément existe déjà et n’a pas été remplacé.


</dt> </dl> </dd> <dt>

<span id="PEERDIST_ERROR_OPERATION_NOTFOUND"></span><span id="peerdist_error_operation_notfound"></span>**\_opération d’erreur PEERDIST \_ \_ NotFound**
</dt> <dd> <dl> <dt>

4059 (0xFDB)
</dt> <dt>



Impossible d’annuler l’opération demandée, car elle est déjà terminée.


</dt> </dl> </dd> <dt>

<span id="PEERDIST_ERROR_ALREADY_COMPLETED"></span><span id="peerdist_error_already_completed"></span>**\_erreur PEERDIST \_ déjà \_ terminée**
</dt> <dd> <dl> <dt>

4060 (0xFDC)
</dt> <dt>



Impossible d’effectuer l’opération variante requise, car elle a déjà été exécutée.


</dt> </dl> </dd> <dt>

<span id="PEERDIST_ERROR_OUT_OF_BOUNDS"></span><span id="peerdist_error_out_of_bounds"></span>**\_erreur PEERDIST \_ hors \_ \_ limites**
</dt> <dd> <dl> <dt>

4061 (0xFDD)
</dt> <dt>



Une opération a accédé à des données au-delà des limites des données valides.


</dt> </dl> </dd> <dt>

<span id="PEERDIST_ERROR_VERSION_UNSUPPORTED"></span><span id="peerdist_error_version_unsupported"></span>**\_version d’erreur PEERDIST \_ \_ non prise en charge**
</dt> <dd> <dl> <dt>

4062 (0xFDE)
</dt> <dt>



La version demandée n’est pas prise en charge.


</dt> </dl> </dd> <dt>

<span id="PEERDIST_ERROR_INVALID_CONFIGURATION"></span><span id="peerdist_error_invalid_configuration"></span>**\_erreur PEERDIST \_ configuration non valide \_**
</dt> <dd> <dl> <dt>

4063 (0xFDF)
</dt> <dt>



Une valeur de configuration n’est pas valide.


</dt> </dl> </dd> <dt>

<span id="PEERDIST_ERROR_NOT_LICENSED"></span><span id="peerdist_error_not_licensed"></span>**\_erreur PEERDIST \_ non \_ concédée sous licence**
</dt> <dd> <dl> <dt>

4064 (0xFE0)
</dt> <dt>



La référence SKU n’est pas sous licence.


</dt> </dl> </dd> <dt>

<span id="PEERDIST_ERROR_SERVICE_UNAVAILABLE"></span><span id="peerdist_error_service_unavailable"></span>**\_service d’erreur PEERDIST \_ \_ non disponible**
</dt> <dd> <dl> <dt>

4065 (0xFE1)
</dt> <dt>



Le service PeerDist est toujours en cours d’initialisation et sera bientôt disponible.


</dt> </dl> </dd> <dt>

<span id="PEERDIST_ERROR_TRUST_FAILURE"></span><span id="peerdist_error_trust_failure"></span>**échec de l' \_ approbation des erreurs PEERDIST \_ \_**
</dt> <dd> <dl> <dt>

4066 (0xFE2)
</dt> <dt>



La communication avec un ou plusieurs ordinateurs sera temporairement bloquée en raison d’erreurs récentes.


</dt> </dl> </dd> <dt>

<span id="ERROR_DHCP_ADDRESS_CONFLICT"></span><span id="error_dhcp_address_conflict"></span>**ERREUR \_ de \_ conflit d’adresses DHCP \_**
</dt> <dd> <dl> <dt>

4100 (0x1004)
</dt> <dt>



Le client DHCP a obtenu une adresse IP qui est déjà en cours d’utilisation sur le réseau. L’interface locale sera désactivée jusqu’à ce que le client DHCP puisse obtenir une nouvelle adresse.


</dt> </dl> </dd> <dt>

<span id="ERROR_WMI_GUID_NOT_FOUND"></span><span id="error_wmi_guid_not_found"></span>**ERREUR \_ \_ GUID WMI \_ \_ introuvable**
</dt> <dd> <dl> <dt>

4200 (0x1068)
</dt> <dt>



Le GUID passé n’a pas été reconnu comme valide par un fournisseur de données WMI.


</dt> </dl> </dd> <dt>

<span id="ERROR_WMI_INSTANCE_NOT_FOUND"></span><span id="error_wmi_instance_not_found"></span>**ERREUR \_ l' \_ instance WMI est \_ \_ introuvable**
</dt> <dd> <dl> <dt>

4201 (0x1069)
</dt> <dt>



Le nom d’instance passé n’a pas été reconnu comme valide par un fournisseur de données WMI.


</dt> </dl> </dd> <dt>

<span id="ERROR_WMI_ITEMID_NOT_FOUND"></span><span id="error_wmi_itemid_not_found"></span>**ERREUR \_ WMI \_ ID d’ID de service \_ \_ introuvable**
</dt> <dd> <dl> <dt>

4202 (0x106A)
</dt> <dt>



L’ID d’élément de données passé n’a pas été reconnu comme valide par un fournisseur de données WMI.


</dt> </dl> </dd> <dt>

<span id="ERROR_WMI_TRY_AGAIN"></span><span id="error_wmi_try_again"></span>**ERREUR \_ WMI de \_ Réessayer \_**
</dt> <dd> <dl> <dt>

4203 (0x106B)
</dt> <dt>



La requête WMI n’a pas pu être terminée et doit être retentée.


</dt> </dl> </dd> <dt>

<span id="ERROR_WMI_DP_NOT_FOUND"></span><span id="error_wmi_dp_not_found"></span>**ERREUR \_ WMI \_ DP \_ \_ introuvable**
</dt> <dd> <dl> <dt>

4204 (0x106C)
</dt> <dt>



Le fournisseur de données WMI est introuvable.


</dt> </dl> </dd> <dt>

<span id="ERROR_WMI_UNRESOLVED_INSTANCE_REF"></span><span id="error_wmi_unresolved_instance_ref"></span>**ERREUR \_ WMI \_ de \_ référence d’instance non résolue \_**
</dt> <dd> <dl> <dt>

4205 (0x106D)
</dt> <dt>



Le fournisseur de données WMI fait référence à un jeu d’instances qui n’a pas été inscrit.


</dt> </dl> </dd> <dt>

<span id="ERROR_WMI_ALREADY_ENABLED"></span><span id="error_wmi_already_enabled"></span>**ERREUR \_ WMI \_ déjà \_ activée**
</dt> <dd> <dl> <dt>

4206 (0x106E)
</dt> <dt>



Le bloc de données WMI ou la notification d’événement a déjà été activé.


</dt> </dl> </dd> <dt>

<span id="ERROR_WMI_GUID_DISCONNECTED"></span><span id="error_wmi_guid_disconnected"></span>**ERREUR \_ \_ GUID WMI \_ déconnectée**
</dt> <dd> <dl> <dt>

4207 (0x106F)
</dt> <dt>



Le bloc de données WMI n’est plus disponible.


</dt> </dl> </dd> <dt>

<span id="ERROR_WMI_SERVER_UNAVAILABLE"></span><span id="error_wmi_server_unavailable"></span>**ERREUR \_ \_ serveur WMI \_ non disponible**
</dt> <dd> <dl> <dt>

4208 (0x1070)
</dt> <dt>



Le service de données WMI n’est pas disponible.


</dt> </dl> </dd> <dt>

<span id="ERROR_WMI_DP_FAILED"></span><span id="error_wmi_dp_failed"></span>**ERREUR \_ WMI \_ DP \_ échec**
</dt> <dd> <dl> <dt>

4209 (0x1071)
</dt> <dt>



Le fournisseur de données WMI n’a pas pu effectuer la requête.


</dt> </dl> </dd> <dt>

<span id="ERROR_WMI_INVALID_MOF"></span><span id="error_wmi_invalid_mof"></span>**ERREUR \_ \_ MOF non valide dans WMI \_**
</dt> <dd> <dl> <dt>

4210 (0x1072)
</dt> <dt>



Les informations MOF WMI ne sont pas valides.


</dt> </dl> </dd> <dt>

<span id="ERROR_WMI_INVALID_REGINFO"></span><span id="error_wmi_invalid_reginfo"></span>**ERREUR \_ WMI \_ non valide \_ REGINFO**
</dt> <dd> <dl> <dt>

4211 (0x1073)
</dt> <dt>



Les informations d’inscription WMI ne sont pas valides.


</dt> </dl> </dd> <dt>

<span id="ERROR_WMI_ALREADY_DISABLED"></span><span id="error_wmi_already_disabled"></span>**ERREUR \_ WMI \_ déjà \_ désactivée**
</dt> <dd> <dl> <dt>

4212 (0x1074)
</dt> <dt>



Le bloc de données WMI ou la notification d’événement a déjà été désactivé.


</dt> </dl> </dd> <dt>

<span id="ERROR_WMI_READ_ONLY"></span><span id="error_wmi_read_only"></span>**ERREUR \_ WMI \_ en lecture \_ seule**
</dt> <dd> <dl> <dt>

4213 (0x1075)
</dt> <dt>



L’élément de données ou le bloc de données WMI est en lecture seule.


</dt> </dl> </dd> <dt>

<span id="ERROR_WMI_SET_FAILURE"></span><span id="error_wmi_set_failure"></span>**ERREUR \_ échec de la \_ définition WMI \_**
</dt> <dd> <dl> <dt>

4214 (0x1076)
</dt> <dt>



Impossible de modifier l’élément de données ou le bloc de données WMI.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_APPCONTAINER"></span><span id="error_not_appcontainer"></span>**ERREUR \_ non \_ APPCONTAINER**
</dt> <dd> <dl> <dt>

4250 (0x109A)
</dt> <dt>



Cette opération n’est valide que dans le contexte d’un conteneur d’application.


</dt> </dl> </dd> <dt>

<span id="ERROR_APPCONTAINER_REQUIRED"></span><span id="error_appcontainer_required"></span>**ERREUR \_ APPCONTAINER \_ obligatoire**
</dt> <dd> <dl> <dt>

4251 (0x109B)
</dt> <dt>



Cette application ne peut s’exécuter que dans le contexte d’un conteneur d’application.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_SUPPORTED_IN_APPCONTAINER"></span><span id="error_not_supported_in_appcontainer"></span>**ERREUR \_ non \_ prise en charge \_ dans \_ APPCONTAINER**
</dt> <dd> <dl> <dt>

4252 (0x109C)
</dt> <dt>



Cette fonctionnalité n’est pas prise en charge dans le contexte d’un conteneur d’application.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_PACKAGE_SID_LENGTH"></span><span id="error_invalid_package_sid_length"></span>**ERREUR \_ de \_ \_ longueur du SID du package non valide \_**
</dt> <dd> <dl> <dt>

4253 (0x109D)
</dt> <dt>



La longueur du SID fourni n’est pas une longueur valide pour les SID de conteneur d’application.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_MEDIA"></span><span id="error_invalid_media"></span>**ERREUR \_ de \_ support non valide**
</dt> <dd> <dl> <dt>

4300 (0x10CC)
</dt> <dt>



L’identificateur de média ne représente pas un support valide.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_LIBRARY"></span><span id="error_invalid_library"></span>**ERREUR \_ de \_ bibliothèque non valide**
</dt> <dd> <dl> <dt>

4301 (0x10CD)
</dt> <dt>



L’identificateur de bibliothèque ne représente pas une bibliothèque valide.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_MEDIA_POOL"></span><span id="error_invalid_media_pool"></span>**ERREUR \_ de \_ pool de supports non valide \_**
</dt> <dd> <dl> <dt>

4302 (0x10CE)
</dt> <dt>



L’identificateur du pool de médias ne représente pas un pool de médias valide.


</dt> </dl> </dd> <dt>

<span id="ERROR_DRIVE_MEDIA_MISMATCH"></span><span id="error_drive_media_mismatch"></span>**incompatibilité de support de lecteur d’erreur \_ \_ \_**
</dt> <dd> <dl> <dt>

4303 (0x10CF)
</dt> <dt>



Le lecteur et le support ne sont pas compatibles ou n’existent pas dans différentes bibliothèques.


</dt> </dl> </dd> <dt>

<span id="ERROR_MEDIA_OFFLINE"></span><span id="error_media_offline"></span>**support d’erreur \_ \_ hors connexion**
</dt> <dd> <dl> <dt>

4304 (0x10D0)
</dt> <dt>



Le support existe actuellement dans une bibliothèque hors connexion et doit être en ligne pour effectuer cette opération.


</dt> </dl> </dd> <dt>

<span id="ERROR_LIBRARY_OFFLINE"></span><span id="error_library_offline"></span>**bibliothèque d’erreurs \_ \_ hors connexion**
</dt> <dd> <dl> <dt>

4305 (0x10D1)
</dt> <dt>



L’opération ne peut pas être effectuée sur une bibliothèque hors connexion.


</dt> </dl> </dd> <dt>

<span id="ERROR_EMPTY"></span><span id="error_empty"></span>**ERREUR \_ vide**
</dt> <dd> <dl> <dt>

4306 (0x10D2)
</dt> <dt>



La bibliothèque, le lecteur ou le pool de supports est vide.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_EMPTY"></span><span id="error_not_empty"></span>**ERREUR \_ non \_ vide**
</dt> <dd> <dl> <dt>

4307 (0x10D3)
</dt> <dt>



La bibliothèque, le lecteur ou le pool de supports doit être vide pour effectuer cette opération.


</dt> </dl> </dd> <dt>

<span id="ERROR_MEDIA_UNAVAILABLE"></span><span id="error_media_unavailable"></span>**support d’erreur \_ \_ non disponible**
</dt> <dd> <dl> <dt>

4308 (0x10D4)
</dt> <dt>



Aucun support n’est actuellement disponible dans ce pool de médias ou cette bibliothèque.


</dt> </dl> </dd> <dt>

<span id="ERROR_RESOURCE_DISABLED"></span><span id="error_resource_disabled"></span>**ressource d’erreur \_ \_ désactivée**
</dt> <dd> <dl> <dt>

4309 (0x10D5)
</dt> <dt>



Une ressource requise pour cette opération est désactivée.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_CLEANER"></span><span id="error_invalid_cleaner"></span>**ERREUR \_ de \_ nettoyage non valide**
</dt> <dd> <dl> <dt>

4310 (0x10D6)
</dt> <dt>



L’identificateur de média ne représente pas un nettoyeur valide.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNABLE_TO_CLEAN"></span><span id="error_unable_to_clean"></span>**ERREUR \_ Impossible \_ de \_ nettoyer**
</dt> <dd> <dl> <dt>

4311 (0x10D7)
</dt> <dt>



Le lecteur ne peut pas être nettoyé ou ne prend pas en charge le nettoyage.


</dt> </dl> </dd> <dt>

<span id="ERROR_OBJECT_NOT_FOUND"></span><span id="error_object_not_found"></span>**\_objet d' \_ erreur \_ introuvable**
</dt> <dd> <dl> <dt>

4312 (0x10D8)
</dt> <dt>



L’identificateur d’objet ne représente pas un objet valide.


</dt> </dl> </dd> <dt>

<span id="ERROR_DATABASE_FAILURE"></span><span id="error_database_failure"></span>**\_échec de la base de données d’erreurs \_**
</dt> <dd> <dl> <dt>

4313 (0x10D9)
</dt> <dt>



Impossible de lire ou d’écrire dans la base de données.


</dt> </dl> </dd> <dt>

<span id="ERROR_DATABASE_FULL"></span><span id="error_database_full"></span>**\_base de données d’erreurs \_ pleine**
</dt> <dd> <dl> <dt>

4314 (0x10DA)
</dt> <dt>



La base de données est pleine.


</dt> </dl> </dd> <dt>

<span id="ERROR_MEDIA_INCOMPATIBLE"></span><span id="error_media_incompatible"></span>**support d’erreur \_ \_ incompatible**
</dt> <dd> <dl> <dt>

4315 (0x10DB)
</dt> <dt>



Le support n’est pas compatible avec le périphérique ou le pool de supports.


</dt> </dl> </dd> <dt>

<span id="ERROR_RESOURCE_NOT_PRESENT"></span><span id="error_resource_not_present"></span>**\_ressource d' \_ erreur \_ absente**
</dt> <dd> <dl> <dt>

4316 (0x10DC)
</dt> <dt>



La ressource requise pour cette opération n’existe pas.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_OPERATION"></span><span id="error_invalid_operation"></span>**ERREUR \_ d' \_ opération non valide**
</dt> <dd> <dl> <dt>

4317 (0x10DD)
</dt> <dt>



L’identificateur d’opération n’est pas valide.


</dt> </dl> </dd> <dt>

<span id="ERROR_MEDIA_NOT_AVAILABLE"></span><span id="error_media_not_available"></span>**le \_ support d’erreur \_ n’est pas \_ disponible**
</dt> <dd> <dl> <dt>

4318 (0x10DE)
</dt> <dt>



Le support n’est pas monté ou n’est pas prêt à être utilisé.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEVICE_NOT_AVAILABLE"></span><span id="error_device_not_available"></span>**périphérique d’erreur \_ \_ non \_ disponible**
</dt> <dd> <dl> <dt>

4319 (0x10DF)
</dt> <dt>



L’appareil n’est pas prêt à être utilisé.


</dt> </dl> </dd> <dt>

<span id="ERROR_REQUEST_REFUSED"></span><span id="error_request_refused"></span>**demande d’erreur \_ \_ refusée**
</dt> <dd> <dl> <dt>

4320 (0x10E0)
</dt> <dt>



L’opérateur ou l’administrateur a refusé la demande.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_DRIVE_OBJECT"></span><span id="error_invalid_drive_object"></span>**ERREUR \_ d' \_ objet lecteur non valide \_**
</dt> <dd> <dl> <dt>

4321 (0x10E1)
</dt> <dt>



L’identificateur de lecteur ne représente pas un lecteur valide.


</dt> </dl> </dd> <dt>

<span id="ERROR_LIBRARY_FULL"></span><span id="error_library_full"></span>**bibliothèque d’erreurs \_ \_ complète**
</dt> <dd> <dl> <dt>

4322 (0x10E2)
</dt> <dt>



La bibliothèque est pleine. Aucun emplacement n’est disponible pour utilisation.


</dt> </dl> </dd> <dt>

<span id="ERROR_MEDIUM_NOT_ACCESSIBLE"></span><span id="error_medium_not_accessible"></span>**support d’erreur \_ \_ non \_ accessible**
</dt> <dd> <dl> <dt>

4323 (0x10E3)
</dt> <dt>



Le transport ne peut pas accéder au support.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNABLE_TO_LOAD_MEDIUM"></span><span id="error_unable_to_load_medium"></span>**ERREUR \_ Impossible \_ de \_ charger le \_ support**
</dt> <dd> <dl> <dt>

4324 (0x10E4)
</dt> <dt>



Impossible de charger le média dans le lecteur.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNABLE_TO_INVENTORY_DRIVE"></span><span id="error_unable_to_inventory_drive"></span>**ERREUR \_ Impossible \_ d' \_ inventorier le \_ lecteur**
</dt> <dd> <dl> <dt>

4325 (0x10E5)
</dt> <dt>



Impossible de récupérer l’état du lecteur.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNABLE_TO_INVENTORY_SLOT"></span><span id="error_unable_to_inventory_slot"></span>**ERREUR \_ Impossible \_ d' \_ inventorier l' \_ emplacement**
</dt> <dd> <dl> <dt>

4326 (0x10E6)
</dt> <dt>



Impossible de récupérer l’état de l’emplacement.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNABLE_TO_INVENTORY_TRANSPORT"></span><span id="error_unable_to_inventory_transport"></span>**ERREUR \_ Impossible \_ d' \_ inventorier le \_ transport**
</dt> <dd> <dl> <dt>

4327 (0x10E7)
</dt> <dt>



Impossible de récupérer l’état du transport.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSPORT_FULL"></span><span id="error_transport_full"></span>**TRANSPORT d’erreur \_ \_ complet**
</dt> <dd> <dl> <dt>

4328 (0x10E8)
</dt> <dt>



Impossible d’utiliser le transport, car il est déjà en cours d’utilisation.


</dt> </dl> </dd> <dt>

<span id="ERROR_CONTROLLING_IEPORT"></span><span id="error_controlling_ieport"></span>**ERREUR de \_ contrôle de \_ insertion/éjection**
</dt> <dd> <dl> <dt>

4329 (0x10E9)
</dt> <dt>



Impossible d’ouvrir ou de fermer le port d’insertion/éjection.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNABLE_TO_EJECT_MOUNTED_MEDIA"></span><span id="error_unable_to_eject_mounted_media"></span>**ERREUR \_ Impossible \_ d' \_ éjecter le \_ \_ média monté**
</dt> <dd> <dl> <dt>

4330 (0x10EA)
</dt> <dt>



Impossible d’éjecter le support, car il se trouve dans un lecteur.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLEANER_SLOT_SET"></span><span id="error_cleaner_slot_set"></span>**\_jeu d' \_ emplacements de nettoyage d’erreur \_**
</dt> <dd> <dl> <dt>

4331 (0x10EB)
</dt> <dt>



Un emplacement de nettoyage est déjà réservé.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLEANER_SLOT_NOT_SET"></span><span id="error_cleaner_slot_not_set"></span>**\_emplacement du nettoyeur d’erreur \_ \_ non \_ défini**
</dt> <dd> <dl> <dt>

4332 (0x10EC)
</dt> <dt>



Un emplacement de nettoyage n’est pas réservé.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLEANER_CARTRIDGE_SPENT"></span><span id="error_cleaner_cartridge_spent"></span>**cartouche de nettoyage des erreurs \_ \_ \_ passée**
</dt> <dd> <dl> <dt>

4333 (0x10ED)
</dt> <dt>



La cartouche de nettoyage a effectué le nombre maximal de nettoyages de lecteur.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNEXPECTED_OMID"></span><span id="error_unexpected_omid"></span>**ERREUR \_ Omid inattendue \_**
</dt> <dd> <dl> <dt>

4334 (0x10EE)
</dt> <dt>



Identificateur on-medium inattendu.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANT_DELETE_LAST_ITEM"></span><span id="error_cant_delete_last_item"></span>**ERREUR \_ Impossible de \_ supprimer le \_ dernier \_ élément**
</dt> <dd> <dl> <dt>

4335 (0x10EF)
</dt> <dt>



Le dernier élément restant dans ce groupe ou cette ressource ne peut pas être supprimé.


</dt> </dl> </dd> <dt>

<span id="ERROR_MESSAGE_EXCEEDS_MAX_SIZE"></span><span id="error_message_exceeds_max_size"></span>**le \_ message d’erreur \_ dépasse la \_ \_ taille maximale**
</dt> <dd> <dl> <dt>

4336 (0x10F0)
</dt> <dt>



Le message fourni dépasse la taille maximale autorisée pour ce paramètre.


</dt> </dl> </dd> <dt>

<span id="ERROR_VOLUME_CONTAINS_SYS_FILES"></span><span id="error_volume_contains_sys_files"></span>**le \_ volume d’erreurs \_ contient des \_ \_ fichiers sys**
</dt> <dd> <dl> <dt>

4337 (0x10F1)
</dt> <dt>



Le volume contient des fichiers système ou d’échange.


</dt> </dl> </dd> <dt>

<span id="ERROR_INDIGENOUS_TYPE"></span><span id="error_indigenous_type"></span>**ERREUR \_ \_ type autochtone**
</dt> <dd> <dl> <dt>

4338 (0x10F2)
</dt> <dt>



Impossible de supprimer le type de média de cette bibliothèque, car au moins un lecteur de la bibliothèque peut prendre en charge ce type de média.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_SUPPORTING_DRIVES"></span><span id="error_no_supporting_drives"></span>**ERREUR \_ aucun \_ lecteur de prise en charge \_**
</dt> <dd> <dl> <dt>

4339 (0x10F3)
</dt> <dt>



Ce média hors connexion ne peut pas être monté sur ce système, car aucun lecteur activé ne peut être utilisé.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLEANER_CARTRIDGE_INSTALLED"></span><span id="error_cleaner_cartridge_installed"></span>**cartouche de nettoyage d’erreur \_ \_ \_ installée**
</dt> <dd> <dl> <dt>

4340 (0x10F4)
</dt> <dt>



Une cartouche de nettoyage est présente dans la bibliothèque de bandes.


</dt> </dl> </dd> <dt>

<span id="ERROR_IEPORT_FULL"></span><span id="error_ieport_full"></span>**ERREUR \_ insertion/éjection \_ complète**
</dt> <dd> <dl> <dt>

4341 (0x10F5)
</dt> <dt>



Impossible d’utiliser le port d’insertion/éjection, car il n’est pas vide.


</dt> </dl> </dd> <dt>

<span id="ERROR_FILE_OFFLINE"></span><span id="error_file_offline"></span>**fichier d’erreur \_ \_ hors connexion**
</dt> <dd> <dl> <dt>

4350 (0x10FE)
</dt> <dt>



Ce fichier n’est actuellement pas disponible pour être utilisé sur cet ordinateur.


</dt> </dl> </dd> <dt>

<span id="ERROR_REMOTE_STORAGE_NOT_ACTIVE"></span><span id="error_remote_storage_not_active"></span>**ERREUR \_ de \_ stockage distant \_ non \_ active**
</dt> <dd> <dl> <dt>

4351 (0x10FF)
</dt> <dt>



Le service de stockage distant n’est pas opérationnel pour l’instant.


</dt> </dl> </dd> <dt>

<span id="ERROR_REMOTE_STORAGE_MEDIA_ERROR"></span><span id="error_remote_storage_media_error"></span>**erreur \_ de \_ support de stockage distant \_ erreur \_**
</dt> <dd> <dl> <dt>

4352 (0x1100)
</dt> <dt>



Le service de stockage étendu a rencontré une erreur de support.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_A_REPARSE_POINT"></span><span id="error_not_a_reparse_point"></span>**ERREUR \_ non \_ un \_ point d’analyse \_**
</dt> <dd> <dl> <dt>

4390 (0x1126)
</dt> <dt>



Le fichier ou le répertoire n’est pas un point d’analyse.


</dt> </dl> </dd> <dt>

<span id="ERROR_REPARSE_ATTRIBUTE_CONFLICT"></span><span id="error_reparse_attribute_conflict"></span>**ERREUR lors de l’analyse d’un \_ \_ conflit d’attribut \_**
</dt> <dd> <dl> <dt>

4391 (0x1127)
</dt> <dt>



L’attribut de point d’analyse ne peut pas être défini, car il est en conflit avec un attribut existant.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_REPARSE_DATA"></span><span id="error_invalid_reparse_data"></span>**ERREUR \_ de \_ données d’analyse non valide \_**
</dt> <dd> <dl> <dt>

4392 (0x1128)
</dt> <dt>



Les données présentes dans la mémoire tampon du point d’analyse ne sont pas valides.


</dt> </dl> </dd> <dt>

<span id="ERROR_REPARSE_TAG_INVALID"></span><span id="error_reparse_tag_invalid"></span>**balise d’erreur d' \_ analyse \_ \_ non valide**
</dt> <dd> <dl> <dt>

4393 (0x1129)
</dt> <dt>



La balise présente dans la mémoire tampon du point d’analyse n’est pas valide.


</dt> </dl> </dd> <dt>

<span id="ERROR_REPARSE_TAG_MISMATCH"></span><span id="error_reparse_tag_mismatch"></span>**ERREUR d' \_ \_ incompatibilité de la balise d’analyse \_**
</dt> <dd> <dl> <dt>

4394 (0x112A)
</dt> <dt>



Il existe une incompatibilité entre la balise spécifiée dans la demande et la balise présente dans le point d’analyse.


</dt> </dl> </dd> <dt>

<span id="ERROR_APP_DATA_NOT_FOUND"></span><span id="error_app_data_not_found"></span>**données de l' \_ application erreur \_ \_ \_ introuvables**
</dt> <dd> <dl> <dt>

4400 (0x1130)
</dt> <dt>



Données du cache rapide introuvables.


</dt> </dl> </dd> <dt>

<span id="ERROR_APP_DATA_EXPIRED"></span><span id="error_app_data_expired"></span>**ERREUR lors de l’expiration des données de l' \_ application \_ \_**
</dt> <dd> <dl> <dt>

4401 (0x1131)
</dt> <dt>



Les données du cache rapide ont expiré.


</dt> </dl> </dd> <dt>

<span id="ERROR_APP_DATA_CORRUPT"></span><span id="error_app_data_corrupt"></span>**données d’application ERRONÉes \_ \_ \_ endommagées**
</dt> <dd> <dl> <dt>

4402 (0x1132)
</dt> <dt>



Données du cache rapide endommagées.


</dt> </dl> </dd> <dt>

<span id="ERROR_APP_DATA_LIMIT_EXCEEDED"></span><span id="error_app_data_limit_exceeded"></span>**limite de données d’application d’erreur \_ \_ \_ \_ dépassée**
</dt> <dd> <dl> <dt>

4403 (0x1133)
</dt> <dt>



Les données du cache rapide ont dépassé la taille maximale et ne peuvent pas être mises à jour.


</dt> </dl> </dd> <dt>

<span id="ERROR_APP_DATA_REBOOT_REQUIRED"></span><span id="error_app_data_reboot_required"></span>**ERREUR \_ de \_ redémarrage des données de l’application \_ \_ requise**
</dt> <dd> <dl> <dt>

4404 (0x1134)
</dt> <dt>



Le cache rapide a été réarmé et nécessite un redémarrage jusqu’à ce qu’il puisse être mis à jour.


</dt> </dl> </dd> <dt>

<span id="ERROR_SECUREBOOT_ROLLBACK_DETECTED"></span><span id="error_secureboot_rollback_detected"></span>**ERREUR \_ SECUREBOOT, \_ restauration \_ détectée**
</dt> <dd> <dl> <dt>

4420 (0x1144)
</dt> <dt>



Le démarrage sécurisé a détecté que la restauration des données protégées a été tentée.


</dt> </dl> </dd> <dt>

<span id="ERROR_SECUREBOOT_POLICY_VIOLATION"></span><span id="error_secureboot_policy_violation"></span>**ERREUR de violation de la \_ \_ stratégie SECUREBOOT \_**
</dt> <dd> <dl> <dt>

4421 (0x1145)
</dt> <dt>



La valeur est protégée par la stratégie de démarrage sécurisé et ne peut pas être modifiée ou supprimée.


</dt> </dl> </dd> <dt>

<span id="ERROR_SECUREBOOT_INVALID_POLICY"></span><span id="error_secureboot_invalid_policy"></span>**ERREUR \_ SECUREBOOT \_ , \_ stratégie non valide**
</dt> <dd> <dl> <dt>

4422 (0x1146)
</dt> <dt>



La stratégie de démarrage sécurisé n’est pas valide.


</dt> </dl> </dd> <dt>

<span id="ERROR_SECUREBOOT_POLICY_PUBLISHER_NOT_FOUND"></span><span id="error_secureboot_policy_publisher_not_found"></span>**ERREUR de l' \_ \_ éditeur de stratégie SECUREBOOT \_ \_ \_ introuvable**
</dt> <dd> <dl> <dt>

4423 (0x1147)
</dt> <dt>



Une nouvelle stratégie de démarrage sécurisé ne contenait pas le serveur de publication actuel dans sa liste de mises à jour.


</dt> </dl> </dd> <dt>

<span id="ERROR_SECUREBOOT_POLICY_NOT_SIGNED"></span><span id="error_secureboot_policy_not_signed"></span>**ERREUR de la \_ \_ stratégie SECUREBOOT \_ non \_ signée**
</dt> <dd> <dl> <dt>

4424 (0x1148)
</dt> <dt>



La stratégie de démarrage sécurisé n’est pas signée ou est signée par un signataire non approuvé.


</dt> </dl> </dd> <dt>

<span id="ERROR_SECUREBOOT_NOT_ENABLED"></span><span id="error_secureboot_not_enabled"></span>**ERREUR \_ SECUREBOOT \_ non \_ activée**
</dt> <dd> <dl> <dt>

4425 (0x1149)
</dt> <dt>



Le démarrage sécurisé n’est pas activé sur cet ordinateur.


</dt> </dl> </dd> <dt>

<span id="ERROR_SECUREBOOT_FILE_REPLACED"></span><span id="error_secureboot_file_replaced"></span>**ERREUR \_ \_ fichier SECUREBOOT \_ remplacé**
</dt> <dd> <dl> <dt>

4426 (0x114A)
</dt> <dt>



Le démarrage sécurisé nécessite que certains fichiers et pilotes ne soient pas remplacés par d’autres fichiers ou pilotes.


</dt> </dl> </dd> <dt>

<span id="ERROR_OFFLOAD_READ_FLT_NOT_SUPPORTED"></span><span id="error_offload_read_flt_not_supported"></span>**ERREUR de \_ lecture du déchargement \_ \_ flt \_ non \_ prise en charge**
</dt> <dd> <dl> <dt>

4440 (0x1158)
</dt> <dt>



L’opération de lecture du déchargement de copie n’est pas prise en charge par un filtre.


</dt> </dl> </dd> <dt>

<span id="ERROR_OFFLOAD_WRITE_FLT_NOT_SUPPORTED"></span><span id="error_offload_write_flt_not_supported"></span>**ERREUR de \_ déchargement d' \_ écriture \_ flt \_ non \_ prise en charge**
</dt> <dd> <dl> <dt>

4441 (0x1159)
</dt> <dt>



L’opération d’écriture de déchargement de copie n’est pas prise en charge par un filtre.


</dt> </dl> </dd> <dt>

<span id="ERROR_OFFLOAD_READ_FILE_NOT_SUPPORTED"></span><span id="error_offload_read_file_not_supported"></span>**ERREUR de \_ lecture de fichier de déchargement \_ \_ \_ non \_ prise en charge**
</dt> <dd> <dl> <dt>

4442 (0x115A)
</dt> <dt>



L’opération de lecture du déchargement de copie n’est pas prise en charge pour le fichier.


</dt> </dl> </dd> <dt>

<span id="ERROR_OFFLOAD_WRITE_FILE_NOT_SUPPORTED"></span><span id="error_offload_write_file_not_supported"></span>**ERREUR lors du \_ déchargement du \_ fichier d’écriture \_ \_ non \_ prise en charge**
</dt> <dd> <dl> <dt>

4443 (0x115B)
</dt> <dt>



L’opération d’écriture de déchargement de copie n’est pas prise en charge pour le fichier.


</dt> </dl> </dd> <dt>

<span id="ERROR_VOLUME_NOT_SIS_ENABLED"></span><span id="error_volume_not_sis_enabled"></span>**le \_ volume d’erreurs \_ n’est pas \_ activé pour SIS \_**
</dt> <dd> <dl> <dt>

4500 (0x1194)
</dt> <dt>



Le stockage d’instance simple n’est pas disponible sur ce volume.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEPENDENT_RESOURCE_EXISTS"></span><span id="error_dependent_resource_exists"></span>**la \_ ressource dépendante de l’erreur \_ \_ existe**
</dt> <dd> <dl> <dt>

5001 (0x1389)
</dt> <dt>



L’opération ne peut pas être effectuée, car d’autres ressources dépendent de cette ressource.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEPENDENCY_NOT_FOUND"></span><span id="error_dependency_not_found"></span>**\_dépendance d' \_ erreur \_ introuvable**
</dt> <dd> <dl> <dt>

5002 (0x138A)
</dt> <dt>



La dépendance de ressource de cluster est introuvable.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEPENDENCY_ALREADY_EXISTS"></span><span id="error_dependency_already_exists"></span>**la \_ dépendance d’erreur \_ \_ existe déjà**
</dt> <dd> <dl> <dt>

5003 (0x138B)
</dt> <dt>



La ressource de cluster ne peut pas être rendue dépendante de la ressource spécifiée, car elle est déjà dépendante.


</dt> </dl> </dd> <dt>

<span id="ERROR_RESOURCE_NOT_ONLINE"></span><span id="error_resource_not_online"></span>**la \_ ressource d’erreur \_ n’est pas \_ en ligne**
</dt> <dd> <dl> <dt>

5004 (0x138C)
</dt> <dt>



La ressource de cluster n’est pas en ligne.


</dt> </dl> </dd> <dt>

<span id="ERROR_HOST_NODE_NOT_AVAILABLE"></span><span id="error_host_node_not_available"></span>**le \_ nœud d’hôte d’erreur \_ n’est \_ pas \_ disponible**
</dt> <dd> <dl> <dt>

5005 (0x138D)
</dt> <dt>



Un nœud de cluster n’est pas disponible pour cette opération.


</dt> </dl> </dd> <dt>

<span id="ERROR_RESOURCE_NOT_AVAILABLE"></span><span id="error_resource_not_available"></span>**ressource d’erreur \_ \_ non \_ disponible**
</dt> <dd> <dl> <dt>

5006 (0x138E)
</dt> <dt>



La ressource de cluster n’est pas disponible.


</dt> </dl> </dd> <dt>

<span id="ERROR_RESOURCE_NOT_FOUND"></span><span id="error_resource_not_found"></span>**\_ressource d' \_ erreur \_ introuvable**
</dt> <dd> <dl> <dt>

5007 (0x138F)
</dt> <dt>



La ressource de cluster est introuvable.


</dt> </dl> </dd> <dt>

<span id="ERROR_SHUTDOWN_CLUSTER"></span><span id="error_shutdown_cluster"></span>**ERREUR lors de l' \_ arrêt du \_ cluster**
</dt> <dd> <dl> <dt>

5008 (0x1390)
</dt> <dt>



Le cluster est en cours d’arrêt.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANT_EVICT_ACTIVE_NODE"></span><span id="error_cant_evict_active_node"></span>**ERREUR \_ Impossible de \_ supprimer le \_ \_ nœud actif**
</dt> <dd> <dl> <dt>

5009 (0x1391)
</dt> <dt>



Un nœud de cluster ne peut pas être expulsé du cluster, sauf si le nœud est en service ou s’il s’agit du dernier nœud.


</dt> </dl> </dd> <dt>

<span id="ERROR_OBJECT_ALREADY_EXISTS"></span><span id="error_object_already_exists"></span>**l' \_ objet d’erreur \_ \_ existe déjà**
</dt> <dd> <dl> <dt>

5010 (0x1392)
</dt> <dt>



L'objet existe déjà.


</dt> </dl> </dd> <dt>

<span id="ERROR_OBJECT_IN_LIST"></span><span id="error_object_in_list"></span>**\_objet \_ d’erreur dans la \_ liste**
</dt> <dd> <dl> <dt>

5011 (0x1393)
</dt> <dt>



L’objet figure déjà dans la liste.


</dt> </dl> </dd> <dt>

<span id="ERROR_GROUP_NOT_AVAILABLE"></span><span id="error_group_not_available"></span>**Groupe d’erreurs \_ \_ non \_ disponible**
</dt> <dd> <dl> <dt>

5012 (0x1394)
</dt> <dt>



Le groupe de clusters n’est pas disponible pour les nouvelles demandes.


</dt> </dl> </dd> <dt>

<span id="ERROR_GROUP_NOT_FOUND"></span><span id="error_group_not_found"></span>**\_groupe d' \_ Erreurs \_ introuvable**
</dt> <dd> <dl> <dt>

5013 (0x1395)
</dt> <dt>



Le groupe de clusters est introuvable.


</dt> </dl> </dd> <dt>

<span id="ERROR_GROUP_NOT_ONLINE"></span><span id="error_group_not_online"></span>**Groupe d’erreurs \_ \_ non \_ en ligne**
</dt> <dd> <dl> <dt>

5014 (0x1396)
</dt> <dt>



L’opération n’a pas pu aboutir car le groupe de clusters n’est pas en ligne.


</dt> </dl> </dd> <dt>

<span id="ERROR_HOST_NODE_NOT_RESOURCE_OWNER"></span><span id="error_host_node_not_resource_owner"></span>**ERREUR \_ du \_ nœud \_ hôte \_ non \_ propriétaire de la ressource**
</dt> <dd> <dl> <dt>

5015 (0x1397)
</dt> <dt>



L’opération a échoué, car le nœud de cluster spécifié n’est pas le propriétaire de la ressource ou le nœud n’est pas un propriétaire possible de la ressource.


</dt> </dl> </dd> <dt>

<span id="ERROR_HOST_NODE_NOT_GROUP_OWNER"></span><span id="error_host_node_not_group_owner"></span>**ERREUR \_ le \_ nœud hôte \_ n’est pas \_ propriétaire du groupe \_**
</dt> <dd> <dl> <dt>

5016 (0x1398)
</dt> <dt>



L’opération a échoué car le nœud de cluster spécifié n’est pas le propriétaire du groupe ou le nœud n’est pas un propriétaire possible du groupe.


</dt> </dl> </dd> <dt>

<span id="ERROR_RESMON_CREATE_FAILED"></span><span id="error_resmon_create_failed"></span>**ERREUR \_ RESMON \_ échec de la création \_**
</dt> <dd> <dl> <dt>

5017 (0x1399)
</dt> <dt>



Impossible de créer la ressource de cluster dans le moniteur de ressource spécifié.


</dt> </dl> </dd> <dt>

<span id="ERROR_RESMON_ONLINE_FAILED"></span><span id="error_resmon_online_failed"></span>**ERREUR \_ RESMON \_ en ligne \_**
</dt> <dd> <dl> <dt>

5018 (0x139A)
</dt> <dt>



La ressource de cluster n’a pas pu être mise en ligne par le moniteur de ressource.


</dt> </dl> </dd> <dt>

<span id="ERROR_RESOURCE_ONLINE"></span><span id="error_resource_online"></span>**ressource d’erreur \_ \_ en ligne**
</dt> <dd> <dl> <dt>

5019 (0x139B)
</dt> <dt>



L’opération n’a pas pu aboutir car la ressource de cluster est en ligne.


</dt> </dl> </dd> <dt>

<span id="ERROR_QUORUM_RESOURCE"></span><span id="error_quorum_resource"></span>**\_ressource de quorum d’erreur \_**
</dt> <dd> <dl> <dt>

5020 (0x139C)
</dt> <dt>



La ressource de cluster n’a pas pu être supprimée ou mise hors connexion, car il s’agit de la ressource de quorum.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_QUORUM_CAPABLE"></span><span id="error_not_quorum_capable"></span>**ERREUR \_ non liée au \_ quorum \_**
</dt> <dd> <dl> <dt>

5021 (0x139D)
</dt> <dt>



Le cluster n’a pas pu transformer la ressource spécifiée en ressource de quorum car elle ne peut pas être une ressource de quorum.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_SHUTTING_DOWN"></span><span id="error_cluster_shutting_down"></span>**\_arrêt du cluster d’erreurs \_ \_**
</dt> <dd> <dl> <dt>

5022 (0x139E)
</dt> <dt>



Le logiciel de cluster est en cours d’arrêt.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_STATE"></span><span id="error_invalid_state"></span>**État d’erreur \_ non valide \_**
</dt> <dd> <dl> <dt>

5023 (0x139F)
</dt> <dt>



Le groupe ou la ressource n’est pas dans l’état correct pour effectuer l’opération demandée.


</dt> </dl> </dd> <dt>

<span id="ERROR_RESOURCE_PROPERTIES_STORED"></span><span id="error_resource_properties_stored"></span>**Propriétés des ressources d’erreur \_ \_ \_ stockées**
</dt> <dd> <dl> <dt>

5024 (0x13A0)
</dt> <dt>



Les propriétés ont été stockées, mais toutes les modifications ne prendront effet qu’à la prochaine mise en ligne de la ressource.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_QUORUM_CLASS"></span><span id="error_not_quorum_class"></span>**ERREUR \_ non \_ de \_ classe de quorum**
</dt> <dd> <dl> <dt>

5025 (0x13A1)
</dt> <dt>



Le cluster n’a pas pu faire de la ressource spécifiée une ressource de quorum car elle n’appartient pas à une classe de stockage partagée.


</dt> </dl> </dd> <dt>

<span id="ERROR_CORE_RESOURCE"></span><span id="error_core_resource"></span>**ERREUR \_ de \_ ressource principale**
</dt> <dd> <dl> <dt>

5026 (0x13A2)
</dt> <dt>



La ressource de cluster n’a pas pu être supprimée, car il s’agit d’une ressource principale.


</dt> </dl> </dd> <dt>

<span id="ERROR_QUORUM_RESOURCE_ONLINE_FAILED"></span><span id="error_quorum_resource_online_failed"></span>**échec de la ressource de quorum d’erreur \_ \_ \_ en ligne \_**
</dt> <dd> <dl> <dt>

5027 (0x13A3)
</dt> <dt>



La ressource de quorum n’a pas pu être mise en ligne.


</dt> </dl> </dd> <dt>

<span id="ERROR_QUORUMLOG_OPEN_FAILED"></span><span id="error_quorumlog_open_failed"></span>**échec de l’ouverture du QUORUMLOG d’erreur \_ \_ \_**
</dt> <dd> <dl> <dt>

5028 (0x13A4)
</dt> <dt>



Le journal de quorum n’a pas pu être créé ou monté correctement.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTERLOG_CORRUPT"></span><span id="error_clusterlog_corrupt"></span>**ERREUR \_ Clusterlog \_ endommagée**
</dt> <dd> <dl> <dt>

5029 (0x13A5)
</dt> <dt>



Le journal de cluster est endommagé.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTERLOG_RECORD_EXCEEDS_MAXSIZE"></span><span id="error_clusterlog_record_exceeds_maxsize"></span>**l’erreur de l' \_ \_ enregistrement Clusterlog \_ dépasse \_ MaxSize**
</dt> <dd> <dl> <dt>

5030 (0x13A6)
</dt> <dt>



L’enregistrement n’a pas pu être écrit dans le journal du cluster, car il dépasse la taille maximale.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTERLOG_EXCEEDS_MAXSIZE"></span><span id="error_clusterlog_exceeds_maxsize"></span>**l’erreur \_ Clusterlog \_ dépasse \_ MaxSize**
</dt> <dd> <dl> <dt>

5031 (0x13A7)
</dt> <dt>



Le journal du cluster dépasse sa taille maximale.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTERLOG_CHKPOINT_NOT_FOUND"></span><span id="error_clusterlog_chkpoint_not_found"></span>**ERREUR \_ Clusterlog \_ CHKPOINT \_ \_ introuvable**
</dt> <dd> <dl> <dt>

5032 (0x13A8)
</dt> <dt>



Aucun enregistrement de point de contrôle n’a été trouvé dans le journal de cluster.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTERLOG_NOT_ENOUGH_SPACE"></span><span id="error_clusterlog_not_enough_space"></span>**ERREUR \_ Clusterlog \_ \_ espace insuffisant \_**
</dt> <dd> <dl> <dt>

5033 (0x13A9)
</dt> <dt>



L’espace disque minimal requis pour la journalisation n’est pas disponible.


</dt> </dl> </dd> <dt>

<span id="ERROR_QUORUM_OWNER_ALIVE"></span><span id="error_quorum_owner_alive"></span>**propriétaire du quorum d’erreurs \_ \_ \_ actif**
</dt> <dd> <dl> <dt>

5034 (0x13AA)
</dt> <dt>



Le nœud de cluster n’a pas pu prendre le contrôle de la ressource de quorum, car la ressource est détenue par un autre nœud actif.


</dt> </dl> </dd> <dt>

<span id="ERROR_NETWORK_NOT_AVAILABLE"></span><span id="error_network_not_available"></span>**ERREUR \_ réseau \_ non \_ disponible**
</dt> <dd> <dl> <dt>

5035 (0x13AB)
</dt> <dt>



Un réseau de clusters n’est pas disponible pour cette opération.


</dt> </dl> </dd> <dt>

<span id="ERROR_NODE_NOT_AVAILABLE"></span><span id="error_node_not_available"></span>**nœud d’erreur \_ \_ non \_ disponible**
</dt> <dd> <dl> <dt>

5036 (0x13AC)
</dt> <dt>



Un nœud de cluster n’est pas disponible pour cette opération.


</dt> </dl> </dd> <dt>

<span id="ERROR_ALL_NODES_NOT_AVAILABLE"></span><span id="error_all_nodes_not_available"></span>**ERREUR \_ tous les \_ nœuds \_ non \_ disponibles**
</dt> <dd> <dl> <dt>

5037 (0x13AD)
</dt> <dt>



Tous les nœuds de cluster doivent être en cours d’exécution pour effectuer cette opération.


</dt> </dl> </dd> <dt>

<span id="ERROR_RESOURCE_FAILED"></span><span id="error_resource_failed"></span>**échec de la ressource d’erreur \_ \_**
</dt> <dd> <dl> <dt>

5038 (0x13AE)
</dt> <dt>



échec d’une ressource de cluster.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_INVALID_NODE"></span><span id="error_cluster_invalid_node"></span>**nœud d’erreur de \_ cluster \_ non valide \_**
</dt> <dd> <dl> <dt>

5039 (0x13AF)
</dt> <dt>



Le nœud de cluster n’est pas valide.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NODE_EXISTS"></span><span id="error_cluster_node_exists"></span>**le \_ nœud de cluster d’erreurs \_ \_ existe**
</dt> <dd> <dl> <dt>

5040 (0x13B0)
</dt> <dt>



Le nœud de cluster existe déjà.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_JOIN_IN_PROGRESS"></span><span id="error_cluster_join_in_progress"></span>**ERREUR \_ \_ de jonction \_ de cluster en \_ cours**
</dt> <dd> <dl> <dt>

5041 (0x13B1)
</dt> <dt>



Un nœud est en train de joindre le cluster.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NODE_NOT_FOUND"></span><span id="error_cluster_node_not_found"></span>**nœud de cluster d’erreurs \_ \_ \_ \_ introuvable**
</dt> <dd> <dl> <dt>

5042 (0x13B2)
</dt> <dt>



Le nœud de cluster est introuvable.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_LOCAL_NODE_NOT_FOUND"></span><span id="error_cluster_local_node_not_found"></span>**le \_ nœud local du cluster d’erreurs est \_ \_ \_ \_ introuvable**
</dt> <dd> <dl> <dt>

5043 (0x13B3)
</dt> <dt>



Les informations du nœud local du cluster sont introuvables.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NETWORK_EXISTS"></span><span id="error_cluster_network_exists"></span>**le \_ réseau du cluster d’erreurs \_ \_ existe**
</dt> <dd> <dl> <dt>

5044 (0x13B4)
</dt> <dt>



Le réseau de clusters existe déjà.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NETWORK_NOT_FOUND"></span><span id="error_cluster_network_not_found"></span>**le réseau du cluster d’erreurs est \_ \_ \_ \_ introuvable**
</dt> <dd> <dl> <dt>

5045 (0x13B5)
</dt> <dt>



Le réseau de clusters est introuvable.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NETINTERFACE_EXISTS"></span><span id="error_cluster_netinterface_exists"></span>**l’erreur \_ cluster \_ netinterface \_ existe**
</dt> <dd> <dl> <dt>

5046 (0x13B6)
</dt> <dt>



L’interface réseau de clusters existe déjà.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NETINTERFACE_NOT_FOUND"></span><span id="error_cluster_netinterface_not_found"></span>**ERREUR \_ de \_ netinterface de cluster \_ \_ introuvable**
</dt> <dd> <dl> <dt>

5047 (0x13B7)
</dt> <dt>



L’interface réseau du cluster est introuvable.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_INVALID_REQUEST"></span><span id="error_cluster_invalid_request"></span>**demande de cluster d’erreurs \_ \_ non valide \_**
</dt> <dd> <dl> <dt>

5048 (0x13B8)
</dt> <dt>



La demande de cluster n’est pas valide pour cet objet.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_INVALID_NETWORK_PROVIDER"></span><span id="error_cluster_invalid_network_provider"></span>**\_ \_ fournisseur réseau non valide du cluster d’erreurs \_ \_**
</dt> <dd> <dl> <dt>

5049 (0x13B9)
</dt> <dt>



Le fournisseur réseau de clusters n’est pas valide.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NODE_DOWN"></span><span id="error_cluster_node_down"></span>**nœud de cluster d’erreurs \_ \_ \_ inactif**
</dt> <dd> <dl> <dt>

5050 (0x13BA)
</dt> <dt>



Le nœud de cluster est inactif.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NODE_UNREACHABLE"></span><span id="error_cluster_node_unreachable"></span>**ERREUR \_ de \_ nœud de cluster \_ inaccessible**
</dt> <dd> <dl> <dt>

5051 (0x13BB)
</dt> <dt>



Le nœud de cluster n’est pas accessible.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NODE_NOT_MEMBER"></span><span id="error_cluster_node_not_member"></span>**nœud de cluster d’erreurs \_ \_ \_ non \_ membre**
</dt> <dd> <dl> <dt>

5052 (0x13BC)
</dt> <dt>



Le nœud de cluster n’est pas membre du cluster.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_JOIN_NOT_IN_PROGRESS"></span><span id="error_cluster_join_not_in_progress"></span>**la \_ \_ jonction \_ du cluster d’erreurs n’est pas \_ en \_ cours**
</dt> <dd> <dl> <dt>

5053 (0x13BD)
</dt> <dt>



Une opération de jonction de clusters n’est pas en cours.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_INVALID_NETWORK"></span><span id="error_cluster_invalid_network"></span>**réseau d’erreurs \_ \_ réseau non valide \_**
</dt> <dd> <dl> <dt>

5054 (0x13BE)
</dt> <dt>



Le réseau de clusters n’est pas valide.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NODE_UP"></span><span id="error_cluster_node_up"></span>**nœud de cluster d’erreurs \_ \_ vers le \_ haut**
</dt> <dd> <dl> <dt>

5056 (0x13C0)
</dt> <dt>



Le nœud de cluster est en place.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_IPADDR_IN_USE"></span><span id="error_cluster_ipaddr_in_use"></span>**\_ \_ ipaddr du cluster \_ d’erreurs en cours d' \_ utilisation**
</dt> <dd> <dl> <dt>

5057 (0x13C1)
</dt> <dt>



L’adresse IP de cluster est déjà utilisée.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NODE_NOT_PAUSED"></span><span id="error_cluster_node_not_paused"></span>**nœud de cluster d’erreurs \_ \_ \_ non \_ suspendu**
</dt> <dd> <dl> <dt>

5058 (0x13C2)
</dt> <dt>



Le nœud de cluster n’est pas suspendu.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NO_SECURITY_CONTEXT"></span><span id="error_cluster_no_security_context"></span>**CLUSTER d’erreurs- \_ \_ aucun \_ contexte de sécurité \_**
</dt> <dd> <dl> <dt>

5059 (0x13C3)
</dt> <dt>



Aucun contexte de sécurité de cluster n’est disponible.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NETWORK_NOT_INTERNAL"></span><span id="error_cluster_network_not_internal"></span>**ERREUR \_ réseau de cluster \_ \_ non \_ interne**
</dt> <dd> <dl> <dt>

5060 (0x13C4)
</dt> <dt>



Le réseau de clusters n’est pas configuré pour la communication interne du cluster.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NODE_ALREADY_UP"></span><span id="error_cluster_node_already_up"></span>**nœud de cluster d’erreurs \_ \_ déjà en \_ cours \_**
</dt> <dd> <dl> <dt>

5061 (0x13C5)
</dt> <dt>



Le nœud de cluster est déjà en cours d’installation.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NODE_ALREADY_DOWN"></span><span id="error_cluster_node_already_down"></span>**nœud de cluster d’erreurs \_ \_ déjà en cours d' \_ \_ inversion**
</dt> <dd> <dl> <dt>

5062 (0x13C6)
</dt> <dt>



Le nœud de cluster est déjà en cours d’inversion.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NETWORK_ALREADY_ONLINE"></span><span id="error_cluster_network_already_online"></span>**ERREUR \_ réseau de cluster \_ \_ déjà \_ en ligne**
</dt> <dd> <dl> <dt>

5063 (0x13C7)
</dt> <dt>



Le réseau de clusters est déjà en ligne.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NETWORK_ALREADY_OFFLINE"></span><span id="error_cluster_network_already_offline"></span>**ERREUR \_ réseau de clusters \_ \_ déjà \_ hors connexion**
</dt> <dd> <dl> <dt>

5064 (0x13C8)
</dt> <dt>



Le réseau de clusters est déjà hors connexion.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NODE_ALREADY_MEMBER"></span><span id="error_cluster_node_already_member"></span>**nœud de cluster d’erreurs \_ \_ \_ déjà \_ membre**
</dt> <dd> <dl> <dt>

5065 (0x13C9)
</dt> <dt>



Le nœud de cluster est déjà membre du cluster.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_LAST_INTERNAL_NETWORK"></span><span id="error_cluster_last_internal_network"></span>**ERREUR \_ du \_ dernier \_ réseau interne du cluster \_**
</dt> <dd> <dl> <dt>

5066 (0x13CA)
</dt> <dt>



Le réseau de clusters est le seul configuré pour la communication interne du cluster entre deux nœuds de cluster actifs ou plus. La capacité de communication interne ne peut pas être supprimée du réseau.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NETWORK_HAS_DEPENDENTS"></span><span id="error_cluster_network_has_dependents"></span>**ERREUR liée au \_ réseau de clusters d’erreurs \_ \_ \_**
</dt> <dd> <dl> <dt>

5067 (0x13CB)
</dt> <dt>



Une ou plusieurs ressources de cluster dépendent du réseau pour fournir le service aux clients. La fonctionnalité d’accès client ne peut pas être supprimée du réseau.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_OPERATION_ON_QUORUM"></span><span id="error_invalid_operation_on_quorum"></span>**ERREUR \_ \_ d’opération non valide \_ sur le \_ quorum**
</dt> <dd> <dl> <dt>

5068 (0x13CC)
</dt> <dt>



Cette opération ne peut pas être effectuée sur la ressource de cluster en tant que ressource de quorum. Vous ne pouvez pas mettre la ressource de quorum hors connexion ou modifier sa liste de propriétaires possibles.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEPENDENCY_NOT_ALLOWED"></span><span id="error_dependency_not_allowed"></span>**dépendance d’erreur \_ \_ non \_ autorisée**
</dt> <dd> <dl> <dt>

5069 (0x13CD)
</dt> <dt>



La ressource quorum du cluster n’est pas autorisée à avoir des dépendances.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NODE_PAUSED"></span><span id="error_cluster_node_paused"></span>**nœud de cluster d’erreurs \_ \_ \_ suspendu**
</dt> <dd> <dl> <dt>

5070 (0x13CE)
</dt> <dt>



Le nœud de cluster est suspendu.


</dt> </dl> </dd> <dt>

<span id="ERROR_NODE_CANT_HOST_RESOURCE"></span><span id="error_node_cant_host_resource"></span>**nœud d’erreur déverser la \_ \_ \_ \_ ressource hôte**
</dt> <dd> <dl> <dt>

5071 (0x13CF)
</dt> <dt>



La ressource de cluster ne peut pas être mise en ligne. Le nœud propriétaire ne peut pas exécuter cette ressource.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NODE_NOT_READY"></span><span id="error_cluster_node_not_ready"></span>**le \_ nœud de cluster d’erreur \_ n’est \_ pas \_ prêt**
</dt> <dd> <dl> <dt>

5072 (0x13D0)
</dt> <dt>



Le nœud de cluster n’est pas prêt à effectuer l’opération demandée.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NODE_SHUTTING_DOWN"></span><span id="error_cluster_node_shutting_down"></span>**ERREUR lors de l’arrêt du nœud de \_ cluster \_ \_ \_**
</dt> <dd> <dl> <dt>

5073 (0x13D1)
</dt> <dt>



Le nœud de cluster est en cours d’arrêt.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_JOIN_ABORTED"></span><span id="error_cluster_join_aborted"></span>**ERREUR \_ de \_ jonction de cluster \_ abandonnée**
</dt> <dd> <dl> <dt>

5074 (0x13D2)
</dt> <dt>



L’opération de jonction de cluster a été abandonnée.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_INCOMPATIBLE_VERSIONS"></span><span id="error_cluster_incompatible_versions"></span>**\_ \_ versions incompatibles du cluster d’erreurs \_**
</dt> <dd> <dl> <dt>

5075 (0x13D3)
</dt> <dt>



L’opération de jonction de cluster a échoué en raison de versions logicielles incompatibles entre le nœud joint et son sponsor.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_MAXNUM_OF_RESOURCES_EXCEEDED"></span><span id="error_cluster_maxnum_of_resources_exceeded"></span>**\_ \_ MAXNUM \_ de ressources de cluster d’erreurs \_ \_ dépassé**
</dt> <dd> <dl> <dt>

5076 (0x13D4)
</dt> <dt>



Impossible de créer cette ressource, car le cluster a atteint la limite du nombre de ressources qu’il peut surveiller.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_SYSTEM_CONFIG_CHANGED"></span><span id="error_cluster_system_config_changed"></span>**ERREUR \_ de \_ configuration du système de cluster \_ \_ modifiée**
</dt> <dd> <dl> <dt>

5077 (0x13D5)
</dt> <dt>



La configuration système a été modifiée lors de la jonction de cluster ou de l’opération de formulaire. L’opération de jointure ou de formulaire a été abandonnée.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_RESOURCE_TYPE_NOT_FOUND"></span><span id="error_cluster_resource_type_not_found"></span>**ERREUR de \_ type de ressource de cluster \_ \_ \_ \_ introuvable**
</dt> <dd> <dl> <dt>

5078 (0x13D6)
</dt> <dt>



Le type de ressource spécifié est introuvable.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_RESTYPE_NOT_SUPPORTED"></span><span id="error_cluster_restype_not_supported"></span>**RESTYPE du cluster d’erreurs \_ \_ \_ non \_ pris en charge**
</dt> <dd> <dl> <dt>

5079 (0x13D7)
</dt> <dt>



Le nœud spécifié ne prend pas en charge une ressource de ce type. Cela peut être dû à des incohérences de version ou en raison de l’absence de la DLL de ressource sur ce nœud.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_RESNAME_NOT_FOUND"></span><span id="error_cluster_resname_not_found"></span>**RESNAME du cluster d’erreurs \_ \_ \_ \_ introuvable**
</dt> <dd> <dl> <dt>

5080 (0x13D8)
</dt> <dt>



Le nom de ressource spécifié n’est pas pris en charge par cette DLL de ressource. Cela peut être dû à un nom incorrect (ou modifié) fourni à la DLL de ressource.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NO_RPC_PACKAGES_REGISTERED"></span><span id="error_cluster_no_rpc_packages_registered"></span>**CLUSTER d’erreurs- \_ \_ aucun \_ \_ package RPC \_ inscrit**
</dt> <dd> <dl> <dt>

5081 (0x13D9)
</dt> <dt>



Aucun package d’authentification n’a pu être inscrit auprès du serveur RPC.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_OWNER_NOT_IN_PREFLIST"></span><span id="error_cluster_owner_not_in_preflist"></span>**le \_ \_ propriétaire \_ du cluster d’erreurs n’est pas \_ dans \_ PREFLIST**
</dt> <dd> <dl> <dt>

5082 (0x13DA)
</dt> <dt>



Vous ne pouvez pas mettre le groupe en ligne, car le propriétaire du groupe n’est pas dans la liste par défaut du groupe. Pour modifier le nœud propriétaire du groupe, déplacez le groupe.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_DATABASE_SEQMISMATCH"></span><span id="error_cluster_database_seqmismatch"></span>**ERREUR \_ \_ de base de données de cluster \_ SEQMISMATCH**
</dt> <dd> <dl> <dt>

5083 (0x13DB)
</dt> <dt>



L’opération de jointure a échoué, car le numéro de séquence de la base de données de cluster a été modifié ou n’est pas compatible avec le nœud de verrouillage. Cela peut se produire lors d’une opération de jointure si la base de données de cluster a été modifiée lors de la jointure.


</dt> </dl> </dd> <dt>

<span id="ERROR_RESMON_INVALID_STATE"></span><span id="error_resmon_invalid_state"></span>**ERREUR \_ RESMON \_ État non valide \_**
</dt> <dd> <dl> <dt>

5084 (0x13DC)
</dt> <dt>



Le moniteur de ressource n’autorise pas l’exécution de l’opération d’échec tant que la ressource est dans son état actuel. Cela peut se produire si la ressource est dans un état d’attente.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_GUM_NOT_LOCKER"></span><span id="error_cluster_gum_not_locker"></span>**ERREUR de blocage de la \_ gomme du cluster \_ \_ \_**
</dt> <dd> <dl> <dt>

5085 (0x13DD)
</dt> <dt>



Un code qui n’a pas de verrou a reçu une demande de réservation du verrou pour la mise à jour globale.


</dt> </dl> </dd> <dt>

<span id="ERROR_QUORUM_DISK_NOT_FOUND"></span><span id="error_quorum_disk_not_found"></span>**ERREUR \_ \_ disque quorum \_ \_ introuvable**
</dt> <dd> <dl> <dt>

5086 (0x13DE)
</dt> <dt>



Le disque quorum n’a pas pu être localisé par le service de cluster.


</dt> </dl> </dd> <dt>

<span id="ERROR_DATABASE_BACKUP_CORRUPT"></span><span id="error_database_backup_corrupt"></span>**ERREUR \_ de sauvegarde de base de données \_ \_ endommagée**
</dt> <dd> <dl> <dt>

5087 (0x13DF)
</dt> <dt>



La base de données de cluster sauvegardée est peut-être endommagée.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NODE_ALREADY_HAS_DFS_ROOT"></span><span id="error_cluster_node_already_has_dfs_root"></span>**le \_ nœud de cluster d’erreurs \_ \_ a déjà une \_ \_ \_ racine DFS**
</dt> <dd> <dl> <dt>

5088 (0x13E0)
</dt> <dt>



Il existe déjà une racine DFS dans ce nœud de cluster.


</dt> </dl> </dd> <dt>

<span id="ERROR_RESOURCE_PROPERTY_UNCHANGEABLE"></span><span id="error_resource_property_unchangeable"></span>**propriété de ressource d’erreur non \_ \_ \_ modifiable**
</dt> <dd> <dl> <dt>

5089 (0x13E1)
</dt> <dt>



Une tentative de modification d’une propriété de ressource a échoué, car elle est en conflit avec une autre propriété existante.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_MEMBERSHIP_INVALID_STATE"></span><span id="error_cluster_membership_invalid_state"></span>**\_État d' \_ appartenance au cluster d’erreurs \_ non valide \_**
</dt> <dd> <dl> <dt>

5890 (0x1702)
</dt> <dt>



Une opération qui n’est pas compatible avec l’état d’appartenance actuel du nœud a été tentée.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_QUORUMLOG_NOT_FOUND"></span><span id="error_cluster_quorumlog_not_found"></span>**QUORUMLOG du cluster d’erreurs \_ \_ \_ \_ introuvable**
</dt> <dd> <dl> <dt>

5891 (0x1703)
</dt> <dt>



La ressource quorum ne contient pas le journal quorum.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_MEMBERSHIP_HALT"></span><span id="error_cluster_membership_halt"></span>**ERREUR \_ d' \_ arrêt de l’appartenance au cluster \_**
</dt> <dd> <dl> <dt>

5892 (0x1704)
</dt> <dt>



Le moteur d’appartenance a demandé l’arrêt du service de cluster sur ce nœud.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_INSTANCE_ID_MISMATCH"></span><span id="error_cluster_instance_id_mismatch"></span>**ERREUR \_ d' \_ \_ incompatibilité d’ID d’instance de cluster \_**
</dt> <dd> <dl> <dt>

5893 (0x1705)
</dt> <dt>



L’opération de jointure a échoué, car l’ID d’instance de cluster du nœud joint ne correspond pas à l’ID d’instance de cluster du nœud sponsor.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NETWORK_NOT_FOUND_FOR_IP"></span><span id="error_cluster_network_not_found_for_ip"></span>**le \_ \_ réseau du cluster d’erreurs est \_ \_ introuvable \_ pour l' \_ adresse IP**
</dt> <dd> <dl> <dt>

5894 (0x1706)
</dt> <dt>



Impossible de trouver un réseau de clusters correspondant pour l’adresse IP spécifiée.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_PROPERTY_DATA_TYPE_MISMATCH"></span><span id="error_cluster_property_data_type_mismatch"></span>**incompatibilité de type de données de propriété de cluster d’erreurs \_ \_ \_ \_ \_**
</dt> <dd> <dl> <dt>

5895 (0x1707)
</dt> <dt>



Le type de données réel de la propriété ne correspond pas au type de données attendu de la propriété.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_EVICT_WITHOUT_CLEANUP"></span><span id="error_cluster_evict_without_cleanup"></span>**suppression du cluster d’erreurs \_ \_ \_ sans \_ nettoyage**
</dt> <dd> <dl> <dt>

5896 (0x1708)
</dt> <dt>



Le nœud de cluster a été supprimé du cluster avec succès, mais le nœud n’a pas été nettoyé. Pour déterminer les étapes de nettoyage qui ont échoué et comment récupérer, consultez le journal des événements de l’application de clustering de basculement à l’aide de observateur d’événements.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_PARAMETER_MISMATCH"></span><span id="error_cluster_parameter_mismatch"></span>**incompatibilité des paramètres de cluster d’erreurs \_ \_ \_**
</dt> <dd> <dl> <dt>

5897 (0x1709)
</dt> <dt>



Au moins deux valeurs de paramètre spécifiées pour les propriétés d’une ressource sont en conflit.


</dt> </dl> </dd> <dt>

<span id="ERROR_NODE_CANNOT_BE_CLUSTERED"></span><span id="error_node_cannot_be_clustered"></span>**le \_ nœud d’erreur \_ ne peut pas \_ être \_ mis en cluster**
</dt> <dd> <dl> <dt>

5898 (0x170A)
</dt> <dt>



Cet ordinateur ne peut pas être membre d’un cluster.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_WRONG_OS_VERSION"></span><span id="error_cluster_wrong_os_version"></span>**ERREUR \_ de \_ \_ version du système d’exploitation incorrecte du cluster \_**
</dt> <dd> <dl> <dt>

5899 (0x170B)
</dt> <dt>



Cet ordinateur ne peut pas être membre d’un cluster, car il n’a pas la version appropriée de Windows installée.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_CANT_CREATE_DUP_CLUSTER_NAME"></span><span id="error_cluster_cant_create_dup_cluster_name"></span>**ERREUR de \_ cluster \_ Impossible de créer un \_ \_ \_ nom de cluster DUP \_**
</dt> <dd> <dl> <dt>

5900 (0x170C)
</dt> <dt>



Impossible de créer un cluster avec le nom de cluster spécifié, car ce nom de cluster est déjà utilisé. Spécifiez un autre nom pour le cluster.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSCFG_ALREADY_COMMITTED"></span><span id="error_cluscfg_already_committed"></span>**ERREUR \_ CLUSCFG \_ déjà \_ validée**
</dt> <dd> <dl> <dt>

5901 (0x170D)
</dt> <dt>



L’action de configuration du cluster a déjà été validée.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSCFG_ROLLBACK_FAILED"></span><span id="error_cluscfg_rollback_failed"></span>**ERREUR \_ CLUSCFG \_ échec de la restauration \_**
</dt> <dd> <dl> <dt>

5902 (0x170E)
</dt> <dt>



Impossible de restaurer l’action de configuration du cluster.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSCFG_SYSTEM_DISK_DRIVE_LETTER_CONFLICT"></span><span id="error_cluscfg_system_disk_drive_letter_conflict"></span>**ERREUR \_ CLUSCFG \_ \_ conflit de \_ lettre de lecteur de disque système \_ \_**
</dt> <dd> <dl> <dt>

5903 (0x170F)
</dt> <dt>



La lettre de lecteur affectée à un disque système sur un nœud est en conflit avec la lettre de lecteur affectée à un disque d’un autre nœud.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_OLD_VERSION"></span><span id="error_cluster_old_version"></span>**\_ \_ version antérieure du cluster d’erreurs \_**
</dt> <dd> <dl> <dt>

5904 (0x1710)
</dt> <dt>



Un ou plusieurs nœuds du cluster exécutent une version de Windows qui ne prend pas en charge cette opération.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_MISMATCHED_COMPUTER_ACCT_NAME"></span><span id="error_cluster_mismatched_computer_acct_name"></span>**le cluster d’erreurs ne \_ \_ correspond pas au \_ nom du compte d’ordinateur \_ \_**
</dt> <dd> <dl> <dt>

5905 (0x1711)
</dt> <dt>



Le nom du compte d’ordinateur correspondant ne correspond pas au nom réseau de cette ressource.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NO_NET_ADAPTERS"></span><span id="error_cluster_no_net_adapters"></span>**ERREUR \_ de \_ cluster \_ sans \_ adaptateurs réseau**
</dt> <dd> <dl> <dt>

5906 (0x1712)
</dt> <dt>



Aucune carte réseau n’est disponible.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_POISONED"></span><span id="error_cluster_poisoned"></span>**CLUSTER d’erreurs \_ \_ incohérent**
</dt> <dd> <dl> <dt>

5907 (0x1713)
</dt> <dt>



Le nœud de cluster a été incohérent.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_GROUP_MOVING"></span><span id="error_cluster_group_moving"></span>**ERREUR \_ de \_ déplacement du groupe de clusters \_**
</dt> <dd> <dl> <dt>

5908 (0x1714)
</dt> <dt>



Le groupe n’est pas en mesure d’accepter la demande, car elle est déplacée vers un autre nœud.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_RESOURCE_TYPE_BUSY"></span><span id="error_cluster_resource_type_busy"></span>**TYPE de ressource de cluster d’erreurs \_ \_ \_ \_ occupé**
</dt> <dd> <dl> <dt>

5909 (0x1715)
</dt> <dt>



Le type de ressource ne peut pas accepter la demande, car est trop occupé à effectuer une autre opération.


</dt> </dl> </dd> <dt>

<span id="ERROR_RESOURCE_CALL_TIMED_OUT"></span><span id="error_resource_call_timed_out"></span>**expiration du délai d’attente de l' \_ appel de ressource \_ \_ \_**
</dt> <dd> <dl> <dt>

5910 (0x1716)
</dt> <dt>



L’appel à la DLL de ressource de cluster a expiré.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_CLUSTER_IPV6_ADDRESS"></span><span id="error_invalid_cluster_ipv6_address"></span>**ERREUR \_ d' \_ \_ adresse IPv6 de cluster non valide \_**
</dt> <dd> <dl> <dt>

5911 (0x1717)
</dt> <dt>



L’adresse n’est pas valide pour une ressource d’adresse IPv6. Une adresse IPv6 globale est requise et doit correspondre à un réseau de clusters. Les adresses de compatibilité ne sont pas autorisées.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_INTERNAL_INVALID_FUNCTION"></span><span id="error_cluster_internal_invalid_function"></span>**\_ \_ \_ fonction interne non valide du cluster \_ d’erreurs**
</dt> <dd> <dl> <dt>

5912 (0x1718)
</dt> <dt>



Une erreur de cluster interne s’est produite. Une tentative d’appel à une fonction non valide a été effectuée.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_PARAMETER_OUT_OF_BOUNDS"></span><span id="error_cluster_parameter_out_of_bounds"></span>**\_ \_ paramètre de cluster \_ d’erreurs hors \_ \_ limites**
</dt> <dd> <dl> <dt>

5913 (0x1719)
</dt> <dt>



Une valeur de paramètre est en dehors de la plage acceptable.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_PARTIAL_SEND"></span><span id="error_cluster_partial_send"></span>**\_ \_ envoi partiel du cluster d’erreurs \_**
</dt> <dd> <dl> <dt>

5914 (0x171A)
</dt> <dt>



Une erreur réseau s’est produite lors de l’envoi de données vers un autre nœud du cluster. Le nombre d’octets transmis était inférieur au nombre requis.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_REGISTRY_INVALID_FUNCTION"></span><span id="error_cluster_registry_invalid_function"></span>**\_ \_ \_ fonction non valide du Registre du cluster d’erreurs \_**
</dt> <dd> <dl> <dt>

5915 (0x171B)
</dt> <dt>



Une opération de registre de cluster non valide a été tentée.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_INVALID_STRING_TERMINATION"></span><span id="error_cluster_invalid_string_termination"></span>**\_fin de \_ chaîne non valide du cluster \_ d’erreurs \_**
</dt> <dd> <dl> <dt>

5916 (0x171C)
</dt> <dt>



Une chaîne d’entrée de caractères n’est pas correctement terminée.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_INVALID_STRING_FORMAT"></span><span id="error_cluster_invalid_string_format"></span>**\_format de \_ chaîne non valide du cluster \_ d’erreurs \_**
</dt> <dd> <dl> <dt>

5917 (0x171D)
</dt> <dt>



Une chaîne d’entrée de caractères n’est pas dans un format valide pour les données qu’elle représente.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_DATABASE_TRANSACTION_IN_PROGRESS"></span><span id="error_cluster_database_transaction_in_progress"></span>**ERREUR \_ de \_ transaction de base de données de cluster \_ \_ en \_ cours**
</dt> <dd> <dl> <dt>

5918 (0x171E)
</dt> <dt>



Une erreur de cluster interne s’est produite. Une transaction de base de données de cluster a été tentée alors qu’une transaction était déjà en cours.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_DATABASE_TRANSACTION_NOT_IN_PROGRESS"></span><span id="error_cluster_database_transaction_not_in_progress"></span>**ERREUR \_ \_ de transaction de base de données de cluster \_ \_ non \_ en \_ cours**
</dt> <dd> <dl> <dt>

5919 (0x171F)
</dt> <dt>



Une erreur de cluster interne s’est produite. Une tentative de validation d’une transaction de base de données de cluster a été effectuée alors qu’aucune transaction n’était en cours.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NULL_DATA"></span><span id="error_cluster_null_data"></span>**\_ \_ données null du cluster d’erreurs \_**
</dt> <dd> <dl> <dt>

5920 (0x1720)
</dt> <dt>



Une erreur de cluster interne s’est produite. Les données n’ont pas été initialisées correctement.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_PARTIAL_READ"></span><span id="error_cluster_partial_read"></span>**\_ \_ lecture partielle du cluster d’erreurs \_**
</dt> <dd> <dl> <dt>

5921 (0x1721)
</dt> <dt>



Une erreur s’est produite lors de la lecture d’un flux de données. Un nombre inattendu d’octets a été retourné.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_PARTIAL_WRITE"></span><span id="error_cluster_partial_write"></span>**\_ \_ écriture partielle du cluster d’erreurs \_**
</dt> <dd> <dl> <dt>

5922 (0x1722)
</dt> <dt>



Une erreur s’est produite lors de l’écriture dans un flux de données. Impossible d’écrire le nombre d’octets requis.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_CANT_DESERIALIZE_DATA"></span><span id="error_cluster_cant_deserialize_data"></span>**ERREUR \_ de \_ \_ désérialisation des \_ données par le cluster d’erreurs**
</dt> <dd> <dl> <dt>

5923 (0x1723)
</dt> <dt>



Une erreur s’est produite lors de la désérialisation d’un flux de données de cluster.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEPENDENT_RESOURCE_PROPERTY_CONFLICT"></span><span id="error_dependent_resource_property_conflict"></span>**\_conflit de \_ propriété de ressource dépendante d' \_ erreur \_**
</dt> <dd> <dl> <dt>

5924 (0x1724)
</dt> <dt>



Une ou plusieurs valeurs de propriété pour cette ressource sont en conflit avec une ou plusieurs valeurs de propriété associées à ses ressources dépendantes.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NO_QUORUM"></span><span id="error_cluster_no_quorum"></span>**CLUSTER d’erreurs- \_ \_ aucun \_ quorum**
</dt> <dd> <dl> <dt>

5925 (0x1725)
</dt> <dt>



Un quorum de nœuds de cluster n’était pas présent pour former un cluster.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_INVALID_IPV6_NETWORK"></span><span id="error_cluster_invalid_ipv6_network"></span>**ERREUR \_ \_ réseau IPv6 non valide du cluster \_ \_**
</dt> <dd> <dl> <dt>

5926 (0x1726)
</dt> <dt>



Le réseau de clusters n’est pas valide pour une ressource d’adresse IPv6, ou il ne correspond pas à l’adresse configurée.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_INVALID_IPV6_TUNNEL_NETWORK"></span><span id="error_cluster_invalid_ipv6_tunnel_network"></span>**Erreur \_ de \_ \_ réseau de \_ tunnel \_ IPv6 non valide pour le cluster d’erreurs**
</dt> <dd> <dl> <dt>

5927 (0x1727)
</dt> <dt>



Le réseau de clusters n’est pas valide pour une ressource de tunnel IPv6. Vérifiez la configuration de la ressource d’adresse IP dont dépend la ressource de tunnel IPv6.


</dt> </dl> </dd> <dt>

<span id="ERROR_QUORUM_NOT_ALLOWED_IN_THIS_GROUP"></span><span id="error_quorum_not_allowed_in_this_group"></span>**\_le quorum \_ d’erreur n’est pas \_ autorisé \_ dans \_ ce \_ groupe**
</dt> <dd> <dl> <dt>

5928 (0x1728)
</dt> <dt>



La ressource de quorum ne peut pas résider dans le groupe de stockage disponible.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEPENDENCY_TREE_TOO_COMPLEX"></span><span id="error_dependency_tree_too_complex"></span>**\_arborescence de dépendances d’erreur \_ \_ trop \_ complexe**
</dt> <dd> <dl> <dt>

5929 (0x1729)
</dt> <dt>



Les dépendances de cette ressource sont imbriquées trop profondément.


</dt> </dl> </dd> <dt>

<span id="ERROR_EXCEPTION_IN_RESOURCE_CALL"></span><span id="error_exception_in_resource_call"></span>**\_exception \_ d’erreur dans l’appel de \_ ressource \_**
</dt> <dd> <dl> <dt>

5930 (0x172A)
</dt> <dt>



L’appel dans la DLL de ressource a levé une exception non gérée.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_RHS_FAILED_INITIALIZATION"></span><span id="error_cluster_rhs_failed_initialization"></span>**\_ \_ \_ échec \_ d’initialisation du RHS du cluster d’erreurs**
</dt> <dd> <dl> <dt>

5931 (0x172B)
</dt> <dt>



Échec de l’initialisation du processus RHS.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NOT_INSTALLED"></span><span id="error_cluster_not_installed"></span>**le \_ cluster d’erreurs \_ n’est pas \_ installé**
</dt> <dd> <dl> <dt>

5932 (0x172C)
</dt> <dt>



La fonctionnalité de clustering de basculement n’est pas installée sur ce nœud.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_RESOURCES_MUST_BE_ONLINE_ON_THE_SAME_NODE"></span><span id="error_cluster_resources_must_be_online_on_the_same_node"></span>**\_ \_ \_ les ressources de cluster d’erreurs doivent \_ être \_ en ligne \_ sur \_ le \_ même \_ nœud**
</dt> <dd> <dl> <dt>

5933 (0x172D)
</dt> <dt>



Les ressources doivent être en ligne sur le même nœud pour cette opération.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_MAX_NODES_IN_CLUSTER"></span><span id="error_cluster_max_nodes_in_cluster"></span>**\_ \_ nombre maximal \_ de nœuds \_ de cluster d’erreurs dans le \_ cluster**
</dt> <dd> <dl> <dt>

5934 (0x172E)
</dt> <dt>



Impossible d’ajouter un nouveau nœud, car ce cluster a déjà un nombre maximal de nœuds.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_TOO_MANY_NODES"></span><span id="error_cluster_too_many_nodes"></span>**ERREURS \_ de \_ \_ nœud trop nombreux \_ dans le cluster**
</dt> <dd> <dl> <dt>

5935 (0x172F)
</dt> <dt>



Ce cluster ne peut pas être créé, car le nombre de nœuds spécifié dépasse la limite maximale autorisée.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_OBJECT_ALREADY_USED"></span><span id="error_cluster_object_already_used"></span>**objet de cluster d’erreurs \_ \_ \_ déjà \_ utilisé**
</dt> <dd> <dl> <dt>

5936 (0x1730)
</dt> <dt>



Une tentative d’utilisation du nom de cluster spécifié a échoué, car un objet ordinateur activé portant le même nom existe déjà dans le domaine.


</dt> </dl> </dd> <dt>

<span id="ERROR_NONCORE_GROUPS_FOUND"></span><span id="error_noncore_groups_found"></span>**ERREUR de \_ \_ groupes principaux \_ introuvables**
</dt> <dd> <dl> <dt>

5937 (0x1731)
</dt> <dt>



Ce cluster ne peut pas être détruit. Il possède des groupes d’applications non centraux qui doivent être supprimés avant que le cluster puisse être détruit.


</dt> </dl> </dd> <dt>

<span id="ERROR_FILE_SHARE_RESOURCE_CONFLICT"></span><span id="error_file_share_resource_conflict"></span>**ERREUR \_ de \_ \_ conflit de ressources de partage de fichiers \_**
</dt> <dd> <dl> <dt>

5938 (0x1732)
</dt> <dt>



Le partage de fichiers associé à la ressource témoin de partage de fichiers ne peut pas être hébergé par ce cluster ou l’un de ses nœuds.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_EVICT_INVALID_REQUEST"></span><span id="error_cluster_evict_invalid_request"></span>**\_Suppression de \_ la \_ demande non valide du cluster d’erreurs \_**
</dt> <dd> <dl> <dt>

5939 (0x1733)
</dt> <dt>



L’éviction de ce nœud n’est pas valide pour l’instant. En raison de l’éviction du nœud exigences de quorum, l’arrêt du cluster se produit. S’il s’agit du dernier nœud dans le cluster, la commande destroy cluster doit être utilisée.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_SINGLETON_RESOURCE"></span><span id="error_cluster_singleton_resource"></span>**\_ \_ ressource singleton du cluster d’erreurs \_**
</dt> <dd> <dl> <dt>

5940 (0x1734)
</dt> <dt>



Une seule instance de ce type de ressource est autorisée dans le cluster.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_GROUP_SINGLETON_RESOURCE"></span><span id="error_cluster_group_singleton_resource"></span>**\_ \_ ressource singleton du groupe de clusters d’erreurs \_ \_**
</dt> <dd> <dl> <dt>

5941 (0x1735)
</dt> <dt>



Une seule instance de ce type de ressource est autorisée par groupe de ressources.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_RESOURCE_PROVIDER_FAILED"></span><span id="error_cluster_resource_provider_failed"></span>**ERREUR lors de l' \_ échec du fournisseur de ressources de cluster \_ \_ \_**
</dt> <dd> <dl> <dt>

5942 (0x1736)
</dt> <dt>



La ressource n’a pas pu être mise en ligne en raison de l’échec d’une ou de plusieurs ressources du fournisseur.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_RESOURCE_CONFIGURATION_ERROR"></span><span id="error_cluster_resource_configuration_error"></span>**erreur de configuration de la \_ ressource de cluster erreur \_ \_ \_**
</dt> <dd> <dl> <dt>

5943 (0x1737)
</dt> <dt>



La ressource a indiqué qu’elle ne peut pas être mise en ligne sur un nœud.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_GROUP_BUSY"></span><span id="error_cluster_group_busy"></span>**ERREUR du \_ groupe de clusters \_ \_ occupé**
</dt> <dd> <dl> <dt>

5944 (0x1738)
</dt> <dt>



L’opération en cours ne peut pas être effectuée sur ce groupe pour l’instant.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NOT_SHARED_VOLUME"></span><span id="error_cluster_not_shared_volume"></span>**\_ \_ \_ volume non partagé \_ du cluster d’erreurs**
</dt> <dd> <dl> <dt>

5945 (0x1739)
</dt> <dt>



Le répertoire ou le fichier ne se trouve pas sur un volume partagé de cluster.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_INVALID_SECURITY_DESCRIPTOR"></span><span id="error_cluster_invalid_security_descriptor"></span>**descripteur de sécurité de cluster d’erreurs \_ \_ non valide \_ \_**
</dt> <dd> <dl> <dt>

5946 (0x173A)
</dt> <dt>



Le descripteur de sécurité ne remplit pas les conditions requises pour un cluster.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_SHARED_VOLUMES_IN_USE"></span><span id="error_cluster_shared_volumes_in_use"></span>**\_ \_ \_ volumes partagés de cluster \_ d’erreurs en cours d' \_ utilisation**
</dt> <dd> <dl> <dt>

5947 (0x173B)
</dt> <dt>



Une ou plusieurs ressources de volumes partagés sont configurées dans le cluster. Ces ressources doivent être déplacées vers le stockage disponible pour que l’opération aboutisse.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_USE_SHARED_VOLUMES_API"></span><span id="error_cluster_use_shared_volumes_api"></span>**\_ \_ API utiliser des \_ \_ volumes partagés \_ de cluster d’erreurs**
</dt> <dd> <dl> <dt>

5948 (0x173C)
</dt> <dt>



Ce groupe ou cette ressource ne peut pas être manipulé directement. Utilisez des API de volume partagé pour effectuer l’opération souhaitée.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_BACKUP_IN_PROGRESS"></span><span id="error_cluster_backup_in_progress"></span>**ERREUR \_ \_ de sauvegarde \_ du cluster en \_ cours**
</dt> <dd> <dl> <dt>

5949 (0x173D)
</dt> <dt>



La sauvegarde est en cours. Veuillez attendre la fin de la sauvegarde avant de recommencer l’opération.


</dt> </dl> </dd> <dt>

<span id="ERROR_NON_CSV_PATH"></span><span id="error_non_csv_path"></span>**ERREUR \_ non \_ CSV \_ path**
</dt> <dd> <dl> <dt>

5950 (0x173E)
</dt> <dt>



Le chemin d’accès n’appartient pas à un volume partagé de cluster.


</dt> </dl> </dd> <dt>

<span id="ERROR_CSV_VOLUME_NOT_LOCAL"></span><span id="error_csv_volume_not_local"></span>**ERREUR \_ \_ volume CSV \_ non \_ local**
</dt> <dd> <dl> <dt>

5951 (0x173F)
</dt> <dt>



Le volume partagé de cluster n’est pas monté localement sur ce nœud.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_WATCHDOG_TERMINATING"></span><span id="error_cluster_watchdog_terminating"></span>**arrêt de la surveillance du cluster d’erreurs \_ \_ \_**
</dt> <dd> <dl> <dt>

5952 (0x1740)
</dt> <dt>



La surveillance du cluster se termine.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_RESOURCE_VETOED_MOVE_INCOMPATIBLE_NODES"></span><span id="error_cluster_resource_vetoed_move_incompatible_nodes"></span>**ERREUR de \_ ressource de cluster ayant refusé le déplacement des \_ \_ \_ \_ nœuds incompatibles \_**
</dt> <dd> <dl> <dt>

5953 (0x1741)
</dt> <dt>



Une ressource a refusé un déplacement entre deux nœuds, car ils sont incompatibles.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_INVALID_NODE_WEIGHT"></span><span id="error_cluster_invalid_node_weight"></span>**poids du nœud de cluster d’erreurs \_ \_ non valide \_ \_**
</dt> <dd> <dl> <dt>

5954 (0x1742)
</dt> <dt>



La demande n’est pas valide, car la pondération du nœud ne peut pas être modifiée tant que le cluster est en mode de quorum disque uniquement, ou parce que la modification du poids du nœud ne respecte pas les exigences minimales de quorum de cluster.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_RESOURCE_VETOED_CALL"></span><span id="error_cluster_resource_vetoed_call"></span>**ERREUR \_ d' \_ \_ \_ appel refusé de la ressource de cluster**
</dt> <dd> <dl> <dt>

5955 (0x1743)
</dt> <dt>



La ressource a refusé l’appel.


</dt> </dl> </dd> <dt>

<span id="ERROR_RESMON_SYSTEM_RESOURCES_LACKING"></span><span id="error_resmon_system_resources_lacking"></span>**ERREUR \_ RESMON \_ \_ ressources système \_ manquantes**
</dt> <dd> <dl> <dt>

5956 (0x1744)
</dt> <dt>



La ressource n’a pas pu démarrer ou s’exécuter car elle n’a pas pu réserver suffisamment de ressources système.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_RESOURCE_VETOED_MOVE_NOT_ENOUGH_RESOURCES_ON_DESTINATION"></span><span id="error_cluster_resource_vetoed_move_not_enough_resources_on_destination"></span>**erreur \_ \_ \_ de refus de la ressource \_ de cluster d’erreurs déplacer les \_ \_ \_ ressources sur la \_ \_ destination**
</dt> <dd> <dl> <dt>

5957 (0x1745)
</dt> <dt>



Une ressource a refusé un déplacement entre deux nœuds, car la destination ne dispose pas actuellement de ressources suffisantes pour terminer l’opération.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_RESOURCE_VETOED_MOVE_NOT_ENOUGH_RESOURCES_ON_SOURCE"></span><span id="error_cluster_resource_vetoed_move_not_enough_resources_on_source"></span>**ERREUR \_ \_ \_ de refus de ressource \_ \_ de cluster \_ insuffisante déplacer les \_ ressources \_ sur la \_ source**
</dt> <dd> <dl> <dt>

5958 (0x1746)
</dt> <dt>



Une ressource a refusé un déplacement entre deux nœuds, car la source ne dispose pas actuellement de ressources suffisantes pour terminer l’opération.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_GROUP_QUEUED"></span><span id="error_cluster_group_queued"></span>**\_groupe de clusters d’erreurs en \_ \_ file d’attente**
</dt> <dd> <dl> <dt>

5959 (0x1747)
</dt> <dt>



L’opération demandée ne peut pas être effectuée, car le groupe est mis en file d’attente pour une opération.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_RESOURCE_LOCKED_STATUS"></span><span id="error_cluster_resource_locked_status"></span>**État du verrouillage de la \_ ressource de cluster d’erreurs \_ \_ \_**
</dt> <dd> <dl> <dt>

5960 (0x1748)
</dt> <dt>



L’opération demandée ne peut pas être effectuée, car une ressource a l’état verrouillé.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_SHARED_VOLUME_FAILOVER_NOT_ALLOWED"></span><span id="error_cluster_shared_volume_failover_not_allowed"></span>**\_basculement du volume partagé de cluster d’erreurs \_ \_ \_ \_ non \_ autorisé**
</dt> <dd> <dl> <dt>

5961 (0x1749)
</dt> <dt>



La ressource ne peut pas être déplacée vers un autre nœud, car un volume partagé de cluster a refusé l’opération.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NODE_DRAIN_IN_PROGRESS"></span><span id="error_cluster_node_drain_in_progress"></span>**ERREUR \_ \_ \_ \_ de drainage du nœud de cluster en \_ cours**
</dt> <dd> <dl> <dt>

5962 (0x174A)
</dt> <dt>



Une vidange de nœud est déjà en cours.

Cette valeur était également nommée **\_ \_ \_ évacuation des nœuds de cluster d’erreur \_ en \_ cours**


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_DISK_NOT_CONNECTED"></span><span id="error_cluster_disk_not_connected"></span>**ERREUR \_ disque de cluster \_ \_ non \_ connecté**
</dt> <dd> <dl> <dt>

5963 (0x174B)
</dt> <dt>



Le stockage en cluster n’est pas connecté au nœud.


</dt> </dl> </dd> <dt>

<span id="ERROR_DISK_NOT_CSV_CAPABLE"></span><span id="error_disk_not_csv_capable"></span>**ERREUR \_ disque \_ non \_ CSV \_**
</dt> <dd> <dl> <dt>

5964 (0x174C)
</dt> <dt>



Le disque n’est pas configuré de manière à être utilisé avec des volumes partagés de cluster. Les disques CSV doivent avoir au moins une partition formatée avec NTFS.


</dt> </dl> </dd> <dt>

<span id="ERROR_RESOURCE_NOT_IN_AVAILABLE_STORAGE"></span><span id="error_resource_not_in_available_storage"></span>**la \_ ressource \_ d’erreur n’est pas \_ dans le \_ \_ stockage disponible**
</dt> <dd> <dl> <dt>

5965 (0x174D)
</dt> <dt>



La ressource doit faire partie du groupe de stockage disponible pour effectuer cette action.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_SHARED_VOLUME_REDIRECTED"></span><span id="error_cluster_shared_volume_redirected"></span>**ERREUR \_ de \_ \_ redirection du volume partagé de cluster \_**
</dt> <dd> <dl> <dt>

5966 (0x174E)
</dt> <dt>



Échec de l’opération CSVFS car le volume est en mode Redirigé.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_SHARED_VOLUME_NOT_REDIRECTED"></span><span id="error_cluster_shared_volume_not_redirected"></span>**\_volume partagé de cluster d’erreurs \_ \_ \_ non \_ Redirigé**
</dt> <dd> <dl> <dt>

5967 (0x174F)
</dt> <dt>



Échec de l’opération CSVFS car le volume n’est pas en mode Redirigé.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_CANNOT_RETURN_PROPERTIES"></span><span id="error_cluster_cannot_return_properties"></span>**le \_ cluster d’erreurs \_ ne peut pas \_ retourner les \_ Propriétés**
</dt> <dd> <dl> <dt>

5968 (0x1750)
</dt> <dt>



Les propriétés du cluster ne peuvent pas être retournées pour l’instant.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_RESOURCE_CONTAINS_UNSUPPORTED_DIFF_AREA_FOR_SHARED_VOLUMES"></span><span id="error_cluster_resource_contains_unsupported_diff_area_for_shared_volumes"></span>**ERREUR \_ la \_ ressource \_ de cluster contient une \_ zone diff non prise en charge \_ \_ \_ pour les \_ \_ volumes partagés**
</dt> <dd> <dl> <dt>

5969 (0x1751)
</dt> <dt>



La ressource de disque en cluster contient une zone diff de capture instantanée logicielle qui n’est pas prise en charge pour les volumes partagés de cluster.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_RESOURCE_IS_IN_MAINTENANCE_MODE"></span><span id="error_cluster_resource_is_in_maintenance_mode"></span>**la \_ \_ ressource \_ de cluster d’erreurs est \_ en \_ \_ mode maintenance**
</dt> <dd> <dl> <dt>

5970 (0x1752)
</dt> <dt>



Impossible d’effectuer l’opération, car la ressource est en mode maintenance.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_AFFINITY_CONFLICT"></span><span id="error_cluster_affinity_conflict"></span>**ERREUR \_ de \_ conflit d’affinités de cluster \_**
</dt> <dd> <dl> <dt>

5971 (0x1753)
</dt> <dt>



Impossible d’effectuer l’opération en raison de conflits d’affinité de cluster.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_RESOURCE_IS_REPLICA_VIRTUAL_MACHINE"></span><span id="error_cluster_resource_is_replica_virtual_machine"></span>**ERREUR \_ \_ la ressource de cluster \_ est une \_ \_ machine virtuelle de réplication \_**
</dt> <dd> <dl> <dt>

5972 (0x1754)
</dt> <dt>



Impossible d’effectuer l’opération, car la ressource est un ordinateur virtuel de réplication.


</dt> </dl> </dd> </dl>


## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows XP uniquement\]<br/>                                           |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>WinError. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Codes d’erreur système](system-error-codes.md)
</dt> </dl>

 

 




