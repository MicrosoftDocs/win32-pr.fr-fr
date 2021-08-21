---
description: Contient les définitions des termes de sécurité qui commencent par la lettre P.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a
title: P (Glossaire de la sécurité)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea06fef6f39c1cbee3adbb8f53870013da9cec52cceef6e318e679af42fd37ac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117969957"
---
# <a name="p-security-glossary"></a>P (Glossaire de la sécurité)

[A](a-gly.md) [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) [e](e-gly.md) F [G](g-gly.md) [H](h-gly.md) [I](i-gly.md) J [K](k-gly.md) [L](l-gly.md) [M](m-gly.md) [N](n-gly.md) [O](o-gly.md) P Q [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) [W](w-gly.md) [X](x-gly.md) Y Z

<dl> <dt>

<span id="_security_padding_gly"></span><span id="_SECURITY_PADDING_GLY"></span>**remplissage**
</dt> <dd>

Chaîne, généralement ajoutée quand le dernier bloc de texte en clair est court. Par exemple, si la longueur de bloc est de 64 bits et que le dernier bloc contient uniquement 40 bits, 24 bits de remplissage doivent être ajoutés au dernier bloc. La chaîne de remplissage peut contenir des zéros, des zéros et des zéros, ou un autre modèle. Les applications qui utilisent [*CryptoAPI*](c-gly.md) n’ont pas besoin d’ajouter un remplissage à leur texte en clair avant d’être chiffrées, ni de les supprimer après le déchiffrement. Tout est géré automatiquement.

</dd> <dt>

<span id="_security_password_filter_gly"></span><span id="_SECURITY_PASSWORD_FILTER_GLY"></span>**filtre de mot de passe**
</dt> <dd>

DLL qui fournit une mise en œuvre de la stratégie de mot de passe et une notification de modification. Les fonctions implémentées par les filtres de mot de passe sont appelées par l' [*autorité de sécurité locale*](l-gly.md).

</dd> <dt>

<span id="_security_persistent_storage_gly"></span><span id="_SECURITY_PERSISTENT_STORAGE_GLY"></span>**stockage persistant**
</dt> <dd>

Tout support de stockage qui reste intact lorsque la puissance est déconnectée. De nombreuses bases de données du [*magasin de certificats*](c-gly.md) sont des formes de stockage persistant.

</dd> <dt>

<span id="_security_pkcs_gly"></span><span id="_SECURITY_PKCS_GLY"></span>**PKCS#12**
</dt> <dd>

Consultez *normes de cryptographie à clé publique*.

</dd> <dt>

<span id="_security_pkcs_1_standard_gly"></span><span id="_SECURITY_PKCS_1_STANDARD_GLY"></span>**PKCS \# 1**
</dt> <dd>

