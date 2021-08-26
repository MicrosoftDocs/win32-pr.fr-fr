---
title: Windows Constantes d’erreur du journal des événements (WinError. h)
description: voici les codes d’erreur que Windows journal des événements définit.
ms.assetid: 889ea4ae-dede-45d5-9293-cec85d81f010
topic_type:
- apiref
api_name:
- ERROR_EVT_INVALID_CHANNEL_PATH
- ERROR_EVT_INVALID_QUERY
- ERROR_EVT_PUBLISHER_METADATA_NOT_FOUND
- ERROR_EVT_EVENT_TEMPLATE_NOT_FOUND
- ERROR_EVT_INVALID_PUBLISHER_NAME
- ERROR_EVT_INVALID_EVENT_DATA
- ERROR_EVT_CHANNEL_NOT_FOUND
- ERROR_EVT_MALFORMED_XML_TEXT
- ERROR_EVT_SUBSCRIPTION_TO_DIRECT_CHANNEL
- ERROR_EVT_CONFIGURATION_ERROR
- ERROR_EVT_QUERY_RESULT_STALE
- ERROR_EVT_QUERY_RESULT_INVALID_POSITION
- ERROR_EVT_NON_VALIDATING_MSXML
- ERROR_EVT_FILTER_ALREADYSCOPED
- ERROR_EVT_FILTER_NOTELTSET
- ERROR_EVT_FILTER_INVARG
- ERROR_EVT_FILTER_INVTEST
- ERROR_EVT_FILTER_INVTYPE
- ERROR_EVT_FILTER_PARSEERR
- ERROR_EVT_FILTER_UNSUPPORTEDOP
- ERROR_EVT_FILTER_UNEXPECTEDTOKEN
- ERROR_EVT_INVALID_OPERATION_OVER_ENABLED_DIRECT_CHANNEL
- ERROR_EVT_INVALID_CHANNEL_PROPERTY_VALUE
- ERROR_EVT_INVALID_PUBLISHER_PROPERTY_VALUE
- ERROR_EVT_CHANNEL_CANNOT_ACTIVATE
- ERROR_EVT_FILTER_TOO_COMPLEX
- ERROR_EVT_MESSAGE_NOT_FOUND
- ERROR_EVT_MESSAGE_ID_NOT_FOUND
- ERROR_EVT_UNRESOLVED_VALUE_INSERT
- ERROR_EVT_UNRESOLVED_PARAMETER_INSERT
- ERROR_EVT_MAX_INSERTS_REACHED
- ERROR_EVT_EVENT_DEFINITION_NOT_FOUND
- ERROR_EVT_MESSAGE_LOCALE_NOT_FOUND
- ERROR_EVT_VERSION_TOO_OLD
- ERROR_EVT_VERSION_TOO_NEW
- ERROR_EVT_CANNOT_OPEN_CHANNEL_OF_QUERY
- ERROR_EVT_PUBLISHER_DISABLED
- ERROR_EVT_FILTER_OUT_OF_RANGE
api_location:
- WinError.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0f6f0bd3e2805c02dad78c064b56a443bfbb596cf42f25e9b52ac7ba584f123
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120031939"
---
# <a name="windows-event-log-error-constants"></a>Windows Constantes d’erreur du journal des événements

voici les codes d’erreur que Windows journal des événements définit.

<dl> <dt>

<span id="ERROR_EVT_INVALID_CHANNEL_PATH"></span><span id="error_evt_invalid_channel_path"></span>**ERREUR \_ evt \_ \_ chemin de canal non valide \_**
</dt> <dd> <dl> <dt>

15000
</dt> <dt>



Le chemin d’accès au canal spécifié n’est pas valide.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_INVALID_QUERY"></span><span id="error_evt_invalid_query"></span>**ERREUR \_ evt \_ requête non valide \_**
</dt> <dd> <dl> <dt>

15001
</dt> <dt>



La requête spécifiée n’est pas valide.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_PUBLISHER_METADATA_NOT_FOUND"></span><span id="error_evt_publisher_metadata_not_found"></span>**ERREUR \_ evt \_ métadonnées du serveur de publication \_ \_ \_ introuvables**
</dt> <dd> <dl> <dt>

15002
</dt> <dt>



