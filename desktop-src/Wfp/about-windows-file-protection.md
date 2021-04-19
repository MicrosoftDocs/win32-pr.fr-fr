---
description: Protection des ressources Windows (WRP) empêche le remplacement des fichiers système essentiels, des dossiers et des clés de Registre installés dans le cadre du système d’exploitation.
ms.assetid: 39069f57-d9f6-4890-ba87-37175184d7a2
title: À propos de Protection des ressources Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c102225a547c4e454c3fb67ac94f715cd3adf8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106545063"
---
# <a name="about-windows-resource-protection"></a><span data-ttu-id="88450-103">À propos de Protection des ressources Windows</span><span class="sxs-lookup"><span data-stu-id="88450-103">About Windows Resource Protection</span></span>

<span data-ttu-id="88450-104">Protection des ressources Windows (WRP) empêche le remplacement des fichiers système essentiels, des dossiers et des clés de Registre installés dans le cadre du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="88450-104">Windows Resource Protection (WRP) prevents the replacement of essential system files, folders, and registry keys that are installed as part of the operating system.</span></span> <span data-ttu-id="88450-105">Il est devenu disponible à partir de Windows Server 2008 et Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="88450-105">It became available starting with Windows Server 2008 and Windows Vista.</span></span> <span data-ttu-id="88450-106">L’autorisation d’accès complet pour modifier les ressources protégées par WRP est limitée à TrustedInstaller.</span><span class="sxs-lookup"><span data-stu-id="88450-106">Permission for full access to modify WRP-protected resources is restricted to TrustedInstaller.</span></span> <span data-ttu-id="88450-107">Les ressources protégées par WRP ne peuvent être modifiées qu’à l’aide des [mécanismes de remplacement des ressources pris en charge](supported-file-replacement-mechanisms.md) par le service d’installation des modules Windows.</span><span class="sxs-lookup"><span data-stu-id="88450-107">WRP-protected resources can only be changed using the [Supported Resource Replacement Mechanisms](supported-file-replacement-mechanisms.md) with the Windows Modules Installer service.</span></span> <span data-ttu-id="88450-108">La protection de ces ressources empêche les défaillances de l’application et du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="88450-108">Protecting these resources prevents application and operating system failures.</span></span>

<span data-ttu-id="88450-109">Les applications ne doivent pas tenter de modifier les ressources protégées par WRP, car celles-ci sont utilisées par Windows et d’autres applications.</span><span class="sxs-lookup"><span data-stu-id="88450-109">Applications should not attempt to modify WRP-protected resources because these are used by Windows and other applications.</span></span> <span data-ttu-id="88450-110">Si une application tente de modifier une ressource protégée par WRP, elle peut avoir les résultats suivants.</span><span class="sxs-lookup"><span data-stu-id="88450-110">If an application attempts to modify a WRP-protected resource, it can have the following results.</span></span>

-   <span data-ttu-id="88450-111">Les programmes d’installation d’application qui tentent de remplacer, de modifier ou de supprimer les fichiers ou clés de Registre critiques de Windows peuvent ne pas réussir à installer l’application et recevront un message d’erreur indiquant que l’accès à la ressource a été refusé.</span><span class="sxs-lookup"><span data-stu-id="88450-111">Application installers that attempt to replace, modify, or delete critical Windows files or registry keys may fail to install the application and will receive an error message stating that access to the resource was denied.</span></span>
-   <span data-ttu-id="88450-112">Les applications qui tentent d’ajouter ou de supprimer des sous-clés ou de modifier les valeurs des clés de Registre protégées peuvent échouer et un message d’erreur s’affiche indiquant que l’accès à la ressource a été refusé.</span><span class="sxs-lookup"><span data-stu-id="88450-112">Applications that attempt to add or remove sub-keys or change the values of protected registry keys may fail and will receive an error message stating that access to the resource was denied.</span></span>
-   <span data-ttu-id="88450-113">Les applications qui reposent sur l’écriture d’informations dans des clés de Registre protégées, des dossiers ou des fichiers peuvent échouer.</span><span class="sxs-lookup"><span data-stu-id="88450-113">Applications that rely on writing any information into protected registry keys, folders, or files may fail.</span></span>

<span data-ttu-id="88450-114">WRP est le nouveau nom de la protection de fichiers Windows (WFP).</span><span class="sxs-lookup"><span data-stu-id="88450-114">WRP is the new name for Windows File Protection (WFP).</span></span> <span data-ttu-id="88450-115">WRP protège les clés de Registre et les dossiers, ainsi que les fichiers système essentiels.</span><span class="sxs-lookup"><span data-stu-id="88450-115">WRP protects registry keys and folders as well as essential system files.</span></span> <span data-ttu-id="88450-116">WFP était disponible dans Microsoft Windows Server 2003 et Windows XP.</span><span class="sxs-lookup"><span data-stu-id="88450-116">WFP was available in Microsoft Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="88450-117">WRP remplace WFP dans Windows Server 2008 et Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="88450-117">WRP replaces WFP in Windows Server 2008 and Windows Vista.</span></span>

<span data-ttu-id="88450-118">Les rubriques suivantes décrivent WRP :</span><span class="sxs-lookup"><span data-stu-id="88450-118">The following topics describe WRP:</span></span>

-   [<span data-ttu-id="88450-119">Liste des ressources protégées</span><span class="sxs-lookup"><span data-stu-id="88450-119">Protected Resource List</span></span>](protected-file-list.md)
-   [<span data-ttu-id="88450-120">Détection du remplacement des ressources</span><span class="sxs-lookup"><span data-stu-id="88450-120">Detecting Resource Replacement</span></span>](detecting-file-replacement.md)
-   [<span data-ttu-id="88450-121">Mécanismes de remplacement des ressources pris en charge</span><span class="sxs-lookup"><span data-stu-id="88450-121">Supported Resource Replacement Mechanisms</span></span>](supported-file-replacement-mechanisms.md)
-   [<span data-ttu-id="88450-122">Vérificateur des fichiers système</span><span class="sxs-lookup"><span data-stu-id="88450-122">System File Checker</span></span>](system-file-checker.md)
-   [<span data-ttu-id="88450-123">Considérations relatives à l’administration à distance</span><span class="sxs-lookup"><span data-stu-id="88450-123">Remote Administration Considerations</span></span>](remote-administration-considerations.md)

 

 



