---
description: Les objets BLOB de clé publique DSS version 3 de type PUBLICKEYBLOB permettent d’exporter et d’importer des informations sur une clé publique DH.
ms.assetid: 9aac1d61-8b61-4f0f-b037-afe4a60302de
title: Objets BLOB de clé publique DSS version 3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 593ac69025ff046a9a8d014286c2464788c07b02
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516635"
---
# <a name="dss-version-3-public-key-blobs"></a><span data-ttu-id="2b993-103">Objets BLOB de clé publique DSS version 3</span><span class="sxs-lookup"><span data-stu-id="2b993-103">DSS Version 3 Public Key BLOBs</span></span>

<span data-ttu-id="2b993-104">Les [*objets BLOB de clé publique*](../secgloss/p-gly.md) DSS version 3 de type PublicKeyBlob permettent d’exporter et d’importer des informations sur une clé publique DH.</span><span class="sxs-lookup"><span data-stu-id="2b993-104">DSS version 3 [*Public Key BLOBs*](../secgloss/p-gly.md) of type PUBLICKEYBLOB are used to export and import information about a DH public key.</span></span> <span data-ttu-id="2b993-105">Ils ont le format suivant :</span><span class="sxs-lookup"><span data-stu-id="2b993-105">They have the following format:</span></span>


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



<span data-ttu-id="2b993-106">Ce format d' [*objet BLOB*](../secgloss/b-gly.md) est exporté lorsque l’indicateur de chiffrement \_ d’objets BLOB \_ VER3 est utilisé avec [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey).</span><span class="sxs-lookup"><span data-stu-id="2b993-106">This [*BLOB*](../secgloss/b-gly.md) format is exported when the CRYPT\_BLOB\_VER3 flag is used with [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey).</span></span> <span data-ttu-id="2b993-107">Étant donné que la version se trouve dans l’objet BLOB, il n’est pas nécessaire de spécifier un indicateur lors de l’utilisation de cet objet BLOB avec [**CryptImportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey).</span><span class="sxs-lookup"><span data-stu-id="2b993-107">Because the version is in the BLOB, there is no need to specify a flag when using this BLOB with [**CryptImportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey).</span></span>

<span data-ttu-id="2b993-108">En outre, ce format d’objet BLOB est utilisé avec la fonction [**CryptSetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam) lorsque la valeur *dwParam* KP \_ pub \_ param est utilisée pour définir des paramètres de clé sur une clé DSS.</span><span class="sxs-lookup"><span data-stu-id="2b993-108">In addition, this BLOB format is used with the [**CryptSetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam) function when the *dwParam* value KP\_PUB\_PARAMS is used to set key parameters on a DSS key.</span></span> <span data-ttu-id="2b993-109">Cela se fait lorsque l' \_ indicateur de chiffrement PREGEN a été utilisé pour générer la clé.</span><span class="sxs-lookup"><span data-stu-id="2b993-109">This is done when the CRYPT\_PREGEN flag has been used to generate the key.</span></span> <span data-ttu-id="2b993-110">Lorsqu’elle est utilisée dans cette situation, la valeur y est ignorée et ne doit donc pas être incluse dans l’objet BLOB.</span><span class="sxs-lookup"><span data-stu-id="2b993-110">When used in this situation, the y value is ignored and therefore should not be included in the BLOB.</span></span>