Les métadonnées du fournisseur sont introuvables dans la ressource.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_EVENT_TEMPLATE_NOT_FOUND"></span><span id="error_evt_event_template_not_found"></span>**le \_ modèle d’événement d’erreur evt est \_ \_ \_ \_ introuvable**
</dt> <dd> <dl> <dt>

15003
</dt> <dt>



Le modèle d’une définition d’événement est introuvable dans la ressource.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_INVALID_PUBLISHER_NAME"></span><span id="error_evt_invalid_publisher_name"></span>**ERREUR \_ evt \_ \_ nom d’éditeur non valide \_**
</dt> <dd> <dl> <dt>

15004
</dt> <dt>



Le nom du fournisseur spécifié n’est pas valide.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_INVALID_EVENT_DATA"></span><span id="error_evt_invalid_event_data"></span>**ERREUR \_ evt \_ \_ données d’événement non valides \_**
</dt> <dd> <dl> <dt>

15005
</dt> <dt>



Les données d’événement générées par le fournisseur ne sont pas compatibles avec la définition de modèle d’événement dans le manifeste du fournisseur.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_CHANNEL_NOT_FOUND"></span><span id="error_evt_channel_not_found"></span>**ERREUR \_ de \_ canal \_ evt \_ introuvable**
</dt> <dd> <dl> <dt>

15007
</dt> <dt>



Le canal spécifié est introuvable. Vérifiez la configuration du canal.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_MALFORMED_XML_TEXT"></span><span id="error_evt_malformed_xml_text"></span>**ERREUR \_ evt \_ \_ texte XML mal formé \_**
</dt> <dd> <dl> <dt>

15008
</dt> <dt>



Le texte XML spécifié n’est pas correctement formé. Pour plus d’informations, appelez la fonction [**EvtGetExtendedStatus**](/windows/desktop/api/WinEvt/nf-winevt-evtgetextendedstatus) .


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_SUBSCRIPTION_TO_DIRECT_CHANNEL"></span><span id="error_evt_subscription_to_direct_channel"></span>**ERREUR \_ evt \_ abonnement \_ au \_ \_ canal direct**
</dt> <dd> <dl> <dt>

15009
</dt> <dt>



Vous ne pouvez pas vous abonner à un canal d’analyse ou de débogage ; les événements d’un canal d’analyse ou de débogage sont directement dirigés vers un fichier journal et ne peuvent pas être abonnés à.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_CONFIGURATION_ERROR"></span><span id="error_evt_configuration_error"></span>**erreur de configuration de l’erreur \_ evt \_ \_**
</dt> <dd> <dl> <dt>

15010
</dt> <dt>



Une erreur de configuration s'est produite.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_QUERY_RESULT_STALE"></span><span id="error_evt_query_result_stale"></span>**ERREUR \_ evt \_ résultat de la requête \_ \_ obsolète**
</dt> <dd> <dl> <dt>

15011
</dt> <dt>



Le résultat de la requête n’est pas valide. Cela peut être dû au fait que le journal est effacé ou basculé après la création du résultat de la requête. Libérez l’objet résultat de la requête et réexécutez la requête.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_QUERY_RESULT_INVALID_POSITION"></span><span id="error_evt_query_result_invalid_position"></span>**ERREUR \_ evt \_ résultat de la requête- \_ \_ position non valide \_**
</dt> <dd> <dl> <dt>

15012
</dt> <dt>



Le curseur du résultat de la requête ne pointe pas vers une position valide.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_NON_VALIDATING_MSXML"></span><span id="error_evt_non_validating_msxml"></span>**ERREUR \_ evt \_ non \_ validant \_ MSXML**
</dt> <dd> <dl> <dt>

15013
</dt> <dt>



l’analyseur de MSXML inscrit ne prend pas en charge la validation.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_FILTER_ALREADYSCOPED"></span><span id="error_evt_filter_alreadyscoped"></span>**ERREUR \_ evt \_ Filter \_ ALREADYSCOPED**
</dt> <dd> <dl> <dt>

15014
</dt> <dt>



Une expression ne peut être suivie d’une modification de l’étendue que si l’expression est évaluée à un ensemble de nœuds et qu’elle ne fait pas déjà partie d’une autre modification de l’opération d’étendue.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_FILTER_NOTELTSET"></span><span id="error_evt_filter_noteltset"></span>**ERREUR \_ evt \_ Filter \_ NOTELTSET**
</dt> <dd> <dl> <dt>

