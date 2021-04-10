---
title: Appels imbriqués à SRSetRestorePoint
description: Cette rubrique décrit la prise en charge des appels imbriqués à SRSetRestorePoint par le biais des types d’événements de modification de système imbriqué de début \_ \_ et de fin de modification de \_ \_ \_ système imbriqué \_ .
ms.assetid: ee2dea47-f95d-4293-ac33-eff622b84db6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5654dc7bb6e42ae55cbad18fc2418df3bdd942d2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104196877"
---
# <a name="nested-calls-to-srsetrestorepoint"></a><span data-ttu-id="e0a38-103">Appels imbriqués à SRSetRestorePoint</span><span class="sxs-lookup"><span data-stu-id="e0a38-103">Nested Calls to SRSetRestorePoint</span></span>

<span data-ttu-id="e0a38-104">Cette rubrique décrit la prise en charge des appels imbriqués à [**SRSetRestorePoint**](/windows/desktop/api/SRRestorePtAPI/nf-srrestoreptapi-srsetrestorepointa) par le biais des types d’événements de modification de système imbriqué de début \_ et de fin de modification de \_ \_ \_ \_ système imbriqué \_ .</span><span class="sxs-lookup"><span data-stu-id="e0a38-104">This topic describes support for nested calls to [**SRSetRestorePoint**](/windows/desktop/api/SRRestorePtAPI/nf-srrestoreptapi-srsetrestorepointa) through the BEGIN\_NESTED\_SYSTEM\_CHANGE and END\_NESTED\_SYSTEM\_CHANGE event types.</span></span>

<span data-ttu-id="e0a38-105">Les applications peuvent appeler [**SRSetRestorePoint**](/windows/desktop/api/SRRestorePtAPI/nf-srrestoreptapi-srsetrestorepointa) en toute sécurité lors de l’utilisation de ces types d’événements.</span><span class="sxs-lookup"><span data-stu-id="e0a38-105">Applications can safely call [**SRSetRestorePoint**](/windows/desktop/api/SRRestorePtAPI/nf-srrestoreptapi-srsetrestorepointa) when using these event types.</span></span> <span data-ttu-id="e0a38-106">Le premier appel à la fonction crée un point de restauration.</span><span class="sxs-lookup"><span data-stu-id="e0a38-106">The first call to the function creates a restore point.</span></span> <span data-ttu-id="e0a38-107">Les appels imbriqués suivants à la fonction ne créent pas de points de restauration.</span><span class="sxs-lookup"><span data-stu-id="e0a38-107">Subsequent nested calls to the function do not create restore points.</span></span> <span data-ttu-id="e0a38-108">Supposons, par exemple, qu’une application effectue les appels suivants à **SRSetRestorePoint**:</span><span class="sxs-lookup"><span data-stu-id="e0a38-108">For example, suppose an application makes the following calls to **SRSetRestorePoint**:</span></span><dl> <span data-ttu-id="e0a38-109">Pour le point de restauration A avec dwEventType = BEGIN \_ Nested \_ System \_ change</span><span class="sxs-lookup"><span data-stu-id="e0a38-109">For restore point A with dwEventType = BEGIN\_NESTED\_SYSTEM\_CHANGE</span></span>  
<span data-ttu-id="e0a38-110">Pour le point de restauration B avec dwEventType = BEGIN la \_ \_ modification du système imbriqué \_</span><span class="sxs-lookup"><span data-stu-id="e0a38-110">For restore point B with dwEventType = BEGIN\_NESTED\_SYSTEM\_CHANGE</span></span>  
<span data-ttu-id="e0a38-111">Pour le point de restauration B avec dwEventType = fin de la \_ \_ modification du système imbriqué \_</span><span class="sxs-lookup"><span data-stu-id="e0a38-111">For restore point B with dwEventType = END\_NESTED\_SYSTEM\_CHANGE</span></span>  
<span data-ttu-id="e0a38-112">Pour le point de restauration A avec dwEventType = fin de la \_ \_ modification du système imbriqué \_</span><span class="sxs-lookup"><span data-stu-id="e0a38-112">For restore point A with dwEventType = END\_NESTED\_SYSTEM\_CHANGE</span></span>  
</dl>

<span data-ttu-id="e0a38-113">Le deuxième appel ne crée pas de point de restauration, car l’appel est imbriqué.</span><span class="sxs-lookup"><span data-stu-id="e0a38-113">The second call does not create a new restore point because the call is nested.</span></span>

 

 