<span data-ttu-id="2b993-111">Le tableau suivant décrit chaque composant de l’objet BLOB de clé.</span><span class="sxs-lookup"><span data-stu-id="2b993-111">The following table describes each component of the key BLOB.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2b993-112">Champ</span><span class="sxs-lookup"><span data-stu-id="2b993-112">Field</span></span></th>
<th><span data-ttu-id="2b993-113">Description</span><span class="sxs-lookup"><span data-stu-id="2b993-113">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2b993-114">Blobheader</span><span class="sxs-lookup"><span data-stu-id="2b993-114">Blobheader</span></span></td>
<td><span data-ttu-id="2b993-115">Structure <a href="/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc"><strong>BLOBHEADER</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="2b993-115">A <a href="/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc"><strong>BLOBHEADER</strong></a> structure.</span></span> <span data-ttu-id="2b993-116">Le membre <strong>bType</strong> doit avoir la valeur PublicKeyBlob.</span><span class="sxs-lookup"><span data-stu-id="2b993-116">The <strong>bType</strong> member must have a value of PUBLICKEYBLOB.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2b993-117">Dsspubkeyver3</span><span class="sxs-lookup"><span data-stu-id="2b993-117">Dsspubkeyver3</span></span></td>
<td><span data-ttu-id="2b993-118">Structure <a href="/previous-versions/windows/desktop/legacy/aa381983(v=vs.85)"><strong>DSSPUBKEY_VER3</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="2b993-118">A <a href="/previous-versions/windows/desktop/legacy/aa381983(v=vs.85)"><strong>DSSPUBKEY_VER3</strong></a> structure.</span></span> <span data-ttu-id="2b993-119">Le membre <strong>magique</strong> doit être défini sur &quot; DSS3 &quot; (0x33535344) pour les clés publiques.</span><span class="sxs-lookup"><span data-stu-id="2b993-119">The <strong>magic</strong> member should be set to &quot;DSS3&quot; (0x33535344) for public keys.</span></span> <span data-ttu-id="2b993-120">Notez que la valeur hexadécimale est simplement un encodage <a href="/windows/desktop/SecGloss/a-gly"><em>ASCII</em></a> de &quot; DSS3.&quot;</span><span class="sxs-lookup"><span data-stu-id="2b993-120">Notice that the hexadecimal value is just an <a href="/windows/desktop/SecGloss/a-gly"><em>ASCII</em></a> encoding of &quot;DSS3.&quot;</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2b993-121">P</span><span class="sxs-lookup"><span data-stu-id="2b993-121">P</span></span></td>
<td><span data-ttu-id="2b993-122">La valeur P est située directement après la structure <a href="/previous-versions/windows/desktop/legacy/aa381983(v=vs.85)"><strong>DSSPUBKEY_VER3</strong></a> , et doit toujours être la longueur, en octets, du champ <strong>bitlenP</strong> DSSPUBKEY_VER3 (longueur binaire de P) divisé par huit (format<a href="/windows/desktop/SecGloss/l-gly"><em>Little-endian</em></a> ).</span><span class="sxs-lookup"><span data-stu-id="2b993-122">The P value is located directly after the <a href="/previous-versions/windows/desktop/legacy/aa381983(v=vs.85)"><strong>DSSPUBKEY_VER3</strong></a> structure, and should always be the length, in bytes, of the DSSPUBKEY_VER3 <strong>bitlenP</strong> field (bit length of P) divided by eight (<a href="/windows/desktop/SecGloss/l-gly"><em>little-endian</em></a> format).</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2b993-123">Q</span><span class="sxs-lookup"><span data-stu-id="2b993-123">Q</span></span></td>
<td><span data-ttu-id="2b993-124">La valeur Q est située directement après la valeur P et doit toujours être la longueur en octets du membre <a href="/previous-versions/windows/desktop/legacy/aa381983(v=vs.85)"><strong>DSSPUBKEY_VER3</strong></a><strong>bitlenQ</strong> divisé par huit (format<a href="/windows/desktop/SecGloss/l-gly"><em>Little endian</em></a> ).</span><span class="sxs-lookup"><span data-stu-id="2b993-124">The Q value is located directly after the P value and should always be the length in bytes of the <a href="/previous-versions/windows/desktop/legacy/aa381983(v=vs.85)"><strong>DSSPUBKEY_VER3</strong></a><strong>bitlenQ</strong> member divided by eight (<a href="/windows/desktop/SecGloss/l-gly"><em>little-endian</em></a> format).</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2b993-125">G</span><span class="sxs-lookup"><span data-stu-id="2b993-125">G</span></span></td>
<td><span data-ttu-id="2b993-126">La valeur G est située directement après la valeur Q et doit toujours être la longueur, en octets, du membre <a href="/previous-versions/windows/desktop/legacy/aa381983(v=vs.85)"><strong>DSSPUBKEY_VER3</strong></a><strong>bitlenP</strong> (longueur de bit de P) divisé par huit.</span><span class="sxs-lookup"><span data-stu-id="2b993-126">The G value is located directly after the Q value and should always be the length, in bytes, of the <a href="/previous-versions/windows/desktop/legacy/aa381983(v=vs.85)"><strong>DSSPUBKEY_VER3</strong></a><strong>bitlenP</strong> member (bit length of P) divided by eight.</span></span> <span data-ttu-id="2b993-127">Si la longueur des données est un ou plusieurs octets plus courts que P divisés par 8, les données doivent être complétées par les octets nécessaires (de zéro valeur) pour que les données soient de la longueur souhaitée (format<a href="/windows/desktop/SecGloss/l-gly"><em>Little-endian</em></a> ).</span><span class="sxs-lookup"><span data-stu-id="2b993-127">If the length of the data is one or more bytes shorter than P divided by 8, the data must be padded with the necessary bytes (of zero value) to make the data the desired length (<a href="/windows/desktop/SecGloss/l-gly"><em>little-endian</em></a> format).</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2b993-128">J</span><span class="sxs-lookup"><span data-stu-id="2b993-128">J</span></span></td>
<td><span data-ttu-id="2b993-129">La valeur J est située directement après la valeur G et doit toujours être la longueur en octets du membre <a href="/previous-versions/windows/desktop/legacy/aa381983(v=vs.85)"><strong>DSSPUBKEY_VER3</strong></a><strong>bitlenJ</strong> divisé par huit (format<a href="/windows/desktop/SecGloss/l-gly"><em>Little endian</em></a> ).</span><span class="sxs-lookup"><span data-stu-id="2b993-129">The J value is located directly after the G value and should always be the length in bytes of the <a href="/previous-versions/windows/desktop/legacy/aa381983(v=vs.85)"><strong>DSSPUBKEY_VER3</strong></a><strong>bitlenJ</strong> member divided by eight (<a href="/windows/desktop/SecGloss/l-gly"><em>little-endian</em></a> format).</span></span> <span data-ttu-id="2b993-130">Si la valeur bitlenQ est 0, la valeur est absente de l’objet BLOB.</span><span class="sxs-lookup"><span data-stu-id="2b993-130">If the bitlenQ value is 0, then the value is absent from the BLOB.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2b993-131">O</span><span class="sxs-lookup"><span data-stu-id="2b993-131">Y</span></span></td>
<td><span data-ttu-id="2b993-132">La valeur Y, (G ^ X) mod P, est située directement après la valeur J et doit toujours être la longueur, en octets, de la <a href="/previous-versions/windows/desktop/legacy/aa381983(v=vs.85)"><strong>DSSPUBKEY_VER3</strong></a>membre<strong>bitlenP</strong> (longueur de bit de P) divisé par huit.</span><span class="sxs-lookup"><span data-stu-id="2b993-132">The Y value, (G^X) mod P, is located directly after the J value, and should always be the length, in bytes, of the <a href="/previous-versions/windows/desktop/legacy/aa381983(v=vs.85)"><strong>DSSPUBKEY_VER3</strong></a><strong>bitlenP</strong> member (bit length of P) divided by eight.</span></span> <span data-ttu-id="2b993-133">Si la longueur des données résultant du calcul de (G ^ X) mod P est un ou plusieurs octets plus courts que P divisé par 8, les données doivent être complétées par les octets nécessaires (de zéro valeur) pour que les données soient de la longueur souhaitée (format<a href="/windows/desktop/SecGloss/l-gly"><em>Little endian</em></a> ).</span><span class="sxs-lookup"><span data-stu-id="2b993-133">If the length of the data that results from the calculation of (G^X) mod P is one or more bytes shorter than P divided by 8, the data must be padded with the necessary bytes (of zero value) to make the data the desired length (<a href="/windows/desktop/SecGloss/l-gly"><em>little-endian</em></a> format).</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="2b993-134">Lorsque cette structure est utilisée avec <a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam"><strong>CryptSetKeyParam</strong></a> avec la valeur <em>dwParam</em> KP_PUB_PARAMS, cette valeur n’est pas incluse dans l’objet BLOB.</span><span class="sxs-lookup"><span data-stu-id="2b993-134">When this structure is used with <a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam"><strong>CryptSetKeyParam</strong></a> with the <em>dwParam</em> value KP_PUB_PARAMS, then this value is not included in the BLOB.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
</tbody>
</table>



 

> [!Note]  
> <span data-ttu-id="2b993-135">Les objets BLOB de clé publique ne sont pas chiffrés, mais contiennent des clés publiques sous forme de texte en clair.</span><span class="sxs-lookup"><span data-stu-id="2b993-135">Public key BLOBs are not encrypted, but contain public keys in plaintext form.</span></span>

 

 

 
