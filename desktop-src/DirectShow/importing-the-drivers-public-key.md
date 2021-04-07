---
description: Importation de la clé publique des pilotes
ms.assetid: 9bab0e43-6e9f-4cdb-bfd0-cdafcc12d526
title: Importation de la clé publique des pilotes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 222b9c62bd9babe0a01a0e6a9b3a50747ab3b039
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103846498"
---
# <a name="importing-the-drivers-public-key"></a><span data-ttu-id="e0712-103">Importation de la clé publique des pilotes</span><span class="sxs-lookup"><span data-stu-id="e0712-103">Importing the Drivers Public Key</span></span>

<span data-ttu-id="e0712-104">La clé publique RSA du pilote est contenue dans les balises de modulo et d’exposant du nœud terminal du certificat.</span><span class="sxs-lookup"><span data-stu-id="e0712-104">The driver's RSA public key is contained in the Modulus and Exponent tags of the certificate's leaf node.</span></span> <span data-ttu-id="e0712-105">Les deux valeurs sont encodées en base64 et doivent être décodées.</span><span class="sxs-lookup"><span data-stu-id="e0712-105">Both values are base64-encoded and must be decoded.</span></span> <span data-ttu-id="e0712-106">Si vous utilisez la CryptoAPI de Microsoft, vous devez importer la clé dans un fournisseur de services de chiffrement (CSP), qui est le module qui implémente les algorithmes de chiffrement.</span><span class="sxs-lookup"><span data-stu-id="e0712-106">If you are using Microsoft's CryptoAPI, you must import the key into a cryptographic service provider (CSP), which is the module that implements the cryptographic algorithms.</span></span>

<span data-ttu-id="e0712-107">Pour convertir le modulo et les exposants de l’encodage Base64 en tableaux binaires, utilisez la fonction **CryptStringToBinary** , comme indiqué dans le code suivant.</span><span class="sxs-lookup"><span data-stu-id="e0712-107">To convert the modulus and exponents from base64 encoding to binary arrays, use the **CryptStringToBinary** function, as shown in the following code.</span></span> <span data-ttu-id="e0712-108">Appelez la fonction une fois pour récupérer la taille du tableau d’octets.</span><span class="sxs-lookup"><span data-stu-id="e0712-108">Call the function once to get the size of the byte array.</span></span> <span data-ttu-id="e0712-109">Allouez ensuite la mémoire tampon et rappelez la fonction.</span><span class="sxs-lookup"><span data-stu-id="e0712-109">Then allocate the buffer and call the function again.</span></span>


```C++
DWORD cbLen = 0, dwSkip = 0, dwFlags = 0;
::CryptStringToBinary(
   pszModulus,  // String that contains the Base64-encoded modulus.
   cchModulus,  // Length of the string, not including the trailing NULL.
   CRYPT_STRING_BASE64,  // Base64 encoding.
   NULL,     // Do not convert yet. Just calculate the length.
   &cbLen,   // Receives the length of the buffer that is required.
   &dwSkip,  // Receives the number of skipped characters.
   &dwFlags  // Receives flags.
);

// Allocate a new buffer.
BYTE *pbBuffer = new BYTE [cbLen];
::CryptStringToBinary(pszModulus, cchModulus, CRYPT_STRING_BASE64, 
    pbBuffer, &cbLen, &dwSkip, &dwFlags);

// (Repeat these steps for the exponent.)
```



