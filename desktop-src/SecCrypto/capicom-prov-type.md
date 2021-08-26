---
description: Spécifie le type de fournisseur de services de chiffrement (CSP).
ms.assetid: faf2390d-bf78-4943-91f3-1db9939fedfb
title: Énumération CAPICOM_PROV_TYPE (CAPICOM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_PROV_TYPE
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: bf85d2eb01ffd4290c5200e09c842f280cd5418dc5203bba068ecb5bcd65c355
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119879019"
---
# <a name="capicom_prov_type-enumeration"></a>\_ \_ Énumération de type Proven

L’énumération de **\_ \_ type de CAPICOM Proval** spécifie le type de fournisseur de services de [*chiffrement*](../secgloss/c-gly.md) (CSP).

## <a name="members"></a>Membres



| Membre                             | Description                                                                                                                                                                                                                                                                                                                                                                        | Valeur |
|------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------|
| **CAPICOM \_ Proven \_ RSA \_ Full**       | La totalité du CSP [*RSA*](../secgloss/r-gly.md) . Ce type de fournisseur prend en charge les [*signatures numériques*](../secgloss/d-gly.md) et le [*chiffrement*](../secgloss/e-gly.md)des données.<br/>                                                            | 1     |
| **CAPICOM \_ Proven \_ RSA \_ SIG**        | Le sous-ensemble du CSP RSA qui prend uniquement en charge les fonctions et algorithmes requis pour les hachages et les signatures numériques.<br/>                                                                                                                                                                                                                                        | 2     |
| **CAPICOM \_ Proven \_**             | CSP DSS ( [*Digital Signature standard*](../secgloss/d-gly.md) ). Ce type de fournisseur prend uniquement en charge les hachages et les signatures numériques. DSS utilise l' [*algorithme de signature numérique*](../secgloss/d-gly.md) (DSA).<br/> | 3     |
| **CAPICOM \_ Proven ( \_ Fortezza)**        | Fournisseur de services de chiffrement qui contient les protocoles et algorithmes de chiffrement détenus par le [*National Institute of Standards and Technology*](../secgloss/n-gly.md) (NIST).<br/>                                                                                      | 4     |
| **CAPICOM Prov- \_ Microsoft \_ \_**    | fournisseur de services de chiffrement conçu pour les besoins de chiffrement de Exchange et d’autres applications compatibles avec Microsoft Mail.<br/>                                                                                                                                                                                                                                       | 5     |
| **CAPICOM Prov- \_ \_ SSL**             | Fournisseur de services de chiffrement qui prend en charge le protocole [*SSL (Secure Sockets Layer)*](../secgloss/s-gly.md) (SSL).<br/>                                                                                                                                                                                              | 6     |
| **CAPICOM \_ Proven \_ RSA \_ Schannel**   | Fournisseur de services de chiffrement qui prend en charge les protocoles [*RSA*](../secgloss/r-gly.md) et [*Schannel*](../secgloss/s-gly.md) .<br/>                                                                                                                                                                                        | 12    |
| **CAPICOM \_ Proven \_ DSS \_**         | Fournisseur de services de chiffrement qui prend en charge les protocoles DSS et [*Diffie-Hellman*](../secgloss/d-gly.md) .<br/>                                                                                                                                                                                                          | 13    |
| **CAPICOM \_ Proven \_ EC EC \_ \_**  | Fournisseur de services de chiffrement qui prend en charge les fonctions et algorithmes ECDSA (Elliptic Curve Digital Signature Algorithm) requis pour les signatures numériques.<br/>                                                                                                                                                                                                                                  | 14    |
| **CAPICOM \_ Proven \_ EC \_ ECNRA \_ SIG**  | Fournisseur de services de chiffrement qui prend en charge les fonctions ECNRA (Elliptic Curve Nyberg-Rueppel ANALOG) et les algorithmes requis pour les signatures numériques.<br/>                                                                                                                                                                                                                                        | 15    |
| **CAPICOM \_ Proven \_ EC \_ \_ complet** | Fournisseur de services de chiffrement qui prend en charge l’algorithme ECDSA complet.<br/>                                                                                                                                                                                                                                                                                                                                   | 16    |
| **CAPICOM \_ Proven \_ EC \_ ECNRA \_ Full** | Fournisseur de services de chiffrement qui prend en charge la ECNRA complète.<br/>                                                                                                                                                                                                                                                                                                                                   | 17    |
| **CAPICOM \_ Proven- \_ DH \_ Schannel**    | Fournisseur de services de chiffrement qui prend en charge les protocoles [*Diffie-Hellman*](../secgloss/d-gly.md) et [*Schannel*](../secgloss/s-gly.md) .<br/>                                                                                                                                   | 18    |
| **CAPICOM \_ Prov \_ Spyrus \_ Lynks**   | Fournisseur de services de chiffrement qui prend en charge l’appareil de carte SPYRUS LYNKS.<br/>                                                                                                                                                                                                                                                                                                                     | 20    |
| **CAPICOM \_ Prov \_ RNG**             | CSP qui gère la génération de nombres aléatoires.<br/>                                                                                                                                                                                                                                                                                                                          | 21    |
| **CAPICOM \_ Prov \_ Intel \_**      | CSP qui fournit la sécurité Intel.<br/>                                                                                                                                                                                                                                                                                                                                   | 22    |
| **CAPICOM Prov- \_ \_ remplacer \_ OWF**    | Fournisseur de services de chiffrement qui prend en charge le remplacement de la manière dont les formats unidirectionnels sont générés à partir des mots de passe.<br/>                                                                                                                                                                                                                                                                  | 23    |
| **CAPICOM \_ Prov \_ RSA \_ AES**        | CSP qui prend en charge les signatures numériques et le chiffrement des données à l’aide de l’algorithme Advanced Encryption Standard ([*AES*](../secgloss/a-gly.md)).<br/>                                                                                                                                                                                       | 24    |



## <a name="remarks"></a>Remarques

L’énumération de **\_ \_ type de CAPICOM Proven** est utilisée par les propriétés et méthodes suivantes :

-   Propriété [**PrivateKey. ProviderType**](privatekey-providertype.md) .
-   Méthode [**PrivateKey. Open**](privatekey-open.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------------|--------------------------------------------------------------------------------------|
| Composant redistribuable<br/> | capicom 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP<br/>                |
| En-tête<br/>          | <dl> <dt>CAPICOM. h</dt> </dl> |



 

 