15015
</dt> <dt>



Impossible d’effectuer une opération d’étape à partir d’un terme qui ne représente pas un ensemble d’éléments.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_FILTER_INVARG"></span><span id="error_evt_filter_invarg"></span>**ERREUR \_ evt \_ Filter \_ INVARG**
</dt> <dd> <dl> <dt>

15016
</dt> <dt>



Les arguments sur le côté gauche d’un opérateur binaire doivent être des attributs, des nœuds ou des variables, et les arguments à droite doivent être des constantes.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_FILTER_INVTEST"></span><span id="error_evt_filter_invtest"></span>**ERREUR \_ evt \_ Filter \_ INVTEST**
</dt> <dd> <dl> <dt>

15017
</dt> <dt>



Une opération d’étape doit impliquer un test de nœud ou, dans le cas d’un prédicat, une expression algébrique sur laquelle tester chaque nœud de l’ensemble de nœuds identifié par l’ensemble de nœuds précédent peut être évaluée.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_FILTER_INVTYPE"></span><span id="error_evt_filter_invtype"></span>**ERREUR \_ evt \_ Filter \_ INVTYPE**
</dt> <dd> <dl> <dt>

15018
</dt> <dt>



Ce type de données n’est pas pris en charge.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_FILTER_PARSEERR"></span><span id="error_evt_filter_parseerr"></span>**ERREUR \_ evt \_ Filter \_ PARSEERR**
</dt> <dd> <dl> <dt>

15019
</dt> <dt>



Une erreur de syntaxe s’est produite à la position spécifiée.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_FILTER_UNSUPPORTEDOP"></span><span id="error_evt_filter_unsupportedop"></span>**ERREUR \_ evt \_ Filter \_ UNSUPPORTEDOP**
</dt> <dd> <dl> <dt>

15020
</dt> <dt>



Cet opérateur n’est pas pris en charge par cette implémentation du filtre.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_FILTER_UNEXPECTEDTOKEN"></span><span id="error_evt_filter_unexpectedtoken"></span>**ERREUR \_ evt \_ Filter \_ UNEXPECTEDTOKEN**
</dt> <dd> <dl> <dt>

15021
</dt> <dt>



Le jeton rencontré était inattendu.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_INVALID_OPERATION_OVER_ENABLED_DIRECT_CHANNEL"></span><span id="error_evt_invalid_operation_over_enabled_direct_channel"></span>**ERREUR \_ evt \_ opération non valide \_ \_ sur le \_ \_ canal direct activé \_**
</dt> <dd> <dl> <dt>

15022
</dt> <dt>



L’opération demandée ne peut pas être effectuée sur un canal d’analyse ou de débogage activé. Vous devez désactiver le canal avant d’effectuer l’opération demandée.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_INVALID_CHANNEL_PROPERTY_VALUE"></span><span id="error_evt_invalid_channel_property_value"></span>**ERREUR \_ evt \_ \_ valeur de \_ propriété de canal non valide \_**
</dt> <dd> <dl> <dt>

15023
</dt> <dt>



La propriété de canal contient une valeur qui n’est pas valide. Le type de la valeur n’est peut-être pas valide, la valeur est peut-être hors limites ou la valeur ne peut pas être mise à jour ou n’est pas prise en charge pour ce type de canal.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_INVALID_PUBLISHER_PROPERTY_VALUE"></span><span id="error_evt_invalid_publisher_property_value"></span>**ERREUR \_ evt \_ valeur de la \_ propriété Publisher non valide \_ \_**
</dt> <dd> <dl> <dt>

15024
</dt> <dt>



La propriété du fournisseur contient une valeur qui n’est pas valide. Le type de la valeur n’est peut-être pas valide, la valeur est peut-être hors limites ou la valeur ne peut pas être mise à jour ou n’est pas prise en charge pour ce type de fournisseur.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_CHANNEL_CANNOT_ACTIVATE"></span><span id="error_evt_channel_cannot_activate"></span>**ERREUR \_ \_ Impossible d' \_ \_ activer le canal evt**
</dt> <dd> <dl> <dt>

15025
</dt> <dt>



Le canal n’a pas pu être activé.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_FILTER_TOO_COMPLEX"></span><span id="error_evt_filter_too_complex"></span>**ERREUR \_ de \_ filtre evt \_ trop \_ complexe**
</dt> <dd> <dl> <dt>

