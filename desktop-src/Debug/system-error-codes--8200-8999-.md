---
description: Décrit les codes d’erreur 8200-8999 définis dans le fichier d’en-tête WinError. h et est destiné aux développeurs.
ms.assetid: f16fdfa3-b080-47ee-a7dd-241fe2d24278
title: Codes d’erreur système (8200-8999) (WinError. h)
ms.topic: reference
ms.date: 07/18/2019
ms.openlocfilehash: e9fd65025c3d51575cb0ece83cba14e0c62980d11a60ec6cb351919b6c7714c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119572959"
---
# <a name="system-error-codes-8200-8999"></a>Codes d’erreur système (8200-8999)

> [!NOTE]
> Ces informations sont destinées aux développeurs qui déboguent les erreurs système. pour les autres erreurs, telles que les problèmes de Windows Update, il existe une liste de ressources dans la page [codes d’erreur](system-error-codes.md) .

La liste suivante décrit les [codes d’erreur système](system-error-codes.md) pour les erreurs 8200 à 8999. Elles sont retournées par la fonction [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) lorsque de nombreuses fonctions échouent. Pour récupérer le texte de description de l’erreur dans votre application, utilisez la fonction [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) avec le **format \_ message \_ de \_** l’indicateur système.

<dl> <dt>

<span id="ERROR_DS_NOT_INSTALLED"></span><span id="error_ds_not_installed"></span>**ERREUR \_ DS \_ non \_ installée**
</dt> <dd> <dl> <dt>

8200 (0x2008)
</dt> <dt>



Une erreur s’est produite lors de l’installation du service d’annuaire. Pour plus d’informations, consultez le journal des événements.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_MEMBERSHIP_EVALUATED_LOCALLY"></span><span id="error_ds_membership_evaluated_locally"></span>**ERREUR d' \_ appartenance aux services DS \_ \_ évaluée \_ localement**
</dt> <dd> <dl> <dt>

8201 (0x2009)
</dt> <dt>



Le service d’annuaire a évalué les appartenances aux groupes localement.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_ATTRIBUTE_OR_VALUE"></span><span id="error_ds_no_attribute_or_value"></span>**ERREUR \_ DS \_ aucun \_ attribut \_ ou \_ valeur**
</dt> <dd> <dl> <dt>

8202 (0x200A)
</dt> <dt>



L’attribut ou la valeur de service d’annuaire spécifié n’existe pas.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INVALID_ATTRIBUTE_SYNTAX"></span><span id="error_ds_invalid_attribute_syntax"></span>**ERREUR \_ de \_ \_ syntaxe d’attribut non valide du service d’annuaire \_**
</dt> <dd> <dl> <dt>

8203 (0x200B)
</dt> <dt>



La syntaxe d’attribut spécifiée pour le service d’annuaire n’est pas valide.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ATTRIBUTE_TYPE_UNDEFINED"></span><span id="error_ds_attribute_type_undefined"></span>**ERREUR \_ de \_ type d’attribut DS \_ \_ non défini**
</dt> <dd> <dl> <dt>

8204 (0x200C)
</dt> <dt>



Le type d’attribut spécifié au service d’annuaire n’est pas défini.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ATTRIBUTE_OR_VALUE_EXISTS"></span><span id="error_ds_attribute_or_value_exists"></span>**l' \_ attribut ou la valeur du service d’annuaire d’erreurs \_ \_ \_ \_ existe**
</dt> <dd> <dl> <dt>

8205 (0x200D)
</dt> <dt>



La valeur ou l’attribut de service d’annuaire spécifié existe déjà.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_BUSY"></span><span id="error_ds_busy"></span>**ERREUR \_ DS \_ occupé**
</dt> <dd> <dl> <dt>

8206 (0x200E)
</dt> <dt>



Le service d’annuaire est occupé.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_UNAVAILABLE"></span><span id="error_ds_unavailable"></span>**ERREUR \_ DS \_ non disponible**
</dt> <dd> <dl> <dt>

8207 (0x200F)
</dt> <dt>



Le service d’annuaire n’est pas disponible.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_RIDS_ALLOCATED"></span><span id="error_ds_no_rids_allocated"></span>**ERREUR \_ DS \_ aucun \_ RID \_ alloué**
</dt> <dd> <dl> <dt>

8208 (0x2010)
</dt> <dt>



Le service d'annuaire n'a pas pu allouer un identificateur relatif.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_MORE_RIDS"></span><span id="error_ds_no_more_rids"></span>**ERREUR \_ DS \_ aucun \_ autre \_ RID**
</dt> <dd> <dl> <dt>

8209 (0x2011)
</dt> <dt>



Le service d’annuaire a épuisé le pool d’identificateurs relatifs.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INCORRECT_ROLE_OWNER"></span><span id="error_ds_incorrect_role_owner"></span>**ERREUR \_ \_ propriétaire du \_ rôle incorrect DS \_**
</dt> <dd> <dl> <dt>

8210 (0x2012)
</dt> <dt>



L’opération demandée n’a pas pu être effectuée car le service d’annuaire n’est pas le maître pour ce type d’opération.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_RIDMGR_INIT_ERROR"></span><span id="error_ds_ridmgr_init_error"></span>**erreur d’initialisation de l' \_ \_ RIDMGR DS \_ \_**
</dt> <dd> <dl> <dt>

8211 (0x2013)
</dt> <dt>



Le service d’annuaire n’a pas pu initialiser le sous-système qui alloue des identificateurs relatifs.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_OBJ_CLASS_VIOLATION"></span><span id="error_ds_obj_class_violation"></span>**ERREUR \_ de \_ \_ violation de classe obj du DS \_**
</dt> <dd> <dl> <dt>

8212 (0x2014)
</dt> <dt>



L’opération demandée n’a pas satisfait à une ou plusieurs contraintes associées à la classe de l’objet.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_ON_NON_LEAF"></span><span id="error_ds_cant_on_non_leaf"></span>**ERREUR \_ DS \_ Impossible \_ sur un \_ non- \_ Terminal**
</dt> <dd> <dl> <dt>

8213 (0x2015)
</dt> <dt>



Le service d’annuaire peut effectuer l’opération demandée uniquement sur un objet feuille.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_ON_RDN"></span><span id="error_ds_cant_on_rdn"></span>**ERREUR \_ DS \_ Impossible \_ sur \_ RDN**
</dt> <dd> <dl> <dt>

8214 (0x2016)
</dt> <dt>



Le service d’annuaire ne peut pas effectuer l’opération demandée sur l’attribut RDN d’un objet.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_MOD_OBJ_CLASS"></span><span id="error_ds_cant_mod_obj_class"></span>**ERREUR DS inverser la \_ \_ \_ \_ \_ classe obj**
</dt> <dd> <dl> <dt>

8215 (0x2017)
</dt> <dt>



Le service d’annuaire a détecté une tentative de modification de la classe d’objet d’un objet.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CROSS_DOM_MOVE_ERROR"></span><span id="error_ds_cross_dom_move_error"></span>**erreur \_ de \_ \_ déplacement entre \_ DOM \_ des services d’annuaire**
</dt> <dd> <dl> <dt>

8216 (0x2018)
</dt> <dt>



L’opération de déplacement entre domaines demandée n’a pas pu être effectuée.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_GC_NOT_AVAILABLE"></span><span id="error_ds_gc_not_available"></span>**ERREUR \_ DS \_ GC \_ non \_ disponible**
</dt> <dd> <dl> <dt>

8217 (0x2019)
</dt> <dt>



Impossible de contacter le serveur de catalogue global.


</dt> </dl> </dd> <dt>

<span id="ERROR_SHARED_POLICY"></span><span id="error_shared_policy"></span>**\_stratégie partagée d’erreur \_**
</dt> <dd> <dl> <dt>

8218 (0x201A)
</dt> <dt>



L’objet de stratégie est partagé et ne peut être modifié qu’à la racine.


</dt> </dl> </dd> <dt>

<span id="ERROR_POLICY_OBJECT_NOT_FOUND"></span><span id="error_policy_object_not_found"></span>**objet de stratégie d’erreur \_ \_ \_ \_ introuvable**
</dt> <dd> <dl> <dt>

8219 (0x201B)
</dt> <dt>



L’objet de stratégie n’existe pas.


</dt> </dl> </dd> <dt>

<span id="ERROR_POLICY_ONLY_IN_DS"></span><span id="error_policy_only_in_ds"></span>**\_stratégie \_ d’erreur uniquement \_ dans \_ DS**
</dt> <dd> <dl> <dt>

8220 (0x201C)
</dt> <dt>



Les informations de stratégie demandées se trouvent uniquement dans le service d’annuaire.


</dt> </dl> </dd> <dt>

<span id="ERROR_PROMOTION_ACTIVE"></span><span id="error_promotion_active"></span>**PROMOTION d’erreur \_ \_ active**
</dt> <dd> <dl> <dt>

8221 (0x201D)
</dt> <dt>



Une promotion de contrôleur de domaine est actuellement active.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_PROMOTION_ACTIVE"></span><span id="error_no_promotion_active"></span>**ERREUR \_ aucune \_ promotion \_ active**
</dt> <dd> <dl> <dt>

8222 (0x201E)
</dt> <dt>



Une promotion de contrôleur de domaine n’est pas active actuellement.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_OPERATIONS_ERROR"></span><span id="error_ds_operations_error"></span>**erreur des opérations de l’annuaire d’erreurs \_ \_ \_**
</dt> <dd> <dl> <dt>

8224 (0x2020)
</dt> <dt>



Une erreur d’opération s’est produite.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_PROTOCOL_ERROR"></span><span id="error_ds_protocol_error"></span>**erreur de \_ protocole du service d’annuaire \_ \_**
</dt> <dd> <dl> <dt>

8225 (0x2021)
</dt> <dt>



Une erreur de protocole s'est produite.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_TIMELIMIT_EXCEEDED"></span><span id="error_ds_timelimit_exceeded"></span>**ERREUR \_ TIMELIMIT de l’annuaire de services \_ \_ dépassée**
</dt> <dd> <dl> <dt>

8226 (0x2022)
</dt> <dt>



La limite de temps pour cette requête a été dépassée.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SIZELIMIT_EXCEEDED"></span><span id="error_ds_sizelimit_exceeded"></span>**ERREUR \_ SIZELIMIT de l’annuaire de services \_ \_ dépassée**
</dt> <dd> <dl> <dt>

8227 (0x2023)
</dt> <dt>



La limite de taille de cette demande a été dépassée.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ADMIN_LIMIT_EXCEEDED"></span><span id="error_ds_admin_limit_exceeded"></span>**ERREUR \_ de \_ limite d’administration DS \_ \_ dépassée**
</dt> <dd> <dl> <dt>

8228 (0x2024)
</dt> <dt>



La limite administrative de cette demande a été dépassée.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_COMPARE_FALSE"></span><span id="error_ds_compare_false"></span>**ERREUR de \_ comparaison des services d’annuaire \_ \_**
</dt> <dd> <dl> <dt>

8229 (0x2025)
</dt> <dt>



La réponse de comparaison était false.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_COMPARE_TRUE"></span><span id="error_ds_compare_true"></span>**ERREUR de \_ comparaison des services d’annuaire \_ \_**
</dt> <dd> <dl> <dt>

8230 (0x2026)
</dt> <dt>



La réponse de comparaison a la valeur true.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_AUTH_METHOD_NOT_SUPPORTED"></span><span id="error_ds_auth_method_not_supported"></span>**ERREUR \_ de \_ méthode d’authentification DS \_ \_ non \_ prise en charge**
</dt> <dd> <dl> <dt>

8231 (0x2027)
</dt> <dt>



La méthode d’authentification demandée n’est pas prise en charge par le serveur.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_STRONG_AUTH_REQUIRED"></span><span id="error_ds_strong_auth_required"></span>**ERREUR d’authentification forte de l' \_ Annuaire de services \_ \_ \_ requise**
</dt> <dd> <dl> <dt>

8232 (0x2028)
</dt> <dt>



Une méthode d’authentification plus sécurisée est requise pour ce serveur.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INAPPROPRIATE_AUTH"></span><span id="error_ds_inappropriate_auth"></span>**ERREUR \_ d' \_ authentification incorrecte DS \_**
</dt> <dd> <dl> <dt>

8233 (0x2029)
</dt> <dt>



Authentification inappropriée.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_AUTH_UNKNOWN"></span><span id="error_ds_auth_unknown"></span>**ERREUR \_ d' \_ authentification DS \_ inconnue**
</dt> <dd> <dl> <dt>

8234 (0x202A)
</dt> <dt>



Le mécanisme d’authentification est inconnu.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_REFERRAL"></span><span id="error_ds_referral"></span>**Référence de l’annuaire d’erreurs \_ \_**
</dt> <dd> <dl> <dt>

8235 (0x202B)
</dt> <dt>



Une référence a été retournée à partir du serveur.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_UNAVAILABLE_CRIT_EXTENSION"></span><span id="error_ds_unavailable_crit_extension"></span>**erreur d’extension d’erreur de \_ service d’annuaire \_ non disponible \_ \_**
</dt> <dd> <dl> <dt>

8236 (0x202C)
</dt> <dt>



Le serveur ne prend pas en charge l’extension critique demandée.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CONFIDENTIALITY_REQUIRED"></span><span id="error_ds_confidentiality_required"></span>**confidentialité des erreurs du \_ service d’annuaire \_ \_ requise**
</dt> <dd> <dl> <dt>

8237 (0x202D)
</dt> <dt>



Cette demande requiert une connexion sécurisée.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INAPPROPRIATE_MATCHING"></span><span id="error_ds_inappropriate_matching"></span>**ERREUR \_ de \_ correspondance inappropriée DS \_**
</dt> <dd> <dl> <dt>

8238 (0x202E)
</dt> <dt>



Correspondance inappropriée.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CONSTRAINT_VIOLATION"></span><span id="error_ds_constraint_violation"></span>**ERREUR \_ de \_ violation de contrainte DS \_**
</dt> <dd> <dl> <dt>

8239 (0x202F)
</dt> <dt>



Une violation de contrainte s’est produite.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_SUCH_OBJECT"></span><span id="error_ds_no_such_object"></span>**ERREUR \_ DS \_ non- \_ objet de ce type \_**
</dt> <dd> <dl> <dt>

8240 (0x2030)
</dt> <dt>



Cet objet ne se trouve pas sur le serveur.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ALIAS_PROBLEM"></span><span id="error_ds_alias_problem"></span>**ERREUR d' \_ alias du service d’annuaire \_ \_**
</dt> <dd> <dl> <dt>

8241 (0x2031)
</dt> <dt>



Il y a un problème d’alias.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INVALID_DN_SYNTAX"></span><span id="error_ds_invalid_dn_syntax"></span>**ERREUR \_ DS \_ \_ syntaxe DN non valide \_**
</dt> <dd> <dl> <dt>

8242 (0x2032)
</dt> <dt>



Une syntaxe DN non valide a été spécifiée.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_IS_LEAF"></span><span id="error_ds_is_leaf"></span>**l’erreur \_ DS \_ est \_ feuille**
</dt> <dd> <dl> <dt>

8243 (0x2033)
</dt> <dt>



L’objet est un objet feuille.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ALIAS_DEREF_PROBLEM"></span><span id="error_ds_alias_deref_problem"></span>**ERREUR de l' \_ alias du service d’annuaire \_ \_ \_**
</dt> <dd> <dl> <dt>

8244 (0x2034)
</dt> <dt>



Il y a un problème de déréférencement d’alias.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_UNWILLING_TO_PERFORM"></span><span id="error_ds_unwilling_to_perform"></span>**ERREUR \_ \_ \_ d’exécution du service d' \_ Annuaire**
</dt> <dd> <dl> <dt>

8245 (0x2035)
</dt> <dt>



Le serveur ne souhaite pas traiter la demande.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_LOOP_DETECT"></span><span id="error_ds_loop_detect"></span>**ERREUR \_ de \_ détection de boucle DS \_**
</dt> <dd> <dl> <dt>

8246 (0x2036)
</dt> <dt>



Une boucle a été détectée.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NAMING_VIOLATION"></span><span id="error_ds_naming_violation"></span>**ERREUR \_ de \_ violation d’appellation des services d’annuaire \_**
</dt> <dd> <dl> <dt>

8247 (0x2037)
</dt> <dt>



Violation de nom.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_OBJECT_RESULTS_TOO_LARGE"></span><span id="error_ds_object_results_too_large"></span>**ERREUR de résultats de l' \_ \_ objet DS \_ \_ trop \_ grand**
</dt> <dd> <dl> <dt>

8248 (0x2038)
</dt> <dt>



Le jeu de résultats est trop grand.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_AFFECTS_MULTIPLE_DSAS"></span><span id="error_ds_affects_multiple_dsas"></span>**l’erreur \_ DS \_ affecte \_ plusieurs \_ DSA**
</dt> <dd> <dl> <dt>

8249 (0x2039)
</dt> <dt>



L’opération affecte plusieurs DSA.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SERVER_DOWN"></span><span id="error_ds_server_down"></span>**ERREUR \_ de \_ défaillance du serveur DS \_**
</dt> <dd> <dl> <dt>

8250 (0x203A)
</dt> <dt>



Le serveur n’est pas opérationnel.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_LOCAL_ERROR"></span><span id="error_ds_local_error"></span>**erreur de l’erreur \_ \_ locale DS \_**
</dt> <dd> <dl> <dt>

8251 (0x203B)
</dt> <dt>



Une erreur locale s’est produite.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ENCODING_ERROR"></span><span id="error_ds_encoding_error"></span>**erreur \_ d' \_ encodage du service d’annuaire \_**
</dt> <dd> <dl> <dt>

8252 (0x203C)
</dt> <dt>



Une erreur d’encodage s’est produite.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DECODING_ERROR"></span><span id="error_ds_decoding_error"></span>**erreur \_ de \_ décodage du service d’annuaire \_**
</dt> <dd> <dl> <dt>

8253 (0x203D)
</dt> <dt>



Une erreur de décodage s’est produite.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_FILTER_UNKNOWN"></span><span id="error_ds_filter_unknown"></span>**ERREUR de \_ filtre de service d’annuaire \_ \_ inconnu**
</dt> <dd> <dl> <dt>

8254 (0x203E)
</dt> <dt>



Le filtre de recherche ne peut pas être reconnu.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_PARAM_ERROR"></span><span id="error_ds_param_error"></span>**erreur \_ de \_ paramètre DS Error \_**
</dt> <dd> <dl> <dt>

8255 (0x203F)
</dt> <dt>



Un ou plusieurs paramètres ne sont pas conformes.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NOT_SUPPORTED"></span><span id="error_ds_not_supported"></span>**ERREUR \_ DS \_ non \_ prise en charge**
</dt> <dd> <dl> <dt>

8256 (0x2040)
</dt> <dt>



La méthode spécifiée n’est pas prise en charge.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_RESULTS_RETURNED"></span><span id="error_ds_no_results_returned"></span>**ERREUR \_ DS \_ aucun \_ résultat \_ retourné**
</dt> <dd> <dl> <dt>

8257 (0x2041)
</dt> <dt>



Aucun résultat n’a été retourné.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CONTROL_NOT_FOUND"></span><span id="error_ds_control_not_found"></span>**le contrôle de l’annuaire d’erreurs est \_ \_ \_ \_ introuvable**
</dt> <dd> <dl> <dt>

