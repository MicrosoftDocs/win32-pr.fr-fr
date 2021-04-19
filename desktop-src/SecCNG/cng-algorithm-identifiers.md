---
description: Utilisé pour identifier les algorithmes de chiffrement standard dans différentes structures et fonctions CNG, telles que la structure de chiffrement de l' \_ interface \_ reg.
ms.assetid: a05ae7e6-d882-4287-9990-23e4cd340b05
title: Identificateurs d’algorithme CNG (bcrypt. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba244f2a815933322793fdd572ed7a4e69256a0a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514376"
---
# <a name="cng-algorithm-identifiers"></a>Identificateurs d’algorithme CNG

Les identificateurs suivants sont utilisés pour identifier des algorithmes de chiffrement standard dans diverses structures et fonctions CNG, telles que la structure de chiffrement de l' [**\_ interface \_ reg**](/windows/desktop/api/Bcrypt/ns-bcrypt-crypt_interface_reg) . Les fournisseurs tiers peuvent avoir des algorithmes supplémentaires qu’ils prennent en charge.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Constante/valeur</th>
<th style="text-align: left;">Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="BCRYPT_3DES_ALGORITHM"></span><span id="bcrypt_3des_algorithm"></span><dl> <dt><strong>BCRYPT_3DES_ALGORITHM</strong></dt> <dt> &quot; 3DES &quot; </dt> </dl></td>
<td style="text-align: left;">Algorithme de chiffrement symétrique Triple Data Encryption Standard.<br/> Standard : SP800-67, SP800-38A<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="BCRYPT_3DES_112_ALGORITHM"></span><span id="bcrypt_3des_112_algorithm"></span><dl> <dt><strong>BCRYPT_3DES_112_ALGORITHM</strong></dt> <dt> &quot; 3DES_112 &quot; </dt> </dl></td>
<td style="text-align: left;">Algorithme de chiffrement symétrique standard Triple Data Encryption 112 bits.<br/> Standard : SP800-67, SP800-38A<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="BCRYPT_AES_ALGORITHM"></span><span id="bcrypt_aes_algorithm"></span><dl> <dt><strong>BCRYPT_AES_ALGORITHM</strong></dt> <dt> &quot; AES &quot; </dt> </dl></td>
<td style="text-align: left;">Algorithme de chiffrement symétrique standard de chiffrement avancé.<br/> Standard : FIPS 197<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="BCRYPT_AES_CMAC_ALGORITHM"></span><span id="bcrypt_aes_cmac_algorithm"></span><dl> <dt><strong>BCRYPT_AES_CMAC_ALGORITHM</strong></dt> <dt> &quot; AES-CMAC &quot; </dt> </dl></td>
<td style="text-align: left;">Algorithme de chiffrement symétrique CMAC (Advanced Encryption Standard) basé sur le chiffrement du code d’authentification de message (AES).<br/> Standard : SP 800-38B<br/> <strong>Windows 8 :</strong> La prise en charge de cet algorithme commence.<br/> <br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="BCRYPT_AES_GMAC_ALGORITHM"></span><span id="bcrypt_aes_gmac_algorithm"></span><dl> <dt><strong>BCRYPT_AES_GMAC_ALGORITHM</strong></dt> <dt> &quot; AES-GMAC &quot; </dt> </dl></td>
<td style="text-align: left;">Algorithme de chiffrement symétrique GMAC (Advanced Encryption Standard) Galois (Advanced Encryption code).<br/> Standard : SP800-38D<br/> <strong>Windows Vista :</strong> Cet algorithme est pris en charge à partir de Windows Vista avec SP1.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="BCRYPT_CAPI_KDF_ALGORITHM"></span><span id="bcrypt_capi_kdf_algorithm"></span><dl> <dt><strong>BCRYPT_CAPI_KDF_ALGORITHM</strong></dt> <dt>L &quot; CAPI_KDF &quot; </dt> </dl></td>
<td style="text-align: left;">Algorithme de la fonction de dérivation de clé de crypto API (CAPI). Utilisé par les fonctions <a href="/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptkeyderivation"><strong>BCryptKeyDerivation</strong></a> et <a href="/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptkeyderivation"><strong>NCryptKeyDerivation</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="BCRYPT_DES_ALGORITHM"></span><span id="bcrypt_des_algorithm"></span><dl> <dt><strong>BCRYPT_DES_ALGORITHM</strong></dt> <dt> &quot; des &quot; </dt> </dl></td>
<td style="text-align: left;">Algorithme de chiffrement symétrique standard de chiffrement de données.<br/> Standard : FIPS 46-3, FIPS 81<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="BCRYPT_DESX_ALGORITHM"></span><span id="bcrypt_desx_algorithm"></span><dl> <dt><strong>BCRYPT_DESX_ALGORITHM</strong></dt> <dt> &quot; DESX &quot; </dt> </dl></td>
<td style="text-align: left;">Algorithme de chiffrement symétrique standard de chiffrement de données étendu.<br/> Standard : aucun<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="BCRYPT_DH_ALGORITHM"></span><span id="bcrypt_dh_algorithm"></span><dl> <dt><strong>BCRYPT_DH_ALGORITHM</strong></dt> <dt> &quot; DH &quot; </dt> </dl></td>
<td style="text-align: left;">Algorithme d’échange de clés Diffie-Hellman.<br/> Standard : #3 PKCS<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="BCRYPT_DSA_ALGORITHM"></span><span id="bcrypt_dsa_algorithm"></span><dl> <dt><strong>BCRYPT_DSA_ALGORITHM</strong></dt> <dt> &quot; DSA &quot; </dt> </dl></td>
<td style="text-align: left;">Algorithme de signature numérique.<br/> Standard : FIPS 186-2<br/> <strong>Windows 8 :</strong> À partir de Windows 8, cet algorithme prend en charge FIPS 186-3. Les clés inférieures ou égales à 1024 bits adhèrent à FIPS 186-2 et les clés supérieures à 1024 à FIPS 186-3.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="BCRYPT_ECDH_P256_ALGORITHM"></span><span id="bcrypt_ecdh_p256_algorithm"></span><dl> <dt><strong>BCRYPT_ECDH_P256_ALGORITHM</strong></dt> <dt> &quot; ECDH_P256 &quot; </dt> </dl></td>
<td style="text-align: left;">Algorithme d’échange de clés Diffie-Hellman à courbe elliptique d’initiation 256 bits.<br/> Standard : SP800-56A<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="BCRYPT_ECDH_P384_ALGORITHM"></span><span id="bcrypt_ecdh_p384_algorithm"></span><dl> <dt><strong>BCRYPT_ECDH_P384_ALGORITHM</strong></dt> <dt> &quot; ECDH_P384 &quot; </dt> </dl></td>
<td style="text-align: left;">Algorithme d’échange de clés Diffie-Hellman à courbe elliptique d’initiation 384 bits.<br/> Standard : SP800-56A<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="BCRYPT_ECDH_P521_ALGORITHM"></span><span id="bcrypt_ecdh_p521_algorithm"></span><dl> <dt><strong>BCRYPT_ECDH_P521_ALGORITHM</strong></dt> <dt> &quot; ECDH_P521 &quot; </dt> </dl></td>
<td style="text-align: left;">Algorithme d’échange de clés Diffie-Hellman à courbe elliptique d’initiation 521 bits.<br/> Standard : SP800-56A<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="BCRYPT_ECDSA_P256_ALGORITHM"></span><span id="bcrypt_ecdsa_p256_algorithm"></span><dl> <dt><strong>BCRYPT_ECDSA_P256_ALGORITHM</strong></dt> <dt> &quot; ECDSA_P256 &quot; </dt> </dl></td>
<td style="text-align: left;">Algorithme de signature numérique à courbe elliptique (FIPS 186-2) 256 bits.<br/> Standard : FIPS 186-2, X 9.62<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="BCRYPT_ECDSA_P384_ALGORITHM"></span><span id="bcrypt_ecdsa_p384_algorithm"></span><dl> <dt><strong>BCRYPT_ECDSA_P384_ALGORITHM</strong></dt> <dt> &quot; ECDSA_P384 &quot; </dt> </dl></td>
<td style="text-align: left;">Algorithme de signature numérique à courbe elliptique (FIPS 186-2) 384 bits.<br/> Standard : FIPS 186-2, X 9.62<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="BCRYPT_ECDSA_P521_ALGORITHM"></span><span id="bcrypt_ecdsa_p521_algorithm"></span><dl> <dt><strong>BCRYPT_ECDSA_P521_ALGORITHM</strong></dt> <dt> &quot; ECDSA_P521 &quot; </dt> </dl></td>
<td style="text-align: left;">Algorithme de signature numérique à courbe elliptique (FIPS 186-2) 521 bits.<br/> Standard : FIPS 186-2, X 9.62<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="BCRYPT_MD2_ALGORITHM"></span><span id="bcrypt_md2_algorithm"></span><dl> <dt><strong>BCRYPT_MD2_ALGORITHM</strong></dt> <dt> &quot; MD2 &quot; </dt> </dl></td>
<td style="text-align: left;">Algorithme de hachage MD2.<br/> Standard : RFC 1319<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="BCRYPT_MD4_ALGORITHM"></span><span id="bcrypt_md4_algorithm"></span><dl> <dt><strong>BCRYPT_MD4_ALGORITHM</strong></dt> <dt> &quot; MD4 &quot; </dt> </dl></td>
<td style="text-align: left;">Algorithme de hachage MD4.<br/> Standard : RFC 1320<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="BCRYPT_MD5_ALGORITHM"></span><span id="bcrypt_md5_algorithm"></span><dl> <dt><strong>BCRYPT_MD5_ALGORITHM</strong></dt> <dt> &quot; MD5 &quot; </dt> </dl></td>
<td style="text-align: left;">Algorithme de hachage MD5.<br/> Standard : RFC 1321<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="BCRYPT_RC2_ALGORITHM"></span><span id="bcrypt_rc2_algorithm"></span><dl> <dt><strong>BCRYPT_RC2_ALGORITHM</strong></dt> <dt> &quot; RC2 &quot; </dt> </dl></td>
<td style="text-align: left;">Algorithme de chiffrement symétrique en bloc RC2.<br/> Standard : RFC 2268<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="BCRYPT_RC4_ALGORITHM"></span><span id="bcrypt_rc4_algorithm"></span><dl> <dt><strong>BCRYPT_RC4_ALGORITHM</strong></dt> <dt> &quot; RC4 &quot; </dt> </dl></td>
<td style="text-align: left;">Algorithme de chiffrement symétrique RC4.<br/> Standard : divers<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="BCRYPT_RNG_ALGORITHM"></span><span id="bcrypt_rng_algorithm"></span><dl> <dt><strong>BCRYPT_RNG_ALGORITHM</strong></dt> <dt> &quot; RNG &quot; </dt> </dl></td>
<td style="text-align: left;">Algorithme du générateur de nombres aléatoires.<br/> Standard : FIPS 186-2, FIPS 140-2, NIST SP 800-90<br/>
<blockquote>
[!Note]<br />
À compter de Windows Vista avec SP1 et Windows Server 2008, le générateur de nombres aléatoires est basé sur le mode de compteur AES spécifié dans la norme NIST SP 800-90.
</blockquote>
<br/> <strong>Windows Vista :</strong> Le générateur de nombres aléatoires est basé sur le générateur de nombres aléatoires basé sur le hachage spécifié dans la norme FIPS 186-2.<br/> <strong>Windows 8 :</strong> À partir de Windows 8, l’algorithme RNG prend en charge FIPS 186-3. Les clés inférieures ou égales à 1024 bits adhèrent à FIPS 186-2 et les clés supérieures à 1024 à FIPS 186-3.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="BCRYPT_RNG_DUAL_EC_ALGORITHM"></span><span id="bcrypt_rng_dual_ec_algorithm"></span><dl> <dt><strong>BCRYPT_RNG_DUAL_EC_ALGORITHM</strong></dt> <dt> &quot; DUALECRNG &quot; </dt> </dl></td>
<td style="text-align: left;">Algorithme de générateur de nombres aléatoires à double courbe elliptique. <br/> Standard : SP800-90.<br/> <strong>Windows 8 :</strong> À compter de Windows 8, l’algorithme EC RNG prend en charge FIPS 186-3. Les clés inférieures ou égales à 1024 bits adhèrent à FIPS 186-2 et les clés supérieures à 1024 à FIPS 186-3.<br/> <strong>Windows 10 :</strong> À partir de Windows 10, l’algorithme de générateur de nombres aléatoires à deux courbes elliptiques a été supprimé. Les utilisations existantes de cet algorithme continuent de fonctionner. Toutefois, le générateur de nombres aléatoires est basé sur le mode de compteur AES spécifié dans la norme NIST SP 800-90. Le nouveau code doit utiliser <strong>BCRYPT_RNG_ALGORITHM</strong>, et il est recommandé de modifier le code existant pour utiliser <strong>BCRYPT_RNG_ALGORITHM</strong>. <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="BCRYPT_RNG_FIPS186_DSA_ALGORITHM"></span><span id="bcrypt_rng_fips186_dsa_algorithm"></span><dl> <dt><strong>BCRYPT_RNG_FIPS186_DSA_ALGORITHM</strong></dt> <dt> &quot; FIPS186DSARNG &quot; </dt> </dl></td>
<td style="text-align: left;">Algorithme de génération de nombres aléatoires approprié pour DSA (Digital Signature Algorithm). <br/> Standard : FIPS 186-2.<br/> <strong>Windows 8 :</strong> La prise en charge de FIPS 186-3 commence.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="BCRYPT_RSA_ALGORITHM"></span><span id="bcrypt_rsa_algorithm"></span><dl> <dt><strong>BCRYPT_RSA_ALGORITHM</strong></dt> <dt> &quot; RSA &quot; </dt> </dl></td>
<td style="text-align: left;">Algorithme de clé publique RSA. <br/> Standard : PKCS #1 v 1.5 et v 2.0.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="BCRYPT_RSA_SIGN_ALGORITHM"></span><span id="bcrypt_rsa_sign_algorithm"></span><dl> <dt><strong>BCRYPT_RSA_SIGN_ALGORITHM</strong></dt> <dt> &quot; RSA_SIGN &quot; </dt> </dl></td>
<td style="text-align: left;">Algorithme de signature RSA. Cet algorithme n’est pas pris en charge actuellement. Vous pouvez utiliser l’algorithme <strong>BCRYPT_RSA_ALGORITHM</strong> pour effectuer des opérations de signature RSA. <br/> Standard : PKCS #1 v 1.5 et v 2.0.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="BCRYPT_SHA1_ALGORITHM"></span><span id="bcrypt_sha1_algorithm"></span><dl> <dt><strong>BCRYPT_SHA1_ALGORITHM</strong></dt> <dt> &quot; SHA1 &quot; </dt> </dl></td>
<td style="text-align: left;">Algorithme de hachage sécurisé 160 bits. <br/> Standard : FIPS 180-2, FIPS 198.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="BCRYPT_SHA256_ALGORITHM"></span><span id="bcrypt_sha256_algorithm"></span><dl> <dt><strong>BCRYPT_SHA256_ALGORITHM</strong></dt> <dt> &quot; SHA256 &quot; </dt> </dl></td>
<td style="text-align: left;">Algorithme de hachage sécurisé 256 bits.<br/> Standard : FIPS 180-2, FIPS 198.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="BCRYPT_SHA384_ALGORITHM"></span><span id="bcrypt_sha384_algorithm"></span><dl> <dt><strong>BCRYPT_SHA384_ALGORITHM</strong></dt> <dt> &quot; SHA384 &quot; </dt> </dl></td>
<td style="text-align: left;">Algorithme de hachage sécurisé 384 bits. <br/> Standard : FIPS 180-2, FIPS 198.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="BCRYPT_SHA512_ALGORITHM"></span><span id="bcrypt_sha512_algorithm"></span><dl> <dt><strong>BCRYPT_SHA512_ALGORITHM</strong></dt> <dt> &quot; SHA512 &quot; </dt> </dl></td>
<td style="text-align: left;">Algorithme de hachage sécurisé 512 bits. <br/> Standard : FIPS 180-2, FIPS 198.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="BCRYPT_SP800108_CTR_HMAC_ALGORITHM"></span><span id="bcrypt_sp800108_ctr_hmac_algorithm"></span><dl> <dt><strong>BCRYPT_SP800108_CTR_HMAC_ALGORITHM</strong></dt> <dt>L &quot; SP800_108_CTR_HMAC &quot; </dt> </dl></td>
<td style="text-align: left;">Mode compteur, algorithme HMAC (Hash-based Message Authentication Code) fonction de dérivation de clés. Utilisé par les fonctions <a href="/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptkeyderivation"><strong>BCryptKeyDerivation</strong></a> et <a href="/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptkeyderivation"><strong>NCryptKeyDerivation</strong></a> .<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="BCRYPT_SP80056A_CONCAT_ALGORITHM"></span><span id="bcrypt_sp80056a_concat_algorithm"></span><dl> <dt><strong>BCRYPT_SP80056A_CONCAT_ALGORITHM</strong></dt> <dt>L &quot; SP800_56A_CONCAT &quot; </dt> </dl></td>
<td style="text-align: left;">Algorithme de fonction de dérivation de clé SP800-56A. Utilisé par les fonctions <a href="/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptkeyderivation"><strong>BCryptKeyDerivation</strong></a> et <a href="/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptkeyderivation"><strong>NCryptKeyDerivation</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="_BCRYPT_PBKDF2_ALGORITHM"></span><span id="_bcrypt_pbkdf2_algorithm"></span><dl> <dt> <strong>BCRYPT_PBKDF2_ALGORITHM</strong> </dt> <dt>L &quot; PBKDF2 &quot; </dt> </dl></td>
<td style="text-align: left;">Algorithme de la fonction de dérivation de clé basée sur mot de passe (PBKDF2). Utilisé par les fonctions <a href="/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptkeyderivation"><strong>BCryptKeyDerivation</strong></a> et <a href="/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptkeyderivation"><strong>NCryptKeyDerivation</strong></a> .<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="BCRYPT_ECDSA_ALGORITHM"></span><span id="bcrypt_ecdsa_algorithm"></span><dl> <dt><strong>BCRYPT_ECDSA_ALGORITHM</strong></dt> <dt> &quot; ECDSA &quot; </dt> </dl></td>
<td style="text-align: left;">Algorithme de signature numérique à courbe elliptique générique principale (pour plus d’informations, consultez la <strong>section Notes</strong> ). <br/> Standard : ANSI X 9.62.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="BCRYPT_ECDH_ALGORITHM"></span><span id="bcrypt_ecdh_algorithm"></span><dl> <dt><strong>BCRYPT_ECDH_ALGORITHM</strong></dt> <dt> &quot; ECDH &quot; </dt> </dl></td>
<td style="text-align: left;">Algorithme d’échange de clés de la courbe elliptique générique principale Diffie-Hellman (pour plus d’informations, consultez la <strong>section Notes</strong> ). <br/> Standard : SP800-56A.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="BCRYPT_XTS_AES_ALGORITHM"></span><span id="bcrypt_xts_aes_algorithm"></span><dl> <dt><strong>BCRYPT_XTS_AES_ALGORITHM</strong></dt> <dt> &quot; XTS-AES &quot; </dt> </dl></td>
<td style="text-align: left;">Algorithme de chiffrement symétrique Advanced Encryption Standard en mode XTS. <br/> Standard : SP-800-38E, IEEE STD 1619-2007.<br/> <strong>Windows 10 :</strong> La prise en charge de cet algorithme commence.<br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a>Notes

Pour utiliser l’algorithme ECDH **\_ ECDSA \_ souhaité** ou bcrypt, appelez [**BCryptOpenAlgorithmProvider**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptopenalgorithmprovider) avec l’algorithme **\_ ECDSA bcrypt \_** ou l' **\_ \_ algorithme ECDH** de bcrypt comme *pszAlgId*. **\_ \_** Utilisez ensuite [**BCryptSetProperty**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptsetproperty) pour définir la propriété de nom de la **\_ \_ courbe \_ ECC BCRYPT** sur un algorithme nommé listé dans CNG named Curves.

Pour le fournisseur de paramètres de courbe elliptique définis par l’utilisateur directement, utilisez [**BCryptSetProperty**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptsetproperty) pour définir la propriété **BCRYPT \_ ECC \_ Parameters** . Pour plus d’informations, téléchargez le [Kit de développement du fournisseur de services de chiffrement Windows 10 (CPDK)](https://www.microsoft.com/download/details.aspx?id=30688) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                      |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>Bcrypt. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**BCryptOpenAlgorithmProvider**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptopenalgorithmprovider)
</dt> <dt>

[**NCryptCreatePersistedKey**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptcreatepersistedkey)
</dt> </dl>

 

 




