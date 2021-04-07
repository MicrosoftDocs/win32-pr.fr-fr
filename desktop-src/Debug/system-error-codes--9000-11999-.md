---
description: Décrit les codes d’erreur 9000-11999 définis dans le fichier d’en-tête WinError. h et est destiné aux développeurs.
ms.assetid: 27fe3fee-4ae3-43f1-a1f2-91c935e9851b
title: Codes d’erreur système (9000-11999) (WinError. h)
ms.topic: reference
ms.date: 07/18/2019
ms.openlocfilehash: 01eb071962d8d0f5beb801067ce1d72adc796bad
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748380"
---
# <a name="system-error-codes-9000-11999"></a>Codes d’erreur système (9000-11999)

> [!NOTE]
> Ces informations sont destinées aux développeurs qui déboguent les erreurs système. Pour les autres erreurs, telles que les problèmes de Windows Update, il existe une liste de ressources dans la page [codes d’erreur](system-error-codes.md) .

La liste suivante décrit les [codes d’erreur système](system-error-codes.md) (erreurs 9000 à 11999). Elles sont retournées par la fonction [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) lorsque de nombreuses fonctions échouent. Pour récupérer le texte de description de l’erreur dans votre application, utilisez la fonction [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) avec le **format \_ message \_ de \_** l’indicateur système.

<dl> <dt>

<span id="DNS_ERROR_RCODE_FORMAT_ERROR"></span><span id="dns_error_rcode_format_error"></span>**erreur DNS erreur de \_ \_ \_ format RCODE \_**
</dt> <dd> <dl> <dt>

9001 (0x2329)
</dt> <dt>



Le serveur DNS ne peut pas interpréter le format.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_RCODE_SERVER_FAILURE"></span><span id="dns_error_rcode_server_failure"></span>**erreur DNS- \_ \_ \_ défaillance du serveur RCODE \_**
</dt> <dd> <dl> <dt>

9002 (0x232A)
</dt> <dt>



Échec du serveur DNS.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_RCODE_NAME_ERROR"></span><span id="dns_error_rcode_name_error"></span>**erreur DNS erreur de \_ \_ \_ nom RCODE \_**
</dt> <dd> <dl> <dt>

9003 (0x232B)
</dt> <dt>



Le nom DNS n’existe pas.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_RCODE_NOT_IMPLEMENTED"></span><span id="dns_error_rcode_not_implemented"></span>**\_erreur DNS \_ RCODE \_ non \_ implémentée**
</dt> <dd> <dl> <dt>

9004 (0x232C)
</dt> <dt>



Demande DNS non prise en charge par le serveur de noms.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_RCODE_REFUSED"></span><span id="dns_error_rcode_refused"></span>**\_erreur DNS \_ RCODE \_ refusée**
</dt> <dd> <dl> <dt>

9005 (0x232D)
</dt> <dt>



Opération DNS refusée.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_RCODE_YXDOMAIN"></span><span id="dns_error_rcode_yxdomain"></span>**\_erreur DNS \_ RCODE \_ YXDOMAIN**
</dt> <dd> <dl> <dt>

9006 (0x232E)
</dt> <dt>



Le nom DNS qui ne devrait pas exister existe déjà.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_RCODE_YXRRSET"></span><span id="dns_error_rcode_yxrrset"></span>**\_erreur DNS \_ RCODE \_ YXRRSET**
</dt> <dd> <dl> <dt>

9007 (0x232F)
</dt> <dt>



Il n’existe pas d’ensemble de RR DNS qui ne devrait pas exister.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_RCODE_NXRRSET"></span><span id="dns_error_rcode_nxrrset"></span>**\_erreur DNS \_ RCODE \_ NXRRSET**
</dt> <dd> <dl> <dt>

9008 (0x2330)
</dt> <dt>



L’ensemble de RR DNS qui devrait exister n’existe pas.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_RCODE_NOTAUTH"></span><span id="dns_error_rcode_notauth"></span>**\_erreur DNS \_ RCODE \_ NOTAUTH**
</dt> <dd> <dl> <dt>

9009 (0x2331)
</dt> <dt>



Serveur DNS ne faisant pas autorité pour la zone.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_RCODE_NOTZONE"></span><span id="dns_error_rcode_notzone"></span>**\_erreur DNS \_ RCODE \_ NOTZONE**
</dt> <dd> <dl> <dt>

9010 (0x2332)
</dt> <dt>



Le nom DNS dans Update ou PREREQ n’est pas dans la zone.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_RCODE_BADSIG"></span><span id="dns_error_rcode_badsig"></span>**\_erreur DNS \_ RCODE \_ BADSIG**
</dt> <dd> <dl> <dt>

9016 (0x2338)
</dt> <dt>



Échec de la vérification de la signature DNS.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_RCODE_BADKEY"></span><span id="dns_error_rcode_badkey"></span>**\_erreur DNS \_ RCODE \_ BADKEY**
</dt> <dd> <dl> <dt>

9017 (0x2339)
</dt> <dt>



Clé DNS incorrecte.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_RCODE_BADTIME"></span><span id="dns_error_rcode_badtime"></span>**\_erreur DNS \_ RCODE \_ BADTIME**
</dt> <dd> <dl> <dt>

9018 (0x233A)
</dt> <dt>



Validité de la signature DNS expirée.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_KEYMASTER_REQUIRED"></span><span id="dns_error_keymaster_required"></span>**erreur DNS- \_ \_ principal \_ requis**
</dt> <dd> <dl> <dt>

9101 (0x238D)
</dt> <dt>



Seul le serveur DNS agissant comme maître des clés pour la zone peut effectuer cette opération.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NOT_ALLOWED_ON_SIGNED_ZONE"></span><span id="dns_error_not_allowed_on_signed_zone"></span>**\_erreur DNS \_ non \_ autorisée \_ sur \_ une \_ zone signée**
</dt> <dd> <dl> <dt>

9102 (0x238E)
</dt> <dt>



Cette opération n’est pas autorisée sur une zone qui est signée ou qui possède des clés de signature.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NSEC3_INCOMPATIBLE_WITH_RSA_SHA1"></span><span id="dns_error_nsec3_incompatible_with_rsa_sha1"></span>**\_Erreur DNS \_ NSEC3 \_ incompatible \_ avec \_ RSA \_ SHA1**
</dt> <dd> <dl> <dt>

9103 (0x238F)
</dt> <dt>



NSEC3 n’est pas compatible avec l’algorithme RSA-SHA-1. Choisissez un autre algorithme ou utilisez NSEC.

Cette valeur était également nommée **\_ erreur DNS \_ \_ \_ paramètres NSEC3 non valides**


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NOT_ENOUGH_SIGNING_KEY_DESCRIPTORS"></span><span id="dns_error_not_enough_signing_key_descriptors"></span>**\_erreur DNS \_ \_ insuffisante pour les \_ \_ descripteurs de clé de signature \_**
</dt> <dd> <dl> <dt>

9104 (0x2390)
</dt> <dt>



La zone ne dispose pas de suffisamment de clés de signature. Il doit y avoir au moins une clé de signature de clé (KSK) et au moins une clé de signature de zone (ZSK).


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_UNSUPPORTED_ALGORITHM"></span><span id="dns_error_unsupported_algorithm"></span>**\_algorithme d’erreur DNS \_ non pris en charge \_**
</dt> <dd> <dl> <dt>

9105 (0x2391)
</dt> <dt>



L’algorithme spécifié n’est pas pris en charge.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_INVALID_KEY_SIZE"></span><span id="dns_error_invalid_key_size"></span>**\_erreur DNS \_ \_ taille de clé non valide \_**
</dt> <dd> <dl> <dt>

9106 (0x2392)
</dt> <dt>



La taille de clé spécifiée n’est pas prise en charge.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_SIGNING_KEY_NOT_ACCESSIBLE"></span><span id="dns_error_signing_key_not_accessible"></span>**\_clé de signature d’erreur DNS \_ \_ \_ \_ inaccessible**
</dt> <dd> <dl> <dt>

9107 (0x2393)
</dt> <dt>



Une ou plusieurs clés de signature pour une zone ne sont pas accessibles au serveur DNS. La signature de zone ne sera pas opérationnelle tant que cette erreur ne sera pas résolue.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_KSP_DOES_NOT_SUPPORT_PROTECTION"></span><span id="dns_error_ksp_does_not_support_protection"></span>**l' \_ erreur \_ DNS \_ KSP \_ ne \_ prend pas en charge la \_ protection**
</dt> <dd> <dl> <dt>

9108 (0x2394)
</dt> <dt>



Le fournisseur de stockage de clés spécifié ne prend pas en charge la protection des données DPAPI + +. La signature de zone ne sera pas opérationnelle tant que cette erreur ne sera pas résolue.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_UNEXPECTED_DATA_PROTECTION_ERROR"></span><span id="dns_error_unexpected_data_protection_error"></span>**erreur DNS erreur de \_ \_ protection inattendue des \_ données \_ \_**
</dt> <dd> <dl> <dt>

9109 (0x2395)
</dt> <dt>



Une erreur DPAPI + + inattendue a été rencontrée. La signature de zone ne sera pas opérationnelle tant que cette erreur ne sera pas résolue.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_UNEXPECTED_CNG_ERROR"></span><span id="dns_error_unexpected_cng_error"></span>**erreur DNS- \_ \_ \_ erreur CNG inattendue \_**
</dt> <dd> <dl> <dt>

9110 (0x2396)
</dt> <dt>