8258 (0x2042)
</dt> <dt>



Le contrôle spécifié n’est pas pris en charge par le serveur.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CLIENT_LOOP"></span><span id="error_ds_client_loop"></span>**ERREUR \_ de \_ boucle du client DS \_**
</dt> <dd> <dl> <dt>

8259 (0x2043)
</dt> <dt>



Une boucle de référence a été détectée par le client.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_REFERRAL_LIMIT_EXCEEDED"></span><span id="error_ds_referral_limit_exceeded"></span>**ERREUR \_ de \_ \_ dépassement de la limite de référence DS \_**
</dt> <dd> <dl> <dt>

8260 (0x2044)
</dt> <dt>



La limite de référence prédéfinie a été dépassée.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SORT_CONTROL_MISSING"></span><span id="error_ds_sort_control_missing"></span>**ERREUR de \_ contrôle de tri des services d’annuaire \_ \_ \_ manquante**
</dt> <dd> <dl> <dt>

8261 (0x2045)
</dt> <dt>



La recherche requiert un contrôle SORT.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_OFFSET_RANGE_ERROR"></span><span id="error_ds_offset_range_error"></span>**erreur d’erreur de \_ \_ plage de décalage DS \_ \_**
</dt> <dd> <dl> <dt>

8262 (0x2046)
</dt> <dt>



Les résultats de la recherche dépassent la plage de décalage spécifiée.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_RIDMGR_DISABLED"></span><span id="error_ds_ridmgr_disabled"></span>**ERREUR \_ DS \_ RIDMGR \_ désactivée**
</dt> <dd> <dl> <dt>

8263 (0x2047)
</dt> <dt>



Le service d’annuaire a détecté que le sous-système qui alloue des identificateurs relatifs est désactivé. Cela peut se produire comme un mécanisme de protection lorsque le système détermine qu’une partie importante des identificateurs relatifs (RID) est épuisée. Pour connaître <https://go.microsoft.com/fwlink/p/?linkid=228610> les étapes de diagnostic recommandées et la procédure à suivre pour réactiver la création de comptes, consultez.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ROOT_MUST_BE_NC"></span><span id="error_ds_root_must_be_nc"></span>**l’erreur la \_ \_ racine DS \_ doit \_ être \_ NC**
</dt> <dd> <dl> <dt>

8301 (0x206D)
</dt> <dt>



L’objet racine doit être le début d’un contexte d’appellation. L’objet racine ne peut pas avoir de parent instancié.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ADD_REPLICA_INHIBITED"></span><span id="error_ds_add_replica_inhibited"></span>**ERREUR d’ajout d’un \_ réplica au DS d’erreurs \_ \_ \_**
</dt> <dd> <dl> <dt>

8302 (0x206E)
</dt> <dt>



Impossible d’effectuer l’opération d’ajout de réplica. Le contexte d’appellation doit être accessible en écriture pour pouvoir créer le réplica.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ATT_NOT_DEF_IN_SCHEMA"></span><span id="error_ds_att_not_def_in_schema"></span>**ERREUR \_ DS \_ att \_ non \_ Def \_ dans le \_ schéma**
</dt> <dd> <dl> <dt>

8303 (0x206F)
</dt> <dt>



Une référence à un attribut qui n’est pas défini dans le schéma s’est produite.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_MAX_OBJ_SIZE_EXCEEDED"></span><span id="error_ds_max_obj_size_exceeded"></span>**ERREUR de dépassement de la \_ \_ taille maximale du \_ obj DS \_ \_**
</dt> <dd> <dl> <dt>

8304 (0x2070)
</dt> <dt>



La taille maximale d’un objet a été dépassée.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_OBJ_STRING_NAME_EXISTS"></span><span id="error_ds_obj_string_name_exists"></span>**le nom de la chaîne de l’erreur \_ DS \_ obj \_ \_ \_ existe**
</dt> <dd> <dl> <dt>

8305 (0x2071)
</dt> <dt>



Une tentative a été effectuée pour ajouter un objet au répertoire avec un nom qui est déjà en cours d’utilisation.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_RDN_DEFINED_IN_SCHEMA"></span><span id="error_ds_no_rdn_defined_in_schema"></span>**ERREUR \_ DS \_ non \_ RDN \_ définie \_ dans le \_ schéma**
</dt> <dd> <dl> <dt>

8306 (0x2072)
</dt> <dt>



Une tentative a été effectuée pour ajouter un objet d’une classe qui n’a pas de RDN défini dans le schéma.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_RDN_DOESNT_MATCH_SCHEMA"></span><span id="error_ds_rdn_doesnt_match_schema"></span>**ERREUR \_ DS \_ RDN ne pas \_ \_ correspondre au \_ schéma**
</dt> <dd> <dl> <dt>

8307 (0x2073)
</dt> <dt>



Une tentative d’ajout d’un objet à l’aide d’un RDN qui n’est pas le RDN défini dans le schéma a été effectuée.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_REQUESTED_ATTS_FOUND"></span><span id="error_ds_no_requested_atts_found"></span>**ERREUR \_ DS \_ aucun \_ \_ ATTS demandé \_ trouvé**
</dt> <dd> <dl> <dt>

8308 (0x2074)
</dt> <dt>



Aucun des attributs requis n’a été trouvé sur les objets.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_USER_BUFFER_TO_SMALL"></span><span id="error_ds_user_buffer_to_small"></span>**ERREUR \_ \_ \_ de mémoire tampon de l’utilisateur DS \_ \_ insuffisant**
</dt> <dd> <dl> <dt>

8309 (0x2075)
</dt> <dt>



La mémoire tampon de l’utilisateur est insuffisante.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ATT_IS_NOT_ON_OBJ"></span><span id="error_ds_att_is_not_on_obj"></span>**l’erreur \_ DS \_ att \_ n’est \_ pas \_ sur \_ obj**
</dt> <dd> <dl> <dt>

8310 (0x2076)
</dt> <dt>



L’attribut spécifié dans l’opération n’est pas présent sur l’objet.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ILLEGAL_MOD_OPERATION"></span><span id="error_ds_illegal_mod_operation"></span>**ERREUR de l' \_ \_ \_ opération mod illégale DS \_**
</dt> <dd> <dl> <dt>

8311 (0x2077)
</dt> <dt>



Opération de modification non autorisée. Certains aspects de la modification ne sont pas autorisés.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_OBJ_TOO_LARGE"></span><span id="error_ds_obj_too_large"></span>**ERREUR \_ DS \_ obj \_ trop \_ grande**
</dt> <dd> <dl> <dt>

8312 (0x2078)
</dt> <dt>



L’objet spécifié est trop grand.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_BAD_INSTANCE_TYPE"></span><span id="error_ds_bad_instance_type"></span>**ERREUR \_ de \_ \_ type d’instance incorrecte DS \_**
</dt> <dd> <dl> <dt>

8313 (0x2079)
</dt> <dt>



Le type d’instance spécifié n’est pas valide.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_MASTERDSA_REQUIRED"></span><span id="error_ds_masterdsa_required"></span>**ERREUR \_ MASTERDSA de l’annuaire de services \_ \_ requise**
</dt> <dd> <dl> <dt>

8314 (0x207A)
</dt> <dt>



L’opération doit être effectuée sur un DSA maître.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_OBJECT_CLASS_REQUIRED"></span><span id="error_ds_object_class_required"></span>**\_classe d' \_ objet Error DS \_ \_ obligatoire**
</dt> <dd> <dl> <dt>

8315 (0x207B)
</dt> <dt>



L’attribut de classe d’objet doit être spécifié.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_MISSING_REQUIRED_ATT"></span><span id="error_ds_missing_required_att"></span>**erreur indiquant que le \_ service d’annuaire est \_ manquant \_ \_ ATT**
</dt> <dd> <dl> <dt>

8316 (0x207C)
</dt> <dt>



Un attribut requis est manquant.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ATT_NOT_DEF_FOR_CLASS"></span><span id="error_ds_att_not_def_for_class"></span>**ERREUR \_ DS \_ att \_ non \_ Def \_ pour la \_ classe**
</dt> <dd> <dl> <dt>

8317 (0x207D)
</dt> <dt>



Une tentative de modification d’un objet pour inclure un attribut qui n’est pas légal pour sa classe a été effectuée.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ATT_ALREADY_EXISTS"></span><span id="error_ds_att_already_exists"></span>**l' \_ erreur \_ DS \_ att \_ existe déjà**
</dt> <dd> <dl> <dt>

8318 (0x207E)
</dt> <dt>



L’attribut spécifié est déjà présent sur l’objet.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_ADD_ATT_VALUES"></span><span id="error_ds_cant_add_att_values"></span>**ERREUR \_ DS \_ Impossible d' \_ Ajouter des \_ \_ valeurs ATT**
</dt> <dd> <dl> <dt>

8320 (0x2080)
</dt> <dt>



L’attribut spécifié n’est pas présent ou n’a pas de valeur.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SINGLE_VALUE_CONSTRAINT"></span><span id="error_ds_single_value_constraint"></span>**ERREUR \_ de \_ \_ contrainte de valeur unique \_ de l’annuaire**
</dt> <dd> <dl> <dt>

8321 (0x2081)
</dt> <dt>



Plusieurs valeurs ont été spécifiées pour un attribut qui ne peut avoir qu’une seule valeur.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_RANGE_CONSTRAINT"></span><span id="error_ds_range_constraint"></span>**ERREUR \_ de \_ contrainte de plage DS \_**
</dt> <dd> <dl> <dt>

8322 (0x2082)
</dt> <dt>



Une valeur pour l’attribut n’était pas dans la plage de valeurs acceptable.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ATT_VAL_ALREADY_EXISTS"></span><span id="error_ds_att_val_already_exists"></span>**l' \_ erreur \_ DS \_ att \_ Val \_ existe déjà**
</dt> <dd> <dl> <dt>

8323 (0x2083)
</dt> <dt>



La valeur spécifiée existe déjà.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_REM_MISSING_ATT"></span><span id="error_ds_cant_rem_missing_att"></span>**ERREUR DS inversion \_ \_ \_ REM \_ manquant \_ ATT**
</dt> <dd> <dl> <dt>

8324 (0x2084)
</dt> <dt>



Impossible de supprimer l’attribut, car il n’est pas présent sur l’objet.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_REM_MISSING_ATT_VAL"></span><span id="error_ds_cant_rem_missing_att_val"></span>**erreur Impossible de trouver une erreur dans \_ DS \_ \_ \_ \_ \_ Val**
</dt> <dd> <dl> <dt>

8325 (0x2085)
</dt> <dt>



La valeur de l’attribut ne peut pas être supprimée, car elle n’est pas présente sur l’objet.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ROOT_CANT_BE_SUBREF"></span><span id="error_ds_root_cant_be_subref"></span>**ERREUR \_ la \_ racine \_ DS \_ ne peut pas être \_ SUBREF**
</dt> <dd> <dl> <dt>

8326 (0x2086)
</dt> <dt>



L’objet racine spécifié ne peut pas être un subref.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_CHAINING"></span><span id="error_ds_no_chaining"></span>**ERREUR de chaînage du service d' \_ annuaire \_ \_**
</dt> <dd> <dl> <dt>

8327 (0x2087)
</dt> <dt>



Le chaînage n’est pas autorisé.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_CHAINED_EVAL"></span><span id="error_ds_no_chained_eval"></span>**ERREUR \_ DS \_ sans \_ chaîne \_ eval**
</dt> <dd> <dl> <dt>

8328 (0x2088)
</dt> <dt>



L’évaluation chaînée n’est pas autorisée.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_PARENT_OBJECT"></span><span id="error_ds_no_parent_object"></span>**ERREUR \_ DS \_ aucun \_ \_ objet parent**
</dt> <dd> <dl> <dt>

8329 (0x2089)
</dt> <dt>



L'opération n'a pas pu être effectuée car le parent de l'objet n'est pas instancié ou a été supprimé.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_PARENT_IS_AN_ALIAS"></span><span id="error_ds_parent_is_an_alias"></span>**ERREUR \_ le \_ parent DS \_ est \_ un \_ alias**
</dt> <dd> <dl> <dt>

8330 (0x208A)
</dt> <dt>



Le fait de disposer d’un parent qui est un alias n’est pas autorisé. Les alias sont des objets feuilles.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_MIX_MASTER_AND_REPS"></span><span id="error_ds_cant_mix_master_and_reps"></span>**ERREUR \_ de combinaison du maître d’erreurs DS \_ \_ \_ \_ et des \_ représentants**
</dt> <dd> <dl> <dt>

8331 (0x208B)
</dt> <dt>



L’objet et le parent doivent être du même type, qu’il s’agisse de maîtres ou de deux réplicas.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CHILDREN_EXIST"></span><span id="error_ds_children_exist"></span>**ERREUR \_ les \_ enfants DS \_ existent**
</dt> <dd> <dl> <dt>

8332 (0x208C)
</dt> <dt>



Impossible d’effectuer l’opération, car des objets enfants existent. Cette opération ne peut être effectuée que sur un objet feuille.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_OBJ_NOT_FOUND"></span><span id="error_ds_obj_not_found"></span>**ERREUR \_ DS \_ obj \_ \_ introuvable**
</dt> <dd> <dl> <dt>

8333 (0x208D)
</dt> <dt>



Objet répertoire introuvable.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ALIASED_OBJ_MISSING"></span><span id="error_ds_aliased_obj_missing"></span>**\_obj avec alias DS d’erreur \_ \_ \_ manquant**
</dt> <dd> <dl> <dt>

8334 (0x208E)
</dt> <dt>



L’objet avec alias est manquant.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_BAD_NAME_SYNTAX"></span><span id="error_ds_bad_name_syntax"></span>**ERREUR \_ de \_ \_ syntaxe de nom incorrect DS \_**
</dt> <dd> <dl> <dt>

8335 (0x208F)
</dt> <dt>



La syntaxe du nom de l’objet est incorrecte.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ALIAS_POINTS_TO_ALIAS"></span><span id="error_ds_alias_points_to_alias"></span>**l' \_ \_ alias \_ d’erreur \_ du service d’annuaire pointe vers l' \_ alias**
</dt> <dd> <dl> <dt>

8336 (0x2090)
</dt> <dt>



Un alias ne peut pas faire référence à un autre alias.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_DEREF_ALIAS"></span><span id="error_ds_cant_deref_alias"></span>**ERREUR DS inverse \_ \_ \_ Deref \_ alias**
</dt> <dd> <dl> <dt>

8337 (0x2091)
</dt> <dt>



L’alias ne peut pas être déréférencé.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_OUT_OF_SCOPE"></span><span id="error_ds_out_of_scope"></span>**ERREUR \_ \_ du service \_ d’annuaire hors de l' \_ étendue**
</dt> <dd> <dl> <dt>

8338 (0x2092)
</dt> <dt>



L’opération est hors de portée.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_OBJECT_BEING_REMOVED"></span><span id="error_ds_object_being_removed"></span>**ERREUR de suppression de l' \_ \_ objet DS \_ \_**
</dt> <dd> <dl> <dt>

8339 (0x2093)
</dt> <dt>



L’opération ne peut pas continuer, car l’objet est en cours de suppression.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_DELETE_DSA_OBJ"></span><span id="error_ds_cant_delete_dsa_obj"></span>**ERREUR \_ DS \_ Impossible de \_ supprimer le \_ DSA \_ obj**
</dt> <dd> <dl> <dt>

8340 (0x2094)
</dt> <dt>



Impossible de supprimer l’objet DSA.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_GENERIC_ERROR"></span><span id="error_ds_generic_error"></span>**erreur \_ générique de l’annuaire de services \_ \_**
</dt> <dd> <dl> <dt>

8341 (0x2095)
</dt> <dt>



Une erreur de service d’annuaire s’est produite.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DSA_MUST_BE_INT_MASTER"></span><span id="error_ds_dsa_must_be_int_master"></span>**l’erreur le \_ \_ DSA DS \_ doit \_ être de \_ type int \_ maître**
</dt> <dd> <dl> <dt>

8342 (0x2096)
</dt> <dt>



L’opération ne peut être effectuée que sur un objet DSA maître interne.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CLASS_NOT_DSA"></span><span id="error_ds_class_not_dsa"></span>**ERREUR de \_ classe de service d’annuaire \_ \_ non \_ DSA**
</dt> <dd> <dl> <dt>

8343 (0x2097)
</dt> <dt>



L’objet doit être de type DSA.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INSUFF_ACCESS_RIGHTS"></span><span id="error_ds_insuff_access_rights"></span>**\_droits d' \_ \_ accès insuff \_ des erreurs DS**
</dt> <dd> <dl> <dt>

8344 (0x2098)
</dt> <dt>



Droits d’accès insuffisants pour effectuer l’opération.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ILLEGAL_SUPERIOR"></span><span id="error_ds_illegal_superior"></span>**ERREUR \_ DS \_ non conforme \_**
</dt> <dd> <dl> <dt>

8345 (0x2099)
</dt> <dt>



Impossible d’ajouter l’objet, car le parent ne figure pas dans la liste des supérieurs possibles.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ATTRIBUTE_OWNED_BY_SAM"></span><span id="error_ds_attribute_owned_by_sam"></span>**ERREUR \_ \_ d’attribut DS \_ appartenant \_ à \_ Sam**
</dt> <dd> <dl> <dt>

8346 (0x209A)
</dt> <dt>



L’accès à l’attribut n’est pas autorisé, car l’attribut appartient au gestionnaire de comptes de sécurité (SAM).


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NAME_TOO_MANY_PARTS"></span><span id="error_ds_name_too_many_parts"></span>**ERREUR \_ nom du service d’annuaire \_ \_ trop \_ grand nombre de \_ parties**
</dt> <dd> <dl> <dt>

8347 (0x209B)
</dt> <dt>



Le nom comporte un trop grand nombre de parties.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NAME_TOO_LONG"></span><span id="error_ds_name_too_long"></span>**ERREUR \_ nom du service d’annuaire \_ \_ trop \_ long**
</dt> <dd> <dl> <dt>

8348 (0x209C)
</dt> <dt>



Le nom est trop long.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NAME_VALUE_TOO_LONG"></span><span id="error_ds_name_value_too_long"></span>**ERREUR de \_ nom de service d’annuaire \_ \_ \_ trop \_ longue**
</dt> <dd> <dl> <dt>

8349 (0x209D)
</dt> <dt>



La valeur de nom est trop longue.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NAME_UNPARSEABLE"></span><span id="error_ds_name_unparseable"></span>**ERREUR de \_ nom de service d’annuaire non \_ \_ analysable**
</dt> <dd> <dl> <dt>

8350 (0x209E)
</dt> <dt>



Le service d’annuaire a rencontré une erreur lors de l’analyse d’un nom.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NAME_TYPE_UNKNOWN"></span><span id="error_ds_name_type_unknown"></span>**ERREUR de \_ type de nom de service d’annuaire \_ \_ \_ inconnu**
</dt> <dd> <dl> <dt>

8351 (0x209F)
</dt> <dt>



Le service d’annuaire ne peut pas obtenir le type d’attribut d’un nom.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NOT_AN_OBJECT"></span><span id="error_ds_not_an_object"></span>**ERREUR \_ DS \_ n’est pas \_ un \_ objet**
</dt> <dd> <dl> <dt>

