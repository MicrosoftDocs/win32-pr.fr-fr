---
description: Les fournisseurs de services de chiffrement \_ RSA \_ Schannel doivent prendre en charge le \_ hachage CALG SSL3 \_ SHAMD5 qui est compatible avec le fournisseur de services de chiffrement de base Microsoft utilisé dans l’authentification du client SSL 3,0 et TLS 1,0.
ms.assetid: ca8be4fd-e7ca-4def-927d-b168628c566e
title: Type de signature SHA/MD5 RSA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71dcd515c61a4baf3da1fb35e4b5e6d21d5c849e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106539051"
---
# <a name="shamd5-rsa-signature-type"></a><span data-ttu-id="20b5b-103">Type de signature SHA/MD5 RSA</span><span class="sxs-lookup"><span data-stu-id="20b5b-103">SHA/MD5 RSA Signature Type</span></span>

<span data-ttu-id="20b5b-104">Les fournisseurs de services de chiffrement \_ RSA \_ Schannel doivent prendre en charge le \_ hachage CALG SSL3 \_ SHAMD5 qui est compatible avec le fournisseur de services de chiffrement de base Microsoft utilisé dans l’authentification du client SSL 3,0 et TLS 1,0. [](../secgloss/h-gly.md)</span><span class="sxs-lookup"><span data-stu-id="20b5b-104">CSPs for PROV\_RSA\_SCHANNEL must support the CALG\_SSL3\_SHAMD5 [*hash*](../secgloss/h-gly.md) that is compatible with the Microsoft Base Cryptographic Provider used in SSL 3.0 and TLS 1.0 client authentication.</span></span> <span data-ttu-id="20b5b-105">Ce hachage est constitué d’une concaténation d’un hachage [*MD5*](../secgloss/m-gly.md) et d’un hachage SHA signé avec une clé privée RSA ou Diffie-Hellman.</span><span class="sxs-lookup"><span data-stu-id="20b5b-105">This hash consists of a concatenation of an [*MD5*](../secgloss/m-gly.md) hash and a SHA hash signed with an RSA or Diffie-Hellman private key.</span></span> <span data-ttu-id="20b5b-106">Un handle vers une valeur de hachage de ce type est créé à l’aide de la fonction [**CryptCreateHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash) ou [**CPCreateHash**](https://www.bing.com/search?q=**CPCreateHash**) avec CALG \_ SSL3 \_ SHAMD5 comme paramètre *algid* .</span><span class="sxs-lookup"><span data-stu-id="20b5b-106">A handle to a hash value of this type is created by using the [**CryptCreateHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash) or [**CPCreateHash**](https://www.bing.com/search?q=**CPCreateHash**) function with CALG\_SSL3\_SHAMD5 as the *Algid* parameter.</span></span> <span data-ttu-id="20b5b-107">Vous pouvez consulter des exemples de fonctions de hachage dans l' [exemple de programme c : création et hachage d’une clé de session](example-c-program-creating-and-hashing-a-session-key.md) et [exemple de programme c : signature d’un hachage et vérification de la signature de hachage](example-c-program-signing-a-hash-and-verifying-the-hash-signature.md).</span><span class="sxs-lookup"><span data-stu-id="20b5b-107">Examples of using hash functions can be seen in [Example C Program: Creating and Hashing a Session Key](example-c-program-creating-and-hashing-a-session-key.md) and [Example C Program: Signing a Hash and Verifying the Hash Signature](example-c-program-signing-a-hash-and-verifying-the-hash-signature.md).</span></span>

 

 
