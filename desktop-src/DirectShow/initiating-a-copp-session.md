---
description: Lancement d’une session COPP
ms.assetid: c84a83b4-51b2-4b46-860f-d740b42323fa
title: Lancement d’une session COPP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72e3d952e7e938eee3eef27663ea075b3a5b23d4e61ef9f9fd0ea9b5395708cf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119748669"
---
# <a name="initiating-a-copp-session"></a>Lancement d’une session COPP

Pour lancer une session COPP (Certified Output Protection Protocol), vous devez préparer une *signature*, qui est un tableau qui contient la concaténation des nombres suivants :

-   Nombre aléatoire 128 bits retourné par le pilote. (Cette valeur est indiquée en tant que *guidRandom* pour [obtenir la chaîne de certificats du pilote](obtaining-the-drivers-certificate-chain.md).)
-   Clé AES symétrique 128 bits.
-   Numéro de séquence de départ 32 bits pour les demandes d’État.
-   Numéro de séquence de départ 32 bits pour les commandes COPP.

Générez une clé AES symétrique comme suit :


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



La fonction **CryptGenKey** crée la clé symétrique, mais la clé est toujours conservée dans le CSP. Pour exporter la clé dans un tableau d’octets, utilisez la fonction **CryptExportKey** . C’est la raison pour laquelle vous utilisez l’indicateur de chiffrement \_ EXportable lors de l’appel de **CryptGenKey**. Le code suivant exporte la clé et la copie dans le


```
pData
```



.


```C++
DWORD cbData = 0; 
BYTE *pData = NULL;
// Get the size of the blob.
CryptExportKey(hAESKey, 0, PLAINTEXTKEYBLOB, 0, NULL, &cbData);  

// Allocate the array and call again.
pData = new BYTE[cbData];
CryptExportKey(hAESKey, 0, PLAINTEXTKEYBLOB, 0, pData, &cbData);  
```



Données retournées dans


```
pData
```



a la disposition suivante :


```C++
BLOBHEADER header
DWORD      cbSize
BYTE       key[]
```



Toutefois, aucune structure qui correspond à cette disposition n’est définie dans les en-têtes CryptoAPI. Vous pouvez définir un ou plusieurs opérations arithmétiques sur les pointeurs. Par exemple, pour vérifier la taille de la clé :


```C++
DWORD *pcbKey = (DWORD*)(pData + sizeof(BLOBHEADER));
if (*pcbKey != 16)
{
    // Wrong size! Should be 16 bytes (128 bits).
}
```



Pour faire passer le pointeur à la clé elle-même :


```C++
BYTE *pKey = pData + sizeof(BLOBHEADER) + sizeof(DWORD);
```



Ensuite, générez un nombre aléatoire 32 bits à utiliser comme séquence de départ pour les demandes d’État COPP. La méthode recommandée pour créer un nombre aléatoire consiste à appeler la fonction **CryptGenRandom** . N’utilisez pas la fonction **Rand** dans la bibliothèque Runtime C, car elle n’est pas véritablement aléatoire. Générez un deuxième nombre aléatoire de 32 bits à utiliser comme séquence de départ pour les commandes COPP.


```C++
UINT uStatusSeq;     // Status sequence number.
UINT uCommandSeq;    // Command sequence number.
CryptGenRandom(hCSP, sizeof(UINT), &uStatusSeq);
CryptGenRandom(hCSP, sizeof(UINT), &uCommandSeq);
```



Vous pouvez maintenant préparer la signature COPP. Il s’agit d’un tableau de 256 octets, défini en tant que structure [**AMCOPPSignature**](/windows/win32/api/strmif/ns-strmif-amcoppsignature) . Initialise le contenu du tableau à zéro. Copiez ensuite les quatre nombres dans le tableau (le nombre aléatoire du pilote, la clé AES, le numéro de séquence d’État et le numéro de séquence de commande), dans cet ordre. Enfin, échangez l’ordre d’octet du tableau entier.

En fonction de la documentation de **CryptEncrypt**:

<dl> «La longueur des données en texte brut qui peuvent être chiffrées à l’aide d’un appel à **CryptEncrypt** avec une clé RSA est la longueur du modulo de clé moins onze octets. La valeur minimale choisie pour le remplissage PKCS 1 est de onze octets \# .»  
</dl>

Dans ce cas, le modulo est de 256 octets, ce qui signifie que la longueur maximale du message est de 245 octets (256 – 11). La structure **AMCOPPSignature** est de 256 octets, mais les données significatives dans la signature ne sont que 40 octets. Le code suivant chiffre la signature et fournit le résultat dans


```
CoppSig
```



.


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



À présent, transmettez le tableau chiffré à [**IAMCertifiedOutputProtection :: SessionSequenceStart**](/windows/desktop/api/Strmif/nf-strmif-iamcertifiedoutputprotection-sessionsequencestart):


```C++
hr = pCOPP->SessionSequenceStart(&CoppSig);
if (SUCCEEDED(hr))
{
    // Ready to send COPP commands and status requests.
}
```



Si cette méthode est établie, vous êtes prêt à envoyer des commandes COPP et des demandes d’État au pilote.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation du protocole COPP (Certified Output Protection Protocol)](using-certified-output-protection-protocol--copp.md)
</dt> </dl>

 

 



