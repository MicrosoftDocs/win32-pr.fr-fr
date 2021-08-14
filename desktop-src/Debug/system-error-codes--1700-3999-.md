---
description: Décrit les codes d’erreur 1700-3999 définis dans le fichier d’en-tête WinError. h et est destiné aux développeurs.
ms.assetid: 7e57c087-53e4-443d-9227-21d9eb3cc71f
title: Codes d’erreur système (1700-3999) (WinError. h)
ms.topic: reference
ms.date: 07/18/2019
ms.openlocfilehash: 707425f7714c84d92bf5bc001f57c1677183b9edbd9170236d1c629bc0aaf121
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118405600"
---
# <a name="system-error-codes-1700-3999"></a>Codes d’erreur système (1700-3999)

> [!NOTE]
> Ces informations sont destinées aux développeurs qui déboguent les erreurs système. pour les autres erreurs, telles que les problèmes de Windows Update, il existe une liste de ressources dans la page [codes d’erreur](system-error-codes.md) .

La liste suivante décrit les [codes d’erreur système](system-error-codes.md) pour les erreurs 1700 à 3999. Elles sont retournées par la fonction [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) lorsque de nombreuses fonctions échouent. Pour récupérer le texte de description de l’erreur dans votre application, utilisez la fonction [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) avec le **format \_ message \_ de \_** l’indicateur système.

<dl> <dt>

<span id="RPC_S_INVALID_STRING_BINDING"></span><span id="rpc_s_invalid_string_binding"></span>**RPC \_ S \_ \_ liaison de chaîne non valide \_**
</dt> <dd> <dl> <dt>

1700 (0x6A4)
</dt> <dt>



La liaison de chaîne n’est pas valide.


</dt> </dl> </dd> <dt>

<span id="RPC_S_WRONG_KIND_OF_BINDING"></span><span id="rpc_s_wrong_kind_of_binding"></span>**le \_ \_ \_ type \_ de liaison RPC \_ est incorrect**
</dt> <dd> <dl> <dt>

1701 (0x6A5)
</dt> <dt>



Le type du handle de liaison n’est pas correct.


</dt> </dl> </dd> <dt>

<span id="RPC_S_INVALID_BINDING"></span><span id="rpc_s_invalid_binding"></span>**\_liaison RPC S \_ non valide \_**
</dt> <dd> <dl> <dt>

1702 (0x6A6)
</dt> <dt>



Le handle de liaison n’est pas valide.


</dt> </dl> </dd> <dt>

<span id="RPC_S_PROTSEQ_NOT_SUPPORTED"></span><span id="rpc_s_protseq_not_supported"></span>**RPC \_ S \_ PROTSEQ \_ non \_ pris en charge**
</dt> <dd> <dl> <dt>

1703 (0x6A7)
</dt> <dt>



La séquence de protocole RPC n’est pas prise en charge.


</dt> </dl> </dd> <dt>

<span id="RPC_S_INVALID_RPC_PROTSEQ"></span><span id="rpc_s_invalid_rpc_protseq"></span>**RPC \_ S \_ PROTSEQ non valide \_ \_**
</dt> <dd> <dl> <dt>

1704 (0x6A8)
</dt> <dt>



La séquence de protocole RPC n’est pas valide.


</dt> </dl> </dd> <dt>

<span id="RPC_S_INVALID_STRING_UUID"></span><span id="rpc_s_invalid_string_uuid"></span>**\_UUID de \_ chaîne non valide RPC \_ \_**
</dt> <dd> <dl> <dt>

1705 (0x6A9)
</dt> <dt>



L’identificateur unique universel (UUID) de la chaîne n’est pas valide.


</dt> </dl> </dd> <dt>

<span id="RPC_S_INVALID_ENDPOINT_FORMAT"></span><span id="rpc_s_invalid_endpoint_format"></span>**FORMAT de point de terminaison de RPC \_ S \_ non valide \_ \_**
</dt> <dd> <dl> <dt>

1706 (0x6AA)
</dt> <dt>



Le format du point de terminaison n’est pas valide.


</dt> </dl> </dd> <dt>

<span id="RPC_S_INVALID_NET_ADDR"></span><span id="rpc_s_invalid_net_addr"></span>**\_ \_ \_ adresse réseau non valide \_ RPC**
</dt> <dd> <dl> <dt>

1707 (0x6AB)
</dt> <dt>



L’adresse réseau n’est pas valide.


</dt> </dl> </dd> <dt>

<span id="RPC_S_NO_ENDPOINT_FOUND"></span><span id="rpc_s_no_endpoint_found"></span>**\_ \_ aucun point de \_ terminaison RPC n' \_ a été trouvé**
</dt> <dd> <dl> <dt>

1708 (0x6AC)
</dt> <dt>



Aucun point de terminaison n’a été trouvé.


</dt> </dl> </dd> <dt>

<span id="RPC_S_INVALID_TIMEOUT"></span><span id="rpc_s_invalid_timeout"></span>**\_ \_ \_ délai d’attente des S RPC non valide**
</dt> <dd> <dl> <dt>

1709 (0x6AD)
</dt> <dt>



La valeur du délai d’attente n’est pas valide.


</dt> </dl> </dd> <dt>

<span id="RPC_S_OBJECT_NOT_FOUND"></span><span id="rpc_s_object_not_found"></span>**\_objet RPC \_ S \_ \_ introuvable**
</dt> <dd> <dl> <dt>

1710 (0x6AE)
</dt> <dt>



L’identificateur unique universel (UUID) de l’objet est introuvable.


</dt> </dl> </dd> <dt>

<span id="RPC_S_ALREADY_REGISTERED"></span><span id="rpc_s_already_registered"></span>**RPC \_ \_ déjà \_ inscrit**
</dt> <dd> <dl> <dt>

1711 (0x6AF)
</dt> <dt>



L’identificateur unique universel (UUID) de l’objet a déjà été inscrit.


</dt> </dl> </dd> <dt>

<span id="RPC_S_TYPE_ALREADY_REGISTERED"></span><span id="rpc_s_type_already_registered"></span>**\_type RPC \_ S \_ déjà \_ inscrit**
</dt> <dd> <dl> <dt>

1712 (0x6B0)
</dt> <dt>



Le type d’identificateur unique universel (UUID) a déjà été inscrit.


</dt> </dl> </dd> <dt>

<span id="RPC_S_ALREADY_LISTENING"></span><span id="rpc_s_already_listening"></span>**RPC \_ déjà à l' \_ \_ écoute**
</dt> <dd> <dl> <dt>

1713 (0x6B1)
</dt> <dt>



Le serveur RPC est déjà à l’écoute.


</dt> </dl> </dd> <dt>

<span id="RPC_S_NO_PROTSEQS_REGISTERED"></span><span id="rpc_s_no_protseqs_registered"></span>**RPC \_ S \_ non \_ PROTSEQS \_ inscrits**
</dt> <dd> <dl> <dt>

1714 (0x6B2)
</dt> <dt>



Aucune séquence de protocole n’a été inscrite.


</dt> </dl> </dd> <dt>

<span id="RPC_S_NOT_LISTENING"></span><span id="rpc_s_not_listening"></span>**RPC \_ S \_ n' \_ écoutant pas**
</dt> <dd> <dl> <dt>

1715 (0x6B3)
</dt> <dt>



Le serveur RPC n’est pas à l’écoute.


</dt> </dl> </dd> <dt>

<span id="RPC_S_UNKNOWN_MGR_TYPE"></span><span id="rpc_s_unknown_mgr_type"></span>**\_type de \_ \_ Gestionnaire inconnu \_ RPC**
</dt> <dd> <dl> <dt>

1716 (0x6B4)
</dt> <dt>



Le type de gestionnaire est inconnu.


</dt> </dl> </dd> <dt>

<span id="RPC_S_UNKNOWN_IF"></span><span id="rpc_s_unknown_if"></span>**RPC \_ S \_ inconnu \_ si**
</dt> <dd> <dl> <dt>

1717 (0x6B5)
</dt> <dt>



L’interface est inconnue.


</dt> </dl> </dd> <dt>

<span id="RPC_S_NO_BINDINGS"></span><span id="rpc_s_no_bindings"></span>**\_ \_ aucune \_ liaison RPC**
</dt> <dd> <dl> <dt>

1718 (0x6B6)
</dt> <dt>



Il n’y a aucune liaison.


</dt> </dl> </dd> <dt>

<span id="RPC_S_NO_PROTSEQS"></span><span id="rpc_s_no_protseqs"></span>**RPC \_ S \_ non \_ PROTSEQS**
</dt> <dd> <dl> <dt>

1719 (0x6B7)
</dt> <dt>



Il n’existe aucune séquence de protocole.


</dt> </dl> </dd> <dt>

<span id="RPC_S_CANT_CREATE_ENDPOINT"></span><span id="rpc_s_cant_create_endpoint"></span>**RPC \_ \_ Impossible de \_ créer un \_ point de terminaison**
</dt> <dd> <dl> <dt>

1720 (0x6B8)
</dt> <dt>



Impossible de créer le point de terminaison.


</dt> </dl> </dd> <dt>

<span id="RPC_S_OUT_OF_RESOURCES"></span><span id="rpc_s_out_of_resources"></span>**\_ressources RPC \_ insuffisantes \_ \_**
</dt> <dd> <dl> <dt>

1721 (0x6B9)
</dt> <dt>



Les ressources disponibles sont insuffisantes pour terminer cette opération.


</dt> </dl> </dd> <dt>

<span id="RPC_S_SERVER_UNAVAILABLE"></span><span id="rpc_s_server_unavailable"></span>**\_serveur RPC \_ S \_ non disponible**
</dt> <dd> <dl> <dt>

1722 (0x6BA)
</dt> <dt>



Le serveur RPC est indisponible.


</dt> </dl> </dd> <dt>

<span id="RPC_S_SERVER_TOO_BUSY"></span><span id="rpc_s_server_too_busy"></span>**\_serveur RPC \_ S \_ encombré \_**
</dt> <dd> <dl> <dt>

1723 (0x6BB)
</dt> <dt>



Le serveur RPC est trop occupé pour terminer cette opération.


</dt> </dl> </dd> <dt>

<span id="RPC_S_INVALID_NETWORK_OPTIONS"></span><span id="rpc_s_invalid_network_options"></span>**\_ \_ options réseau non VALIDEs RPC \_ \_**
</dt> <dd> <dl> <dt>

