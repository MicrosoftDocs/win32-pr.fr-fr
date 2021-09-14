---
description: Contient les définitions des termes de sécurité qui commencent par la lettre B.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 2e570727-7da0-4e17-bf5d-6fe0e6aef65b
title: B (Glossaire de la sécurité)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40aedaebddb86ddf9f32a9a3d86cf4cf4a613642
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127013615"
---
# <a name="b-security-glossary"></a>B (Glossaire de la sécurité)

[A](a-gly.md) B [C](c-gly.md) [D](d-gly.md) [e](e-gly.md) F [G](g-gly.md) [H](h-gly.md) [I](i-gly.md) J [K](k-gly.md) [L](l-gly.md) [M](m-gly.md) [N](n-gly.md) [O](o-gly.md) [P](p-gly.md) Q [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) [W](w-gly.md) [X](x-gly.md) Y Z

<dl> <dt>

<span id="_security_backup_authority_gly"></span><span id="_SECURITY_BACKUP_AUTHORITY_GLY"></span>**autorité de sauvegarde**
</dt> <dd>

Application approuvée s’exécutant sur un ordinateur sécurisé qui fournit un stockage secondaire pour les clés de session de ses clients. L’autorité de sauvegarde stocke les clés de session en tant qu’objets BLOB de clé chiffrés avec la clé publique de l’autorité de sauvegarde.

</dd> <dt>

<span id="_security_base_content_type_gly"></span><span id="_SECURITY_BASE_CONTENT_TYPE_GLY"></span>**type de contenu de base**
</dt> <dd>

Type de données contenu dans un message PKCS \# 7. Les types de contenu de base contiennent uniquement des données, aucune amélioration de chiffrement telle que les hachages ou les signatures. Actuellement, le seul type de contenu de base est le type de contenu de données.

</dd> <dt>

<span id="_security_base_cryptographic_functions_gly"></span><span id="_SECURITY_BASE_CRYPTOGRAPHIC_FUNCTIONS_GLY"></span>**fonctions de chiffrement de base**
</dt> <dd>

Niveau le plus bas des fonctions dans l’architecture CryptoAPI. Ils sont utilisés par les applications et d’autres fonctions CryptoAPI de haut niveau pour fournir un accès aux algorithmes de chiffrement fournis par le fournisseur de solutions de chiffrement, à la génération de clés sécurisées et au stockage sécurisé des secrets.

Voir aussi [*fournisseurs de services de chiffrement*](c-gly.md).

</dd> <dt>

<span id="_security_basic_encoding_rules_gly"></span><span id="_SECURITY_BASIC_ENCODING_RULES_GLY"></span>**Règles d’encodage de base**
</dt> <dd>

BER Ensemble de règles utilisées pour encoder les données ASN. 1 définies en un flux de bits (zéros ou autres) pour le stockage ou la transmission externes. Un seul objet ASN. 1 peut avoir plusieurs encodages BER équivalents. BER est défini dans la recommandation CCITT X. 209. Il s’agit de l’une des deux méthodes d’encodage actuellement utilisées par CryptoAPI.

</dd> <dt>

<span id="_security_ber_gly"></span><span id="_SECURITY_BER_GLY"></span>**BER**
</dt> <dd>

Consultez *règles d’encodage de base*.

</dd> <dt>

<span id="_security_big_endian_gly"></span><span id="_SECURITY_BIG_ENDIAN_GLY"></span>**Big endian**
</dt> <dd>

Un format de mémoire ou de données dans lequel l’octet le plus significatif est stocké à l’adresse inférieure ou qui arrive en premier.

Voir aussi [*Little endian*](l-gly.md).

</dd> <dt>

<span id="_security_blob_gly"></span><span id="_SECURITY_BLOB_GLY"></span>**OBJET BLOB**
</dt> <dd>

Séquence générique de bits qui contiennent une ou plusieurs structures d’en-tête de longueur fixe, ainsi que des données spécifiques au contexte.

Voir aussi [*objets BLOB de clé*](k-gly.md), [*objets BLOB de certificat*](c-gly.md), objets BLOB de [*nom de certificat*](c-gly.md)et [*objets BLOB d’attribut*](a-gly.md).

</dd> <dt>

<span id="_security_block_cipher_gly"></span><span id="_SECURITY_BLOCK_CIPHER_GLY"></span>**chiffrement par bloc**
</dt> <dd>

Algorithme de chiffrement qui chiffre les données en unités discrètes (appelées blocs), plutôt qu’en tant que flux continu de bits. La taille de bloc la plus courante est 64 bits. Par exemple, est un chiffrement par bloc.

Voir aussi [*chiffrement de flux*](s-gly.md).

</dd> <dt>

<span id="_security_bulk_encryption_key_gly"></span><span id="_SECURITY_BULK_ENCRYPTION_KEY_GLY"></span>**clé de chiffrement en bloc**
</dt> <dd>

Clé de session dérivée d’une clé principale. Les clés de chiffrement en bloc sont utilisées dans le chiffrement [*Schannel*](s-gly.md) .

</dd> </dl>

 

 