8352 (0x20A0)
</dt> <dt>



Le nom n’identifie pas un objet ; le nom identifie un fantôme.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SEC_DESC_TOO_SHORT"></span><span id="error_ds_sec_desc_too_short"></span>**Erreur Description de l’erreur \_ DS \_ sec \_ \_ trop \_ brève**
</dt> <dd> <dl> <dt>

8353 (0x20A1)
</dt> <dt>



Le descripteur de sécurité est trop petit.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SEC_DESC_INVALID"></span><span id="error_ds_sec_desc_invalid"></span>**ERREUR de \_ Description du service d’annuaire \_ sec \_ \_ non valide**
</dt> <dd> <dl> <dt>

8354 (0x20A2)
</dt> <dt>



Le descripteur de sécurité n’est pas valide.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_DELETED_NAME"></span><span id="error_ds_no_deleted_name"></span>**ERREUR \_ DS \_ no \_ Deleted \_ Name**
</dt> <dd> <dl> <dt>

8355 (0x20A3)
</dt> <dt>



Impossible de créer le nom de l’objet supprimé.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SUBREF_MUST_HAVE_PARENT"></span><span id="error_ds_subref_must_have_parent"></span>**l' \_ erreur \_ SUBREF DS \_ doit \_ avoir le \_ parent**
</dt> <dd> <dl> <dt>

8356 (0x20A4)
</dt> <dt>



Le parent d’un nouveau subref doit exister.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NCNAME_MUST_BE_NC"></span><span id="error_ds_ncname_must_be_nc"></span>**l’erreur le \_ NCName du DS \_ \_ doit \_ être \_ NC**
</dt> <dd> <dl> <dt>

8357 (0x20A5)
</dt> <dt>



L’objet doit être un contexte d’appellation.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_ADD_SYSTEM_ONLY"></span><span id="error_ds_cant_add_system_only"></span>**ERREUR \_ DS \_ Impossible d' \_ Ajouter le \_ système \_ uniquement**
</dt> <dd> <dl> <dt>

8358 (0x20A6)
</dt> <dt>



L’ajout d’un attribut détenu par le système n’est pas autorisé.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CLASS_MUST_BE_CONCRETE"></span><span id="error_ds_class_must_be_concrete"></span>**la classe de l’erreur \_ DS \_ \_ doit \_ être \_ concrète**
</dt> <dd> <dl> <dt>

8359 (0x20A7)
</dt> <dt>



La classe de l’objet doit être structurelle ; vous ne pouvez pas instancier une classe abstraite.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INVALID_DMD"></span><span id="error_ds_invalid_dmd"></span>**ERREUR de la \_ \_ DMD non valide du DS \_**
</dt> <dd> <dl> <dt>

8360 (0x20A8)
</dt> <dt>



L’objet de schéma est introuvable.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_OBJ_GUID_EXISTS"></span><span id="error_ds_obj_guid_exists"></span>**le \_ GUID obj du DS d’erreur \_ \_ \_ existe**
</dt> <dd> <dl> <dt>

8361 (0x20A9)
</dt> <dt>



Un objet local avec ce GUID (Dead ou Alive) existe déjà.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NOT_ON_BACKLINK"></span><span id="error_ds_not_on_backlink"></span>**ERREUR \_ DS \_ non \_ sur \_ lien secondaire**
</dt> <dd> <dl> <dt>

8362 (0x20AA)
</dt> <dt>



L’opération ne peut pas être effectuée sur un lien précédent.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_CROSSREF_FOR_NC"></span><span id="error_ds_no_crossref_for_nc"></span>**ERREUR \_ DS \_ no \_ CROSSREF \_ pour \_ NC**
</dt> <dd> <dl> <dt>

8363 (0x20AB)
</dt> <dt>



La référence croisée pour le contexte d’appellation spécifié est introuvable.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SHUTTING_DOWN"></span><span id="error_ds_shutting_down"></span>**ERREUR d' \_ arrêt du service d’annuaire \_ \_**
</dt> <dd> <dl> <dt>

8364 (0x20AC)
</dt> <dt>



L’opération n’a pas pu être effectuée car le service d’annuaire est en cours d’arrêt.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_UNKNOWN_OPERATION"></span><span id="error_ds_unknown_operation"></span>**ERREUR de l' \_ \_ \_ opération inconnue de l’annuaire**
</dt> <dd> <dl> <dt>

8365 (0x20AD)
</dt> <dt>



La demande du service d’annuaire n’est pas valide.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INVALID_ROLE_OWNER"></span><span id="error_ds_invalid_role_owner"></span>**ERREUR \_ DS \_ \_ propriétaire du rôle non valide \_**
</dt> <dd> <dl> <dt>

8366 (0x20AE)
</dt> <dt>



Impossible de lire l’attribut propriétaire du rôle.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_COULDNT_CONTACT_FSMO"></span><span id="error_ds_couldnt_contact_fsmo"></span>**ERREUR \_ \_ impossible du \_ contact du service d’annuaire \_**
</dt> <dd> <dl> <dt>

8367 (0x20AF)
</dt> <dt>



L'opération FSMO demandée a échoué. Le propriétaire FSMO actuel n'a pas pu être contacté.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CROSS_NC_DN_RENAME"></span><span id="error_ds_cross_nc_dn_rename"></span>**ERREUR \_ de \_ changement \_ de \_ nom du DN Cross NC \_**
</dt> <dd> <dl> <dt>

8368 (0x20B0)
</dt> <dt>



La modification d’un DN dans un contexte d’appellation n’est pas autorisée.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_MOD_SYSTEM_ONLY"></span><span id="error_ds_cant_mod_system_only"></span>**ERREUR DS inverser \_ \_ \_ \_ système \_ uniquement**
</dt> <dd> <dl> <dt>

8369 (0x20B1)
</dt> <dt>



L’attribut ne peut pas être modifié, car il appartient au système.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_REPLICATOR_ONLY"></span><span id="error_ds_replicator_only"></span>**ERREUR \_ du \_ réplicateur DS \_ uniquement**
</dt> <dd> <dl> <dt>

8370 (0x20B2)
</dt> <dt>



Seul le réplicateur peut exécuter cette fonction.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_OBJ_CLASS_NOT_DEFINED"></span><span id="error_ds_obj_class_not_defined"></span>**ERREUR \_ de \_ classe obj du DS \_ \_ non \_ définie**
</dt> <dd> <dl> <dt>

8371 (0x20B3)
</dt> <dt>



La classe spécifiée n’est pas définie.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_OBJ_CLASS_NOT_SUBCLASS"></span><span id="error_ds_obj_class_not_subclass"></span>**ERREUR \_ de \_ \_ classe \_ non sous- \_ classe obj de l’annuaire d’annuaire**
</dt> <dd> <dl> <dt>

8372 (0x20B4)
</dt> <dt>



La classe spécifiée n’est pas une sous-classe.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NAME_REFERENCE_INVALID"></span><span id="error_ds_name_reference_invalid"></span>**ERREUR de \_ référence de nom de service d’annuaire \_ \_ \_ non valide**
</dt> <dd> <dl> <dt>

8373 (0x20B5)
</dt> <dt>



La référence de nom n’est pas valide.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CROSS_REF_EXISTS"></span><span id="error_ds_cross_ref_exists"></span>**ERREUR \_ de \_ référence croisée DS \_ \_**
</dt> <dd> <dl> <dt>

8374 (0x20B6)
</dt> <dt>



Une référence croisée existe déjà.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_DEL_MASTER_CROSSREF"></span><span id="error_ds_cant_del_master_crossref"></span>**ERREUR DS ne dispose pas de l' \_ \_ \_ \_ \_ CROSSREF maître**
</dt> <dd> <dl> <dt>

8375 (0x20B7)
</dt> <dt>



La suppression d’une référence croisée principale n’est pas autorisée.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SUBTREE_NOTIFY_NOT_NC_HEAD"></span><span id="error_ds_subtree_notify_not_nc_head"></span>**ERREUR de notification de la \_ \_ \_ sous-arborescence DS \_ non \_ \_ -en-tête**
</dt> <dd> <dl> <dt>

8376 (0x20B8)
</dt> <dt>



Les notifications de sous-arborescence sont uniquement prises en charge sur les têtes NC.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NOTIFY_FILTER_TOO_COMPLEX"></span><span id="error_ds_notify_filter_too_complex"></span>**ERREUR de \_ filtre de notification du service d’annuaire \_ \_ \_ trop \_ complexe**
</dt> <dd> <dl> <dt>

8377 (0x20B9)
</dt> <dt>



Le filtre de notification est trop complexe.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DUP_RDN"></span><span id="error_ds_dup_rdn"></span>**ERREUR du RDN du service d' \_ annuaire \_ \_**
</dt> <dd> <dl> <dt>

8378 (0x20BA)
</dt> <dt>



Échec de la mise à jour du schéma : RDN dupliqué.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DUP_OID"></span><span id="error_ds_dup_oid"></span>**ERREUR \_ d' \_ OID DUP du DS \_**
</dt> <dd> <dl> <dt>

8379 (0x20BB)
</dt> <dt>



Échec de la mise à jour du schéma : OID dupliqué.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DUP_MAPI_ID"></span><span id="error_ds_dup_mapi_id"></span>**\_ \_ \_ ID MAPI DUP \_ de l’erreur DS**
</dt> <dd> <dl> <dt>

8380 (0x20BC)
</dt> <dt>



Échec de la mise à jour du schéma : identificateur MAPI dupliqué.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DUP_SCHEMA_ID_GUID"></span><span id="error_ds_dup_schema_id_guid"></span>**ERREUR \_ GUID de l’ID de \_ schéma DUP du DS \_ \_ \_**
</dt> <dd> <dl> <dt>

8381 (0x20BD)
</dt> <dt>



Échec de la mise à jour du schéma : GUID de l’ID de schéma dupliqué.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DUP_LDAP_DISPLAY_NAME"></span><span id="error_ds_dup_ldap_display_name"></span>**ERREUR \_ \_ \_ \_ nom complet LDAP DUP du DS \_**
</dt> <dd> <dl> <dt>

8382 (0x20BE)
</dt> <dt>



Échec de la mise à jour du schéma : nom complet LDAP dupliqué.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SEMANTIC_ATT_TEST"></span><span id="error_ds_semantic_att_test"></span>**ERREUR du test de la \_ \_ sémantique \_ att DS \_**
</dt> <dd> <dl> <dt>

8383 (0x20BF)
</dt> <dt>



Échec de la mise à jour du schéma : plage inférieure à la plage supérieure à la plage supérieure.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SYNTAX_MISMATCH"></span><span id="error_ds_syntax_mismatch"></span>**ERREUR \_ d' \_ incompatibilité de syntaxe DS \_**
</dt> <dd> <dl> <dt>

8384 (0x20C0)
</dt> <dt>



Échec de la mise à jour du schéma : incompatibilité de syntaxe.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_EXISTS_IN_MUST_HAVE"></span><span id="error_ds_exists_in_must_have"></span>**\_l’erreur DS \_ existe \_ dans \_ doit \_ avoir**
</dt> <dd> <dl> <dt>

8385 (0x20C1)
</dt> <dt>



Échec de la suppression du schéma : l’attribut est utilisé dans la doit contenir.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_EXISTS_IN_MAY_HAVE"></span><span id="error_ds_exists_in_may_have"></span>**\_l’erreur \_ DS \_ existe \_ peut- \_ être**
</dt> <dd> <dl> <dt>

8386 (0x20C2)
</dt> <dt>



Échec de la suppression du schéma : l’attribut est utilisé dans la relation contenant-contenu.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NONEXISTENT_MAY_HAVE"></span><span id="error_ds_nonexistent_may_have"></span>**l’erreur \_ DS \_ inexistant \_ peut \_ avoir**
</dt> <dd> <dl> <dt>

8387 (0x20C3)
</dt> <dt>



Échec de la mise à jour du schéma : l’attribut dans peut contenir n’existe pas.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NONEXISTENT_MUST_HAVE"></span><span id="error_ds_nonexistent_must_have"></span>**l’erreur \_ DS \_ inexistant \_ doit \_ avoir**
</dt> <dd> <dl> <dt>

8388 (0x20C4)
</dt> <dt>



Échec de la mise à jour du schéma : l’attribut dans doit contenir n’existe pas.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_AUX_CLS_TEST_FAIL"></span><span id="error_ds_aux_cls_test_fail"></span>**ERREUR \_ échec du test DS aux \_ \_ CLS \_ \_**
</dt> <dd> <dl> <dt>

8389 (0x20C5)
</dt> <dt>



Échec de la mise à jour du schéma : la classe dans la liste des classes auxiliaires n’existe pas ou n’est pas une classe auxiliaire.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NONEXISTENT_POSS_SUP"></span><span id="error_ds_nonexistent_poss_sup"></span>**ERREUR d' \_ annuaire \_ \_ poss inexistant \_**
</dt> <dd> <dl> <dt>

8390 (0x20C6)
</dt> <dt>



Échec de la mise à jour du schéma : la classe dans Poss-Superior n’existe pas.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SUB_CLS_TEST_FAIL"></span><span id="error_ds_sub_cls_test_fail"></span>**ERREUR \_ \_ échec du test DS Sub \_ CLS \_ \_**
</dt> <dd> <dl> <dt>

8391 (0x20C7)
</dt> <dt>



Échec de la mise à jour du schéma : la classe dans la liste subclassof n’existe pas ou ne répond pas aux règles de hiérarchie.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_BAD_RDN_ATT_ID_SYNTAX"></span><span id="error_ds_bad_rdn_att_id_syntax"></span>**ERREUR \_ DS \_ incorrecte, syntaxe de l' \_ \_ ID att att \_ \_**
</dt> <dd> <dl> <dt>

8392 (0x20C8)
</dt> <dt>



Échec de la mise à jour du schéma : RDN-att-ID a une syntaxe incorrecte.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_EXISTS_IN_AUX_CLS"></span><span id="error_ds_exists_in_aux_cls"></span>**\_l’erreur DS \_ existe \_ dans \_ \_ CLS**
</dt> <dd> <dl> <dt>

8393 (0x20C9)
</dt> <dt>



Échec de la suppression du schéma : la classe est utilisée comme classe auxiliaire.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_EXISTS_IN_SUB_CLS"></span><span id="error_ds_exists_in_sub_cls"></span>**\_l’erreur DS \_ existe dans la sous- \_ \_ \_ spécification CLS**
</dt> <dd> <dl> <dt>

8394 (0x20CA)
</dt> <dt>



Échec de la suppression du schéma : la classe est utilisée en tant que sous-classe.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_EXISTS_IN_POSS_SUP"></span><span id="error_ds_exists_in_poss_sup"></span>**\_l’erreur DS \_ existe \_ dans \_ poss \_ sup**
</dt> <dd> <dl> <dt>

8395 (0x20CB)
</dt> <dt>



Échec de la suppression du schéma : la classe est utilisée en tant que Poss Superior.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_RECALCSCHEMA_FAILED"></span><span id="error_ds_recalcschema_failed"></span>**échec de l’RECALCSCHEMA de l’erreur \_ DS \_ \_**
</dt> <dd> <dl> <dt>

8396 (0x20CC)
</dt> <dt>



Échec de la mise à jour du schéma lors du recalcul du cache de validation.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_TREE_DELETE_NOT_FINISHED"></span><span id="error_ds_tree_delete_not_finished"></span>**ERREUR de suppression de l' \_ arborescence du service d’annuaire \_ \_ \_ non \_ terminée**
</dt> <dd> <dl> <dt>

8397 (0x20CD)
</dt> <dt>



La suppression de l’arborescence n’est pas terminée. La demande doit être réexécutée pour poursuivre la suppression de l’arborescence.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_DELETE"></span><span id="error_ds_cant_delete"></span>**ERREUR \_ DS \_ Impossible de \_ Supprimer**
</dt> <dd> <dl> <dt>

8398 (0x20CE)
</dt> <dt>



Impossible d’effectuer l’opération de suppression demandée.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ATT_SCHEMA_REQ_ID"></span><span id="error_ds_att_schema_req_id"></span>**ERREUR de l’ID de la \_ \_ demande de schéma DS att \_ \_ \_**
</dt> <dd> <dl> <dt>

8399 (0x20CF)
</dt> <dt>



Impossible de lire l’identificateur de classe gouvernes pour l’enregistrement de schéma.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_BAD_ATT_SCHEMA_SYNTAX"></span><span id="error_ds_bad_att_schema_syntax"></span>**ERREUR \_ de \_ \_ syntaxe de \_ schéma \_ att de l’annuaire de services**
</dt> <dd> <dl> <dt>

8400 (0x20D0)
</dt> <dt>



La syntaxe du schéma d’attribut est incorrecte.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_CACHE_ATT"></span><span id="error_ds_cant_cache_att"></span>**ERREUR \_ DS \_ Impossible de mettre \_ en cache \_ ATT**
</dt> <dd> <dl> <dt>

8401 (0x20D1)
</dt> <dt>



L’attribut n’a pas pu être mis en cache.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_CACHE_CLASS"></span><span id="error_ds_cant_cache_class"></span>**ERREUR \_ de \_ \_ classe de cache du service DS \_**
</dt> <dd> <dl> <dt>

8402 (0x20D2)
</dt> <dt>



La classe n’a pas pu être mise en cache.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_REMOVE_ATT_CACHE"></span><span id="error_ds_cant_remove_att_cache"></span>**ERREUR \_ DS \_ Impossible de \_ supprimer le \_ \_ cache ATT**
</dt> <dd> <dl> <dt>

8403 (0x20D3)
</dt> <dt>



L’attribut n’a pas pu être supprimé du cache.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_REMOVE_CLASS_CACHE"></span><span id="error_ds_cant_remove_class_cache"></span>**ERREUR \_ DS \_ Impossible de \_ supprimer le \_ cache de classe \_**
</dt> <dd> <dl> <dt>

8404 (0x20D4)
</dt> <dt>



La classe n’a pas pu être supprimée du cache.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_RETRIEVE_DN"></span><span id="error_ds_cant_retrieve_dn"></span>**ERREUR \_ DS \_ Impossible de \_ récupérer le \_ DN**
</dt> <dd> <dl> <dt>

8405 (0x20D5)
</dt> <dt>



L’attribut de nom unique n’a pas pu être lu.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_MISSING_SUPREF"></span><span id="error_ds_missing_supref"></span>**ERREUR \_ \_ SUPREF manquante du service d’annuaire \_**
</dt> <dd> <dl> <dt>

8406 (0x20D6)
</dt> <dt>



Aucun renvoi supérieur n'a été configuré pour le service d'annuaire. Le service d’annuaire n’est donc pas en mesure d’émettre des références aux objets en dehors de cette forêt.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_RETRIEVE_INSTANCE"></span><span id="error_ds_cant_retrieve_instance"></span>**ERREUR \_ DS \_ Impossible de \_ récupérer l' \_ instance**
</dt> <dd> <dl> <dt>

8407 (0x20D7)
</dt> <dt>



L’attribut de type d’instance n’a pas pu être récupéré.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CODE_INCONSISTENCY"></span><span id="error_ds_code_inconsistency"></span>**ERREUR \_ d' \_ incohérence de code DS \_**
</dt> <dd> <dl> <dt>

