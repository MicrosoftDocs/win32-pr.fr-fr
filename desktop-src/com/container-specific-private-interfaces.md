---
title: Interfaces privées Container-Specific
description: Interfaces privées Container-Specific
ms.assetid: 429cf71c-9b9d-4d0b-b5de-91fbe1dde3cf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25c6569a79e9f1801c6fd82543bc40408903c780
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311299"
---
# <a name="container-specific-private-interfaces"></a><span data-ttu-id="78bfa-103">Interfaces privées Container-Specific</span><span class="sxs-lookup"><span data-stu-id="78bfa-103">Container-Specific Private Interfaces</span></span>

<span data-ttu-id="78bfa-104">Certains conteneurs fournissent des interfaces privées spécifiques au conteneur pour des fonctionnalités supplémentaires ou des performances améliorées.</span><span class="sxs-lookup"><span data-stu-id="78bfa-104">Some containers provide container-specific private interfaces for additional functionality or improved performance.</span></span> <span data-ttu-id="78bfa-105">Les contrôles qui reposent sur ces interfaces spécifiques au conteneur doivent, si possible, travailler sans ces interfaces spécifiques au conteneur pour que le contrôle fonctionne dans différents conteneurs.</span><span class="sxs-lookup"><span data-stu-id="78bfa-105">Controls that rely on those container-specific interfaces should, if possible, work without those container-specific interfaces present so that the control functions in different containers.</span></span> <span data-ttu-id="78bfa-106">Par exemple, Visual Basic implémente des interfaces privées qui fournissent des fonctionnalités de mise en forme de chaînes aux contrôles.</span><span class="sxs-lookup"><span data-stu-id="78bfa-106">For example, Visual Basic implements private interfaces that provide string formatting functionality to controls.</span></span> <span data-ttu-id="78bfa-107">Si un contrôle utilise ces interfaces de mise en forme privée, il doit pouvoir s’exécuter avec la prise en charge de la mise en forme par défaut si ces interfaces ne sont pas disponibles.</span><span class="sxs-lookup"><span data-stu-id="78bfa-107">If a control makes use of these private formatting interfaces, it should be able to run with default formatting support if these interfaces are not available.</span></span> <span data-ttu-id="78bfa-108">Si le contrôle peut fonctionner sans les interfaces privées, il doit prendre les mesures appropriées (par exemple, avertir l’utilisateur de fonctionnalités réduites) tout en continuant à fonctionner.</span><span class="sxs-lookup"><span data-stu-id="78bfa-108">If the control can function without the private interfaces, it should take appropriate action (such as warn the user of reduced functionality) but continue to work.</span></span> <span data-ttu-id="78bfa-109">Si ce n’est pas le cas, une catégorie de composant doit être inscrite en fonction des besoins afin que seuls les conteneurs prenant en charge cette fonctionnalité puissent héberger ces contrôles.</span><span class="sxs-lookup"><span data-stu-id="78bfa-109">If this is not an option, a component category should be registered as required so that only containers supporting this functionality can host these controls.</span></span>

 

 




