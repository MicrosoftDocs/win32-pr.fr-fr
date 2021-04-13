---
description: Les applications peuvent récupérer et définir la date et l’heure de création, de modification ou de dernier accès d’un fichier à l’aide des fonctions GetFileTime et SetFileTime.
ms.assetid: f8930be6-7c2a-4e50-a7a1-d25f6e2a3951
title: Définition et obtention de l’horodateur d’un fichier
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34735994dd3017662f517a8c0a57be1d5c0e3096
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201606"
---
# <a name="setting-and-getting-the-timestamp-of-a-file"></a><span data-ttu-id="a561c-103">Définition et obtention de l’horodateur d’un fichier</span><span class="sxs-lookup"><span data-stu-id="a561c-103">Setting and Getting the Timestamp of a File</span></span>

<span data-ttu-id="a561c-104">Les applications peuvent récupérer et définir la date et l’heure de création, de modification ou de dernier accès d’un fichier à l’aide des fonctions [**GetFileTime**](/windows/desktop/api/fileapi/nf-fileapi-getfiletime) et [**SetFileTime**](/windows/desktop/api/fileapi/nf-fileapi-setfiletime) .</span><span class="sxs-lookup"><span data-stu-id="a561c-104">Applications can retrieve and set the date and time a file is created, last modified, or last accessed by using the [**GetFileTime**](/windows/desktop/api/fileapi/nf-fileapi-getfiletime) and [**SetFileTime**](/windows/desktop/api/fileapi/nf-fileapi-setfiletime) functions.</span></span> <span data-ttu-id="a561c-105">Pour plus d’informations, consultez [temps de fichier](/windows/desktop/SysInfo/file-times).</span><span class="sxs-lookup"><span data-stu-id="a561c-105">For more information, see [File Times](/windows/desktop/SysInfo/file-times).</span></span>

> [!Note]  
> <span data-ttu-id="a561c-106">Tous les systèmes de fichiers ne peuvent pas enregistrer les heures de création et de dernier accès, et tous les systèmes de fichiers ne les enregistrent pas de la même manière.</span><span class="sxs-lookup"><span data-stu-id="a561c-106">Not all file systems can record creation and last access times, and not all file systems record them in the same manner.</span></span> <span data-ttu-id="a561c-107">Par exemple, sur le système de fichiers FAT, l’heure de création a une résolution de 10 millisecondes, le temps d’écriture a une résolution de 2 secondes et le temps d’accès a une résolution de 1 jour (en réalité, la date d’accès).</span><span class="sxs-lookup"><span data-stu-id="a561c-107">For example, on FAT file system, create time has a resolution of 10 milliseconds, write time has a resolution of 2 seconds, and access time has a resolution of 1 day (really, the access date).</span></span> <span data-ttu-id="a561c-108">Le système de fichiers NTFS retarde la mise à jour de l’heure du dernier accès pour un fichier jusqu’à une heure après le dernier accès.</span><span class="sxs-lookup"><span data-stu-id="a561c-108">The NTFS file system delays update to the last access time for a file by up to one hour after the last access.</span></span>

 

 

 
