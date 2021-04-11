---
title: Création d’une application de sauvegarde
description: Pour effectuer une entrée ou une sortie sur une bande, une application de sauvegarde doit d’abord obtenir un descripteur du périphérique à bandes. L’exemple de code suivant montre comment utiliser la fonction CreateFile pour ouvrir un périphérique à bandes.
ms.assetid: a2d367e1-13a9-47a8-8329-6e550c09ad58
keywords:
- Sauvegarde des applications de sauvegarde
- création d’une sauvegarde d’applications de sauvegarde
- sauvegarde de sauvegarde, création d’applications
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77409a0c74ee61e333b92dad8b22d9c68ed92eba
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031610"
---
# <a name="creating-a-backup-application"></a><span data-ttu-id="14f47-107">Création d’une application de sauvegarde</span><span class="sxs-lookup"><span data-stu-id="14f47-107">Creating a Backup Application</span></span>

<span data-ttu-id="14f47-108">Pour effectuer une entrée ou une sortie sur une bande, une application de sauvegarde doit d’abord obtenir un descripteur du périphérique à bandes.</span><span class="sxs-lookup"><span data-stu-id="14f47-108">To perform input or output on a tape, a backup application must first obtain a handle of the tape device.</span></span> <span data-ttu-id="14f47-109">L’exemple de code suivant montre comment utiliser la fonction [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) pour ouvrir un périphérique à bandes.</span><span class="sxs-lookup"><span data-stu-id="14f47-109">The following code sample shows you how to use the [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) function to open a tape device.</span></span>


```C++
HANDLE hTape;   // handle to tape device
 
hTape = CreateFile(TEXT("\\\\.\\TAPE0"),         // tape dev to open
                   GENERIC_READ | GENERIC_WRITE, // read/write access
                   0,                            // not used
                   0,                            // not used
                   OPEN_EXISTING,                // req for tape devs
                   0,                            // not used
                   NULL);                        // not used
```



<span data-ttu-id="14f47-110">Pour sauvegarder une arborescence de répertoires sur une bande, une application doit utiliser les fonctions [**FindFirstFile**](/windows/desktop/api/fileapi/nf-fileapi-findfirstfilea) et [**FindNextFile**](/windows/desktop/api/fileapi/nf-fileapi-findnextfilea) pour parcourir l’arborescence de répertoires.</span><span class="sxs-lookup"><span data-stu-id="14f47-110">To back up a directory tree to a tape, an application must use the [**FindFirstFile**](/windows/desktop/api/fileapi/nf-fileapi-findfirstfilea) and [**FindNextFile**](/windows/desktop/api/fileapi/nf-fileapi-findnextfilea) functions to traverse the directory tree.</span></span> <span data-ttu-id="14f47-111">Chaque fois qu’un fichier est trouvé, l’application doit obtenir les attributs de fichier à l’aide de la fonction [**GetFileAttributes**](/windows/desktop/api/fileapi/nf-fileapi-getfileattributesa) .</span><span class="sxs-lookup"><span data-stu-id="14f47-111">Each time a file is found, the application should get the file attributes by using the [**GetFileAttributes**](/windows/desktop/api/fileapi/nf-fileapi-getfileattributesa) function.</span></span>

