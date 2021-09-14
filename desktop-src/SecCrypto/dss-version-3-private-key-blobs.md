---
description: Décrit le format d’une clé privée DSS version 3 exportée.
ms.assetid: 650532fd-919b-495a-9fb9-981790447d3d
title: Objets BLOB de clé privée DSS version 3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a6434e411ba3268901176a5c9739ceecfa79689
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127416475"
---
# <a name="dss-version-3-private-key-blobs"></a>Objets BLOB de clé privée DSS version 3

Quand une [*clé privée*](../secgloss/p-gly.md) [*DSS*](../secgloss/d-gly.md) de la version 3 est exportée, son format est le suivant :


```C++
BLOBHEADER        blobheader; 
DSSPRIVKEY_VER3   dssprivkeyver3;
BYTE p[dssprivkeyver3.bitlenP/8]; 
                    // Where P is the prime modulus
BYTE q[dssprivkeyver3.bitlenQ/8]; 
                    // Where Q is a large factor of P-1
BYTE g[dssprivkeyver3.bitlenP/8]; 
                    // Where G is the generator parameter
BYTE j[dssprivkeyver3.bitlenJ/8]; 
                    // Where J is (P-1)/Q
BYTE y[dssprivkeyver3.bitlenP/8]; 
                    // Where Y is (G^X) mod P
BYTE x[dssprivkeyver3.bitlenX/8]; 
                    // Where X is the private exponent
```



Ce format d' [*objet BLOB*](../secgloss/b-gly.md) est exporté lorsque l’indicateur de chiffrement \_ d’objets BLOB \_ VER3 est utilisé avec [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey). Étant donné que la version se trouve dans l’objet BLOB, il n’est pas nécessaire de spécifier un indicateur lors de l’utilisation de cet objet BLOB avec [**CryptImportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey).

Le tableau suivant décrit chaque composant de l' [*objet blob de clé*](../secgloss/k-gly.md).



| Champ          | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Blobheader     | Structure [**BLOBHEADER**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) . Le membre **bType** doit avoir la valeur PublicKeyBlob.                                                                                                                                                                                                                                                                                                                                                                                                                      |
| Dssprivkeyver3 | Structure **DSSPRIVKEY \_ VER3** . Le membre **magique** doit être défini sur « DSS4 » (0x34535344) pour les clés privées. Notez que la valeur hexadécimale est simplement un encodage [*ASCII*](../secgloss/a-gly.md) de « DSS4 ».<br/>                                                                                                                                                                                                                                                                     |
| P              | La valeur P est située directement après la structure **DSSPRIVKEY \_ VER3** , et doit toujours être la longueur, en octets, du champ **DSSPRIVKEY \_ VER3 BitlenP** (longueur binaire de P) divisé par huit (format [*Little-endian*](../secgloss/l-gly.md) ).                                                                                                                                                                                                                           |
| Q              | La valeur Q est située directement après la valeur P et doit toujours être la longueur, en octets, du champ **DSSPRIVKEY \_ VER3 bitlenQ** divisé par huit (format [*Little endian*](../secgloss/l-gly.md) ).                                                                                                                                                                                                                                                                     |
| G              | La valeur G est située juste après la valeur Q et doit toujours être la longueur, en octets, du champ **DSSPRIVKEY \_ VER3 bitlenP** (longueur de bit de P) divisé par huit. Si la longueur des données est un ou plusieurs octets plus courts que P divisés par 8, les données doivent être complétées par les octets nécessaires (de zéro valeur) pour que les données soient de la longueur souhaitée (format [*Little-endian*](../secgloss/l-gly.md) ).                                                                 |
| J              | La valeur J est située directement après la valeur G et doit toujours être la longueur, en octets, du champ **DSSPRIVKEY \_ VER3 bitlenJ** divisé par huit (format [*Little endian*](../secgloss/l-gly.md) ). Si la valeur bitlenJ est 0, la valeur est absente de l’objet BLOB.                                                                                                                                                                                                   |
| O              | La valeur Y, (G ^ X) mod P, est située directement après la valeur J et doit toujours être la longueur, en octets, du champ **DSSPRIVKEY \_ VER3 bitlenP** (longueur binaire de P) divisé par huit. Si la longueur des données résultant du calcul de (G ^ X) mod P est un ou plusieurs octets plus courts que P divisé par 8, les données doivent être complétées par les octets nécessaires (de zéro valeur) pour que les données soient de la longueur souhaitée (format [*Little endian*](../secgloss/l-gly.md) ). |
| X              | La valeur X est un entier aléatoire de grande taille, de sorte que la partie publique de la paire de clés DH, Y, est égale à : Y = (G ^ X) mod P<br/>                                                                                                                                                                                                                                                                                                                                                                                               |



 

Lors de l’appel de [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey), le développeur peut choisir de chiffrer ou non la clé. La clé est chiffrée si le paramètre *hExpKey* contient un handle valide pour une clé de session. Tout sauf la partie [**BLOBHEADER**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) de l’objet blob est chiffré. Notez que les paramètres d’algorithme de chiffrement et de clé de chiffrement ne sont pas stockés avec l' [*objet blob de clé privée*](../secgloss/p-gly.md). L’application doit gérer et stocker ces informations. Si la valeur zéro est passée pour *hExpKey*, la clé privée est exportée sans chiffrement.

> [!IMPORTANT]
> Il est dangereux d’exporter les clés privées sans chiffrement, car elles sont ensuite vulnérables à l’interception et à l’utilisation par des entités non autorisées.

 

 

 