8408 (0x20D8)
</dt> <dt>



Une erreur interne s'est produite.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DATABASE_ERROR"></span><span id="error_ds_database_error"></span>**erreur \_ \_ de base de données DS Error \_**
</dt> <dd> <dl> <dt>

8409 (0x20D9)
</dt> <dt>



Une erreur de base de données s’est produite.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_GOVERNSID_MISSING"></span><span id="error_ds_governsid_missing"></span>**ERREUR \_ de \_ governsID DS \_ manquante**
</dt> <dd> <dl> <dt>

8410 (0x20DA)
</dt> <dt>



L’attribut GOVERNSID est manquant.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_MISSING_EXPECTED_ATT"></span><span id="error_ds_missing_expected_att"></span>**erreur indiquant que le \_ DS est \_ manquant \_ \_ ATT**
</dt> <dd> <dl> <dt>

8411 (0x20DB)
</dt> <dt>



Un attribut attendu est manquant.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NCNAME_MISSING_CR_REF"></span><span id="error_ds_ncname_missing_cr_ref"></span>**ERREUR du NCName de la \_ DM du service DS \_ \_ manquant \_ \_**
</dt> <dd> <dl> <dt>

8412 (0x20DC)
</dt> <dt>



Il manque une référence croisée dans le contexte d’appellation spécifié.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SECURITY_CHECKING_ERROR"></span><span id="error_ds_security_checking_error"></span>**erreur de vérification de la \_ sécurité du service d’annuaire \_ \_ \_**
</dt> <dd> <dl> <dt>

8413 (0x20DD)
</dt> <dt>



Une erreur de vérification de la sécurité s’est produite.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SCHEMA_NOT_LOADED"></span><span id="error_ds_schema_not_loaded"></span>**ERREUR de chargement du schéma du service d' \_ annuaire \_ \_ \_**
</dt> <dd> <dl> <dt>

8414 (0x20DE)
</dt> <dt>



Le schéma n’est pas chargé.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SCHEMA_ALLOC_FAILED"></span><span id="error_ds_schema_alloc_failed"></span>**ERREUR \_ échec de l’allocation du \_ schéma DS \_ \_**
</dt> <dd> <dl> <dt>

8415 (0x20DF)
</dt> <dt>



Échec de l’allocation du schéma. Vérifiez que la mémoire est insuffisante sur l’ordinateur.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ATT_SCHEMA_REQ_SYNTAX"></span><span id="error_ds_att_schema_req_syntax"></span>**ERREUR de syntaxe de la \_ \_ demande de schéma DS att \_ \_ \_**
</dt> <dd> <dl> <dt>

8416 (0x20E0)
</dt> <dt>



Échec de l’obtention de la syntaxe requise pour le schéma d’attribut.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_GCVERIFY_ERROR"></span><span id="error_ds_gcverify_error"></span>**erreur de \_ GCVERIFY du service d’annuaire \_ \_**
</dt> <dd> <dl> <dt>

8417 (0x20E1)
</dt> <dt>



Échec de la vérification du catalogue global. Le catalogue global n’est pas disponible ou ne prend pas en charge l’opération. Une partie du répertoire n’est pas disponible actuellement.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_SCHEMA_MISMATCH"></span><span id="error_ds_dra_schema_mismatch"></span>**ERREUR \_ d' \_ \_ incompatibilité de schéma DRA de l’annuaire \_**
</dt> <dd> <dl> <dt>

8418 (0x20E2)
</dt> <dt>



L’opération de réplication a échoué en raison d’une incompatibilité de schéma entre les serveurs impliqués.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_FIND_DSA_OBJ"></span><span id="error_ds_cant_find_dsa_obj"></span>**ERREUR \_ DS \_ Impossible de \_ trouver \_ DSA \_ obj**
</dt> <dd> <dl> <dt>

8419 (0x20E3)
</dt> <dt>



L’objet DSA est introuvable.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_FIND_EXPECTED_NC"></span><span id="error_ds_cant_find_expected_nc"></span>**ERREUR \_ \_ Impossible de \_ trouver le \_ contexte de nommage DS attendu \_**
</dt> <dd> <dl> <dt>

8420 (0x20E4)
</dt> <dt>



Le contexte d’appellation est introuvable.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_FIND_NC_IN_CACHE"></span><span id="error_ds_cant_find_nc_in_cache"></span>**ERREUR \_ DS \_ Impossible \_ de trouver le \_ contexte \_ de nommage dans le \_ cache**
</dt> <dd> <dl> <dt>

8421 (0x20E5)
</dt> <dt>



Le contexte d’appellation est introuvable dans le cache.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_RETRIEVE_CHILD"></span><span id="error_ds_cant_retrieve_child"></span>**ERREUR \_ DS \_ Impossible de \_ récupérer l' \_ enfant**
</dt> <dd> <dl> <dt>

8422 (0x20E6)
</dt> <dt>



Impossible de récupérer l’objet enfant.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SECURITY_ILLEGAL_MODIFY"></span><span id="error_ds_security_illegal_modify"></span>**ERREUR \_ de \_ \_ modification non conforme de la sécurité DS \_**
</dt> <dd> <dl> <dt>

8423 (0x20E7)
</dt> <dt>



La modification n’a pas été autorisée pour des raisons de sécurité.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_REPLACE_HIDDEN_REC"></span><span id="error_ds_cant_replace_hidden_rec"></span>**ERREUR \_ DS \_ Impossible de \_ remplacer le \_ \_ Rapp masqué**
</dt> <dd> <dl> <dt>

8424 (0x20E8)
</dt> <dt>



L’opération ne peut pas remplacer l’enregistrement masqué.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_BAD_HIERARCHY_FILE"></span><span id="error_ds_bad_hierarchy_file"></span>**ERREUR \_ du \_ \_ fichier de hiérarchie incorrecte DS \_**
</dt> <dd> <dl> <dt>

8425 (0x20E9)
</dt> <dt>



Le fichier de hiérarchie n’est pas valide.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_BUILD_HIERARCHY_TABLE_FAILED"></span><span id="error_ds_build_hierarchy_table_failed"></span>**ERREUR lors de la table de la \_ \_ hiérarchie de génération DS \_ \_ \_**
</dt> <dd> <dl> <dt>

8426 (0x20EA)
</dt> <dt>



Échec de la tentative de création de la table de hiérarchie.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CONFIG_PARAM_MISSING"></span><span id="error_ds_config_param_missing"></span>**paramètre de configuration de l’annuaire d’erreurs \_ \_ \_ \_ manquant**
</dt> <dd> <dl> <dt>

8427 (0x20EB)
</dt> <dt>



Le paramètre de configuration de répertoire est manquant dans le registre.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_COUNTING_AB_INDICES_FAILED"></span><span id="error_ds_counting_ab_indices_failed"></span>**ERREUR \_ de \_ comptage \_ des \_ indices AB du service d’annuaire \_**
</dt> <dd> <dl> <dt>

8428 (0x20EC)
</dt> <dt>



La tentative de compter les index du carnet d’adresses a échoué.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_HIERARCHY_TABLE_MALLOC_FAILED"></span><span id="error_ds_hierarchy_table_malloc_failed"></span>**ERREUR d’échec de malloc de la table de \_ hiérarchie des services d’annuaire \_ \_ \_ \_**
</dt> <dd> <dl> <dt>

8429 (0x20ED)
</dt> <dt>



Échec de l’allocation de la table de hiérarchie.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INTERNAL_FAILURE"></span><span id="error_ds_internal_failure"></span>**ERREUR \_ interne de l’annuaire de services \_ \_**
</dt> <dd> <dl> <dt>

8430 (0x20EE)
</dt> <dt>



Le service d’annuaire a rencontré une erreur interne.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_UNKNOWN_ERROR"></span><span id="error_ds_unknown_error"></span>**erreur \_ DS erreur \_ inconnue \_**
</dt> <dd> <dl> <dt>

8431 (0x20EF)
</dt> <dt>



Le service d’annuaire a rencontré une erreur inconnue.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ROOT_REQUIRES_CLASS_TOP"></span><span id="error_ds_root_requires_class_top"></span>**la racine de l’erreur \_ DS \_ requiert la \_ \_ classe \_ Top**
</dt> <dd> <dl> <dt>

8432 (0x20F0)
</dt> <dt>



Un objet racine requiert une classe de’Top'.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_REFUSING_FSMO_ROLES"></span><span id="error_ds_refusing_fsmo_roles"></span>**ERREUR \_ de \_ refus des \_ \_ rôles FSMO pour le service d’annuaire**
</dt> <dd> <dl> <dt>

8433 (0x20F1)
</dt> <dt>



Ce serveur d’annuaire est en cours d’arrêt et ne peut pas prendre possession de nouveaux rôles d’opérations à maître unique flottant.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_MISSING_FSMO_SETTINGS"></span><span id="error_ds_missing_fsmo_settings"></span>**\_ \_ paramètres FSMO manquants de \_ l’erreur DS \_**
</dt> <dd> <dl> <dt>

8434 (0x20F2)
</dt> <dt>



Les informations de configuration obligatoires sont manquantes dans le service d’annuaire et il est impossible de déterminer la propriété des rôles d’opérations à maître unique flottant.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_UNABLE_TO_SURRENDER_ROLES"></span><span id="error_ds_unable_to_surrender_roles"></span>**ERREUR \_ DS \_ Impossible \_ de \_ renoncer aux \_ rôles**
</dt> <dd> <dl> <dt>

8435 (0x20F3)
</dt> <dt>



Le service d’annuaire n’a pas pu transférer la propriété d’un ou plusieurs rôles d’opérations à maître unique flottants à d’autres serveurs.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_GENERIC"></span><span id="error_ds_dra_generic"></span>**ERREUR \_ \_ générique DRA de l’annuaire \_**
</dt> <dd> <dl> <dt>

8436 (0x20F4)
</dt> <dt>



L’opération de réplication a échoué.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_INVALID_PARAMETER"></span><span id="error_ds_dra_invalid_parameter"></span>**ERREUR \_ du \_ \_ paramètre DRA non valide du service d’annuaire \_**
</dt> <dd> <dl> <dt>

8437 (0x20F5)
</dt> <dt>



Un paramètre non valide a été spécifié pour cette opération de réplication.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_BUSY"></span><span id="error_ds_dra_busy"></span>**ERREUR \_ \_ DRA \_ occupée**
</dt> <dd> <dl> <dt>

8438 (0x20F6)
</dt> <dt>



Le service d’annuaire est trop occupé pour terminer l’opération de réplication pour l’instant.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_BAD_DN"></span><span id="error_ds_dra_bad_dn"></span>**ERREUR \_ de \_ \_ DN DRA incorrecte du DS \_**
</dt> <dd> <dl> <dt>

8439 (0x20F7)
</dt> <dt>



Le nom unique spécifié pour cette opération de réplication n’est pas valide.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_BAD_NC"></span><span id="error_ds_dra_bad_nc"></span>**ERREUR \_ \_ NC DRA \_ Bad \_ NC**
</dt> <dd> <dl> <dt>

8440 (0x20F8)
</dt> <dt>



Le contexte d’appellation spécifié pour cette opération de réplication n’est pas valide.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_DN_EXISTS"></span><span id="error_ds_dra_dn_exists"></span>**ERREUR \_ de \_ \_ nom de domaine DRA \_ de l’annuaire**
</dt> <dd> <dl> <dt>

8441 (0x20F9)
</dt> <dt>



Le nom unique spécifié pour cette opération de réplication existe déjà.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_INTERNAL_ERROR"></span><span id="error_ds_dra_internal_error"></span>**erreur \_ \_ interne de DRA DRA \_ \_**
</dt> <dd> <dl> <dt>

8442 (0x20FA)
</dt> <dt>



Le système de réplication a rencontré une erreur interne.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_INCONSISTENT_DIT"></span><span id="error_ds_dra_inconsistent_dit"></span>**ERREUR \_ \_ DRA non \_ cohérente du DS \_**
</dt> <dd> <dl> <dt>

8443 (0x20FB)
</dt> <dt>



L’opération de réplication a rencontré une incohérence de base de données.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_CONNECTION_FAILED"></span><span id="error_ds_dra_connection_failed"></span>**ERREUR \_ échec de la \_ \_ connexion DRA \_ de l’annuaire**
</dt> <dd> <dl> <dt>

8444 (0x20FC)
</dt> <dt>



Le serveur spécifié pour cette opération de réplication n’a pas pu être contacté.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_BAD_INSTANCE_TYPE"></span><span id="error_ds_dra_bad_instance_type"></span>**ERREUR \_ de \_ \_ type d' \_ instance incorrecte du DS DRA \_**
</dt> <dd> <dl> <dt>

8445 (0x20FD)
</dt> <dt>



L’opération de réplication a rencontré un objet avec un type d’instance non valide.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_OUT_OF_MEM"></span><span id="error_ds_dra_out_of_mem"></span>**ERREUR \_ \_ de l' \_ agent \_ de récupération de la \_ mémoire DS**
</dt> <dd> <dl> <dt>

8446 (0x20FE)
</dt> <dt>



L’opération de réplication n’a pas pu allouer de mémoire.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_MAIL_PROBLEM"></span><span id="error_ds_dra_mail_problem"></span>**ERREUR du \_ service de \_ \_ messages DRA \_ de l’erreur**
</dt> <dd> <dl> <dt>

8447 (0x20FF)
</dt> <dt>



L’opération de réplication a rencontré une erreur avec le système de messagerie.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_REF_ALREADY_EXISTS"></span><span id="error_ds_dra_ref_already_exists"></span>**l’erreur la \_ référence DRA de l’annuaire \_ \_ \_ \_ existe déjà**
</dt> <dd> <dl> <dt>

8448 (0x2100)
</dt> <dt>



Les informations de référence sur la réplication du serveur cible existent déjà.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_REF_NOT_FOUND"></span><span id="error_ds_dra_ref_not_found"></span>**ERREUR \_ de \_ \_ référence DRA \_ non \_ trouvée**
</dt> <dd> <dl> <dt>

8449 (0x2101)
</dt> <dt>



Les informations de référence sur la réplication du serveur cible n’existent pas.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_OBJ_IS_REP_SOURCE"></span><span id="error_ds_dra_obj_is_rep_source"></span>**erreur la source DRA de l’annuaire d’erreurs \_ \_ \_ \_ est \_ REP \_ .**
</dt> <dd> <dl> <dt>

8450 (0x2102)
</dt> <dt>



Impossible de supprimer le contexte d’appellation, car il est répliqué sur un autre serveur.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_DB_ERROR"></span><span id="error_ds_dra_db_error"></span>**erreur \_ de \_ \_ base \_ de**
</dt> <dd> <dl> <dt>

8451 (0x2103)
</dt> <dt>



L’opération de réplication a rencontré une erreur de base de données.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_NO_REPLICA"></span><span id="error_ds_dra_no_replica"></span>**ERREUR \_ \_ DRA \_ non \_ répliquée du service d’annuaire**
</dt> <dd> <dl> <dt>

8452 (0x2104)
</dt> <dt>



Le contexte d’appellation est en cours de suppression ou n’est pas répliqué à partir du serveur spécifié.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_ACCESS_DENIED"></span><span id="error_ds_dra_access_denied"></span>**ERREUR \_ de \_ refus d’accès DRA de \_ l’annuaire \_**
</dt> <dd> <dl> <dt>

8453 (0x2105)
</dt> <dt>



L’accès à la réplication a été refusé.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_NOT_SUPPORTED"></span><span id="error_ds_dra_not_supported"></span>**ERREUR \_ \_ DRA \_ non \_ prise en charge**
</dt> <dd> <dl> <dt>

8454 (0x2106)
</dt> <dt>



L’opération demandée n’est pas prise en charge par cette version du service d’annuaire.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_RPC_CANCELLED"></span><span id="error_ds_dra_rpc_cancelled"></span>**ERREUR \_ \_ RPC DRA \_ \_ annulée**
</dt> <dd> <dl> <dt>

8455 (0x2107)
</dt> <dt>



L’appel de procédure distante de réplication a été annulé.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_SOURCE_DISABLED"></span><span id="error_ds_dra_source_disabled"></span>**ERREUR \_ de \_ source DRA de l’annuaire \_ \_ désactivée**
</dt> <dd> <dl> <dt>

8456 (0x2108)
</dt> <dt>



Le serveur source rejette actuellement les demandes de réplication.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_SINK_DISABLED"></span><span id="error_ds_dra_sink_disabled"></span>**ERREUR du \_ récepteur DRA du service d’annuaire \_ \_ \_ désactivé**
</dt> <dd> <dl> <dt>

8457 (0x2109)
</dt> <dt>



Le serveur de destination rejette actuellement les demandes de réplication.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_NAME_COLLISION"></span><span id="error_ds_dra_name_collision"></span>**ERREUR \_ de \_ \_ collision de nom DRA \_ de l’annuaire**
</dt> <dd> <dl> <dt>

8458 (0x210A)
</dt> <dt>



L’opération de réplication a échoué en raison d’une collision de noms d’objets.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_SOURCE_REINSTALLED"></span><span id="error_ds_dra_source_reinstalled"></span>**ERREUR lors de la \_ RÉinstallation de la \_ source DRA DS \_ \_**
</dt> <dd> <dl> <dt>

8459 (0x210B)
</dt> <dt>



La source de réplication a été réinstallée.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_MISSING_PARENT"></span><span id="error_ds_dra_missing_parent"></span>**ERREUR de l' \_ \_ absence du \_ parent du DRA \_ de l’annuaire**
</dt> <dd> <dl> <dt>

8460 (0x210C)
</dt> <dt>



L’opération de réplication a échoué car un objet parent requis est manquant.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_PREEMPTED"></span><span id="error_ds_dra_preempted"></span>**ERREUR \_ \_ DRA en \_ préemption**
</dt> <dd> <dl> <dt>

8461 (0x210D)
</dt> <dt>



L’opération de réplication a été préemptée.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_ABANDON_SYNC"></span><span id="error_ds_dra_abandon_sync"></span>**ERREUR \_ de \_ \_ synchronisation des abandons DRA \_ de l’annuaire**
</dt> <dd> <dl> <dt>

8462 (0x210E)
</dt> <dt>



La tentative de synchronisation de réplication a été abandonnée en raison d’un manque de mises à jour.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_SHUTDOWN"></span><span id="error_ds_dra_shutdown"></span>**ERREUR de l' \_ \_ arrêt DRA du DS \_**
</dt> <dd> <dl> <dt>

8463 (0x210F)
</dt> <dt>



L’opération de réplication a été arrêtée car le système est en cours d’arrêt.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_INCOMPATIBLE_PARTIAL_SET"></span><span id="error_ds_dra_incompatible_partial_set"></span>**ERREUR de l' \_ \_ \_ \_ ensemble partiel incompatible \_ de la DRA du DS**
</dt> <dd> <dl> <dt>

8464 (0x2110)
</dt> <dt>