Une erreur de chiffrement inattendue s’est produite. La signature de zone peut ne pas être opérationnelle tant que cette erreur n’est pas résolue.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_UNKNOWN_SIGNING_PARAMETER_VERSION"></span><span id="dns_error_unknown_signing_parameter_version"></span>**\_erreur DNS \_ \_ version de paramètre de signature inconnue \_ \_**
</dt> <dd> <dl> <dt>

9111 (0x2397)
</dt> <dt>



Le serveur DNS a rencontré une clé de signature avec une version inconnue. La signature de zone ne sera pas opérationnelle tant que cette erreur ne sera pas résolue.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_KSP_NOT_ACCESSIBLE"></span><span id="dns_error_ksp_not_accessible"></span>**le \_ KSP des erreurs DNS \_ n’est \_ pas \_ accessible**
</dt> <dd> <dl> <dt>

9112 (0x2398)
</dt> <dt>



Le fournisseur du service de clés spécifié ne peut pas être ouvert par le serveur DNS.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_TOO_MANY_SKDS"></span><span id="dns_error_too_many_skds"></span>**\_erreur DNS \_ trop \_ de \_ SKDS**
</dt> <dd> <dl> <dt>

9113 (0x2399)
</dt> <dt>



Le serveur DNS ne peut pas accepter d’autres clés de signature avec l’algorithme spécifié et la valeur de l’indicateur KSK pour cette zone.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_INVALID_ROLLOVER_PERIOD"></span><span id="dns_error_invalid_rollover_period"></span>**\_erreur DNS \_ \_ période de substitution non valide \_**
</dt> <dd> <dl> <dt>

9114 (0x239A)
</dt> <dt>



La période de substitution spécifiée n’est pas valide.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_INVALID_INITIAL_ROLLOVER_OFFSET"></span><span id="dns_error_invalid_initial_rollover_offset"></span>**erreur DNS- \_ \_ \_ décalage de substitution initial non valide \_ \_**
</dt> <dd> <dl> <dt>

9115 (0x239B)
</dt> <dt>



Le décalage de substitution initial spécifié n’est pas valide.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_ROLLOVER_IN_PROGRESS"></span><span id="dns_error_rollover_in_progress"></span>**\_ \_ substitution d’erreur DNS \_ en \_ cours**
</dt> <dd> <dl> <dt>

9116 (0x239C)
</dt> <dt>



La clé de signature spécifiée est déjà en cours de substitution des clés.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_STANDBY_KEY_NOT_PRESENT"></span><span id="dns_error_standby_key_not_present"></span>**\_clé de secours d’erreur DNS \_ \_ \_ \_ absente**
</dt> <dd> <dl> <dt>

9117 (0x239D)
</dt> <dt>



La clé de signature spécifiée n’a pas de clé de secours à révoquer.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NOT_ALLOWED_ON_ZSK"></span><span id="dns_error_not_allowed_on_zsk"></span>**\_erreur DNS \_ non \_ autorisée \_ sur \_ ZSK**
</dt> <dd> <dl> <dt>

9118 (0x239E)
</dt> <dt>



Cette opération n’est pas autorisée sur une clé de signature de zone (ZSK).


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NOT_ALLOWED_ON_ACTIVE_SKD"></span><span id="dns_error_not_allowed_on_active_skd"></span>**\_erreur DNS \_ non \_ autorisée \_ sur \_ un \_ SKD actif**
</dt> <dd> <dl> <dt>

9119 (0x239F)
</dt> <dt>



Cette opération n’est pas autorisée sur une clé de signature active.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_ROLLOVER_ALREADY_QUEUED"></span><span id="dns_error_rollover_already_queued"></span>**\_ \_ substitution d’erreur DNS déjà en \_ \_ file d’attente**
</dt> <dd> <dl> <dt>

9120 (0x23A0)
</dt> <dt>



La clé de signature spécifiée est déjà en file d’attente pour la substitution.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NOT_ALLOWED_ON_UNSIGNED_ZONE"></span><span id="dns_error_not_allowed_on_unsigned_zone"></span>**\_erreur DNS \_ non \_ autorisée \_ sur une \_ zone non signée \_**
</dt> <dd> <dl> <dt>

9121 (0x23A1)
</dt> <dt>



Cette opération n’est pas autorisée sur une zone non signée.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_BAD_KEYMASTER"></span><span id="dns_error_bad_keymaster"></span>**\_erreur DNS \_ mauvais \_ maître**
</dt> <dd> <dl> <dt>

9122 (0x23A2)
</dt> <dt>



Impossible d’effectuer cette opération, car le serveur DNS indiqué comme maître des clés actuel pour cette zone est défaillant ou mal configuré. Résolvez le problème sur le maître des clés actuel pour cette zone ou utilisez un autre serveur DNS pour prendre le rôle de maître des clés.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_INVALID_SIGNATURE_VALIDITY_PERIOD"></span><span id="dns_error_invalid_signature_validity_period"></span>**erreur DNS période de validité de la \_ \_ signature non valide \_ \_ \_**
</dt> <dd> <dl> <dt>

9123 (0x23A3)
</dt> <dt>



La période de validité de la signature spécifiée n’est pas valide.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_INVALID_NSEC3_ITERATION_COUNT"></span><span id="dns_error_invalid_nsec3_iteration_count"></span>**Erreur DNS- \_ \_ \_ nombre d' \_ itérations NSEC3 non valide \_**
</dt> <dd> <dl> <dt>

9124 (0x23A4)
</dt> <dt>



Le nombre d’itérations NSEC3 spécifié est plus élevé que ce qui est autorisé par la longueur de clé minimale utilisée dans la zone.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_DNSSEC_IS_DISABLED"></span><span id="dns_error_dnssec_is_disabled"></span>**l' \_ erreur DNS \_ DNSSEC \_ est \_ désactivée**
</dt> <dd> <dl> <dt>

9125 (0x23A5)
</dt> <dt>



Cette opération n’a pas pu aboutir car le serveur DNS a été configuré avec les fonctionnalités DNSSEC désactivées. Activez DNSSEC sur le serveur DNS.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_INVALID_XML"></span><span id="dns_error_invalid_xml"></span>**\_ \_ code XML non valide pour l’erreur DNS \_**
</dt> <dd> <dl> <dt>

9126 (0x23A6)
</dt> <dt>



Impossible d’effectuer cette opération, car le flux de données XML reçu est vide ou n’est pas valide syntaxiquement.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NO_VALID_TRUST_ANCHORS"></span><span id="dns_error_no_valid_trust_anchors"></span>**\_erreur DNS \_ aucune \_ \_ ancre d’approbation valide \_**
</dt> <dd> <dl> <dt>

9127 (0x23A7)
</dt> <dt>



Cette opération s’est terminée, mais aucune ancre d’approbation n’a été ajoutée, car toutes les ancres d’approbation reçues n’étaient pas valides, ne sont pas prises en charge, ont expiré ou ne seraient pas valides dans moins de 30 jours.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_ROLLOVER_NOT_POKEABLE"></span><span id="dns_error_rollover_not_pokeable"></span>**\_substitution d’erreur DNS \_ non survolée \_ \_**
</dt> <dd> <dl> <dt>

9128 (0x23A8)
</dt> <dt>



La clé de signature spécifiée n’attend pas la mise à jour des services de domaine Active Directory parental.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NSEC3_NAME_COLLISION"></span><span id="dns_error_nsec3_name_collision"></span>**\_Erreur DNS \_ \_ collision de nom NSEC3 \_**
</dt> <dd> <dl> <dt>

9129 (0x23A9)
</dt> <dt>



Collision de hachage détectée au cours de la signature NSEC3. Spécifiez un autre Salt fourni par l’utilisateur ou utilisez un Salt généré de manière aléatoire, puis essayez de signer à nouveau la zone.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NSEC_INCOMPATIBLE_WITH_NSEC3_RSA_SHA1"></span><span id="dns_error_nsec_incompatible_with_nsec3_rsa_sha1"></span>**\_Erreur DNS \_ NSEC \_ incompatible \_ avec la fonction de \_ \_ \_ hachage RSA SHA1**
</dt> <dd> <dl> <dt>

9130 (0x23AA)
</dt> <dt>



NSEC n’est pas compatible avec l’algorithme NSEC3-RSA-SHA-1. Choisissez un algorithme différent ou utilisez NSEC3.


</dt> </dl> </dd> <dt>

<span id="DNS_INFO_NO_RECORDS"></span><span id="dns_info_no_records"></span>**\_informations DNS \_ aucun \_ enregistrement**
</dt> <dd> <dl> <dt>

9501 (0x251D)
</dt> <dt>



Aucun enregistrement trouvé pour la requête DNS donnée.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_BAD_PACKET"></span><span id="dns_error_bad_packet"></span>**erreur DNS de \_ \_ paquet incorrect \_**
</dt> <dd> <dl> <dt>

9502 (0x251E)
</dt> <dt>



Paquet DNS incorrect.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NO_PACKET"></span><span id="dns_error_no_packet"></span>**erreur DNS- \_ \_ aucun \_ paquet**
</dt> <dd> <dl> <dt>

9503 (0x251F)
</dt> <dt>



Aucun paquet DNS.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_RCODE"></span><span id="dns_error_rcode"></span>**\_erreur DNS \_ RCODE**
</dt> <dd> <dl> <dt>

9504 (0x2520)
</dt> <dt>



Erreur DNS, vérifiez le RCODE.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_UNSECURE_PACKET"></span><span id="dns_error_unsecure_packet"></span>**\_paquet d’erreur DNS \_ non sécurisé \_**
</dt> <dd> <dl> <dt>

9505 (0x2521)
</dt> <dt>



Paquet DNS non sécurisé.


</dt> </dl> </dd> <dt>

