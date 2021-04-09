---
description: Contient les définitions des termes de sécurité qui commencent par la lettre S.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 3e9d7672-2314-45c8-8178-5a0afcfd0c50
title: S (Glossaire de la sécurité)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 975df9e3638f12ba7f3766d6119685fba1fa599b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952373"
---
# <a name="s-security-glossary"></a>S (Glossaire de la sécurité)

[A](a-gly.md) [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) [e](e-gly.md) F [G](g-gly.md) [H](h-gly.md) [I](i-gly.md) J [K](k-gly.md) [L](l-gly.md) [M](m-gly.md) [N](n-gly.md) [O](o-gly.md) [P](p-gly.md) Q [R](r-gly.md) S [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) [W](w-gly.md) [X](x-gly.md) Y Z

<dl> <dt>

<span id="_security_s_mime_gly"></span><span id="_SECURITY_S_MIME_GLY"></span>**S/MIME**
</dt> <dd>

Consultez *extensions de messagerie Internet sécurisées/Multipurpose*.

</dd> <dt>

<span id="_security_sacl_gly"></span><span id="_SECURITY_SACL_GLY"></span>**SACL**
</dt> <dd>

Consultez *liste de contrôle d’accès système*.

</dd> <dt>

<span id="_security_salt_value_gly"></span><span id="_SECURITY_SALT_VALUE_GLY"></span>**valeur Salt**
</dt> <dd>

Données aléatoires qui sont parfois incluses dans le cadre d’une clé de session. En cas d’ajout à une clé de session, les données Salt de texte en clair sont placées devant les données de clé chiffrées. Des valeurs Salt sont ajoutées pour augmenter le travail nécessaire pour monter une attaque par force brute (dictionnaire) contre les données chiffrées à l’aide d’un chiffrement à clé symétrique. Les valeurs Salt sont générées en appelant **CryptGenRandom**.

</dd> <dt>

<span id="_security_sam_gly"></span><span id="_SECURITY_SAM_GLY"></span>**Hervé**
</dt> <dd>

Voir *Gestionnaire de comptes de sécurité*.

</dd> <dt>

<span id="_security_sanitized_name_gly"></span><span id="_SECURITY_SANITIZED_NAME_GLY"></span>**nom assaini**
</dt> <dd>

Forme d’un nom d’autorité de certification utilisé dans les noms de fichiers (par exemple, pour une [*liste de révocation de certificats*](c-gly.md)) et dans les clés de registre. Le processus d’assainissement du nom de l’autorité de certification est nécessaire pour supprimer les caractères non autorisés pour les noms de fichiers, les noms de clés de registre ou les valeurs de noms uniques, ou qui ne sont pas conformes pour des raisons spécifiques à la technologie. Dans les services de certificats, le processus de nettoyage convertit tout caractère illégal du nom commun de l’autorité de certification en une représentation à 5 caractères au format **!** _xxxx_, où **!** est utilisé comme caractère d’échappement et *xxxx* représente quatre entiers hexadécimaux qui identifient de façon unique le caractère en cours de conversion.

</dd> <dt>

<span id="security.s_1_gly"></span><span id="SECURITY.S_1_GLY"></span>**ÉTABLIES**
</dt> <dd>

Consultez *séquence de vigilance sécurisée*.

</dd> <dt>

<span id="_security_scard_defaultreaders_gly"></span><span id="_SECURITY_SCARD_DEFAULTREADERS_GLY"></span>**Cicatrice $ DefaultReaders**
</dt> <dd>

Toutefois, un groupe de lecteurs Terminal Server qui contient tous les lecteurs attribués à ce terminal n’est pas réservé pour cette utilisation spécifique.

</dd> <dt>

<span id="_security_scard_allreaders_gly"></span><span id="_SECURITY_SCARD_ALLREADERS_GLY"></span>**Cicatrice $ AllReaders**
</dt> <dd>

Groupe de lecteurs à l’ensemble du système de cartes à puce qui comprend tous les lecteurs introduits dans le gestionnaire de ressources des cartes à puce. Les lecteurs sont automatiquement ajoutés au groupe lorsqu’ils sont introduits dans le système.

</dd> <dt>

<span id="_security_scard_autoallocate_gly"></span><span id="_SECURITY_SCARD_AUTOALLOCATE_GLY"></span>**\_allocation allouée**
</dt> <dd>

Constante système de carte à puce qui indique au gestionnaire de ressources des cartes à puce d’allouer suffisamment de mémoire, en retournant un pointeur vers la mémoire tampon allouée au lieu de remplir une mémoire tampon fournie par l’utilisateur. La mémoire tampon retournée doit ensuite être libérée en appelant **SCardFreeMemory**.

