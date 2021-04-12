---
description: Décrit comment les points d’analyse activent le comportement du système de fichiers qui fait partie du comportement de la plupart des développeurs Windows.
ms.assetid: 1aaebda9-0013-4282-9ae1-7c829e171942
title: Points d’analyse et opérations sur les fichiers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be1132197cd689157cd9f219afa5bfc1474b587c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104209722"
---
# <a name="reparse-points-and-file-operations"></a><span data-ttu-id="255b4-103">Points d’analyse et opérations sur les fichiers</span><span class="sxs-lookup"><span data-stu-id="255b4-103">Reparse Points and File Operations</span></span>

<span data-ttu-id="255b4-104">Les *points d’analyse* activent le comportement du système de fichiers qui fait partie du comportement auquel la plupart des développeurs Windows peuvent être habitués. par conséquent, la connaissance de ces comportements lors de l’écriture d’applications qui manipulent des fichiers est vitale pour les applications fiables et fiables destinées à accéder aux systèmes de fichiers qui prennent en charge les points d’analyse.</span><span class="sxs-lookup"><span data-stu-id="255b4-104">*Reparse points* enable file system behavior that departs from the behavior most Windows developers may be accustomed to, therefore being aware of these behaviors when writing applications that manipulate files is vital to robust and reliable applications intended to access file systems that support reparse points.</span></span> <span data-ttu-id="255b4-105">L’étendue de ces considérations dépend de l’implémentation spécifique et du comportement de filtre du système de fichiers associé d’un point d’analyse particulier, qui peut être défini par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="255b4-105">The extent of these considerations will depend on the specific implementation and associated file system filter behavior of a particular reparse point, which can be user-defined.</span></span> <span data-ttu-id="255b4-106">Pour plus d’informations, consultez [points d’analyse](reparse-points.md).</span><span class="sxs-lookup"><span data-stu-id="255b4-106">For more information, see [Reparse Points](reparse-points.md).</span></span>

<span data-ttu-id="255b4-107">Tenez compte des exemples suivants concernant les implémentations du point d’analyse NTFS, notamment les dossiers montés, les fichiers liés et le serveur de stockage distant Microsoft :</span><span class="sxs-lookup"><span data-stu-id="255b4-107">Consider the following examples regarding NTFS reparse point implementations, which include mounted folders, linked files, and the Microsoft Remote Storage Server:</span></span>

