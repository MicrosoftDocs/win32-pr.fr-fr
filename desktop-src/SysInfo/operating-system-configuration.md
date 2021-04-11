---
description: Le répertoire Windows est le répertoire qui contient des applications Windows, des fichiers d’initialisation et des fichiers d’aide. La fonction GetWindowsDirectory récupère le chemin d’accès à ce répertoire.
ms.assetid: c07c6337-2c92-42c5-8283-c95637fcb85a
title: Configuration du système d’exploitation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a38aa2c2b6b4f6b3ac5caac78a89ad980a9bd074
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203984"
---
# <a name="operating-system-configuration"></a><span data-ttu-id="e445f-104">Configuration du système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="e445f-104">Operating System Configuration</span></span>

<span data-ttu-id="e445f-105">Le *répertoire Windows* est le répertoire qui contient des applications Windows, des fichiers d’initialisation et des fichiers d’aide.</span><span class="sxs-lookup"><span data-stu-id="e445f-105">The *Windows directory* is the directory that contains Windows-based applications, initialization files, and help files.</span></span> <span data-ttu-id="e445f-106">La fonction [**GetWindowsDirectory**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getwindowsdirectorya) récupère le chemin d’accès à ce répertoire.</span><span class="sxs-lookup"><span data-stu-id="e445f-106">The [**GetWindowsDirectory**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getwindowsdirectorya) function retrieves the path to this directory.</span></span>

<span data-ttu-id="e445f-107">Le *répertoire système* est le répertoire qui contient les bibliothèques de liens dynamiques, les pilotes et les fichiers de police.</span><span class="sxs-lookup"><span data-stu-id="e445f-107">The *system directory* is the directory that contains dynamic-link libraries, drivers, and font files.</span></span> <span data-ttu-id="e445f-108">La fonction [**GetSystemDirectory**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemdirectorya) récupère le chemin d’accès à ce répertoire.</span><span class="sxs-lookup"><span data-stu-id="e445f-108">The [**GetSystemDirectory**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemdirectorya) function retrieves the path to this directory.</span></span>

<span data-ttu-id="e445f-109">La fonction [**getUserName**](/windows/desktop/api/Winbase/nf-winbase-getusernamea) récupère le nom de l’utilisateur actuellement connecté au système.</span><span class="sxs-lookup"><span data-stu-id="e445f-109">The [**GetUserName**](/windows/desktop/api/Winbase/nf-winbase-getusernamea) function retrieves the name of the user currently logged onto the system.</span></span> <span data-ttu-id="e445f-110">Le nom d’utilisateur est soit le nom d’ouverture de session, soit le nom complet de l’utilisateur, si ce dernier est inclus dans le registre.</span><span class="sxs-lookup"><span data-stu-id="e445f-110">The user name is either the logon name or the user's full name, if the latter is included in the registry.</span></span>

<span data-ttu-id="e445f-111">Une *variable d’environnement* est une variable symbolique qui représente un élément du système, tel qu’un chemin d’accès, un nom de fichier ou d’autres données littérales.</span><span class="sxs-lookup"><span data-stu-id="e445f-111">An *environment variable* is a symbolic variable that represents some element of the system, such as a path, a file name, or other literal data.</span></span> <span data-ttu-id="e445f-112">Par exemple, le chemin d’accès de la variable d’environnement représente les répertoires dans lesquels rechercher les fichiers exécutables.</span><span class="sxs-lookup"><span data-stu-id="e445f-112">For example, the environment variable PATH represents the directories in which to search for executable files.</span></span> <span data-ttu-id="e445f-113">Lorsqu’un utilisateur ouvre une session, le système initialise les variables d’environnement en fonction de la section environnement du Registre.</span><span class="sxs-lookup"><span data-stu-id="e445f-113">When a user logs on, the system initializes environment variables based on the environment section of the registry.</span></span> <span data-ttu-id="e445f-114">La fonction [**ExpandEnvironmentStrings**](/windows/win32/api/processenv/nf-processenv-expandenvironmentstringsa) récupère les valeurs des variables d’environnement spécifiées.</span><span class="sxs-lookup"><span data-stu-id="e445f-114">The [**ExpandEnvironmentStrings**](/windows/win32/api/processenv/nf-processenv-expandenvironmentstringsa) function retrieves the values of specified environment variables.</span></span>

<span data-ttu-id="e445f-115">Des informations supplémentaires sont fournies par l’interface [**IADsADSystemInfo**](/windows/desktop/api/iads/nn-iads-iadsadsysteminfo) .</span><span class="sxs-lookup"><span data-stu-id="e445f-115">Additional information is provided by the [**IADsADSystemInfo**](/windows/desktop/api/iads/nn-iads-iadsadsysteminfo) interface.</span></span>

 

 
