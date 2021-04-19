---
description: Le système de fichiers EFS (Encrypted File System) fournit une protection par chiffrement des fichiers individuels sur les volumes de système de fichiers NTFS à l’aide d’un système à clé publique.
ms.assetid: 5f20109f-727d-44a9-90a1-0adc19b00d28
title: Chiffrement de fichier
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55c05d8d746e597fe180feffe25f7f553819e822
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106534744"
---
# <a name="file-encryption"></a><span data-ttu-id="98930-103">Chiffrement de fichier</span><span class="sxs-lookup"><span data-stu-id="98930-103">File Encryption</span></span>

<span data-ttu-id="98930-104">Le système de fichiers EFS (Encrypted File System) fournit un niveau supplémentaire de sécurité pour les fichiers et les répertoires.</span><span class="sxs-lookup"><span data-stu-id="98930-104">The Encrypted File System, or EFS, provides an additional level of security for files and directories.</span></span> <span data-ttu-id="98930-105">Il fournit une protection par chiffrement des fichiers individuels sur les volumes de système de fichiers NTFS à l’aide d’un système à clé publique.</span><span class="sxs-lookup"><span data-stu-id="98930-105">It provides cryptographic protection of individual files on NTFS file system volumes using a public-key system.</span></span>

<span data-ttu-id="98930-106">En règle générale, le contrôle d’accès aux objets de fichiers et d’annuaire fournis par le modèle de sécurité Windows est suffisant pour protéger l’accès non autorisé aux informations sensibles.</span><span class="sxs-lookup"><span data-stu-id="98930-106">Typically, the access control to file and directory objects provided by the Windows security model is sufficient to protect unauthorized access to sensitive information.</span></span> <span data-ttu-id="98930-107">Toutefois, si un ordinateur portable qui contient des données sensibles est perdu ou volé, la protection de la sécurité de ces données risque d’être compromise.</span><span class="sxs-lookup"><span data-stu-id="98930-107">However, if a laptop that contains sensitive data is lost or stolen, the security protection of that data may be compromised.</span></span> <span data-ttu-id="98930-108">Le chiffrement des fichiers augmente la sécurité.</span><span class="sxs-lookup"><span data-stu-id="98930-108">Encrypting the files increases security.</span></span>

<span data-ttu-id="98930-109">Pour déterminer si un système de fichiers prend en charge le chiffrement de fichier pour les fichiers et les répertoires, appelez la fonction [**GetVolumeInformation**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa) et examinez l’indicateur de bit de **\_ \_ chiffrement de fichier FS** .</span><span class="sxs-lookup"><span data-stu-id="98930-109">To determine whether a file system supports file encryption for files and directories, call the [**GetVolumeInformation**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa) function and examine the **FS\_FILE\_ENCRYPTION** bit flag.</span></span> <span data-ttu-id="98930-110">Notez que les éléments suivants ne peuvent pas être chiffrés :</span><span class="sxs-lookup"><span data-stu-id="98930-110">Note that the following items cannot be encrypted:</span></span>

-   <span data-ttu-id="98930-111">Fichiers compressés</span><span class="sxs-lookup"><span data-stu-id="98930-111">Compressed files</span></span>
-   <span data-ttu-id="98930-112">Fichiers système</span><span class="sxs-lookup"><span data-stu-id="98930-112">System files</span></span>
-   <span data-ttu-id="98930-113">Répertoires système</span><span class="sxs-lookup"><span data-stu-id="98930-113">System directories</span></span>
-   <span data-ttu-id="98930-114">Répertoires racine</span><span class="sxs-lookup"><span data-stu-id="98930-114">Root directories</span></span>
-   <span data-ttu-id="98930-115">Transactions</span><span class="sxs-lookup"><span data-stu-id="98930-115">Transactions</span></span>

<span data-ttu-id="98930-116">Les fichiers partiellement alloués peuvent être chiffrés.</span><span class="sxs-lookup"><span data-stu-id="98930-116">Sparse files can be encrypted.</span></span>

