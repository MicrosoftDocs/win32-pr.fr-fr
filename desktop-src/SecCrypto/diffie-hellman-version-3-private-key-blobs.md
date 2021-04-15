---
description: Décrit le format d’un objet BLOB de clé privée Diffie-Hellman version 3 exporté.
ms.assetid: c759e6e1-f7af-4cd6-a67e-ff0da1e91eb1
title: Diffie-Hellman blob de clé privée de la version 3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb35a6db0cfd75d34ba30d26be816a64c1b04205
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484593"
---
# <a name="diffie-hellman-version-3-private-key-blobs"></a>Diffie-Hellman blob de clé privée de la version 3

Quand un objet blob de [*clé privée*](../secgloss/p-gly.md) de Diffie-Hellman version 3 est exporté, son format est le suivant :


```C++
BLOBHEADER        blobheader;
DHPRIVKEY_VER3   dhprivkeyver3;
BYTE p[dhprivkeyver3.bitlenP/8]; 
            // Where P is the prime modulus
BYTE q[dhprivkeyver3.bitlenQ/8]; 
            // Where Q is a large factor of P-1
BYTE g[dhprivkeyver3.bitlenP/8]; 
            // Where G is the generator parameter
BYTE j[dhprivkeyver3.bitlenJ/8]; 
            // Where J is (P-1)/Q
BYTE y[dhprivkeyver3.bitlenP/8]; 
            // Where Y is (G^X) mod P
BYTE x[dhprivkeyver3.bitlenX/8]; 
            // Where X is the private exponent
```



Ce format d' [*objet BLOB*](../secgloss/b-gly.md) est exporté lorsque l’indicateur de chiffrement \_ d’objets BLOB \_ VER3 est utilisé avec [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey). Étant donné que la version se trouve dans l’objet BLOB, il n’est pas nécessaire de spécifier un indicateur lors de l’utilisation de cet objet BLOB avec [**CryptImportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey).

Le tableau suivant décrit chaque composant de l' [*objet blob de clé*](../secgloss/k-gly.md).



| Champ         | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|---------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| blobheader    | Structure [**BLOBHEADER**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) .                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| dhprivkeyver3 | Structure [**DHPRIVKEY \_ VER3**](/windows/win32/api/wincrypt/ns-wincrypt-dhprivkey_ver3) . Le membre **magique** doit être défini sur 0x34484400 pour les clés privées. Notez que la valeur hexadécimale est simplement un encodage [*ASCII*](../secgloss/a-gly.md) de « DH4 ».                                                                                                                                                                                                                                                                                            |
| P             | La valeur P est située directement après la [**structure DHPRIVKEY \_ VER3**](/windows/win32/api/wincrypt/ns-wincrypt-dhprivkey_ver3) , et doit toujours être la longueur en octets du champ **DHPRIVKEY \_ VER3** **bitlenP** (longueur binaire de P) divisée par huit (format [*Little-endian*](../secgloss/l-gly.md) ).                                                                                                                                                                                                                            |
| Q             | La valeur Q est située directement après la valeur P et doit toujours être la longueur en octets du champ [**DHPRIVKEY \_ VER3**](/windows/win32/api/wincrypt/ns-wincrypt-dhprivkey_ver3) **bitlenQ** divisé par huit (format [*Little endian*](../secgloss/l-gly.md) ). Si la valeur bitlenQ est 0, la valeur est absente de l’objet BLOB.                                                                                                                                                                                                  |
| G             | La valeur G est située directement après la valeur Q et doit toujours être la longueur, en octets, du champ [**DHPRIVKEY \_ VER3**](/windows/win32/api/wincrypt/ns-wincrypt-dhprivkey_ver3) **bitlenP** (longueur binaire de P) divisé par huit. Si la longueur des données est un ou plusieurs octets plus courts que P divisés par 8, les données doivent être complétées par les octets nécessaires (de zéro valeur) pour que les données soient de la longueur souhaitée (format [*Little-endian*](../secgloss/l-gly.md) ).                                                                 |
| J             | La valeur J est située directement après la valeur G et doit toujours être la longueur en octets du champ [**DHPRIVKEY \_ VER3**](/windows/win32/api/wincrypt/ns-wincrypt-dhprivkey_ver3) **bitlenJ** divisé par huit (format [*Little endian*](../secgloss/l-gly.md) ). Si la valeur bitlenJ est 0, la valeur est absente de l’objet BLOB.                                                                                                                                                                                                  |
| O             | La valeur Y, (G ^ X) mod P, est située directement après la valeur J et doit toujours être la longueur, en octets, du champ [**DHPRIVKEY \_ VER3**](/windows/win32/api/wincrypt/ns-wincrypt-dhprivkey_ver3) **bitlenP** (longueur binaire de P) divisé par huit. Si la longueur des données résultant du calcul de (G ^ X) mod P est un ou plusieurs octets plus courts que P divisé par 8, les données doivent être complétées par les octets nécessaires (de zéro valeur) pour que les données soient de la longueur souhaitée (format [*Little endian*](../secgloss/l-gly.md) ). |
| X             | La valeur X est un entier aléatoire de grande taille, de sorte que la partie publique de la paire de clés DH, Y, est égale à : Y = (G ^ X) mod P<br/>                                                                                                                                                                                                                                                                                                                                                                                                                      |



 

Lors de l’appel de [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey), le développeur peut choisir de chiffrer ou non la clé. La clé est chiffrée si le paramètre *hExpKey* contient un handle valide pour une clé de session. Tout sauf la partie [**BLOBHEADER**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) de l’objet blob est chiffré. Notez que les paramètres d’algorithme de chiffrement et de clé de chiffrement ne sont pas stockés avec l' [*objet blob de clé privée*](../secgloss/p-gly.md). L’application doit gérer et stocker ces informations. Si la valeur zéro est passée pour *hExpKey*, la clé privée est exportée sans chiffrement.

> [!Note]  
> Il est dangereux d’exporter les clés privées sans chiffrement, car elles sont ensuite vulnérables à l’interception et à l’utilisation par des entités non autorisées.

 

 

 
