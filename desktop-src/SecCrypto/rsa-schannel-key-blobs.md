---
description: Les objets BLOB sont utilisés avec le fournisseur RSA/SChannel pour exporter des clés et importer des clés dans, le fournisseur de services de chiffrement (CSP).
ms.assetid: 97d5ee6d-4687-4cd2-b122-36f8ea3c93ca
title: Objets BLOB de clé RSA/Schannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3be8bfa8b87ee901317e220583ff7b08ea110e342a2d9dd9abb477053ffdf05c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118900534"
---
# <a name="rsaschannel-key-blobs"></a>Objets BLOB de clé RSA/Schannel

Les [*objets BLOB*](../secgloss/b-gly.md) sont utilisés avec le fournisseur [*RSA*](../secgloss/r-gly.md) / [*Schannel*](../secgloss/s-gly.md) pour exporter les clés et importer les clés dans, le [*fournisseur de services de chiffrement*](../secgloss/c-gly.md) (CSP).

-   [Objets BLOB de clé publique](#public-key-blobs)
-   [Objets BLOB de clé privée](#private-key-blobs)
-   [Objets BLOB de clé simple](#simple-key-blobs)

## <a name="public-key-blobs"></a>Objets BLOB de clé publique

Les [*objets BLOB de clé publique*](../secgloss/p-gly.md), de type **publicKeyBlob**, sont utilisés pour stocker les [*clés publiques*](../secgloss/p-gly.md). Ces clés sont exportées et importées sous la forme d’une séquence d’octets au format suivant.

``` syntax
PUBLICKEYSTRUC  publickeystruc ;
RSAPUBKEY       rsapubkey;
BYTE            modulus[rsapubkey.bitlen/8];
```

Le tableau suivant décrit chaque composant de clé publique. Toutes les valeurs sont au format [*Little endian*](../secgloss/l-gly.md) .



| Champ          | Description                                                                                                                                                                                                                                                                                        |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| modulo        | Séquence d' **octets** . Les données du modulo de la clé publique se trouvent directement après la structure **RSAPUBKEY** . La longueur de ces données varie en fonction de la longueur de la clé publique. Le nombre d’octets peut être déterminé en divisant la valeur du membre **bitlen** de **RSAPUBKEY** par huit. |
| publickeystruc | Structure [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) .                                                                                                                                                                                                                                              |
| rsapubkey      | Structure [**RSAPUBKEY**](/windows/desktop/api/Wincrypt/ns-wincrypt-rsapubkey) . Le membre **magique** doit être défini sur 0x31415352. Cette valeur hexadécimale est l’encodage [*ASCII*](../secgloss/a-gly.md) de RSA1.                                                                                      |



 

> [!Note]  
> Les objets BLOB de clé publique ne sont pas chiffrés. Elles contiennent des clés publiques sous forme de [*texte en clair*](../secgloss/p-gly.md) .

 

## <a name="private-key-blobs"></a>Objets BLOB de clé privée

Les [*objets BLOB de clé privée*](../secgloss/p-gly.md), de type **PRIVATEKEYBLOB**, sont utilisés pour stocker les [*paires de clés publique/privée*](../secgloss/p-gly.md). Ces clés sont exportées et importées sous la forme d’une séquence d’octets au format suivant.

``` syntax
PUBLICKEYSTRUC  publickeystruc ;
RSAPUBKEY       rsapubkey;
BYTE            modulus[rsapubkey.bitlen/8];
BYTE            prime1[rsapubkey.bitlen/16];
BYTE            prime2[rsapubkey.bitlen/16];
BYTE            exponent1[rsapubkey.bitlen/16];
BYTE            exponent2[rsapubkey.bitlen/16];
BYTE            coefficient[rsapubkey.bitlen/16];
BYTE            privateExponent[rsapubkey.bitlen/8];
```

Si l' [*objet blob de clé*](../secgloss/k-gly.md) est chiffré, tout sauf la partie [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) de l’objet blob est chiffré.

> [!Note]  
> Les paramètres d’algorithme de chiffrement et de clé de chiffrement ne sont pas stockés avec l’objet BLOB de clé privée. Il incombe à l’application de gérer ces informations.

 

Le tableau suivant décrit chaque composant BLOB de clé privée.

> [!Note]  
> Ces champs correspondent aux champs décrits dans la section 7,2 des [*normes de chiffrement à clé publique*](../secgloss/p-gly.md) (PKCS) \# 1 avec des différences mineures.

 



| Champ           | Description                                                                                                                                                                                                   |
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| exponent1       | Séquence d' **octets** . Premier exposant. Il a une valeur numérique de d mod (p – 1).                                                                                                                           |
| exponent2       | Séquence d' **octets** . Deuxième exposant. Il a une valeur numérique de d mod (q – 1).                                                                                                                          |
| coefficient     | Séquence d' **octets** . Coefficient. A la valeur numérique (inverse de q) mod p.                                                                                                                           |
| Modulus         | Séquence d' **octets** . Modulo. A une chaîne qui contient *Prime1* \* *Prime2*. Il est souvent appelé n.                                                                                               |
| prime1          | Séquence d' **octets** . Nombre premier 1, souvent appelé p.                                                                                                                                                        |
| prime2          | Séquence d' **octets** . Nombre premier 2, souvent appelé q.                                                                                                                                                        |
| publickeystruc  | Structure [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) .                                                                                                                                                         |
| privateExponent | Séquence d' **octets** . Exposant privé, souvent appelé d.                                                                                                                                                  |
| rsapubkey       | Structure [**RSAPUBKEY**](/windows/desktop/api/Wincrypt/ns-wincrypt-rsapubkey) . Le membre **magique** doit être défini sur 0x32415352. Cette valeur hexadécimale est l’encodage [*ASCII*](../secgloss/a-gly.md) de RSA2. |



 

> [!Note]  
> Les objets BLOB de clé privée ne sont pas chiffrés. Elles contiennent des clés privées sous forme de texte en clair.

 

Lors de l’appel de [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey), le développeur peut choisir de chiffrer ou non la clé. Le **PRIVATEKEYBLOB** est chiffré si le paramètre *hExpKey* contient un handle valide pour une clé de session. Tout sauf la partie [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) de l’objet blob est chiffré.

> [!Note]  
> Les paramètres d’algorithme de chiffrement et de clé de chiffrement ne sont pas stockés avec l’objet BLOB de clé privée. L’application doit gérer et stocker ces informations. Si la valeur zéro est passée pour *hExpKey*, la clé privée est exportée sans chiffrement.

 

> [!Caution]  
> Il est dangereux d’exporter les clés privées sans chiffrement, car elles sont ensuite vulnérables à l’interception et à l’utilisation par des entités non autorisées.

 

## <a name="simple-key-blobs"></a>Objets BLOB de clé simple

Les [*objets BLOB de clé simple*](../secgloss/s-gly.md), de type **SIMPLEBLOB**, sont utilisés pour stocker et transporter des clés de session. Ils sont toujours chiffrés avec une [*clé publique d’échange de clés*](../secgloss/k-gly.md). Ces clés sont exportées et importées sous la forme d’une séquence d’octets au format suivant.

``` syntax
PUBLICKEYSTRUC  publickeystruc ;
ALG_ID          algid;
BYTE            encryptedkey[rsapubkey.bitlen/8];
```

Le tableau suivant décrit chaque composant d’objet BLOB simple.



| Champ          | Description                                                                                                                                                                                                                                                                                                                   |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| algid          | Structure [**d' \_ ID ALG**](alg-id.md) . Cela spécifie généralement l' \_ \_ algorithme RSA KEYX CALG, qui indique que les données de la clé de session ont été chiffrées avec une clé publique d’échange de clés, à l’aide de l' [*algorithme de clé publique RSA*](../secgloss/r-gly.md). |
| EncryptedKey   | Séquence d' **octets** . Les données de la clé de session chiffrée se présente sous la forme d’un \# bloc de chiffrement PKCS 1, type 2. Pour plus d’informations sur ce format de données, consultez les normes de chiffrement à clé publique (PKCS), publiées par RSA Data Security, Inc.                                                                                     |
| publickeystruc | Structure [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) .                                                                                                                                                                                                                                                                         |



 

Ces données ont toujours la même taille que le modulo de la clé publique. Par exemple, les clés publiques générées par le fournisseur de services de chiffrement de base Microsoft ont toujours une longueur de 512 bits (64 octets). par conséquent, les données de la clé de session chiffrée sont également toujours de 64 octets.

 

 
