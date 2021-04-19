---
description: Diffie-Hellman objets BLOB de clé publique de la version 3 (type PUBLICKEYBLOB) sont utilisés pour exporter et importer des informations sur une clé publique DH.
ms.assetid: ba29a71a-7509-49c7-93d2-f0a699532706
title: Diffie-Hellman blob de clé publique de la version 3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df7228e4b4a786dc0eb25d1ba199b5c20923dd8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517071"
---
# <a name="diffie-hellman-version-3-public-key-blobs"></a>Diffie-Hellman blob de clé publique de la version 3

Diffie-Hellman [*objets BLOB de clé publique*](../secgloss/p-gly.md) de la version 3 (type PublicKeyBlob) sont utilisés pour exporter et importer des informations sur une clé publique DH. Ils ont le format suivant :


```C++
BLOBHEADER blobheader; 
                 // As explained under "Data Structures"
DHPUBKEY_VER3 dhpubkeyver3;
BYTE p[dhpubkeyver3.bitlenP/8]; 
                 // Where P is the prime modulus
BYTE q[dhpubkeyver3.bitlenQ/8]; 
                 // Where Q is a large factor of P-1
BYTE g[dhpubkeyver3.bitlenP/8]; 
                 // Where G is the generator parameter
BYTE j[dhpubkeyver3.bitlenJ/8]; 
                 // Where J is (P-1)/Q
BYTE y[dhpubkeyver3.bitlenP/8]; 
                 // Where Y is (G^X) mod P
```



Ce format d’objet BLOB est exporté lorsque l’indicateur de chiffrement \_ d’objets BLOB \_ VER3 est utilisé avec [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey). Étant donné que la version se trouve dans l’objet BLOB, il n’est pas nécessaire de spécifier un indicateur lors de l’utilisation de cet [*objet BLOB*](../secgloss/b-gly.md) avec [**CryptImportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey).

En outre, ce format d’objet BLOB est utilisé avec la fonction [**CryptSetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam) lorsque la valeur *dwParam* KP \_ pub \_ param est utilisée pour définir des paramètres de clé sur une clé DH. Cela se fait lorsque l' \_ indicateur de chiffrement PREGEN a été utilisé pour générer la clé. Lorsqu’elle est utilisée dans cette situation, la valeur y est ignorée et ne doit donc pas être incluse dans l’objet BLOB.

Le tableau suivant décrit chaque composant de l’objet BLOB de clé.



| Champ        | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| blobheader   | Structure [**BLOBHEADER**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) . Le membre **bType** doit avoir la valeur PublicKeyBlob.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| dhpubkeyver3 | Structure [**DHPUBKEY \_ VER3**](/windows/win32/api/wincrypt/ns-wincrypt-dhpubkey_ver3) . Le membre **magique** doit être défini sur 0x33484400 pour les clés publiques. Notez que la valeur hexadécimale est simplement un encodage [*ASCII*](../secgloss/a-gly.md) de « DH3 ».                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| P            | La valeur P est située directement après la [**structure DHPUBKEY \_ VER3**](/windows/win32/api/wincrypt/ns-wincrypt-dhpubkey_ver3) et doit toujours être la longueur, en octets, du champ **DHPUBKEY \_ VER3** **bitlenP** (longueur binaire de P) divisé par huit (format [*Little-endian*](../secgloss/l-gly.md) ).                                                                                                                                                                                                                                                                                                                                                                                           |
| Q            | La valeur Q est située directement après la valeur P et doit toujours être la longueur en octets du champ [**DHPUBKEY \_ VER3**](/windows/win32/api/wincrypt/ns-wincrypt-dhpubkey_ver3) **bitlenQ** divisé par huit (format [*Little endian*](../secgloss/l-gly.md) ). Si la valeur bitlenQ est 0, la valeur est absente de l’objet BLOB.                                                                                                                                                                                                                                                                                                                                                                 |
| G            | La valeur G est située juste après la valeur Q et doit toujours être la longueur, en octets, du champ [**DHPUBKEY \_ VER3**](/windows/win32/api/wincrypt/ns-wincrypt-dhpubkey_ver3) **bitlenP** (longueur de bit de P) divisé par huit. Si la longueur des données est un ou plusieurs octets plus courts que P divisés par 8, les données doivent être complétées par les octets nécessaires (de zéro valeur) pour que les données soient de la longueur souhaitée (format [*Little-endian*](../secgloss/l-gly.md) ).                                                                                                                                                                                                                              |
| J            | La valeur J est située directement après la valeur G et doit toujours être la longueur en octets du champ [**DHPUBKEY \_ VER3**](/windows/win32/api/wincrypt/ns-wincrypt-dhpubkey_ver3) **bitlenJ** divisé par huit (format [*Little endian*](../secgloss/l-gly.md) ). Si la valeur bitlenQ est 0, la valeur est absente de l’objet BLOB.                                                                                                                                                                                                                                                                                                                                                                 |
| O            | La valeur Y, (G ^ X) mod P, est située directement après la valeur J et doit toujours être la longueur, en octets, du champ [**DHPUBKEY \_ VER3**](/windows/win32/api/wincrypt/ns-wincrypt-dhpubkey_ver3) **bitlenP** (longueur binaire de P) divisé par huit. Si la longueur des données résultant du calcul de (G ^ X) mod P est un ou plusieurs octets plus courts que P divisé par 8, les données doivent être complétées par les octets nécessaires (de zéro valeur) pour que les données soient de la longueur souhaitée (format [*Little endian*](../secgloss/l-gly.md) ). Lorsque cette structure est utilisée avec [**CryptSetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam) avec la valeur *dwParam* KP \_ pub \_ param, cette valeur n’est pas incluse dans l’objet BLOB. |



 

> [!Note]  
> Les objets BLOB de clé publique ne sont pas chiffrés, mais contiennent des clés publiques sous forme de texte en clair.

 

 

 
