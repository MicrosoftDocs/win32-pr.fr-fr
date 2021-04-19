---
description: Le chiffrement en bloc et les clés MAC sont dérivés d’une clé principale, mais peuvent inclure d’autres sources en fonction du protocole et de la suite de chiffrement utilisés.
ms.assetid: f78acb54-c32a-46a8-b465-855251069a57
title: Dériver le chiffrement en bloc et les clés MAC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97cbf216fd850c7b98c638d4fdc10a84087d91ac
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2021
ms.locfileid: "106545870"
---
# <a name="deriving-bulk-encryption-and-mac-keys"></a><span data-ttu-id="1e6fc-103">Dériver le chiffrement en bloc et les clés MAC</span><span class="sxs-lookup"><span data-stu-id="1e6fc-103">Deriving Bulk Encryption and MAC Keys</span></span>

<span data-ttu-id="1e6fc-104">Le [*chiffrement en bloc*](../secgloss/b-gly.md) et les [*clés Mac*](../secgloss/m-gly.md) sont dérivés d’une [*clé principale*](../secgloss/m-gly.md) , mais peuvent inclure d’autres sources en fonction du protocole et de la suite de chiffrement utilisés.</span><span class="sxs-lookup"><span data-stu-id="1e6fc-104">[*Bulk encryption*](../secgloss/b-gly.md) and [*MAC keys*](../secgloss/m-gly.md) are derived from a [*master key*](../secgloss/m-gly.md) but can include other sources depending on the protocol and cipher suite used.</span></span>

<span data-ttu-id="1e6fc-105">Le processus de dérivation du chiffrement en bloc et des clés MAC est le même pour le client et le serveur :</span><span class="sxs-lookup"><span data-stu-id="1e6fc-105">The process of deriving bulk encryption and MAC keys is the same for both client and server:</span></span>

1.  <span data-ttu-id="1e6fc-106">Le moteur de protocole appelle [**CryptSetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam) sur la clé principale une ou plusieurs fois pour fournir au CSP les informations nécessaires pour générer les clés.</span><span class="sxs-lookup"><span data-stu-id="1e6fc-106">The protocol engine calls [**CryptSetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam) on the master key one or more times to provide the CSP with the information needed to build the keys.</span></span>
2.  <span data-ttu-id="1e6fc-107">Étant donné que les clés [*CryptoAPI*](../secgloss/c-gly.md) ne peuvent pas être dérivées directement d’autres clés, un objet de hachage est créé à partir de la clé principale à l’aide de [**CryptCreateHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash).</span><span class="sxs-lookup"><span data-stu-id="1e6fc-107">Because [*CryptoAPI*](../secgloss/c-gly.md) keys cannot be derived directly from other keys, a hash object is created from the master key using [**CryptCreateHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash).</span></span> <span data-ttu-id="1e6fc-108">Ce [*hachage*](../secgloss/h-gly.md) est utilisé pour créer les nouvelles clés.</span><span class="sxs-lookup"><span data-stu-id="1e6fc-108">This [*hash*](../secgloss/h-gly.md) is used to create the new keys.</span></span>
3.  <span data-ttu-id="1e6fc-109">Les deux clés de chiffrement en bloc et les deux clés MAC sont créées à partir de l’objet « principal Hash » à l’aide de quatre appels à [**CryptDeriveKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptderivekey).</span><span class="sxs-lookup"><span data-stu-id="1e6fc-109">The two bulk encryption keys and the two MAC keys are created from the "master hash" object using four calls to [**CryptDeriveKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptderivekey).</span></span>

> [!Note]
> <span data-ttu-id="1e6fc-110">Lorsque vous effectuez une reconnexion SSL, un moteur de protocole peut exécuter la procédure ci-dessus plusieurs fois à l’aide de la même clé principale.</span><span class="sxs-lookup"><span data-stu-id="1e6fc-110">When performing SSL reconnects, a protocol engine can perform the above procedure several times using the same master key.</span></span> <span data-ttu-id="1e6fc-111">Cela permet au client et au serveur d’avoir plusieurs connexions souvent simultanées, chacune utilisant des clés de [*chiffrement et de chiffrement en bloc*](../secgloss/b-gly.md) différentes sans aucune autre opération de Diffie-Hellman ou RSA.</span><span class="sxs-lookup"><span data-stu-id="1e6fc-111">This enables the client and server to have multiple, often simultaneous connections, each using different [*Bulk encryption*](../secgloss/b-gly.md) and MAC keys without additional RSA or Diffie-Hellman operations.</span></span>
> 
> <span data-ttu-id="1e6fc-112">Tous les fournisseurs de services de chiffrement doivent utiliser de bonnes pratiques thread-safe.</span><span class="sxs-lookup"><span data-stu-id="1e6fc-112">All CSPs must use good thread-safe practices.</span></span> <span data-ttu-id="1e6fc-113">Les nombres de threads de plusieurs douzaines ne sont pas inhabituels.</span><span class="sxs-lookup"><span data-stu-id="1e6fc-113">Thread counts of several dozen are not unusual.</span></span>

 

