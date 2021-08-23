---
description: Les objets BLOB de clé publique DSS version 3 de type PUBLICKEYBLOB permettent d’exporter et d’importer des informations sur une clé publique DH.
ms.assetid: 9aac1d61-8b61-4f0f-b037-afe4a60302de
title: Objets BLOB de clé publique DSS version 3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5cc4894000f284dfd5d1b1dd9e9a7353e4eee0b09a42edc63de76e8eaa93184
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119875259"
---
# <a name="dss-version-3-public-key-blobs"></a>Objets BLOB de clé publique DSS version 3

Les [*objets BLOB de clé publique*](../secgloss/p-gly.md) DSS version 3 de type PublicKeyBlob permettent d’exporter et d’importer des informations sur une clé publique DH. Ils ont le format suivant :


```C++
BLOBHEADER blobheader; 
        // As explained under "Data Structures"
DSSPUBKEY_VER3 dsspubkeyver3;
BYTE p[dsspubkeyver3.bitlenP/8]; 
       // Where P is the prime modulus
BYTE q[dsspubkeyver3.bitlenQ/8]; 
       // Where Q is a large factor of P-1
BYTE g[dsspubkeyver3.bitlenP/8]; 
       // Where G is the generator parameter
BYTE j[dsspubkeyver3.bitlenJ/8]; 
       // Where J is (P-1)/Q
BYTE y[dsspubkeyver3.bitlenP/8]; 
       // Where Y is (G^X) mod P
```



Ce format d' [*objet BLOB*](../secgloss/b-gly.md) est exporté lorsque l’indicateur de chiffrement \_ d’objets BLOB \_ VER3 est utilisé avec [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey). Étant donné que la version se trouve dans l’objet BLOB, il n’est pas nécessaire de spécifier un indicateur lors de l’utilisation de cet objet BLOB avec [**CryptImportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey).

En outre, ce format d’objet BLOB est utilisé avec la fonction [**CryptSetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam) lorsque la valeur *dwParam* KP \_ pub \_ param est utilisée pour définir des paramètres de clé sur une clé DSS. Cela se fait lorsque l' \_ indicateur de chiffrement PREGEN a été utilisé pour générer la clé. Lorsqu’elle est utilisée dans cette situation, la valeur y est ignorée et ne doit donc pas être incluse dans l’objet BLOB.

Le tableau suivant décrit chaque composant de l’objet BLOB de clé.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Champ</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Blobheader</td>
<td>Structure <a href="/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc"><strong>BLOBHEADER</strong></a> . Le membre <strong>bType</strong> doit avoir la valeur PublicKeyBlob.</td>
</tr>
<tr class="even">
<td>Dsspubkeyver3</td>
<td>Structure <a href="/previous-versions/windows/desktop/legacy/aa381983(v=vs.85)"><strong>DSSPUBKEY_VER3</strong></a> . Le membre <strong>magique</strong> doit être défini sur &quot; DSS3 &quot; (0x33535344) pour les clés publiques. Notez que la valeur hexadécimale est simplement un encodage <a href="/windows/desktop/SecGloss/a-gly"><em>ASCII</em></a> de &quot; DSS3.&quot;<br/></td>
</tr>
<tr class="odd">
<td>P</td>
<td>La valeur P est située directement après la structure <a href="/previous-versions/windows/desktop/legacy/aa381983(v=vs.85)"><strong>DSSPUBKEY_VER3</strong></a> , et doit toujours être la longueur, en octets, du champ <strong>bitlenP</strong> DSSPUBKEY_VER3 (longueur binaire de P) divisé par huit (format<a href="/windows/desktop/SecGloss/l-gly"><em>Little-endian</em></a> ).</td>
</tr>
<tr class="even">
<td>Q</td>
<td>La valeur Q est située directement après la valeur P et doit toujours être la longueur en octets du membre <a href="/previous-versions/windows/desktop/legacy/aa381983(v=vs.85)"><strong>DSSPUBKEY_VER3</strong></a><strong>bitlenQ</strong> divisé par huit (format<a href="/windows/desktop/SecGloss/l-gly"><em>Little endian</em></a> ).</td>
</tr>
<tr class="odd">
<td>G</td>
<td>La valeur G est située directement après la valeur Q et doit toujours être la longueur, en octets, du membre <a href="/previous-versions/windows/desktop/legacy/aa381983(v=vs.85)"><strong>DSSPUBKEY_VER3</strong></a><strong>bitlenP</strong> (longueur de bit de P) divisé par huit. Si la longueur des données est un ou plusieurs octets plus courts que P divisés par 8, les données doivent être complétées par les octets nécessaires (de zéro valeur) pour que les données soient de la longueur souhaitée (format<a href="/windows/desktop/SecGloss/l-gly"><em>Little-endian</em></a> ).</td>
</tr>
<tr class="even">
<td>J</td>
<td>La valeur J est située directement après la valeur G et doit toujours être la longueur en octets du membre <a href="/previous-versions/windows/desktop/legacy/aa381983(v=vs.85)"><strong>DSSPUBKEY_VER3</strong></a><strong>bitlenJ</strong> divisé par huit (format<a href="/windows/desktop/SecGloss/l-gly"><em>Little endian</em></a> ). Si la valeur bitlenQ est 0, la valeur est absente de l’objet BLOB.</td>
</tr>
<tr class="odd">
<td>O</td>
<td>La valeur Y, (G ^ X) mod P, est située directement après la valeur J et doit toujours être la longueur, en octets, de la <a href="/previous-versions/windows/desktop/legacy/aa381983(v=vs.85)"><strong>DSSPUBKEY_VER3</strong></a>membre<strong>bitlenP</strong> (longueur de bit de P) divisé par huit. Si la longueur des données résultant du calcul de (G ^ X) mod P est un ou plusieurs octets plus courts que P divisé par 8, les données doivent être complétées par les octets nécessaires (de zéro valeur) pour que les données soient de la longueur souhaitée (format<a href="/windows/desktop/SecGloss/l-gly"><em>Little endian</em></a> ).
<blockquote>
[!Note]<br />
Lorsque cette structure est utilisée avec <a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam"><strong>CryptSetKeyParam</strong></a> avec la valeur <em>dwParam</em> KP_PUB_PARAMS, cette valeur n’est pas incluse dans l’objet BLOB.
</blockquote>
<br/> <br/></td>
</tr>
</tbody>
</table>



 

> [!Note]  
> Les objets BLOB de clé publique ne sont pas chiffrés, mais contiennent des clés publiques sous forme de texte en clair.

 

 

 
