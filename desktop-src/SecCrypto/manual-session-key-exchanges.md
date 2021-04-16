---
description: Montre comment envoyer un message chiffré.
ms.assetid: 928b1863-7a54-4bf0-b447-85b8c2868bcd
title: Échange de clés de session manuelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0114f8173084126a72519d291158f15f3e1c171
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104556695"
---
# <a name="manual-session-key-exchanges"></a><span data-ttu-id="d0bb2-103">Échange de clés de session manuelle</span><span class="sxs-lookup"><span data-stu-id="d0bb2-103">Manual Session Key Exchanges</span></span>

> [!Note]  
> <span data-ttu-id="d0bb2-104">La procédure décrite dans cette section suppose que les utilisateurs (ou les clients CryptoAPI) possèdent déjà leur propre ensemble de [*paires de clés publiques/privées*](../secgloss/p-gly.md) et ont également obtenu les [*clés publiques*](../secgloss/p-gly.md)de l’autre.</span><span class="sxs-lookup"><span data-stu-id="d0bb2-104">The procedure described in this section assumes that the users (or CryptoAPI clients) already possess their own set of [*public/private key pairs*](../secgloss/p-gly.md) and have also obtained each other's [*public keys*](../secgloss/p-gly.md).</span></span>

 

<span data-ttu-id="d0bb2-105">L’illustration suivante montre comment utiliser cette procédure pour envoyer un message chiffré.</span><span class="sxs-lookup"><span data-stu-id="d0bb2-105">The following illustration shows how to use this procedure to send an encrypted message.</span></span>

![envoi d’un message chiffré](images/capi04.png)

<span data-ttu-id="d0bb2-107">Cette approche est vulnérable à au moins une forme d’attaque courante.</span><span class="sxs-lookup"><span data-stu-id="d0bb2-107">This approach is vulnerable to at least one common form of attack.</span></span> <span data-ttu-id="d0bb2-108">Une personne malveillante peut acquérir des copies d’un ou de plusieurs messages chiffrés et de clés chiffrées.</span><span class="sxs-lookup"><span data-stu-id="d0bb2-108">An eavesdropper can acquire copies of one or more encrypted messages and the encrypted keys.</span></span> <span data-ttu-id="d0bb2-109">Ensuite, plus tard, l’écouteur peut envoyer l’un de ces messages au récepteur et le destinataire n’aura aucun moyen de savoir que le message ne provient pas directement de l’expéditeur d’origine.</span><span class="sxs-lookup"><span data-stu-id="d0bb2-109">Then, at some later time, the eavesdropper can send one of these messages to the receiver and the receiver will have no way of knowing the message did not come directly from the original sender.</span></span> <span data-ttu-id="d0bb2-110">Ce risque peut être réduit en horodateurant tous les messages ou en utilisant des numéros de série.</span><span class="sxs-lookup"><span data-stu-id="d0bb2-110">This risk can be reduced by time-stamping all messages or by using serial numbers.</span></span>

<span data-ttu-id="d0bb2-111">Le moyen le plus simple d’envoyer des messages chiffrés à un autre utilisateur consiste à envoyer le message chiffré à l’aide d’une clé de session aléatoire avec la clé de session chiffrée avec la clé [*publique d’échange de clé*](../secgloss/k-gly.md)du récepteur.</span><span class="sxs-lookup"><span data-stu-id="d0bb2-111">The easiest way to send encrypted messages to another user is to send the message encrypted with a random session key along with the session key encrypted with the receiver's [*key exchange public key*](../secgloss/k-gly.md).</span></span>

<span data-ttu-id="d0bb2-112">Voici les étapes à suivre pour envoyer une clé de session chiffrée.</span><span class="sxs-lookup"><span data-stu-id="d0bb2-112">Following are the steps for sending an encrypted session key.</span></span>

<span data-ttu-id="d0bb2-113">**Pour envoyer une clé de session chiffrée**</span><span class="sxs-lookup"><span data-stu-id="d0bb2-113">**To send an encrypted session key**</span></span>

1.  <span data-ttu-id="d0bb2-114">Créez une [*clé de session*](../secgloss/s-gly.md) aléatoire à l’aide de la fonction [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) .</span><span class="sxs-lookup"><span data-stu-id="d0bb2-114">Create a random [*session key*](../secgloss/s-gly.md) by using the [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) function.</span></span>
2.  <span data-ttu-id="d0bb2-115">Chiffrez le message à l’aide de la clé de session.</span><span class="sxs-lookup"><span data-stu-id="d0bb2-115">Encrypt the message by using the session key.</span></span> <span data-ttu-id="d0bb2-116">Cette procédure est décrite dans [chiffrement et déchiffrement des données](data-encryption-and-decryption.md).</span><span class="sxs-lookup"><span data-stu-id="d0bb2-116">This procedure is discussed in [Data Encryption and Decryption](data-encryption-and-decryption.md).</span></span>
3.  <span data-ttu-id="d0bb2-117">Exportez la clé de session dans un [*objet blob de clé*](../secgloss/k-gly.md) avec la fonction [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) , en spécifiant que la clé doit être chiffrée avec la clé publique d’échange de clé de l’utilisateur de destination.</span><span class="sxs-lookup"><span data-stu-id="d0bb2-117">Export the session key into a [*key BLOB*](../secgloss/k-gly.md) with the [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) function, specifying that the key be encrypted with the destination user's key exchange public key.</span></span>
4.  <span data-ttu-id="d0bb2-118">Envoyez le message chiffré et l’objet BLOB de clé chiffrée à l’utilisateur de destination.</span><span class="sxs-lookup"><span data-stu-id="d0bb2-118">Send both the encrypted message and the encrypted key BLOB to the destination user.</span></span>
5.  <span data-ttu-id="d0bb2-119">L’utilisateur de destination importe l’objet BLOB de clé dans son CSP à l’aide de la fonction [**CryptImportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey) .</span><span class="sxs-lookup"><span data-stu-id="d0bb2-119">The destination user imports the key BLOB into his or her CSP by using the [**CryptImportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey) function.</span></span> <span data-ttu-id="d0bb2-120">Cette opération déchiffre automatiquement la clé de session, à condition que la clé publique d’échange de clé de l’utilisateur de destination ait été spécifiée à l’étape 3.</span><span class="sxs-lookup"><span data-stu-id="d0bb2-120">This will automatically decrypt the session key, provided the destination user's key exchange public key was specified in step 3.</span></span>
6.  <span data-ttu-id="d0bb2-121">L’utilisateur de destination peut ensuite déchiffrer le message à l’aide de la clé de session, en suivant la procédure décrite dans [chiffrement et déchiffrement des données](data-encryption-and-decryption.md).</span><span class="sxs-lookup"><span data-stu-id="d0bb2-121">The destination user can then decrypt the message by using the session key, following the procedure discussed in [Data Encryption and Decryption](data-encryption-and-decryption.md).</span></span>

 

 
