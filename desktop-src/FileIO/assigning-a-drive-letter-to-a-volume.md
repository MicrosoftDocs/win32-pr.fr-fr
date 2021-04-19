---
description: 'Vous pouvez affecter une lettre de lecteur (par exemple, X : \) à un volume local à l’aide de la fonction SetVolumeMountPoint, à condition qu’il n’y ait aucun volume déjà affecté à cette lettre de lecteur.'
ms.assetid: 8c78b2e8-199a-4934-a9c4-6f3913f44efe
title: Affectation d’une lettre de lecteur à un volume
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f31b9446cc41ad26f14a34874c59e153e1db8ce5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106534179"
---
# <a name="assigning-a-drive-letter-to-a-volume"></a><span data-ttu-id="e67bd-103">Affectation d’une lettre de lecteur à un volume</span><span class="sxs-lookup"><span data-stu-id="e67bd-103">Assigning a Drive Letter to a Volume</span></span>

<span data-ttu-id="e67bd-104">Vous pouvez affecter une lettre de lecteur (par exemple, X : \) à un volume local à l’aide de la fonction [**SetVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa) , à condition qu’il n’y ait aucun volume déjà affecté à cette lettre de lecteur.</span><span class="sxs-lookup"><span data-stu-id="e67bd-104">You can assign a drive letter (for example, X:\) to a local volume by using the [**SetVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa) function, provided there is no volume already assigned to that drive letter.</span></span> <span data-ttu-id="e67bd-105">Si le volume local a déjà une lettre de lecteur.</span><span class="sxs-lookup"><span data-stu-id="e67bd-105">If the local volume already has a drive letter.</span></span> <span data-ttu-id="e67bd-106">Ensuite, [**SetVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa) échoue.</span><span class="sxs-lookup"><span data-stu-id="e67bd-106">then [**SetVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa) will fail.</span></span> <span data-ttu-id="e67bd-107">Pour gérer cela, commencez par supprimer la lettre de lecteur à l’aide de la fonction [**DeleteVolumeMountPoint**](/windows/desktop/api/FileAPI/nf-fileapi-deletevolumemountpointw) .</span><span class="sxs-lookup"><span data-stu-id="e67bd-107">To handle this, first delete the drive letter by using the [**DeleteVolumeMountPoint**](/windows/desktop/api/FileAPI/nf-fileapi-deletevolumemountpointw) function.</span></span> <span data-ttu-id="e67bd-108">Pour obtenir un exemple de code, consultez [modification des affectations de lettres de lecteur](editing-drive-letter-assignments.md).</span><span class="sxs-lookup"><span data-stu-id="e67bd-108">For example code, see [Editing Drive Letter Assignments](editing-drive-letter-assignments.md).</span></span>

<span data-ttu-id="e67bd-109">Le système prend en charge au plus une lettre de lecteur par volume.</span><span class="sxs-lookup"><span data-stu-id="e67bd-109">The system supports at most one drive letter per volume.</span></span> <span data-ttu-id="e67bd-110">Par conséquent, vous ne pouvez pas avoir C : \\ et F : \\ représentent le même volume.</span><span class="sxs-lookup"><span data-stu-id="e67bd-110">Therefore, you cannot have C:\\ and F:\\ represent the same volume.</span></span>

> [!Caution]
>
> <span data-ttu-id="e67bd-111">La suppression d’une lettre de lecteur existante et l’affectation d’une nouvelle lettre peuvent altérer les chemins existants, tels que ceux des raccourcis sur le bureau.</span><span class="sxs-lookup"><span data-stu-id="e67bd-111">Deleting an existing drive letter and assigning a new one may break existing paths, such as those in desktop shortcuts.</span></span> <span data-ttu-id="e67bd-112">Il peut également rompre le chemin d’accès au programme en modifiant la lettre de lecteur.</span><span class="sxs-lookup"><span data-stu-id="e67bd-112">It may also break the path to the program making the drive letter changes.</span></span> <span data-ttu-id="e67bd-113">Avec la gestion de la mémoire virtuelle Windows, cela peut perturber l’application, ce qui laisse le système dans un état instable et peut-être inutilisable.</span><span class="sxs-lookup"><span data-stu-id="e67bd-113">With Windows virtual memory management, this may break the application, leaving the system in an unstable and possibly unusable state.</span></span> <span data-ttu-id="e67bd-114">Il incombe au concepteur de programme d’éviter ces catastrophes potentielles.</span><span class="sxs-lookup"><span data-stu-id="e67bd-114">It is the program designer's responsibility to avoid such potential catastrophes.</span></span>

 

 

 