Normes recommandées pour l’implémentation du chiffrement à clé publique basée sur l’algorithme RSA, tel que défini dans la [norme RFC 3447](https://tools.ietf.org/html/rfc3447).

</dd> <dt>

<span id="_security_pkcs_12_standard_gly"></span><span id="_SECURITY_PKCS_12_STANDARD_GLY"></span>**PKCS \# 12**
</dt> <dd>

informations personnelles Exchange la norme de syntaxe, développée et gérée par RSA Data Security, Inc. Cette norme de syntaxe spécifie un format portable pour le stockage ou le transport des clés privées, des certificats et des secrets divers d’un utilisateur.

Voir également les *normes de chiffrement* des [*certificats*](c-gly.md) et des clés publiques.

</dd> <dt>

<span id="_security_pkcs_7_signed_data_gly"></span><span id="_SECURITY_PKCS_7_SIGNED_DATA_GLY"></span>**\#Données signées PKCS 7**
</dt> <dd>

Objet de données signé avec la norme publique de chiffrement à clé publique \# 7 (PKCS \# 7) et qui encapsule les informations utilisées pour signer un fichier. En règle générale, il comprend le certificat du signataire et le [*certificat racine*](r-gly.md).

</dd> <dt>

<span id="_security_pkcs_7_standard_gly"></span><span id="_SECURITY_PKCS_7_STANDARD_GLY"></span>**PKCS \# 7**
</dt> <dd>

Norme de syntaxe de message de chiffrement. Syntaxe générale des données auxquelles le chiffrement peut être appliqué, telles que les signatures numériques et le chiffrement. Il fournit également une syntaxe pour diffuser des certificats ou des listes de révocation de certificats et d’autres attributs de message, tels que des horodatages, au message.

</dd> <dt>

<span id="_security_pkcs_7_asn_encoding_gly"></span><span id="_SECURITY_PKCS_7_ASN_ENCODING_GLY"></span>**Encodage ASN de PKCS \_ 7 \_ \_**
</dt> <dd>

[*Type d’encodage de message*](m-gly.md). Les types d’encodage de message sont stockés dans le mot de poids fort d’une valeur **DWORD** (la valeur est : 0x00010000).

</dd> <dt>

<span id="_security_plaintext_gly"></span><span id="_SECURITY_PLAINTEXT_GLY"></span>**en**
</dt> <dd>

Message non chiffré. Les messages en texte brut sont quelquefois connus sous le nom de messages en texte clair.

</dd> <dt>

<span id="_security_portable_executable_pe_image_gly"></span><span id="_SECURITY_PORTABLE_EXECUTABLE_PE_IMAGE_GLY"></span>**Image PE (Portable Executable)**
</dt> <dd>

format d’exécutable standard Windows.

</dd> <dt>

<span id="_security_prf_gly"></span><span id="_SECURITY_PRF_GLY"></span>**PRF**
</dt> <dd>

Consultez *fonction Pseudo-aléatoire*.

</dd> <dt>

<span id="_security_primary_credentials_gly"></span><span id="_SECURITY_PRIMARY_CREDENTIALS_GLY"></span>**informations d’identification principales**
</dt> <dd>

Le \_ package d’authentification MsV1 0 définit une valeur de chaîne de clé d’informations d’identification primaire : la chaîne d’informations d’identification principales contient les informations d’identification fournies lors de l’ouverture de session initiale. Il comprend le nom d’utilisateur et les formes qui respectent la casse et qui ne respectent pas la casse du mot de passe de l’utilisateur.

Voir aussi [*informations d’identification supplémentaires*](s-gly.md).

</dd> <dt>

<span id="_security_primary_service_provider_gly"></span><span id="_SECURITY_PRIMARY_SERVICE_PROVIDER_GLY"></span>**fournisseur de services principal**
</dt> <dd>

Fournisseur de services qui fournit les interfaces de contrôle à la carte. Chaque carte à puce peut inscrire son fournisseur de services principal dans la base de données des cartes à puce.

</dd> <dt>

<span id="_security_primary_token_gly"></span><span id="_SECURITY_PRIMARY_TOKEN_GLY"></span>**jeton principal**
</dt> <dd>

jeton d’accès qui est généralement créé uniquement par le noyau Windows. Il peut être assigné à un processus pour représenter les informations de sécurité par défaut pour ce processus.

Voir aussi jeton d' [*accès*](a-gly.md) et jeton d' [*emprunt d’identité*](i-gly.md).

</dd> <dt>

<span id="_security_principal_gly"></span><span id="_SECURITY_PRINCIPAL_GLY"></span>**Directeur**
</dt> <dd>

Consultez [*principal de sécurité*](s-gly.md).

</dd> <dt>

<span id="_security_privacy_gly"></span><span id="_SECURITY_PRIVACY_GLY"></span>**nominative**
</dt> <dd>

Condition qui est isolée de la vue ou du secret. En ce qui concerne les messages, les messages privés sont des messages chiffrés dont le texte est masqué. En ce qui concerne les clés, une clé privée est une clé secrète masquée des autres.

</dd> <dt>

<span id="_security_private_key_gly"></span><span id="_SECURITY_PRIVATE_KEY_GLY"></span>**clé privée**
</dt> <dd>

Moitié secrète d’une paire de clés utilisée dans un algorithme de clé publique. Les clés privées sont utilisées en général pour chiffrer une clé de session symétrique, signer numériquement un message ou déchiffrer un message qui a été chiffré avec la clé publique correspondante.

Voir aussi *clé publique*.

</dd> <dt>

<span id="_security_private_key_blob_gly"></span><span id="_SECURITY_PRIVATE_KEY_BLOB_GLY"></span>**BLOB de clé privée**
</dt> <dd>

Objet BLOB de clé qui contient une paire de clés publique/privée complète. Les objets BLOB de clé privée sont utilisés par les programmes d’administration pour transporter les paires de clés. Comme la partie clé privée de la paire de clés est extrêmement confidentielle, ces objets BLOB sont généralement gardés chiffrés à l’aide d’un chiffrement symétrique. Ces objets BLOB de clé peuvent également être utilisés par les applications avancées où les paires de clés sont stockées au sein de l’application, plutôt que de s’appuyer sur le mécanisme de stockage du CSP. Un objet BLOB de clé est créé en appelant la fonction **CryptExportKey** .

</dd> <dt>

<span id="_security_privilege_gly"></span><span id="_SECURITY_PRIVILEGE_GLY"></span>**limités**
</dt> <dd>

Droit d'un utilisateur à exécuter différentes opérations relatives au système, telles que l'arrêt du système, le chargement de pilotes de périphériques, ou la modification de l'heure système. Le jeton d’accès d’un utilisateur contient une liste des privilèges détenus par l’utilisateur ou par les groupes de l’utilisateur.

</dd> <dt>

<span id="_security_process_gly"></span><span id="_SECURITY_PROCESS_GLY"></span>**traiter**
</dt> <dd>

Contexte de sécurité dans lequel une application s'exécute. En général, le contexte de sécurité est associé à un utilisateur, donc toutes les applications qui s'exécutent dans un processus donné récupèrent les autorisations et les privilèges de l'utilisateur à qui elles appartiennent.

</dd> <dt>

<span id="_security_prov_dss_gly"></span><span id="_SECURITY_PROV_DSS_GLY"></span>**DSS PROVen \_**
</dt> <dd>

Consultez *\_ type de fournisseur DSS Proven*.

</dd> <dt>

<span id="_security_prov_dss_provider_type_gly"></span><span id="_SECURITY_PROV_DSS_PROVIDER_TYPE_GLY"></span>**Type de fournisseur PROVen \_ DSS**
</dt> <dd>

Type de fournisseur prédéfini qui prend uniquement en charge les signatures numériques et les hachages. Il spécifie l’algorithme de signature DSA et les algorithmes de hachage MD5 et SHA-1.

</dd> <dt>

<span id="_security_prov_dss_dh_gly"></span><span id="_SECURITY_PROV_DSS_DH_GLY"></span>**PROVen \_ DSS \_**
</dt> <dd>

Consultez *le \_ \_ type de fournisseur Proven DSS*.

</dd> <dt>

<span id="_security_prov_dss_dh_provider_type_gly"></span><span id="_SECURITY_PROV_DSS_DH_PROVIDER_TYPE_GLY"></span>**\_Type de fournisseur prouvé DSS- \_ DH**
</dt> <dd>

Type de fournisseur prédéfini qui fournit l’échange de clés, la signature numérique et les algorithmes de hachage. Elle est similaire au type de \_ fournisseur DSS Proven.

</dd> <dt>

<span id="_security_prov_fortezza_gly"></span><span id="_SECURITY_PROV_FORTEZZA_GLY"></span>**\_Fortezza-Fortezza**
</dt> <dd>

Consultez *\_ type de fournisseur Fortezza*.

</dd> <dt>

<span id="_security_prov_fortezza_provider_type_gly"></span><span id="_SECURITY_PROV_FORTEZZA_PROVIDER_TYPE_GLY"></span>**Type de fournisseur Fortezza de la preuve \_**
</dt> <dd>

Type de fournisseur prédéfini qui fournit l’échange de clés, la signature numérique, le chiffrement et les algorithmes de hachage. Les protocoles et algorithmes de chiffrement spécifiés par ce type de fournisseur sont détenus par le NIST (National Institute of Standards and Technology).

</dd> <dt>

<span id="_security_prov_ms_exchange_gly"></span><span id="_SECURITY_PROV_MS_EXCHANGE_GLY"></span>**PROUVER \_ MS \_ Exchange**
</dt> <dd>

Consultez *\_ type de \_ fournisseur MS Exchange Prov*.

</dd> <dt>

<span id="_security_prov_ms_exchange_provider_type_gly"></span><span id="_SECURITY_PROV_MS_EXCHANGE_PROVIDER_TYPE_GLY"></span>**\_Type de \_ fournisseur MS Exchange Prov.**
</dt> <dd>

type de fournisseur prédéfini conçu pour les besoins de microsoft Exchange, ainsi que d’autres applications compatibles avec microsoft Mail. Il fournit l’échange de clés, la signature numérique, le chiffrement et les algorithmes de hachage.

</dd> <dt>

<span id="_security_prov_rsa_full_gly"></span><span id="_SECURITY_PROV_RSA_FULL_GLY"></span>**PROUVER \_ RSA \_ Full**
</dt> <dd>

Consultez la page *prouver le \_ type de \_ fournisseur complet RSA*.

</dd> <dt>

<span id="_security_prov_rsa_full_provider_type_gly"></span><span id="_SECURITY_PROV_RSA_FULL_PROVIDER_TYPE_GLY"></span>**\_Type de \_ fournisseur complet RSA Prov.**
</dt> <dd>

Type de fournisseur prédéfini défini par Microsoft et RSA Data Security, Inc. Ce type de fournisseur à usage général fournit l’échange de clés, la signature numérique, le chiffrement et les algorithmes de hachage. L’échange de clés, la signature numérique et les algorithmes de chiffrement sont basés sur le chiffrement à clé publique RSA.

</dd> <dt>

<span id="_security_prov_rsa_sig_gly"></span><span id="_SECURITY_PROV_RSA_SIG_GLY"></span>**PROUVER \_ RSA \_ SIG**
</dt> <dd>

Consultez la page *prouver le \_ type de \_ fournisseur RSA SIG*.

</dd> <dt>

<span id="_security_prov_rsa_sig_provider_type_gly"></span><span id="_SECURITY_PROV_RSA_SIG_PROVIDER_TYPE_GLY"></span>**\_Type de \_ fournisseur prouver RSA SIG**
</dt> <dd>

Type de fournisseur prédéfini défini par Microsoft et RSA Data Security. Ce type de fournisseur est un sous-ensemble de la preuve \_ \_ complète RSA qui fournit uniquement des algorithmes de hachage et de signature numérique. L’algorithme de signature numérique est un algorithme de clé publique RSA.

</dd> <dt>

<span id="_security_prov_ssl_gly"></span><span id="_SECURITY_PROV_SSL_GLY"></span>**SSL PROV. \_**
</dt> <dd>

Consultez *\_ type de fournisseur SSL Prov*.

</dd> <dt>

<span id="_security_prov_ssl_provider_type_gly"></span><span id="_SECURITY_PROV_SSL_PROVIDER_TYPE_GLY"></span>**\_Type de fournisseur de chiffrement SSL Prov**
</dt> <dd>

Type de fournisseur prédéfini qui prend en charge le protocole SSL (Secure Sockets Layer) (SSL). Ce type fournit le chiffrement à clé, la signature numérique, le chiffrement et les algorithmes de hachage. Une spécification décrivant le protocole SSL est disponible auprès de Netscape Communications Corp.

</dd> <dt>

<span id="_security_provider_gly"></span><span id="_SECURITY_PROVIDER_GLY"></span>**moteur**
</dt> <dd>

Consultez [*fournisseur de services de chiffrement*](c-gly.md).

</dd> <dt>

<span id="_security_provider_name_gly"></span><span id="_SECURITY_PROVIDER_NAME_GLY"></span>**nom du fournisseur**
</dt> <dd>

Nom utilisé pour identifier un CSP. Par exemple, le fournisseur de services de chiffrement de base Microsoft version 1,0. Le nom du fournisseur est généralement utilisé lors de l’appel de la fonction **CryptAcquireContext** pour se connecter à un CSP.

</dd> <dt>

<span id="_security_provider_type_gly"></span><span id="_SECURITY_PROVIDER_TYPE_GLY"></span>**type de fournisseur**
</dt> <dd>

Terme utilisé pour identifier un type de fournisseur de services de chiffrement (CSP). Les fournisseurs de services de chiffrement sont regroupés en différents types de fournisseurs qui représentent une famille spécifique de formats de données et de protocoles standard. Contrairement au nom unique du fournisseur CSP, les types de fournisseurs ne sont pas uniques pour un CSP donné. Le type de fournisseur est généralement utilisé lors de l’appel de la fonction **CryptAcquireContext** pour se connecter à un CSP.

</dd> <dt>

<span id="_security_pseudo_random_function_gly"></span><span id="_SECURITY_PSEUDO_RANDOM_FUNCTION_GLY"></span>**fonction Pseudo-aléatoire**
</dt> <dd>

PRF Fonction qui prend une clé, une étiquette et une valeur initiale comme entrée, puis produit une sortie de longueur arbitraire.

</dd> <dt>

<span id="_security_public_private_key_pair_gly"></span><span id="_SECURITY_PUBLIC_PRIVATE_KEY_PAIR_GLY"></span>**paire de clés publique/privée**
</dt> <dd>

Jeu de clés de chiffrement utilisé pour le chiffrement à clé publique. Pour chaque utilisateur, un fournisseur de services Cloud gère généralement deux paires de clés publiques/privées : une paire de clés d’échange et une paire de clés de signature numérique. Les deux paires de clés sont conservées d'une session à une autre.

Consultez paire de clés et paire de [*clés de signature*](s-gly.md) [*Exchange*](e-gly.md) .

</dd> <dt>

<span id="_security_public_key_gly"></span><span id="_SECURITY_PUBLIC_KEY_GLY"></span>**clé publique**
</dt> <dd>

Clé de chiffrement utilisée en général pour déchiffrer une clé de session ou une signature numérique. La clé publique peut également être utilisée pour chiffrer un message, ce qui garantit que seule la personne avec la clé privée correspondante peut déchiffrer le message.

Voir aussi *clé privée*.

</dd> <dt>

<span id="_security_public_key_algorithm_gly"></span><span id="_SECURITY_PUBLIC_KEY_ALGORITHM_GLY"></span>**algorithme de clé publique**
</dt> <dd>

Un chiffrement asymétrique qui utilise deux clés : une pour le chiffrement, la clé publique et l’autre pour le déchiffrement, la clé privée. Comme les noms de clé le présupposent, la clé publique utilisée pour encoder du texte brut peut être mise à la disposition de tout le monde. Toutefois, la clé privée doit rester secrète. Seule la clé privée peut déchiffrer le texte chiffré. L’algorithme de clé publique utilisé dans ce processus est lent (de l’ordre de 1 000 fois plus lentement que les algorithmes symétriques), et est généralement utilisé pour chiffrer les clés de session ou signer numériquement un message.

Voir aussi *clé publique* et *clé privée*.

</dd> <dt>

<span id="_security_public_key_blob_gly"></span><span id="_SECURITY_PUBLIC_KEY_BLOB_GLY"></span>**objet BLOB de clé publique**
</dt> <dd>

Objet BLOB utilisé pour stocker la partie clé publique d’une paire de clés publique/privée. Les objets BLOB de clé publique ne sont pas chiffrés, car la clé publique contenue dans n’est pas secrète. Un objet BLOB de clé publique est créé en appelant la fonction **CryptExportKey** .

</dd> <dt>

<span id="_security_public_key_cryptography_standards_gly"></span><span id="_SECURITY_PUBLIC_KEY_CRYPTOGRAPHY_STANDARDS_GLY"></span>**Normes de chiffrement à clé publique**
</dt> <dd>

PKCS#12 Ensemble de normes syntaxiques pour le chiffrement à clé publique couvrant les fonctions de sécurité, y compris les méthodes pour la signature des données, l’échange de clés, la demande de certificats, le chiffrement et le déchiffrement à clé publique, ainsi que d’autres fonctions de sécurité.

</dd> <dt>

<span id="_security_public_key_encryption_gly"></span><span id="_SECURITY_PUBLIC_KEY_ENCRYPTION_GLY"></span>**chiffrement à clé publique**
</dt> <dd>

Chiffrement qui utilise une paire de clés, une clé pour chiffrer des données et une autre clé pour déchiffrer des données. Par opposition, algorithmes de chiffrement symétrique qui utilisent la même clé à la fois pour le chiffrement et le déchiffrement. Dans la pratique, le chiffrement à clé publique est généralement utilisé pour protéger la clé de session utilisée par un algorithme de chiffrement symétrique. Dans ce cas, la clé publique est utilisée pour chiffrer la clé de session, qui a ensuite été utilisée pour chiffrer des données, et la clé privée est utilisée pour le déchiffrement. En plus de protéger les clés de session, le chiffrement à clé publique peut également être utilisé pour signer un message numériquement (à l'aide de la clé privée) et valider la signature (à l'aide de la clé publique).

Voir aussi *algorithme de clé publique*.

</dd> </dl>

 

 