<span id="DNS_REQUEST_PENDING"></span><span id="dns_request_pending"></span>**\_demande DNS \_ en attente**
</dt> <dd> <dl> <dt>

9506 (0x2522)
</dt> <dt>



La demande de requête DNS est en attente.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_INVALID_TYPE"></span><span id="dns_error_invalid_type"></span>**\_erreur DNS \_ type non valide \_**
</dt> <dd> <dl> <dt>

9551 (0x254F)
</dt> <dt>



Type DNS non valide.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_INVALID_IP_ADDRESS"></span><span id="dns_error_invalid_ip_address"></span>**\_erreur DNS \_ \_ adresse IP non valide \_**
</dt> <dd> <dl> <dt>

9552 (0x2550)
</dt> <dt>



Adresse IP non valide.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_INVALID_PROPERTY"></span><span id="dns_error_invalid_property"></span>**\_propriété erreur DNS \_ non valide \_**
</dt> <dd> <dl> <dt>

9553 (0x2551)
</dt> <dt>



Propriété non valide.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_TRY_AGAIN_LATER"></span><span id="dns_error_try_again_later"></span>**\_erreur DNS \_ Réessayer \_ \_ plus tard**
</dt> <dd> <dl> <dt>

9554 (0x2552)
</dt> <dt>



Réessayez l’opération DNS ultérieurement.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NOT_UNIQUE"></span><span id="dns_error_not_unique"></span>**\_erreur DNS \_ non \_ unique**
</dt> <dd> <dl> <dt>

9555 (0x2553)
</dt> <dt>



L’enregistrement pour le nom et le type donnés n’est pas unique.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NON_RFC_NAME"></span><span id="dns_error_non_rfc_name"></span>**\_erreur DNS \_ \_ nom non RFC \_**
</dt> <dd> <dl> <dt>

9556 (0x2554)
</dt> <dt>



Le nom DNS n’est pas conforme aux spécifications RFC.


</dt> </dl> </dd> <dt>

<span id="DNS_STATUS_FQDN"></span><span id="dns_status_fqdn"></span>**\_nom de \_ domaine complet de l’État DNS**
</dt> <dd> <dl> <dt>

9557 (0x2555)
</dt> <dt>



Le nom DNS est un nom DNS complet.


</dt> </dl> </dd> <dt>

<span id="DNS_STATUS_DOTTED_NAME"></span><span id="dns_status_dotted_name"></span>**\_nom en \_ pointillés de l’État DNS \_**
</dt> <dd> <dl> <dt>

9558 (0x2556)
</dt> <dt>



Le nom DNS est en pointillés (étiquette multiple).


</dt> </dl> </dd> <dt>

<span id="DNS_STATUS_SINGLE_PART_NAME"></span><span id="dns_status_single_part_name"></span>**nom de la \_ \_ seule \_ partie \_ de l’État DNS**
</dt> <dd> <dl> <dt>

9559 (0x2557)
</dt> <dt>



Le nom DNS est un nom en une seule partie.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_INVALID_NAME_CHAR"></span><span id="dns_error_invalid_name_char"></span>**\_erreur DNS \_ nom de \_ nom non valide \_**
</dt> <dd> <dl> <dt>

9560 (0x2558)
</dt> <dt>



Le nom DNS contient un caractère non valide.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NUMERIC_NAME"></span><span id="dns_error_numeric_name"></span>**\_ \_ nom numérique de l’erreur DNS \_**
</dt> <dd> <dl> <dt>

9561 (0x2559)
</dt> <dt>



Le nom DNS est entièrement numérique.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NOT_ALLOWED_ON_ROOT_SERVER"></span><span id="dns_error_not_allowed_on_root_server"></span>**\_erreur DNS \_ non \_ autorisée \_ sur \_ le \_ serveur racine**
</dt> <dd> <dl> <dt>

9562 (0x255A)
</dt> <dt>



L’opération demandée n’est pas autorisée sur un serveur racine DNS.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NOT_ALLOWED_UNDER_DELEGATION"></span><span id="dns_error_not_allowed_under_delegation"></span>**\_erreur DNS \_ non \_ autorisée \_ sous \_ délégation**
</dt> <dd> <dl> <dt>

9563 (0x255B)
</dt> <dt>



L’enregistrement n’a pas pu être créé, car cette partie de l’espace de noms DNS a été déléguée à un autre serveur.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_CANNOT_FIND_ROOT_HINTS"></span><span id="dns_error_cannot_find_root_hints"></span>**\_erreur DNS \_ Impossible de trouver les \_ \_ indications de racine \_**
</dt> <dd> <dl> <dt>

9564 (0x255C)
</dt> <dt>



Le serveur DNS n’a pas pu trouver un ensemble d’indications de racine.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_INCONSISTENT_ROOT_HINTS"></span><span id="dns_error_inconsistent_root_hints"></span>**\_indications de \_ racine incohérentes d’erreur DNS \_ \_**
</dt> <dd> <dl> <dt>

9565 (0x255D)
</dt> <dt>



Le serveur DNS a trouvé des indications de racine, mais elles n’étaient pas cohérentes sur tous les adaptateurs.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_DWORD_VALUE_TOO_SMALL"></span><span id="dns_error_dword_value_too_small"></span>**\_valeur DWORD de l’erreur DNS \_ \_ \_ trop \_ petite**
</dt> <dd> <dl> <dt>

9566 (0x255E)
</dt> <dt>



La valeur spécifiée est trop petite pour ce paramètre.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_DWORD_VALUE_TOO_LARGE"></span><span id="dns_error_dword_value_too_large"></span>**\_valeur DWORD de l’erreur DNS \_ \_ \_ trop \_ grande**
</dt> <dd> <dl> <dt>

9567 (0x255F)
</dt> <dt>



La valeur spécifiée est trop grande pour ce paramètre.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_BACKGROUND_LOADING"></span><span id="dns_error_background_loading"></span>**erreur DNS lors \_ \_ du chargement en arrière-plan \_**
</dt> <dd> <dl> <dt>

9568 (0x2560)
</dt> <dt>



Cette opération n’est pas autorisée pendant que le serveur DNS charge des zones en arrière-plan. Veuillez réessayer plus tard.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NOT_ALLOWED_ON_RODC"></span><span id="dns_error_not_allowed_on_rodc"></span>**\_erreur DNS \_ non \_ autorisée \_ sur \_ RODC**
</dt> <dd> <dl> <dt>

9569 (0x2561)
</dt> <dt>



L’opération demandée n’est pas autorisée sur un serveur DNS s’exécutant sur un contrôleur de domaine en lecture seule.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NOT_ALLOWED_UNDER_DNAME"></span><span id="dns_error_not_allowed_under_dname"></span>**\_erreur DNS \_ non \_ autorisée \_ sous \_ dname**
</dt> <dd> <dl> <dt>

9570 (0x2562)
</dt> <dt>



Aucune donnée ne peut exister sous un enregistrement DNAME.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_DELEGATION_REQUIRED"></span><span id="dns_error_delegation_required"></span>**\_délégation d’erreurs DNS \_ \_ requise**
</dt> <dd> <dl> <dt>

9571 (0x2563)
</dt> <dt>



Cette opération nécessite la délégation des informations d’identification.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_INVALID_POLICY_TABLE"></span><span id="dns_error_invalid_policy_table"></span>**\_erreur DNS \_ \_ table de stratégie non valide \_**
</dt> <dd> <dl> <dt>

9572 (0x2564)
</dt> <dt>



La table de stratégie de résolution de noms a été endommagée. La résolution DNS échouera jusqu’à ce qu’elle soit résolue. Contactez votre administrateur réseau.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_ZONE_DOES_NOT_EXIST"></span><span id="dns_error_zone_does_not_exist"></span>**la \_ zone d’erreur DNS \_ \_ n' \_ \_ existe pas**
</dt> <dd> <dl> <dt>

9601 (0x2581)
</dt> <dt>



La zone DNS n’existe pas.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NO_ZONE_INFO"></span><span id="dns_error_no_zone_info"></span>**\_erreur DNS \_ aucune \_ information de zone \_**
</dt> <dd> <dl> <dt>

9602 (0x2582)
</dt> <dt>



Les informations de zone DNS ne sont pas disponibles.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_INVALID_ZONE_OPERATION"></span><span id="dns_error_invalid_zone_operation"></span>**\_erreur DNS erreur de \_ zone non valide \_ \_**
</dt> <dd> <dl> <dt>

9603 (0x2583)
</dt> <dt>



Opération non valide pour la zone DNS.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_ZONE_CONFIGURATION_ERROR"></span><span id="dns_error_zone_configuration_error"></span>**\_erreur de \_ configuration du fuseau erreur \_ DNS \_**
</dt> <dd> <dl> <dt>

9604 (0x2584)
</dt> <dt>



Configuration de zone DNS non valide.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_ZONE_HAS_NO_SOA_RECORD"></span><span id="dns_error_zone_has_no_soa_record"></span>**la \_ zone d’erreur DNS n' \_ \_ a \_ pas d' \_ \_ enregistrement SOA**
</dt> <dd> <dl> <dt>

9605 (0x2585)
</dt> <dt>



La zone DNS n’a pas d’enregistrement SOA (Start of Authority).


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_ZONE_HAS_NO_NS_RECORDS"></span><span id="dns_error_zone_has_no_ns_records"></span>**la \_ zone d’erreur DNS n' \_ \_ a \_ pas d' \_ \_ enregistrements NS**
</dt> <dd> <dl> <dt>

9606 (0x2586)
</dt> <dt>



La zone DNS n’a aucun enregistrement de serveur de noms (NS).


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_ZONE_LOCKED"></span><span id="dns_error_zone_locked"></span>**\_zone d’erreur DNS \_ \_ verrouillée**
</dt> <dd> <dl> <dt>

