---
title: Type de démarrage BITS
description: Le type de démarrage pour BITS est retardé automatiquement. Avant Windows Vista, le type de démarrage pour BITS est manuel. Quand une tâche BITS est créée, le type de démarrage passe à automatique. Le type de démarrage revient à manuel lorsque toutes les tâches sont terminées ou annulées.
ms.assetid: 0d9ec60f-3488-4eb2-a6a2-22932fd74caf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd1ce1dcd2f939237142a0afd44e49b4b63df419
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104379629"
---
# <a name="bits-startup-type"></a><span data-ttu-id="e1d9a-106">Type de démarrage BITS</span><span class="sxs-lookup"><span data-stu-id="e1d9a-106">BITS Startup Type</span></span>

<span data-ttu-id="e1d9a-107">Le **type de démarrage** pour bits est le démarrage automatique différé (s’il y a des travaux en bits actifs) ou le démarrage à la demande (s’il n’y a pas de travaux actifs).</span><span class="sxs-lookup"><span data-stu-id="e1d9a-107">The **Startup Type** for BITS is delayed auto-start (if there are active BITS jobs) or demand start (if there are no active jobs).</span></span> <span data-ttu-id="e1d9a-108">Les versions de Windows antérieures à la mise à jour de novembre utilisaient uniquement le type de démarrage à démarrage automatique retardé ; les versions antérieures à Vista utilisaient le type de démarrage manuel.</span><span class="sxs-lookup"><span data-stu-id="e1d9a-108">Versions of Windows prior to the November Update used only the delayed auto-start startup type; versions prior to Vista used the manual startup type.</span></span>

<span data-ttu-id="e1d9a-109">Vous ne devez pas définir le **type de démarrage** sur désactivé.</span><span class="sxs-lookup"><span data-stu-id="e1d9a-109">You should not set the **Startup Type** to Disabled.</span></span> <span data-ttu-id="e1d9a-110">La désactivation du service BITS peut perturber les applications qui reposent sur BITS pour transférer des fichiers.</span><span class="sxs-lookup"><span data-stu-id="e1d9a-110">Disabling BITS may break applications that rely on BITS to transfer files.</span></span>

 

 




