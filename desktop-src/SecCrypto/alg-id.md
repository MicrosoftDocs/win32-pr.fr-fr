---
description: Spécifie un identificateur d’algorithme.
ms.assetid: 557436b4-f7f1-4708-acc7-c6b47e6322ad
title: ALG_ID (Wincrypt. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ab1eb6dc262faae76d38f2b96c9e6191a313390
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106538724"
---
# <a name="alg_id"></a>ALG_ID

Le type de données **ALG_ID** spécifie un identificateur d’algorithme. Les paramètres de ce type de données sont passés à la plupart des fonctions dans CryptoAPI.


```C++
typedef unsigned int ALG_ID;
```



Le tableau suivant répertorie les identificateurs d’algorithme actuellement définis. Les auteurs des [*fournisseurs de services de chiffrement*](../secgloss/c-gly.md) (CSP) personnalisés peuvent définir de nouvelles valeurs. En outre, les **ALG_ID** utilisés par des fournisseurs de services de chiffrement personnalisés pour les spécifications de clé **AT_KEYEXCHANGE** et **AT_SIGNATURE** dépendent du fournisseur. Les mappages actuels suivent le tableau.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Identificateur</th>
<th>Valeur</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>CALG_3DES</td>
<td>0x00006603</td>
<td>Algorithme de chiffrement <a href="/windows/desktop/SecGloss/t-gly"><em>triple des</em></a> .</td>
</tr>
<tr class="even">
<td>CALG_3DES_112</td>
<td>0x00006609</td>
<td>Chiffrement <a href="/windows/desktop/SecGloss/t-gly"><em>triple des</em></a> à deux clés avec une longueur de clé effective égale à 112 bits.</td>
</tr>
<tr class="odd">
<td>CALG_AES</td>
<td>0x00006611</td>
<td>Advanced Encryption Standard (AES). Cet algorithme est pris en charge par le <a href="microsoft-aes-cryptographic-provider.md">fournisseur de services de chiffrement AES Microsoft</a>.</td>
</tr>
<tr class="even">
<td>CALG_AES_128</td>
<td>0x0000660e</td>
<td>AES 128 bits. Cet algorithme est pris en charge par le <a href="microsoft-aes-cryptographic-provider.md">fournisseur de services de chiffrement AES Microsoft</a>.</td>
</tr>
<tr class="odd">
<td>CALG_AES_192</td>
<td>0x0000660f</td>
<td>AES 192 bits. Cet algorithme est pris en charge par le <a href="microsoft-aes-cryptographic-provider.md">fournisseur de services de chiffrement AES Microsoft</a>.</td>
</tr>
<tr class="even">
<td>CALG_AES_256</td>
<td>0x00006610</td>
<td>AES 256 bits. Cet algorithme est pris en charge par le <a href="microsoft-aes-cryptographic-provider.md">fournisseur de services de chiffrement AES Microsoft</a>.</td>
</tr>
<tr class="odd">
<td>CALG_AGREEDKEY_ANY</td>
<td>0x0000aa03</td>
<td>Identificateur d’algorithme temporaire pour les handles de Diffie-Hellman : clés convenues.</td>
</tr>
<tr class="even">
<td>CALG_CYLINK_MEK</td>
<td>0x0000660c</td>
<td>Algorithme permettant de créer une clé de 40 bits avec DES bits de parité et des bits de clé mis à zéro pour faire de la longueur de clé 64 bits. Cet algorithme est pris en charge par le <a href=""></a> <a href="microsoft-base-cryptographic-provider.md">fournisseur de services de chiffrement de base Microsoft</a>.</td>
</tr>
<tr class="odd">
<td>CALG_DES</td>
<td>0x00006601</td>
<td>Algorithme de chiffrement DES.</td>
</tr>
<tr class="even">
<td>CALG_DESX</td>
<td>0x00006604</td>
<td>Algorithme de chiffrement DESX.</td>
</tr>
<tr class="odd">
<td>CALG_DH_EPHEM</td>
<td>0x0000aa02</td>
<td>Diffie-Hellman algorithme d’échange de clés éphémères.</td>
</tr>
<tr class="even">
<td>CALG_DH_SF</td>
<td>0x0000aa01</td>
<td>Diffie-Hellman l’algorithme d’échange de clés de stockage et de transfert.</td>
</tr>
<tr class="odd">
<td>CALG_DSS_SIGN</td>
<td>0x00002200</td>
<td>Algorithme de signature de <a href="/windows/desktop/SecGloss/p-gly"><em>clé publique</em></a> DSA.</td>
</tr>
<tr class="even">
<td>CALG_ECDH</td>
<td>0x0000aa05</td>
<td>Algorithme d’échange de clés Diffie-Hellman à courbe elliptique.
<blockquote>
[!Note]<br />
Cet algorithme est pris en charge uniquement par le biais de l' <a href="/windows/desktop/SecCNG/cng-portal">API de chiffrement : Next Generation</a>.
</blockquote>
<br/> <strong>Windows Server 2003 et Windows XP :</strong> Cet algorithme n’est pas pris en charge.<br/></td>
</tr>
<tr class="odd">
<td>CALG_ECDH_EPHEM</td>
<td>0x0000ae06</td>
<td>Algorithme d’échange de clés Diffie-Hellman à courbe elliptique éphémère.
<blockquote>
[!Note]<br />
Cet algorithme est pris en charge uniquement par le biais de l' <a href="/windows/desktop/SecCNG/cng-portal">API de chiffrement : Next Generation</a>.
</blockquote>
<br/> <strong>Windows Server 2003 et Windows XP :</strong> Cet algorithme n’est pas pris en charge.<br/></td>
</tr>
<tr class="even">
<td>CALG_ECDSA</td>
<td>0x00002203</td>
<td>Algorithme de signature numérique à courbe elliptique.
<blockquote>
[!Note]<br />
Cet algorithme est pris en charge uniquement par le biais de l' <a href="/windows/desktop/SecCNG/cng-portal">API de chiffrement : Next Generation</a>.
</blockquote>
<br/> <strong>Windows Server 2003 et Windows XP :</strong> Cet algorithme n’est pas pris en charge.<br/></td>
</tr>
<tr class="odd">
<td>CALG_ECMQV</td>
<td>0x0000a001</td>
<td>Algorithme d’échange de clés elliptique Curve Menezes, qu et Vanstone (MQV). Cet algorithme n’est pas pris en charge.</td>
</tr>
<tr class="even">
<td>CALG_HASH_REPLACE_OWF</td>
<td>0x0000800b</td>
<td>Algorithme de hachage de fonction unidirectionnel.</td>
</tr>
<tr class="odd">
<td>CALG_HUGHES_MD5</td>
<td>0x0000a003</td>
<td>Algorithme de hachage MD5 Hughes.</td>
</tr>
<tr class="even">
<td>CALG_HMAC</td>
<td>0x00008009</td>
<td>Algorithme de hachage à clé HMAC. Cet algorithme est pris en charge par le <a href="microsoft-base-cryptographic-provider.md">fournisseur de services de chiffrement de base Microsoft</a>.</td>
</tr>
<tr class="odd">
<td>CALG_KEA_KEYX</td>
<td>0x0000aa04</td>
<td>Algorithme d’échange de clés KEA (FORTEZZA). Cet algorithme n’est pas pris en charge.</td>
</tr>
<tr class="even">
<td>CALG_MAC</td>
<td>0x00008005</td>
<td>Algorithme de hachage à clé <a href="/windows/desktop/SecGloss/m-gly"><em>Mac</em></a> . Cet algorithme est pris en charge par le <a href="microsoft-base-cryptographic-provider.md">fournisseur de services de chiffrement de base Microsoft</a>.</td>
</tr>
<tr class="odd">
<td>CALG_MD2</td>
<td>0x00008001</td>
<td>Algorithme de hachage MD2. Cet algorithme est pris en charge par le <a href="microsoft-base-cryptographic-provider.md">fournisseur de services de chiffrement de base Microsoft</a>.</td>
</tr>
<tr class="even">
<td>CALG_MD4</td>
<td>0x00008002</td>
<td>Algorithme de hachage MD4.</td>
</tr>
<tr class="odd">
<td>CALG_MD5</td>
<td>0x00008003</td>
<td>Algorithme de hachage MD5. Cet algorithme est pris en charge par le <a href="microsoft-base-cryptographic-provider.md">fournisseur de services de chiffrement de base Microsoft</a>.</td>
</tr>
<tr class="even">
<td>CALG_NO_SIGN</td>
<td>0x00002000</td>
<td>Pas d’algorithme de signature.</td>
</tr>
<tr class="odd">
<td>CALG_OID_INFO_CNG_ONLY</td>
<td>égale</td>
<td>L’algorithme est uniquement implémenté dans CNG. La macro, IS_SPECIAL_OID_INFO_ALGID, peut être utilisée pour déterminer si un algorithme de chiffrement est pris en charge uniquement à l’aide des fonctions CNG.</td>
</tr>
<tr class="even">
<td>CALG_OID_INFO_PARAMETERS</td>
<td>0xfffffffe</td>
<td>L’algorithme est défini dans les paramètres encodés. L’algorithme est pris en charge uniquement à l’aide de CNG. La macro, IS_SPECIAL_OID_INFO_ALGID, peut être utilisée pour déterminer si un algorithme de chiffrement est pris en charge uniquement à l’aide des fonctions CNG.</td>
</tr>
<tr class="odd">
<td>CALG_PCT1_MASTER</td>
<td>0x00004c04</td>
<td>Utilisé par le système d’exploitation Schannel.dll. Cette <strong>ALG_ID</strong> ne doit pas être utilisée par les applications.</td>
</tr>
<tr class="even">
<td>CALG_RC2</td>
<td>0x00006602</td>
<td>Algorithme de chiffrement par bloc RC2. Cet algorithme est pris en charge par le <a href="microsoft-base-cryptographic-provider.md">fournisseur de services de chiffrement de base Microsoft</a>.</td>
</tr>
<tr class="odd">
<td>CALG_RC4</td>
<td>0x00006801</td>
<td>Algorithme de chiffrement de flux RC4. Cet algorithme est pris en charge par le <a href="microsoft-base-cryptographic-provider.md">fournisseur de services de chiffrement de base Microsoft</a>.</td>
</tr>
<tr class="even">
<td>CALG_RC5</td>
<td>0x0000660d</td>
<td>Algorithme de chiffrement par bloc RC5.</td>
</tr>
<tr class="odd">
<td>CALG_RSA_KEYX</td>
<td>0x0000a400</td>
<td>Algorithme d’échange de clés publiques RSA. Cet algorithme est pris en charge par le <a href="microsoft-base-cryptographic-provider.md">fournisseur de services de chiffrement de base Microsoft</a>.</td>
</tr>
<tr class="even">
<td>CALG_RSA_SIGN</td>
<td>0x00002400</td>
<td>Algorithme de signature de clé publique RSA. Cet algorithme est pris en charge par le <a href="microsoft-base-cryptographic-provider.md">fournisseur de services de chiffrement de base Microsoft</a>.</td>
</tr>
<tr class="odd">
<td>CALG_SCHANNEL_ENC_KEY</td>
<td>0x00004c07</td>
<td>Utilisé par le système d’exploitation Schannel.dll. Cette <strong>ALG_ID</strong> ne doit pas être utilisée par les applications.</td>
</tr>
<tr class="even">
<td>CALG_SCHANNEL_MAC_KEY</td>
<td>0x00004c03</td>
<td>Utilisé par le système d’exploitation Schannel.dll. Cette <strong>ALG_ID</strong> ne doit pas être utilisée par les applications.</td>
</tr>
<tr class="odd">
<td>CALG_SCHANNEL_MASTER_HASH</td>
<td>0x00004c02</td>
<td>Utilisé par le système d’exploitation Schannel.dll. Cette <strong>ALG_ID</strong> ne doit pas être utilisée par les applications.</td>
</tr>
<tr class="even">
<td>CALG_SEAL</td>
<td>0x00006802</td>
<td>SCELLe l’algorithme de chiffrement. Cet algorithme n’est pas pris en charge.</td>
</tr>
<tr class="odd">
<td>CALG_SHA</td>
<td>0x00008004</td>
<td>Algorithme de hachage SHA. Cet algorithme est pris en charge par le <a href="microsoft-base-cryptographic-provider.md">fournisseur de services de chiffrement de base Microsoft</a>.</td>
</tr>
<tr class="even">
<td>CALG_SHA1</td>
<td>0x00008004</td>
<td>Identique à <strong>CALG_SHA</strong>. Cet algorithme est pris en charge par le <a href="microsoft-base-cryptographic-provider.md">fournisseur de services de chiffrement de base Microsoft</a>.</td>
</tr>
<tr class="odd">
<td>CALG_SHA_256</td>
<td>0x0000800c</td>
<td>algorithme de hachage SHA de 256 bits. Cet algorithme est pris en charge par Microsoft Enhanced RSA et le fournisseur de services de chiffrement AES. <strong>Windows XP avec SP3 :</strong> Cet algorithme est pris en charge par le fournisseur de services de chiffrement RSA et AES Microsoft amélioré (prototype).<br/> <strong>Windows XP avec SP2, Windows XP avec SP1 et Windows XP :</strong> Cet algorithme n’est pas pris en charge.<br/></td>
</tr>
<tr class="even">
<td>CALG_SHA_384</td>
<td>0x0000800d</td>
<td>algorithme de hachage SHA de 384 bits. Cet algorithme est pris en charge par Microsoft Enhanced RSA et le fournisseur de services de chiffrement AES. <strong>Windows XP avec SP3 :</strong> Cet algorithme est pris en charge par le fournisseur de services de chiffrement RSA et AES Microsoft amélioré (prototype).<br/> <strong>Windows XP avec SP2, Windows XP avec SP1 et Windows XP :</strong> Cet algorithme n’est pas pris en charge.<br/></td>
</tr>
<tr class="odd">
<td>CALG_SHA_512</td>
<td>0x0000800e</td>
<td>algorithme de hachage SHA de 512 bits. Cet algorithme est pris en charge par Microsoft Enhanced RSA et le fournisseur de services de chiffrement AES. <strong>Windows XP avec SP3 :</strong> Cet algorithme est pris en charge par le fournisseur de services de chiffrement RSA et AES Microsoft amélioré (prototype).<br/> <strong>Windows XP avec SP2, Windows XP avec SP1 et Windows XP :</strong> Cet algorithme n’est pas pris en charge.<br/></td>
</tr>
<tr class="even">
<td>CALG_SKIPJACK</td>
<td>0x0000660a</td>
<td>Algorithme de chiffrement par bloc Skipjack (FORTEZZA). Cet algorithme n’est pas pris en charge.</td>
</tr>
<tr class="odd">
<td>CALG_SSL2_MASTER</td>
<td>0x00004c05</td>
<td>Utilisé par le système d’exploitation Schannel.dll. Cette <strong>ALG_ID</strong> ne doit pas être utilisée par les applications.</td>
</tr>
<tr class="even">
<td>CALG_SSL3_MASTER</td>
<td>0x00004c01</td>
<td>Utilisé par le système d’exploitation Schannel.dll. Cette <strong>ALG_ID</strong> ne doit pas être utilisée par les applications.</td>
</tr>
<tr class="odd">
<td>CALG_SSL3_SHAMD5</td>
<td>0x00008008</td>
<td>Utilisé par le système d’exploitation Schannel.dll. Cette <strong>ALG_ID</strong> ne doit pas être utilisée par les applications.</td>
</tr>
<tr class="even">
<td>CALG_TEK</td>
<td>0x0000660b</td>
<td>TEK (FORTEZZA). Cet algorithme n’est pas pris en charge.</td>
</tr>
<tr class="odd">
<td>CALG_TLS1_MASTER</td>
<td>0x00004c06</td>
<td>Utilisé par le système d’exploitation Schannel.dll. Cette <strong>ALG_ID</strong> ne doit pas être utilisée par les applications.</td>
</tr>
<tr class="even">
<td>CALG_TLS1PRF</td>
<td>0x0000800a</td>
<td>Utilisé par le système d’exploitation Schannel.dll. Cette <strong>ALG_ID</strong> ne doit pas être utilisée par les applications.</td>
</tr>
</tbody>
</table>



 

Pour le [fournisseur de services de chiffrement de base Microsoft](microsoft-base-cryptographic-provider.md), le fournisseur de services de chiffrement [renforcé](microsoft-strong-cryptographic-provider.md)Microsoft et le [fournisseur de services de chiffrement amélioré Microsoft](microsoft-enhanced-cryptographic-provider.md), les **ALG_IDs** utilisés pour les spécifications de clé **AT_KEYEXCHANGE** et **AT_SIGNATURE** sont les suivantes :

-   **CALG_RSA_KEYX** est utilisé pour les **AT_KEYEXCHANGE**.
-   **CALG_RSA_SIGN** est utilisé pour les **AT_SIGNATURE**.

Pour les [fournisseurs de services de chiffrement DSS et Diffie-Hellman de base Microsoft](microsoft-base-dss-and-diffie-hellman-cryptographic-provider.md), les **ALG_IDs** utilisés pour les spécifications de clé **AT_KEYEXCHANGE** et **AT_SIGNATURE** sont les suivantes :

-   **CALG_DH_SF** est utilisé pour les **AT_KEYEXCHANGE**.
-   **CALG_DSS_SIGN** est utilisé pour les **AT_SIGNATURE**.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows XP uniquement\]<br/>                                           |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Wincrypt. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions de chiffrement](cryptography-functions.md)
</dt> <dt>

[**CRYPT_ALGORITHM_IDENTIFIER**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_algorithm_identifier)
</dt> <dt>

[**CryptFindOIDInfo**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptfindoidinfo)
</dt> </dl>

 

 
