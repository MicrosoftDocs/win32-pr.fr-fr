---
description: Décrit les codes d’erreur 12000-1599 définis dans le fichier d’en-tête WinError. h et est destiné aux développeurs.
ms.assetid: bb3c658d-96db-495a-a0dc-e93949c3835d
title: Codes d’erreur système (12000-15999) (WinError. h)
ms.topic: reference
ms.date: 07/18/2019
ms.openlocfilehash: aa250eb26db3a2dfefda4c8b31bb2bbfd5e5d6415ea50d7279121fb09302c7ce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120058989"
---
# <a name="system-error-codes-12000-15999"></a>Codes d’erreur système (12000-15999)

> [!NOTE]
> Ces informations sont destinées aux développeurs qui déboguent les erreurs système. pour les autres erreurs, telles que les problèmes de Windows Update, il existe une liste de ressources dans la page [codes d’erreur](system-error-codes.md) .

La liste suivante décrit les [codes d’erreur système](system-error-codes.md) (erreurs 12000 à 15999). Elles sont retournées par la fonction [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) lorsque de nombreuses fonctions échouent. Pour récupérer le texte de description de l’erreur dans votre application, utilisez la fonction [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) avec le **format \_ message \_ de \_** l’indicateur système.

<dl> <dt>

<span id="ERROR_INTERNET__"></span><span id="error_internet__"></span>**ERREUR \_ Internet\_\***
</dt> <dd> <dl> <dt>

12000-12175 (0x2EE0)
</dt> <dt>



Consultez [codes d’erreur Internet](../wininet/wininet-errors.md) et wininet. h.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_QM_POLICY_EXISTS"></span><span id="error_ipsec_qm_policy_exists"></span>**ERREUR l’existence d’une \_ \_ stratégie de QM IPSec \_ \_**
</dt> <dd> <dl> <dt>

13000 (0x32C8)
</dt> <dt>



La stratégie de mode rapide spécifiée existe déjà.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_QM_POLICY_NOT_FOUND"></span><span id="error_ipsec_qm_policy_not_found"></span>**ERREUR \_ la \_ stratégie de QM IPSec est \_ \_ \_ introuvable**
</dt> <dd> <dl> <dt>

13001 (0x32C9)
</dt> <dt>



La stratégie de mode rapide spécifiée est introuvable.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_QM_POLICY_IN_USE"></span><span id="error_ipsec_qm_policy_in_use"></span>**ERREUR \_ \_ de la \_ stratégie de QM IPSec \_ en cours d' \_ utilisation**
</dt> <dd> <dl> <dt>

13002 (0x32CA)
</dt> <dt>



La stratégie de mode rapide spécifiée est utilisée.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_MM_POLICY_EXISTS"></span><span id="error_ipsec_mm_policy_exists"></span>**ERREUR \_ la \_ stratégie IPSec mm \_ \_ existe**
</dt> <dd> <dl> <dt>

13003 (0x32CB)
</dt> <dt>



La stratégie de mode principal spécifiée existe déjà.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_MM_POLICY_NOT_FOUND"></span><span id="error_ipsec_mm_policy_not_found"></span>**ERREUR \_ la \_ stratégie IPSec mm est \_ \_ \_ introuvable**
</dt> <dd> <dl> <dt>

13004 (0x32CC)
</dt> <dt>



La stratégie de mode principal spécifiée est introuvable.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_MM_POLICY_IN_USE"></span><span id="error_ipsec_mm_policy_in_use"></span>**ERREUR \_ \_ de la stratégie IPSec mm \_ \_ en cours d' \_ utilisation**
</dt> <dd> <dl> <dt>

13005 (0x32CD)
</dt> <dt>



La stratégie de mode principal spécifiée est en cours d’utilisation.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_MM_FILTER_EXISTS"></span><span id="error_ipsec_mm_filter_exists"></span>**ERREUR \_ le \_ filtre IPSec mm \_ \_ existe**
</dt> <dd> <dl> <dt>

13006 (0x32CE)
</dt> <dt>



Le filtre en mode principal spécifié existe déjà.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_MM_FILTER_NOT_FOUND"></span><span id="error_ipsec_mm_filter_not_found"></span>**ERREUR \_ de \_ filtre IPSec mm \_ \_ \_ introuvable**
</dt> <dd> <dl> <dt>

13007 (0x32CF)
</dt> <dt>



Le filtre de mode principal spécifié est introuvable.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_TRANSPORT_FILTER_EXISTS"></span><span id="error_ipsec_transport_filter_exists"></span>**ERREUR \_ le \_ filtre de transport IPSec \_ \_ existe**
</dt> <dd> <dl> <dt>

13008 (0x32D0)
</dt> <dt>



Le filtre de mode de transport spécifié existe déjà.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_TRANSPORT_FILTER_NOT_FOUND"></span><span id="error_ipsec_transport_filter_not_found"></span>**ERREUR \_ de \_ filtre de transport IPSec \_ \_ \_ introuvable**
</dt> <dd> <dl> <dt>

13009 (0x32D1)
</dt> <dt>



Le filtre de mode de transport spécifié n’existe pas.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_MM_AUTH_EXISTS"></span><span id="error_ipsec_mm_auth_exists"></span>**ERREUR \_ IPSec \_ mm \_ auth \_ existe**
</dt> <dd> <dl> <dt>

13010 (0x32D2)
</dt> <dt>



La liste d’authentification en mode principal spécifiée existe.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_MM_AUTH_NOT_FOUND"></span><span id="error_ipsec_mm_auth_not_found"></span>**ERREUR \_ IPSec \_ mm \_ auth \_ \_ introuvable**
</dt> <dd> <dl> <dt>

13011 (0x32D3)
</dt> <dt>



La liste d’authentification du mode principal spécifiée est introuvable.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_MM_AUTH_IN_USE"></span><span id="error_ipsec_mm_auth_in_use"></span>**ERREUR \_ IPSec \_ mm \_ auth \_ en cours d' \_ utilisation**
</dt> <dd> <dl> <dt>

13012 (0x32D4)
</dt> <dt>



La liste d’authentification en mode principal spécifiée est utilisée.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_DEFAULT_MM_POLICY_NOT_FOUND"></span><span id="error_ipsec_default_mm_policy_not_found"></span>**ERREUR \_ la \_ stratégie mm par défaut IPSec est \_ \_ \_ \_ introuvable**
</dt> <dd> <dl> <dt>

13013 (0x32D5)
</dt> <dt>



La stratégie de mode principal par défaut spécifiée est introuvable.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_DEFAULT_MM_AUTH_NOT_FOUND"></span><span id="error_ipsec_default_mm_auth_not_found"></span>**ERREUR \_ la \_ valeur par défaut de l' \_ authentification mm IPSec est \_ \_ \_ introuvable**
</dt> <dd> <dl> <dt>

13014 (0x32D6)
</dt> <dt>



La liste d’authentification du mode principal par défaut spécifiée est introuvable.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_DEFAULT_QM_POLICY_NOT_FOUND"></span><span id="error_ipsec_default_qm_policy_not_found"></span>**ERREUR \_ \_ stratégie de QM par défaut IPSec \_ \_ \_ non \_ trouvée**
</dt> <dd> <dl> <dt>

13015 (0x32D7)
</dt> <dt>



La stratégie de mode rapide par défaut spécifiée est introuvable.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_TUNNEL_FILTER_EXISTS"></span><span id="error_ipsec_tunnel_filter_exists"></span>**ERREUR \_ de \_ filtre de tunnel IPSec \_ \_**
</dt> <dd> <dl> <dt>

13016 (0x32D8)
</dt> <dt>



Le filtre de mode de tunnel spécifié existe.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_TUNNEL_FILTER_NOT_FOUND"></span><span id="error_ipsec_tunnel_filter_not_found"></span>**ERREUR \_ de \_ filtre de tunnel IPSec \_ \_ \_ introuvable**
</dt> <dd> <dl> <dt>

13017 (0x32D9)
</dt> <dt>



Le filtre de mode de tunnel spécifié est introuvable.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_MM_FILTER_PENDING_DELETION"></span><span id="error_ipsec_mm_filter_pending_deletion"></span>**ERREUR \_ de \_ \_ \_ suppression en attente du filtre IPSec mm \_**
</dt> <dd> <dl> <dt>

13018 (0x32DA)
</dt> <dt>



Le filtre en mode principal est en attente de suppression.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_TRANSPORT_FILTER_PENDING_DELETION"></span><span id="error_ipsec_transport_filter_pending_deletion"></span>**ERREUR \_ de \_ \_ \_ suppression en attente du filtre de transport IPSec \_**
</dt> <dd> <dl> <dt>

13019 (0x32DB)
</dt> <dt>



Le filtre de transport est en attente de suppression.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_TUNNEL_FILTER_PENDING_DELETION"></span><span id="error_ipsec_tunnel_filter_pending_deletion"></span>**ERREUR \_ de \_ \_ \_ suppression en attente du filtre de tunnel IPSec \_**
</dt> <dd> <dl> <dt>

13020 (0x32DC)
</dt> <dt>



Le filtre de tunnel est en attente de suppression.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_MM_POLICY_PENDING_DELETION"></span><span id="error_ipsec_mm_policy_pending_deletion"></span>**ERREUR \_ de \_ \_ \_ suppression en attente de la stratégie IPSec mm \_**
</dt> <dd> <dl> <dt>

13021 (0x32DD)
</dt> <dt>



La stratégie en mode principal est en attente de suppression.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_MM_AUTH_PENDING_DELETION"></span><span id="error_ipsec_mm_auth_pending_deletion"></span>**ERREUR \_ de \_ \_ \_ suppression en attente d’authentification IPSec mm \_**
</dt> <dd> <dl> <dt>

13022 (0x32DE)
</dt> <dt>



Le bundle d’authentification en mode principal est en attente de suppression.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_QM_POLICY_PENDING_DELETION"></span><span id="error_ipsec_qm_policy_pending_deletion"></span>**ERREUR \_ de \_ \_ \_ suppression en attente de la stratégie de QM IPSec \_**
</dt> <dd> <dl> <dt>

13023 (0x32DF)
</dt> <dt>



La stratégie de mode rapide est en attente de suppression.


</dt> </dl> </dd> <dt>

<span id="WARNING_IPSEC_MM_POLICY_PRUNED"></span><span id="warning_ipsec_mm_policy_pruned"></span>**Avertissement de la \_ \_ stratégie IPSec mm \_ \_ nettoyée**
</dt> <dd> <dl> <dt>

13024 (0x32E0)
</dt> <dt>



La stratégie en mode principal a été ajoutée avec succès, mais certaines des offres demandées ne sont pas prises en charge.


</dt> </dl> </dd> <dt>

<span id="WARNING_IPSEC_QM_POLICY_PRUNED"></span><span id="warning_ipsec_qm_policy_pruned"></span>**Avertissement de la \_ \_ stratégie de QM IPSec \_ \_ nettoyée**
</dt> <dd> <dl> <dt>

13025 (0x32E1)
</dt> <dt>



La stratégie de mode rapide a été ajoutée avec succès, mais certaines des offres demandées ne sont pas prises en charge.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_NEG_STATUS_BEGIN"></span><span id="error_ipsec_ike_neg_status_begin"></span>**ERREUR lors du démarrage de l’état de la \_ sécurité \_ Ike Ike \_ \_ \_**
</dt> <dd> <dl> <dt>

13800 (0x35E8)
</dt> <dt>



ERREUR lors du démarrage de l’état de la \_ sécurité \_ Ike Ike \_ \_ \_


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_AUTH_FAIL"></span><span id="error_ipsec_ike_auth_fail"></span>**ERREUR d’échec de l' \_ \_ authentification IKE IPSec \_ \_**
</dt> <dd> <dl> <dt>

13801 (0x35E9)
</dt> <dt>



Les informations d’authentification IKE ne sont pas acceptables.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_ATTRIB_FAIL"></span><span id="error_ipsec_ike_attrib_fail"></span>**ERREUR \_ d' \_ \_ échec d’attrib IKE IPSec \_**
</dt> <dd> <dl> <dt>

13802 (0x35EA)
</dt> <dt>



Les attributs de sécurité IKE ne sont pas acceptables.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_NEGOTIATION_PENDING"></span><span id="error_ipsec_ike_negotiation_pending"></span>**ERREUR \_ de \_ négociation IKE IPSec \_ \_ en attente**
</dt> <dd> <dl> <dt>

13803 (0x35EB)
</dt> <dt>



Négociation IKE en cours.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_GENERAL_PROCESSING_ERROR"></span><span id="error_ipsec_ike_general_processing_error"></span>**erreur \_ de \_ \_ traitement général \_ IKE \_ IPSec**
</dt> <dd> <dl> <dt>

13804 (0x35EC)
</dt> <dt>



Erreur de traitement général.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_TIMED_OUT"></span><span id="error_ipsec_ike_timed_out"></span>**ERREUR \_ IPSec \_ IKE \_ expiré \_**
</dt> <dd> <dl> <dt>

13805 (0x35ED)
</dt> <dt>



Expiration du délai d’attente de la négociation.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_NO_CERT"></span><span id="error_ipsec_ike_no_cert"></span>**ERREUR \_ IPSec \_ IKE \_ aucun \_ certificat**
</dt> <dd> <dl> <dt>

13806 (0x35EE)
</dt> <dt>



IKE n’a pas pu trouver un certificat d’ordinateur valide. Contactez votre administrateur de sécurité réseau pour installer un certificat valide dans le magasin de certificats approprié.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_SA_DELETED"></span><span id="error_ipsec_ike_sa_deleted"></span>**ERREUR \_ IPSec \_ IKE \_ sa \_ supprimée**
</dt> <dd> <dl> <dt>

13807 (0x35EF)
</dt> <dt>



SA IKE supprimée par l’homologue avant la fin de l’établissement.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_SA_REAPED"></span><span id="error_ipsec_ike_sa_reaped"></span>**ERREUR d' \_ Association de sécurité \_ Ike Ike \_ \_**
</dt> <dd> <dl> <dt>

13808 (0x35F0)
</dt> <dt>



SA IKE a été supprimée avant la fin de l’établissement.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_MM_ACQUIRE_DROP"></span><span id="error_ipsec_ike_mm_acquire_drop"></span>**ERREUR de suppression de l' \_ acquisition d’IPSec \_ IKE \_ mm \_ \_**
</dt> <dd> <dl> <dt>

13809 (0x35F1)
</dt> <dt>



La demande de négociation est restée trop longue dans la file d’attente.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_QM_ACQUIRE_DROP"></span><span id="error_ipsec_ike_qm_acquire_drop"></span>**ERREUR d’obtention de la suppression du \_ \_ QM IPsec IKE \_ \_ \_**
</dt> <dd> <dl> <dt>

13810 (0x35F2)
</dt> <dt>



La demande de négociation est restée trop longue dans la file d’attente.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_QUEUE_DROP_MM"></span><span id="error_ipsec_ike_queue_drop_mm"></span>**ERREUR \_ de \_ \_ Suppression de file d’attente IKE \_ IPSec \_**
</dt> <dd> <dl> <dt>

13811 (0x35F3)
</dt> <dt>



La demande de négociation est restée trop longue dans la file d’attente.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_QUEUE_DROP_NO_MM"></span><span id="error_ipsec_ike_queue_drop_no_mm"></span>**ERREUR de suppression de la \_ \_ \_ file d’attente IKE IPSec \_ \_ non \_ mm**
</dt> <dd> <dl> <dt>

13812 (0x35F4)
</dt> <dt>



La demande de négociation est restée trop longue dans la file d’attente.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_DROP_NO_RESPONSE"></span><span id="error_ipsec_ike_drop_no_response"></span>**ERREUR \_ de \_ Suppression d’absence de \_ réponse IPsec IKE \_ \_**
</dt> <dd> <dl> <dt>

13813 (0x35F5)
</dt> <dt>



Aucune réponse de l’homologue.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_MM_DELAY_DROP"></span><span id="error_ipsec_ike_mm_delay_drop"></span>**ERREUR \_ de \_ \_ \_ suppression différée IPsec IKE mm \_**
</dt> <dd> <dl> <dt>

13814 (0x35F6)
</dt> <dt>



La négociation a pris trop de temps.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_QM_DELAY_DROP"></span><span id="error_ipsec_ike_qm_delay_drop"></span>**ERREUR \_ de \_ \_ suppression du délai de QM IKE \_ IPSec \_**
</dt> <dd> <dl> <dt>

13815 (0x35F7)
</dt> <dt>



La négociation a pris trop de temps.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_ERROR"></span><span id="error_ipsec_ike_error"></span>**erreur \_ IPSec \_ IKE \_**
</dt> <dd> <dl> <dt>

13816 (0x35F8)
</dt> <dt>



Une erreur inconnue s’est produite.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_CRL_FAILED"></span><span id="error_ipsec_ike_crl_failed"></span>**ERREUR \_ \_ \_ échec de la liste de révocation de certificats IKE IPSec \_**
</dt> <dd> <dl> <dt>

13817 (0x35F9)
</dt> <dt>



Échec de la vérification de la révocation des certificats.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_KEY_USAGE"></span><span id="error_ipsec_ike_invalid_key_usage"></span>**ERREUR d’utilisation de la \_ \_ \_ clé non valide IPsec IKE \_ \_**
</dt> <dd> <dl> <dt>

13818 (0x35FA)
</dt> <dt>



Utilisation de clé de certificat non valide.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_CERT_TYPE"></span><span id="error_ipsec_ike_invalid_cert_type"></span>**ERREUR \_ de \_ \_ type de \_ certificat non valide IPsec IKE \_**
</dt> <dd> <dl> <dt>

13819 (0x35FB)
</dt> <dt>



Type de certificat non valide.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_NO_PRIVATE_KEY"></span><span id="error_ipsec_ike_no_private_key"></span>**ERREUR \_ IPSec \_ IKE \_ sans \_ \_ clé privée**
</dt> <dd> <dl> <dt>

13820 (0x35FC)
</dt> <dt>



La négociation IKE a échoué, car le certificat de l’ordinateur utilisé n’a pas de clé privée. Les certificats IPsec nécessitent une clé privée. Contactez votre administrateur de sécurité réseau pour remplacer par un certificat qui a une clé privée.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_SIMULTANEOUS_REKEY"></span><span id="error_ipsec_ike_simultaneous_rekey"></span>**ERREUR \_ de \_ \_ régénération simultanée d’IPsec IKE \_**
</dt> <dd> <dl> <dt>

13821 (0x35FD)
</dt> <dt>



Des retouches simultanées ont été détectées.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_DH_FAIL"></span><span id="error_ipsec_ike_dh_fail"></span>**ERREUR \_ IPSec \_ IKE \_ DH \_ échoue**
</dt> <dd> <dl> <dt>

13822 (0x35FE)
</dt> <dt>



Échec dans le calcul de la Diffie-Hellman.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_CRITICAL_PAYLOAD_NOT_RECOGNIZED"></span><span id="error_ipsec_ike_critical_payload_not_recognized"></span>**ERREUR \_ de \_ \_ charge utile critique IKE IPSec \_ \_ non \_ reconnue**
</dt> <dd> <dl> <dt>

13823 (0x35FF)
</dt> <dt>



Je ne sais pas comment traiter la charge utile critique.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_HEADER"></span><span id="error_ipsec_ike_invalid_header"></span>**ERREUR \_ d' \_ \_ \_ en-tête IPsec IKE non valide**
</dt> <dd> <dl> <dt>

13824 (0x3600)
</dt> <dt>



En-tête non valide.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_NO_POLICY"></span><span id="error_ipsec_ike_no_policy"></span>**ERREUR \_ IPSec \_ IKE \_ aucune \_ stratégie**
</dt> <dd> <dl> <dt>