1724 (0x6BC)
</dt> <dt>



Les options réseau ne sont pas valides.


</dt> </dl> </dd> <dt>

<span id="RPC_S_NO_CALL_ACTIVE"></span><span id="rpc_s_no_call_active"></span>**RPC \_ S \_ aucun \_ appel \_ actif**
</dt> <dd> <dl> <dt>

1725 (0x6BD)
</dt> <dt>



Aucun appel de procédure distante n’est actif sur ce thread.


</dt> </dl> </dd> <dt>

<span id="RPC_S_CALL_FAILED"></span><span id="rpc_s_call_failed"></span>**échec de l' \_ appel RPC S \_ \_**
</dt> <dd> <dl> <dt>

1726 (0x6BE)
</dt> <dt>



L’appel de procédure distante a échoué.


</dt> </dl> </dd> <dt>

<span id="RPC_S_CALL_FAILED_DNE"></span><span id="rpc_s_call_failed_dne"></span>**échec de l’appel des RPC \_ S \_ \_ \_ dne**
</dt> <dd> <dl> <dt>

1727 (0x6BF)
</dt> <dt>



L’appel de procédure distante a échoué et ne s’est pas exécuté.


</dt> </dl> </dd> <dt>

<span id="RPC_S_PROTOCOL_ERROR"></span><span id="rpc_s_protocol_error"></span>**\_erreur de \_ protocole \_ S RPC**
</dt> <dd> <dl> <dt>

1728 (0x6C0)
</dt> <dt>



Une erreur de protocole d’appel de procédure distante (RPC) s’est produite.


</dt> </dl> </dd> <dt>

<span id="RPC_S_PROXY_ACCESS_DENIED"></span><span id="rpc_s_proxy_access_denied"></span>**\_ \_ accès proxy RPC \_ \_ refusé**
</dt> <dd> <dl> <dt>

1729 (0x6C1)
</dt> <dt>



L’accès au proxy HTTP est refusé.


</dt> </dl> </dd> <dt>

<span id="RPC_S_UNSUPPORTED_TRANS_SYN"></span><span id="rpc_s_unsupported_trans_syn"></span>**RPC \_ \_ non pris en charge par \_ TRANS \_ syn**
</dt> <dd> <dl> <dt>

1730 (0x6C2)
</dt> <dt>



La syntaxe de transfert n’est pas prise en charge par le serveur RPC.


</dt> </dl> </dd> <dt>

<span id="RPC_S_UNSUPPORTED_TYPE"></span><span id="rpc_s_unsupported_type"></span>**\_ \_ type non pris en charge par RPC \_**
</dt> <dd> <dl> <dt>

1732 (0x6C4)
</dt> <dt>



Le type d’identificateur unique universel (UUID) n’est pas pris en charge.


</dt> </dl> </dd> <dt>

<span id="RPC_S_INVALID_TAG"></span><span id="rpc_s_invalid_tag"></span>**\_ \_ balise RPC S non valide \_**
</dt> <dd> <dl> <dt>

1733 (0x6C5)
</dt> <dt>



La balise n’est pas valide.


</dt> </dl> </dd> <dt>

<span id="RPC_S_INVALID_BOUND"></span><span id="rpc_s_invalid_bound"></span>**\_liaison RPC \_ non valide \_**
</dt> <dd> <dl> <dt>

1734 (0x6C6)
</dt> <dt>



Les limites du tableau ne sont pas valides.


</dt> </dl> </dd> <dt>

<span id="RPC_S_NO_ENTRY_NAME"></span><span id="rpc_s_no_entry_name"></span>**RPC \_ \_ sans \_ nom d’entrée \_**
</dt> <dd> <dl> <dt>

1735 (0x6C7)
</dt> <dt>



La liaison ne contient pas de nom d’entrée.


</dt> </dl> </dd> <dt>

<span id="RPC_S_INVALID_NAME_SYNTAX"></span><span id="rpc_s_invalid_name_syntax"></span>**RPC \_ S \_ \_ syntaxe de nom non valide \_**
</dt> <dd> <dl> <dt>

1736 (0x6C8)
</dt> <dt>



La syntaxe du nom n’est pas valide.


</dt> </dl> </dd> <dt>

<span id="RPC_S_UNSUPPORTED_NAME_SYNTAX"></span><span id="rpc_s_unsupported_name_syntax"></span>**RPC \_ S \_ syntaxe de nom non prise en charge \_ \_**
</dt> <dd> <dl> <dt>

1737 (0x6C9)
</dt> <dt>



La syntaxe du nom n’est pas prise en charge.


</dt> </dl> </dd> <dt>

<span id="RPC_S_UUID_NO_ADDRESS"></span><span id="rpc_s_uuid_no_address"></span>**\_UUID RPC \_ S \_ aucune \_ adresse**
</dt> <dd> <dl> <dt>

1739 (0x6CB)
</dt> <dt>



Aucune adresse réseau ne peut être utilisée pour construire un identificateur unique universel (UUID).


</dt> </dl> </dd> <dt>

<span id="RPC_S_DUPLICATE_ENDPOINT"></span><span id="rpc_s_duplicate_endpoint"></span>**\_point de terminaison RPC S \_ dupliqué \_**
</dt> <dd> <dl> <dt>

1740 (0x6CC)
</dt> <dt>



Le point de terminaison est un doublon.


</dt> </dl> </dd> <dt>

<span id="RPC_S_UNKNOWN_AUTHN_TYPE"></span><span id="rpc_s_unknown_authn_type"></span>**\_ \_ \_ type AUTHn inconnu RPC \_**
</dt> <dd> <dl> <dt>

1741 (0x6CD)
</dt> <dt>



Le type d’authentification est inconnu.


</dt> </dl> </dd> <dt>

<span id="RPC_S_MAX_CALLS_TOO_SMALL"></span><span id="rpc_s_max_calls_too_small"></span>**\_ \_ nombre maximal d’appels RPC S \_ \_ trop \_ petit**
</dt> <dd> <dl> <dt>

1742 (0x6CE)
</dt> <dt>



Le nombre maximal d’appels est trop petit.


</dt> </dl> </dd> <dt>

<span id="RPC_S_STRING_TOO_LONG"></span><span id="rpc_s_string_too_long"></span>**\_chaîne RPC \_ \_ trop \_ longue**
</dt> <dd> <dl> <dt>

1743 (0x6CF)
</dt> <dt>



La chaîne est trop longue.


</dt> </dl> </dd> <dt>

<span id="RPC_S_PROTSEQ_NOT_FOUND"></span><span id="rpc_s_protseq_not_found"></span>**RPC \_ S \_ PROTSEQ \_ \_ introuvable**
</dt> <dd> <dl> <dt>

1744 (0x6D0)
</dt> <dt>



La séquence de protocole RPC est introuvable.


</dt> </dl> </dd> <dt>

<span id="RPC_S_PROCNUM_OUT_OF_RANGE"></span><span id="rpc_s_procnum_out_of_range"></span>**RPC \_ S \_ PROCNUM \_ hors \_ \_ limites**
</dt> <dd> <dl> <dt>

1745 (0x6D1)
</dt> <dt>



Le numéro de la procédure est hors limites.


</dt> </dl> </dd> <dt>

<span id="RPC_S_BINDING_HAS_NO_AUTH"></span><span id="rpc_s_binding_has_no_auth"></span>**la \_ liaison RPC S n' \_ \_ a \_ pas d' \_ authentification**
</dt> <dd> <dl> <dt>

1746 (0x6D2)
</dt> <dt>



La liaison ne contient pas d’informations d’authentification.


</dt> </dl> </dd> <dt>

<span id="RPC_S_UNKNOWN_AUTHN_SERVICE"></span><span id="rpc_s_unknown_authn_service"></span>**RPC \_ S \_ \_ service d’authentification inconnu \_**
</dt> <dd> <dl> <dt>

1747 (0x6D3)
</dt> <dt>



Le service d’authentification est inconnu.


</dt> </dl> </dd> <dt>

<span id="RPC_S_UNKNOWN_AUTHN_LEVEL"></span><span id="rpc_s_unknown_authn_level"></span>**\_niveau d' \_ authentification inconnue RPC S \_ \_**
</dt> <dd> <dl> <dt>

1748 (0x6D4)
</dt> <dt>



Le niveau d’authentification est inconnu.


</dt> </dl> </dd> <dt>

<span id="RPC_S_INVALID_AUTH_IDENTITY"></span><span id="rpc_s_invalid_auth_identity"></span>**\_identité d’authentification RPC S \_ non valide \_ \_**
</dt> <dd> <dl> <dt>

1749 (0x6D5)
</dt> <dt>



Le contexte de sécurité n’est pas valide.


</dt> </dl> </dd> <dt>

<span id="RPC_S_UNKNOWN_AUTHZ_SERVICE"></span><span id="rpc_s_unknown_authz_service"></span>**RPC \_ S \_ service d’autorisation inconnu \_ \_**
</dt> <dd> <dl> <dt>

1750 (0x6D6)
</dt> <dt>



Le service d’autorisation est inconnu.


</dt> </dl> </dd> <dt>

<span id="EPT_S_INVALID_ENTRY"></span><span id="ept_s_invalid_entry"></span>**\_entrée EPT S \_ non valide \_**
</dt> <dd> <dl> <dt>

1751 (0x6D7)
</dt> <dt>



L’entrée n’est pas valide.


</dt> </dl> </dd> <dt>

<span id="EPT_S_CANT_PERFORM_OP"></span><span id="ept_s_cant_perform_op"></span>**EPT \_ S ne pas \_ effectuer d' \_ \_ opérations**
</dt> <dd> <dl> <dt>

1752 (0x6D8)
</dt> <dt>



Le point de terminaison de serveur ne peut pas effectuer l’opération.


</dt> </dl> </dd> <dt>

<span id="EPT_S_NOT_REGISTERED"></span><span id="ept_s_not_registered"></span>**EPT \_ S \_ non \_ inscrit**
</dt> <dd> <dl> <dt>

1753 (0x6D9)
</dt> <dt>



il n’y a plus de points de terminaison disponibles auprès du mappeur de point de terminaison.


</dt> </dl> </dd> <dt>

<span id="RPC_S_NOTHING_TO_EXPORT"></span><span id="rpc_s_nothing_to_export"></span>**RPC \_ S \_ rien \_ à \_ Exporter**
</dt> <dd> <dl> <dt>

