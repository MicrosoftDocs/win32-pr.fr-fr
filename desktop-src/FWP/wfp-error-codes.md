---
title: Codes d’erreur WFP (Winerror.h)
description: Codes d’erreur spécifiques à WFP.
ms.assetid: 11f3085a-f044-4a78-b47a-59b9086562bf
topic_type:
- apiref
api_name:
- FWP_E_CALLOUT_NOT_FOUND
- FWP_E_CONDITION_NOT_FOUND
- FWP_E_FILTER_NOT_FOUND
- FWP_E_LAYER_NOT_FOUND
- FWP_E_PROVIDER_NOT_FOUND
- FWP_E_PROVIDER_CONTEXT_NOT_FOUND
- FWP_E_SUBLAYER_NOT_FOUND
- FWP_E_NOT_FOUND
- FWP_E_ALREADY_EXISTS
- FWP_E_IN_USE
- FWP_E_DYNAMIC_SESSION_IN_PROGRESS
- FWP_E_WRONG_SESSION
- FWP_E_NO_TXN_IN_PROGRESS
- FWP_E_TXN_IN_PROGRESS
- FWP_E_TXN_ABORTED
- FWP_E_SESSION_ABORTED
- FWP_E_INCOMPATIBLE_TXN
- FWP_E_TIMEOUT
- FWP_E_NET_EVENTS_DISABLED
- FWP_E_INCOMPATIBLE_LAYER
- FWP_E_KM_CLIENTS_ONLY
- FWP_E_LIFETIME_MISMATCH
- FWP_E_BUILTIN_OBJECT
- FWP_E_TOO_MANY_CALLOUTS
- FWP_E_NOTIFICATION_DROPPED
- FWP_E_TRAFFIC_MISMATCH
- FWP_E_INCOMPATIBLE_SA_STATE
- FWP_E_NULL_POINTER
- FWP_E_INVALID_ENUMERATOR
- FWP_E_INVALID_FLAGS
- FWP_E_INVALID_NET_MASK
- FWP_E_INVALID_RANGE
- FWP_E_INVALID_INTERVAL
- FWP_E_ZERO_LENGTH_ARRAY
- FWP_E_NULL_DISPLAY_NAME
- FWP_E_INVALID_ACTION_TYPE
- FWP_E_INVALID_WEIGHT
- FWP_E_MATCH_TYPE_MISMATCH
- FWP_E_TYPE_MISMATCH
- FWP_E_OUT_OF_BOUNDS
- FWP_E_RESERVED
- FWP_E_DUPLICATE_CONDITION
- FWP_E_DUPLICATE_KEYMOD
- FWP_E_ACTION_INCOMPATIBLE_WITH_LAYER
- FWP_E_ACTION_INCOMPATIBLE_WITH_SUBLAYER
- FWP_E_CONTEXT_INCOMPATIBLE_WITH_LAYER
- FWP_E_CONTEXT_INCOMPATIBLE_WITH_CALLOUT
- FWP_E_INCOMPATIBLE_AUTH_METHOD
- FWP_E_INCOMPATIBLE_DH_GROUP
- FWP_E_EM_NOT_SUPPORTED
- FWP_E_NEVER_MATCH
- FWP_E_PROVIDER_CONTEXT_MISMATCH
- FWP_E_INVALID_PARAMETER
- FWP_E_TOO_MANY_SUBLAYERS
- FWP_E_CALLOUT_NOTIFICATION_FAILED
- FWP_E_INVALID_AUTH_TRANSFORM
- FWP_E_INVALID_CIPHER_TRANSFORM
api_location:
- winerror.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a0e7ee1ab0364a31f136f0c0cdbf87f459225b1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466054"
---
# <a name="wfp-error-codes"></a>Codes d’erreur WFP

Les codes d’erreur spécifiques à la plateforme de filtrage Windows (WFP) sont les suivants.

<dl> <dt>