</dd> <dt>

<span id="_security_scep_gly"></span><span id="_SECURITY_SCEP_GLY"></span>**SCEP**
</dt> <dd>

Voir *protocole d’Inscription de certificats simple*

</dd> <dt>

<span id="_security_schannel_gly"></span><span id="_SECURITY_SCHANNEL_GLY"></span>**Schannel**
</dt> <dd>

Package de sécurité qui assure l’authentification entre les clients et les serveurs.

</dd> <dt>

<span id="_security_secure_attention_sequence_gly"></span><span id="_SECURITY_SECURE_ATTENTION_SEQUENCE_GLY"></span>**séquence d’intervention sécurisée**
</dt> <dd>

ÉTABLIES Séquence clé qui commence le processus d’ouverture ou de fermeture de session. La séquence par défaut est CTRL + ALT + SUPPR.

</dd> <dt>

<span id="_security_secure_electronic_transaction_gly"></span><span id="_SECURITY_SECURE_ELECTRONIC_TRANSACTION_GLY"></span>**Transaction électronique sécurisée**
</dt> <dd>

DÉFINIE Protocole pour les transactions électroniques sécurisées sur Internet.

</dd> <dt>

<span id="_security_secure_hash_algorithm_gly"></span><span id="_SECURITY_SECURE_HASH_ALGORITHM_GLY"></span>**Algorithme de hachage sécurisé**
</dt> <dd>

Tcha Algorithme de hachage qui génère un résumé de message. L'algorithme de hachage est utilisé avec l'algorithme de signature numérique (DSA) dans la norme de signature numérique (DSS), entre autres. CryptoAPI fait référence à cet algorithme par l’identificateur de l’algorithme (CALG \_ SHA), le nom (SHA) et la classe ( \_ classe de hachage ALG \_ ). Il existe quatre types de SHA : SHA-1, SHA-256, SHA-384 et SHA-512. SHA-1 génère un condensat de message en 160 bits. SHA-256, SHA-384 et SHA-512 génèrent respectivement des condensats du message en 256, 384 et 512 bits. L'algorithme SHA a été développé par le National Institute of Standards and Technology (NIST) et par la National Security Agency (NSA).

</dd> <dt>

<span id="_security_secure_hash_standard_gly"></span><span id="_SECURITY_SECURE_HASH_STANDARD_GLY"></span>**Norme de hachage sécurisé**
</dt> <dd>

Norme conçue par NIST et NSA. Cette norme définit l’algorithme de hachage sécurisé (SHA-1) pour une utilisation avec la norme de signature numérique (DSS).

Voir aussi *algorithme de hachage sécurisé*.

</dd> <dt>

<span id="_security_secure_sockets_layer_protocol_gly"></span><span id="_SECURITY_SECURE_SOCKETS_LAYER_PROTOCOL_GLY"></span>**Protocole SSL (Secure Sockets Layer)**
</dt> <dd>

Socket Protocole pour sécuriser les communications réseau à l’aide d’une combinaison de technologies de clé publique et secrète.

</dd> <dt>

<span id="_security_secure_multipurpose_internet_mail_extensions_gly"></span><span id="_SECURITY_SECURE_MULTIPURPOSE_INTERNET_MAIL_EXTENSIONS_GLY"></span>**Extensions de messagerie Internet sécurisées/Multipurpose**
</dt> <dd>

(S/MIME) Norme de sécurité de messagerie qui utilise le chiffrement à clé publique.

</dd> <dt>

<span id="_security_security_accounts_manager_gly"></span><span id="_SECURITY_SECURITY_ACCOUNTS_MANAGER_GLY"></span>**Gestionnaire des comptes de sécurité**
</dt> <dd>

Hervé Service Windows utilisé pendant le processus d’ouverture de session. SAM gère les informations de compte d’utilisateur, y compris les groupes auxquels un utilisateur appartient.

</dd> <dt>

<span id="_security_security_context_gly"></span><span id="_SECURITY_SECURITY_CONTEXT_GLY"></span>**contexte de sécurité**
</dt> <dd>

Attributs ou règles de sécurité actuellement en vigueur. Par exemple, l'utilisateur actuel connecté à l'ordinateur ou le code confidentiel entré par l'utilisateur d'une carte à puce. Pour le SSPI, un contexte de sécurité est une structure de données opaque qui contient des données de sécurité pertinentes à une connexion, telles qu'une clé de session ou une indication de la durée de la session.

</dd> <dt>