1754 (0x6DA)
</dt> <dt>



Aucune interface n’a été exportée.


</dt> </dl> </dd> <dt>

<span id="RPC_S_INCOMPLETE_NAME"></span><span id="rpc_s_incomplete_name"></span>**\_ \_ nom incomplet RPC S \_**
</dt> <dd> <dl> <dt>

1755 (0x6DB)
</dt> <dt>



Le nom de l’entrée est incomplet.


</dt> </dl> </dd> <dt>

<span id="RPC_S_INVALID_VERS_OPTION"></span><span id="rpc_s_invalid_vers_option"></span>**\_option RPC S \_ non valide \_ \_**
</dt> <dd> <dl> <dt>

1756 (0x6DC)
</dt> <dt>



L’option version n’est pas valide.


</dt> </dl> </dd> <dt>

<span id="RPC_S_NO_MORE_MEMBERS"></span><span id="rpc_s_no_more_members"></span>**RPC \_ \_ ne pas \_ plus de \_ membres**
</dt> <dd> <dl> <dt>

1757 (0x6DD)
</dt> <dt>



Il n’y a plus de membres.


</dt> </dl> </dd> <dt>

<span id="RPC_S_NOT_ALL_OBJS_UNEXPORTED"></span><span id="rpc_s_not_all_objs_unexported"></span>**RPC \_ \_ non \_ tous les \_ ne comportaient non \_ exportés**
</dt> <dd> <dl> <dt>

1758 (0x6DE)
</dt> <dt>



Il n’y a rien à désexporter.


</dt> </dl> </dd> <dt>

<span id="RPC_S_INTERFACE_NOT_FOUND"></span><span id="rpc_s_interface_not_found"></span>**\_interface RPC \_ S \_ \_ introuvable**
</dt> <dd> <dl> <dt>

1759 (0x6DF)
</dt> <dt>



L’interface est introuvable.


</dt> </dl> </dd> <dt>

<span id="RPC_S_ENTRY_ALREADY_EXISTS"></span><span id="rpc_s_entry_already_exists"></span>**l' \_ entrée RPC S \_ \_ \_ existe déjà**
</dt> <dd> <dl> <dt>

1760 (0x6E0)
</dt> <dt>



L’entrée existe déjà.


</dt> </dl> </dd> <dt>

<span id="RPC_S_ENTRY_NOT_FOUND"></span><span id="rpc_s_entry_not_found"></span>**\_entrée RPC \_ S \_ \_ introuvable**
</dt> <dd> <dl> <dt>

1761 (0x6E1)
</dt> <dt>



L’entrée est introuvable.


</dt> </dl> </dd> <dt>

<span id="RPC_S_NAME_SERVICE_UNAVAILABLE"></span><span id="rpc_s_name_service_unavailable"></span>**\_service de \_ noms \_ RPC \_ non disponible**
</dt> <dd> <dl> <dt>

1762 (0x6E2)
</dt> <dt>



Le service de noms n’est pas disponible.


</dt> </dl> </dd> <dt>

<span id="RPC_S_INVALID_NAF_ID"></span><span id="rpc_s_invalid_naf_id"></span>**\_ \_ \_ ID NAF non valide \_ de RPC**
</dt> <dd> <dl> <dt>

1763 (0x6E3)
</dt> <dt>



La famille d’adresses réseau n’est pas valide.


</dt> </dl> </dd> <dt>

<span id="RPC_S_CANNOT_SUPPORT"></span><span id="rpc_s_cannot_support"></span>**RPC \_ \_ ne peut pas \_ prendre en charge**
</dt> <dd> <dl> <dt>

1764 (0x6E4)
</dt> <dt>



L'opération demandée n'est pas prise en charge.


</dt> </dl> </dd> <dt>

<span id="RPC_S_NO_CONTEXT_AVAILABLE"></span><span id="rpc_s_no_context_available"></span>**RPC \_ \_ sans \_ contexte \_ disponible**
</dt> <dd> <dl> <dt>

1765 (0x6E5)
</dt> <dt>



Aucun contexte de sécurité n’est disponible pour autoriser l’emprunt d’identité.


</dt> </dl> </dd> <dt>

<span id="RPC_S_INTERNAL_ERROR"></span><span id="rpc_s_internal_error"></span>**\_ \_ erreur interne RPC \_ S**
</dt> <dd> <dl> <dt>

1766 (0x6E6)
</dt> <dt>



Une erreur interne s’est produite dans un appel de procédure distante (RPC).


</dt> </dl> </dd> <dt>

<span id="RPC_S_ZERO_DIVIDE"></span><span id="rpc_s_zero_divide"></span>**\_ \_ Division zéro du \_ RPC**
</dt> <dd> <dl> <dt>

1767 (0x6E7)
</dt> <dt>



Le serveur RPC a tenté une division d’entier par zéro.


</dt> </dl> </dd> <dt>

<span id="RPC_S_ADDRESS_ERROR"></span><span id="rpc_s_address_error"></span>**\_erreur d' \_ adresse RPC S \_**
</dt> <dd> <dl> <dt>

1768 (0x6E8)
</dt> <dt>



Une erreur d’adressage s’est produite sur le serveur RPC.


</dt> </dl> </dd> <dt>

<span id="RPC_S_FP_DIV_ZERO"></span><span id="rpc_s_fp_div_zero"></span>**\_ \_ \_ valeur zéro div FP \_ de RPC**
</dt> <dd> <dl> <dt>

1769 (0x6E9)
</dt> <dt>



Une opération à virgule flottante au niveau du serveur RPC a provoqué une division par zéro.


</dt> </dl> </dd> <dt>

<span id="RPC_S_FP_UNDERFLOW"></span><span id="rpc_s_fp_underflow"></span>**dépassement de capacité négatif RPC \_ S \_ \_**
</dt> <dd> <dl> <dt>

1770 (0x6EA)
</dt> <dt>



Un dépassement de capacité négatif à virgule flottante s’est produit au niveau du serveur RPC.


</dt> </dl> </dd> <dt>

<span id="RPC_S_FP_OVERFLOW"></span><span id="rpc_s_fp_overflow"></span>**\_dépassement de \_ capacité du FP RPC S \_**
</dt> <dd> <dl> <dt>

1771 (0x6EB)
</dt> <dt>



Un dépassement de capacité à virgule flottante s’est produit au niveau du serveur RPC.


</dt> </dl> </dd> <dt>

<span id="RPC_X_NO_MORE_ENTRIES"></span><span id="rpc_x_no_more_entries"></span>**RPC \_ X \_ \_ plus d' \_ entrées**
</dt> <dd> <dl> <dt>

1772 (0x6EC)
</dt> <dt>



La liste des serveurs RPC disponibles pour la liaison des handles automatiques est épuisée.


</dt> </dl> </dd> <dt>

<span id="RPC_X_SS_CHAR_TRANS_OPEN_FAIL"></span><span id="rpc_x_ss_char_trans_open_fail"></span>**\_échec d' \_ \_ ouverture de \_ TRANS \_ . RPC X SS \_**
</dt> <dd> <dl> <dt>

1773 (0x6ED)
</dt> <dt>



Impossible d’ouvrir le fichier de table de traduction des caractères.


</dt> </dl> </dd> <dt>

<span id="RPC_X_SS_CHAR_TRANS_SHORT_FILE"></span><span id="rpc_x_ss_char_trans_short_file"></span>**\_fichier de \_ \_ type \_ short de \_ transaction \_ RPC X SS**
</dt> <dd> <dl> <dt>

1774 (0x6EE)
</dt> <dt>



Le fichier contenant la table de traduction de caractères a moins de 512 octets.


</dt> </dl> </dd> <dt>

<span id="RPC_X_SS_IN_NULL_CONTEXT"></span><span id="rpc_x_ss_in_null_context"></span>**RPC \_ X \_ SS \_ dans \_ le \_ contexte null**
</dt> <dd> <dl> <dt>

1775 (0x6EF)
</dt> <dt>



Un handle de contexte null a été passé du client à l’hôte pendant un appel de procédure distante.


</dt> </dl> </dd> <dt>

<span id="RPC_X_SS_CONTEXT_DAMAGED"></span><span id="rpc_x_ss_context_damaged"></span>**\_ \_ contexte SS RPC \_ X \_ endommagé**
</dt> <dd> <dl> <dt>

1777 (0x6F1)
</dt> <dt>



Le handle de contexte a changé pendant un appel de procédure distante.


</dt> </dl> </dd> <dt>

<span id="RPC_X_SS_HANDLES_MISMATCH"></span><span id="rpc_x_ss_handles_mismatch"></span>**non \_ - \_ \_ concordance des handles RPC X SS \_**
</dt> <dd> <dl> <dt>

1778 (0x6F2)
</dt> <dt>



Les handles de liaison passés à un appel de procédure distante ne correspondent pas.


</dt> </dl> </dd> <dt>

<span id="RPC_X_SS_CANNOT_GET_CALL_HANDLE"></span><span id="rpc_x_ss_cannot_get_call_handle"></span>**RPC \_ X \_ SS \_ ne peut pas \_ recevoir le \_ handle d’appel \_**
</dt> <dd> <dl> <dt>

1779 (0x6F3)
</dt> <dt>



Le stub ne peut pas recevoir le descripteur d’appel de procédure distante.


</dt> </dl> </dd> <dt>

<span id="RPC_X_NULL_REF_POINTER"></span><span id="rpc_x_null_ref_pointer"></span>**\_ \_ \_ pointeur Ref null RPC \_ X**
</dt> <dd> <dl> <dt>

1780 (0x6F4)
</dt> <dt>



Un pointeur de référence null a été passé au stub.


</dt> </dl> </dd> <dt>

<span id="RPC_X_ENUM_VALUE_OUT_OF_RANGE"></span><span id="rpc_x_enum_value_out_of_range"></span>**\_ \_ valeur enum RPC \_ X \_ hors \_ \_ limites**
</dt> <dd> <dl> <dt>

1781 (0x6F5)
</dt> <dt>



La valeur d'énumération est hors limites.


</dt> </dl> </dd> <dt>

<span id="RPC_X_BYTE_COUNT_TOO_SMALL"></span><span id="rpc_x_byte_count_too_small"></span>**le \_ nombre d’octets RPC X est \_ \_ \_ trop \_ petit**
</dt> <dd> <dl> <dt>

1782 (0x6F6)
</dt> <dt>



