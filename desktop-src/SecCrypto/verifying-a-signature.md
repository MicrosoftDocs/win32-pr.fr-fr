---
description: Pour vérifier une signature, créez un objet de hachage à l’aide de CryptCreateHash. Cet objet de hachage accumule les données à vérifier. Les données sont ensuite ajoutées à l’objet de hachage avec la fonction CryptHashData.
ms.assetid: 3779f83b-0d87-4f47-949b-9eb39690adfb
title: Vérification d’une signature
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9a416dc2c3f7523af781e68fe78b066accbe6d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114110"
---
# <a name="verifying-a-signature"></a><span data-ttu-id="0798d-105">Vérification d’une signature</span><span class="sxs-lookup"><span data-stu-id="0798d-105">Verifying a Signature</span></span>

<span data-ttu-id="0798d-106">Pour vérifier une signature, créez un [*objet de hachage*](../secgloss/h-gly.md) à l’aide de [**CryptCreateHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash).</span><span class="sxs-lookup"><span data-stu-id="0798d-106">To verify a signature, create a [*hash object*](../secgloss/h-gly.md) using [**CryptCreateHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash).</span></span> <span data-ttu-id="0798d-107">Cet objet de hachage accumule les données à vérifier.</span><span class="sxs-lookup"><span data-stu-id="0798d-107">This hash object accumulates the data to be verified.</span></span> <span data-ttu-id="0798d-108">Les données sont ensuite ajoutées à l’objet de hachage avec la fonction [**CryptHashData**](/windows/desktop/api/Wincrypt/nf-wincrypt-crypthashdata) .</span><span class="sxs-lookup"><span data-stu-id="0798d-108">The data is then added to the hash object with the [**CryptHashData**](/windows/desktop/api/Wincrypt/nf-wincrypt-crypthashdata) function.</span></span>

<span data-ttu-id="0798d-109">Une fois le dernier bloc de données ajouté au hachage, utilisez [**CryptVerifySignature**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptverifysignaturea) pour vérifier la signature.</span><span class="sxs-lookup"><span data-stu-id="0798d-109">After the last block of data is added to the hash, use [**CryptVerifySignature**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptverifysignaturea) to verify the signature.</span></span> <span data-ttu-id="0798d-110">L’adresse des données de signature, un descripteur de l’objet de hachage et le descripteur des clés publiques sont passés à **CryptVerifySignature**.</span><span class="sxs-lookup"><span data-stu-id="0798d-110">The address of the signature data, a handle to the hash object, and the handle of the public keys are passed to **CryptVerifySignature**.</span></span>

<span data-ttu-id="0798d-111">Une fois que la signature a été vérifiée (ou n’a pas réussi la vérification), détruisez l’objet de hachage à l’aide de la fonction [**CryptDestroyHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdestroyhash) .</span><span class="sxs-lookup"><span data-stu-id="0798d-111">After the signature has been verified (or has failed the verification), destroy the hash object using the [**CryptDestroyHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdestroyhash) function.</span></span>

 

 