<span id="_security_security_descriptor_gly"></span><span id="_SECURITY_SECURITY_DESCRIPTOR_GLY"></span>**descripteur de sécurité**
</dt> <dd>

Structure et données associées qui contiennent les informations de sécurité pour un objet sécurisable. Un descripteur de sécurité identifie le propriétaire et le groupe principal de l’objet. Il peut également contenir une liste DACL qui contrôle l’accès à l’objet, et une liste SACL qui contrôle la journalisation des tentatives d’accès à l’objet.

Voir aussi [*descripteur de sécurité absolu*](a-gly.md), [*liste de contrôle d’accès discrétionnaire*](d-gly.md), *descripteur de sécurité auto-relatif*, *liste de contrôle d’accès système*.

</dd> <dt>

<span id="_security_security_identifier_gly"></span><span id="_SECURITY_SECURITY_IDENTIFIER_GLY"></span>**identificateur de sécurité**
</dt> <dd>

SID Structure de données de longueur variable qui identifie les comptes d’utilisateurs, de groupes et d’ordinateurs. Chaque compte sur un réseau reçoit un SID unique lors de la création du compte. Les processus internes dans Windows font référence au SID d’un compte plutôt qu’au nom de groupe ou d’utilisateur du compte.

</dd> <dt>

<span id="_security_security_package_gly"></span><span id="_SECURITY_SECURITY_PACKAGE_GLY"></span>**package de sécurité**
</dt> <dd>

Implémentation logicielle d’un protocole de sécurité. Les packages de sécurité sont contenus dans les dll du fournisseur de support de sécurité ou le fournisseur de support de sécurité/dll du package d’authentification.

</dd> <dt>

<span id="_security_security_protocol_gly"></span><span id="_SECURITY_SECURITY_PROTOCOL_GLY"></span>**Protocole de sécurité**
</dt> <dd>

Spécification qui définit les objets de données liés à la sécurité et les règles relatives à la façon dont les objets sont utilisés pour maintenir la sécurité sur un système informatique.

</dd> <dt>

<span id="_security_security_principal_gly"></span><span id="_SECURITY_SECURITY_PRINCIPAL_GLY"></span>**principal de sécurité**
</dt> <dd>

Entité reconnue par le système de sécurité. Les entités peuvent inclure des utilisateurs humains ainsi que des processus autonomes.

</dd> <dt>

<span id="_security_security_support_provider_gly"></span><span id="_SECURITY_SECURITY_SUPPORT_PROVIDER_GLY"></span>**fournisseur de support de sécurité**
</dt> <dd>

CADRE Bibliothèque de liens dynamiques (DLL) qui implémente l’interface SSPI en mettant un ou plusieurs packages de sécurité à la disposition des applications. Chaque package de sécurité fournit des mappages entre les appels de fonction SSPI d'une application et les fonctions d'un modèle de sécurité réel. Les packages de sécurité prennent en charge des protocoles de sécurité tels que l’authentification Kerberos et Microsoft LAN Manager.

</dd> <dt>

<span id="_security_security_support_provider_interface_gly"></span><span id="_SECURITY_SECURITY_SUPPORT_PROVIDER_INTERFACE_GLY"></span>**Interface du fournisseur de support de sécurité**
</dt> <dd>

INTERFACE Interface commune entre les applications de niveau transport, telles que l’appel de procédure distante Microsoft (RPC) et les fournisseurs de sécurité, tels que la sécurité distribuée Windows. Le SSPI permet à une application de transport d'appeler l'un des fournisseurs de sécurité pour obtenir une connexion authentifiée. Ces appels ne requièrent pas une connaissance étendue des détails du protocole de sécurité.

</dd> <dt>

<span id="_security_self_relative_security_descriptor_gly"></span><span id="_SECURITY_SELF_RELATIVE_SECURITY_DESCRIPTOR_GLY"></span>**descripteur de sécurité auto-relatif**
</dt> <dd>

Descripteur de sécurité qui stocke toutes ses informations de sécurité dans un bloc de mémoire contigu.

Voir aussi *descripteur de sécurité*.

</dd> <dt>

<span id="_security_serialize_gly"></span><span id="_SECURITY_SERIALIZE_GLY"></span>**sérialiser**
</dt> <dd>

Processus de conversion de données en une chaîne de uns et de zéros pour qu’elle puisse être transmise en série. L’encodage fait partie de ce processus.

</dd> <dt>

<span id="_security_serialized_certificate_store_format_gly"></span><span id="_SECURITY_SERIALIZED_CERTIFICATE_STORE_FORMAT_GLY"></span>**Format du magasin de certificats sérialisé**
</dt> <dd>