<span id="FWP_E_CALLOUT_NOT_FOUND"></span><span id="fwp_e_callout_not_found"></span>**le \_ CALLOUT E fwp est \_ \_ \_ introuvable**
</dt> <dd> <dl> <dt>

0x80320001
</dt> <dt>



La légende n’existe pas.


</dt> </dl> </dd> <dt>

<span id="FWP_E_CONDITION_NOT_FOUND"></span><span id="fwp_e_condition_not_found"></span>**la \_ condition fwp E est \_ \_ \_ introuvable**
</dt> <dd> <dl> <dt>

0x80320002
</dt> <dt>



La condition de filtre n’existe pas.


</dt> </dl> </dd> <dt>

<span id="FWP_E_FILTER_NOT_FOUND"></span><span id="fwp_e_filter_not_found"></span>**\_filtre fwp \_ E \_ \_ introuvable**
</dt> <dd> <dl> <dt>

0x80320003
</dt> <dt>



Le filtre n’existe pas.


</dt> </dl> </dd> <dt>

<span id="FWP_E_LAYER_NOT_FOUND"></span><span id="fwp_e_layer_not_found"></span>**\_couche E \_ fwp \_ \_ introuvable**
</dt> <dd> <dl> <dt>

0x80320004
</dt> <dt>



La couche n’existe pas.


</dt> </dl> </dd> <dt>

<span id="FWP_E_PROVIDER_NOT_FOUND"></span><span id="fwp_e_provider_not_found"></span>**\_fournisseur fwp \_ E \_ \_ introuvable**
</dt> <dd> <dl> <dt>

0x80320005
</dt> <dt>



Le fournisseur n’existe pas.


</dt> </dl> </dd> <dt>

<span id="FWP_E_PROVIDER_CONTEXT_NOT_FOUND"></span><span id="fwp_e_provider_context_not_found"></span>**\_contexte du fournisseur fwp E \_ \_ \_ \_ introuvable**
</dt> <dd> <dl> <dt>

0x80320006
</dt> <dt>



Le contexte du fournisseur n’existe pas.


</dt> </dl> </dd> <dt>

<span id="FWP_E_SUBLAYER_NOT_FOUND"></span><span id="fwp_e_sublayer_not_found"></span>**sous \_ - \_ couche fwp \_ E \_ introuvable**
</dt> <dd> <dl> <dt>

0x80320007
</dt> <dt>



La sous-couche n’existe pas.


</dt> </dl> </dd> <dt>

<span id="FWP_E_NOT_FOUND"></span><span id="fwp_e_not_found"></span>**FWP \_ E \_ \_ introuvable**
</dt> <dd> <dl> <dt>

0x80320008
</dt> <dt>



L'objet n'existe pas.

Les [fonctions \* IPsecSaContext](fwp-ipsec-functions.md) retournent cette erreur si l’ID de contexte sa est introuvable.


</dt> </dl> </dd> <dt>

<span id="FWP_E_ALREADY_EXISTS"></span><span id="fwp_e_already_exists"></span>**FWP \_ E \_ \_ existe déjà**
</dt> <dd> <dl> <dt>

0x80320009
</dt> <dt>



Un objet avec ce GUID ou le LUID existe déjà.


</dt> </dl> </dd> <dt>

<span id="FWP_E_IN_USE"></span><span id="fwp_e_in_use"></span>**FWP \_ E \_ en cours d' \_ utilisation**
</dt> <dd> <dl> <dt>

0x8032000A
</dt> <dt>



L’objet est référencé par d’autres objets, il ne peut donc pas être supprimé.


</dt> </dl> </dd> <dt>

<span id="FWP_E_DYNAMIC_SESSION_IN_PROGRESS"></span><span id="fwp_e_dynamic_session_in_progress"></span>**\_ \_ session dynamique fwp \_ E \_ en \_ cours**
</dt> <dd> <dl> <dt>

0x8032000B
</dt> <dt>



L’appel n’est pas autorisé à partir d’une session dynamique.


