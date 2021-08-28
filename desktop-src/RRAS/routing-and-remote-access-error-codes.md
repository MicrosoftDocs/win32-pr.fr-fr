---
title: Codes d’erreur de routage et d’accès distant
description: Les codes d’erreur de l’API de routage et d’accès à distance (RRAS) suivants sont définis dans raserror. h.
ms.assetid: 1fa41438-7c93-4e9c-851c-652fba23da4f
topic_type:
- apiref
api_name:
- Routing and Remote Access Error Codes
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7bd68c31ef2b92cce75059d5d86ee68dc65d1151
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2021
ms.locfileid: "122624325"
---
# <a name="routing-and-remote-access-error-codes"></a>Codes d’erreur de routage et d’accès distant

Les codes d’erreur de l’API de routage et d’accès à distance (RRAS) suivants sont définis dans raserror. h. tous les codes d’erreur sont pris en charge dans Windows 2000 ou les versions ultérieures de Windows, sauf indication contraire.



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Code/valeur de retour</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="PENDING"></span><span id="pending"></span><dl> <dt><strong>En attente</strong></dt> <dt>600</dt> </dl></td>
<td>Une opération est en attente.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_INVALID_PORT_HANDLE"></span><span id="error_invalid_port_handle"></span><dl> <dt><strong>ERROR_INVALID_PORT_HANDLE</strong></dt> <dt>601</dt> </dl></td>
<td>Le descripteur de port fourni n’est pas valide.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_PORT_ALREADY_OPEN"></span><span id="error_port_already_open"></span><dl> <dt><strong>ERROR_PORT_ALREADY_OPEN</strong></dt> <dt>602</dt> </dl></td>
<td>Le port spécifié est déjà ouvert.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_BUFFER_TOO_SMALL"></span><span id="error_buffer_too_small"></span><dl> <dt><strong>ERROR_BUFFER_TOO_SMALL</strong></dt> <dt>603</dt> </dl></td>
<td>La mémoire tampon fournie est trop petite.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_WRONG_INFO_SPECIFIED"></span><span id="error_wrong_info_specified"></span><dl> <dt><strong>ERROR_WRONG_INFO_SPECIFIED</strong></dt> <dt>604</dt> </dl></td>
<td>Les informations de port spécifiées sont incorrectes.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_CANNOT_SET_PORT_INFO"></span><span id="error_cannot_set_port_info"></span><dl> <dt><strong>ERROR_CANNOT_SET_PORT_INFO</strong></dt> <dt>605</dt> </dl></td>
<td>Impossible de définir les informations de port spécifiées.<br/>
<blockquote>
[!Note]<br />
déconseillé dans Windows Vista et les versions ultérieures de Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_PORT_NOT_CONNECTED"></span><span id="error_port_not_connected"></span><dl> <dt><strong>ERROR_PORT_NOT_CONNECTED</strong></dt> <dt>606</dt> </dl></td>
<td>Le port spécifié n’est pas connecté.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_EVENT_INVALID"></span><span id="error_event_invalid"></span><dl> <dt><strong>ERROR_EVENT_INVALID</strong></dt> <dt>607</dt> </dl></td>
<td>Un événement qui n’est pas valide a été détecté.<br/>
<blockquote>
[!Note]<br />
déconseillé dans Windows Vista et les versions ultérieures de Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_DEVICE_DOES_NOT_EXIST"></span><span id="error_device_does_not_exist"></span><dl> <dt><strong>ERROR_DEVICE_DOES_NOT_EXIST</strong></dt> <dt>608</dt> </dl></td>
<td>L’appareil spécifié n’existe pas.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_DEVICETYPE_DOES_NOT_EXIST"></span><span id="error_devicetype_does_not_exist"></span><dl> <dt><strong>ERROR_DEVICETYPE_DOES_NOT_EXIST</strong></dt> <dt>609</dt> </dl></td>
<td>Le type d’appareil spécifié n’existe pas.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_BUFFER_INVALID"></span><span id="error_buffer_invalid"></span><dl> <dt><strong>ERROR_BUFFER_INVALID</strong></dt> <dt>610</dt> </dl></td>
<td>La mémoire tampon fournie n’est pas valide.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_ROUTE_NOT_AVAILABLE"></span><span id="error_route_not_available"></span><dl> <dt><strong>ERROR_ROUTE_NOT_AVAILABLE</strong></dt> <dt>611</dt> </dl></td>
<td>Un itinéraire spécifié n’est pas disponible.<br/>
<blockquote>
[!Note]<br />
déconseillé dans Windows Vista et les versions ultérieures de Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_ROUTE_NOT_ALLOCATED"></span><span id="error_route_not_allocated"></span><dl> <dt><strong>ERROR_ROUTE_NOT_ALLOCATED</strong></dt> <dt>612</dt> </dl></td>
<td>L’itinéraire spécifié n’est pas alloué.<br/></td>
</tr>
<tr class="even">
<td><span id="ERRERROR_INVALID_COMPRESSION_SPECIFIED"></span><span id="errerror_invalid_compression_specified"></span><dl> <dt><strong>ERRERROR_INVALID_COMPRESSION_SPECIFIED</strong></dt> <dt>613</dt> </dl></td>
<td>La compression spécifiée n’est pas valide.<br/>
<blockquote>
[!Note]<br />
déconseillé dans Windows Vista et les versions ultérieures de Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_OUT_OF_BUFFERS"></span><span id="error_out_of_buffers"></span><dl> <dt><strong>ERROR_OUT_OF_BUFFERS</strong></dt> <dt>614</dt> </dl></td>
<td>Les mémoires tampons sont insuffisantes.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_PORT_NOT_FOUND_"></span><span id="error_port_not_found_"></span><dl> <dt> <strong>ERROR_PORT_NOT_FOUND</strong> </dt> <dt>615</dt> </dl></td>
<td>Le port spécifié est introuvable.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_ASYNC_REQUEST_PENDING"></span><span id="error_async_request_pending"></span><dl> <dt><strong>ERROR_ASYNC_REQUEST_PENDING</strong></dt> <dt>616</dt> </dl></td>
<td>Une demande asynchrone est en attente.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_ALREADY_DISCONNECTING"></span><span id="error_already_disconnecting"></span><dl> <dt><strong>ERROR_ALREADY_DISCONNECTING</strong></dt> <dt>617</dt> </dl></td>
<td>Le port ou l’appareil spécifié est déjà en cours de déconnexion.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_PORT_NOT_OPEN"></span><span id="error_port_not_open"></span><dl> <dt><strong>ERROR_PORT_NOT_OPEN</strong></dt> <dt>618</dt> </dl></td>
<td>Le port spécifié n'est pas ouvert.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_PORT_DISCONNECTED"></span><span id="error_port_disconnected"></span><dl> <dt><strong>ERROR_PORT_DISCONNECTED</strong></dt> <dt>619</dt> </dl></td>
<td>Le port spécifié est déconnecté.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_NO_ENDPOINTS"></span><span id="error_no_endpoints"></span><dl> <dt><strong>ERROR_NO_ENDPOINTS</strong></dt> <dt>620</dt> </dl></td>
<td>Aucun point de terminaison n’a pu être déterminé.<br/>
<blockquote>
[!Note]<br />
déconseillé dans Windows Vista et les versions ultérieures de Windows.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_CANNOT_OPEN_PHONEBOOK"></span><span id="error_cannot_open_phonebook"></span><dl> <dt><strong>ERROR_CANNOT_OPEN_PHONEBOOK</strong></dt> <dt>621</dt> </dl></td>
<td>Impossible d’ouvrir le fichier de l’annuaire téléphonique spécifié.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_CANNOT_LOAD_PHONEBOOK"></span><span id="error_cannot_load_phonebook"></span><dl> <dt><strong>ERROR_CANNOT_LOAD_PHONEBOOK</strong></dt> <dt>622</dt> </dl></td>
<td>Impossible de charger le fichier d’annuaire téléphonique spécifié.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_CANNOT_FIND_PHONEBOOK_ENTRY"></span><span id="error_cannot_find_phonebook_entry"></span><dl> <dt><strong>ERROR_CANNOT_FIND_PHONEBOOK_ENTRY</strong></dt> <dt>623</dt> </dl></td>
<td>Impossible de trouver l’entrée de l’annuaire téléphonique spécifiée.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_CANNOT_WRITE_PHONEBOOK"></span><span id="error_cannot_write_phonebook"></span><dl> <dt><strong>ERROR_CANNOT_WRITE_PHONEBOOK</strong></dt> <dt>624</dt> </dl></td>
<td>Impossible d’écrire dans le fichier de l’annuaire téléphonique spécifié.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_CORRUPT_PHONEBOOK"></span><span id="error_corrupt_phonebook"></span><dl> <dt><strong>ERROR_CORRUPT_PHONEBOOK</strong></dt> <dt>625</dt> </dl></td>
<td>Les informations trouvées dans l’annuaire téléphonique spécifié ne sont pas valides.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_CANNOT_LOAD_STRING"></span><span id="error_cannot_load_string"></span><dl> <dt><strong>ERROR_CANNOT_LOAD_STRING</strong></dt> <dt>626</dt> </dl></td>
<td>Une chaîne n’a pas pu être chargée.<br/>
<blockquote>
[!Note]<br />
déconseillé dans Windows Vista et les versions ultérieures de Windows.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_KEY_NOT_FOUND"></span><span id="error_key_not_found"></span><dl> <dt><strong>ERROR_KEY_NOT_FOUND</strong></dt> <dt>627</dt> </dl></td>
<td>Impossible de trouver la clé spécifiée.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_DISCONNECTION"></span><span id="error_disconnection"></span><dl> <dt><strong>ERROR_DISCONNECTION</strong></dt> <dt>628</dt> </dl></td>
<td>Le port spécifié a été déconnecté.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_REMOTE_DISCONNECTION"></span><span id="error_remote_disconnection"></span><dl> <dt><strong>ERROR_REMOTE_DISCONNECTION</strong></dt> <dt>629</dt> </dl></td>
<td>Le port spécifié a été déconnecté par l’ordinateur distant.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_HARDWARE_FAILURE"></span><span id="error_hardware_failure"></span><dl> <dt><strong>ERROR_HARDWARE_FAILURE</strong></dt> <dt>630</dt> </dl></td>
<td>Le port spécifié a été déconnecté en raison d’une défaillance matérielle.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_USER_DISCONNECTION"></span><span id="error_user_disconnection"></span><dl> <dt><strong>ERROR_USER_DISCONNECTION</strong></dt> <dt>631</dt> </dl></td>
<td>Le port spécifié a été déconnecté par l’utilisateur.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_INVALID_SIZE"></span><span id="error_invalid_size"></span><dl> <dt><strong>ERROR_INVALID_SIZE</strong></dt> <dt>632</dt> </dl></td>
<td>Taille de structure incorrecte.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_PORT_NOT_AVAILABLE"></span><span id="error_port_not_available"></span><dl> <dt><strong>ERROR_PORT_NOT_AVAILABLE</strong></dt> <dt>633</dt> </dl></td>
<td>Le port spécifié est déjà utilisé ou n’est pas configuré pour la connexion d’accès à distance.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_CANNOT_PROJECT_CLIENT"></span><span id="error_cannot_project_client"></span><dl> <dt><strong>ERROR_CANNOT_PROJECT_CLIENT</strong></dt> <dt>634</dt> </dl></td>
<td>Votre ordinateur n’a pas pu être enregistré sur le réseau distant.<br/>
<blockquote>
[!Note]<br />
déconseillé dans Windows Vista et les versions ultérieures de Windows.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_UNKNOWN"></span><span id="error_unknown"></span><dl> <dt><strong>ERROR_UNKNOWN</strong></dt> <dt>635</dt> </dl></td>
<td>Une erreur inconnue s’est produite.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_WRONG_DEVICE_ATTACHED"></span><span id="error_wrong_device_attached"></span><dl> <dt><strong>ERROR_WRONG_DEVICE_ATTACHED</strong></dt> <dt>636</dt> </dl></td>
<td>Le mauvais appareil est attaché au port spécifié.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_BAD_STRING"></span><span id="error_bad_string"></span><dl> <dt><strong>ERROR_BAD_STRING</strong></dt> <dt>637</dt> </dl></td>
<td>Une chaîne qui n’a pas pu être convertie a été détectée.<br/>
<blockquote>
[!Note]<br />
déconseillé dans Windows Vista et les versions ultérieures de Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_REQUEST_TIMEOUT"></span><span id="error_request_timeout"></span><dl> <dt><strong>ERROR_REQUEST_TIMEOUT</strong></dt> <dt>638</dt> </dl></td>
<td>Le délai d'attente de la requête a expiré.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_CANNOT_GET_LANA"></span><span id="error_cannot_get_lana"></span><dl> <dt><strong>ERROR_CANNOT_GET_LANA</strong></dt> <dt>639</dt> </dl></td>
<td>Aucun réseau asynchrone n’est disponible.<br/>
<blockquote>
[!Note]<br />
déconseillé dans Windows Vista et les versions ultérieures de Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_NETBIOS_ERROR"></span><span id="error_netbios_error"></span><dl> <dt><strong>ERROR_NETBIOS_ERROR</strong></dt> <dt>640</dt> </dl></td>
<td>Une erreur s’est produite lors de l’appel de NetBIOS.<br/>
<blockquote>
[!Note]<br />
déconseillé dans Windows Vista et les versions ultérieures de Windows.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_SERVER_OUT_OF_RESOURCES"></span><span id="error_server_out_of_resources"></span><dl> <dt><strong>ERROR_SERVER_OUT_OF_RESOURCES</strong></dt> <dt>641</dt> </dl></td>
<td>le serveur ne peut pas allouer les ressources NetBIOS nécessaires à la prise en charge du client.<br/>
<blockquote>
[!Note]<br />
déconseillé dans Windows Vista et les versions ultérieures de Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_NAME_EXISTS_ON_NET"></span><span id="error_name_exists_on_net"></span><dl> <dt><strong>ERROR_NAME_EXISTS_ON_NET</strong></dt> <dt>642</dt> </dl></td>
<td>L’un des noms NetBIOS de votre ordinateur est déjà inscrit sur le réseau distant.<br/>
<blockquote>
[!Note]<br />
déconseillé dans Windows Vista et les versions ultérieures de Windows.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_SERVER_GENERAL_NET_FAILURE"></span><span id="error_server_general_net_failure"></span><dl> <dt><strong>ERROR_SERVER_GENERAL_NET_FAILURE</strong></dt> <dt>643</dt> </dl></td>
<td>Échec d’une carte réseau sur le serveur.<br/>
<blockquote>
[!Note]<br />
déconseillé dans Windows Vista et les versions ultérieures de Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="WARNING_MSG_ALIAS_NOT_ADDED"></span><span id="warning_msg_alias_not_added"></span><dl> <dt><strong>WARNING_MSG_ALIAS_NOT_ADDED</strong></dt> <dt>644</dt> </dl></td>
<td>Vous ne recevrez pas de message sur le réseau.<br/>
<blockquote>
[!Note]<br />
déconseillé dans Windows Vista et les versions ultérieures de Windows.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_AUTH_INTERNAL"></span><span id="error_auth_internal"></span><dl> <dt><strong>ERROR_AUTH_INTERNAL</strong></dt> <dt>645</dt> </dl></td>
<td>Une erreur d’authentification interne s’est produite.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_RESTRICTED_LOGON_HOURS"></span><span id="error_restricted_logon_hours"></span><dl> <dt><strong>ERROR_RESTRICTED_LOGON_HOURS</strong></dt> <dt>646</dt> </dl></td>
<td>Le compte spécifié n’est pas autorisé à se connecter à cette heure de la journée.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_ACCT_DISABLED"></span><span id="error_acct_disabled"></span><dl> <dt><strong>ERROR_ACCT_DISABLED</strong></dt> <dt>647</dt> </dl></td>
<td>Le compte spécifié est désactivé.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_PASSWD_EXPIRED"></span><span id="error_passwd_expired"></span><dl> <dt><strong>ERROR_PASSWD_EXPIRED</strong></dt> <dt>648</dt> </dl></td>
<td>Le mot de passe spécifié a expiré.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_NO_DIALIN_PERMISSION"></span><span id="error_no_dialin_permission"></span><dl> <dt><strong>ERROR_NO_DIALIN_PERMISSION</strong></dt> <dt>649</dt> </dl></td>
<td>Le compte spécifié ne dispose pas des autorisations d’accès à distance.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_SERVER_NOT_RESPONDING"></span><span id="error_server_not_responding"></span><dl> <dt><strong>ERROR_SERVER_NOT_RESPONDING</strong></dt> <dt>650</dt> </dl></td>
<td>Le serveur d’accès à distance ne répond pas.<br/>
<blockquote>
[!Note]<br />
déconseillé dans Windows Vista et les versions ultérieures de Windows.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_FROM_DEVICE"></span><span id="error_from_device"></span><dl> <dt><strong>ERROR_FROM_DEVICE</strong></dt> <dt>651</dt> </dl></td>
<td>Votre modem ou autre périphérique de connexion a signalé une erreur.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_UNRECOGNIZED_RESPONSE"></span><span id="error_unrecognized_response"></span><dl> <dt><strong>ERROR_UNRECOGNIZED_RESPONSE</strong></dt> <dt>652</dt> </dl></td>
<td>Une réponse non reconnue a été retournée par l’appareil.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_MACRO_NOT_FOUND"></span><span id="error_macro_not_found"></span><dl> <dt><strong>ERROR_MACRO_NOT_FOUND</strong></dt> <dt>653</dt> </dl></td>
<td>Une macro requise par l’appareil est introuvable dans l’appareil. Section du fichier INF.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_MACRO_NOT_DEFINED"></span><span id="error_macro_not_defined"></span><dl> <dt><strong>ERROR_MACRO_NOT_DEFINED</strong></dt> <dt>654</dt> </dl></td>
<td>Commande ou réponse dans l’appareil. La section du fichier INF fait référence à une macro non définie.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_MESSAGE_MACRO_NOT_FOUND"></span><span id="error_message_macro_not_found"></span><dl> <dt><strong>ERROR_MESSAGE_MACRO_NOT_FOUND</strong></dt> <dt>655</dt> </dl></td>
<td>La <message> macro est introuvable dans l’appareil. Section du fichier INF.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_DEFAULTOFF_MACRO_NOT_FOUND"></span><span id="error_defaultoff_macro_not_found"></span><dl> <dt><strong>ERROR_DEFAULTOFF_MACRO_NOT_FOUND</strong></dt> <dt>656</dt> </dl></td>
<td><defaultoff>Macro dans l’appareil. La section du fichier INF contient une macro non définie.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_FILE_COULD_NOT_BE_OPENED"></span><span id="error_file_could_not_be_opened"></span><dl> <dt><strong>ERROR_FILE_COULD_NOT_BE_OPENED</strong></dt> <dt>657</dt> </dl></td>
<td>L’appareil. Impossible d’ouvrir le fichier INF.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_DEVICENAME_TOO_LONG"></span><span id="error_devicename_too_long"></span><dl> <dt><strong>ERROR_DEVICENAME_TOO_LONG</strong></dt> <dt>658</dt> </dl></td>
<td>Nom de l’appareil dans l’appareil. Le fichier INF ou .INI du média est trop long. <br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_DEVICENAME_NOT_FOUND"></span><span id="error_devicename_not_found"></span><dl> <dt><strong>ERROR_DEVICENAME_NOT_FOUND</strong></dt> <dt>659</dt> </dl></td>
<td>Le fichier de .INI de média fait référence à un nom de périphérique inconnu.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_NO_RESPONSES"></span><span id="error_no_responses"></span><dl> <dt><strong>ERROR_NO_RESPONSES</strong></dt> <dt>660</dt> </dl></td>
<td>L’appareil. Le fichier INF ne contient aucune réponse pour la commande.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_NO_COMMAND_FOUND"></span><span id="error_no_command_found"></span><dl> <dt><strong>ERROR_NO_COMMAND_FOUND</strong></dt> <dt>661</dt> </dl></td>
<td>L’appareil. Une commande est manquante dans le fichier INF.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_WRONG_KEY_SPECIFIED"></span><span id="error_wrong_key_specified"></span><dl> <dt><strong>ERROR_WRONG_KEY_SPECIFIED</strong></dt> <dt>662</dt> </dl></td>
<td>Tentative de définition d’une macro non listée dans le périphérique. Section du fichier INF.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_UNKNOWN_DEVICE_TYPE"></span><span id="error_unknown_device_type"></span><dl> <dt><strong>ERROR_UNKNOWN_DEVICE_TYPE</strong></dt> <dt>663</dt> </dl></td>
<td>Le fichier de .INI de média fait référence à un type d’appareil inconnu.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_ALLOCATING_MEMORY"></span><span id="error_allocating_memory"></span><dl> <dt><strong>ERROR_ALLOCATING_MEMORY</strong></dt> <dt>664</dt> </dl></td>
<td>Impossible d’allouer de la mémoire.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_PORT_NOT_CONFIGURED"></span><span id="error_port_not_configured"></span><dl> <dt><strong>ERROR_PORT_NOT_CONFIGURED</strong></dt> <dt>665</dt> </dl></td>
<td>Le port n’est pas configuré pour l’accès à distance.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_DEVICE_NOT_READY"></span><span id="error_device_not_ready"></span><dl> <dt><strong>ERROR_DEVICE_NOT_READY</strong></dt> <dt>666</dt> </dl></td>
<td>Votre modem ou autre périphérique de connexion ne fonctionne pas.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_READING_INI_FILE"></span><span id="error_reading_ini_file"></span><dl> <dt><strong>ERROR_READING_INI_FILE</strong></dt> <dt>667</dt> </dl></td>
<td>Impossible de lire le fichier de .INI de média.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_NO_CONNECTION"></span><span id="error_no_connection"></span><dl> <dt><strong>ERROR_NO_CONNECTION</strong></dt> <dt>668</dt> </dl></td>
<td>La connexion a été abandonnée.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_BAD_USAGE_IN_INI_FILE"></span><span id="error_bad_usage_in_ini_file"></span><dl> <dt><strong>ERROR_BAD_USAGE_IN_INI_FILE</strong></dt> <dt>669</dt> </dl></td>
<td>Le paramètre d’utilisation du fichier de .ini de média n’est pas valide.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_READING_SECTIONNAME"></span><span id="error_reading_sectionname"></span><dl> <dt><strong>ERROR_READING_SECTIONNAME</strong></dt> <dt>670</dt> </dl></td>
<td>Impossible de lire le nom de la section à partir du fichier de .INI de média.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_READING_DEVICETYPE"></span><span id="error_reading_devicetype"></span><dl> <dt><strong>ERROR_READING_DEVICETYPE</strong></dt> <dt>671</dt> </dl></td>
<td>Impossible de lire le type d’appareil à partir du fichier de .INI de média.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_READING_DEVICENAME"></span><span id="error_reading_devicename"></span><dl> <dt><strong>ERROR_READING_DEVICENAME</strong></dt> <dt>672</dt> </dl></td>
<td>Impossible de lire le nom de l’appareil à partir du fichier de .INI de média.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_READING_USAGE"></span><span id="error_reading_usage"></span><dl> <dt><strong>ERROR_READING_USAGE</strong></dt> <dt>673</dt> </dl></td>
<td>Impossible de lire l’utilisation à partir du fichier de .INI de média.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_READING_MAXCONNECTBPS"></span><span id="error_reading_maxconnectbps"></span><dl> <dt><strong>ERROR_READING_MAXCONNECTBPS</strong></dt> <dt>674</dt> </dl></td>
<td>Le système n’a pas pu lire la vitesse maximale de connexion du transporteur à partir du fichier de .INI de média.<br/>
<blockquote>
[!Note]<br />
déconseillé dans Windows Vista et les versions ultérieures de Windows.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_READING_MAXCARRIERBPS"></span><span id="error_reading_maxcarrierbps"></span><dl> <dt><strong>ERROR_READING_MAXCARRIERBPS</strong></dt> <dt>675</dt> </dl></td>
<td>Impossible de lire l’utilisation à partir du fichier de .INI de média.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_LINE_BUSY"></span><span id="error_line_busy"></span><dl> <dt><strong>ERROR_LINE_BUSY</strong></dt> <dt>676</dt> </dl></td>
<td>La ligne est occupée.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_VOICE_ANSWER"></span><span id="error_voice_answer"></span><dl> <dt><strong>ERROR_VOICE_ANSWER</strong></dt> <dt>677</dt> </dl></td>
<td>Une personne a répondu à la place d’un modem.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_NO_ANSWER"></span><span id="error_no_answer"></span><dl> <dt><strong>ERROR_NO_ANSWER</strong></dt> <dt>678</dt> </dl></td>
<td>Il n’y a pas de réponse.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_NO_CARRIER"></span><span id="error_no_carrier"></span><dl> <dt><strong>ERROR_NO_CARRIER</strong></dt> <dt>679</dt> </dl></td>
<td>Impossible de détecter un signal d’opérateur.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_NO_DIALTONE"></span><span id="error_no_dialtone"></span><dl> <dt><strong>ERROR_NO_DIALTONE</strong></dt> <dt>680</dt> </dl></td>
<td>Il n’y a pas de tonalité.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_IN_COMMAND"></span><span id="error_in_command"></span><dl> <dt><strong>ERROR_IN_COMMAND</strong></dt> <dt>681</dt> </dl></td>
<td>Le modem (ou un autre périphérique de connexion) a signalé une erreur générale.<br/>
<blockquote>
[!Note]<br />
déconseillé dans Windows Vista et les versions ultérieures de Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_WRITING_SECTIONNAME"></span><span id="error_writing_sectionname"></span><dl> <dt><strong>ERROR_WRITING_SECTIONNAME</strong></dt> <dt>682</dt> </dl></td>
<td>Une erreur s’est produite lors de l’écriture du nom de la section.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_WRITING_DEVICETYPE"></span><span id="error_writing_devicetype"></span><dl> <dt><strong>ERROR_WRITING_DEVICETYPE</strong></dt> <dt>683</dt> </dl></td>
<td>Une erreur s’est produite lors de l’écriture du type d’appareil.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_WRITING_DEVICENAME"></span><span id="error_writing_devicename"></span><dl> <dt><strong>ERROR_WRITING_DEVICENAME</strong></dt> <dt>684</dt> </dl></td>
<td>Une erreur s’est produite lors de l’écriture du nom de l’appareil.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_WRITING_MAXCONNECTBPS"></span><span id="error_writing_maxconnectbps"></span><dl> <dt><strong>ERROR_WRITING_MAXCONNECTBPS</strong></dt> <dt>685</dt> </dl></td>
<td>Une erreur s’est produite lors de l’écriture de la vitesse de connexion maximale.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_WRITING_MAXCARRIERBPS"></span><span id="error_writing_maxcarrierbps"></span><dl> <dt><strong>ERROR_WRITING_MAXCARRIERBPS</strong></dt> <dt>686</dt> </dl></td>
<td>Une erreur s’est produite lors de l’écriture de la vitesse maximale de l’opérateur.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_WRITING_USAGE"></span><span id="error_writing_usage"></span><dl> <dt><strong>ERROR_WRITING_USAGE</strong></dt> <dt>687</dt> </dl></td>
<td>Une erreur s’est produite lors de l’écriture de l’utilisation.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_WRITING_DEFAULTOFF"></span><span id="error_writing_defaultoff"></span><dl> <dt><strong>ERROR_WRITING_DEFAULTOFF</strong></dt> <dt>688</dt> </dl></td>
<td>Une erreur s’est produite lors de l’écriture de la valeur par défaut OFF.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_READING_DEFAULTOFF"></span><span id="error_reading_defaultoff"></span><dl> <dt><strong>ERROR_READING_DEFAULTOFF</strong></dt> <dt>689</dt> </dl></td>