SST Le format du magasin de certificats sérialisé est le seul format qui conserve toutes les propriétés du magasin de certificats. Cela est utile dans les cas où des racines ont été configurées avec des propriétés EKU personnalisées et que vous souhaitez les déplacer vers un autre ordinateur.

</dd> <dt>

<span id="_security_server_gly"></span><span id="_SECURITY_SERVER_GLY"></span>**serveurs**
</dt> <dd>

Ordinateur qui répond aux commandes d’un ordinateur client. Le client et le serveur fonctionnent ensemble pour exécuter des fonctionnalités d’application distribuable.

Voir aussi [*client*](c-gly.md).

</dd> <dt>

<span id="_security_server_certificate_gly"></span><span id="_SECURITY_SERVER_CERTIFICATE_GLY"></span>**certificat de serveur**
</dt> <dd>

Fait référence à un certificat utilisé pour l’authentification du serveur, par exemple l’authentification d’un serveur Web sur un navigateur Web. Lorsqu’un client de navigateur Web tente d’accéder à un serveur Web sécurisé, le serveur envoie son certificat au navigateur pour lui permettre de vérifier l’identité du serveur.

</dd> <dt>

<span id="_security_server_gated_cryptography_gly"></span><span id="_SECURITY_SERVER_GATED_CRYPTOGRAPHY_GLY"></span>**chiffrement contrôlé par le serveur**
</dt> <dd>

SGC Extension de *SSL (Secure Sockets Layer)* (SSL) qui permet aux organisations, telles que les institutions financières, qui ont des versions d’exportation de Internet Information Services (IIS) d’utiliser un chiffrement fort (par exemple, le chiffrement 128 bits).

</dd> <dt>

<span id="_security_service_principal_name_gly"></span><span id="_SECURITY_SERVICE_PRINCIPAL_NAME_GLY"></span>**nom du principal du service**
</dt> <dd>

SPN Nom par lequel un client identifie de manière unique une instance d’un service. Si vous installez plusieurs instances d'un service sur les ordinateurs d'une forêt, chaque instance doit posséder son propre SPN. Une instance de service donnée peut avoir plusieurs noms de principal du service (SPN) s’il existe plusieurs noms que les clients peuvent utiliser pour l’authentification

</dd> <dt>

<span id="_security_service_provider_smart_card__gly"></span><span id="_SECURITY_SERVICE_PROVIDER_SMART_CARD__GLY"></span>**fournisseur de services (carte à puce)**
</dt> <dd>

Composant de sous-système de carte à puce qui fournit l’accès à des services de carte à puce spécifiques par le biais d’interfaces COM.

Voir aussi [*fournisseur de services principal*](p-gly.md).

</dd> <dt>

<span id="_security_session_gly"></span><span id="_SECURITY_SESSION_GLY"></span>**session**
</dt> <dd>

Échange de messages sous la protection d'un morceau unique d'élément de génération de clé. Par exemple, les sessions SSL utilisent une clé unique pour envoyer plusieurs messages sous cette clé.

</dd> <dt>

<span id="_security_session_key_gly"></span><span id="_SECURITY_SESSION_KEY_GLY"></span>**clé de session**
</dt> <dd>

Clé de chiffrement à durée de vie relativement courte, souvent négociée par un client et un serveur basé sur un secret partagé. La durée de vie d’une clé de session est limitée par la session à laquelle elle est associée. Une clé de session doit être suffisamment forte pour résister à Cryptanalysis pendant la durée de vie de la session. Lorsque les clés de session sont transmises, elles sont généralement protégées par des clés d’échange de clés (qui sont généralement des clés asymétriques), de sorte que seul le destinataire prévu puisse y accéder. Les clés de session peuvent être dérivées des valeurs de hachage en appelant la fonction **CryptDeriveKey** .

</dd> <dt>

<span id="_security_session_key_derivation_scheme_gly"></span><span id="_SECURITY_SESSION_KEY_DERIVATION_SCHEME_GLY"></span>**schéma de dérivation de clé de session**
</dt> <dd>

Spécifie quand une clé est dérivée d’un hachage. Les méthodes utilisées dépendent du type de fournisseur de services de chiffrement.

</dd> <dt>

<span id="_security_set_gly"></span><span id="_SECURITY_SET_GLY"></span>**DÉFINIE**
</dt> <dd>

Voir *transactions électroniques sécurisées*.

</dd> <dt>

<span id="_security_sha_gly"></span><span id="_SECURITY_SHA_GLY"></span>**Tcha**
</dt> <dd>

