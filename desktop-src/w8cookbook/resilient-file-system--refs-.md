---
title: Système de fichiers résilient
description: Système de fichiers résilient
ms.assetid: 6E5532F9-64BC-4DD7-9873-3FE4E4DE2DD0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0dba011dcdd3cd39280e0a79d0b325f9e75d6b64
ms.sourcegitcommit: 46376be61d3fa308f9b1a06d7e2fa122a39755af
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2020
ms.locfileid: "104032035"
---
# <a name="resilient-file-system"></a><span data-ttu-id="a1296-103">Système de fichiers résilient</span><span class="sxs-lookup"><span data-stu-id="a1296-103">Resilient file system</span></span>

## <a name="platform"></a><span data-ttu-id="a1296-104">Plateforme</span><span class="sxs-lookup"><span data-stu-id="a1296-104">Platform</span></span>

<span data-ttu-id="a1296-105">**Serveurs** – Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a1296-105">**Servers** – Windows Server 2012</span></span> 

## <a name="description"></a><span data-ttu-id="a1296-106">Description</span><span class="sxs-lookup"><span data-stu-id="a1296-106">Description</span></span>

<span data-ttu-id="a1296-107">Le système de fichiers résilient (ReFS) est un nouveau système de fichiers local.</span><span class="sxs-lookup"><span data-stu-id="a1296-107">Resilient File System (ReFS) is a new local file system.</span></span> <span data-ttu-id="a1296-108">Il optimise la disponibilité des données, malgré les erreurs qui pourraient entraîner une perte de données ou des temps d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="a1296-108">It maximizes data availability, despite errors that would historically cause data loss or downtime.</span></span> <span data-ttu-id="a1296-109">L’intégrité des données garantit que les données critiques de l’entreprise sont protégées contre les erreurs et disponibles si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="a1296-109">Data integrity ensures that business critical data is protected from errors and available when needed.</span></span> <span data-ttu-id="a1296-110">Son architecture est conçue pour fournir une évolutivité et des performances dans une ère qui augmente constamment la taille des jeux de données et les charges de travail dynamiques.</span><span class="sxs-lookup"><span data-stu-id="a1296-110">Its architecture is designed to provide scalability and performance in an era of constantly growing data set sizes and dynamic workloads.</span></span>

<span data-ttu-id="a1296-111">Les principales fonctionnalités de ReFS sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="a1296-111">The key features of ReFS are:</span></span>

-   <span data-ttu-id="a1296-112">**Intégrité**: ReFS stocke les données afin qu’elles soient protégées contre nombre des erreurs courantes qui peuvent entraîner une perte de données.</span><span class="sxs-lookup"><span data-stu-id="a1296-112">**Integrity**: ReFS stores data so that it is protected from many of the common errors that can cause data loss.</span></span> <span data-ttu-id="a1296-113">Les métadonnées du système de fichiers sont toujours protégées.</span><span class="sxs-lookup"><span data-stu-id="a1296-113">File system metadata is always protected.</span></span> <span data-ttu-id="a1296-114">Si vous le souhaitez, les données utilisateur peuvent être protégées par volume, par répertoire ou par fichier.</span><span class="sxs-lookup"><span data-stu-id="a1296-114">Optionally, user data can be protected on a per-volume, per-directory, or per-file basis.</span></span> <span data-ttu-id="a1296-115">En cas d’endommagement, ReFS peut détecter et, lorsqu’il est configuré avec des espaces de stockage, corriger automatiquement les dommages.</span><span class="sxs-lookup"><span data-stu-id="a1296-115">If corruption occurs, ReFS can detect and, when configured with Storage Spaces, automatically correct the corruption.</span></span> <span data-ttu-id="a1296-116">En cas d’erreur système, ReFS est conçu pour récupérer rapidement à partir de cette erreur, sans perte de données utilisateur.</span><span class="sxs-lookup"><span data-stu-id="a1296-116">In the event of a system error, ReFS is designed to recover from that error rapidly, with no loss of user data.</span></span>
-   <span data-ttu-id="a1296-117">**Disponibilité**: ReFS est conçu pour hiérarchiser la disponibilité des données.</span><span class="sxs-lookup"><span data-stu-id="a1296-117">**Availability**: ReFS is designed to prioritize the availability of data.</span></span> <span data-ttu-id="a1296-118">Avec ReFS, si une altération se produit et qu’elle ne peut pas être réparée automatiquement, le processus de récupération en ligne est localisé dans la zone d’altération, ce qui ne nécessite pas de temps d’arrêt du volume.</span><span class="sxs-lookup"><span data-stu-id="a1296-118">With ReFS, if corruption occurs, and it cannot be repaired automatically, the online salvage process is localized to the area of corruption, requiring no volume down-time.</span></span> <span data-ttu-id="a1296-119">En bref, en cas d’endommagement, ReFS reste en ligne.</span><span class="sxs-lookup"><span data-stu-id="a1296-119">In short, if corruption occurs, ReFS will stay online.</span></span>
-   <span data-ttu-id="a1296-120">**Scalabilité**: ReFS est conçu pour les tailles de jeux de données actuelles et les tailles de jeux de données de demain. elle est optimisée pour une évolutivité élevée.</span><span class="sxs-lookup"><span data-stu-id="a1296-120">**Scalability**: ReFS is designed for the data set sizes of today and the data set sizes of tomorrow; it’s optimized for high scalability.</span></span>
-   <span data-ttu-id="a1296-121">**Compatibilité des applications**: pour optimiser AppCompat, ReFS prend en charge un sous-ensemble de fonctionnalités NTFS et les API Win32 qui sont largement adoptées.</span><span class="sxs-lookup"><span data-stu-id="a1296-121">**App Compatibility**: To maximize AppCompat, ReFS supports a subset of NTFS features plus Win32 APIs that are widely adopted.</span></span>
-   <span data-ttu-id="a1296-122">**Identification proactive des erreurs**: les fonctionnalités d’intégrité de ReFS sont exploitées par un scanneur d’intégrité des données (un « épurateur ») qui analyse régulièrement le volume, tente d’identifier une altération latente, puis déclenche de manière proactive une réparation de ces données endommagées.</span><span class="sxs-lookup"><span data-stu-id="a1296-122">**Proactive Error Identification**: The integrity capabilities of ReFS are leveraged by a data integrity scanner (a “scrubber”) that periodically scans the volume, attempts to identify latent corruption, and then proactively triggers a repair of that corrupt data.</span></span>

## <a name="resources"></a><span data-ttu-id="a1296-123">Ressources</span><span class="sxs-lookup"><span data-stu-id="a1296-123">Resources</span></span>

-   [<span data-ttu-id="a1296-124">Création du billet de blog Windows 8 : génération du système de fichiers de nouvelle génération pour Windows : ReFS</span><span class="sxs-lookup"><span data-stu-id="a1296-124">Building Windows 8 Blog Post – Building the next generation file system for Windows: ReFS</span></span>](/archive/blogs/b8/building-the-next-generation-file-system-for-windows-refs)
-   [<span data-ttu-id="a1296-125">Compatibilité des applications et références</span><span class="sxs-lookup"><span data-stu-id="a1296-125">Application Compatibility and ReFS</span></span>](https://www.microsoft.com/download/en/details.aspx?id=29043)

 

 