---
description: Accède à un conteneur de clé existant. Cette méthode associe le conteneur de clé au certificat qui correspond à la clé privée en ajoutant la propriété de la clé de certificat \_ \_ Prov \_ info \_ prop \_ ID à l’aide des informations spécifiées.
ms.assetid: e5e19452-bfdc-4427-ac1d-cf8aa349bb89
title: PrivateKey. Open, méthode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PrivateKey.Open
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 7e39738a6e28ebbaffbc867f3098270d5043887a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127120857"
---
# <a name="privatekeyopen-method"></a>PrivateKey. Open, méthode

\[La méthode **Open** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section relative à la configuration requise. Utilisez plutôt la [**propriété X509Certificate2. PrivateKey**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.privatekey?view=netcore-3.1) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

La méthode **Open** accède à un [*conteneur de clé*](../secgloss/k-gly.md)existant. Cette méthode associe le conteneur de clé au [*certificat*](../secgloss/c-gly.md) qui correspond à la [*clé privée*](../secgloss/p-gly.md) en ajoutant la propriété de la clé de certificat \_ \_ Prov \_ info \_ prop \_ ID à l’aide des informations spécifiées.

## <a name="syntax"></a>Syntaxe


```VB
PrivateKey.Open( _
  ByVal ContainerName, _
  [ ByVal ProviderName ], _
  [ ByVal ProviderType ], _
  [ ByVal KeySpec ], _
  [ ByVal StoreLocation ], _
  [ ByVal bCheckExistence ] _
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ContainerName* \[ dans\]
</dt> <dd>

Chaîne qui contient le nom du conteneur de clé.

</dd> <dt>

*ProviderName* \[ dans, facultatif\]
</dt> <dd>

Chaîne qui contient le nom du fournisseur. La valeur par défaut est CAPICOM \_ Prov \_ \_ améliorée \_ Prov. Ce paramètre peut prendre les valeurs suivantes.



| Valeur                                                                                                                                                                                                                                      | Signification                                                                      |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span id="CAPICOM_PROV_MS_DEF_PROV"></span><span id="capicom_prov_ms_def_prov"></span><dl> <dt>**CAPICOM \_ Proven \_ MS \_ Def \_ Prov**</dt> </dl>                                          | Fournisseur de services de chiffrement de base Microsoft.<br/>                            |
| <span id="CAPICOM_PROV_MS_ENHANCED_PROV"></span><span id="capicom_prov_ms_enhanced_prov"></span><dl> <dt>**CAPICOM \_ Proven Prov \_ \_ amélioré \_**</dt> </dl>                           | Fournisseur de services de chiffrement amélioré Microsoft.<br/>                        |
| <span id="CAPICOM_PROV_MS_STRONG_PROV"></span><span id="capicom_prov_ms_strong_prov"></span><dl> <dt>**CAPICOM \_ prove Prov \_ \_ solide \_ Proven**</dt> </dl>                                 | Fournisseur de services de chiffrement renforcé Microsoft.<br/>                          |
| <span id="CAPICOM_PROV_MS_DEF_RSA_SIG_PROV"></span><span id="capicom_prov_ms_def_rsa_sig_prov"></span><dl> <dt>**CAPICOM \_ Proven \_ MS \_ Def \_ RSA \_ SIG \_ Prov**</dt> </dl>                | Fournisseur de chiffrement de signature Microsoft RSA.<br/>                   |
| <span id="CAPICOM_PROV_MS_DEF_RSA_SCHANNEL_PROV"></span><span id="capicom_prov_ms_def_rsa_schannel_prov"></span><dl> <dt>**CAPICOM \_ Proven \_ MS \_ Def \_ RSA \_ Schannel \_ Prov**</dt> </dl> | Fournisseur de services de chiffrement Microsoft RSA Schannel.<br/>                    |
| <span id="CAPICOM_PROV_MS_DEF_DSS_PROV"></span><span id="capicom_prov_ms_def_dss_prov"></span><dl> <dt>**CAPICOM \_ Provo Prov \_ - \_ Def \_ Prov \_**</dt> </dl>                             | Fournisseur de services de chiffrement DSS de base Microsoft.<br/>                        |
| <span id="CAPICOM_PROV_MS_DEF_DSS_DH_PROV"></span><span id="capicom_prov_ms_def_dss_dh_prov"></span><dl> <dt>**CAPICOM \_ Proven, \_ MS \_ Def \_ DSS \_ , \_ Prov.**</dt> </dl>                   | Microsoft Base DSS et Diffie-Hellman fournisseur de services de chiffrement.<br/>     |
| <span id="CAPICOM_PROV_MS_ENH_DSS_DH_PROV"></span><span id="capicom_prov_ms_enh_dss_dh_prov"></span><dl> <dt>**CAPICOM \_ Proven \_ \_ ENH \_ DSS \_ \_**</dt> </dl>                   | Microsoft Enhanced DSS et Diffie-Hellman fournisseur de services de chiffrement.<br/> |
| <span id="CAPICOM_PROV_MS_DEF_DH_SCHANNEL_PROV"></span><span id="capicom_prov_ms_def_dh_schannel_prov"></span><dl> <dt>**CAPICOM \_ prouver \_ MS \_ Def \_ DH \_ Schannel \_ Prov**</dt> </dl>    | Fournisseur de services de chiffrement Microsoft DH SChannel.<br/>                     |
| <span id="CAPICOM_PROV_MS_SCARD_PROV"></span><span id="capicom_prov_ms_scard_prov"></span><dl> <dt>**CAPICOM prove prove proved \_ \_ \_ \_ Prov**</dt> </dl>                                    | Fournisseur de chiffrement de la carte à puce de base Microsoft.<br/>                 |
| <span id="CAPICOM_PROV_MS_ENH_RSA_AES_PROV"></span><span id="capicom_prov_ms_enh_rsa_aes_prov"></span><dl> <dt>**CAPICOM \_ prove \_ \_ ENH \_ RSA \_ AES \_ Prov**</dt> </dl>                | Fournisseur de services de chiffrement RSA et AES amélioré par Microsoft.<br/>            |



 

</dd> <dt>

*ProviderType* \[ dans, facultatif\]
</dt> <dd>

Valeur de l’énumération de [**\_ \_ type**](capicom-prov-type.md) de CAPICOM Prov qui spécifie un type de fournisseur. La valeur par défaut est CAPICOM \_ Prov \_ \_ Complete RSA. Ce paramètre peut prendre les valeurs suivantes.



| Valeur                                                                                                                                                                                                   | Signification                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_PROV_RSA_FULL"></span><span id="capicom_prov_rsa_full"></span><dl> <dt>**CAPICOM \_ Proven \_ RSA \_ Full**</dt> </dl>                 | Fournisseur de [](../secgloss/r-gly.md) [*services de chiffrement*](../secgloss/c-gly.md) (CSP) RSA complet. Ce type de fournisseur prend en charge les [*signatures numériques*](../secgloss/d-gly.md) et le [*chiffrement*](../secgloss/e-gly.md)des données.<br/> |
| <span id="CAPICOM_PROV_RSA_SIG"></span><span id="capicom_prov_rsa_sig"></span><dl> <dt>**CAPICOM \_ Proven \_ RSA \_ SIG**</dt> </dl>                    | Le sous-ensemble du CSP RSA qui prend uniquement en charge les fonctions et algorithmes requis pour les [*hachages*](../secgloss/h-gly.md) et les [*signatures numériques*](../secgloss/d-gly.md).<br/>                                                                                                                                                                              |
| <span id="CAPICOM_PROV_DSS"></span><span id="capicom_prov_dss"></span><dl> <dt>**CAPICOM \_ Proven \_**</dt> </dl>                                 | CSP DSS ( [*Digital Signature standard*](../secgloss/d-gly.md) ). Ce type de fournisseur prend uniquement en charge les hachages et les signatures numériques. DSS utilise l' [*algorithme de signature numérique*](../secgloss/d-gly.md) (DSA).<br/>                                                                                     |
| <span id="CAPICOM_PROV_FORTEZZA"></span><span id="capicom_prov_fortezza"></span><dl> <dt>**CAPICOM \_ Proven ( \_ Fortezza)**</dt> </dl>                  | Fournisseur de services de chiffrement qui contient les protocoles et algorithmes de chiffrement détenus par le [*National Institute of Standards and Technology*](../secgloss/n-gly.md) (NIST).<br/>                                                                                                                                                                          |
| <span id="CAPICOM_PROV_MS_EXCHANGE"></span><span id="capicom_prov_ms_exchange"></span><dl> <dt>**CAPICOM Prov- \_ Microsoft \_ \_**</dt> </dl>        | fournisseur de services de chiffrement qui prend en charge l’application microsoft Exchange mail et d’autres applications compatibles avec microsoft mail.<br/>                                                                                                                                                                                                                                                                                                                               |
| <span id="CAPICOM_PROV_SSL"></span><span id="capicom_prov_ssl"></span><dl> <dt>**CAPICOM Prov- \_ \_ SSL**</dt> </dl>                                 | Fournisseur de services de chiffrement qui prend en charge le protocole [*SSL (Secure Sockets Layer)*](../secgloss/s-gly.md) (SSL).<br/>                                                                                                                                                                                                                                                                                  |
| <span id="CAPICOM_PROV_RSA_SCHANNEL"></span><span id="capicom_prov_rsa_schannel"></span><dl> <dt>**CAPICOM \_ Proven \_ RSA \_ Schannel**</dt> </dl>     | Fournisseur de services de chiffrement qui prend en charge les protocoles RSA et [*Schannel*](../secgloss/s-gly.md) .<br/>                                                                                                                                                                                                                                                                                                                                    |
| <span id="CAPICOM_PROV_DSS_DH"></span><span id="capicom_prov_dss_dh"></span><dl> <dt>**CAPICOM \_ Proven \_ DSS \_**</dt> </dl>                       | Fournisseur de services de chiffrement qui prend en charge les protocoles DSS et [*Diffie-Hellman*](../secgloss/d-gly.md) .<br/>                                                                                                                                                                                                                                                                                              |
| <span id="CAPICOM_PROV_EC_ECDSA_SIG"></span><span id="capicom_prov_ec_ecdsa_sig"></span><dl> <dt>**CAPICOM \_ Proven \_ EC EC \_ \_**</dt> </dl>    | Fournisseur de services de chiffrement qui prend en charge les fonctions et algorithmes ECDSA (Elliptic Curve Digital Signature Algorithm) requis pour les signatures numériques.<br/>                                                                                                                                                                                                                                                                                                                      |
| <span id="CAPICOM_PROV_EC_ECNRA_SIG"></span><span id="capicom_prov_ec_ecnra_sig"></span><dl> <dt>**CAPICOM \_ Proven \_ EC \_ ECNRA \_ SIG**</dt> </dl>    | Fournisseur de services de chiffrement qui prend en charge les fonctions ECNRA (Elliptic Curve Nyberg-Rueppel ANALOG) et les algorithmes requis pour les signatures numériques.<br/>                                                                                                                                                                                                                                                                                                                            |
| <span id="CAPICOM_PROV_EC_ECDSA_FULL"></span><span id="capicom_prov_ec_ecdsa_full"></span><dl> <dt>**CAPICOM \_ Proven \_ EC \_ \_ complet**</dt> </dl> | Fournisseur de services de chiffrement qui prend en charge l’algorithme ECDSA complet.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="CAPICOM_PROV_EC_ECNRA_FULL"></span><span id="capicom_prov_ec_ecnra_full"></span><dl> <dt>**CAPICOM \_ Proven \_ EC \_ ECNRA \_ Full**</dt> </dl> | Fournisseur de services de chiffrement qui prend en charge la ECNRA complète.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="CAPICOM_PROV_DH_SCHANNEL"></span><span id="capicom_prov_dh_schannel"></span><dl> <dt>**CAPICOM \_ Proven- \_ DH \_ Schannel**</dt> </dl>        | Fournisseur de services de chiffrement qui prend en charge les protocoles [*Diffie-Hellman*](../secgloss/d-gly.md) et [*Schannel*](../secgloss/s-gly.md) .<br/>                                                                                                                                                                                                                       |
| <span id="CAPICOM_PROV_SPYRUS_LYNKS"></span><span id="capicom_prov_spyrus_lynks"></span><dl> <dt>**CAPICOM \_ Prov \_ Spyrus \_ Lynks**</dt> </dl>     | Fournisseur de services de chiffrement qui prend en charge l’appareil de carte SPYRUS LYNKS.<br/>                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="CAPICOM_PROV_RNG"></span><span id="capicom_prov_rng"></span><dl> <dt>**CAPICOM \_ Prov \_ RNG**</dt> </dl>                                 | CSP qui gère la génération de nombres aléatoires.<br/>                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="CAPICOM_PROV_INTEL_SEC"></span><span id="capicom_prov_intel_sec"></span><dl> <dt>**CAPICOM \_ Prov \_ Intel \_**</dt> </dl>              | CSP qui fournit la sécurité Intel.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="CAPICOM_PROV_REPLACE_OWF"></span><span id="capicom_prov_replace_owf"></span><dl> <dt>**CAPICOM Prov- \_ \_ remplacer \_ OWF**</dt> </dl>        | Fournisseur de services de chiffrement qui prend en charge le remplacement de la manière dont les formats unidirectionnels sont générés à partir des mots de passe.<br/>                                                                                                                                                                                                                                                                                                                                                      |
| <span id="CAPICOM_PROV_RSA_AES"></span><span id="capicom_prov_rsa_aes"></span><dl> <dt>**CAPICOM \_ Prov \_ RSA \_ AES**</dt> </dl>                    | CSP qui prend en charge les signatures numériques et le chiffrement des données à l’aide de l’algorithme Advanced Encryption Standard ([*AES*](../secgloss/a-gly.md)).<br/>                                                                                                                                                                                                                                                                           |



 

</dd> <dt>

*KeySpec* \[ dans, facultatif\]
</dt> <dd>

Valeur de l’énumération des [**\_ \_ spécifications de clé CAPICOM**](capicom-key-spec.md) qui spécifie le type de clé privée. La valeur par défaut est la signature de la \_ spécification de clé CAPICOM \_ \_ . Ce paramètre peut prendre les valeurs suivantes.



| Valeur                                                                                                                                                                                                        | Signification                                                    |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <span id="CAPICOM_KEY_SPEC_KEYEXCHANGE"></span><span id="capicom_key_spec_keyexchange"></span><dl> <dt>**clé d’échange de la \_ spécification de clé CAPICOM \_ \_**</dt> </dl> | La clé peut être utilisée pour le chiffrement et la signature.<br/> |
| <span id="CAPICOM_KEY_SPEC_SIGNATURE"></span><span id="capicom_key_spec_signature"></span><dl> <dt>**SIGNATURE de la \_ spécification de clé CAPICOM \_ \_**</dt> </dl>       | La clé peut être utilisée uniquement pour la signature.<br/>           |



 

</dd> <dt>

*StoreLocation* \[ dans, facultatif\]
</dt> <dd>

Valeur de l’énumération de l' [**\_ \_ emplacement du magasin CAPICOM**](capicom-store-location.md) qui spécifie l’emplacement du magasin dans lequel réside la clé. La valeur par défaut est le magasin de l' \_ utilisateur actuel CAPICOM \_ \_ . Ce paramètre peut prendre les valeurs suivantes.



| Valeur                                                                                                                                                                                                                              | Signification                                                                                                                                                                                                                                                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_MEMORY_STORE"></span><span id="capicom_memory_store"></span><dl> <dt>**\_magasin mémoire CAPICOM \_**</dt> </dl>                                                | Le magasin est un magasin de mémoire. Les modifications apportées au contenu du magasin ne sont pas conservées.<br/>                                                                                                                                                                                |
| <span id="CAPICOM_LOCAL_MACHINE_STORE"></span><span id="capicom_local_machine_store"></span><dl> <dt>**base de l' \_ ordinateur local CAPICOM \_ \_**</dt> </dl>                          | Le magasin est un magasin de l’ordinateur local. Les magasins d’ordinateurs locaux peuvent être des magasins de lecture/écriture uniquement si l’utilisateur dispose d’autorisations de lecture/écriture. Si l’utilisateur dispose d’autorisations de lecture/écriture et si le magasin est ouvert en lecture/écriture, les modifications apportées au contenu du magasin sont conservées.<br/> |
| <span id="CAPICOM_CURRENT_USER_STORE"></span><span id="capicom_current_user_store"></span><dl> <dt>**magasin de l' \_ utilisateur actuel CAPICOM \_ \_**</dt> </dl>                             | Le magasin est un magasin de l’utilisateur actuel. Un magasin de l’utilisateur actuel peut être un magasin en lecture/écriture. Si c’est le cas, les modifications apportées au contenu du magasin sont conservées.<br/>                                                                                                                        |
| <span id="CAPICOM_ACTIVE_DIRECTORY_USER_STORE"></span><span id="capicom_active_directory_user_store"></span><dl> <dt>**magasin d’utilisateurs de CAPICOM \_ active \_ Directory \_ \_**</dt> </dl> | Le magasin est un magasin de Active Directory. Les magasins de Active Directory ne peuvent être ouverts qu’en mode lecture seule. Impossible d’ajouter ou de supprimer des certificats dans des magasins de Active Directory.<br/>                                                                                          |
| <span id="CAPICOM_SMART_CARD_USER_STORE"></span><span id="capicom_smart_card_user_store"></span><dl> <dt>**\_magasin d’utilisateurs de \_ carte à puce \_ CAPICOM \_**</dt> </dl>                   | Le magasin est le groupe de cartes à puce actuelles. Introduit dans CAPICOM 2,0.<br/>                                                                                                                                                                                               |



 

</dd> <dt>

*bCheckExistence* \[ dans, facultatif\]
</dt> <dd>

Valeur booléenne qui indique si CAPICOM tentera d’accéder à la clé. Si la **valeur est true**, CAPICOM tente d’accéder à la clé. Si la clé est protégée par l’utilisateur ou sur une carte à puce ou un autre périphérique, une boîte de dialogue peut être générée. La valeur par défaut est **False**.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Cette méthode retourne CAPICOM \_ E \_ non \_ autorisé lorsqu’il s’agit d’un script à partir d’une application Web.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|----------------------------|----------------------------------------------------------------------------------------|
| Composant redistribuable<br/> | capicom 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**PrivateKey**](privatekey.md)
</dt> <dt>

[**Certificate. HasPrivateKey**](certificate-hasprivatekey.md)
</dt> </dl>

 

 
