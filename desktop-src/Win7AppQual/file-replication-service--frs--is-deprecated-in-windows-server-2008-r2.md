---
description: Le service de réplication de fichiers (FRS) est déconseillé dans Windows Server 2008 R2
ms.assetid: 18a03469-737a-4905-9851-f7961c46b867
title: Le service de réplication de fichiers (FRS) est déconseillé dans Windows Server 2008 R2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d3c34e43daf8346888a32ef76d55f93ac5a563e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088367"
---
# <a name="file-replication-service-frs-is-deprecated-in-windows-server-2008-r2"></a><span data-ttu-id="1fd34-103">Le service de réplication de fichiers (FRS) est déconseillé dans Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="1fd34-103">File Replication Service (FRS) Is Deprecated in Windows Server 2008 R2</span></span>

## <a name="platform"></a><span data-ttu-id="1fd34-104">Plateforme</span><span class="sxs-lookup"><span data-stu-id="1fd34-104">Platform</span></span>

 <span data-ttu-id="1fd34-105">**Serveurs-** Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="1fd34-105">**Servers -** Windows Server 2008 R2</span></span>  

## <a name="feature-impact"></a><span data-ttu-id="1fd34-106">Impact sur les fonctionnalités</span><span class="sxs-lookup"><span data-stu-id="1fd34-106">Feature Impact</span></span>

 <span data-ttu-id="1fd34-107">**Gravité-** Rapide</span><span class="sxs-lookup"><span data-stu-id="1fd34-107">**Severity -** High</span></span>  
<span data-ttu-id="1fd34-108">**Fréquence-** Rapide</span><span class="sxs-lookup"><span data-stu-id="1fd34-108">**Frequency -** High</span></span>  


## <a name="description"></a><span data-ttu-id="1fd34-109">Description</span><span class="sxs-lookup"><span data-stu-id="1fd34-109">Description</span></span>

<span data-ttu-id="1fd34-110">Dans Windows Server 2008 R2, le service de réplication de fichiers (FRS) ne peut pas être utilisé pour répliquer des dossiers système de fichiers DFS (DFS) ou des données personnalisées (autres que SYSVOL).</span><span class="sxs-lookup"><span data-stu-id="1fd34-110">In Windows Server 2008 R2, File Replication Service (FRS) cannot be used for replicating Distributed File System (DFS) folders or custom (non-SYSVOL) data.</span></span> <span data-ttu-id="1fd34-111">Un contrôleur de domaine Windows Server 2008 R2 peut toujours utiliser FRS pour répliquer le contenu du partage SYSVOL dans un domaine qui utilise le service FRS pour répliquer le partage SYSVOL entre les contrôleurs de domaine.</span><span class="sxs-lookup"><span data-stu-id="1fd34-111">A Windows Server 2008 R2 domain controller can still use FRS to replicate the contents of the SYSVOL share in a domain that uses FRS for replicating the SYSVOL share between domain controllers.</span></span> <span data-ttu-id="1fd34-112">Toutefois, les serveurs Windows Server 2008 R2 ne peuvent pas utiliser FRS pour répliquer le contenu d’un jeu de réplicas séparé du partage SYSVOL.</span><span class="sxs-lookup"><span data-stu-id="1fd34-112">However, Windows Server 2008 R2 servers cannot use FRS to replicate the contents of any replica set apart from the SYSVOL share.</span></span> <span data-ttu-id="1fd34-113">Le service réplication DFS remplace le service FRS et peut être utilisé pour répliquer le contenu du partage SYSVOL, les dossiers DFS, ainsi que d’autres données personnalisées (autres que SYSVOL).</span><span class="sxs-lookup"><span data-stu-id="1fd34-113">The DFS Replication service is a replacement for FRS and can be used to replicate the contents of the SYSVOL share, DFS folders as well as other custom (non-SYSVOL) data.</span></span> <span data-ttu-id="1fd34-114">Migrez tous les jeux de réplicas FRS non SYSVOL vers réplication DFS.</span><span class="sxs-lookup"><span data-stu-id="1fd34-114">Migrate all non-SYSVOL FRS replica sets to DFS Replication.</span></span> <span data-ttu-id="1fd34-115">Nous vous recommandons également de migrer la réplication du partage SYSVOL de FRS vers réplication DFS, car réplication DFS est plus robuste, évolutive et offre de meilleures performances de réplication que FRS.</span><span class="sxs-lookup"><span data-stu-id="1fd34-115">We also highly recommend that you migrate replication of the SYSVOL share from FRS to DFS Replication because DFS Replication is more robust, scalable and has better replication performance than FRS.</span></span>

