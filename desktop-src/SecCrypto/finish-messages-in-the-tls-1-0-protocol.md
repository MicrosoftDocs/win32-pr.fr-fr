---
description: Un message de fin est envoyé immédiatement après un message de spécification de chiffrement de modification pour vérifier la réussite de l’échange de clés et des processus d’authentification.
ms.assetid: 1ae92223-3729-48be-af42-146c9cbae6a5
title: Finaliser les messages dans le protocole TLS 1,0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5a0f0f3e85916e66d434cb3e69b083348e40143
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106521320"
---
# <a name="finish-messages-in-the-tls-10-protocol"></a>Finaliser les messages dans le protocole TLS 1,0

Un message de fin est envoyé immédiatement après un message de spécification de chiffrement de modification pour vérifier la réussite de l’échange de clés et des processus d’authentification. Les messages de fin dans le protocole TLS 1,0 sont calculés à l’aide d’une [*fonction Pseudo-aléatoire*](../secgloss/p-gly.md) (PRF) avec la [*clé principale*](../secgloss/m-gly.md), une étiquette et une valeur initiale comme entrée. Le PRF produit une sortie de longueur arbitraire. La méthode suivante est utilisée pour générer la sortie PRF utilisée dans les messages de fin TLS 1,0.

Un descripteur de [*hachage*](../secgloss/h-gly.md) PRF est généré à l’aide de [**CryptCreateHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash) avec la valeur d' **\_ ID ALG** définie sur CALG \_ TLS1PRF et le descripteur de la clé principale passée dans le paramètre *HKEY* . Les valeurs d’étiquette et de valeur initiale sont définies sur le descripteur de hachage à l’aide des valeurs \_ étiquette HP TLS1PRF \_ et valeur \_ initiale HP TLS1PRF \_ , respectivement, dans le paramètre *dwParam* avec la fonction [**CryptSetHashParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsethashparam) . Enfin, le moteur de protocole appelle la fonction [**CryptGetHashParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgethashparam) avec la valeur HP \_ HASHVAL dans le paramètre *dwParam* pour récupérer les données de PRF à inclure dans le message de fin. Lorsque vous effectuez l’appel à **CryptGetHashParam**, le moteur de protocole doit spécifier le nombre d’octets de données que le PRF produira. Cela s’effectue dans le paramètre *pdwDataLen* , et les données résultantes sont placées dans la mémoire tampon vers laquelle pointe le paramètre *pbData* .

Voici un code source classique pour ce moteur de protocole :


```C++
CRYPT_DATA_BLOB Data;
HCRYPTHASH hFinishHash;
BYTE rgbFinishPRF[12];
BYTE rgbCliHashOfHandshakes[36];

//------------------------------------------------------------
// get client finish message

CryptCreateHash(
         hProv, 
         CALG_TLS1PRF, 
         hMasterKey, 
         0, 
         &hFinishHash);

Data.pbData = (BYTE*)"client finished";
Data.cbData = 15;
CryptSetHashParam(
         hFinishHash, 
         HP_TLS1PRF_LABEL, 
         (BYTE*)&Data, 
         0);

Data.pbData = rgbCliHashOfHandshakes;
Data.cbData = sizeof(rgbCliHashOfHandshakes);
CryptSetHashParam(
          hFinishHash, 
          HP_TLS1PRF_SEED, 
          (BYTE*)&Data, 
          0);

cbFinishPRF = sizeof(rgbFinishPRF);
CryptGetHashParam(
          hFinishHash, 
          HP_HASHVAL, 
          rgbFinishPRF, 
          &cbFinishPRF, 
          0);

CryptDestroyHash(hFinishHash);
```



 

 