<span data-ttu-id="98930-117">TxF ne prend pas en charge la plupart des opérations sur les fichiers EFS (Encrypted File System).</span><span class="sxs-lookup"><span data-stu-id="98930-117">TxF does not support most operations on Encrypted File System (EFS) files.</span></span> <span data-ttu-id="98930-118">Les seules opérations prises en charge par TxF sont les opérations de lecture, telles que [**ReadEncryptedFileRaw**](/windows/desktop/api/WinBase/nf-winbase-readencryptedfileraw).</span><span class="sxs-lookup"><span data-stu-id="98930-118">The only operations TxF supports are read operations, such as [**ReadEncryptedFileRaw**](/windows/desktop/api/WinBase/nf-winbase-readencryptedfileraw).</span></span>

## <a name="in-this-section"></a><span data-ttu-id="98930-119">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="98930-119">In this section</span></span>



| <span data-ttu-id="98930-120">Rubrique</span><span class="sxs-lookup"><span data-stu-id="98930-120">Topic</span></span>                                                                                               | <span data-ttu-id="98930-121">Description</span><span class="sxs-lookup"><span data-stu-id="98930-121">Description</span></span>                                                                                                                                                              |
|-----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="98930-122">Gestion des fichiers et des répertoires chiffrés</span><span class="sxs-lookup"><span data-stu-id="98930-122">Handling Encrypted Files and Directories</span></span>](handling-encrypted-files-and-directories.md)<br/> | <span data-ttu-id="98930-123">Un fichier marqué comme chiffré est chiffré par le système de fichiers NTFS à l’aide du pilote de chiffrement actuel.</span><span class="sxs-lookup"><span data-stu-id="98930-123">A file marked encrypted is encrypted by the NTFS file system by using the current encryption driver.</span></span><br/>                                                          |
| [<span data-ttu-id="98930-124">Fichiers chiffrés et clés utilisateur</span><span class="sxs-lookup"><span data-stu-id="98930-124">Encrypted Files and User Keys</span></span>](encrypted-files-and-user-keys.md)<br/>                       | <span data-ttu-id="98930-125">Répertorie les fonctions à utiliser pour créer une nouvelle clé, ajouter une clé à un fichier chiffré, interroger les clés d’un fichier chiffré et supprimer des clés d’un fichier chiffré.</span><span class="sxs-lookup"><span data-stu-id="98930-125">Lists the functions to use to create a new key, add a key to an encrypted file, query the keys for an encrypted file, and remove keys from an encrypted file.</span></span><br/> |
| [<span data-ttu-id="98930-126">Sauvegarde et restauration de fichiers chiffrés</span><span class="sxs-lookup"><span data-stu-id="98930-126">Backup and Restore of Encrypted Files</span></span>](backup-and-restore-of-encrypted-files.md)<br/>       | <span data-ttu-id="98930-127">Les fonctions de chiffrement brutes permettent de sauvegarder des fichiers chiffrés.</span><span class="sxs-lookup"><span data-stu-id="98930-127">The raw encryption functions enable backup of encrypted files.</span></span><br/>                                                                                                |



 

<span data-ttu-id="98930-128">Pour plus d’informations sur le chiffrement, consultez [Ajout d’utilisateurs à un fichier chiffré](adding-users-to-an-encrypted-file.md).</span><span class="sxs-lookup"><span data-stu-id="98930-128">For more information about encryption, see [Adding Users to an Encrypted File](adding-users-to-an-encrypted-file.md).</span></span>

<span data-ttu-id="98930-129">Pour plus d’informations sur le chiffrement, consultez [chiffrement](/windows/desktop/SecCrypto/cryptography-portal).</span><span class="sxs-lookup"><span data-stu-id="98930-129">For more information about cryptography, see [Cryptography](/windows/desktop/SecCrypto/cryptography-portal).</span></span>

 

