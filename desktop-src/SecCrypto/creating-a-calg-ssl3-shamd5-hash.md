---
description: Explique comment créer un hachage CALG \_ SSL3 \_ SHAMD5.
ms.assetid: dad6fc7f-8abd-4f90-b3e4-8d0169e95087
title: Création d’un hachage de CALG_SSL3_SHAMD5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2f38b5939dc64467ef813b354f33a90f009619f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106536711"
---
# <a name="creating-a-calg_ssl3_shamd5-hash"></a><span data-ttu-id="3ff5d-103">Création d’un \_ hachage CALG SSL3 \_ SHAMD5</span><span class="sxs-lookup"><span data-stu-id="3ff5d-103">Creating a CALG\_SSL3\_SHAMD5 Hash</span></span>

<span data-ttu-id="3ff5d-104">**Pour créer un \_ hachage CALG SSL3 \_ SHAMD5**</span><span class="sxs-lookup"><span data-stu-id="3ff5d-104">**To create a CALG\_SSL3\_SHAMD5 hash**</span></span>

1.  <span data-ttu-id="3ff5d-105">À l’aide de la méthodologie CryptoAPI standard, créez un [](../secgloss/s-gly.md) [*hachage*](../secgloss/h-gly.md) MD5 et un hachage SHA des données cibles.</span><span class="sxs-lookup"><span data-stu-id="3ff5d-105">Using standard CryptoAPI methodology, create both a MD5 and a [*SHA*](../secgloss/s-gly.md) [*hash*](../secgloss/h-gly.md) of the target data.</span></span>
2.  <span data-ttu-id="3ff5d-106">Concaténez les deux hachages, avec la valeur MD5 la plus à gauche et la valeur SHA la plus à droite.</span><span class="sxs-lookup"><span data-stu-id="3ff5d-106">Concatenate the two hashes, with the MD5 value leftmost and the SHA value rightmost.</span></span> <span data-ttu-id="3ff5d-107">Cela génère une valeur de 36 octets (16 octets + 20 octets).</span><span class="sxs-lookup"><span data-stu-id="3ff5d-107">This results in a 36-byte value (16 bytes + 20 bytes).</span></span>
3.  <span data-ttu-id="3ff5d-108">Obtient un handle vers un [*objet de hachage*](../secgloss/h-gly.md) en appelant [**CryptCreateHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash) avec CALG \_ SSL3 \_ SHAMD5 passé dans le paramètre *algid* .</span><span class="sxs-lookup"><span data-stu-id="3ff5d-108">Get a handle to a [*hash object*](../secgloss/h-gly.md) by calling [**CryptCreateHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash) with CALG\_SSL3\_SHAMD5 passed in the *Algid* parameter.</span></span>
4.  <span data-ttu-id="3ff5d-109">Définissez la valeur de hachage avec un appel à [**CryptSetHashParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsethashparam).</span><span class="sxs-lookup"><span data-stu-id="3ff5d-109">Set the hash value with a call to [**CryptSetHashParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsethashparam).</span></span> <span data-ttu-id="3ff5d-110">Les valeurs de hachage concaténées sont passées en tant qu' **octets** \* dans le paramètre *pbData* , et la \_ valeur HP HASHVAL doit être transmise dans le paramètre *dwParam* .</span><span class="sxs-lookup"><span data-stu-id="3ff5d-110">The concatenated hash values are passed as a **BYTE**\* in the *pbData* parameter, and the HP\_HASHVAL value must be passed in the *dwParam* parameter.</span></span> <span data-ttu-id="3ff5d-111">L’appel de [**CryptHashData**](/windows/desktop/api/Wincrypt/nf-wincrypt-crypthashdata) à l’aide du handle retourné par [**CryptCreateHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash) à l’étape 3 échouera.</span><span class="sxs-lookup"><span data-stu-id="3ff5d-111">Calling [**CryptHashData**](/windows/desktop/api/Wincrypt/nf-wincrypt-crypthashdata) using the handle returned by [**CryptCreateHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash) in step 3 will fail.</span></span>
5.  <span data-ttu-id="3ff5d-112">Appelez [**CryptSignHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsignhasha) pour générer la signature.</span><span class="sxs-lookup"><span data-stu-id="3ff5d-112">Call [**CryptSignHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsignhasha) to generate the signature.</span></span>
6.  <span data-ttu-id="3ff5d-113">Appelez [**CryptDestroyHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdestroyhash) pour détruire l’objet de hachage.</span><span class="sxs-lookup"><span data-stu-id="3ff5d-113">Call [**CryptDestroyHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdestroyhash) to destroy the hash object.</span></span>

 

 