Nom CryptoAPI pour l’algorithme de hachage sécurisé, SHA-1. Les autres algorithmes de hachage incluent [*MD2*](m-gly.md), [*MD4*](m-gly.md)et [*MD5*](m-gly.md).

Voir aussi *algorithme de hachage sécurisé*.

</dd> <dt>

<span id="_security_shs_gly"></span><span id="_SECURITY_SHS_GLY"></span>**SHS**
</dt> <dd>

Consultez *Secure Hash Standard*.

</dd> <dt>

<span id="_security_sid_gly"></span><span id="_SECURITY_SID_GLY"></span>**SID**
</dt> <dd>

Consultez *identificateur de sécurité*.

</dd> <dt>

<span id="_security_signature_and_data_verification_functions_gly"></span><span id="_SECURITY_SIGNATURE_AND_DATA_VERIFICATION_FUNCTIONS_GLY"></span>**fonctions de vérification des signatures et des données**
</dt> <dd>

Fonctions de message simplifiées utilisées pour signer les messages sortants et vérifier l’authenticité des signatures appliquées dans les messages reçus et les données associées.

Consultez *fonctions de message simplifiées*.

</dd> <dt>

<span id="_security_signature_certificate_gly"></span><span id="_SECURITY_SIGNATURE_CERTIFICATE_GLY"></span>**certificat de signature**
</dt> <dd>

Un certificat qui contient une clé publique utilisée pour vérifier les signatures numériques.

</dd> <dt>

<span id="_security_signature_file_gly"></span><span id="_SECURITY_SIGNATURE_FILE_GLY"></span>**fichier de signature**
</dt> <dd>

Fichier qui contient la signature d’un fournisseur de [*services de chiffrement*](c-gly.md) (CSP) particulier. Le fichier de signature est nécessaire pour garantir que CryptoAPI reconnaît le CSP. CryptoAPI valide cette signature régulièrement pour s’assurer que le CSP n’a pas été falsifié.

</dd> <dt>

<span id="_security_signature_functions_gly"></span><span id="_SECURITY_SIGNATURE_FUNCTIONS_GLY"></span>**fonctions de signature**
</dt> <dd>

Fonctions utilisées pour créer et vérifier des signatures numériques.

Voir aussi *fonctions de message simplifiées*.

</dd> <dt>

<span id="_security_signature_key_pair_gly"></span><span id="_SECURITY_SIGNATURE_KEY_PAIR_GLY"></span>**paire de clés de signature**
</dt> <dd>

Paire de clés publique/privée utilisée pour authentifier les messages (signature numérique). Les paires de clés de signature sont créées en appelant **CryptGenKey**.

Voir aussi [*paire de clés Exchange*](e-gly.md).

</dd> <dt>

<span id="_security_signature_private_key_gly"></span><span id="_SECURITY_SIGNATURE_PRIVATE_KEY_GLY"></span>**clé privée de signature**
</dt> <dd>

Clé privée d’une paire de clés de signature.

Consultez *paire de clés de signature*.

</dd> <dt>

<span id="_security_signed_and_enveloped_data_gly"></span><span id="_SECURITY_SIGNED_AND_ENVELOPED_DATA_GLY"></span>**données signées et enveloppées**
</dt> <dd>

Type de contenu de données défini par PKCS \# 7. Ce type de données est constitué d’un contenu chiffré de tout type, de clés de chiffrement de contenu chiffrées pour un ou plusieurs destinataires et de hachages de messages chiffrés doublement pour un ou plusieurs signataires. Le double chiffrement est constitué d’un chiffrement avec la clé privée d’un signataire, suivi d’un chiffrement avec la clé de chiffrement de contenu.

</dd> <dt>

<span id="_security_signed_data_gly"></span><span id="_SECURITY_SIGNED_DATA_GLY"></span>**données signées**
</dt> <dd>

Type de contenu de données défini par PKCS \# 7. Ce type de données est constitué de tout type de contenu, ainsi que de hachages de message chiffré (Digests) du contenu pour zéro ou plusieurs signataires. Les hachages résultants peuvent être utilisés pour confirmer la personne qui a signé le message. Ces hachages confirment également que le message d’origine n’a pas été modifié depuis la signature du message.

</dd> <dt>

<span id="_security_simple_certificate_enrollment_protocol_gly"></span><span id="_SECURITY_SIMPLE_CERTIFICATE_ENROLLMENT_PROTOCOL_GLY"></span>**Protocole d'inscription de certificats simple**
</dt> <dd>