La tentative de synchronisation a échoué car le DC de destination attend actuellement de synchroniser de nouveaux attributs partiels à partir de la source. Cette condition est normale si une modification récente du schéma a modifié l’ensemble des attributs partiels. L’ensemble d’attributs partiels de destination n’est pas un sous-ensemble de l’ensemble d’attributs partiels source.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_SOURCE_IS_PARTIAL_REPLICA"></span><span id="error_ds_dra_source_is_partial_replica"></span>**ERREUR \_ la \_ source DRA du DS \_ est un \_ \_ \_ réplica partiel**
</dt> <dd> <dl> <dt>

8465 (0x2111)
</dt> <dt>



La tentative de synchronisation de la réplication a échoué car un réplica principal a tenté de se synchroniser à partir d’un réplica partiel.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_EXTN_CONNECTION_FAILED"></span><span id="error_ds_dra_extn_connection_failed"></span>**ERREUR \_ échec de la \_ \_ connexion DRA Extn \_ \_ de l’annuaire**
</dt> <dd> <dl> <dt>

8466 (0x2112)
</dt> <dt>



Le serveur spécifié pour cette opération de réplication a été contacté, mais ce serveur n’a pas pu contacter un serveur supplémentaire nécessaire pour terminer l’opération.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INSTALL_SCHEMA_MISMATCH"></span><span id="error_ds_install_schema_mismatch"></span>**ERREUR \_ d' \_ \_ incompatibilité de schéma d’installation du service d’annuaire \_**
</dt> <dd> <dl> <dt>

8467 (0x2113)
</dt> <dt>



La version du schéma du service d’annuaire de la forêt source n’est pas compatible avec la version du service d’annuaire sur cet ordinateur.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DUP_LINK_ID"></span><span id="error_ds_dup_link_id"></span>**\_ID de \_ lien du doublon DS d' \_ erreur \_**
</dt> <dd> <dl> <dt>

8468 (0x2114)
</dt> <dt>



Échec de la mise à jour du schéma : un attribut avec le même identificateur de lien existe déjà.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NAME_ERROR_RESOLVING"></span><span id="error_ds_name_error_resolving"></span>**ERREUR \_ de \_ \_ résolution des erreurs de nom du service d’annuaire \_**
</dt> <dd> <dl> <dt>

8469 (0x2115)
</dt> <dt>



Traduction de nom : erreur de traitement générique.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NAME_ERROR_NOT_FOUND"></span><span id="error_ds_name_error_not_found"></span>**ERREUR de \_ nom du service d’annuaire \_ \_ \_ \_ introuvable**
</dt> <dd> <dl> <dt>

8470 (0x2116)
</dt> <dt>



Traduction de nom : impossible de trouver le nom ou le droit insuffisant pour afficher le nom.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NAME_ERROR_NOT_UNIQUE"></span><span id="error_ds_name_error_not_unique"></span>**erreur de \_ nom du service d’annuaire \_ \_ \_ non \_ unique**
</dt> <dd> <dl> <dt>

8471 (0x2117)
</dt> <dt>



Traduction de nom : nom d’entrée mappé à plusieurs noms de sortie.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NAME_ERROR_NO_MAPPING"></span><span id="error_ds_name_error_no_mapping"></span>**ERREUR de nom d’erreur de \_ nom de service d’annuaire \_ \_ \_ \_**
</dt> <dd> <dl> <dt>

8472 (0x2118)
</dt> <dt>



Traduction de nom : nom d’entrée trouvé, mais pas le format de sortie associé.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NAME_ERROR_DOMAIN_ONLY"></span><span id="error_ds_name_error_domain_only"></span>**ERREUR \_ \_ nom du \_ domaine d’erreur du nom \_ \_ de l’annuaire**
</dt> <dd> <dl> <dt>

8473 (0x2119)
</dt> <dt>



Traduction de nom : impossible de résoudre complètement, seul le domaine a été trouvé.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NAME_ERROR_NO_SYNTACTICAL_MAPPING"></span><span id="error_ds_name_error_no_syntactical_mapping"></span>**ERREUR de nom de l’annuaire d’erreurs \_ \_ \_ \_ sans \_ \_ mappage syntaxique**
</dt> <dd> <dl> <dt>

8474 (0x211A)
</dt> <dt>



Traduction de noms : impossible d’effectuer un mappage syntaxique purement incorrect au client sans passer par le câble.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CONSTRUCTED_ATT_MOD"></span><span id="error_ds_constructed_att_mod"></span>**ERREUR \_ de \_ \_ modification att \_ construite par DS**
</dt> <dd> <dl> <dt>

8475 (0x211B)
</dt> <dt>



La modification d’un attribut construit n’est pas autorisée.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_WRONG_OM_OBJ_CLASS"></span><span id="error_ds_wrong_om_obj_class"></span>**erreur \_ du \_ \_ modèle de \_ \_ classe obj de l’erreur DS incorrect**
</dt> <dd> <dl> <dt>

8476 (0x211C)
</dt> <dt>



La classe OM-Object-Class spécifiée est incorrecte pour un attribut avec la syntaxe spécifiée.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_REPL_PENDING"></span><span id="error_ds_dra_repl_pending"></span>**ERREUR \_ de \_ \_ REPL DRA \_ en attente**
</dt> <dd> <dl> <dt>

8477 (0x211D)
</dt> <dt>



La demande de réplication a été publiée ; en attente de réponse.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DS_REQUIRED"></span><span id="error_ds_ds_required"></span>**ERREUR \_ DS \_ \_ obligatoire**
</dt> <dd> <dl> <dt>

8478 (0x211E)
</dt> <dt>



L’opération demandée requiert un service d’annuaire et aucune n’était disponible.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INVALID_LDAP_DISPLAY_NAME"></span><span id="error_ds_invalid_ldap_display_name"></span>**ERREUR \_ DS \_ \_ \_ nom complet LDAP non valide \_**
</dt> <dd> <dl> <dt>

8479 (0x211F)
</dt> <dt>



Le nom complet LDAP de la classe ou de l’attribut contient des caractères non-ASCII.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NON_BASE_SEARCH"></span><span id="error_ds_non_base_search"></span>**ERREUR \_ DS \_ non \_ - \_ recherche de base**
</dt> <dd> <dl> <dt>

8480 (0x2120)
</dt> <dt>



L’opération de recherche demandée est uniquement prise en charge pour les recherches de base.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_RETRIEVE_ATTS"></span><span id="error_ds_cant_retrieve_atts"></span>**ERREUR \_ DS \_ Impossible de \_ récupérer \_ ATTS**
</dt> <dd> <dl> <dt>

8481 (0x2121)
</dt> <dt>



La recherche n’a pas pu récupérer les attributs de la base de données.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_BACKLINK_WITHOUT_LINK"></span><span id="error_ds_backlink_without_link"></span>**ERREUR \_ DS \_ lien secondaire \_ sans \_ lien**
</dt> <dd> <dl> <dt>

8482 (0x2122)
</dt> <dt>



L’opération de mise à jour du schéma a tenté d’ajouter un attribut de lien ascendant qui n’a pas de lien de transfert correspondant.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_EPOCH_MISMATCH"></span><span id="error_ds_epoch_mismatch"></span>**ERREUR \_ d' \_ incompatibilité de l’époque du DS \_**
</dt> <dd> <dl> <dt>

8483 (0x2123)
</dt> <dt>



La source et la destination d’un déplacement entre domaines ne sont pas d’accord sur le numéro de la époque de l’objet. La source ou la destination ne dispose pas de la dernière version de l’objet.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SRC_NAME_MISMATCH"></span><span id="error_ds_src_name_mismatch"></span>**ERREUR \_ d' \_ \_ incompatibilité de nom de source DS \_**
</dt> <dd> <dl> <dt>

8484 (0x2124)
</dt> <dt>



La source et la destination d’un déplacement entre domaines ne sont pas d’accord sur le nom actuel de l’objet. La source ou la destination ne dispose pas de la dernière version de l’objet.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SRC_AND_DST_NC_IDENTICAL"></span><span id="error_ds_src_and_dst_nc_identical"></span>**ERREUR du contrôleur \_ \_ de domaine source \_ et \_ DST \_ \_ identique**
</dt> <dd> <dl> <dt>

8485 (0x2125)
</dt> <dt>



La source et la destination de l’opération de déplacement entre domaines sont identiques. L’appelant doit utiliser l’opération de déplacement local au lieu de l’opération de déplacement entre domaines.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DST_NC_MISMATCH"></span><span id="error_ds_dst_nc_mismatch"></span>**ERREUR \_ d' \_ \_ \_ incompatibilité NC du service d’heure DS**
</dt> <dd> <dl> <dt>

8486 (0x2126)
</dt> <dt>



La source et la destination d’un déplacement entre domaines ne sont pas accordées sur les contextes d’attribution de noms de la forêt. La source ou la destination ne dispose pas de la dernière version du conteneur partitions.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NOT_AUTHORITIVE_FOR_DST_NC"></span><span id="error_ds_not_authoritive_for_dst_nc"></span>**ERREUR \_ DS \_ non \_ AUTHORITIVE \_ pour le \_ contexte d’heure d’été \_**
</dt> <dd> <dl> <dt>

8487 (0x2127)
</dt> <dt>



La destination d’un déplacement entre domaines ne fait pas autorité pour le contexte d’appellation de destination.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SRC_GUID_MISMATCH"></span><span id="error_ds_src_guid_mismatch"></span>**ERREUR \_ d' \_ \_ incompatibilité de GUID SRC DS \_**
</dt> <dd> <dl> <dt>

8488 (0x2128)
</dt> <dt>



La source et la destination d’un déplacement inter-domaines ne sont pas d’accord sur l’identité de l’objet source. La source ou la destination ne dispose pas de la dernière version de l’objet source.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_MOVE_DELETED_OBJECT"></span><span id="error_ds_cant_move_deleted_object"></span>**ERREUR \_ DS \_ Impossible de \_ déplacer l' \_ \_ objet supprimé**
</dt> <dd> <dl> <dt>

8489 (0x2129)
</dt> <dt>



L’objet en cours de déplacement entre domaines est déjà connu pour être supprimé par le serveur de destination. Le serveur source ne dispose pas de la dernière version de l’objet source.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_PDC_OPERATION_IN_PROGRESS"></span><span id="error_ds_pdc_operation_in_progress"></span>**ERREUR \_ \_ \_ de l’opération de contrôleur de domaine principal DS \_ en \_ cours**
</dt> <dd> <dl> <dt>

8490 (0x212A)
</dt> <dt>



Une autre opération qui requiert un accès exclusif au FSMO du contrôleur de domaine principal est déjà en cours.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CROSS_DOMAIN_CLEANUP_REQD"></span><span id="error_ds_cross_domain_cleanup_reqd"></span>**ERREUR \_ de \_ nettoyage inter- \_ domaines DS \_ \_ REQD**
</dt> <dd> <dl> <dt>

8491 (0x212B)
</dt> <dt>



Une opération de déplacement entre domaines a échoué, de sorte que deux versions de l’objet déplacé existent-une dans les domaines source et de destination. L’objet de destination doit être supprimé pour restaurer le système à un état cohérent.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ILLEGAL_XDOM_MOVE_OPERATION"></span><span id="error_ds_illegal_xdom_move_operation"></span>**ERREUR \_ d' \_ \_ opération de \_ déplacement \_ XDOM illégale du service d’annuaire**
</dt> <dd> <dl> <dt>

8492 (0x212C)
</dt> <dt>



Cet objet ne peut pas être déplacé au-delà des limites du domaine, soit parce que les déplacements inter-domaines pour cette classe ne sont pas autorisés, soit parce que l’objet a des caractéristiques spéciales, par exemple : compte de confiance ou RID restreint, ce qui empêche son déplacement.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_WITH_ACCT_GROUP_MEMBERSHPS"></span><span id="error_ds_cant_with_acct_group_membershps"></span>**ERREUR DS inversion \_ \_ avec le \_ \_ \_ groupe ACCT \_ MEMBERSHPS**
</dt> <dd> <dl> <dt>

8493 (0x212D)
</dt> <dt>



Impossible de déplacer des objets ayant des appartenances au-delà des limites du domaine, car une fois qu’ils sont déplacés, cela ne respecte pas les conditions d’appartenance du groupe de comptes. Supprimez l’objet des appartenances aux groupes de comptes et réessayez.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NC_MUST_HAVE_NC_PARENT"></span><span id="error_ds_nc_must_have_nc_parent"></span>**l’erreur \_ DS \_ NC \_ doit avoir un \_ \_ \_ parent NC**
</dt> <dd> <dl> <dt>

8494 (0x212E)
</dt> <dt>



Un en-tête de contexte d’appellation doit être l’enfant immédiat d’un autre en-tête de contexte d’attribution de noms, et non d’un nœud intérieur.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CR_IMPOSSIBLE_TO_VALIDATE"></span><span id="error_ds_cr_impossible_to_validate"></span>**ERREUR \_ DS \_ CR \_ Impossible \_ à \_ valider**
</dt> <dd> <dl> <dt>

8495 (0x212F)
</dt> <dt>



Le répertoire ne peut pas valider le nom de contexte de nommage proposé, car il ne contient pas de réplica du contexte d’appellation au-dessus du contexte d’appellation proposé. Vérifiez que le rôle de maître d’attribution de noms de domaine est détenu par un serveur configuré en tant que serveur de catalogue global et que le serveur est à jour avec ses partenaires de réplication. (s’applique uniquement aux maîtres d’attribution de noms de domaine Windows 2000.)


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DST_DOMAIN_NOT_NATIVE"></span><span id="error_ds_dst_domain_not_native"></span>**ERREUR \_ de \_ domaine d’heure d’été DS \_ \_ non \_ Native**
</dt> <dd> <dl> <dt>

8496 (0x2130)
</dt> <dt>



Le domaine de destination doit être en mode natif.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_MISSING_INFRASTRUCTURE_CONTAINER"></span><span id="error_ds_missing_infrastructure_container"></span>**ERREUR \_ de \_ \_ conteneur d’infrastructure manquante du service d’annuaire \_**
</dt> <dd> <dl> <dt>

8497 (0x2131)
</dt> <dt>



Impossible d’effectuer l’opération, car le serveur n’a pas de conteneur d’infrastructure dans le domaine d’intérêt.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_MOVE_ACCOUNT_GROUP"></span><span id="error_ds_cant_move_account_group"></span>**ERREUR \_ DS \_ Impossible de \_ déplacer le \_ groupe de comptes \_**
</dt> <dd> <dl> <dt>

8498 (0x2132)
</dt> <dt>



Le déplacement entre domaines de groupes de comptes non vides n’est pas autorisé.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_MOVE_RESOURCE_GROUP"></span><span id="error_ds_cant_move_resource_group"></span>**ERREUR \_ DS \_ Impossible de \_ déplacer le \_ groupe de ressources \_**
</dt> <dd> <dl> <dt>

8499 (0x2133)
</dt> <dt>



Le déplacement entre domaines de groupes de ressources non vides n’est pas autorisé.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INVALID_SEARCH_FLAG"></span><span id="error_ds_invalid_search_flag"></span>**indicateur de recherche de l’erreur \_ DS \_ non valide \_ \_**
</dt> <dd> <dl> <dt>

8500 (0x2134)
</dt> <dt>



Les indicateurs de recherche de l’attribut ne sont pas valides. Le bit ANR n’est valide que sur les attributs des chaînes Unicode ou TELETEX.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_TREE_DELETE_ABOVE_NC"></span><span id="error_ds_no_tree_delete_above_nc"></span>**ERREUR \_ DS \_ non \_ arborescence \_ supprimée \_ au-dessus du \_ contexte de nommage**
</dt> <dd> <dl> <dt>

8501 (0x2135)
</dt> <dt>



Les suppressions d’arborescence à partir d’un objet qui a une tête NC en tant que descendant ne sont pas autorisées.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_COULDNT_LOCK_TREE_FOR_DELETE"></span><span id="error_ds_couldnt_lock_tree_for_delete"></span>**ERREUR \_ \_ de l' \_ arborescence de verrous impossible DS \_ \_ pour \_ suppression**
</dt> <dd> <dl> <dt>

8502 (0x2136)
</dt> <dt>



Le service d’annuaire n’a pas pu verrouiller une arborescence en vue d’une suppression de l’arborescence, car l’arborescence était en cours d’utilisation.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_COULDNT_IDENTIFY_OBJECTS_FOR_TREE_DELETE"></span><span id="error_ds_couldnt_identify_objects_for_tree_delete"></span>**ERREUR \_ \_ Impossible \_ de l' \_ identification \_ des objets pour la \_ Suppression d’arborescence \_**
</dt> <dd> <dl> <dt>

8503 (0x2137)
</dt> <dt>



Le service d’annuaire n’a pas pu identifier la liste des objets à supprimer lors de la tentative de suppression de l’arborescence.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SAM_INIT_FAILURE"></span><span id="error_ds_sam_init_failure"></span>**ERREUR \_ échec de l’initialisation du service DS \_ sam \_ \_**
</dt> <dd> <dl> <dt>

8504 (0x2138)
</dt> <dt>



L’initialisation du gestionnaire des comptes de sécurité a échoué en raison de l’erreur suivante : %1. État d’erreur : 0x %2. Arrêtez ce système et redémarrez en mode restauration des services d’annuaire, consultez le journal des événements pour obtenir des informations plus détaillées.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SENSITIVE_GROUP_VIOLATION"></span><span id="error_ds_sensitive_group_violation"></span>**ERREUR \_ de \_ \_ violation de groupe sensible aux services d’annuaire \_**
</dt> <dd> <dl> <dt>

8505 (0x2139)
</dt> <dt>



Seul un administrateur peut modifier la liste des membres d’un groupe d’administration.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_MOD_PRIMARYGROUPID"></span><span id="error_ds_cant_mod_primarygroupid"></span>**ERREUR DS inverser \_ \_ \_ \_ PRIMARYGROUPID**
</dt> <dd> <dl> <dt>

8506 (0x213A)
</dt> <dt>



Impossible de modifier l’ID de groupe principal d’un compte de contrôleur de domaine.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ILLEGAL_BASE_SCHEMA_MOD"></span><span id="error_ds_illegal_base_schema_mod"></span>**ERREUR \_ de \_ \_ schéma de base illégal du \_ service d’annuaire \_**
</dt> <dd> <dl> <dt>

8507 (0x213B)
</dt> <dt>



Une tentative de modification du schéma de base a été effectuée.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NONSAFE_SCHEMA_CHANGE"></span><span id="error_ds_nonsafe_schema_change"></span>**ERREUR \_ de \_ changement de schéma non sécurisé DS \_ \_**
</dt> <dd> <dl> <dt>

8508 (0x213C)
</dt> <dt>



L’ajout d’un nouvel attribut obligatoire à une classe existante, la suppression d’un attribut obligatoire d’une classe existante, ou l’ajout d’un attribut facultatif à la classe spéciale Top qui n’est pas un attribut lien secondaire (directement ou par héritage, par exemple, en ajoutant ou supprimant une classe auxiliaire) n’est pas autorisé.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SCHEMA_UPDATE_DISALLOWED"></span><span id="error_ds_schema_update_disallowed"></span>**ERREUR \_ de \_ \_ mise à jour du schéma DS non \_ autorisée**
</dt> <dd> <dl> <dt>

8509 (0x213D)
</dt> <dt>