9607 (0x2587)
</dt> <dt>



La zone DNS est verrouillée.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_ZONE_CREATION_FAILED"></span><span id="dns_error_zone_creation_failed"></span>**échec de la création de la \_ zone d’erreur DNS \_ \_ \_**
</dt> <dd> <dl> <dt>

9608 (0x2588)
</dt> <dt>



Échec de la création de la zone DNS.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_ZONE_ALREADY_EXISTS"></span><span id="dns_error_zone_already_exists"></span>**la \_ zone d’erreur DNS \_ \_ \_ existe déjà**
</dt> <dd> <dl> <dt>

9609 (0x2589)
</dt> <dt>



La zone DNS existe déjà.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_AUTOZONE_ALREADY_EXISTS"></span><span id="dns_error_autozone_already_exists"></span>**une \_ erreur DNS \_ \_ existe déjà \_**
</dt> <dd> <dl> <dt>

9610 (0x258A)
</dt> <dt>



La zone DNS automatique existe déjà.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_INVALID_ZONE_TYPE"></span><span id="dns_error_invalid_zone_type"></span>**\_erreur DNS \_ \_ type de zone non valide \_**
</dt> <dd> <dl> <dt>

9611 (0x258B)
</dt> <dt>



Type de zone DNS non valide.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_SECONDARY_REQUIRES_MASTER_IP"></span><span id="dns_error_secondary_requires_master_ip"></span>**erreur DNS la base de données \_ \_ secondaire \_ requiert une \_ \_ adresse IP principale**
</dt> <dd> <dl> <dt>

9612 (0x258C)
</dt> <dt>



La zone DNS secondaire requiert une adresse IP principale.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_ZONE_NOT_SECONDARY"></span><span id="dns_error_zone_not_secondary"></span>**\_zone d’erreur DNS \_ \_ non \_ secondaire**
</dt> <dd> <dl> <dt>

9613 (0x258D)
</dt> <dt>



Zone DNS non secondaire.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NEED_SECONDARY_ADDRESSES"></span><span id="dns_error_need_secondary_addresses"></span>**une \_ erreur DNS \_ nécessite des \_ \_ adresses secondaires**
</dt> <dd> <dl> <dt>

9614 (0x258E)
</dt> <dt>



Vous avez besoin d’une adresse IP secondaire.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_WINS_INIT_FAILED"></span><span id="dns_error_wins_init_failed"></span>**\_échec de \_ l' \_ initialisation \_ WINS de l’erreur DNS**
</dt> <dd> <dl> <dt>

9615 (0x258F)
</dt> <dt>



Échec de l’initialisation WINS.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NEED_WINS_SERVERS"></span><span id="dns_error_need_wins_servers"></span>**une \_ erreur DNS \_ nécessite des \_ \_ serveurs WINS**
</dt> <dd> <dl> <dt>

9616 (0x2590)
</dt> <dt>



Serveurs WINS requis.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NBSTAT_INIT_FAILED"></span><span id="dns_error_nbstat_init_failed"></span>**\_erreur DNS \_ NBSTAT \_ init \_ failed**
</dt> <dd> <dl> <dt>

9617 (0x2591)
</dt> <dt>



Échec de l’appel d’initialisation NBTSTAT.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_SOA_DELETE_INVALID"></span><span id="dns_error_soa_delete_invalid"></span>**\_erreur DNS \_ SOA \_ suppression \_ non valide**
</dt> <dd> <dl> <dt>

9618 (0x2592)
</dt> <dt>



Suppression non valide du SOA (Start of Authority).


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_FORWARDER_ALREADY_EXISTS"></span><span id="dns_error_forwarder_already_exists"></span>**le \_ redirecteur des erreurs DNS \_ \_ \_ existe déjà**
</dt> <dd> <dl> <dt>

9619 (0x2593)
</dt> <dt>



Il existe déjà une zone de transfert conditionnel pour ce nom.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_ZONE_REQUIRES_MASTER_IP"></span><span id="dns_error_zone_requires_master_ip"></span>**la \_ zone d’erreur DNS \_ nécessite une \_ \_ \_ adresse IP principale**
</dt> <dd> <dl> <dt>

9620 (0x2594)
</dt> <dt>



Cette zone doit être configurée avec une ou plusieurs adresses IP de serveur DNS maître.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_ZONE_IS_SHUTDOWN"></span><span id="dns_error_zone_is_shutdown"></span>**la \_ zone d’erreur DNS \_ \_ est \_ Shutdown**
</dt> <dd> <dl> <dt>

9621 (0x2595)
</dt> <dt>



Impossible d’effectuer l’opération, car cette zone est arrêtée.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_ZONE_LOCKED_FOR_SIGNING"></span><span id="dns_error_zone_locked_for_signing"></span>**\_ \_ zone d’erreur DNS \_ verrouillée \_ pour la \_ signature**
</dt> <dd> <dl> <dt>

9622 (0x2596)
</dt> <dt>



Impossible d’effectuer cette opération, car la zone est actuellement signée. Veuillez réessayer plus tard.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_PRIMARY_REQUIRES_DATAFILE"></span><span id="dns_error_primary_requires_datafile"></span>**une \_ erreur DNS \_ principale \_ nécessite un fichier de \_ fichier**
</dt> <dd> <dl> <dt>

9651 (0x25B3)
</dt> <dt>



La zone DNS principale nécessite un fichier de fichier.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_INVALID_DATAFILE_NAME"></span><span id="dns_error_invalid_datafile_name"></span>**\_erreur DNS \_ nom du fichier de fichier non valide \_ \_**
</dt> <dd> <dl> <dt>

9652 (0x25B4)
</dt> <dt>



Nom de fichier de fichier non valide pour la zone DNS.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_DATAFILE_OPEN_FAILURE"></span><span id="dns_error_datafile_open_failure"></span>**échec de l' \_ ouverture du fichier de fichier d’erreur DNS \_ \_ \_**
</dt> <dd> <dl> <dt>

9653 (0x25B5)
</dt> <dt>



Impossible d’ouvrir le fichier de fichier pour la zone DNS.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_FILE_WRITEBACK_FAILED"></span><span id="dns_error_file_writeback_failed"></span>**\_échec de \_ l' \_ écriture différée du fichier d’erreurs DNS \_**
</dt> <dd> <dl> <dt>

9654 (0x25B6)
</dt> <dt>



Échec de l’écriture du fichier de fichier pour la zone DNS.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_DATAFILE_PARSING"></span><span id="dns_error_datafile_parsing"></span>**erreur DNS lors de l' \_ \_ analyse du fichier de fichier \_**
</dt> <dd> <dl> <dt>

9655 (0x25B7)
</dt> <dt>



Échec lors de la lecture du fichier de fichier pour la zone DNS.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_RECORD_DOES_NOT_EXIST"></span><span id="dns_error_record_does_not_exist"></span>**l' \_ enregistrement d’erreur DNS \_ \_ n' \_ \_ existe pas**
</dt> <dd> <dl> <dt>

9701 (0x25E5)
</dt> <dt>



L’enregistrement DNS n’existe pas.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_RECORD_FORMAT"></span><span id="dns_error_record_format"></span>**\_format d' \_ enregistrement des erreurs DNS \_**
</dt> <dd> <dl> <dt>

9702 (0x25E6)
</dt> <dt>



Erreur de format d’enregistrement DNS.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NODE_CREATION_FAILED"></span><span id="dns_error_node_creation_failed"></span>**échec de la création du nœud d' \_ erreur DNS \_ \_ \_**
</dt> <dd> <dl> <dt>

9703 (0x25E7)
</dt> <dt>



Échec de la création du nœud dans DNS.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_UNKNOWN_RECORD_TYPE"></span><span id="dns_error_unknown_record_type"></span>**\_type d’enregistrement d’erreur DNS \_ inconnu \_ \_**
</dt> <dd> <dl> <dt>

9704 (0x25E8)
</dt> <dt>



Type d’enregistrement DNS inconnu.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_RECORD_TIMED_OUT"></span><span id="dns_error_record_timed_out"></span>**expiration du délai de l' \_ enregistrement d’erreur DNS \_ \_ \_**
</dt> <dd> <dl> <dt>

9705 (0x25E9)
</dt> <dt>



Expiration du délai de l’enregistrement DNS.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NAME_NOT_IN_ZONE"></span><span id="dns_error_name_not_in_zone"></span>**\_ \_ nom d’erreur DNS \_ non dans la \_ \_ zone**
</dt> <dd> <dl> <dt>

9706 (0x25EA)
</dt> <dt>



Le nom n’est pas dans la zone DNS.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_CNAME_LOOP"></span><span id="dns_error_cname_loop"></span>**\_ \_ boucle CNAME d’erreur DNS \_**
</dt> <dd> <dl> <dt>

9707 (0x25EB)
</dt> <dt>



Boucle CNAMe détectée.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NODE_IS_CNAME"></span><span id="dns_error_node_is_cname"></span>**le \_ nœud d’erreur DNS \_ \_ est \_ CNAME**
</dt> <dd> <dl> <dt>

9708 (0x25EC)
</dt> <dt>



Le nœud est un enregistrement DNS CNAMe.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_CNAME_COLLISION"></span><span id="dns_error_cname_collision"></span>**\_erreur DNS \_ CNAME \_ collision**
</dt> <dd> <dl> <dt>

9709 (0x25ED)
</dt> <dt>