</dt> </dl> </dd> <dt>

<span id="FWP_E_WRONG_SESSION"></span><span id="fwp_e_wrong_session"></span>**FWP \_ E \_ session incorrecte \_**
</dt> <dd> <dl> <dt>

0x8032000C
</dt> <dt>



L’appel a été effectué à partir de la mauvaise session. il ne peut donc pas être terminé.


</dt> </dl> </dd> <dt>

<span id="FWP_E_NO_TXN_IN_PROGRESS"></span><span id="fwp_e_no_txn_in_progress"></span>**FWP \_ E \_ no \_ TXN \_ en \_ cours**
</dt> <dd> <dl> <dt>

0x8032000D
</dt> <dt>



L’appel doit être effectué dans une transaction explicite.


</dt> </dl> </dd> <dt>

<span id="FWP_E_TXN_IN_PROGRESS"></span><span id="fwp_e_txn_in_progress"></span>**FWP \_ E \_ TXN \_ en \_ cours**
</dt> <dd> <dl> <dt>

0x8032000E
</dt> <dt>



L’appel n’est pas autorisé dans une transaction explicite.


</dt> </dl> </dd> <dt>

<span id="FWP_E_TXN_ABORTED"></span><span id="fwp_e_txn_aborted"></span>**le \_ TXN fwp E a été \_ \_ abandonné**
</dt> <dd> <dl> <dt>

0x8032000F
</dt> <dt>



La transaction explicite a été annulée de force.


</dt> </dl> </dd> <dt>

<span id="FWP_E_SESSION_ABORTED"></span><span id="fwp_e_session_aborted"></span>**\_session fwp \_ E \_ abandonnée**
</dt> <dd> <dl> <dt>

0x80320010
</dt> <dt>



La session a été annulée.

Le descripteur de session doit être fermé en appelant [**FwpmEngineClose0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmengineclose0), même s’il n’est plus valide ; dans le cas contraire, l’État côté client est divulgué. Une nouvelle session doit être créée en appelant [**FwpmEngineOpen0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmengineopen0).


</dt> </dl> </dd> <dt>

<span id="FWP_E_INCOMPATIBLE_TXN"></span><span id="fwp_e_incompatible_txn"></span>**FWP \_ E \_ incompatible \_ TXN**
</dt> <dd> <dl> <dt>

0x80320011
</dt> <dt>



L’appel n’est pas autorisé à partir d’une transaction en lecture seule.


</dt> </dl> </dd> <dt>

<span id="FWP_E_TIMEOUT"></span><span id="fwp_e_timeout"></span>**\_ \_ délai d’expiration fwp E**
</dt> <dd> <dl> <dt>

0x80320012
</dt> <dt>



L’appel a expiré en attendant d’acquérir le verrou de transaction.


</dt> </dl> </dd> <dt>

<span id="FWP_E_NET_EVENTS_DISABLED"></span><span id="fwp_e_net_events_disabled"></span>**\_événements du \_ réseau fwp E \_ \_ désactivé**
</dt> <dd> <dl> <dt>

0x80320013
</dt> <dt>



La collection d’événements de diagnostics du réseau est désactivée.


</dt> </dl> </dd> <dt>

<span id="FWP_E_INCOMPATIBLE_LAYER"></span><span id="fwp_e_incompatible_layer"></span>**\_couche E non \_ compatible \_ fwp**
</dt> <dd> <dl> <dt>

0x80320014
</dt> <dt>



L’opération n’est pas prise en charge par la couche spécifiée.


</dt> </dl> </dd> <dt>

<span id="FWP_E_KM_CLIENTS_ONLY"></span><span id="fwp_e_km_clients_only"></span>**\_clients fwp \_ E \_ km \_ uniquement**
</dt> <dd> <dl> <dt>

0x80320015
</dt> <dt>



L’appel est autorisé uniquement pour les appelants en mode noyau.