La mise à jour du schéma n’est pas autorisée sur ce contrôleur de périphérique car le contrôleur de périphérique n’est pas le propriétaire du rôle FSMO du schéma.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_CREATE_UNDER_SCHEMA"></span><span id="error_ds_cant_create_under_schema"></span>**ERREUR \_ DS \_ Impossible de \_ créer \_ sous le \_ schéma**
</dt> <dd> <dl> <dt>

8510 (0x213E)
</dt> <dt>



Impossible de créer un objet de cette classe sous le conteneur de schéma. Vous pouvez uniquement créer des objets attribute-Schema et Class-Schema sous le conteneur Schema.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INSTALL_NO_SRC_SCH_VERSION"></span><span id="error_ds_install_no_src_sch_version"></span>**ERREUR d' \_ installation du service d’annuaire \_ \_ non \_ src \_ \_ version SCH**
</dt> <dd> <dl> <dt>

8511 (0x213F)
</dt> <dt>



Le réplica/l’installation enfant n’a pas pu récupérer l’attribut objectVersion sur le conteneur de schéma sur le contrôleur de périphérique source. Soit l’attribut est manquant dans le conteneur de schéma, soit les informations d’identification fournies n’ont pas l’autorisation de le lire.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INSTALL_NO_SCH_VERSION_IN_INIFILE"></span><span id="error_ds_install_no_sch_version_in_inifile"></span>**ERREUR \_ \_ d’installation \_ de la DS non \_ \_ version SCH \_ dans \_ INIFILE**
</dt> <dd> <dl> <dt>

8512 (0x2140)
</dt> <dt>



L’installation du réplica/enfant n’a pas pu lire l’attribut objectVersion dans la section SCHEMA du fichier schema.ini dans le répertoire system32.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INVALID_GROUP_TYPE"></span><span id="error_ds_invalid_group_type"></span>**ERREUR \_ de \_ \_ type de groupe non valide DS \_**
</dt> <dd> <dl> <dt>

8513 (0x2141)
</dt> <dt>



Le type de groupe spécifié n’est pas valide.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_NEST_GLOBALGROUP_IN_MIXEDDOMAIN"></span><span id="error_ds_no_nest_globalgroup_in_mixeddomain"></span>**ERREUR \_ DS \_ non \_ imbriquer \_ GLOBALGROUP \_ dans \_ MIXEDDOMAIN**
</dt> <dd> <dl> <dt>

8514 (0x2142)
</dt> <dt>



Vous ne pouvez pas imbriquer des groupes globaux dans un domaine mixte si la sécurité est activée pour le groupe.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_NEST_LOCALGROUP_IN_MIXEDDOMAIN"></span><span id="error_ds_no_nest_localgroup_in_mixeddomain"></span>**ERREUR \_ DS \_ non \_ imbriquer un \_ localgroup \_ dans \_ MIXEDDOMAIN**
</dt> <dd> <dl> <dt>

8515 (0x2143)
</dt> <dt>



Vous ne pouvez pas imbriquer des groupes locaux dans un domaine mixte si la sécurité est activée pour le groupe.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_GLOBAL_CANT_HAVE_LOCAL_MEMBER"></span><span id="error_ds_global_cant_have_local_member"></span>**ERREUR le \_ service \_ Global DS \_ \_ ne dispose pas du \_ \_ membre local**
</dt> <dd> <dl> <dt>

8516 (0x2144)
</dt> <dt>



Un groupe global ne peut pas avoir un groupe local en tant que membre.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_GLOBAL_CANT_HAVE_UNIVERSAL_MEMBER"></span><span id="error_ds_global_cant_have_universal_member"></span>**ERREUR \_ \_ global des services DS impossible d’avoir un \_ \_ \_ \_ membre universel**
</dt> <dd> <dl> <dt>

8517 (0x2145)
</dt> <dt>



Un groupe global ne peut pas avoir un groupe universel en tant que membre.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_UNIVERSAL_CANT_HAVE_LOCAL_MEMBER"></span><span id="error_ds_universal_cant_have_local_member"></span>**ERREUR le \_ service \_ universel DS \_ \_ n’a pas de \_ \_ membre local**
</dt> <dd> <dl> <dt>

8518 (0x2146)
</dt> <dt>



Un groupe universel ne peut pas avoir un groupe local en tant que membre.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_GLOBAL_CANT_HAVE_CROSSDOMAIN_MEMBER"></span><span id="error_ds_global_cant_have_crossdomain_member"></span>**ERREUR le \_ service \_ Global DS \_ \_ ne dispose pas d’un \_ \_ membre CROSSDOMAIN**
</dt> <dd> <dl> <dt>

8519 (0x2147)
</dt> <dt>



Un groupe global ne peut pas avoir de membre inter-domaines.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_LOCAL_CANT_HAVE_CROSSDOMAIN_LOCAL_MEMBER"></span><span id="error_ds_local_cant_have_crossdomain_local_member"></span>**ERREUR \_ DS \_ local \_ Impossible d' \_ utiliser le \_ \_ membre local CROSSDOMAIN \_**
</dt> <dd> <dl> <dt>

8520 (0x2148)
</dt> <dt>



Un groupe local ne peut pas avoir un autre groupe local inter-domaines en tant que membre.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_HAVE_PRIMARY_MEMBERS"></span><span id="error_ds_have_primary_members"></span>**l’erreur \_ DS \_ a des \_ \_ membres principaux**
</dt> <dd> <dl> <dt>

8521 (0x2149)
</dt> <dt>



Un groupe avec des membres principaux ne peut pas passer à un groupe dont la sécurité est désactivée.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_STRING_SD_CONVERSION_FAILED"></span><span id="error_ds_string_sd_conversion_failed"></span>**ERREUR lors de la \_ \_ \_ conversion SD de la chaîne DS \_ \_**
</dt> <dd> <dl> <dt>

8522 (0x214A)
</dt> <dt>



Le chargement du cache de schéma n’a pas pu convertir le SD par défaut de la chaîne sur un objet de schéma de classe.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NAMING_MASTER_GC"></span><span id="error_ds_naming_master_gc"></span>**ERREUR \_ du \_ maître d’attribution de noms DS \_ \_**
</dt> <dd> <dl> <dt>

8523 (0x214B)
</dt> <dt>



Seuls les serveurs DSA configurés comme serveurs de catalogue global doivent être autorisés à conserver le rôle FSMO du maître d’attribution de noms de domaine. (s’applique uniquement aux serveurs Windows 2000.)


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DNS_LOOKUP_FAILURE"></span><span id="error_ds_dns_lookup_failure"></span>**ERREUR d’échec de la \_ \_ recherche DNS DNS \_ \_**
</dt> <dd> <dl> <dt>

8524 (0x214C)
</dt> <dt>



L’opération DSA ne peut pas continuer en raison d’un échec de la recherche DNS.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_COULDNT_UPDATE_SPNS"></span><span id="error_ds_couldnt_update_spns"></span>**ERREUR \_ de \_ \_ mise à jour des SPN impossible DS \_**
</dt> <dd> <dl> <dt>

8525 (0x214D)
</dt> <dt>



Lors du traitement d’une modification apportée au nom d’hôte DNS pour un objet, les valeurs de nom de principal du service n’ont pas pu être synchronisées.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_RETRIEVE_SD"></span><span id="error_ds_cant_retrieve_sd"></span>**ERREUR \_ DS \_ Impossible de \_ récupérer la \_ SD**
</dt> <dd> <dl> <dt>

8526 (0x214E)
</dt> <dt>



Impossible de lire l’attribut descripteur de sécurité.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_KEY_NOT_UNIQUE"></span><span id="error_ds_key_not_unique"></span>**ERREUR \_ de \_ clé DS \_ non \_ unique**
</dt> <dd> <dl> <dt>

8527 (0x214F)
</dt> <dt>



L’objet demandé est introuvable, mais un objet avec cette clé a été trouvé.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_WRONG_LINKED_ATT_SYNTAX"></span><span id="error_ds_wrong_linked_att_syntax"></span>**ERREUR \_ de \_ \_ \_ syntaxe att liée \_ à l’erreur DS**
</dt> <dd> <dl> <dt>

8528 (0x2150)
</dt> <dt>



La syntaxe de l’attribut lié en cours d’ajout est incorrecte. Les liens de transfert peuvent uniquement avoir la syntaxe 2.5.5.1, 2.5.5.7 et 2.5.5.14, et les liens de liaison ne peuvent comporter que des 2.5.5.1 de syntaxe.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SAM_NEED_BOOTKEY_PASSWORD"></span><span id="error_ds_sam_need_bootkey_password"></span>**ERREUR \_ DS \_ sam \_ nécessite \_ un \_ mot de passe BOOTKEY**
</dt> <dd> <dl> <dt>

8529 (0x2151)
</dt> <dt>



Le gestionnaire de compte de sécurité doit recevoir le mot de passe de démarrage.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SAM_NEED_BOOTKEY_FLOPPY"></span><span id="error_ds_sam_need_bootkey_floppy"></span>**ERREUR \_ DS \_ sam \_ nécessite \_ une \_ disquette BOOTKEY**
</dt> <dd> <dl> <dt>

8530 (0x2152)
</dt> <dt>



Le gestionnaire de compte de sécurité doit récupérer la clé de démarrage à partir d’une disquette.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_START"></span><span id="error_ds_cant_start"></span>**ERREUR \_ \_ Impossible de \_ Démarrer DS**
</dt> <dd> <dl> <dt>

8531 (0x2153)
</dt> <dt>



Impossible de démarrer le service d’annuaire.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INIT_FAILURE"></span><span id="error_ds_init_failure"></span>**ERREUR d' \_ initialisation du service d’annuaire \_ \_**
</dt> <dd> <dl> <dt>

8532 (0x2154)
</dt> <dt>



Les services d’annuaire n’ont pas pu démarrer.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_PKT_PRIVACY_ON_CONNECTION"></span><span id="error_ds_no_pkt_privacy_on_connection"></span>**ERREUR \_ DS \_ no \_ PKT \_ Privacy \_ on \_ Connection**
</dt> <dd> <dl> <dt>

8533 (0x2155)
</dt> <dt>



La connexion entre le client et le serveur nécessite une confidentialité du paquet ou une meilleure.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SOURCE_DOMAIN_IN_FOREST"></span><span id="error_ds_source_domain_in_forest"></span>**ERREUR \_ \_ \_ de domaine source DS dans la \_ \_ forêt**
</dt> <dd> <dl> <dt>

8534 (0x2156)
</dt> <dt>



Le domaine source n’est peut-être pas dans la même forêt que la destination.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DESTINATION_DOMAIN_NOT_IN_FOREST"></span><span id="error_ds_destination_domain_not_in_forest"></span>**ERREUR \_ \_ \_ domaine de destination DS \_ non dans la \_ \_ forêt**
</dt> <dd> <dl> <dt>

8535 (0x2157)
</dt> <dt>



Le domaine de destination doit se trouver dans la forêt.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DESTINATION_AUDITING_NOT_ENABLED"></span><span id="error_ds_destination_auditing_not_enabled"></span>**\_ \_ l’audit de destination de \_ l’annuaire d’erreurs \_ n’est pas \_ activé**
</dt> <dd> <dl> <dt>

8536 (0x2158)
</dt> <dt>



L’opération requiert l’activation de l’audit du domaine de destination.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_FIND_DC_FOR_SRC_DOMAIN"></span><span id="error_ds_cant_find_dc_for_src_domain"></span>**ERREUR \_ DS \_ Impossible \_ de trouver le \_ contrôleur \_ de domaine pour le \_ \_ domaine SRC**
</dt> <dd> <dl> <dt>

8537 (0x2159)
</dt> <dt>



L’opération n’a pas pu localiser de contrôleur de domaine pour le domaine source.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SRC_OBJ_NOT_GROUP_OR_USER"></span><span id="error_ds_src_obj_not_group_or_user"></span>**ERREUR \_ du \_ \_ \_ \_ groupe \_ ou de l' \_ utilisateur de la source DS SRC**
</dt> <dd> <dl> <dt>

8538 (0x215A)
</dt> <dt>



L’objet source doit être un groupe ou un utilisateur.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SRC_SID_EXISTS_IN_FOREST"></span><span id="error_ds_src_sid_exists_in_forest"></span>**ERREUR \_ \_ \_ de sid SRC SRC dans la \_ \_ \_ forêt**
</dt> <dd> <dl> <dt>

8539 (0x215B)
</dt> <dt>



Le SID de l’objet source existe déjà dans la forêt de destination.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SRC_AND_DST_OBJECT_CLASS_MISMATCH"></span><span id="error_ds_src_and_dst_object_class_mismatch"></span>**ERREUR \_ d' \_ \_ \_ \_ incompatibilité de la classe d’objet source et DST du \_ \_ DS**
</dt> <dd> <dl> <dt>

8540 (0x215C)
</dt> <dt>



L’objet source et l’objet de destination doivent être du même type.


</dt> </dl> </dd> <dt>

<span id="ERROR_SAM_INIT_FAILURE"></span><span id="error_sam_init_failure"></span>**ERREUR \_ sam \_ init \_ Failure**
</dt> <dd> <dl> <dt>

8541 (0x215D)
</dt> <dt>



L’initialisation du gestionnaire des comptes de sécurité a échoué en raison de l’erreur suivante : %1. État d’erreur : 0x %2. cliquez sur OK pour arrêter le système et redémarrez en Mode Coffre. Pour plus d’informations, consultez le journal des événements.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_SCHEMA_INFO_SHIP"></span><span id="error_ds_dra_schema_info_ship"></span>**ERREUR \_ d' \_ \_ informations sur le schéma DRA \_ \_ de l’annuaire**
</dt> <dd> <dl> <dt>

8542 (0x215E)
</dt> <dt>



Les informations de schéma n’ont pas pu être incluses dans la demande de réplication.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_SCHEMA_CONFLICT"></span><span id="error_ds_dra_schema_conflict"></span>**ERREUR \_ de \_ \_ conflit de schéma DRA \_ de l’annuaire**
</dt> <dd> <dl> <dt>

8543 (0x215F)
</dt> <dt>



L’opération de réplication n’a pas pu aboutir en raison d’une incompatibilité de schéma.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_EARLIER_SCHEMA_CONFLICT"></span><span id="error_ds_dra_earlier_schema_conflict"></span>**ERREUR \_ de \_ \_ schéma DRA \_ antérieur \_ du service d’annuaire**
</dt> <dd> <dl> <dt>

8544 (0x2160)
</dt> <dt>



L’opération de réplication n’a pas pu aboutir en raison d’une incompatibilité de schéma précédente.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_OBJ_NC_MISMATCH"></span><span id="error_ds_dra_obj_nc_mismatch"></span>**ERREUR de non- \_ \_ concordance du contexte de \_ \_ nommage DRA DRA \_**
</dt> <dd> <dl> <dt>

8545 (0x2161)
</dt> <dt>



Impossible d’appliquer la mise à jour de réplication, car la source ou la destination n’a pas encore reçu d’informations concernant une opération de déplacement entre domaines récente.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NC_STILL_HAS_DSAS"></span><span id="error_ds_nc_still_has_dsas"></span>**l' \_ erreur \_ DS \_ NC \_ contient toujours des \_ DSA**
</dt> <dd> <dl> <dt>

8546 (0x2162)
</dt> <dt>



Le domaine demandé n’a pas pu être supprimé, car il existe des contrôleurs de domaine qui hébergent toujours ce domaine.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_GC_REQUIRED"></span><span id="error_ds_gc_required"></span>**ERREUR \_ de \_ GC DS \_ obligatoire**
</dt> <dd> <dl> <dt>

8547 (0x2163)
</dt> <dt>



L’opération demandée ne peut être effectuée que sur un serveur de catalogue global.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_LOCAL_MEMBER_OF_LOCAL_ONLY"></span><span id="error_ds_local_member_of_local_only"></span>**ERREUR \_ \_ \_ de membre local DS \_ de \_ local \_ uniquement**
</dt> <dd> <dl> <dt>

8548 (0x2164)
</dt> <dt>



Un groupe local peut uniquement être membre d’autres groupes locaux dans le même domaine.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_FPO_IN_UNIVERSAL_GROUPS"></span><span id="error_ds_no_fpo_in_universal_groups"></span>**ERREUR \_ DS \_ non \_ FPO \_ dans \_ les \_ groupes universels**
</dt> <dd> <dl> <dt>

8549 (0x2165)
</dt> <dt>



Les principaux de sécurité étrangers ne peuvent pas être membres de groupes universels.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_ADD_TO_GC"></span><span id="error_ds_cant_add_to_gc"></span>**ERREUR \_ DS \_ Impossible \_ \_ d’ajouter à \_ gc**
</dt> <dd> <dl> <dt>

8550 (0x2166)
</dt> <dt>



L’attribut ne peut pas être répliqué dans le catalogue global pour des raisons de sécurité.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_CHECKPOINT_WITH_PDC"></span><span id="error_ds_no_checkpoint_with_pdc"></span>**ERREUR \_ DS \_ aucun \_ point de contrôle \_ avec \_ PDC**
</dt> <dd> <dl> <dt>

8551 (0x2167)
</dt> <dt>



Le point de contrôle avec le contrôleur de domaine principal n’a pas pu être pris en raison d’un trop grand nombre de modifications actuellement traitées.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SOURCE_AUDITING_NOT_ENABLED"></span><span id="error_ds_source_auditing_not_enabled"></span>**ERREUR \_ \_ d’audit de la source DS \_ \_ non \_ activée**
</dt> <dd> <dl> <dt>

8552 (0x2168)
</dt> <dt>



L’opération requiert l’activation de l’audit du domaine source.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_CREATE_IN_NONDOMAIN_NC"></span><span id="error_ds_cant_create_in_nondomain_nc"></span>**ERREUR \_ DS \_ Impossible \_ \_ de créer dans le \_ contexte de nommage de domaine \_**
</dt> <dd> <dl> <dt>

8553 (0x2169)
</dt> <dt>



Les objets principal de sécurité peuvent uniquement être créés dans des contextes d’attribution de noms de domaine.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INVALID_NAME_FOR_SPN"></span><span id="error_ds_invalid_name_for_spn"></span>**ERREUR \_ \_ \_ de nom de service d’annuaire non valide \_ pour le \_ SPN**
</dt> <dd> <dl> <dt>

8554 (0x216A)
</dt> <dt>



Impossible de construire un nom de principal du service (SPN) car le nom d’hôte fourni n’est pas au format nécessaire.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_FILTER_USES_CONTRUCTED_ATTRS"></span><span id="error_ds_filter_uses_contructed_attrs"></span>**ERREUR \_ le \_ filtre DS \_ utilise \_ construit \_ ATTRS**
</dt> <dd> <dl> <dt>

8555 (0x216B)
</dt> <dt>



Un filtre qui utilise des attributs construits a été passé.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_UNICODEPWD_NOT_IN_QUOTES"></span><span id="error_ds_unicodepwd_not_in_quotes"></span>**ERREUR \_ \_ de l’erreur DS UNICODEPWD \_ non \_ entre \_ guillemets**
</dt> <dd> <dl> <dt>

8556 (0x216C)
</dt> <dt>



La valeur de l’attribut unicodePwd doit être placée entre guillemets doubles.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_MACHINE_ACCOUNT_QUOTA_EXCEEDED"></span><span id="error_ds_machine_account_quota_exceeded"></span>**ERREUR \_ de \_ \_ dépassement du quota du compte d’ordinateur DS \_ \_**
</dt> <dd> <dl> <dt>

