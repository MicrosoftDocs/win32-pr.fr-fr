---
description: Récupère une valeur de l' \_ \_ énumération de type d’un type de preuve Proven qui spécifie le type de fournisseur.
ms.assetid: bc6a579f-5532-45e3-97f4-adcde2cd29e5
title: PrivateKey. ProviderType, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PrivateKey.ProviderType
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: b38cc9a030bc27a30a66624f1faeca080104e7fa
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127120853"
---
# <a name="privatekeyprovidertype-property"></a>PrivateKey. ProviderType, propriété

\[La propriété **ProviderType** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise. Utilisez plutôt la [**propriété X509Certificate2. PrivateKey**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.privatekey?view=netcore-3.1) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

La propriété **ProviderType** récupère une valeur de l’énumération de type d’un [**\_ \_ type de preuve Proven**](capicom-prov-type.md) qui spécifie le type de fournisseur.

## <a name="syntax"></a>Syntaxe


```VB
PrivateKey.ProviderType As CAPICOM_PROV_TYPE
```



## <a name="property-value"></a>Valeur de la propriété

Valeur de l’énumération de [**\_ \_ type**](capicom-prov-type.md) de CAPICOM Prov qui indique le type de fournisseur. Le tableau suivant répertorie les valeurs possibles.



| Value                                                                                                                                                                                                   | Signification                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_PROV_RSA_FULL"></span><span id="capicom_prov_rsa_full"></span><dl> <dt>**CAPICOM \_ Proven \_ RSA \_ Full**</dt> </dl>                 | Fournisseur de [](../secgloss/r-gly.md) [*services de chiffrement*](../secgloss/c-gly.md) (CSP) RSA complet. Ce type de fournisseur prend en charge les [*signatures numériques*](../secgloss/d-gly.md) et le [*chiffrement*](../secgloss/e-gly.md)des données.<br/> |
| <span id="CAPICOM_PROV_RSA_SIG"></span><span id="capicom_prov_rsa_sig"></span><dl> <dt>**CAPICOM \_ Proven \_ RSA \_ SIG**</dt> </dl>                    | Le sous-ensemble du CSP RSA qui prend uniquement en charge les fonctions et algorithmes requis pour les hachages et les signatures numériques.<br/>                                                                                                                                                                                                                                                                                                                                     |
| <span id="CAPICOM_PROV_DSS"></span><span id="capicom_prov_dss"></span><dl> <dt>**CAPICOM \_ Proven \_**</dt> </dl>                                 | CSP DSS ( [*Digital Signature standard*](../secgloss/d-gly.md) ). Ce type de fournisseur prend uniquement en charge les hachages et les signatures numériques. DSS utilise l' [*algorithme de signature numérique*](../secgloss/d-gly.md) (DSA).<br/>                                                                                     |
| <span id="CAPICOM_PROV_FORTEZZA"></span><span id="capicom_prov_fortezza"></span><dl> <dt>**CAPICOM \_ Proven ( \_ Fortezza)**</dt> </dl>                  | Fournisseur de services de chiffrement qui contient les protocoles et algorithmes de chiffrement détenus par le [*National Institute of Standards and Technology*](../secgloss/n-gly.md) (NIST).<br/>                                                                                                                                                                          |
| <span id="CAPICOM_PROV_MS_EXCHANGE"></span><span id="capicom_prov_ms_exchange"></span><dl> <dt>**CAPICOM Prov- \_ Microsoft \_ \_**</dt> </dl>        | fournisseur de services de chiffrement conçu pour les besoins de chiffrement de l’application microsoft Exchange mail et d’autres applications compatibles avec microsoft mail.<br/>                                                                                                                                                                                                                                                                                                              |
| <span id="CAPICOM_PROV_SSL"></span><span id="capicom_prov_ssl"></span><dl> <dt>**CAPICOM Prov- \_ \_ SSL**</dt> </dl>                                 | Fournisseur de services de chiffrement qui prend en charge le protocole [*SSL (Secure Sockets Layer)*](../secgloss/s-gly.md) (SSL).<br/>                                                                                                                                                                                                                                                                                  |
| <span id="CAPICOM_PROV_RSA_SCHANNEL"></span><span id="capicom_prov_rsa_schannel"></span><dl> <dt>**CAPICOM \_ Proven \_ RSA \_ Schannel**</dt> </dl>     | Fournisseur de services de chiffrement qui prend en charge les protocoles RSA et [*Schannel*](../secgloss/s-gly.md) .<br/>                                                                                                                                                                                                                                                                                                                                    |
| <span id="CAPICOM_PROV_DSS_DH"></span><span id="capicom_prov_dss_dh"></span><dl> <dt>**CAPICOM \_ Proven \_ DSS \_**</dt> </dl>                       | Fournisseur de services de chiffrement qui prend en charge les protocoles de [*signature numérique standard*](../secgloss/d-gly.md) (DSS) et [*Diffie-Hellman*](../secgloss/d-gly.md) .<br/>                                                                                                                                                           |
| <span id="CAPICOM_PROV_EC_ECDSA_SIG"></span><span id="capicom_prov_ec_ecdsa_sig"></span><dl> <dt>**CAPICOM \_ Proven \_ EC EC \_ \_**</dt> </dl>    | Fournisseur de services de chiffrement qui prend en charge les fonctions et algorithmes ECDSA (Elliptic Curve Digital Signature Algorithm) requis pour les signatures numériques.<br/>                                                                                                                                                                                                                                                                                                                      |
| <span id="CAPICOM_PROV_EC_ECNRA_SIG"></span><span id="capicom_prov_ec_ecnra_sig"></span><dl> <dt>**CAPICOM \_ Proven \_ EC \_ ECNRA \_ SIG**</dt> </dl>    | Fournisseur de services de chiffrement qui prend en charge les fonctions ECNRA (Elliptic Curve Nyberg-Rueppel ANALOG) et les algorithmes requis pour les signatures numériques.<br/>                                                                                                                                                                                                                                                                                                                            |
| <span id="CAPICOM_PROV_EC_ECDSA_FULL"></span><span id="capicom_prov_ec_ecdsa_full"></span><dl> <dt>**CAPICOM \_ Proven \_ EC \_ \_ complet**</dt> </dl> | Fournisseur de services de chiffrement qui prend en charge l’algorithme ECDSA complet.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="CAPICOM_PROV_EC_ECNRA_FULL"></span><span id="capicom_prov_ec_ecnra_full"></span><dl> <dt>**CAPICOM \_ Proven \_ EC \_ ECNRA \_ Full**</dt> </dl> | Fournisseur de services de chiffrement qui prend en charge la ECNRA complète.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="CAPICOM_PROV_DH_SCHANNEL"></span><span id="capicom_prov_dh_schannel"></span><dl> <dt>**CAPICOM \_ Proven- \_ DH \_ Schannel**</dt> </dl>        | Fournisseur de services de chiffrement qui prend en charge les protocoles [*Diffie-Hellman*](../secgloss/d-gly.md) et [*Schannel*](../secgloss/s-gly.md) .<br/>                                                                                                                                                                                                                       |
| <span id="CAPICOM_PROV_SPYRUS_LYNKS"></span><span id="capicom_prov_spyrus_lynks"></span><dl> <dt>**CAPICOM \_ Prov \_ Spyrus \_ Lynks**</dt> </dl>     | Fournisseur de services de chiffrement qui prend en charge l’appareil de carte SPYRUS LYNKS.<br/>                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="CAPICOM_PROV_RNG"></span><span id="capicom_prov_rng"></span><dl> <dt>**CAPICOM \_ Prov \_ RNG**</dt> </dl>                                 | CSP qui gère la génération de nombres aléatoires.<br/>                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="CAPICOM_PROV_INTEL_SEC"></span><span id="capicom_prov_intel_sec"></span><dl> <dt>**CAPICOM \_ Prov \_ Intel \_**</dt> </dl>              | CSP qui fournit la sécurité Intel.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="CAPICOM_PROV_REPLACE_OWF"></span><span id="capicom_prov_replace_owf"></span><dl> <dt>**CAPICOM Prov- \_ \_ remplacer \_ OWF**</dt> </dl>        | Fournisseur de services de chiffrement qui prend en charge le remplacement de la manière dont les formats unidirectionnels (OWFs) sont générés à partir de mots de passe.<br/>                                                                                                                                                                                                                                                                                                                                               |
| <span id="CAPICOM_PROV_RSA_AES"></span><span id="capicom_prov_rsa_aes"></span><dl> <dt>**CAPICOM \_ Prov \_ RSA \_ AES**</dt> </dl>                    | CSP qui prend en charge les signatures numériques et le chiffrement des données à l’aide de l’algorithme [*Advanced Encryption Standard*](../secgloss/a-gly.md) (AES).<br/>                                                                                                                                                                                                                                                                           |



 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|----------------------------|----------------------------------------------------------------------------------------|
| Composant redistribuable<br/> | capicom 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**PrivateKey**](privatekey.md)
</dt> </dl>

 

 
