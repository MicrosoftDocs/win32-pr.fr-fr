---
description: Les objets BLOB sont utilisés avec le fournisseur Diffie-Hellman/Schannel pour exporter des clés et importer des clés dans, le fournisseur de services de chiffrement (CSP).
ms.assetid: ebb85b7c-204d-4b1c-86dc-5a03c8eda47b
title: Objets BLOB de clé Diffie-Hellman/Schannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03c653e26f53611e8b00a1dae4e49df7084e6dc655d67f11550a430860fab12d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117767693"
---
# <a name="diffie-hellmanschannel-key-blobs"></a>Objets BLOB de clé Diffie-Hellman/Schannel

Les [*objets BLOB*](../secgloss/b-gly.md) sont utilisés avec le fournisseur Schannel [*Diffie-Hellman*](../secgloss/d-gly.md) / [](../secgloss/s-gly.md) pour exporter des clés et importer des clés dans, le [*fournisseur de services de chiffrement*](../secgloss/c-gly.md) (CSP).

-   [Objets BLOB de clé publique](#public-key-blobs)
-   [Objets BLOB de clé privée](#private-key-blobs)

## <a name="public-key-blobs"></a>Objets BLOB de clé publique

Diffie-Hellman [*objets BLOB de clé publique*](../secgloss/p-gly.md), de type **publicKeyBlob**, sont utilisés pour échanger la valeur (G ^ X) mod P dans un échange de clés Diffie-Hellman. Ces clés sont exportées et importées sous la forme d’une séquence d’octets au format suivant.

``` syntax
PUBLICKEYSTRUC  publickeystruc;
DHPUBKEY        dhpubkey;
BYTE            y[dhpubkey.bitlen/8]; // Where y = (G^X) mod P
```

Le tableau suivant décrit chaque composant de l' [*objet blob de clé*](../secgloss/k-gly.md).



| Champ          | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| dhpubkey       | Structure [**DHPUBKEY**](/windows/win32/api/wincrypt/ns-wincrypt-dhpubkey) . Le membre **magique** doit être défini sur 0x31484400. Cette valeur hexadécimale est l’encodage [*ASCII*](../secgloss/a-gly.md) de DH1.                                                                                                                                                                                                                                                                                                                                                      |
| publickeystruc | Structure [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) .                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| y              | Séquence d' **octets** . La valeur y, (G ^ X) mod P, est située directement après la structure [**DHPUBKEY**](/windows/win32/api/wincrypt/ns-wincrypt-dhpubkey) . La longueur, en octets, de la séquence est le membre **bitlen** de **DHPUBKEY** divisé par huit. Si la longueur des données résultant du calcul de (G ^ X) mod P est un ou plusieurs octets plus courts que P divisés par huit, les données doivent être complétées par les octets nécessaires (de zéro valeur) pour que les données soient de la longueur souhaitée (format [*Little endian*](../secgloss/l-gly.md) ). |



 

## <a name="private-key-blobs"></a>Objets BLOB de clé privée

Les [*objets BLOB de clé privée*](../secgloss/p-gly.md)D-h, de type **PRIVATEKEYBLOB**, sont utilisés pour exporter et importer des informations privées d’une clé D-H. Ces clés sont exportées et importées sous la forme d’une séquence d’octets au format suivant.

``` syntax
PUBLICKEYSTRUC  publickeystruc;
DHPUBKEY        dhpubkey;
BYTE            prime[dhpubkey.bitlen/8];
BYTE            generator[dhpubkey.bitlen/8];
BYTE            secret[dhpubkey.bitlen/8];
```

Le tableau suivant décrit chaque composant de l’objet BLOB de clé.



| Champ          | Description                                                                                                                                                                                                |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| dhpubkey       | Structure [**DHPUBKEY**](/windows/win32/api/wincrypt/ns-wincrypt-dhpubkey) . Le membre **magique** doit être défini sur 0x32484400. Cette valeur hexadécimale est l’encodage [*ASCII*](../secgloss/a-gly.md) de DH2. |
| générateur      | Séquence d' **octets** . Générateur G.                                                                                                                                                                      |
| publickeystruc | Structure [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) .                                                                                                                                                      |
| candidat          | Séquence d' **octets** . Le modulo principal, P. Ces données doivent toujours avoir le bit le plus significatif de l’octet le plus significatif défini sur un.                                                                    |
| secret         | Séquence d' **octets** . Exposant X secret.                                                                                                                                                                |



 

> [!Note]  
> Les valeurs prime, générateur et secret doivent toujours avoir la même longueur, en octets. Si une valeur est d’un octet ou plus, elle doit être complétée avec le nombre de zéro octet nécessaire pour les rendre identiques. Le premier, le générateur et le secret sont au format [*Little endian*](../secgloss/l-gly.md) .

 

 

 
