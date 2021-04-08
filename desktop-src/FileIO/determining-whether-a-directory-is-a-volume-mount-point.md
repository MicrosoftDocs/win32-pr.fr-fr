---
description: Comment déterminer si un répertoire spécifié est un dossier monté.
ms.assetid: b4a2c3d7-8805-41de-b316-592e77076570
title: Déterminer si un répertoire est un dossier monté
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ca7492a3114ff0c9c9ce0685c6d3e2b94724457
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867697"
---
# <a name="determining-whether-a-directory-is-a-mounted-folder"></a><span data-ttu-id="06136-103">Déterminer si un répertoire est un dossier monté</span><span class="sxs-lookup"><span data-stu-id="06136-103">Determining Whether a Directory Is a Mounted Folder</span></span>

<span data-ttu-id="06136-104">Il est utile de déterminer si un répertoire est un dossier monté lorsque, par exemple, vous utilisez une application de sauvegarde ou de recherche limitée à un volume.</span><span class="sxs-lookup"><span data-stu-id="06136-104">It is useful to determine whether a directory is a mounted folder when, for example, you are using a backup or search application that is limited to one volume.</span></span> <span data-ttu-id="06136-105">Une telle application peut atteindre des informations sur plusieurs volumes si vous utilisez des fonctions telles que [**SetVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa) pour créer des dossiers montés pour les autres volumes sur le volume auquel l’application est limitée.</span><span class="sxs-lookup"><span data-stu-id="06136-105">Such an application can reach information on multiple volumes if you use functions such as [**SetVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa) to create mounted folders for the other volumes on the volume that the application is limited to.</span></span> <span data-ttu-id="06136-106">Pour plus d’informations, consultez [création de dossiers montés](mounting-and-dismounting-a-volume.md).</span><span class="sxs-lookup"><span data-stu-id="06136-106">For more information, see [Creating Mounted Folders](mounting-and-dismounting-a-volume.md).</span></span>

<span data-ttu-id="06136-107">Pour déterminer si un répertoire spécifié est un dossier monté, appelez d’abord la fonction [**GetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesa) , puis examinez l’indicateur de point d’analyse d’attribut de fichier dans la valeur de retour pour voir si le répertoire a un point d’analyse associé. **\_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="06136-107">To determine if a specified directory is a mounted folder, first call the [**GetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesa) function and inspect the **FILE\_ATTRIBUTE\_REPARSE\_POINT** flag in the return value to see if the directory has an associated reparse point.</span></span> <span data-ttu-id="06136-108">Si c’est le cas, utilisez les fonctions [**FindFirstFile**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea) et [**FindNextFile**](/windows/desktop/api/FileAPI/nf-fileapi-findnextfilea) pour obtenir la balise d’analyse dans le membre **dwReserved0** de la structure de [**\_ \_ données de recherche Win32**](/windows/desktop/api/MinWinBase/ns-minwinbase-win32_find_dataa) .</span><span class="sxs-lookup"><span data-stu-id="06136-108">If it does, use the [**FindFirstFile**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea) and [**FindNextFile**](/windows/desktop/api/FileAPI/nf-fileapi-findnextfilea) functions to obtain the reparse tag in the **dwReserved0** member of the [**WIN32\_FIND\_DATA**](/windows/desktop/api/MinWinBase/ns-minwinbase-win32_find_dataa) structure.</span></span> <span data-ttu-id="06136-109">Pour déterminer si le point d’analyse est un dossier monté (et non une autre forme de point d’analyse), testez si la valeur de balise est égale au **point de montage d’étiquette d’analyse d’e/s \_ \_ \_ \_** de valeur.</span><span class="sxs-lookup"><span data-stu-id="06136-109">To determine if the reparse point is a mounted folder (and not some other form of reparse point), test whether the tag value equals the value **IO\_REPARSE\_TAG\_MOUNT\_POINT**.</span></span> <span data-ttu-id="06136-110">Pour plus d’informations, consultez [points d’analyse](reparse-points.md).</span><span class="sxs-lookup"><span data-stu-id="06136-110">For more information, see [Reparse Points](reparse-points.md).</span></span>

<span data-ttu-id="06136-111">Pour obtenir le volume cible d’un dossier monté, utilisez la fonction [**GetVolumeNameForVolumeMountPoint**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumenameforvolumemountpointw) .</span><span class="sxs-lookup"><span data-stu-id="06136-111">To obtain the target volume of a mounted folder, use the [**GetVolumeNameForVolumeMountPoint**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumenameforvolumemountpointw) function.</span></span>

<span data-ttu-id="06136-112">De la même façon, vous pouvez déterminer si un point d’analyse est un lien symbolique en testant si la valeur de balise est un lien de **\_ \_ BALIse \_ d’analyse d’e/s**.</span><span class="sxs-lookup"><span data-stu-id="06136-112">In a similar manner, you can determine if a reparse point is a symbolic link by testing whether the tag value is **IO\_REPARSE\_TAG\_SYMLINK**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="06136-113">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="06136-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="06136-114">**Constantes d’attribut de fichier**</span><span class="sxs-lookup"><span data-stu-id="06136-114">**File Attribute Constants**</span></span>](file-attribute-constants.md)
</dt> </dl>

 

 