Le nombre d’octets est trop petit.


</dt> </dl> </dd> <dt>

<span id="RPC_X_BAD_STUB_DATA"></span><span id="rpc_x_bad_stub_data"></span>**RPC \_ X \_ \_ données de stub incorrectes \_**
</dt> <dd> <dl> <dt>

1783 (0x6F7)
</dt> <dt>



Le stub a reçu des données incorrectes.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_USER_BUFFER"></span><span id="error_invalid_user_buffer"></span>**ERREUR \_ de \_ mémoire tampon utilisateur non valide \_**
</dt> <dd> <dl> <dt>

1784 (0x6F8)
</dt> <dt>



La mémoire tampon de l’utilisateur fournie n’est pas valide pour l’opération demandée.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNRECOGNIZED_MEDIA"></span><span id="error_unrecognized_media"></span>**ERREUR de \_ média non reconnu \_**
</dt> <dd> <dl> <dt>

1785 (0x6F9)
</dt> <dt>



Le support de disque n’est pas reconnu. Elle n’est peut-être pas mise en forme.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_TRUST_LSA_SECRET"></span><span id="error_no_trust_lsa_secret"></span>**ERREUR de \_ non- \_ \_ \_ secret LSA secret**
</dt> <dd> <dl> <dt>

1786 (0x6FA)
</dt> <dt>



La station de travail n’a pas de secret de confiance.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_TRUST_SAM_ACCOUNT"></span><span id="error_no_trust_sam_account"></span>**ERREUR \_ aucun \_ \_ compte Sam d’approbation \_**
</dt> <dd> <dl> <dt>

1787 (0x6FB)
</dt> <dt>



La base de données de sécurité sur le serveur ne dispose pas d’un compte d’ordinateur pour cette relation d’approbation de station de travail.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRUSTED_DOMAIN_FAILURE"></span><span id="error_trusted_domain_failure"></span>**erreur \_ de \_ domaine approuvé d’erreur \_**
</dt> <dd> <dl> <dt>

1788 (0x6FC)
</dt> <dt>



La relation d’approbation entre le domaine principal et le domaine approuvé a échoué.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRUSTED_RELATIONSHIP_FAILURE"></span><span id="error_trusted_relationship_failure"></span>**échec de la \_ relation approuvée d’erreur \_ \_**
</dt> <dd> <dl> <dt>

1789 (0x6FD)
</dt> <dt>



La relation d'approbation entre cette station de travail et le domaine principal a échoué.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRUST_FAILURE"></span><span id="error_trust_failure"></span>**échec de l’approbation d’erreur \_ \_**
</dt> <dd> <dl> <dt>

1790 (0x6FE)
</dt> <dt>



Échec de l’ouverture de session réseau.


</dt> </dl> </dd> <dt>

<span id="RPC_S_CALL_IN_PROGRESS"></span><span id="rpc_s_call_in_progress"></span>**\_appel RPC \_ S \_ en \_ cours**
</dt> <dd> <dl> <dt>

1791 (0x6FF)
</dt> <dt>



Un appel de procédure distante est déjà en cours pour ce thread.


</dt> </dl> </dd> <dt>

<span id="ERROR_NETLOGON_NOT_STARTED"></span><span id="error_netlogon_not_started"></span>**ERREUR \_ Netlogon \_ non \_ démarrée**
</dt> <dd> <dl> <dt>

1792 (0X700)
</dt> <dt>



Une tentative de connexion a été effectuée, mais le service d’ouverture de session réseau n’a pas été démarré.


</dt> </dl> </dd> <dt>

<span id="ERROR_ACCOUNT_EXPIRED"></span><span id="error_account_expired"></span>**compte d’erreur \_ \_ expiré**
</dt> <dd> <dl> <dt>

1793 (0x701)
</dt> <dt>



Le compte de l’utilisateur a expiré.


</dt> </dl> </dd> <dt>

<span id="ERROR_REDIRECTOR_HAS_OPEN_HANDLES"></span><span id="error_redirector_has_open_handles"></span>**le \_ REdirecteur d’erreurs \_ a des \_ \_ Handles ouverts**
</dt> <dd> <dl> <dt>

1794 (0x702)
</dt> <dt>



Le redirecteur est en cours d’utilisation et ne peut pas être déchargé.


</dt> </dl> </dd> <dt>

<span id="ERROR_PRINTER_DRIVER_ALREADY_INSTALLED"></span><span id="error_printer_driver_already_installed"></span>**ERREUR le \_ pilote d’imprimante est \_ \_ déjà \_ installé**
</dt> <dd> <dl> <dt>

1795 (0x703)
</dt> <dt>



Le pilote d’imprimante spécifié est déjà installé.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNKNOWN_PORT"></span><span id="error_unknown_port"></span>**ERREUR \_ \_ port inconnu**
</dt> <dd> <dl> <dt>

1796 (0x704)
</dt> <dt>



Le port spécifié est inconnu.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNKNOWN_PRINTER_DRIVER"></span><span id="error_unknown_printer_driver"></span>**ERREUR \_ de \_ pilote d’imprimante inconnu \_**
</dt> <dd> <dl> <dt>

1797 (0x705)
</dt> <dt>



Le pilote d’imprimante est inconnu.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNKNOWN_PRINTPROCESSOR"></span><span id="error_unknown_printprocessor"></span>**ERREUR \_ inconnue \_ PRINTPROCESSOR**
</dt> <dd> <dl> <dt>

1798 (0x706)
</dt> <dt>



Le processeur d’impression est inconnu.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_SEPARATOR_FILE"></span><span id="error_invalid_separator_file"></span>**ERREUR \_ \_ fichier séparateur non valide \_**
</dt> <dd> <dl> <dt>

1799 (0x707)
</dt> <dt>



Le fichier séparateur spécifié n’est pas valide.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_PRIORITY"></span><span id="error_invalid_priority"></span>**priorité d’erreur \_ non valide \_**
</dt> <dd> <dl> <dt>

1800 (0x708)
</dt> <dt>



La priorité spécifiée n’est pas valide.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_PRINTER_NAME"></span><span id="error_invalid_printer_name"></span>**ERREUR \_ de \_ nom d’imprimante non valide \_**
</dt> <dd> <dl> <dt>

1801 (0x709)
</dt> <dt>



Le nom de l’imprimante n’est pas valide.


</dt> </dl> </dd> <dt>

<span id="ERROR_PRINTER_ALREADY_EXISTS"></span><span id="error_printer_already_exists"></span>**une erreur d' \_ imprimante \_ \_ existe déjà**
</dt> <dd> <dl> <dt>

1802 (0x70A)
</dt> <dt>



L’imprimante existe déjà.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_PRINTER_COMMAND"></span><span id="error_invalid_printer_command"></span>**ERREUR \_ de \_ commande d’imprimante non valide \_**
</dt> <dd> <dl> <dt>

1803 (0x70B)
</dt> <dt>



La commande d’imprimante n’est pas valide.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_DATATYPE"></span><span id="error_invalid_datatype"></span>**ERREUR \_ de \_ type de données non valide**
</dt> <dd> <dl> <dt>

1804 (0x70C)
</dt> <dt>



Le type de données spécifié n’est pas valide.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_ENVIRONMENT"></span><span id="error_invalid_environment"></span>**ERREUR \_ d' \_ environnement non valide**
</dt> <dd> <dl> <dt>

1805 (0x70D)
</dt> <dt>



L’environnement spécifié n’est pas valide.


</dt> </dl> </dd> <dt>

<span id="RPC_S_NO_MORE_BINDINGS"></span><span id="rpc_s_no_more_bindings"></span>**RPC \_ \_ ne pas \_ plus de \_ liaisons**
</dt> <dd> <dl> <dt>

1806 (0x70E)
</dt> <dt>



Il n’y a plus de liaisons.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOLOGON_INTERDOMAIN_TRUST_ACCOUNT"></span><span id="error_nologon_interdomain_trust_account"></span>**ERREUR \_ NOlogo- \_ compte de \_ confiance interdomaine \_**
</dt> <dd> <dl> <dt>

1807 (0x70F)
</dt> <dt>



Le compte utilisé est un compte de confiance interdomaine. Utilisez votre compte d’utilisateur global ou votre compte d’utilisateur local pour accéder à ce serveur.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOLOGON_WORKSTATION_TRUST_ACCOUNT"></span><span id="error_nologon_workstation_trust_account"></span>**ERREUR \_ NOlogos \_ \_ compte de confiance de station de travail \_**
</dt> <dd> <dl> <dt>

1808 (0x710)
</dt> <dt>



Le compte utilisé est un compte d’ordinateur. Utilisez votre compte d’utilisateur global ou votre compte d’utilisateur local pour accéder à ce serveur.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOLOGON_SERVER_TRUST_ACCOUNT"></span><span id="error_nologon_server_trust_account"></span>**ERREUR \_ NOlogos \_ \_ compte de confiance du serveur \_**
</dt> <dd> <dl> <dt>

1809 (0x711)
</dt> <dt>



Le compte utilisé est un compte de confiance de serveur. Utilisez votre compte d’utilisateur global ou votre compte d’utilisateur local pour accéder à ce serveur.


</dt> </dl> </dd> <dt>

<span id="ERROR_DOMAIN_TRUST_INCONSISTENT"></span><span id="error_domain_trust_inconsistent"></span>**approbation de domaine d’erreur \_ \_ \_ incohérente**
</dt> <dd> <dl> <dt>

1810 (0x712)
</dt> <dt>



Le nom ou l’ID de sécurité (SID) du domaine spécifié est incohérent avec les informations d’approbation pour ce domaine.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVER_HAS_OPEN_HANDLES"></span><span id="error_server_has_open_handles"></span>**le \_ serveur d’erreurs \_ a des \_ \_ Handles ouverts**
</dt> <dd> <dl> <dt>

1811 (0x713)
</dt> <dt>



Le serveur est en cours d’utilisation et ne peut pas être déchargé.


</dt> </dl> </dd> <dt>

<span id="ERROR_RESOURCE_DATA_NOT_FOUND"></span><span id="error_resource_data_not_found"></span>**données de ressource d’erreur \_ \_ \_ \_ introuvables**
</dt> <dd> <dl> <dt>

1812 (0x714)
</dt> <dt>



Le fichier image spécifié ne contenait pas de section de ressource.


</dt> </dl> </dd> <dt>