-   <span data-ttu-id="255b4-108">Les applications de sauvegarde qui utilisent des [flux de fichier](file-streams.md) doivent spécifier des **\_ \_ données d’analyse de sauvegarde** dans la structure d' [**\_ \_ ID de flux Win32**](/windows/desktop/api/winbase/ns-winbase-win32_stream_id) lors de la sauvegarde de fichiers avec des points d’analyse.</span><span class="sxs-lookup"><span data-stu-id="255b4-108">Backup applications that use [file streams](file-streams.md) should specify **BACKUP\_REPARSE\_DATA** in the [**WIN32\_STREAM\_ID**](/windows/desktop/api/winbase/ns-winbase-win32_stream_id) structure when backing up files with reparse points.</span></span>
-   <span data-ttu-id="255b4-109">Les applications qui utilisent la fonction [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) doivent spécifier l’indicateur de fichier ouvrir l’indicateur de **\_ \_ \_ \_ point d’analyse** lors de l’ouverture du fichier s’il s’agit d’un point d’analyse.</span><span class="sxs-lookup"><span data-stu-id="255b4-109">Applications that use the [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) function should specify the **FILE\_FLAG\_OPEN\_REPARSE\_POINT** flag when opening the file if it is a reparse point.</span></span> <span data-ttu-id="255b4-110">Pour plus d’informations, consultez [création et ouverture de fichiers](creating-and-opening-files.md).</span><span class="sxs-lookup"><span data-stu-id="255b4-110">For more information, see [Creating and Opening Files](creating-and-opening-files.md).</span></span>
-   <span data-ttu-id="255b4-111">Le processus de [défragmentation des fichiers](defragmenting-files.md) nécessite une gestion spéciale des points d’analyse.</span><span class="sxs-lookup"><span data-stu-id="255b4-111">The process of [defragmenting files](defragmenting-files.md) requires special handling for reparse points.</span></span>
-   <span data-ttu-id="255b4-112">Les applications de détection de virus doivent rechercher les points d’analyse qui indiquent des fichiers liés.</span><span class="sxs-lookup"><span data-stu-id="255b4-112">Virus detection applications should search for reparse points that indicate linked files.</span></span>
-   <span data-ttu-id="255b4-113">La plupart des applications doivent prendre des mesures spéciales pour les fichiers qui ont été déplacés vers un stockage à long terme, si uniquement pour informer l’utilisateur qu’il peut prendre un certain temps pour récupérer le fichier.</span><span class="sxs-lookup"><span data-stu-id="255b4-113">Most applications should take special actions for files that have been moved to long-term storage, if only to notify the user that it may take a while to retrieve the file.</span></span>
-   <span data-ttu-id="255b4-114">La fonction [**OpenFileById**](/windows/desktop/api/WinBase/nf-winbase-openfilebyid) ouvre le fichier ou le point d’analyse, en fonction de l’utilisation de l’indicateur de **fichier ouvrir l’indicateur de \_ \_ \_ \_ point d’analyse** .</span><span class="sxs-lookup"><span data-stu-id="255b4-114">The [**OpenFileById**](/windows/desktop/api/WinBase/nf-winbase-openfilebyid) function will either open the file or the reparse point, depending on the use of the **FILE\_FLAG\_OPEN\_REPARSE\_POINT** flag.</span></span>
-   <span data-ttu-id="255b4-115">Les liens symboliques, en tant que points d’analyse, ont certaines [considérations de programmation](symbolic-link-programming-considerations.md) spécifiques.</span><span class="sxs-lookup"><span data-stu-id="255b4-115">Symbolic links, as reparse points, have certain [programming considerations](symbolic-link-programming-considerations.md) specific to them.</span></span>
-   <span data-ttu-id="255b4-116">Les activités de gestion des volumes pour la lecture des enregistrements du journal des modifications du numéro de séquence de mise à jour nécessitent un traitement spécial des points d’analyse lors de l’utilisation de l' [**\_ enregistrement USN**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v2) et de la lecture des structures de [**\_ \_ \_ données du journal USN**](/windows/desktop/api/WinIoCtl/ns-winioctl-read_usn_journal_data_v0) .</span><span class="sxs-lookup"><span data-stu-id="255b4-116">Volume management activities for reading update sequence number (USN) change journal records require special handling for reparse points when using the [**USN\_RECORD**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v2) and [**READ\_USN\_JOURNAL\_DATA**](/windows/desktop/api/WinIoCtl/ns-winioctl-read_usn_journal_data_v0) structures.</span></span>

## <a name="related-topics"></a><span data-ttu-id="255b4-117">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="255b4-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="255b4-118">Déterminer si un répertoire est un dossier monté</span><span class="sxs-lookup"><span data-stu-id="255b4-118">Determining Whether a Directory Is a Mounted Folder</span></span>](determining-whether-a-directory-is-a-volume-mount-point.md)
</dt> <dt>

[<span data-ttu-id="255b4-119">Création de dossiers montés</span><span class="sxs-lookup"><span data-stu-id="255b4-119">Creating Mounted Folders</span></span>](mounting-and-dismounting-a-volume.md)
</dt> <dt>

[<span data-ttu-id="255b4-120">Effets de liens symboliques sur les fonctions des systèmes de fichiers</span><span class="sxs-lookup"><span data-stu-id="255b4-120">Symbolic Link Effects on File Systems Functions</span></span>](symbolic-link-effects-on-file-systems-functions.md)
</dt> </dl>

 

 