Un enregistrement CNAMe existe déjà pour le nom donné.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_RECORD_ONLY_AT_ZONE_ROOT"></span><span id="dns_error_record_only_at_zone_root"></span>**\_enregistrement des erreurs DNS \_ \_ uniquement à la \_ racine de la \_ zone \_**
</dt> <dd> <dl> <dt>

9710 (0x25EE)
</dt> <dt>



Enregistrement uniquement au niveau de la racine de la zone DNS.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_RECORD_ALREADY_EXISTS"></span><span id="dns_error_record_already_exists"></span>**un \_ enregistrement d’erreur DNS \_ \_ \_ existe déjà**
</dt> <dd> <dl> <dt>

9711 (0x25EF)
</dt> <dt>



L’enregistrement DNS existe déjà.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_SECONDARY_DATA"></span><span id="dns_error_secondary_data"></span>**\_ \_ données secondaires d’erreur DNS \_**
</dt> <dd> <dl> <dt>

9712 (0x25F0)
</dt> <dt>



Erreur de données de la zone DNS secondaire.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NO_CREATE_CACHE_DATA"></span><span id="dns_error_no_create_cache_data"></span>**erreur DNS- \_ \_ pas de création de \_ \_ données de cache \_**
</dt> <dd> <dl> <dt>

9713 (0x25F1)
</dt> <dt>



Impossible de créer les données du cache DNS.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NAME_DOES_NOT_EXIST"></span><span id="dns_error_name_does_not_exist"></span>**le \_ nom d’erreur DNS \_ \_ n' \_ \_ existe pas**
</dt> <dd> <dl> <dt>

9714 (0x25F2)
</dt> <dt>



Le nom DNS n’existe pas.


</dt> </dl> </dd> <dt>

<span id="DNS_WARNING_PTR_CREATE_FAILED"></span><span id="dns_warning_ptr_create_failed"></span>**échec de la création du PTR d' \_ Avertissement DNS \_ \_ \_**
</dt> <dd> <dl> <dt>

9715 (0x25F3)
</dt> <dt>



Impossible de créer un enregistrement de pointeur (PTR).


</dt> </dl> </dd> <dt>

<span id="DNS_WARNING_DOMAIN_UNDELETED"></span><span id="dns_warning_domain_undeleted"></span>**\_domaine d’avertissement DNS \_ \_ supprimé**
</dt> <dd> <dl> <dt>

9716 (0x25F4)
</dt> <dt>



Le domaine DNS n’a pas été supprimé.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_DS_UNAVAILABLE"></span><span id="dns_error_ds_unavailable"></span>**\_erreur DNS \_ \_ non disponible**
</dt> <dd> <dl> <dt>

9717 (0x25F5)
</dt> <dt>



Le service d’annuaire n’est pas disponible.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_DS_ZONE_ALREADY_EXISTS"></span><span id="dns_error_ds_zone_already_exists"></span>**une erreur DNS de la \_ \_ \_ zone DS \_ \_ existe déjà**
</dt> <dd> <dl> <dt>

9718 (0x25F6)
</dt> <dt>



La zone DNS existe déjà dans le service d’annuaire.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NO_BOOTFILE_IF_DS_ZONE"></span><span id="dns_error_no_bootfile_if_ds_zone"></span>**\_erreur DNS \_ non \_ BOOTFILE \_ si \_ la \_ zone DS**
</dt> <dd> <dl> <dt>

9719 (0x25F7)
</dt> <dt>



Le serveur DNS ne crée pas ou ne lit pas le fichier de démarrage pour la zone DNS intégrée au service d’annuaire.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NODE_IS_DNAME"></span><span id="dns_error_node_is_dname"></span>**le \_ nœud d’erreur DNS \_ \_ est \_ dname**
</dt> <dd> <dl> <dt>

9720 (0x25F8)
</dt> <dt>



Le nœud est un enregistrement DNS DNAME.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_DNAME_COLLISION"></span><span id="dns_error_dname_collision"></span>**\_erreur DNS \_ - \_ collision dname**
</dt> <dd> <dl> <dt>

9721 (0x25F9)
</dt> <dt>



Un enregistrement DNAME existe déjà pour le nom donné.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_ALIAS_LOOP"></span><span id="dns_error_alias_loop"></span>**\_boucle d' \_ alias d’erreur DNS \_**
</dt> <dd> <dl> <dt>

9722 (0x25FA)
</dt> <dt>



Une boucle d’alias a été détectée avec des enregistrements CNAMe ou DNAME.


</dt> </dl> </dd> <dt>

<span id="DNS_INFO_AXFR_COMPLETE"></span><span id="dns_info_axfr_complete"></span>**informations de DNS \_ sur le \_ AXFR \_ terminées**
</dt> <dd> <dl> <dt>

9751 (0x2617)
</dt> <dt>



DNS AXFR (transfert de zone) terminé.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_AXFR"></span><span id="dns_error_axfr"></span>**\_erreur DNS \_ AXFR**
</dt> <dd> <dl> <dt>

9752 (0x2618)
</dt> <dt>



Échec du transfert de la zone DNS.


</dt> </dl> </dd> <dt>

<span id="DNS_INFO_ADDED_LOCAL_WINS"></span><span id="dns_info_added_local_wins"></span>**\_Ajout du \_ \_ WINS local \_ aux informations DNS**
</dt> <dd> <dl> <dt>

9753 (0x2619)
</dt> <dt>



Serveur WINS local ajouté.


</dt> </dl> </dd> <dt>

<span id="DNS_STATUS_CONTINUE_NEEDED"></span><span id="dns_status_continue_needed"></span>**\_État DNS \_ toujours \_ nécessaire**
</dt> <dd> <dl> <dt>

9801 (0x2649)
</dt> <dt>



L’appel de mise à jour sécurisée doit continuer la demande de mise à jour.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NO_TCPIP"></span><span id="dns_error_no_tcpip"></span>**\_erreur DNS \_ non \_ tcpip**
</dt> <dd> <dl> <dt>

9851 (0x267B)
</dt> <dt>



Le protocole réseau TCP/IP n’est pas installé.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NO_DNS_SERVERS"></span><span id="dns_error_no_dns_servers"></span>**\_erreur DNS \_ aucun \_ \_ serveur DNS**
</dt> <dd> <dl> <dt>

9852 (0x267C)
</dt> <dt>



Aucun serveur DNS configuré pour le système local.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_DP_DOES_NOT_EXIST"></span><span id="dns_error_dp_does_not_exist"></span>**l' \_ erreur \_ DNS \_ DP \_ n' \_ existe pas**
</dt> <dd> <dl> <dt>

9901 (0x26AD)
</dt> <dt>



La partition d’annuaire spécifiée n’existe pas.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_DP_ALREADY_EXISTS"></span><span id="dns_error_dp_already_exists"></span>**l' \_ erreur \_ DNS \_ DP \_ existe déjà**
</dt> <dd> <dl> <dt>

9902 (0x26AE)
</dt> <dt>



La partition d’annuaire spécifiée existe déjà.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_DP_NOT_ENLISTED"></span><span id="dns_error_dp_not_enlisted"></span>**\_erreur DNS \_ DP \_ non \_ inscrite**
</dt> <dd> <dl> <dt>

9903 (0x26AF)
</dt> <dt>



Ce serveur DNS n’est pas inscrit dans la partition d’annuaire spécifiée.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_DP_ALREADY_ENLISTED"></span><span id="dns_error_dp_already_enlisted"></span>**\_erreur DNS \_ DP \_ déjà \_ inscrite**
</dt> <dd> <dl> <dt>

9904 (0x26B0)
</dt> <dt>



Ce serveur DNS est déjà inscrit dans la partition d’annuaire spécifiée.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_DP_NOT_AVAILABLE"></span><span id="dns_error_dp_not_available"></span>**\_DP d’erreur DNS \_ \_ non \_ disponible**
</dt> <dd> <dl> <dt>

9905 (0x26B1)
</dt> <dt>



La partition d’annuaire n’est pas disponible pour l’instant. Patientez quelques minutes et recommencez.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_DP_FSMO_ERROR"></span><span id="dns_error_dp_fsmo_error"></span>**erreur \_ DNS \_ DP \_ FSMO \_**
</dt> <dd> <dl> <dt>

9906 (0x26B2)
</dt> <dt>



L’opération a échoué car le rôle FSMO du maître d’opérations des noms de domaine est inaccessible. Le contrôleur de domaine détenant le rôle FSMO du maître d’attribution de noms de domaine est inactif ou ne peut pas traiter la demande ou n’exécute pas Windows Server 2003 ou une version ultérieure.


</dt> </dl> </dd> <dt>

<span id="WSAEINTR"></span><span id="wsaeintr"></span>**WSAEINTR**
</dt> <dd> <dl> <dt>

10004 (0x2714)
</dt> <dt>



Une opération de blocage a été interrompue par un appel à WSACancelBlockingCall.


</dt> </dl> </dd> <dt>

<span id="WSAEBADF"></span><span id="wsaebadf"></span>**WSAEBADF**
</dt> <dd> <dl> <dt>

10009 (0x2719)
</dt> <dt>



Le descripteur de fichier fourni n’est pas valide.


</dt> </dl> </dd> <dt>

<span id="WSAEACCES"></span><span id="wsaeacces"></span>**WSAEACCES**
</dt> <dd> <dl> <dt>

10013 (0x271D)
</dt> <dt>



Une tentative a été effectuée pour accéder à un socket de manière interdite par ses autorisations d’accès.


</dt> </dl> </dd> <dt>

<span id="WSAEFAULT"></span><span id="wsaefault"></span>**WSAEFAULT**
</dt> <dd> <dl> <dt>

10014 (0x271E)
</dt> <dt>



Le système a détecté une adresse de pointeur non valide lors de la tentative d’utilisation d’un argument de pointeur dans un appel.