SCEP Acronyme qui représente Protocole d’inscription de certificats simple. Le protocole est actuellement une norme Internet préliminaire qui définit la communication entre les périphériques réseau et une autorité d’inscription (RA) pour l’inscription de certificats. Pour plus d’informations, consultez le livre blanc sur l' [implémentation de Microsoft SCEP](https://www.scribd.com/document/31941679/Microsoft-SCEP-Implementation-Whitepaper).

</dd> <dt>

<span id="_security_simple_key_blob_gly"></span><span id="_SECURITY_SIMPLE_KEY_BLOB_GLY"></span>**objet BLOB de clé simple**
</dt> <dd>

Clé de session chiffrée avec la clé publique d’échange de clés de l’utilisateur de destination. Ce type d’objet BLOB de clé est utilisé lors du stockage d’une clé de session ou de la transmission d’une clé de session à un autre utilisateur. Un objet BLOB de clé est créé en appelant **CryptExportKey**.

</dd> <dt>

<span id="_security_simplified_message_functions_gly"></span><span id="_SECURITY_SIMPLIFIED_MESSAGE_FUNCTIONS_GLY"></span>**fonctions de message simplifiées**
</dt> <dd>

Fonctions de gestion des messages, telles que le chiffrement des messages, le déchiffrement, la signature et les fonctions de vérification de signature. Les fonctions de message simplifiées fonctionnent à un niveau supérieur à celui des fonctions de chiffrement de base ou des fonctions de message de bas niveau. Les fonctions de message simplifiées encapsulent plusieurs fonctions de chiffrement de base, de message de bas niveau et de certificat dans une fonction unique qui effectue une tâche spécifique d’une manière spécifique, telle que le chiffrement d’un \# message PKCS 7 ou la signature d’un message.

Voir aussi [*fonctions de message de bas niveau*](l-gly.md).

</dd> <dt>

<span id="_security_single_sign_on_gly"></span><span id="_SECURITY_SINGLE_SIGN_ON_GLY"></span>**authentification unique**
</dt> <dd>

SIGNATURE La possibilité de lier une compte Microsoft (par exemple, un compte Microsoft Outlook.com) à un compte local, de sorte qu’une ouverture de session permet à l’utilisateur d’utiliser d’autres applications prenant en charge la connexion avec son compte Microsoft.

</dd> <dt>

<span id="_security_sip_gly"></span><span id="_SECURITY_SIP_GLY"></span>**PANNEAU**
</dt> <dd>

Consultez *package d’interface de sujet*.

</dd> <dt>

<span id="_security_site_certificate_gly"></span><span id="_SECURITY_SITE_CERTIFICATE_GLY"></span>**certificat de site**
</dt> <dd>

Les certificats de serveur et les certificats d' [*autorité de certification*](c-gly.md) sont parfois appelés certificats de site. Lorsque vous faites référence à un certificat de serveur, le certificat identifie le serveur Web présentant le certificat. Lorsque vous faites référence à un certificat d’autorité de certification, le certificat identifie l’autorité de certification qui émet des certificats d’authentification serveur et/ou client aux serveurs et clients qui demandent ces certificats.

</dd> <dt>

<span id="_security_skipjack_gly"></span><span id="_SECURITY_SKIPJACK_GLY"></span>**Skipjack**
</dt> <dd>

Algorithme de chiffrement spécifié dans le cadre de la suite de chiffrement Fortezza. Skipjack est un chiffrement symétrique avec une longueur de clé fixe de 80 bits. Skipjack est un algorithme classifié créé par le États-Unis NSA (National Security Agency). Les détails techniques de l’algorithme Skipjack sont secrets.

</dd> <dt>

<span id="_security_smart_card_gly"></span><span id="_SECURITY_SMART_CARD_GLY"></span>**carte à puce**
</dt> <dd>

Carte à circuit intégré (ICC) appartenant à un individu ou à un groupe dont les informations doivent être protégées selon des attributions de propriété spécifiques. Il fournit son propre contrôle d’accès physique ; sans le sous-système de carte à puce, placez un contrôle d’accès supplémentaire sur la carte à puce. Une carte à puce est une carte en plastique qui contient un circuit intégré compatible avec la norme ISO 7816.

</dd> <dt>

<span id="_security_smart_card_common_dialog_gly"></span><span id="_SECURITY_SMART_CARD_COMMON_DIALOG_GLY"></span>**boîte de dialogue commune de la carte à puce**
</dt> <dd>

Boîte de dialogue commune qui aide l’utilisateur à sélectionner et localiser une carte à puce. Il fonctionne avec les services de gestion de la base de données des cartes à puce et les services de lecture pour aider l’application et, si nécessaire, l’utilisateur à identifier la carte à puce à utiliser dans un but donné.

</dd> <dt>

