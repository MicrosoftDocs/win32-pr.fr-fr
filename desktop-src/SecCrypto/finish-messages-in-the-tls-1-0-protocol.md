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
# <a name="finish-messages-in-the-tls-10-protocol"></a><span data-ttu-id="71fdd-103">Finaliser les messages dans le protocole TLS 1,0</span><span class="sxs-lookup"><span data-stu-id="71fdd-103">Finish Messages in the TLS 1.0 Protocol</span></span>

<span data-ttu-id="71fdd-104">Un message de fin est envoyé immédiatement après un message de spécification de chiffrement de modification pour vérifier la réussite de l’échange de clés et des processus d’authentification.</span><span class="sxs-lookup"><span data-stu-id="71fdd-104">A finish message is sent immediately after a change cipher spec message to verify the success of key exchange and authentication processes.</span></span> <span data-ttu-id="71fdd-105">Les messages de fin dans le protocole TLS 1,0 sont calculés à l’aide d’une [*fonction Pseudo-aléatoire*](../secgloss/p-gly.md) (PRF) avec la [*clé principale*](../secgloss/m-gly.md), une étiquette et une valeur initiale comme entrée.</span><span class="sxs-lookup"><span data-stu-id="71fdd-105">The finish messages in the TLS 1.0 protocol are calculated using [*Pseudo-Random Function*](../secgloss/p-gly.md) (PRF) with the [*master key*](../secgloss/m-gly.md), a label, and a seed as input.</span></span> <span data-ttu-id="71fdd-106">Le PRF produit une sortie de longueur arbitraire.</span><span class="sxs-lookup"><span data-stu-id="71fdd-106">PRF produces an output of arbitrary length.</span></span> <span data-ttu-id="71fdd-107">La méthode suivante est utilisée pour générer la sortie PRF utilisée dans les messages de fin TLS 1,0.</span><span class="sxs-lookup"><span data-stu-id="71fdd-107">The following method is used to generate the PRF output used in TLS 1.0 finish messages.</span></span>

<span data-ttu-id="71fdd-108">Un descripteur de [*hachage*](../secgloss/h-gly.md) PRF est généré à l’aide de [**CryptCreateHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash) avec la valeur d' **\_ ID ALG** définie sur CALG \_ TLS1PRF et le descripteur de la clé principale passée dans le paramètre *HKEY* .</span><span class="sxs-lookup"><span data-stu-id="71fdd-108">A PRF [*hash*](../secgloss/h-gly.md) handle is generated using [**CryptCreateHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash) with the **ALG\_ID** value set to CALG\_TLS1PRF and the handle to the master key passed in the *hKey* parameter.</span></span> <span data-ttu-id="71fdd-109">Les valeurs d’étiquette et de valeur initiale sont définies sur le descripteur de hachage à l’aide des valeurs \_ étiquette HP TLS1PRF \_ et valeur \_ initiale HP TLS1PRF \_ , respectivement, dans le paramètre *dwParam* avec la fonction [**CryptSetHashParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsethashparam) .</span><span class="sxs-lookup"><span data-stu-id="71fdd-109">The label and seed values are set on the hash handle using the values HP\_TLS1PRF\_LABEL and HP\_TLS1PRF\_SEED, respectively, in the *dwParam* parameter with the [**CryptSetHashParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsethashparam) function.</span></span> <span data-ttu-id="71fdd-110">Enfin, le moteur de protocole appelle la fonction [**CryptGetHashParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgethashparam) avec la valeur HP \_ HASHVAL dans le paramètre *dwParam* pour récupérer les données de PRF à inclure dans le message de fin.</span><span class="sxs-lookup"><span data-stu-id="71fdd-110">Finally, the protocol engine calls the function [**CryptGetHashParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgethashparam) with the value HP\_HASHVAL in the *dwParam* parameter to retrieve the PRF data to be included in the finish message.</span></span> <span data-ttu-id="71fdd-111">Lorsque vous effectuez l’appel à **CryptGetHashParam**, le moteur de protocole doit spécifier le nombre d’octets de données que le PRF produira.</span><span class="sxs-lookup"><span data-stu-id="71fdd-111">When making the call to **CryptGetHashParam**, the protocol engine must specify how many bytes of data PRF will produce.</span></span> <span data-ttu-id="71fdd-112">Cela s’effectue dans le paramètre *pdwDataLen* , et les données résultantes sont placées dans la mémoire tampon vers laquelle pointe le paramètre *pbData* .</span><span class="sxs-lookup"><span data-stu-id="71fdd-112">This is done in the *pdwDataLen* parameter, and the resulting data is placed in the buffer pointed to by the *pbData* parameter.</span></span>

<span data-ttu-id="71fdd-113">Voici un code source classique pour ce moteur de protocole :</span><span class="sxs-lookup"><span data-stu-id="71fdd-113">The following is typical source code for this protocol engine:</span></span>


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



 

 