</dt> </dl> </dd> <dt>

<span id="WSAEINVAL"></span><span id="wsaeinval"></span>**WSAEINVAL**
</dt> <dd> <dl> <dt>

10022 (0x2726)
</dt> <dt>



Argument non valide fourni.


</dt> </dl> </dd> <dt>

<span id="WSAEMFILE"></span><span id="wsaemfile"></span>**WSAEMFILE**
</dt> <dd> <dl> <dt>

10024 (0x2728)
</dt> <dt>



Trop de sockets ouverts.


</dt> </dl> </dd> <dt>

<span id="WSAEWOULDBLOCK"></span><span id="wsaewouldblock"></span>**WSAEWOULDBLOCK**
</dt> <dd> <dl> <dt>

10035 (0x2733)
</dt> <dt>



Une opération de socket non bloquante n’a pas pu être effectuée immédiatement.


</dt> </dl> </dd> <dt>

<span id="WSAEINPROGRESS"></span><span id="wsaeinprogress"></span>**WSAEINPROGRESS**
</dt> <dd> <dl> <dt>

10036 (0x2734)
</dt> <dt>



Une opération de blocage est actuellement en cours d'exécution.


</dt> </dl> </dd> <dt>

<span id="WSAEALREADY"></span><span id="wsaealready"></span>**WSAEALREADY**
</dt> <dd> <dl> <dt>

10037 (0x2735)
</dt> <dt>



Tentative d'opération sur un socket non bloquant au niveau duquel une opération était déjà en cours.


</dt> </dl> </dd> <dt>

<span id="WSAENOTSOCK"></span><span id="wsaenotsock"></span>**WSAENOTSOCK**
</dt> <dd> <dl> <dt>

10038 (0x2736)
</dt> <dt>



Une opération a été tentée sur un qui n’est pas un Socket.


</dt> </dl> </dd> <dt>

<span id="WSAEDESTADDRREQ"></span><span id="wsaedestaddrreq"></span>**WSAEDESTADDRREQ**
</dt> <dd> <dl> <dt>

10039 (0x2737)
</dt> <dt>



Une adresse requise a été omise d’une opération sur un Socket.


</dt> </dl> </dd> <dt>

<span id="WSAEMSGSIZE"></span><span id="wsaemsgsize"></span>**WSAEMSGSIZE**
</dt> <dd> <dl> <dt>

10040 (0x2738)
</dt> <dt>



Un message envoyé sur un socket datagramme était plus volumineux que le tampon de messages interne ou qu'une autre limite réseau ou bien le tampon utilisé pour recevoir un datagramme était plus petit que le datagramme lui-même.


</dt> </dl> </dd> <dt>

<span id="WSAEPROTOTYPE"></span><span id="wsaeprototype"></span>**WSAEPROTOTYPE**
</dt> <dd> <dl> <dt>

10041 (0x2739)
</dt> <dt>



Un protocole a été spécifié dans l’appel de fonction socket qui ne prend pas en charge la sémantique du type de socket demandé.


</dt> </dl> </dd> <dt>

<span id="WSAENOPROTOOPT"></span><span id="wsaenoprotoopt"></span>**WSAENOPROTOOPT**
</dt> <dd> <dl> <dt>

10042 (0x273A)
</dt> <dt>



Une option ou un niveau inconnu, non valide ou non pris en charge a été spécifié dans un appel getsockopt ou setsockopt.


</dt> </dl> </dd> <dt>

<span id="WSAEPROTONOSUPPORT"></span><span id="wsaeprotonosupport"></span>**WSAEPROTONOSUPPORT**
</dt> <dd> <dl> <dt>

10043 (0x273B)
</dt> <dt>



Le protocole demandé n’a pas été configuré dans le système, ou aucune implémentation de ce dernier n’existe.


</dt> </dl> </dd> <dt>

<span id="WSAESOCKTNOSUPPORT"></span><span id="wsaesocktnosupport"></span>**WSAESOCKTNOSUPPORT**
</dt> <dd> <dl> <dt>

10044 (0x273C)
</dt> <dt>



La prise en charge du type de socket spécifié n'existe pas dans cette famille d'adresses.


</dt> </dl> </dd> <dt>

<span id="WSAEOPNOTSUPP"></span><span id="wsaeopnotsupp"></span>**WSAEOPNOTSUPP**
</dt> <dd> <dl> <dt>

10045 (0x273D)
</dt> <dt>



L’opération tentée n’est pas prise en charge pour le type d’objet référencé.


</dt> </dl> </dd> <dt>

<span id="WSAEPFNOSUPPORT"></span><span id="wsaepfnosupport"></span>**WSAEPFNOSUPPORT**
</dt> <dd> <dl> <dt>

10046 (0x273E)
</dt> <dt>



La famille de protocoles n’a pas été configurée dans le système ou aucune implémentation de celle-ci n’existe.


</dt> </dl> </dd> <dt>

<span id="WSAEAFNOSUPPORT"></span><span id="wsaeafnosupport"></span>**WSAEAFNOSUPPORT**
</dt> <dd> <dl> <dt>

10047 (0x273F)
</dt> <dt>



Une adresse incompatible avec le protocole demandé a été utilisée.


</dt> </dl> </dd> <dt>

<span id="WSAEADDRINUSE"></span><span id="wsaeaddrinuse"></span>**WSAEADDRINUSE**
</dt> <dd> <dl> <dt>

10048 (0x2740)
</dt> <dt>



Une seule utilisation de chaque adresse de socket (protocole/adresse réseau/port) est habituellement autorisée.


</dt> </dl> </dd> <dt>

<span id="WSAEADDRNOTAVAIL"></span><span id="wsaeaddrnotavail"></span>**WSAEADDRNOTAVAIL**
</dt> <dd> <dl> <dt>

10049 (0x2741)
</dt> <dt>



L’adresse demandée n’est pas valide dans son contexte.


</dt> </dl> </dd> <dt>

<span id="WSAENETDOWN"></span><span id="wsaenetdown"></span>**WSAENETDOWN**
</dt> <dd> <dl> <dt>

10050 (0x2742)
</dt> <dt>



Une opération de socket a rencontré un réseau inactif.


</dt> </dl> </dd> <dt>

<span id="WSAENETUNREACH"></span><span id="wsaenetunreach"></span>**WSAENETUNREACH**
</dt> <dd> <dl> <dt>

10051 (0x2743)
</dt> <dt>



Une opération de socket a été tentée sur un réseau inaccessible.


</dt> </dl> </dd> <dt>

<span id="WSAENETRESET"></span><span id="wsaenetreset"></span>**WSAENETRESET**
</dt> <dd> <dl> <dt>

10052 (0x2744)
</dt> <dt>



La connexion a été interrompue en raison d’une activité de maintien en état de la détection d’un échec pendant l’opération.


</dt> </dl> </dd> <dt>

<span id="WSAECONNABORTED"></span><span id="wsaeconnaborted"></span>**WSAECONNABORTED**
</dt> <dd> <dl> <dt>

10053 (0x2745)
</dt> <dt>



Une connexion établie a été abandonnée par un logiciel de votre ordinateur hôte.


</dt> </dl> </dd> <dt>

<span id="WSAECONNRESET"></span><span id="wsaeconnreset"></span>**WSAECONNRESET**
</dt> <dd> <dl> <dt>

10054 (0x2746)
</dt> <dt>



une connexion existante a dû être fermée par l’hôte distant.


</dt> </dl> </dd> <dt>

<span id="WSAENOBUFS"></span><span id="wsaenobufs"></span>**WSAENOBUFS**
</dt> <dd> <dl> <dt>

10055 (0x2747)
</dt> <dt>



Impossible d’effectuer une opération sur un socket en raison de l’insuffisance de l’espace de mémoire tampon du système ou de la saturation de la file d’attente.


</dt> </dl> </dd> <dt>

<span id="WSAEISCONN"></span><span id="wsaeisconn"></span>**WSAEISCONN**
</dt> <dd> <dl> <dt>

10056 (0x2748)
</dt> <dt>



Une demande de connexion a été effectuée sur un socket déjà connecté.


</dt> </dl> </dd> <dt>

<span id="WSAENOTCONN"></span><span id="wsaenotconn"></span>**WSAENOTCONN**
</dt> <dd> <dl> <dt>

10057 (0x2749)
</dt> <dt>



Une requête d'envoi ou de réception de données n'a pas été autorisée, car le socket n'est pas connecté et (lors de l'envoi sur un socket datagramme en utilisant un appel sendto) aucune adresse n'a été fournie.


</dt> </dl> </dd> <dt>

<span id="WSAESHUTDOWN"></span><span id="wsaeshutdown"></span>**WSAESHUTDOWN**
</dt> <dd> <dl> <dt>

10058 (0x274A)
</dt> <dt>



Une demande d'envoi ou de réception de données n'a pas été autorisée car le socket avait déjà été éteint dans cette direction par un appel d'arrêt précédent.


</dt> </dl> </dd> <dt>

<span id="WSAETOOMANYREFS"></span><span id="wsaetoomanyrefs"></span>**WSAETOOMANYREFS**
</dt> <dd> <dl> <dt>

10059 (0x274B)
</dt> <dt>



Trop de références à un objet de noyau.


</dt> </dl> </dd> <dt>

<span id="WSAETIMEDOUT"></span><span id="wsaetimedout"></span>**WSAETIMEDOUT**
</dt> <dd> <dl> <dt>

10060 (0x274C)
</dt> <dt>



Une tentative de connexion a échoué car le tiers connecté n’a pas répondu correctement après une certaine période, ou la connexion établie a échoué, car l’hôte connecté n’a pas pu répondre.