<span data-ttu-id="1e6fc-114">Voici un code source classique pour le moteur de protocole :</span><span class="sxs-lookup"><span data-stu-id="1e6fc-114">The following is typical source code for the protocol engine:</span></span>


```C++
//--------------------------------------------------------------------
//   Define and initialize local variables.

BOOL fClient = <TRUE if this is code for the client?>;
CRYPT_DATA_BLOB Data;
HCRYPTHASH hMasterHash;

//--------------------------------------------------------------------
// Finish creating the master_secret.

switch(<protocol being used>)
{
    case <PCT 1.0>:

//------------------------------------------------------------
// Specify clear key value.

        Data.pbData = pClearKey;
        Data.cbData = cbClearKey;
        CryptSetKeyParam(
                   hMasterKey, 
                   KP_CLEAR_KEY, 
                   (PBYTE)&Data, 
                   0);

//------------------------------------------------------------
// Specify the CH_CHALLENGE_DATA.

        Data.pbData = pChallenge;
        Data.cbData = cbChallenge;
        CryptSetKeyParam(
                    hMasterKey, 
                    KP_CLIENT_RANDOM, 
                    (PBYTE)&Data, 
                    0);

//------------------------------------------------------------
// Specify the SH_CONNECTION_ID_DATA.

        Data.pbData = pConnectionID;
        Data.cbData = cbConnectionID;
        CryptSetKeyParam(
                    hMasterKey, 
                    KP_SERVER_RANDOM, 
                    (PBYTE)&Data, 
                    0);

//------------------------------------------------------------
// Specify the SH_CERTIFICATE_DATA.
        Data.pbData = pbServerCertificate;
        Data.cbData = cbServerCertificate;
        CryptSetKeyParam(
                    hMasterKey, 
                    KP_CERTIFICATE, 
                    (PBYTE)&Data, 
                    0);
        break;

    case <SSL 2.0>:

//------------------------------------------------------------
// Specify clear key value.

        Data.pbData = pClearKey;
        Data.cbData = cbClearKey;
        CryptSetKeyParam(
                 hMasterKey, 
                 KP_CLEAR_KEY, 
                 (PBYTE)&Data, 
                 0);

//------------------------------------------------------------
// Specify the CH_CHALLENGE_DATA.

        Data.pbData = pChallenge;
        Data.cbData = cbChallenge;
        CryptSetKeyParam(
                 hMasterKey, 
                 KP_CLIENT_RANDOM,
                 (BYTE*)&Data, 
                 0);

//------------------------------------------------------------
// Specify the SH_CONNECTION_ID_DATA.

        Data.pbData = pConnectionID;
        Data.cbData = cbConnectionID;
        CryptSetKeyParam(
                   hMasterKey, 
                   KP_SERVER_RANDOM,
                   (BYTE*)&Data, 
                   0);
        break;

case <SSL 3.0>:
case <TLS 1.0>:


//------------------------------------------------------------
// Specify client_random.

        Data.pbData = pClientRandom;
        Data.cbData = cbClientRandom;
        CryptSetKeyParam(
                hMasterKey, 
                KP_CLIENT_RANDOM, 
                (PBYTE)&Data, 
                 0);

//------------------------------------------------------------
// Specify server_random.

        Data.pbData = pServerRandom;
        Data.cbData = cbServerRandom;
        CryptSetKeyParam(
                  hMasterKey, 
                  KP_SERVER_RANDOM, 
                  (PBYTE)&Data, 
                  0);
}

//------------------------------------------------------------
// Create the master hash object from the master key.

CryptCreateHash(
            hProv, 
            CALG_SCHANNEL_MASTER_HASH,
            hMasterKey, 
            0, 
            &hMasterHash);

//------------------------------------------------------------
// Derive read key from the master hash object.

CryptDeriveKey(hProv, 
               CALG_SCHANNEL_ENC_KEY, 
               hMasterHash,
               fClient ? CRYPT_SERVER : 0,
               &hReadKey);

//------------------------------------------------------------
// Derive write key from the master hash object.

CryptDeriveKey(
           hProv,
           CALG_SCHANNEL_ENC_KEY,
           hMasterHash,
           fClient ? 0 : CRYPT_SERVER,
           &hWriteKey);

if(<protocol being used> != <SSL 2.0>)   // for SSL 2.0, the master 
                                         // key is also the MAC.
{
//------------------------------------------------------------
// Derive read MAC from the master hash object.

    CryptDeriveKey(
              hProv,
              CALG_SCHANNEL_MAC_KEY,
              hMasterHash,
              fClient ? CRYPT_SERVER : 0,
              &hReadMAC);

//------------------------------------------------------------
// Derive write MAC from the master hash object.

    CryptDeriveKey(
             hProv,
             CALG_SCHANNEL_MAC_KEY,
             hMasterHash,
             fClient ? 0 : CRYPT_SERVER,
             &hWriteMAC);
}

CryptDestroyHash(hMasterHash);
```



 

 
