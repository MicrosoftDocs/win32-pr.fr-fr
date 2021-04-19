---
description: Explique la procédure utilisée pour stocker une clé de session.
ms.assetid: 9ab7f747-9c69-40b5-af78-163f3ba315bf
title: Stockage d’une clé de session
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3b17de657ddba47dd77f68c1ee7a2adfdf93e7f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106524681"
---
# <a name="storing-a-session-key"></a><span data-ttu-id="1d70e-103">Stockage d’une clé de session</span><span class="sxs-lookup"><span data-stu-id="1d70e-103">Storing a Session Key</span></span>

> [!Note]  
> <span data-ttu-id="1d70e-104">Cette section part du principe que les utilisateurs possèdent un ensemble de [*paires de clés publiques/privées*](../secgloss/p-gly.md).</span><span class="sxs-lookup"><span data-stu-id="1d70e-104">This section assumes that users possess a set of [*public/private key pairs*](../secgloss/p-gly.md).</span></span> <span data-ttu-id="1d70e-105">Vous trouverez des instructions et un exemple de création de paires de clés dans l' [exemple de programme C : création d’un conteneur de clé et génération de clés](example-c-program-creating-a-key-container-and-generating-keys.md).</span><span class="sxs-lookup"><span data-stu-id="1d70e-105">Instructions and an example for creating key pairs can be found in [Example C Program: Creating a Key Container and Generating Keys](example-c-program-creating-a-key-container-and-generating-keys.md).</span></span>

 

<span data-ttu-id="1d70e-106">**Pour stocker une clé de session**</span><span class="sxs-lookup"><span data-stu-id="1d70e-106">**To store a session key**</span></span>

1.  <span data-ttu-id="1d70e-107">Créez un [*objet blob de clé*](../secgloss/k-gly.md) simple à l’aide de la fonction [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) .</span><span class="sxs-lookup"><span data-stu-id="1d70e-107">Create a simple [*key BLOB*](../secgloss/k-gly.md) by using the [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) function.</span></span> <span data-ttu-id="1d70e-108">Cela permet de transférer la clé de session du CSP vers l’espace mémoire d’une application.</span><span class="sxs-lookup"><span data-stu-id="1d70e-108">This will transfer the session key from the CSP to an application's memory space.</span></span> <span data-ttu-id="1d70e-109">Spécifie qu’une clé publique Exchange doit être utilisée pour signer l’objet BLOB de clé.</span><span class="sxs-lookup"><span data-stu-id="1d70e-109">Specify that an exchange public key be used to sign the key BLOB.</span></span>
2.  <span data-ttu-id="1d70e-110">Stockez l’objet BLOB de clé signée sur le disque.</span><span class="sxs-lookup"><span data-stu-id="1d70e-110">Store the signed key BLOB to disk.</span></span> <span data-ttu-id="1d70e-111">Il est supposé que tous les disques sont non sécurisés.</span><span class="sxs-lookup"><span data-stu-id="1d70e-111">It is assumed that all disks are nonsecure.</span></span>
3.  <span data-ttu-id="1d70e-112">Lorsque la clé est nécessaire, lisez l’objet BLOB de clé à partir du disque.</span><span class="sxs-lookup"><span data-stu-id="1d70e-112">When the key is needed, read the key BLOB from disk.</span></span>
4.  <span data-ttu-id="1d70e-113">Importez à nouveau l’objet BLOB de clé dans le CSP à l’aide de la fonction [**CryptImportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey) .</span><span class="sxs-lookup"><span data-stu-id="1d70e-113">Import the key BLOB back into the CSP by using the [**CryptImportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey) function.</span></span>

<span data-ttu-id="1d70e-114">Pour obtenir un exemple de création d’une [*clé de session*](../secgloss/s-gly.md) et d’exportation de cette clé vers un [*objet blob de clé simple*](../secgloss/s-gly.md) pouvant être écrit dans un fichier sur disque, consultez [exemple de programme C : exportation d’une clé de session](example-c-program-exporting-a-session-key.md).</span><span class="sxs-lookup"><span data-stu-id="1d70e-114">For an example of creating a [*session key*](../secgloss/s-gly.md) and exporting that key to a [*simple key BLOB*](../secgloss/s-gly.md) that can be written to a disk file, see [Example C Program: Exporting a Session Key](example-c-program-exporting-a-session-key.md).</span></span>

<span data-ttu-id="1d70e-115">Cette procédure fournit uniquement une sécurité minimale.</span><span class="sxs-lookup"><span data-stu-id="1d70e-115">This procedure provides only minimal security.</span></span> <span data-ttu-id="1d70e-116">Si la clé de session stockée sera utilisée pour chiffrer les données à une date ultérieure, la procédure précédente ne fournit pas de sécurité adéquate.</span><span class="sxs-lookup"><span data-stu-id="1d70e-116">If the stored session key will be used to encrypt data at a later date, the preceding procedure does not provide adequate security.</span></span>

<span data-ttu-id="1d70e-117">Pour renforcer la sécurité, signez l’objet BLOB de clé avec une clé privée Exchange avant qu’il ne soit stocké sur le disque.</span><span class="sxs-lookup"><span data-stu-id="1d70e-117">To provide greater security, sign the key BLOB with an exchange private key before it is stored to disk.</span></span> <span data-ttu-id="1d70e-118">Lorsque l’objet BLOB de clé est lu ultérieurement à partir du disque, sa signature peut être validée pour s’assurer que l’objet BLOB de clé est intact.</span><span class="sxs-lookup"><span data-stu-id="1d70e-118">When the key BLOB is later read from disk, its signature can be validated to ensure that the key BLOB is intact.</span></span>

<span data-ttu-id="1d70e-119">Si l’objet BLOB de clé n’est pas signé, toute personne ayant accès au disque ou à un autre support où la clé est stockée peut créer une nouvelle clé de session.</span><span class="sxs-lookup"><span data-stu-id="1d70e-119">If the key BLOB is not signed, anyone with access to the disk or other media where the key is stored can create a new session key.</span></span>

<span data-ttu-id="1d70e-120">La nouvelle clé de session peut être chiffrée avec la [*clé d’échange*](../secgloss/e-gly.md)de [*clé publique*](../secgloss/p-gly.md) de l’utilisateur d’origine, et cette nouvelle clé peut être substituée à l’original.</span><span class="sxs-lookup"><span data-stu-id="1d70e-120">The new session key can be encrypted with the original user's [*public key*](../secgloss/p-gly.md) [*exchange key*](../secgloss/e-gly.md), and this new key can be substituted for the original.</span></span> <span data-ttu-id="1d70e-121">Si l’utilisateur a déjà utilisé la clé de session substituée pour chiffrer les fichiers et les messages, la personne qui a créé la clé de substitution peut facilement les déchiffrer.</span><span class="sxs-lookup"><span data-stu-id="1d70e-121">If the user unknowingly used the substituted session key to encrypt files and messages, the individual who created the substitute key could easily decrypt them.</span></span>

<span data-ttu-id="1d70e-122">Les signatures numériques sont décrites en détail dans [hachages et signatures numériques](hashes-and-digital-signatures.md).</span><span class="sxs-lookup"><span data-stu-id="1d70e-122">Digital signatures are discussed in detail in [Hashes and Digital Signatures](hashes-and-digital-signatures.md).</span></span>

 

 