</dt> </dl> </dd> <dt>

<span id="WSAECONNREFUSED"></span><span id="wsaeconnrefused"></span>**WSAECONNREFUSED**
</dt> <dd> <dl> <dt>

10061 (0x274D)
</dt> <dt>



Aucune connexion n’a pu être établie car l’ordinateur cible l’a refusé activement.


</dt> </dl> </dd> <dt>

<span id="WSAELOOP"></span><span id="wsaeloop"></span>**WSAELOOP**
</dt> <dd> <dl> <dt>

10062 (0x274E)
</dt> <dt>



Impossible de traduire le nom.


</dt> </dl> </dd> <dt>

<span id="WSAENAMETOOLONG"></span><span id="wsaenametoolong"></span>**WSAENAMETOOLONG**
</dt> <dd> <dl> <dt>

10063 (0x274F)
</dt> <dt>



Le nom ou le composant du nom est trop long.


</dt> </dl> </dd> <dt>

<span id="WSAEHOSTDOWN"></span><span id="wsaehostdown"></span>**WSAEHOSTDOWN**
</dt> <dd> <dl> <dt>

10064 (0x2750)
</dt> <dt>



Une opération de socket a échoué, car l’ordinateur hôte de destination était en panne.


</dt> </dl> </dd> <dt>

<span id="WSAEHOSTUNREACH"></span><span id="wsaehostunreach"></span>**WSAEHOSTUNREACH**
</dt> <dd> <dl> <dt>

10065 (0x2751)
</dt> <dt>



Une opération de socket a été tentée sur un hôte impossible à atteindre.


</dt> </dl> </dd> <dt>

<span id="WSAENOTEMPTY"></span><span id="wsaenotempty"></span>**WSAENOTEMPTY**
</dt> <dd> <dl> <dt>

10066 (0x2752)
</dt> <dt>



Impossible de supprimer un répertoire qui n’est pas vide.


</dt> </dl> </dd> <dt>

<span id="WSAEPROCLIM"></span><span id="wsaeproclim"></span>**WSAEPROCLIM**
</dt> <dd> <dl> <dt>

10067 (0x2753)
</dt> <dt>



Une implémentation de Windows Sockets peut avoir une limite du nombre d’applications qui peuvent l’utiliser simultanément.


</dt> </dl> </dd> <dt>

<span id="WSAEUSERS"></span><span id="wsaeusers"></span>**WSAEUSERS**
</dt> <dd> <dl> <dt>

10068 (0x2754)
</dt> <dt>



Le quota est insuffisant.


</dt> </dl> </dd> <dt>

<span id="WSAEDQUOT"></span><span id="wsaedquot"></span>**WSAEDQUOT**
</dt> <dd> <dl> <dt>

10069 (0x2755)
</dt> <dt>



Le quota de disque est insuffisant.


</dt> </dl> </dd> <dt>

<span id="WSAESTALE"></span><span id="wsaestale"></span>**WSAESTALE**
</dt> <dd> <dl> <dt>

10070 (0x2756)
</dt> <dt>



La référence de descripteur de fichier n’est plus disponible.


</dt> </dl> </dd> <dt>

<span id="WSAEREMOTE"></span><span id="wsaeremote"></span>**WSAEREMOTE**
</dt> <dd> <dl> <dt>

10071 (0x2757)
</dt> <dt>



L’élément n’est pas disponible localement.


</dt> </dl> </dd> <dt>

<span id="WSASYSNOTREADY"></span><span id="wsasysnotready"></span>**WSASYSNOTREADY**
</dt> <dd> <dl> <dt>

10091 (0x276B)
</dt> <dt>



WSAStartup ne peut pas fonctionner pour l’instant, car le système sous-jacent qu’il utilise pour fournir des services réseau n’est pas disponible actuellement.


</dt> </dl> </dd> <dt>

<span id="WSAVERNOTSUPPORTED"></span><span id="wsavernotsupported"></span>**WSAVERNOTSUPPORTED**
</dt> <dd> <dl> <dt>

10092 (0x276C)
</dt> <dt>



La version de Windows Sockets demandée n’est pas prise en charge.


</dt> </dl> </dd> <dt>

<span id="WSANOTINITIALISED"></span><span id="wsanotinitialised"></span>**WSANOTINITIALISED**
</dt> <dd> <dl> <dt>

10093 (0x276D)
</dt> <dt>



Soit l’application n’a pas appelé WSAStartup, soit WSAStartup a échoué.


</dt> </dl> </dd> <dt>

<span id="WSAEDISCON"></span><span id="wsaediscon"></span>**WSAEDISCON**
</dt> <dd> <dl> <dt>

10101 (0x2775)
</dt> <dt>



Retourné par WSARecv ou WSARecvFrom pour indiquer que le tiers distant a initié une séquence d’arrêt appropriée.


</dt> </dl> </dd> <dt>

<span id="WSAENOMORE"></span><span id="wsaenomore"></span>**WSAENOMORE**
</dt> <dd> <dl> <dt>

10102 (0x2776)
</dt> <dt>



Aucun autre résultat ne peut être retourné par WSALookupServiceNext.


</dt> </dl> </dd> <dt>

<span id="WSAECANCELLED"></span><span id="wsaecancelled"></span>**WSAECANCELLED**
</dt> <dd> <dl> <dt>

10103 (0x2777)
</dt> <dt>



Un appel à WSALookupServiceEnd a été effectué alors que cet appel était toujours en cours de traitement. L’appel a été annulé.


</dt> </dl> </dd> <dt>

<span id="WSAEINVALIDPROCTABLE"></span><span id="wsaeinvalidproctable"></span>**WSAEINVALIDPROCTABLE**
</dt> <dd> <dl> <dt>

10104 (0x2778)
</dt> <dt>



La table des appels de procédure n’est pas valide.


</dt> </dl> </dd> <dt>

<span id="WSAEINVALIDPROVIDER"></span><span id="wsaeinvalidprovider"></span>**WSAEINVALIDPROVIDER**
</dt> <dd> <dl> <dt>

10105 (0x2779)
</dt> <dt>



Le fournisseur de services demandé n’est pas valide.


</dt> </dl> </dd> <dt>

<span id="WSAEPROVIDERFAILEDINIT"></span><span id="wsaeproviderfailedinit"></span>**WSAEPROVIDERFAILEDINIT**
</dt> <dd> <dl> <dt>

10106 (0x277A)
</dt> <dt>



Impossible de charger ou d’initialiser le fournisseur de services demandé.


</dt> </dl> </dd> <dt>

<span id="WSASYSCALLFAILURE"></span><span id="wsasyscallfailure"></span>**WSASYSCALLFAILURE**
</dt> <dd> <dl> <dt>

10107 (0x277B)
</dt> <dt>



Un appel système a échoué.


</dt> </dl> </dd> <dt>

<span id="WSASERVICE_NOT_FOUND"></span><span id="wsaservice_not_found"></span>**WSASERVICE \_ \_ introuvable**
</dt> <dd> <dl> <dt>

10108 (0x277C)
</dt> <dt>



Aucun service de ce type n’est connu. Le service est introuvable dans l’espace de noms spécifié.


</dt> </dl> </dd> <dt>

<span id="WSATYPE_NOT_FOUND"></span><span id="wsatype_not_found"></span>**WSATYPE \_ \_ introuvable**
</dt> <dd> <dl> <dt>

10109 (0x277D)
</dt> <dt>



La classe spécifiée est introuvable.


</dt> </dl> </dd> <dt>

<span id="WSA_E_NO_MORE"></span><span id="wsa_e_no_more"></span>**WSA \_ E \_ plus \_**
</dt> <dd> <dl> <dt>

10110 (0x277E)
</dt> <dt>



Aucun autre résultat ne peut être retourné par WSALookupServiceNext.


</dt> </dl> </dd> <dt>

<span id="WSA_E_CANCELLED"></span><span id="wsa_e_cancelled"></span>**WSA \_ E \_ annulée**
</dt> <dd> <dl> <dt>

10111 (0x277F)
</dt> <dt>



Un appel à WSALookupServiceEnd a été effectué alors que cet appel était toujours en cours de traitement. L’appel a été annulé.


</dt> </dl> </dd> <dt>

<span id="WSAEREFUSED"></span><span id="wsaerefused"></span>**WSAEREFUSED**
</dt> <dd> <dl> <dt>

10112 (0x2780)
</dt> <dt>



Une requête de base de données a échoué car elle a été refusée activement.


</dt> </dl> </dd> <dt>

<span id="WSAHOST_NOT_FOUND"></span><span id="wsahost_not_found"></span>**WSAHOST \_ \_ introuvable**
</dt> <dd> <dl> <dt>

11001 (0x2AF9)
</dt> <dt>



Hôte inconnu.


</dt> </dl> </dd> <dt>

<span id="WSATRY_AGAIN"></span><span id="wsatry_again"></span>**WSATRY \_ à nouveau**
</dt> <dd> <dl> <dt>

11002 (0x2AFA)
</dt> <dt>



Il s'agit habituellement d'une erreur temporaire qui se produit durant la résolution du nom d'hôte et qui signifie que le serveur local n'a pas reçu de réponse d'un serveur de référence.


</dt> </dl> </dd> <dt>

<span id="WSANO_RECOVERY"></span><span id="wsano_recovery"></span>**\_récupération WSANO**
</dt> <dd> <dl> <dt>

11003 (0x2AFB)
</dt> <dt>



Une erreur non récupérable s’est produite lors d’une recherche de base de données.


</dt> </dl> </dd> <dt>