## <a name="manifestation"></a><span data-ttu-id="1fd34-116">Manifestation</span><span class="sxs-lookup"><span data-stu-id="1fd34-116">Manifestation</span></span>

<span data-ttu-id="1fd34-117">La réplication FRS de données personnalisées est irréversible sur la mise à niveau sur place.</span><span class="sxs-lookup"><span data-stu-id="1fd34-117">FRS replication of custom data will break irreversibly upon in-place upgrade.</span></span> <span data-ttu-id="1fd34-118">La seule façon de procéder à une récupération à partir de cette situation consiste à réinstaller un système d’exploitation plus ancien sur le serveur et à réinitialiser la réplication FRS.</span><span class="sxs-lookup"><span data-stu-id="1fd34-118">The only way to recover from this situation would be to reinstall an older operating system on the server and reinitialize FRS replication.</span></span> <span data-ttu-id="1fd34-119">Les serveurs qui ont été mis à niveau vers Windows Server 2008 R2 ne sont pas autorisés à participer à des groupes de réplication FRS existants.</span><span class="sxs-lookup"><span data-stu-id="1fd34-119">Servers that have been upgraded to Windows Server 2008 R2 are not allowed to participate in existing FRS replication groups.</span></span>

## <a name="mitigation-of-impact"></a><span data-ttu-id="1fd34-120">Atténuation de l’impact</span><span class="sxs-lookup"><span data-stu-id="1fd34-120">Mitigation of Impact</span></span>

<span data-ttu-id="1fd34-121">Pour éviter les problèmes qui peuvent se produire suite à ces modifications, migrez les jeux de réplication FRS personnalisés vers réplication DFS.</span><span class="sxs-lookup"><span data-stu-id="1fd34-121">To prevent issues that might occur as a result of these changes, migrate custom FRS replication sets to DFS Replication.</span></span> <span data-ttu-id="1fd34-122">Le service réplication DFS présente de nombreux avantages par rapport à FRS, y compris des outils de gestion améliorés, des performances supérieures et une gestion déléguée.</span><span class="sxs-lookup"><span data-stu-id="1fd34-122">The DFS Replication service has many benefits over FRS, including improved management tools, higher performance, and delegated management.</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="1fd34-123">Liens vers d’autres ressources</span><span class="sxs-lookup"><span data-stu-id="1fd34-123">Links to Other Resources</span></span>

-   <span data-ttu-id="1fd34-124">[Vue d’ensemble de FRS](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc754297(v=ws.11))</span><span class="sxs-lookup"><span data-stu-id="1fd34-124">[FRS Overview](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc754297(v=ws.11))</span></span>
-   [<span data-ttu-id="1fd34-125">Réplication du système de fichiers DFS : Forum Aux Questions</span><span class="sxs-lookup"><span data-stu-id="1fd34-125">Distributed File System Replication: Frequently Asked Questions</span></span>](/windows-server/storage/dfs-replication/dfsr-faq)
-   [<span data-ttu-id="1fd34-126">Guide de migration de la réplication SYSVOL : Réplication FRS vers DFS</span><span class="sxs-lookup"><span data-stu-id="1fd34-126">SYSVOL Replication Migration Guide: FRS to DFS Replication</span></span>](/windows-server/storage/dfs-replication/migrate-sysvol-to-dfsr)

 

 