13825 (0x3601)
</dt> <dt>



Aucune stratégie n’est configurée.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_SIGNATURE"></span><span id="error_ipsec_ike_invalid_signature"></span>**ERREUR \_ de \_ signature IPsec IKE \_ non valide \_**
</dt> <dd> <dl> <dt>

13826 (0x3602)
</dt> <dt>



Impossible de vérifier la signature.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_KERBEROS_ERROR"></span><span id="error_ipsec_ike_kerberos_error"></span>**erreur \_ IPSec \_ IKE \_ IKE \_**
</dt> <dd> <dl> <dt>

13827 (0x3603)
</dt> <dt>



Échec de l’authentification à l’aide de Kerberos.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_NO_PUBLIC_KEY"></span><span id="error_ipsec_ike_no_public_key"></span>**ERREUR \_ IPSec \_ IKE \_ aucune \_ \_ clé publique**
</dt> <dd> <dl> <dt>

13828 (0x3604)
</dt> <dt>



Le certificat de l’homologue n’a pas de clé publique.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_PROCESS_ERR"></span><span id="error_ipsec_ike_process_err"></span>**ERREUR \_ de \_ processus IKE IPSec \_ \_**
</dt> <dd> <dl> <dt>

13829 (0x3605)
</dt> <dt>



Erreur lors du traitement de la charge utile.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_PROCESS_ERR_SA"></span><span id="error_ipsec_ike_process_err_sa"></span>**ERREUR \_ du \_ processus Ike Ike de l' \_ \_ \_ Association de sécurité**
</dt> <dd> <dl> <dt>

13830 (0x3606)
</dt> <dt>



Erreur lors du traitement de la charge de SA.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_PROCESS_ERR_PROP"></span><span id="error_ipsec_ike_process_err_prop"></span>**erreur de traitement de l’erreur du \_ \_ processus IKE IPSec \_ \_ \_**
</dt> <dd> <dl> <dt>

13831 (0x3607)
</dt> <dt>



Erreur lors du traitement de la charge utile de la proposition.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_PROCESS_ERR_TRANS"></span><span id="error_ipsec_ike_process_err_trans"></span>**ERREUR \_ de \_ \_ transfert de processus IKE \_ IPSec \_**
</dt> <dd> <dl> <dt>

13832 (0x3608)
</dt> <dt>



Erreur lors du traitement de la charge utile de transformation.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_PROCESS_ERR_KE"></span><span id="error_ipsec_ike_process_err_ke"></span>**erreur \_ de \_ \_ processus IKE \_ IKE \_ de l’erreur**
</dt> <dd> <dl> <dt>

13833 (0x3609)
</dt> <dt>



Erreur lors du traitement de la charge utile.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_PROCESS_ERR_ID"></span><span id="error_ipsec_ike_process_err_id"></span>**erreur ID d’erreur du \_ \_ processus IKE IPSec \_ \_ \_**
</dt> <dd> <dl> <dt>

13834 (0x360A)
</dt> <dt>



Erreur lors du traitement de la charge utile de l’ID.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_PROCESS_ERR_CERT"></span><span id="error_ipsec_ike_process_err_cert"></span>**erreur de certificat d’erreur de \_ \_ processus IKE IPSec \_ \_ \_**
</dt> <dd> <dl> <dt>

13835 (0x360B)
</dt> <dt>



Erreur lors du traitement de la charge utile du certificat.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_PROCESS_ERR_CERT_REQ"></span><span id="error_ipsec_ike_process_err_cert_req"></span>**ERREUR \_ de \_ \_ certificat du processus Ike Ike \_ \_ de \_ l’erreur**
</dt> <dd> <dl> <dt>

13836 (0x360C)
</dt> <dt>



Erreur lors du traitement de la charge utile de la demande de certificat.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_PROCESS_ERR_HASH"></span><span id="error_ipsec_ike_process_err_hash"></span>**ERREUR \_ de \_ \_ hachage d’Err de processus IKE \_ IPSec \_**
</dt> <dd> <dl> <dt>

13837 (0x360D)
</dt> <dt>



Erreur lors du traitement de la charge utile de hachage.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_PROCESS_ERR_SIG"></span><span id="error_ipsec_ike_process_err_sig"></span>**erreur d’erreur du \_ \_ processus IKE IPSec \_ \_ \_**
</dt> <dd> <dl> <dt>

13838 (0x360E)
</dt> <dt>



Erreur lors du traitement de la charge utile de la signature.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_PROCESS_ERR_NONCE"></span><span id="error_ipsec_ike_process_err_nonce"></span>**ERREUR de la valeur à usage \_ \_ unique du processus IKE IPSec \_ \_ \_**
</dt> <dd> <dl> <dt>

13839 (0x360F)
</dt> <dt>



Erreur lors du traitement de la charge à usage unique.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_PROCESS_ERR_NOTIFY"></span><span id="error_ipsec_ike_process_err_notify"></span>**erreur de traitement de l’erreur du \_ \_ processus IKE IPSec \_ \_ \_**
</dt> <dd> <dl> <dt>

13840 (0x3610)
</dt> <dt>



Erreur lors du traitement de la charge utile de notification.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_PROCESS_ERR_DELETE"></span><span id="error_ipsec_ike_process_err_delete"></span>**ERREUR de suppression de l' \_ \_ Err du processus IKE IPSec \_ \_ \_**
</dt> <dd> <dl> <dt>

13841 (0x3611)
</dt> <dt>



Erreur lors du traitement de la charge utile de suppression.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_PROCESS_ERR_VENDOR"></span><span id="error_ipsec_ike_process_err_vendor"></span>**erreur fournisseur d’erreur de \_ \_ processus IKE IPSec \_ \_ \_**
</dt> <dd> <dl> <dt>

13842 (0x3612)
</dt> <dt>



Erreur lors du traitement de la charge du ID de message.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_PAYLOAD"></span><span id="error_ipsec_ike_invalid_payload"></span>**ERREUR \_ IPSec \_ IKE \_ non valide \_**
</dt> <dd> <dl> <dt>

13843 (0x3613)
</dt> <dt>



Charge utile non valide reçue.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_LOAD_SOFT_SA"></span><span id="error_ipsec_ike_load_soft_sa"></span>**ERREUR de chargement de la \_ \_ \_ \_ \_ sa logicielle IPsec IKE**
</dt> <dd> <dl> <dt>

13844 (0x3614)
</dt> <dt>



SA logicielle chargée.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_SOFT_SA_TORN_DOWN"></span><span id="error_ipsec_ike_soft_sa_torn_down"></span>**ERREUR \_ d' \_ Association de sécurité logicielle Ike Ike \_ \_ \_ endommagée \_**
</dt> <dd> <dl> <dt>

13845 (0x3615)
</dt> <dt>



SA détruite.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_COOKIE"></span><span id="error_ipsec_ike_invalid_cookie"></span>**ERREUR \_ de \_ cookie IPsec IKE \_ non valide \_**
</dt> <dd> <dl> <dt>

13846 (0x3616)
</dt> <dt>



Cookie non valide reçu.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_NO_PEER_CERT"></span><span id="error_ipsec_ike_no_peer_cert"></span>**ERREUR \_ IPSec \_ IKE \_ aucun \_ certificat homologue \_**
</dt> <dd> <dl> <dt>

13847 (0x3617)
</dt> <dt>



L’homologue n’a pas pu envoyer un certificat d’ordinateur valide.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_PEER_CRL_FAILED"></span><span id="error_ipsec_ike_peer_crl_failed"></span>**ERREUR \_ \_ \_ \_ échec de la liste de révocation de certificats homologues IKE IPSec \_**
</dt> <dd> <dl> <dt>

13848 (0x3618)
</dt> <dt>



Échec de la vérification de la révocation de certification du certificat de l’homologue.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_POLICY_CHANGE"></span><span id="error_ipsec_ike_policy_change"></span>**ERREUR de modification de la \_ \_ stratégie IKE IPSec \_ \_**
</dt> <dd> <dl> <dt>

13849 (0x3619)
</dt> <dt>



Nouvelle stratégie non validée par une SAP formée avec l’ancienne stratégie.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_NO_MM_POLICY"></span><span id="error_ipsec_ike_no_mm_policy"></span>**ERREUR \_ \_ stratégie IPsec IKE \_ non \_ mm \_**
</dt> <dd> <dl> <dt>

13850 (0x361A)
</dt> <dt>



Il n’existe aucune stratégie IKE en mode principal disponible.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_NOTCBPRIV"></span><span id="error_ipsec_ike_notcbpriv"></span>**ERREUR \_ IPSec \_ IKE \_ NOTCBPRIV**
</dt> <dd> <dl> <dt>

13851 (0x361B)
</dt> <dt>



Échec de l’activation du privilège TCB.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_SECLOADFAIL"></span><span id="error_ipsec_ike_secloadfail"></span>**ERREUR \_ IPSec \_ IKE \_ SECLOADFAIL**
</dt> <dd> <dl> <dt>

13852 (0x361C)
</dt> <dt>



Impossible de charger SECURITY.DLL.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_FAILSSPINIT"></span><span id="error_ipsec_ike_failsspinit"></span>**ERREUR \_ IPSec \_ IKE \_ FAILSSPINIT**
</dt> <dd> <dl> <dt>

13853 (0x361D)
</dt> <dt>



Échec de l’obtention de l’adresse de distribution de la table de fonctions de sécurité à partir de SSPI.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_FAILQUERYSSP"></span><span id="error_ipsec_ike_failqueryssp"></span>**ERREUR \_ IPSec \_ IKE \_ FAILQUERYSSP**
</dt> <dd> <dl> <dt>

13854 (0x361E)
</dt> <dt>



Impossible d’interroger le package Kerberos pour obtenir la taille de jeton maximale.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_SRVACQFAIL"></span><span id="error_ipsec_ike_srvacqfail"></span>**ERREUR \_ IPSec \_ IKE \_ SRVACQFAIL**
</dt> <dd> <dl> <dt>

13855 (0x361F)
</dt> <dt>



Échec de l’obtention des informations d’identification du serveur Kerberos pour le service IKE/d’erreur ISAKMP/ERROR \_ \_ . L’authentification Kerberos ne fonctionnera pas. La raison la plus probable de ce problème est l’absence d’appartenance au domaine. Cela est normal si votre ordinateur est membre d’un groupe de travail.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_SRVQUERYCRED"></span><span id="error_ipsec_ike_srvquerycred"></span>**ERREUR \_ IPSec \_ IKE \_ SRVQUERYCRED**
</dt> <dd> <dl> <dt>

13856 (0x3620)
</dt> <dt>



Impossible de déterminer le nom principal SSPI pour le \_ service IKE/erreur IPSec \_ IKE ([**QueryCredentialsAttributes**](/windows/win32/api/sspi/nf-sspi-querycredentialsattributesa)).


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_GETSPIFAIL"></span><span id="error_ipsec_ike_getspifail"></span>**ERREUR \_ IPSec \_ IKE \_ GETSPIFAIL**
</dt> <dd> <dl> <dt>

13857 (0x3621)
</dt> <dt>



Échec de l’obtention du nouveau SPI pour la SA entrante à partir du pilote IPsec. La cause la plus courante est que le pilote n’a pas le bon filtre. Vérifiez votre stratégie pour vérifier les filtres.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_FILTER"></span><span id="error_ipsec_ike_invalid_filter"></span>**ERREUR \_ de \_ \_ filtre non valide IPsec IKE \_**
</dt> <dd> <dl> <dt>

13858 (0x3622)
</dt> <dt>



Le filtre spécifié n’est pas valide.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_OUT_OF_MEMORY"></span><span id="error_ipsec_ike_out_of_memory"></span>**ERREUR \_ \_ \_ \_ de \_ mémoire insuffisante IPsec IKE**
</dt> <dd> <dl> <dt>

13859 (0x3623)
</dt> <dt>



L'allocation de mémoire a échoué.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_ADD_UPDATE_KEY_FAILED"></span><span id="error_ipsec_ike_add_update_key_failed"></span>**ERREUR Échec de l’ajout de la \_ \_ \_ clé de \_ mise à jour IPSec \_ IKE \_**
</dt> <dd> <dl> <dt>

13860 (0x3624)
</dt> <dt>



Échec de l’ajout de l’Association de sécurité au pilote IPsec. La cause la plus courante est que la négociation IKE a mis trop de temps à se terminer. Si le problème persiste, réduisez la charge sur l’ordinateur défaillant.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_POLICY"></span><span id="error_ipsec_ike_invalid_policy"></span>**ERREUR \_ de \_ \_ stratégie non valide IPsec IKE \_**
</dt> <dd> <dl> <dt>

13861 (0x3625)
</dt> <dt>



Stratégie non valide.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_UNKNOWN_DOI"></span><span id="error_ipsec_ike_unknown_doi"></span>**ERREUR \_ IPSec \_ IKE \_ inconnu \_**
</dt> <dd> <dl> <dt>

13862 (0x3626)
</dt> <dt>



DOI non valide.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_SITUATION"></span><span id="error_ipsec_ike_invalid_situation"></span>**ERREUR \_ IPSec \_ IKE \_ non valide \_**
</dt> <dd> <dl> <dt>

13863 (0x3627)
</dt> <dt>



Situation non valide.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_DH_FAILURE"></span><span id="error_ipsec_ike_dh_failure"></span>**ERREUR \_ IPSec \_ IKE \_ DH \_**
</dt> <dd> <dl> <dt>

13864 (0x3628)
</dt> <dt>



Échec de la Diffie-Hellman.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_GROUP"></span><span id="error_ipsec_ike_invalid_group"></span>**ERREUR \_ de \_ \_ groupe non valide IPsec IKE \_**
</dt> <dd> <dl> <dt>

13865 (0x3629)
</dt> <dt>



Groupe de Diffie-Hellman non valide.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_ENCRYPT"></span><span id="error_ipsec_ike_encrypt"></span>**ERREUR \_ de \_ \_ chiffrement IKE IPSec**
</dt> <dd> <dl> <dt>

13866 (0x362A)
</dt> <dt>



Erreur lors du chiffrement de la charge utile.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_DECRYPT"></span><span id="error_ipsec_ike_decrypt"></span>**ERREUR \_ de \_ \_ déchiffrement IKE IPSec**
</dt> <dd> <dl> <dt>

13867 (0x362B)
</dt> <dt>



Erreur lors du déchiffrement de la charge utile.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_POLICY_MATCH"></span><span id="error_ipsec_ike_policy_match"></span>**ERREUR de correspondance de la \_ \_ stratégie IKE IPSec \_ \_**
</dt> <dd> <dl> <dt>

13868 (0x362C)
</dt> <dt>



Erreur de correspondance de stratégie.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_UNSUPPORTED_ID"></span><span id="error_ipsec_ike_unsupported_id"></span>**ERREUR \_ \_ \_ ID non pris en charge IPSec IKE \_**
</dt> <dd> <dl> <dt>

13869 (0x362D)
</dt> <dt>



ID non pris en charge.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_HASH"></span><span id="error_ipsec_ike_invalid_hash"></span>**ERREUR \_ de \_ \_ hachage non valide IPsec IKE \_**
</dt> <dd> <dl> <dt>

13870 (0x362E)
</dt> <dt>



Échec de la vérification du hachage.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_HASH_ALG"></span><span id="error_ipsec_ike_invalid_hash_alg"></span>**ERREUR \_ IPSec \_ IKE \_ \_ hash \_ ALG non valide**
</dt> <dd> <dl> <dt>

13871 (0x362F)
</dt> <dt>



Algorithme de hachage non valide.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_HASH_SIZE"></span><span id="error_ipsec_ike_invalid_hash_size"></span>**ERREUR \_ IPSec \_ IKE \_ - \_ taille de hachage non valide \_**
</dt> <dd> <dl> <dt>

13872 (0x3630)
</dt> <dt>



Taille de hachage non valide.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_ENCRYPT_ALG"></span><span id="error_ipsec_ike_invalid_encrypt_alg"></span>**ERREUR \_ IPSec \_ IKE \_ \_ chiffrement non valide \_ ALG**
</dt> <dd> <dl> <dt>

13873 (0x3631)
</dt> <dt>



Algorithme de chiffrement non valide.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_AUTH_ALG"></span><span id="error_ipsec_ike_invalid_auth_alg"></span>**ERREUR \_ IPSec \_ IKE \_ - \_ authentification non valide \_ ALG**
</dt> <dd> <dl> <dt>

13874 (0x3632)
</dt> <dt>



Algorithme d’authentification non valide.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_SIG"></span><span id="error_ipsec_ike_invalid_sig"></span>**ERREUR \_ IPSec \_ IKE \_ non valide \_ SIG**
</dt> <dd> <dl> <dt>

13875 (0x3633)
</dt> <dt>



Signature de certificat non valide.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_LOAD_FAILED"></span><span id="error_ipsec_ike_load_failed"></span>**ERREUR \_ \_ échec du \_ chargement \_ IKE IPSec**
</dt> <dd> <dl> <dt>

13876 (0x3634)
</dt> <dt>



Échec du chargement.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_RPC_DELETE"></span><span id="error_ipsec_ike_rpc_delete"></span>**ERREUR \_ IPSec \_ IKE \_ RPC \_ Delete**
</dt> <dd> <dl> <dt>

13877 (0x3635)
</dt> <dt>



Supprimé par le biais de l’appel RPC.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_BENIGN_REINIT"></span><span id="error_ipsec_ike_benign_reinit"></span>**ERREUR \_ IPSec \_ IKE \_ Bénin- \_ Réinit**
</dt> <dd> <dl> <dt>

13878 (0x3636)
</dt> <dt>



État temporaire créé pour effectuer la réinitialisation. Il ne s’agit pas d’une défaillance réelle.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_RESPONDER_LIFETIME_NOTIFY"></span><span id="error_ipsec_ike_invalid_responder_lifetime_notify"></span>**ERREUR \_ de \_ durée \_ de \_ vie du répondeur non valide IPsec IKE \_ \_**
</dt> <dd> <dl> <dt>

13879 (0x3637)
</dt> <dt>



la valeur de durée de vie reçue dans la notification de durée de vie du répondeur est inférieure à la valeur minimale configurée Windows 2000. Corrigez la stratégie sur l’ordinateur homologue.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_MAJOR_VERSION"></span><span id="error_ipsec_ike_invalid_major_version"></span>**ERREUR \_ IPSec \_ IKE \_ \_ version majeure non valide \_**
</dt> <dd> <dl> <dt>

13880 (0x3638)
</dt> <dt>



Le destinataire ne peut pas gérer la version d’IKE spécifiée dans l’en-tête.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_CERT_KEYLEN"></span><span id="error_ipsec_ike_invalid_cert_keylen"></span>**ERREUR \_ IPSec \_ IKE \_ certificat non valide \_ \_ KEYLEN**
</dt> <dd> <dl> <dt>

13881 (0x3639)
</dt> <dt>



La longueur de clé dans le certificat est trop petite pour les exigences de sécurité configurées.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_MM_LIMIT"></span><span id="error_ipsec_ike_mm_limit"></span>**ERREUR \_ de \_ limite IPsec IKE \_ mm \_**
</dt> <dd> <dl> <dt>

13882 (0x363A)
</dt> <dt>



Le nombre maximal de MM SAs établies à l’homologue est dépassé.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_NEGOTIATION_DISABLED"></span><span id="error_ipsec_ike_negotiation_disabled"></span>**ERREUR \_ de \_ négociation IKE IPSec \_ \_ désactivée**
</dt> <dd> <dl> <dt>

13883 (0x363B)
</dt> <dt>



