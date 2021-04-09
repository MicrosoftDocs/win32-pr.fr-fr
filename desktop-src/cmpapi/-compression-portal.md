---
description: .
ms.assetid: 3ef35cd0-3742-4fc2-9c06-e0485d3538f2
title: API de compression
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e23493310643ad83dc476c31c094dfe336f910f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111459"
---
# <a name="compression-api"></a><span data-ttu-id="e9045-103">API de compression</span><span class="sxs-lookup"><span data-stu-id="e9045-103">Compression API</span></span>

## <a name="purpose"></a><span data-ttu-id="e9045-104">Objectif</span><span class="sxs-lookup"><span data-stu-id="e9045-104">Purpose</span></span>

<span data-ttu-id="e9045-105">L’API de compression expose les algorithmes de compression Windows MSZIP, XPRESS, XPRESS \_ Huff et LZMS.</span><span class="sxs-lookup"><span data-stu-id="e9045-105">The Compression API exposes the Windows MSZIP, XPRESS, XPRESS\_HUFF, and LZMS compression algorithms.</span></span> <span data-ttu-id="e9045-106">Cela permet aux développeurs d’applications Windows de gérer les versions, le service et d’étendre les algorithmes de compression exposés.</span><span class="sxs-lookup"><span data-stu-id="e9045-106">This enables developers of Windows applications to manage versions, service, and extend the exposed compression algorithms.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="e9045-107">Développeurs concernés</span><span class="sxs-lookup"><span data-stu-id="e9045-107">Developer audience</span></span>

<span data-ttu-id="e9045-108">L’API de compression est conçue pour être utilisée par les développeurs professionnels C/C++ des applications Windows.</span><span class="sxs-lookup"><span data-stu-id="e9045-108">The Compression API is designed for use by professional C/C++ developers of Windows applications.</span></span> <span data-ttu-id="e9045-109">L’API de compression expose les algorithmes de compression sans perte utilisés par Windows par le biais d’une interface publique et d’une API en mode utilisateur.</span><span class="sxs-lookup"><span data-stu-id="e9045-109">The Compression API exposes the lossless compression algorithms used by Windows though a public interface and user-mode API.</span></span> <span data-ttu-id="e9045-110">L’API de compression est la méthode recommandée pour les développeurs Windows qui contrôlent les algorithmes de compression.</span><span class="sxs-lookup"><span data-stu-id="e9045-110">The Compression API is the recommended method for Windows developers to control the compression algorithms.</span></span> <span data-ttu-id="e9045-111">Cette fonctionnalité est 64 bits sur Windows 64 bits et 32 bits sur Windows 32 bits.</span><span class="sxs-lookup"><span data-stu-id="e9045-111">This feature is 64-bit on 64-bit Windows and 32-bit on 32-bit Windows.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="e9045-112">Conditions d’exécution</span><span class="sxs-lookup"><span data-stu-id="e9045-112">Run-time requirements</span></span>

<span data-ttu-id="e9045-113">L’API de compression est disponible à partir de Windows 8 ou Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="e9045-113">The Compression API is available beginning with the Windows 8 or Windows Server 2012.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="e9045-114">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="e9045-114">In this section</span></span>

-   [<span data-ttu-id="e9045-115">Utilisation de l’API de compression</span><span class="sxs-lookup"><span data-stu-id="e9045-115">Using the Compression API</span></span>](using-the-compression-api.md)
-   [<span data-ttu-id="e9045-116">Fonctions de l’API de compression</span><span class="sxs-lookup"><span data-stu-id="e9045-116">Compression API Functions</span></span>](compression-api-functions.md)
-   [<span data-ttu-id="e9045-117">Structures de l’API de compression</span><span class="sxs-lookup"><span data-stu-id="e9045-117">Compression API Structures</span></span>](compression-api-structures.md)
-   [<span data-ttu-id="e9045-118">Énumérations de l’API de compression</span><span class="sxs-lookup"><span data-stu-id="e9045-118">Compression API Enumerations</span></span>](compression-api-enumerations.md)

 

 



