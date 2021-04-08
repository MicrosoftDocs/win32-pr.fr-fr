---
title: Cohérence du transfert de fichiers
description: BITS garantit que la version du fichier qu’il transfère est cohérente en fonction de la taille du fichier et de l’horodatage, et non du contenu (le service BITS ne protège pas contre les attaques de l’intercepteur).
ms.assetid: ba82f172-a3ac-49d6-bccd-7d0b68ba66de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 533bc0c0db9708528d4ae919572d6e4c1d251ac8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839361"
---
# <a name="file-transfer-consistency"></a><span data-ttu-id="acd29-103">Cohérence du transfert de fichiers</span><span class="sxs-lookup"><span data-stu-id="acd29-103">File Transfer Consistency</span></span>

<span data-ttu-id="acd29-104">BITS garantit que la version du fichier qu’il transfère est cohérente en fonction de la taille du fichier et de l’horodatage, et non du contenu (le service BITS ne protège pas contre les attaques de l’intercepteur).</span><span class="sxs-lookup"><span data-stu-id="acd29-104">BITS guarantees that the version of the file it transfers is consistent based on the file size and time stamp, not content (BITS does not protect against man-in-the-middle attacks).</span></span> <span data-ttu-id="acd29-105">Pour vérifier le contenu vous-même, vous pouvez utiliser la méthode [**IBackgroundCopyFile3 :: GetTemporaryName**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibackgroundcopyfile3-gettemporaryname) pour récupérer le nom du fichier qui contient le contenu téléchargé, vérifier le contenu à l’aide de votre propre mécanisme, puis appeler la méthode [**IBackgroundCopyFile3 :: SetValidationState**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibackgroundcopyfile3-setvalidationstate) pour indiquer à bits si le contenu du fichier est valide.</span><span class="sxs-lookup"><span data-stu-id="acd29-105">To verify the contents yourself, you can use the [**IBackgroundCopyFile3::GetTemporaryName**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibackgroundcopyfile3-gettemporaryname) method to get the name of the file that contains the downloaded content, verify the contents using your own mechanism, and then call the [**IBackgroundCopyFile3::SetValidationState**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibackgroundcopyfile3-setvalidationstate) method to indicate to BITS if the contents of the file is valid.</span></span> <span data-ttu-id="acd29-106">Si vous définissez l’état de validation sur **false** et que le contenu provient du serveur d’origine, le travail passe à l’état d’erreur.</span><span class="sxs-lookup"><span data-stu-id="acd29-106">If you set the validation state to **FALSE** and the content is from the origin server, the job goes into the error state.</span></span> <span data-ttu-id="acd29-107">Si le contenu provient d’un homologue, le service BITS télécharge le fichier à partir du serveur d’origine.</span><span class="sxs-lookup"><span data-stu-id="acd29-107">If the content is from a peer, BITS downloads the file from the origin server.</span></span>

<span data-ttu-id="acd29-108">Pour les téléchargements, si la taille du fichier ou l’horodatage change alors que BITS transfère le fichier, BITS redémarre le transfert de ce fichier uniquement.</span><span class="sxs-lookup"><span data-stu-id="acd29-108">For downloads, if the file size or time stamp changes while BITS is transferring the file, BITS restarts the transfer of that file only.</span></span> <span data-ttu-id="acd29-109">Par exemple, si le travail de téléchargement contient deux fichiers et que les fichiers sont mis à jour sur le serveur pendant que BITS transfère le deuxième fichier, BITS redémarre le transfert du deuxième fichier uniquement.</span><span class="sxs-lookup"><span data-stu-id="acd29-109">For example, if the download job contains two files and the files are updated on the server while BITS is transferring the second file, BITS restarts the transfer of the second file only.</span></span> <span data-ttu-id="acd29-110">Le premier fichier, qui a déjà été transféré avec succès, n’est pas mis à jour pour refléter les nouvelles modifications.</span><span class="sxs-lookup"><span data-stu-id="acd29-110">The first file, which already transferred successfully, is not updated to reflect the new changes.</span></span>

<span data-ttu-id="acd29-111">Notez que si vous êtes le propriétaire du fichier téléchargé à partir du serveur, vous devez créer une nouvelle URL pour chaque nouvelle version du fichier.</span><span class="sxs-lookup"><span data-stu-id="acd29-111">Note that if you own the file being downloaded from the server, you should create a new URL for each new version of the file.</span></span> <span data-ttu-id="acd29-112">Si vous utilisez la même URL pour les nouvelles versions du fichier, certains serveurs proxy peuvent servir des données obsolètes à partir de leur cache, car ils ne vérifient pas avec le serveur d’origine si le fichier est périmé.</span><span class="sxs-lookup"><span data-stu-id="acd29-112">If you use the same URL for new versions of the file, some proxy servers may serve stale data from their cache because they do not verify with the original server if the file is stale.</span></span>

<span data-ttu-id="acd29-113">Pour les téléchargements, si la taille du fichier ou l’horodatage change pendant le transfert de fichiers, BITS génère une erreur et le travail est placé dans l' \_ État d’erreur d’état de la tâche BG \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="acd29-113">For uploads, if the file size or time stamp changes during the file transfer, BITS generates an error and the job is placed in the BG\_JOB\_STATE\_ERROR state.</span></span>

<span data-ttu-id="acd29-114">Le service BITS ne synchronise pas les demandes de transfert lorsqu’un ou plusieurs utilisateurs demandent que le même fichier soit transféré au même emplacement.</span><span class="sxs-lookup"><span data-stu-id="acd29-114">BITS does not synchronize transfer requests when one or more users request that the same file be transferred to the same location.</span></span> <span data-ttu-id="acd29-115">BITS transfère le fichier pour chaque demande séparément.</span><span class="sxs-lookup"><span data-stu-id="acd29-115">BITS transfers the file for each request separately.</span></span>

 

 