IKE a reçu une stratégie qui désactive la négociation.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_QM_LIMIT"></span><span id="error_ipsec_ike_qm_limit"></span>**ERREUR de la \_ \_ limite de QM IKE IPSec \_ \_**
</dt> <dd> <dl> <dt>

13884 (0x363C)
</dt> <dt>



Limite maximale du mode rapide atteinte pour le mode principal. Le nouveau mode principal démarrera.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_MM_EXPIRED"></span><span id="error_ipsec_ike_mm_expired"></span>**ERREUR \_ IPSec \_ IKE \_ mm \_ expiré**
</dt> <dd> <dl> <dt>

13885 (0x363D)
</dt> <dt>



Durée de vie de la SA de mode principal expirée ou l’homologue a envoyé une suppression en mode principal.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_PEER_MM_ASSUMED_INVALID"></span><span id="error_ipsec_ike_peer_mm_assumed_invalid"></span>**ERREUR \_ IPSec \_ IKE \_ pair \_ mm \_ pris en défaut \_**
</dt> <dd> <dl> <dt>

13886 (0x363E)
</dt> <dt>



La SA de mode principal est supposée être non valide, car l’homologue a cessé de répondre.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_CERT_CHAIN_POLICY_MISMATCH"></span><span id="error_ipsec_ike_cert_chain_policy_mismatch"></span>**ERREUR \_ d' \_ \_ \_ \_ incompatibilité de stratégie de chaîne de certificats IKE IPSec \_**
</dt> <dd> <dl> <dt>

13887 (0x363F)
</dt> <dt>



Le certificat n’est pas lié à une racine approuvée dans la stratégie IPsec.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_UNEXPECTED_MESSAGE_ID"></span><span id="error_ipsec_ike_unexpected_message_id"></span>**ERREUR \_ d' \_ \_ ID de \_ message \_ inattendu IPsec IKE**
</dt> <dd> <dl> <dt>

13888 (0x3640)
</dt> <dt>



Réception d’un ID de message inattendu.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_AUTH_PAYLOAD"></span><span id="error_ipsec_ike_invalid_auth_payload"></span>**ERREUR \_ IPSec \_ IKE \_ - \_ charge d’authentification non valide \_**
</dt> <dd> <dl> <dt>

13889 (0x3641)
</dt> <dt>



Offres d’authentification non valides reçues.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_DOS_COOKIE_SENT"></span><span id="error_ipsec_ike_dos_cookie_sent"></span>**ERREUR \_ de \_ \_ cookie dos IKE IPSec \_ \_ envoyé**
</dt> <dd> <dl> <dt>

13890 (0x3642)
</dt> <dt>



Envoi d’une notification de cookie DoS à l’initiateur.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_SHUTTING_DOWN"></span><span id="error_ipsec_ike_shutting_down"></span>**ERREUR \_ IPsec IKE en cours d' \_ \_ arrêt \_**
</dt> <dd> <dl> <dt>

13891 (0x3643)
</dt> <dt>



Arrêt du service IKE en cours.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_CGA_AUTH_FAILED"></span><span id="error_ipsec_ike_cga_auth_failed"></span>**ERREUR d’échec de l' \_ \_ authentification du CGA IPsec IKE \_ \_ \_**
</dt> <dd> <dl> <dt>

13892 (0x3644)
</dt> <dt>



Impossible de vérifier la liaison entre l’adresse CGA et le certificat.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_PROCESS_ERR_NATOA"></span><span id="error_ipsec_ike_process_err_natoa"></span>**ERREUR \_ de \_ processus IKE IPSec- \_ \_ \_ OTAN**
</dt> <dd> <dl> <dt>

13893 (0x3645)
</dt> <dt>



Erreur lors du traitement de la charge de l’Otana.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_MM_FOR_QM"></span><span id="error_ipsec_ike_invalid_mm_for_qm"></span>**ERREUR \_ IPSec \_ IKE \_ non valide \_ mm \_ pour \_ QM**
</dt> <dd> <dl> <dt>

13894 (0x3646)
</dt> <dt>



Les paramètres du mode principal ne sont pas valides pour ce mode rapide.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_QM_EXPIRED"></span><span id="error_ipsec_ike_qm_expired"></span>**ERREUR \_ IPSec \_ IKE \_ QM \_ expiré**
</dt> <dd> <dl> <dt>

13895 (0x3647)
</dt> <dt>



La SA du mode rapide a expiré par le pilote IPsec.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_TOO_MANY_FILTERS"></span><span id="error_ipsec_ike_too_many_filters"></span>**ERREUR \_ IPSec \_ IKE \_ trop \_ grand nombre de \_ filtres**
</dt> <dd> <dl> <dt>

13896 (0x3648)
</dt> <dt>



Un trop grand nombre de filtres IKEEXT ajoutés dynamiquement ont été détectés.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_NEG_STATUS_END"></span><span id="error_ipsec_ike_neg_status_end"></span>**ERREUR de fin d’état de la \_ sécurité \_ Ike Ike IPSec \_ \_ \_**
</dt> <dd> <dl> <dt>

13897 (0x3649)
</dt> <dt>



ERREUR de fin d’état de la \_ sécurité \_ Ike Ike IPSec \_ \_ \_


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_KILL_DUMMY_NAP_TUNNEL"></span><span id="error_ipsec_ike_kill_dummy_nap_tunnel"></span>**ERREUR \_ IPSec \_ IKE- \_ supprimer le \_ \_ tunnel NAP factice \_**
</dt> <dd> <dl> <dt>

13898 (0x364A)
</dt> <dt>



La réauthentification NAP a réussi et doit supprimer le tunnel IKEv2 NAP factice.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INNER_IP_ASSIGNMENT_FAILURE"></span><span id="error_ipsec_ike_inner_ip_assignment_failure"></span>**ERREUR d’affectation de l' \_ \_ \_ \_ adresse IP interne \_ Ike Ike \_**
</dt> <dd> <dl> <dt>

13899 (0x364B)
</dt> <dt>



Erreur lors de l’affectation de l’adresse IP interne à l’initiateur en mode tunnel.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_REQUIRE_CP_PAYLOAD_MISSING"></span><span id="error_ipsec_ike_require_cp_payload_missing"></span>**ERREUR \_ IPSec \_ IKE \_ exiger \_ une \_ charge utile CP \_ manquante**
</dt> <dd> <dl> <dt>

13900 (0x364C)
</dt> <dt>



La charge utile de configuration requise est manquante.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_KEY_MODULE_IMPERSONATION_NEGOTIATION_PENDING"></span><span id="error_ipsec_key_module_impersonation_negotiation_pending"></span>**ERREUR \_ de \_ négociation d’emprunt d’identité du module de clé IPSec \_ \_ \_ \_ en attente**
</dt> <dd> <dl> <dt>

13901 (0x364D)
</dt> <dt>



Une négociation s’exécutant comme principe de sécurité qui a émis la connexion est en cours.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_COEXISTENCE_SUPPRESS"></span><span id="error_ipsec_ike_coexistence_suppress"></span>**ERREUR \_ de \_ \_ Suppression de coexistence IPsec IKE \_**
</dt> <dd> <dl> <dt>

13902 (0x364E)
</dt> <dt>



SA a été supprimée en raison de la vérification de la coexistence de la coexistence IKEv1/AuthIP.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_RATELIMIT_DROP"></span><span id="error_ipsec_ike_ratelimit_drop"></span>**ERREUR \_ de \_ \_ suppression du RATELIMIT IKE IPSec \_**
</dt> <dd> <dl> <dt>

13903 (0x364F)
</dt> <dt>



La requête SA entrante a été supprimée en raison de la limitation du taux d’adresses IP d’homologue.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_PEER_DOESNT_SUPPORT_MOBIKE"></span><span id="error_ipsec_ike_peer_doesnt_support_mobike"></span>**ERREUR \_ IPSec \_ IKE \_ Peer \_ ne \_ prend pas en charge \_ MOBIKE**
</dt> <dd> <dl> <dt>

13904 (0x3650)
</dt> <dt>



L’homologue ne prend pas en charge MOBIKE.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_AUTHORIZATION_FAILURE"></span><span id="error_ipsec_ike_authorization_failure"></span>**ERREUR \_ \_ \_ d’échec d’autorisation IKE IPSec \_**
</dt> <dd> <dl> <dt>

13905 (0x3651)
</dt> <dt>



L'établissement d'associations de sécurité n'est pas autorisé.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_STRONG_CRED_AUTHORIZATION_FAILURE"></span><span id="error_ipsec_ike_strong_cred_authorization_failure"></span>**ERREUR \_ \_ \_ \_ \_ d’autorisation d’identification d’identification renforcée IPsec IKE \_**
</dt> <dd> <dl> <dt>

13906 (0x3652)
</dt> <dt>



L’établissement de SA n’est pas autorisé, car il n’y a pas d’informations d’identification PKINIT suffisamment fortes.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_AUTHORIZATION_FAILURE_WITH_OPTIONAL_RETRY"></span><span id="error_ipsec_ike_authorization_failure_with_optional_retry"></span>**ERREUR \_ \_ \_ d’autorisation IKE IPSec avec une \_ \_ \_ \_ nouvelle tentative facultative**
</dt> <dd> <dl> <dt>

13907 (0x3653)
</dt> <dt>



L'établissement d'associations de sécurité n'est pas autorisé. Vous devrez peut-être entrer des informations d’identification mises à jour ou différentes, telles qu’une carte à puce.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_STRONG_CRED_AUTHORIZATION_AND_CERTMAP_FAILURE"></span><span id="error_ipsec_ike_strong_cred_authorization_and_certmap_failure"></span>**ERREUR \_ \_ \_ d’autorisation d’identification d’identification forte IPsec IKE \_ \_ \_ et \_ échec de CERTMAP \_**
</dt> <dd> <dl> <dt>

13908 (0x3654)
</dt> <dt>



L’établissement de SA n’est pas autorisé, car il n’y a pas d’informations d’identification PKINIT suffisamment fortes. Cela peut être lié à un échec de mappage de certificat à compte pour l’administrateur système.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_NEG_STATUS_EXTENDED_END"></span><span id="error_ipsec_ike_neg_status_extended_end"></span>**ERREUR \_ de \_ \_ \_ \_ fin étendue d’état de la sécurité Ike Ike IPSec \_**
</dt> <dd> <dl> <dt>

13909 (0x3655)
</dt> <dt>



ERREUR \_ de \_ \_ \_ \_ fin étendue d’état de la sécurité Ike Ike IPSec \_


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_BAD_SPI"></span><span id="error_ipsec_bad_spi"></span>**ERREUR \_ IPSec \_ mauvais \_ SPI**
</dt> <dd> <dl> <dt>

13910 (0x3656)
</dt> <dt>



Le SPI du paquet ne correspond pas à une association de sécurité IPsec valide.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_SA_LIFETIME_EXPIRED"></span><span id="error_ipsec_sa_lifetime_expired"></span>**ERREUR \_ durée de vie de l’Association de sécurité IPSec \_ \_ \_ expirée**
</dt> <dd> <dl> <dt>

13911 (0x3657)
</dt> <dt>



Le paquet a été reçu sur une association de sécurité IPsec dont la durée de vie a expiré.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_WRONG_SA"></span><span id="error_ipsec_wrong_sa"></span>**erreur IPSec erreur d’association de \_ sécurité \_ \_**
</dt> <dd> <dl> <dt>

13912 (0x3658)
</dt> <dt>



Le paquet a été reçu sur une association de sécurité IPsec qui ne correspond pas aux caractéristiques du paquet.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_REPLAY_CHECK_FAILED"></span><span id="error_ipsec_replay_check_failed"></span>**ERREUR lors de la vérification de la \_ \_ relecture IPSec \_ \_**
</dt> <dd> <dl> <dt>

13913 (0x3659)
</dt> <dt>



Échec de la vérification de la relecture du numéro de séquence du paquet.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_INVALID_PACKET"></span><span id="error_ipsec_invalid_packet"></span>**ERREUR \_ de \_ paquet non valide IPSec \_**
</dt> <dd> <dl> <dt>

13914 (0x365A)
</dt> <dt>



L’en-tête et/ou le code de fin IPsec du paquet n’est pas valide.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_INTEGRITY_CHECK_FAILED"></span><span id="error_ipsec_integrity_check_failed"></span>**ERREUR \_ échec de la \_ vérification de l’intégrité IPSec \_ \_**
</dt> <dd> <dl> <dt>

13915 (0x365B)
</dt> <dt>



Échec de la vérification de l’intégrité IPsec.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_CLEAR_TEXT_DROP"></span><span id="error_ipsec_clear_text_drop"></span>**ERREUR \_ d' \_ effacement du texte en clair IPSec \_ \_**
</dt> <dd> <dl> <dt>

13916 (0x365C)
</dt> <dt>



IPsec a supprimé un paquet de texte en clair.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_AUTH_FIREWALL_DROP"></span><span id="error_ipsec_auth_firewall_drop"></span>**ERREUR \_ de \_ \_ suppression du pare-feu d’authentification IPSec \_**
</dt> <dd> <dl> <dt>

13917 (0x365D)
</dt> <dt>



IPsec a supprimé un paquet ESP entrant en mode pare-feu authentifié. Cette suppression est sans gravité.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_THROTTLE_DROP"></span><span id="error_ipsec_throttle_drop"></span>**ERREUR \_ de \_ Suppression d’accélération IPSec \_**
</dt> <dd> <dl> <dt>

13918 (0x365E)
</dt> <dt>



IPsec a supprimé un paquet en raison d’une limitation de la sécurité de l’attaque.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_DOSP_BLOCK"></span><span id="error_ipsec_dosp_block"></span>**ERREUR \_ de \_ bloc DOSP IPSec \_**
</dt> <dd> <dl> <dt>

13925 (0x3665)
</dt> <dt>



La protection DoS IPsec correspond à une règle de blocage explicite.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_DOSP_RECEIVED_MULTICAST"></span><span id="error_ipsec_dosp_received_multicast"></span>**ERREUR \_ IPSec \_ DOSP \_ reçue par la \_ multidiffusion**
</dt> <dd> <dl> <dt>

13926 (0x3666)
</dt> <dt>



La protection DoS IPsec a reçu un paquet de multidiffusion spécifique à IPsec, ce qui n’est pas autorisé.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_DOSP_INVALID_PACKET"></span><span id="error_ipsec_dosp_invalid_packet"></span>**ERREUR \_ IPSec \_ DOSP \_ paquet non valide \_**
</dt> <dd> <dl> <dt>

13927 (0x3667)
</dt> <dt>



La protection DoS IPsec a reçu un paquet mis en forme de manière incorrecte.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_DOSP_STATE_LOOKUP_FAILED"></span><span id="error_ipsec_dosp_state_lookup_failed"></span>**ERREUR \_ échec de la recherche d' \_ État DOSP IPSec \_ \_ \_**
</dt> <dd> <dl> <dt>

13928 (0x3668)
</dt> <dt>



La protection DoS IPsec n’a pas pu Rechercher l’État.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_DOSP_MAX_ENTRIES"></span><span id="error_ipsec_dosp_max_entries"></span>**ERREUR \_ \_ \_ nombre maximal d' \_ entrées IPSec DOSP**
</dt> <dd> <dl> <dt>

13929 (0x3669)
</dt> <dt>



La protection DoS IPsec n’a pas pu créer l’État, car le nombre maximal d’entrées autorisées par la stratégie a été atteint.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_DOSP_KEYMOD_NOT_ALLOWED"></span><span id="error_ipsec_dosp_keymod_not_allowed"></span>**ERREUR \_ IPSec \_ DOSP \_ KEYMOD \_ non \_ autorisée**
</dt> <dd> <dl> <dt>

13930 (0x366A)
</dt> <dt>



La protection DoS IPsec a reçu un paquet de négociation IPsec pour un module de génération de clé qui n’est pas autorisé par la stratégie.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_DOSP_NOT_INSTALLED"></span><span id="error_ipsec_dosp_not_installed"></span>**ERREUR \_ IPSec \_ DOSP \_ non \_ installé**
</dt> <dd> <dl> <dt>

13931 (0x366B)
</dt> <dt>



La protection DoS IPsec n’a pas été activée.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_DOSP_MAX_PER_IP_RATELIMIT_QUEUES"></span><span id="error_ipsec_dosp_max_per_ip_ratelimit_queues"></span>**ERREUR \_ IPSec \_ DOSP \_ Max. \_ par \_ RATELIMIT de \_ \_ files d’attente IP**
</dt> <dd> <dl> <dt>

13932 (0x366C)
</dt> <dt>



La protection DoS IPsec n’a pas pu créer une file d’attente par limite de débit IP interne, car le nombre maximal de files d’attente autorisées par la stratégie a été atteint.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_SECTION_NOT_FOUND"></span><span id="error_sxs_section_not_found"></span>**la section SxS de l’erreur est \_ \_ \_ \_ introuvable**
</dt> <dd> <dl> <dt>

14000 (0x36B0)
</dt> <dt>



La section demandée n’était pas présente dans le contexte d’activation.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_CANT_GEN_ACTCTX"></span><span id="error_sxs_cant_gen_actctx"></span>**ERREUR \_ SxS \_ Impossible \_ GEN \_ ACTCTX**
</dt> <dd> <dl> <dt>

14001 (0x36B1)
</dt> <dt>



L’application n’a pas pu démarrer, car sa configuration côte à côte est incorrecte. Pour plus d’informations, consultez le journal des événements de l’application ou utilisez l’outil de sxstrace.exe de ligne de commande.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_INVALID_ACTCTXDATA_FORMAT"></span><span id="error_sxs_invalid_actctxdata_format"></span>**ERREUR \_ SxS \_ \_ format de ACTCTXDATA non valide \_**
</dt> <dd> <dl> <dt>

14002 (0x36B2)
</dt> <dt>



Le format des données de liaison d’application n’est pas valide.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_ASSEMBLY_NOT_FOUND"></span><span id="error_sxs_assembly_not_found"></span>**ERREUR \_ SxS \_ assembly \_ \_ introuvable**
</dt> <dd> <dl> <dt>

14003 (0x36B3)
</dt> <dt>



L’assembly référencé n’est pas installé sur votre système.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_MANIFEST_FORMAT_ERROR"></span><span id="error_sxs_manifest_format_error"></span>**erreur \_ SxS \_ - \_ erreur de format du manifeste \_**
</dt> <dd> <dl> <dt>

14004 (0x36B4)
</dt> <dt>



Le fichier manifeste ne commence pas par la balise et les informations de format nécessaires.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_MANIFEST_PARSE_ERROR"></span><span id="error_sxs_manifest_parse_error"></span>**ERREUR \_ SxS \_ \_ erreur d’analyse du manifeste \_**
</dt> <dd> <dl> <dt>

14005 (0x36B5)
</dt> <dt>



Le fichier manifeste contient une ou plusieurs erreurs de syntaxe.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_ACTIVATION_CONTEXT_DISABLED"></span><span id="error_sxs_activation_context_disabled"></span>**ERREUR \_ de \_ contexte d’activation SxS \_ \_ désactivé**
</dt> <dd> <dl> <dt>

14006 (0x36B6)
</dt> <dt>



L’application a essayé d’activer un contexte d’activation désactivé.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_KEY_NOT_FOUND"></span><span id="error_sxs_key_not_found"></span>**ERREUR \_ SxS \_ clé \_ \_ introuvable**
</dt> <dd> <dl> <dt>

14007 (0x36B7)
</dt> <dt>



La clé de recherche demandée est introuvable dans un contexte d’activation actif.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_VERSION_CONFLICT"></span><span id="error_sxs_version_conflict"></span>**ERREUR \_ de \_ conflit de version SxS \_**
</dt> <dd> <dl> <dt>

