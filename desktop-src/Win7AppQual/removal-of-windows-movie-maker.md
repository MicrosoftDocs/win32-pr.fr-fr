---
description: .
ms.assetid: af55e570-0f24-4376-905a-3b879d5f3a1c
title: Suppression de Windows Movie Maker
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d71a3336421ae2bde761aa1d4f238b5cd135ba64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106518893"
---
# <a name="removal-of-windows-movie-maker"></a><span data-ttu-id="e09ad-103">Suppression de Windows Movie Maker</span><span class="sxs-lookup"><span data-stu-id="e09ad-103">Removal of Windows Movie Maker</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="e09ad-104">Plateformes affectées</span><span class="sxs-lookup"><span data-stu-id="e09ad-104">Affected Platforms</span></span>

<span data-ttu-id="e09ad-105">**Clients** -Windows 7</span><span class="sxs-lookup"><span data-stu-id="e09ad-105">**Clients** - Windows 7</span></span>  
<span data-ttu-id="e09ad-106">**Serveurs** -Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="e09ad-106">**Servers** - Windows Server 2008 R2</span></span>  









## <a name="feature-impact"></a><span data-ttu-id="e09ad-107">Impact sur les fonctionnalités</span><span class="sxs-lookup"><span data-stu-id="e09ad-107">Feature Impact</span></span>

 <span data-ttu-id="e09ad-108">**Gravité** -haute</span><span class="sxs-lookup"><span data-stu-id="e09ad-108">**Severity** - High</span></span>  
<span data-ttu-id="e09ad-109">**Fréquence** -moyenne</span><span class="sxs-lookup"><span data-stu-id="e09ad-109">**Frequency** - Medium</span></span>  


## <a name="description"></a><span data-ttu-id="e09ad-110">Description</span><span class="sxs-lookup"><span data-stu-id="e09ad-110">Description</span></span>

<span data-ttu-id="e09ad-111">Microsoft déprécie et supprime l’utilitaire Windows Movie Maker.</span><span class="sxs-lookup"><span data-stu-id="e09ad-111">Microsoft is deprecating and removing the Windows Movie Maker utility.</span></span> <span data-ttu-id="e09ad-112">notamment :</span><span class="sxs-lookup"><span data-stu-id="e09ad-112">This includes:</span></span>

-   <span data-ttu-id="e09ad-113">Tous les points d’entrée vers Windows Movie Maker (par exemple, menu Démarrer, démarrer > exécuter)</span><span class="sxs-lookup"><span data-stu-id="e09ad-113">All entry points to Windows Movie Maker (for example, Start Menu, Start > Run)</span></span>
-   <span data-ttu-id="e09ad-114">Tous les fichiers binaires qui ont été utilisés par Windows Movie Maker (tout ce qui se trouvait dans% ProgramFiles% \\ Movie Maker)</span><span class="sxs-lookup"><span data-stu-id="e09ad-114">All binaries that were used by Windows Movie Maker (everything that was in %ProgramFiles%\\Movie Maker)</span></span>

<span data-ttu-id="e09ad-115">Toutefois, les fichiers projet Movie Maker d’un utilisateur restent sur le système et sont accessibles aux autres applications qui prennent en charge ce format de fichier.</span><span class="sxs-lookup"><span data-stu-id="e09ad-115">However, a user's Movie Maker project files will remain on the system and be accessible to other applications that support this file format.</span></span>

## <a name="manifestation"></a><span data-ttu-id="e09ad-116">Manifestation</span><span class="sxs-lookup"><span data-stu-id="e09ad-116">Manifestation</span></span>

<span data-ttu-id="e09ad-117">Les résultats de la suppression de Windows Movie Maker sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="e09ad-117">Remove of Windows Movie Maker results in the following:</span></span>

-   <span data-ttu-id="e09ad-118">Toute tentative de lancement de Windows Movie Maker avec ses arguments de ligne de commande échoue</span><span class="sxs-lookup"><span data-stu-id="e09ad-118">Any attempt to launch Windows Movie Maker with its command line arguments will fail</span></span>
-   <span data-ttu-id="e09ad-119">Tous les plug-ins installés pour activer les nouvelles transformations et les animations restent installés, mais ne sont pas exposés à l’utilisateur final.</span><span class="sxs-lookup"><span data-stu-id="e09ad-119">Any plug-ins that were installed to enable new transforms and animations will remain installed but will not be exposed to the end user</span></span>

## <a name="solution"></a><span data-ttu-id="e09ad-120">Solution</span><span class="sxs-lookup"><span data-stu-id="e09ad-120">Solution</span></span>

<span data-ttu-id="e09ad-121">Pour que ces fonctionnalités soient à l’avenir, l’utilisateur doit installer une application similaire à partir de Microsoft ou d’un autre fournisseur de logiciels.</span><span class="sxs-lookup"><span data-stu-id="e09ad-121">To have such functionality in the future, a user will need to install a similar application from Microsoft or another software provider.</span></span>

 

 



