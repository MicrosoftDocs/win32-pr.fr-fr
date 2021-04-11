---
description: Décrit les tâches qui doivent être effectuées pour créer un message signé.
ms.assetid: 61896022-28c2-4f70-977a-c990b4b23c55
title: Création d’un message signé
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f68511c41a10fc0f690574e71c1dfe8a354efbd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203553"
---
# <a name="creating-a-signed-message"></a><span data-ttu-id="953b5-103">Création d’un message signé</span><span class="sxs-lookup"><span data-stu-id="953b5-103">Creating a Signed Message</span></span>

<span data-ttu-id="953b5-104">L’illustration suivante représente les tâches qui doivent être accomplies pour créer un message signé.</span><span class="sxs-lookup"><span data-stu-id="953b5-104">The following illustration depicts the tasks that must be accomplished to create a signed message.</span></span> <span data-ttu-id="953b5-105">Les étapes sont répertoriées à la suite de l’illustration.</span><span class="sxs-lookup"><span data-stu-id="953b5-105">The steps are listed following the illustration.</span></span>

![signature d’un message](images/signdmsg.png)

<span data-ttu-id="953b5-107">**Pour créer un message signé**</span><span class="sxs-lookup"><span data-stu-id="953b5-107">**To create a signed message**</span></span>

1.  <span data-ttu-id="953b5-108">Créez les données (si nécessaire) et recevez un pointeur vers celle-ci.</span><span class="sxs-lookup"><span data-stu-id="953b5-108">Create the data (if necessary) and get a pointer to it.</span></span>
2.  <span data-ttu-id="953b5-109">Ouvrez un [*magasin de certificats*](../secgloss/c-gly.md) qui contient le certificat du signataire.</span><span class="sxs-lookup"><span data-stu-id="953b5-109">Open a [*certificate store*](../secgloss/c-gly.md) that contains the signer's certificate.</span></span>
3.  <span data-ttu-id="953b5-110">Obtenir la [*clé privée*](../secgloss/p-gly.md) du certificat.</span><span class="sxs-lookup"><span data-stu-id="953b5-110">Get the [*private key*](../secgloss/p-gly.md) for the certificate.</span></span> <span data-ttu-id="953b5-111">Une propriété doit être définie sur le certificat avant de l’utiliser pour lier un certificat à un [*CSP*](../secgloss/c-gly.md)particulier, et, dans ce CSP, à une clé privée particulière.</span><span class="sxs-lookup"><span data-stu-id="953b5-111">A property must be set on the certificate before using it, to tie a certificate to a particular [*CSP*](../secgloss/c-gly.md), and, within that CSP, to a particular private key.</span></span> <span data-ttu-id="953b5-112">Cela doit être défini une seule fois.</span><span class="sxs-lookup"><span data-stu-id="953b5-112">This needs to be set once.</span></span>
4.  <span data-ttu-id="953b5-113">Choisissez un algorithme de hachage pour l’opération Digest.</span><span class="sxs-lookup"><span data-stu-id="953b5-113">Choose a hashing algorithm for the digest operation.</span></span> <span data-ttu-id="953b5-114">Nous vous recommandons de sélectionner l’algorithme de hachage à partir d’un emplacement configurable qui peut être mis à jour par la suite sans qu’il soit nécessaire de modifier le code.</span><span class="sxs-lookup"><span data-stu-id="953b5-114">We recommend that the hashing algorithm be selected from a configurable location that can be subsequently updated without requiring changes to code.</span></span>
5.  <span data-ttu-id="953b5-115">Envoyer les données par le biais de la fonction de hachage à l’aide de l’algorithme de hachage, créant ainsi un [*hachage*](../secgloss/h-gly.md) (Digest) des données.</span><span class="sxs-lookup"><span data-stu-id="953b5-115">Send the data through the hashing function by using the hashing algorithm, thus creating a [*hash*](../secgloss/h-gly.md) (digest) of the data.</span></span>
6.  <span data-ttu-id="953b5-116">À l’aide de la [*clé privée*](../secgloss/p-gly.md) obtenue par le biais de la propriété sur le certificat, chiffrez le condensé et créez la signature.</span><span class="sxs-lookup"><span data-stu-id="953b5-116">Using the [*private key*](../secgloss/p-gly.md) obtained through the property on the certificate, encrypt the digest, creating the signature.</span></span>
7.  <span data-ttu-id="953b5-117">Incluez ce qui suit dans le message signé :</span><span class="sxs-lookup"><span data-stu-id="953b5-117">Include the following in the signed message:</span></span>

    -   <span data-ttu-id="953b5-118">Données signées</span><span class="sxs-lookup"><span data-stu-id="953b5-118">The signed data</span></span>
    -   <span data-ttu-id="953b5-119">Algorithme de hachage</span><span class="sxs-lookup"><span data-stu-id="953b5-119">The hash algorithm</span></span>
    -   <span data-ttu-id="953b5-120">La signature</span><span class="sxs-lookup"><span data-stu-id="953b5-120">The signature</span></span>
    -   <span data-ttu-id="953b5-121">Identificateur du signataire (émetteur et numéro de série du certificat)</span><span class="sxs-lookup"><span data-stu-id="953b5-121">The signer identifier (certificate issuer and serial number)</span></span>
    -   <span data-ttu-id="953b5-122">Le certificat du signataire (facultatif)</span><span class="sxs-lookup"><span data-stu-id="953b5-122">The signer's certificate (optional)</span></span>

<span data-ttu-id="953b5-123">Pour obtenir une procédure détaillée et un exemple, consultez [procédure de signature des données](procedure-for-signing-data.md) et [exemple de programme C : signature d’un message et vérification d’une signature de message](example-c-program-signing-a-message-and-verifying-a-message-signature.md).</span><span class="sxs-lookup"><span data-stu-id="953b5-123">For a detailed procedure and example, see [Procedure for Signing Data](procedure-for-signing-data.md) and [Example C Program: Signing a Message and Verifying a Message Signature](example-c-program-signing-a-message-and-verifying-a-message-signature.md).</span></span>

 

 
