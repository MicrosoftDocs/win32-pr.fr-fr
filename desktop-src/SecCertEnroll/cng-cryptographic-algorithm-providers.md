---
description: 'Contrairement à l’API de chiffrement (CryptoAPI), API de chiffrement : Next Generation (CNG) sépare les fournisseurs de chiffrement des fournisseurs de stockage de clés.'
ms.assetid: ce29bc97-049e-4c82-979f-4c805a318ba0
title: Fournisseurs d’algorithmes de chiffrement CNG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bc64926236157e581ce6406d95681bd8d4add14
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106538917"
---
# <a name="cng-cryptographic-algorithm-providers"></a>Fournisseurs d’algorithmes de chiffrement CNG

Contrairement à l’API de chiffrement (CryptoAPI), API de chiffrement : Next Generation (CNG) sépare les fournisseurs de chiffrement des fournisseurs de stockage de clés. Les opérations d’algorithme de chiffrement de base, telles que le hachage et la signature, sont appelées opérations primitives ou simplement Primitives. CNG intègre un fournisseur qui implémente les algorithmes suivants.

-   [Algorithmes symétriques](#symmetric-algorithms)
-   [Algorithmes asymétriques](#asymmetric-algorithms)
-   [Algorithmes de hachage](#hashing-algorithms)
-   [Algorithmes d’échange de clés](#key-exchange-algorithms)
-   [Rubriques connexes](#related-topics)

## <a name="symmetric-algorithms"></a>Algorithmes symétriques



| Nom                                   | Modes pris en charge                                                                                                                                                                                                 | Taille de la clé en bits (valeur par défaut/min/max) |
|----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------|
| AES (Advanced Encryption Standard)     | BCE, CBC, CFB8, CFB128, GCM, CCM, GMAC, CMAC, AES Key Wrap, XTS<br/> **Windows 8 :** La prise en charge des modes CFB128 et CMAC démarre.<br/> **Windows 10 :** La prise en charge du mode XTS-AES démarre.<br/> | 128/192/256                        |
| Data Encryption Standard (DES)         | BCE, CBC, CFB8, CFB64<br/> **Windows 8 :** La prise en charge du mode CFB64 commence.<br/>                                                                                                                   | 56/56/56                           |
| DESX (Data Encryption Standard XOR)   | BCE, CBC, CFB8, CFB64 <br/> **Windows 8 :** La prise en charge du mode CFB64 commence.<br/>                                                                                                                  | 192/192/192                        |
| 3DES (Triple Data Encryption Standard) | BCE, CBC, CFB8, CFB64 <br/> **Windows 8 :** La prise en charge du mode CFB64 commence.<br/>                                                                                                                  | 112/168                            |
| RSA Data Security 2 (RC2)              | Les modes ECB, CBC, CFB8 et CFB64 sont pris en charge.<br/> **Windows 8 :** La prise en charge du mode CFB64 commence.<br/>                                                                                              | de 16 à 128 par incréments de 8 bits      |
| RSA Data Security 4 (RC4)              |                                                                                                                                                                                                                 | 8 à 512, par incréments de 8 bits      |



 

## <a name="asymmetric-algorithms"></a>Algorithmes asymétriques



| Nom                              | Notes                                                                                                                                                                             | Taille de la clé en bits (valeur par défaut/min/max)                                                                            |
|-----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Algorithme de signature numérique (DSA) | L’implémentation est conforme à la norme FIPS 186-3 pour les tailles de clé comprises entre 1024 et 3072 bits. <br/> L’implémentation est conforme à la norme FIPS 186-2 pour les tailles de clé de 512 à 1024 bits.<br/> | 512 à 3072, en incréments de 64 bits<br/> **Windows 8 :** La prise en charge de la clé a 3072 bits commence.<br/> |
| RSA                               | Comprend des algorithmes RSA qui utilisent PKCS1, l’encodage ou le remplissage OAEP (Optimal Asymmetric Encryption Padding) ou le remplissage en texte clair du schéma de signature probabiliste (PSS).               | 512 à 16384, en incréments de 64 bits                                                                            |



 

## <a name="hashing-algorithms"></a>Algorithmes de hachage



| Nom                               | Notes               | Taille de la clé en bits (valeur par défaut/min/max) |
|------------------------------------|---------------------|------------------------------------|
| Secure Hash Algorithm 1 (SHA1)     | Comprend HmacSha1   | 160/160/160                        |
| Algorithme de hachage sécurisé 256 (SHA256) | Comprend HmacSha256 | 256/256/256                        |
| Algorithme de hachage sécurisé 384 (SHA384) | Comprend HmacSha384 | 384/384/384                        |
| Algorithme de hachage sécurisé 512 (SHA512) | Comprend HmacSha512 | 512/512/512                        |
| Message condensé 2 (MD2)             | Comprend HmacMd2    | 128/128/128                        |
| Message condensé 4 (MD4)             | Comprend HmacMd4    | 128/128/128                        |
| Message Digest 5 (MD5)             | Comprend HmacMd5    | 128/128/128                        |



 

## <a name="key-exchange-algorithms"></a>Algorithmes d’échange de clés



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Nom de l'algorithme</th>
<th>Notes</th>
<th>Taille de la clé en bits (valeur par défaut/min/max)</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Algorithme d’échange de clés Diffie-Hellman</td>

<td>512 à 4096, en incréments de 64 bits</td>
</tr>
<tr class="even">
<td>ECDH (Elliptic Curve Diffie-Hellman)</td>
<td>Comprend des courbes qui utilisent des clés publiques 256, 384 et 521 bits comme spécifié dans SP800-56A.</td>
<td>256/384/521</td>
</tr>
<tr class="odd">
<td>Algorithme ECDSA (Elliptic Curve Digital Signature Algorithm)</td>
<td>Comprend des courbes qui utilisent des clés publiques 256, 384 et 521 bits comme spécifié dans la norme FIPS 186-3.
<blockquote>
[!Note]<br />
Pour afficher toutes les courbes elliptiques nommées, utilisez <strong>certutil displayEccCurve</strong>.
</blockquote>
<br/></td>
<td>256/384/521</td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Identificateurs d’algorithme CNG**](/windows/desktop/SecCNG/cng-algorithm-identifiers)
</dt> <dt>

[Fonctions de primitives de chiffrement CNG](/windows/desktop/SecCNG/cng-cryptographic-primitive-functions)
</dt> <dt>

[Comprendre les fournisseurs de services de chiffrement](understanding-cryptographic-providers.md)
</dt> </dl>

 

