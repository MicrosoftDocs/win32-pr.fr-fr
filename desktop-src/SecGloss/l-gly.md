---
description: Contient les définitions des termes de sécurité qui commencent par la lettre L.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 65dd9a04-fc7c-4179-95ff-dac7dad4668f
title: L (Glossaire sécurité)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b33ee054c2bcf414ef289cc381ac13ef970da6dc
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127311270"
---
# <a name="l-security-glossary"></a>L (Glossaire sécurité)

[A](a-gly.md) [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) [e](e-gly.md) F [G](g-gly.md) [H](h-gly.md) [I](i-gly.md) J [K](k-gly.md) L [M](m-gly.md) [N](n-gly.md) [O](o-gly.md) [P](p-gly.md) Q [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) [W](w-gly.md) [X](x-gly.md) Y Z

<dl> <dt>

<span id="_security_ldap_gly"></span><span id="_SECURITY_LDAP_GLY"></span>**LDAP**
</dt> <dd>

Voir *protocole LDAP (Lightweight Directory Access* )

</dd> <dt>

<span id="_security_lightweight_directory_access_protocol_gly"></span><span id="_SECURITY_LIGHTWEIGHT_DIRECTORY_ACCESS_PROTOCOL_GLY"></span>**Protocole d’accès à Lightweight Directory**
</dt> <dd>

Un sous-ensemble plus facile à implémenter de la norme X. 500 DAP pour les services d’annuaire.

</dd> <dt>

<span id="_security_little_endian_gly"></span><span id="_SECURITY_LITTLE_ENDIAN_GLY"></span>**Little endian**
</dt> <dd>

Mémoire ou format de données dans lequel l’octet le moins significatif est stocké à l’adresse inférieure ou arrive en premier.

Voir aussi [*Big-endian*](b-gly.md).

</dd> <dt>

<span id="_security_locally_unique_identifier_gly"></span><span id="_SECURITY_LOCALLY_UNIQUE_IDENTIFIER_GLY"></span>**identificateur unique local**
</dt> <dd>

LUID Valeur 64 bits qui est garantie comme étant unique sur le système d’exploitation qui l’a générée jusqu’au redémarrage du système.

</dd> <dt>

<span id="_security_local_registration_authority_gly"></span><span id="_SECURITY_LOCAL_REGISTRATION_AUTHORITY_GLY"></span>**autorité d’inscription locale**
</dt> <dd>

(LRA) Intermédiaire entre un serveur de publication et une [*autorité de certification*](c-gly.md) (ca). Le LRA peut, par exemple, vérifier les informations d’identification d’un éditeur avant de les envoyer à l’autorité de certification.

</dd> <dt>

<span id="_security_local_security_authority_gly"></span><span id="_SECURITY_LOCAL_SECURITY_AUTHORITY_GLY"></span>**Autorité de sécurité locale**
</dt> <dd>

LOCALE Sous-système protégé qui authentifie et journalise les utilisateurs sur le système local. LSA gère également les informations sur tous les aspects de la sécurité locale sur un système, collectivement appelée stratégie de sécurité locale du système.

</dd> <dt>

<span id="_security_logical_store_gly"></span><span id="_SECURITY_LOGICAL_STORE_GLY"></span>**magasin logique**
</dt> <dd>

Consultez le [*magasin virtuel*](v-gly.md).

</dd> <dt>

<span id="_security_logon_data_gly"></span><span id="_SECURITY_LOGON_DATA_GLY"></span>**données d’ouverture de session**
</dt> <dd>

Informations présentées au système par un [*principal de sécurité*](s-gly.md) pour l’authentification.

</dd> <dt>

<span id="_security_logon_identifier_gly"></span><span id="_SECURITY_LOGON_IDENTIFIER_GLY"></span>**identificateur de connexion**
</dt> <dd>

LUID qui identifie une *session de connexion*. Un ID de connexion est valide jusqu’à ce que l’utilisateur se déconnecte. Un ID d’ouverture de session est unique pendant que l’ordinateur est en cours d’exécution ; aucune autre session de connexion n’aura le même ID de connexion. Toutefois, l’ensemble des ID d’ouverture de session possibles est réinitialisé au démarrage de l’ordinateur. Pour récupérer l’ID d’ouverture de session à partir d’un [*jeton d’accès*](a-gly.md), appelez la fonction **GetTokenInformation** pour TokenStatistics ; l’ID de connexion se trouve dans le membre **AuthenticationId** .

</dd> <dt>

<span id="_security_logon_session_gly"></span><span id="_SECURITY_LOGON_SESSION_GLY"></span>**ouverture de session**
</dt> <dd>

Une session de connexion commence chaque fois qu’un utilisateur se connecte à un ordinateur. Tous les processus d’une session de connexion ont le même [*jeton d’accès*](a-gly.md)principal. Le jeton d’accès contient des informations sur le contexte de sécurité de la session d’ouverture de session, y compris le SID de l’utilisateur, l' *identificateur d’ouverture* de session et le *SID d’ouverture* de session.

</dd> <dt>

<span id="_security_logon_sid_gly"></span><span id="_SECURITY_LOGON_SID_GLY"></span>**SID d’ouverture de session**
</dt> <dd>

[*Identificateur de sécurité*](s-gly.md) (SID) qui identifie une *session de connexion*. Vous pouvez utiliser le SID d’ouverture de session dans une [*liste DACL*](d-gly.md) pour contrôler l’accès au cours d’une session de connexion. Un SID d’ouverture de session est valide jusqu’à ce que l’utilisateur se déconnecte. Un SID d’ouverture de session est unique pendant que l’ordinateur est en cours d’exécution ; aucune autre session de connexion n’aura le même SID d’ouverture de session. Toutefois, l’ensemble d’identificateurs de sécurité d’ouverture de session possibles est réinitialisé au démarrage de l’ordinateur. Pour récupérer le SID d’ouverture de session à partir d’un [*jeton d’accès*](a-gly.md), appelez la fonction **GetTokenInformation** pour tokenGroups.

</dd> <dt>

<span id="_security_low_level_message_functions_gly"></span><span id="_SECURITY_LOW_LEVEL_MESSAGE_FUNCTIONS_GLY"></span>**fonctions de message de bas niveau**
</dt> <dd>

Fonctions de gestion des messages qui fonctionnent à un niveau plus élevé que les fonctions de chiffrement de base. Ces fonctions fournissent des fonctionnalités permettant d’encoder les données pour la transmission et de décoder les données qui ont été reçues. Les fonctions de message de bas niveau offrent plus de flexibilité que les fonctions de message simplifiées, mais nécessitent davantage d’appels de fonction.

Voir aussi [*fonctions de message simplifiées*](s-gly.md).

</dd> <dt>

<span id="_security_lsa_gly"></span><span id="_SECURITY_LSA_GLY"></span>**LOCALE**
</dt> <dd>

Consultez *autorité de sécurité locale*.

</dd> <dt>

<span id="_security_luid_gly"></span><span id="_SECURITY_LUID_GLY"></span>**LUID**
</dt> <dd>

Consultez *identificateur unique local*.

</dd> </dl>

 

 



