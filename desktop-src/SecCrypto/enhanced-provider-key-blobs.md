---
description: Le fournisseur de base, le fournisseur fort et le fournisseur amélioré utilisent les mêmes objets BLOB de clé.
ms.assetid: f1bd347b-33bd-40bc-9a9b-c06f264f1af4
title: Objets BLOB de clé de fournisseur améliorée
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1098ec45f73183f31cb91d15e2957dcc5964591bd8c6de4e30616df0808ade6b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119874439"
---
# <a name="enhanced-provider-key-blobs"></a>Objets BLOB de clé de fournisseur améliorée

Le fournisseur de base, le fournisseur fort et le fournisseur amélioré utilisent les mêmes [*objets BLOB de clé*](../secgloss/k-gly.md).

-   [Objets BLOB de clé publique](#public-key-blobs)
-   [Objets BLOB de clé privée](#private-key-blobs)
-   [Objets BLOB de clé simple](#simple-key-blobs)

## <a name="public-key-blobs"></a>Objets BLOB de clé publique

Les [*objets BLOB de clé publique*](../secgloss/p-gly.md), de type **publicKeyBlob**, sont utilisés pour stocker des [*clés publiques*](../secgloss/p-gly.md) en dehors d’un [*fournisseur de services de chiffrement*](../secgloss/c-gly.md) (CSP). Les objets BLOB de clé publique de fournisseur étendu ont le format suivant.

``` syntax
PUBLICKEYSTRUC  publickeystruc;
RSAPUBKEY rsapubkey;
BYTE modulus[rsapubkey.bitlen/8];
```

Le tableau suivant décrit chaque composant de clé publique. Toutes les valeurs sont au format [*Little endian*](../secgloss/l-gly.md) .



| Champ          | Description                                                                                                                                                                                                                                                                           |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| modulo        | Les données du modulo de la clé publique se trouvent directement après la structure [**RSAPUBKEY**](/windows/desktop/api/Wincrypt/ns-wincrypt-rsapubkey) . La taille de ces données varie en fonction de la taille de la clé publique. Le nombre d’octets peut être déterminé en divisant la valeur du champ **RSAPUBKEY bitlen** par huit. |
| publickeystruc | Structure [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) .                                                                                                                                                                                                                                 |
| rsapubkey      | Structure [**RSAPUBKEY**](/windows/desktop/api/Wincrypt/ns-wincrypt-rsapubkey) . Le membre **magique** doit être défini sur 0x31415352. Cette valeur hexadécimale est l’encodage [*ASCII*](../secgloss/a-gly.md) de RSA1.                                                                         |



 

> [!Note]  
> Les objets BLOB de clé publique ne sont pas chiffrés. Elles contiennent des clés publiques sous forme de [*texte en clair*](../secgloss/p-gly.md) .

 

## <a name="private-key-blobs"></a>Objets BLOB de clé privée

Les [*objets BLOB de clé privée*](../secgloss/p-gly.md), de type **PRIVATEKEYBLOB**, sont utilisés pour stocker des [*clés privées*](../secgloss/p-gly.md) en dehors d’un CSP. Les objets BLOB de clé privée du fournisseur étendu ont le format suivant.

``` syntax
PUBLICKEYSTRUC  publickeystruc;
RSAPUBKEY rsapubkey;
BYTE modulus[rsapubkey.bitlen/8];
BYTE prime1[rsapubkey.bitlen/16];
BYTE prime2[rsapubkey.bitlen/16];
BYTE exponent1[rsapubkey.bitlen/16];
BYTE exponent2[rsapubkey.bitlen/16];
BYTE coefficient[rsapubkey.bitlen/16];
BYTE privateExponent[rsapubkey.bitlen/8];
```

Le tableau suivant décrit le composant BLOB de clé privée.

> [!Note]  
> Ces champs correspondent aux champs décrits dans la section 7,2 des [*normes de chiffrement à clé publique*](../secgloss/p-gly.md) (PKCS) \# 1 avec des différences mineures.

 



| Champ           | Description                                                                                                                                                                                                   |
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| coefficient     | Coefficient. A la valeur numérique (inverse de q) mod p.                                                                                                                                                |
| exponent1       | Exposant 1. Il a une valeur numérique de d mod (p – 1).                                                                                                                                                        |
| exponent2       | Exposant 2. Il a une valeur numérique de d mod (q – 1).                                                                                                                                                        |
| Modulus         | Modulo. Il a la valeur *Prime1*×*Prime2* et est souvent appelé n.                                                                                                                                   |
| prime1          | Nombre premier 1, souvent appelé p.                                                                                                                                                                             |
| prime2          | Nombre premier 2, souvent appelé q.                                                                                                                                                                             |
| privateExponent | Exposant privé, souvent appelé d.                                                                                                                                                                           |
| publickeystruc  | Structure [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) .                                                                                                                                                         |
| rsapubkey       | Structure [**RSAPUBKEY**](/windows/desktop/api/Wincrypt/ns-wincrypt-rsapubkey) . Le membre **magique** doit être défini sur 0x32415352. Cette valeur hexadécimale est l’encodage [*ASCII*](../secgloss/a-gly.md) de RSA2. |



 

> [!Note]  
> Les objets BLOB de clé privée ne sont pas chiffrés. Elles contiennent des clés privées sous forme de texte en clair.

 

Lors de l’appel de [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey), le développeur peut choisir de chiffrer ou non la clé. Le **PRIVATEKEYBLOB** est chiffré si le paramètre *hExpKey* contient un handle valide pour une clé de session. Tout sauf la partie [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) de l’objet blob est chiffré.

> [!Note]  
> Les paramètres d’algorithme de chiffrement et de clé de chiffrement ne sont pas stockés avec l’objet BLOB de clé privée. L’application doit gérer et stocker ces informations. Si la valeur zéro est passée pour *hExpKey*, la clé privée est exportée sans chiffrement.

 

> [!Caution]  
> Il est dangereux d’exporter les clés privées sans chiffrement, car elles sont ensuite vulnérables à l’interception et à l’utilisation par des entités non autorisées.

 

## <a name="simple-key-blobs"></a>Objets BLOB de clé simple

Les [*objets BLOB de clé simple*](../secgloss/s-gly.md), de type **SIMPLEBLOB**, sont utilisés pour stocker et transporter des clés de session en dehors d’un CSP. Les objets BLOB de clé simple du fournisseur étendu sont toujours chiffrés avec une [*clé publique d’échange de clés*](../secgloss/k-gly.md). Le membre **pbData** du **SIMPLEBLOB** est une séquence d’octets au format suivant.

``` syntax
PUBLICKEYSTRUC  publickeystruc;
ALG_ID algid;
BYTE encryptedkey[rsapubkey.bitlen/8];
```

Le tableau suivant décrit chaque composant du membre **pbData** du **SIMPLEBLOB**.



| Champ          | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| algid          | Structure [**d' \_ ID ALG**](alg-id.md) qui spécifie l’algorithme de chiffrement utilisé pour chiffrer les données de la clé de session. Cela a généralement la valeur CALG \_ RSA \_ KEYX, qui indique que les données de la clé de session ont été chiffrées avec une clé publique d’échange de clés à l’aide de l' [*algorithme de clé publique RSA*](../secgloss/r-gly.md).                                                                                                                           |
| EncryptedKey   | Séquence d' **octets** qui représente les données de clé de session chiffrées sous la forme d’un \# bloc de chiffrement PKCS 1, type 2. Pour plus d’informations sur ce format de données, consultez les normes de chiffrement à clé publique (PKCS) \# 1, publiées par RSA Data Security, Inc. Ces données ont toujours la même taille que le modulo de la clé publique. Par exemple, les clés publiques générées par le fournisseur de base Microsoft RSA peuvent avoir une longueur de 512 bits (64 octets). par conséquent, les données de clé de session chiffrées sont également toujours 512 bits (64 octets).<br/> |
| publickeystruc | Structure [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) .                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |



 

Pour plus d’informations sur le fournisseur de base et les objets BLOB de clé du fournisseur étendu, consultez [objets BLOB de clé du fournisseur](base-provider-key-blobs.md).

 

 
