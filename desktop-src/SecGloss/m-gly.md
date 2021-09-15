---
description: Contient les définitions des termes de sécurité qui commencent par la lettre M.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 4c4402e9-7455-4868-978f-3899a8fd86c1
title: M (Glossaire de la sécurité)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db63fc76d4b8b803d523c46012dcb10ed5380e4a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127311269"
---
# <a name="m-security-glossary"></a>M (Glossaire de la sécurité)

[A](a-gly.md) [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) [e](e-gly.md) F [G](g-gly.md) [H](h-gly.md) [I](i-gly.md) J [K](k-gly.md) [L](l-gly.md) M [N](n-gly.md) [O](o-gly.md) [P](p-gly.md) Q [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) [W](w-gly.md) [X](x-gly.md) Y Z

<dl> <dt>

<span id="_security_mac_gly"></span><span id="_SECURITY_MAC_GLY"></span>**Macintosh**
</dt> <dd>

Consultez *code d’Authentification de message*.

</dd> <dt>

<span id="_security_mac_key_gly"></span><span id="_SECURITY_MAC_KEY_GLY"></span>**Clé MAC**
</dt> <dd>

Clé de code d’authentification de message utilisée avec les protocoles [*Schannel*](s-gly.md) .

</dd> <dt>

<span id="_security_master_key_gly"></span><span id="_SECURITY_MASTER_KEY_GLY"></span>**clé principale**
</dt> <dd>

Clé utilisée par le client et le serveur pour toute la génération de la clé de session. La clé principale est utilisée pour générer la clé de lecture du client, la clé d’écriture du client, la clé de lecture du serveur et la clé d’écriture sur le serveur. Les clés principales peuvent être exportées en tant qu’objets BLOB de clé simple.

</dd> <dt>

<span id="_security_md2_gly"></span><span id="_SECURITY_MD2_GLY"></span>**MD2**
</dt> <dd>

Nom de l’algorithme CryptoAPI pour l’algorithme de hachage MD2. Parmi les autres algorithmes de hachage, citons *MD4*, *MD5* et [*SHA*](s-gly.md).

Voir aussi *algorithme MD2*.

</dd> <dt>

<span id="_security_md2_algorithm_gly"></span><span id="_SECURITY_MD2_ALGORITHM_GLY"></span>**MD2 (algorithme)**
</dt> <dd>

MD2 Algorithme de hachage qui crée une valeur de hachage 128 bits. MD2 a été optimisé pour une utilisation avec des ordinateurs 8 bits. CryptoAPI fait référence à cet algorithme par son type (CALG \_ MD2), son nom (Mac) et sa classe ( \_ classe de hachage ALG \_ ). MD2 a été développé par RSA Data Security, Inc.

Voir aussi *algorithme MD4*, *algorithme MD5*.

</dd> <dt>

<span id="_security_md4_gly"></span><span id="_SECURITY_MD4_GLY"></span>**MD4**
</dt> <dd>

Nom de l’algorithme CryptoAPI pour l’algorithme de hachage MD4. Les autres algorithmes de hachage incluent *MD2*, *MD5* et [*SHA*](s-gly.md).

Consultez l' *algorithme MD4*.

</dd> <dt>

<span id="_security_md4_algorithm_gly"></span><span id="_SECURITY_MD4_ALGORITHM_GLY"></span>**Algorithme MD4**
</dt> <dd>

MD4 Algorithme de hachage qui crée une valeur de hachage 128 bits. MD4 a été optimisé pour les ordinateurs 32 bits. Elle est maintenant considérée comme rompue, car les collisions peuvent être détectées trop rapidement et facilement. MD4 a été développé par RSA Data Security, Inc.

Voir aussi *algorithme MD2*, *algorithme MD5*.

</dd> <dt>

<span id="_security_md5_gly"></span><span id="_SECURITY_MD5_GLY"></span>**ISSU**
</dt> <dd>

Nom de l’algorithme CryptoAPI pour l’algorithme de hachage MD5. Les autres algorithmes de hachage incluent *MD2*, *MD4* et [*SHA*](s-gly.md).

Voir aussi *algorithme MD5*.

</dd> <dt>

<span id="_security_md5_algorithm_gly"></span><span id="_SECURITY_MD5_ALGORITHM_GLY"></span>**Algorithme MD5**
</dt> <dd>