<span id="_security_smart_card_database_gly"></span><span id="_SECURITY_SMART_CARD_DATABASE_GLY"></span>**base de données de carte à puce**
</dt> <dd>

Base de données utilisée par le gestionnaire de ressources pour gérer les ressources. Il contient une liste de cartes à puce connues, les interfaces et le fournisseur de services principal de chaque carte, ainsi que les lecteurs de cartes à puce et les groupes de lecteurs connus.

</dd> <dt>

<span id="_security_smart_card_subsystem_gly"></span><span id="_SECURITY_SMART_CARD_SUBSYSTEM_GLY"></span>**sous-système de carte à puce**
</dt> <dd>

Sous-système utilisé pour fournir un lien entre les lecteurs de carte à puce et les applications prenant en charge les cartes à puce.

</dd> <dt>

<span id="_security_software_publisher_certificate_gly"></span><span id="_SECURITY_SOFTWARE_PUBLISHER_CERTIFICATE_GLY"></span>**Certificat de l’éditeur de logiciel**
</dt> <dd>

VOIE Objet de \# données signées PKCS 7 qui contient des certificats X. 509.

</dd> <dt>

<span id="_security_spc_gly"></span><span id="_SECURITY_SPC_GLY"></span>**VOIE**
</dt> <dd>

Consultez *certificat* de l’éditeur de logiciel.

</dd> <dt>

<span id="_security_spn_gly"></span><span id="_SECURITY_SPN_GLY"></span>**SPN**
</dt> <dd>

Consultez *nom de principal du service*.

</dd> <dt>

<span id="_security_ssl_gly"></span><span id="_SECURITY_SSL_GLY"></span>**Socket**
</dt> <dd>

Consultez *SSL (Secure Sockets Layer) protocole*.

</dd> <dt>

<span id="_security_ssl3_client_authentication_algorithm_gly"></span><span id="_SECURITY_SSL3_CLIENT_AUTHENTICATION_ALGORITHM_GLY"></span>**Algorithme d’authentification du client SSL3**
</dt> <dd>

Algorithme utilisé pour l’authentification du client dans SSL (Secure Sockets Layer) (SSL) version 3. Dans le protocole SSL3, une concaténation d’un hachage MD5 et d’un hachage SHA-1 est signée avec une clé privée RSA. CryptoAPI et la base Microsoft et les fournisseurs de services de chiffrement améliorés prennent en charge SSL3 avec le type de hachage CALG \_ SSL3 \_ SHAMD5.

</dd> <dt>

<span id="_security_ssl3_protocol_gly"></span><span id="_SECURITY_SSL3_PROTOCOL_GLY"></span>**Protocole SSL3**
</dt> <dd>

Version 3 du protocole SSL (Secure Sockets Layer) (SSL).

</dd> <dt>

<span id="_security_sso_gly"></span><span id="_SECURITY_SSO_GLY"></span>**SIGNATURE**
</dt> <dd>

Voir *authentification unique*.

</dd> <dt>

<span id="_security_ssp_gly"></span><span id="_SECURITY_SSP_GLY"></span>**CADRE**
</dt> <dd>

Consultez *Security Support Provider*.

</dd> <dt>

<span id="_security_sspi_gly"></span><span id="_SECURITY_SSPI_GLY"></span>**INTERFACE**
</dt> <dd>

Voir *interface du fournisseur de support de sécurité*.

</dd> <dt>

<span id="_security_sst_gly"></span><span id="_SECURITY_SST_GLY"></span>**SST**
</dt> <dd>

Consultez *format du magasin de certificats sérialisé*.

</dd> <dt>

<span id="_security_state_gly"></span><span id="_SECURITY_STATE_GLY"></span>**Département**
</dt> <dd>

Ensemble de toutes les valeurs persistantes associées à une entité de chiffrement telle qu’une clé ou un hachage. Cet ensemble peut inclure des éléments tels que le [*vecteur d’initialisation*](i-gly.md) (IV) utilisé, l’algorithme utilisé ou la valeur de l’entité déjà calculée.

</dd> <dt>

<span id="_security_stream_cipher_gly"></span><span id="_SECURITY_STREAM_CIPHER_GLY"></span>**chiffrement de flux**
</dt> <dd>

Chiffrement qui chiffre en série les données, un bit à la fois.

Voir aussi [*chiffrement par bloc*](b-gly.md).

</dd> <dt>

<span id="_security_subauthentication_package_gly"></span><span id="_SECURITY_SUBAUTHENTICATION_PACKAGE_GLY"></span>**package de sous-authentification**
</dt> <dd>