15026
</dt> <dt>



L’expression XPath a dépassé la complexité prise en charge. Simplifiez l’expression ou Fractionnez-la en deux ou plusieurs expressions simples.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_MESSAGE_NOT_FOUND"></span><span id="error_evt_message_not_found"></span>**MESSAGE d’erreur \_ evt \_ \_ \_ introuvable**
</dt> <dd> <dl> <dt>

15027
</dt> <dt>



La ressource de message est présente, mais le message est introuvable dans la chaîne ou la table de messages.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_MESSAGE_ID_NOT_FOUND"></span><span id="error_evt_message_id_not_found"></span>**ERREUR \_ evt \_ ID de message \_ \_ \_ introuvable**
</dt> <dd> <dl> <dt>

15028
</dt> <dt>



L’identificateur de message est introuvable.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_UNRESOLVED_VALUE_INSERT"></span><span id="error_evt_unresolved_value_insert"></span>**ERREUR \_ evt \_ - \_ Insérer une valeur non résolue \_**
</dt> <dd> <dl> <dt>

15029
</dt> <dt>



La chaîne de substitution pour l’index d’insertion est introuvable.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_UNRESOLVED_PARAMETER_INSERT"></span><span id="error_evt_unresolved_parameter_insert"></span>**ERREUR \_ evt \_ - \_ Insérer un paramètre non résolu \_**
</dt> <dd> <dl> <dt>

15030
</dt> <dt>



La chaîne de description de la référence de paramètre (%1) est introuvable.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_MAX_INSERTS_REACHED"></span><span id="error_evt_max_inserts_reached"></span>**ERREUR \_ evt \_ nombre maximal d' \_ insertions \_ atteint**
</dt> <dd> <dl> <dt>

15031
</dt> <dt>



Le nombre maximal de remplacements a été atteint.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_EVENT_DEFINITION_NOT_FOUND"></span><span id="error_evt_event_definition_not_found"></span>**ERREUR \_ evt \_ définition de l’événement \_ \_ \_ introuvable**
</dt> <dd> <dl> <dt>

15032
</dt> <dt>



La définition de l’événement est introuvable pour l’identificateur d’événement.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_MESSAGE_LOCALE_NOT_FOUND"></span><span id="error_evt_message_locale_not_found"></span>**ERREUR \_ evt \_ message \_ local \_ \_ introuvable**
</dt> <dd> <dl> <dt>

15033
</dt> <dt>



La ressource spécifique aux paramètres régionaux pour le message souhaité n’est pas présente.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_VERSION_TOO_OLD"></span><span id="error_evt_version_too_old"></span>**ERREUR \_ evt \_ version \_ trop \_ ancienne**
</dt> <dd> <dl> <dt>

15034
</dt> <dt>



La ressource est trop ancienne pour être compatible.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_VERSION_TOO_NEW"></span><span id="error_evt_version_too_new"></span>**ERREUR \_ evt \_ version \_ insuffisante \_**
</dt> <dd> <dl> <dt>

15035
</dt> <dt>



La ressource est trop nouvelle pour être compatible.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_CANNOT_OPEN_CHANNEL_OF_QUERY"></span><span id="error_evt_cannot_open_channel_of_query"></span>**ERREUR \_ evt \_ Impossible \_ d’ouvrir le \_ canal \_ de la \_ requête**
</dt> <dd> <dl> <dt>

15036
</dt> <dt>



Impossible d’ouvrir le canal à l’index spécifié de la requête.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_PUBLISHER_DISABLED"></span><span id="error_evt_publisher_disabled"></span>**ERREUR \_ evt serveur de \_ publication \_ désactivé**
</dt> <dd> <dl> <dt>

15037
</dt> <dt>



Le fournisseur a été désactivé et ses ressources ne sont pas disponibles. Cela peut se produire lors de la désinstallation ou de la mise à niveau du fournisseur.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_FILTER_OUT_OF_RANGE"></span><span id="error_evt_filter_out_of_range"></span>**ERREUR \_ \_ de filtre \_ evt \_ hors \_ limites**
</dt> <dd> <dl> <dt>

15038
</dt> <dt>



Tentative de création d’un type numérique qui est en dehors de sa plage valide.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>WinError. h</dt> </dl> |



 

 