8557 (0x216D)
</dt> <dt>



Votre ordinateur n’a pas pu être joint au domaine. Vous avez dépassé le nombre maximal de comptes d’ordinateur que vous êtes autorisé à créer dans ce domaine. Contactez votre administrateur système pour que cette limite soit réinitialisée ou augmentée.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_MUST_BE_RUN_ON_DST_DC"></span><span id="error_ds_must_be_run_on_dst_dc"></span>**l’erreur \_ DS \_ doit \_ être \_ exécutée \_ sur le \_ \_ contrôleur de domaine DST**
</dt> <dd> <dl> <dt>

8558 (0x216E)
</dt> <dt>



Pour des raisons de sécurité, l’opération doit être exécutée sur le contrôleur de service de destination.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SRC_DC_MUST_BE_SP4_OR_GREATER"></span><span id="error_ds_src_dc_must_be_sp4_or_greater"></span>**ERREUR \_ le \_ contrôleur de domaine SRC DS \_ \_ doit \_ être \_ \_ supérieur ou égal à SP4 \_**
</dt> <dd> <dl> <dt>

8559 (0x216F)
</dt> <dt>



Pour des raisons de sécurité, le contrôleur de source doit être NT4SP4 ou supérieur.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_TREE_DELETE_CRITICAL_OBJ"></span><span id="error_ds_cant_tree_delete_critical_obj"></span>**ERREUR de suppression de l' \_ \_ \_ arborescence \_ \_ critique \_ du service d’annuaire**
</dt> <dd> <dl> <dt>

8560 (0x2170)
</dt> <dt>



Impossible de supprimer les objets de système de service d’annuaire critiques lors des opérations de suppression d’arborescence. La suppression de l’arborescence a peut-être été effectuée partiellement.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INIT_FAILURE_CONSOLE"></span><span id="error_ds_init_failure_console"></span>**ERREUR de la \_ \_ console d’échec d’initialisation DS \_ \_**
</dt> <dd> <dl> <dt>

8561 (0x2171)
</dt> <dt>



Les services d’annuaire n’ont pas pu démarrer en raison de l’erreur suivante : %1. État d’erreur : 0x %2. Cliquez sur OK pour arrêter le système. Vous pouvez utiliser la console de récupération pour diagnostiquer le système de manière minutieuse.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SAM_INIT_FAILURE_CONSOLE"></span><span id="error_ds_sam_init_failure_console"></span>**ERREUR de la console d’échec de l' \_ \_ initialisation DS sam \_ \_ \_**
</dt> <dd> <dl> <dt>

8562 (0x2172)
</dt> <dt>



L’initialisation du gestionnaire des comptes de sécurité a échoué en raison de l’erreur suivante : %1. État d’erreur : 0x %2. Cliquez sur OK pour arrêter le système. Vous pouvez utiliser la console de récupération pour diagnostiquer le système de manière minutieuse.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_FOREST_VERSION_TOO_HIGH"></span><span id="error_ds_forest_version_too_high"></span>**ERREUR \_ de \_ version de forêt DS \_ \_ trop \_ élevée**
</dt> <dd> <dl> <dt>

8563 (0x2173)
</dt> <dt>



La version du système d’exploitation est incompatible avec le niveau fonctionnel actuel de la forêt AD DS ou AD LDS niveau fonctionnel du jeu de configuration. Vous devez effectuer une mise à niveau vers une nouvelle version du système d’exploitation pour que ce serveur puisse devenir un contrôleur de domaine AD DS ou ajouter une instance de AD LDS dans ce AD DS forêt ou le jeu de configuration AD LDS.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DOMAIN_VERSION_TOO_HIGH"></span><span id="error_ds_domain_version_too_high"></span>**ERREUR \_ de \_ version de domaine DS \_ \_ trop \_ élevée**
</dt> <dd> <dl> <dt>

8564 (0x2174)
</dt> <dt>



La version du système d’exploitation installée n’est pas compatible avec le niveau fonctionnel du domaine actuel. Vous devez effectuer une mise à niveau vers une nouvelle version du système d’exploitation pour que ce serveur puisse devenir un contrôleur de domaine dans ce domaine.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_FOREST_VERSION_TOO_LOW"></span><span id="error_ds_forest_version_too_low"></span>**ERREUR \_ de \_ version de forêt DS \_ \_ trop \_ faible**
</dt> <dd> <dl> <dt>

8565 (0x2175)
</dt> <dt>



La version du système d’exploitation installé sur ce serveur ne prend plus en charge le niveau fonctionnel actuel de la forêt AD DS ou AD LDS niveau fonctionnel du jeu de configuration. Vous devez élever le niveau fonctionnel de la forêt AD DS ou AD LDS niveau fonctionnel du jeu de configuration pour que ce serveur puisse devenir un contrôleur de domaine AD DS ou une instance de AD LDS dans cette forêt ou ce jeu de configuration.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DOMAIN_VERSION_TOO_LOW"></span><span id="error_ds_domain_version_too_low"></span>**ERREUR \_ de \_ version du domaine DS \_ \_ trop \_ faible**
</dt> <dd> <dl> <dt>

8566 (0x2176)
</dt> <dt>



La version du système d’exploitation installé sur ce serveur ne prend plus en charge le niveau fonctionnel du domaine actuel. Vous devez augmenter le niveau fonctionnel du domaine pour que ce serveur puisse devenir un contrôleur de domaine dans ce domaine.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INCOMPATIBLE_VERSION"></span><span id="error_ds_incompatible_version"></span>**ERREUR \_ de \_ version incompatible de DS \_**
</dt> <dd> <dl> <dt>

8567 (0x2177)
</dt> <dt>



La version du système d’exploitation installé sur ce serveur est incompatible avec le niveau fonctionnel du domaine ou de la forêt.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_LOW_DSA_VERSION"></span><span id="error_ds_low_dsa_version"></span>**ERREUR \_ DS \_ \_ version faible DSA \_**
</dt> <dd> <dl> <dt>

8568 (0x2178)
</dt> <dt>



Le niveau fonctionnel du domaine (ou de la forêt) ne peut pas être élevé à la valeur demandée, car il existe un ou plusieurs contrôleurs de domaine dans le domaine (ou la forêt) qui sont à un niveau fonctionnel inférieur incompatible.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_BEHAVIOR_VERSION_IN_MIXEDDOMAIN"></span><span id="error_ds_no_behavior_version_in_mixeddomain"></span>**ERREUR \_ DS \_ aucune \_ \_ version \_ de comportement dans \_ MIXEDDOMAIN**
</dt> <dd> <dl> <dt>

8569 (0x2179)
</dt> <dt>



Le niveau fonctionnel de la forêt ne peut pas être élevé à la valeur demandée, car un ou plusieurs domaines sont toujours en mode de domaine mixte. Tous les domaines de la forêt doivent être en mode natif, pour vous permettre d’augmenter le niveau fonctionnel de la forêt.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NOT_SUPPORTED_SORT_ORDER"></span><span id="error_ds_not_supported_sort_order"></span>**ordre de tri des erreurs d' \_ annuaire \_ non \_ pris en charge \_ \_**
</dt> <dd> <dl> <dt>

8570 (0x217A)
</dt> <dt>



L’ordre de tri demandé n’est pas pris en charge.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NAME_NOT_UNIQUE"></span><span id="error_ds_name_not_unique"></span>**le \_ nom du service d’annuaire \_ \_ n’est pas \_ unique**
</dt> <dd> <dl> <dt>

8571 (0x217B)
</dt> <dt>



Le nom demandé existe déjà en tant qu’identificateur unique.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_MACHINE_ACCOUNT_CREATED_PRENT4"></span><span id="error_ds_machine_account_created_prent4"></span>**ERREUR \_ de \_ création du compte d’ordinateur DS \_ \_ \_ PRENT4**
</dt> <dd> <dl> <dt>

8572 (0x217C)
</dt> <dt>



Le compte d’ordinateur a été créé avant NT4. Le compte doit être recréé.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_OUT_OF_VERSION_STORE"></span><span id="error_ds_out_of_version_store"></span>**ERREUR \_ \_ de la \_ \_ Banque des versions du service d’annuaire \_**
</dt> <dd> <dl> <dt>

8573 (0x217D)
</dt> <dt>



La base de données est hors de la Banque des versions.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INCOMPATIBLE_CONTROLS_USED"></span><span id="error_ds_incompatible_controls_used"></span>**ERREUR de contrôle de l' \_ \_ incompatibilité des services DS \_ \_**
</dt> <dd> <dl> <dt>

8574 (0x217E)
</dt> <dt>



Impossible de poursuivre l’opération, car plusieurs contrôles conflictuels ont été utilisés.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_REF_DOMAIN"></span><span id="error_ds_no_ref_domain"></span>**ERREUR \_ DS \_ aucun \_ domaine de référence \_**
</dt> <dd> <dl> <dt>

8575 (0x217F)
</dt> <dt>



Impossible de trouver un domaine de référence de descripteur de sécurité valide pour cette partition.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_RESERVED_LINK_ID"></span><span id="error_ds_reserved_link_id"></span>**\_ID de \_ \_ lien réservé \_ d’erreur DS**
</dt> <dd> <dl> <dt>

8576 (0x2180)
</dt> <dt>



Échec de la mise à jour du schéma : l’identificateur de lien est réservé.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_LINK_ID_NOT_AVAILABLE"></span><span id="error_ds_link_id_not_available"></span>**ERREUR \_ d' \_ ID de lien DS \_ \_ non \_ disponible**
</dt> <dd> <dl> <dt>

8577 (0x2181)
</dt> <dt>



Échec de la mise à jour du schéma : aucun identificateur de lien n’est disponible.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_AG_CANT_HAVE_UNIVERSAL_MEMBER"></span><span id="error_ds_ag_cant_have_universal_member"></span>**ERREUR \_ DS \_ AG \_ \_ ne pas avoir de \_ \_ membre universel**
</dt> <dd> <dl> <dt>

8578 (0x2182)
</dt> <dt>



Un groupe de comptes ne peut pas avoir un groupe universel en tant que membre.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_MODIFYDN_DISALLOWED_BY_INSTANCE_TYPE"></span><span id="error_ds_modifydn_disallowed_by_instance_type"></span>**ERREUR \_ DS \_ modifyDN non \_ autorisée \_ par \_ type d’instance \_**
</dt> <dd> <dl> <dt>

8579 (0x2183)
</dt> <dt>



Les opérations de renommage ou de déplacement sur des têtes de contexte d’appellation ou des objets en lecture seule ne sont pas autorisées.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_OBJECT_MOVE_IN_SCHEMA_NC"></span><span id="error_ds_no_object_move_in_schema_nc"></span>**ERREUR \_ DS \_ aucun \_ \_ déplacement \_ d’objet dans le \_ contexte de nommage de schéma \_**
</dt> <dd> <dl> <dt>

8580 (0x2184)
</dt> <dt>



Les opérations de déplacement sur les objets dans le contexte de nommage de schéma ne sont pas autorisées.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_MODIFYDN_DISALLOWED_BY_FLAG"></span><span id="error_ds_modifydn_disallowed_by_flag"></span>**ERREUR \_ DS \_ modifyDN non \_ autorisée \_ par l' \_ indicateur**
</dt> <dd> <dl> <dt>

8581 (0x2185)
</dt> <dt>



Un indicateur système a été défini sur l’objet et ne permet pas de déplacer ou de renommer l’objet.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_MODIFYDN_WRONG_GRANDPARENT"></span><span id="error_ds_modifydn_wrong_grandparent"></span>**ERREUR \_ DS modifyDN le grand- \_ \_ parent incorrect \_**
</dt> <dd> <dl> <dt>

8582 (0x2186)
</dt> <dt>



Cet objet n’est pas autorisé à modifier son conteneur grand-parent. Les déplacements ne sont pas interdits sur cet objet, mais sont limités aux conteneurs frères.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NAME_ERROR_TRUST_REFERRAL"></span><span id="error_ds_name_error_trust_referral"></span>**ERREUR de référence de l' \_ approbation d’erreur de nom de service d’annuaire \_ \_ \_ \_**
</dt> <dd> <dl> <dt>

8583 (0x2187)
</dt> <dt>



Impossible de résoudre complètement, une référence à une autre forêt est générée.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_SUPPORTED_ON_STANDARD_SERVER"></span><span id="error_not_supported_on_standard_server"></span>**ERREUR \_ non \_ prise en charge \_ sur le \_ \_ serveur standard**
</dt> <dd> <dl> <dt>

8584 (0x2188)
</dt> <dt>



L’action demandée n’est pas prise en charge sur le serveur standard.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_ACCESS_REMOTE_PART_OF_AD"></span><span id="error_ds_cant_access_remote_part_of_ad"></span>**ERREUR \_ DS \_ Impossible \_ \_ d’accéder à la partie distante \_ \_ d' \_ ad**
</dt> <dd> <dl> <dt>

8585 (0x2189)
</dt> <dt>



Impossible d’accéder à une partition du service d’annuaire situé sur un serveur distant. Assurez-vous qu’au moins un serveur est en cours d’exécution pour la partition en question.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CR_IMPOSSIBLE_TO_VALIDATE_V2"></span><span id="error_ds_cr_impossible_to_validate_v2"></span>**ERREUR \_ DS \_ CR \_ Impossible \_ de \_ valider \_ v2**
</dt> <dd> <dl> <dt>

8586 (0x218A)
</dt> <dt>



Le répertoire ne peut pas valider le nom de contexte de nommage (ou de partition) proposé, car il ne contient pas de réplica et ne peut pas contacter un réplica du contexte d’appellation au-dessus du contexte de nommage proposé. Assurez-vous que le contexte de nommage parent est correctement inscrit dans DNS, et qu’au moins un réplica de ce contexte de nommage est accessible par le maître d’attribution de noms de domaine.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_THREAD_LIMIT_EXCEEDED"></span><span id="error_ds_thread_limit_exceeded"></span>**limite de threads de l’annuaire des erreurs \_ \_ \_ \_ dépassée**
</dt> <dd> <dl> <dt>

8587 (0x218B)
</dt> <dt>



La limite de threads pour cette requête a été dépassée.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NOT_CLOSEST"></span><span id="error_ds_not_closest"></span>**ERREUR \_ DS \_ non \_ plus proche**
</dt> <dd> <dl> <dt>

8588 (0x218C)
</dt> <dt>



Le serveur de catalogue global n’est pas sur le site le plus proche.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_DERIVE_SPN_WITHOUT_SERVER_REF"></span><span id="error_ds_cant_derive_spn_without_server_ref"></span>**ERREUR \_ DS \_ Impossible de \_ dériver le \_ SPN \_ sans \_ serveur de \_ référence**
</dt> <dd> <dl> <dt>

8589 (0x218D)
</dt> <dt>



Le DS ne peut pas dériver un nom de principal du service (SPN) avec lequel authentifier mutuellement le serveur cible, car l’objet serveur correspondant dans la base de données DS locale n’a pas d’attribut serverReference.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SINGLE_USER_MODE_FAILED"></span><span id="error_ds_single_user_mode_failed"></span>**ERREUR \_ \_ échec du mode mono-utilisateur du service d’annuaire \_ \_ \_**
</dt> <dd> <dl> <dt>

8590 (0x218E)
</dt> <dt>



Le service d’annuaire n’a pas pu passer en mode mono-utilisateur.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NTDSCRIPT_SYNTAX_ERROR"></span><span id="error_ds_ntdscript_syntax_error"></span>**erreur \_ de \_ syntaxe de NTDSCRIPT du service d’annuaire \_ \_**
</dt> <dd> <dl> <dt>

8591 (0x218F)
</dt> <dt>



Le service d’annuaire ne peut pas analyser le script en raison d’une erreur de syntaxe.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NTDSCRIPT_PROCESS_ERROR"></span><span id="error_ds_ntdscript_process_error"></span>**erreur \_ de \_ \_ traitement NTDSCRIPT \_ de l’annuaire d’erreurs**
</dt> <dd> <dl> <dt>

8592 (0x2190)
</dt> <dt>



Le service d’annuaire ne peut pas traiter le script en raison d’une erreur.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DIFFERENT_REPL_EPOCHS"></span><span id="error_ds_different_repl_epochs"></span>**ERREUR \_ des \_ \_ époques de réplication différente DS \_**
</dt> <dd> <dl> <dt>

8593 (0x2191)
</dt> <dt>



Le service d’annuaire ne peut pas effectuer l’opération demandée, car les serveurs impliqués ont des époques de réplication différentes (généralement liées à un changement de nom de domaine en cours).


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRS_EXTENSIONS_CHANGED"></span><span id="error_ds_drs_extensions_changed"></span>**ERREUR \_ de \_ \_ modification des extensions \_ des services d’annuaire**
</dt> <dd> <dl> <dt>

8594 (0x2192)
</dt> <dt>



La liaison de service d’annuaire doit être renégociée en raison d’une modification des informations des extensions serveur.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_REPLICA_SET_CHANGE_NOT_ALLOWED_ON_DISABLED_CR"></span><span id="error_ds_replica_set_change_not_allowed_on_disabled_cr"></span>**ERREUR \_ \_ \_ de modification du jeu de réplicas DS \_ \_ non \_ autorisée \_ sur un \_ \_ CR désactivé**
</dt> <dd> <dl> <dt>

8595 (0x2193)
</dt> <dt>



Opération non autorisée sur une référence croisée désactivée.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_MSDS_INTID"></span><span id="error_ds_no_msds_intid"></span>**ERREUR \_ DS \_ no \_ MSDS \_ IntID**
</dt> <dd> <dl> <dt>

8596 (0x2194)
</dt> <dt>



Échec de la mise à jour du schéma : aucune valeur pour msDS-IntId n’est disponible.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DUP_MSDS_INTID"></span><span id="error_ds_dup_msds_intid"></span>**ERREUR \_ MSDS de l' \_ attribut de reduplication du DS \_ \_**
</dt> <dd> <dl> <dt>

8597 (0x2195)
</dt> <dt>



Échec de la mise à jour du schéma : msDS-INtId dupliqué. Retentez l’opération.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_EXISTS_IN_RDNATTID"></span><span id="error_ds_exists_in_rdnattid"></span>**\_l’erreur DS \_ existe \_ dans \_ RDNATTID**
</dt> <dd> <dl> <dt>

8598 (0x2196)
</dt> <dt>



Échec de la suppression du schéma : l’attribut est utilisé dans rDNAttID.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_AUTHORIZATION_FAILED"></span><span id="error_ds_authorization_failed"></span>**ERREUR \_ échec de l’autorisation du service \_ d’annuaire \_**
</dt> <dd> <dl> <dt>

8599 (0x2197)
</dt> <dt>



Le service d’annuaire n’a pas pu autoriser la demande.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INVALID_SCRIPT"></span><span id="error_ds_invalid_script"></span>**ERREUR \_ de \_ script DS non valide \_**
</dt> <dd> <dl> <dt>

8600 (0x2198)
</dt> <dt>