</dt> </dl> </dd> <dt>

<span id="FWP_E_LIFETIME_MISMATCH"></span><span id="fwp_e_lifetime_mismatch"></span>**non-concordance de la durée de vie de FWP \_ E \_ \_**
</dt> <dd> <dl> <dt>

0x80320016
</dt> <dt>



L’appel a tenté d’associer deux objets avec des durées de vie incompatibles.

Pour plus d’informations sur la durée de vie des objets et l’Association d’objets, consultez [gestion des objets](object-management.md) .


</dt> </dl> </dd> <dt>

<span id="FWP_E_BUILTIN_OBJECT"></span><span id="fwp_e_builtin_object"></span>**\_ \_ objet intégré fwp \_ E**
</dt> <dd> <dl> <dt>

0x80320017
</dt> <dt>



L’objet étant intégré, il ne peut pas être supprimé.


</dt> </dl> </dd> <dt>

<span id="FWP_E_TOO_MANY_CALLOUTS"></span><span id="fwp_e_too_many_callouts"></span>**FWP \_ E \_ trop \_ de \_ légendes**
</dt> <dd> <dl> <dt>

0x80320018
</dt> <dt>



Le nombre maximal de légendes a été atteint.

Au maximum, 100 000 légendes peuvent être inscrites en même temps.


</dt> </dl> </dd> <dt>

<span id="FWP_E_NOTIFICATION_DROPPED"></span><span id="fwp_e_notification_dropped"></span>**\_notification fwp \_ E \_ supprimée**
</dt> <dd> <dl> <dt>

0x80320019
</dt> <dt>



Une notification n’a pas pu être remise parce qu’une file d’attente de messages est à sa capacité maximale.


</dt> </dl> </dd> <dt>

<span id="FWP_E_TRAFFIC_MISMATCH"></span><span id="fwp_e_traffic_mismatch"></span>**non \_ - \_ concordance du trafic fwp E \_**
</dt> <dd> <dl> <dt>

0x8032001A
</dt> <dt>



Les paramètres du trafic réseau ne correspondent pas à ceux du contexte d’association de sécurité.

[**IPsecSaContextGetSpi0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextgetspi0) peut être appelé plusieurs fois, mais l’appelant doit spécifier les mêmes [**\_ TRAFFIC0 IPSec**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_traffic0) à chaque fois. Cette erreur est retournée si un appel suivant fournit un **\_ TRAFFIC0 IPSec** différent.


</dt> </dl> </dd> <dt>

<span id="FWP_E_INCOMPATIBLE_SA_STATE"></span><span id="fwp_e_incompatible_sa_state"></span>**l' \_ \_ État de sa incompatibilité avec fwp E \_ \_**
</dt> <dd> <dl> <dt>

0x8032001B
</dt> <dt>



L’appel n’est pas autorisé pour l’état actuel de l’Association de sécurité.

Les fonctions de contexte SA doivent être appelées dans un ordre spécifique :

-   [**IPsecSaContextCreate0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextcreate0)
-   [**IPsecSaContextGetSpi0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextgetspi0)
-   [**IPsecSaContextAddInbound0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextaddinbound0)
-   [**IPsecSaContextAddOutbound0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextaddoutbound0)

Cette erreur est retournée si elles sont appelées dans le désordre.


</dt> </dl> </dd> <dt>

<span id="FWP_E_NULL_POINTER"></span><span id="fwp_e_null_pointer"></span>**\_ \_ pointeur null fwp \_ E**
</dt> <dd> <dl> <dt>

0x8032001C
</dt> <dt>



Un pointeur requis a la valeur null.


</dt> </dl> </dd> <dt>

<span id="FWP_E_INVALID_ENUMERATOR"></span><span id="fwp_e_invalid_enumerator"></span>**FWP \_ E \_ énumérateur non valide \_**
</dt> <dd> <dl> <dt>

0x8032001D
</dt> <dt>



Une valeur d’énumérateur dans une structure est hors limites.


