---
description: Un hachage d’un texte ou d’une autre chaîne d’octets est une valeur associée de longueur fixe, unique et statistique.
ms.assetid: e54d5a3b-cae1-47dd-a565-7bf1ccef7f52
title: Hachages de données
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed785c79bef67f5a54b0d91c0c2686f8fd1b967f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868426"
---
# <a name="data-hashes"></a><span data-ttu-id="cb58d-103">Hachages de données</span><span class="sxs-lookup"><span data-stu-id="cb58d-103">Data Hashes</span></span>

<span data-ttu-id="cb58d-104">Un [*hachage*](../secgloss/h-gly.md) d’un texte ou d’une autre chaîne d’octets est une valeur associée de longueur fixe, unique et statistique.</span><span class="sxs-lookup"><span data-stu-id="cb58d-104">A [*hash*](../secgloss/h-gly.md) of a text or other string of bytes is an associated, statistically unique, fixed-length value.</span></span> <span data-ttu-id="cb58d-105">Dans certains documents, le *hachage* d’un texte est également appelé un condensé. Toutefois, dans cette documentation, le terme hachage est toujours utilisé.</span><span class="sxs-lookup"><span data-stu-id="cb58d-105">In some documents, a *hash* of a text is also called a digest; however, in this documentation the term hash will always be used.</span></span> <span data-ttu-id="cb58d-106">Les fonctions CryptoAPI offrent un moyen de créer un hachage pour tout texte ou une autre chaîne d’octets.</span><span class="sxs-lookup"><span data-stu-id="cb58d-106">CryptoAPI functions provide a means to create a hash for any text or other string of bytes.</span></span> <span data-ttu-id="cb58d-107">Ce hachage, Then, peut être utilisé comme identificateur unique de ses données associées.</span><span class="sxs-lookup"><span data-stu-id="cb58d-107">That hash, then, can be used as a unique identifier of its associated data.</span></span>

<span data-ttu-id="cb58d-108">Pour garantir l' [*intégrité*](../secgloss/i-gly.md) d’un texte, un [*hachage*](../secgloss/h-gly.md) de texte peut être envoyé pour accompagner le texte.</span><span class="sxs-lookup"><span data-stu-id="cb58d-108">To ensure the [*integrity*](../secgloss/i-gly.md) of a text, a [*hash*](../secgloss/h-gly.md) of a text can be sent to accompany the text.</span></span> <span data-ttu-id="cb58d-109">Le récepteur peut ensuite calculer un hachage sur les données reçues et comparer le hachage calculé avec le hachage reçu.</span><span class="sxs-lookup"><span data-stu-id="cb58d-109">The receiver can then compute a hash on the data received and compare the hash computed with the hash received.</span></span> <span data-ttu-id="cb58d-110">Si les deux correspondances sont identiques, les données reçues doivent être les mêmes que celles à partir desquelles le hachage reçu a été créé.</span><span class="sxs-lookup"><span data-stu-id="cb58d-110">If the two match, the data received must be the same as the data from which the received hash was created.</span></span>

<span data-ttu-id="cb58d-111">Pour obtenir une valeur de hachage, créez un objet de hachage à l’aide de [**CryptCreateHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash).</span><span class="sxs-lookup"><span data-stu-id="cb58d-111">To obtain a hash value, create a hash object using [**CryptCreateHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash).</span></span> <span data-ttu-id="cb58d-112">Cet objet accumule les données à vérifier.</span><span class="sxs-lookup"><span data-stu-id="cb58d-112">This object will accumulate the data to be verified.</span></span> <span data-ttu-id="cb58d-113">Les données sont ensuite ajoutées à l’objet de hachage avec la fonction [**CryptHashData**](/windows/desktop/api/Wincrypt/nf-wincrypt-crypthashdata) .</span><span class="sxs-lookup"><span data-stu-id="cb58d-113">The data is then added to the hash object with the [**CryptHashData**](/windows/desktop/api/Wincrypt/nf-wincrypt-crypthashdata) function.</span></span>

<span data-ttu-id="cb58d-114">Une fois le dernier bloc de données ajouté au hachage, la fonction [**CryptGetHashParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgethashparam) est utilisée pour obtenir la valeur de hachage des données.</span><span class="sxs-lookup"><span data-stu-id="cb58d-114">After the last block of data is added to the hash, the [**CryptGetHashParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgethashparam) function is used to obtain the hash value of the data.</span></span>

<span data-ttu-id="cb58d-115">Une meilleure sécurité est fournie en détruisant l’objet de hachage avec [**CryptDestroyHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdestroyhash) dès que la valeur de hachage a été obtenue.</span><span class="sxs-lookup"><span data-stu-id="cb58d-115">Better security is provided by destroying the hash object with [**CryptDestroyHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdestroyhash) as soon as the hash value has been obtained.</span></span>

 

 