ISSU Algorithme de hachage qui crée une valeur de hachage 128 bits. MD5 a été optimisé pour les ordinateurs 32 bits. CryptoAPI fait référence à cet algorithme par son identificateur d’algorithme (CALG \_ MD5), son nom (MD5) et sa classe ( \_ classe de hachage ALG \_ ). MD5 a été développé par RSA Data Security, Inc. et est spécifié par les types PROV RSA \_ \_ complet, Prov- \_ RSA \_ SIG, Proven \_ DSS, Prov \_ DSS \_ DH et prove de \_ \_ fournisseurs MS Exchange.

Voir aussi *algorithme MD2*, *algorithme MD4*.

</dd> <dt>

<span id="_security_message_gly"></span><span id="_SECURITY_MESSAGE_GLY"></span>**Message**
</dt> <dd>

Toutes les données qui ont été encodées pour être transmises à une personne ou une entité et reçues de celle-ci. Les messages peuvent être chiffrés pour des raisons de confidentialité, signés numériquement à des fins d’authentification ou les deux.

</dd> <dt>

<span id="_security_message_digest_gly"></span><span id="_SECURITY_MESSAGE_DIGEST_GLY"></span>**Résumé du message**
</dt> <dd>

Consultez [*hachage*](h-gly.md).

</dd> <dt>

<span id="_security_message_authentication_code_gly"></span><span id="_SECURITY_MESSAGE_AUTHENTICATION_CODE_GLY"></span>**code d'authentification de message**
</dt> <dd>

Macintosh Algorithme de hachage à clé qui utilise une clé de session symétrique pour garantir qu’un bloc de données a conservé son intégrité à partir du moment où il a été envoyé jusqu’au moment où il a été reçu. Lors de l’utilisation de ce type d’algorithme, l’application réceptrice doit également posséder la clé de session pour recalculer la valeur de hachage afin de pouvoir vérifier que les données de base n’ont pas changé. CryptoAPI fait référence à cet algorithme par son type (CALG \_ Mac), son nom (Mac) et sa classe ( \_ classe de hachage ALG \_ ).

</dd> <dt>

<span id="_security_message_encoding_type_gly"></span><span id="_SECURITY_MESSAGE_ENCODING_TYPE_GLY"></span>**type d’encodage de message**
</dt> <dd>

Définit la façon dont le message est encodé. Le type d’encodage de message est stocké dans le mot de poids fort de la structure de type d’encodage. Les types d’encodage actuellement définis sont : CRYPTer l’encodage \_ ASN \_ , \_ codage ASN x509 \_ et \_ \_ codage ASN PKCS 7 \_ .

</dd> <dt>

<span id="_security_message_management_functions_gly"></span><span id="_SECURITY_MESSAGE_MANAGEMENT_FUNCTIONS_GLY"></span>**fonctions de gestion des messages**
</dt> <dd>

Fonctions qui fournissent deux niveaux de gestion des messages : fonctions de message de bas niveau et fonctions de message simplifiées. Les fonctions de message de bas niveau offrent plus de flexibilité que les fonctions de message simplifiées. Toutefois, ils nécessitent davantage d’appels de fonction.

</dd> <dt>

<span id="_security_message_signing_functions_gly"></span><span id="_SECURITY_MESSAGE_SIGNING_FUNCTIONS_GLY"></span>**fonctions de signature des messages**
</dt> <dd>

Fonctions utilisées pour signer les messages et les données.

Voir aussi [*fonctions de message simplifiées*](s-gly.md).

</dd> <dt>

<span id="_security_mpr_gly"></span><span id="_SECURITY_MPR_GLY"></span>**MPR**
</dt> <dd>

Voir *routeur à plusieurs fournisseurs*.

</dd> <dt>

<span id="_security_multiple_provider_router_gly"></span><span id="_SECURITY_MULTIPLE_PROVIDER_ROUTER_GLY"></span>**Routeur à plusieurs fournisseurs**
</dt> <dd>

MPR Composant système qui gère les communications entre le système et tous les fournisseurs de réseau. Le MPR appelle les fonctions du fournisseur de réseau qui sont exposées par chaque fournisseur de réseau.

</dd> </dl>

 

 