</dt> </dl> </dd> <dt>

<span id="FWP_E_INVALID_FLAGS"></span><span id="fwp_e_invalid_flags"></span>**FWP \_ E \_ indicateurs non valides \_**
</dt> <dd> <dl> <dt>

0x8032001E
</dt> <dt>



Le champ Indicateurs contient une valeur non valide.


</dt> </dl> </dd> <dt>

<span id="FWP_E_INVALID_NET_MASK"></span><span id="fwp_e_invalid_net_mask"></span>**FWP \_ E \_ \_ masque réseau non valide \_**
</dt> <dd> <dl> <dt>

0x8032001F
</dt> <dt>



Un masque de réseau n’est pas valide.


</dt> </dl> </dd> <dt>

<span id="FWP_E_INVALID_RANGE"></span><span id="fwp_e_invalid_range"></span>**FWP \_ E \_ plage non valide \_**
</dt> <dd> <dl> <dt>

0x80320020
</dt> <dt>



Une structure [**fwp \_ RANGE0**](/windows/desktop/api/Fwptypes/ns-fwptypes-fwp_range0) n’est pas valide.


</dt> </dl> </dd> <dt>

<span id="FWP_E_INVALID_INTERVAL"></span><span id="fwp_e_invalid_interval"></span>**FWP \_ E \_ intervalle non valide \_**
</dt> <dd> <dl> <dt>

0x80320021
</dt> <dt>



L’intervalle de temps n’est pas valide.


</dt> </dl> </dd> <dt>

<span id="FWP_E_ZERO_LENGTH_ARRAY"></span><span id="fwp_e_zero_length_array"></span>**\_tableau de \_ \_ longueur zéro fwp E \_**
</dt> <dd> <dl> <dt>

0x80320022
</dt> <dt>



Un tableau qui doit contenir au moins un élément a une longueur égale à zéro.


</dt> </dl> </dd> <dt>

<span id="FWP_E_NULL_DISPLAY_NAME"></span><span id="fwp_e_null_display_name"></span>**\_ \_ nom complet du null fwp E \_ \_**
</dt> <dd> <dl> <dt>

0x80320023
</dt> <dt>



Le champ **displayData.Name** ne peut pas être null.


</dt> </dl> </dd> <dt>

<span id="FWP_E_INVALID_ACTION_TYPE"></span><span id="fwp_e_invalid_action_type"></span>**FWP \_ E \_ \_ type d’action non valide \_**
</dt> <dd> <dl> <dt>

0x80320024
</dt> <dt>



Le type d’action n’est pas l’un des types d’action autorisés pour un filtre.


</dt> </dl> </dd> <dt>

<span id="FWP_E_INVALID_WEIGHT"></span><span id="fwp_e_invalid_weight"></span>**FWP \_ E \_ poids non valide \_**
</dt> <dd> <dl> <dt>

0x80320025
</dt> <dt>



Le poids du filtre n’est pas valide.

Pour plus d’informations, consultez [assignation de poids de filtre](filter-weight-assignment.md) .


</dt> </dl> </dd> <dt>

<span id="FWP_E_MATCH_TYPE_MISMATCH"></span><span id="fwp_e_match_type_mismatch"></span>**non \_ \_ concordance du \_ type de correspondance fwp E \_**
</dt> <dd> <dl> <dt>

0x80320026
</dt> <dt>



Une condition de filtre contient un type de correspondance qui n’est pas compatible avec les opérandes.

Pour plus d’informations, consultez [**\_ \_ type de correspondance fwp**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_match_type) .


</dt> </dl> </dd> <dt>

<span id="FWP_E_TYPE_MISMATCH"></span><span id="fwp_e_type_mismatch"></span>**incompatibilité de \_ type E fwp \_ \_**
</dt> <dd> <dl> <dt>

0x80320027
</dt> <dt>