DLL facultative qui fournit des fonctionnalités d’authentification supplémentaires, généralement en étendant l’algorithme d’authentification. Si un package de sous-authentification est installé, le package d’authentification appellera le package de sous-authentification avant de renvoyer son résultat d’authentification à l’autorité de sécurité locale (LSA).

Voir aussi [*autorité de sécurité locale*](l-gly.md).

</dd> <dt>

<span id="_security_subject_interface_package_gly"></span><span id="_SECURITY_SUBJECT_INTERFACE_PACKAGE_GLY"></span>**package d’interface objet**
</dt> <dd>

PANNEAU Spécification propriétaire Microsoft pour une couche logicielle qui permet aux applications de créer, stocker, récupérer et vérifier une signature d’objet. Les sujets incluent, sans s’y limiter, les images exécutables portables (. exe), les images CAB (. cab), les fichiers plats et les fichiers de catalogue. Chaque type d’objet utilise un sous-ensemble différent de ses données pour le calcul du hachage et requiert une procédure différente pour le stockage et la récupération. Par conséquent, chaque type d’objet a une spécification de package d’interface objet unique.

</dd> <dt>

<span id="_security_suite_b_gly"></span><span id="_SECURITY_SUITE_B_GLY"></span>**Suite B**
</dt> <dd>

Un ensemble d’algorithmes de chiffrement déclarés de manière ouverte par l’Agence de sécurité nationale américaine dans le cadre de son programme de modernisation du chiffrement.

</dd> <dt>

<span id="_security_supplemental_credentials_gly"></span><span id="_SECURITY_SUPPLEMENTAL_CREDENTIALS_GLY"></span>**informations d’identification supplémentaires**
</dt> <dd>

Informations d’identification à utiliser lors de l’authentification d’un *principal de sécurité* pour les domaines de sécurité étrangers.

Voir aussi [*informations d’identification principales*](p-gly.md).

</dd> <dt>

<span id="_security_symmetric_algorithm_gly"></span><span id="_SECURITY_SYMMETRIC_ALGORITHM_GLY"></span>**algorithme symétrique**
</dt> <dd>

Algorithme de chiffrement qui utilise généralement une clé unique, souvent appelée clé de session, pour le chiffrement et le déchiffrement. Les algorithmes symétriques peuvent être divisés en deux catégories : les algorithmes de flux et les algorithmes de bloc (également appelés [*chiffrements*](b-gly.md)de *flux* et de bloc).

</dd> <dt>

<span id="_security_symmetric_encryption_gly"></span><span id="_SECURITY_SYMMETRIC_ENCRYPTION_GLY"></span>**chiffrement symétrique**
</dt> <dd>

Chiffrement qui utilise une clé unique à la fois pour le chiffrement et le déchiffrement. Le chiffrement symétrique est préférable lors du chiffrement de grandes quantités de données. Les algorithmes de chiffrement symétrique les plus courants sont [*RC2*](r-gly.md), [*RC4*](r-gly.md)et [*Data Encryption Standard*](d-gly.md) (des).

Voir aussi [*chiffrement à clé publique*](p-gly.md).

</dd> <dt>

<span id="_security_symmetric_key_gly"></span><span id="_SECURITY_SYMMETRIC_KEY_GLY"></span>**clé symétrique**
</dt> <dd>

Clé secrète utilisée avec un algorithme de chiffrement symétrique (autrement dit, un algorithme qui utilise la même clé pour le chiffrement et le déchiffrement). Une telle clé doit être connue de tous les tiers communicants.

</dd> <dt>

<span id="_security_system_access_control_list_gly"></span><span id="_SECURITY_SYSTEM_ACCESS_CONTROL_LIST_GLY"></span>**liste de contrôle d’accès système**
</dt> <dd>

SACL LISTE de contrôle d’accès qui contrôle la génération des messages d’audit pour les tentatives d’accès à un objet sécurisable. La capacité d’obtenir ou de définir la liste SACL d’un objet est contrôlée par un privilège généralement détenu uniquement par les administrateurs système.

Voir aussi [*liste de contrôle d’accès*](a-gly.md), [*liste de contrôle d’accès discrétionnaire*](d-gly.md), [*privilège*](p-gly.md).

</dd> <dt>

<span id="_security_system_program_interface_gly"></span><span id="_SECURITY_SYSTEM_PROGRAM_INTERFACE_GLY"></span>**interface du programme système**
</dt> <dd>

Ensemble des fonctions fournies par un [*fournisseur de services de chiffrement*](c-gly.md) (CSP) qui implémente les fonctions d’une application.

</dd> </dl>

 

 