<span id="ERROR_RESOURCE_TYPE_NOT_FOUND"></span><span id="error_resource_type_not_found"></span>**TYPE de ressource d’erreur \_ \_ \_ \_ introuvable**
</dt> <dd> <dl> <dt>

1813 (0x715)
</dt> <dt>



Le type de ressource spécifié est introuvable dans le fichier image.


</dt> </dl> </dd> <dt>

<span id="ERROR_RESOURCE_NAME_NOT_FOUND"></span><span id="error_resource_name_not_found"></span>**ERREUR \_ de \_ nom de ressource \_ \_ introuvable**
</dt> <dd> <dl> <dt>

1814 (0x716)
</dt> <dt>



Le nom de ressource spécifié est introuvable dans le fichier image.


</dt> </dl> </dd> <dt>

<span id="ERROR_RESOURCE_LANG_NOT_FOUND"></span><span id="error_resource_lang_not_found"></span>**ERREUR \_ de \_ ressource \_ lang \_ introuvable**
</dt> <dd> <dl> <dt>

1815 (0x717)
</dt> <dt>



L’ID de langue de ressource spécifié est introuvable dans le fichier image.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_ENOUGH_QUOTA"></span><span id="error_not_enough_quota"></span>**QUOTA d’erreur \_ \_ insuffisante \_**
</dt> <dd> <dl> <dt>

1816 (0x718)
</dt> <dt>



Quota insuffisant pour traiter cette commande.


</dt> </dl> </dd> <dt>

<span id="RPC_S_NO_INTERFACES"></span><span id="rpc_s_no_interfaces"></span>**\_interfaces RPC \_ sans \_ interface**
</dt> <dd> <dl> <dt>

1817 (0x719)
</dt> <dt>



Aucune interface n’a été inscrite.


</dt> </dl> </dd> <dt>

<span id="RPC_S_CALL_CANCELLED"></span><span id="rpc_s_call_cancelled"></span>**\_appel RPC \_ S \_ annulé**
</dt> <dd> <dl> <dt>

1818 (0x71A)
</dt> <dt>



L’appel de procédure distante a été annulé.


</dt> </dl> </dd> <dt>

<span id="RPC_S_BINDING_INCOMPLETE"></span><span id="rpc_s_binding_incomplete"></span>**\_liaison RPC \_ S \_ incomplète**
</dt> <dd> <dl> <dt>

1819 (0x71B)
</dt> <dt>



Le handle de liaison ne contient pas toutes les informations requises.


</dt> </dl> </dd> <dt>

<span id="RPC_S_COMM_FAILURE"></span><span id="rpc_s_comm_failure"></span>**\_échec de \_ communication RPC S \_**
</dt> <dd> <dl> <dt>

1820 (0x71C)
</dt> <dt>



Un échec de communication s’est produit lors d’un appel de procédure distante.


</dt> </dl> </dd> <dt>

<span id="RPC_S_UNSUPPORTED_AUTHN_LEVEL"></span><span id="rpc_s_unsupported_authn_level"></span>**RPC \_ S \_ niveau non pris en charge par \_ Authn \_**
</dt> <dd> <dl> <dt>

1821 (0x71D)
</dt> <dt>



Le niveau d’authentification demandé n’est pas pris en charge.


</dt> </dl> </dd> <dt>

<span id="RPC_S_NO_PRINC_NAME"></span><span id="rpc_s_no_princ_name"></span>**RPC \_ \_ n’a pas de \_ nom de princ \_**
</dt> <dd> <dl> <dt>

1822 (0x71E)
</dt> <dt>



Aucun nom principal n’est inscrit.


</dt> </dl> </dd> <dt>

<span id="RPC_S_NOT_RPC_ERROR"></span><span id="rpc_s_not_rpc_error"></span>**RPC \_ S \_ non \_ \_ erreur RPC**
</dt> <dd> <dl> <dt>

1823 (0x71F)
</dt> <dt>



l’erreur spécifiée n’est pas un code d’erreur Windows RPC valide.


</dt> </dl> </dd> <dt>

<span id="RPC_S_UUID_LOCAL_ONLY"></span><span id="rpc_s_uuid_local_only"></span>**\_UUID RPC \_ \_ uniquement local \_**
</dt> <dd> <dl> <dt>

1824 (0x720)
</dt> <dt>



Un UUID qui est valide uniquement sur cet ordinateur a été alloué.


</dt> </dl> </dd> <dt>

<span id="RPC_S_SEC_PKG_ERROR"></span><span id="rpc_s_sec_pkg_error"></span>**erreur du s de la \_ \_ seconde RPC \_ \_**
</dt> <dd> <dl> <dt>

1825 (0x721)
</dt> <dt>



Une erreur spécifique au package de sécurité s’est produite.


</dt> </dl> </dd> <dt>

<span id="RPC_S_NOT_CANCELLED"></span><span id="rpc_s_not_cancelled"></span>**RPC \_ S \_ non \_ annulés**
</dt> <dd> <dl> <dt>

1826 (0x722)
</dt> <dt>



Le thread n’est pas annulé.


</dt> </dl> </dd> <dt>

<span id="RPC_X_INVALID_ES_ACTION"></span><span id="rpc_x_invalid_es_action"></span>**\_ \_ action es non valides RPC X \_ \_**
</dt> <dd> <dl> <dt>

1827 (0x723)
</dt> <dt>



Opération non valide sur le handle d’encodage/décodage.


</dt> </dl> </dd> <dt>

<span id="RPC_X_WRONG_ES_VERSION"></span><span id="rpc_x_wrong_es_version"></span>**RPC \_ X \_ mauvaise \_ \_ version es**
</dt> <dd> <dl> <dt>

1828 (0x724)
</dt> <dt>



Version incompatible du package de sérialisation.


</dt> </dl> </dd> <dt>

<span id="RPC_X_WRONG_STUB_VERSION"></span><span id="rpc_x_wrong_stub_version"></span>**\_version de stub RPC X \_ incorrecte \_ \_**
</dt> <dd> <dl> <dt>

1829 (0x725)
</dt> <dt>



Version incompatible du stub RPC.


</dt> </dl> </dd> <dt>

<span id="RPC_X_INVALID_PIPE_OBJECT"></span><span id="rpc_x_invalid_pipe_object"></span>**\_ \_ objet canal non valide RPC X \_ \_**
</dt> <dd> <dl> <dt>

1830 (0x726)
</dt> <dt>



L’objet du canal RPC n’est pas valide ou est endommagé.


</dt> </dl> </dd> <dt>

<span id="RPC_X_WRONG_PIPE_ORDER"></span><span id="rpc_x_wrong_pipe_order"></span>**\_ \_ mauvais ordre des \_ canaux RPC X \_**
</dt> <dd> <dl> <dt>

1831 (0x727)
</dt> <dt>



Une opération non valide a été tentée sur un objet canal RPC.


</dt> </dl> </dd> <dt>

<span id="RPC_X_WRONG_PIPE_VERSION"></span><span id="rpc_x_wrong_pipe_version"></span>**\_version du canal RPC X \_ incorrect \_ \_**
</dt> <dd> <dl> <dt>

1832 (0x728)
</dt> <dt>



Version du canal RPC non prise en charge.


</dt> </dl> </dd> <dt>

<span id="RPC_S_COOKIE_AUTH_FAILED"></span><span id="rpc_s_cookie_auth_failed"></span>**échec de l’authentification des cookies RPC \_ S \_ \_ \_**
</dt> <dd> <dl> <dt>

1833 (0x729)
</dt> <dt>



Le serveur proxy HTTP a rejeté la connexion en raison de l’échec de l’authentification du cookie.


</dt> </dl> </dd> <dt>

<span id="RPC_S_GROUP_MEMBER_NOT_FOUND"></span><span id="rpc_s_group_member_not_found"></span>**\_membre du groupe RPC S \_ \_ \_ \_ introuvable**
</dt> <dd> <dl> <dt>

1898 (0x76A)
</dt> <dt>



Le membre du groupe est introuvable.


</dt> </dl> </dd> <dt>

<span id="EPT_S_CANT_CREATE"></span><span id="ept_s_cant_create"></span>**EPT \_ S \_ impossible à \_ créer**
</dt> <dd> <dl> <dt>

1899 (0x76B)
</dt> <dt>



Impossible de créer l’entrée de la base de données du mappeur du point de terminaison.


</dt> </dl> </dd> <dt>

<span id="RPC_S_INVALID_OBJECT"></span><span id="rpc_s_invalid_object"></span>**\_objet RPC S \_ non valide \_**
</dt> <dd> <dl> <dt>

1900 (0x76C)
</dt> <dt>



L’identificateur unique universel (UUID) de l’objet est l’UUID Nil.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_TIME"></span><span id="error_invalid_time"></span>**\_heure non valide de l’erreur \_**
</dt> <dd> <dl> <dt>

1901 (0x76D)
</dt> <dt>



L’heure spécifiée n’est pas valide.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_FORM_NAME"></span><span id="error_invalid_form_name"></span>**ERREUR \_ de \_ nom de formulaire non valide \_**
</dt> <dd> <dl> <dt>

1902 (0x76E)
</dt> <dt>



Le nom de formulaire spécifié n’est pas valide.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_FORM_SIZE"></span><span id="error_invalid_form_size"></span>**ERREUR \_ de \_ taille de formulaire non valide \_**
</dt> <dd> <dl> <dt>

1903 (0x76F)
</dt> <dt>



La taille de formulaire spécifiée n’est pas valide.


</dt> </dl> </dd> <dt>

<span id="ERROR_ALREADY_WAITING"></span><span id="error_already_waiting"></span>**ERREUR \_ déjà en \_ attente**
</dt> <dd> <dl> <dt>

1904 (0x770)
</dt> <dt>



Le handle d’imprimante spécifié est déjà attendu.


</dt> </dl> </dd> <dt>

<span id="ERROR_PRINTER_DELETED"></span><span id="error_printer_deleted"></span>**ERREUR d' \_ imprimante \_ supprimée**
</dt> <dd> <dl> <dt>

1905 (0x771)
</dt> <dt>



L’imprimante spécifiée a été supprimée.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_PRINTER_STATE"></span><span id="error_invalid_printer_state"></span>**ERREUR de l’état de l' \_ imprimante non valide \_ \_**
</dt> <dd> <dl> <dt>

1906 (0x772)
</dt> <dt>



L’état de l’imprimante n’est pas valide.


