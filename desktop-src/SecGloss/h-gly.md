---
description: Contient les définitions des termes de sécurité qui commencent par la lettre H.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 4165b820-30fc-477e-a690-81109f161323
title: H (Glossaire de la sécurité)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 665cd90cfc8a849030b6a1cfd1cb4e6d6f687557
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127311282"
---
# <a name="h-security-glossary"></a>H (Glossaire de la sécurité)

[A](a-gly.md) [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) [e](e-gly.md) F [G](g-gly.md) H [I](i-gly.md) J [K](k-gly.md) [L](l-gly.md) [M](m-gly.md) [N](n-gly.md) [O](o-gly.md) [P](p-gly.md) Q [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) [W](w-gly.md) [X](x-gly.md) Y Z

<dl> <dt>

<span id="_security_handle_gly"></span><span id="_SECURITY_HANDLE_GLY"></span>**traitée**
</dt> <dd>

Jeton utilisé pour identifier ou accéder à un objet, tel que le handle d’un fournisseur de services de chiffrement, d’un magasin de certificats, d’un message ou d’une paire de clés.

</dd> <dt>

<span id="_security_hash_gly"></span><span id="_SECURITY_HASH_GLY"></span>**format**
</dt> <dd>

Résultat de taille fixe obtenu en appliquant une fonction mathématique (l' *algorithme de hachage*) à une quantité arbitraire de données. (Également appelé « synthèse des messages »)

Voir aussi *fonctions de hachage*.

</dd> <dt>

<span id="_security_hash_object_gly"></span><span id="_SECURITY_HASH_OBJECT_GLY"></span>**objet de hachage**
</dt> <dd>

Objet utilisé pour hacher des messages ou des clés de session. L’objet de hachage est créé par un appel à **CryptCreateHash**. La définition de l’objet est définie par le fournisseur de services de chiffrement spécifié dans l’appel.

</dd> <dt>

<span id="_security_hashing_algorithm_gly"></span><span id="_SECURITY_HASHING_ALGORITHM_GLY"></span>**algorithme de hachage**
</dt> <dd>

Algorithme utilisé pour produire une valeur de hachage d'un échantillon de données, tel qu'un message ou une clé de session. Les algorithmes de hachage typiques incluent MD2, MD4, MD5 et SHA-1.

</dd> <dt>

<span id="_security_hashing_functions_gly"></span><span id="_SECURITY_HASHING_FUNCTIONS_GLY"></span>**fonctions de hachage**
</dt> <dd>

Ensemble de fonctions utilisées pour créer et détruire des objets de hachage, obtenir ou définir les paramètres d’un objet de hachage, ainsi que des données de hachage et des clés de session.

</dd> <dt>

<span id="_security_hash_based_message_authentication_code_gly"></span><span id="_SECURITY_HASH_BASED_MESSAGE_AUTHENTICATION_CODE_GLY"></span>**Code d’authentification de message basées sur le hachage**
</dt> <dd>

CALCULÉ Algorithme de hachage à clé symétrique implémenté par les fournisseurs de services de chiffrement Microsoft. Un HMAC est utilisé pour vérifier l’intégrité des données afin de s’assurer qu’elles n’ont pas été modifiées pendant le stockage ou le transit. Il peut être utilisé avec n’importe quel algorithme de hachage de chiffrement itéré, tel que MD5 ou SHA-1. CryptoAPI fait référence à cet algorithme par son identificateur d’algorithme (CALG \_ HMAC) et sa classe (classe de hachage de la \_ classe ALG \_ ).

Voir aussi [*code d’Authentification de message*](m-gly.md).

</dd> <dt>

<span id="_security_hcsbc_gly"></span><span id="_SECURITY_HCSBC_GLY"></span>**HCSBC**
</dt> <dd>

Type de données qui sert de handle à un contexte de sauvegarde des services de certificats. Son rôle est de maintenir l’état de contexte entre le serveur et les API de sauvegarde lors de l’exécution d’une sauvegarde.

</dd> <dt>

<span id="_security_hmac_gly"></span><span id="_SECURITY_HMAC_GLY"></span>**CALCULÉ**
</dt> <dd>

Consultez *code d’Authentification de message basées sur le hachage*.

</dd> </dl>

 

 