<span id="WSANO_DATA"></span><span id="wsano_data"></span>**\_données WSANO**
</dt> <dd> <dl> <dt>

11004 (0x2AFC)
</dt> <dt>



Le nom demandé est valide, mais aucune donnée du type demandé n’a été trouvée.


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_RECEIVERS"></span><span id="wsa_qos_receivers"></span>**\_récepteurs de qualité de service WSA \_**
</dt> <dd> <dl> <dt>

11005 (0x2AFD)
</dt> <dt>



Au moins une réserve est arrivée.


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_SENDERS"></span><span id="wsa_qos_senders"></span>**\_expéditeurs de la QoS WSA \_**
</dt> <dd> <dl> <dt>

11006 (0x2AFE)
</dt> <dt>



Au moins un chemin d’accès est arrivé.


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_NO_SENDERS"></span><span id="wsa_qos_no_senders"></span>**\_non- \_ \_ expéditeurs de la QoS WSA**
</dt> <dd> <dl> <dt>

11007 (0x2AFF)
</dt> <dt>



Il n’y a pas d’expéditeurs.


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_NO_RECEIVERS"></span><span id="wsa_qos_no_receivers"></span>**\_non- \_ \_ destinataires de la QoS WSA**
</dt> <dd> <dl> <dt>

11008 (0x2B00)
</dt> <dt>



Il n’existe aucun destinataire.


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_REQUEST_CONFIRMED"></span><span id="wsa_qos_request_confirmed"></span>**\_demande de QoS WSA \_ \_ confirmée**
</dt> <dd> <dl> <dt>

11009 (0x2B01)
</dt> <dt>



La réserve a été confirmée.


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_ADMISSION_FAILURE"></span><span id="wsa_qos_admission_failure"></span>**échec d’admission de la \_ QoS WSA \_ \_**
</dt> <dd> <dl> <dt>

11010 (0x2B02)
</dt> <dt>



Erreur due à un manque de ressources.


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_POLICY_FAILURE"></span><span id="wsa_qos_policy_failure"></span>**échec de la \_ stratégie de QoS WSA \_ \_**
</dt> <dd> <dl> <dt>

11011 (0x2B03)
</dt> <dt>



Rejeté pour des raisons d’administration : informations d’identification incorrectes.


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_BAD_STYLE"></span><span id="wsa_qos_bad_style"></span>**STYLE de qualité de service WSA non \_ \_ valide \_**
</dt> <dd> <dl> <dt>

11012 (0x2B04)
</dt> <dt>



Style inconnu ou en conflit.


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_BAD_OBJECT"></span><span id="wsa_qos_bad_object"></span>**\_ \_ objet incorrect de la QoS WSA \_**
</dt> <dd> <dl> <dt>

11013 (0x2B05)
</dt> <dt>



Problème avec une partie de la mémoire tampon filterspec ou providerspecific en général.


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_TRAFFIC_CTRL_ERROR"></span><span id="wsa_qos_traffic_ctrl_error"></span>**\_erreur de \_ Ctrl pour le trafic de QoS WSA \_ \_**
</dt> <dd> <dl> <dt>

11014 (0x2B06)
</dt> <dt>



Problème avec une partie du flowspec.


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_GENERIC_ERROR"></span><span id="wsa_qos_generic_error"></span>**\_ \_ erreur générique de la QoS WSA \_**
</dt> <dd> <dl> <dt>

11015 (0x2B07)
</dt> <dt>



Erreur QOS générale.


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_ESERVICETYPE"></span><span id="wsa_qos_eservicetype"></span>**\_ESERVICETYPE de qualité de service WSA \_**
</dt> <dd> <dl> <dt>

11016 (0x2B08)
</dt> <dt>



Un type de service non valide ou non reconnu a été trouvé dans le flowspec.


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_EFLOWSPEC"></span><span id="wsa_qos_eflowspec"></span>**\_EFLOWSPEC de qualité de service WSA \_**
</dt> <dd> <dl> <dt>

11017 (0x2B09)
</dt> <dt>



Un flowspec non valide ou incohérent a été trouvé dans la structure QOS.


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_EPROVSPECBUF"></span><span id="wsa_qos_eprovspecbuf"></span>**\_EPROVSPECBUF de qualité de service WSA \_**
</dt> <dd> <dl> <dt>

11018 (0x2B0A)
</dt> <dt>



Mémoire tampon spécifique au fournisseur QOS non valide.


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_EFILTERSTYLE"></span><span id="wsa_qos_efilterstyle"></span>**\_EFILTERSTYLE de qualité de service WSA \_**
</dt> <dd> <dl> <dt>

11019 (0x2B0B)
</dt> <dt>



Un style de filtre QOS non valide a été utilisé.


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_EFILTERTYPE"></span><span id="wsa_qos_efiltertype"></span>**\_EFILTERTYPE de qualité de service WSA \_**
</dt> <dd> <dl> <dt>

11020 (0x2B0C)
</dt> <dt>



Un type de filtre QOS non valide a été utilisé.


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_EFILTERCOUNT"></span><span id="wsa_qos_efiltercount"></span>**\_EFILTERCOUNT de qualité de service WSA \_**
</dt> <dd> <dl> <dt>

11021 (0x2B0D)
</dt> <dt>



Un nombre incorrect de FILTERSPECs QOS a été spécifié dans le FLOWDESCRIPTOR.


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_EOBJLENGTH"></span><span id="wsa_qos_eobjlength"></span>**\_EOBJLENGTH de qualité de service WSA \_**
</dt> <dd> <dl> <dt>

11022 (0x2B0E)
</dt> <dt>



Un objet avec un champ ObjectLength non valide a été spécifié dans la mémoire tampon spécifique au fournisseur QOS.


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_EFLOWCOUNT"></span><span id="wsa_qos_eflowcount"></span>**\_EFLOWCOUNT de qualité de service WSA \_**
</dt> <dd> <dl> <dt>

11023 (0x2B0F)
</dt> <dt>



Un nombre incorrect de descripteurs de workflow a été spécifié dans la structure QOS.


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_EUNKOWNPSOBJ"></span><span id="wsa_qos_eunkownpsobj"></span>**\_EUNKOWNPSOBJ de qualité de service WSA \_**
</dt> <dd> <dl> <dt>

11024 (0x2B10)
</dt> <dt>



Un objet non reconnu a été trouvé dans la mémoire tampon spécifique au fournisseur QOS.


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_EPOLICYOBJ"></span><span id="wsa_qos_epolicyobj"></span>**\_EPOLICYOBJ de qualité de service WSA \_**
</dt> <dd> <dl> <dt>

11025 (0x2B11)
</dt> <dt>



Un objet de stratégie non valide a été trouvé dans la mémoire tampon spécifique au fournisseur QOS.


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_EFLOWDESC"></span><span id="wsa_qos_eflowdesc"></span>**\_EFLOWDESC de qualité de service WSA \_**
</dt> <dd> <dl> <dt>

11026 (0x2B12)
</dt> <dt>



Un descripteur de workflow QOS non valide a été trouvé dans la liste des descripteurs de Flow.


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_EPSFLOWSPEC"></span><span id="wsa_qos_epsflowspec"></span>**\_EPSFLOWSPEC de qualité de service WSA \_**
</dt> <dd> <dl> <dt>

11027 (0x2B13)
</dt> <dt>



Un flowspec non valide ou incohérent a été trouvé dans la mémoire tampon spécifique du fournisseur QOS.


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_EPSFILTERSPEC"></span><span id="wsa_qos_epsfilterspec"></span>**\_EPSFILTERSPEC de qualité de service WSA \_**
</dt> <dd> <dl> <dt>

11028 (0x2B14)
</dt> <dt>



Un FILTERSPEC non valide a été trouvé dans la mémoire tampon spécifique au fournisseur QOS.


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_ESDMODEOBJ"></span><span id="wsa_qos_esdmodeobj"></span>**\_ESDMODEOBJ de qualité de service WSA \_**
</dt> <dd> <dl> <dt>

11029 (0x2B15)
</dt> <dt>



Un objet de mode de suppression de forme non valide a été trouvé dans la mémoire tampon spécifique du fournisseur QOS.


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_ESHAPERATEOBJ"></span><span id="wsa_qos_eshaperateobj"></span>**\_ESHAPERATEOBJ de qualité de service WSA \_**
</dt> <dd> <dl> <dt>

11030 (0x2B16)
</dt> <dt>



Un objet de taux de mise en forme non valide a été trouvé dans la mémoire tampon spécifique au fournisseur QOS.


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_RESERVED_PETYPE"></span><span id="wsa_qos_reserved_petype"></span>**\_ \_ PETYPE réservée de la QoS WSA \_**
</dt> <dd> <dl> <dt>

11031 (0x2B17)
</dt> <dt>



Un élément de stratégie réservée a été trouvé dans la mémoire tampon spécifique au fournisseur QOS.


</dt> </dl> </dd> <dt>

<span id="WSA_SECURE_HOST_NOT_FOUND"></span><span id="wsa_secure_host_not_found"></span>**l' \_ hôte sécurisé WSA est \_ \_ \_ introuvable**
</dt> <dd> <dl> <dt>

11032 (0x2B18)
</dt> <dt>



Aucun hôte de ce type n’est connu en toute sécurité.


</dt> </dl> </dd> <dt>

<span id="WSA_IPSEC_NAME_POLICY_ERROR"></span><span id="wsa_ipsec_name_policy_error"></span>**\_erreur de \_ stratégie de nom d’IPSec WSA \_ \_**
</dt> <dd> <dl> <dt>

11033 (0x2B19)
</dt> <dt>



Impossible d’ajouter la stratégie IPSEC basée sur le nom.


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

 

 