</dt> </dl> </dd> <dt>

<span id="ERROR_PASSWORD_MUST_CHANGE"></span><span id="error_password_must_change"></span>**le \_ mot de passe d’erreur \_ doit \_ changer**
</dt> <dd> <dl> <dt>

1907 (0x773)
</dt> <dt>



Le mot de passe de l’utilisateur doit être modifié avant la connexion.


</dt> </dl> </dd> <dt>

<span id="ERROR_DOMAIN_CONTROLLER_NOT_FOUND"></span><span id="error_domain_controller_not_found"></span>**contrôleur de domaine d’erreur \_ \_ \_ \_ introuvable**
</dt> <dd> <dl> <dt>

1908 (0x774)
</dt> <dt>



Impossible de trouver le contrôleur de domaine pour ce domaine.


</dt> </dl> </dd> <dt>

<span id="ERROR_ACCOUNT_LOCKED_OUT"></span><span id="error_account_locked_out"></span>**compte d’erreur \_ \_ verrouillé \_**
</dt> <dd> <dl> <dt>

1909 (0x775)
</dt> <dt>



Le compte référencé est actuellement verrouillé et n’est peut-être pas connecté à.


</dt> </dl> </dd> <dt>

<span id="OR_INVALID_OXID"></span><span id="or_invalid_oxid"></span>**OU \_ Oxid non valide \_**
</dt> <dd> <dl> <dt>

1910 (0x776)
</dt> <dt>



L’exportateur d’objets spécifié est introuvable.


</dt> </dl> </dd> <dt>

<span id="OR_INVALID_OID"></span><span id="or_invalid_oid"></span>**OU \_ OID non valide \_**
</dt> <dd> <dl> <dt>

1911 (0x777)
</dt> <dt>



L’objet spécifié est introuvable.


</dt> </dl> </dd> <dt>

<span id="OR_INVALID_SET"></span><span id="or_invalid_set"></span>**OU \_ jeu non valide \_**
</dt> <dd> <dl> <dt>

1912 (0x778)
</dt> <dt>



Le programme de résolution d’objets spécifié n’a pas été trouvé.


</dt> </dl> </dd> <dt>

<span id="RPC_S_SEND_INCOMPLETE"></span><span id="rpc_s_send_incomplete"></span>**RPC \_ S \_ envoyés \_ incomplets**
</dt> <dd> <dl> <dt>

1913 (0x779)
</dt> <dt>



Certaines données restent à envoyer dans la mémoire tampon de la demande.


</dt> </dl> </dd> <dt>

<span id="RPC_S_INVALID_ASYNC_HANDLE"></span><span id="rpc_s_invalid_async_handle"></span>**RPC \_ S \_ \_ handle asynchrone non valide \_**
</dt> <dd> <dl> <dt>

1914 (0x77A)
</dt> <dt>



Handle d’appel de procédure distante asynchrone non valide.


</dt> </dl> </dd> <dt>

<span id="RPC_S_INVALID_ASYNC_CALL"></span><span id="rpc_s_invalid_async_call"></span>**RPC \_ S \_ \_ appel asynchrone non valide \_**
</dt> <dd> <dl> <dt>

1915 (0x77B)
</dt> <dt>



Handle d’appel RPC asynchrone non valide pour cette opération.


</dt> </dl> </dd> <dt>

<span id="RPC_X_PIPE_CLOSED"></span><span id="rpc_x_pipe_closed"></span>**\_canal RPC \_ X \_ fermé**
</dt> <dd> <dl> <dt>

1916 (0x77C)
</dt> <dt>



L’objet canal RPC a déjà été fermé.


</dt> </dl> </dd> <dt>

<span id="RPC_X_PIPE_DISCIPLINE_ERROR"></span><span id="rpc_x_pipe_discipline_error"></span>**\_erreur de \_ discipline de canal RPC X \_ \_**
</dt> <dd> <dl> <dt>

1917 (0x77D)
</dt> <dt>



L’appel RPC est terminé avant le traitement de tous les canaux.


</dt> </dl> </dd> <dt>

<span id="RPC_X_PIPE_EMPTY"></span><span id="rpc_x_pipe_empty"></span>**\_canal RPC \_ X \_ vide**
</dt> <dd> <dl> <dt>

1918 (0x77E)
</dt> <dt>



Aucune donnée n’est disponible à partir du canal RPC.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_SITENAME"></span><span id="error_no_sitename"></span>**ERREUR \_ non \_ SiteName**
</dt> <dd> <dl> <dt>

1919 (0x77F)
</dt> <dt>



Aucun nom de site n’est disponible pour cet ordinateur.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANT_ACCESS_FILE"></span><span id="error_cant_access_file"></span>**ERREUR \_ Impossible d' \_ accéder au \_ fichier**
</dt> <dd> <dl> <dt>

1920 (0x780)
</dt> <dt>



Le système ne peut pas accéder au fichier.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANT_RESOLVE_FILENAME"></span><span id="error_cant_resolve_filename"></span>**ERREUR \_ Impossible de \_ résoudre le nom de \_ fichier**
</dt> <dd> <dl> <dt>

1921 (0x781)
</dt> <dt>



Le nom du fichier ne peut pas être résolu par le système.


</dt> </dl> </dd> <dt>

<span id="RPC_S_ENTRY_TYPE_MISMATCH"></span><span id="rpc_s_entry_type_mismatch"></span>**incompatibilité de type d’entrée RPC \_ S \_ \_ \_**
</dt> <dd> <dl> <dt>

1922 (0x782)
</dt> <dt>



L’entrée n’est pas du type attendu.


</dt> </dl> </dd> <dt>

<span id="RPC_S_NOT_ALL_OBJS_EXPORTED"></span><span id="rpc_s_not_all_objs_exported"></span>**RPC \_ S \_ \_ tous les \_ ne comportaient \_ exportés**
</dt> <dd> <dl> <dt>

1923 (0x783)
</dt> <dt>



Tous les UUID d’objet n’ont pas pu être exportés vers l’entrée spécifiée.


</dt> </dl> </dd> <dt>

<span id="RPC_S_INTERFACE_NOT_EXPORTED"></span><span id="rpc_s_interface_not_exported"></span>**\_interface RPC \_ S \_ non \_ exportée**
</dt> <dd> <dl> <dt>

1924 (0x784)
</dt> <dt>



L’interface n’a pas pu être exportée vers l’entrée spécifiée.


</dt> </dl> </dd> <dt>

<span id="RPC_S_PROFILE_NOT_ADDED"></span><span id="rpc_s_profile_not_added"></span>**\_Profil RPC \_ S \_ non \_ ajouté**
</dt> <dd> <dl> <dt>

1925 (0x785)
</dt> <dt>



Impossible d’ajouter l’entrée de profil spécifiée.


</dt> </dl> </dd> <dt>

<span id="RPC_S_PRF_ELT_NOT_ADDED"></span><span id="rpc_s_prf_elt_not_added"></span>**le \_ PRF du PRF RPC S \_ \_ n’a \_ pas \_ été ajouté**
</dt> <dd> <dl> <dt>

1926 (0x786)
</dt> <dt>



Impossible d’ajouter l’élément de profil spécifié.


</dt> </dl> </dd> <dt>

<span id="RPC_S_PRF_ELT_NOT_REMOVED"></span><span id="rpc_s_prf_elt_not_removed"></span>**le PRF de la RPC \_ S \_ \_ ELT \_ n’a pas \_ été supprimé**
</dt> <dd> <dl> <dt>

1927 (0x787)
</dt> <dt>



Impossible de supprimer l’élément de profil spécifié.


</dt> </dl> </dd> <dt>

<span id="RPC_S_GRP_ELT_NOT_ADDED"></span><span id="rpc_s_grp_elt_not_added"></span>**la GRP de l’appel de procédure de \_ \_ GRP est \_ \_ non \_ ajoutée**
</dt> <dd> <dl> <dt>

1928 (0x788)
</dt> <dt>



Impossible d’ajouter l’élément de groupe.


</dt> </dl> </dd> <dt>

<span id="RPC_S_GRP_ELT_NOT_REMOVED"></span><span id="rpc_s_grp_elt_not_removed"></span>**la GRP des appels RPC \_ \_ \_ ELT \_ n’a pas \_ été supprimée**
</dt> <dd> <dl> <dt>

1929 (0x789)
</dt> <dt>



Impossible de supprimer l’élément de groupe.


</dt> </dl> </dd> <dt>

<span id="ERROR_KM_DRIVER_BLOCKED"></span><span id="error_km_driver_blocked"></span>**ERREUR \_ de \_ pilote km \_ bloqué**
</dt> <dd> <dl> <dt>

1930 (0x78A)
</dt> <dt>



Le pilote d’imprimante n’est pas compatible avec une stratégie activée sur votre ordinateur qui bloque les pilotes NT 4,0.


</dt> </dl> </dd> <dt>

<span id="ERROR_CONTEXT_EXPIRED"></span><span id="error_context_expired"></span>**contexte d’erreur \_ \_ expiré**
</dt> <dd> <dl> <dt>

1931 (0x78B)
</dt> <dt>



Le contexte a expiré et ne peut plus être utilisé.


</dt> </dl> </dd> <dt>

<span id="ERROR_PER_USER_TRUST_QUOTA_EXCEEDED"></span><span id="error_per_user_trust_quota_exceeded"></span>**ERREUR \_ par \_ quota de confiance de l’utilisateur \_ \_ \_ dépassé**
</dt> <dd> <dl> <dt>

1932 (0x78C)
</dt> <dt>



Le quota de création d’approbation déléguée de l’utilisateur actuel a été dépassé.


</dt> </dl> </dd> <dt>

<span id="ERROR_ALL_USER_TRUST_QUOTA_EXCEEDED"></span><span id="error_all_user_trust_quota_exceeded"></span>**ERREUR l’intégralité du quota de confiance de l' \_ utilisateur est \_ \_ \_ \_ dépassée**
</dt> <dd> <dl> <dt>

1933 (0x78D)
</dt> <dt>



Le quota de création d’approbation déléguée totale a été dépassé.


</dt> </dl> </dd> <dt>

<span id="ERROR_USER_DELETE_TRUST_QUOTA_EXCEEDED"></span><span id="error_user_delete_trust_quota_exceeded"></span>**ERREUR la suppression du quota de confiance par l' \_ utilisateur est \_ \_ \_ \_ dépassée**
</dt> <dd> <dl> <dt>