Une structure [**fwp \_ VALUE0**](/windows/desktop/api/Fwptypes/ns-fwptypes-fwp_value0) ou une structure [**FWPM \_ condition \_ VALUE0**](/windows/desktop/api/Fwptypes/ns-fwptypes-fwp_condition_value0) est de type incorrect.


</dt> </dl> </dd> <dt>

<span id="FWP_E_OUT_OF_BOUNDS"></span><span id="fwp_e_out_of_bounds"></span>**FWP \_ E \_ hors \_ \_ limites**
</dt> <dd> <dl> <dt>

0x80320028
</dt> <dt>



Une valeur entière est en dehors de la plage autorisée.


</dt> </dl> </dd> <dt>

<span id="FWP_E_RESERVED"></span><span id="fwp_e_reserved"></span>**FWP \_ E \_ réservé**
</dt> <dd> <dl> <dt>

0x80320029
</dt> <dt>



Un champ réservé est différent de zéro.


</dt> </dl> </dd> <dt>

<span id="FWP_E_DUPLICATE_CONDITION"></span><span id="fwp_e_duplicate_condition"></span>**\_erreur fwp E \_ dupliquée \_**
</dt> <dd> <dl> <dt>

0x8032002A
</dt> <dt>



Un filtre ne peut pas contenir plusieurs conditions opérant sur un seul champ.


</dt> </dl> </dd> <dt>

<span id="FWP_E_DUPLICATE_KEYMOD"></span><span id="fwp_e_duplicate_keymod"></span>**FWP \_ E \_ KEYMOD en double \_**
</dt> <dd> <dl> <dt>

0x8032002B
</dt> <dt>



Une stratégie ne peut pas contenir plusieurs fois le même module de génération de clé.


</dt> </dl> </dd> <dt>

<span id="FWP_E_ACTION_INCOMPATIBLE_WITH_LAYER"></span><span id="fwp_e_action_incompatible_with_layer"></span>**l' \_ action fwp E n’est \_ \_ pas compatible \_ avec la \_ couche**
</dt> <dd> <dl> <dt>

0x8032002C
</dt> <dt>



Le type d’action n’est pas compatible avec la couche.


</dt> </dl> </dd> <dt>

<span id="FWP_E_ACTION_INCOMPATIBLE_WITH_SUBLAYER"></span><span id="fwp_e_action_incompatible_with_sublayer"></span>**l' \_ action fwp E n’est \_ \_ pas compatible \_ avec la sous- \_ couche**
</dt> <dd> <dl> <dt>

0x8032002D
</dt> <dt>



Le type d’action n’est pas compatible avec la sous-couche.


</dt> </dl> </dd> <dt>

<span id="FWP_E_CONTEXT_INCOMPATIBLE_WITH_LAYER"></span><span id="fwp_e_context_incompatible_with_layer"></span>**\_éditeur \_ de contexte fwp non \_ compatible avec la \_ \_ couche**
</dt> <dd> <dl> <dt>

0x8032002E
</dt> <dt>



Le contexte brut ou le contexte du fournisseur n’est pas compatible avec la couche.


</dt> </dl> </dd> <dt>

<span id="FWP_E_CONTEXT_INCOMPATIBLE_WITH_CALLOUT"></span><span id="fwp_e_context_incompatible_with_callout"></span>**\_contexte E \_ fwp \_ incompatible \_ avec la \_ légende**
</dt> <dd> <dl> <dt>

0x8032002F
</dt> <dt>



Le contexte brut ou le contexte du fournisseur n’est pas compatible avec la légende.


</dt> </dl> </dd> <dt>

