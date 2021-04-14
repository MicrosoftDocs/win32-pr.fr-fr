---
title: Licences
description: Licences
ms.assetid: 74717519-bfd5-4a64-88eb-680d4bdfe74a
keywords:
- Kit de développement logiciel (SDK) Windows Media format, gestion des droits numériques (DRM)
- Windows Media Format SDK, licences DRM
- Windows Media Format SDK, licences pour DRM
- gestion des droits numériques (DRM), licences
- DRM (gestion des droits numériques), licences
- gestion des droits numériques (DRM), gestion des licences de fichiers protégés
- DRM (gestion des droits numériques), gestion des licences de fichiers protégés
- licences, DRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0fbf2d7c0a25b2b19241d90743f43f46a71d7e0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311260"
---
# <a name="licenses"></a><span data-ttu-id="1d6fb-111">Licences</span><span class="sxs-lookup"><span data-stu-id="1d6fb-111">Licenses</span></span>

<span data-ttu-id="1d6fb-112">Une licence est un ensemble de données décrivant les conditions dans lesquelles les données des fichiers protégés peuvent être lues.</span><span class="sxs-lookup"><span data-stu-id="1d6fb-112">A license is a set of data that describes the conditions under which data in protected files can be read.</span></span> <span data-ttu-id="1d6fb-113">Chaque licence s’applique à un identificateur de clé, qui est généralement affecté à un seul fichier multimédia.</span><span class="sxs-lookup"><span data-stu-id="1d6fb-113">Each license applies to a key identifier, which is typically assigned to a single media file.</span></span> <span data-ttu-id="1d6fb-114">Cet identificateur est utilisé pour identifier le contenu protégé de la licence.</span><span class="sxs-lookup"><span data-stu-id="1d6fb-114">This identifier is what is used to identify the protected content in the license.</span></span>

<span data-ttu-id="1d6fb-115">Chaque licence spécifie une ou plusieurs actions qui peuvent être effectuées avec le contenu protégé.</span><span class="sxs-lookup"><span data-stu-id="1d6fb-115">Each license specifies one or more actions that can be performed with the protected content.</span></span> <span data-ttu-id="1d6fb-116">Ces actions, également appelées droits, peuvent être limitées de plusieurs façons.</span><span class="sxs-lookup"><span data-stu-id="1d6fb-116">These actions, also called rights, can be limited in a number of ways.</span></span> <span data-ttu-id="1d6fb-117">En associant les dates de début, les dates de fin, les nombres et les limites de temps, l’émetteur de licence peut créer quasiment n’importe quelle limitation imaginaire sur un droit.</span><span class="sxs-lookup"><span data-stu-id="1d6fb-117">By combining start dates, end dates, counts, and time limits, the license issuer can create almost any imaginable limitation on a right.</span></span>

<span data-ttu-id="1d6fb-118">Les licences sont émises par un service Web.</span><span class="sxs-lookup"><span data-stu-id="1d6fb-118">Licenses are issued by a Web service.</span></span> <span data-ttu-id="1d6fb-119">Lorsqu’une licence est acquise, elle est stockée sur l’ordinateur client dans le magasin de licences local, qui est un fichier protégé qui contient des licences et d’autres données DRM.</span><span class="sxs-lookup"><span data-stu-id="1d6fb-119">When a license is acquired, it is stored on the client computer in the local license store, which is a protected file that contains licenses and other DRM data.</span></span> <span data-ttu-id="1d6fb-120">Quand une application accède au contenu protégé, le sous-système DRM recherche une licence qui accorde le droit approprié dans le magasin de licences local.</span><span class="sxs-lookup"><span data-stu-id="1d6fb-120">When protected content is accessed by an application, the DRM subsystem searches the local license store for a license that grants the appropriate right.</span></span> <span data-ttu-id="1d6fb-121">Si aucune licence n’est trouvée, l’application peut en acquérir une en fonction des informations stockées dans l’en-tête DRM du fichier.</span><span class="sxs-lookup"><span data-stu-id="1d6fb-121">If no license is found, the application can acquire one based on information stored in the DRM header of the file.</span></span>

<span data-ttu-id="1d6fb-122">Plusieurs licences peuvent être émises pour le même fichier protégé.</span><span class="sxs-lookup"><span data-stu-id="1d6fb-122">Multiple licenses can be issued for the same protected file.</span></span> <span data-ttu-id="1d6fb-123">Lorsque le sous-système DRM détermine si une action est autorisée, il agrège les droits de toutes les licences qui s’appliquent.</span><span class="sxs-lookup"><span data-stu-id="1d6fb-123">When the DRM subsystem determines whether an action is allowed, it aggregates the rights from all licenses that apply.</span></span> <span data-ttu-id="1d6fb-124">Une priorité peut être affectée à chaque licence.</span><span class="sxs-lookup"><span data-stu-id="1d6fb-124">Each license can be assigned a priority.</span></span> <span data-ttu-id="1d6fb-125">Si plusieurs licences s’appliquent à une action, la licence dont la priorité est la plus élevée est vérifiée pour déterminer si les nombres doivent être décrémentée.</span><span class="sxs-lookup"><span data-stu-id="1d6fb-125">If more than one license applies to an action, the highest priority license is checked to determine whether counts need to be decremented.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1d6fb-126">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="1d6fb-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1d6fb-127">**Concepts**</span><span class="sxs-lookup"><span data-stu-id="1d6fb-127">**Concepts**</span></span>](drmconcepts.md)
</dt> </dl>

 

 