14008 (0x36B8)
</dt> <dt>



Une version de composant requise par l’application est en conflit avec une autre version de composant déjà active.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_WRONG_SECTION_TYPE"></span><span id="error_sxs_wrong_section_type"></span>**ERREUR \_ SxS \_ \_ type de section incorrecte \_**
</dt> <dd> <dl> <dt>

14009 (0x36B9)
</dt> <dt>



La section de contexte d’activation demandée du type ne correspond pas à l’API de requête utilisée.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_THREAD_QUERIES_DISABLED"></span><span id="error_sxs_thread_queries_disabled"></span>**ERREUR \_ de \_ requête de thread SxS \_ \_ désactivée**
</dt> <dd> <dl> <dt>

14010 (0x36BA)
</dt> <dt>



L’absence de ressources système exige que l’activation isolée soit désactivée pour le thread d’exécution actuel.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_PROCESS_DEFAULT_ALREADY_SET"></span><span id="error_sxs_process_default_already_set"></span>**ERREUR \_ SxS le \_ processus \_ par défaut est \_ déjà \_ défini**
</dt> <dd> <dl> <dt>

14011 (0x36BB)
</dt> <dt>



Une tentative de définition du contexte d’activation par défaut du processus a échoué, car le contexte d’activation par défaut du processus était déjà défini.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_UNKNOWN_ENCODING_GROUP"></span><span id="error_sxs_unknown_encoding_group"></span>**ERREUR \_ SxS \_ - \_ groupe d’encodage inconnu \_**
</dt> <dd> <dl> <dt>

14012 (0x36BC)
</dt> <dt>



L’identificateur de groupe d’encodage spécifié n’est pas reconnu.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_UNKNOWN_ENCODING"></span><span id="error_sxs_unknown_encoding"></span>**ERREUR \_ SxS \_ \_ encodage inconnu**
</dt> <dd> <dl> <dt>

14013 (0x36BD)
</dt> <dt>



L’encodage demandé n’est pas reconnu.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_INVALID_XML_NAMESPACE_URI"></span><span id="error_sxs_invalid_xml_namespace_uri"></span>**ERREUR \_ SxS \_ \_ URI d' \_ espace de noms XML non valide \_**
</dt> <dd> <dl> <dt>

14014 (0x36BE)
</dt> <dt>



Le manifeste contient une référence à un URI non valide.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_ROOT_MANIFEST_DEPENDENCY_NOT_INSTALLED"></span><span id="error_sxs_root_manifest_dependency_not_installed"></span>**ERREUR \_ SxS \_ la \_ dépendance du manifeste racine \_ n’est \_ pas \_ installée**
</dt> <dd> <dl> <dt>

14015 (0x36BF)
</dt> <dt>



Le manifeste d’application contient une référence à un assembly dépendant qui n’est pas installé.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_LEAF_MANIFEST_DEPENDENCY_NOT_INSTALLED"></span><span id="error_sxs_leaf_manifest_dependency_not_installed"></span>**ERREUR \_ SxS la dépendance du manifeste de la \_ feuille \_ n’est \_ \_ pas \_ installée**
</dt> <dd> <dl> <dt>

14016 (0x36C0)
</dt> <dt>



Le manifeste d’un assembly utilisé par l’application a une référence à un assembly dépendant qui n’est pas installé.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_INVALID_ASSEMBLY_IDENTITY_ATTRIBUTE"></span><span id="error_sxs_invalid_assembly_identity_attribute"></span>**ERREUR \_ SxS \_ \_ attribut d’identité d’assembly non valide \_ \_**
</dt> <dd> <dl> <dt>

14017 (0x36C1)
</dt> <dt>



Le manifeste contient un attribut pour l’identité de l’assembly qui n’est pas valide.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_MANIFEST_MISSING_REQUIRED_DEFAULT_NAMESPACE"></span><span id="error_sxs_manifest_missing_required_default_namespace"></span>**ERREUR \_ côte au \_ manifeste \_ manquant espace de \_ \_ noms par défaut requis \_**
</dt> <dd> <dl> <dt>

14018 (0x36C2)
</dt> <dt>



Le manifeste ne contient pas la spécification d’espace de noms par défaut requise sur l’élément d’assembly.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_MANIFEST_INVALID_REQUIRED_DEFAULT_NAMESPACE"></span><span id="error_sxs_manifest_invalid_required_default_namespace"></span>**ERREUR \_ SxS \_ manifeste de l’espace de \_ \_ \_ noms par défaut requis non valide \_**
</dt> <dd> <dl> <dt>

14019 (0x36C3)
</dt> <dt>



Le manifeste a un espace de noms par défaut spécifié sur l’élément assembly, mais sa valeur n’est pas « urn : schemas-microsoft-com : ASM. v1 ».


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_PRIVATE_MANIFEST_CROSS_PATH_WITH_REPARSE_POINT"></span><span id="error_sxs_private_manifest_cross_path_with_reparse_point"></span>**ERREUR \_ SxS \_ \_ \_ chemin d’accès croisé du manifeste privé \_ \_ avec le \_ point d’analyse \_**
</dt> <dd> <dl> <dt>

14020 (0x36C4)
</dt> <dt>



Le manifeste privé détecté a franchi un chemin d’accès avec un point d’analyse non pris en charge.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_DUPLICATE_DLL_NAME"></span><span id="error_sxs_duplicate_dll_name"></span>**ERREUR \_ SxS \_ nom de la dll dupliquée \_ \_**
</dt> <dd> <dl> <dt>

14021 (0x36C5)
</dt> <dt>



Au moins deux composants référencés directement ou indirectement par le manifeste de l’application ont des fichiers portant le même nom.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_DUPLICATE_WINDOWCLASS_NAME"></span><span id="error_sxs_duplicate_windowclass_name"></span>**ERREUR \_ SxS \_ \_ nom de WINDOWCLASS dupliqué \_**
</dt> <dd> <dl> <dt>

14022 (0x36C6)
</dt> <dt>



Au moins deux composants référencés directement ou indirectement par le manifeste de l’application ont des classes de fenêtre portant le même nom.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_DUPLICATE_CLSID"></span><span id="error_sxs_duplicate_clsid"></span>**ERREUR \_ SxS \_ doublon \_ CLSID**
</dt> <dd> <dl> <dt>

14023 (0x36C7)
</dt> <dt>



Au moins deux composants référencés directement ou indirectement par le manifeste de l’application ont les mêmes CLSID du serveur COM.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_DUPLICATE_IID"></span><span id="error_sxs_duplicate_iid"></span>**ERREUR \_ SxS \_ en doublon d' \_ IID**
</dt> <dd> <dl> <dt>

14024 (0x36C8)
</dt> <dt>



Au moins deux composants référencés directement ou indirectement par le manifeste de l’application ont des proxies pour les mêmes IID de l’interface COM.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_DUPLICATE_TLBID"></span><span id="error_sxs_duplicate_tlbid"></span>**ERREUR \_ SxS \_ en double \_ TLBID (**
</dt> <dd> <dl> <dt>

14025 (0x36C9)
</dt> <dt>



Au moins deux composants référencés directement ou indirectement par le manifeste de l’application ont la même bibliothèque de types COM TLBIDs.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_DUPLICATE_PROGID"></span><span id="error_sxs_duplicate_progid"></span>**ERREUR \_ SxS \_ en doublon \_ ProgID**
</dt> <dd> <dl> <dt>

14026 (0x36CA)
</dt> <dt>



Au moins deux composants référencés directement ou indirectement par le manifeste de l’application ont les mêmes ProgID COM.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_DUPLICATE_ASSEMBLY_NAME"></span><span id="error_sxs_duplicate_assembly_name"></span>**ERREUR \_ SxS \_ \_ nom d’assembly dupliqué \_**
</dt> <dd> <dl> <dt>

14027 (0x36CB)
</dt> <dt>



Au moins deux composants référencés directement ou indirectement par le manifeste d’application sont des versions différentes du même composant, ce qui n’est pas autorisé.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_FILE_HASH_MISMATCH"></span><span id="error_sxs_file_hash_mismatch"></span>**ERREUR \_ SxS \_ \_ incompatibilité de hachage de fichier \_**
</dt> <dd> <dl> <dt>

14028 (0x36CC)
</dt> <dt>



Le fichier d’un composant ne correspond pas aux informations de vérification présentes dans le manifeste du composant.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_POLICY_PARSE_ERROR"></span><span id="error_sxs_policy_parse_error"></span>**erreur d’analyse de la \_ \_ stratégie SxS \_ \_**
</dt> <dd> <dl> <dt>

14029 (0x36CD)
</dt> <dt>



Le manifeste de la stratégie contient une ou plusieurs erreurs de syntaxe.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_MISSINGQUOTE"></span><span id="error_sxs_xml_e_missingquote"></span>**ERREUR \_ SxS \_ XML \_ E \_ MISSINGQUOTE**
</dt> <dd> <dl> <dt>

14030 (0x36CE)
</dt> <dt>



Erreur d’analyse du manifeste : un littéral de chaîne était attendu, mais aucun caractère de guillemet d’ouverture n’a été trouvé.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_COMMENTSYNTAX"></span><span id="error_sxs_xml_e_commentsyntax"></span>**ERREUR \_ SxS \_ XML \_ E \_ COMMENTSYNTAX**
</dt> <dd> <dl> <dt>

14031 (0x36CF)
</dt> <dt>



Erreur d’analyse du manifeste : une syntaxe incorrecte a été utilisée dans un commentaire.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_BADSTARTNAMECHAR"></span><span id="error_sxs_xml_e_badstartnamechar"></span>**ERREUR \_ SxS \_ XML \_ E \_ BADSTARTNAMECHAR**
</dt> <dd> <dl> <dt>

14032 (0x36D0)
</dt> <dt>



Erreur d’analyse du manifeste : un nom a été démarré avec un caractère non valide.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_BADNAMECHAR"></span><span id="error_sxs_xml_e_badnamechar"></span>**ERREUR \_ SxS \_ XML \_ E \_ BADNAMECHAR**
</dt> <dd> <dl> <dt>

14033 (0x36D1)
</dt> <dt>



Erreur d’analyse du manifeste : un nom contenait un caractère non valide.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_BADCHARINSTRING"></span><span id="error_sxs_xml_e_badcharinstring"></span>**ERREUR \_ SxS \_ XML \_ E \_ BADCHARINSTRING**
</dt> <dd> <dl> <dt>

14034 (0x36D2)
</dt> <dt>



Erreur d’analyse du manifeste : un littéral de chaîne contenait un caractère non valide.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_XMLDECLSYNTAX"></span><span id="error_sxs_xml_e_xmldeclsyntax"></span>**ERREUR \_ SxS \_ XML \_ E \_ XMLDECLSYNTAX**
</dt> <dd> <dl> <dt>

14035 (0x36D3)
</dt> <dt>



Erreur d’analyse du manifeste : syntaxe non valide pour une déclaration XML.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_BADCHARDATA"></span><span id="error_sxs_xml_e_badchardata"></span>**ERREUR \_ SxS \_ XML \_ E \_ BADCHARDATA**
</dt> <dd> <dl> <dt>

14036 (0x36D4)
</dt> <dt>



Erreur d’analyse du manifeste : un caractère non valide a été trouvé dans le contenu de texte.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_MISSINGWHITESPACE"></span><span id="error_sxs_xml_e_missingwhitespace"></span>**ERREUR \_ SxS \_ XML \_ E \_ MISSINGWHITESPACE**
</dt> <dd> <dl> <dt>

14037 (0x36D5)
</dt> <dt>



Erreur d’analyse du manifeste : un espace blanc requis était manquant.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_EXPECTINGTAGEND"></span><span id="error_sxs_xml_e_expectingtagend"></span>**ERREUR \_ SxS \_ XML \_ E \_ EXPECTINGTAGEND**
</dt> <dd> <dl> <dt>

14038 (0x36D6)
</dt> <dt>



Erreur d’analyse du manifeste : le caractère' > 'était attendu.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_MISSINGSEMICOLON"></span><span id="error_sxs_xml_e_missingsemicolon"></span>**ERREUR \_ SxS \_ XML \_ E \_ MISSINGSEMICOLON**
</dt> <dd> <dl> <dt>

14039 (0x36D7)
</dt> <dt>



Erreur d’analyse du manifeste : un point-virgule était attendu.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_UNBALANCEDPAREN"></span><span id="error_sxs_xml_e_unbalancedparen"></span>**ERREUR \_ SxS \_ XML \_ E \_ UNBALANCEDPAREN**
</dt> <dd> <dl> <dt>

14040 (0x36D8)
</dt> <dt>



Erreur d’analyse du manifeste : parenthèses non équilibrées.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_INTERNALERROR"></span><span id="error_sxs_xml_e_internalerror"></span>**ERREUR \_ SxS \_ XML \_ E \_ INTERNALERROR**
</dt> <dd> <dl> <dt>

14041 (0x36D9)
</dt> <dt>



Erreur d’analyse du manifeste : erreur interne.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_UNEXPECTED_WHITESPACE"></span><span id="error_sxs_xml_e_unexpected_whitespace"></span>**ERREUR \_ SxS \_ XML \_ E \_ espace inattendu \_**
</dt> <dd> <dl> <dt>

14042 (0x36DA)
</dt> <dt>



Erreur d’analyse du manifeste : un espace blanc n’est pas autorisé à cet emplacement.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_INCOMPLETE_ENCODING"></span><span id="error_sxs_xml_e_incomplete_encoding"></span>**ERREUR \_ SxS \_ XML \_ E \_ \_ encodage incomplet**
</dt> <dd> <dl> <dt>

14043 (0x36DB)
</dt> <dt>



Erreur d’analyse du manifeste : la fin du fichier a atteint un État non valide pour l’encodage actuel.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_MISSING_PAREN"></span><span id="error_sxs_xml_e_missing_paren"></span>**ERREUR \_ SxS \_ XML \_ E \_ manquant \_ parenthèse**
</dt> <dd> <dl> <dt>

14044 (0x36DC)
</dt> <dt>



Erreur d’analyse du manifeste : parenthèses manquantes.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_EXPECTINGCLOSEQUOTE"></span><span id="error_sxs_xml_e_expectingclosequote"></span>**ERREUR \_ SxS \_ XML \_ E \_ EXPECTINGCLOSEQUOTE**
</dt> <dd> <dl> <dt>

14045 (0x36DD)
</dt> <dt>