1934 (0x78E)
</dt> <dt>



Le quota de suppression d’approbation déléguée de l’utilisateur actuel a été dépassé.


</dt> </dl> </dd> <dt>

<span id="ERROR_AUTHENTICATION_FIREWALL_FAILED"></span><span id="error_authentication_firewall_failed"></span>**ERREUR \_ de \_ pare-feu d’authentification \_**
</dt> <dd> <dl> <dt>

1935 (0x78F)
</dt> <dt>



L’ordinateur avec lequel vous vous connectez est protégé par un pare-feu d’authentification. Le compte spécifié n’est pas autorisé à s’authentifier sur l’ordinateur.


</dt> </dl> </dd> <dt>

<span id="ERROR_REMOTE_PRINT_CONNECTIONS_BLOCKED"></span><span id="error_remote_print_connections_blocked"></span>**ERREUR \_ de \_ connexions d’impression à distance \_ \_ bloquées**
</dt> <dd> <dl> <dt>

1936 (0x790)
</dt> <dt>



Les connexions à distance au spouleur d’impression sont bloquées par une stratégie définie sur votre machine.


</dt> </dl> </dd> <dt>

<span id="ERROR_NTLM_BLOCKED"></span><span id="error_ntlm_blocked"></span>**ERREUR \_ NTLM \_ bloquée**
</dt> <dd> <dl> <dt>

1937 (0x791)
</dt> <dt>



L’authentification a échoué car l’authentification NTLM a été désactivée.


</dt> </dl> </dd> <dt>

<span id="ERROR_PASSWORD_CHANGE_REQUIRED"></span><span id="error_password_change_required"></span>**\_modification du mot de passe d’erreur \_ \_ obligatoire**
</dt> <dd> <dl> <dt>

1938 (0x792)
</dt> <dt>



Échec de l’ouverture de session : la stratégie EAS exige que l’utilisateur modifie son mot de passe avant que cette opération puisse être effectuée.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_PIXEL_FORMAT"></span><span id="error_invalid_pixel_format"></span>**ERREUR \_ \_ au format de pixel non valide \_**
</dt> <dd> <dl> <dt>

2000 (0x7D0)
</dt> <dt>



Le format de pixel n’est pas valide.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_DRIVER"></span><span id="error_bad_driver"></span>**ERREUR \_ de \_ pilote incorrect**
</dt> <dd> <dl> <dt>

2001 (0x7D1)
</dt> <dt>



Le pilote spécifié n’est pas valide.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_WINDOW_STYLE"></span><span id="error_invalid_window_style"></span>**ERREUR \_ de \_ style de fenêtre non valide \_**
</dt> <dd> <dl> <dt>

2002 (0x7D2)
</dt> <dt>



Le style de fenêtre ou l’attribut de classe n’est pas valide pour cette opération.


</dt> </dl> </dd> <dt>

<span id="ERROR_METAFILE_NOT_SUPPORTED"></span><span id="error_metafile_not_supported"></span>**métafichier d’erreur \_ \_ non \_ pris en charge**
</dt> <dd> <dl> <dt>

2003 (0x7D3)
</dt> <dt>



L’opération de métafichier demandée n’est pas prise en charge.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSFORM_NOT_SUPPORTED"></span><span id="error_transform_not_supported"></span>**transformation d’erreur \_ \_ non \_ prise en charge**
</dt> <dd> <dl> <dt>

2004 (0x7D4)
</dt> <dt>



L’opération de transformation demandée n’est pas prise en charge.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLIPPING_NOT_SUPPORTED"></span><span id="error_clipping_not_supported"></span>**découpage des erreurs \_ \_ non \_ pris en charge**
</dt> <dd> <dl> <dt>

2005 (0x7D5)
</dt> <dt>



L’opération de découpage demandée n’est pas prise en charge.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_CMM"></span><span id="error_invalid_cmm"></span>**ERREUR \_ CMM non valide \_**
</dt> <dd> <dl> <dt>

2010 (0x7DA)
</dt> <dt>



Le module de gestion des couleurs spécifié n’est pas valide.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_PROFILE"></span><span id="error_invalid_profile"></span>**ERREUR \_ de \_ Profil non valide**
</dt> <dd> <dl> <dt>

2011 (0x7DB)
</dt> <dt>



Le profil de couleurs spécifié n’est pas valide.


</dt> </dl> </dd> <dt>

<span id="ERROR_TAG_NOT_FOUND"></span><span id="error_tag_not_found"></span>**\_balise d’erreur \_ \_ introuvable**
</dt> <dd> <dl> <dt>

2012 (0x7DC)
</dt> <dt>



La balise spécifiée est introuvable.


</dt> </dl> </dd> <dt>

<span id="ERROR_TAG_NOT_PRESENT"></span><span id="error_tag_not_present"></span>**\_balise d’erreur \_ \_ absente**
</dt> <dd> <dl> <dt>

2013 (0x7DD)
</dt> <dt>



Une balise requise n’est pas présente.


</dt> </dl> </dd> <dt>

<span id="ERROR_DUPLICATE_TAG"></span><span id="error_duplicate_tag"></span>**\_balise d’erreur dupliquée \_**
</dt> <dd> <dl> <dt>

2014 (0x7DE)
</dt> <dt>



La balise spécifiée est déjà présente.


</dt> </dl> </dd> <dt>

<span id="ERROR_PROFILE_NOT_ASSOCIATED_WITH_DEVICE"></span><span id="error_profile_not_associated_with_device"></span>**\_profil \_ d’erreur non \_ associé à l' \_ \_ appareil**
</dt> <dd> <dl> <dt>

2015 (0x7DF)
</dt> <dt>



Le profil de couleurs spécifié n’est pas associé à l’appareil spécifié.


</dt> </dl> </dd> <dt>

<span id="ERROR_PROFILE_NOT_FOUND"></span><span id="error_profile_not_found"></span>**\_profil d' \_ erreur \_ introuvable**
</dt> <dd> <dl> <dt>

2016 (0x7E0)
</dt> <dt>



Le profil de couleurs spécifié est introuvable.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_COLORSPACE"></span><span id="error_invalid_colorspace"></span>**ERREUR \_ COLORSPACE non valide \_**
</dt> <dd> <dl> <dt>

2017 (0x7E1)
</dt> <dt>



L’espace de couleurs spécifié n’est pas valide.


</dt> </dl> </dd> <dt>

<span id="ERROR_ICM_NOT_ENABLED"></span><span id="error_icm_not_enabled"></span>**erreur \_ ICM \_ non \_ activée**
</dt> <dd> <dl> <dt>

2018 (0x7E2)
</dt> <dt>



La gestion des couleurs des images n’est pas activée.


</dt> </dl> </dd> <dt>

<span id="ERROR_DELETING_ICM_XFORM"></span><span id="error_deleting_icm_xform"></span>**erreur lors de \_ la suppression \_ ICM \_ XFORM**
</dt> <dd> <dl> <dt>

2019 (0x7E3)
</dt> <dt>



Une erreur s’est produite lors de la suppression de la transformation de couleur.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_TRANSFORM"></span><span id="error_invalid_transform"></span>**ERREUR \_ de \_ transformation non valide**
</dt> <dd> <dl> <dt>

2020 (0x7E4)
</dt> <dt>



La transformation de couleur spécifiée n’est pas valide.


</dt> </dl> </dd> <dt>

<span id="ERROR_COLORSPACE_MISMATCH"></span><span id="error_colorspace_mismatch"></span>**ERREUR \_ d' \_ incompatibilité COLORSPACE**
</dt> <dd> <dl> <dt>

2021 (0x7E5)
</dt> <dt>



La transformation spécifiée ne correspond pas à l’espace de couleurs de la bitmap.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_COLORINDEX"></span><span id="error_invalid_colorindex"></span>**ERREUR \_ ColorIndex non valide \_**
</dt> <dd> <dl> <dt>

2022 (0x7E6)
</dt> <dt>



L’index de couleur nommé spécifié n’est pas présent dans le profil.


</dt> </dl> </dd> <dt>

<span id="ERROR_PROFILE_DOES_NOT_MATCH_DEVICE"></span><span id="error_profile_does_not_match_device"></span>**le \_ profil d’erreur \_ ne \_ \_ correspond pas au \_ périphérique**
</dt> <dd> <dl> <dt>

2023 (0x7E7)
</dt> <dt>



Le profil spécifié est destiné à un périphérique d’un type différent de celui du périphérique spécifié.


</dt> </dl> </dd> <dt>

<span id="ERROR_CONNECTED_OTHER_PASSWORD"></span><span id="error_connected_other_password"></span>**ERREUR lors de la connexion d’un \_ \_ autre \_ mot de passe**
</dt> <dd> <dl> <dt>

2108 (0x83C)
</dt> <dt>



La connexion réseau a été établie avec succès, mais l’utilisateur devait être invité à entrer un mot de passe différent de celui spécifié à l’origine.


</dt> </dl> </dd> <dt>

<span id="ERROR_CONNECTED_OTHER_PASSWORD_DEFAULT"></span><span id="error_connected_other_password_default"></span>**ERREUR \_ liée à un \_ autre \_ mot de passe \_ par défaut**
</dt> <dd> <dl> <dt>

2109 (0x83D)
</dt> <dt>



La connexion réseau a été établie avec succès à l’aide des informations d’identification par défaut.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_USERNAME"></span><span id="error_bad_username"></span>**ERREUR \_ \_ nom d’utilisateur incorrect**
</dt> <dd> <dl> <dt>

2202 (0x89A)
</dt> <dt>



Le nom d’utilisateur spécifié n’est pas valide.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_CONNECTED"></span><span id="error_not_connected"></span>**ERREUR \_ non \_ connectée**
</dt> <dd> <dl> <dt>

2250 (0x8CA)
</dt> <dt>



Cette connexion réseau n’existe pas.


</dt> </dl> </dd> <dt>

<span id="ERROR_OPEN_FILES"></span><span id="error_open_files"></span>**ERREUR lors de l' \_ ouverture des \_ fichiers**
</dt> <dd> <dl> <dt>

2401 (0x961)
</dt> <dt>



Cette connexion réseau a des fichiers ouverts ou des demandes en attente.


</dt> </dl> </dd> <dt>

<span id="ERROR_ACTIVE_CONNECTIONS"></span><span id="error_active_connections"></span>**\_connexions actives d’erreur \_**
</dt> <dd> <dl> <dt>