<span id="FWP_E_INCOMPATIBLE_AUTH_METHOD"></span><span id="fwp_e_incompatible_auth_method"></span>**FWP \_ E ( \_ méthode d' \_ authentification incompatible \_ )**
</dt> <dd> <dl> <dt>

0x80320030
</dt> <dt>



La méthode d’authentification n’est pas compatible avec le type de stratégie.


</dt> </dl> </dd> <dt>

<span id="FWP_E_INCOMPATIBLE_DH_GROUP"></span><span id="fwp_e_incompatible_dh_group"></span>**FWP \_ E- \_ \_ groupe DH \_ incompatible**
</dt> <dd> <dl> <dt>

0x80320031L
</dt> <dt>



Le groupe de Diffie-Hellman n’est pas compatible avec le type de stratégie.


</dt> </dl> </dd> <dt>

<span id="FWP_E_EM_NOT_SUPPORTED"></span><span id="fwp_e_em_not_supported"></span>**FWP \_ E \_ em \_ non \_ pris en charge**
</dt> <dd> <dl> <dt>

0x80320032
</dt> <dt>



Une stratégie IKE ne peut pas contenir une stratégie en mode étendu.


</dt> </dl> </dd> <dt>

<span id="FWP_E_NEVER_MATCH"></span><span id="fwp_e_never_match"></span>**FWP \_ E \_ ne \_ correspond jamais**
</dt> <dd> <dl> <dt>

0x80320033
</dt> <dt>



Le modèle d’énumération ou l’abonnement ne correspondra jamais aux objets.


</dt> </dl> </dd> <dt>

<span id="FWP_E_PROVIDER_CONTEXT_MISMATCH"></span><span id="fwp_e_provider_context_mismatch"></span>**non \_ - \_ \_ concordance du contexte du fournisseur fwp E \_**
</dt> <dd> <dl> <dt>

0x80320034
</dt> <dt>



Le type du contexte du fournisseur est incorrect.


</dt> </dl> </dd> <dt>

<span id="FWP_E_INVALID_PARAMETER"></span><span id="fwp_e_invalid_parameter"></span>**FWP \_ E \_ paramètre non valide \_**
</dt> <dd> <dl> <dt>

0x80320035
</dt> <dt>



Le paramètre est incorrect.

Raisons possibles pour cette erreur :

-   [**FwpmIPsecTunnelAdd0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmipsectunneladd0) a été appelé sans définir le **\_ \_ point d’indicateur de tunnel FWPM de l’indicateur \_ \_ sur \_ point** et avec des conditions autres que local/adresse distante.
-   Chaîne Unicode non valide, ou chaîne Unicode qui contient des caractères non imprimables.


</dt> </dl> </dd> <dt>

<span id="FWP_E_TOO_MANY_SUBLAYERS"></span><span id="fwp_e_too_many_sublayers"></span>**FWP \_ E trop de sous- \_ \_ \_ couches**
</dt> <dd> <dl> <dt>

0x80320036
</dt> <dt>



Le nombre maximal de sous-couches a été atteint.

WFP prend en charge au maximum 2 6 sous-couches.


</dt> </dl> </dd> <dt>

<span id="FWP_E_CALLOUT_NOTIFICATION_FAILED"></span><span id="fwp_e_callout_notification_failed"></span>**échec de la \_ \_ notification de légende E \_ fwp \_**
</dt> <dd> <dl> <dt>

0x80320037
</dt> <dt>



La fonction de notification pour une légende a retourné une erreur.


</dt> </dl> </dd> <dt>

<span id="FWP_E_INVALID_AUTH_TRANSFORM"></span><span id="fwp_e_invalid_auth_transform"></span>**FWP \_ E \_ \_ transformation d’authentification non valide \_**
</dt> <dd> <dl> <dt>

0x80320038
</dt> <dt>



La transformation d’authentification IPsec n’est pas valide.


</dt> </dl> </dd> <dt>

<span id="FWP_E_INVALID_CIPHER_TRANSFORM"></span><span id="fwp_e_invalid_cipher_transform"></span>**FWP \_ E de la transformation de \_ \_ chiffrement non valide \_**
</dt> <dd> <dl> <dt>

0x80320039
</dt> <dt>



La transformation de chiffrement IPsec n’est pas valide.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Winerror. h</dt> </dl> |



 

 