Erreur d’analyse du manifeste : un guillemet simple ou double de fermeture ( \\ 'ou \\ ") est manquant.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_MULTIPLE_COLONS"></span><span id="error_sxs_xml_e_multiple_colons"></span>**ERREUR \_ SxS \_ XML \_ E \_ plusieurs \_ signes deux-points**
</dt> <dd> <dl> <dt>

14046 (0x36DE)
</dt> <dt>



Erreur d’analyse du manifeste : plusieurs signes deux-points ne sont pas autorisés dans un nom.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_INVALID_DECIMAL"></span><span id="error_sxs_xml_e_invalid_decimal"></span>**ERREUR \_ SxS \_ XML \_ E \_ non valide \_**
</dt> <dd> <dl> <dt>

14047 (0x36DF)
</dt> <dt>



Erreur d’analyse du manifeste : caractère non valide pour un chiffre décimal.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_INVALID_HEXIDECIMAL"></span><span id="error_sxs_xml_e_invalid_hexidecimal"></span>**ERREUR \_ SxS \_ XML \_ E \_ hexadécimal non valide \_**
</dt> <dd> <dl> <dt>

14048 (0x36E0)
</dt> <dt>



Erreur d’analyse du manifeste : caractère non valide pour un chiffre hexadécimal.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_INVALID_UNICODE"></span><span id="error_sxs_xml_e_invalid_unicode"></span>**ERREUR \_ SxS \_ XML \_ E \_ Unicode non valide \_**
</dt> <dd> <dl> <dt>

14049 (0x36E1)
</dt> <dt>



Erreur d’analyse du manifeste : valeur de caractère Unicode non valide pour cette plateforme.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_WHITESPACEORQUESTIONMARK"></span><span id="error_sxs_xml_e_whitespaceorquestionmark"></span>**ERREUR \_ SxS \_ XML \_ E \_ WHITESPACEORQUESTIONMARK**
</dt> <dd> <dl> <dt>

14050 (0x36E2)
</dt> <dt>



Erreur d’analyse du manifeste : espace blanc attendu ou' ? '.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_UNEXPECTEDENDTAG"></span><span id="error_sxs_xml_e_unexpectedendtag"></span>**ERREUR \_ SxS \_ XML \_ E \_ UNEXPECTEDENDTAG**
</dt> <dd> <dl> <dt>

14051 (0x36E3)
</dt> <dt>



Erreur d’analyse du manifeste : balise de fin non attendue à cet emplacement.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_UNCLOSEDTAG"></span><span id="error_sxs_xml_e_unclosedtag"></span>**ERREUR \_ SxS \_ XML \_ E \_ UNCLOSEDTAG**
</dt> <dd> <dl> <dt>

14052 (0x36E4)
</dt> <dt>



Erreur d’analyse du manifeste : les balises suivantes n’ont pas été fermées : %1.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_DUPLICATEATTRIBUTE"></span><span id="error_sxs_xml_e_duplicateattribute"></span>**ERREUR \_ SxS \_ XML \_ E \_ DUPLICATEATTRIBUTE**
</dt> <dd> <dl> <dt>

14053 (0x36E5)
</dt> <dt>



Erreur d’analyse du manifeste : attribut dupliqué.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_MULTIPLEROOTS"></span><span id="error_sxs_xml_e_multipleroots"></span>**ERREUR \_ SxS \_ XML \_ E \_ MULTIPLEROOTS**
</dt> <dd> <dl> <dt>

14054 (0x36E6)
</dt> <dt>



Erreur d’analyse du manifeste : un seul élément de niveau supérieur est autorisé dans un document XML.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_INVALIDATROOTLEVEL"></span><span id="error_sxs_xml_e_invalidatrootlevel"></span>**ERREUR \_ SxS \_ XML \_ E \_ INVALIDATROOTLEVEL**
</dt> <dd> <dl> <dt>

14055 (0x36E7)
</dt> <dt>



Erreur d’analyse du manifeste : non valide au niveau supérieur du document.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_BADXMLDECL"></span><span id="error_sxs_xml_e_badxmldecl"></span>**ERREUR \_ SxS \_ XML \_ E \_ BADXMLDECL**
</dt> <dd> <dl> <dt>

14056 (0x36E8)
</dt> <dt>



Erreur d’analyse du manifeste : déclaration XML non valide.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_MISSINGROOT"></span><span id="error_sxs_xml_e_missingroot"></span>**ERREUR \_ SxS \_ XML \_ E \_ MISSINGROOT**
</dt> <dd> <dl> <dt>

14057 (0x36E9)
</dt> <dt>



Erreur d’analyse du manifeste : le document XML doit avoir un élément de niveau supérieur.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_UNEXPECTEDEOF"></span><span id="error_sxs_xml_e_unexpectedeof"></span>**ERREUR \_ SxS \_ XML \_ E \_ UNEXPECTEDEOF**
</dt> <dd> <dl> <dt>

14058 (0x36EA)
</dt> <dt>



Erreur d’analyse du manifeste : fin de fichier inattendue.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_BADPEREFINSUBSET"></span><span id="error_sxs_xml_e_badperefinsubset"></span>**ERREUR \_ SxS \_ XML \_ E \_ BADPEREFINSUBSET**
</dt> <dd> <dl> <dt>

14059 (0x36EB)
</dt> <dt>



Erreur d’analyse du manifeste : les entités de paramètre ne peuvent pas être utilisées dans des déclarations de balisage dans un sous-ensemble interne.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_UNCLOSEDSTARTTAG"></span><span id="error_sxs_xml_e_unclosedstarttag"></span>**ERREUR \_ SxS \_ XML \_ E \_ UNCLOSEDSTARTTAG**
</dt> <dd> <dl> <dt>

14060 (0x36EC)
</dt> <dt>



Erreur d’analyse du manifeste : l’élément n’a pas été fermé.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_UNCLOSEDENDTAG"></span><span id="error_sxs_xml_e_unclosedendtag"></span>**ERREUR \_ SxS \_ XML \_ E \_ UNCLOSEDENDTAG**
</dt> <dd> <dl> <dt>

14061 (0x36ED)
</dt> <dt>



Erreur d’analyse du manifeste : le caractère' > 'est manquant dans l’élément de fin.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_UNCLOSEDSTRING"></span><span id="error_sxs_xml_e_unclosedstring"></span>**ERREUR \_ SxS \_ XML \_ E \_ UNCLOSEDSTRING**
</dt> <dd> <dl> <dt>

14062 (0x36EE)
</dt> <dt>



Erreur d’analyse du manifeste : un littéral de chaîne n’a pas été fermé.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_UNCLOSEDCOMMENT"></span><span id="error_sxs_xml_e_unclosedcomment"></span>**ERREUR \_ SxS \_ XML \_ E \_ UNCLOSEDCOMMENT**
</dt> <dd> <dl> <dt>

14063 (0x36EF)
</dt> <dt>



Erreur d’analyse du manifeste : un commentaire n’a pas été fermé.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_UNCLOSEDDECL"></span><span id="error_sxs_xml_e_uncloseddecl"></span>**ERREUR \_ SxS \_ XML \_ E \_ UNCLOSEDDECL**
</dt> <dd> <dl> <dt>

14064 (0x36F0)
</dt> <dt>



Erreur d’analyse du manifeste : une déclaration n’a pas été fermée.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_UNCLOSEDCDATA"></span><span id="error_sxs_xml_e_unclosedcdata"></span>**ERREUR \_ SxS \_ XML \_ E \_ UNCLOSEDCDATA**
</dt> <dd> <dl> <dt>

14065 (0x36F1)
</dt> <dt>



Erreur d’analyse du manifeste : une section CDATA n’a pas été fermée.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_RESERVEDNAMESPACE"></span><span id="error_sxs_xml_e_reservednamespace"></span>**ERREUR \_ SxS \_ XML \_ E \_ RESERVEDNAMESPACE**
</dt> <dd> <dl> <dt>

14066 (0x36F2)
</dt> <dt>



Erreur d’analyse du manifeste : le préfixe de l’espace de noms n’est pas autorisé à démarrer avec la chaîne réservée « xml ».


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_INVALIDENCODING"></span><span id="error_sxs_xml_e_invalidencoding"></span>**ERREUR \_ SxS \_ XML \_ E \_ INVALIDENCODING**
</dt> <dd> <dl> <dt>

14067 (0x36F3)
</dt> <dt>



Erreur d’analyse du manifeste : le système ne prend pas en charge l’encodage spécifié.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_INVALIDSWITCH"></span><span id="error_sxs_xml_e_invalidswitch"></span>**ERREUR \_ SxS \_ XML \_ E \_ INVALIDSWITCH**
</dt> <dd> <dl> <dt>

14068 (0x36F4)
</dt> <dt>



Erreur d’analyse du manifeste : le passage de l’encodage actuel à l’encodage spécifié n’est pas pris en charge.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_BADXMLCASE"></span><span id="error_sxs_xml_e_badxmlcase"></span>**ERREUR \_ SxS \_ XML \_ E \_ BADXMLCASE**
</dt> <dd> <dl> <dt>

14069 (0x36F5)
</dt> <dt>



Erreur d’analyse du manifeste : le nom’XML’est réservé et doit être en minuscules.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_INVALID_STANDALONE"></span><span id="error_sxs_xml_e_invalid_standalone"></span>**ERREUR \_ SxS \_ XML \_ E \_ non valide \_ autonome**
</dt> <dd> <dl> <dt>

14070 (0x36F6)
</dt> <dt>



Erreur d’analyse du manifeste : l’attribut autonome doit avoir la valeur’Yes’ou’no'.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_UNEXPECTED_STANDALONE"></span><span id="error_sxs_xml_e_unexpected_standalone"></span>**ERREUR \_ SxS \_ XML \_ E \_ inattendu en mode \_ autonome**
</dt> <dd> <dl> <dt>

14071 (0x36F7)
</dt> <dt>



Erreur d’analyse du manifeste : l’attribut autonome ne peut pas être utilisé dans des entités externes.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_INVALID_VERSION"></span><span id="error_sxs_xml_e_invalid_version"></span>**ERREUR \_ SxS \_ XML \_ E \_ version non valide \_**
</dt> <dd> <dl> <dt>

14072 (0x36F8)
</dt> <dt>



Erreur d’analyse du manifeste : numéro de version non valide.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_MISSINGEQUALS"></span><span id="error_sxs_xml_e_missingequals"></span>**ERREUR \_ SxS \_ XML \_ E \_ MISSINGEQUALS**
</dt> <dd> <dl> <dt>

14073 (0x36F9)
</dt> <dt>



Erreur d’analyse du manifeste : signe égal manquant entre l’attribut et la valeur de l’attribut.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_PROTECTION_RECOVERY_FAILED"></span><span id="error_sxs_protection_recovery_failed"></span>**ERREUR d’échec de la récupération de la \_ \_ protection SxS \_ \_**
</dt> <dd> <dl> <dt>

14074 (0x36FA)
</dt> <dt>



Erreur de protection de l’assembly : impossible de récupérer l’assembly spécifié.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_PROTECTION_PUBLIC_KEY_TOO_SHORT"></span><span id="error_sxs_protection_public_key_too_short"></span>**ERREUR \_ de \_ clé publique de protection SxS \_ \_ \_ trop \_ brève**
</dt> <dd> <dl> <dt>

14075 (0x36FB)
</dt> <dt>



Erreur de protection de l’assembly : la clé publique d’un assembly est trop petite pour être autorisée.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_PROTECTION_CATALOG_NOT_VALID"></span><span id="error_sxs_protection_catalog_not_valid"></span>**ERREUR \_ du \_ catalogue de protection SxS \_ \_ non \_ valide**
</dt> <dd> <dl> <dt>

14076 (0x36FC)
</dt> <dt>



Erreur de protection de l’assembly : le catalogue d’un assembly n’est pas valide ou ne correspond pas au manifeste de l’assembly.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_UNTRANSLATABLE_HRESULT"></span><span id="error_sxs_untranslatable_hresult"></span>**ERREUR \_ SxS \_ untranslateable \_ HRESULT**
</dt> <dd> <dl> <dt>

14077 (0x36FD)
</dt> <dt>



Un HRESULT n’a pas pu être traduit en code d’erreur Win32 correspondant.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_PROTECTION_CATALOG_FILE_MISSING"></span><span id="error_sxs_protection_catalog_file_missing"></span>**ERREUR \_ SxS \_ fichier du catalogue de protection \_ \_ \_ manquant**
</dt> <dd> <dl> <dt>

14078 (0x36FE)
</dt> <dt>



Erreur de protection de l’assembly : le catalogue d’un assembly est manquant.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_MISSING_ASSEMBLY_IDENTITY_ATTRIBUTE"></span><span id="error_sxs_missing_assembly_identity_attribute"></span>**ERREUR \_ SxS \_ \_ attribut d' \_ identité d’assembly manquant \_**
</dt> <dd> <dl> <dt>

14079 (0x36FF)
</dt> <dt>



L’identité d’assembly fournie ne contient pas un ou plusieurs attributs qui doivent être présents dans ce contexte.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_INVALID_ASSEMBLY_IDENTITY_ATTRIBUTE_NAME"></span><span id="error_sxs_invalid_assembly_identity_attribute_name"></span>**ERREUR \_ SxS \_ \_ nom d' \_ attribut d’identité d’assembly non \_ valide \_**
</dt> <dd> <dl> <dt>

14080 (0x3700)
</dt> <dt>



L’identité d’assembly fournie a un ou plusieurs noms d’attribut qui contiennent des caractères non autorisés dans les noms XML.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_ASSEMBLY_MISSING"></span><span id="error_sxs_assembly_missing"></span>**ERREUR de l' \_ \_ assembly SxS \_ manquant**
</dt> <dd> <dl> <dt>

14081 (0x3701)
</dt> <dt>



L’assembly référencé est introuvable.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_CORRUPT_ACTIVATION_STACK"></span><span id="error_sxs_corrupt_activation_stack"></span>**ERREUR \_ SxS \_ , \_ pile d’activation endommagée \_**
</dt> <dd> <dl> <dt>

14082 (0x3702)
</dt> <dt>



La pile d’activation du contexte d’activation pour le thread d’exécution en cours d’exécution est endommagée.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_CORRUPTION"></span><span id="error_sxs_corruption"></span>**ERREUR \_ SxS d' \_ altération**
</dt> <dd> <dl> <dt>

14083 (0x3703)
</dt> <dt>



Les métadonnées d’isolation d’application pour ce processus ou ce thread sont endommagées.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_EARLY_DEACTIVATION"></span><span id="error_sxs_early_deactivation"></span>**ERREUR \_ SxS \_ la \_ désactivation précoce**
</dt> <dd> <dl> <dt>

14084 (0x3704)
</dt> <dt>



Le contexte d’activation en cours de désactivation n’est pas le contexte activé le plus récemment.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_INVALID_DEACTIVATION"></span><span id="error_sxs_invalid_deactivation"></span>**ERREUR \_ SxS \_ \_ désactivation non valide**
</dt> <dd> <dl> <dt>

14085 (0x3705)
</dt> <dt>



Le contexte d’activation en cours de désactivation n’est pas actif pour le thread d’exécution actuel.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_MULTIPLE_DEACTIVATION"></span><span id="error_sxs_multiple_deactivation"></span>**ERREUR \_ SxS \_ plusieurs \_ désactivations**
</dt> <dd> <dl> <dt>

14086 (0x3706)
</dt> <dt>



Le contexte d’activation en cours de désactivation a déjà été désactivé.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_PROCESS_TERMINATION_REQUESTED"></span><span id="error_sxs_process_termination_requested"></span>**ERREUR \_ d' \_ arrêt de processus SxS \_ \_ demandée**
</dt> <dd> <dl> <dt>

14087 (0x3707)
</dt> <dt>



Un composant utilisé par la fonctionnalité d’isolation a demandé l’arrêt du processus.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_RELEASE_ACTIVATION_CONTEXT"></span><span id="error_sxs_release_activation_context"></span>**ERREUR \_ côte \_ à \_ l’activation de la libération \_**
</dt> <dd> <dl> <dt>

14088 (0x3708)
</dt> <dt>



Un composant en mode noyau publie une référence sur un contexte d’activation.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_SYSTEM_DEFAULT_ACTIVATION_CONTEXT_EMPTY"></span><span id="error_sxs_system_default_activation_context_empty"></span>**ERREUR \_ SxS \_ \_ contexte d’activation par défaut du système SxS \_ \_ \_ vide**
</dt> <dd> <dl> <dt>

14089 (0x3709)
</dt> <dt>



Impossible de générer le contexte d’activation de l’assembly par défaut du système.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_INVALID_IDENTITY_ATTRIBUTE_VALUE"></span><span id="error_sxs_invalid_identity_attribute_value"></span>**ERREUR \_ SxS \_ \_ valeur d' \_ attribut d’identité non valide \_**
</dt> <dd> <dl> <dt>

14090 (0x370A)
</dt> <dt>



La valeur d’un attribut dans une identité n’est pas comprise dans la plage autorisée.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_INVALID_IDENTITY_ATTRIBUTE_NAME"></span><span id="error_sxs_invalid_identity_attribute_name"></span>**ERREUR \_ SxS \_ \_ nom d' \_ attribut d’identité non valide \_**
</dt> <dd> <dl> <dt>

14091 (0x370B)
</dt> <dt>



Le nom d’un attribut dans une identité n’est pas compris dans la plage légale.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_IDENTITY_DUPLICATE_ATTRIBUTE"></span><span id="error_sxs_identity_duplicate_attribute"></span>**ERREUR \_ SxS- \_ attribut d’identité \_ en double \_**
</dt> <dd> <dl> <dt>

14092 (0x370C)
</dt> <dt>



Une identité contient deux définitions pour le même attribut.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_IDENTITY_PARSE_ERROR"></span><span id="error_sxs_identity_parse_error"></span>**ERREUR \_ SxS \_ \_ erreur d’analyse \_ de l’identité**
</dt> <dd> <dl> <dt>

14093 (0x370D)
</dt> <dt>



La chaîne d’identité est incorrecte. Cela peut être dû à une virgule de fin, à plus de deux attributs sans nom, à un nom d’attribut manquant ou à une valeur d’attribut manquante.


</dt> </dl> </dd> <dt>

<span id="ERROR_MALFORMED_SUBSTITUTION_STRING"></span><span id="error_malformed_substitution_string"></span>**ERREUR \_ de \_ chaîne de substitution incorrecte \_**
</dt> <dd> <dl> <dt>

14094 (0x370E)
</dt> <dt>



Une chaîne contenant du contenu substitué localisé est incorrecte. Le signe dollar ($) a été suivi d’un autre signe dollar ou d’un autre signe dollar ou bien la parenthèse droite d’une substitution est introuvable.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_INCORRECT_PUBLIC_KEY_TOKEN"></span><span id="error_sxs_incorrect_public_key_token"></span>**ERREUR \_ SxS \_ \_ jeton de \_ clé \_ publique incorrect**
</dt> <dd> <dl> <dt>

14095 (0x370F)
</dt> <dt>



Le jeton de clé publique ne correspond pas à la clé publique spécifiée.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNMAPPED_SUBSTITUTION_STRING"></span><span id="error_unmapped_substitution_string"></span>**ERREUR de \_ chaîne de substitution non mappée \_ \_**
</dt> <dd> <dl> <dt>

14096 (0x3710)
</dt> <dt>



Aucune chaîne de substitution n’a été mappée.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_ASSEMBLY_NOT_LOCKED"></span><span id="error_sxs_assembly_not_locked"></span>**ERREUR \_ SxS \_ assembly \_ non \_ verrouillé**
</dt> <dd> <dl> <dt>

14097 (0x3711)
</dt> <dt>



Le composant doit être verrouillé avant d’effectuer la demande.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_COMPONENT_STORE_CORRUPT"></span><span id="error_sxs_component_store_corrupt"></span>**ERREUR \_ du \_ magasin de composants SxS \_ \_ endommagé**
</dt> <dd> <dl> <dt>

14098 (0x3712)
</dt> <dt>



Le magasin de composants a été endommagé.


</dt> </dl> </dd> <dt>

<span id="ERROR_ADVANCED_INSTALLER_FAILED"></span><span id="error_advanced_installer_failed"></span>**ERREUR \_ \_ échec du programme d’installation avancé \_**
</dt> <dd> <dl> <dt>

14099 (0x3713)
</dt> <dt>



Un programme d’installation avancé a échoué lors de l’installation ou de la maintenance.


</dt> </dl> </dd> <dt>

<span id="ERROR_XML_ENCODING_MISMATCH"></span><span id="error_xml_encoding_mismatch"></span>**ERREUR \_ d' \_ incompatibilité d’encodage XML \_**
</dt> <dd> <dl> <dt>

14100 (0x3714)
</dt> <dt>



L’encodage de caractères dans la déclaration XML ne correspondait pas à l’encodage utilisé dans le document.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_MANIFEST_IDENTITY_SAME_BUT_CONTENTS_DIFFERENT"></span><span id="error_sxs_manifest_identity_same_but_contents_different"></span>**ERREUR \_ SxS \_ identité du manifeste, \_ \_ \_ mais \_ contenu \_ différent**
</dt> <dd> <dl> <dt>

14101 (0x3715)
</dt> <dt>



Les identités des manifestes sont identiques, mais leur contenu est différent.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_IDENTITIES_DIFFERENT"></span><span id="error_sxs_identities_different"></span>**ERREUR \_ SxS \_ différente des identités \_**
</dt> <dd> <dl> <dt>

14102 (0x3716)
</dt> <dt>



Les identités des composants sont différentes.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_ASSEMBLY_IS_NOT_A_DEPLOYMENT"></span><span id="error_sxs_assembly_is_not_a_deployment"></span>**ERREUR \_ SxS l' \_ assembly \_ n’est \_ pas \_ un \_ déploiement**
</dt> <dd> <dl> <dt>

14103 (0x3717)
</dt> <dt>



L’assembly n’est pas un déploiement.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_FILE_NOT_PART_OF_ASSEMBLY"></span><span id="error_sxs_file_not_part_of_assembly"></span>**ERREUR \_ SxS \_ fichier \_ ne \_ faisant pas partie \_ de l' \_ assembly**
</dt> <dd> <dl> <dt>

14104 (0x3718)
</dt> <dt>



Le fichier ne fait pas partie de l’assembly.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_MANIFEST_TOO_BIG"></span><span id="error_sxs_manifest_too_big"></span>**ERREUR \_ SxS le \_ manifeste est \_ trop \_ volumineux**
</dt> <dd> <dl> <dt>

14105 (0x3719)
</dt> <dt>



La taille du manifeste dépasse la valeur maximale autorisée.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_SETTING_NOT_REGISTERED"></span><span id="error_sxs_setting_not_registered"></span>**ERREUR \_ SxS \_ paramètre \_ non \_ inscrit**
</dt> <dd> <dl> <dt>

14106 (0x371A)
</dt> <dt>



Le paramètre n’est pas inscrit.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_TRANSACTION_CLOSURE_INCOMPLETE"></span><span id="error_sxs_transaction_closure_incomplete"></span>**ERREUR \_ SxS \_ transaction \_ Closure \_ incomplète**
</dt> <dd> <dl> <dt>

14107 (0x371B)
</dt> <dt>



Un ou plusieurs membres requis de la transaction ne sont pas présents.


</dt> </dl> </dd> <dt>

<span id="ERROR_SMI_PRIMITIVE_INSTALLER_FAILED"></span><span id="error_smi_primitive_installer_failed"></span>**ERREUR \_ SMI \_ primitive le \_ programme d’installation \_ a échoué**
</dt> <dd> <dl> <dt>

14108 (0x371C)
</dt> <dt>



Le programme d’installation primitif de SMI a échoué lors de l’installation ou de la maintenance.


</dt> </dl> </dd> <dt>

<span id="ERROR_GENERIC_COMMAND_FAILED"></span><span id="error_generic_command_failed"></span>**échec de la \_ commande générique d’erreur \_ \_**
</dt> <dd> <dl> <dt>

14109 (0x371D)
</dt> <dt>



Un exécutable de commande générique a retourné un résultat qui indique un échec.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_FILE_HASH_MISSING"></span><span id="error_sxs_file_hash_missing"></span>**ERREUR \_ de \_ hachage du fichier SxS \_ \_ manquant**
</dt> <dd> <dl> <dt>

14110 (0x371E)
</dt> <dt>



Il manque des informations de vérification de fichier dans le manifeste d’un composant.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_INVALID_CHANNEL_PATH"></span><span id="error_evt_invalid_channel_path"></span>**ERREUR \_ evt \_ \_ chemin de canal non valide \_**
</dt> <dd> <dl> <dt>

15000 (0x3A98)
</dt> <dt>



Le chemin d’accès au canal spécifié n’est pas valide.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_INVALID_QUERY"></span><span id="error_evt_invalid_query"></span>**ERREUR \_ evt \_ requête non valide \_**
</dt> <dd> <dl> <dt>

15001 (0x3A99)
</dt> <dt>



La requête spécifiée n’est pas valide.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_PUBLISHER_METADATA_NOT_FOUND"></span><span id="error_evt_publisher_metadata_not_found"></span>**ERREUR \_ evt \_ métadonnées du serveur de publication \_ \_ \_ introuvables**
</dt> <dd> <dl> <dt>

15002 (0x3A9A)
</dt> <dt>



Les métadonnées du serveur de publication sont introuvables dans la ressource.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_EVENT_TEMPLATE_NOT_FOUND"></span><span id="error_evt_event_template_not_found"></span>**le \_ modèle d’événement d’erreur evt est \_ \_ \_ \_ introuvable**
</dt> <dd> <dl> <dt>

15003 (0x3A9B)
</dt> <dt>



Le modèle d’une définition d’événement est introuvable dans la ressource (erreur = %1).


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_INVALID_PUBLISHER_NAME"></span><span id="error_evt_invalid_publisher_name"></span>**ERREUR \_ evt \_ \_ nom d’éditeur non valide \_**
</dt> <dd> <dl> <dt>

15004 (0x3A9C)
</dt> <dt>



Le nom du serveur de publication spécifié n’est pas valide.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_INVALID_EVENT_DATA"></span><span id="error_evt_invalid_event_data"></span>**ERREUR \_ evt \_ \_ données d’événement non valides \_**
</dt> <dd> <dl> <dt>

15005 (0x3A9D)
</dt> <dt>



Les données d’événement générées par le serveur de publication ne sont pas compatibles avec la définition du modèle d’événement dans le manifeste de l’éditeur.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_CHANNEL_NOT_FOUND"></span><span id="error_evt_channel_not_found"></span>**ERREUR \_ de \_ canal \_ evt \_ introuvable**
</dt> <dd> <dl> <dt>

15007 (0x3A9F)
</dt> <dt>



Le canal spécifié est introuvable. Vérifiez la configuration du canal.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_MALFORMED_XML_TEXT"></span><span id="error_evt_malformed_xml_text"></span>**ERREUR \_ evt \_ \_ texte XML mal formé \_**
</dt> <dd> <dl> <dt>

15008 (0x3AA0)
</dt> <dt>



Le texte XML spécifié n’est pas correctement formé. Pour plus d’informations, consultez erreur étendue.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_SUBSCRIPTION_TO_DIRECT_CHANNEL"></span><span id="error_evt_subscription_to_direct_channel"></span>**ERREUR \_ evt \_ abonnement \_ au \_ \_ canal direct**
</dt> <dd> <dl> <dt>

15009 (0x3AA1)
</dt> <dt>



L’appelant tente de s’abonner à un canal direct qui n’est pas autorisé. Les événements d’un canal direct accèdent directement à un fichier journal et ne peuvent pas être abonnés à.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_CONFIGURATION_ERROR"></span><span id="error_evt_configuration_error"></span>**erreur de configuration de l’erreur \_ evt \_ \_**
</dt> <dd> <dl> <dt>

15010 (0x3AA2)
</dt> <dt>



Erreur de configuration.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_QUERY_RESULT_STALE"></span><span id="error_evt_query_result_stale"></span>**ERREUR \_ evt \_ résultat de la requête \_ \_ obsolète**
</dt> <dd> <dl> <dt>

15011 (0x3AA3)
</dt> <dt>



Le résultat de la requête est obsolète/non valide. Cela peut être dû au fait que le journal est effacé ou basculé après la création du résultat de la requête. Les utilisateurs doivent gérer ce code en libérant l’objet de résultat de la requête et en réémettant la requête.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_QUERY_RESULT_INVALID_POSITION"></span><span id="error_evt_query_result_invalid_position"></span>**ERREUR \_ evt \_ résultat de la requête- \_ \_ position non valide \_**
</dt> <dd> <dl> <dt>

15012 (0x3AA4)
</dt> <dt>



Le résultat de la requête est actuellement à une position non valide.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_NON_VALIDATING_MSXML"></span><span id="error_evt_non_validating_msxml"></span>**ERREUR \_ evt \_ non \_ validant \_ MSXML**
</dt> <dd> <dl> <dt>

15013 (0x3AA5)
</dt> <dt>



la MSXML inscrite ne prend pas en charge la validation.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_FILTER_ALREADYSCOPED"></span><span id="error_evt_filter_alreadyscoped"></span>**ERREUR \_ evt \_ Filter \_ ALREADYSCOPED**
</dt> <dd> <dl> <dt>

15014 (0x3AA6)
</dt> <dt>



Une expression ne peut être suivie que par une modification de l’opération d’étendue si elle correspond à un ensemble de nœuds et qu’elle ne fait pas déjà partie d’une autre modification de l’opération d’étendue.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_FILTER_NOTELTSET"></span><span id="error_evt_filter_noteltset"></span>**ERREUR \_ evt \_ Filter \_ NOTELTSET**
</dt> <dd> <dl> <dt>

15015 (0x3AA7)
</dt> <dt>



Impossible d’effectuer une opération d’étape à partir d’un terme qui ne représente pas un ensemble d’éléments.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_FILTER_INVARG"></span><span id="error_evt_filter_invarg"></span>**ERREUR \_ evt \_ Filter \_ INVARG**
</dt> <dd> <dl> <dt>

15016 (0x3AA8)
</dt> <dt>



Les arguments côté gauche des opérateurs binaires doivent être des attributs, des nœuds ou des variables et les arguments de la partie droite doivent être des constantes.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_FILTER_INVTEST"></span><span id="error_evt_filter_invtest"></span>**ERREUR \_ evt \_ Filter \_ INVTEST**
</dt> <dd> <dl> <dt>

15017 (0x3AA9)
</dt> <dt>



Une opération d’étape doit impliquer un test de nœud ou, dans le cas d’un prédicat, une expression algébrique sur laquelle tester chaque nœud de l’ensemble de nœuds identifié par l’ensemble de nœuds précédent peut être évaluée.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_FILTER_INVTYPE"></span><span id="error_evt_filter_invtype"></span>**ERREUR \_ evt \_ Filter \_ INVTYPE**
</dt> <dd> <dl> <dt>

15018 (0x3AAA)
</dt> <dt>



Ce type de données n’est actuellement pas pris en charge.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_FILTER_PARSEERR"></span><span id="error_evt_filter_parseerr"></span>**ERREUR \_ evt \_ Filter \_ PARSEERR**
</dt> <dd> <dl> <dt>

15019 (0x3AAB)
</dt> <dt>



Une erreur de syntaxe s’est produite à la position %1 ! d !.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_FILTER_UNSUPPORTEDOP"></span><span id="error_evt_filter_unsupportedop"></span>**ERREUR \_ evt \_ Filter \_ UNSUPPORTEDOP**
</dt> <dd> <dl> <dt>

15020 (0x3AAC)
</dt> <dt>



Cet opérateur n’est pas pris en charge par cette implémentation du filtre.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_FILTER_UNEXPECTEDTOKEN"></span><span id="error_evt_filter_unexpectedtoken"></span>**ERREUR \_ evt \_ Filter \_ UNEXPECTEDTOKEN**
</dt> <dd> <dl> <dt>

15021 (0x3AAD)
</dt> <dt>



Le jeton rencontré était inattendu.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_INVALID_OPERATION_OVER_ENABLED_DIRECT_CHANNEL"></span><span id="error_evt_invalid_operation_over_enabled_direct_channel"></span>**ERREUR \_ evt \_ opération non valide \_ \_ sur le \_ \_ canal direct activé \_**
</dt> <dd> <dl> <dt>

15022 (0x3AAE)
</dt> <dt>



L’opération demandée ne peut pas être effectuée sur un canal direct activé. Le canal doit d’abord être désactivé avant d’effectuer l’opération demandée.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_INVALID_CHANNEL_PROPERTY_VALUE"></span><span id="error_evt_invalid_channel_property_value"></span>**ERREUR \_ evt \_ \_ valeur de \_ propriété de canal non valide \_**
</dt> <dd> <dl> <dt>

15023 (0x3AAF)
</dt> <dt>



Propriété de canal %1 ! s ! contient une valeur non valide. Le type de la valeur n’est pas valide, est en dehors de la plage valide, ne peut pas être mis à jour ou n’est pas pris en charge par ce type de canal.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_INVALID_PUBLISHER_PROPERTY_VALUE"></span><span id="error_evt_invalid_publisher_property_value"></span>**ERREUR \_ evt \_ valeur de la \_ propriété Publisher non valide \_ \_**
</dt> <dd> <dl> <dt>

15024 (0x3AB0)
</dt> <dt>



Publisher la propriété %1 ! s ! contient une valeur non valide. Le type de la valeur n’est pas valide, est en dehors de la plage valide, ne peut pas être mis à jour ou n’est pas pris en charge par ce type de serveur de publication.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_CHANNEL_CANNOT_ACTIVATE"></span><span id="error_evt_channel_cannot_activate"></span>**ERREUR \_ \_ Impossible d' \_ \_ activer le canal evt**
</dt> <dd> <dl> <dt>

15025 (0x3AB1)
</dt> <dt>



L’activation du canal échoue.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_FILTER_TOO_COMPLEX"></span><span id="error_evt_filter_too_complex"></span>**ERREUR \_ de \_ filtre evt \_ trop \_ complexe**
</dt> <dd> <dl> <dt>

15026 (0x3AB2)
</dt> <dt>



L’expression XPath a dépassé la complexité prise en charge. Symplifyz-le ou fractionnez-le en deux ou plusieurs expressions simples.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_MESSAGE_NOT_FOUND"></span><span id="error_evt_message_not_found"></span>**MESSAGE d’erreur \_ evt \_ \_ \_ introuvable**
</dt> <dd> <dl> <dt>

15027 (0x3AB3)
</dt> <dt>



la ressource de message est présente, mais le message est introuvable dans la table de chaînes/messages.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_MESSAGE_ID_NOT_FOUND"></span><span id="error_evt_message_id_not_found"></span>**ERREUR \_ evt \_ ID de message \_ \_ \_ introuvable**
</dt> <dd> <dl> <dt>

15028 (0x3AB4)
</dt> <dt>



L’ID de message du message souhaité est introuvable.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_UNRESOLVED_VALUE_INSERT"></span><span id="error_evt_unresolved_value_insert"></span>**ERREUR \_ evt \_ - \_ Insérer une valeur non résolue \_**
</dt> <dd> <dl> <dt>

15029 (0x3AB5)
</dt> <dt>



La chaîne de substitution pour l’instruction INSERT index (%1) est introuvable.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_UNRESOLVED_PARAMETER_INSERT"></span><span id="error_evt_unresolved_parameter_insert"></span>**ERREUR \_ evt \_ - \_ Insérer un paramètre non résolu \_**
</dt> <dd> <dl> <dt>

15030 (0x3AB6)
</dt> <dt>



La chaîne de description de la référence de paramètre (%1) est introuvable.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_MAX_INSERTS_REACHED"></span><span id="error_evt_max_inserts_reached"></span>**ERREUR \_ evt \_ nombre maximal d' \_ insertions \_ atteint**
</dt> <dd> <dl> <dt>

15031 (0x3AB7)
</dt> <dt>



Le nombre maximal de remplacements a été atteint.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_EVENT_DEFINITION_NOT_FOUND"></span><span id="error_evt_event_definition_not_found"></span>**ERREUR \_ evt \_ définition de l’événement \_ \_ \_ introuvable**
</dt> <dd> <dl> <dt>

15032 (0x3AB8)
</dt> <dt>



La définition de l’événement est introuvable pour l’ID d’événement (%1).


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_MESSAGE_LOCALE_NOT_FOUND"></span><span id="error_evt_message_locale_not_found"></span>**ERREUR \_ evt \_ message \_ local \_ \_ introuvable**
</dt> <dd> <dl> <dt>

15033 (0x3AB9)
</dt> <dt>



La ressource spécifique aux paramètres régionaux pour le message souhaité n’est pas présente.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_VERSION_TOO_OLD"></span><span id="error_evt_version_too_old"></span>**ERREUR \_ evt \_ version \_ trop \_ ancienne**
</dt> <dd> <dl> <dt>

15034 (0x3ABA)
</dt> <dt>



La ressource est trop ancienne pour être compatible.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_VERSION_TOO_NEW"></span><span id="error_evt_version_too_new"></span>**ERREUR \_ evt \_ version \_ insuffisante \_**
</dt> <dd> <dl> <dt>

15035 (0x3ABB)
</dt> <dt>



La ressource est trop nouvelle pour être compatible.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_CANNOT_OPEN_CHANNEL_OF_QUERY"></span><span id="error_evt_cannot_open_channel_of_query"></span>**ERREUR \_ evt \_ Impossible \_ d’ouvrir le \_ canal \_ de la \_ requête**
</dt> <dd> <dl> <dt>

15036 (0x3ABC)
</dt> <dt>



Le canal à l’index %1 ! d ! Impossible d’ouvrir la requête.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_PUBLISHER_DISABLED"></span><span id="error_evt_publisher_disabled"></span>**ERREUR \_ evt serveur de \_ publication \_ désactivé**
</dt> <dd> <dl> <dt>

15037 (0x3ABD)
</dt> <dt>



Le serveur de publication a été désactivé et sa ressource n’est pas disponible. Cela se produit généralement lorsque le serveur de publication est en cours de désinstallation ou de mise à niveau.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_FILTER_OUT_OF_RANGE"></span><span id="error_evt_filter_out_of_range"></span>**ERREUR \_ \_ de filtre \_ evt \_ hors \_ limites**
</dt> <dd> <dl> <dt>

15038 (0x3ABE)
</dt> <dt>



Tentative de création d’un type numérique qui est en dehors de sa plage valide.


</dt> </dl> </dd> <dt>

<span id="ERROR_EC_SUBSCRIPTION_CANNOT_ACTIVATE"></span><span id="error_ec_subscription_cannot_activate"></span>**ERREUR \_ \_ Impossible d' \_ \_ activer l’abonnement EC**
</dt> <dd> <dl> <dt>

15080 (0x3AE8)
</dt> <dt>



L’activation de l’abonnement échoue.


</dt> </dl> </dd> <dt>

<span id="ERROR_EC_LOG_DISABLED"></span><span id="error_ec_log_disabled"></span>**ERREUR \_ de \_ journalisation EC \_ désactivée**
</dt> <dd> <dl> <dt>

15081 (0x3AE9)
</dt> <dt>



Le journal de l’abonnement est dans un état désactivé et ne peut pas être utilisé pour transférer des événements à. Le journal doit d’abord être activé pour que l’abonnement puisse être activé.


</dt> </dl> </dd> <dt>

<span id="ERROR_EC_CIRCULAR_FORWARDING"></span><span id="error_ec_circular_forwarding"></span>**ERREUR \_ de \_ transfert circulaire ce \_**
</dt> <dd> <dl> <dt>

15082 (0x3AEA)
</dt> <dt>



Lors du transfert d’événements de l’ordinateur local à lui-même, la requête de l’abonnement ne peut pas contenir le journal cible de l’abonnement.


</dt> </dl> </dd> <dt>

<span id="ERROR_EC_CREDSTORE_FULL"></span><span id="error_ec_credstore_full"></span>**ERREUR \_ EC \_ CREDSTORE \_ Full**
</dt> <dd> <dl> <dt>

15083 (0x3AEB)
</dt> <dt>



La Banque d’informations d’identification utilisée pour enregistrer les informations d’identification est complète.


</dt> </dl> </dd> <dt>

<span id="ERROR_EC_CRED_NOT_FOUND"></span><span id="error_ec_cred_not_found"></span>**ERREUR \_ EC \_ \_ non \_ trouvé**
</dt> <dd> <dl> <dt>

15084 (0x3AEC)
</dt> <dt>



Les informations d’identification utilisées par cet abonnement sont introuvables dans la Banque d’informations d’identification.


</dt> </dl> </dd> <dt>

<span id="ERROR_EC_NO_ACTIVE_CHANNEL"></span><span id="error_ec_no_active_channel"></span>**ERREUR \_ EC \_ non \_ active \_ Channel**
</dt> <dd> <dl> <dt>

15085 (0x3AED)
</dt> <dt>



Aucun canal actif n’a été trouvé pour la requête.


</dt> </dl> </dd> <dt>

<span id="ERROR_MUI_FILE_NOT_FOUND"></span><span id="error_mui_file_not_found"></span>**\_fichier MUI \_ \_ \_ introuvable**
</dt> <dd> <dl> <dt>

15100 (0x3AFC)
</dt> <dt>



Le chargeur de ressources n’a pas pu trouver le fichier MUI.


</dt> </dl> </dd> <dt>

<span id="ERROR_MUI_INVALID_FILE"></span><span id="error_mui_invalid_file"></span>**ERREUR \_ de \_ fichier non valide MUI \_**
</dt> <dd> <dl> <dt>

15101 (0x3AFD)
</dt> <dt>



Le chargeur de ressources n’a pas pu charger le fichier MUI car le fichier n’a pas réussi à réussir la validation.


</dt> </dl> </dd> <dt>

<span id="ERROR_MUI_INVALID_RC_CONFIG"></span><span id="error_mui_invalid_rc_config"></span>**ERREUR \_ de \_ \_ configuration RC non valide pour MUI \_**
</dt> <dd> <dl> <dt>

15102 (0x3AFE)
</dt> <dt>



Le manifeste RC est endommagé avec des données de garbage collection ou une version non prise en charge ou un élément requis manquant.


</dt> </dl> </dd> <dt>

<span id="ERROR_MUI_INVALID_LOCALE_NAME"></span><span id="error_mui_invalid_locale_name"></span>**ERREUR \_ MUI \_ \_ nom de paramètres régionaux non valide \_**
</dt> <dd> <dl> <dt>

15103 (0x3AFF)
</dt> <dt>



Le manifeste RC a un nom de culture non valide.


</dt> </dl> </dd> <dt>

<span id="ERROR_MUI_INVALID_ULTIMATEFALLBACK_NAME"></span><span id="error_mui_invalid_ultimatefallback_name"></span>**ERREUR \_ ULTIMATEFALLBACK nom de l’interface MUI \_ non valide \_ \_**
</dt> <dd> <dl> <dt>

15104 (0x3B00)
</dt> <dt>



Le manifeste RC a un nom de ultimatefallback non valide.


</dt> </dl> </dd> <dt>

<span id="ERROR_MUI_FILE_NOT_LOADED"></span><span id="error_mui_file_not_loaded"></span>**ERREUR lors du chargement du \_ \_ fichier MUI \_ \_**
</dt> <dd> <dl> <dt>

15105 (0x3B01)
</dt> <dt>



Le cache du chargeur de ressources n’a pas d’entrée MUI chargée.


</dt> </dl> </dd> <dt>

<span id="ERROR_RESOURCE_ENUM_USER_STOP"></span><span id="error_resource_enum_user_stop"></span>**arrêt de l' \_ énumération des ressources d’erreur \_ \_ \_**
</dt> <dd> <dl> <dt>

15106 (0x3B02)
</dt> <dt>



L’utilisateur a arrêté l’énumération des ressources.


</dt> </dl> </dd> <dt>

<span id="ERROR_MUI_INTLSETTINGS_UILANG_NOT_INSTALLED"></span><span id="error_mui_intlsettings_uilang_not_installed"></span>**ERREUR \_ MUI \_ INTLSETTINGS \_ UILANG \_ non \_ installé**
</dt> <dd> <dl> <dt>

15107 (0x3B03)
</dt> <dt>



Échec de l’installation de la langue de l’interface utilisateur.


</dt> </dl> </dd> <dt>

<span id="ERROR_MUI_INTLSETTINGS_INVALID_LOCALE_NAME"></span><span id="error_mui_intlsettings_invalid_locale_name"></span>**ERREUR \_ MUI \_ INTLSETTINGS \_ \_ nom de paramètres régionaux non valide \_**
</dt> <dd> <dl> <dt>

15108 (0x3B04)
</dt> <dt>



Échec de l’installation des paramètres régionaux.


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_RUNTIME_NO_DEFAULT_OR_NEUTRAL_RESOURCE"></span><span id="error_mrm_runtime_no_default_or_neutral_resource"></span>**ERREUR \_ MRM \_ Runtime \_ sans \_ ressource par défaut \_ ou \_ neutre \_**
</dt> <dd> <dl> <dt>

15110 (0x3B06)
</dt> <dt>



Une ressource n’a pas de valeur par défaut ou neutre.


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_INVALID_PRICONFIG"></span><span id="error_mrm_invalid_priconfig"></span>**ERREUR \_ MRM \_ fichier priconfig non valide \_**
</dt> <dd> <dl> <dt>

15111 (0x3B07)
</dt> <dt>



Fichier de configuration PRI non valide.


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_INVALID_FILE_TYPE"></span><span id="error_mrm_invalid_file_type"></span>**ERREUR \_ MRM \_ \_ type de fichier non valide \_**
</dt> <dd> <dl> <dt>

15112 (0x3B08)
</dt> <dt>



Type de fichier non valide.


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_UNKNOWN_QUALIFIER"></span><span id="error_mrm_unknown_qualifier"></span>**ERREUR \_ MRM \_ \_ qualificateur inconnu**
</dt> <dd> <dl> <dt>

15113 (0x3B09)
</dt> <dt>



Qualificateur inconnu.


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_INVALID_QUALIFIER_VALUE"></span><span id="error_mrm_invalid_qualifier_value"></span>**ERREUR \_ MRM \_ valeur de qualificateur non valide \_ \_**
</dt> <dd> <dl> <dt>

15114 (0x3B0A)
</dt> <dt>



Valeur de qualificateur non valide.


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_NO_CANDIDATE"></span><span id="error_mrm_no_candidate"></span>**ERREUR \_ MRM \_ aucun \_ candidat**
</dt> <dd> <dl> <dt>

15115 (0x3B0B)
</dt> <dt>



Aucun candidat n’a été trouvé.


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_NO_MATCH_OR_DEFAULT_CANDIDATE"></span><span id="error_mrm_no_match_or_default_candidate"></span>**ERREUR \_ MRM \_ aucune \_ correspondance \_ ou \_ candidat par défaut \_**
</dt> <dd> <dl> <dt>

15116 (0x3B0C)
</dt> <dt>



ResourceMap ou NamedResource a un élément qui n’a pas de ressource par défaut ou neutre..


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_RESOURCE_TYPE_MISMATCH"></span><span id="error_mrm_resource_type_mismatch"></span>**ERREUR \_ d' \_ \_ incompatibilité de type de ressource MRM \_**
</dt> <dd> <dl> <dt>

15117 (0x3B0D)
</dt> <dt>



Type de ResourceCandidate non valide.


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_DUPLICATE_MAP_NAME"></span><span id="error_mrm_duplicate_map_name"></span>**ERREUR \_ MRM \_ \_ nom de mappage dupliqué \_**
</dt> <dd> <dl> <dt>

15118 (0x3B0E)
</dt> <dt>



Mappage de ressources en double.


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_DUPLICATE_ENTRY"></span><span id="error_mrm_duplicate_entry"></span>**ERREUR \_ MRM de l' \_ entrée dupliquée \_**
</dt> <dd> <dl> <dt>

15119 (0x3B0F)
</dt> <dt>



Entrée dupliquée.


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_INVALID_RESOURCE_IDENTIFIER"></span><span id="error_mrm_invalid_resource_identifier"></span>**ERREUR \_ MRM \_ \_ identificateur de ressource non valide \_**
</dt> <dd> <dl> <dt>

15120 (0x3B10)
</dt> <dt>



Identificateur de ressource non valide.


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_FILEPATH_TOO_LONG"></span><span id="error_mrm_filepath_too_long"></span>**erreur MRM le chemin d’erreur est \_ \_ \_ trop \_ long**
</dt> <dd> <dl> <dt>

15121 (0x3B11)
</dt> <dt>



FilePath trop long.


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_UNSUPPORTED_DIRECTORY_TYPE"></span><span id="error_mrm_unsupported_directory_type"></span>**ERREUR \_ MRM \_ type de répertoire non pris en charge \_ \_**
</dt> <dd> <dl> <dt>

15122 (0x3B12)
</dt> <dt>



Type de répertoire non pris en charge.


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_INVALID_PRI_FILE"></span><span id="error_mrm_invalid_pri_file"></span>**ERREUR \_ MRM \_ \_ fichier PRI non valide \_**
</dt> <dd> <dl> <dt>

15126 (0x3B16)
</dt> <dt>



Fichier PRI non valide.


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_NAMED_RESOURCE_NOT_FOUND"></span><span id="error_mrm_named_resource_not_found"></span>**ERREUR \_ MRM \_ nommée \_ ressource \_ \_ introuvable**
</dt> <dd> <dl> <dt>

15127 (0x3B17)
</dt> <dt>



NamedResource introuvable.


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_MAP_NOT_FOUND"></span><span id="error_mrm_map_not_found"></span>**ERREUR \_ de \_ mappage de MRM \_ \_ introuvable**
</dt> <dd> <dl> <dt>

15135 (0x3B1F)
</dt> <dt>



ResourceMap introuvable.


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_UNSUPPORTED_PROFILE_TYPE"></span><span id="error_mrm_unsupported_profile_type"></span>**ERREUR \_ MRM \_ type de profil non pris en charge \_ \_**
</dt> <dd> <dl> <dt>

15136 (0x3B20)
</dt> <dt>



Type de profil MRT non pris en charge.


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_INVALID_QUALIFIER_OPERATOR"></span><span id="error_mrm_invalid_qualifier_operator"></span>**ERREUR \_ MRM \_ opérateur de qualificateur non valide \_ \_**
</dt> <dd> <dl> <dt>

15137 (0x3B21)
</dt> <dt>



Opérateur de qualificateur non valide.


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_INDETERMINATE_QUALIFIER_VALUE"></span><span id="error_mrm_indeterminate_qualifier_value"></span>**ERREUR \_ MRM \_ \_ valeur du qualificateur indéterminé \_**
</dt> <dd> <dl> <dt>

15138 (0x3B22)
</dt> <dt>



Impossible de déterminer la valeur du qualificateur ou la valeur du qualificateur n’a pas été définie.


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_AUTOMERGE_ENABLED"></span><span id="error_mrm_automerge_enabled"></span>**ERREUR \_ de \_ fusion automatique MRM \_ activée**
</dt> <dd> <dl> <dt>

15139 (0x3B23)
</dt> <dt>



La fusion automatique est activée dans le fichier PRI.


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_TOO_MANY_RESOURCES"></span><span id="error_mrm_too_many_resources"></span>**ERREUR \_ MRM \_ trop \_ de \_ ressources**
</dt> <dd> <dl> <dt>

15140 (0x3B24)
</dt> <dt>



Trop de ressources définies pour le package.


</dt> </dl> </dd> <dt>

<span id="ERROR_MCA_INVALID_CAPABILITIES_STRING"></span><span id="error_mca_invalid_capabilities_string"></span>**ERREUR \_ MCA \_ \_ chaîne de fonctionnalités non valides \_**
</dt> <dd> <dl> <dt>

15200 (0x3B60)
</dt> <dt>



Le moniteur a renvoyé une chaîne de fonctionnalités DDC/CI qui n’était pas conforme à la spécification ACCESS. bus 3,0, DDC/CI 1,1 ou MCCS 2 révision 1.


</dt> </dl> </dd> <dt>

<span id="ERROR_MCA_INVALID_VCP_VERSION"></span><span id="error_mca_invalid_vcp_version"></span>**ERREUR \_ MCA \_ \_ version du VCP non valide \_**
</dt> <dd> <dl> <dt>

15201 (0x3B61)
</dt> <dt>



Le code VCP de la version du moniteur VCP (0xDF) a retourné une valeur de version non valide.


</dt> </dl> </dd> <dt>

<span id="ERROR_MCA_MONITOR_VIOLATES_MCCS_SPECIFICATION"></span><span id="error_mca_monitor_violates_mccs_specification"></span>**une erreur \_ MCA \_ Monitor enfreint la \_ \_ \_ spécification MCCS**
</dt> <dd> <dl> <dt>

15202 (0x3B62)
</dt> <dt>



Le moniteur n’est pas conforme à la spécification MCCS qu’il prétend prendre en charge.


</dt> </dl> </dd> <dt>

<span id="ERROR_MCA_MCCS_VERSION_MISMATCH"></span><span id="error_mca_mccs_version_mismatch"></span>**ERREUR \_ d' \_ \_ incompatibilité de version de MCA MCCS \_**
</dt> <dd> <dl> <dt>

15203 (0x3B63)
</dt> <dt>



La version MCCS de la fonctionnalité MCCS ver d’un moniteur \_ ne correspond pas à la version MCCS que le moniteur signale lorsque le code VCP version (0xDF) VCP est utilisé.


</dt> </dl> </dd> <dt>

<span id="ERROR_MCA_UNSUPPORTED_MCCS_VERSION"></span><span id="error_mca_unsupported_mccs_version"></span>**ERREUR \_ de \_ \_ version MCCS non prise en charge par MCA \_**
</dt> <dd> <dl> <dt>

15204 (0x3B64)
</dt> <dt>



L’API de configuration de l’analyse fonctionne uniquement avec les analyses qui prennent en charge la spécification MCCS 1,0, la spécification MCCS 2,0 ou la spécification MCCS 2,0 révision 1.


</dt> </dl> </dd> <dt>

<span id="ERROR_MCA_INTERNAL_ERROR"></span><span id="error_mca_internal_error"></span>**ERREUR \_ MCA erreur \_ interne \_**
</dt> <dd> <dl> <dt>

15205 (0x3B65)
</dt> <dt>



Une erreur de l’API de configuration de l’analyse interne s’est produite.


</dt> </dl> </dd> <dt>

<span id="ERROR_MCA_INVALID_TECHNOLOGY_TYPE_RETURNED"></span><span id="error_mca_invalid_technology_type_returned"></span>**ERREUR \_ MCA \_ type de technologie non valide \_ \_ \_ retourné**
</dt> <dd> <dl> <dt>

15206 (0x3B66)
</dt> <dt>



Le moniteur a retourné un type de technologie d’analyse non valide. CRT, plasma et LCD (TFT) sont des exemples de types de technologies de surveillance. Cette erreur signifie que le moniteur n’est pas conforme à la spécification MCCS 2,0 ou MCCS 2,0 révision 1.


</dt> </dl> </dd> <dt>

<span id="ERROR_MCA_UNSUPPORTED_COLOR_TEMPERATURE"></span><span id="error_mca_unsupported_color_temperature"></span>**ERREUR \_ MCA \_ température de couleur non prise en charge \_ \_**
</dt> <dd> <dl> <dt>

15207 (0x3B67)
</dt> <dt>



L’appelant de [**SetMonitorColorTemperature**](/windows/win32/api/highlevelmonitorconfigurationapi/nf-highlevelmonitorconfigurationapi-setmonitorcolortemperature) a spécifié une température de couleur que le moniteur en cours ne prenait pas en charge. Cette erreur signifie que le moniteur n’est pas conforme à la spécification MCCS 2,0 ou MCCS 2,0 révision 1.


</dt> </dl> </dd> <dt>

<span id="ERROR_AMBIGUOUS_SYSTEM_DEVICE"></span><span id="error_ambiguous_system_device"></span>**ERREUR \_ de \_ périphérique système ambigu \_**
</dt> <dd> <dl> <dt>

15250 (0x3B92)
</dt> <dt>



L’appareil système demandé ne peut pas être identifié en raison de plusieurs périphériques indifférenciables susceptibles de correspondre aux critères d’identification.


</dt> </dl> </dd> <dt>

<span id="ERROR_SYSTEM_DEVICE_NOT_FOUND"></span><span id="error_system_device_not_found"></span>**\_périphérique système d’erreur \_ \_ \_ introuvable**
</dt> <dd> <dl> <dt>

15299 (0x3BC3)
</dt> <dt>



Le périphérique système demandé est introuvable.


</dt> </dl> </dd> <dt>

<span id="ERROR_HASH_NOT_SUPPORTED"></span><span id="error_hash_not_supported"></span>**hachage d’erreur \_ \_ non \_ pris en charge**
</dt> <dd> <dl> <dt>

15300 (0x3BC4)
</dt> <dt>



La génération de hachage pour la version de hachage et le type de hachage spécifiés n’est pas activée sur le serveur.


</dt> </dl> </dd> <dt>

<span id="ERROR_HASH_NOT_PRESENT"></span><span id="error_hash_not_present"></span>**\_hachage d' \_ erreur \_ absent**
</dt> <dd> <dl> <dt>

15301 (0x3BC5)
</dt> <dt>



Le hachage demandé à partir du serveur n’est pas disponible ou n’est plus valide.


</dt> </dl> </dd> <dt>

<span id="ERROR_SECONDARY_IC_PROVIDER_NOT_REGISTERED"></span><span id="error_secondary_ic_provider_not_registered"></span>**ERREUR \_ \_ fournisseur IC \_ secondaire \_ non \_ inscrit**
</dt> <dd> <dl> <dt>

15321 (0x3BD9)
</dt> <dt>



L’instance de contrôleur d’interruption secondaire qui gère l’interruption spécifiée n’est pas inscrite.


</dt> </dl> </dd> <dt>

<span id="ERROR_GPIO_CLIENT_INFORMATION_INVALID"></span><span id="error_gpio_client_information_invalid"></span>**ERREUR \_ d' \_ informations du client GPIO \_ \_ non valide**
</dt> <dd> <dl> <dt>

15322 (0x3BDA)
</dt> <dt>



Les informations fournies par le pilote du client GPIO ne sont pas valides.


</dt> </dl> </dd> <dt>

<span id="ERROR_GPIO_VERSION_NOT_SUPPORTED"></span><span id="error_gpio_version_not_supported"></span>**ERREUR \_ \_ version GPIO \_ non \_ prise en charge**
</dt> <dd> <dl> <dt>

15323 (0x3BDB)
</dt> <dt>



La version spécifiée par le pilote du client GPIO n’est pas prise en charge.


</dt> </dl> </dd> <dt>

<span id="ERROR_GPIO_INVALID_REGISTRATION_PACKET"></span><span id="error_gpio_invalid_registration_packet"></span>**ERREUR \_ GPIO \_ \_ paquet d’inscription non valide \_**
</dt> <dd> <dl> <dt>

15324 (0x3BDC)
</dt> <dt>



Le paquet d’inscription fourni par le pilote du client GPIO n’est pas valide.


</dt> </dl> </dd> <dt>

<span id="ERROR_GPIO_OPERATION_DENIED"></span><span id="error_gpio_operation_denied"></span>**ERREUR de l' \_ \_ opération GPIO \_ refusée**
</dt> <dd> <dl> <dt>

15325 (0x3BDD)
</dt> <dt>



L’opération demandée n’est pas prise en charge pour le handle spécifié.


</dt> </dl> </dd> <dt>

<span id="ERROR_GPIO_INCOMPATIBLE_CONNECT_MODE"></span><span id="error_gpio_incompatible_connect_mode"></span>**ERREUR \_ GPIO \_ mode de \_ connexion incompatible \_**
</dt> <dd> <dl> <dt>

15326 (0x3BDE)
</dt> <dt>



Le mode de connexion demandé est en conflit avec un mode existant sur une ou plusieurs des broches spécifiées.


</dt> </dl> </dd> <dt>

<span id="ERROR_GPIO_INTERRUPT_ALREADY_UNMASKED"></span><span id="error_gpio_interrupt_already_unmasked"></span>**ERREUR \_ GPIO \_ interruption \_ déjà \_ démasquée**
</dt> <dd> <dl> <dt>

15327 (0x3BDF)
</dt> <dt>



L’interruption demandée pour être démasquée n’est pas masquée.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANNOT_SWITCH_RUNLEVEL"></span><span id="error_cannot_switch_runlevel"></span>**l’erreur \_ ne peut pas \_ basculer \_ RUNLEVEL**
</dt> <dd> <dl> <dt>

15400 (0x3C28)
</dt> <dt>



Le commutateur de niveau d’exécution demandé ne peut pas être exécuté correctement.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_RUNLEVEL_SETTING"></span><span id="error_invalid_runlevel_setting"></span>**ERREUR \_ de \_ paramètre RUNLEVEL non valide \_**
</dt> <dd> <dl> <dt>

15401 (0x3C29)
</dt> <dt>



Le service a un paramètre de niveau d’exécution non valide. Le niveau d’exécution d’un service ne doit pas être supérieur au niveau d’exécution de ses services dépendants.


</dt> </dl> </dd> <dt>

<span id="ERROR_RUNLEVEL_SWITCH_TIMEOUT"></span><span id="error_runlevel_switch_timeout"></span>**ERREUR \_ de \_ \_ délai d’attente du commutateur RUNLEVEL**
</dt> <dd> <dl> <dt>

15402 (0x3C2A)
</dt> <dt>



Le commutateur de niveau d’exécution demandé ne peut pas être exécuté correctement, car un ou plusieurs services ne s’arrêteront pas ou ne redémarreront pas dans le délai spécifié.


</dt> </dl> </dd> <dt>

<span id="ERROR_RUNLEVEL_SWITCH_AGENT_TIMEOUT"></span><span id="error_runlevel_switch_agent_timeout"></span>**ERREUR \_ RUNLEVEL \_ du commutateur de \_ l’agent \_**
</dt> <dd> <dl> <dt>

15403 (0x3C2B)
</dt> <dt>



Un agent de commutation au niveau de l’exécution n’a pas répondu dans le délai imparti.


</dt> </dl> </dd> <dt>

<span id="ERROR_RUNLEVEL_SWITCH_IN_PROGRESS"></span><span id="error_runlevel_switch_in_progress"></span>**ERREUR \_ \_ de commutateur RUNLEVEL \_ en \_ cours**
</dt> <dd> <dl> <dt>

15404 (0x3C2C)
</dt> <dt>



Un commutateur au niveau de l’exécution est actuellement en cours.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVICES_FAILED_AUTOSTART"></span><span id="error_services_failed_autostart"></span>**\_échec du \_ \_ démarrage automatique des services d’erreur**
</dt> <dd> <dl> <dt>

15405 (0x3C2D)
</dt> <dt>



Un ou plusieurs services n’ont pas pu démarrer au cours de la phase de démarrage du service d’un commutateur de niveau d’exécution.


</dt> </dl> </dd> <dt>

<span id="ERROR_COM_TASK_STOP_PENDING"></span><span id="error_com_task_stop_pending"></span>**ERREUR d’arrêt de la \_ \_ tâche com \_ \_ en attente**
</dt> <dd> <dl> <dt>

15501 (0x3C8D)
</dt> <dt>



La demande d’arrêt de la tâche ne peut pas être effectuée immédiatement, car la tâche a besoin de plus de temps pour s’arrêter.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_OPEN_PACKAGE_FAILED"></span><span id="error_install_open_package_failed"></span>**ERREUR d’installation de l' \_ \_ ouverture du \_ package \_**
</dt> <dd> <dl> <dt>

15600 (0x3CF0)
</dt> <dt>



Impossible d’ouvrir le package.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_PACKAGE_NOT_FOUND"></span><span id="error_install_package_not_found"></span>**ERREUR lors de l' \_ installation du \_ package \_ \_ introuvable**
</dt> <dd> <dl> <dt>

15601 (0x3CF1)
</dt> <dt>



Le package est introuvable.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_INVALID_PACKAGE"></span><span id="error_install_invalid_package"></span>**ERREUR d’installation d’un \_ \_ package non valide \_**
</dt> <dd> <dl> <dt>

15602 (0x3CF2)
</dt> <dt>



Les données du package ne sont pas valides.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_RESOLVE_DEPENDENCY_FAILED"></span><span id="error_install_resolve_dependency_failed"></span>**échec de la résolution de l’erreur d’installation de la \_ \_ \_ dépendance \_**
</dt> <dd> <dl> <dt>

15603 (0x3CF3)
</dt> <dt>



Échec des mises à jour du package, de la dépendance ou de la validation des conflits.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_OUT_OF_DISK_SPACE"></span><span id="error_install_out_of_disk_space"></span>**ERREUR \_ \_ d’installation \_ de \_ l' \_ espace disque insuffisant**
</dt> <dd> <dl> <dt>

15604 (0x3CF4)
</dt> <dt>



L’espace disque est insuffisant sur votre ordinateur. Libérez de l’espace et réessayez.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_NETWORK_FAILURE"></span><span id="error_install_network_failure"></span>**ERREUR lors de l’installation d’une \_ \_ \_ défaillance réseau**
</dt> <dd> <dl> <dt>

15605 (0x3CF5)
</dt> <dt>



Un problème est survenu lors du téléchargement de votre produit.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_REGISTRATION_FAILURE"></span><span id="error_install_registration_failure"></span>**ERREUR \_ \_ d’échec d’enregistrement d’installation \_**
</dt> <dd> <dl> <dt>

15606 (0x3CF6)
</dt> <dt>



Le package n’a pas pu être inscrit.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_DEREGISTRATION_FAILURE"></span><span id="error_install_deregistration_failure"></span>**ERREUR \_ d’installation de \_ l’échec de l’inscription \_**
</dt> <dd> <dl> <dt>

15607 (0x3CF7)
</dt> <dt>



L’inscription du package n’a pas pu être annulée.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_CANCEL"></span><span id="error_install_cancel"></span>**ERREUR d' \_ installation \_ Annuler**
</dt> <dd> <dl> <dt>

15608 (0x3CF8)
</dt> <dt>



L’utilisateur a annulé la demande d’installation.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_FAILED"></span><span id="error_install_failed"></span>**échec de l' \_ installation \_**
</dt> <dd> <dl> <dt>

15609 (0x3CF9)
</dt> <dt>



Échec de l’installation. Veuillez contacter votre fournisseur de logiciels.


</dt> </dl> </dd> <dt>

<span id="ERROR_REMOVE_FAILED"></span><span id="error_remove_failed"></span>**échec de la suppression de l’erreur \_ \_**
</dt> <dd> <dl> <dt>

15610 (0x3CFA)
</dt> <dt>



Échec de la suppression. Veuillez contacter votre fournisseur de logiciels.


</dt> </dl> </dd> <dt>

<span id="ERROR_PACKAGE_ALREADY_EXISTS"></span><span id="error_package_already_exists"></span>**le \_ package d’erreurs \_ \_ existe déjà**
</dt> <dd> <dl> <dt>

15611 (0x3CFB)
</dt> <dt>



Le package fourni est déjà installé, et la réinstallation du package a été bloquée. Pour plus d’informations, consultez le journal des événements AppXDeployment-Server.


</dt> </dl> </dd> <dt>

<span id="ERROR_NEEDS_REMEDIATION"></span><span id="error_needs_remediation"></span>**ERREUR \_ nécessitant une \_ Correction**
</dt> <dd> <dl> <dt>

15612 (0x3CFC)
</dt> <dt>



Impossible de démarrer l’application. Essayez de réinstaller l’application pour résoudre le problème.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_PREREQUISITE_FAILED"></span><span id="error_install_prerequisite_failed"></span>**ERREUR lors de l’échec de l' \_ installation des \_ composants requis \_**
</dt> <dd> <dl> <dt>

15613 (0x3CFD)
</dt> <dt>



Un composant requis pour une installation n’a pas pu être satisfait.


</dt> </dl> </dd> <dt>

<span id="ERROR_PACKAGE_REPOSITORY_CORRUPTED"></span><span id="error_package_repository_corrupted"></span>**DÉPÔT de packages d’erreurs \_ \_ \_ endommagé**
</dt> <dd> <dl> <dt>

15614 (0x3CFE)
</dt> <dt>



Le référentiel du package est endommagé.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_POLICY_FAILURE"></span><span id="error_install_policy_failure"></span>**ERREUR lors de l’installation de la \_ \_ stratégie \_**
</dt> <dd> <dl> <dt>

15615 (0x3CFF)
</dt> <dt>



pour installer cette application, vous avez besoin d’une licence de développeur Windows ou d’un système compatible chargement.


</dt> </dl> </dd> <dt>

<span id="ERROR_PACKAGE_UPDATING"></span><span id="error_package_updating"></span>**\_ \_ mise à jour du package d’erreurs**
</dt> <dd> <dl> <dt>

15616 (0x3D00)
</dt> <dt>



L’application ne peut pas être démarrée car elle est en cours de mise à jour.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEPLOYMENT_BLOCKED_BY_POLICY"></span><span id="error_deployment_blocked_by_policy"></span>**ERREUR \_ \_ de déploiement bloqué \_ par la \_ stratégie**
</dt> <dd> <dl> <dt>

15617 (0x3D01)
</dt> <dt>



L’opération de déploiement de package est bloquée par la stratégie. Contactez votre administrateur système.


</dt> </dl> </dd> <dt>

<span id="ERROR_PACKAGES_IN_USE"></span><span id="error_packages_in_use"></span>**\_packages \_ d’erreurs en cours d' \_ utilisation**
</dt> <dd> <dl> <dt>

15618 (0x3D02)
</dt> <dt>



Le package n’a pas pu être installé car les ressources qu’il modifie sont actuellement utilisées.


</dt> </dl> </dd> <dt>

<span id="ERROR_RECOVERY_FILE_CORRUPT"></span><span id="error_recovery_file_corrupt"></span>**fichier de récupération d’erreur \_ \_ \_ endommagé**
</dt> <dd> <dl> <dt>

15619 (0x3D03)
</dt> <dt>



Le package n’a pas pu être récupéré car les données nécessaires à la récupération ont été endommagées.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_STAGED_SIGNATURE"></span><span id="error_invalid_staged_signature"></span>**ERREUR \_ de \_ signature intermédiaire non valide \_**
</dt> <dd> <dl> <dt>

15620 (0x3D04)
</dt> <dt>



La signature n’est pas valide. Pour s’inscrire en mode développeur, AppxSignature. p7x et AppxBlockMap.xml doivent être valides ou ne doivent pas être présents.


</dt> </dl> </dd> <dt>

<span id="ERROR_DELETING_EXISTING_APPLICATIONDATA_STORE_FAILED"></span><span id="error_deleting_existing_applicationdata_store_failed"></span>**ERREUR lors de \_ la suppression du \_ \_ magasin APPLICATIONDATA existant \_ \_**
</dt> <dd> <dl> <dt>

15621 (0x3D05)
</dt> <dt>



Une erreur s’est produite lors de la suppression des données d’application précédemment existantes du package.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_PACKAGE_DOWNGRADE"></span><span id="error_install_package_downgrade"></span>**ERREUR lors de l’installation du package à une \_ \_ \_ version antérieure**
</dt> <dd> <dl> <dt>

15622 (0x3D06)
</dt> <dt>



Le package n’a pas pu être installé car une version plus récente de ce package est déjà installée.


</dt> </dl> </dd> <dt>

<span id="ERROR_SYSTEM_NEEDS_REMEDIATION"></span><span id="error_system_needs_remediation"></span>**le \_ système d’erreur \_ doit être mis à \_ jour**
</dt> <dd> <dl> <dt>

15623 (0x3D07)
</dt> <dt>



Une erreur a été détectée dans un fichier binaire système. Essayez d’actualiser le PC pour résoudre le problème.


</dt> </dl> </dd> <dt>

<span id="ERROR_APPX_INTEGRITY_FAILURE_CLR_NGEN"></span><span id="error_appx_integrity_failure_clr_ngen"></span>**erreur d’erreur d' \_ \_ intégrité AppX \_ \_ CLR \_ Ngen**
</dt> <dd> <dl> <dt>

15624 (0x3D08)
</dt> <dt>



Un fichier binaire NGEN CLR endommagé a été détecté sur le système.


</dt> </dl> </dd> <dt>

<span id="ERROR_RESILIENCY_FILE_CORRUPT"></span><span id="error_resiliency_file_corrupt"></span>**\_fichier de résilience des erreurs \_ \_ endommagé**
</dt> <dd> <dl> <dt>

15625 (0x3D09)
</dt> <dt>



Impossible de reprendre l’opération, car les données nécessaires à la récupération ont été endommagées.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_FIREWALL_SERVICE_NOT_RUNNING"></span><span id="error_install_firewall_service_not_running"></span>**ERREUR lors de l' \_ installation du \_ service pare-feu \_ \_ \_ inactif**
</dt> <dd> <dl> <dt>

15626 (0x3D0A)
</dt> <dt>



le package n’a pas pu être installé car le service de pare-feu Windows n’est pas en cours d’exécution. activez le service de pare-feu Windows, puis réessayez.


</dt> </dl> </dd> <dt>

<span id="APPMODEL_ERROR_NO_PACKAGE"></span><span id="appmodel_error_no_package"></span>**\_erreur APPMODEL \_ aucun \_ package**
</dt> <dd> <dl> <dt>

15700 (0x3D54)
</dt> <dt>



Le processus n’a pas d’identité de package.


</dt> </dl> </dd> <dt>

<span id="APPMODEL_ERROR_PACKAGE_RUNTIME_CORRUPT"></span><span id="appmodel_error_package_runtime_corrupt"></span>**\_Runtime du package d’erreurs APPMODEL \_ \_ \_ endommagé**
</dt> <dd> <dl> <dt>

15701 (0x3D55)
</dt> <dt>



Les informations d’exécution du package sont endommagées.


</dt> </dl> </dd> <dt>

<span id="APPMODEL_ERROR_PACKAGE_IDENTITY_CORRUPT"></span><span id="appmodel_error_package_identity_corrupt"></span>**\_identité du package d’erreur APPMODEL \_ \_ \_ endommagée**
</dt> <dd> <dl> <dt>

15702 (0x3D56)
</dt> <dt>



L’identité du package est endommagée.


</dt> </dl> </dd> <dt>

<span id="APPMODEL_ERROR_NO_APPLICATION"></span><span id="appmodel_error_no_application"></span>**erreur APPMODEL- \_ \_ aucune \_ application**
</dt> <dd> <dl> <dt>

15703 (0x3D57)
</dt> <dt>



Le processus n’a pas d’identité d’application.


</dt> </dl> </dd> <dt>

<span id="ERROR_STATE_LOAD_STORE_FAILED"></span><span id="error_state_load_store_failed"></span>**\_échec du \_ magasin de chargement d’état d’erreur \_ \_**
</dt> <dd> <dl> <dt>

15800 (0x3DB8)
</dt> <dt>



Échec du chargement du magasin d’État.


</dt> </dl> </dd> <dt>

<span id="ERROR_STATE_GET_VERSION_FAILED"></span><span id="error_state_get_version_failed"></span>**échec de la récupération de la version de l’état d’erreur \_ \_ \_ \_**
</dt> <dd> <dl> <dt>

15801 (0x3DB9)
</dt> <dt>



Échec de la récupération de la version d’état de l’application.


</dt> </dl> </dd> <dt>

<span id="ERROR_STATE_SET_VERSION_FAILED"></span><span id="error_state_set_version_failed"></span>**échec de la version du jeu d' \_ État d’erreur \_ \_ \_**
</dt> <dd> <dl> <dt>

15802 (0x3DBA)
</dt> <dt>



Échec de la définition de la version d’état de l’application.


</dt> </dl> </dd> <dt>

<span id="ERROR_STATE_STRUCTURED_RESET_FAILED"></span><span id="error_state_structured_reset_failed"></span>**\_échec de \_ la \_ réinitialisation structurée d’état d’erreur \_**
</dt> <dd> <dl> <dt>

15803 (0x3DBB)
</dt> <dt>



Échec de la réinitialisation de l’État structuré de l’application.


</dt> </dl> </dd> <dt>

<span id="ERROR_STATE_OPEN_CONTAINER_FAILED"></span><span id="error_state_open_container_failed"></span>**échec de l’état d’erreur d' \_ \_ ouverture du \_ conteneur \_**
</dt> <dd> <dl> <dt>

15804 (0x3DBC)
</dt> <dt>



Le gestionnaire d’État n’a pas pu ouvrir le conteneur.


</dt> </dl> </dd> <dt>

<span id="ERROR_STATE_CREATE_CONTAINER_FAILED"></span><span id="error_state_create_container_failed"></span>**échec de la \_ \_ création du \_ conteneur d’état \_**
</dt> <dd> <dl> <dt>

15805 (0x3DBD)
</dt> <dt>



Le gestionnaire d’État n’a pas pu créer le conteneur.


</dt> </dl> </dd> <dt>

<span id="ERROR_STATE_DELETE_CONTAINER_FAILED"></span><span id="error_state_delete_container_failed"></span>**échec de la suppression de l’état d’erreur du \_ \_ \_ conteneur \_**
</dt> <dd> <dl> <dt>

15806 (0x3DBE)
</dt> <dt>



Le gestionnaire d’État n’a pas pu supprimer le conteneur.


</dt> </dl> </dd> <dt>

<span id="ERROR_STATE_READ_SETTING_FAILED"></span><span id="error_state_read_setting_failed"></span>**\_échec du \_ paramètre de lecture \_ \_ de l’état d’erreur**
</dt> <dd> <dl> <dt>

15807 (0x3DBF)
</dt> <dt>



Le gestionnaire d’État n’a pas pu lire le paramètre.


</dt> </dl> </dd> <dt>

<span id="ERROR_STATE_WRITE_SETTING_FAILED"></span><span id="error_state_write_setting_failed"></span>**\_échec du \_ paramètre d’écriture d’état d’erreur \_ \_**
</dt> <dd> <dl> <dt>

15808 (0x3DC0)
</dt> <dt>



Le gestionnaire d’État n’a pas pu écrire le paramètre.


</dt> </dl> </dd> <dt>

<span id="ERROR_STATE_DELETE_SETTING_FAILED"></span><span id="error_state_delete_setting_failed"></span>**\_échec du \_ paramètre de suppression \_ \_ de l’état d’erreur**
</dt> <dd> <dl> <dt>

15809 (0x3DC1)
</dt> <dt>



Le gestionnaire d’État n’a pas pu supprimer le paramètre.


</dt> </dl> </dd> <dt>

<span id="ERROR_STATE_QUERY_SETTING_FAILED"></span><span id="error_state_query_setting_failed"></span>**\_échec du \_ paramètre de requête d’état d’erreur \_ \_**
</dt> <dd> <dl> <dt>

15810 (0x3DC2)
</dt> <dt>



Le gestionnaire d’État n’a pas pu interroger le paramètre.


</dt> </dl> </dd> <dt>

<span id="ERROR_STATE_READ_COMPOSITE_SETTING_FAILED"></span><span id="error_state_read_composite_setting_failed"></span>**\_échec de \_ lecture \_ du \_ paramètre composite \_ de l’état d’erreur**
</dt> <dd> <dl> <dt>

15811 (0x3DC3)
</dt> <dt>



Le gestionnaire d’État n’a pas pu lire le paramètre composite.


</dt> </dl> </dd> <dt>

<span id="ERROR_STATE_WRITE_COMPOSITE_SETTING_FAILED"></span><span id="error_state_write_composite_setting_failed"></span>**échec de l’écriture de l' \_ état \_ \_ composite du paramètre composite \_ \_**
</dt> <dd> <dl> <dt>

15812 (0x3DC4)
</dt> <dt>



Le gestionnaire d’État n’a pas pu écrire le paramètre composite.


</dt> </dl> </dd> <dt>

<span id="ERROR_STATE_ENUMERATE_CONTAINER_FAILED"></span><span id="error_state_enumerate_container_failed"></span>**échec de l’énumération de l’état d’erreur du \_ \_ \_ conteneur \_**
</dt> <dd> <dl> <dt>

15813 (0x3DC5)
</dt> <dt>



Le gestionnaire d’État n’a pas pu énumérer les conteneurs.


</dt> </dl> </dd> <dt>

<span id="ERROR_STATE_ENUMERATE_SETTINGS_FAILED"></span><span id="error_state_enumerate_settings_failed"></span>**échec de l' \_ \_ énumération de l’état d' \_ erreur \_**
</dt> <dd> <dl> <dt>

15814 (0x3DC6)
</dt> <dt>



Le gestionnaire d’État n’a pas pu énumérer les paramètres.


</dt> </dl> </dd> <dt>

<span id="ERROR_STATE_COMPOSITE_SETTING_VALUE_SIZE_LIMIT_EXCEEDED"></span><span id="error_state_composite_setting_value_size_limit_exceeded"></span>**\_limite de \_ taille de valeur de paramètre composite d’état d’erreur \_ \_ \_ \_ \_ dépassée**
</dt> <dd> <dl> <dt>

15815 (0x3DC7)
</dt> <dt>



La taille de la valeur du paramètre composite du gestionnaire d’État a dépassé la limite.


</dt> </dl> </dd> <dt>

<span id="ERROR_STATE_SETTING_VALUE_SIZE_LIMIT_EXCEEDED"></span><span id="error_state_setting_value_size_limit_exceeded"></span>**limite de taille de valeur de paramètre d’état d’erreur \_ \_ \_ \_ \_ \_ dépassée**
</dt> <dd> <dl> <dt>

15816 (0x3DC8)
</dt> <dt>



La taille de la valeur du paramètre du gestionnaire d’État a dépassé la limite.


</dt> </dl> </dd> <dt>

<span id="ERROR_STATE_SETTING_NAME_SIZE_LIMIT_EXCEEDED"></span><span id="error_state_setting_name_size_limit_exceeded"></span>**paramètre d’état d’erreur- \_ \_ limite de taille de \_ nom \_ \_ \_ dépassée**
</dt> <dd> <dl> <dt>

15817 (0x3DC9)
</dt> <dt>



La longueur du nom du paramètre du gestionnaire d’État a dépassé la limite.


</dt> </dl> </dd> <dt>

<span id="ERROR_STATE_CONTAINER_NAME_SIZE_LIMIT_EXCEEDED"></span><span id="error_state_container_name_size_limit_exceeded"></span>**le \_ nom du conteneur d’état d’erreur \_ \_ \_ \_ a dépassé la limite de taille \_**
</dt> <dd> <dl> <dt>

15818 (0x3DCA)
</dt> <dt>



La longueur du nom de conteneur du gestionnaire d’État a dépassé la limite.


</dt> </dl> </dd> <dt>

<span id="ERROR_API_UNAVAILABLE"></span><span id="error_api_unavailable"></span>**API d’erreur \_ \_ non disponible**
</dt> <dd> <dl> <dt>

15841 (0x3DE1)
</dt> <dt>



Cette API ne peut pas être utilisée dans le contexte du type d’application de l’appelant.


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

 

 