<span data-ttu-id="14f47-112">S’il existe des liens physiques, une application doit déterminer le nombre de liens et enregistrer l’identificateur unique du fichier dans une table pour les comparaisons ultérieures.</span><span class="sxs-lookup"><span data-stu-id="14f47-112">If there are hard links, an application should determine the number of links, and save the unique identifier of the file in a table for future comparisons.</span></span> <span data-ttu-id="14f47-113">La première fois qu’un fichier est trouvé, l’application doit utiliser [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) pour ouvrir le fichier, et la fonction [**BackupRead**](/windows/desktop/api/Winbase/nf-winbase-backupread) pour commencer la sauvegarde.</span><span class="sxs-lookup"><span data-stu-id="14f47-113">The first time a file is found, the application should use [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) to open the file, and the [**BackupRead**](/windows/desktop/api/Winbase/nf-winbase-backupread) function to begin the backup.</span></span> <span data-ttu-id="14f47-114">Elle peut ensuite utiliser la fonction [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile) à plusieurs reprises pour transférer toutes les informations contenues dans la mémoire tampon utilisée par **BackupRead** à la bande.</span><span class="sxs-lookup"><span data-stu-id="14f47-114">Then it can use the [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile) function repeatedly to transfer all the information in the buffer used by **BackupRead** to the tape.</span></span> <span data-ttu-id="14f47-115">La deuxième fois qu’un fichier est trouvé (vérifié par rapport à la table des identificateurs de fichier en présence de liens physiques), l’application peut écrire les informations générales sur le fichier sur la bande, suivies d’un flux qui a un identificateur qui est un **\_ lien de sauvegarde**.</span><span class="sxs-lookup"><span data-stu-id="14f47-115">The second time a file is found (checked against the table of file identifiers when there are hard links), the application can write the general file information to the tape, followed by a stream that has an identifier that is **BACKUP\_LINK**.</span></span>

<span data-ttu-id="14f47-116">Lors de la restauration de fichiers à partir d’une bande sur un disque, une application doit utiliser les fonctions [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea), [**BackupWrite**](/windows/desktop/api/Winbase/nf-winbase-backupwrite)et [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) .</span><span class="sxs-lookup"><span data-stu-id="14f47-116">When restoring files from tape to disk, an application must use the [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea), [**BackupWrite**](/windows/desktop/api/Winbase/nf-winbase-backupwrite), and [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) functions.</span></span> <span data-ttu-id="14f47-117">Pour chaque fichier sur une bande, l’application doit utiliser **CreateFile** pour créer un nouveau fichier sur le disque, et **BackupWrite** pour commencer la restauration du fichier.</span><span class="sxs-lookup"><span data-stu-id="14f47-117">For each file on a tape, the application should use **CreateFile** to create a new file on disk, and **BackupWrite** to begin restoring the file.</span></span> <span data-ttu-id="14f47-118">L’application doit ensuite utiliser **ReadFile** à plusieurs reprises jusqu’à ce que toutes les informations du fichier soient lues à partir de la bande dans la mémoire tampon remplie par **BackupWrite**.</span><span class="sxs-lookup"><span data-stu-id="14f47-118">Then the application should use **ReadFile** repeatedly until all the information for the file is read from the tape into the buffer filled by **BackupWrite**.</span></span>

<span data-ttu-id="14f47-119">Si l’un des flux de la mémoire tampon [**BackupWrite**](/windows/desktop/api/Winbase/nf-winbase-backupwrite) a un identificateur de flux de **\_ lien de sauvegarde** , l’application doit établir un lien physique.</span><span class="sxs-lookup"><span data-stu-id="14f47-119">If one of the streams in the [**BackupWrite**](/windows/desktop/api/Winbase/nf-winbase-backupwrite) buffer has a **BACKUP\_LINK** stream identifier, the application must establish a hard link.</span></span> <span data-ttu-id="14f47-120">Si les données nécessaires pour établir le lien n’existent pas, **BackupWrite** échoue.</span><span class="sxs-lookup"><span data-stu-id="14f47-120">If the data needed to establish the link does not exist, **BackupWrite** fails.</span></span> <span data-ttu-id="14f47-121">L’application peut utiliser un catalogue préexistant pour rechercher et restaurer les données d’origine, ou elle peut informer l’utilisateur que les données de fichier à restaurer se trouvent dans un emplacement différent.</span><span class="sxs-lookup"><span data-stu-id="14f47-121">The application can use a pre-existing catalog to locate and restore the original data, or it can notify the user that the file data to be restored is in a different location.</span></span>

 

 