2402 (0x962)
</dt> <dt>



Les connexions actives existent toujours.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEVICE_IN_USE"></span><span id="error_device_in_use"></span>**\_périphérique \_ d’erreur en cours d' \_ utilisation**
</dt> <dd> <dl> <dt>

2404 (0x964)
</dt> <dt>



L’appareil est en cours d’utilisation par un processus actif et ne peut pas être déconnecté.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNKNOWN_PRINT_MONITOR"></span><span id="error_unknown_print_monitor"></span>**ERREUR \_ de \_ moniteur d’impression inconnu \_**
</dt> <dd> <dl> <dt>

3000 (0xBB8)
</dt> <dt>



Le moniteur d’impression spécifié est inconnu.


</dt> </dl> </dd> <dt>

<span id="ERROR_PRINTER_DRIVER_IN_USE"></span><span id="error_printer_driver_in_use"></span>**ERREUR \_ \_ de pilote \_ d’imprimante en cours d' \_ utilisation**
</dt> <dd> <dl> <dt>

3001 (0xBB9)
</dt> <dt>



Le pilote d’imprimante spécifié est en cours d’utilisation.


</dt> </dl> </dd> <dt>

<span id="ERROR_SPOOL_FILE_NOT_FOUND"></span><span id="error_spool_file_not_found"></span>**fichier de mise en file d’attente d’erreurs \_ \_ \_ \_ introuvable**
</dt> <dd> <dl> <dt>

3002 (0xBBA)
</dt> <dt>



Le fichier de mise en file d’attente est introuvable.


</dt> </dl> </dd> <dt>

<span id="ERROR_SPL_NO_STARTDOC"></span><span id="error_spl_no_startdoc"></span>**ERREUR \_ SPL \_ non \_ STARTDOC**
</dt> <dd> <dl> <dt>

3003 (0xBBB)
</dt> <dt>



Un appel StartDocPrinter n’a pas été émis.


</dt> </dl> </dd> <dt>

<span id="ERROR_SPL_NO_ADDJOB"></span><span id="error_spl_no_addjob"></span>**ERREUR \_ SPL \_ non \_ ADDJOB**
</dt> <dd> <dl> <dt>

3004 (0xBBC)
</dt> <dt>



Un appel AddJob n’a pas été émis.


</dt> </dl> </dd> <dt>

<span id="ERROR_PRINT_PROCESSOR_ALREADY_INSTALLED"></span><span id="error_print_processor_already_installed"></span>**le processeur d’impression des erreurs est \_ \_ \_ déjà \_ installé**
</dt> <dd> <dl> <dt>

3005 (0xBBD)
</dt> <dt>



Le processeur d’impression spécifié a déjà été installé.


</dt> </dl> </dd> <dt>

<span id="ERROR_PRINT_MONITOR_ALREADY_INSTALLED"></span><span id="error_print_monitor_already_installed"></span>**ERREUR \_ de \_ moniteur d’impression \_ déjà \_ installée**
</dt> <dd> <dl> <dt>

3006 (0xBBE)
</dt> <dt>



Le moniteur d’impression spécifié a déjà été installé.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_PRINT_MONITOR"></span><span id="error_invalid_print_monitor"></span>**ERREUR \_ de \_ moniteur d’impression non valide \_**
</dt> <dd> <dl> <dt>

3007 (0xBBF)
</dt> <dt>



Le moniteur d’impression spécifié ne dispose pas des fonctions requises.


</dt> </dl> </dd> <dt>

<span id="ERROR_PRINT_MONITOR_IN_USE"></span><span id="error_print_monitor_in_use"></span>**ERREUR \_ \_ \_ de l’analyseur d’impression en cours d' \_ utilisation**
</dt> <dd> <dl> <dt>

3008 (0xBC0)
</dt> <dt>



Le moniteur d’impression spécifié est en cours d’utilisation.


</dt> </dl> </dd> <dt>

<span id="ERROR_PRINTER_HAS_JOBS_QUEUED"></span><span id="error_printer_has_jobs_queued"></span>**l' \_ imprimante Error \_ a des travaux en \_ \_ file d’attente**
</dt> <dd> <dl> <dt>

3009 (0xBC1)
</dt> <dt>



L’opération demandée n’est pas autorisée lorsque des travaux sont en file d’attente sur l’imprimante.


</dt> </dl> </dd> <dt>

<span id="ERROR_SUCCESS_REBOOT_REQUIRED"></span><span id="error_success_reboot_required"></span>**ERREUR \_ de \_ redémarrage de la réussite \_ obligatoire**
</dt> <dd> <dl> <dt>

3010 (0xBC2)
</dt> <dt>



L’opération demandée est réussie. Les modifications ne seront effectives qu’après le redémarrage du système.


</dt> </dl> </dd> <dt>

<span id="ERROR_SUCCESS_RESTART_REQUIRED"></span><span id="error_success_restart_required"></span>**ERREUR \_ de \_ redémarrage de la réussite \_ requise**
</dt> <dd> <dl> <dt>

3011 (0xBC3)
</dt> <dt>



L’opération demandée est réussie. Les modifications ne sont pas effectives tant que le service n’est pas redémarré.


</dt> </dl> </dd> <dt>

<span id="ERROR_PRINTER_NOT_FOUND"></span><span id="error_printer_not_found"></span>**ERREUR \_ imprimante \_ \_ introuvable**
</dt> <dd> <dl> <dt>

3012 (0xBC4)
</dt> <dt>



Aucune imprimante n’a été trouvée.


</dt> </dl> </dd> <dt>

<span id="ERROR_PRINTER_DRIVER_WARNED"></span><span id="error_printer_driver_warned"></span>**ERREUR \_ de \_ pilote d’imprimante \_**
</dt> <dd> <dl> <dt>

3013 (0xBC5)
</dt> <dt>



Le pilote d’imprimante est réputé non fiable.


</dt> </dl> </dd> <dt>

<span id="ERROR_PRINTER_DRIVER_BLOCKED"></span><span id="error_printer_driver_blocked"></span>**ERREUR \_ de \_ pilote d’imprimante \_ bloquée**
</dt> <dd> <dl> <dt>

3014 (0xBC6)
</dt> <dt>



Le pilote d’imprimante est connu pour endommager le système.


</dt> </dl> </dd> <dt>

<span id="ERROR_PRINTER_DRIVER_PACKAGE_IN_USE"></span><span id="error_printer_driver_package_in_use"></span>**ERREUR \_ \_ \_ \_ de package de pilotes d’imprimante en cours d' \_ utilisation**
</dt> <dd> <dl> <dt>

3015 (0xBC7)
</dt> <dt>



Le package de pilotes d’imprimante spécifié est en cours d’utilisation.


</dt> </dl> </dd> <dt>

<span id="ERROR_CORE_DRIVER_PACKAGE_NOT_FOUND"></span><span id="error_core_driver_package_not_found"></span>**PACKAGE de pilotes d’erreur \_ Core \_ \_ \_ \_ introuvable**
</dt> <dd> <dl> <dt>

3016 (0xBC8)
</dt> <dt>



Impossible de trouver un package de pilotes principal requis par le package de pilotes d’imprimante.


</dt> </dl> </dd> <dt>

<span id="ERROR_FAIL_REBOOT_REQUIRED"></span><span id="error_fail_reboot_required"></span>**ERREUR d' \_ échec de \_ redémarrage \_ requis**
</dt> <dd> <dl> <dt>

3017 (0xBC9)
</dt> <dt>



L'opération demandée a échoué. Un redémarrage système est nécessaire pour restaurer les modifications apportées.


</dt> </dl> </dd> <dt>

<span id="ERROR_FAIL_REBOOT_INITIATED"></span><span id="error_fail_reboot_initiated"></span>**ERREUR lors de l' \_ échec du \_ redémarrage \_**
</dt> <dd> <dl> <dt>

3018 (0xBCA)
</dt> <dt>



L'opération demandée a échoué. Un redémarrage système a été initié pour restaurer les modifications apportées.


</dt> </dl> </dd> <dt>

<span id="ERROR_PRINTER_DRIVER_DOWNLOAD_NEEDED"></span><span id="error_printer_driver_download_needed"></span>**ERREUR lors du téléchargement du pilote d' \_ imprimante \_ \_ \_**
</dt> <dd> <dl> <dt>

3019 (0xBCB)
</dt> <dt>



Le pilote d’imprimante spécifié est introuvable sur le système et doit être téléchargé.


</dt> </dl> </dd> <dt>

<span id="ERROR_PRINT_JOB_RESTART_REQUIRED"></span><span id="error_print_job_restart_required"></span>**ERREUR \_ de \_ redémarrage du travail d’impression \_ \_ requis**
</dt> <dd> <dl> <dt>

3020 (0xBCC)
</dt> <dt>



L’impression du travail d’impression demandé a échoué. Une mise à jour du système d’impression exige que le travail soit renvoyé.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_PRINTER_DRIVER_MANIFEST"></span><span id="error_invalid_printer_driver_manifest"></span>**ERREUR \_ du \_ \_ manifeste du pilote d’imprimante non valide \_**
</dt> <dd> <dl> <dt>

3021 (0xBCD)
</dt> <dt>



Le pilote d’imprimante ne contient pas de manifeste valide ou contient un trop grand nombre de manifestes.


</dt> </dl> </dd> <dt>

<span id="ERROR_PRINTER_NOT_SHAREABLE"></span><span id="error_printer_not_shareable"></span>**ERREUR de partage de l' \_ imprimante \_ \_**
</dt> <dd> <dl> <dt>

3022 (0xBCE)
</dt> <dt>



Impossible de partager l’imprimante spécifiée.


</dt> </dl> </dd> <dt>

<span id="ERROR_REQUEST_PAUSED"></span><span id="error_request_paused"></span>**demande d’erreur \_ \_ suspendue**
</dt> <dd> <dl> <dt>

3050 (0xBEA)
</dt> <dt>



L’opération a été suspendue.


</dt> </dl> </dd> <dt>

<span id="ERROR_IO_REISSUE_AS_CACHED"></span><span id="error_io_reissue_as_cached"></span>**ERREUR \_ de RÉémission d’e/s \_ \_ \_ mise en cache**
</dt> <dd> <dl> <dt>

3950 (0xF6E)
</dt> <dt>



Réémettez l’opération donnée en tant qu’opération d’e/s mise en cache.


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

 

 




