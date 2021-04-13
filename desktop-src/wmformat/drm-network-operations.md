---
title: Opérations de réseau DRM
description: Opérations de réseau DRM
ms.assetid: 4a10c811-2aa1-4b97-8a72-61e8b04075a8
keywords:
- SDK Windows Media format, opérations de réseau DRM
- ASF (Advanced Systems Format), opérations de réseau DRM
- ASF (format de systèmes avancés), opérations de réseau DRM
- gestion des droits numériques (DRM), opérations réseau
- DRM (gestion des droits numériques), opérations réseau
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 875186e43e066d71847da014468e9b1764b60cf2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309386"
---
# <a name="drm-network-operations"></a><span data-ttu-id="6f242-108">Opérations de réseau DRM</span><span class="sxs-lookup"><span data-stu-id="6f242-108">DRM Network Operations</span></span>

<span data-ttu-id="6f242-109">Plusieurs opérations DRM requièrent que votre application se connecte à un service s’exécutant sur un réseau.</span><span class="sxs-lookup"><span data-stu-id="6f242-109">Several DRM-related operations require your application to connect to a service running on a network.</span></span> <span data-ttu-id="6f242-110">Ces opérations incluent l’individualisation, l’acquisition de licence, la révocation de licence et la sauvegarde et la restauration de licence.</span><span class="sxs-lookup"><span data-stu-id="6f242-110">These operations include individualization, license acquisition, license revocation, and license backup and restoration.</span></span>

<span data-ttu-id="6f242-111">Comme pour toute transaction réseau, votre application doit prendre en compte de nombreuses difficultés lors de l’inclusion de fonctionnalités nécessitant des opérations réseau.</span><span class="sxs-lookup"><span data-stu-id="6f242-111">As with any network transaction, your application should account for a variety of difficulties when including features that require network operations.</span></span> <span data-ttu-id="6f242-112">Votre application doit suivre l’état de l’opération dans l’étendue qui est possible pour la fonctionnalité spécifique, généralement en gérant les messages d’État.</span><span class="sxs-lookup"><span data-stu-id="6f242-112">Your application should track the status of the operation to whatever extent is possible for the specific feature, usually by handling status messages.</span></span> <span data-ttu-id="6f242-113">Vous devez fournir des commentaires à l’utilisateur sur l’État.</span><span class="sxs-lookup"><span data-stu-id="6f242-113">You should provide feedback to the user about status.</span></span> <span data-ttu-id="6f242-114">Si une opération échoue à la première tentative, vous devez permettre à l’utilisateur de réessayer.</span><span class="sxs-lookup"><span data-stu-id="6f242-114">If an operation fails on the first try, you should give the user the opportunity to retry.</span></span> <span data-ttu-id="6f242-115">Dans de nombreux cas, la première tentative rencontre des difficultés, mais une tentative suivante se termine sans erreur.</span><span class="sxs-lookup"><span data-stu-id="6f242-115">In many cases, the first attempt encounters difficulty, but a subsequent try completes without error.</span></span>

> [!Note]  
> <span data-ttu-id="6f242-116">DRM n’est pas pris en charge par la version x64 de ce kit de développement logiciel (SDK).</span><span class="sxs-lookup"><span data-stu-id="6f242-116">DRM is not supported by the x64-based version of this SDK.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="6f242-117">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="6f242-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6f242-118">**Activation de la prise en charge de DRM**</span><span class="sxs-lookup"><span data-stu-id="6f242-118">**Enabling DRM Support**</span></span>](enabling-drm-support.md)
</dt> </dl>

 

 