</tr>
<tr class="odd">
<td><span id="ERROR_EMPTY_INI_FILE"></span><span id="error_empty_ini_file"></span><dl> <dt><strong>ERROR_EMPTY_INI_FILE</strong></dt> <dt>690</dt> </dl></td>
<td>Le fichier de .INI de média est vide.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_AUTHENTICATION_FAILURE"></span><span id="error_authentication_failure"></span><dl> <dt><strong>ERROR_AUTHENTICATION_FAILURE</strong></dt> <dt>691</dt> </dl></td>
<td>Accès refusé, car le nom d’utilisateur, le mot de passe ou les deux ne sont pas valides sur le domaine.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_PORT_OR_DEVICE"></span><span id="error_port_or_device"></span><dl> <dt><strong>ERROR_PORT_OR_DEVICE</strong></dt> <dt>692</dt> </dl></td>
<td>Une défaillance matérielle s’est produite dans le port ou l’appareil attaché<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_NOT_BINARY_MACRO"></span><span id="error_not_binary_macro"></span><dl> <dt><strong>ERROR_NOT_BINARY_MACRO</strong></dt> <dt>693</dt> </dl></td>
<td>La macro n’est pas une macro binaire.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_DCB_NOT_FOUND"></span><span id="error_dcb_not_found"></span><dl> <dt><strong>ERROR_DCB_NOT_FOUND</strong></dt> <dt>694</dt> </dl></td>
<td>DCB introuvable.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_STATE_MACHINES_NOT_STARTED"></span><span id="error_state_machines_not_started"></span><dl> <dt><strong>ERROR_STATE_MACHINES_NOT_STARTED</strong></dt> <dt>695</dt> </dl></td>
<td>Les machines d’État ne sont pas démarrées.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_STATE_MACHINES_ALREADY_STARTED"></span><span id="error_state_machines_already_started"></span><dl> <dt><strong>ERROR_STATE_MACHINES_ALREADY_STARTED</strong></dt> <dt>696</dt> </dl></td>
<td>Les machines d’État sont déjà démarrées.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_PARTIAL_RESPONSE_LOOPING"></span><span id="error_partial_response_looping"></span><dl> <dt><strong>ERROR_PARTIAL_RESPONSE_LOOPING</strong></dt> <dt>697</dt> </dl></td>
<td>Boucle de réponse partielle.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_UNKNOWN_RESPONSE_KEY"></span><span id="error_unknown_response_key"></span><dl> <dt><strong>ERROR_UNKNOWN_RESPONSE_KEY</strong></dt> <dt>698</dt> </dl></td>
<td>Nom de la clé de réponse dans l’appareil. Le fichier INF n’est pas au format attendu.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_RECV_BUF_FULL"></span><span id="error_recv_buf_full"></span><dl> <dt><strong>ERROR_RECV_BUF_FULL</strong></dt> <dt>699</dt> </dl></td>
<td>La réponse de l’appareil a provoqué un dépassement de mémoire tampon.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_CMD_TOO_LONG"></span><span id="error_cmd_too_long"></span><dl> <dt><strong>ERROR_CMD_TOO_LONG</strong></dt> <dt>700</dt> </dl></td>
<td>Commande développée dans l’appareil. Le fichier INF est trop long.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_UNSUPPORTED_BPS"></span><span id="error_unsupported_bps"></span><dl> <dt><strong>ERROR_UNSUPPORTED_BPS</strong></dt> <dt>701</dt> </dl></td>
<td>L’appareil a été déplacé vers une vitesse de connexion qui n’est pas prise en charge par le pilote COM.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_UNEXPECTED_RESPONSE"></span><span id="error_unexpected_response"></span><dl> <dt><strong>ERROR_UNEXPECTED_RESPONSE</strong></dt> <dt>702</dt> </dl></td>
<td>Réponse de l’appareil reçue quand aucune n’est attendue.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_INTERACTIVE_MODE"></span><span id="error_interactive_mode"></span><dl> <dt><strong>ERROR_INTERACTIVE_MODE</strong></dt> <dt>703</dt> </dl></td>
<td>Une erreur s’est produite, car le mode interactif est activé.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_BAD_CALLBACK_NUMBER"></span><span id="error_bad_callback_number"></span><dl> <dt><strong>ERROR_BAD_CALLBACK_NUMBER</strong></dt> <dt>704</dt> </dl></td>
<td>Un numéro de rappel incorrect a été spécifié.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_INVALID_AUTH_STATE"></span><span id="error_invalid_auth_state"></span><dl> <dt><strong>ERROR_INVALID_AUTH_STATE</strong></dt> <dt>705</dt> </dl></td>
<td>L’état d’authentification spécifié n’est pas valide.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_WRITING_INITBPS"></span><span id="error_writing_initbps"></span><dl> <dt><strong>ERROR_WRITING_INITBPS</strong></dt> <dt>706</dt> </dl></td>
<td>Une erreur s’est produite lors de l’écriture de la vitesse de connexion initiale.<br/>
<blockquote>
[!Note]<br />
déconseillé dans Windows Vista et les versions ultérieures de Windows.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_X25_DIAGNOSTIC"></span><span id="error_x25_diagnostic"></span><dl> <dt><strong>ERROR_X25_DIAGNOSTIC</strong></dt> <dt>707</dt> </dl></td>
<td>Une indication de diagnostic X. 25 a été reçue.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_ACCT_EXPIRED"></span><span id="error_acct_expired"></span><dl> <dt><strong>ERROR_ACCT_EXPIRED</strong></dt> <dt>708</dt> </dl></td>
<td>Le compte spécifié a expiré.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_CHANGING_PASSWORD"></span><span id="error_changing_password"></span><dl> <dt><strong>ERROR_CHANGING_PASSWORD</strong></dt> <dt>709</dt> </dl></td>
<td>Une erreur s’est produite lors de la tentative de modification du mot de passe sur le domaine.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_OVERRUN"></span><span id="error_overrun"></span><dl> <dt><strong>ERROR_OVERRUN</strong></dt> <dt>710</dt> </dl></td>
<td>Des erreurs de dépassement de série ont été détectées lors de la communication avec votre modem.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_RASMAN_CANNOT_INITIALIZE"></span><span id="error_rasman_cannot_initialize"></span><dl> <dt><strong>ERROR_RASMAN_CANNOT_INITIALIZE</strong></dt> <dt>711</dt> </dl></td>
<td>Échec de l’initialisation de RasMan. Vérifiez le journal des événements.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_BIPLEX_PORT_NOT_AVAILABLE"></span><span id="error_biplex_port_not_available"></span><dl> <dt><strong>ERROR_BIPLEX_PORT_NOT_AVAILABLE</strong></dt> <dt>712</dt> </dl></td>
<td>Le port bidirectionnel est en cours d’initialisation. Patientez quelques secondes et recomposez.<br/>
<blockquote>
[!Note]<br />
déconseillé dans Windows Vista et les versions ultérieures de Windows.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_NO_ACTIVE_ISDN_LINES"></span><span id="error_no_active_isdn_lines"></span><dl> <dt><strong>ERROR_NO_ACTIVE_ISDN_LINES</strong></dt> <dt>713</dt> </dl></td>
<td>Aucune ligne RNIS active n’est disponible.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_NO_ISDN_CHANNELS_AVAILABLE"></span><span id="error_no_isdn_channels_available"></span><dl> <dt><strong>ERROR_NO_ISDN_CHANNELS_AVAILABLE</strong></dt> <dt>714</dt> </dl></td>
<td>Aucun canal RNIS n’est disponible pour effectuer l’appel.<br/>
<blockquote>
[!Note]<br />
déconseillé dans Windows Vista et les versions ultérieures de Windows.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_TOO_MANY_LINE_ERRORS"></span><span id="error_too_many_line_errors"></span><dl> <dt><strong>ERROR_TOO_MANY_LINE_ERRORS</strong></dt> <dt>715</dt> </dl></td>
<td>Trop d’erreurs se sont produites en raison d’une mauvaise qualité de ligne téléphonique.<br/>
<blockquote>
[!Note]<br />
déconseillé dans Windows Vista et les versions ultérieures de Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_IP_CONFIGURATION"></span><span id="error_ip_configuration"></span><dl> <dt><strong>ERROR_IP_CONFIGURATION</strong></dt> <dt>716</dt> </dl></td>
<td>La configuration IP d’accès à distance est inutilisable.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_NO_IP_ADDRESSES"></span><span id="error_no_ip_addresses"></span><dl> <dt><strong>ERROR_NO_IP_ADDRESSES</strong></dt> <dt>717</dt> </dl></td>
<td>Aucune adresse IP n’est disponible dans le pool statique d’adresses IP d’accès à distance.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_PPP_TIMEOUT"></span><span id="error_ppp_timeout"></span><dl> <dt><strong>ERROR_PPP_TIMEOUT</strong></dt> <dt>718</dt> </dl></td>
<td>Un délai d’attente PPP s’est produit.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_PPP_REMOTE_TERMINATED"></span><span id="error_ppp_remote_terminated"></span><dl> <dt><strong>ERROR_PPP_REMOTE_TERMINATED</strong></dt> <dt>719</dt> </dl></td>
<td>La connexion a été arrêtée par l’ordinateur distant.<br/>
<blockquote>
[!Note]<br />
déconseillé dans Windows Vista et les versions ultérieures de Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_PPP_NO_PROTOCOLS_CONFIGURED"></span><span id="error_ppp_no_protocols_configured"></span><dl> <dt><strong>ERROR_PPP_NO_PROTOCOLS_CONFIGURED</strong></dt> <dt>720</dt> </dl></td>
<td>Aucun protocole de contrôle PPP n’est configuré.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_PPP_NO_RESPONSE"></span><span id="error_ppp_no_response"></span><dl> <dt><strong>ERROR_PPP_NO_RESPONSE</strong></dt> <dt>721</dt> </dl></td>
<td>L’homologue PPP distant ne répond pas.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_PPP_INVALID_PACKET"></span><span id="error_ppp_invalid_packet"></span><dl> <dt><strong>ERROR_PPP_INVALID_PACKET</strong></dt> <dt>722</dt> </dl></td>
<td>Le paquet PPP n’est pas valide.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_PHONE_NUMBER_TOO_LONG"></span><span id="error_phone_number_too_long"></span><dl> <dt><strong>ERROR_PHONE_NUMBER_TOO_LONG</strong></dt> <dt>723</dt> </dl></td>
<td>Le numéro de téléphone, y compris le préfixe et le suffixe, est trop long.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_IPXCP_NO_DIALOUT_CONFIGURED"></span><span id="error_ipxcp_no_dialout_configured"></span><dl> <dt><strong>ERROR_IPXCP_NO_DIALOUT_CONFIGURED</strong></dt> <dt>724</dt> </dl></td>
<td>Le protocole IPX ne peut pas effectuer de numérotation sur le modem (ou sur un autre périphérique de connexion), car cet ordinateur n’est pas configuré pour la connexion sortante (il s’agit d’un routeur IPX).<br/>
<blockquote>
[!Note]<br />
déconseillé dans Windows Vista et les versions ultérieures de Windows.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_IPXCP_NO_DIALIN_CONFIGURED"></span><span id="error_ipxcp_no_dialin_configured"></span><dl> <dt><strong>ERROR_IPXCP_NO_DIALIN_CONFIGURED</strong></dt> <dt>725</dt> </dl></td>
<td>Le protocole IPX ne peut pas se connecter sur le modem (ou un autre périphérique de connexion) car cet ordinateur n’est pas configuré pour la numérotation dans (le routeur IPX n’est pas installé).<br/>
<blockquote>
[!Note]<br />
déconseillé dans Windows Vista et les versions ultérieures de Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_IPXCP_DIALOUT_ALREADY_ACTIVE"></span><span id="error_ipxcp_dialout_already_active"></span><dl> <dt><strong>ERROR_IPXCP_DIALOUT_ALREADY_ACTIVE</strong></dt> <dt>726</dt> </dl></td>
<td>Le protocole IPX ne peut pas être utilisé pour la numérotation à distance sur plusieurs ports à la fois.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_ACCESSING_TCPCFGDLL"></span><span id="error_accessing_tcpcfgdll"></span><dl> <dt><strong>ERROR_ACCESSING_TCPCFGDLL</strong></dt> <dt>727</dt> </dl></td>
<td>Impossible d’accéder à TCPCFG.DLL.<br/>
<blockquote>
[!Note]<br />
déconseillé dans Windows Vista et les versions ultérieures de Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_NO_IP_RAS_ADAPTER"></span><span id="error_no_ip_ras_adapter"></span><dl> <dt><strong>ERROR_NO_IP_RAS_ADAPTER</strong></dt> <dt>728</dt> </dl></td>
<td>Impossible de trouver une carte IP liée à l’accès à distance.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_SLIP_REQUIRES_IP"></span><span id="error_slip_requires_ip"></span><dl> <dt><strong>ERROR_SLIP_REQUIRES_IP</strong></dt> <dt>729</dt> </dl></td>
<td>SLIP ne peut pas être utilisé tant que le protocole IP n’est pas installé.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_PROJECTION_NOT_COMPLETE"></span><span id="error_projection_not_complete"></span><dl> <dt><strong>ERROR_PROJECTION_NOT_COMPLETE</strong></dt> <dt>730</dt> </dl></td>
<td>L’inscription de l’ordinateur n’est pas terminée.<br/>
<blockquote>
[!Note]<br />
déconseillé dans Windows Vista et les versions ultérieures de Windows.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_PROTOCOL_NOT_CONFIGURED"></span><span id="error_protocol_not_configured"></span><dl> <dt><strong>ERROR_PROTOCOL_NOT_CONFIGURED</strong></dt> <dt>731</dt> </dl></td>
<td>Le protocole spécifié n’est pas configuré.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_PPP_NOT_CONVERGING"></span><span id="error_ppp_not_converging"></span><dl> <dt><strong>ERROR_PPP_NOT_CONVERGING</strong></dt> <dt>732</dt> </dl></td>
<td>La négociation PPP ne converge pas.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_PPP_CP_REJECTED"></span><span id="error_ppp_cp_rejected"></span><dl> <dt><strong>ERROR_PPP_CP_REJECTED</strong></dt> <dt>733</dt> </dl></td>
<td>le protocole de contrôle PPP du protocole réseau spécifié n’est pas disponible sur le serveur.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_PPP_LCP_TERMINATED"></span><span id="error_ppp_lcp_terminated"></span><dl> <dt><strong>ERROR_PPP_LCP_TERMINATED</strong></dt> <dt>734</dt> </dl></td>
<td>Le protocole de contrôle de liaison PPP a été arrêté.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_PPP_REQUIRED_ADDRESS_REJECTED"></span><span id="error_ppp_required_address_rejected"></span><dl> <dt><strong>ERROR_PPP_REQUIRED_ADDRESS_REJECTED</strong></dt> <dt>735</dt> </dl></td>
<td>L’adresse demandée a été rejetée par le serveur.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_PPP_NCP_TERMINATED"></span><span id="error_ppp_ncp_terminated"></span><dl> <dt><strong>ERROR_PPP_NCP_TERMINATED</strong></dt> <dt>736</dt> </dl></td>
<td>L’ordinateur distant a mis fin au protocole de contrôle.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_PPP_LOOPBACK_DETECTED"></span><span id="error_ppp_loopback_detected"></span><dl> <dt><strong>ERROR_PPP_LOOPBACK_DETECTED</strong></dt> <dt>737</dt> </dl></td>
<td>Bouclage détecté.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_PPP_NO_ADDRESS_ASSIGNED"></span><span id="error_ppp_no_address_assigned"></span><dl> <dt><strong>ERROR_PPP_NO_ADDRESS_ASSIGNED</strong></dt> <dt>738</dt> </dl></td>
<td>Le serveur n’a pas attribué d’adresse.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_CANNOT_USE_LOGON_CREDENTIALS"></span><span id="error_cannot_use_logon_credentials"></span><dl> <dt><strong>ERROR_CANNOT_USE_LOGON_CREDENTIALS</strong></dt> <dt>739</dt> </dl></td>
<td>Le serveur distant ne peut pas utiliser le mot de passe chiffré Windows NT.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_TAPI_CONFIGURATION"></span><span id="error_tapi_configuration"></span><dl> <dt><strong>ERROR_TAPI_CONFIGURATION</strong></dt> <dt>740</dt> </dl></td>
<td>Les périphériques TAPI configurés pour l’accès à distance n’ont pas pu être initialisés ou n’ont pas été installés correctement.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_NO_LOCAL_ENCRYPTION"></span><span id="error_no_local_encryption"></span><dl> <dt><strong>ERROR_NO_LOCAL_ENCRYPTION</strong></dt> <dt>741</dt> </dl></td>
<td>L’ordinateur local ne prend pas en charge le chiffrement.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_NO_REMOTE_ENCRYPTION"></span><span id="error_no_remote_encryption"></span><dl> <dt><strong>ERROR_NO_REMOTE_ENCRYPTION</strong></dt> <dt>742</dt> </dl></td>
<td>Le serveur distant ne prend pas en charge le chiffrement.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_REMOTE_REQUIRES_ENCRYPTION"></span><span id="error_remote_requires_encryption"></span><dl> <dt><strong>ERROR_REMOTE_REQUIRES_ENCRYPTION</strong></dt> <dt>743</dt> </dl></td>
<td>L’ordinateur distant requiert le chiffrement des données.<br/>
<blockquote>
[!Note]<br />
déconseillé dans Windows Vista et les versions ultérieures de Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_IPXCP_NET_NUMBER_CONFLICT"></span><span id="error_ipxcp_net_number_conflict"></span><dl> <dt><strong>ERROR_IPXCP_NET_NUMBER_CONFLICT</strong></dt> <dt>744</dt> </dl></td>
<td>Le système ne peut pas utiliser le numéro de réseau IPX attribué par l’ordinateur distant. Des informations supplémentaires sont fournies dans le journal des événements.<br/>
<blockquote>
[!Note]<br />
déconseillé dans Windows Vista et les versions ultérieures de Windows.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_INVALID_SMM"></span><span id="error_invalid_smm"></span><dl> <dt><strong>ERROR_INVALID_SMM</strong></dt> <dt>745</dt> </dl></td>
<td>Le module de gestion de session (SMM) n’est pas valide.<br/>
<blockquote>
[!Note]<br />
déconseillé dans Windows Vista et les versions ultérieures de Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_SMM_UNINITIALIZED"></span><span id="error_smm_uninitialized"></span><dl> <dt><strong>ERROR_SMM_UNINITIALIZED</strong></dt> <dt>746</dt> </dl></td>
<td>Le SMM n’est pas initialisé.<br/>
<blockquote>
[!Note]<br />
déconseillé dans Windows Vista et les versions ultérieures de Windows.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_NO_MAC_FOR_PORT"></span><span id="error_no_mac_for_port"></span><dl> <dt><strong>ERROR_NO_MAC_FOR_PORT</strong></dt> <dt>747</dt> </dl></td>
<td>Aucun MAC pour le port.<br/>
<blockquote>
[!Note]<br />
déconseillé dans Windows Vista et les versions ultérieures de Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_SMM_TIMEOUT"></span><span id="error_smm_timeout"></span><dl> <dt><strong>ERROR_SMM_TIMEOUT</strong></dt> <dt>748</dt> </dl></td>
<td>Le SMM a dépassé le délai d’attente.<br/>
<blockquote>
[!Note]<br />
déconseillé dans Windows Vista et les versions ultérieures de Windows.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_BAD_PHONE_NUMBER"></span><span id="error_bad_phone_number"></span><dl> <dt><strong>ERROR_BAD_PHONE_NUMBER</strong></dt> <dt>749</dt> </dl></td>
<td>Un numéro de téléphone incorrect a été spécifié.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_WRONG_MODULE"></span><span id="error_wrong_module"></span><dl> <dt><strong>ERROR_WRONG_MODULE</strong></dt> <dt>750</dt> </dl></td>
<td>Le mauvais SMM a été spécifié.<br/>
<blockquote>
[!Note]<br />
déconseillé dans Windows Vista et les versions ultérieures de Windows.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_INVALID_CALLBACK_NUMBER"></span><span id="error_invalid_callback_number"></span><dl> <dt><strong>ERROR_INVALID_CALLBACK_NUMBER</strong></dt> <dt>751</dt> </dl></td>
<td>Le numéro de rappel contient un caractère qui n’est pas valide. Seuls les 18 caractères suivants sont autorisés : de 0 à 9, T, P, W, (,),-, @ et Space.<br/>
<blockquote>
[!Note]<br />
déconseillé dans Windows Vista et les versions ultérieures de Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_SCRIPT_SYNTAX"></span><span id="error_script_syntax"></span><dl> <dt><strong>ERROR_SCRIPT_SYNTAX</strong></dt> <dt>752</dt> </dl></td>
<td>Une erreur de syntaxe s’est produite lors du traitement d’un script.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_HANGUP_FAILED"></span><span id="error_hangup_failed"></span><dl> <dt><strong>ERROR_HANGUP_FAILED</strong></dt> <dt>753</dt> </dl></td>
<td>La connexion n’a pas pu être déconnectée, car elle a été créée par le routeur multiprotocole.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_BUNDLE_NOT_FOUND"></span><span id="error_bundle_not_found"></span><dl> <dt><strong>ERROR_BUNDLE_NOT_FOUND</strong></dt> <dt>754</dt> </dl></td>
<td>Le système n’a pas pu trouver le bundle à liaisons multiples.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_CANNOT_DO_CUSTOMDIAL"></span><span id="error_cannot_do_customdial"></span><dl> <dt><strong>ERROR_CANNOT_DO_CUSTOMDIAL</strong></dt> <dt>755</dt> </dl></td>
<td>Le système ne peut pas effectuer la numérotation automatique, car un numéroteur personnalisé a été spécifié pour cette connexion.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_DIAL_ALREADY_IN_PROGRESS"></span><span id="error_dial_already_in_progress"></span><dl> <dt><strong>ERROR_DIAL_ALREADY_IN_PROGRESS</strong></dt> <dt>756</dt> </dl></td>
<td>Cette connexion est déjà en cours de numérotation.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_RASAUTO_CANNOT_INITIALIZE"></span><span id="error_rasauto_cannot_initialize"></span><dl> <dt><strong>ERROR_RASAUTO_CANNOT_INITIALIZE</strong></dt> <dt>757</dt> </dl></td>
<td>RAS n’a pas pu être démarré automatiquement. Des informations supplémentaires sont fournies dans le journal des événements.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_CONNECTION_ALREADY_SHARED"></span><span id="error_connection_already_shared"></span><dl> <dt><strong>ERROR_CONNECTION_ALREADY_SHARED</strong></dt> <dt>758</dt> </dl></td>
<td>Le partage de connexion Internet (ICS) est déjà activé sur la connexion.<br/>
<blockquote>
[!Note]<br />
déconseillé dans Windows Vista et les versions ultérieures de Windows.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_SHARING_CHANGE_FAILED"></span><span id="error_sharing_change_failed"></span><dl> <dt><strong>ERROR_SHARING_CHANGE_FAILED</strong></dt> <dt>759</dt> </dl></td>
<td>Une erreur s’est produite lors de la modification des paramètres de partage de connexion Internet existants.<br/>
<blockquote>
[!Note]<br />
déconseillé dans Windows Vista et les versions ultérieures de Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_SHARING_ROUTER_INSTALL"></span><span id="error_sharing_router_install"></span><dl> <dt><strong>ERROR_SHARING_ROUTER_INSTALL</strong></dt> <dt>760</dt> </dl></td>
<td>Une erreur s’est produite lors de l’activation des fonctionnalités de routage.<br/>
<blockquote>
[!Note]<br />
déconseillé dans Windows Vista et les versions ultérieures de Windows.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_SHARE_CONNECTION_FAILED"></span><span id="error_share_connection_failed"></span><dl> <dt><strong>ERROR_SHARE_CONNECTION_FAILED</strong></dt> <dt>761</dt> </dl></td>
<td>Une erreur s’est produite lors de l’activation du partage de connexion Internet pour la connexion.<br/>
<blockquote>
[!Note]<br />
déconseillé dans Windows Vista et les versions ultérieures de Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="7ERROR_SHARING_PRIVATE_INSTALL64"></span><span id="7error_sharing_private_install64"></span><dl> <dt><strong>7ERROR_SHARING_PRIVATE_INSTALL64</strong></dt> <dt>762</dt> </dl></td>
<td>Une erreur s’est produite lors de la configuration du réseau local pour le partage.<br/>
<blockquote>
[!Note]<br />
déconseillé dans Windows Vista et les versions ultérieures de Windows.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_CANNOT_SHARE_CONNECTION"></span><span id="error_cannot_share_connection"></span><dl> <dt><strong>ERROR_CANNOT_SHARE_CONNECTION</strong></dt> <dt>763</dt> </dl></td>
<td>Impossible d’activer le partage de connexion Internet. Il y a plus d’une connexion LAN autre que la connexion à partager.<br/>
<blockquote>
[!Note]<br />
déconseillé dans Windows Vista et les versions ultérieures de Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_NO_SMART_CARD_READER"></span><span id="error_no_smart_card_reader"></span><dl> <dt><strong>ERROR_NO_SMART_CARD_READER</strong></dt> <dt>764</dt> </dl></td>
<td>Aucun lecteur de carte à puce n’est installé.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_SHARING_ADDRESS_EXISTS"></span><span id="error_sharing_address_exists"></span><dl> <dt><strong>ERROR_SHARING_ADDRESS_EXISTS</strong></dt> <dt>765</dt> </dl></td>
<td>Impossible d’activer le partage de connexion Internet. Une connexion au réseau local est déjà configurée avec l’adresse IP requise pour l’adressage IP automatique. <br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_NO_CERTIFICATE"></span><span id="error_no_certificate"></span><dl> <dt><strong>ERROR_NO_CERTIFICATE</strong></dt> <dt>766</dt> </dl></td>
<td>Un certificat est introuvable. Les connexions qui utilisent le protocole L2TP sur IPSec nécessitent l’installation d’un certificat d’ordinateur, également appelé certificat d’ordinateur. <br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_SHARING_MULTIPLE_ADDRESSES"></span><span id="error_sharing_multiple_addresses"></span><dl> <dt><strong>ERROR_SHARING_MULTIPLE_ADDRESSES</strong></dt> <dt>767</dt> </dl></td>
<td>Impossible d’activer le partage de connexion Internet. Plus d’une adresse IP est configurée pour la connexion LAN sélectionnée en tant que réseau privé. Reconfigurez la connexion LAN avec une seule adresse IP avant d’activer le partage de connexion Internet. <br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_FAILED_TO_ENCRYPT"></span><span id="error_failed_to_encrypt"></span><dl> <dt><strong>ERROR_FAILED_TO_ENCRYPT</strong></dt> <dt>768</dt> </dl></td>
<td>La tentative de connexion a échoué en raison d’un échec de chiffrement des données. <br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_BAD_ADDRESS_SPECIFIED"></span><span id="error_bad_address_specified"></span><dl> <dt><strong>ERROR_BAD_ADDRESS_SPECIFIED</strong></dt> <dt>769</dt> </dl></td>
<td>La destination spécifiée n’est pas accessible. <br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_CONNECTION_REJECT"></span><span id="error_connection_reject"></span><dl> <dt><strong>ERROR_CONNECTION_REJECT</strong></dt> <dt>770</dt> </dl></td>
<td>L’ordinateur distant a rejeté la tentative de connexion. <br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_CONGESTION"></span><span id="error_congestion"></span><dl> <dt><strong>ERROR_CONGESTION</strong></dt> <dt>771</dt> </dl></td>
<td>La tentative de connexion a échoué car le réseau est occupé. <br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_INCOMPATIBLE"></span><span id="error_incompatible"></span><dl> <dt><strong>ERROR_INCOMPATIBLE</strong></dt> <dt>772</dt> </dl></td>
<td>Le matériel réseau de l’ordinateur distant est incompatible avec le type d’appel demandé. <br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_NUMBERCHANGED"></span><span id="error_numberchanged"></span><dl> <dt><strong>ERROR_NUMBERCHANGED</strong></dt> <dt>773</dt> </dl></td>
<td>La tentative de connexion a échoué car le numéro de destination a changé. <br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_TEMPFAILURE"></span><span id="error_tempfailure"></span><dl> <dt><strong>ERROR_TEMPFAILURE</strong></dt> <dt>774</dt> </dl></td>
<td>La tentative de connexion a échoué en raison d’une défaillance temporaire. Réessayez de vous connecter.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_BLOCKED"></span><span id="error_blocked"></span><dl> <dt><strong>ERROR_BLOCKED</strong></dt> <dt>775</dt> </dl></td>
<td>L’appel a été bloqué par l’ordinateur distant. <br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_DONOTDISTURB"></span><span id="error_donotdisturb"></span><dl> <dt><strong>ERROR_DONOTDISTURB</strong></dt> <dt>776</dt> </dl></td>
<td>L’appel n’a pas pu être connecté, car l’ordinateur distant a appelé la fonctionnalité ne pas déranger. <br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_OUTOFORDER"></span><span id="error_outoforder"></span><dl> <dt><strong>ERROR_OUTOFORDER</strong></dt> <dt>777</dt> </dl></td>
<td>La tentative de connexion a échoué car le modem ou un autre périphérique de connexion sur l’ordinateur distant n’est pas dans le désordre. <br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_UNABLE_TO_AUTHENTICATE_SERVER"></span><span id="error_unable_to_authenticate_server"></span><dl> <dt><strong>ERROR_UNABLE_TO_AUTHENTICATE_SERVER</strong></dt> <dt>778</dt> </dl></td>
<td>Il n’était pas possible de vérifier l’identité du serveur. <br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_SMART_CARD_REQUIRED"></span><span id="error_smart_card_required"></span><dl> <dt><strong>ERROR_SMART_CARD_REQUIRED</strong></dt> <dt>779</dt> </dl></td>
<td>Pour effectuer une numérotation à l’aide de cette connexion, vous devez utiliser une carte à puce.<br/>
<blockquote>
[!Note]<br />
déconseillé dans Windows Vista et les versions ultérieures de Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_INVALID_FUNCTION_FOR_ENTRY"></span><span id="error_invalid_function_for_entry"></span><dl> <dt><strong>ERROR_INVALID_FUNCTION_FOR_ENTRY</strong></dt> <dt>780</dt> </dl></td>
<td>Une fonction tentée n’est pas valide pour cette connexion. <br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_CERT_FOR_ENCRYPTION_NOT_FOUND"></span><span id="error_cert_for_encryption_not_found"></span><dl> <dt><strong>ERROR_CERT_FOR_ENCRYPTION_NOT_FOUND</strong></dt> <dt>781</dt> </dl></td>
<td>La tentative de chiffrement a échoué, car aucun certificat valide n’a été trouvé.<br/>
<blockquote>
[!Note]<br />
déconseillé dans Windows Vista et les versions ultérieures de Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_SHARING_RRAS_CONFLICT"></span><span id="error_sharing_rras_conflict"></span><dl> <dt><strong>ERROR_SHARING_RRAS_CONFLICT</strong></dt> <dt>782</dt> </dl></td>
<td>Le partage de connexion (NAT) est actuellement installé en tant que protocole de routage et doit être supprimé avant d’activer le partage de connexion Internet.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_SHARING_NO_PRIVATE_LAN"></span><span id="error_sharing_no_private_lan"></span><dl> <dt><strong>ERROR_SHARING_NO_PRIVATE_LAN</strong></dt> <dt>783</dt> </dl></td>
<td>Impossible d’activer le partage de connexion Internet. La connexion LAN sélectionnée en tant que réseau privé n’est pas présente ou est déconnectée du réseau. Vérifiez que la carte réseau est connectée avant d’activer le partage de connexion Internet. <br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_NO_DIFF_USER_AT_LOGON"></span><span id="error_no_diff_user_at_logon"></span><dl> <dt><strong>ERROR_NO_DIFF_USER_AT_LOGON</strong></dt> <dt>784</dt> </dl></td>
<td>Vous ne pouvez pas établir une connexion à l’aide de cette connexion au moment de la connexion, car elle est configurée pour utiliser un nom d’utilisateur différent de celui de la carte à puce. Si vous souhaitez utiliser cette connexion au moment de la connexion, vous devez la configurer pour qu’elle utilise le nom d’utilisateur sur la carte à puce. <br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_NO_REG_CERT_AT_LOGON"></span><span id="error_no_reg_cert_at_logon"></span><dl> <dt><strong>ERROR_NO_REG_CERT_AT_LOGON</strong></dt> <dt>785</dt> </dl></td>
<td>Vous ne pouvez pas établir une connexion à l’aide de cette connexion au moment de la connexion, car elle n’est pas configurée pour utiliser une carte à puce. Si vous souhaitez l’utiliser au moment de la connexion, vous devez modifier les propriétés de cette connexion pour qu’elle utilise une carte à puce. <br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_OAKLEY_NO_CERT"></span><span id="error_oakley_no_cert"></span><dl> <dt><strong>ERROR_OAKLEY_NO_CERT</strong></dt> <dt>786</dt> </dl></td>
<td>La tentative de connexion L2TP a échoué, car il n’existe aucun certificat d’ordinateur valide sur votre ordinateur pour l’authentification de sécurité. <br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_OAKLEY_AUTH_FAIL"></span><span id="error_oakley_auth_fail"></span><dl> <dt><strong>ERROR_OAKLEY_AUTH_FAIL</strong></dt> <dt>787</dt> </dl></td>
<td>La tentative de connexion L2TP a échoué car la couche de sécurité n’a pas pu authentifier l’ordinateur distant. <br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_OAKLEY_ATTRIB_FAIL"></span><span id="error_oakley_attrib_fail"></span><dl> <dt><strong>ERROR_OAKLEY_ATTRIB_FAIL</strong></dt> <dt>788</dt> </dl></td>
<td>La tentative de connexion L2TP a échoué car la couche de sécurité n’a pas pu négocier de paramètres compatibles avec l’ordinateur distant. <br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_OAKLEY_GENERAL_PROCESSING"></span><span id="error_oakley_general_processing"></span><dl> <dt><strong>ERROR_OAKLEY_GENERAL_PROCESSING</strong></dt> <dt>789</dt> </dl></td>
<td>La tentative de connexion L2TP a échoué car la couche de sécurité a rencontré une erreur de traitement lors des négociations initiales avec l’ordinateur distant. <br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_OAKLEY_NO_PEER_CERT"></span><span id="error_oakley_no_peer_cert"></span><dl> <dt><strong>ERROR_OAKLEY_NO_PEER_CERT</strong></dt> <dt>790</dt> </dl></td>
<td>Échec de la tentative de connexion L2TP en raison de l’échec de la validation du certificat sur l’ordinateur distant. <br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_OAKLEY_NO_POLICY"></span><span id="error_oakley_no_policy"></span><dl> <dt><strong>ERROR_OAKLEY_NO_POLICY</strong></dt> <dt>791</dt> </dl></td>
<td>La tentative de connexion L2TP a échoué car la stratégie de sécurité pour la connexion est introuvable. <br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_OAKLEY_TIMED_OUT"></span><span id="error_oakley_timed_out"></span><dl> <dt><strong>ERROR_OAKLEY_TIMED_OUT</strong></dt> <dt>792</dt> </dl></td>
<td>La tentative de connexion L2TP a échoué car la négociation de sécurité a expiré. <br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_OAKLEY_ERROR"></span><span id="error_oakley_error"></span><dl> <dt><strong>ERROR_OAKLEY_ERROR</strong></dt> <dt>793</dt> </dl></td>
<td>La tentative de connexion L2TP a échoué car une erreur s’est produite lors de la négociation de la sécurité. <br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_UNKNOWN_FRAMED_PROTOCOL"></span><span id="error_unknown_framed_protocol"></span><dl> <dt><strong>ERROR_UNKNOWN_FRAMED_PROTOCOL</strong></dt> <dt>794</dt> </dl></td>
<td>L’attribut RADIUS du protocole encadré pour cet utilisateur n’est pas PPP. <br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_WRONG_TUNNEL_TYPE"></span><span id="error_wrong_tunnel_type"></span><dl> <dt><strong>ERROR_WRONG_TUNNEL_TYPE</strong></dt> <dt>795</dt> </dl></td>
<td>l’attribut RADIUS de Type Tunnel pour cet utilisateur n’est pas correct. <br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_UNKNOWN_SERVICE_TYPE"></span><span id="error_unknown_service_type"></span><dl> <dt><strong>ERROR_UNKNOWN_SERVICE_TYPE</strong></dt> <dt>796</dt> </dl></td>
<td>L’attribut RADIUS du type de service pour cet utilisateur n’est ni encadré, ni rappelé. <br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_CONNECTING_DEVICE_NOT_FOUND"></span><span id="error_connecting_device_not_found"></span><dl> <dt><strong>ERROR_CONNECTING_DEVICE_NOT_FOUND</strong></dt> <dt>797</dt> </dl></td>
<td>Impossible d’établir une connexion à l’ordinateur distant, car le modem est introuvable ou était occupé. <br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_NO_EAPTLS_CERTIFICATE"></span><span id="error_no_eaptls_certificate"></span><dl> <dt><strong>ERROR_NO_EAPTLS_CERTIFICATE</strong></dt> <dt>798</dt> </dl></td>
<td>Impossible de trouver un certificat pouvant être utilisé avec le protocole EAP (Extensible Authentication Protocol). <br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_SHARING_HOST_ADDRESS_CONFLICT"></span><span id="error_sharing_host_address_conflict"></span><dl> <dt><strong>ERROR_SHARING_HOST_ADDRESS_CONFLICT</strong></dt> <dt>799</dt> </dl></td>
<td>Le partage de connexion Internet (ICS) ne peut pas être activé en raison d’un conflit d’adresse IP sur le réseau. ICS nécessite que l’hôte soit configuré pour utiliser <strong>192.168.0.1</strong>. Assurez-vous qu’aucun autre client sur le réseau n’est configuré pour utiliser <strong>192.168.0.1</strong>.<br/>
<blockquote>
[!Note]<br />
pris en charge dans Windows XP et les versions ultérieures de Windows.
</blockquote>
<br/>
<blockquote>
[!Note]<br />
Windows 7 et versions ultérieures : l’ordinateur hôte doit être configuré pour utiliser <strong>192.168.137.1</strong>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_AUTOMATIC_VPN_FAILED"></span><span id="error_automatic_vpn_failed"></span><dl> <dt><strong>ERROR_AUTOMATIC_VPN_FAILED</strong></dt> <dt>800</dt> </dl></td>
<td>Impossible d’établir la connexion VPN. Le serveur VPN est peut-être inaccessible ou les paramètres de sécurité ne sont peut-être pas configurés correctement pour cette connexion. <br/>
<blockquote>
[!Note]<br />
pris en charge dans Windows XP et les versions ultérieures de Windows.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_VALIDATING_SERVER_CERT"></span><span id="error_validating_server_cert"></span><dl> <dt><strong>ERROR_VALIDATING_SERVER_CERT</strong></dt> <dt>801</dt> </dl></td>
<td>cette connexion est configurée pour valider l’identité du serveur d’accès, mais Windows ne peut pas vérifier le certificat numérique envoyé par le serveur.<br/>
<blockquote>
[!Note]<br />
pris en charge dans Windows XP et les versions ultérieures de Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_READING_SCARD"></span><span id="error_reading_scard"></span><dl> <dt><strong>ERROR_READING_SCARD</strong></dt> <dt>802</dt> </dl></td>
<td>La carte fournie n’a pas été reconnue. Vérifiez que la carte est insérée correctement et qu’elle s’adapte en toute sécurité.<br/>
<blockquote>
[!Note]<br />
pris en charge dans Windows XP avec SP1 et les versions ultérieures de Windows.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_INVALID_PEAP_COOKIE_CONFIG"></span><span id="error_invalid_peap_cookie_config"></span><dl> <dt><strong>ERROR_INVALID_PEAP_COOKIE_CONFIG</strong></dt> <dt>803</dt> </dl></td>
<td>La configuration PEAP stockée dans le cookie de session ne correspond pas à la configuration de la session active.<br/>
<blockquote>
[!Note]<br />
pris en charge dans Windows XP avec SP1 et les versions ultérieures de Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_INVALID_PEAP_COOKIE_USER"></span><span id="error_invalid_peap_cookie_user"></span><dl> <dt><strong>ERROR_INVALID_PEAP_COOKIE_USER</strong></dt> <dt>804</dt> </dl></td>
<td>L’identité PEAP stockée dans le cookie de session ne correspond pas à l’identité actuelle.<br/>
<blockquote>
[!Note]<br />
pris en charge dans Windows XP avec SP1 et les versions ultérieures de Windows.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_INVALID_MSCHAPV2_CONFIG"></span><span id="error_invalid_mschapv2_config"></span><dl> <dt><strong>ERROR_INVALID_MSCHAPV2_CONFIG</strong></dt> <dt>805</dt> </dl></td>
<td>Vous ne pouvez pas établir une connexion à l’aide de cette connexion au moment de la connexion, car elle est configurée pour utiliser les informations d’identification de l’utilisateur actuellement connecté.<br/>
<blockquote>
[!Note]<br />
pris en charge dans Windows XP avec SP1 et les versions ultérieures de Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_VPN_GRE_BLOCKED"></span><span id="error_vpn_gre_blocked"></span><dl> <dt><strong>ERROR_VPN_GRE_BLOCKED</strong></dt> <dt>806</dt> </dl></td>
<td>Une connexion entre votre ordinateur et le serveur VPN a été démarrée, mais la connexion VPN ne peut pas être effectuée. La cause la plus courante est qu’au moins un périphérique Internet (par exemple, un pare-feu ou un routeur) entre votre ordinateur et le serveur VPN n’est pas configuré pour autoriser les paquets de protocole GRE (Generic Routing Encapsulation).<br/>
<blockquote>
[!Note]<br />
pris en charge dans Windows Vista et les versions ultérieures de Windows.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_VPN_DISCONNECT"></span><span id="error_vpn_disconnect"></span><dl> <dt><strong>ERROR_VPN_DISCONNECT</strong></dt> <dt>807</dt> </dl></td>
<td>La connexion réseau entre votre ordinateur et le serveur VPN a été interrompue. Cela peut être dû à un problème dans la transmission VPN et est généralement le résultat de la latence Internet ou simplement que votre serveur VPN a atteint sa capacité maximale. Essayez de vous reconnecter au serveur VPN.<br/>
<blockquote>
[!Note]<br />
pris en charge dans Windows Vista et les versions ultérieures de Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_VPN_REFUSED"></span><span id="error_vpn_refused"></span><dl> <dt><strong>ERROR_VPN_REFUSED</strong></dt> <dt>808</dt> </dl></td>
<td>La connexion réseau entre votre ordinateur et le serveur VPN n’a pas pu être établie car le serveur distant a refusé la connexion. Cela est généralement dû à une incompatibilité entre la configuration du serveur et vos paramètres de connexion.<br/>
<blockquote>
[!Note]<br />
pris en charge dans Windows Vista et les versions ultérieures de Windows.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_VPN_TIMEOUT"></span><span id="error_vpn_timeout"></span><dl> <dt><strong>ERROR_VPN_TIMEOUT</strong></dt> <dt>809</dt> </dl></td>
<td>La connexion réseau entre votre ordinateur et le serveur VPN n’a pas pu être établie car le serveur distant ne répond pas. Cela peut être dû au fait que l’un des périphériques réseau (par exemple, pare-feu, NAT, routeurs) entre votre ordinateur et le serveur distant n’est pas configuré pour autoriser les connexions VPN.<br/>
<blockquote>
[!Note]<br />
pris en charge dans Windows Vista et les versions ultérieures de Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_VPN_BAD_CERT"></span><span id="error_vpn_bad_cert"></span><dl> <dt><strong>ERROR_VPN_BAD_CERT</strong></dt> <dt>810</dt> </dl></td>
<td>Une connexion réseau entre votre ordinateur et le serveur VPN a été démarrée, mais la connexion VPN n’est pas terminée. Cela est généralement dû à l’utilisation d’un certificat incorrect ou arrivé à expiration pour l’authentification entre le client et le serveur.<br/>
<blockquote>
[!Note]<br />
pris en charge dans Windows Vista et les versions ultérieures de Windows
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_VPN_BAD_PSK"></span><span id="error_vpn_bad_psk"></span><dl> <dt><strong>ERROR_VPN_BAD_PSK</strong></dt> <dt>811</dt> </dl></td>
<td>La connexion réseau entre votre ordinateur et le serveur VPN n’a pas pu être établie car le serveur distant ne répond pas. Cela est généralement dû à un problème de clé pré-partagée entre le client et le serveur. Une clé prépartagée est utilisée pour vous assurer que vous êtes bien celui que vous déclarez dans un cycle de communication de sécurité IP (IPSec).<br/>
<blockquote>
[!Note]<br />
pris en charge dans Windows Vista et les versions ultérieures de Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_SERVER_POLICY"></span><span id="error_server_policy"></span><dl> <dt><strong>ERROR_SERVER_POLICY</strong></dt> <dt>812</dt> </dl></td>
<td>la connexion a été empêchée en raison d’une stratégie configurée sur votre serveur RAS/VPN. Plus précisément, la méthode d’authentification utilisée par le serveur pour vérifier votre nom d’utilisateur et votre mot de passe peut ne pas correspondre à la méthode d’authentification configurée dans votre profil de connexion.<br/>
<blockquote>
[!Note]<br />
pris en charge dans Windows Vista et les versions ultérieures de Windows.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_BROADBAND_ACTIVE"></span><span id="error_broadband_active"></span><dl> <dt><strong>ERROR_BROADBAND_ACTIVE</strong></dt> <dt>813</dt> </dl></td>
<td>Vous avez tenté d’établir une deuxième connexion large bande alors qu’une connexion haut débit précédente est déjà établie à l’aide du même périphérique ou du même port.<br/>
<blockquote>
[!Note]<br />
pris en charge dans Windows Vista et les versions ultérieures de Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_BROADBAND_NO_NIC"></span><span id="error_broadband_no_nic"></span><dl> <dt><strong>ERROR_BROADBAND_NO_NIC</strong></dt> <dt>814</dt> </dl></td>
<td>La connectivité Ethernet sous-jacente requise pour la connexion large bande est introuvable.<br/>
<blockquote>
[!Note]<br />
pris en charge dans Windows Vista et les versions ultérieures de Windows.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_BROADBAND_TIMEOUT"></span><span id="error_broadband_timeout"></span><dl> <dt><strong>ERROR_BROADBAND_TIMEOUT</strong></dt> <dt>815</dt> </dl></td>
<td>Impossible d’établir la connexion au réseau haut débit sur votre ordinateur, car le serveur distant ne répond pas. Cela peut être dû à une valeur qui n’est pas valide pour le champ « nom du service » pour cette connexion.<br/>
<blockquote>
[!Note]<br />
pris en charge dans Windows Vista et les versions ultérieures de Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_FEATURE_DEPRECATED"></span><span id="error_feature_deprecated"></span><dl> <dt><strong>ERROR_FEATURE_DEPRECATED</strong></dt> <dt>816</dt> </dl></td>
<td>Une fonctionnalité ou un paramètre que vous avez essayé d’activer n’est plus pris en charge par le service d’accès à distance.<br/>
<blockquote>
[!Note]<br />
pris en charge dans Windows Vista et les versions ultérieures de Windows.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_CANNOT_DELETE"></span><span id="error_cannot_delete"></span><dl> <dt><strong>ERROR_CANNOT_DELETE</strong></dt> <dt>817</dt> </dl></td>
<td>Impossible de supprimer une connexion pendant qu’elle est connectée.<br/>
<blockquote>
[!Note]<br />
pris en charge dans Windows Vista et les versions ultérieures de Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_RASQEC_RESOURCE_CREATION_FAILED"></span><span id="error_rasqec_resource_creation_failed"></span><dl> <dt><strong>ERROR_RASQEC_RESOURCE_CREATION_FAILED</strong></dt> <dt>818</dt> </dl></td>
<td>Le client de contrainte de mise en conformité NAP n’a pas pu créer de ressources système pour les connexions d’accès à distance. Certains services ou ressources réseau peuvent ne pas être disponibles.<br/>
<blockquote>
[!Note]<br />
pris en charge dans Windows Vista et les versions ultérieures de Windows.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_RASQEC_NAPAGENT_NOT_ENABLED"></span><span id="error_rasqec_napagent_not_enabled"></span><dl> <dt><strong>ERROR_RASQEC_NAPAGENT_NOT_ENABLED</strong></dt> <dt>819</dt> </dl></td>
<td>Le service agent de protection d’accès réseau (agent NAP) a été désactivé ou n’est pas installé sur cet ordinateur. Certains services ou ressources réseau peuvent ne pas être disponibles.<br/>
<blockquote>
[!Note]<br />
pris en charge dans Windows Vista et les versions ultérieures de Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_RASQEC_NAPAGENT_NOT_CONNECTED"></span><span id="error_rasqec_napagent_not_connected"></span><dl> <dt><strong>ERROR_RASQEC_NAPAGENT_NOT_CONNECTED</strong></dt> <dt>820</dt> </dl></td>
<td>Le client de contrainte de mise en conformité de la protection d’accès réseau (NAP) n’a pas pu s’inscrire auprès du service agent de protection d’accès réseau (agent NAP). Certains services ou ressources réseau peuvent ne pas être disponibles.<br/>
<blockquote>
[!Note]<br />
pris en charge dans Windows Vista et les versions ultérieures de Windows.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_RASQEC_CONN_DOESNOTEXIST"></span><span id="error_rasqec_conn_doesnotexist"></span><dl> <dt><strong>ERROR_RASQEC_CONN_DOESNOTEXIST</strong></dt> <dt>821</dt> </dl></td>
<td>Le client de contrainte de mise en conformité NAP n’a pas pu traiter la demande, car la connexion d’accès à distance n’existe pas.<br/>
<blockquote>
[!Note]<br />
pris en charge dans Windows Vista et les versions ultérieures de Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_RASQEC_TIMEOUT"></span><span id="error_rasqec_timeout"></span><dl> <dt><strong>ERROR_RASQEC_TIMEOUT</strong></dt> <dt>822</dt> </dl></td>
<td>Le client de contrainte de mise en conformité NAP n’a pas répondu. Certains services ou ressources réseau peuvent ne pas être disponibles.<br/>
<blockquote>
[!Note]<br />
pris en charge dans Windows Vista et les versions ultérieures de Windows.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_PEAP_CRYPTOBINDING_INVALID"></span><span id="error_peap_cryptobinding_invalid"></span><dl> <dt><strong>ERROR_PEAP_CRYPTOBINDING_INVALID</strong></dt> <dt>823</dt> </dl></td>
<td>Le Crypto-Binding type-length-value (TLV) reçu n’est pas valide.<br/>
<blockquote>
[!Note]<br />
pris en charge dans Windows Vista et les versions ultérieures de Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_PEAP_CRYPTOBINDING_NOTRECEIVED"></span><span id="error_peap_cryptobinding_notreceived"></span><dl> <dt><strong>ERROR_PEAP_CRYPTOBINDING_NOTRECEIVED</strong></dt> <dt>824</dt> </dl></td>
<td>Crypto-Binding TLV n’a pas été reçu.<br/>
<blockquote>
[!Note]<br />
pris en charge dans Windows Vista et les versions ultérieures de Windows.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_INVALID_VPNSTRATEGY"></span><span id="error_invalid_vpnstrategy"></span><dl> <dt><strong>ERROR_INVALID_VPNSTRATEGY</strong></dt> <dt>825</dt> </dl></td>
<td>Le protocole PPTP (point-to-Point Tunneling Protocol) n’est pas compatible avec IPv6. Modifiez le type de réseau privé virtuel en protocole L2TP (Layer Two Tunneling Protocol).<br/>
<blockquote>
[!Note]<br />
pris en charge dans Windows Vista et les versions ultérieures de Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_EAPTLS_CACHE_CREDENTIALS_INVALID"></span><span id="error_eaptls_cache_credentials_invalid"></span><dl> <dt><strong>ERROR_EAPTLS_CACHE_CREDENTIALS_INVALID</strong></dt> <dt>826</dt> </dl></td>
<td>Échec de la validation EAPTLS des informations d’identification mises en cache. Supprimer les informations d’identification mises en cache.<br/>
<blockquote>
[!Note]<br />
pris en charge dans Windows Vista et les versions ultérieures de Windows.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_IPSEC_SERVICE_STOPPED"></span><span id="error_ipsec_service_stopped"></span><dl> <dt><strong>ERROR_IPSEC_SERVICE_STOPPED</strong></dt> <dt>827</dt> </dl></td>
<td>La connexion L2TP/IPsec ne peut pas être effectuée car le service des modules de génération de clé IPSec IKE et AuthIP et/ou le service de moteur de filtrage de base ne sont pas en cours d’exécution. Ces services sont requis pour établir une connexion L2TP/IPSec.<br/>
<blockquote>
[!Note]<br />
pris en charge dans Windows Vista et les versions ultérieures de Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_IDLE_TIMEOUT"></span><span id="error_idle_timeout"></span><dl> <dt><strong>ERROR_IDLE_TIMEOUT</strong></dt> <dt>828</dt> </dl></td>
<td>La connexion a été arrêtée en raison d’un délai d’inactivité.<br/>
<blockquote>
[!Note]<br />
pris en charge dans Windows Vista et les versions ultérieures de Windows.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_LINK_FAILURE"></span><span id="error_link_failure"></span><dl> <dt><strong>ERROR_LINK_FAILURE</strong></dt> <dt>829</dt> </dl></td>
<td>Le modem (ou un autre périphérique de connexion) a été déconnecté en raison d’une erreur de liaison.<br/>
<blockquote>
[!Note]<br />
pris en charge dans Windows Vista et les versions ultérieures de Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_USER_LOGOFF"></span><span id="error_user_logoff"></span><dl> <dt><strong>ERROR_USER_LOGOFF</strong></dt> <dt>830</dt> </dl></td>
<td>La connexion a été interrompue, car l’utilisateur s’est déconnecté.<br/>
<blockquote>
[!Note]<br />
pris en charge dans Windows Vista et les versions ultérieures de Windows.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_FAST_USER_SWITCH"></span><span id="error_fast_user_switch"></span><dl> <dt><strong>ERROR_FAST_USER_SWITCH</strong></dt> <dt>831</dt> </dl></td>
<td>La connexion a été interrompue car le changement d’utilisateur s’est produit.<br/>
<blockquote>
[!Note]<br />
pris en charge dans Windows Vista et les versions ultérieures de Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_HIBERNATION"></span><span id="error_hibernation"></span><dl> <dt><strong>ERROR_HIBERNATION</strong></dt> <dt>832</dt> </dl></td>
<td>La connexion a été interrompue en raison de la mise en veille prolongée.<br/>
<blockquote>
[!Note]<br />
pris en charge dans Windows Vista et les versions ultérieures de Windows.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_SYSTEM_SUSPENDED"></span><span id="error_system_suspended"></span><dl> <dt><strong>ERROR_SYSTEM_SUSPENDED</strong></dt> <dt>833</dt> </dl></td>
<td>La connexion a été interrompue car le système a été suspendu.<br/>
<blockquote>
[!Note]<br />
pris en charge dans Windows Vista et les versions ultérieures de Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_RASMAN_SERVICE_STOPPED"></span><span id="error_rasman_service_stopped"></span><dl> <dt><strong>ERROR_RASMAN_SERVICE_STOPPED</strong></dt> <dt>834</dt> </dl></td>
<td>La connexion a été interrompue car le gestionnaire de connexions d’accès à distance s’est arrêté.<br/>
<blockquote>
[!Note]<br />
pris en charge dans Windows Vista et les versions ultérieures de Windows.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_INVALID_SERVER_CERT"></span><span id="error_invalid_server_cert"></span><dl> <dt><strong>ERROR_INVALID_SERVER_CERT</strong></dt> <dt>835</dt> </dl></td>
<td>La tentative de connexion L2TP a échoué car la couche de sécurité n’a pas pu authentifier l’ordinateur distant. Cela peut être dû au fait qu’un ou plusieurs champs du certificat présenté par le serveur distant n’ont pas pu être validés comme appartenant à la destination cible.<br/>
<blockquote>
[!Note]<br />
pris en charge dans Windows Vista et les versions ultérieures de Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_NOT_NAP_CAPABLE"></span><span id="error_not_nap_capable"></span><dl> <dt><strong>ERROR_NOT_NAP_CAPABLE</strong></dt> <dt>836</dt> </dl></td>
<td>La machine ne prend pas en charge la protection d’accès réseau.<br/>
<blockquote>
[!Note]<br />
pris en charge dans Windows Vista et les versions ultérieures de Windows.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_INVALID_TUNNELID"></span><span id="error_invalid_tunnelid"></span><dl> <dt><strong>ERROR_INVALID_TUNNELID</strong></dt> <dt>837</dt> </dl></td>
<td>ID de Tunnel non valide.<br/>
<blockquote>
[!Note]<br />
pris en charge dans Windows 7 et les versions ultérieures de Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_UPDATECONNECTION_REQUEST_IN_PROCESS"></span><span id="error_updateconnection_request_in_process"></span><dl> <dt><strong>ERROR_UPDATECONNECTION_REQUEST_IN_PROCESS</strong></dt> <dt>838</dt> </dl></td>
<td>Une autre demande de mise à jour de la connexion est en cours. RAS n’autorise qu’une seule demande de mise à jour de la connexion à la fois.<br/>
<blockquote>
[!Note]<br />
pris en charge dans Windows 7 et les versions ultérieures de Windows.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_PROTOCOL_ENGINE_DISABLED"></span><span id="error_protocol_engine_disabled"></span><dl> <dt><strong>ERROR_PROTOCOL_ENGINE_DISABLED</strong></dt> <dt>839</dt> </dl></td>
<td>La négociation à l’aide du protocole configuré est désactivée. Modifiez les propriétés de connexion et sélectionnez un protocole différent pour la négociation, puis réessayez.<br/>
<blockquote>
[!Note]<br />
pris en charge dans Windows 7 et les versions ultérieures de Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_INTERNAL_ADDRESS_FAILURE"></span><span id="error_internal_address_failure"></span><dl> <dt><strong>ERROR_INTERNAL_ADDRESS_FAILURE</strong></dt> <dt>840</dt> </dl></td>
<td>Échec de la négociation d’adresse interne.<br/>
<blockquote>
[!Note]<br />
pris en charge dans Windows 7 et les versions ultérieures de Windows.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_FAILED_CP_REQUIRED"></span><span id="error_failed_cp_required"></span><dl> <dt><strong>ERROR_FAILED_CP_REQUIRED</strong></dt> <dt>841</dt> </dl></td>
<td>Le client doit demander une adresse IPv4 ou IPv6 interne.<br/>
<blockquote>
[!Note]<br />
pris en charge dans Windows 7 et les versions ultérieures de Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_TS_UNACCEPTABLE"></span><span id="error_ts_unacceptable"></span><dl> <dt><strong>ERROR_TS_UNACCEPTABLE</strong></dt> <dt>842</dt> </dl></td>
<td>Échec de la négociation des sélecteurs de trafic.<br/>
<blockquote>
[!Note]<br />
pris en charge dans Windows 7 et les versions ultérieures de Windows.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_MOBIKE_DISABLED"></span><span id="error_mobike_disabled"></span><dl> <dt><strong>ERROR_MOBIKE_DISABLED</strong></dt> <dt>843</dt> </dl></td>
<td>La mobilité est désactivée pour cette connexion.<br/>
<blockquote>
[!Note]<br />
pris en charge dans Windows 7 et les versions ultérieures de Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_CANNOT_INITIATE_MOBIKE_UPDATE"></span><span id="error_cannot_initiate_mobike_update"></span><dl> <dt><strong>ERROR_CANNOT_INITIATE_MOBIKE_UPDATE</strong></dt> <dt>844</dt> </dl></td>
<td>La connexion VPN est toujours en cours de connexion ou de réauthentification en raison de la modification de l’état de mise en quarantaine. Lancer Mobile Update uniquement lorsque l’état de la connexion est « connecté ».<br/>
<blockquote>
[!Note]<br />
pris en charge dans Windows 7 et les versions ultérieures de Windows.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_PEAP_SERVER_REJECTED_CLIENT_TLV"></span><span id="error_peap_server_rejected_client_tlv"></span><dl> <dt><strong>ERROR_PEAP_SERVER_REJECTED_CLIENT_TLV</strong></dt> <dt>845</dt> </dl></td>
<td>L’authentification du client a été rejetée par le serveur en raison d’un TLV inattendu ou d’une non-concordance de valeur pour un TLV.<br/>
<blockquote>
[!Note]<br />
pris en charge dans Windows 7 et les versions ultérieures de Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_INVALID_PREFERENCES"></span><span id="error_invalid_preferences"></span><dl> <dt><strong>ERROR_INVALID_PREFERENCES</strong></dt> <dt>846</dt> </dl></td>
<td>Soit la préférence de destination VPN n’est pas sélectionnée par l’utilisateur, soit elle n’est plus valide.<br/>
<blockquote>
[!Note]<br />
pris en charge dans Windows 7 et les versions ultérieures de Windows.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_EAPTLS_SCARD_CACHE_CREDENTIALS_INVALID"></span><span id="error_eaptls_scard_cache_credentials_invalid"></span><dl> <dt><strong>ERROR_EAPTLS_SCARD_CACHE_CREDENTIALS_INVALID</strong></dt> <dt>847</dt> </dl></td>
<td>Les informations d’identification de carte à puce mises en cache ne sont pas valides.<br/>
<blockquote>
[!Note]<br />
pris en charge dans Windows 7 et les versions ultérieures de Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_SSTP_COOKIE_SET_FAILURE"></span><span id="error_sstp_cookie_set_failure"></span><dl> <dt><strong>ERROR_SSTP_COOKIE_SET_FAILURE</strong></dt> <dt>848</dt> </dl></td>
<td>Échec de la tentative de connexion VPN en raison d’une erreur interne lors de l’ajout de cookies au protocole SSTP (Secure Socket Tunneling Protocol). Pour plus d’informations, consultez le journal des événements système.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_INVALID_PEAP_COOKIE_ATTRIBUTES"></span><span id="error_invalid_peap_cookie_attributes"></span><dl> <dt><strong>ERROR_INVALID_PEAP_COOKIE_ATTRIBUTES</strong></dt> <dt>849</dt> </dl></td>
<td>Le ou les attributs de la méthode interne PEAP stockés dans le cookie sont/ne sont pas valides.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_EAP_METHOD_NOT_INSTALLED"></span><span id="error_eap_method_not_installed"></span><dl> <dt><strong>ERROR_EAP_METHOD_NOT_INSTALLED</strong></dt> <dt>850</dt> </dl></td>
<td>Le type de protocole d’authentification extensible requis pour l’authentification de la connexion d’accès à distance n’est pas installé sur votre ordinateur.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_EAP_METHOD_DOES_NOT_SUPPORT_SSO"></span><span id="error_eap_method_does_not_support_sso"></span><dl> <dt><strong>ERROR_EAP_METHOD_DOES_NOT_SUPPORT_SSO</strong></dt> <dt>851</dt> </dl></td>
<td>Le type de protocole EAP (Extensible Authentication Protocol) configuré sur la connexion d’accès à distance ne prend pas en charge l’authentification unique.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_EAP_METHOD_OPERATION_NOT_SUPPORTED"></span><span id="error_eap_method_operation_not_supported"></span><dl> <dt><strong>ERROR_EAP_METHOD_OPERATION_NOT_SUPPORTED</strong></dt> <dt>852</dt> </dl></td>
<td>Le type de protocole EAP (Extensible Authentication Protocol) configuré sur la connexion d’accès à distance ne prend pas en charge l’opération demandée.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_EAP_USER_CERT_INVALID"></span><span id="error_eap_user_cert_invalid"></span><dl> <dt><strong>ERROR_EAP_USER_CERT_INVALID</strong></dt> <dt>853</dt> </dl></td>
<td>La connexion d’accès à distance est terminée, mais l’authentification a échoué car le certificat qui authentifie le client sur le serveur n’est pas valide. Assurez-vous que le certificat utilisé pour l’authentification est valide.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_EAP_USER_CERT_EXPIRED"></span><span id="error_eap_user_cert_expired"></span><dl> <dt><strong>ERROR_EAP_USER_CERT_EXPIRED</strong></dt> <dt>854</dt> </dl></td>
<td>La connexion d’accès à distance est terminée, mais l’authentification a échoué, car le certificat qui authentifie le client auprès du serveur a expiré. Renouvelez le certificat.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_EAP_USER_CERT_REVOKED"></span><span id="error_eap_user_cert_revoked"></span><dl> <dt><strong>ERROR_EAP_USER_CERT_REVOKED</strong></dt> <dt>855</dt> </dl></td>
<td>La connexion d’accès à distance est terminée, mais l’authentification a échoué car le certificat qui authentifie le client sur le serveur est révoqué. Utilisez un certificat qui n’a pas été révoqué.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_EAP_USER_CERT_OTHER_ERROR"></span><span id="error_eap_user_cert_other_error"></span><dl> <dt><strong>ERROR_EAP_USER_CERT_OTHER_ERROR</strong></dt> <dt>856</dt> </dl></td>
<td>La connexion d’accès à distance est terminée, mais l’authentification a échoué en raison d’une erreur dans le certificat qui authentifie le client auprès du serveur.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_EAP_SERVER_CERT_INVALID"></span><span id="error_eap_server_cert_invalid"></span><dl> <dt><strong>ERROR_EAP_SERVER_CERT_INVALID</strong></dt> <dt>857</dt> </dl></td>
<td>La connexion d’accès à distance est terminée, mais l’authentification a échoué, car le certificat utilisé par le client pour authentifier le serveur n’est pas valide.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_EAP_SERVER_CERT_EXPIRED"></span><span id="error_eap_server_cert_expired"></span><dl> <dt><strong>ERROR_EAP_SERVER_CERT_EXPIRED</strong></dt> <dt>858</dt> </dl></td>
<td>La connexion d’accès à distance est terminée, mais l’authentification a échoué, car le certificat utilisé par le client pour authentifier le serveur a expiré.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_EAP_SERVER_CERT_REVOKED"></span><span id="error_eap_server_cert_revoked"></span><dl> <dt><strong>ERROR_EAP_SERVER_CERT_REVOKED</strong></dt> <dt>859</dt> </dl></td>
<td>La connexion d’accès à distance est terminée, mais l’authentification a échoué, car le certificat que le client utilise pour authentifier le serveur est révoqué.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_EAP_SERVER_CERT_OTHER_ERROR"></span><span id="error_eap_server_cert_other_error"></span><dl> <dt><strong>ERROR_EAP_SERVER_CERT_OTHER_ERROR</strong></dt> <dt>860</dt> </dl></td>
<td>La connexion d’accès à distance est terminée, mais l’authentification a échoué en raison d’une erreur dans le certificat que le client utilise pour authentifier le serveur.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_EAP_USER_ROOT_CERT_NOT_FOUND"></span><span id="error_eap_user_root_cert_not_found"></span><dl> <dt><strong>ERROR_EAP_USER_ROOT_CERT_NOT_FOUND</strong></dt> <dt>861</dt> </dl></td>
<td>La connexion d’accès à distance est terminée, mais l’authentification a échoué, car un certificat racine approuvé qui valide le certificat de l’utilisateur est introuvable dans le magasin de certificats des autorités de certification racines de confiance.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_EAP_USER_ROOT_CERT_INVALID"></span><span id="error_eap_user_root_cert_invalid"></span><dl> <dt><strong>ERROR_EAP_USER_ROOT_CERT_INVALID</strong></dt> <dt>862</dt> </dl></td>
<td>La connexion d’accès à distance est terminée, mais l’authentification a échoué, car le certificat racine approuvé utilisé pour valider le certificat utilisateur n’est pas valide.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_EAP_USER_ROOT_CERT_EXPIRED"></span><span id="error_eap_user_root_cert_expired"></span><dl> <dt><strong>ERROR_EAP_USER_ROOT_CERT_EXPIRED</strong></dt> <dt>863</dt> </dl></td>
<td>La connexion d’accès à distance est terminée, mais l’authentification a échoué, car le certificat dans le magasin de certificats des autorités de certification racines de confiance qui authentifie le certificat utilisateur a expiré. Renouvelez le certificat.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_EAP_SERVER_ROOT_CERT_NOT_FOUND"></span><span id="error_eap_server_root_cert_not_found"></span><dl> <dt><strong>ERROR_EAP_SERVER_ROOT_CERT_NOT_FOUND</strong></dt> <dt>864</dt> </dl></td>
<td>La connexion d’accès à distance est terminée, mais l’authentification a échoué, car un certificat qui valide le certificat de serveur est introuvable dans le magasin de certificats des autorités de certification racines de confiance.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_EAP_SERVER_ROOT_CERT_INVALID"></span><span id="error_eap_server_root_cert_invalid"></span><dl> <dt><strong>ERROR_EAP_SERVER_ROOT_CERT_INVALID</strong></dt> <dt>865</dt> </dl></td>
<td>La connexion d’accès à distance est terminée, mais l’authentification a échoué car le certificat dans le magasin de certificats des autorités de certification racines de confiance qui valide le certificat de serveur n’est pas valide.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_EAP_SERVER_ROOT_CERT_NAME_REQUIRED"></span><span id="error_eap_server_root_cert_name_required"></span><dl> <dt><strong>ERROR_EAP_SERVER_ROOT_CERT_NAME_REQUIRED</strong></dt> <dt>866</dt> </dl></td>
<td>La connexion d’accès à distance est terminée, mais l’authentification a échoué, car aucun nom de serveur n’a été spécifié pour le certificat sur l’ordinateur serveur.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_PEAP_IDENTITY_MISMATCH"></span><span id="error_peap_identity_mismatch"></span><dl> <dt><strong>ERROR_PEAP_IDENTITY_MISMATCH</strong></dt> <dt>867</dt> </dl></td>
<td>L’identité externe PEAP n’est pas identique à l’identité interne lorsque la confidentialité de l’identité est désactivée.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_DNSNAME_NOT_RESOLVABLE"></span><span id="error_dnsname_not_resolvable"></span><dl> <dt><strong>ERROR_DNSNAME_NOT_RESOLVABLE</strong></dt> <dt>868</dt> </dl></td>
<td>La connexion à distance n’a pas été établie, car le nom du serveur d’accès à distance n’a pas été résolu.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_EAPTLS_PASSWD_INVALID"></span><span id="error_eaptls_passwd_invalid"></span><dl> <dt><strong>ERROR_EAPTLS_PASSWD_INVALID</strong></dt> <dt>869</dt> </dl></td>
<td>Le mot de passe fourni pour le certificat n’est pas valide.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_IKEV2_PSK_INTERFACE_ALREADY_EXISTS"></span><span id="error_ikev2_psk_interface_already_exists"></span><dl> <dt><strong>ERROR_IKEV2_PSK_INTERFACE_ALREADY_EXISTS</strong></dt> <dt>870</dt> </dl></td>
<td>L’interface n’a pas pu être activée, car plusieurs interfaces ayant la même destination ont été créées avec la méthode d’authentification par clé prépartagée. Modifiez la méthode d’authentification/destination et activez l’interface.<br/></td>
</tr>
</tbody>
</table>



 

