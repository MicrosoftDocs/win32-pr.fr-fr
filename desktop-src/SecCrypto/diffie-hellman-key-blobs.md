---
description: Les objets BLOB sont utilisés avec le fournisseur Diffie-Hellman pour exporter des clés et importer des clés dans, le fournisseur de services de chiffrement (CSP).
ms.assetid: 052f2108-d402-41a0-b4ac-e93ba6b06b49
title: Objets BLOB de clé de Diffie-Hellman
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9194a9c12542fc0acf36aa0064a2f3e304e25f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106543500"
---
# <a name="diffie-hellman-key-blobs"></a>Objets BLOB de clé de Diffie-Hellman

Les [*objets BLOB*](../secgloss/b-gly.md) sont utilisés avec le fournisseur [*Diffie-Hellman*](../secgloss/d-gly.md) pour exporter des clés et importer des clés dans, le [*fournisseur de services de chiffrement*](../secgloss/c-gly.md) (CSP).

-   [Objets BLOB de clé publique](#public-key-blobs)
-   [Objets BLOB de clé privée](#private-key-blobs)

## <a name="public-key-blobs"></a>Objets BLOB de clé publique

Diffie-Hellman [*objets BLOB de clé publique*](../secgloss/p-gly.md), de type **publicKeyBlob**, sont utilisés pour échanger la valeur (G ^ X) mod P dans un échange de clés Diffie-Hellman. Ces clés sont exportées et importées sous la forme d’une séquence d’octets au format suivant.

``` syntax
PUBLICKEYSTRUC  publickeystruc; 
DHPUBKEY dhpubkey;
BYTE y[dhpubkey.bitlen/8]; // Where y = (G^X) mod P
```

Le tableau suivant décrit chaque composant de l' [*objet blob de clé*](../secgloss/k-gly.md).



| Champ          | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| dhpubkey       | Structure [**DHPUBKEY**](/windows/win32/api/wincrypt/ns-wincrypt-dhpubkey) . Le membre **magique** doit être défini sur 0x31484400. Cette valeur hexadécimale est l’encodage [*ASCII*](../secgloss/a-gly.md) de « DH1 ».                                                                                                                                                                                                                                                                                                                                                                 |
| publickeystruc | Structure [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) .                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| y              | Séquence d' **octets** . La valeur Y, (G ^ X) mod P, est située directement après la structure [**DHPUBKEY**](/windows/win32/api/wincrypt/ns-wincrypt-dhpubkey) et doit toujours être la longueur, en octets, du champ **DHPUBKEY bitlen** (longueur binaire de P) divisé par huit. Si la longueur des données résultant du calcul de (G ^ X) mod P est un ou plusieurs octets plus courts que P divisés par huit, les données doivent être complétées par les octets nécessaires (de zéro valeur) pour que les données soient de la longueur souhaitée (format [*Little endian*](../secgloss/l-gly.md) ). |



 

## <a name="private-key-blobs"></a>Objets BLOB de clé privée

Diffie-Hellman [*objets BLOB de clé privée*](../secgloss/p-gly.md), tapez **PRIVATEKEYBLOB**, sont utilisés pour stocker les informations publiques/privées d’une clé de Diffie-Hellman. Ces clés sont exportées et importées sous la forme d’une séquence d’octets au format suivant.

``` syntax
PUBLICKEYSTRUC  publickeystruc; 
DHPUBKEY        dhpubkey;
BYTE            prime[dhpubkey.bitlen/8];
BYTE            generator[dhpubkey.bitlen/8];
BYTE            secret[dhpubkey.bitlen/8];
```

Le tableau suivant décrit chaque composant de l’objet BLOB de clé.



| Champ          | Description                                                                                                                                                                                                  |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| dhpubkey       | Structure [**DHPUBKEY**](/windows/win32/api/wincrypt/ns-wincrypt-dhpubkey) . Le membre **magique** doit être défini sur 0x32484400. Cette valeur hexadécimale est l’encodage [*ASCII*](../secgloss/a-gly.md) de « DH2 ». |
| générateur      | Séquence d' **octets** . Générateur, G.                                                                                                                                                                       |
| publickeystruc | Structure [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) .                                                                                                                                                        |
| candidat          | Séquence d' **octets** . Le modulo principal, P. Ces données doivent toujours avoir le bit le plus significatif de l’octet le plus significatif défini sur un.                                                                      |
| secret         | Séquence d' **octets** . Exposant secret, X.                                                                                                                                                                 |



 

> [!Note]  
> Le générateur et le secret doivent toujours avoir la même longueur, en octets. Si l’un ou l’autre octet est plus petit que l’autre, il doit être complété avec le nombre d’octets de zéro valeur nécessaire pour les rendre identiques. Le générateur et le secret sont au format [*Little endian*](../secgloss/l-gly.md) .

 

 

 
