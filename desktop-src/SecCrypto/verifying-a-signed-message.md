---
description: Ces étapes vérifient la signature des données signées.
ms.assetid: 18246cc1-d3c4-4426-a342-ce3864cc412e
title: Vérification d’un message signé
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e8f85a5bcde56df7bb41bb92276123bcd26024e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106538939"
---
# <a name="verifying-a-signed-message"></a><span data-ttu-id="50d14-103">Vérification d’un message signé</span><span class="sxs-lookup"><span data-stu-id="50d14-103">Verifying a Signed Message</span></span>

<span data-ttu-id="50d14-104">Ces étapes vérifient la signature des données signées.</span><span class="sxs-lookup"><span data-stu-id="50d14-104">These steps verify the signature of signed data.</span></span> <span data-ttu-id="50d14-105">L’illustration suivante représente les tâches individuelles qui doivent être accomplies, comme indiqué dans la liste qui la suit.</span><span class="sxs-lookup"><span data-stu-id="50d14-105">The following illustration depicts the individual tasks that must be accomplished, as shown in the list that follows it.</span></span>

![vérification d’un message signé](images/verifmsg.png)

<span data-ttu-id="50d14-107">**Pour vérifier la signature d’un message signé**</span><span class="sxs-lookup"><span data-stu-id="50d14-107">**To verify the signature of a signed message**</span></span>

1.  <span data-ttu-id="50d14-108">Obtient un pointeur vers le message signé.</span><span class="sxs-lookup"><span data-stu-id="50d14-108">Get a pointer to the signed message.</span></span>
2.  <span data-ttu-id="50d14-109">Ouvrez un [*magasin de certificats*](../secgloss/c-gly.md).</span><span class="sxs-lookup"><span data-stu-id="50d14-109">Open a [*certificate store*](../secgloss/c-gly.md).</span></span>
3.  <span data-ttu-id="50d14-110">À l’aide de l’ID du signataire contenu dans le message, récupérez le certificat de l’expéditeur et recevez un handle de sa [*clé publique*](../secgloss/p-gly.md).</span><span class="sxs-lookup"><span data-stu-id="50d14-110">Using the signer ID contained in the message, get the sender's certificate and get a handle to its [*public key*](../secgloss/p-gly.md).</span></span>

    <span data-ttu-id="50d14-111">Comme alternative aux étapes 2 et 3, vous pouvez utiliser le certificat contenu dans le message pour récupérer la clé publique du signataire.</span><span class="sxs-lookup"><span data-stu-id="50d14-111">As an alternative to steps 2 and 3, you can use the certificate contained in the message to retrieve the signer's public key.</span></span>

4.  <span data-ttu-id="50d14-112">À l’aide de la clé publique du signataire, déchiffrez la signature numérique, en générant le condensé d’origine des données dans le message.</span><span class="sxs-lookup"><span data-stu-id="50d14-112">Using the signer's public key, decrypt the digital signature, producing the original digest of the data in the message.</span></span>
5.  <span data-ttu-id="50d14-113">À l’aide de l’algorithme de hachage contenu dans le message, [*Hachez*](../secgloss/h-gly.md) les données contenues dans le message, en générant un nouveau condensé.</span><span class="sxs-lookup"><span data-stu-id="50d14-113">Using the hash algorithm contained in the message, [*hash*](../secgloss/h-gly.md) the data contained in the message, yielding a new digest.</span></span>
6.  <span data-ttu-id="50d14-114">Comparez le condensé récupéré à partir du message avec le nouveau condensé que vous venez de créer.</span><span class="sxs-lookup"><span data-stu-id="50d14-114">Compare the digest retrieved from the message with the new digest just created.</span></span>
7.  <span data-ttu-id="50d14-115">Si les deux résumés correspondent, la signature est vérifiée.</span><span class="sxs-lookup"><span data-stu-id="50d14-115">If the two digests match, the signature is verified.</span></span> <span data-ttu-id="50d14-116">Cela signifie que la [*clé privée*](../secgloss/p-gly.md) qui a été utilisée pour signer les données correspond à la clé publique utilisée pour déchiffrer la signature, et que les données n’ont pas changé depuis la signature des données.</span><span class="sxs-lookup"><span data-stu-id="50d14-116">This means that the [*private key*](../secgloss/p-gly.md) that was used to sign the data matches the public key just used to decrypt the signature, and that the data has not changed since the data was signed.</span></span>

    <span data-ttu-id="50d14-117">Si les deux résumés ne correspondent pas, cela signifie que la signature n’est pas vérifiée et que les clés privée/publique ne correspondent pas, ou que les données ont été modifiées depuis la signature des données, ou les deux à la fois.</span><span class="sxs-lookup"><span data-stu-id="50d14-117">If the two digests do not match, the signature is not verified, and either the private/public keys do not match, or the data has been changed since the data was signed, or both.</span></span>

<span data-ttu-id="50d14-118">Une seule fonction, [**CryptVerifyMessageSignature**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptverifymessagesignature), peut être utilisée pour vérifier une signature, comme indiqué dans la procédure suivante.</span><span class="sxs-lookup"><span data-stu-id="50d14-118">A single function, [**CryptVerifyMessageSignature**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptverifymessagesignature), can be used to verify a signature, as shown in the following procedure.</span></span>

<span data-ttu-id="50d14-119">**Pour vérifier un message signé**</span><span class="sxs-lookup"><span data-stu-id="50d14-119">**To verify a signed message**</span></span>

1.  <span data-ttu-id="50d14-120">Obtient un pointeur vers le message signé.</span><span class="sxs-lookup"><span data-stu-id="50d14-120">Get a pointer to the signed message.</span></span>
2.  <span data-ttu-id="50d14-121">Obtient la taille du message signé.</span><span class="sxs-lookup"><span data-stu-id="50d14-121">Get the size of the signed message.</span></span>
3.  <span data-ttu-id="50d14-122">Obtenir un handle sur un fournisseur de services de chiffrement.</span><span class="sxs-lookup"><span data-stu-id="50d14-122">Get a handle on a cryptographic provider.</span></span>
4.  <span data-ttu-id="50d14-123">Initialisez la structure du [**\_ \_ message \_ de vérification**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_verify_message_para) de chiffrement.</span><span class="sxs-lookup"><span data-stu-id="50d14-123">Initialize the [**CRYPT\_VERIFY\_MESSAGE\_PARA**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_verify_message_para) structure.</span></span>
5.  <span data-ttu-id="50d14-124">Appelez [**CryptVerifyMessageSignature**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptverifymessagesignature) pour vérifier la signature.</span><span class="sxs-lookup"><span data-stu-id="50d14-124">Call [**CryptVerifyMessageSignature**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptverifymessagesignature) to verify the signature.</span></span>

<span data-ttu-id="50d14-125">Le code qui implémente cette procédure est inclus dans l' [exemple de programme C : signature d’un message et vérification d’une signature de message](example-c-program-signing-a-message-and-verifying-a-message-signature.md).</span><span class="sxs-lookup"><span data-stu-id="50d14-125">Code that implements this procedure is included in [Example C Program: Signing a Message and Verifying a Message Signature](example-c-program-signing-a-message-and-verifying-a-message-signature.md).</span></span>

 

 