Les codes d’erreur de l’API de routage et d’accès à distance (RRAS) suivants sont définis dans mprerror. h. tous les codes d’erreur sont pris en charge dans Windows 2000 ou les versions ultérieures de Windows, sauf indication contraire.



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Code/valeur de retour</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="ERROR_ROUTER_STOPPED"></span><span id="error_router_stopped"></span><dl> <dt><strong>ERROR_ROUTER_STOPPED</strong></dt> <dt>900</dt> </dl></td>
<td>Le routeur n’est pas en cours d’exécution.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_ALREADY_CONNECTED"></span><span id="error_already_connected"></span><dl> <dt><strong>ERROR_ALREADY_CONNECTED</strong></dt> <dt>901</dt> </dl></td>
<td>L’interface est déjà connectée.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_UNKNOWN_PROTOCOL_ID"></span><span id="error_unknown_protocol_id"></span><dl> <dt><strong>ERROR_UNKNOWN_PROTOCOL_ID</strong></dt> <dt>902</dt> </dl></td>
<td>L’identificateur de protocole spécifié n’est pas connu du routeur.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_DDM_NOT_RUNNING"></span><span id="error_ddm_not_running"></span><dl> <dt><strong>ERROR_DDM_NOT_RUNNING</strong></dt> <dt>903</dt> </dl></td>
<td>Le gestionnaire de l’interface de connexion à la demande (DDM) n’est pas en cours d’exécution.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_INTERFACE_ALREADY_EXISTS"></span><span id="error_interface_already_exists"></span><dl> <dt><strong>ERROR_INTERFACE_ALREADY_EXISTS</strong></dt> <dt>904</dt> </dl></td>
<td>Une interface portant ce nom est déjà inscrite auprès du routeur.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_NO_SUCH_INTERFACE"></span><span id="error_no_such_interface"></span><dl> <dt><strong>ERROR_NO_SUCH_INTERFACE</strong></dt> <dt>905</dt> </dl></td>
<td>Une interface portant ce nom n’est pas inscrite auprès du routeur.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_INTERFACE_NOT_CONNECTED"></span><span id="error_interface_not_connected"></span><dl> <dt><strong>ERROR_INTERFACE_NOT_CONNECTED</strong></dt> <dt>906</dt> </dl></td>
<td>L’interface n’est pas connectée.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_PROTOCOL_STOP_PENDING"></span><span id="error_protocol_stop_pending"></span><dl> <dt><strong>ERROR_PROTOCOL_STOP_PENDING</strong></dt> <dt>907</dt> </dl></td>
<td>Le protocole spécifié est en cours d’arrêt.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_INTERFACE_CONNECTED"></span><span id="error_interface_connected"></span><dl> <dt><strong>ERROR_INTERFACE_CONNECTED</strong></dt> <dt>908</dt> </dl></td>
<td>L’interface est connectée et ne peut donc pas être supprimée.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_NO_INTERFACE_CREDENTIALS_SET"></span><span id="error_no_interface_credentials_set"></span><dl> <dt><strong>ERROR_NO_INTERFACE_CREDENTIALS_SET</strong></dt> <dt>909</dt> </dl></td>
<td>Les informations d’identification de l’interface n’ont pas été définies.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_ALREADY_CONNECTING"></span><span id="error_already_connecting"></span><dl> <dt><strong>ERROR_ALREADY_CONNECTING</strong></dt> <dt>910</dt> </dl></td>
<td>Cette interface est déjà en cours de connexion.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_UPDATE_IN_PROGRESS"></span><span id="error_update_in_progress"></span><dl> <dt><strong>ERROR_UPDATE_IN_PROGRESS</strong></dt> <dt>911</dt> </dl></td>
<td>Une mise à jour des informations de routage sur cette interface est déjà en cours.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_INTERFACE_CONFIGURATION"></span><span id="error_interface_configuration"></span><dl> <dt><strong>ERROR_INTERFACE_CONFIGURATION</strong></dt> <dt>912</dt> </dl></td>
<td>La validation de l’interface n’est pas valide. Une autre interface est déjà connectée à la même interface sur le routeur distant.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_NOT_CLIENT_PORT"></span><span id="error_not_client_port"></span><dl> <dt><strong>ERROR_NOT_CLIENT_PORT</strong></dt> <dt>913</dt> </dl></td>
<td>Un client d’accès à distance a tenté de se connecter sur un port réservé aux routeurs.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_NOT_ROUTER_PORT"></span><span id="error_not_router_port"></span><dl> <dt><strong>ERROR_NOT_ROUTER_PORT</strong></dt> <dt>914</dt> </dl></td>
<td>Un routeur de connexion à la demande a tenté de se connecter sur un port réservé aux clients d’accès à distance uniquement.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_CLIENT_INTERFACE_ALREADY_EXISTS"></span><span id="error_client_interface_already_exists"></span><dl> <dt><strong>ERROR_CLIENT_INTERFACE_ALREADY_EXISTS</strong></dt> <dt>915</dt> </dl></td>
<td>L’interface cliente portant ce nom existe déjà et est actuellement connectée.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_INTERFACE_DISABLED"></span><span id="error_interface_disabled"></span><dl> <dt><strong>ERROR_INTERFACE_DISABLED</strong></dt> <dt>916</dt> </dl></td>
<td>L’interface est dans un état désactivé.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_AUTH_PROTOCOL_REJECTED"></span><span id="error_auth_protocol_rejected"></span><dl> <dt><strong>ERROR_AUTH_PROTOCOL_REJECTED</strong></dt> <dt>917</dt> </dl></td>
<td>Le protocole d’authentification a été rejeté par l’homologue distant.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_NO_AUTH_PROTOCOL_AVAILABLE"></span><span id="error_no_auth_protocol_available"></span><dl> <dt><strong>ERROR_NO_AUTH_PROTOCOL_AVAILABLE</strong></dt> <dt>918</dt> </dl></td>
<td>Aucun protocole d’authentification n’est disponible pour l’utilisation.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_PEER_REFUSED_AUTH"></span><span id="error_peer_refused_auth"></span><dl> <dt><strong>ERROR_PEER_REFUSED_AUTH</strong></dt> <dt>919</dt> </dl></td>
<td>Impossible d’établir la connexion, car le protocole d’authentification utilisé par le serveur RAS/VPN pour vérifier votre nom d’utilisateur et votre mot de passe n’a pas pu être mis en correspondance avec les paramètres de votre profil de connexion.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_REMOTE_NO_DIALIN_PERMISSION"></span><span id="error_remote_no_dialin_permission"></span><dl> <dt><strong>ERROR_REMOTE_NO_DIALIN_PERMISSION</strong></dt> <dt>920</dt> </dl></td>
<td>Le compte distant ne dispose pas de l’autorisation d’accès à distance.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_REMOTE_PASSWD_EXPIRED"></span><span id="error_remote_passwd_expired"></span><dl> <dt><strong>ERROR_REMOTE_PASSWD_EXPIRED</strong></dt> <dt>921</dt> </dl></td>
<td>Le compte distant a expiré.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_REMOTE_ACCT_DISABLED"></span><span id="error_remote_acct_disabled"></span><dl> <dt><strong>ERROR_REMOTE_ACCT_DISABLED</strong></dt> <dt>922</dt> </dl></td>
<td>Le compte distant est désactivé.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_REMOTE_RESTRICTED_LOGON_HOURS"></span><span id="error_remote_restricted_logon_hours"></span><dl> <dt><strong>ERROR_REMOTE_RESTRICTED_LOGON_HOURS</strong></dt> <dt>923</dt> </dl></td>
<td>Le compte distant n’est pas autorisé à se connecter à cette heure de la journée.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_REMOTE_AUTHENTICATION_FAILURE"></span><span id="error_remote_authentication_failure"></span><dl> <dt><strong>ERROR_REMOTE_AUTHENTICATION_FAILURE</strong></dt> <dt>924</dt> </dl></td>
<td>L’accès a été refusé à l’homologue distant, car le nom d’utilisateur, le mot de passe ou les deux ne sont pas valides sur le domaine.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_INTERFACE_HAS_NO_DEVICES"></span><span id="error_interface_has_no_devices"></span><dl> <dt><strong>ERROR_INTERFACE_HAS_NO_DEVICES</strong></dt> <dt>925</dt> </dl></td>
<td>Aucun port activé pour le routage n’est disponible pour une utilisation par cette interface de connexion à la demande.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_IDLE_DISCONNECTED"></span><span id="error_idle_disconnected"></span><dl> <dt><strong>ERROR_IDLE_DISCONNECTED</strong></dt> <dt>926</dt> </dl></td>
<td>Le port a été déconnecté en raison d’une inactivité.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_INTERFACE_UNREACHABLE"></span><span id="error_interface_unreachable"></span><dl> <dt><strong>ERROR_INTERFACE_UNREACHABLE</strong></dt> <dt>927</dt> </dl></td>
<td>L’interface n’est pas accessible pour l’instant.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_SERVICE_IS_PAUSED"></span><span id="error_service_is_paused"></span><dl> <dt><strong>ERROR_SERVICE_IS_PAUSED</strong></dt> <dt>928</dt> </dl></td>
<td>Le service de numérotation à la demande est dans un état suspendu.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_INTERFACE_DISCONNECTED"></span><span id="error_interface_disconnected"></span><dl> <dt><strong>ERROR_INTERFACE_DISCONNECTED</strong></dt> <dt>929</dt> </dl></td>
<td>L’interface a été déconnectée par l’administrateur.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_AUTH_SERVER_TIMEOUT"></span><span id="error_auth_server_timeout"></span><dl> <dt><strong>ERROR_AUTH_SERVER_TIMEOUT</strong></dt> <dt>930</dt> </dl></td>
<td>Le serveur d’authentification n’a pas répondu aux demandes d’authentification en temps opportun.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_PORT_LIMIT_REACHED"></span><span id="error_port_limit_reached"></span><dl> <dt><strong>ERROR_PORT_LIMIT_REACHED</strong></dt> <dt>931</dt> </dl></td>
<td>Le nombre maximal de ports autorisés pour une utilisation dans la connexion à plusieurs liaisons a été atteint.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_PPP_SESSION_TIMEOUT"></span><span id="error_ppp_session_timeout"></span><dl> <dt><strong>ERROR_PPP_SESSION_TIMEOUT</strong></dt> <dt>932</dt> </dl></td>
<td>Le délai de connexion de l’utilisateur a été atteint.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_MAX_LAN_INTERFACE_LIMIT"></span><span id="error_max_lan_interface_limit"></span><dl> <dt><strong>ERROR_MAX_LAN_INTERFACE_LIMIT</strong></dt> <dt>933</dt> </dl></td>
<td>La limite maximale du nombre d’interfaces LAN prises en charge a été atteinte.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_MAX_WAN_INTERFACE_LIMIT"></span><span id="error_max_wan_interface_limit"></span><dl> <dt><strong>ERROR_MAX_WAN_INTERFACE_LIMIT</strong></dt> <dt>934</dt> </dl></td>
<td>La limite maximale du nombre d’interfaces de connexion à la demande prises en charge a été atteinte.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_MAX_CLIENT_INTERFACE_LIMIT"></span><span id="error_max_client_interface_limit"></span><dl> <dt><strong>ERROR_MAX_CLIENT_INTERFACE_LIMIT</strong></dt> <dt>935</dt> </dl></td>
<td>La limite maximale du nombre de clients d’accès à distance pris en charge a été atteinte.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_BAP_DISCONNECTED"></span><span id="error_bap_disconnected"></span><dl> <dt><strong>ERROR_BAP_DISCONNECTED</strong></dt> <dt>936</dt> </dl></td>
<td>Le port a été déconnecté en raison de la stratégie du protocole BAP (Bandwidth Allocation Protocol).<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_USER_LIMIT"></span><span id="error_user_limit"></span><dl> <dt><strong>ERROR_USER_LIMIT</strong></dt> <dt>937</dt> </dl></td>
<td>Une autre connexion de votre type étant en cours d’utilisation, la connexion entrante ne peut pas accepter votre demande de connexion.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_NO_RADIUS_SERVERS"></span><span id="error_no_radius_servers"></span><dl> <dt><strong>ERROR_NO_RADIUS_SERVERS</strong></dt> <dt>938</dt> </dl></td>
<td>Aucun serveur RADIUS n’a été trouvé sur le réseau.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_INVALID_RADIUS_RESPONSE"></span><span id="error_invalid_radius_response"></span><dl> <dt><strong>ERROR_INVALID_RADIUS_RESPONSE</strong></dt> <dt>939</dt> </dl></td>
<td>La réponse reçue du serveur d’authentification RADIUS n’est pas valide. Assurez-vous que le mot de passe secret sensible à la casse pour le serveur RADIUS est correctement défini.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_DIALIN_HOURS_RESTRICTION"></span><span id="error_dialin_hours_restriction"></span><dl> <dt><strong>ERROR_DIALIN_HOURS_RESTRICTION</strong></dt> <dt>940</dt> </dl></td>
<td>Vous n’êtes pas autorisé à vous connecter pour l’instant.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_ALLOWED_PORT_TYPE_RESTRICTION"></span><span id="error_allowed_port_type_restriction"></span><dl> <dt><strong>ERROR_ALLOWED_PORT_TYPE_RESTRICTION</strong></dt> <dt>941</dt> </dl></td>
<td>Vous n’êtes pas autorisé à vous connecter à l’aide du type d’appareil actuel.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_AUTH_PROTOCOL_RESTRICTION"></span><span id="error_auth_protocol_restriction"></span><dl> <dt><strong>ERROR_AUTH_PROTOCOL_RESTRICTION</strong></dt> <dt>942</dt> </dl></td>
<td>La connexion n’a pas pu être établie, car la méthode d’authentification utilisée par votre profil de connexion n’est pas autorisée pour une utilisation par une stratégie d’accès configurée sur le serveur RAS/VPN. Plus précisément, cela peut être dû à des différences de configuration entre la méthode d’authentification sélectionnée sur le serveur RAS/VPN et la stratégie d’accès configurée pour celle-ci.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_BAP_REQUIRED"></span><span id="error_bap_required"></span><dl> <dt><strong>ERROR_BAP_REQUIRED</strong></dt> <dt>943</dt> </dl></td>
<td>BAP est requis pour cet utilisateur.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_DIALOUT_HOURS_RESTRICTION"></span><span id="error_dialout_hours_restriction"></span><dl> <dt><strong>ERROR_DIALOUT_HOURS_RESTRICTION</strong></dt> <dt>944</dt> </dl></td>
<td>L’interface n’est pas autorisée à se connecter pour l’instant.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_ROUTER_CONFIG_INCOMPATIBLE"></span><span id="error_router_config_incompatible"></span><dl> <dt><strong>ERROR_ROUTER_CONFIG_INCOMPATIBLE</strong></dt> <dt>945</dt> </dl></td>
<td>La configuration du routeur enregistrée n’est pas compatible avec le routeur actuel.<br/></td>
</tr>
<tr class="odd">
<td><span id="WARNING_NO_MD5_MIGRATION"></span><span id="warning_no_md5_migration"></span><dl> <dt><strong>WARNING_NO_MD5_MIGRATION</strong></dt> <dt>946</dt> </dl></td>
<td>L’accès à distance a détecté des comptes d’utilisateur de format plus anciens qui ne seront pas migrés automatiquement.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_PROTOCOL_ALREADY_INSTALLED"></span><span id="error_protocol_already_installed"></span><dl> <dt><strong>ERROR_PROTOCOL_ALREADY_INSTALLED</strong></dt> <dt>948</dt> </dl></td>
<td>Le transport est déjà installé avec le routeur.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_INVALID_SIGNATURE_LENGTH"></span><span id="error_invalid_signature_length"></span><dl> <dt><strong>ERROR_INVALID_SIGNATURE_LENGTH</strong></dt> <dt>949</dt> </dl></td>
<td>La longueur de signature reçue dans un paquet du serveur RADIUS n’est pas valide.<br/>
<blockquote>
[!Note]<br />
pris en charge dans Windows XP et les versions ultérieures de Windows.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_INVALID_SIGNATURE"></span><span id="error_invalid_signature"></span><dl> <dt><strong>ERROR_INVALID_SIGNATURE</strong></dt> <dt>950</dt> </dl></td>
<td>La signature reçue dans un paquet du serveur RADIUS n’est pas valide.<br/>
<blockquote>
[!Note]<br />
pris en charge dans Windows XP et les versions ultérieures de Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_NO_SIGNATURE"></span><span id="error_no_signature"></span><dl> <dt><strong>ERROR_NO_SIGNATURE</strong></dt> <dt>951</dt> </dl></td>
<td>Impossible de recevoir la signature avec EAPMessage du serveur RADIUS.<br/>
<blockquote>
[!Note]<br />
pris en charge dans Windows XP et les versions ultérieures de Windows.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_INVALID_PACKET_LENGTH_OR_ID"></span><span id="error_invalid_packet_length_or_id"></span><dl> <dt><strong>ERROR_INVALID_PACKET_LENGTH_OR_ID</strong></dt> <dt>952</dt> </dl></td>
<td>La longueur ou l’ID reçu dans un paquet du serveur RADIUS n’est pas valide.<br/>
<blockquote>
[!Note]<br />
pris en charge dans Windows XP et les versions ultérieures de Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_INVALID_ATTRIBUTE_LENGTH"></span><span id="error_invalid_attribute_length"></span><dl> <dt><strong>ERROR_INVALID_ATTRIBUTE_LENGTH</strong></dt> <dt>953</dt> </dl></td>
<td>La longueur reçue dans un paquet avec un attribut du serveur RADIUS n’est pas valide.<br/>
<blockquote>
[!Note]<br />
pris en charge dans Windows XP et les versions ultérieures de Windows.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_INVALID_PACKET"></span><span id="error_invalid_packet"></span><dl> <dt><strong>ERROR_INVALID_PACKET</strong></dt> <dt>954</dt> </dl></td>
<td>Le paquet reçu du serveur RADIUS n’est pas valide.<br/>
<blockquote>
[!Note]<br />
pris en charge dans Windows XP et les versions ultérieures de Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_AUTHENTICATOR_MISMATCH"></span><span id="error_authenticator_mismatch"></span><dl> <dt><strong>ERROR_AUTHENTICATOR_MISMATCH</strong></dt> <dt>955</dt> </dl></td>
<td>Authenticator ne correspond pas au paquet du serveur RADIUS.<br/>
<blockquote>
[!Note]<br />
pris en charge dans Windows XP et les versions ultérieures de Windows.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_REMOTEACCESS_NOT_CONFIGURED"></span><span id="error_remoteaccess_not_configured"></span><dl> <dt><strong>ERROR_REMOTEACCESS_NOT_CONFIGURED</strong></dt> <dt>956</dt> </dl></td>
<td>Le serveur de routage et d’accès à distance n’est pas configuré ou n’est pas en cours d’exécution.<br/>
<blockquote>
[!Note]<br />
pris en charge dans Windows 7 et les versions ultérieures de Windows.
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/> |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>       |



 

 





