---
description: Spécifie un identificateur d’algorithme.
ms.assetid: 557436b4-f7f1-4708-acc7-c6b47e6322ad
title: ALG_ID (Wincrypt. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 82f4b6c476a8ea6e61785a096abf33c357d9b024
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122482395"
---
# <a name="alg_id"></a>ALG_ID

Le type de données **ALG_ID** spécifie un identificateur d’algorithme. Les paramètres de ce type de données sont passés à la plupart des fonctions dans CryptoAPI.


```C++
typedef unsigned int ALG_ID;
```



Le tableau suivant répertorie les identificateurs d’algorithme actuellement définis. Les auteurs des [*fournisseurs de services de chiffrement*](../secgloss/c-gly.md) (CSP) personnalisés peuvent définir de nouvelles valeurs. En outre, les **ALG_ID** utilisés par des fournisseurs de services de chiffrement personnalisés pour les spécifications de clé **AT_KEYEXCHANGE** et **AT_SIGNATURE** dépendent du fournisseur. Les mappages actuels suivent le tableau.




| Identificateur | Valeur | Description | 
|------------|-------|-------------|
| CALG_3DES | 0x00006603 | Algorithme de chiffrement <a href="/windows/desktop/SecGloss/t-gly"><em>triple des</em></a> . | 
| CALG_3DES_112 | 0x00006609 | Chiffrement <a href="/windows/desktop/SecGloss/t-gly"><em>triple des</em></a> à deux clés avec une longueur de clé effective égale à 112 bits. | 
| CALG_AES | 0x00006611 | Advanced Encryption Standard (AES). Cet algorithme est pris en charge par le <a href="microsoft-aes-cryptographic-provider.md">fournisseur de services de chiffrement AES Microsoft</a>. | 
| CALG_AES_128 | 0x0000660e | AES 128 bits. Cet algorithme est pris en charge par le <a href="microsoft-aes-cryptographic-provider.md">fournisseur de services de chiffrement AES Microsoft</a>. | 
| CALG_AES_192 | 0x0000660f | AES 192 bits. Cet algorithme est pris en charge par le <a href="microsoft-aes-cryptographic-provider.md">fournisseur de services de chiffrement AES Microsoft</a>. | 
| CALG_AES_256 | 0x00006610 | AES 256 bits. Cet algorithme est pris en charge par le <a href="microsoft-aes-cryptographic-provider.md">fournisseur de services de chiffrement AES Microsoft</a>. | 
| CALG_AGREEDKEY_ANY | 0x0000aa03 | Identificateur d’algorithme temporaire pour les handles de Diffie-Hellman : clés convenues. | 
| CALG_CYLINK_MEK | 0x0000660c | Algorithme permettant de créer une clé de 40 bits avec DES bits de parité et des bits de clé mis à zéro pour faire de la longueur de clé 64 bits. Cet algorithme est pris en charge par le <a href=""></a> <a href="microsoft-base-cryptographic-provider.md">fournisseur de services de chiffrement de base Microsoft</a>. | 
| CALG_DES | 0x00006601 | Algorithme de chiffrement DES. | 
| CALG_DESX | 0x00006604 | Algorithme de chiffrement DESX. | 
| CALG_DH_EPHEM | 0x0000aa02 | Diffie-Hellman algorithme d’échange de clés éphémères. | 
| CALG_DH_SF | 0x0000aa01 | Diffie-Hellman l’algorithme d’échange de clés de stockage et de transfert. | 
| CALG_DSS_SIGN | 0x00002200 | Algorithme de signature de <a href="/windows/desktop/SecGloss/p-gly"><em>clé publique</em></a> DSA. | 
| CALG_ECDH | 0x0000aa05 | Algorithme d’échange de clés Diffie-Hellman à courbe elliptique.<blockquote>[!Note]<br />Cet algorithme est pris en charge uniquement par le biais de l' <a href="/windows/desktop/SecCNG/cng-portal">API de chiffrement : Next Generation</a>.</blockquote><br /><strong>Windows Server 2003 et Windows XP :</strong> Cet algorithme n’est pas pris en charge.<br /> | 
| CALG_ECDH_EPHEM | 0x0000ae06 | Algorithme d’échange de clés Diffie-Hellman à courbe elliptique éphémère.<blockquote>[!Note]<br />Cet algorithme est pris en charge uniquement par le biais de l' <a href="/windows/desktop/SecCNG/cng-portal">API de chiffrement : Next Generation</a>.</blockquote><br /><strong>Windows Server 2003 et Windows XP :</strong> Cet algorithme n’est pas pris en charge.<br /> | 
| CALG_ECDSA | 0x00002203 | Algorithme de signature numérique à courbe elliptique.<blockquote>[!Note]<br />Cet algorithme est pris en charge uniquement par le biais de l' <a href="/windows/desktop/SecCNG/cng-portal">API de chiffrement : Next Generation</a>.</blockquote><br /><strong>Windows Server 2003 et Windows XP :</strong> Cet algorithme n’est pas pris en charge.<br /> | 
| CALG_ECMQV | 0x0000a001 | Algorithme d’échange de clés elliptique Curve Menezes, qu et Vanstone (MQV). Cet algorithme n’est pas pris en charge. | 
| CALG_HASH_REPLACE_OWF | 0x0000800b | Algorithme de hachage de fonction unidirectionnel. | 
| CALG_HUGHES_MD5 | 0x0000a003 | Algorithme de hachage MD5 Hughes. | 
| CALG_HMAC | 0x00008009 | Algorithme de hachage à clé HMAC. Cet algorithme est pris en charge par le <a href="microsoft-base-cryptographic-provider.md">fournisseur de services de chiffrement de base Microsoft</a>. | 
| CALG_KEA_KEYX | 0x0000aa04 | Algorithme d’échange de clés KEA (FORTEZZA). Cet algorithme n’est pas pris en charge. | 
| CALG_MAC | 0x00008005 | Algorithme de hachage à clé <a href="/windows/desktop/SecGloss/m-gly"><em>Mac</em></a> . Cet algorithme est pris en charge par le <a href="microsoft-base-cryptographic-provider.md">fournisseur de services de chiffrement de base Microsoft</a>. | 
| CALG_MD2 | 0x00008001 | Algorithme de hachage MD2. Cet algorithme est pris en charge par le <a href="microsoft-base-cryptographic-provider.md">fournisseur de services de chiffrement de base Microsoft</a>. | 
| CALG_MD4 | 0x00008002 | Algorithme de hachage MD4. | 
| CALG_MD5 | 0x00008003 | Algorithme de hachage MD5. Cet algorithme est pris en charge par le <a href="microsoft-base-cryptographic-provider.md">fournisseur de services de chiffrement de base Microsoft</a>. | 
| CALG_NO_SIGN | 0x00002000 | Pas d’algorithme de signature. | 
| CALG_OID_INFO_CNG_ONLY | 0xffffffff | L’algorithme est uniquement implémenté dans CNG. La macro, IS_SPECIAL_OID_INFO_ALGID, peut être utilisée pour déterminer si un algorithme de chiffrement est pris en charge uniquement à l’aide des fonctions CNG. | 
| CALG_OID_INFO_PARAMETERS | 0xfffffffe | L’algorithme est défini dans les paramètres encodés. L’algorithme est pris en charge uniquement à l’aide de CNG. La macro, IS_SPECIAL_OID_INFO_ALGID, peut être utilisée pour déterminer si un algorithme de chiffrement est pris en charge uniquement à l’aide des fonctions CNG. | 
| CALG_PCT1_MASTER | 0x00004c04 | Utilisé par le système d’exploitation Schannel.dll. Cette <strong>ALG_ID</strong> ne doit pas être utilisée par les applications. | 
| CALG_RC2 | 0x00006602 | Algorithme de chiffrement par bloc RC2. Cet algorithme est pris en charge par le <a href="microsoft-base-cryptographic-provider.md">fournisseur de services de chiffrement de base Microsoft</a>. | 
| CALG_RC4 | 0x00006801 | Algorithme de chiffrement de flux RC4. Cet algorithme est pris en charge par le <a href="microsoft-base-cryptographic-provider.md">fournisseur de services de chiffrement de base Microsoft</a>. | 
| CALG_RC5 | 0x0000660d | Algorithme de chiffrement par bloc RC5. | 
| CALG_RSA_KEYX | 0x0000a400 | Algorithme d’échange de clés publiques RSA. Cet algorithme est pris en charge par le <a href="microsoft-base-cryptographic-provider.md">fournisseur de services de chiffrement de base Microsoft</a>. | 
| CALG_RSA_SIGN | 0x00002400 | Algorithme de signature de clé publique RSA. Cet algorithme est pris en charge par le <a href="microsoft-base-cryptographic-provider.md">fournisseur de services de chiffrement de base Microsoft</a>. | 
| CALG_SCHANNEL_ENC_KEY | 0x00004c07 | Utilisé par le système d’exploitation Schannel.dll. Cette <strong>ALG_ID</strong> ne doit pas être utilisée par les applications. | 
| CALG_SCHANNEL_MAC_KEY | 0x00004c03 | Utilisé par le système d’exploitation Schannel.dll. Cette <strong>ALG_ID</strong> ne doit pas être utilisée par les applications. | 
| CALG_SCHANNEL_MASTER_HASH | 0x00004c02 | Utilisé par le système d’exploitation Schannel.dll. Cette <strong>ALG_ID</strong> ne doit pas être utilisée par les applications. | 
| CALG_SEAL | 0x00006802 | SCELLe l’algorithme de chiffrement. Cet algorithme n’est pas pris en charge. | 
| CALG_SHA | 0x00008004 | Algorithme de hachage SHA. Cet algorithme est pris en charge par le <a href="microsoft-base-cryptographic-provider.md">fournisseur de services de chiffrement de base Microsoft</a>. | 
| CALG_SHA1 | 0x00008004 | Identique à <strong>CALG_SHA</strong>. Cet algorithme est pris en charge par le <a href="microsoft-base-cryptographic-provider.md">fournisseur de services de chiffrement de base Microsoft</a>. | 
| CALG_SHA_256 | 0x0000800c | algorithme de hachage SHA de 256 bits. Cet algorithme est pris en charge par Microsoft Enhanced RSA et le fournisseur de services de chiffrement AES. <strong>Windows XP avec SP3 :</strong> Cet algorithme est pris en charge par le fournisseur de services de chiffrement RSA et AES Microsoft amélioré (prototype).<br /><strong>Windows xp avec SP2, Windows xp avec SP1 et Windows xp :</strong> Cet algorithme n’est pas pris en charge.<br /> | 
| CALG_SHA_384 | 0x0000800d | algorithme de hachage SHA de 384 bits. Cet algorithme est pris en charge par Microsoft Enhanced RSA et le fournisseur de services de chiffrement AES. <strong>Windows XP avec SP3 :</strong> Cet algorithme est pris en charge par le fournisseur de services de chiffrement RSA et AES Microsoft amélioré (prototype).<br /><strong>Windows xp avec SP2, Windows xp avec SP1 et Windows xp :</strong> Cet algorithme n’est pas pris en charge.<br /> | 
| CALG_SHA_512 | 0x0000800e | algorithme de hachage SHA de 512 bits. Cet algorithme est pris en charge par Microsoft Enhanced RSA et le fournisseur de services de chiffrement AES. <strong>Windows XP avec SP3 :</strong> Cet algorithme est pris en charge par le fournisseur de services de chiffrement RSA et AES Microsoft amélioré (prototype).<br /><strong>Windows xp avec SP2, Windows xp avec SP1 et Windows xp :</strong> Cet algorithme n’est pas pris en charge.<br /> | 
| CALG_SKIPJACK | 0x0000660a | Algorithme de chiffrement par bloc Skipjack (FORTEZZA). Cet algorithme n’est pas pris en charge. | 
| CALG_SSL2_MASTER | 0x00004c05 | Utilisé par le système d’exploitation Schannel.dll. Cette <strong>ALG_ID</strong> ne doit pas être utilisée par les applications. | 
| CALG_SSL3_MASTER | 0x00004c01 | Utilisé par le système d’exploitation Schannel.dll. Cette <strong>ALG_ID</strong> ne doit pas être utilisée par les applications. | 
| CALG_SSL3_SHAMD5 | 0x00008008 | Utilisé par le système d’exploitation Schannel.dll. Cette <strong>ALG_ID</strong> ne doit pas être utilisée par les applications. | 
| CALG_TEK | 0x0000660b | TEK (FORTEZZA). Cet algorithme n’est pas pris en charge. | 
| CALG_TLS1_MASTER | 0x00004c06 | Utilisé par le système d’exploitation Schannel.dll. Cette <strong>ALG_ID</strong> ne doit pas être utilisée par les applications. | 
| CALG_TLS1PRF | 0x0000800a | Utilisé par le système d’exploitation Schannel.dll. Cette <strong>ALG_ID</strong> ne doit pas être utilisée par les applications. | 




 

Pour le [fournisseur de services de chiffrement de base Microsoft](microsoft-base-cryptographic-provider.md), le fournisseur de services de chiffrement [renforcé](microsoft-strong-cryptographic-provider.md)Microsoft et le [fournisseur de services de chiffrement amélioré Microsoft](microsoft-enhanced-cryptographic-provider.md), les **ALG_IDs** utilisés pour les spécifications de clé **AT_KEYEXCHANGE** et **AT_SIGNATURE** sont les suivantes :

-   **CALG_RSA_KEYX** est utilisé pour les **AT_KEYEXCHANGE**.
-   **CALG_RSA_SIGN** est utilisé pour les **AT_SIGNATURE**.

Pour les [fournisseurs de services de chiffrement DSS et Diffie-Hellman de base Microsoft](microsoft-base-dss-and-diffie-hellman-cryptographic-provider.md), les **ALG_IDs** utilisés pour les spécifications de clé **AT_KEYEXCHANGE** et **AT_SIGNATURE** sont les suivantes :

-   **CALG_DH_SF** est utilisé pour les **AT_KEYEXCHANGE**.
-   **CALG_DSS_SIGN** est utilisé pour les **AT_SIGNATURE**.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>                                           |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Wincrypt. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions de chiffrement](cryptography-functions.md)
</dt> <dt>

[**CRYPT_ALGORITHM_IDENTIFIER**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_algorithm_identifier)
</dt> <dt>

[**CryptFindOIDInfo**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptfindoidinfo)
</dt> </dl>

 

 
