---
description: Comment générer, récupérer et exporter des clés RSA/Schannel.
ms.assetid: 3069232f-d016-4973-ae39-89b0e2a03cd7
title: Clés RSA/Schannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: edc134557bcac9f38f204ebb70a3c55a7b3e1be476ef2c4d767dd216701bcd25
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117974783"
---
# <a name="rsaschannel-keys"></a>Clés RSA/Schannel

## <a name="generating-and-retrieving-rsaschannel-keys"></a>Génération et récupération des clés RSA/Schannel

[*RSA*](../secgloss/r-gly.md) / Les clés [*Schannel*](../secgloss/s-gly.md) peuvent être générées en appelant la fonction [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) . L’appel à **CryptGenKey** nécessite un \_ identificateur d’algorithme at KeyExchange passé dans le paramètre *algid* .

**Pour générer une paire de clés publique/privée RSA/Schannel**

1.  Appelez la fonction [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) pour obtenir un descripteur du [fournisseur de services de chiffrement Microsoft RSA/SChannel](microsoft-rsa-schannel-cryptographic-provider.md).
2.  Appelez la fonction [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) pour générer les clés. La \_ valeur de KeyExchange doit être transmise pour le paramètre *algid* , et les 16 bits supérieurs du paramètre *dwFlags* doivent avoir la taille de clé souhaitée (512 bits). Un handle de structure [**HCRYPTKEY**](hcryptkey.md) est retourné dans le paramètre *HKEY* .

**Pour récupérer un pointeur vers des clés d’utilisateur RSA/SChannel générées précédemment**

1.  Appelez la fonction [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) pour obtenir un descripteur du [fournisseur de services de chiffrement Microsoft RSA/SChannel](microsoft-rsa-schannel-cryptographic-provider.md).
2.  Appelez la fonction [**CryptGetUserKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetuserkey) , avec le paramètre *dwKeySpec* défini sur \_ KeyExchange.

## <a name="exporting-rsaschannel-keys"></a>Exportation des clés RSA/Schannel

Les [*clés principales*](../secgloss/m-gly.md) peuvent être exportées dans des structures blob de clé simple. Cela doit être implémenté de la même façon que l’exportation de [*clés de chiffrement en bloc*](../secgloss/b-gly.md) [*RC4*](../secgloss/r-gly.md) ou [*Data Encryption Standard*](../secgloss/d-gly.md) (des) normales, comme décrit dans [simple blob de clé](https://www.bing.com/search?q=Simple+Key+BLOB). Le membre **aiKeyAlg** de la structure [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) est défini sur l’identificateur d’algorithme de la clé principale (CALG \_ PCT1 \_ maître, CALG \_ SSL2 \_ Master, CALG \_ SSL3 \_ maître ou CALG \_ TLS1 \_ Master).

Si la fonction [**CPExportKey**](https://www.bing.com/search?q=**CPExportKey**) exporte une clé principale SSL2 et que l' \_ indicateur de secours crypt SSL2 \_ est défini, afin d’éviter les attaques par restauration de version, définissez les huit premiers octets du [*remplissage*](../secgloss/p-gly.md) du bloc de chiffrement sur 0x03 et non sur les données aléatoires.

Si la **constante \_ DESTROYKEY** de chiffrement est spécifiée dans le paramètre *DwFlags* de la fonction [**CPExportKey**](https://www.bing.com/search?q=**CPExportKey**) , le CSP détruit la clé ou le handle de clé après l’exportation de la clé. Cet indicateur est destiné à être utilisé uniquement avec des [*objets BLOB opaques*](../secgloss/o-gly.md).

 

 