Le service d’annuaire ne peut pas traiter le script, car il n’est pas valide.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_REMOTE_CROSSREF_OP_FAILED"></span><span id="error_ds_remote_crossref_op_failed"></span>**erreur Échec de l’opération de l’erreur de la \_ \_ CROSSREF à distance DS \_ \_ \_**
</dt> <dd> <dl> <dt>

8601 (0x2199)
</dt> <dt>



Échec de l’opération de création d’une référence croisée distante sur le FSMO du maître d’attribution de noms de domaine. L’erreur de l’opération se trouve dans les données étendues.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CROSS_REF_BUSY"></span><span id="error_ds_cross_ref_busy"></span>**ERREUR \_ \_ croisée de \_ référence des \_ services de domaine Active Directory**
</dt> <dd> <dl> <dt>

8602 (0x219A)
</dt> <dt>



Une référence croisée est en cours d’utilisation localement avec le même nom.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_DERIVE_SPN_FOR_DELETED_DOMAIN"></span><span id="error_ds_cant_derive_spn_for_deleted_domain"></span>**ERREUR \_ DS \_ Impossible \_ de dériver le \_ SPN \_ pour le \_ \_ domaine supprimé**
</dt> <dd> <dl> <dt>

8603 (0x219B)
</dt> <dt>



Le DS ne peut pas dériver un nom de principal du service (SPN) avec lequel authentifier mutuellement le serveur cible, car le domaine du serveur a été supprimé de la forêt.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_DEMOTE_WITH_WRITEABLE_NC"></span><span id="error_ds_cant_demote_with_writeable_nc"></span>**ERREUR \_ DS \_ Impossible \_ de rétrograder \_ avec le \_ contexte de \_ nommage inscriptible**
</dt> <dd> <dl> <dt>

8604 (0x219C)
</dt> <dt>



Les NC inscriptibles empêchent ce contrôleur de l’être de rétrograder.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DUPLICATE_ID_FOUND"></span><span id="error_ds_duplicate_id_found"></span>**ERREUR \_ ID dupliqué de l’annuaire de services \_ \_ \_ trouvée**
</dt> <dd> <dl> <dt>

8605 (0x219D)
</dt> <dt>



L’objet demandé a un identificateur non unique et ne peut pas être récupéré.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INSUFFICIENT_ATTR_TO_CREATE_OBJECT"></span><span id="error_ds_insufficient_attr_to_create_object"></span>**ERREUR \_ Impossible \_ pour l’attr insuffisant \_ \_ pour \_ créer un \_ objet**
</dt> <dd> <dl> <dt>

8606 (0x219E)
</dt> <dt>



Des attributs insuffisants ont été donnés pour créer un objet. Cet objet n’existe peut-être pas, car il a peut-être été supprimé et a déjà été récupéré par le garbage collector.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_GROUP_CONVERSION_ERROR"></span><span id="error_ds_group_conversion_error"></span>**erreur \_ de \_ conversion du groupe des services d’annuaire \_ \_**
</dt> <dd> <dl> <dt>

8607 (0x219F)
</dt> <dt>



Le groupe ne peut pas être converti en raison de restrictions d’attribut sur le type de groupe demandé.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_MOVE_APP_BASIC_GROUP"></span><span id="error_ds_cant_move_app_basic_group"></span>**ERREUR \_ DS \_ Impossible de \_ déplacer le \_ \_ groupe de base \_**
</dt> <dd> <dl> <dt>

8608 (0x21A0)
</dt> <dt>



Le déplacement entre domaines de groupes d’applications de base non vides n’est pas autorisé.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_MOVE_APP_QUERY_GROUP"></span><span id="error_ds_cant_move_app_query_group"></span>**ERREUR \_ DS \_ Impossible de \_ déplacer le groupe de \_ requêtes d’application \_ \_**
</dt> <dd> <dl> <dt>

8609 (0x21A1)
</dt> <dt>



Le déplacement entre domaines d’un groupe d’applications non vide basé sur une requête n’est pas autorisé.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ROLE_NOT_VERIFIED"></span><span id="error_ds_role_not_verified"></span>**le rôle de l’annuaire d’erreurs \_ \_ n’a \_ pas été \_ vérifié**
</dt> <dd> <dl> <dt>

8610 (0x21A2)
</dt> <dt>



La propriété du rôle FSMO n’a pas pu être vérifiée, car sa partition d’annuaire n’a pas été répliquée avec au moins un partenaire de réplication.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_WKO_CONTAINER_CANNOT_BE_SPECIAL"></span><span id="error_ds_wko_container_cannot_be_special"></span>**ERREUR \_ le \_ conteneur WKO DS \_ \_ ne peut pas \_ être \_ spécial**
</dt> <dd> <dl> <dt>

8611 (0x21A3)
</dt> <dt>



Le conteneur cible pour une redirection d’un conteneur d’objets bien connu ne peut pas déjà être un conteneur spécial.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DOMAIN_RENAME_IN_PROGRESS"></span><span id="error_ds_domain_rename_in_progress"></span>**ERREUR \_ \_ \_ de changement de nom \_ de domaine DS en \_ cours**
</dt> <dd> <dl> <dt>

8612 (0x21A4)
</dt> <dt>



Le service d’annuaire ne peut pas effectuer l’opération demandée, car une opération de changement de nom de domaine est en cours.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_EXISTING_AD_CHILD_NC"></span><span id="error_ds_existing_ad_child_nc"></span>**ERREUR \_ du \_ \_ contexte de \_ nommage enfant ad \_ de l’annuaire Active Directory existant**
</dt> <dd> <dl> <dt>

8613 (0x21A5)
</dt> <dt>



Le service d’annuaire a détecté une partition enfant sous le nom de partition demandé. La hiérarchie de la partition doit être créée dans une méthode de haut en haut.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_REPL_LIFETIME_EXCEEDED"></span><span id="error_ds_repl_lifetime_exceeded"></span>**ERREUR \_ de \_ durée de vie de réplication DS \_ \_ dépassée**
</dt> <dd> <dl> <dt>

8614 (0x21A6)
</dt> <dt>



Le service d’annuaire ne peut pas répliquer avec ce serveur, car la durée de vie de la dernière réplication avec ce serveur a dépassé la durée de vie de désactivation.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DISALLOWED_IN_SYSTEM_CONTAINER"></span><span id="error_ds_disallowed_in_system_container"></span>**ERREUR \_ DS non \_ autorisée \_ dans le \_ \_ conteneur système**
</dt> <dd> <dl> <dt>

8615 (0x21A7)
</dt> <dt>



L’opération demandée n’est pas autorisée sur un objet sous le conteneur système.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_LDAP_SEND_QUEUE_FULL"></span><span id="error_ds_ldap_send_queue_full"></span>**ERREUR de saturation de la \_ \_ \_ \_ file d’attente d’envoi LDAP DS \_**
</dt> <dd> <dl> <dt>

8616 (0x21A8)
</dt> <dt>



La file d’attente d’envoi réseau des serveurs LDAP a été remplie car le client ne traite pas les résultats de ses demandes suffisamment rapidement. Aucune demande supplémentaire n’est traitée tant que le client n’a pas effectué la capture. Si le client ne rattrape pas le problème, il sera déconnecté.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_OUT_SCHEDULE_WINDOW"></span><span id="error_ds_dra_out_schedule_window"></span>**fenêtre d’erreur de planification de la récupération du \_ service d’annuaire \_ \_ \_ \_**
</dt> <dd> <dl> <dt>

8617 (0x21A9)
</dt> <dt>



La réplication planifiée n’a pas eu lieu car le système était trop occupé pour exécuter la demande dans la fenêtre de planification. La file d’attente de réplication est surchargée. Envisagez de réduire le nombre de partenaires ou de réduire la fréquence de réplication planifiée.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_POLICY_NOT_KNOWN"></span><span id="error_ds_policy_not_known"></span>**ERREUR \_ de \_ stratégie DS \_ non \_ connue**
</dt> <dd> <dl> <dt>

8618 (0x21AA)
</dt> <dt>



À ce stade, il n’est pas possible de déterminer si la stratégie de réplication de branche est disponible sur le contrôleur de domaine Hub. Réessayez ultérieurement pour prendre en compte les latences de réplication.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_SITE_SETTINGS_OBJECT"></span><span id="error_no_site_settings_object"></span>**ERREUR \_ aucun \_ \_ objet paramètres de site \_**
</dt> <dd> <dl> <dt>

8619 (0x21AB)
</dt> <dt>



L’objet de paramètres de site pour le site spécifié n’existe pas.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_SECRETS"></span><span id="error_no_secrets"></span>**ERREUR \_ aucun \_ secret**
</dt> <dd> <dl> <dt>

8620 (0x21AC)
</dt> <dt>



Le magasin de comptes local ne contient pas de matériel secret pour le compte spécifié.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_WRITABLE_DC_FOUND"></span><span id="error_no_writable_dc_found"></span>**ERREUR \_ aucun \_ contrôleur de périphérique accessible en écriture \_ \_ trouvé**
</dt> <dd> <dl> <dt>

8621 (0x21AD)
</dt> <dt>



Impossible de trouver un contrôleur de domaine accessible en écriture dans le domaine.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_SERVER_OBJECT"></span><span id="error_ds_no_server_object"></span>**ERREUR \_ DS \_ aucun \_ \_ objet serveur**
</dt> <dd> <dl> <dt>

8622 (0x21AE)
</dt> <dt>



L’objet serveur pour le contrôleur de domaine n’existe pas.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_NTDSA_OBJECT"></span><span id="error_ds_no_ntdsa_object"></span>**ERREUR \_ DS \_ no \_ ntdsa \_**
</dt> <dd> <dl> <dt>

8623 (0x21AF)
</dt> <dt>



l’objet Paramètres NTDS du contrôleur de domaine n’existe pas.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NON_ASQ_SEARCH"></span><span id="error_ds_non_asq_search"></span>**ERREUR \_ DS \_ \_ recherche non ASQ \_**
</dt> <dd> <dl> <dt>

8624 (0x21B0)
</dt> <dt>



L’opération de recherche demandée n’est pas prise en charge pour les recherches ASQ.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_AUDIT_FAILURE"></span><span id="error_ds_audit_failure"></span>**ERREUR \_ \_ d’audit du service d’annuaire \_**
</dt> <dd> <dl> <dt>

8625 (0x21B1)
</dt> <dt>



Un événement d’audit requis n’a pas pu être généré pour l’opération.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INVALID_SEARCH_FLAG_SUBTREE"></span><span id="error_ds_invalid_search_flag_subtree"></span>**ERREUR de sous-arborescence de l' \_ \_ indicateur de recherche non valide DS \_ \_ \_**
</dt> <dd> <dl> <dt>

8626 (0x21B2)
</dt> <dt>



Les indicateurs de recherche de l’attribut ne sont pas valides. Le bit d’index de sous-arborescence n’est valide que sur des attributs à valeur unique.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INVALID_SEARCH_FLAG_TUPLE"></span><span id="error_ds_invalid_search_flag_tuple"></span>**ERREUR du TUPLE de l' \_ \_ indicateur de recherche non valide DS \_ \_ \_**
</dt> <dd> <dl> <dt>

8627 (0x21B3)
</dt> <dt>



Les indicateurs de recherche de l’attribut ne sont pas valides. Le bit d’index de tuple est valide uniquement sur les attributs de chaînes Unicode.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_HIERARCHY_TABLE_TOO_DEEP"></span><span id="error_ds_hierarchy_table_too_deep"></span>**ERREUR de \_ table de hiérarchie des services d’annuaire \_ \_ \_ trop \_ profonde**
</dt> <dd> <dl> <dt>

8628 (0x21B4)
</dt> <dt>



Les carnets d’adresses sont imbriqués trop profondément. Échec de la création de la table de hiérarchie.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_CORRUPT_UTD_VECTOR"></span><span id="error_ds_dra_corrupt_utd_vector"></span>**ERREUR \_ du \_ \_ \_ vecteur UTD) de l’agent DRA endommagé \_**
</dt> <dd> <dl> <dt>

8629 (0x21B5)
</dt> <dt>



Le vecteur d’inscription à jour spécifié est endommagé.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_SECRETS_DENIED"></span><span id="error_ds_dra_secrets_denied"></span>**ERREUR \_ de \_ \_ secrets DRA \_ refusés**
</dt> <dd> <dl> <dt>

8630 (0x21B6)
</dt> <dt>



La demande de réplication des secrets est refusée.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_RESERVED_MAPI_ID"></span><span id="error_ds_reserved_mapi_id"></span>**\_ \_ \_ ID MAPI réservé de l’annuaire d’erreurs \_**
</dt> <dd> <dl> <dt>

8631 (0x21B7)
</dt> <dt>



Échec de la mise à jour du schéma : l’identificateur MAPI est réservé.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_MAPI_ID_NOT_AVAILABLE"></span><span id="error_ds_mapi_id_not_available"></span>**ERREUR de l' \_ \_ ID MAPI MAPI \_ \_ non \_ disponible**
</dt> <dd> <dl> <dt>

8632 (0x21B8)
</dt> <dt>



Échec de la mise à jour du schéma : aucun identificateur MAPI n’est disponible.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_MISSING_KRBTGT_SECRET"></span><span id="error_ds_dra_missing_krbtgt_secret"></span>**ERREUR \_ le \_ \_ \_ secret krbtgt est manquant dans le DRA du DS \_**
</dt> <dd> <dl> <dt>

8633 (0x21B9)
</dt> <dt>



L’opération de réplication a échoué car les attributs requis de l’objet krbtgt local sont manquants.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DOMAIN_NAME_EXISTS_IN_FOREST"></span><span id="error_ds_domain_name_exists_in_forest"></span>**ERREUR \_ le \_ \_ nom de domaine DS \_ existe dans la \_ \_ forêt**
</dt> <dd> <dl> <dt>

8634 (0x21BA)
</dt> <dt>



Le nom de domaine du domaine approuvé existe déjà dans la forêt.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_FLAT_NAME_EXISTS_IN_FOREST"></span><span id="error_ds_flat_name_exists_in_forest"></span>**ERREUR \_ \_ \_ de nom plat DS dans la \_ \_ \_ forêt**
</dt> <dd> <dl> <dt>

8635 (0x21BB)
</dt> <dt>



Le nom plat du domaine approuvé existe déjà dans la forêt.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_USER_PRINCIPAL_NAME"></span><span id="error_invalid_user_principal_name"></span>**ERREUR \_ \_ nom d’utilisateur \_ principal \_ non valide**
</dt> <dd> <dl> <dt>

8636 (0x21BC)
</dt> <dt>



Le nom d’utilisateur principal (UPN) n’est pas valide.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_OID_MAPPED_GROUP_CANT_HAVE_MEMBERS"></span><span id="error_ds_oid_mapped_group_cant_have_members"></span>**ERREUR \_ le \_ groupe mappé de l’OID des services de domaine \_ \_ \_ \_ a des \_ membres**
</dt> <dd> <dl> <dt>

8637 (0x21BD)
</dt> <dt>



Les groupes mappés OID ne peuvent pas avoir de membres.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_OID_NOT_FOUND"></span><span id="error_ds_oid_not_found"></span>**ERREUR de l' \_ OID du DS \_ \_ \_ introuvable**
</dt> <dd> <dl> <dt>

8638 (0x21BE)
</dt> <dt>



L’OID spécifié est introuvable.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_RECYCLED_TARGET"></span><span id="error_ds_dra_recycled_target"></span>**ERREUR de la \_ \_ \_ cible recyclée DRA \_**
</dt> <dd> <dl> <dt>

8639 (0x21BF)
</dt> <dt>



L’opération de réplication a échoué, car l’objet cible référencé par une valeur de lien est recyclé.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DISALLOWED_NC_REDIRECT"></span><span id="error_ds_disallowed_nc_redirect"></span>**ERREUR \_ de \_ \_ redirection NC non autorisée dans le service d’annuaire \_**
</dt> <dd> <dl> <dt>

8640 (0x21C0)
</dt> <dt>



L’opération de redirection a échoué, car l’objet cible est dans un contexte de nommage différent du contexte de nommage de domaine du contrôleur de domaine actuel.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_HIGH_ADLDS_FFL"></span><span id="error_ds_high_adlds_ffl"></span>**ERREUR \_ DS \_ High \_ ADLDS \_ FFL**
</dt> <dd> <dl> <dt>

8641 (0x21C1)
</dt> <dt>



Le niveau fonctionnel du jeu de configuration AD LDS ne peut pas être abaissé à la valeur demandée.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_HIGH_DSA_VERSION"></span><span id="error_ds_high_dsa_version"></span>**ERREUR \_ de \_ \_ version DSA \_ élevée du DS**
</dt> <dd> <dl> <dt>

8642 (0x21C2)
</dt> <dt>



Le niveau fonctionnel du domaine (ou de la forêt) ne peut pas être abaissé à la valeur demandée.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_LOW_ADLDS_FFL"></span><span id="error_ds_low_adlds_ffl"></span>**ERREUR \_ DS \_ Low \_ ADLDS \_ FFL**
</dt> <dd> <dl> <dt>

8643 (0x21C3)
</dt> <dt>



Le niveau fonctionnel du jeu de configuration AD LDS ne peut pas être élevé à la valeur demandée, car il existe une ou plusieurs instances ADLDS qui ont un niveau fonctionnel inférieur incompatible.


</dt> </dl> </dd> <dt>

<span id="ERROR_DOMAIN_SID_SAME_AS_LOCAL_WORKSTATION"></span><span id="error_domain_sid_same_as_local_workstation"></span>**SID du domaine d’erreur \_ \_ \_ identique \_ à la \_ station de \_ travail locale**
</dt> <dd> <dl> <dt>

8644 (0x21C4)
</dt> <dt>



La jonction de domaine ne peut pas être effectuée, car le SID du domaine que vous avez tenté de joindre était identique au SID de cet ordinateur. Il s’agit d’un symptôme de l’installation d’un système d’exploitation cloné de manière incorrecte. Vous devez exécuter Sysprep sur cet ordinateur afin de générer un nouveau SID d’ordinateur. Pour plus d’informations, consultez <https://go.microsoft.com/fwlink/p/?linkid=168895>.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_UNDELETE_SAM_VALIDATION_FAILED"></span><span id="error_ds_undelete_sam_validation_failed"></span>**ERREUR \_ \_ échec de la \_ \_ validation sam \_ de l’annulation de la suppression du service d’annuaire**
</dt> <dd> <dl> <dt>

8645 (0x21C5)
</dt> <dt>



L’opération d’annulation de suppression a échoué, car le nom de compte Sam ou le nom de compte Sam supplémentaire de l’objet en cours de restauration est en conflit avec un objet dynamique existant.


</dt> </dl> </dd> <dt>

<span id="ERROR_INCORRECT_ACCOUNT_TYPE"></span><span id="error_incorrect_account_type"></span>**ERREUR \_ de \_ type de compte incorrect \_**
</dt> <dd> <dl> <dt>

8646 (0x21C6)
</dt> <dt>



Le système ne fait pas autorité pour le compte spécifié et ne peut donc pas terminer l’opération. Recommencez l’opération en utilisant le fournisseur associé à ce compte. S’il s’agit d’un fournisseur en ligne, utilisez le site en ligne du fournisseur.


</dt> </dl> </dd> </dl>


## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>                                           |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>WinError. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Codes d’erreur système](system-error-codes.md)
</dt> </dl>

 

 




