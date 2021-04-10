---
description: Les exemples suivants utilisent les fonctions de gestion de fichiers.
ms.assetid: 0879898b-b661-48b3-af94-9ba24811503f
title: Utilisation de la gestion des fichiers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88838ee99dde16c5c2288c00e2e2f3b35747dae5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104035096"
---
# <a name="using-file-management"></a><span data-ttu-id="9ac97-103">Utilisation de la gestion des fichiers</span><span class="sxs-lookup"><span data-stu-id="9ac97-103">Using File Management</span></span>

<span data-ttu-id="9ac97-104">Les exemples suivants utilisent les fonctions de gestion de fichiers.</span><span class="sxs-lookup"><span data-stu-id="9ac97-104">The following samples use the file management functions.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="9ac97-105">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="9ac97-105">In this section</span></span>



| <span data-ttu-id="9ac97-106">Rubrique</span><span class="sxs-lookup"><span data-stu-id="9ac97-106">Topic</span></span>                                                                                                   | <span data-ttu-id="9ac97-107">Description</span><span class="sxs-lookup"><span data-stu-id="9ac97-107">Description</span></span>                                                                                                                                                                                      |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9ac97-108">Ajout d’utilisateurs à un fichier chiffré</span><span class="sxs-lookup"><span data-stu-id="9ac97-108">Adding Users to an Encrypted File</span></span>](adding-users-to-an-encrypted-file.md)<br/>                   | <span data-ttu-id="9ac97-109">Exemple de code qui montre comment ajouter un nouvel utilisateur à un fichier chiffré existant à l’aide de la fonction [**AddUsersToEncryptedFile**](/windows/desktop/api/Winefs/nf-winefs-adduserstoencryptedfile) .</span><span class="sxs-lookup"><span data-stu-id="9ac97-109">Example code that shows how to add a new user to an existing encrypted file by using the [**AddUsersToEncryptedFile**](/windows/desktop/api/Winefs/nf-winefs-adduserstoencryptedfile) function.</span></span><br/>                         |
| [<span data-ttu-id="9ac97-110">Ajout d’un fichier à un autre fichier</span><span class="sxs-lookup"><span data-stu-id="9ac97-110">Appending One File to Another File</span></span>](appending-one-file-to-another-file.md)<br/>                 | <span data-ttu-id="9ac97-111">Exemple de code qui montre comment une application peut ajouter un fichier à la fin d’un autre fichier, y compris comment ouvrir et fermer des fichiers, lire et écrire dans des fichiers, et verrouiller et déverrouiller des fichiers.</span><span class="sxs-lookup"><span data-stu-id="9ac97-111">Example code that shows how an application can append one file to the end of another file, including how to open and close files, read and write to files, and lock and unlock files.</span></span><br/> |
| [<span data-ttu-id="9ac97-112">Création et utilisation d’un fichier temporaire</span><span class="sxs-lookup"><span data-stu-id="9ac97-112">Creating and Using a Temporary File</span></span>](creating-and-using-a-temporary-file.md)<br/>               | <span data-ttu-id="9ac97-113">Exemple de code qui montre comment créer un fichier temporaire à des fins de manipulation de données à l’aide des fonctions GetTempFileName et GetTempPath.</span><span class="sxs-lookup"><span data-stu-id="9ac97-113">Example code that shows how to create a temporary file for data manipulation purposes by using the GetTempFileName and GetTempPath functions.</span></span><br/>                                         |
| [<span data-ttu-id="9ac97-114">Verrouillage et déverrouillage des plages d’octets dans les fichiers</span><span class="sxs-lookup"><span data-stu-id="9ac97-114">Locking and Unlocking Byte Ranges in Files</span></span>](locking-and-unlocking-byte-ranges-in-files.md)<br/> | <span data-ttu-id="9ac97-115">Exemple de code illustrant le verrouillage et le déverrouillage de la plage d’octets à l’aide des fonctions LockFileEx et UnlockFileEx.</span><span class="sxs-lookup"><span data-stu-id="9ac97-115">Example code that shows byte range locking and unlocking by using the LockFileEx and UnlockFileEx functions.</span></span><br/>                                                                          |
| [<span data-ttu-id="9ac97-116">Ouverture d’un fichier pour la lecture ou l’écriture</span><span class="sxs-lookup"><span data-stu-id="9ac97-116">Opening a File for Reading or Writing</span></span>](opening-a-file-for-reading-or-writing.md)<br/>           | <span data-ttu-id="9ac97-117">Exemple de code qui montre comment utiliser la fonction CreateFile pour créer un nouveau fichier ou ouvrir un fichier existant.</span><span class="sxs-lookup"><span data-stu-id="9ac97-117">Example code that shows how to use the CreateFile function to create a new file or open an existing file.</span></span><br/>                                                                             |
| [<span data-ttu-id="9ac97-118">Récupération et modification des attributs de fichier</span><span class="sxs-lookup"><span data-stu-id="9ac97-118">Retrieving and Changing File Attributes</span></span>](retrieving-and-changing-file-attributes.md)<br/>       | <span data-ttu-id="9ac97-119">Exemple de code qui montre comment utiliser la fonction GetFileAttributesEx pour récupérer des attributs de fichier.</span><span class="sxs-lookup"><span data-stu-id="9ac97-119">Example code that shows how to use the GetFileAttributesEx function to retrieve file attributes.</span></span><br/>                                                                                      |
| [<span data-ttu-id="9ac97-120">Test de la fin d’un fichier</span><span class="sxs-lookup"><span data-stu-id="9ac97-120">Testing for the End of a File</span></span>](testing-for-the-end-of-a-file.md)<br/>                           | <span data-ttu-id="9ac97-121">Exemple de code qui montre comment tester la fin du fichier pendant une opération de lecture synchrone et pendant une opération de lecture asynchrone.</span><span class="sxs-lookup"><span data-stu-id="9ac97-121">Example code that shows how to test for the end of file during a synchronous read operation and during an asynchronous read operation.</span></span><br/>                                                |
| [<span data-ttu-id="9ac97-122">Utilisation des flux</span><span class="sxs-lookup"><span data-stu-id="9ac97-122">Using Streams</span></span>](using-streams.md)<br/>                                                           | <span data-ttu-id="9ac97-123">Exemple de code qui montre comment utiliser les flux de base du système de fichiers NTFS.</span><span class="sxs-lookup"><span data-stu-id="9ac97-123">Example code that shows how to use basic NTFS file system streams.</span></span><br/>                                                                                                                    |



 

 

 




