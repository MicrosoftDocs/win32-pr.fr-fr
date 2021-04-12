---
description: Lancement d’une session COPP
ms.assetid: c84a83b4-51b2-4b46-860f-d740b42323fa
title: Lancement d’une session COPP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53d64ef848874aee95d3f928a5b8bb637323a92a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109558"
---
# <a name="initiating-a-copp-session"></a><span data-ttu-id="ef039-103">Lancement d’une session COPP</span><span class="sxs-lookup"><span data-stu-id="ef039-103">Initiating a COPP Session</span></span>

<span data-ttu-id="ef039-104">Pour lancer une session COPP (Certified Output Protection Protocol), vous devez préparer une *signature*, qui est un tableau qui contient la concaténation des nombres suivants :</span><span class="sxs-lookup"><span data-stu-id="ef039-104">To initiate a Certified Output Protection Protocol (COPP) session, you must prepare a *signature*, which is an array that contains the concatenation of the following numbers:</span></span>

-   <span data-ttu-id="ef039-105">Nombre aléatoire 128 bits retourné par le pilote.</span><span class="sxs-lookup"><span data-stu-id="ef039-105">The 128-bit random number returned by the driver.</span></span> <span data-ttu-id="ef039-106">(Cette valeur est indiquée en tant que *guidRandom* pour [obtenir la chaîne de certificats du pilote](obtaining-the-drivers-certificate-chain.md).)</span><span class="sxs-lookup"><span data-stu-id="ef039-106">(This value is shown as *guidRandom* in [Obtaining the Driver's Certificate Chain](obtaining-the-drivers-certificate-chain.md).)</span></span>
-   <span data-ttu-id="ef039-107">Clé AES symétrique 128 bits.</span><span class="sxs-lookup"><span data-stu-id="ef039-107">A 128-bit symmetric AES key.</span></span>
-   <span data-ttu-id="ef039-108">Numéro de séquence de départ 32 bits pour les demandes d’État.</span><span class="sxs-lookup"><span data-stu-id="ef039-108">A 32-bit starting sequence number for status requests.</span></span>
-   <span data-ttu-id="ef039-109">Numéro de séquence de départ 32 bits pour les commandes COPP.</span><span class="sxs-lookup"><span data-stu-id="ef039-109">A 32-bit starting sequence number for COPP commands.</span></span>

<span data-ttu-id="ef039-110">Générez une clé AES symétrique comme suit :</span><span class="sxs-lookup"><span data-stu-id="ef039-110">Generate a symmetric AES key as follows:</span></span>


```C++
DWORD dwFlag = 0x80;         // Bit length: 128-bit AES.
dwFlag <<= 16;               // Move this value to the upper 16 bits.
dwFlag |= CRYPT_EXPORTABLE;  // We want to export the key.
CryptGenKey(
    hCSP,           // Handle to the CSP.
    CALG_AES_128,   // Use 128-bit AES block encryption algorithm.
    dwFlag,
    &m_hAESKey      // Receives a handle to the AES key.
);
```



<span data-ttu-id="ef039-111">La fonction **CryptGenKey** crée la clé symétrique, mais la clé est toujours conservée dans le CSP.</span><span class="sxs-lookup"><span data-stu-id="ef039-111">The **CryptGenKey** function creates the symmetric key, but the key is still held in the CSP.</span></span> <span data-ttu-id="ef039-112">Pour exporter la clé dans un tableau d’octets, utilisez la fonction **CryptExportKey** .</span><span class="sxs-lookup"><span data-stu-id="ef039-112">To export the key into a byte array, use the **CryptExportKey** function.</span></span> <span data-ttu-id="ef039-113">C’est la raison pour laquelle vous utilisez l’indicateur de chiffrement \_ EXportable lors de l’appel de **CryptGenKey**.</span><span class="sxs-lookup"><span data-stu-id="ef039-113">This is the reason for using the CRYPT\_EXPORTABLE flag when calling **CryptGenKey**.</span></span> <span data-ttu-id="ef039-114">Le code suivant exporte la clé et la copie dans le</span><span class="sxs-lookup"><span data-stu-id="ef039-114">The following code exports the key and copies it into the</span></span>


```
pData
```



<span data-ttu-id="ef039-115">.</span><span class="sxs-lookup"><span data-stu-id="ef039-115">array.</span></span>


```C++
DWORD cbData = 0; 
BYTE *pData = NULL;
// Get the size of the blob.
CryptExportKey(hAESKey, 0, PLAINTEXTKEYBLOB, 0, NULL, &cbData);  

// Allocate the array and call again.
pData = new BYTE[cbData];
CryptExportKey(hAESKey, 0, PLAINTEXTKEYBLOB, 0, pData, &cbData);  
```



<span data-ttu-id="ef039-116">Données retournées dans</span><span class="sxs-lookup"><span data-stu-id="ef039-116">The data returned in</span></span>


```
pData
```



<span data-ttu-id="ef039-117">a la disposition suivante :</span><span class="sxs-lookup"><span data-stu-id="ef039-117">has the following layout:</span></span>


```C++
BLOBHEADER header
DWORD      cbSize
BYTE       key[]
```



<span data-ttu-id="ef039-118">Toutefois, aucune structure qui correspond à cette disposition n’est définie dans les en-têtes CryptoAPI.</span><span class="sxs-lookup"><span data-stu-id="ef039-118">However, no structure that matches this layout is defined in the CryptoAPI headers.</span></span> <span data-ttu-id="ef039-119">Vous pouvez définir un ou plusieurs opérations arithmétiques sur les pointeurs.</span><span class="sxs-lookup"><span data-stu-id="ef039-119">You can either define one or do some pointer arithmetic.</span></span> <span data-ttu-id="ef039-120">Par exemple, pour vérifier la taille de la clé :</span><span class="sxs-lookup"><span data-stu-id="ef039-120">For example, to verify the size of the key:</span></span>


```C++
DWORD *pcbKey = (DWORD*)(pData + sizeof(BLOBHEADER));
if (*pcbKey != 16)
{
    // Wrong size! Should be 16 bytes (128 bits).
}
```



<span data-ttu-id="ef039-121">Pour faire passer le pointeur à la clé elle-même :</span><span class="sxs-lookup"><span data-stu-id="ef039-121">To get the pointer to the key itself:</span></span>


```C++
BYTE *pKey = pData + sizeof(BLOBHEADER) + sizeof(DWORD);
```



<span data-ttu-id="ef039-122">Ensuite, générez un nombre aléatoire 32 bits à utiliser comme séquence de départ pour les demandes d’État COPP.</span><span class="sxs-lookup"><span data-stu-id="ef039-122">Next, generate a 32-bit random number to use as the starting sequence for COPP status requests.</span></span> <span data-ttu-id="ef039-123">La méthode recommandée pour créer un nombre aléatoire consiste à appeler la fonction **CryptGenRandom** .</span><span class="sxs-lookup"><span data-stu-id="ef039-123">The recommended way to create a random number is to call the **CryptGenRandom** function.</span></span> <span data-ttu-id="ef039-124">N’utilisez pas la fonction **Rand** dans la bibliothèque Runtime C, car elle n’est pas véritablement aléatoire.</span><span class="sxs-lookup"><span data-stu-id="ef039-124">Do not use the **rand** function in the C run-time library, because it is not truly random.</span></span> <span data-ttu-id="ef039-125">Générez un deuxième nombre aléatoire de 32 bits à utiliser comme séquence de départ pour les commandes COPP.</span><span class="sxs-lookup"><span data-stu-id="ef039-125">Generate a second 32-bit random number to use as the starting sequence for COPP commands.</span></span>


```C++
UINT uStatusSeq;     // Status sequence number.
UINT uCommandSeq;    // Command sequence number.
CryptGenRandom(hCSP, sizeof(UINT), &uStatusSeq);
CryptGenRandom(hCSP, sizeof(UINT), &uCommandSeq);
```



<span data-ttu-id="ef039-126">Vous pouvez maintenant préparer la signature COPP.</span><span class="sxs-lookup"><span data-stu-id="ef039-126">Now you can prepare the COPP signature.</span></span> <span data-ttu-id="ef039-127">Il s’agit d’un tableau de 256 octets, défini en tant que structure [**AMCOPPSignature**](/windows/win32/api/strmif/ns-strmif-amcoppsignature) .</span><span class="sxs-lookup"><span data-stu-id="ef039-127">This is a 256-byte array, defined as the [**AMCOPPSignature**](/windows/win32/api/strmif/ns-strmif-amcoppsignature) structure.</span></span> <span data-ttu-id="ef039-128">Initialise le contenu du tableau à zéro.</span><span class="sxs-lookup"><span data-stu-id="ef039-128">Initialize the contents of the array to zero.</span></span> <span data-ttu-id="ef039-129">Copiez ensuite les quatre nombres dans le tableau (le nombre aléatoire du pilote, la clé AES, le numéro de séquence d’État et le numéro de séquence de commande), dans cet ordre.</span><span class="sxs-lookup"><span data-stu-id="ef039-129">Then copy the four numbers into the array—the driver's random number, the AES key, the status sequence number, and the command sequence number, in that order.</span></span> <span data-ttu-id="ef039-130">Enfin, échangez l’ordre d’octet du tableau entier.</span><span class="sxs-lookup"><span data-stu-id="ef039-130">Finally, swap the byte order of the entire array.</span></span>

<span data-ttu-id="ef039-131">En fonction de la documentation de **CryptEncrypt**:</span><span class="sxs-lookup"><span data-stu-id="ef039-131">According to the documentation for **CryptEncrypt**:</span></span>

<dl> <span data-ttu-id="ef039-132">«La longueur des données en texte brut qui peuvent être chiffrées à l’aide d’un appel à **CryptEncrypt** avec une clé RSA est la longueur du modulo de clé moins onze octets.</span><span class="sxs-lookup"><span data-stu-id="ef039-132">"The length of plaintext data that can be encrypted with a call to **CryptEncrypt** with an RSA key is the length of the key modulus minus eleven bytes.</span></span> <span data-ttu-id="ef039-133">La valeur minimale choisie pour le remplissage PKCS 1 est de onze octets \# .»</span><span class="sxs-lookup"><span data-stu-id="ef039-133">The eleven bytes is the chosen minimum for PKCS \#1 padding."</span></span>  
</dl>

<span data-ttu-id="ef039-134">Dans ce cas, le modulo est de 256 octets, ce qui signifie que la longueur maximale du message est de 245 octets (256 – 11).</span><span class="sxs-lookup"><span data-stu-id="ef039-134">In this case, the modulus is 256 bytes, so the maximum message length is 245 bytes (256 – 11).</span></span> <span data-ttu-id="ef039-135">La structure **AMCOPPSignature** est de 256 octets, mais les données significatives dans la signature ne sont que 40 octets.</span><span class="sxs-lookup"><span data-stu-id="ef039-135">The **AMCOPPSignature** structure is 256 bytes, but the meaningful data in the signature is only 40 bytes.</span></span> <span data-ttu-id="ef039-136">Le code suivant chiffre la signature et fournit le résultat dans</span><span class="sxs-lookup"><span data-stu-id="ef039-136">The following code encrypts the signature and provides the result in</span></span>


```
CoppSig
```



<span data-ttu-id="ef039-137">.</span><span class="sxs-lookup"><span data-stu-id="ef039-137">.</span></span>


```C++
AMCOPPSignature CoppSig;
ZeroMemory(&CoppSig, sizeof(CoppSig));
// Copy the signature data into CoppSig. (Not shown.)

// Encrypt the signature:
const DWORD RSA_PADDING = 11;    // 11-byte padding.
DWORD cbDataOut = sizeof(AMCOPPSignature);
DWORD cbDataIn = cbDataOut - RSA_PADDING;
CryptEncrypt(
    hRSAKey, 
    NULL,     // No hash object.
    TRUE,     // Final block to encrypt.
    0,        // Reserved.
    &CoppSig, // COPP signature.
    &cbDataOut, 
    cbDataIn
);
```



<span data-ttu-id="ef039-138">À présent, transmettez le tableau chiffré à [**IAMCertifiedOutputProtection :: SessionSequenceStart**](/windows/desktop/api/Strmif/nf-strmif-iamcertifiedoutputprotection-sessionsequencestart):</span><span class="sxs-lookup"><span data-stu-id="ef039-138">Now pass the encrypted array to [**IAMCertifiedOutputProtection::SessionSequenceStart**](/windows/desktop/api/Strmif/nf-strmif-iamcertifiedoutputprotection-sessionsequencestart):</span></span>


```C++
hr = pCOPP->SessionSequenceStart(&CoppSig);
if (SUCCEEDED(hr))
{
    // Ready to send COPP commands and status requests.
}
```



<span data-ttu-id="ef039-139">Si cette méthode est établie, vous êtes prêt à envoyer des commandes COPP et des demandes d’État au pilote.</span><span class="sxs-lookup"><span data-stu-id="ef039-139">If this method succeeds, you are ready to send COPP commands and status requests to the driver.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ef039-140">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ef039-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ef039-141">Utilisation du protocole COPP (Certified Output Protection Protocol)</span><span class="sxs-lookup"><span data-stu-id="ef039-141">Using Certified Output Protection Protocol (COPP)</span></span>](using-certified-output-protection-protocol--copp.md)
</dt> </dl>

 

 



