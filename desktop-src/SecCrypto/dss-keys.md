---
description: Explique comment générer, récupérer, vérifier et exporter des clés et des signatures DSS.
ms.assetid: d28fe531-af4b-4b5e-ab67-47ef70f8fa5b
title: Clés DSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f6ab8adcc4d551c4196e99ce48f5afdd380dc3a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515830"
---
# <a name="dss-keys"></a>Clés DSS

-   [Génération et récupération des clés DSS](#generating-and-retrieving-dss-keys)
-   [Génération de signatures DSS](#generating-dss-signatures)
-   [Vérification d’une signature DSS](#verifying-a-dss-signature)
-   [Exportation des clés DSS](#exporting-dss-keys)

## <a name="generating-and-retrieving-dss-keys"></a>Génération et récupération des clés DSS

Les clés DSS peuvent être générées par un appel à la fonction [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) . L’appel à **CryptGenKey** requiert que soit au niveau de la signature, soit le \_ \_ signe CALG DSS \_ soit passé dans l’argument *algid* . Cet appel va générer les valeurs P (premier module), Q (prime), G (générateur), X (exposant secret) et Y (clé publique) à partir de zéro et les conserver dans un [*objet blob de clé*](../secgloss/k-gly.md) dans un stockage local.

**Pour générer une paire de clés de signature DSS**

1.  Appelez la fonction [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) pour obtenir un handle pour le fournisseur de services de chiffrement DSS Microsoft.
2.  Appelez [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) pour générer les clés. Au niveau de la \_ signature ou \_ du CALG DSS \_ doit être transmis pour l’argument *algid* et les 16 bits supérieurs de l’argument *dwFlags* doivent être définis sur la taille de clé souhaitée. Si les 16 bits supérieurs sont nuls, la taille de clé par défaut de 1 024 bits est utilisée. Un descripteur [**HCRYPTKEY**](hcryptkey.md) est retourné dans l’argument *HKEY* .

**Pour récupérer un pointeur vers des clés de signature précédemment générées**

1.  Appelez [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) pour obtenir un descripteur du fournisseur de services de chiffrement DSS Microsoft.
2.  Appelez la fonction [**CryptGetUserKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetuserkey) avec l’argument *dwKeySpec* défini sur \_ signature ou sur signe CALG \_ DSS \_ .

**Pour récupérer les valeurs P, Q et G**

1.  Appelez [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) pour obtenir un descripteur du fournisseur de services de chiffrement DSS Microsoft.
2.  Appelez [**CryptGetUserKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetuserkey) avec l’argument *dwKeySpec* défini sur la \_ signature ou le signe CALG \_ DSS \_ .
3.  Appelez [**CryptGetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetkeyparam) avec l’argument *HKEY* défini sur le pointeur récupéré à l’étape précédente. L’argument *dwParam* doit être défini sur l’indicateur souhaité. KP \_ P, KP \_ Q ou KP \_ G. La valeur est retournée dans l’argument *pbData* , et la longueur des données est retournée dans l’argument *pdwDataLen* . La valeur est retournée sans informations d’en-tête et au format avec [*primauté des octets de poids faible*](../secgloss/l-gly.md) .

## <a name="generating-dss-signatures"></a>Génération de signatures DSS

Les données à signer doivent d’abord être [*hachées*](../secgloss/h-gly.md) à l’aide de l’algorithme [*SHA*](../secgloss/s-gly.md) . Une fois que ces données ont été hachées, une signature [*DSS*](../secgloss/d-gly.md) est générée en appelant la fonction [**CryptSignHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsignhasha) .

**Pour générer une signature DSS**

1.  Appelez [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) pour obtenir un descripteur du fournisseur de services de chiffrement DSS Microsoft.
2.  Appelez [**CryptCreateHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash) avec l’argument *ALGID* défini sur CALG \_ SHA pour obtenir un handle vers un objet de hachage SHA.
3.  Appelez [**CryptHashData**](/windows/desktop/api/Wincrypt/nf-wincrypt-crypthashdata) avec l’argument *hHash* défini sur le handle récupéré à l’étape précédente. Cela crée un hachage des données et retourne un descripteur au hachage dans l’argument *phHash* de l’appel de fonction [**CryptCreateHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash) .
4.  Appelez [**CryptSignHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsignhasha) avec l’argument *hHash* défini sur le handle récupéré à l’étape précédente. Au niveau de \_ la signature ou \_ du CALG DSS, \_ le signe peut être transmis dans le paramètre *dwKeySpec* . La signature est retournée à l’adresse fournie dans l’argument *pbSignature* , et la longueur de la signature est retournée à l’adresse fournie dans l’argument *pdwSigLen* . Un pointeur **null** peut être passé dans l’argument *pbSignature* et, dans ce cas, la signature n’est pas générée, mais la longueur de la signature est retournée à l’adresse fournie dans le paramètre *pdwSigLen* .

## <a name="verifying-a-dss-signature"></a>Vérification d’une signature DSS

Pour vérifier une signature DSS, la clé publique DSS du signataire doit être importée, les [*données signées*](../secgloss/s-gly.md) doivent être hachées, puis la signature peut être vérifiée.

**Pour vérifier une signature DSS**

1.  Appelez [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) pour obtenir un descripteur du fournisseur de services de chiffrement DSS Microsoft.
2.  Appelez [**CryptImportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey) pour importer la clé publique DSS du signataire.
3.  Appelez [**CryptCreateHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash) avec l’argument *ALGID* défini sur CALG \_ SHA pour obtenir un handle vers un objet de hachage SHA.
4.  Appelez [**CryptHashData**](/windows/desktop/api/Wincrypt/nf-wincrypt-crypthashdata) avec l’argument *hHash* défini sur le handle récupéré à l’étape précédente et avec *pbData* pointant vers les données signées. Cela crée un hachage des données et retourne un descripteur au hachage dans l’argument *phHash* de l’appel de fonction [**CryptCreateHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash) .
5.  Appelez [**CryptVerifySignature**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptverifysignaturea) avec les paramètres suivants :

    *hHash* est défini sur le descripteur du hachage effectué à l’étape précédente.

    *pbSignature* pointe vers la signature à vérifier.

    *dwSigLen* est défini sur la longueur de la signature.

    *hPubKey* est défini sur le descripteur de la clé publique importée à l’étape 2.

    *dwFlags* a la valeur zéro.

## <a name="exporting-dss-keys"></a>Exportation des clés DSS

Lorsque vous envoyez des [*données signées*](../secgloss/s-gly.md) à une personne où la signature doit être vérifiée par le destinataire, la clé publique du signataire doit être fournie au destinataire et est généralement envoyée avec les données signées. Par conséquent, il est nécessaire de pouvoir exporter les clés [*DSS*](../secgloss/d-gly.md) dans un format [*blob de clé*](../secgloss/k-gly.md) .

**Pour exporter la clé publique DSS**

1.  Appelez [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) pour obtenir un descripteur du fournisseur de services de chiffrement DSS Microsoft.
2.  Appelez [**CryptGetUserKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetuserkey) avec l’argument *dwKeySpec* défini sur la \_ signature ou le signe CALG \_ DSS \_ .
3.  Appelez [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) avec *HKEY* défini sur le handle récupéré à l’étape précédente, *DwBlobType* défini sur PublicKeyBlob et *dwFlags* défini sur zéro. L' [*objet blob de clé publique*](../secgloss/p-gly.md) DSS est retourné dans *pbData*, et la longueur de l' [*objet blob de clé*](../secgloss/k-gly.md) est retournée dans *pdwDataLen*. Un pointeur **null** peut être passé dans *pbData* et, dans ce cas, seule la longueur de l’objet blob de clé DSS sera retournée. L’objet BLOB retourné lors de l’appel à **CryptExportKey** est au format décrit dans [objets BLOB de clé du fournisseur DSS](dss-provider-key-blobs.md).

**Pour exporter la clé privée DSS**

-   Suivez la même procédure que pour l’exportation d’une clé publique DSS, sauf que lorsque vous effectuez l’appel à [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey), *dwBlobType* est défini sur PRIVATEKEYBLOB. L’objet BLOB retourné lors de l’appel à **CryptExportKey** est au format décrit dans [objets BLOB de clé du fournisseur DSS](dss-provider-key-blobs.md).

 

 