<span data-ttu-id="e0712-110">Le tableau encodé en base64 est dans l’ordre de primauté des octets de poids fort, tandis que l’ordonnanceur CryptoAPI attend le nombre dans l’ordre de primauté des octets de poids faible (Little endian). vous devez donc permuter l’ordre d’octet du tableau retourné par **CryptStringToBinary**.</span><span class="sxs-lookup"><span data-stu-id="e0712-110">The base64-encoded array is in big-endian order, whereas the CryptoAPI expects the number in little-endian order, so you need to swap the byte order of the array that is returned from **CryptStringToBinary**.</span></span> <span data-ttu-id="e0712-111">Le modulo est de 256 octets, mais le tableau d’octets décodé peut être inférieur à 256 octets.</span><span class="sxs-lookup"><span data-stu-id="e0712-111">The modulus is 256 bytes, but the decoded byte array might be less than 256 bytes.</span></span> <span data-ttu-id="e0712-112">Si c’est le cas, vous devez allouer un nouveau tableau de 256 octets, copier les données dans le nouveau tableau et remplir le début du tableau avec des zéros.</span><span class="sxs-lookup"><span data-stu-id="e0712-112">If so, you will need to allocate a new array that is 256 bytes, copy the data into the new array, and pad the front of the array with zeros.</span></span> <span data-ttu-id="e0712-113">L’exposant est une valeur DWORD (4 octets).</span><span class="sxs-lookup"><span data-stu-id="e0712-113">The exponent is a DWORD (4-byte) value.</span></span>

<span data-ttu-id="e0712-114">Une fois que vous avez les valeurs du modulo et de l’exposant, vous pouvez importer la clé dans le fournisseur de services de chiffrement (CSP) par défaut, comme indiqué dans le code suivant :</span><span class="sxs-lookup"><span data-stu-id="e0712-114">After you have the modulus and exponent values, you can import the key into the default cryptographic service provider (CSP), as shown in the following code:</span></span>


```C++
// Assume the following values exist:
BYTE *pModulus;     // Byte array that contains the modulus.
DWORD cbModulus;    // Size of the modulus in bytes.
DWORD dwExponent;   // Exponent.

// Create a new key container to hold the key. 
::CryptAcquireContext(
    &hCSP,         // Receives a handle to the CSP.
    NULL,          // Use the default key container.
    NULL,          // Use the default CSP.
    PROV_RSA_AES,  // Use the AES provider (public-key algorithm).
    CRYPT_SILENT | CRYPT_NEWKEYSET 
);

// Move the key into the key container. 
// The data format is: PUBLICKEYSTRUC + RSAPUBKEY + key
DWORD cbKeyBlob = cbModulus + sizeof(PUBLICKEYSTRUC) + sizeof(RSAPUBKEY)
BYTE *pBlob = new BYTE[cbKeyBlob];

// Fill in the data.
PUBLICKEYSTRUC *pPublicKey = (PUBLICKEYSTRUC*)pBlob;
pPublicKey->bType = PUBLICKEYBLOB; 
pPublicKey->bVersion = CUR_BLOB_VERSION;  // Always use this value.
pPublicKey->reserved = 0;                 // Must be zero.
pPublicKey->aiKeyAlg = CALG_RSA_KEYX;     // RSA public-key key exchange. 

// The next block of data is the RSAPUBKEY structure.
RSAPUBKEY *pRsaPubKey = (RSAPUBKEY*)(pBlob + sizeof(PUBLICKEYSTRUC));
pRsaPubKey->magic = RSA1;            // Public key.
pRsaPubKey->bitlen = cbModulus * 8;  // Number of bits in the modulus.
pRsaPubKey->pubexp = dwExponent;     // Exponent.

// Copy the modulus into the blob. Put the modulus directly after the
// RSAPUBKEY structure in the blob.
BYTE *pKey = (BYTE*)(pRsaPubkey + sizeof(RSAPUBKEY));
CopyMemory(pKey, pModulus, cbModulus);

// Now import the key.
HCRYPTKEY hRSAKey;  // Receives a handle to the key.
CryptImportKey(hCSP, pBlob, cbKeyBlob, 0, 0, &hRSAKey) 
```



<span data-ttu-id="e0712-115">Vous pouvez désormais utiliser l’CryptoAPI pour chiffrer les commandes et les demandes d’État avec la clé publique du pilote.</span><span class="sxs-lookup"><span data-stu-id="e0712-115">Now you can use the CryptoAPI to encrypt commands and status requests with the driver's public key.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e0712-116">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e0712-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e0712-117">Utilisation du protocole COPP (Certified Output Protection Protocol)</span><span class="sxs-lookup"><span data-stu-id="e0712-117">Using Certified Output Protection Protocol (COPP)</span></span>](using-certified-output-protection-protocol--copp.md)
</dt> </dl>

 

 



